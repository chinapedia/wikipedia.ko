> This article is converted from Wikipedia: [:Solar eclipse](https://ko.wikipedia.org/wiki/:Solar_eclipse).


local eclipse = {} local args = {}

local data_module_prefix = "Module:Solar eclipse/db/"

local natureTbl = {

`   ["Total"] = "개기일식",`
`   ["Partial"] = "부분일식",`
`   ["Annular"] = "금환일식",`
`   ["Hybrid"] = "혼성일식",`
`   [""] = ""`

}

local function ifnotempty(s,a,b)

`   if (s and s ~= '') then`
`       return a`
`   else`
`       return b`
`   end`

end

local function ifexist(page)

`   if not page then return false end`
`   if mw.title.new(page).exists then return true end`
`   return false`

end

local function parsedate(y,m,d)

`   local lang = mw.language.getContentLanguage()`
`   d = (tonumber(d) < 10) and ('0' .. tonumber(d)) or (d)`
`   m = (tonumber(m) < 10) and ('0' .. tonumber(m)) or (m)`
`   local success, result = pcall(lang.formatDate, lang, 'Y년 M월 j일', y .. '-' .. m .. '-' .. d)`
`   return success and result or nil`

end

local function parsecoord(frame, s)

`   local lat = s:match('^%s*([%d][%d.]*)%s*[NS]%s*[%d][%d.]*[EW]%s*$')`
`   local  NS = s:match('^%s*[%d][%d.]*%s*([NS])%s*[%d][%d.]*[EW]%s*$')`
`   local lon = s:match('^%s*[%d][%d.]*%s*[NS]%s*([%d][%d.]*)[EW]%s*$')`
`   local  EW = s:match('^%s*[%d][%d.]*%s*[NS]%s*[%d][%d.]*([EW])%s*$')`
`   if( lat and NS and lon and EW ) then`
`       return frame:expandTemplate{ title = '좌표', args = {lat, NS, lon, EW, 'type:landmark'} }`
`   else`
`       return s`
`   end`

end

local function parsekm(frame, s)

`   if(s and s ~= '') then`
`       return s .. ' km'`
`   else`
`       return nil`
`   end`

end

local function parsetime(s)

`   if(s and s ~= '') then`
`       local min = s:match('^%s*([%d][%d]*)m%s*[%d][%d]*s%s*$')`
`       local sec = s:match('^%s*[%d][%d]*m%s*([%d][%d]*)s%s*$')`
`       if( min and sec ) then`
`           return tostring(tonumber(min)*60 + tonumber(sec)) .. '초' ..`
`               ' (' .. min .. '분 ' .. sec .. '초)'`
`       end`
`   end`
`   return s`

end

local function cataloglink(c, y)

`   if(c and tonumber(c)) then`
`       local y1 = math.floor( (tonumber(y) - 1) / 10 ) * 10 + 1`
`       local y2 = y1 + 99`
`       return '[`<https://eclipse.gsfc.nasa.gov/SEcat5/SE>`' .. tostring(y1) .. '-' .. tostring(y2) .. '.html ' .. c .. ']'`
`   else`
`       return c`
`   end`

end

local function loadsolardb(frame, s)

`   local yearstr = s:match('^%s*([%d][%d][%d][%d])[A-Z][a-z][a-z][%d][%d]%s*$') or ''`
`   local function setarg(k, v)`
`       if(v and v ~= '') then args[k] = v end`
`   end`
`   if( yearstr ~= '' ) then`
`       local dbsubpage = math.floor( (tonumber(yearstr) - 1) / 50 ) * 5`
`       local dbpage  = data_module_prefix .. tostring( dbsubpage )`
`       if (ifexist(dbpage)) then`
`           local data = mw.loadData(dbpage)`
`           local dargs = data[s]`
`           setarg('date', parsedate(dargs['y'], dargs['m'] or dargs['m3'] or dargs['m2'], dargs['d'] or dargs['d2']))`
`           setarg('image', (dargs['Ph'] and dargs['Ph'] ~= '') and '[[`<File:'_>`.._dargs['Ph']__.._'|320px]]' or nil)`
`           setarg('caption', dargs['PhCap'])`
`           setarg('map', (dargs['Map'] and dargs['Map'] ~= '') and '[[`<File:'_>`.._dargs['Map']__.._'|320px]]' or nil)`
`           setarg('map_caption', '지도')`
`           setarg('type_ref', '')`
`           setarg('cat', cataloglink(dargs['Cat'], dargs['y']) )`
`           setarg('nature', dargs['Ty'])`
`           setarg('gamma', dargs['Gam'])`
`           setarg('magnitude', dargs['Mag'])`
`           -- setarg('saros', dargs['Saros'] and '[[Solar_Saros_'_.._dargs['Saros']_.._'|'  .. dargs['Saros'] .. ']]')`
`           setarg('saros', dargs['Saros'])`
`           setarg('saros_sequence', dargs['Mem'])`
`           setarg('saros_total', dargs['Max'])`
`           setarg('max_eclipse_ref', '')`
`           setarg('duration', parsetime(dargs['Dur']))`
`           setarg('location', '')`
`           setarg('coords', parsecoord(frame,dargs['Loc']))`
`           setarg('max_width', parsekm(frame,dargs['Wid']))`
`           setarg('times_ref', '')`
`           setarg('start_partial', dargs['TiPB'])`
`           setarg('start_total', dargs['TiTB'])`
`           setarg('start_central', '')`
`           setarg('greatest_eclipse', dargs['TiG'])`
`           setarg('end_central', '')`
`           setarg('end_total', dargs['TiTE'])`
`           setarg('end_partial', dargs['TiPE'])`
`       end`
`   end`

end

local function infobox(frame)

`   local abovestr = ifnotempty(args['date'], `
`       (args['date'] or '') .. " 일식",`
`       "사용법은 `[`틀:일식``   ``정보를`](https://ko.wikipedia.org/wiki/틀:일식_정보 "wikilink")` 참고하세요")`
`   local bgcolor = args['background'] or args['bgcolour'] or ''`
`   local mapstr = ifnotempty(args['map'],`
`       "`

<div style='padding-bottom:0.5em;'>

" ..

`       (args['map'] or '') .. ifnotempty(args['map_caption'], `
`           "`

<div style='line-height:1.2em; padding-top:0.1em;'>

<small>" ..

`           (args['map_caption'] or '') .. "`</small>

</div>

", '') .. '

</div>

')

`   return frame:expandTemplate{ title = 'infobox', args = {`
`       ["bodyclass"] = "vevent",`
`       ["bodystyle"] = "width:25em; text-align:left; font-size:90%;",`
`       ["above"] = abovestr,`
`       ["aboveclass"] = "summary",`
`       ["abovestyle"] = "padding-bottom:0.25em; background:" .. bgcolor .. "; line-height:1.2em; text-align:center; font-size:115%;",`

\------------------ Images and maps ------------------

`       ["image"] = args['image'] or '',`
`       ["imagestyle"] = "padding-bottom:0.5em;",`
`       ["caption"] = args['caption'] or '',`
`       ["captionstyle"] = "padding-top:0.1em; line-height:1.2em; font-size:90%;",`
`       ["headerstyle"] = "background:#eee; font-size:105%;",`
`       ["labelstyle"] = "padding:0 0.5em 0 0; line-height:1.1em;",`
`       ["datastyle"] = "padding:0; line-height:1.2em; vertical-align:middle;",`
`       ["data1"] = mapstr,`

\------------- Type of eclipse and saros -------------

`       ["header2"] = "일식 종류" .. (args['type_ref'] or ''),`
`       ["label3"]  = "종류",`
`       ["data3"]   = natureTbl[args['nature'] or ''],`
`       ["label4"]  = "`[`감마`](https://ko.wikipedia.org/wiki/감마_\(식현상\) "wikilink")`",`
`       ["data4"]   = args['gamma'] or '',`
`       ["label5"]  = "`[`식분`](https://ko.wikipedia.org/wiki/식분 "wikilink")`",`
`       ["data5"]   = args['magnitude'] or '',`

\------------------ Maximum eclipse ------------------

`       ["header7"] = "최대 일식" .. (args['max_eclipse_ref'] or ''),`
`       ["label8"] = "지속 시간",`
`       ["data8"] = args['duration'] or '',`
`       ["label9"] = "위치",`
`       ["data9"] = args['location'] or '',`
`       ["class9"] = "location",`
`       ["label10"] = "좌표",`
`       ["data10"] = args['coords'] or '',`
`       ["label11"] = "최대 구간 폭",`
`       ["data11"] = args['max_width'] or '',`

\----------------------- Times -----------------------

`       ["header12"] = "시간 (`[`UTC`](https://ko.wikipedia.org/wiki/협정_세계시 "wikilink")`)" .. (args['times_ref'] or ''),`
`       ["label13"] = "(P1) 반영접촉 시작",`
`       ["data13"] = args['start_partial'] or '',`
`       ["label14"] = "(U1) 본영접촉 시작",`
`       ["data14"] = args['start_total'] or '',`
`       ["label15"] = "(U2) 중심 시작",`
`       ["data15"] = args['start_central'] or '',`
`       ["label16"] = "최대식",`
`       ["data16"] = args['greatest_eclipse'] or '',`
`       ["label17"] = "(U3) 중심 끝",`
`       ["data17"] = args['end_central'] or '',`
`       ["label18"] = "(U4) 본영접촉 끝",`
`       ["data18"] = args['end_total'] or '',`
`       ["label19"] = "(P4) 반영접촉 끝",`
`       ["data19"] = args['end_partial'] or '',`

\------------------------ Event references -------------------------

`       ["header20"] = "출처",`
`       ["label21"] = "`[`사로스``   ``주기`](https://ko.wikipedia.org/wiki/사로스_주기 "wikilink")`",`
`       ["data21"] = (args['saros'] or '') `
`           .. " (" .. (args['saros_total'] or '') .. "개 중 " .. (args['saros_sequence'] or '') .. "번 째)",`
`       ["label22"] = "목록 # (SE5000)",`
`       ["data22"] = args['cat'] or '',`
`       } }`
`   `

end

function eclipse.box(frame)

`   args = require('Module:Arguments').getArgs(frame, {`
`           wrappers = '틀:일식 정보'`
`       })`

`   if( args['2'] and args['2'] ~= '') then`
`       loadsolardb(frame,args['2'])`
`   elseif( args['1'] and args['1'] ~= '') then`
`       loadsolardb(frame,args['1'])`
`   end`
`   `
`   return infobox(frame)`

end

return eclipse