> This article is converted from Wikipedia: [모듈:Property](https://ko.wikipedia.org/wiki/모듈:Property).


\-- [Module:Property](https://ko.wikipedia.org/wiki/Module:Property "wikilink")

local p = {}

\-- trim string function trim(s)

`   -- incase nil`
`   if s == nil then return '' end`
`   s = tostring(s)`
`   return s:gsub("^%s+", ""):gsub("%s+$", "")`

end

\-- Get the property of given wikidata entity. -- [:mw:Extension:Wikibase Client/Lua](https://ko.wikipedia.org/wiki/:mw:Extension:Wikibase_Client/Lua "wikilink") function p.data(frame)

`   if mw.wikibase == nil then`
`       return 'Not yet install Extension:Wikibase ?'`
`   end`

`   local entity = trim(frame.args[2])`
`   if not entity:match('^[QP]%d{1,10}$') then`
`       entity = mw.wikibase.resolvePropertyId(entity) or entity`
`   end`
`   -- entity = mw.wikibase.getEntity(trim(frame.args[2]) or nil)`
`   if entity == '' then`
`       entity = mw.wikibase.getEntity()`
`       if entity == nil or entity.claims == nil then return 'No wikidata entity' end`
`   else`
`       entity = mw.wikibase.getEntity(entity)`
`       if entity == nil then`
`           return 'No wikidata entity: ' .. frame.args[2]`
`       end`
`   end`

`   local property_id = trim(frame.args[1])`

`   if property_id == '' then`
`       -- `<https://www.mediawiki.org/wiki/Extension:Wikibase_Client/Lua#mw.wikibase.label>
`       local language = trim(frame.args[3])`
`       if language == '' then`
`           -- return mw.wikibase.label(entity.id)`
`           return entity:getLabel()`
`       end`
`       return entity:getLabel(language)`
`   end`

`   if property_id == 'link' then`
`       local language = trim(frame.args[3])`
`       if language == '' then language = 'en' end`
`       return entity:getSitelink(language .. 'wiki')`
`   end`

`   if not property_id:match('^P%d{1,10}$') then`
`       property_id = mw.wikibase.resolvePropertyId(property_id) or property_id`
`   end`

`   -- return entity:formatPropertyValues(property_id)`

`   local property = entity.claims[property_id]`
`   if property == nil then`
`       local prefix`
`       if trim(frame.args[2]) == '' then`
`           prefix = 'The page'`
`       else`
`           prefix = 'The entity [[d:'_.._trim(frame.args[2])_.._'|d:' .. trim(frame.args[2]) .. ']]'`
`       end`
`       return prefix .. ' has no property: ' .. property_id`
`   end`

`   property = property[1]['mainsnak']['datavalue']`

`   -- ['datavalue']: e.g.,`
`   -- {"value":{'entity-type':'item','numeric-id':1647152},type:'wikibase-entityid'}`
`   -- {"value":{"amount":"+10","unit":"1","upperBound":"+10","lowerBound":"+10"},"type":"quantity"}`
`   -- {"value":{"time":"-0800-01-01T00:00:00Z","timezone":0,"before":0,"after":0,"precision":7,"calendarmodel":"`<http://www.wikidata.org/entity/Q1985727>`"},"type":"time"}`

`   property = property['value']`

`   if type(property) ~= 'table' then`
`       return property`
`   end`

`   if property['amount'] ~= nil then`
`       return tonumber(property['amount'])`
`   end`

`   if property['time'] ~= nil then`
`       -- local BCE, y, m, d = string.match(property['time'], '^([+\\-]?)0*([1-9]%d*)-0*([1-9]%d*)-0*([1-9]%d*)T')`
`       -- local BCE, y, m, d = property['time']:match('^([+\\-]?)0*([1-9]%d*)-0*([1-9]%d*)-0*([1-9]%d*)T')`
`       local BCE, y, m, d = property['time']:match('^([+\\-]?)(%d+)-(%d+)-0*(%d+)T')`
`       local unit`
`       if property['precision'] <= 7 then`
`           if property['precision'] == 7 then`
`               y = y / 100`
`               unit = '세기'`
`           else`
`               y = y / 1000`
`               unit = '천 기'`
`           end`
`       else`
`           y = y - 0`
`       end`
`       if BCE == '-' then`
`           y = '기원전 ' .. y`
`       end`
`       if property['precision'] <= 7 then`
`           return y .. unit`
`       end`
`       if property['precision'] <= 9 then`
`           return y .. '년'`
`       end`
`       if property['precision'] <= 10 then`
`           return y..'년 '..m..'월'`
`       end`
`       -- TODO: other precisions 정밀도 `<https://en.wikipedia.org/wiki/Module:Wikidata>
`       m = m - 0`
`       d = d - 0`
`       return y..'년 '..m..'월 '..d..'일'`
`   end`

`   if property['numeric-id'] ~= nil then`
`       return mw.wikibase.label('Q' .. property['numeric-id'])`
`   end`

`   -- TODO: other types`
`   -- `<https://www.mediawiki.org/wiki/Wikibase/API>
`   -- `<https://www.mediawiki.org/wiki/Wikibase/Indexing/RDF_Dump_Format#Value_representation>
`   return 'Can not parse the type: ' .. property_id .. ', please fix Module:property.'`

end

return p