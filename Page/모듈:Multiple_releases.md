> This article is converted from Wikipedia: [모듈:Multiple releases](https://ko.wikipedia.org/wiki/모듈:Multiple_releases).


local infobox = require ('Module:Infobox').infobox local getArgs = require ('Module:Arguments').getArgs

local p = {}

function p.main( frame )

`   local args = getArgs (frame)`

`   InfoboxArgs = {}`
`   InfoboxArgs["subbox"] = "yes"`

`   local a = 1`
`   local IsEmpty = true`
`   local KeepCheckingForArgs = true`
`   while KeepCheckingForArgs == true do`
`       local thisBranch = "branch" .. a`
`       local thisVersion = "version" .. a`
`       local thisDate = "date" .. a`
`       local CurLabel = "label" .. a`
`       local CurData = "data" .. a`

`       if args[thisBranch] and args[thisVersion] then`
`           InfoboxArgs[CurLabel] = args[thisBranch]`
`           InfoboxArgs[CurData] = args[thisVersion]`
`           if args[thisDate] then InfoboxArgs[CurData] = InfoboxArgs[CurData] .. " / " .. args[thisDate] end`
`       else`
`           KeepCheckingForArgs = false`
`           if a > 1 then IsEmpty = false end`
`       end`
`       a = a + 1`
`   end`

`   if IsEmpty == false then`
`       return infobox(InfoboxArgs)`
`   else`
`       return nil`
`   end`

end

return p