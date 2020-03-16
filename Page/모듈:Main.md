> This article is converted from Wikipedia: [:Main](https://ko.wikipedia.org/wiki/:Main).


\--[-- This module produces a link to a main article or articles. It implements the -- template {{main}}. -- -- If the module is used in category or category talk space, it produces "The -- main article for this category is xxx". Otherwise, it produces -- "Main article: xxx". --](https://ko.wikipedia.org/wiki/--_This_module_produces_a_link_to_a_main_article_or_articles._It_implements_the_--_template_{{main}}._--_--_If_the_module_is_used_in_category_or_category_talk_space,_it_produces_"The_--_main_article_for_this_category_is_xxx"._Otherwise,_it_produces_--_"Main_article:_xxx"._-- "wikilink")

local mHatnote = require('Module:Hatnote') local mHatlist = require('Module:Hatnote list') local mArguments -- lazily initialise local p = {}

function p.main(frame)

`   mArguments = require('Module:Arguments')`
`   local args = mArguments.getArgs(frame, {parentOnly = true})`
`   local pages = {}`
`   for k, v in pairs(args) do`
`       if type(k) == 'number' then`
`           local display = args['label ' .. k] or args['l' .. k]`
`           local page = display and`
`               string.format('%s|%s', string.gsub(v, '|.*$', ''), display) or v`
`           pages[#pages + 1] = page`
`       end`
`   end`
`   if #pages == 0 and mw.title.getCurrentTitle().namespace == 0 then`
`       return mHatnote.makeWikitextError(`
`           '문서 이름이 지정되지 않았음',`
`           '틀:본문#오류',`
`           args.category`
`       )`
`   end`
`   local options = {`
`       selfref = args.selfref`
`   }`
`   return p._main(pages, options)`

end

function p._main(args, options)

`   -- Get the list of pages. If no first page was specified we use the current`
`   -- page name.`
`   local currentTitle = mw.title.getCurrentTitle()`
`   if #args == 0 then args = {currentTitle.text} end`
`   local firstPage = string.gsub(args[1], '|.*$', '')`
`   -- Make the formatted link text`
`   list = mHatlist.andList(args, true)`
`   -- Build the text.`
`   local mainForm`
`   local curNs = currentTitle.namespace`
`   if (curNs == 14) or (curNs == 15) then --category/talk namespaces`
`       mainForm = '이 `[`분류의`](../Page/위키백과:분류.md "wikilink")` 본문은 %s입니다.'`
`   else`
`       mainForm = '이 부분의 본문은 %s입니다.'`
`   end`
`   mainForm = "`[`16px`](https://ko.wikipedia.org/wiki/파일:Crystal_Clear_app_xmag.svg "wikilink")`" .. mainForm`
`   local text = string.format(mainForm, list)`
`   -- Process the options and pass the text to the _rellink function in`
`   -- `[`Module:Hatnote`](https://ko.wikipedia.org/wiki/Module:Hatnote "wikilink")`.`
`   options = options or {}`
`   local hnOptions = {`
`       selfref = options.selfref`
`   }`
`   return mHatnote._hatnote(text, hnOptions)`

end

return p