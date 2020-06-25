> This article is converted from Wikipedia: [모듈:Video game release](https://ko.wikipedia.org/wiki/모듈:Video_game_release).


require('Module:No globals')

local getArgs = require('Module:Arguments').getArgs local cd = require('Module:CountryData') local list = require('Module:List'); local p = {}

local labels = {

`   ['NA'] = "`[`북미`](../Page/북아메리카.md "wikilink")`",`
`   ['EU'] = "`[`유럽`](../Page/유럽.md "wikilink")`",`
`   ['EUR'] = "`[`유럽`](../Page/유럽.md "wikilink")`",`
`   ['AU'] = "`[`호주`](../Page/오스트레일리아.md "wikilink")`",`
`   ['AUS'] = "`[`호주`](../Page/오스트레일리아.md "wikilink")`",`
`   ['PAL'] = "`[`PAL`](../Page/PAL_지역.md "wikilink")`",`
`   ['SEA'] = "`[`동남아`](../Page/동남아시아.md "wikilink")`",`
`   ['AS'] = "`[`아시아`](../Page/아시아.md "wikilink")`",`
`   ['SA'] = "`[`남미`](../Page/남아메리카.md "wikilink")`",`
`   ['INT'] = "`<abbr title=\"국제판\">`국제`</abbr>`",`
`   ['WW'] = "전 세계",`
`   ['JP'] = "`[`일본`](../Page/일본.md "wikilink")`",`
`   ['KR'] = "`[`한국`](../Page/대한민국.md "wikilink")`",`
`   ['CN'] = "`[`중국`](../Page/중화인민공화국.md "wikilink")`",`
`   ['TW'] = "`[`대만`](../Page/중화민국.md "wikilink")`",`
`   ['HK'] = "`[`홍콩`](../Page/홍콩.md "wikilink")`",`
`   ['UK'] = "`[`영국`](../Page/영국.md "wikilink")`",`
`   ['US'] = "`[`미국`](../Page/미국.md "wikilink")`",`
`   ['CA'] = "`[`캐나다`](../Page/캐나다.md "wikilink")`",`
`   ['NZ'] = "`[`뉴질랜드`](../Page/뉴질랜드.md "wikilink")`",`
`   ['NZL'] = "`[`뉴질랜드`](../Page/뉴질랜드.md "wikilink")`",`
`   ['?'] = "<abbr title=\"알 수 없음\">?`</abbr>`"`

}

local function getLocalLabel(alias)

`   local label = labels[string.upper(alias)] `

`   return label`

end

local countryData = {}; -- Used to store country data to avoid the need of repeated calls to Module:CountryData. This saves a little time if the same abbreviation appears multiple times in the template.

local function getCountryData(frame, alias)

`   local ualias = string.upper(alias)`
`   `
`   if(countryData[ualias] == nil) then`
`       local cdtable = cd.gettable(frame,alias,{})`
`       countryData[ualias] = cdtable['alias']`
`   end`

`   return countryData[ualias]`

end

function p.main(frame)

`   local args = getArgs(frame)`
`   local listformat = args['format']`
`   if(listformat == nil or listformat == "") then`
`       listformat = "unbulleted"`
`   end`
`   local items = {}`
`   `
`   -- Old syntax "Two parameter region" use case, where param 1 is an article, param 2 is a label, and param 3 is the date. We assume this case if argument 4 is nil.`
`   if(args[3] ~= nil and args[4] == nil) then`
`       local item = "`<span style=\"font-size:95%;\">`[["`
`       if(args[1] ~= nil) then`
`           item = item .. args[1]`
`       end`
`       item = item .. "|"`
`       if(args[2] ~= nil) then`
`           item = item .. args[2]`
`       end`
`       item = item .. "]]:`</span>` " .. args[3] .. "`[`분류:두``   ``개의``   ``변수``   ``지역``   ``없이``   ``vgarelease가``   ``쓰인``   ``글`](https://ko.wikipedia.org/wiki/분류:두_개의_변수_지역_없이_vgarelease가_쓰인_글 "wikilink")`"`
`       table.insert(items, item)`
`   -- Old syntax "Blank region" use case, where param 1 is empty, and param 2 is the date.`
`   elseif(args[1] == nil and args[2] ~= nil) then`
`       local item = args[2] .. "`[`분류:지역``   ``없이``   ``vgrelease가``   ``쓰인``   ``글`](https://ko.wikipedia.org/wiki/분류:지역_없이_vgrelease가_쓰인_글 "wikilink")`"`
`       table.insert(items, item)`
`   -- Normal use cases, region/date pairs in 1/2, 3/4, 5/6, etc.`
`   else`
`       local i = 1`
`       local j = 2`
`       while(args[i] and args[j]) do`
`           local label = getLocalLabel(args[i]);`
`       `
`           -- Didn't find a local label? Check for country data.`
`           if(label == nil) then`
`               label = getCountryData(frame, args[i])`
`           `
`               -- Found something? Build a sitelink with it.`
`               if(label ~= nil) then`
`                   label = "[["_.._label_.._"|" .. args[i] .. "]]"`
`               else`
`                   label = args[i]`
`               end`
`           end`

`           local item = "`<span style=\"font-size:95%;\">`" .. label .. ":`</span>` " .. args[j]`
`           table.insert(items, item)`
`     `
`           i = i + 2`
`           j = j + 2`
`       end`
`   end`

`   local out = list.makeList(listformat, items)`

`   -- Set message for invalid parameters. Decide catagory based on list format chosen.`
`   local parameterMsg`
`   if(listformat == "horizontal") then`
`       parameterMsg = "`[`_VALUE_`](https://ko.wikipedia.org/wiki/분류:명명된_변수_없이_vgarelease_hlist가_쓰인_글 "wikilink")`"`
`   else`
`       parameterMsg = "`[`_VALUE_`](https://ko.wikipedia.org/wiki/분류:명명된_변수_없이_vgarelease가_쓰인_글 "wikilink")`"`
`   end`
`   `
`   -- Preview message.`
`   if(frame:preprocess( "``" ) == "") then`
`       parameterMsg = "`

<div class=\"hatnote\" style=\"color:red\">

<strong>경고:</strong> 알 수 없는 변수 \\"_VALUE_\\" (이 메시지는 미리 보기에서만 표시됩니다).

</div>

"

`   end`
`   `
`   -- Check for named parameters   `
`   for k, v in pairs(args) do`
`       if(type(k) ~= 'number' and k ~= 'format') then`
`           local msg = parameterMsg:gsub('_VALUE_', k)`
`           out = out .. msg`
`       end`
`   end`

`   return out`

end

return p