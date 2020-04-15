> This article is converted from Wikipedia: [모듈:IPA symbol](https://ko.wikipedia.org/wiki/모듈:IPA_symbol).


local p, __output, args, data = {}, {}, {}, mw.loadData("Module:IPA symbol/data") local id, output

__output.name = function() return data.correspondences\[id\]\["name"\] end __output.wikipage = function() return data.correspondences\[id\]\["wikipage"\] end __output.soundfile = function() return data.correspondences\[id\]\["soundfile"\] end __output.type = function() return data.correspondences\[id\]\["type"\] end

local function html_error(message)

` if args[2] then`
`   return args[2]`
` else`
`   return mw.ustring.format(`
`     '`<strong class="error">`{{`[`IPA``   ``기호`](https://ko.wikipedia.org/wiki/틀:IPA_기호 "wikilink")`}} 사용 중 오류가 발생했습니다: %s%s`</strong>`'`
`     ,message`
`     ,mw.title.getCurrentTitle().isContentPage and ("[[분류:관심이_필요한_IPA_문서|" .. (args[1] or "") .. "]]") or ""`
`    )`
` end`

end

function p.main(frame)

` -- all input is trimmed; accepted parameters are:`
` --   name              description`
` --   ====              ===========`
` --   (1)               the input`
` --   (2)               overwrite the error message`
` --   (3)               overwrite the output when input is empty`
` --   output            the output, one of: input; name; wikipage; soundfile; type`

` for k, v in pairs(frame:getParent().args) do`
`   args[k] = v and mw.text.trim(v)`
` end`
` args.output = args.output or 'wikipage'`

` if not args[1] or args[1] == "" then return args[3] or "" end`

` id = data.symbols[args[1]]`
` if not id then return html_error('"' .. args[1] .. '" 항목이 목록에 없습니다') end`

` return  __output[args.output] and __output[args.output]() or html_error("해당 출력 옵션이 없습니다")`

end

return p