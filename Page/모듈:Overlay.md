> This article is converted from Wikipedia: [:Overlay](https://ko.wikipedia.org/wiki/:Overlay).


\-- this module implements [Template:Overlay](https://ko.wikipedia.org/wiki/Template:Overlay "wikilink") -- imported from [:en:Module:Overlay](https://ko.wikipedia.org/wiki/:en:Module:Overlay "wikilink") local p = {}

local mArguments = require('Module:Arguments')

\-- used to cache the calculated font color to avoid repeat calculations local previous_backgroundcolor = '' local fontcolor = ''

local function buildicon(n, form, lk, c, t)

`   local res`
`   if form == 'text' then`
`       return tostring(`
`               mw.html.create('span')`
`                   :css('font-weight', 'bold')`
`                   :css('color', c)`
`                   :wikitext(n)`
`               )`
`   elseif form == 'color' or form == 'colour' then`
`       return tostring(`
`               mw.html.create('span')`
`                   :css('background-color', c)`
`                   :wikitext('  ')`
`               )`
`   else`
`       -- check if the color is difference from the previous color`
`       if c ~= previous_backgroundcolor then`
`           -- color changed, so look up the best font color`
`           local greatercontrast = require('Module:Color contrast')._greatercontrast`
`           fontcolor = greatercontrast{c, 'white', 'black', bias = 1.3}`
`           -- update the previous value for the next check`
`           previous_backgroundcolor = c`
`       end`
`       -- build the inner span for the icon`
`       local span = mw.html.create('span')`
`           :css('color', fontcolor)`
`           :css('font-size', '88%')`
`           :css('font-weight', 'bold')`
`           :attr('title', t)`
`           :wikitext(n)`
`       -- build the outer div`
`       local div = mw.html.create('div')`
`           :css('display', 'inline-block')`
`           :css('width', 'auto')`
`           :css('height', 'auto')`
`           :css('text-align', 'center')`
`           :css('padding', ((tonumber(n) or 0) < 10) and '0px 4px' or '0px 2px')`
`           :css('vertical-align', 'middle')`
`           :css('-moz-border-radius', '3px')`
`           :css('-webkit-border-radius', '3px')`
`           :css('border-radius', '3px')`
`           :css('background-color', c)`

`       -- link the inner span if requested and insert in the div`
`       if lk ~= '' then`
`           div:wikitext('`[`'``   ``..``   ``tostring(span)``   ``..``   ``'`](https://ko.wikipedia.org/wiki/:'_.._lk_.._' "wikilink")`')`
`       else`
`           div:wikitext(tostring(span))`
`       end`
`       -- convert to a string`
`       return tostring(div)`
`   end`

end

local function buildlegend(data, cols, border, caption)

`   -- create the outer table to hold the columns`
`   local root = mw.html.create('table')`
`       :css('width', '100%')`
`       :css('border', (border ~= 'no') and '1px #ccc solid' or '')`
`   -- create the outer row which will contain the columns`
`   local outerrow = root:tag('tr')`
`   local percol = math.ceil((#data) / cols)`
`   local k = 0`
`   for j=1,cols do`
`       -- create the outer cell to hold this column`
`       local colcell = outerrow:tag('td')`
`           :css('width', (math.floor(10/cols)/10) .. '%')`
`           :css('vertical-align', 'top')`
`       -- create the inner table to hold the entries in the column`
`       local coltable = colcell:tag('table')`
`           :css('width', '100%')`
`           :css('font-size', '85%')`
`           :css('line-height', '95%')`
`       -- add the entries to the column`
`       for l = 1,percol do`
`           k = k + 1`
`           if k <= #data then`
`               local rdata = data[k]`
`               local tr = coltable:tag('tr'):css('vertical-align','top')`
`               tr:tag('td')`
`                   :css('width', '12px')`
`                   :css('text-align', 'right')`
`                   :css('padding-bottom', '2px')`
`                   :wikitext(rdata[1] or '')`
`               tr:tag('td')`
`                   :css('padding-bottom', '2px')`
`                   :wikitext(rdata[2] or '')`
`           end`
`       end`
`   end`
`   return caption .. tostring(root)`

end

local function buildlegenditem(im, lk, t)

`   local res = {im, ''}`
`   if t ~= '' then`
`       if lk ~= '' then`
`           res[2] = '`[`'``   ``..``   ``t``   ``..``   ``'`](https://ko.wikipedia.org/wiki/:'_.._lk_.._' "wikilink")`'`
`       else`
`           res[2] = t`
`       end`
`   else`
`       res[2] = '`[`'``   ``..``   ``lk``   ``..``   ``'`](https://ko.wikipedia.org/wiki/:'_.._lk_.._' "wikilink")`'`
`   end`
`   return res `

end

function p.icon(frame)

`   local args = mArguments.getArgs(frame)`
`   return tostring(`
`       mw.html.create('div')`
`           :css('display', 'inline-block')`
`           :css('line-height', '95%')`
`           :wikitext(buildicon(args['1'] or '', `
`                               args['form'] or 'icon',`
`                               args['link'] or '', `
`                               args['2'] or 'red',`
`                               args['tip'] or ''))`
`   )`

end

function p.main(frame)

`   local args = mArguments.getArgs(frame)`
`   `
`   local image = args['image'] or ''`
`   local width = tonumber(args['width'] or '500') or 500`
`   local height = tonumber(args['height'] or '500') or 500`
`   local columns = tonumber(args['columns'] or '3') or 3`
`   local grid = ((args['grid'] or ''):lower() == 'yes') and 'yes' or 'no'`
`   local legendbox = ((args['legendbox'] or ''):lower() == 'no') and 'no' or 'yes'`
`   local overlay = (image == '') and 'no' or ( ((args['overlay'] or ''):lower() == 'no') and 'no' or 'yes' )`
`   local float = args['float'] or 'center'`
`   local border = ((args['border'] or ''):lower() == 'no') and 'no' or 'yes'`
`   local padding = args['padding'] or ''`

`   -- create the root table`
`   local root = mw.html.create('table')`
`   if float == 'center' or float == 'centre' then`
`       root:css('margin-left', 'auto')`
`           :css('margin-right', 'auto')`
`   elseif float == 'right' then`
`       root:css('float', 'right')`
`           :css('clear', 'right')`
`           :css('margin-left', '1em')`
`   elseif float == 'left' then`
`       root:css('float', 'left')`
`           :css('clear', 'left')`
`           :css('margin-right', '1em')`
`   else`
`       root:css('float', float)`
`   end`
`   if border == 'yes' then`
`       root:css('border', '1px #ccc solid')`
`   end`

`   -- create a list of all the overlay numbers`
`   local itemnums = {}`
`   for k, v in pairs( args ) do`
`       local i = tonumber(tostring(k):match( '^%s*overlay([%d]+)%s*$' ) or '-1')`
`       if i > -1 then`
`           table.insert(itemnums, i)`
`       else`
`           i = tonumber(tostring(k):match( '^%s*overlay([%d]+)tip%s*$' ) or '-1')`
`           if i > -1 then`
`               table.insert(itemnums, i)`
`           end`
`       end`
`   end`
`   -- sort to process in order`
`   table.sort( itemnums )`
`   `
`   -- remove duplicates`
`   for k = 2,#itemnums do`
`       if itemnums[k] == itemnums[k-1] then`
`           table.remove(itemnums, k)`
`       end`
`   end`

`   -- build the overlay markers and text`
`   itemdata = {}`
`   local colori = args['color'] or args['colour'] or 'red'`
`   local formi = ''    `
`   for k = 1,#itemnums do`
`       local i = itemnums[k]`
`       formi = args['overlay' .. i .. 'form'] or formi`
`       colori = args['overlay' .. i .. 'color'] or args['overlay' .. i .. 'colour'] or colori`
`       local linki = args['overlay' .. i .. 'link'] or ''`
`       local tipi = args['overlay' .. i .. 'tip'] or args['overlay' .. i] or ''`
`       local overlayi = args['overlay' .. i] or args['overlay' .. i .. 'tip'] or ''`
`       if (overlayi ~= '' or tipi ~= '') then`
`           local imagei = buildicon(i, formi, linki, colori, tipi)`
`           itemdata[k] = buildlegenditem(imagei, args['overlay' .. i .. 'link'] or '', overlayi)`
`       end`
`   end`

`   -- create the overlay image`
`   if image ~= '' then`
`       local cell = root:tag('tr'):tag('td')`
`       cell:attr('align', 'center')`
`       if( padding ~= '' ) then`
`           cell:css('padding', padding)`
`       end`
`       if( columns > 1 and legendbox == 'yes' ) then`
`           cell:attr('colspan', columns)`
`       end`
`       local imagediv = cell:tag('div')`
`       imagediv:css('position','relative')`
`           :css('left', '0px')`
`           :css('top', '0px')`
`           :css('width', ((grid == 'yes') and 940 or width) .. 'px')`
`           :css('height', ((grid == 'yes') and 940 or height) .. 'px')`
`       if grid == 'yes' then`
`           imagediv:tag('span')`
`               :css('position', 'absolute')`
`               :css('left', '0px')`
`               :css('top', '0px')`
`               :css('z-index', '2')`
`               :wikitext('`[`Grid_99,_100_int_red_50_int_yellow_(940).svg`](https://ko.wikipedia.org/wiki/File:Grid_99,_100_int_red_50_int_yellow_\(940\).svg "fig:Grid_99,_100_int_red_50_int_yellow_(940).svg")`')`
`       end`
`       imagediv:tag('span')`
`           :css('position', 'absolute')`
`           :css('left', '0px')`
`           :css('top', '0px')`
`           :css('z-index', '0')`
`           :css('width', width .. 'px')`
`           :css('height', height .. 'px')`
`           :wikitext('`[`'``   ``..``   ``width``   ``..``   ``'x'``   ``..``   ``height``   ``..``   ``'px`](https://ko.wikipedia.org/wiki/File:'_.._image_.._' "fig:' .. width .. 'x' .. height .. 'px")`')`
`       if overlay == 'yes' then`
`           for k = 1,#itemnums do`
`               local i = itemnums[k]`
`               local imagei = (itemdata[k])[1]`
`               for j =0,3 do`
`                   local overlayileftj = args['overlay' .. i .. 'left' .. ((j == 0) and '' or j)] or ''`
`                   local overlayitopj = args['overlay' .. i .. 'top' .. ((j == 0) and '' or j)] or ''`
`                   if overlayileftj ~= '' then`
`                       imagediv:tag('div')`
`                           :css('position', 'absolute')`
`                           :css('left', overlayileftj .. 'px')`
`                           :css('top', overlayitopj .. 'px')`
`                           :css('line-height', '95%')`
`                           :css('z-index', '1')`
`                           :wikitext(imagei)`
`                   end`
`               end`
`           end`
`       end`
`   end`

`   -- Split the legend items into sub-legends`
`   legend = {{}, {}, {}, {}, {}}`
`   local jmax = itemnums[#itemnums]`
`   for i=1,5 do`
`       if args['legend' .. i .. 'start'] then`
`           -- default is all items`
`           j1 = 0`
`           j2 = jmax`
`           -- set start item number to (legendistart) or (legend(i-1)end + 1)`
`           if args['legend' .. i .. 'start'] then`
`               j1 = tonumber(args['legend' .. i .. 'start']) or j1`
`           elseif args['legend' .. (i-1) .. 'end'] then`
`               j1 = (tonumber(args['legend' .. (i-1) .. 'end']) or j1) + 1`
`           end`
`           -- set end item number to (legendiend) or (legend(i+1)start - 1)`
`           if args['legend' .. i .. 'end'] then`
`               j2 = tonumber(args['legend' .. i .. 'end']) or j2`
`           elseif args['legend' .. (i+1) .. 'start'] then`
`               j2 = (tonumber(args['legend' .. (i+1) .. 'start']) or j2) - 1`
`           end`
`           -- get the items within the range, marking them as they are used`
`           for k=1,#itemnums do`
`               j = itemnums[k]`
`               if (j >= 0 and j >= j1 and j <= j2) then`
`                   table.insert(legend[i], itemdata[k])`
`                   itemnums[k] = -1`
`               end`
`           end`
`       end`
`   end`

`   -- Add any left over items to the first legend`
`   for k = 1,#itemnums do`
`       if itemnums[k] >= 0 then`
`           table.insert(legend[1], itemdata[k])`
`       end`
`   end`

`   -- Build the legend`
`   if columns > 0 then`
`       for i = 1,5 do`
`           local locallegend = legend[i]`
`           if (locallegend and #locallegend > 0) then`
`               local cell = root:tag('tr'):tag('td')`
`               cell:wikitext(buildlegend(locallegend, columns, border, args['legend' .. i .. 'title'] or ''))`
`           end`
`       end`
`   end`

`   return tostring(root)`

end

return p