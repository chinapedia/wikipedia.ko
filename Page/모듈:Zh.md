> This article is converted from Wikipedia: [모듈:Zh](https://ko.wikipedia.org/wiki/모듈:Zh).


require("Module:No globals")

local p = {} local getArgs = require("Module:Arguments").getArgs -- 변수 처리를 단순화하는 함수

local function intersects(lst, mst)

`   -- 겹침 여부 판단`
`   for key in pairs(mst) do`
`       if lst[key] then`
`           return true`
`       end`
`   end`
`   return false`

end

local function alias(args, p, hp)

`   -- 동명 변수 처리`
`   if not args[p] and args[hp] then`
`       args[p] = args[hp]`
`   end`

end

local function setpref(args, order, orderlists)

`   if args[order] and orderlists[args[order]] then`
`       return orderlists[args[order]]`
`   end`
`   return orderlists["default"]`

end

function p.zh(frame)

`   local args = getArgs(frame)`
`   local title = mw.title.getCurrentTitle()`
`   local zhdatalang = mw.loadData("Module:Zh/data/" .. args["lang"])`
`   local labelslist = zhdatalang.labelslist -- 각 부분에 표시할 라벨들`
`   local articles = zhdatalang.articles -- 각 부분에 링크 걸 문서들`
`   local ipalangs = zhdatalang.ipalangs -- 각 IPA가 표시하는 발음의 언어들`
`   local isocodes = zhdatalang.isocodes -- 각 부분의 ISO 코드들`
`   local cats = zhdatalang.cats -- 각 부분에 붙일 분류들`

`   local pinyins = zhdatalang.pinyins -- 병음 여부`
`   local hanguls = zhdatalang.hanguls -- 한글 여부`
`   local superscript = zhdatalang.superscript -- 자동 위 첨자 여부`
`   local prefix = zhdatalang.prefix -- 접두어 부착 여부`
`   local ignorefirst = zhdatalang.ignorefirst`
`   local savefirst = zhdatalang.savefirst`

`   local delims = zhdatalang.delims -- 일반 구분자들`
`   local hanguldelims = zhdatalang.hanguldelims -- 한글 표기 앞의 구분자`
`   local orderlists = zhdatalang.orderlists -- 각 부분이 표시되는 순서`

`   -- change parameters and specify labels based on other parameters`
`   local labels = labelslist[1]`
`   if labels["p"] and intersects(args, pinyins) then`
`       labels = labelslist[2]`
`   end`
`   if args["s"] and args["s"] == args["t"] then`
`       -- 일치하는 간번체자 병합`
`       args["c"] = args["s"]`
`       args["s"] = nil`
`       args["t"] = nil`
`   end`
`   alias(args, "p", "hp")`
`   alias(args, savefirst, 1)`
`   if intersects(args, ignorefirst) then`
`       -- 대체 가능한 주 변수 제거`
`       args[savefirst] = nil`
`   end`

`   local body = "" -- 출력 문자열`
`   local params -- HTML span을 위한 변수`
`   local label -- 텍스트 앞에 붙는 언어 라벨`
`   local val -- 텍스트`

`   local uselinks = not (args["links"] == "no") -- 라벨 링크 추가 여부`
`   local uselabels = not (args["labels"] == "no") -- 라벨 표시 여부`
`   local useprefix = not (args["prefix"] == "no") -- 맨 앞에 언어 이름 부착 여부`
`   local usesmall = not (args["small"] == "no") -- 언어 라벨 작게 하기 여부`

`   local delim = setpref(args, "delim", delims)`
`   local hanguldelim = setpref(args, "delim", hanguldelims)`
`   local orderlist = setpref(args, "order", orderlists)`
`   `
`   -- go through all possible fields in loop, adding them to the output`
`   for i, part in ipairs(orderlist) do`
`       if args[part] then`
`           -- build label`
`           label = ""`
`           if uselabels then`
`               label = labels[part]`
`               if (uselinks and articles[part]) or hanguls[part] then`
`                   label = "[["_.._articles[part]_.._"|" .. label .. "]]"`
`               end`
`               if ipalangs[part] then`
`                   if uselinks then`
`                       label = label .. "([["_.._ipalangs[part]_.._"|" .. ipalangs[part] .. "]])"`
`                   else`
`                       label = label .. "(" .. ipalangs[part] .. ")"`
`                   end`
`               end`
`               if body == "" and useprefix and prefix[part] then`
`                   if uselinks then`
`                       label = "[["_.._labels[savefirst]_.._"|" .. labels[savefirst] .. "]] " .. label`
`                   else`
`                       label = labels[savefirst] .. " " .. label`
`                   end`
`               end`
`               if hanguls[part] then`
`                   label = "`<sup>`["``   ``..``   ``label``   ``..``   ``"]`</sup>`"`
`               else`
`                   label = label .. ": "`
`               end`
`               if usesmall and not hanguls[part] then`
`                   label = "`<small>`" .. label .. "`</small>`"`
`               end`
`           end`
`           -- build value`
`           val = args[part]`
`           if cats[part] and title.namespace == 0 then`
`               -- if has associated category AND current page in article namespace, add category`
`               val = cats[part] .. val`
`           end`
`           if isocodes[part] then`
`               -- add span for language if needed`
`               params = {["lang"] = isocodes[part], ["xml:lang"] = isocodes[part]}`
`               val = mw.text.tag({name = "span", attrs = params, content = val})`
`           elseif ipalangs[part] then`
`               params = {["class"] = "IPA"}`
`               val = mw.text.tag({name = "span", attrs = params, content = val})`
`           end`
`           if string.match(val, "`

</?sup>

") then

`               val = val .. "`[`분류:모듈``   ``zh에서``   ``태그``   ``sup를``   ``사용하는``   ``문서`](https://ko.wikipedia.org/wiki/분류:모듈_zh에서_태그_sup를_사용하는_문서 "wikilink")`"`
`           end`
`           if superscript[part] or ipalangs[part] then`
`               -- superscript`
`               val = mw.ustring.gsub(val, "([%d%*°]+)", "`<sup>`%1`</sup>`")`
`               val = mw.ustring.gsub(val, "`<sup><sup>`([%d%*°]+)`</sup></sup>`", "`<sup>`%1`</sup>`")`
`           end`
`           -- add both to body`
`           if body > "" then`
`               if hanguls[part] then`
`                   body = body .. hanguldelim`
`               else`
`                   body = body .. delim`
`               end`
`           end`
`           if not hanguls[part] then`
`               body = body .. label .. val`
`           elseif not usesmall then`
`               body = body .. val .. label`
`           else`
`               body = body .. "`<small>`" .. val .. label .. "`</small>`"`
`           end`
`       end`
`   end`
`   `
`   if delim == "\n|" then`
`       body = "|" .. body`
`   end`
`   `
`   return body`

end

return p