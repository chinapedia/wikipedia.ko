> This article is converted from Wikipedia: [모듈:Navseasoncats](https://ko.wikipedia.org/wiki/모듈:Navseasoncats).


local p = {}

local errors = '' local nexistingcats = 0 local currtitle = mw.title.getCurrentTitle() local testcases = (currtitle.subpageText == '시험장') local navborder = true --whether or not a border is displayed

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Utility & category functions](https://ko.wikipedia.org/wiki/Utility_&_category_functions "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

\--Error message handling function errorclass( msg )

`   return mw.text.tag( 'span', {class='error mw-ext-cite-error'}, '`<b>`Error!`</b>` '..string.gsub(msg, '&#', '&#') )`

end

\--Returns a colon if on a testcase subpage function testcasecolon()

`   if testcases then return ':' end`
`   return ''`

end

\--Consolidate avoidance checks function avoidself()

`   return (currtitle.text ~= 'Navseasoncats' and          --avoid self`
`           currtitle.text ~= '시간 분류 둘러보기' and      --avoid self`
`           currtitle.text ~= '시간 분류 둘러보기/설명문서' and      --avoid self`
`           currtitle.text ~= 'Navseasoncats/sandbox' and  --avoid self`
`           (currtitle.nsText ~= '틀' or testcases)) --avoid nested transclusion errors (i.e. ``)`

end

\--Failure handling function failedcat( errors, sortkey )

`   if avoidself() then`
`       return (errors or '')..'***Navseasoncats failed to generate navbox***'..`
`              '`[`'..(sortkey``   ``or``   ``'O')..'`](https://ko.wikipedia.org/wiki/'..testcasecolon\(\)..':시간_분류_둘러보기_-_둘러보기_상자_생성_실패 "wikilink")`'`
`   end`
`   return ''`

end

\--Check for nav\*() navigational isolation (not necessarily an error) function isolatedcat()

`   if nexistingcats == 0 and avoidself() then`
`       return '`[`'..testcasecolon()..'Category:시간``   ``분류``   ``둘러보기``   ``-``   ``외톨이`](https://ko.wikipedia.org/wiki/'..testcasecolon\(\)..'Category:시간_분류_둘러보기_-_외톨이 "wikilink")`'`
`   end`
`   return ''`

end

\--Check for navhyphen default gap size + isolatedcat() (not necessarily an error) function defaultgapcat( bool )

`   if bool and nexistingcats == 0 and avoidself() then`
`       --using "nexistingcats > 0" isn't as useful, since the default gap size obviously worked`
`       return '`[`'..testcasecolon()..'Category:Navseasoncats``   ``default``   ``season``   ``gap``   ``size`](https://ko.wikipedia.org/wiki/'..testcasecolon\(\)..'Category:Navseasoncats_default_season_gap_size "wikilink")`'`
`   end`
`   return ''`

end

\--Similar to : make a piped link to a category, if it exists; --if it doesn't exist, just display the greyed link title without linking function catlink( catname, disp )

`   catname = mw.text.trim(catname or '')`
`   disp    = mw.text.trim(disp or '')`
`   local grey = '#888'`
`   local displaytext = catname`
`   if disp ~= '' then`
`       --use 'disp' parameter instead, and strip any trailing disambiguator`
`       displaytext = mw.ustring.gsub(disp, '%s+%(.+$', '');`
`   end`
`   `
`   local catpage = mw.title.new( catname, 'Category' )`
`   if catpage.exists then`
`       --TODO?: ignore cat #Rs: see 2019 link on nav @ Category:2018 Asian Games`
`       --isRedirect did not change expensive function count (b/c catname passed instead of id?),`
`       --but isRedirect also did not recognize ``,`
`       --and it's not worth calling & parsing getContent, so TODONT`
`       nexistingcats = nexistingcats + 1`
`       return '`[`'..displaytext..'`](https://ko.wikipedia.org/wiki/Category:'..catname..' "wikilink")`'`
`   else`
`       return '`<span style="color:'..grey..'">`'..displaytext..'`</span>`'`
`   end`

end

\--12 -\> 12th, etc. --Used in navordinal() only function addord( i )

`   if tonumber(i) then`
`       local s = tostring(i)`
`       `
`       local tens = string.match(s, '1%d$')`
`       if    tens then return s..'th' end`
`       `
`       local  ones = string.match(s, '%d$')`
`       if     ones == '1' then return s..'st'`
`       elseif ones == '2' then return s..'nd'`
`       elseif ones == '3' then return s..'rd' end`
`       `
`       return s..'th'`
`   end`
`   return i`

end

\--Returns an unsigned string of the 1-4 digit decade ending in "0", else error --Used in navdecade() only function sterilizedec( decade )

`   if decade == nil then return nil end`
`   `
`   local dec = string.match(decade, '^[-%+]?(%d?%d?%d?0)$') or `
`               string.match(decade, '^[-%+]?(%d?%d?%d?0)[^%d]')`
`   if dec then`
`       return dec`
`   else`
`       local decade_fixed234 = string.match(decade, '^[-%+]?(%d%d?%d?)%d[^%d]') or`
`                               string.match(decade, '^[-%+]?(%d%d?%d?)%d$')`
`       local decade_fixed1   = string.match(decade, '^[-%+]?(%d)[^%d]') or`
`                               string.match(decade, '^[-%+]?(%d)$')`
`       if decade_fixed234 then`
`           return decade_fixed234..'0'`
`       elseif decade_fixed1 then`
`           return '0'`
`       else`
`           errors = 'sterilizedec() error'`
`           return nil`
`       end`
`   end`

end

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Formerly separated templates/modules](https://ko.wikipedia.org/wiki/Formerly_separated_templates/modules "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

\--[============================={{ navyear }}==============================](https://ko.wikipedia.org/wiki/============================={{_navyear_}}============================== "wikilink")

function navyear( firstpart, year, lastpart, minimumyear, maximumyear )

`   --- if true then`
`   ---     return '@' .. firstpart .. '@' .. year .. '@' .. lastpart .. '@'`
`   --- end`
`   --Expects a PAGENAME of the form "Some sequential 1760 example cat", where `
`   --  ``=Some sequential`
`   --  ``=1760`
`   --  ``=example cat`
`   --  ``=1758 ('min' year parameter; optional)`
`   --  ``=1800 ('max' year parameter; optional)`
`   year = tonumber(year) or tonumber(mw.ustring.match(year or '', '^%s*(%d*)'))`
`   local minyear = tonumber(string.match(minimumyear or '', '-?%d+')) or -9999    --allow +/- qualifier`
`   local maxyear = tonumber(string.match(maximumyear or '', '-?%d+')) or  9999    --allow +/- qualifier`
`   if string.match(minimumyear or '', 'BC') then minyear = -math.abs(minyear) end --allow BC qualifier (AD otherwise assumed)`
`   if string.match(maximumyear or '', 'BC') then maxyear = -math.abs(maxyear) end --allow BC qualifier (AD otherwise assumed)`

`   local temporal = mw.ustring.match(lastpart, '년') or`
`                    mw.ustring.match(lastpart, '세기') or ''`
`   `
`   if year == nil then`
`       errors = errorclass('Function navyear can\'t recognize the year sent to its 2nd parameter.')`
`       return failedcat(errors, 'Y')`
`   end`
`   `
`   --AD/BC switches & vars`
`   local parentBC = mw.ustring.match(firstpart, '기원전 $') --following the "1 BC" convention for all years BC`
`   firstpart  = mw.ustring.gsub(firstpart,  '기원전 $', '')`
`   local BCe = parentBC or '기원전 ' --"BC" default`
`   `
`   local switchADBC = 1                 --  1=AD parent`
`   if parentBC then switchADBC = -1 end -- -1=BC parent; possibly adjusted later`
`   local Y = 0 --secondary iterator for AD-on-a-BC-parent`
`   `
`   if minyear > year*switchADBC then minyear = year*switchADBC end --input error; minyear should be <= parent`
`   if maxyear < year*switchADBC then maxyear = year*switchADBC end --input error; maxyear should be >= parent`
`   --determine interyear gap size to condense special category types, if possible`
`   local ygapdefault = 1 --assume/start at the most common case: 2001, 2002, etc.`
`   local ygap = ygapdefault`
`   if string.match(lastpart, 'presidential') then`
`       local ygap1, ygap2 = ygapdefault, ygapdefault --need to determine previous & next year gaps indepedently`
`       local ygap1_success, ygap2_success = false, false`
`       `
`       local prevseason = nil`
`       while ygap1 <= 5 do --Czech Republic, Poland, Sri Lanka, etc. have 5-year terms`
`           prevseason = firstpart..' '..(year-ygap1)..' '..lastpart`
`           if mw.title.new(prevseason, 'Category').exists then`
`               ygap1_success = true`
`               break`
`           end`
`           ygap1 = ygap1 + 1`
`       end`
`       `
`       local nextseason = nil`
`       while ygap2 <= 5 do --Czech Republic, Poland, Sri Lanka, etc. have 5-year terms`
`           nextseason = firstpart..' '..(year+ygap2)..' '..lastpart`
`           if mw.title.new(nextseason, 'Category').exists then`
`               ygap2_success = true`
`               break`
`           end`
`           ygap2 = ygap2 + 1`
`       end`
`       `
`       if ygap1_success and ygap2_success then`
`           if ygap1 == ygap2 then ygap = ygap1 end`
`       elseif ygap1_success then  ygap = ygap1`
`       elseif ygap2_success then  ygap = ygap2`
`       end`
`   end`

`   --begin navyears`
`   local navy = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local i = -5`
`   while i <= 5 do`
`       local y = year + i*ygap*switchADBC`
`       local BCdisp = ''`
`       local ADdisp = ''`
`       if i ~= 0 then --left/right navy`
`           `
`           local AD = ''`
`           local BC = ''`
`           if year >= 1 and not parentBC then --parent = 1-10 AD`
`               if y <= 0 then`
`                   BC = BCe`
`                   y = math.abs(y - 1) --skip y = 0 (DNE)`
`               end`
`           elseif parentBC then`
`               if switchADBC == -1 then --displayed y is in the BC regime`
`                   if y >= 1 then     --the common case`
`                       BC = BCe`
`                   elseif y == 0 then --switch from BC to AD regime`
`                       switchADBC = 1`
`                   end`
`               end`
`               if switchADBC == 1 then --displayed y is now in the AD regime`
`                   Y = Y + 1 --skip y = 0 (DNE)`
`                   y = Y     --easiest solution: start another iterator for these AD ys displayed on a BC year parent`
`                   if y == 1 then`
`                       ADdisp = '후 '`
`                   end`
`               end`
`           end`
`           if BC ~= '' and year <= 5 then --only show 'BC' for parent years <= 5: saves room, easier to read,`
`               BCdisp = '전 '          --and 6 is the first/last nav year that doesn't need a disambiguator;`
`           end                            --the center/parent year will always show BC, so no need to show it another 10x`
`           `
`           --populate left/right navy`
`           local ysign = y --use y for display & ysign for logic`
`           if BC ~= '' then ysign = -ysign end`
`           if (minyear <= ysign) and (ysign <= maxyear) then -- ex: 1758, 1759, 1761, 1762, 1763, 1764, 1765`
`               navy = navy..'*'..catlink( firstpart..BC..y..lastpart, ADdisp..BCdisp..y )..'\n'`
`           else -- ex: 1755, 1756, 1757`
`               navy = navy..'*`<span style="visibility:hidden">`'..BCdisp..y..'`</span>`\n'`
`           end`
`       else --center navy; ex: 1760`
`           if parentBC then BCdisp = BCe end`
`           navy = navy..'*`<b>`'..BCdisp..year..temporal..'`</b>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   return navy..'|}'..isolatedcat()`

end

\--[============================{{ navdecade }}=============================](https://ko.wikipedia.org/wiki/============================{{_navdecade_}}============================= "wikilink")

function navdecade( firstpart, decade, lastpart, mindecade, maxdecade )

`   --Expects a PAGENAME of the form "Some sequential 2000 example cat", where `
`   --  ``=Some sequential`
`   --  ``=2000`
`   --  ``=example cat`
`   --and`
`   --  ``=1800 ('min' decade parameter; optional)`
`   --  ``=2020 ('max' decade parameter; optional; defaults to next decade)`
`   `
`   --sterilize dec`
`   local dec = sterilizedec(decade)`
`   if errors ~= '' then`
`       errors = errorclass('Function navdecade was sent "'..(decade or '')..'" as its 2nd parameter, '..`
`                           'but expects a 1 to 4-digit year ending in "0".')`
`       return failedcat(errors, 'D')`
`   end`
`   local ndec = tonumber(dec)`
`   `
`   --sterilize mindecade & determine AD/BC`
`   local mindefault = '-9999'`
`   local mindec = sterilizedec(mindecade) --returns a tostring(unsigned int), or nil + error`
`   if mindec then`
`       if string.match(mindecade, '-%d') or `
`          string.match(mindecade, 'BC') or`
`          mw.ustring.match(mindecade, '기원전')`
`       then`
`           mindec = '-'..mindec --better +/-0 behavior with strings (0-initialized int == "-0" string...)`
`       end`
`   elseif errors ~= '' then`
`       errors = errorclass('Function navdecade was sent "'..(mindecade or '')..'" as its 4th parameter, '..`
`                           'but expects a 1 to 4-digit year ending in "0", the earliest decade to be shown.')`
`       return failedcat(errors, 'E')`
`   else`
`       mindec = mindefault --tonumber() later, after error checks`
`   end`
`   `
`   --sterilize maxdecade & determine AD/BC`
`   local maxdefault = '9999'`
`   local maxdec = sterilizedec(maxdecade) --returns a tostring(unsigned int), or nil + error`
`   if maxdec then`
`       if string.match(maxdecade, '-%d') or `
`          string.match(maxdecade, 'BC')`
`       then                     --better +/-0 behavior with strings (0-initialized int == "-0" string...),`
`           maxdec = '-'..maxdec --but a "-0" string -> tonumber() -> tostring() = "-0",`
`       end                      --and a  "0" string -> tonumber() -> tostring() =  "0"`
`   elseif errors ~= '' then`
`       errors = errorclass('Function navdecade was sent "'..(maxdecade or '')..'" as its 5th parameter, '..`
`                           'but expects a 1 to 4-digit year ending in "0", the highest decade to be shown.')`
`       return failedcat(errors, 'F')`
`   else`
`       maxdec = maxdefault`
`   end`
`   `
`   local tspace = ' ' --assume trailing space for "1950s in X"-type cats`
`   if string.match(lastpart, '^-') then tspace = '' end --DNE for "1970s-related"-type cats`
`   `
`   --AD/BC switches & vars`
`   `
`   local parentBC = mw.ustring.match(firstpart, '기원전 $') --following the "0s BC" convention for all years BC`
`   firstpart = mw.ustring.gsub(firstpart, '기원전 $', '') --handle BC separately; AD never used`
`   --TODO?: handle BCE, but only if it exists in the wild`
`   `
`   local dec0to40AD = (ndec >= 0 and ndec <= 40 and not parentBC) --special behavior in this range`
`   local switchADBC = 1                 --  1=AD parent`
`   if parentBC then switchADBC = -1 end -- -1=BC parent; possibly adjusted later`
`   local BCdisp = ''`
`   local D = -math.huge --secondary switch & iterator for AD/BC transition`
`   `
`   --check non-default min/max more carefully; determine right-offset`
`   local roffset = 0`
`   if mindec ~= mindefault then`
`       if tonumber(mindec) > ndec*switchADBC then`
`           mindec = tostring(ndec*switchADBC) --input error; mindec should be <= parent`
`       end`
`   end`
`   if maxdec ~= maxdefault then --a non-default max will override offsetting behavior`
`       if tonumber(maxdec) < ndec*switchADBC then`
`           maxdec = tostring(ndec*switchADBC) --input error; maxdec should be >= parent`
`       end`
`   --else --offset only if max == maxdefault`
`   elseif mw.ustring.match(lastpart, '를 배경으로 한') == nil then`
`       local thisyear = mw.getContentLanguage():formatDate( 'Y' )`
`       local nthisdecade = tonumber(string.match(thisyear, '^%d%d%d')..'0')`
`       local diff = nthisdecade - ndec*switchADBC --in 2019: diff=30 for 1980; diff=0 for 2010; diff = -20 for 2030`
`       if diff < 0 then diff = 0 end  --always show at least 1 decade ahead for present-decade+ cats`
`       if diff >= 0 and diff <= 30 then`
`           roffset = 40 - diff --in 2019: offset=10 for 1980; offset=40 for 2010; offset=40 for 2030`
`       end`
`   end`
`   local nmindec = tonumber(mindec) --similar behavior to navyear & navordinal`
`   local nmaxdec = tonumber(maxdec) --similar behavior to navordinal`
`   `
`   --begin navdecade`
`   local bnb = '' --border/no border`
`   if navborder == false then --for embedding in `
`       bnb = ' border-style: none; background-color: transparent;'`
`   end`
`   local navd = '{| class="toccolours hlist" style="text-align: center; margin: auto;'..bnb..'"\n'..'|\n'`
`   `
`   local i = (-50 - roffset)`
`   while i <= (50 - roffset) do`
`       local d = ndec + i*switchADBC`
`       `
`       if i ~= 0 then --left/right navd`
`           local BC = ''`
`           BCdisp = ''`
`           if dec0to40AD then`
`               if D < -10 then`
`                   d = math.abs(d + 10) --b/c 2 "0s" decades exist: "0s BC" & "0s" (AD)`
`                   BC = '기원전 '`
`                   if d == 0 then`
`                       D = -10 --track 1st d = 0 use (BC)`
`                   end`
`               elseif D >= -10 then`
`                   D = D + 10 --now iterate from 0s AD`
`                   d = D      --2nd d = 0 use`
`               end`
`           elseif parentBC then`
`               if switchADBC == -1 then --parentBC looking at the BC side (the common case)`
`                   BC = '기원전 '`
`                   if d == 0 then     --prepare to switch to the AD side on the next iteration`
`                       switchADBC = 1 --1st d = 0 use (BC)`
`                       D = -10        --prep`
`                   end`
`               elseif switchADBC == 1 then --switched to the AD side`
`                   D = D + 10 --now iterate from 0s AD`
`                   d = D      --2nd d = 0 use (on first use)`
`               end`
`           end`
`           if BC ~= '' and ndec <= 50 then`
`               BCdisp = '전 ' --show BC for all BC decades whenever a "0s" is displayed on the nav`
`           end`
`           `
`           --populate left/right navd`
`           local hidden = '*`<span style="visibility:hidden">`'..BCdisp..d..'`</span>`\n'`
`           local shown = '*'..catlink( firstpart..BC..d..'년대'..lastpart, BCdisp..d..'' )..'\n'`
`           local dsign = d --use d for display & dsign for logic`
`           if BC ~= '' then dsign = -dsign end`
`           if (nmindec <= dsign) and (dsign <= nmaxdec) then`
`               if dsign == 0 and (nmindec == 0 or nmaxdec == 0) then --distinguish b/w -0 (BC) & 0 (AD)`
`                   --"zoom in" on +/- 0 and turn dsign/min/max temporarily into +/- 1 for easier processing`
`                   local zsign, zmin, zmax = 1, nmindec, nmaxdec`
`                   if BC ~= '' then zsign = -1 end`
`                   if     mindec == '-0' then zmin = -1`
`                   elseif mindec ==  '0' then zmin =  1 end`
`                   if     maxdec == '-0' then zmax = -1`
`                   elseif maxdec ==  '0' then zmax =  1 end`
`                   `
`                   if (zmin <= zsign) and (zsign <= zmax) then`
`                       navd = navd..shown`
`                   else`
`                       navd = navd..hidden`
`                   end`
`               else`
`                   navd = navd..shown --the common case`
`               end`
`           else`
`               navd = navd..hidden`
`           end`
`           `
`       else --center navd`
`           if D >= -10 then`
`               D = D + 10 --housekeeping b/w left/right sides`
`           end`
`           if parentBC then`
`               BCdisp = '기원전 '`
`               if ndec == 0 then`
`                   switchADBC = 1 --next element will be 0s AD`
`                   D = -10 --for this special case, D is still -inf`
`               end`
`           else`
`               BCdisp = ''`
`           end`
`           navd = navd..'*`<b>`'..BCdisp..dec..'년대'..'`</b>`\n'`
`       end`
`       `
`       i = i + 10`
`   end`
`   `
`   return navd..'|}'..isolatedcat()`

end

\--[============================{{ navhyphen }}=============================](https://ko.wikipedia.org/wiki/============================{{_navhyphen_}}============================= "wikilink")

function navhyphen( start, hyph, ish, firstpart, lastpart, minseas, maxseas, testgap )

`   --Expects a PAGENAME of the form "Some sequential 2015–16 example cat", where `
`   --  ``=2015`
`   --  ``=–`
`   --  ``=16 (for "1999-2000", "2000" must be truncated so `` is "00")`
`   --  ``=Some sequential`
`   --  ``=example cat`
`   --  ``=1800 ('min' starting season shown; optional)`
`   --  ``=1999 ('max' starting season shown; optional; 1999 will show 1999-00)`
`   --  ``=0 (testcasegap parameter for easier testing; optional)`
`   `
`   --sterilize start`
`   if string.match(start or '', '^%d%d?%d?%d?$') == nil then --1-4 digits, AD only`
`       local start_fixed = mw.ustring.match(start or '', '^%s*(%d%d?%d?%d?)%D')`
`       if start_fixed then`
`           start = start_fixed`
`       else`
`           errors = errorclass('Function navhyphen can\'t recognize the number "'..(start or '')..'" '..`
`                               'in the first part of the "season" that was passed to it. '..`
`                               'For e.g. "2015–16", "2015" is expected via "|2015|–|16|".')`
`           return failedcat(errors, 'H')`
`       end`
`   end`
`   local nstart = tonumber(start)`
`   `
`   --en dash check`
`   local endashcat = ''`
`   if hyph ~= '–' then`
`       endashcat = '' --nav still processable, but track`
`   end`
`   `
`   --sterilize ish (e.g. "01" part of "2001"; "2" part of "12")`
`   if string.match(ish or '', '^%d?%d$') == nil then --expecting 1 or 2 digits`
`       if string.match(ish or '', '^%d%d%d') then`
`           errors = errorclass('The second part of the season passed to function navhyphen should only be one or two digits, not "'..(ish or '')..'". '..`
`                               'E.g. "1999-2000" should be cut down to "1999-00".')`
`           return failedcat(errors, 'I')..endashcat`
`       end`
`       local ish_fixed = mw.ustring.match(ish or '', '^%s*(%d?%d)%D')`
`       if ish_fixed then`
`           ish = ish_fixed`
`       else`
`           errors = errorclass('Function navhyphen can\'t recognize the number "'..(ish or '')..'" '..`
`                               'in the second part of the "season" that was passed to it. '..`
`                               'For e.g. "2015–16", "16" is expected via "|2015|–|16|".')`
`           return failedcat(errors, 'J')..endashcat`
`       end`
`   end`
`   local nish = tonumber(ish)`
`   `
`   --sterilize min/max`
`   local nminseas = tonumber(minseas) or -9999 --not yet implemented; pending discussion`
`   local nmaxseas = tonumber(maxseas) or  9999 --not yet implemented; pending discussion`
`   `
`   --error check start & ish together`
`   if string.len(start) >= 2 and string.len(ish) ~= 2 then`
`       errors = errorclass('The second part of the season passed to function navhyphen should be two digits, not "'..ish..'".')`
`       return failedcat(errors, 'K')..endashcat`
`   end`
`   `
`   --calculate intRAseason size/term length & finishing year`
`   local t = 1`
`   while t <= 10 do --1~4 iterations should be enough`
`       local nfinish = nstart + t --use switchADBC to flip this sign to work for years BC`
`       if string.match(nfinish, '%d?%d$') == ish then`
`           break`
`       end`
`       if t == 10 then`
`           errors = errorclass('Function navhyphen can\'t determine a reasonable term length for "'..start..hyph..ish..'".')`
`           return failedcat(errors, 'L')..endashcat`
`       end`
`       t = t + 1`
`   end`
`   `
`   --calculate intERseason gap size`
`   local hgapdefault = 0 --assume & start at the most common case: 2001–02, 2002–03, etc.`
`   local hgap = hgapdefault`
`   local hgap_success = false`
`   while hgap <= 5 do --verify`
`       local prevseason = firstpart..' '..(nstart-t-hgap)..hyph..string.match(nstart-hgap, '%d?%d$')..' '..lastpart`
`       local nextseason = firstpart..' '..(nstart+t+hgap)..hyph..string.match(nstart+2*t+hgap, '%d?%d$')..' '..lastpart`
`       if mw.title.new(prevseason, 'Category').exists or   --use 'or', in case we're at the edge of the cat structure,`
`          mw.title.new(nextseason, 'Category').exists then --or we hit a "–00"/"–2000" situation on one side`
`           hgap_success = true`
`           break`
`       end`
`       hgap = hgap + 1`
`   end`
`   if hgap_success == false then`
`       hgap = tonumber(testgap) or hgapdefault --tracked via defaultgapcat()`
`   end`
`   `
`   --begin navhyphen`
`   local navh = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local i = -3`
`   while i <= 3 do`
`       local from = nstart + i*(t+hgap)`
`       local to   = tostring(from+t)`
`       local todisp = string.match(to, '%d?%d$')`
`       local tolink = todisp`
`       if tolink == '00' then`
`           tolink = to`
`       end`
`       `
`       --populate navh`
`       local shown = '*'..catlink( firstpart..' '..from..hyph..tolink..' '..lastpart, `
`                                                   from..hyph..todisp )..'\n'`
`       local hidden = '*`<span style="visibility:hidden">`'..from..hyph..todisp..'`</span>`\n'`
`       if i ~= 0 then --left/right navh`
`           if from >= 0 then`
`               navh =  navh..shown`
`           else`
`               navh = navh..hidden`
`           end`
`       else --center navh`
`           navh = navh..'*`<b>`'..start..hyph..ish..'`</b>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   return navh..'|}'..isolatedcat()..defaultgapcat(not hgap_success)..endashcat`

end

\--[============================{{ navordinal }}============================](https://ko.wikipedia.org/wiki/============================{{_navordinal_}}============================ "wikilink")

function navordinal( firstpart, ord, lastpart, minimumord, maximumord )

`   local nord = tonumber(ord)`
`   local minord = tonumber(string.match(minimumord or '', '(-?%d+)[snrt]?[tdh]?')) or -9999 --allow full ord & +/- qualifier`
`   local maxord = tonumber(string.match(maximumord or '', '(-?%d+)[snrt]?[tdh]?')) or  9999 --allow full ord & +/- qualifier`
`   if string.match(minimumord or '', 'BC') then minord = -math.abs(minord) end --allow BC qualifier (AD otherwise assumed)`
`   if string.match(maximumord or '', 'BC') then maxord = -math.abs(maxord) end --allow BC qualifier (AD otherwise assumed)`
`   `
`   local temporal = string.match(lastpart, 'century') or`
`                    string.match(lastpart, 'millennium') or ''`
`   `
`   local tspace = ' ' --assume a trailing space after ordinal`
`   if string.match(lastpart, '^-') then tspace = '' end --DNE for "19th-century"-type cats`
`   `
`   --AD/BC switches & vars`
`   `
`   local ordBCElastparts = { --needed for parent = AD 1-5, when the BC/E format is unknown`
`       --lists the lastpart of valid BCE cats`
`       --"BCE" removed to match both AD & BCE cats; easier & faster than multiple string.match()s`
`       ['-century Hebrew people'] = 'BCE', --WP:CFD/Log/2016 June 21#Category:11th-century BC Hebrew people`
`       ['-century Jews']          = 'BCE', --co-nominated`
`       ['-century Judaism']       = 'BCE', --co-nominated`
`       ['-century rabbis']        = 'BCE', --co-nominated`
`   }`
`   local parentBC = mw.ustring.match(lastpart, '%s(BCE?)')       --"1st-century BC" format`
`   local lastpartNoBC = mw.ustring.gsub(lastpart, '%sBCE?', '')  --easier than splitting lastpart up in 2; AD never used`
`   local BCe = parentBC or ordBCElastparts[lastpartNoBC] or 'BC' --"BC" default`
`   `
`   local switchADBC = 1                 --  1=AD parent`
`   if parentBC then switchADBC = -1 end -- -1=BC parent; possibly adjusted later`
`   local O = 0 --secondary iterator for AD-on-a-BC-parent`
`   `
`   if not temporal and minord < 1 then minord = 1 end --nothing before "1st parliament", etc.`
`   if minord > nord*switchADBC then minord = nord*switchADBC end --input error; minord should be <= parent`
`   if maxord < nord*switchADBC then maxord = nord*switchADBC end --input error; maxord should be >= parent`
`   `
`   --determine right-offset, to not show unnecessary future millenia`
`   local roffset = 0`
`   if temporal and nord <= 3 then`
`       if string.match(lastpartNoBC, 'millennium ') and --only offset "1st millennium BC in Egypt" to "3rd-millennium people"-type cats`
`          string.match(lastpartNoBC, 'millennium in fiction') == nil and --except these, which extend > 4th millennium`
`          maxord == 9999 --only apply if max unspecified`
`       then`
`           if not parentBC and nord <= 3 then --1st, 2nd, & 3rd millennium parents`
`               roffset = nord + 1`
`           elseif parentBC and nord == 1 then --1st millennium BC only`
`               roffset = 1`
`           end`
`       end`
`   end`
`   `
`   --begin navordinal`
`   local navo = '{| class="toccolours hlist" style="text-align: center; margin: auto;"\n'..'|\n'`
`   `
`   local i = (-5 - roffset)`
`   while i <= (5 - roffset) do`
`       local o = nord + i*switchADBC`
`       local BC = ''`
`       local BCdisp = ''`
`       if i ~= 0 then --left/right navo`
`           `
`           if parentBC then`
`               if switchADBC == -1 then --parentBC looking at the BC side`
`                   if o >= 1 then     --the common case`
`                       BC = ' '..BCe`
`                   elseif o == 0 then --switch to the AD side`
`                       BC = ''`
`                       switchADBC = 1`
`                   end`
`               end`
`               if switchADBC == 1 then --displayed o is now in the AD regime`
`                   O = O + 1 --skip o = 0 (DNE)`
`                   o = O     --easiest solution: start another iterator for these AD o's displayed on a BC year parent`
`               end`
`           elseif o <= 0 then --parentAD looking at BC side`
`               BC = ' '..BCe`
`               o = math.abs(o - 1) --skip o = 0 (DNE)`
`           end`
`           if BC ~= '' and nord <= 5 then --only show 'BC' for parent ords <= 5: saves room, easier to read,`
`               BCdisp = ' '..BCe          --and 6 is the first/last nav ord that doesn't need a disambiguator;`
`           end                            --the center/parent ord will always show BC, so no need to show it another 10x`
`           `
`           --populate left/right navo`
`           local oth = addord(o)`
`           local osign = o --use o for display & osign for logic`
`           if BC ~= '' then osign = -osign end`
`           local hidden = '*`<span style="visibility:hidden">`'..oth..'`</span>`\n'`
`           if temporal then --e.g. "3rd-century BC"`
`               if (minord <= osign) and (osign <= maxord) then`
`                   local lastpart = lastpartNoBC --lest we recursively add multiple "BC"s`
`                   if BC ~= '' then`
`                       lastpart = string.gsub(lastpart, temporal, temporal..BC) --replace BC if needed`
`                   end`
`                   navo = navo..'*'..catlink( firstpart..' '..oth..tspace..lastpart, oth..BCdisp )..'\n'`
`               else`
`                   navo = navo..hidden`
`               end`
`           elseif BC == '' and minord <= osign and osign <= maxord then --e.g. >= "1st parliament"`
`               navo = navo..'*'..catlink( firstpart..' '..oth..tspace..lastpart, oth )..'\n'`
`           else --either out-of-range (hide), or non-temporal + BC = something might be wrong (2nd X parliament BC?); handle exceptions if/as they arise`
`               navo = navo..hidden`
`           end`
`       else --center navo`
`           if parentBC then BC = ' '..BCe end`
`           navo = navo..'*`<b>`'..addord(o)..BC..'`</b>`\n'`
`       end`
`       `
`       i = i + 1`
`   end`
`   `
`   return navo..'|}'..isolatedcat()`

end

\--[============================{{ var_season }}============================](https://ko.wikipedia.org/wiki/============================{{_var_season_}}============================ "wikilink")

function var_season( pn )

`   --Extracts e.g. 2015–16, 3rd, 2000s, or 1999 out of a string`
`   local pagename = currtitle.baseText`
`   if pn and pn ~= '' then`
`       pagename = pn`
`   end`
`   `
`   local cpagename = 'Category:'..pagename --limited-Lua-regex workaround`
`   `
`   local season  = mw.ustring.match(cpagename, '[:%s](%d+[–-]%d+)%s') or --split in 2 b/c %f[%s$] doesn't work`
`                   mw.ustring.match(cpagename, '[:%s](%d+[–-]%d+)$')`
`                   `
`   local ordinal = mw.ustring.match(cpagename, '[:%s](%d+[snrt][tdh])[-%s]') or`
`                   mw.ustring.match(cpagename, '[:%s](%d+[snrt][tdh])$')`
`                   `
`   local decade  = mw.ustring.match(cpagename, '[:%s](%d+년대)[-%s를]') or`
`                   mw.ustring.match(cpagename, '[:%s](%d+년대)$')`
`                   `
`   local year    = mw.ustring.match(cpagename, '[:%s](%d+)[년세%s]') or`
`                   mw.ustring.match(cpagename, '[:%s](%d+)$')`
`                   `
`   local all4 = (season or '')..','..(ordinal or '')..','..(decade or '')..','..(year or '')`
`   `
`   if (season == nil and ordinal == nil and decade == nil and year == nil) or`
`       string.match(all4, '%d%d%d%d%d')`
`   then`
`       errors = errorclass('Function var_season can\'t recognize a season, ordinal, decade, nor year for category "'..pagename..'".')`
`       return failedcat(errors, 'S')`
`   end`
`   `
`   --return in order of decreasing complexity`
`   if season  then return season  end`
`   if ordinal then return ordinal end`
`   if decade  then return decade  end`
`   if year    then return year    end`

end

\--[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink") --[Main](https://ko.wikipedia.org/wiki/Main "wikilink") --[==========================================================================](https://ko.wikipedia.org/wiki/========================================================================== "wikilink")

function p.navseasoncats( frame )

`   local args = frame:getParent().args`
`   local dby         = args['decade-below-year'] --used by `
`   local cat         = args['cat'] --'testcase' alias`
`   local testcase    = args['testcase']`
`   local testcasegap = args['testcasegap']`
`   local minyear = args['min']`
`   local maxyear = args['max']`

`   if dby then`
`       navborder = false`
`       dby = string.gsub(dby, ' ', ' ') --unicodify forced whitespace`
`   end`
`   `
`   local paramtracking = ''`
`   if currtitle.nsText == 'Category' then`
`       if cat      then paramtracking = paramtracking..'' end`
`       if testcase then paramtracking = paramtracking..'' end`
`   end`
`   `
`   local pagename = testcase or cat or dby or currtitle.baseText`
`   `
`   local varseason = var_season(pagename)`
`   if errors ~= '' then return varseason..paramtracking end --some error checking in var_season()`
`   `
`   local firstpart, lastpart = string.match(pagename, '^(.*)'..varseason..'(.*)$')`
`   -- firstpart = mw.text.trim(firstpart or '')`
`   -- lastpart  = mw.text.trim(lastpart or '')`
`   `
`   local start = string.match(varseason, '^%d+')`
`   local hyphen, finish = mw.ustring.match(varseason, '%d([–-])(%d+)') --ascii 150 & 45 (ndash & keyboard hyphen); mw req'd`
`   `
`   --determine the appropriate nav function`
`   if hyphen and finish then                             --e.g. "2015–16"`
`       local ish = string.match(finish, '%d?%d$')        --in case  "1999–2000", "1–4"`
`       return navhyphen( start, hyphen, ish, firstpart, lastpart, minyear, maxyear, testcasegap )..paramtracking`
`       `
`   elseif string.match(varseason, '%d[snrt][tdh]$') then --e.g. "4th"`
`       return navordinal( firstpart, start, lastpart, minyear, maxyear )..paramtracking`
`       `
`   elseif string.match(varseason, '%d년대$') then           --e.g. "0s", "2010s"`
`       return navdecade( firstpart, start, lastpart, minyear, maxyear )..paramtracking`
`       `
`   elseif string.match(varseason, '^%d+$') then          --e.g. "500" or "2001"`
`       return navyear( firstpart, start, lastpart, minyear, maxyear )..paramtracking`
`       `
`   else                                                  --malformed`
`       errors = errorclass('Failed to determine the appropriate nav function from malformed season "'..varseason..'". ')`
`       return failedcat(errors, 'N')..paramtracking`
`   end`

end

return p

[Category:Navseasoncats_range_not_using_en_dash](https://ko.wikipedia.org/wiki/Category:Navseasoncats_range_not_using_en_dash "wikilink") [Category:시간_분류_둘러보기_-_cat_인수_사용](https://ko.wikipedia.org/wiki/Category:시간_분류_둘러보기_-_cat_인수_사용 "wikilink") [Category:시간_분류_둘러보기_-_testcase_인수_사용](https://ko.wikipedia.org/wiki/Category:시간_분류_둘러보기_-_testcase_인수_사용 "wikilink")