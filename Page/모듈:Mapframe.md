> This article is converted from Wikipedia: [:Mapframe](https://ko.wikipedia.org/wiki/:Mapframe).


\-- Note: Originally written on English Wikipedia at <https://en.wikipedia.org/wiki/Module:Mapframe> -- \#\#\#\#\# Localisation (L10n) settings \#\#\#\#\# -- Replace values in quotes ("") with localised values

local L10n = {}

\-- Template parameter names (unnumbered versions only) L10n.para = {

`   display     = "display",`
`   type        = "type",`
`   id              = "id",`
`   ids             = "ids",`
`   from        = "from",`
`   raw     = "raw",`
`   title       = "title",`
`   description = "description",`
`   strokeColor     = "stroke-color",`
`   strokeColour    = "stroke-colour",`
`   strokeWidth = "stroke-width",`
`   coord       = "coord",`
`   marker      = "marker",`
`   markerColor = "marker-color",`
`   markerColour    = "marker-colour",`
`   text        = "text",`
`   icon        = "icon",`
`   zoom        = "zoom",`
`   frame       = "frame",`
`   plain       = "plain",`
`   frameWidth  = "frame-width",`
`   frameHeight = "frame-height",`
`   frameLat    = "frame-lat",`
`   frameLatitude   = "frame-latitude",`
`   frameLong   = "frame-long",`
`   frameLongitude  = "frame-longitude",`
`   frameAlign  = "frame-align"`

}

\-- Names of other templates this module depends on L10n.template = {

`   Coord       = "Coord2"`

}

\-- Error messages L10n.error = {

`   badDisplayPara  = "무효한 표시 한계입니다",`
`   noCoords    = "위키데이터인지|" .. L10n.para.coord .. "= 에 좌표를 지정해주세요",`
`   wikidataCoords  = "위키데이터 좌표가 없습니다"`

}

\-- Other strings L10n.str = {

`   -- valid values for display parameter, e.g. (|display=inline) or (|display=title) or (|display=inline,title) or (|display=title,inline)`
`   inline      = "inline",         `
`   title       = "title",  `
`   dsep        = ",",          -- separator between inline and title (comma in the example above)`

`   -- valid values for type paramter`
`   line        = "line",       -- geoline feature (e.g. a road)`
`   shape       = "shape",      -- geoshape feature (e.g. a state or province)`
`   shapeInverse    = "shape-inverse",  -- geomask feature (the inverse of a geoshape)`
`   data        = "data",       -- geoJSON data page on Commons`
`   point       = "point",      -- single point feature (coordinates)`

`   -- valid values for icon, frame, and plain parameters`
`   affirmedWords = ' '..table.concat({`
`       "add",`
`       "added",`
`       "affirm",`
`       "affirmed",`
`       "include",`
`       "included",`
`       "on",`
`       "true",`
`       "yes",`
`       "y"`
`   }, ' ')..' ',`
`   declinedWords = ' '..table.concat({`
`       "decline",`
`       "declined",`
`       "exclude",`
`       "excluded",`
`       "false",`
`       "none",`
`       "not",`
`       "no",`
`       "n",`
`       "off",`
`       "omit",`
`       "omitted",`
`       "remove",`
`       "removed"`
`   }, ' ')..' '`

}

\-- Default values for parameters L10n.defaults = {

`   display     = L10n.str.inline,`
`   text        = "지도",`
`   frameWidth  = "300",`
`   frameHeight = "200",`
`   marker      = "marker",     -- Do not translate. For valid alternate values, see `<https://www.mediawiki.org/wiki/Maps/Icons>
`   markerColor = "5E74F3",`
`   strokeColor = "#ff0000",`
`   strokeWidth = 6`

}

\-- \#\#\#\# End of L10n settings \#\#\#\#

function setCleanArgs(argsTable)

`   local cleanArgs = {}`
`   for key, val in pairs(argsTable) do`
`       if type(val) == 'string' then`
`           val = val:match('^%s*(.-)%s*$')`
`           if val ~= '' then`
`               cleanArgs[key] = val:gsub('%c',' ')`
`           end`
`       else`
`           cleanArgs[key] = val`
`       end`
`   end`
`   return cleanArgs`

end

function isAffirmed(val)

`   if not(val) then return false end`
`   return string.find(L10n.str.affirmedWords, ' '..val..' ', 1, true ) and true or false`

end

function isDeclined(val)

`   if not(val) then return false end`
`   return string.find(L10n.str.declinedWords , ' '..val..' ', 1, true ) and true or false`

end

function makeContent(args)

`   if args[L10n.para.raw] then`
`       return args[L10n.para.raw]`
`   end`

`   local content = {};`
`   local contentIndex = '';`
`   while args[L10n.para.type .. contentIndex] or args[L10n.para.from .. contentIndex] do`
`       local contentArgs = {}`
`       for k, v in pairs(args) do`
`           if string.match(k, '.*'..contentIndex) then`
`               contentArgs[string.gsub(k, contentIndex, '')] = v`
`           end`
`       end`

`       if contentIndex == '' then contentIndex = 1 end`
`       content[contentIndex] = makeContentJson(contentArgs)`
`       contentIndex = contentIndex + 1`
`   end`
`   `
`   --Single item, no array needed`
`   if #content==1 then return content[1] end`

`   --Multiple items get placed in a FeatureCollection`
`   local contentArray = '[\n' .. table.concat( content, ',\n') .. '\n]'`
`   return contentArray`

end

function parseCoords(coords)

`   local parts = mw.text.split((mw.ustring.match(coords,'[북남]위 [%.%d]+° [동서]경 [%.%d]+') or ''), '° ')`

`   latParts = mw.text.split(parts[1], ' ')`
`   longParts = mw.text.split(parts[2], ' ')`

`   if latParts[1] == '남위' then latParts[2] = '-'..latParts[2] end`
`   if longParts[1] == '서경' then longParts[2] = '-'..longParts[2] end`
`   return tonumber(latParts[2]), tonumber(longParts[2])`

end

function wikidataCoords(item_id)

`   if not(mw.wikibase.isValidEntityId(item_id)) or not(mw.wikibase.entityExists(item_id)) then`
`       error(L10n.error.noCoords, 0)`
`   end`
`   local coordStatements = mw.wikibase.getBestStatements(item_id, 'P625')`
`   if not coordStatements or #coordStatements == 0 then`
`       error(L10n.error.wikidataCoords, 0)`
`   end`
`   local wdCoords = coordStatements[1]['mainsnak']['datavalue']['value']`
`   return tonumber(wdCoords['latitude']), tonumber(wdCoords['longitude'])`

end

function makeCoords(args, plainOutput)

`   local coords, lat, long`
`   local frame = mw.getCurrentFrame()`
`   if args[L10n.para.coord] then`
`       coords = frame:preprocess(args[L10n.para.coord])`
`       lat, long = parseCoords(coords)`
`   else`
`       lat, long = wikidataCoords(args[L10n.para.id] or args[L10n.para.ids] or mw.wikibase.getEntityIdForCurrentPage())`
`   end`
`   if plainOutput then`
`       return lat, long`
`   end`
`   return {[0] = long, [1] = lat}`

end

function makeContentJson(args)

`   local data = {}`

`   if args[L10n.para.type] == L10n.str.point then`
`       data.type = "Feature"`
`       data.geometry = {`
`           type = "Point",`
`           coordinates = makeCoords(args)`
`       }`
`       data.properties = {`
`           title = args[L10n.para.title] or mw.getCurrentFrame():getParent():getTitle(),`
`           ["marker-symbol"] = args[L10n.para.marker] or L10n.defaults.marker,`
`           ["marker-color"] = args[L10n.para.markerColor] or args[L10n.para.markerColour] or L10n.defaults.markerColor`
`       }`
`   else`
`       data.type = "ExternalData"`

`       if args[L10n.para.type] == L10n.str.data or args[L10n.para.from] then`
`           data.service = "page"`
`       elseif args[L10n.para.type] == L10n.str.line then`
`           data.service = "geoline"`
`       elseif args[L10n.para.type] == L10n.str.shape then`
`           data.service = "geoshape"`
`       elseif args[L10n.para.type] == L10n.str.shapeInverse then`
`           data.service = "geomask"`
`       end`

`       if args[L10n.para.id] or args[L10n.para.ids] or (not (args[L10n.para.from]) and mw.wikibase.getEntityIdForCurrentPage()) then`
`           data.ids = args[L10n.para.id] or args[L10n.para.ids] or mw.wikibase.getEntityIdForCurrentPage()`
`       else `
`           data.title = args[L10n.para.from]`
`       end`

`       data.properties = {`
`           stroke = args[L10n.para.strokeColor] or args[L10n.para.strokeColour] or L10n.defaults.strokeColor,`
`           ["stroke-width"] = tonumber(args[L10n.para.strokeWidth]) or L10n.defaults.strokeWidth`
`       }`
`   end`

`   data.properties.title = args[L10n.para.title] or mw.getCurrentFrame():preprocess('``')`
`   if args[L10n.para.description] then`
`       data.properties.description = args[L10n.para.description]`
`   end`

`   return mw.text.jsonEncode(data)`

end

function makeTagAttribs(args, isTitle)

`   local attribs = {}`
`   if args[L10n.para.zoom] then`
`       attribs.zoom = args[L10n.para.zoom]`
`   end`
`   if isDeclined(args[L10n.para.icon]) then`
`       attribs.class = "no-icon"`
`   end`
`   if args[L10n.para.type] == L10n.str.point then`
`       local lat, long = makeCoords(args, 'plainOutput')`
`       attribs.latitude = tostring(lat)`
`       attribs.longitude = tostring(long)`
`   end`
`   if isAffirmed(args[L10n.para.frame]) and not(isTitle) then`
`       attribs.width = args[L10n.para.frameWidth] or L10n.defaults.frameWidth`
`       attribs.height = args[L10n.para.frameHeight] or L10n.defaults.frameHeight`
`       if args[L10n.para.frameLat] or args[L10n.para.frameLatitude] then`
`           attribs.latitude = args[L10n.para.frameLat] or args[L10n.para.frameLatitude]`
`       end`
`       if args[L10n.para.frameLong] or args[L10n.para.frameLongitude] then`
`           attribs.longitude = args[L10n.para.frameLong] or args[L10n.para.frameLongitude]`
`       end`
`       if not attribs.latitude and not attribs.longitude then`
`           local success, lat, long = pcall(wikidataCoords, args[L10n.para.id] or args[L10n.para.ids] or mw.wikibase.getEntityIdForCurrentPage())`
`           if success then`
`               attribs.latitude = tostring(lat)`
`               attribs.longitude = tostring(long)`
`           end`
`       end`
`       if args[L10n.para.frameAlign] then`
`           attribs.align = args[L10n.para.frameAlign]`
`       end`
`       if isAffirmed(args[L10n.para.plain]) then`
`           attribs.frameless = "1"`
`       else`
`           attribs.text = args[L10n.para.text] or L10n.defaults.text`
`       end`
`   else`
`       attribs.text = args[L10n.para.text] or L10n.defaults.text`
`   end`
`   return attribs`

end

function makeTitleOutput(args, tagContent)

`   local titleTag = mw.text.tag('maplink', makeTagAttribs(args, true), tagContent)`
`   local spanAttribs = {`
`       style = "font-size: small;",`
`       id = "coordinates"`
`   }`
`   return mw.text.tag('span', spanAttribs, titleTag)`

end

function makeInlineOutput(args, tagContent)

`   local tagName = 'maplink'`
`   if args[L10n.para.frame] then`
`       tagName = 'mapframe'`
`   end`

`   return mw.text.tag(tagName, makeTagAttribs(args), tagContent)`

end

local p = {}

\-- Entry point for templates function p.main(frame)

`   local parent = frame.getParent(frame)`
`   local output = p._main(parent.args)`
`   return frame:preprocess(output)`

end

\-- Entry point for modules function p._main(_args)

`   local args = setCleanArgs(_args)`

`   local tagContent = makeContent(args)`

`   local display = mw.text.split(args[L10n.para.display] or L10n.defaults.display, '%s*' .. L10n.str.dsep .. '%s*')`
`   local displayInTitle = display[1] ==  L10n.str.title or display[2] ==  L10n.str.title`
`   local displayInline = display[1] ==  L10n.str.inline or display[2] ==  L10n.str.inline`

`   local output`
`   if displayInTitle and displayInline then`
`       output = makeTitleOutput(args, tagContent) .. makeInlineOutput(args, tagContent)`
`   elseif displayInTitle then`
`       output = makeTitleOutput(args, tagContent)`
`   elseif displayInline then`
`       output = makeInlineOutput(args, tagContent)`
`   else`
`       error(L10n.error.badDisplayPara)`
`   end`

`   return output`

end

return p