> This article is converted from Wikipedia: [모듈:Airport destination list](https://ko.wikipedia.org/wiki/모듈:Airport_destination_list).


local p = {}

local function isnotempty(s)

`   return s and s:match( '^%s*(.-)%s*$' ) ~= ''`

end

function p.table(frame)

`   local args = (frame.args[1] ~= nil) and frame.args or frame:getParent().args`
`   local cols`
`   if isnotempty(args['4번째열']) and isnotempty(args['3번째열']) then`
`       cols = 4`
`   elseif isnotempty(args['3번째열']) then cols = 3`
`   else cols = 2`
`   end`

`   -- compute the maximum cell index`
`   local cellcount = 0`
`   for k, v in pairs( args ) do`
`       if type( k ) == 'number' and isnotempty(v) then`
`           cellcount = math.max(cellcount, k)`
`       end`
`   end`
`   -- compute the number of rows`
`   local rows = math.ceil(cellcount / cols)`

`   -- create the root table`
`   local root = mw.html.create('table')`
`   root`
`       :addClass('wikitable')`
`       :addClass('sortable')`
`       :css('font-size', '95%')`

`   -- add the header row`
`   local row = root:tag('tr')`
`   local cell= row:tag('th')`
`   cell:wikitext('항공사')`
`   cell= row:tag('th')`
`   cell:addClass('unsortable')`
`   cell:wikitext('목적지')`
`   if (isnotempty(args['3번째열'])) then`
`       cell= row:tag('th')`
`       cell:css('width','10%')`
`       cell:wikitext(args['3번째열'])`
`   end`
`   if (isnotempty(args['4번째열'])) then`
`       cell= row:tag('th')`
`       cell:wikitext(args['4번째열'])`
`   end`
`   -- loop over rows`
`   for j=1,rows do`
`       row = root:tag('tr')`
`       for i=1,cols do`
`           cell= row:tag('td')`
`           if (i > 2) then cell:css('text-align','center') end`
`           cell:wikitext(args[cols*(j - 1) + i] or '')`
`       end`
`   end`
`   -- return the root table`
`   return tostring(root)`

end

return p