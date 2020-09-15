> This article is converted from Wikipedia: [모듈:Toolbar](https://ko.wikipedia.org/wiki/모듈:Toolbar).


\-- This module implements .

local mArguments -- Lazily initialise [Module:Arguments](https://ko.wikipedia.org/wiki/Module:Arguments "wikilink") local mTableTools = require('Module:TableTools') local yesno = require('Module:Yesno')

local p = {}

function p.main(frame)

`   mArguments = require('Module:Arguments')`
`   local args = mArguments.getArgs(frame)`
`   return p._main(args)`

end

function p._main(args)

`   local toolbarItems = p.makeToolbarItems(args)`
`   if not toolbarItems then`
`       -- Return the blank string if no arguments were specified, rather than`
`       -- returning empty brackets.`
`       return ''`
`   elseif yesno(args.span) == false then`
`       return string.format(`
`           '(%s)',`
`           toolbarItems`
`       )`
`   else`
`       return string.format(`
`           '<span class="plainlinks%s"%s>(%s)`</span>`',`
`           type(args.class) == 'string' and ' ' .. args.class or '',`
`           type(args.style) == 'string' and string.format(' style="%s"', args.style) or '',`
`           toolbarItems`
`       )`
`   end`

end

function p.makeToolbarItems(args)

`   local nums = mTableTools.numKeys(args)`
`   local sep = (args.separator or 'pipe') .. '-separator'`
`   sep = mw.message.new(sep):plain()`
`   local ret = {}`
`   for i, v in ipairs(nums) do`
`       ret[#ret + 1] = mw.ustring.gsub(args[v], "%[%[::+(.-)%]%]", "`[`:%1`](https://ko.wikipedia.org/wiki/:%1 "wikilink")`")`
`   end`
`   if #ret > 0 then`
`       return table.concat(ret, sep)`
`   else`
`       return nil`
`   end`

end

return p