> This article is converted from Wikipedia: [:WikidataCheck](https://ko.wikipedia.org/wiki/:WikidataCheck).


local p = {}

function p.wikidatacheck(frame)

`   local pframe = frame:getParent()`
`   local config = frame.args -- the arguments passed BY the template, in the wikitext of the template itself`
`   local args = pframe.args -- the arguments passed TO the template, in the wikitext that transcludes the template`
`   `
`   local property = config.property`
`   local value = config.value or ""`
`   local catbase = config.category`
`   local namespaces = config.namespaces`
`   local ok = false -- one-way flag to check if we're in a good namespace`
`   local ns = mw.title.getCurrentTitle().namespace`
`   for v in mw.text.gsplit( namespaces, ",", true) do`
`       if tonumber(v) == ns then`
`           ok = true`
`       end`
`   end`
`   if not ok then -- not in one of the approved namespaces`
`       return ""`
`   end`
`   local entity = mw.wikibase.getEntityObject()`
`   if not entity then -- no Wikidata item`
`       return "`[`분류:위키데이터에``   ``없는``   ``"``   ``..``   ``catbase``   ``..``   ``"`](https://ko.wikipedia.org/wiki/분류:위키데이터에_없는_"_.._catbase_.._" "wikilink")`"`
`   end`
`   local claims = entity.claims or {}`
`   local hasProp = claims[property]`
`   if not hasProp then -- no claim of that property`
`       return "`[`분류:위키데이터에``   ``없는``   ``"``   ``..``   ``catbase``   ``..``   ``"`](https://ko.wikipedia.org/wiki/분류:위키데이터에_없는_"_.._catbase_.._" "wikilink")`" -- bad. Bot needs to add the property`
`   end`
`   local propValue = hasProp[1].mainsnak.datavalue.value -- This should eventually iterate over all possible values?`
`   if value == "" then`
`       return nil -- Using Wikidata`
`   elseif propValue == value then`
`       return "`[`분류:위키데이터와``   ``같은``   ``"``   ``..``   ``catbase``   ``..``   ``"`](https://ko.wikipedia.org/wiki/분류:위키데이터와_같은_"_.._catbase_.._" "wikilink")`" -- yay!`
`   else`
`       return "`[`분류:위키데이터와``   ``다른``   ``"``   ``..``   ``catbase``   ``..``   ``"`](https://ko.wikipedia.org/wiki/분류:위키데이터와_다른_"_.._catbase_.._" "wikilink")`" -- needs human review :(`
`   end`

end

return p