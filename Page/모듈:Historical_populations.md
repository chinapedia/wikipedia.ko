> This article is converted from Wikipedia: [:Historical populations](https://ko.wikipedia.org/wiki/:Historical_populations).


\-- -- This template implements  -- local p = {} local lang = mw.getContentLanguage()

local function ifexist(page)

`   if not page then return false end`
`   if mw.title.new(page).exists then return true end`
`   return false`

end

local function isempty( s )

`   return not s or s:match( '^%s*(.-)%s*$' ) == ''`

end

local function formatnumR(num)

`   return lang:parseFormattedNumber(num)`

end

local function formatnum(num)

`   return lang:parseFormattedNumber(num) and lang:formatNum(lang:parseFormattedNumber(num)) or num`

end

local function popheader(percentages, popname, yearname)

`   local percent = ''`
`   local ywidth = '3em'`
`   if( popname == '' ) then`
`       popname = '`<abbr title="각 해의 총인구">`인구`</abbr>`'`
`   end`
`   if( yearname == '' ) then`
`       yearname = '연도'`
`   end`
`   if( percentages == 'off' ) then`
`       ywidth = 'auto'`
`   else`
`       local pstr = ''`
`       if( percentages == 'pagr' ) then`
`           pstr = '`<abbr title="연당 인구 증감율">`±%`</abbr>`'`
`       else`
`           pstr = '`<abbr title="퍼센트 추이">`±%`</abbr>`'`
`       end`
`       local pstyle = 'border-bottom: 1px solid black; padding: 1px; text-align: right'`
`       percent = mw.ustring.format('`

<th style="%s">

%s  

</th>

', pstyle, pstr)

`   end`
`   return mw.ustring.format( [==[`

<tr style="font-size: 95%%">

<th style="border-bottom: 1px solid black; padding: 1px; width: %s;">

%s

</th>

<th style="border-bottom: 1px solid black; padding: 1px; text-align: right;">

%s  

</th>

%s

</tr>

\]==\], ywidth, yearname, popname, percent) end

local function poprow(year, pop, pyear, ppop, linktype, percentages, shading, current_year)

`   local percent = ''`
`   local yearnum = tonumber(formatnumR(mw.ustring.gsub(year or '', '^%s*([%d][%d][%d]+).*$', '%1') or ''))`
`   local pyearnum = tonumber(formatnumR(mw.ustring.gsub(pyear or '', '^%s*([%d][%d][%d]+).*$', '%1') or ''))`
`   local popnum = tonumber(formatnumR(pop or ''))`
`   local ppopnum = tonumber(formatnumR(ppop or ''))`
`   if( linktype == 'US' or linktype == 'USA' ) then`
`       if( (yearnum or 0) >= 1790 and yearnum <= current_year and math.fmod(yearnum, 10) == 0) then`
`           if( yearnum < current_year ) then`
`               year = '`[`'``   ``..``   ``year``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._tostring\(yearnum\)_.._'_United_States_Census "wikilink")`'`
`           elseif( ifexist(tostring(yearnum) .. ' United States Census') ) then`
`               year = '`[`'``   ``..``   ``year``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._tostring\(yearnum\)_.._'_United_States_Census "wikilink")`'`
`           end`
`       end`
`   end`
`   if( shading == 'off' ) then`
`       shading = ''`
`   else`
`       shading = ' border-bottom: 1px solid #bbbbbb;'`
`   end`
`   if(percentages ~= 'off') then`
`       local pstr = '—    '`
`       if(popnum ~= nil and ppopnum ~= nil) then`
`           if(percentages == 'pagr') then`
`               pstr = mw.ustring.format('%.2f', 100*math.abs(math.pow(popnum/ppopnum,1/(yearnum-pyearnum)) - 1))`
`           else`
`               pstr = mw.ustring.format('%.1f', 100*math.abs(popnum/ppopnum - 1))`
`           end`
`           if( popnum < ppopnum ) then`
`               pstr = '−' .. pstr .. '%'`
`           else`
`               pstr = '+' .. pstr .. '%'`
`           end`
`       end`
`       percent = '`

<td style="text-align: right; padding: 1px;' .. shading .. '">

' .. pstr .. '

</td>

'

`   end`
`   `
`   return mw.ustring.format( [==[`

<tr>

<th style="text-align: center; padding: 1px;%s">

%s

</th>

<td style="text-align: right; padding: 1px;%s">

%s

</td>

%s

</tr>

\]==\], shading, year, shading, formatnum(pop), percent) end

function p.poptable(frame)

`   local t = {}`
`   local args = frame:getParent().args`

`   local title = args['title'] or ''`
`   local align = args['align'] or 'right'`
`   local clear = args['clear'] or ''`
`   local percentages = args['percentages'] or ''`
`   local state = args['state'] or ''`
`   local linktype = args['type'] or ''`
`   local shading = args['shading'] or 'on'`
`   local width = args['width'] or ''`
`   local subbox = args['subbox'] or ''`
`   local popname = args['pop_name'] or ''`
`   local yearname = args['year_name'] or ''`
`   local footnote = args['footnote'] or ''`
`   local source = args['source'] or ''`
`   local percol = tonumber(args['percol']) or 0`
`   local cols = tonumber(args['cols']) or 1`
`   local colspan = 3`
`   local style = ''`

`   -- setup classes and styling for outer table`
`   local class = 'toccolours'`
`   if( state == 'collapsed' ) then`
`       class = class .. ' collapsible collapsed'`
`   end`

`   if( isempty(title) ) then`
`       title = '인구 통계 역사'`
`   end`

`   if( isempty(clear) ) then`
`       clear = align`
`   end`
`   `
`   if( isempty(width) ) then`
`       width = '15em'`
`   end`

`   local margin = '0 0 1em 1em'`
`   if( align == 'left' ) then`
`       margin = '0 1em 1em 0'`
`   else`
`       if( align == 'none' ) then`
`           margin = '0.5em 1em 0.5em 0'`
`       end`
`   end`

`   -- count the total number of population rows`
`   local argcount = 0`
`   local rowcount = 0`
`   for k, v in pairs( args ) do`
`       if ( (type( k ) == 'number') and (not isempty(args[k])) ) then`
`           if( k >= 1 and math.floor(k) == k and k > argcount) then`
`               argcount = k`
`           end`
`           if( math.fmod(k - 1, 2) == 0 ) then`
`               rowcount = rowcount + 1`
`           end`
`       end`
`   end`

`   -- setup the footer text`
`   if( source ~= '' ) then`
`       source = '출처: ' .. source`
`       if( footnote ~= '' ) then`
`           footnote = footnote .. '`
`'`
`       end`
`   end`

`   -- override the value of cols if percol has been specified`
`   if( percol > 0 ) then`
`       cols = math.floor( (rowcount - 1) / percol ) + 1`
`   end`

`   -- specify the colspan for the title and footer lines`
`   if( cols > 1 ) then`
`       colspan = cols`
`   else`
`       if (percentages == 'off') then `
`           colspan = 2`
`       else`
`           colspan = 3`
`       end`
`   end`

`   -- compute outer table width`
`   local twidth = width`
`   if( (cols > 1) and width:match('^%s*[%d]+[%w]+%s*$') ) then`
`       local widthnum = mw.ustring.gsub( width, '^%s*([%d]+)([%w]+)%s*$', '%1' )`
`       local widthunit = mw.ustring.gsub( width, '^%s*([%d]+)([%w]+)%s*$', '%2' )`
`       twidth = tostring(widthnum*cols) .. widthunit`
`   end`

`   -- outer table style`
`   if( isempty(subbox) ) then`
`       style = mw.ustring.format("width: %s; text-align: center; border-spacing: 0; float: %s; clear: %s; margin: %s", `
`           twidth, align, clear, margin)`
`   else`
`       style = mw.ustring.format("width: %s; margin:0; border-collapse:collapse; border:none;", twidth)`
`   end `
`   `
`   -- create the outer table and title line`
`   table.insert(t, mw.ustring.format( [==[`

<table class="%s" style="%s">

<tr>

<th colspan="%d" class="navbox-title" style="padding:0.25em; font-size:110%%">

%s

</th>

</tr>

\]==\], class, style, colspan, title) )

`   -- compute the number of rows per col`
`   local rowspercol = math.floor( (rowcount - 1) / cols ) + 1`

`   -- loop over columns and rows within columns`
`   local pyear = ''`
`   local ppop = ''`
`   local offset = 1`
`   local current_year = tonumber(os.date("%Y", os.time()))`
`   for c = 1,cols do`
`       -- add inner tables if we are rendering more than one column`
`       if( cols > 1) then`
`           if (c == 1) then`
`               table.insert(t, '`

<tr valign="top">

<td style="padding:0 0.5em;">

')

`           else`
`               table.insert(t, '`

<td style="padding:0 0.5em; border-left:solid 1px #aaa">

')

`           end`
`           table.insert(t, '`

<table style="border-spacing:0; width:' .. width .. '">

')

`       end`
`       -- header for each column`
`       table.insert(t, popheader(percentages, popname, yearname))`
`       for r = 1,rowspercol do`
`           -- skip blank rows`
`           while(isempty(args[offset]) and offset <= argcount) do`
`               offset = offset + 2`
`           end`
`           -- generate the row if we have not exceeded the rowcount`
`           if(offset <= argcount) then`
`               -- shade every fifth row, unless shading = off`
`               local s = 'off'`
`               if( math.fmod((c - 1)*rowspercol + r, 5) == 0 and r ~= rowspercol) then`
`                   s = shading`
`               end`
`               table.insert(t, poprow(args[offset], args[offset + 1] or '', pyear, ppop, `
`                   linktype, percentages, s, current_year) )`
`               pyear = args[offset]`
`               ppop = args[offset+1] or ''`
`               offset = offset + 2`
`           end`
`       end`
`       -- close the inner tables if we are rendering multiple columns`
`       if( cols > 1 ) then`
`           table.insert(t, '`

</table>

</td>

')

`           if( c == cols ) then`
`               table.insert(t, '`

</td>

</tr>

')

`           end`
`       end`
`   end`

`   -- add the footnote and source line     `
`   if( footnote ~= '' or source ~= '' ) then`
`       table.insert(t, mw.ustring.format([==[`

<tr>

<td colspan="%d" style="border-top: 1px solid black; font-size: 85%%; text-align: left;">

%s%s

</td>

</tr>

\]==\], colspan, footnote, source) )

`   end`

`   -- close the outer table`
`   table.insert(t, '`

</tr>

</table>

')

`   return table.concat( t, '\n' )`

end

return p