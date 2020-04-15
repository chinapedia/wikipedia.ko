> This article is converted from Wikipedia: [모듈:Random portal component](https://ko.wikipedia.org/wiki/모듈:Random_portal_component).


\-- This module implements [Template:Random portal component](https://ko.wikipedia.org/wiki/Template:Random_portal_component "wikilink")

local p = {}

local mRandom = require('Module:Random') local currentTitle = mw.title.getCurrentTitle()

local function getRandomNumber(max)

`   -- gets a random integer between 1 and max; max defaults to 1`
`   return mRandom.number{max or 1}`

end

local function expandArg(args, key)

`   -- Emulate how unspecified template parameters appear in wikitext. If the`
`   -- specified argument exists, its value is returned, and if not the argument`
`   -- name is returned inside triple curly braces.`
`   local val = args[key]`
`   if val then`
`       return val`
`   else`
`       return string.format('``', key)`
`   end`

end

local function getPages(args)

`   local pages = {}`
`   pages.root = args.rootpage or currentTitle.prefixedText`
`   pages.subpage = pages.root .. '/' .. expandArg(args, 'subpage')`
`   pages.random = pages.subpage .. '/' .. getRandomNumber(args.max)`
`   return pages`

end

local function tryExpandTemplate(frame, title, args)

`   local success, result = pcall(frame.expandTemplate, frame, {title = title, args = args})`
`   if success then`
`       return result`
`   else`
`       local msg = string.format(`
`           '`<strong class="error">`The page "`[`%s`](https://ko.wikipedia.org/wiki/%s "wikilink")`" does not exist.`</strong>`',`
`           title`
`       )`
`       if mw.title.getCurrentTitle().namespace == 100 then -- is in the portal namespace`
`           msg = msg .. ''`
`       end`
`       return msg`
`   end`

end

local function getHeader(frame, pages, header)

`   return tryExpandTemplate(`
`       frame,`
`       pages.root .. '/박스 머리말',`
`       {header, pages.random}`
`   )`

end

local function getRandomSubpageContent(frame, pages)

`   return tryExpandTemplate(`
`       frame,`
`       pages.random`
`   )`

end

local function getFooter(frame, pages, link)

`   return tryExpandTemplate(`
`       frame,`
`       pages.root .. '/박스 꼬리말',`
`       {link}`
`   )`

end

function p._main(args, frame)

`   frame = frame or mw.getCurrentFrame()`
`   local pages = getPages(args)`

`   local ret = {}`
`   ret[#ret + 1] = getHeader(frame, pages, args.header or 'subpage')`
`   ret[#ret + 1] = getRandomSubpageContent(frame, pages)`
`   if not args.footer or not args.footer:find('%S') then`
`       ret[#ret + 1] = '`

<div style="clear:both;">

</div>

</div>

'

`   else`
`       ret[#ret + 1] = getFooter(frame, pages, string.format(`
`           '`[`%s`](https://ko.wikipedia.org/wiki/%s "wikilink")`',`
`           pages.subpage,`
`           expandArg(args, 'footer')`
`       ))`
`   end`

`   return table.concat(ret, '\n')`

end

function p._nominate(args, frame)

`   frame = frame or mw.getCurrentFrame()`
`   local pages = getPages(args)`
`   `
`   local ret = {}`
`   ret[#ret + 1] = getHeader(frame, pages, expandArg(args, 'header'))`
`   ret[#ret + 1] = getRandomSubpageContent(frame, pages)`
`   ret[#ret + 1] = getFooter(frame, pages, string.format(`
`       '`[`Suggest`](https://ko.wikipedia.org/wiki/모듈:Random_portal_component/Nominate/%s "wikilink")` • `[`%s`](https://ko.wikipedia.org/wiki/%s "wikilink")` ',`
`       expandArg(args, 'subpage'),`
`       pages.subpage,`
`       args.footer or 'Archive'`
`   ))`

`   return table.concat(ret, '\n')`

end

local function makeInvokeFunction(func)

`   return function (frame)`
`       local args = require('Module:Arguments').getArgs(frame, {`
`           trim = false,`
`           removeBlanks = false,`
`           wrappers = {`
`               'Template:Random portal component',`
`               'Template:Random portal component with nominate'`
`           }`
`       })`
`       return func(args, frame)`
`   end`

end

p.main = makeInvokeFunction(p._main) p.nominate = makeInvokeFunction(p._nominate)

return p

[Category:Portals_needing_attention](https://ko.wikipedia.org/wiki/Category:Portals_needing_attention "wikilink")