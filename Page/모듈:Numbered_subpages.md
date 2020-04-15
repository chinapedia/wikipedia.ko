> This article is converted from Wikipedia: [모듈:Numbered subpages](https://ko.wikipedia.org/wiki/모듈:Numbered_subpages).


\-- This module implements .

local getArgs = require('Module:Arguments').getArgs

p = {}

local function ifexist(page)

`   if not page then return false end`
`   if mw.title.new(page).exists then return true end`
`   return false`

end

function p.main(frame)

`   local args = getArgs(frame)`
`   local maxk = tonumber(args.max or '50') or 50`
`   local mink = tonumber(args.min or '1') or 1`
`   local root = ''`
`   local missing = args.missing or (args.max and 'transclude' or 'skip')`
`   local res = ''`
`   `
`   if missing ~= 'transclude' then`
`       root = frame:preprocess('``')`
`   end`
`   maxk = (maxk > (mink + 250)) and (mink + 250) or maxk`
`   for i=mink,maxk do`
`       if missing == 'transclude' then`
`           res = res .. frame:expandTemplate{title = 'subpage', args = { i } }`
`       else`
`           if ifexist(root .. '/' .. i) then`
`               res = res .. frame:expandTemplate{title = 'subpage', args = { i } }`
`           else`
`               if missing == 'link' then`
`                   res = res .. '`[`'``   ``..``   ``root``   ``..``   ``'/'``   ``..``   ``i``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._root_.._'/'_.._i_.._' "wikilink")` '`
`               elseif missing == 'stop' then`
`                   i = maxk + 1`
`               end`
`           end`
`       end`
`   end`
`   `
`   return res`

end

return p