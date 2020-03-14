> This article is converted from Wikipedia: [:Wikibase](https://ko.wikipedia.org/wiki/:Wikibase).


\-- Module:Wikibase local p = {}

\-- Return the item ID of the item linked to the current page. function p.id(frame)

`       if not mw.wikibase then`
`          return "wikibase module not found"`
`       end`

`       entity = mw.wikibase.getEntityObject()`

`       if entity == nil then`
`          return "(연결된 항목 없음)"`
`       end`

`       return entity.id`

end

\-- Return the label of a given data item. function p.label(frame)

`       if frame.args[1] == nil then`
`           entity = mw.wikibase.getEntityObject()`
`           if not entity then return nil end`

`           id = entity.id`
`       else`
`           id = frame.args[1]`
`       end`

`       return mw.wikibase.label( id )`

end

\-- Return the description of a given data item, or of connected page -- if no argument is provided to this method. function p.description(frame)

`   if frame.args[1] == nil then`
`       entity = mw.wikibase.getEntityObject()`
`       if not entity then return nil end`
`       id = entity.id`
`   else`
`       id = mw.text.trim(frame.args[1])`
`   end`
`   return mw.wikibase.description( id )`

end

\-- Return the local page about a given data item. function p.page(frame)

`       if frame.args[1] == nil then`
`           entity = mw.wikibase.getEntityObject()`
`           if not entity then return nil end`

`           id = entity.id`
`       else`
`           id = frame.args[1]`
`       end`

`       return mw.wikibase.sitelink( id )`

end

\-- Return the data type of a property function p.datatype(frame)

`   if frame.args[1] and string.find(frame.args[1], "Property:P") then`
`       if mw.wikibase.getEntityObject(string.gsub(frame.args[1], "Property:P", "P"))  then`
`           return mw.wikibase.getEntityObject(string.gsub(frame.args[1], "Property:P", "P") ).datatype`
`       end`
`   elseif frame.args[1] and string.find(frame.args[1], "P") then`
`       if mw.wikibase.getEntityObject(frame.args[1])  then`
`           return mw.wikibase.getEntityObject(frame.args[1]).datatype`
`       end`
`   end`

end

\--[lengthOfValue 이 함수는 위키데이터의 특정 속성에 값이 몇 개가 달려 있는지를 출력하는 함수입니다. 변수 \#1 - 속성 ID ('p373'의 형식) - Kwj2772](https://ko.wikipedia.org/wiki/lengthOfValue_이_함수는_위키데이터의_특정_속성에_값이_몇_개가_달려_있는지를_출력하는_함수입니다._변수_#1_-_속성_ID_\('p373'의_형식\)_-_Kwj2772 "wikilink") function p.lengthOfValue(frame)

`       if frame.args[1] == nil then`
`           return '속성을 지정해야 합니다.'`
`       else`
`           property = mw.text.trim( frame.args[1] ) -- 'p373'의 형식`
`       end`
`       local entity = mw.wikibase.getEntityObject()`
`       if not entity then return 0 end`
`       if entity['claims'] == nil or entity['claims'][property] == nil then`
`           length = 0`
`       else`
`           length = #entity['claims'][property]`
`       end`
`       return length`

end

return p