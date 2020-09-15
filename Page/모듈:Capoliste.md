> This article is converted from Wikipedia: [모듈:Capoliste](https://ko.wikipedia.org/wiki/모듈:Capoliste).


\-- -- This module will implement  -- require('Module:No globals') local getArgs = require('Module:Arguments').getArgs

local p = {}

local function read_squadre(args, giornate)

`   local read_next = true`
`   local squadre =  {}`
`   local i = 1`
`   while read_next do`
`       local basename = 'c' .. tostring(i)`
`       local nome = args[basename .. '-nome']`
`       if nome then `
`           squadre[i] = {}`
`           squadre[i].nome = nome`
`           squadre[i].da = tonumber(args[basename .. '-da'] or '')`
`           squadre[i].a = tonumber(args[basename .. '-a'] or '')`
`           squadre[i].colore = args[basename .. '-colore'] or '#FFFFFF'`
`           if squadre[i].da and squadre[i].da > giornate then `
`               squadre[i].da = giornate`
`               read_next = false`
`           end`
`           if squadre[i].a and squadre[i].a > giornate then `
`               squadre[i].a = giornate`
`               read_next = false`
`           end`
`       else`
`           read_next = false`
`       end`
`       i = i + 1`
`   end`
`   if #squadre == 0 then return squadre end`
`   -- annullo i valori negativi`
`   for _,squadra in ipairs(squadre) do`
`       if squadra.da and (squadra.da < 0 or squadra.da > giornate) then squadra.da = nil end`
`       if squadra.a and (squadra.a < 0 or squadra.a > giornate) then squadra.a = nil end`
`   end`
`   --normalizzo e assegno valori di default se il valore da o a non è assegnato`
`   squadre[1].da = squadre[1].da or 1`
`   for i = 2, #squadre do`
`       squadre[i].da = squadre[i].da or ((squadre[i-1].a or squadre[i-1].da) +1)`
`   end`
`   squadre[#squadre].a = squadre[#squadre].a or giornate`
`   for i = 1, #squadre-1 do`
`       squadre[i].a = squadre[i].a or (squadre[i+1].da -1)`
`   end `
`   return squadre`

end

function p.capoliste(frame)

`   local args = getArgs(frame) `
`   local giornate = tonumber(args.giornate) or 38 `
`   local squadre = read_squadre(args, giornate)`
`   --if #squadre == 0 then return '`<span class="errore">`Nessuna capolista inserita`</span>`' end`
`   --if true then return mw.text.jsonEncode(squadre) end`
`   local div = mw.html.create('div'):css('overflow', 'auto')`
`   local int_table = div:tag('table'):cssText('font-size:80%; text-align:center; border-collapse:collapse;')`
`   `
`   --prima riga per il dimensionamento`
`   local first_row = int_table:tag('tr'):css('visibility', 'hidden')`
`   first_row:tag('td'):attr('rowspan', '5'):attr('width', '10px')`
`   first_row:tag('td'):wikitext('——'):css('height', '25px')`
`   for i = 2, giornate do first_row:tag('td'):wikitext('——') end`
`   first_row:tag('td'):attr('rowspan', '5'):attr('width', '1px')`
`   `
`   --riga per i nomi`
`   local name_row = int_table:tag('tr'):cssText('font-family:Arial Narrow; font-size:105%; vertical-align:bottom;')`
`   local last_pos = 0`
`   for _,squadra in ipairs(squadre) do`
`       if squadra.da > last_pos + 1 then`
`           name_row:tag('th'):attr('colspan', tostring(squadra.da - last_pos - 1))`
`       end`
`       name_row:tag('th'):attr('colspan', tostring(squadra.a - squadra.da + 1)):wikitext(squadra.nome)`
`       last_pos = squadra.a`
`   end`
`   if last_pos < giornate then name_row:tag('th'):attr('colspan', tostring(giornate-last_pos)) end`
`   `
`   -- riga per le bande colorate`
`   local color_row = int_table:tag('tr'):css('height', '15px')`
`   last_pos = 0`
`   for _,squadra in ipairs(squadre) do`
`       if squadra.da > last_pos + 1 then`
`           color_row:tag('td'):attr('colspan', tostring(squadra.da - last_pos - 1))`
`       end     `
`       color_row:tag('td')`
`           :attr('colspan', tostring(squadra.a - squadra.da + 1))`
`           :cssText('border-left:inset 1px white;')`
`           :css('background', squadra.colore)`
`       last_pos = squadra.a`
`   end`
`   if last_pos < giornate then color_row:tag('td'):attr('colspan', tostring(giornate-last_pos)) end`

`   --riga per righello`
`   local ruler_row = int_table:tag('tr'):cssText('border-top:solid 1px black;')`
`   local ruler_style = 'border-left:solid 1px black;'`
`   ruler_row:tag('td'):cssText(ruler_style):attr('height', '1px'):wikitext(' ')`
`   for i = 2, giornate-1 do ruler_row:tag('td'):cssText(ruler_style):wikitext(' ') end`
`   ruler_row:tag('td'):cssText('border-left:solid 1px black; border-right:solid 1px black;'):wikitext(' ')`

`   --riga per header`
`   local header_row = int_table:tag('tr')`
`   for i=1, giornate do header_row:tag('th'):wikitext(tostring(i) .. 'ª') end`

`   -- ritorno il risultato`
`   return tostring(div)`

end

return p