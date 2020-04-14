> This article is converted from Wikipedia: [모듈:Su](https://ko.wikipedia.org/wiki/모듈:Su).


\-- This module implements .

local p = {}

function p.main(frame)

`   -- Use arguments from the parent frame only, and remove any blank arguments.`
`   -- We don't need to trim whitespace from any arguments, as this module only`
`   -- uses named arguments, and whitespace is trimmed from them automatically. `
`   local origArgs = frame:getParent().args`
`   local args = {}`
`   for k, v in pairs(origArgs) do`
`       if v ~= '' then`
`           args[k] = v`
`       end`
`   end`

`   -- Define the variables to pass to luaMain.`
`   local sup = args.p`
`   local sub = args.b`
`   local options = {`
`       align = args.a or args['정렬'],`
`       fontSize = args.w or args['폭'] or args['크기']`
`   }`
`   return p._main(sup, sub, options)`

end

function p._main(sup, sub, options)

`   options = options or {}`
`   local span = mw.html.create('span')`

`   -- Set the styles.`
`   span:css{`
`       ['display']        = 'inline-block',`
`       ['margin-bottom']  = '-0.3em',`
`       ['vertical-align'] = sub and '-0.4em' or '0.8em',`
`       ['line-height']    = '1.2em',`
`   }`
`   if options.fontSize == 'f' or options.fontSize == 'fixed' or options.fontSize == '고정' then`
`       span:css{`
`           ['font-family'] = 'monospace,courier',`
`           ['font-size']   = '85%'`
`       }`
`   else`
`       span:css('font-size', options.fontSize and options.fontSize or '85%')`
`   end`
`   if options.align == 'r' or options.align == 'right' or options.align == '오른쪽'  then`
`       span:css('text-align', 'right')`
`   elseif options.align == 'c' or options.align == 'center' or options.align == '가운데' then`
`       span:css('text-align', 'center')`
`   else`
`       span:css('text-align', 'left')`
`   end`

`   -- Add the wikitext.`
`   span`
`       :wikitext(sup)`
`       :tag('br', {selfClosing = true}):done()`
`       :wikitext(sub)`
`   `
`   return tostring(span)`

end

return p