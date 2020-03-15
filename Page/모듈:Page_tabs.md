> This article is converted from Wikipedia: [:Page tabs](https://ko.wikipedia.org/wiki/:Page_tabs).


\-- This module implements .

local getArgs = require('Module:Arguments').getArgs local yesno = require('Module:Yesno')

local p = {}

function p.main(frame)

`   local args = getArgs(frame)`
`   return p._main(args)`

end

function p._main(args)

`   local makeTab = p.makeTab`
`   local root = mw.html.create()`
`   root:wikitext(yesno(args.NOTOC) and '__NOTOC__' or nil)`
`   local troot = root:tag('table')`
`   troot`
`       :css('background', args.Background or args.background or  '#f8fcff')`
`       :css('text-align', 'center')`
`       :css('width', '100%')`
`       :css('border', '0')`
`       :css('border-spacing', '0')`
`       :css('border-collapse', 'collapse')`
`       :css('vertical-align', 'top')`
`   local trow = troot:tag('tr')`
`   if not args[1] then`
`       args[1] = '``'`
`   end`
`   for i, link in ipairs(args) do`
`       local thisPage`
`       if tonumber(args.This) == i then`
`           thisPage = true`
`       end`
`       trow:wikitext(makeTab(args, link, thisPage))`
`   end`
`   trow:tag('td')`
`       :css('border-bottom', args["border-bottom"] or '2px solid #a3b1bf')`
`       :css('width', '3000px')`
`       :wikitext(' ')`
`       `
`   return tostring(root)`

end

function p.makeTab(args, link, thisPage)

`   local tcell = mw.html.create()`
`   tcell:tag('td')`
`       :css('padding', '0.5em')`
`       :css('background-color', thisPage and 'white' or ( args["background-color"] or '#cee0f2' ))`
`       :cssText(not thisPage and 'font-size:95%' or nil)`
`       :cssText(args["font-size"] and ('font-size:' .. args["font-size"] or nil))`
`       :css('line-height', '0.95em')`
`       :css('border', args.border or 'solid 2px #a3b1bf')`
`       :css('border-bottom', args["this-border-bottom"] or "0")`
`       :cssText(thisPage and 'font-weight:bold')`
`       :css('white-space', 'nowrap')`
`       :css('width', '20px')`
`       :wikitext(link)`
`       :done()`
`   :tag('td')`
`       :css('border-bottom', args["border-bottom"] or '2px solid #a3b1bf')`
`       :css('width', '3px')`
`       :css('padding', '0')`
`       :wikitext(' ')`
`   return tostring(tcell)`

end

return p