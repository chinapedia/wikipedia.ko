> This article is converted from Wikipedia: [모듈:Br separated entries](https://ko.wikipedia.org/wiki/모듈:Br_separated_entries).


local p = {}

local function _main( args )

`   local sep = '`
`'`
`   local lastsep`
`   local t = {}`
`   for i, v in ipairs( args ) do`
`       table.insert( t, v )`
`       if mw.ustring.match( v, '%S' ) then`
`           table.insert( t, sep )`
`           lastsep = #t`
`       end`
`   end`
`   if lastsep then`
`       table.remove( t, lastsep )`
`   end`
`   return table.concat( t )`

end

function p.main( frame )

`   local origArgs`
`   if frame == mw.getCurrentFrame() then`
`       -- We're being called via #invoke. If the invoking template passed any arguments,`
`       -- use them. Otherwise, use the arguments that were passed into the template.`
`       origArgs = frame:getParent().args`
`       for k, v in pairs( frame.args ) do`
`           origArgs = frame.args`
`           break`
`       end`
`   else        `
`       -- We're being called from another module or from the debug console, so assume`
`       -- the arguments are passed in directly.`
`       origArgs = frame`
`   end`
`   `
`   -- Use integer args only, and allow for explicit positional arguments`
`   -- that are specified out of order, e.g. ``.`
`   -- After processing, the args can be accessed accurately from ipairs.`
`   local args = {}`
`   for k, v in pairs( origArgs ) do`
`       if type( k ) == 'number' and k >= 1 and math.floor( k ) == k then`
`           table.insert( args, k )`
`       end`
`   end`
`   table.sort( args )`
`   for i,v in ipairs( args ) do`
`       args[ i ] = origArgs[ v ]`
`   end`
`   `
`   return _main( args )`

end

return p