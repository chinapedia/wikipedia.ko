> This article is converted from Wikipedia: [모듈:Pages with authority control identifiers](https://ko.wikipedia.org/wiki/모듈:Pages_with_authority_control_identifiers).


require('Module:No globals')

local p = {} local ac_conf = require('Module:Authority control').conf local currentTitle = mw.title.getCurrentTitle() local title = currentTitle.text local isCat = (currentTitle.namespace == 14)

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Local Utility Functions](https://ko.wikipedia.org/wiki/Local_Utility_Functions "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

\--local function whichTOC( frame ) -- local pageCount = mw.site.stats.pagesInCategory(title, 'pages') -- if pageCount \>= 5000 then -- return frame:expandTemplate{ title = 'Large category TOC' } -- elseif pageCount \> 400 then -- return frame:expandTemplate{ title = 'Category TOC', args = { align = 'center' } } -- end -- return '' --end

local function redCatCheck( catName ) --catName == 'Blah', not 'Category:Blah', not ''

`   if catName and catName ~= '' and mw.title.new(catName, 14).exists == false then`
`       return '`[`분류:깨진``   ``전거``   ``통제``   ``분류를``   ``포함한``   ``문서`](https://ko.wikipedia.org/wiki/분류:깨진_전거_통제_분류를_포함한_문서 "wikilink")`'`
`   end`
`   return ''`

end

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Local Category-Specific Functions](https://ko.wikipedia.org/wiki/Local_Category-Specific_Functions "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

\--For use in , -- i.e. on local function pages( frame, id )

`   for _, conf in pairs( ac_conf ) do`
`       if conf.category == id or conf[1] == id then`
`           local link = conf[2] --not used locally yet`
`           local txCatMore = frame:expandTemplate{ title = '분류 설명', args = {'위키백과:전거 통제'} }`
`           local txWPCat   = frame:expandTemplate{ title = '위키백과 분류' }`
`           local pagesCat = '전거 통제 정보를 포함한 문서'`
`           local outString = txCatMore..txWPCat..'\n'..`
`                   '`[`'..id..'`](https://ko.wikipedia.org/wiki/분류:'..pagesCat..' "wikilink")`'..redCatCheck(pagesCat)`
`           return outString`
`       end`
`   end`
`   return ''`

end

\--For use in , -- i.e. on local function misc( frame, id )

`   for _, conf in pairs( ac_conf ) do`
`       if conf.category == id or conf[1] == id then`
`           local link = conf[2]`
`           local txCatExplain = frame:expandTemplate{ title = 'Category explanation', `
`                   args = { link..' 식별자를 포함한 전거 통제를 사용한 문서' } }`
`           local txCatMore  = frame:expandTemplate{ title = '분류 설명', args = {'위키백과:전거 통제'} }`
`           local txEmptyCat = frame:expandTemplate{ title = '빈 분류' }`
`           local txWPCat    = frame:expandTemplate{ title = '위키백과 분류', args = { hidden = 'yes', tracking = 'yes' } }`
`           --local txTOC = whichTOC( frame )`
`           local idCat = id..' 식별자를 포함한 문서'`
`           local miscCat = '전거 통제 정보를 포함한 기타 문서'`
`           local outString = txCatExplain..txCatMore..txEmptyCat..txWPCat..'\n'..`
`                   '이 분류에 속하는 분류는 `[`Module:Authority``   ``control에`](https://ko.wikipedia.org/wiki/Module:Authority_control "wikilink")` 의해 추가되어야 합니다.'..`
`                   '`[`분류:'..idCat..'`](https://ko.wikipedia.org/wiki/분류:'..idCat..' "wikilink")`'..redCatCheck(idCat)..`
`                   '`[`'..id..'`](https://ko.wikipedia.org/wiki/분류:'..miscCat..' "wikilink")`'..redCatCheck(miscCat)`
`           return outString`
`       end`
`   end`
`   return ''`

end

\--For use in , -- i.e. on local function user( frame, id )

`   for _, conf in pairs( ac_conf ) do`
`       if conf.category == id or conf[1] == id then`
`           local link = conf[2] --not used locally yet`
`           local txCatMore  = frame:expandTemplate{ title = '분류 설명', args = {'전거 통제'} }`
`           local txEmptyCat = frame:expandTemplate{ title = '빈 분류' }`
`           local txWPCat    = frame:expandTemplate{ title = '위키백과 분류', args = { hidden = 'yes', tracking = 'yes' } }`
`           --local txTOC = whichTOC( frame )`
`           local idCat = id..' 식별자를 포함한 문서'`
`           local userCat = '전거 통제 정보를 포함한 사용자 문서'`
`           local outString = txCatMore..txEmptyCat..txWPCat..'\n'..`
`                   '이 분류에 속하는 분류는 `[`Module:Authority``   ``control에`](https://ko.wikipedia.org/wiki/Module:Authority_control "wikilink")` 의해 추가되어야 합니다.'..`
`                   '`[`분류:'..idCat..'`](https://ko.wikipedia.org/wiki/분류:'..idCat..' "wikilink")`'..redCatCheck(idCat)..`
`                   '`[`'..id..'`](https://ko.wikipedia.org/wiki/분류:'..userCat..' "wikilink")`'..redCatCheck(userCat)`
`           return outString`
`       end`
`   end`
`   return ''`

end

\--For use in , -- i.e. on local function wp( frame, id )

`   for _, conf in pairs( ac_conf ) do`
`       if conf.category == id or conf[1] == id then`
`           local link = conf[2]`
`           local txCatExplain = frame:expandTemplate{ title = 'Category explanation', args = {link..' 식별자를 포함한 문서입니다. `[`하위``   ``분류를`](../Page/위키백과:분류.md "wikilink")` 추가해서는 안 되는 문서'} }`
`           local txCatMore    = frame:expandTemplate{ title = '분류 설명', args = {'위키백과:전거 통제'} }`
`           local txEmptyCat   = frame:expandTemplate{ title = '빈 분류' }`
`           local txWPCat      = frame:expandTemplate{ title = '위키백과 분류', args = { hidden = 'yes', tracking = 'yes' } }`
`           --local txTOC = whichTOC( frame )`
`           local idCat = id..' 식별자를 포함한 문서'`
`           local wpCat = '전거 통제 정보를 포함한 위키백과 문서'`
`           local outString = txCatExplain..txCatMore..txEmptyCat..txWPCat..'\n'..`
`                   '이 분류에 속하는 분류는 `[`Module:Authority``   ``control에`](https://ko.wikipedia.org/wiki/Module:Authority_control "wikilink")` 의해 추가되어야 합니다.'..`
`                   '`[`분류:'..idCat..'`](https://ko.wikipedia.org/wiki/분류:'..idCat..' "wikilink")`'..redCatCheck(idCat)..`
`                   '`[`'..id..'`](https://ko.wikipedia.org/wiki/분류:'..wpCat..' "wikilink")`'..redCatCheck(wpCat)`
`           return outString`
`       end`
`   end`
`   return ''`

end

\--For use in , -- i.e. on local function wpfaulty( frame, id )

`   for _, conf in pairs( ac_conf ) do`
`       if conf.category == id or conf[1] == id then`
`           local link = conf[2] --not used locally yet`
`           local param = conf[3]`
`           local txCatMore  = frame:expandTemplate{ title = '분류 설명', args = {'위키백과:전거 통제', 'd:Property:P'..param} }`
`           local txEmptyCat = frame:expandTemplate{ title = '빈 분류' }`
`           local txWPCat    = frame:expandTemplate{ title = '위키백과 분류', args = { hidden = 'yes', tracking = 'yes' } }`
`           --local txDirtyCat = frame:expandTemplate{ title = 'Polluted category' }`
`           --local txTOC = whichTOC( frame )`
`           local idCat = id..' 식별자를 포함한 문서'`
`           local wpfCat = '잘못된 전거 통제 정보를 포함한 위키백과 문서'`
`           local outString = txCatMore..txEmptyCat..txWPCat..'\n'..`
`                   '이 분류에 속하는 분류는 `[`Module:Authority``   ``control에`](https://ko.wikipedia.org/wiki/Module:Authority_control "wikilink")` 의해 추가되어야 합니다.'..`
`                   '`[`분류:'..idCat..'`](https://ko.wikipedia.org/wiki/분류:'..idCat..' "wikilink")`'..redCatCheck(idCat)..`
`                   '`[`'..id..'`](https://ko.wikipedia.org/wiki/분류:'..wpfCat..' "wikilink")`'..redCatCheck(wpfCat)`
`           return outString`
`       end`
`   end`
`   return ''`

end

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Main/External Call](https://ko.wikipedia.org/wiki/Main/External_Call "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") function p.autoDetect( frame )

`   if isCat then`
`       local pagesID    = mw.ustring.match(title, '([%w%.%- ]+) 식별자를 포함한 문서')`
`       local miscID     = mw.ustring.match(title, '([%w%.%- ]+) 식별자를 포함한 기타 문서')`
`       local userID     = mw.ustring.match(title, '([%w%.%- ]+) 식별자를 포함한 사용자 문서')`
`       local wpfaultyID = mw.ustring.match(title, '잘못된 ([%w%.%- ]+) 식별자를 포함한 위키백과 문서')`
`       local wpID       = mw.ustring.match(title, '([%w%.%- ]+) 식별자를 포함한 위키백과 문서')`
`       `
`       if     pagesID    then return pages( frame, pagesID )`
`       elseif miscID     then return misc( frame, miscID )`
`       elseif userID     then return user( frame, userID )`
`       elseif wpfaultyID then return wpfaulty( frame, wpfaultyID ) --must be before wpID check, in case they both match`
`       elseif wpID       then return wp( frame, wpID )             --to keep the regex simple`
`       else   return '`[`분류:알``   ``수``   ``없는``   ``전거``   ``통제``   ``식별자``   ``분류가``   ``포함된``   ``문서`](https://ko.wikipedia.org/wiki/분류:알_수_없는_전거_통제_식별자_분류가_포함된_문서 "wikilink")`'`
`       end`
`   end`
`   return ''`

end

return p

[Category:Blah](https://ko.wikipedia.org/wiki/Category:Blah "wikilink") [Category:Pages_with_authority_control_information](https://ko.wikipedia.org/wiki/Category:Pages_with_authority_control_information "wikilink") [Category:Pages_with_VIAF_identifiers](https://ko.wikipedia.org/wiki/Category:Pages_with_VIAF_identifiers "wikilink") [Category:Miscellaneous_pages_with_authority_control_information](https://ko.wikipedia.org/wiki/Category:Miscellaneous_pages_with_authority_control_information "wikilink") [Category:Miscellaneous_pages_with_VIAF_identifiers](https://ko.wikipedia.org/wiki/Category:Miscellaneous_pages_with_VIAF_identifiers "wikilink") [Category:User_pages_with_authority_control_information](https://ko.wikipedia.org/wiki/Category:User_pages_with_authority_control_information "wikilink") [Category:User_pages_with_VIAF_identifiers](https://ko.wikipedia.org/wiki/Category:User_pages_with_VIAF_identifiers "wikilink") [Category:Wikipedia_articles_with_authority_control_information](https://ko.wikipedia.org/wiki/Category:Wikipedia_articles_with_authority_control_information "wikilink") [Category:Wikipedia_articles_with_VIAF_identifiers](https://ko.wikipedia.org/wiki/Category:Wikipedia_articles_with_VIAF_identifiers "wikilink") [Category:Wikipedia_articles_with_faulty_authority_control_information](https://ko.wikipedia.org/wiki/Category:Wikipedia_articles_with_faulty_authority_control_information "wikilink") [Category:Wikipedia_articles_with_faulty_VIAF_identifiers](https://ko.wikipedia.org/wiki/Category:Wikipedia_articles_with_faulty_VIAF_identifiers "wikilink")