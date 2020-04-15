> This article is converted from Wikipedia: [모듈:Taxonbar](https://ko.wikipedia.org/wiki/모듈:Taxonbar).


require('Module:No globals')

local conf = require( "Module:Taxonbar/conf" ) -- configuration module local TaxonItalics = require("Module:TaxonItalics") -- use a function from Module:TaxonItalics to italicize a taxon name

local function getIdsFromWikidata( item, property )

`   local ids = {}`
`   if not item.claims[property] then`
`       return ids`
`   end`
`   for _, statement in pairs( item.claims[property] ) do`
`       if statement.mainsnak.datavalue then`
`           table.insert( ids, statement.mainsnak.datavalue.value )`
`       end`
`   end`
`   return ids`

end

local function getLink( property, val )

`   local link, returnVal = "", {}`
`   `
`   returnVal.isError = false`
`   `
`   if mw.ustring.find( val, '//' ) then`
`       link = val`
`   else`
`       if type(property) == 'number' and property > 0 then`
`           local entityObject = mw.wikibase.getEntity('P'..property)`
`           local dataType`
`           `
`           if entityObject then dataType = entityObject.datatype`
`           else returnVal.isError = true end`
`           `
`           if dataType == "external-id" then`
`               local formatterURL = entityObject:getBestStatements('P1630')[1]`
`               if formatterURL then link = formatterURL.mainsnak.datavalue.value end`
`           elseif dataType == "url" then`
`               local subjectItem = entityObject:getBestStatements('P1629')[1]`
`               if subjectItem then`
`                   local officialWebsite = mw.wikibase.getEntity(subjectItem.mainsnak.datavalue.value.id):getBestStatements('P856')[1]`
`                   if officialWebsite then link = officialWebsite.mainsnak.datavalue.value end`
`               end`
`           elseif dataType == "string" then`
`               local formatterURL = entityObject:getBestStatements('P1630')[1]`
`               if formatterURL then`
`                   link = formatterURL.mainsnak.datavalue.value`
`               else`
`                   local subjectItem = entityObject:getBestStatements('P1629')[1]`
`                   if subjectItem then`
`                       local officialWebsite = mw.wikibase.getEntity(subjectItem.mainsnak.datavalue.value.id):getBestStatements('P856')[1]`
`                       if officialWebsite then link = officialWebsite.mainsnak.datavalue.value end`
`                   end`
`               end`
`           else`
`               returnVal.isError = true`
`           end`
`       elseif type(property) == 'string' then`
`           link = property`
`       end`
`       `
`       local valurl = val`
`       if mw.ustring.find( link, 'antweb.org' ) then valurl = mw.ustring.gsub(valurl, " ", "%%20") end`
`       valurl = mw.ustring.gsub(valurl,"%%","%%%%")`
`       link = mw.ustring.gsub(link, '$1', valurl)`
`   end`
`   `
`   link = mw.ustring.gsub(link, '^[Hh][Tt][Tt][Pp]([Ss]?)://', 'http%1://') -- fix wikidata URL`
`   val = mw.ustring.match(val, '([^=/]*)/?$') -- get display name from end of URL`
`   if mw.ustring.find( link, '//' ) then`
`       returnVal.text = '['..link..' '..mw.text.encode(mw.uri.decode(val, "PATH"),'%[%]')..']'`
`   elseif link == "" then`
`       returnVal.text = val`
`   else`
`       returnVal.text = '`<span class="external">[`'..val..'`](https://ko.wikipedia.org/wiki/'..link..' "wikilink")</span>`'`
`   end`
`   return returnVal`

end

local function createRow( id, label, rawValue, link, withUid )

`   if link then`
`       local outStr = '*`<span style="white-space:nowrap;">`' .. label .. ' <span'`
`       if withUid then outStr = outStr..' class="uid"' end`
`       return outStr..'>' .. link .. '`</span></span>`\n'`
`   else`
`       return '* ' .. mw.text.tag('span', {class='error'}, '식별자 ' .. id .. ' ' .. rawValue .. '은(는) 유효하지 않습니다.') .. '\n'`
`   end`

end

local function copyTable(inTable)

`   if type(inTable) ~= 'table' then return inTable end`
`   local outTable = setmetatable({}, getmetatable(inTable))`
`   for key, value in pairs (inTable) do outTable[copyTable(key)] = copyTable(value) end`
`   return outTable`

end

local p = {}

function p.authorityControlTaxon( frame )

`   local resolve = require( "Module:ResolveEntityId" )`
`   local parentArgs = copyTable(frame:getParent().args)`
`   local currentTitle = mw.title.getCurrentTitle()`
`   local currentEntityId = mw.wikibase.getEntityIdForCurrentPage()`
`   `
`   local stringArgs = false`
`   local fromTitleCount, firstRow, rowCount = 1, 0, 0`
`   local outString, errors = "", ""`
`   local tfroms = {} --non-sequential table of unique froms`
`   local ifroms = 0 --integer size of tfroms, b/c Lua`
`   local categories = {`
`       '`[`분류:from``   ``변수가``   ``없는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:from_변수가_없는_생물_분류_식별자 "wikilink")`',`
`       '`[`분류:위키데이터에서``   ``비동기된``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:위키데이터에서_비동기된_생물_분류_식별자 "wikilink")`',`
`       '', -- [3] placeholder`
`       '', -- [4] placeholder`
`       '', -- [5] placeholder`
`       '', -- [6] placeholder`
`       '', -- [7] placeholder`
`       '', -- [8] placeholder`
`       '', -- [9] placeholder`
`       '', --[10] placeholder`
`       '', --[11] placeholder`
`       '', --[12] placeholder`
`       '', --[13] placeholder`
`       '', --[14] placeholder`
`       '', --[15] placeholder`
`       '', --[16] placeholder`
`   }`
`   `
`   --Assess the page's relationship with Wikidata`
`   local currentItem = nil`
`   if currentTitle.namespace == 10 then --i.e. Module:Taxonbar/sandbox, Template:Taxonbar/doc, etc.`
`       if resolve._entityid(frame, parentArgs['from']) then`
`           currentItem = mw.wikibase.getEntity(parentArgs['from'])`
`       end`
`       if currentItem == nil then`
`           if resolve._entityid(frame, parentArgs['from1']) then`
`               currentItem = mw.wikibase.getEntity(parentArgs['from1'])`
`           end`
`       end`
`   elseif resolve._entityid(frame, currentEntityId) then`
`       currentItem = mw.wikibase.getEntity(currentEntityId)`
`   else --currentEntityId == nil`
`       categories[6] = '`[`분류:위키데이터``   ``항목이``   ``필요한``   ``생물``   ``분류``   ``식별자``   ``문서`](https://ko.wikipedia.org/wiki/분류:위키데이터_항목이_필요한_생물_분류_식별자_문서 "wikilink")`'`
`   end`
`   if currentItem then`
`       local acceptable = {`
`          ['Q16521'] = 'taxon',`
`          ['Q310890'] = 'monotypic taxon',`
`          ['Q2568288'] = 'ichnotaxon',`
`          ['Q23038290'] = 'fossil taxon',`
`          ['Q47487597'] = 'monotypic fossil taxon',`
`          ['Q42621'] = 'hybrid',`
`          ['Q235536'] = 'incertae sedis',`
`          ['Q713623'] = 'clade',`
`          ['Q848328'] = 'serotype',`
`          ['Q17487588'] = 'unavailable combination',`
`       }`
`       categories[11] = '`[`분류:생물``   ``분류가``   ``아닌``   ``잠재적인``   ``문서의``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:생물_분류가_아닌_잠재적인_문서의_생물_분류_식별자 "wikilink")`' --unset if acceptable found`
`       for _, instanceOfState in pairs ( currentItem:getBestStatements('P31') ) do --instance of`
`           local instanceOf = instanceOfState.mainsnak.datavalue.value.id`
`           if acceptable[instanceOf] then`
`               categories[11] = ''`
`               break`
`           end`
`       end`
`   end`
`   `
`   --Cleanup args`
`   for k, v in pairs( frame:getParent().args ) do`
`       if type(k) == 'string' then`
`           --make args case insensitive`
`           local lowerk = mw.ustring.lower(k)`
`           if not parentArgs[lowerk] or parentArgs[lowerk] == '' then`
`               parentArgs[k] = nil`
`               parentArgs[lowerk] = v`
`           end`
`           --remap abc to abc1`
`           if not mw.ustring.find(lowerk,"%d$") then --if no number at end of param`
`               if not parentArgs[lowerk..'1'] or parentArgs[lowerk..'1'] == '' then`
`                   parentArgs[lowerk] = nil`
`                   lowerk = lowerk..'1'`
`                   parentArgs[lowerk] = v`
`               end`
`           end`
`           if v and v ~= '' then`
`               --remap "for" to "title"`
`               if mw.ustring.sub(lowerk,1,3) == "for" then`
`                   local forTitle = mw.ustring.gsub(lowerk,"^for","title",1)`
`                   if parentArgs[forTitle] == '' or not parentArgs[forTitle] then`
`                       parentArgs[lowerk] = nil`
`                       lowerk = forTitle`
`                       parentArgs[lowerk] = v`
`                   end`
`               end`
`               --find highest from or title param`
`               if mw.ustring.sub(lowerk,1,4) == "from" then`
`                   local fromNumber = tonumber(mw.ustring.sub(lowerk,5,-1))`
`                   if fromNumber and fromNumber >= fromTitleCount then fromTitleCount = fromNumber end`
`                   --look for duplicate froms while we're here`
`                   if mw.ustring.find(v, "^Q%d") then`
`                       if tfroms[v] then`
`                           categories[8] = '`[`분류:중복``   ``변수가``   ``있는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:중복_변수가_있는_생물_분류_식별자 "wikilink")`'`
`                           tfroms[v] = tfroms[v] + 1`
`                       else`
`                           tfroms[v] = 1`
`                           ifroms = ifroms + 1`
`                       end`
`                       if ifroms > 1 then`
`                           categories[3] = '`[`분류:여러``   ``개의``   ``수동``   ``위키데이터``   ``항목을``   ``사용하는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:여러_개의_수동_위키데이터_항목을_사용하는_생물_분류_식별자 "wikilink")`'`
`                       end`
`                   end`
`               elseif mw.ustring.sub(lowerk,1,5) == "title" then`
`                   local titleNumber = tonumber(mw.ustring.sub(lowerk,4,-1))`
`                   if titleNumber and titleNumber >= fromTitleCount then fromTitleCount = titleNumber end`
`               elseif mw.ustring.lower(v) ~= 'no' then`
`                   stringArgs = true`
`                   categories[5] = '`[`분류:수동``   ``생물``   ``분류``   ``ID를``   ``사용하는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:수동_생물_분류_ID를_사용하는_생물_분류_식별자 "wikilink")`'`
`               end`
`           end`
`       end`
`   end`
`   `
`   --Append basionym to arg list, if not already provided`
`   if currentItem then`
`       local currentBasState = currentItem:getBestStatements('P566')[1] --basionym`
`       if currentBasState then`
`           local basionymId = currentBasState.mainsnak.datavalue.value.id`
`           if basionymId and resolve._entityid(frame, basionymId) and tfroms[basionymId] == nil then`
`               --check that basionym is a strict instance of taxon`
`               local basionymItem = mw.wikibase.getEntity(basionymId)`
`               if basionymItem then`
`                   local acceptable = {`
`                      ['Q16521'] = 'taxon',`
`                      ['Q310890'] = 'monotypic taxon',`
`                      ['Q2568288'] = 'ichnotaxon',`
`                      ['Q23038290'] = 'fossil taxon',`
`                      ['Q47487597'] = 'monotypic fossil taxon',`
`                   }`
`                   for _, instanceOfState in pairs ( basionymItem:getBestStatements('P31') ) do --instance of`
`                       local instanceOf = instanceOfState.mainsnak.datavalue.value.id`
`                       if acceptable[instanceOf] then`
`                           --housekeeping`
`                           tfroms[basionymId] = 1`
`                           ifroms = ifroms + 1`
`                           fromTitleCount = fromTitleCount + 1`
`                           --append basionym & track`
`                           parentArgs['from'..fromTitleCount] = basionymId`
`                           categories[14] = '`[`분류:자동으로``   ``기본명이``   ``추가된``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:자동으로_기본명이_추가된_생물_분류_식별자 "wikilink")`'`
`                           break`
`   end end end end end end`
`   `
`   --Append monotypic genus/species to arg list of monotypic species/genus, if not already provided`
`   if currentItem then`
`       for _, instanceOfState in pairs ( currentItem:getBestStatements('P31') ) do --instance of`
`           local taxonRank = nil`
`           local parentItem = nil`
`           local parentTaxon = nil`
`           local parentTaxonRank = nil`
`           local parentMonoGenus = nil --holy grail/tbd`
`           local instanceOf = instanceOfState.mainsnak.datavalue.value.id`
`           if instanceOf and (instanceOf == 'Q310890' or instanceOf == 'Q47487597') then --monotypic/fossil taxon`
`               local taxonRankState = currentItem:getBestStatements('P105')[1] --taxon rank`
`               if taxonRankState then taxonRank = taxonRankState.mainsnak.datavalue.value.id end`
`               `
`               if taxonRank and taxonRank == 'Q7432' then --species`
`                   --is monotypic species; add genus`
`                   local parentTaxonState = currentItem:getBestStatements('P171')[1] --parent taxon`
`                   if parentTaxonState then parentTaxon = parentTaxonState.mainsnak.datavalue.value.id end`
`                   --confirm parent taxon rank == genus & monotypic (too careful/expensive? remove/mod this first if hitting any request limits)`
`                   if parentTaxon and resolve._entityid(frame, parentTaxon) then`
`                       parentItem = mw.wikibase.getEntity(parentTaxon)`
`                       if parentItem then`
`                           local parentTaxonRankState = parentItem:getBestStatements('P105')[1] --taxon rank`
`                           if parentTaxonRankState then parentTaxonRank = parentTaxonRankState.mainsnak.datavalue.value.id end`
`                           if parentTaxonRank and parentTaxonRank == 'Q34740' then -- genus`
`                               for _, parentInstanceOfState in pairs ( parentItem:getBestStatements('P31') ) do --instance of`
`                                   local parentInstanceOf = parentInstanceOfState.mainsnak.datavalue.value.id `
`                                   if parentInstanceOf and`
`                                     (parentInstanceOf == 'Q310890' or parentInstanceOf == 'Q47487597') then --monotypic/fossil taxon`
`                                       parentMonoGenus = parentTaxon --confirmed`
`                                       break`
`                                   end`
`                               end`
`                               if parentMonoGenus and tfroms[parentMonoGenus] == nil then`
`                                   --housekeeping`
`                                   tfroms[parentMonoGenus] = 1`
`                                   ifroms = ifroms + 1`
`                                   fromTitleCount = fromTitleCount + 1`
`                                   --append monotypic genus & track`
`                                   parentArgs['from'..fromTitleCount] = parentMonoGenus`
`                                   categories[15] = '`[`분류:자동으로``   ``단형목이``   ``추가된``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:자동으로_단형목이_추가된_생물_분류_식별자 "wikilink")`'`
`                                   break`
`                               end`
`                           end`
`                       end`
`                   end`
`                   if parentMonoGenus == nil or tfroms[parentMonoGenus] == nil then`
`                       categories[16] = '`[`분류:속이``   ``없는``   ``단형종의``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:속이_없는_단형종의_생물_분류_식별자 "wikilink")`'`
`                       break`
`                   end`
`               elseif taxonRank and taxonRank == 'Q34740' then --genus`
`                   --is monotypic genus; add species`
`                   --...`
`               end`
`               `
`           end`
`       end`
`   end`
`   `
`   --Setup navbox`
`   local navboxParams = {`
`       name  = 'Taxonbar',`
`       bodyclass = 'hlist',`
`       listclass = '',`
`       groupstyle = 'text-align: left;',`
`   }`
`   `
`   for f = 1,fromTitleCount,1`
`   do`
`       local elements, title = {}, nil`
`       --cleanup parameters`
`       if parentArgs['from'..f] == '' then parentArgs['from'..f] = nil end`
`       if parentArgs['title'..f] == '' then parentArgs['title'..f] = nil end`
`       --remap aliases`
`       for _, a in pairs( conf.aliases ) do`
`           local alias, name = mw.ustring.lower(a[1]), mw.ustring.lower(a[2])`
`           if parentArgs[alias..f] and not parentArgs[name..f] then`
`               parentArgs[name..f] = parentArgs[alias..f]`
`               parentArgs[alias..f] = nil`
`           end`
`       end`
`       --Fetch Wikidata item`
`       local from = resolve._entityid(frame, parentArgs['from'..f])`
`       local item = mw.wikibase.getEntity(from)`
`       local label = nil`
`       if type(item) == 'table' then`
`           local statements = item:getBestStatements('P225')[1] --taxon name`
`           if statements then`
`               local datavalue = statements.mainsnak.datavalue`
`               if datavalue then`
`                   label = datavalue.value`
`               end`
`           end`
`           label = label or item:getLabel()`
`       else`
`           if parentArgs['from'..f] then`
`               categories[1] = ''`
`               categories[4] = '`[`분류:잘못된``   ``변수를``   ``사용하는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:잘못된_변수를_사용하는_생물_분류_식별자 "wikilink")`'`
`               errors = errors .. mw.text.tag('strong', {class='error'}, '오류: "' .. `
`                        parentArgs['from'..f] .. '"은(는) 유효한 위키데이터 항목 ID가 아닙니다.`
`')             `
`           end`
`       end`
`       if label and label ~= '' then`
`           title = mw.title.new(label)`
`       end`
`       if not title and parentArgs['title'..f] then`
`           title = mw.title.new(parentArgs['title'..f])`
`       end`
`       if not title and f == 1 then`
`           title = currentTitle`
`       end`
`       `
`       if title then`
`           if (not parentArgs['wikidata'..f] or parentArgs['wikidata'..f] == '') and `
`              (title.namespace == 0) then`
`               if parentArgs['from'..f] then`
`                   parentArgs['wikidata'..f] = parentArgs['from'..f]`
`               elseif item then`
`                   parentArgs['wikidata'..f] = item.id`
`               end`
`           end`
`           if title.namespace == 0 or stringArgs then --Only in the main namespace or if there are manual overrides`
`               local sourcesFound = false`
`               local sourceCount = 0`
`               for _, params in pairs( conf.databases ) do`
`                   params[1] = mw.ustring.lower(params[1])`
`                   local propId = params[3]`
`                   --Wikidata fallback if requested`
`                   if (item ~= nil and item.claims ~= nil) and`
`                      (type(propId) == 'string' or (type(propId) == 'number' and propId > 0)) then`
`                       local wikidataIds = getIdsFromWikidata( item, 'P' .. propId )`
`                       local v = parentArgs[params[1]..f]`
`                       if wikidataIds[1] then`
`                           if (not v or v == '') then`
`                               parentArgs[params[1]..f] = wikidataIds[1]`
`                           else`
`                               if v and v ~= 'no' and v ~= wikidataIds[1] then`
`                                   categories[9] = '`[`분류:위키데이터와``   ``다른``   ``수동``   ``생물``   ``분류``   ``ID를``   ``사용하는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:위키데이터와_다른_수동_생물_분류_ID를_사용하는_생물_분류_식별자 "wikilink")`'`
`                               elseif v and v == wikidataIds[1] then`
`                                   categories[10] = '`[`분류:위키데이터와``   ``동일한``   ``수동``   ``생물``   ``분류``   ``ID를``   ``사용하는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:위키데이터와_동일한_수동_생물_분류_ID를_사용하는_생물_분류_식별자 "wikilink")`'`
`                               end`
`                           end`
`                       end`
`                   end`
`                   local val = parentArgs[params[1]..f]`
`                   if val and val ~= '' and mw.ustring.lower(val) ~= 'no' then`
`                       if type(propId) == 'number' then`
`                           if propId < 0 then propId = -propId end --allow link`
`                           if propId > 0 then --link`
`                               table.insert( elements, createRow( params[1], params[2]..':', val, getLink( propId, val ).text, true ) )`
`                           else --propId == 0; no link`
`                               table.insert( elements, createRow( params[1], params[2]..':', val, val, true ) )`
`                           end`
`                       else`
`                           table.insert( elements, createRow( params[1], params[2]..':', val, getLink( propId, val ).text, true ) )`
`                       end`
`                       if params[1] ~= 'wikidata' then`
`                           sourcesFound = true `
`                           sourceCount = sourceCount + 1`
`                       end`
`                   end`
`               end`
`               `
`               if sourceCount >= 20 then categories[12] = '`[`분류:20개``   ``이상의``   ``생물``   ``분류``   ``ID를``   ``사용하는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:20개_이상의_생물_분류_ID를_사용하는_생물_분류_식별자 "wikilink")`' end`
`               if sourceCount >= 25 then categories[13] = '`[`분류:25개``   ``이상의``   ``생물``   ``분류``   ``ID를``   ``사용하는``   ``생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/분류:25개_이상의_생물_분류_ID를_사용하는_생물_분류_식별자 "wikilink")`' end`
`               `
`               --Generate navbox title`
`               if sourcesFound then`
`                   rowCount = rowCount + 1`
`                   if firstRow == 0 then firstRow = f end`
`                   --set title from wikidata if it doesn't exist`
`                   if parentArgs['title'..f] == '' or not parentArgs['title'..f] then`
`                       parentArgs['noTitle'..f] = true`
`                       parentArgs['title'..f] = title.text`
`                   end`
`                   --if it exists now, set row heading to title`
`                   if parentArgs['title'..f] and parentArgs['title'..f] ~= '' then`
`                       navboxParams['group'..f] = TaxonItalics.italicizeTaxonName(parentArgs['title'..f], false)`
`                   else`
`                       navboxParams['group'..f] = ""`
`                   end`
`                   navboxParams['list'..f] = table.concat( elements )`
`               elseif currentEntityId then`
`                   categories[7] = '`[`분류:위키데이터``   ``생물``   ``분류``   ``ID가``   ``없는``   ``생물``   ``분류``   ``식별자``   ``문서`](https://ko.wikipedia.org/wiki/분류:위키데이터_생물_분류_ID가_없는_생물_분류_식별자_문서 "wikilink")`'`
`               end`
`               `
`               --Categorize`
`               if parentArgs['from'..f] and parentArgs['from'..f] ~= '' then`
`                   --blank "missing from" if 'from' exists`
`                   categories[1] = ''`
`                   --blank "desynced" if 'from' matches current page`
`                   if parentArgs['from'..f] == currentEntityId then categories[2] = '' end`
`               end`
`                   --cannot be "desynced" if no 'from' params`
`               if categories[1] ~= '' then categories[2] = '' end`
`           end`
`       end`
`   end`

`   if rowCount > 0 then`
`       local Navbox = require('Module:Navbox')`
`       if rowCount > 1 then`
`           --remove duplicates and move page title to top`
`           local rowIDs = {}`
`           for f = 1,fromTitleCount,1`
`           do`
`               if parentArgs['title'..f] and parentArgs['title'..f] ~= '' then`
`                   if rowIDs[parentArgs['wikidata'..f]] then --remove duplicate`
`                       navboxParams['group'..f] = nil`
`                       navboxParams['list'..f] = nil`
`                   else`
`                       rowIDs[parentArgs['wikidata'..f]] = true`
`                       if f > firstRow and (parentArgs['title'..f] == currentTitle.text or `
`                          parentArgs['wikidata'..f] == currentEntityId) then --move item linked to page to top`
`                           if navboxParams['group'..f] and `
`                              navboxParams['group'..f] ~= '' and `
`                              navboxParams['list'..f] and `
`                              navboxParams['list'..f] ~= '' then`
`                               local tempGroup, tempList = navboxParams['group'..f], navboxParams['list'..f]`
`                               navboxParams['group'..f], navboxParams['list'..f] = navboxParams['group'..firstRow], navboxParams['list'..firstRow]`
`                               navboxParams['group'..firstRow], navboxParams['list'..firstRow] = tempGroup, tempList`
`                           end`
`                       end`
`                   end`
`               end`
`           end`
`           --adjust navbox for number of rows`
`           navboxParams['title'] = "`[`생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/위키프로젝트:생명체 "wikilink")`"`
`           if rowCount > 2 then`
`               navboxParams['navbar'] = 'plain'`
`           else`
`               navboxParams['state'] = 'off'`
`               navboxParams['navbar'] = 'off'`
`           end`
`       elseif parentArgs['noTitle'..firstRow] then`
`           navboxParams['group'..firstRow] = '`[`생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/위키프로젝트:생명체 "wikilink")`'`
`       else`
`           navboxParams['group'..firstRow] = '`[`생물``   ``분류``   ``식별자`](https://ko.wikipedia.org/wiki/위키프로젝트:생명체 "wikilink")
`' .. navboxParams['group'..firstRow]`
`       end`
`       `
`       --return navbox`
`       outString = Navbox._navbox(navboxParams)`
`   end`
`   `
`   --add categories`
`   if string.sub(currentTitle.subpageText,1,9) == 'testcases' then parentArgs['demo'] = true end`
`   if parentArgs['demo'] and parentArgs['demo'] ~= '' then`
`       outString = outString .. mw.text.nowiki(table.concat(categories)) .. '`
`'`
`   elseif currentTitle.namespace == 0 then`
`       outString = outString .. table.concat(categories)`
`   end`
`   `
`   return outString .. errors`

end

return p