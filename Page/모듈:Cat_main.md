> This article is converted from Wikipedia: [모듈:Cat main](https://ko.wikipedia.org/wiki/모듈:Cat_main).


\-- This module implements .

local mHatnote = require('Module:Hatnote') local yesno = require('Module:Yesno') local mTableTools -- lazily initialise local mArguments -- lazily initialise

local p = {}

function p.catMain(frame)

`   mTableTools = require('Module:TableTools')`
`   mArguments = require('Module:Arguments')`
`   local args = mArguments.getArgs(frame, {wrappers = '틀:분류 설명'})`
`   local pages = mTableTools.compressSparseArray(args)`
`   local options = {`
`       article = args.article,`
`       selfref = args.selfref`
`   }`
`   return p._catMain(options, unpack(pages))`

end

function p._catMain(options, ...)

`   options = options or {}`

`   -- Get the links table.`
`   local links = mHatnote.formatPages(...)`
`   if not links[1] then`
`       local page = mw.title.getCurrentTitle().text`
`       links[1] = mHatnote._formatLink(page)`
`   end`
`   for i, link in ipairs(links) do`
`       links[i] = string.format("`**`%s`**`", link)`
`   end`

`   stringToFormat = '이 분류에 대해서는 %s 문서를 참고하십시오.'`

`   -- Get the text.`
`   local text = string.format(`
`       stringToFormat,`
`       -- pagetype,`
`       mw.text.listToText(links)`
`   )`
`   `
`   -- Pass it through to Module:Hatnote.`
`   local hnOptions = {}`
`   hnOptions.selfref = options.selfref`
`   hnOptions.extraclasses = 'relarticle mainarticle'`

`   return mHatnote._hatnote(text, hnOptions)`

end

return p