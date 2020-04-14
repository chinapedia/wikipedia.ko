> This article is converted from Wikipedia: [모듈:Sports results](https://ko.wikipedia.org/wiki/모듈:Sports_results).


\-- Module to build results cross-tables for standings in Sports -- See documentation for details

require('Module:No globals')

local p = {}

\-- Main function function p.main(frame)

`   -- Declare locals`
`   local Args = frame.args`
`   local N_teams = 0`
`   local t = {}`
`   local t_footer = {}`
`   local t_return = {}`
`   local team_list = {}`
`   local ii, ii_fw, bg_col, team_name, team_code_ii`
`   `
`   -- Load some other modules`
`   local p_sub = require('Module:Sports table/sub')`
`   `
`   -- Read in number of consecutive teams (ignore entries after skipping a spot)`
`   while Args['team'..N_teams+1] ~= nil do`
`       N_teams = N_teams+1`
`       -- Sneakily add it twice to the team_list parameter, once for the actual`
`       -- ranking, the second for position lookup in sub-tables`
`       -- This is possible because Lua allows both numbers and strings as indices.`
`       team_list[N_teams] = Args['team'..N_teams] -- i^th entry is team X`
`       team_list[Args['team'..N_teams]] = N_teams -- team X entry is position i`
`   end`
`   `
`   -- Get team to show`
`   local ii_show = team_list[Args['showteam']] -- nil if non-existant`
`   `
`   -- Create header`
`   -- Open table`
`   table.insert(t,'{|class="wikitable" style="text-align:center;"\n') `
`   -- First column`
`   t_return.count = 0          -- Dummy parameter, using subfunction call seems best at this point because both module are intertwined`
`   t_return.tab_text = t       -- Actual text`
`   t_return = p_sub.colhead(t_return,'auto','홈 \\ 어웨이')    `
`   -- Other columns passed to subfunction`
`   t_return = p.header(t_return,Args,p_sub,N_teams,team_list)`
`   t = t_return.tab_text`
`   `
`   -- Now create individual rows`
`   for ii=1,N_teams do`
`       -- Get team info`
`       team_code_ii = team_list[ii]`
`       team_name = Args['name_'..team_code_ii]         or team_code_ii`
`       `
`       -- Team names`
`       table.insert(t,'|- \n')                                                                         -- New row`
`       table.insert(t,'! scope="row" style="text-align: right;"| '..team_name..'\n')   -- Position number`
`       `
`       -- Then individual results`
`       t = p.row(t,Args,N_teams,team_list,ii,ii_show)`
`   end`
`   `
`   -- Close table`
`   table.insert(t, '|}\n')`
`   `
`   -- Get info for footer`
`   local update = Args['update']           or 'unknown'`
`   local start_date = Args['start_date']   or 'unknown'`
`   local source = Args['source']           or frame:expandTemplate{ title = '출처', args = { ['날짜'] = os.date('%Y-%m-%d') } }`
`   `
`   -- Create footer text`
`   -- Date updating`
`   if string.lower(update)=='complete' then`
`       -- Do nothing`
`   elseif update=='' then`
`       -- Empty parameter`
`       table.insert(t_footer,'Updated to match(es) played on unknown. ')`
`   elseif string.lower(update)=='future' then`
`       -- Future start date`
`       table.insert(t_footer,'First match(es) will be played on '..start_date..'. ')`
`   else`
`       table.insert(t_footer,'Updated to match(es) played on '..update..'. ')`
`   end`
`   table.insert(t_footer,'Source: '..source)`
`   -- As reflist size text`
`   t_footer = '`

<div class="reflist">

'..table.concat(t_footer)..'

</div>

'

`   -- Add footer to main text table`
`   table.insert(t,t_footer)`
`   `
`   return table.concat(t)`

end

\-- Other functions function p.header(tt,Args,p_sub,N_teams,team_list)

`   local ii, team_code_ii, short_name`
`   `
`   -- Set match column width`
`   local col_width = Args['match_col_width'] or '28'`
`   `
`   -- Get some default values in case it doesn't start at 1`
`   local top_pos = tonumber(Args['highest_pos']) or 1`
`   `
`   for ii=top_pos,N_teams do`
`       team_code_ii = team_list[ii]`
`       short_name = Args['short_'..team_code_ii]   or team_code_ii`
`       tt = p_sub.colhead(tt,col_width,short_name)`
`   end`
`   `
`   return tt`

end

function p.row(tt,Args,N_teams,team_list,ii,ii_show)

`   -- Note ii is the row number being shown`
`   local jj, fw, bg, result, team_code_ii, team_code_jj`
`   local cell_bold = false`
`   `
`   team_code_ii = team_list[ii]`
`   `
`   -- Get some default values in case it doesn't start at 1`
`   local top_pos = tonumber(Args['highest_pos']) or 1`
`   `
`   for jj=top_pos,N_teams do`
`       if ii == jj then`
`           -- Solid cell`
`           if ii==ii_show then cell_bold = true else cell_bold = false end`
`           fw = cell_bold and 'font-weight: bold;' or 'font-weight: normal;'`
`           bg = 'background-color:transparent;'`
`           table.insert(tt,'| style="'..fw..bg..'" | —\n')`
`       else`
`           -- Content cell`
`           -- Set bolding and background`
`           if ii==ii_show or jj == ii_show then cell_bold = true else cell_bold = false end`
`           fw = cell_bold and 'font-weight: bold;' or 'font-weight: normal;'`
`           bg = 'background-color:transparent;'`
`           `
`           -- Now for the actual result`
`           team_code_jj = team_list[jj]`
`           result = Args['match_'..team_code_ii..'_'..team_code_jj] or ''`
`           table.insert(tt,'| style="white-space:nowrap;'..fw..bg..'" |'..result..'\n')`
`       end`
`   end`
`   `
`   return tt`

end

return p