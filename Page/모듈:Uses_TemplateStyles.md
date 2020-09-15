> This article is converted from Wikipedia: [모듈:Uses TemplateStyles](https://ko.wikipedia.org/wiki/모듈:Uses_TemplateStyles).


\-- This module implements the  template. local yesno = require('Module:Yesno') local mList = require('Module:List') local mTableTools = require('Module:TableTools') local mMessageBox = require('Module:Message box')

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

`   local tStyles = mTableTools.compressSparseArray(args)`
`   local box = p.renderBox(tStyles)`
`   local trackingCategories = p.renderTrackingCategories(args, tStyles)`
`   return box .. trackingCategories`

end

function p.renderBox(tStyles)

`   local boxArgs = {}`
`   if #tStyles < 1 then`
`       boxArgs.text = '`<strong class="error">`Error: no TemplateStyles specified`</strong>`'`
`   else`
`       local tStylesLinks = {}`
`       for i, ts in ipairs(tStyles) do`
`           local sandboxLink = nil`
`           local tsTitle = mw.title.new(ts)`
`           if tsTitle then`
`               local tsSandboxTitle = mw.title.new(string.format('%s:%s/sandbox/%s', tsTitle.nsText, tsTitle.baseText, tsTitle.subpageText))`
`               if tsSandboxTitle and tsSandboxTitle.exists then`
`                   sandboxLink = string.format(' (`[`sandbox`](https://ko.wikipedia.org/wiki/:%s "wikilink")`)', tsSandboxTitle.prefixedText)`
`               end`
`           end`
`           tStylesLinks[i] = string.format('`[`:%s`](https://ko.wikipedia.org/wiki/:%s "wikilink")`%s', ts, sandboxLink or '')`
`       end`
`       local tStylesList = mList.makeList('bulleted', tStylesLinks)`
`       boxArgs.text = '이 ' .. `
`           (mw.title.getCurrentTitle():inNamespaces(828,829) and '모듈' or '틀') ..`
`           '은 `[`틀스타일을`](../Page/위키백과:틀스타일.md "wikilink")` 사용합니다:\n' .. tStylesList`
`   end`
`   boxArgs.type = 'notice'`
`   boxArgs.small = true`
`   boxArgs.image = '`[`Farm-Fresh_css_add.svg`](https://ko.wikipedia.org/wiki/File:Farm-Fresh_css_add.svg "fig:Farm-Fresh_css_add.svg")`'`
`   return mMessageBox.main('mbox', boxArgs)`

end

function p.renderTrackingCategories(args, tStyles, titleObj)

`   if yesno(args.nocat) then`
`       return ''`
`   end`
`   `
`   local cats = {}`
`   `
`   -- Error category`
`   if #tStyles < 1 then`
`       --cats[#cats + 1] = 'Uses TemplateStyles templates with errors'`
`   end`
`   `
`   -- TemplateStyles category`
`   titleObj = titleObj or mw.title.getCurrentTitle()`
`   local subpageBlacklist = {`
`       ['설명문서'] = true,`
`       ['연습장'] = true,`
`       ['연습장2'] = true,`
`       ['시험장'] = true`
`   }`
`   if (titleObj.namespace == 10 or titleObj.namespace == 828)`
`       and not subpageBlacklist[titleObj.subpageText]`
`   then`
`       local category = args.category`
`       if not category then`
`           category = category or '틀스타일을 사용하는 틀'`
`       end`
`       cats[#cats + 1] = category`
`       if not yesno(args.noprotcat) then`
`           local currentProt = titleObj.protectionLevels["edit"] and titleObj.protectionLevels["edit"][1] or nil`
`           local addedLevelCat = false`
`           local addedPadlockCat = false`
`           for i, ts in ipairs(tStyles) do`
`               local tsTitleObj = mw.title.new(ts)`
`               local tsProt = tsTitleObj.protectionLevels["edit"] and tsTitleObj.protectionLevels["edit"][1] or nil`
`               if tsProt ~= currentProt and not addedLevelCat then`
`                   --cats[#cats + 1] = "Templates using TemplateStyles with a different protection level"`
`               end`
`               if tsProt and not addedPadlockCat then`
`                   local content = tsTitleObj:getContent()`
`                   if not `<content:find>`("{{pp-") then`
`                       --cats[#cats + 1] = "Templates using TemplateStyles without padlocks"`
`                       addedPadlockCat = true`
`                   end`
`               end`
`           end`
`       end`
`   end`
`   for i, cat in ipairs(cats) do`
`       cats[i] = string.format('`[`분류:%s`](https://ko.wikipedia.org/wiki/분류:%s "wikilink")`', cat)`
`   end`
`   return table.concat(cats)`

end

return p