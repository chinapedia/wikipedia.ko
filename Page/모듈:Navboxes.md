> This article is converted from Wikipedia: [모듈:Navboxes](https://ko.wikipedia.org/wiki/모듈:Navboxes).


\-- This implements Template:navboxes local p = {}

local Navbox = require('Module:Navbox')

local param_ko = {

`   ['상태'] = 'state',`
`   ['제목'] = 'title',`
`   ['내용1'] = 'list1',`
`   ['내용'] = 'list',`
`   ['제목모양'] = 'titlestyle'`

}

local function localname(parameter)

`   return param_ko[parameter] or parameter`

end

local function i18nHelper(args)

`   local retArgs = args`
`   for k, v in pairs(args) do`
`       if v ~= '' then`
`           retArgs[localname(k)] = v`
`       end`
`   end`
`   return retArgs`

end

local function isnotempty(s)

`   return s and s:match( '^%s*(.-)%s*$' ) ~= ''`

end

local function navboxes(args, list)

`   local navbar = (args['state'] and args['state'] == 'off') and 'off' or 'plain'`
`   local title = args['title'] or '이 문서와 관련된 항목'`
`   local titlestyle = 'background:' .. (args['bg'] or '#e8e8ff') .. ';'`
`       .. (isnotempty(args['fg']) and ('color:' .. args['fg'] .. ';') or '')`
`       .. (isnotempty(args['bordercolor']) and ('border: 1px solid ' .. args['bordercolor'] .. ';') or '')`
`       .. (args['titlestyle'] or '')`
`   return Navbox._navbox({`
`           navbar = navbar, title = title, `
`           list1 = list,`
`           state = args['state'] or 'collapsed',`
`           titlestyle = titlestyle,`
`           liststyle = 'font-size:114%',`
`           listpadding = '0px',`
`           tracking = 'no'`
`           })`

end

function p.top(frame)

`   local args = frame:getParent().args`
`   args = i18nHelper(args)`
`   local parts = mw.text.split(navboxes(args, '`<ADD LIST HERE>`'), '`<ADD LIST HERE>`')`
`   return parts[1]`

end

function p.bottom(frame)

`   local args = {}`
`   args = i18nHelper(args)`
`   local parts = mw.text.split(navboxes(args, '`<ADD LIST HERE>`'), '`<ADD LIST HERE>`')`
`   return parts[2]`

end

function p.navbox(frame)

`   local args = frame:getParent().args`
`   args = i18nHelper(args)`
`   local list = args['list1'] or args['list'] or ''    `
`   local track_cats = ''`
`   if list == '' then`
`       if mw.title.getCurrentTitle().namespace == 0 then`
`           track_cats = '`[`분류:내용이``   ``없는``   ``둘러보기``   ``상자``   ``묶음``   ``틀`](https://ko.wikipedia.org/wiki/분류:내용이_없는_둘러보기_상자_묶음_틀 "wikilink")`'`
`       end`
`   end`
`   return navboxes(args, list) .. track_cats`

end

return p