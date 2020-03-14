> This article is converted from Wikipedia: [:Lua banner](https://ko.wikipedia.org/wiki/:Lua_banner).


\-- This module implements the  template.

local yesno = require('Module:Yesno') local mList = require('Module:List') local mTableTools = require('Module:TableTools') local mMessageBox = require('Module:Message box')

local p = {}

function p.main(frame)

`   local origArgs = frame:getParent().args`
`   local args = {}`
`   for k, v in pairs(origArgs) do`
`       v = v:match('^%s*(.-)%s*$')`
`       if v ~= '' then`
`           args[k] = v`
`       end`
`   end`
`   return p._main(args)`

end

function p._main(args)

`   local modules = mTableTools.compressSparseArray(args)`
`   local box = p.renderBox(modules)`
`   local trackingCategories = p.renderTrackingCategories(args, modules)`
`   return box .. trackingCategories`

end

function p.renderBox(modules)

`   local boxArgs = {}`
`   if #modules < 1 then`
`       boxArgs.text = '`<strong class="error">`오류: 모듈이 명시되지 않았습니다`</strong>`'`
`   else`
`       local moduleLinks = {}`
`       for i, module in ipairs(modules) do`
`           moduleLinks[i] = string.format('`[`:%s`](https://ko.wikipedia.org/wiki/:%s "wikilink")`', module)`
`       end`
`       local moduleList = mList.makeList('bulleted', moduleLinks)`
`       boxArgs.text = '`[`루아`](https://ko.wikipedia.org/wiki/위키백과:루아 "wikilink")` 사용:\n' .. moduleList`
`   end`
`   boxArgs.type = 'notice'`
`   boxArgs.small = true`
`   boxArgs.image = '`[`Lua-logo-nolabel.svg`](https://ko.wikipedia.org/wiki/File:Lua-logo-nolabel.svg "fig:Lua-logo-nolabel.svg")`'`
`   return mMessageBox.main('mbox', boxArgs)`

end

function p.renderTrackingCategories(args, modules, titleObj)

`   if yesno(args.nocat) then`
`       return ''`
`   end`
`   `
`   local cats = {}`
`   `
`   -- Error category`
`   if #modules < 1 then`
`       cats[#cats + 1] = 'Lua templates with errors'`
`   end`
`   `
`   -- Lua templates category`
`   titleObj = titleObj or mw.title.getCurrentTitle()`
`   local subpageBlacklist = {`
`       doc = true,`
`       sandbox = true,`
`       sandbox2 = true,`
`       testcases = true,`
`       ['설명문서'] = true,`
`       ['연습장']= true,`
`       ['시험장'] = true`
`   }`
`   if titleObj.namespace == 10 `
`       and not subpageBlacklist[titleObj.subpageText]`
`   then`
`       local category = args.category`
`       if not category then`
`           local categories = {`
`               ['모듈:String'] = '루아 String 틀',`
`               ['모듈:Math'] = '루아 Math 틀',`
`               ['모듈:Hangul'] = '루아 Hangul 틀',`
`               ['모듈:BaseConvert'] = '루아 BaseConvert 틀',`
`               ['모듈:Citation'] = '루아 Citation 틀'`
`           }`
`           categories['모듈:Citation/CS1'] = categories['모듈:Citation']`
`           category = modules[1] and categories[modules[1]]`
`           category = category or '루아 틀'`
`       end`
`       cats[#cats + 1] = category`
`   end`
`   `
`   for i, cat in ipairs(cats) do`
`       cats[i] = string.format('`[`분류:%s`](https://ko.wikipedia.org/wiki/분류:%s "wikilink")`', cat)`
`   end`
`   return table.concat(cats)`

end

return p