> This article is converted from Wikipedia: [모듈:DateConverter](https://ko.wikipedia.org/wiki/모듈:DateConverter).


local p = {}

local Date = require('Module:Date')._Date

local function trim(s)

`   -- incase nil`
`   if s == nil then return '' end`
`   s = tostring(s)`
`   return s:gsub("^%s+", ""):gsub("%s+$", "")`

end

function p.DateConverter(frame)

`   local qid = frame.args[2]`
`   local entity, propertyID`
`   local rawdate`
`   local m, d, y = ''`
`   local datavec, lang, case, class, trimYear`
`   local pencil, datestr`

`   if qid == nil then`
`       entity = mw.wikibase.getEntityObject()`
`   else`
`       entity = mw.wikibase.getEntityObject(qid)`
`   end`

`   if entity == nil then`
`       return ""`
`   end`

`   propertyID = trim(frame.args[1])`
`   if entity.claims[propertyID] == nil then`
`       return ""`
`   end`
`   rawdate = entity:formatPropertyValues(propertyID).value`

`   local dtFormat = {`
`       "(%d+)%s+(%d+)%s+(%d+)",`
`       "(%d*)월%s+(%d*)",`
`       "(%d+)"`
`   }`

`   m, y = string.match(rawdate, dtFormat[2])`
`   if m == nil then`
`       d, m, y = string.match(rawdate, dtFormat[1])`
`       if d == nil then`
`           d = ''`
`           m = ''`
`           y = string.match(rawdate, dtFormat[3])`
`           if y == nil then`
`               return ""`
`           end`
`       end`
`   end`

`   datavec = { y, m, d, '', '', '' }`
`   lang = ko`
`   case = ''`
`   class = 'dtstart'`
`   trimYear = '100-999'`
`   pencil = frame:expandTemplate{`
`       title = 'EditAtWikidata',`
`       args = {`
`           qid = qid,`
`           pid = propertyID`
`       }`
`   }`

`   if frame.args['pencil'] == ('no' or 'N') then`
`       datestr = Date(datavec, lang, case, class, trimYear)`
`   else`
`       datestr = Date(datavec, lang, case, class, trimYear) .. pencil`
`   end`

`   return datestr`

end

return p