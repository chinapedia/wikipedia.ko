> This article is converted from Wikipedia: [모듈:MTR](https://ko.wikipedia.org/wiki/모듈:MTR).


\-- This module implements , ,  and .

local getArgs = require('Module:Arguments').getArgs local data = mw.loadData('Module:MTR/data')

local p = {}

local function makeInvokeFunction(funcName)

`   -- makes a function that can be returned from #invoke, using`
`   -- `[`Module:Arguments`](https://ko.wikipedia.org/wiki/Module:Arguments "wikilink")`.`
`   return function (frame)`
`       local args = getArgs(frame, {parentOnly = true})`
`       return p[funcName](args)`
`   end`

end

local function getColor(code)

`   return data.colors[code] or '000'`

end

local function getTextcolor(code)

`   return data.textcolors[code] or '000'`

end

p.colorbyname = makeInvokeFunction('_colorbyname')

function p._colorbyname(args)

`   local code = args[1] or ''`
`   code = code:upper()`
`   return getColor(code)`

end

local function getLink(code)

`   local name = data.names[code]`
`   link = name`
`   if data.link[name] then`
`       link = data.link[name]`
`   elseif data.needs_dab[name] then`
`       link = link .. ' (홍콩)'`
`   elseif data.lr[name] then`
`       link = '홍콩 경전철 ' .. link .. '선'`
`   end`
`   return link`

end

local function invalid(code)

`   return '`<strong class="error">`Error: "' .. tostring(code) .. '" 은(는) 유효한 코드가 아닙니다.`</strong>`'`

end

p.link = makeInvokeFunction('_link')

function p._link(args)

`   -- Retrieve arguments`
`   local code = args[1] or ''`
`   code = code:upper() -- Convert to upper case`
`   if not code then`
`       return invalid(code)`
`   end`
`   return getLink(code)`

end

p.icon = makeInvokeFunction('_icon')

function p._icon(args)

`   local code = args[1] or ''`
`   local link = args[2] or args.link`
`   local text = args[3] or args.text`
`   code = code:upper()`
`   local color = getColor(code)`
`   link = link or getLink(code)`
`   local name = data.names[code]`
`   if not name then`
`       return invalid(code)`
`   end`

`   -- Format the text`
`   if text == noint then`
`       text = name`
`   else`
`       text = text or name .. '환승역'`
`   end`
`   -- Build the link`
`   local lr = data.lr[code]`
`   if lr then`
`       local textcolor = getTextcolor(code)`
`       if link ~= '' then return '`<span style="background-color:#' .. color .. '; border:1px solid #' .. color .. ';">` `[<span style="color:#' .. textcolor .. '; font-weight:bold; font-size:inherit; white-space:nowrap;">`'``   ``..``   ``name``   ``..``   ``'`</span>](https://ko.wikipedia.org/wiki/'.._link_..' "wikilink")` `</span>`' end`
`       return '`<span style="background-color:#' .. color .. '; border:1px solid #' .. color .. ';">` `<span style="color:#' .. textcolor .. '; font-weight:bold; font-size:inherit; white-space:nowrap;">`' .. name .. '`</span>` `</span>`'`
`   else`
`       return '`[<span title="' .. text .. '" style="background-color:#' .. color .. '; border:1px solid #000; text-align:center;">`    `</span>](https://ko.wikipedia.org/wiki/'_.._link_.._' "wikilink")`'`
`   end`

end

p.line = makeInvokeFunction('_line')

function p._line(args)

`   local code = args[1] or ''`
`   local link = args[2] or args.link`
`   local text = args[3] or args.text`
`   code = code:upper()`
`   link = link or getLink(code)`
`   local name = data.names[code]`
`   if not name then`
`       return invalid(code)`
`   end`
`   text = text or name`
`   if link ~= '' then return '`[`'``   ``..``   ``text``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._link_.._' "wikilink")`' end`
`   return text`

end

p.box = makeInvokeFunction('_box')

function p._box(args)

`   local code = args[1] or ''`
`   local link = args[2] or args.link`
`   local text = args[3] or args.text`
`   code = code:upper()`
`   local color = getColor(code)`
`   link = link or getLink(code)`
`   local name = data.names[code]`
`   if not name then`
`       return invalid(code)`
`   end`
`   text = text or name`
`   if link ~= '' then return '`<span title="' .. text .. '" style="background-color:#' .. color .. '; border:1px solid #000; text-align:center;">`    `</span>` `[`'``   ``..``   ``text``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._link_.._' "wikilink")`' end`
`   return '`<span title="' .. text .. '" style="background-color:#' .. color .. '; border:1px solid #000; text-align:center;">`    `</span>` '..text`

end

p.box1 = makeInvokeFunction('_box1')

function p._box1(args)

`   local code = args[1] or ''`
`   local link = args[2] or args.link`
`   local text = args[3] or args.text`
`   code = code:upper()`
`   local color = getColor(code)`
`   link = link or getLink(code)`
`   local name = data.names[code]`
`   if not name then`
`       return invalid(code)`
`   end`
`   text = text or name`

`   return '`<span style="display:inline-block; width:1.5em; height:1.5em; margin:1px 0; border:1px solid #000; background-color:#' .. color .. '; text-align:center;">` `</span>` `[`'``   ``..``   ``text``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._link_.._' "wikilink")`'`

end

return p