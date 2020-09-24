> This article is converted from Wikipedia: [모듈:Authority control](https://ko.wikipedia.org/wiki/모듈:Authority_control).


require('Module:No globals')

local p = {} local title = mw.title.getCurrentTitle() local namespace = title.namespace local testcases = (string.sub(title.subpageText,1,3) == '시험장')

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Category functions](https://ko.wikipedia.org/wiki/Category_functions "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

function p.getCatForId( id )

`   local catName = ''`
`   if namespace == 0 then`
`       catName = id..' 식별자를 포함한 위키백과 문서'`
`   elseif namespace == 2 and not title.isSubpage then`
`       catName = id..' 식별자를 포함한 사용자 문서'`
`   else`
`       catName = id..' 식별자를 포함한 기타 문서'`
`   end`
`   return '`[`분류:'..catName..'`](https://ko.wikipedia.org/wiki/분류:'..catName..' "wikilink")`'..p.redCatLink(catName)`

end

function p.redCatLink( catName ) --catName == 'Blah', not 'Category:Blah', not ''

`   if catName and catName ~= '' and`
`      testcases == false and`
`      mw.title.new(catName, 14).exists == false`
`   then`
`       return '`[`분류:깨진``   ``전거``   ``통제``   ``분류를``   ``포함한``   ``문서`](https://ko.wikipedia.org/wiki/분류:깨진_전거_통제_분류를_포함한_문서 "wikilink")`'`
`   end`
`   return ''`

end

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Property formatting functions](https://ko.wikipedia.org/wiki/Property_formatting_functions "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

function p.aagLink( id )

`   --P3372's format regex: \d+ (e.g. 1)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<https://www.aucklandartgallery.com/explore-art-and-ideas/artist/>`'..id..'/ '..id..']'..p.getCatForId( 'AAG' )`

end

function p.acmLink( id )

`   --P864's format regex: \d{11} (e.g. 12345678901)`
`   if not id:match( '^%d%d%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<https://dl.acm.org/author_page.cfm?id=>`'..id..' '..id..']'..p.getCatForId( 'ACM-DL' )`

end

function p.adbLink( id )

`   --P1907's format regex: [a-z][-a-z]+-([1-2]\d|[1-9])\d{0,3} (e.g. barton-sir-edmund-toby-71)`
`   if not id:match( '^[a-z][-a-z]+-[1-2]%d%d?%d?%d?$' ) and`
`      not id:match( '^[a-z][-a-z]+-[1-9]%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<http://adb.anu.edu.au/biography/>`'..id..' '..id..']'..p.getCatForId( 'ADB' )`

end

function p.agsaLink( id )

`   --P6804's format regex: [1-9]\d* (e.g. 3625)`
`   if not id:match( '^[1-9]%d*$' ) then`
`       return false`
`   end`
`   return '[`<https://www.agsa.sa.gov.au/collection-publications/collection/creators/_/>`'..id..'/ '..id..']'..p.getCatForId( 'AGSA' )`

end

function p.autoresuyLink( id )

`   --P2558's format regex: [1-9]\d{0,4} (e.g. 12345)`
`   if not id:match( '^[1-9]%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://autores.uy/autor/>`'..id..' '..id..']'..p.getCatForId( 'autores.uy' )`

end

function p.awrLink( id )

`   --P4186's format regex: (([A-Z]{3}\d{4})|([A-Z]{2}\d{5}))[a-z] (e.g. PR00768b)`
`   if not id:match( '^[A-Z][A-Z][A-Z]%d%d%d%d[a-z]$' ) and`
`      not id:match( '^[A-Z][A-Z]%d%d%d%d%d[a-z]$' ) then`
`       return false`
`   end`
`   return '[`<http://www.womenaustralia.info/biogs/>`'..id..'.htm '..id..']'..p.getCatForId( 'AWR' )`

end

function p.balatLink( id )

`   --P3293's format regex: \d+ (e.g. 1)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<http://balat.kikirpa.be/object/104257>`'..id..' '..id..']'..p.getCatForId( 'BALaT' ) --no https as of 9/2019`

end

function p.bibsysLink( id )

`   --P1015's format regex: [1-9]\d* or [1-9](\d{0,8}|\d{12}) (e.g. 1234567890123)`
`   --TODO: follow up @ `[`d:Property``   ``talk:P1015#Discrepancy``   ``between``   ``the``   ``2``   ``regex``   ``constraints`](https://ko.wikipedia.org/wiki/d:Property_talk:P1015#Discrepancy_between_the_2_regex_constraints "wikilink")` or escalate/investigate`
`   if not id:match( '^[1-9]%d?%d?%d?%d?%d?%d?%d?%d?$' ) and`
`      not id:match( '^[1-9]%d%d%d%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<https://authority.bibsys.no/authority/rest/authorities/html/>`'..id..' '..id..']'..p.getCatForId( 'BIBSYS' )`

end

function p.bildLink( id )

`   --P2092's format regex: \d+ (e.g. 1)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<https://www.bildindex.de/document/obj>`'..id..' '..id..']'..p.getCatForId( 'Bildindex' )`

end

function p.bncLink( id )

`   --P1890's format regex: \d{9} (e.g. 123456789)`
`   if not id:match( '^%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<http://www.bncatalogo.cl/F?func=direct&local_base=red10&doc_number=>`'..id..' '..id..']'..p.getCatForId( 'BNC' )`

end

function p.bneLink( id )

`   --P950's format regex: (XX|FF|a)\d{4,7}|(bima|bimo|bica|bis[eo]|bivi|Mise|Mimo|Mima)\d{10} (e.g. XX1234567)`
`   if not id:match( '^[XF][XF]%d%d%d%d%d?%d?%d?$' ) and`
`      not id:match( '^a%d%d%d%d%d?%d?%d?$' ) and`
`      not id:match( '^bi[mcsv][aoei]%d%d%d%d%d%d%d%d%d%d$' ) and`
`      not id:match( '^Mi[sm][eoa]%d%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<http://catalogo.bne.es/uhtbin/authoritybrowse.cgi?action=display&authority_id=>`'..id..' '..id..']'..p.getCatForId( 'BNE' ) --no https as of 9/2019`

end

function p.bnfLink( id )

`   --P268's format regex: \d{8}[0-9bcdfghjkmnpqrstvwxz] (e.g. 123456789)`
`   if not id:match( '^c?b?%d%d%d%d%d%d%d%d[0-9bcdfghjkmnpqrstvwxz]$' ) then`
`       return false`
`   end`
`   --Add cb prefix if it has been removed`
`   if not id:match( '^cb.+$' ) then`
`       id = 'cb'..id`
`   end`
`   return '[`<https://catalogue.bnf.fr/ark:/12148/>`'..id..' '..id..'] [`<https://data.bnf.fr/ark:/12148/>`'..id..' (data)]'..p.getCatForId( 'BNF' )`

end

function p.botanistLink( id )

`   --P428's format regex: ('t )?(d')?(de )?(la )?(van (der )?)?(Ma?c)?(De)?(Di)?\p{Lu}?C?['\p{Ll}]*([-'. ]*(van )?(y )?(d[ae][nr]?[- ])?(Ma?c)?[\p{Lu}bht]?C?['\p{Ll}]*)*\.? ?f?\.? (e.g. L.)`
`   --not easily/meaningfully implementable in Lua's regex since "(this)?" is not allowed...`
`   if not mw.ustring.match( id, "^[%u%l%d%. '-]+$" ) then --better than nothing`
`       return false`
`   end`
`   local id2 = id:gsub(' +', '%%20')`
`   return '[`<https://www.ipni.org/ipni/advAuthorSearch.do?find_abbreviation=>`'..id2..' '..id..']'..p.getCatForId( 'Botanist' )`

end

function p.bpnLink( id )

`   --P651's format regex: \d{6,8} (e.g. 00123456)`
`   if not id:match( '^%d%d%d%d%d%d%d%d$' ) and --original format regex, changed 8/2019 to`
`      not id:match( '^0?%d%d%d%d%d%d%d$' ) and --allow 1-2 leading 0s, allowed by the website`
`      not id:match( '^0?0?%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<http://www.biografischportaal.nl/en/persoon/>`'..id..' '..id..']'..p.getCatForId( 'BPN' ) --no https as of 9/2019`

end

function p.canticLink( id )

`   --P1273's format regex: a\d{7}[0-9x] (e.g. a10640745)`
`   if not id:match( '^a%d%d%d%d%d%d%d[%dx]$' ) then`
`       return false`
`   end`
`   return '[`<http://cantic.bnc.cat/registres/CUCId/>`'..id..' '..id..']'..p.getCatForId( 'CANTIC' ) --no https as of 10/2019`

end

function p.ciniiLink( id )

`   --P271's format regex: DA\d{7}[\dX] (e.g. DA12345678)`
`   if not id:match( '^DA%d%d%d%d%d%d%d[%dX]$' ) then`
`       return false`
`   end`
`   return '[`<https://ci.nii.ac.jp/author/>`'..id..'?l=en '..id..']'..p.getCatForId( 'CINII' )`

end

function p.daaoLink( id )

`   --P1707's format regex: [a-z\-]+\d* (e.g. rolf-harris)`
`   if not id:match( '^[a-z%-]+%d*$' ) then`
`       return false`
`   end`
`   return '[`<https://www.daao.org.au/bio/>`'..id..' '..id..']'..p.getCatForId( 'DAAO' )`

end

function p.dblpLink( id )

`   --P2456's format regex: \d{2,3} /\d+(-\d+)?|[a-z] /[a-zA-Z][0-9A-Za-z]*(-\d+)? (e.g. 123/123)`
`   if not id:match( '^%d%d%d?/%d+$' ) and`
`      not id:match( '^%d%d%d?/%d+%-%d+$' ) and`
`      not id:match( '^[a-z]/[a-zA-Z][0-9A-Za-z]*$' ) and`
`      not id:match( '^[a-z]/[a-zA-Z][0-9A-Za-z]*%-%d+$' ) then`
`       return false`
`   end`
`   return '[`<https://dblp.org/pid/>`'..id..' '..id..']'..p.getCatForId( 'DBLP' )`

end

function p.dsiLink( id )

`   --P2349's format regex: [1-9]\d* (e.g. 1538)`
`   if not id:match( '^[1-9]%d*$' ) then`
`       return false`
`   end`
`   return '[`<http://www.uni-stuttgart.de/hi/gnt/dsi2/index.php?table_name=dsi&function=details&where_field=id&where_value=>`'..id..' '..id..']'..p.getCatForId( 'DSI' )`

end

function p.fnzaLink( id )

`   --P6792's format regex: [1-9]\d* (e.g. 9785)`
`   if not id:match( '^[1-9]%d*$' ) then`
`       return false`
`   end`
`   return '[`<https://findnzartists.org.nz/artist/>`'..id..'/ '..id..']'..p.getCatForId( 'FNZA' )`

end

function p.gndLink( id )

`   --P227's format regex: 1[012]?\d{7}[0-9X]|[47]\d{6}-\d|[1-9]\d{0,7}-[0-9X]|3\d{7}[0-9X] (e.g. 4079154-3)`
`   if not id:match( '^1[012]?%d%d%d%d%d%d%d[0-9X]$' ) and`
`      not id:match( '^[47]%d%d%d%d%d%d%-%d$' ) and`
`      not id:match( '^[1-9]%d?%d?%d?%d?%d?%d?%d?%-[0-9X]$' ) and`
`      not id:match( '^3%d%d%d%d%d%d%d[0-9X]$' ) then`
`       return false`
`   end`
`   return '[`<https://d-nb.info/gnd/>`'..id..' '..id..']'..p.getCatForId( 'GND' )`

end

function p.hdsLink( id )

`   --P902's format regex: \d{6} (e.g. 050123)`
`   if not id:match( '^%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<https://hls-dhs-dss.ch/fr/articles/>`'..id..' '..id..']'..p.getCatForId( 'HDS' )`

end

function p.iaafLink( id )

`   --P1146's format regex: [0-9][0-9]* (e.g. 012)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<https://www.iaaf.org/athletes/_/>`'..id..' '..id..']'..p.getCatForId( 'IAAF' )`

end

function p.iciaLink( id )

`   --P1736's format regex: \d+ (e.g. 1)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<https://www.imj.org.il/artcenter/newsite/en/?artist=>`'..id..' '..id..']'..p.getCatForId( 'ICIA' )`

end

function p.isniLink( id )

`   id = p.validateIsni( id ) --e.g. 0000-0000-6653-4145`
`   if not id then`
`       return false`
`   end`
`   return '[`<http://isni.org/isni/>`'..id..' '..id:sub( 1, 4 )..' '..id:sub( 5, 8 )..' '..id:sub( 9, 12 )..' '..id:sub( 13, 16 )..']'..p.getCatForId( 'ISNI' ) --no https as of 9/2019`

end

function p.jocondeLink( id )

`   --P347's format regex: [\-0-9A-Za-z]{11} (e.g. 12345678901)`
`   local regex = '^'..string.rep('[%-0-9A-Za-z]', 11)..'$'`
`   if not id:match( regex ) then`
`       return false`
`   end`
`   return '[`<https://www.pop.culture.gouv.fr/notice/joconde/>`'..id..' '..id..']'..p.getCatForId( 'Joconde' )`

end

function p.kulturnavLink( id )

`   --P1248's format regex: [0-9a-f]{8}\-[0-9a-f]{4}\-[0-9a-f]{4}\-[0-9a-f]{4}\-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<http://kulturnav.org/>`'..id..' '..id..']'..p.getCatForId( 'KULTURNAV' ) --no https as of 9/2019`

end

function p.lccnLink( id )

`   local parts = p.splitLccn( id ) --e.g. n78039510`
`   if not parts then`
`       return false`
`   end`
`   local lccnType = parts[1] ~= 'sh' and 'names' or 'subjects'`
`   id = parts[1] .. parts[2] .. p.append( parts[3], '0', 6 )`
`   return '[`<https://id.loc.gov/authorities/>`'..lccnType..'/'..id..' '..id..']'..p.getCatForId( 'LCCN' )`

end

function p.lirLink( id )

`   --P886's format regex: \d+ (e.g. 1)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<http://www.e-lir.ch/e-LIR___Lexicon>`.'..id..'.450.0.html '..id..']'..p.getCatForId( 'LIR' ) --no https as of 9/2019`

end

function p.lnbLink( id )

`   --P1368's format regex: \d{9} (e.g. 123456789)`
`   if not id:match( '^%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<https://kopkatalogs.lv/F?func=direct&local_base=lnc10&doc_number=>`'..id..'&P_CON_LNG=ENG '..id..']'..p.getCatForId( 'LNB' )`

end

function p.leonoreLink( id )

`   --P640's format regex: LH/\d{1,4}/\d{1,3}|19800035/\d{1,4}/\d{1,5}(Bis)?|C/0/\d{1,2} (e.g. LH/2064/18)`
`   if not id:match( '^LH/%d%d?%d?%d?/%d%d?%d?$' ) and             --IDs from       LH/1/1 to         LH/2794/54 (legionaries)`
`      not id:match( '^19800035/%d%d?%d?%d?/%d%d?%d?%d?%d?$' ) and --IDs from 19800035/1/1 to 19800035/385/51670 (legionnaires who died 1954-1977 & some who died < 1954)`
`      not id:match( '^C/0/%d%d?$' ) then                          --IDs from        C/0/1 to             C/0/84 (84 famous legionaries)`
`       return false`
`   end`
`   return '[`<http://www.culture.gouv.fr/public/mistral/leonore_fr?ACTION=CHERCHER&FIELD_1=COTE&VALUE_1=>`'..id..' '..id..']'..p.getCatForId( 'Léonore' ) --no https as of 9/2019`

end

function p.mbaLink( id )

`   --P434's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/artist/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz' ) --special category name`

end

function p.mbareaLink( id )

`   --P982's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/area/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz area' ) --special category name`

end

function p.mbiLink( id )

`   --P1330's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/instrument/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz instrument' ) --special category name`

end

function p.mblLink( id )

`   --P966's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/label/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz label' ) --special category name`

end

function p.mbpLink( id )

`   --P1004's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/place/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz place' ) --special category name`

end

function p.mbrgLink( id )

`   --P436's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/release-group/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz release group' ) --special category name`

end

function p.mbsLink( id )

`   --P1407's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/series/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz series' ) --special category name`

end

function p.mbwLink( id )

`   --P435's format regex: [0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12} (e.g. 12345678-1234-1234-1234-1234567890AB)`
`   if not id:match( '^%x%x%x%x%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%-%x%x%x%x%x%x%x%x%x%x%x%x$' ) then`
`       return false`
`   end`
`   return '[`<https://musicbrainz.org/work/>`'..id..' '..id..']'..p.getCatForId( 'MusicBrainz work' ) --special category name`

end

function p.mgpLink( id )

`   --P549's format regex: \d{1,6} (e.g. 123456)`
`   if not id:match( '^%d%d?%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://genealogy.math.ndsu.nodak.edu/id.php?id=>`'..id..' '..id..']'..p.getCatForId( 'MGP' )`

end

function p.naraLink( id )

`   --P1225's format regex: ^([1-9]\d{0,8})$ (e.g. 123456789)`
`   if not id:match( '^[1-9]%d?%d?%d?%d?%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://catalog.archives.gov/id/>`'..id..' '..id..']'..p.getCatForId( 'NARA' )`

end

function p.nclLink( id )

`   --P1048's format regex: \d+ (e.g. 1081436)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<http://aleweb.ncl.edu.tw/F/?func=accref&acc_sequence=>`'..id..'&CON_LNG=ENG '..id..']'..p.getCatForId( 'NCL' ) --no https as of 9/2019`

end

function p.ndlLink( id )

`   --P349's format regex: 0?\d{8} (e.g. 012345678)`
`   if not id:match( '^0?%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<https://id.ndl.go.jp/auth/ndlna/>`'..id..' '..id..']'..p.getCatForId( 'NDL' )`

end

function p.ngvLink( id )

`   --P2041's format regex: \d+ (e.g. 12354)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<https://www.ngv.vic.gov.au/explore/collection/artist/>`'..id..'/ '..id..']'..p.getCatForId( 'NGV' )`

end

function p.nkcLink( id )

`   --P691's format regex: [a-z]{2,4}[0-9]{2,14} (e.g. abcd12345678901234)`
`   if not id:match( '^[a-z][a-z][a-z]?[a-z]?%d%d%d?%d?%d?%d?%d?%d?%d?%d?%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://aleph.nkp.cz/F/?func=find-c&local_base=aut&ccl_term=ica=>`'..id..'&CON_LNG=ENG '..id..']'..p.getCatForId( 'NKC' )`

end

function p.nlaLink( id )

`   --P409's format regex: [1-9][0-9]{0,11} (e.g. 123456789012)`
`   if not id:match( '^[1-9]%d?%d?%d?%d?%d?%d?%d?%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://nla.gov.au/anbd.aut-an>`'..id..' '..id..']'..p.getCatForId( 'NLA' )`

end

function p.nlgLink( id )

`   --P3348's format regex: [1-9]\d* (e.g. 1)`
`   if not id:match( '^[1-9]%d*$' ) then`
`       return false`
`   end`
`   return '[`<https://data.nlg.gr/resource/authority/record>`'..id..' '..id..']'..p.getCatForId( 'NLG' )`

end

function p.nliLink( id )

`   --P949's format regex: \d{9} (e.g. 123456789)`
`   if not id:match( '^%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<http://uli.nli.org.il/F/?func=direct&doc_number=>`'..id..'&local_base=nlx10'..' '..id..']'..p.getCatForId( 'NLI' )`

end

function p.nlkLink( id )

`   --P5034's format regex: KA.(19|20).{7} (e.g. KAC201501465)`
`   if not id:match( '^KA.19.......$' ) and`
`      not id:match( '^KA.20.......$' ) then`
`       return false`
`   end`
`   return '[`<https://nl.go.kr/authorities/resource/>`'..id..' '..id..']'..p.getCatForId( 'NLK' )`

end

function p.nlpLink( id )

`   --P1695's format regex: 9810[0-9]\d* or A[0-9]{7}[0-9X] (e.g. 9810123456789012345 or A10414836)`
`   if not id:match( '^9810%d+$' ) and`
`      not id:match( '^A%d%d%d%d%d%d%d[%dX]$' ) then`
`       return false`
`   end`
`   return '[`<https://tools.wmflabs.org/wikidata-externalid-url?p=1695&id=>`'..id..' '..id..']'..p.getCatForId( 'NLP' )`

end

function p.nlrLink( id )

`   --P1003's format regex: \d{9} (e.g. 123456789)`
`   if not id:match( '^%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<http://alephnew.bibnat.ro:8991/F?func=find-b&request=>`'..id..'&find_code=SYS&adjacent=Y&local_base=NLR10 '..id..']'..p.getCatForId( 'NLR' )`

end

function p.nskLink( id )

`   --P1375's format regex: \d{9} (e.g. 123456789)`
`   if not id:match( '^%d%d%d%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<http://katalog.nsk.hr/F/?func=direct&doc_number=>`'..id..'&local_base=nsk10 '..id..']'..p.getCatForId( 'NSK' ) --no https as of 9/2019`

end

function p.ntaLink( id )

`   --P1006's format regex: \d{8}[\dX] (e.g. 12345678X)`
`   if not id:match( '^%d%d%d%d%d%d%d%d[%dX]$' ) then`
`       return false`
`   end`
`   return '[`<http://data.bibliotheken.nl/id/thes/p>`'..id..' '..id..']'..p.getCatForId( 'NTA' )`

end

function p.orcidLink( id )

`   id = p.validateIsni( id ) --e.g. 0000-0002-7398-5483`
`   if not id then`
`       return false`
`   end`
`   id = id:sub( 1, 4 )..'-'..id:sub( 5, 8 )..'-'..id:sub( 9, 12 )..'-'..id:sub( 13, 16 )`
`   return '[`<https://orcid.org/>`'..id..' '..id..']'..p.getCatForId( 'ORCID' )`

end

function p.picLink( id )

`   --P2750's format regex: [1-9]\d* (e.g. 1)`
`   if not id:match( '^[1-9]%d*$' ) then`
`       return false`
`   end`
`   return '[`<https://pic.nypl.org/constituents/>`'..id..' '..id..']'..p.getCatForId( 'PIC' )`

end

function p.ridLink( id )

`   --P1053's format regex: [A-Z]-\d{4}-(19|20)\d\d (e.g. A-1234-1934)`
`   if not id:match( '^[A-Z]%-%d%d%d%d%-19%d%d$' ) and`
`      not id:match( '^[A-Z]%-%d%d%d%d%-20%d%d$' ) then`
`       return false`
`   end`
`   return '[`<https://www.researcherid.com/rid/>`'..id..' '..id..']'..p.getCatForId( 'RID' )`

end

function p.reroLink( id )

`   --P3065's format regex: 0[1-2]-[A-Z0-9]{1,10} (e.g. 02-A012345678)`
`   if not id:match( '^0[1-2]%-[A-Z%d][A-Z%d]?[A-Z%d]?[A-Z%d]?[A-Z%d]?[A-Z%d]?[A-Z%d]?[A-Z%d]?[A-Z%d]?[A-Z%d]?$' ) then`
`       return false`
`   end`
`   return '[`<http://data.rero.ch/>`'..id..' '..id..']'..p.getCatForId( 'RERO' )`

end

function p.rkdartistsLink( id )

`   --P650's format regex: [1-9]\d{0,5} (e.g. 123456)`
`   if not id:match( '^[1-9]%d?%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://rkd.nl/en/explore/artists/>`'..id..' '..id..']'..p.getCatForId( 'RKDartists' )`

end

function p.rkdidLink( id )

`   --P350's format regex: [1-9]\d{0,5} (e.g. 123456)`
`   if not id:match( '^[1-9]%d?%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://rkd.nl/nl/explore/images/>`'..id..' '..id..']'..p.getCatForId( 'RKDID' )`

end

function p.rslLink( id )

`   --P947's format regex: \d{1,9} (e.g. 123456789)`
`   if not id:match( '^%d%d?%d?%d?%d?%d?%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<http://aleph.rsl.ru/F?func=find-b&find_code=SYS&adjacent=Y&local_base=RSL11&request=>`'..id..'&CON_LNG=ENG '..id..']'..p.getCatForId( 'RSL' ) --no https as of 9/2019`

end

function p.sbnLink( id )

`   --P396's format regex: IT\\ICCU\\(\d{10}|\D\D[\D\d]\D\\\d{6}) (e.g. IT\ICCU\CFIV\000163)`
`   if not id:match( '^IT\\ICCU\\%d%d%d%d%d%d%d%d%d%d$' ) and`
`      not id:match( '^IT\\ICCU\\%u%u[%u%d]%u\\%d%d%d%d%d%d$' ) then --legacy: %u used here instead of %D (but the faulty ID cat is empty, out of ~12k uses)`
`       return false`
`   end`
`   return '[`<https://opac.sbn.it/opacsbn/opac/iccu/scheda_authority.jsp?bid=>`'..id..' '..id..']'..p.getCatForId( 'SBN' )`

end

function p.selibrLink( id )

`   --P906's format regex: [1-9]\d{4,5} (e.g. 123456)`
`   if not id:match( '^[1-9]%d%d%d%d%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://libris.kb.se/auth/>`'..id..' '..id..']'..p.getCatForId( 'SELIBR' )`

end

function p.sikartLink( id )

`   --P781's format regex: \d{7,9} (e.g. 123456789)`
`   if not id:match( '^%d%d%d%d%d%d%d%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<http://www.sikart.ch/KuenstlerInnen.aspx?id=>`'..id..'&lng=en '..id..']'..p.getCatForId( 'SIKART' ) --no https as of 9/2019`

end

function p.snacLink( id )

`   --P3430's format regex: \d*[A-Za-z][0-9A-Za-z]* (e.g. A)`
`   if not id:match( '^%d*[A-Za-z][0-9A-Za-z]*$' ) then`
`       return false`
`   end`
`   return '[`<https://snaccooperative.org/ark:/99166/>`'..id..' '..id..']'..p.getCatForId( 'SNAC-ID' )`

end

function p.sudocLink( id )

`   --P269's format regex: (\d{8}[\dX]|) (e.g. 026927608)`
`   if not id:match( '^%d%d%d%d%d%d%d%d[%dxX]$' ) then --legacy: allow lowercase 'x'`
`       return false`
`   end`
`   return '[`<https://www.idref.fr/>`'..id..' '..id..']'..p.getCatForId( 'SUDOC' )`

end

function p.s2authoridLink( id )

`   --P4012's format regex: [1-9]\d* (e.g. 1796130)`
`   if not id:match( '^[1-9]%d*$' ) then`
`       return false`
`   end`
`   return '[`<https://www.semanticscholar.org/author/>`'..id..' '..id..']'..p.getCatForId( 'Semantic Scholar author' ) --special category name`

end

function p.ta98Link( id )

`   --P1323's format regex: A\d{2}\.\d\.\d{2}\.\d{3}[FM]? (e.g. A12.3.45.678)`
`   if not id:match( '^A%d%d%.%d%.%d%d%.%d%d%d[FM]?$' ) then`
`       return false`
`   end`
`   return '[`<http://tools.wmflabs.org/wikidata-externalid-url/?p=1323&url_prefix=https:%2F%2Fwww.unifr.ch%2Fifaa%2FPublic%2FEntryPage%2FTA98%20Tree%2FEntity%20TA98%20EN%2F&url_suffix=%20Entity%20TA98%20EN.htm&id=>`'..id..' '..id..']'..p.getCatForId( 'TA98' )`

end

function p.tdviaLink( id )

`   --P7314's format regex: [a-z/-]+] (e.g. barkan-omer-lutfi)`
`   if not id:match( '^[a-z/-]+$' ) then`
`       return false`
`   end`
`   return '[`<https://islamansiklopedisi.org.tr/>`'..id..' '..id..']'..p.getCatForId( 'TDVİA' )`

end

function p.teLink( id )

`   --P1693's format regex: E[1-8]\.\d{1,2}\.\d{1,2}\.\d{1,2}\.\d{1}\.\d{1}\.\d{1,3} (e.g. E1.23.45.67.8.9.0)`
`   local e1, e2 = id:match( '^E([1-8])%.(%d%d?)%.%d%d?%.%d%d?%.%d%.%d%.%d%d?%d?$' )`
`   if not e1 then`
`       return false`
`   end`
`   local TEnum = 'TEe0'..e1 --no formatter URL in WD, probably due to this complexity`
`   if e1 == '5' or e1 == '7' then`
`       if #e2 == 1 then e2 = '0'..e2 end`
`       TEnum = TEnum..e2`
`   end`
`   return '[`<http://www.unifr.ch/ifaa/Public/EntryPage/ViewTE/>`'..TEnum..'.html '..id..']'..p.getCatForId( 'TE' )`

end

function p.tepapaLink( id )

`   --P3544's format regex: \d+ (e.g. 1)`
`   if not id:match( '^%d+$' ) then`
`       return false`
`   end`
`   return '[`<https://collections.tepapa.govt.nz/agent/>`'..id..' '..id..']'..p.getCatForId( 'TePapa' )`

end

function p.thLink( id )

`   --P1694's format regex: H\d\.\d{2}\.\d{2}\.\d\.\d{5} (e.g. H1.23.45.6.78901)`
`   local h1, h2 = id:match( '^H(%d)%.(%d%d)%.%d%d%.%d%.%d%d%d%d%d$' )`
`   if not h1 then`
`       return false`
`   end`
`   local THnum = 'THh'..h1..h2 --no formatter URL in WD, probably due to this complexity`
`   return '[`<http://www.unifr.ch/ifaa/Public/EntryPage/ViewTH/>`'..THnum..'.html '..id..']'..p.getCatForId( 'TH' )`

end

function p.tlsLink( id )

`   local id2 = id:gsub(' +', '_')`
`   --P1362's format regex: \p{Lu}[\p{L}\d_',\.\-`\(\)`\*/–]{3,59} (e.g. Abcd)`
`   local class = "[%a%d_',%.%-%(%)%*/–]"`
`   local regex = "^%u"..string.rep(class, 3)..string.rep(class.."?", 56).."$"`
`   if not mw.ustring.match( id2, regex ) then`
`       return false`
`   end`
`   return '[`<http://tls.theaterwissenschaft.ch/wiki/>`'..id2..' '..id..']'..p.getCatForId( 'TLS' ) --no https as of 9/2019`

end

function p.troveLink( id )

`   --P1315's format regex: [1-9]\d{5,7} (e.g. 12345678)`
`   if not id:match( '^[1-9]%d%d%d%d%d%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://trove.nla.gov.au/people/>`'..id..' '..id..']'..p.getCatForId( 'Trove' )`

end

function p.ulanLink( id )

`   --P245's format regex: 500\d{6} (e.g. 500123456)`
`   if not id:match( '^500%d%d%d%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<https://www.getty.edu/vow/ULANFullDisplay?find=&role=&nation=&subjectid=>`'..id..' '..id..']'..p.getCatForId( 'ULAN' )`

end

function p.uscongressLink( id )

`   --P1157's format regex: [A-Z]00[01]\d{3} (e.g. A000123)`
`   if not id:match( '^[A-Z]00[01]%d%d%d$' ) then`
`       return false`
`   end`
`   return '[`<http://bioguide.congress.gov/scripts/biodisplay.pl?index=>`'..id..' '..id..']'..p.getCatForId( 'USCongress' ) --no https as of 9/2019`

end

function p.viafLink( id )

`   --P214's format regex: [1-9]\d(\d{0,7}|\d{17,20}) (e.g. 123456789, 1234567890123456789012)`
`   if not id:match( '^[1-9]%d%d?%d?%d?%d?%d?%d?%d?$' ) and`
`      not id:match( '^[1-9]%d%d%d%d%d%d%d%d%d%d%d%d%d%d%d%d%d%d%d?%d?%d?$' ) then`
`       return false`
`   end`
`   return '[`<https://viaf.org/viaf/>`'..id..' '..id..']'..p.getCatForId( 'VIAF' )`

end

\--[=========================== Helper functions =============================](https://ko.wikipedia.org/wiki/===========================_Helper_functions_============================= "wikilink")

function p.append(str, c, length)

`   while str:len() < length do`
`       str = c .. str`
`   end`
`   return str`

end

\--Returns the ISNI check digit isni must be a string where the 15 first elements are digits, e.g. 0000000066534145 function p.getIsniCheckDigit( isni )

`   local total = 0`
`   for i = 1, 15 do`
`       local digit = isni:byte( i ) - 48 --Get integer value`
`       total = (total + digit) * 2`
`   end`
`   local remainder = total % 11`
`   local result = (12 - remainder) % 11`
`   if result == 10 then`
`       return "X"`
`   end`
`   return tostring( result )`

end

\--Validate ISNI (and ORCID) and retuns it as a 16 characters string or returns false if it's invalid --See <http://support.orcid.org/knowledgebase/articles/116780-structure-of-the-orcid-identifier> function p.validateIsni( id )

`   --P213 (ISNI) format regex: [0-9]{4} [0-9]{4} [0-9]{4} [0-9]{3}[0-9X] (e.g. 0000-0000-6653-4145)`
`   --P496 (ORCID) format regex: 0000-000(1-[5-9]|2-[0-9]|3-[0-4])\d{3}-\d{3}[\dX] (e.g. 0000-0002-7398-5483)`
`   id = id:gsub( '[ %-]', '' ):upper()`
`   if not id:match( '^%d%d%d%d%d%d%d%d%d%d%d%d%d%d%d[%dX]$' ) then`
`       return false`
`   end`
`   if p.getIsniCheckDigit( id ) ~= string.char( id:byte( 16 ) ) then`
`       return false`
`   end`
`   return id`

end

function p.splitLccn( id )

`   --P244's format regex: (n|nb|nr|no|ns|sh)([4-9][0-9]|00|20[0-1][0-9])[0-9]{6} (e.g. n78039510)`
`   if id:match( '^%l%l?%l?%d%d%d%d%d%d%d%d%d?%d?$' ) then`
`       id = id:gsub( '^(%l+)(%d+)(%d%d%d%d%d%d)$', '%1/%2/%3' )`
`   end`
`   if id:match( '^%l%l?%l?/%d%d%d?%d?/%d+$' ) then`
`       return mw.text.split( id, '/' )`
`   end`
`   return false`

end

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Wikidata, navigation bar, and documentation functions](https://ko.wikipedia.org/wiki/Wikidata,_navigation_bar,_and_documentation_functions "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

function p.getIdsFromWikidata( itemId, property )

`   local ids = {}`
`   local statements = mw.wikibase.getBestStatements( itemId, property )`
`   if statements then`
`       for _, statement in ipairs( statements ) do`
`           if statement.mainsnak.datavalue then`
`               table.insert( ids, statement.mainsnak.datavalue.value )`
`           end`
`       end`
`   end`
`   return ids`

end

function p.matchesWikidataRequirements( itemId, reqs )

`   for _, group in ipairs( reqs ) do`
`       local property = 'P'..group[1]`
`       local qid = group[2]`
`       local statements = mw.wikibase.getBestStatements( itemId, property )`
`       if statements then`
`           for _, statement in ipairs( statements ) do`
`               if statement.mainsnak.datavalue then`
`                   if statement.mainsnak.datavalue.value['numeric-id'] == qid then`
`                       return true`
`   end end end end end`
`   return false`

end

function p.createRow( id, label, rawValue, link, withUid, specialCat )

`   if link then`
`       if withUid then`
`           return '*`<span class="nowrap">`'..label..' `<span class="uid">`'..link..'`</span></span>`\n'`
`       end`
`       return '*`<span class="nowrap">`'..label..' '..link..'`</span>`\n'`
`   end`

`   local catName = '잘못된 '..(specialCat or id)..' 식별자를 포함한 위키백과 문서'`
`   return '* `<span class="error">`'..id..' id '..rawValue..' 값은 유효하지 않습니다.`</span>[`분류:'..catName..'`](https://ko.wikipedia.org/wiki/분류:'..catName..' "wikilink")`'..p.redCatLink(catName)..'\n'`

end

\-- Creates a human-readable standalone wikitable version of p.conf, and tracking categories with page counts, for use in the documentation function p.docConfTable( frame )

`   local wikiTable = '{| class="wikitable sortable"\n'..`
`                     '! rowspan=2 | 변수\n'..`
`                     '! rowspan=2 | 레이블\n'..`
`                     '! rowspan=2; data-sort-type=number | 위키데이터 속성\n'..`
`                     '! colspan=4 | 추적용 분류와 문서 수\n'..`
`                     '|-\n'..`
`                     '! `[`문서`](https://ko.wikipedia.org/wiki/:분류:전거_통제_정보를_포함한_위키백과_문서 "wikilink")`\n'..`
`                     '! `[`사용자``   ``문서`](https://ko.wikipedia.org/wiki/:분류:전거_통제_정보를_포함한_사용자_문서 "wikilink")`\n'..`
`                     '! `[`기타``   ``문서`](https://ko.wikipedia.org/wiki/:분류:전거_통제_정보를_포함한_기타_문서 "wikilink")`\n'..`
`                     '! `[`잘못된``   ``ID`](https://ko.wikipedia.org/wiki/:분류:잘못된_전거_통제_정보를_포함한_위키백과_문서 "wikilink")`\n'..`
`                     '|-\n'`
`   `
`   local lang = mw.getContentLanguage()`
`   for _, conf in pairs( p.conf ) do`
`       local param, link, pid = conf[1], conf[2], conf[3]`
`       local category = conf.category or param`
`       local args = { id = 'f', pid }`
`       local wpl = frame:expandTemplate{ title = '위키데이터 속성 링크', args = args }`
`       --cats`
`       local articleCat = category..' 식별자를 포함한 위키백과 문서'`
`       local userCat =    category..' 식별자를 포함한 사용자 문서'`
`       local miscCat =    category..' 식별자를 포함한 기타 문서'`
`       local faultyCat =  '잘못된 '..category..' 식별자를 포함한 위키백과 문서'`
`       --counts`
`       local articleCount = lang:formatNum( mw.site.stats.pagesInCategory(articleCat, 'pages') )`
`       local userCount =    lang:formatNum( mw.site.stats.pagesInCategory(userCat, 'pages') )`
`       local miscCount =    lang:formatNum( mw.site.stats.pagesInCategory(miscCat, 'pages') )`
`       local faultyCount =  lang:formatNum( mw.site.stats.pagesInCategory(faultyCat, 'pages') )`
`       --concat`
`       wikiTable = wikiTable..'\n'..`
`                   '|-\n'..`
`                   '||'..param..`
`                   '||'..link..`
`                   '||data-sort-value='..pid..'|'..wpl..`
`                   '||style="text-align: right;"|`[`'..articleCount..'`](https://ko.wikipedia.org/wiki/:분류:'..articleCat..' "wikilink")`'..`
`                   '||style="text-align: right;"|`[`'..``   ``userCount..'`](https://ko.wikipedia.org/wiki/:분류:'.._userCat..' "wikilink")`'..`
`                   '||style="text-align: right;"|`[`'..``   ``miscCount..'`](https://ko.wikipedia.org/wiki/:분류:'.._miscCat..' "wikilink")`'..`
`                   '||style="text-align: right;"|`[`'..``   ``faultyCount..'`](https://ko.wikipedia.org/wiki/:분류:'.._faultyCat..' "wikilink")`'`
`   end`
`   return wikiTable..'\n|}'`

end

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Configuration](https://ko.wikipedia.org/wiki/Configuration "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

\-- Check that the Wikidata item has this property--\>value before adding it local reqs = {}

\-- Parameter format: { parameter name, label, propertyId \# in Wikidata, formatting/validation function } p.conf = {

`   { 'AAG', '`[`AAG`](https://ko.wikipedia.org/wiki/:en:Auckland_Art_Gallery_Toi_o_Tāmaki "wikilink")`', 3372, p.aagLink },`
`   { 'ACM-DL', '`[`ACM``   ``DL`](https://ko.wikipedia.org/wiki/ACM_디지털_라이브러리 "wikilink")`', 864, p.acmLink },`
`   { 'ADB', '`[`ADB`](https://ko.wikipedia.org/wiki/:en:Australian_Dictionary_of_Biography "wikilink")`', 1907, p.adbLink },`
`   { 'AGSA', '`[`AGSA`](https://ko.wikipedia.org/wiki/:en:Art_Gallery_of_South_Australia "wikilink")`', 6804, p.agsaLink },`
`   { 'Autores.uy', '`[`autores.uy`](https://ko.wikipedia.org/wiki/autores.uy "wikilink")`', 2558, p.autoresuyLink }, -- 맨 앞이 소문자로 시작하는 경우 ``가 동작하지 않아 우선 수정함 (autores.uy → Autores.uy)`
`   { 'AWR', '`[`AWR`](https://ko.wikipedia.org/wiki/:en:Australian_Women/'s_Register "wikilink")`', 4186, p.awrLink },`
`   { 'BALaT', '`[`BALaT`](https://ko.wikipedia.org/wiki/:en:Royal_Institute_for_Cultural_Heritage#Online_artworks_pages "wikilink")`', 3293, p.balatLink },`
`   { 'BIBSYS', '`[`BIBSYS`](../Page/BIBSYS.md "wikilink")`', 1015, p.bibsysLink },`
`   { 'Bildindex', '`[`Bildindex`](https://ko.wikipedia.org/wiki/:en:Marburg_Picture_Index "wikilink")`', 2092, p.bildLink },`
`   { 'BNC', '`[`BNC`](https://ko.wikipedia.org/wiki/칠레_국립도서관 "wikilink")`', 1890, p.bncLink }, --initially commented due to excessive WD ID errors (many bad IDs since removed)`
`   { 'BNE', '`[`BNE`](../Page/스페인_국립도서관.md "wikilink")`', 950, p.bneLink },`
`   { 'BNF', '`[`BNF`](../Page/프랑스_국립도서관.md "wikilink")`', 268, p.bnfLink },`
`   { 'Botanist', '`[`Botanist`](https://ko.wikipedia.org/wiki/:en:Author_citation_\(botany\) "wikilink")`', 428, p.botanistLink },`
`   { 'BPN', '`[`BPN`](https://ko.wikipedia.org/wiki/:en:Biografisch_Portaal "wikilink")`', 651, p.bpnLink },`
`   { 'CANTIC', '`[`CANTIC`](https://ko.wikipedia.org/wiki/:en:Name_and_Title_Authority_File_of_Catalonia "wikilink")`', 1273, p.canticLink },`
`   { 'CINII', '`[`CiNii`](https://ko.wikipedia.org/wiki/CiNii "wikilink")`', 271, p.ciniiLink },`
`   { 'DAAO', '`[`DAAO`](https://ko.wikipedia.org/wiki/:en:Dictionary_of_Australian_Artists "wikilink")`', 1707, p.daaoLink },`
`   { 'DBLP', '`[`DBLP`](https://ko.wikipedia.org/wiki/DBLP "wikilink")`', 2456, p.dblpLink },`
`   { 'DSI', '`[`DSI`](https://ko.wikipedia.org/wiki/:en:Stuttgart_Database_of_Scientific_Illustrators_1450–1950 "wikilink")`', 2349, p.dsiLink },`
`   { 'FNZA', '`[`FNZA`](https://ko.wikipedia.org/wiki/:d:Property:P6792 "wikilink")`', 6792, p.fnzaLink },`
`   { 'GND', '`[`GND`](../Page/게마인자메_노름다타이.md "wikilink")`', 227, p.gndLink },`
`   { 'HDS', '`[`HDS`](../Page/스위스_역사_사전.md "wikilink")`', 902, p.hdsLink },`
`   { 'IAAF', '`[`IAAF`](../Page/국제_육상_경기_연맹.md "wikilink")`', 1146, p.iaafLink },`
`   { 'ICIA', '`[`ICIA`](https://ko.wikipedia.org/wiki/:en:Information_Center_for_Israeli_Art "wikilink")`', 1736, p.iciaLink },`
`   { 'ISNI', '`[`ISNI`](../Page/국제_표준_명칭_식별자.md "wikilink")`', 213, p.isniLink },`
`   { 'Joconde', '`[`Joconde`](https://ko.wikipedia.org/wiki/:en:Joconde "wikilink")`' , 347, p.jocondeLink },`
`   { 'KULTURNAV', '`[`KulturNav`](https://ko.wikipedia.org/wiki/:en:KulturNav "wikilink")`', 1248, p.kulturnavLink },`
`   { 'LCCN', '`[`LCCN`](https://ko.wikipedia.org/wiki/미국_의회도서관_제어_번호 "wikilink")`', 244, p.lccnLink },`
`   { 'LIR', '`[`LIR`](../Page/스위스_역사_사전.md "wikilink")`', 886, p.lirLink },`
`   { 'LNB', '`[`LNB`](https://ko.wikipedia.org/wiki/National_Library_of_Latvia "wikilink")`', 1368, p.lnbLink },`
`   { 'Léonore', '`[`Léonore`](https://ko.wikipedia.org/wiki/:fr:Base_Léonore "wikilink")`', 640, p.leonoreLink },`
`   { 'MBA', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")`', 434, p.mbaLink, category = 'MusicBrainz' }, --special category name`
`   { 'MBAREA', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")`', 982, p.mbareaLink, category = 'MusicBrainz area' }, --special category name`
`   { 'MBI', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")`', 1330, p.mbiLink, category = 'MusicBrainz instrument' }, --special category name`
`   { 'MBL', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")`', 966, p.mblLink, category = 'MusicBrainz label' }, --special category name`
`   { 'MBP', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")`', 1004, p.mbpLink, category = 'MusicBrainz place' }, --special category name`
`   { 'MBRG', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")` 릴리스 그룹', 436, p.mbrgLink, category = 'MusicBrainz release group' }, --special category name`
`   { 'MBS', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")`', 1407, p.mbsLink, category = 'MusicBrainz series' }, --special category name`
`   { 'MBW', '`[`뮤직브레인즈`](../Page/뮤직브레인즈.md "wikilink")` 작품', 435, p.mbwLink, category = 'MusicBrainz work' }, --special category name`
`   { 'MGP', '`[`MGP`](../Page/수학_계보_프로젝트.md "wikilink")`', 549, p.mgpLink },`
`   { 'NARA', '`[`NARA`](../Page/미국_국립문서기록관리청.md "wikilink")`', 1225, p.naraLink },`
`   { 'NCL', '`[`NCL`](https://ko.wikipedia.org/wiki/국가도서관 "wikilink")`', 1048, p.nclLink },`
`   { 'NDL', '`[`NDL`](../Page/일본_국립국회도서관.md "wikilink")`', 349, p.ndlLink },`
`   { 'NGV', '`[`NGV`](https://ko.wikipedia.org/wiki/:en:National_Gallery_of_Victoria "wikilink")`', 2041, p.ngvLink },`
`   { 'NKC', '`[`NKC`](https://ko.wikipedia.org/wiki/체코_국립도서관 "wikilink")`', 691, p.nkcLink },`
`   { 'NLA', '`[`NLA`](https://ko.wikipedia.org/wiki/오스트레일리아_국립도서관 "wikilink")`', 409, p.nlaLink },`
`   { 'NLG', '`[`NLG`](https://ko.wikipedia.org/wiki/그리스_국립도서관 "wikilink")`', 3348, p.nlgLink },`
`   { 'NLI', '`[`NLI`](https://ko.wikipedia.org/wiki/이스라엘_국립도서관 "wikilink")`', 949, p.nliLink },`
`   { 'NLK', '`[`NLK`](../Page/국립중앙도서관.md "wikilink")`', 5034, p.nlkLink },`
`   { 'NLP', '`[`NLP`](../Page/폴란드_국립도서관.md "wikilink")`', 1695, p.nlpLink },`
`   { 'NLR', '`[`NLR`](https://ko.wikipedia.org/wiki/루마니아_국립도서관 "wikilink")`', 1003, p.nlrLink }, --initially commented due to excessive WD ID errors (conflated with National Library of Russia IDs)`
`   { 'NSK', '`[`NSK`](https://ko.wikipedia.org/wiki/자그레브_국립_대학_도서관 "wikilink")`', 1375, p.nskLink },`
`   { 'NTA', '`[`NTA`](https://ko.wikipedia.org/wiki/네덜란드_왕립도서관 "wikilink")`', 1006, p.ntaLink },`
`   { 'ORCID', '`[`ORCID`](../Page/ORCID.md "wikilink")`', 496, p.orcidLink },`
`   { 'PIC', '`[`PIC`](https://ko.wikipedia.org/wiki/:d:Q23892012 "wikilink")`', 2750, p.picLink },`
`   { 'RID', '`[`ResearcherID`](https://ko.wikipedia.org/wiki/:en:ResearcherID "wikilink")`', 1053, p.ridLink },`
`   { 'RERO', '`[`RERO`](https://ko.wikipedia.org/wiki/:en:RERO_\(Library_Network_of_Western_Switzerland\) "wikilink")`', 3065, p.reroLink }, --initially commented due to excessive WD ID errors (regex fixed/relaxed)`
`   { 'RKDartists', '`[`RKD`](https://ko.wikipedia.org/wiki/:en:Netherlands_Institute_for_Art_History#Online_artist_pages "wikilink")`', 650, p.rkdartistsLink },`
`   { 'RKDID', '`[`RKDimages``   ``ID`](https://ko.wikipedia.org/wiki/:d:Q17299580 "wikilink")`', 350, p.rkdidLink },`
`   { 'RSL', '`[`RSL`](../Page/러시아_국립도서관_\(모스크바\).md "wikilink")`', 947, p.rslLink },`
`   { 'SBN', '`[`ICCU`](https://ko.wikipedia.org/wiki/:en:Istituto_Centrale_per_il_Catalogo_Unico "wikilink")`', 396, p.sbnLink },`
`   { 'SELIBR', '`[`SELIBR`](../Page/LIBRIS.md "wikilink")`', 906, p.selibrLink },`
`   { 'SIKART', '`[`SIKART`](https://ko.wikipedia.org/wiki/SIKART "wikilink")`', 781, p.sikartLink },`
`   { 'SNAC-ID', '`[`SNAC`](../Page/SNAC.md "wikilink")`', 3430, p.snacLink },`
`   { 'SUDOC', '`[`SUDOC`](https://ko.wikipedia.org/wiki/프랑스_대학도서관_종합목록 "wikilink")`', 269, p.sudocLink },`
`   { 'S2AuthorId', '`[`S2AuthorId`](https://ko.wikipedia.org/wiki/:en:Semantic_Scholar "wikilink")`', 4012, p.s2authoridLink, category = 'Semantic Scholar author' }, --special category name`
`   { 'TA98', '`[`TA98`](https://ko.wikipedia.org/wiki/:en:Terminologia_Anatomica "wikilink")`', 1323, p.ta98Link },`
`   { 'TDVİA', '`[`TDVİA`](https://ko.wikipedia.org/wiki/:d:Q21527102 "wikilink")`', 7314, p.tdviaLink },`
`   { 'TE', '`[`TE`](https://ko.wikipedia.org/wiki/Terminologia_Embryologica "wikilink")`', 1693, p.teLink },`
`   { 'TePapa', '`[`TePapa`](https://ko.wikipedia.org/wiki/:en:Museum_of_New_Zealand_Te_Papa_Tongarewa "wikilink")`', 3544, p.tepapaLink },`
`   { 'TH', '`[`TH`](https://ko.wikipedia.org/wiki/:en:Terminologia_Histologica "wikilink")`', 1694, p.thLink },`
`   { 'TLS', '`[`TLS`](https://ko.wikipedia.org/wiki/:en:Theaterlexikon_der_Schweiz "wikilink")`', 1362, p.tlsLink },`
`   { 'Trove', '`[`Trove`](https://ko.wikipedia.org/wiki/:en:Trove "wikilink")`', 1315, p.troveLink }, --formerly NLA-person`
`   { 'ULAN', '`[`ULAN`](https://ko.wikipedia.org/wiki/:en:Union_List_of_Artist_Names "wikilink")`', 245, p.ulanLink },`
`   { 'USCongress', '`[`US``   ``Congress`](https://ko.wikipedia.org/wiki/미국_의회_인명사전 "wikilink")`', 1157, p.uscongressLink },`
`   { 'VIAF', '`[`VIAF`](https://ko.wikipedia.org/wiki/가상_국제_전거_파일 "wikilink")`', 214, p.viafLink },`
`   { 'WORLDCATID', '`[`WorldCat``   ``Identities`](https://ko.wikipedia.org/wiki/WorldCat_Identities "wikilink")`', 7859, nil },`

}

\-- Legitimate aliases to p.conf, for convenience -- Format: { 'alias', 'parameter name in p.conf' } p.aliases = {

`   { 'RLS', 'RSL' },`
`   { 'MusicBrainz', 'MBA' },`
`   { 'MusicBrainz artist', 'MBA' },`
`   { 'MusicBrainz label', 'MBL' },`
`   { 'MusicBrainz release group', 'MBRG' },`
`   { 'MusicBrainz work', 'MBW' },`
`   { 'Leonore', 'Léonore' },`
`   { 'TDVIA', 'TDVİA' },`

}

\-- Deprecated aliases to p.conf; tracked in -- Format: { 'deprecated parameter name', 'replacement parameter name in p.conf' } p.deprecated = {

`   { 'GKD', 'GND' },`
`   { 'PND', 'GND' },`
`   { 'SWD', 'GND' },`
`   { 'NARA-organization', 'NARA' },`
`   { 'NARA-person', 'NARA' },`

}

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Main](https://ko.wikipedia.org/wiki/Main "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

function p.authorityControl( frame )

`   local resolveEntity = require( "Module:ResolveEntityId" )`
`   local parentArgs = frame:getParent().args`
`   local elements = {} --create/insert rows later`
`   local worldcatCat = ''`
`   local suppressedIdCat = ''`
`   local deprecatedIdCat = ''`
`   `
`   --Redirect aliases to proper parameter names`
`   for _, a in pairs( p.aliases ) do`
`       local alias, param = a[1], a[2]`
`       if (parentArgs[param] == nil or parentArgs[param] == '') and parentArgs[alias] then`
`           parentArgs[param] = parentArgs[alias]`
`       end`
`   end`
`   `
`   --Redirect deprecated parameters to proper parameter names, and assign tracking cat`
`   for _, d in pairs( p.deprecated ) do`
`       local dep, param = d[1], d[2]`
`       if (parentArgs[param] == nil or parentArgs[param] == '') and parentArgs[dep] then`
`           parentArgs[param] = parentArgs[dep]`
`           if namespace == 0 then`
`               deprecatedIdCat = '`[`'..dep..'`](https://ko.wikipedia.org/wiki/분류:구식의_전거_통제_식별자가_포함된_위키백과_문서 "wikilink")`'`
`           end`
`       end`
`   end`
`   `
`   --Use QID= parameter for testing/example purposes only`
`   local itemId = nil`
`   if namespace ~= 0 then`
`       local qid = parentArgs['qid'] or parentArgs['QID']`
`       if qid then`
`           itemId = 'Q'..mw.ustring.gsub(qid, '^[Qq]', '')`
`           itemId = resolveEntity._id(itemId) --nil if unresolvable`
`       end`
`   else`
`       itemId = mw.wikibase.getEntityIdForCurrentPage()`
`   end`
`   `
`   --Wikidata fallback if requested`
`   if itemId then`
`       for _, params in ipairs( p.conf ) do`
`           if params[3] > 0 then`
`               local val = parentArgs[params[1]]`
`               if val == nil or val == '' then`
`                   local canUseWikidata = nil`
`                   if reqs[params[1]] then`
`                       canUseWikidata = p.matchesWikidataRequirements( itemId, reqs[params[1]] )`
`                   else`
`                       canUseWikidata = true`
`                   end`
`                   if canUseWikidata then`
`                       local wikidataIds = p.getIdsFromWikidata( itemId, 'P'..params[3] )`
`                       if wikidataIds[1] then`
`                           if val == '' and (namespace == 0 or testcases) then`
`                               suppressedIdCat = '[[분류:전거_통제_식별자가_생략된_위키백과_문서|'..params[1]..']]'`
`                           else`
`                               parentArgs[params[1]] = wikidataIds[1]`
`   end end end end end end end`
`   `
`   --Configured rows`
`   local rct = 0`
`   for _, params in ipairs( p.conf ) do`
`       local val = parentArgs[params[1]]`
`       if val and val ~= '' and type(params[4]) == 'function' then`
`           table.insert( elements, p.createRow( params[1], params[2]..':', val, params[4]( val ), true, params.category ) )`
`           rct = rct + 1`
`       end`
`   end`
`   `
`   --WorldCat`
`   local worldcatId = parentArgs['WORLDCATID']`
`   if worldcatId and worldcatId ~= '' then --if present & unsuppressed`
`       table.insert( elements, p.createRow( 'WORLDCATID', '', worldcatId, '`[`WorldCat``   ``Identities`](https://ko.wikipedia.org/wiki/WorldCat_Identities "wikilink")`: [`<https://www.worldcat.org/identities/>`'..mw.uri.encode(worldcatId, 'PATH')..' '..worldcatId..']', false ) ) --Validation?`
`       worldcatCat = '`[`분류:월드캣``   ``식별자를``   ``포함한``   ``위키백과``   ``문서`](https://ko.wikipedia.org/wiki/분류:월드캣_식별자를_포함한_위키백과_문서 "wikilink")`'`
`   elseif worldcatId == nil then --if absent & unsuppressed`
`       local viafId = parentArgs['VIAF']`
`       local lccnId = parentArgs['LCCN']`
`       if viafId and viafId ~= '' and p.viafLink( viafId ) then --VIAF must be present, unsuppressed, & validated`
`           table.insert( elements, p.createRow( 'VIAF', '', viafId, '`[`WorldCat``   ``Identities`](https://ko.wikipedia.org/wiki/WorldCat_Identities "wikilink")` (via VIAF): [`<https://www.worldcat.org/identities/containsVIAFID/>`'..viafId..' '..viafId..']', false ) )`
`           if namespace == 0 then `
`               worldcatCat = '`[`분류:월드캣-VIAF``   ``식별자를``   ``포함한``   ``위키백과``   ``문서`](https://ko.wikipedia.org/wiki/분류:월드캣-VIAF_식별자를_포함한_위키백과_문서 "wikilink")`'`
`           end`
`       elseif lccnId and lccnId ~= '' and p.lccnLink( lccnId ) then --LCCN must be present, unsuppressed, & validated`
`           local lccnParts = p.splitLccn( lccnId )`
`           if lccnParts and lccnParts[1] ~= 'sh' then`
`               local lccnIdFmtd = lccnParts[1]..lccnParts[2]..'-'..lccnParts[3]`
`               table.insert( elements, p.createRow( 'LCCN', '', lccnId, '`[`WorldCat``   ``Identities`](https://ko.wikipedia.org/wiki/WorldCat_Identities "wikilink")` (via LCCN): [`<https://www.worldcat.org/identities/lccn->`'..lccnIdFmtd..' '..lccnIdFmtd..']', false ) )`
`               if namespace == 0 then `
`                   worldcatCat = '`[`분류:월드캣-LCCN``   ``식별자를``   ``포함한``   ``위키백과``   ``문서`](https://ko.wikipedia.org/wiki/분류:월드캣-LCCN_식별자를_포함한_위키백과_문서 "wikilink")`'`
`               end`
`           end`
`       end`
`   elseif worldcatId == '' then --if suppressed`
`       suppressedIdCat = '`[`WORLDCATID`](https://ko.wikipedia.org/wiki/분류:전거_통제_식별자가_생략된_위키백과_문서 "wikilink")`'`
`   end`
`   `
`   local Navbox = require('Module:Navbox')`
`   local elementsCat = ''`
`   if rct >= 25 then`
`       local eCat = rct..'개의 요소가 포함된 전거 통제'`
`       elementsCat  = '`[`분류:'..eCat..'`](https://ko.wikipedia.org/wiki/분류:'..eCat..' "wikilink")`'..p.redCatLink(eCat)`
`   end`
`   `
`   local outString = ''`
`   if #elements > 0 then`
`       local args = {}`
`       if testcases and itemId then args = { qid = itemId } end --expensive`
`       local pencil = frame:expandTemplate{ title = 'EditAtWikidata', args = args}`
`       outString = Navbox._navbox( {`
`           name  = 'Authority control',`
`           navboxclass = 'authority-control',`
`           bodyclass = 'hlist',`
`           group1 = '`[`전거``   ``통제`](https://ko.wikipedia.org/wiki/위키백과:전거_통제 "wikilink")`'..pencil,`
`           list1 = table.concat( elements )`
`           } )`
`       local auxCats = worldcatCat .. elementsCat .. suppressedIdCat .. deprecatedIdCat`
`       if testcases then`
`           auxCats = mw.ustring.gsub(auxCats, '(%[%[)(분류)', '%1:%2') --for easier checking`
`       end`
`       outString = outString .. auxCats`
`       if namespace ~= 0 then`
`           outString = mw.ustring.gsub(outString, '(%[%[)(분류:.*위키백과 문서)', '%1:%2') --by definition`
`       end`
`   end`
`   `
`   return outString`

end

return p

[Category:Blah](https://ko.wikipedia.org/wiki/Category:Blah "wikilink") [Category:Wikipedia_articles_with_deprecated_authority_control_identifiers](https://ko.wikipedia.org/wiki/Category:Wikipedia_articles_with_deprecated_authority_control_identifiers "wikilink")