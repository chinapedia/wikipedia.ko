> This article is converted from Wikipedia: [모듈:Navbox temp](https://ko.wikipedia.org/wiki/모듈:Navbox_temp).


\-- --  구현을 위한 모듈입니다. --

local p = {}

local navbar = require('모듈:Navbar')._navbar local getArgs -- lazily initialized

local args local tableRowAdded = false local border local listnums = {}

local function trim(s)

`   return (mw.ustring.gsub(s, "^%s*(.-)%s*$", "%1"))`

end

local function addNewline(s)

`   if s:match('^[*:;#]') or s:match('^{|') then`
`       return '\n' .. s ..'\n'`
`   else`
`       return s`
`   end`

end

local function addTableRow(tbl)

`   -- If any other rows have already been added, then we add a 2px gutter row.`
`   if tableRowAdded then`
`       tbl`
`           :tag('tr')`
`               :css('height', '2px')`
`               :tag('td')`
`                   :attr('colspan',2)`
`   end`

`   tableRowAdded = true`

`   return tbl:tag('tr')`

end

local function renderNavBar(titleCell)

`   -- Depending on the presence of the navbar and/or show/hide link, we may need to add a spacer div on the left`
`   -- or right to keep the title centered.`
`   local spacerSide = nil`

`   if args['상태'] == 'off' then`
`       -- No navbar, and client wants no spacer, i.e. wants the title to be shifted to the left. If there's`
`       -- also no show/hide link, then we need a spacer on the right to achieve the left shift.`
`       if args['상태'] == 'plain' then spacerSide = 'right' end`
`   elseif args.navbar == 'plain' or (not args['이름'] and mw.getCurrentFrame():getParent():getTitle():gsub('/sandbox$', '') == '틀:둘러보기 상자') then`
`       -- No navbar. Need a spacer on the left to balance out the width of the show/hide link.`
`       if args['상태'] ~= 'plain' then spacerSide = 'left' end`
`   else`
`       -- Will render navbar (or error message). If there's no show/hide link, need a spacer on the right`
`       -- to balance out the width of the navbar.`
`       if args['상태'] == 'plain' then spacerSide = 'right' end`

`       titleCell:wikitext(navbar{`
`           args['이름'],`
`           mini = 1,`
`           fontstyle = (args['기반모양'] or '') .. ';' .. (args['제목모양'] or '') ..  ';background:none transparent;border:none;'`
`       })`
`   end`

`   -- Render the spacer div.`
`   if spacerSide then`
`       titleCell`
`           :tag('span')`
`               :css('float', spacerSide)`
`               :css('width', '6em')`
`               :wikitext(' ')`
`   end`

end

\-- -- 제목 구문 -- local function renderTitleRow(tbl)

`   if not args['제목'] then return end`

`   local titleRow = addTableRow(tbl)`

`   if args['제목묶음'] then`
`       titleRow`
`           :tag('th')`
`               :attr('scope', 'row')`
`               :addClass('navbox-group')`
`               :addClass(args['제목묶음속성'])`
`               :cssText(args['기반모양'])`
`               :cssText(args['묶음모양'])`
`               :cssText(args['제목묶음모양'])`
`               :wikitext(args['제목묶음'])`
`   end`

`   local titleCell = titleRow:tag('th'):attr('scope', 'col')`

`   if args['제목묶음'] then`
`       titleCell`
`           :css('border-left', '2px solid #fdfdfd')`
`           :css('width', '100%')`
`   end`

`   local titleColspan = 2`
`   if args['왼쪽그림'] then titleColspan = titleColspan + 1 end`
`   if args['그림'] then titleColspan = titleColspan + 1 end`
`   if args['제목묶음'] then titleColspan = titleColspan - 1 end`

`   titleCell`
`       :cssText(args['기반모양'])`
`       :cssText(args['제목모양'])`
`       :addClass('navbox-title')`
`       :attr('colspan', titleColspan)`

`   renderNavBar(titleCell)`

`   titleCell`
`        :tag('div')`
`            :addClass(args['제목속성'])`
`            :css('font-size', '114%')`
`            :wikitext(addNewline(args['제목']))`

end

\-- -- 아랫글/윗글 구문 --

local function getAboveBelowColspan()

`   local ret = 2`
`   if args['왼쪽그림'] then ret = ret + 1 end`
`   if args['그림'] then ret = ret + 1 end`
`   return ret`

end

local function renderAboveRow(tbl)

`   if not args['윗글'] then return end`

`   addTableRow(tbl)`
`       :tag('td')`
`           :addClass('navbox-abovebelow')`
`           :addClass(args['윗글속성'])`
`           :cssText(args['기반모양'])`
`           :cssText(args['윗글모양'])`
`           :attr('colspan', getAboveBelowColspan())`
`           :tag('div')`
`               :wikitext(addNewline(args['윗글']))`

end

local function renderBelowRow(tbl)

`   if not args['아랫글'] then return end`

`   addTableRow(tbl)`
`       :tag('td')`
`           :addClass('navbox-abovebelow')`
`           :addClass(args['아랫글속성'])`
`           :cssText(args['기반모양'])`
`           :cssText(args['아랫글모양'])`
`           :attr('colspan', getAboveBelowColspan())`
`           :tag('div')`
`               :wikitext(addNewline(args['아랫글']))`

end

\-- -- 내용 구문 -- local function renderListRow(tbl, listnum)

`   local row = addTableRow(tbl)`

`   if listnum == 1 and args['왼쪽그림'] then`
`       row`
`           :tag('td')`
`               :addClass('navbox-image')`
`               :addClass(args['그림속성'])`
`               :css('width', '0%')`
`               :css('padding', '0px 2px 0px 0px')`
`               :cssText(args['왼쪽그림모양'])`
`               :attr('rowspan', 2 * #listnums - 1)`
`               :tag('div')`
`                   :wikitext(addNewline(args['왼쪽그림']))`
`   end`

`   if args['묶음' .. listnum] then`
`       local groupCell = row:tag('th')`

`       groupCell`
`           :attr('scope', 'row')`
`           :addClass('navbox-group')`
`           :addClass(args['묶음속성'])`
`           :cssText(args['기반모양'])`

`       if args['묶음너비'] then`
`           groupCell:css('width', args['묶음너비'])`
`       end`

`       groupCell`
`           :cssText(args['묶음모양'])`
`           :cssText(args['묶음' .. listnum .. '모양'])`
`           :wikitext(args['묶음' .. listnum])`
`   end`

`   local listCell = row:tag('td')`

`   if args['묶음' .. listnum] then`
`       listCell`
`           :css('text-align', 'left')`
`           :css('border-left-width', '2px')`
`           :css('border-left-style', 'solid')`
`   else`
`       listCell:attr('colspan', 2)`
`   end`

`   if not args['묶음너비'] then`
`       listCell:css('width', '100%')`
`   end`

`   local isOdd = (listnum % 2) == 1`
`   local rowstyle = args['짝수모양']`
`   if isOdd then rowstyle = args['홀수모양'] end`

`   local evenOdd`
`   if args.evenodd == 'swap' then`
`       if isOdd then evenOdd = 'even' else evenOdd = 'odd' end`
`   else`
`       if isOdd then evenOdd = args.evenodd or 'odd' else evenOdd = args.evenodd or 'even' end`
`   end`

`   listCell`
`       :css('padding', '0px')`
`       :cssText(args['내용모양'])`
`       :cssText(rowstyle)`
`       :cssText(args['내용' .. listnum .. '모양'])`
`       :addClass('navbox-list')`
`       :addClass('navbox-' .. evenOdd)`
`       :addClass(args['내용속성'])`
`       :tag('div')`
`           :css('padding', (listnum == 1 and args.list1padding) or args.listpadding or '0em 0.25em')`
`           :wikitext(addNewline(args['내용' .. listnum]))`

`   if listnum == 1 and args['그림'] then`
`       row`
`           :tag('td')`
`               :addClass('navbox-image')`
`               :addClass(args['그림속성'])`
`               :css('width', '0%')`
`               :css('padding', '0px 0px 0px 2px')`
`               :cssText(args['그림모양'])`
`               :attr('rowspan', 2 * #listnums - 1)`
`               :tag('div')`
`                   :wikitext(addNewline(args['그림']))`
`   end`

end

\-- -- 분류 추적 --

local function needsHorizontalLists()

`   if border == 'child' or border == 'subgorup'  or args.tracking == 'no' then return false end`

`   local listClasses = {'plainlist', 'hlist', 'hlist hnum', 'hlist hwrap', 'hlist vcard', 'vcard hlist', 'hlist vevent'}`
`   for i, cls in ipairs(listClasses) do`
`       if args['내용속성'] == cls or args['내용속성'] == cls then`
`           return false`
`       end`
`   end`

`   return true`

end

local function hasBackgroundColors()

`   return mw.ustring.match(args['제목모양'] or '','background') or mw.ustring.match(args['묶음모양'] or '','background') or mw.ustring.match(args['기반모양'] or '','background')`

end

local function isIllegible()

`   local styleratio = require('모듈:Color contrast')._styleratio`

`   for key, style in pairs(args) do`
`       if tostring(key):match("style$") then`
`           if styleratio{mw.text.unstripNoWiki(style)} < 4.5 then`
`               return true `
`           end`
`       end`
`   end`
`   return false`

end

local function getTrackingCategories()

`   local cats = {}`
`   if needsHorizontalLists() then table.insert(cats, '가로 목록을 지원하지 않는 둘러보기 틀') end`
`   if hasBackgroundColors() then table.insert(cats, '배경색을 사용하는 둘러보기 틀') end`
`   if isIllegible() then table.insert(cats, '읽기 어려울 수 있는 둘러보기 틀') end`
`   return cats`

end

local function renderTrackingCategories(builder)

`   local title = mw.title.getCurrentTitle()`
`   if title.namespace ~= 10 then return end -- not in template space`
`   local subpage = title.subpageText`
`   if subpage == 'doc' or subpage == 'sandbox' or subpage == 'testcases' then return end`

`   for i, cat in ipairs(getTrackingCategories()) do`
`       builder:wikitext('`[`분류:'``   ``..``   ``cat``   ``..``   ``'`](https://ko.wikipedia.org/wiki/분류:'_.._cat_.._' "wikilink")`')`
`   end`

end

\-- -- 둘러보기 상자 표 본문 구문 -- local function renderMainTable()

`   local tbl = mw.html.create('table')`
`       :addClass('nowraplinks')`
`       :addClass(args['내용속성'])`

`   if args.title and (args['상태'] ~= 'plain' and args['상태'] ~= 'off') then`
`       tbl`
`           :addClass('collapsible')`
`           :addClass(args['상태'] or 'autocollapse')`
`   end`

`   tbl:css('border-spacing', 0)`
`   if border == 'subgroup' or border == 'child' or border == 'none' then`
`       tbl`
`           :addClass('navbox-subgroup')`
`           :cssText(args['내용모양'])`
`           :cssText(args['모양'])`
`   else -- regular navobx - bodystyle and style will be applied to the wrapper table`
`       tbl`
`           :addClass('navbox-inner')`
`           :css('background', 'transparent')`
`           :css('color', 'inherit')`
`   end`
`   tbl:cssText(args['내부모양'])`

`   renderTitleRow(tbl)`
`   renderAboveRow(tbl)`
`   for i, listnum in ipairs(listnums) do`
`       renderListRow(tbl, listnum)`
`   end`
`   renderBelowRow(tbl)`

`   return tbl`

end

function p._navbox(navboxArgs)

`   args = navboxArgs`

`   for k, v in pairs(args) do`
`       local listnum = ('' .. k):match('^list(%d+)$')`
`       if listnum then table.insert(listnums, tonumber(listnum)) end`
`   end`
`   table.sort(listnums)`

`   border = trim(args['border'] or args[1] or '')`

`   -- render the main body of the navbox`
`   local tbl = renderMainTable()`

`   -- render the appropriate wrapper around the navbox, depending on the border param`
`   local res = mw.html.create()`
`   if border == 'none' then`
`       `<res:node(tbl)>
`   elseif border == 'subgroup' or border == 'child' then`
`       -- We assume that this navbox is being rendered in a list cell of a parent navbox, and is`
`       -- therefore inside a div with padding:0em 0.25em. We start with a `

</div>

to avoid the

`       -- padding being applied, and at the end add a `

<div>

to balance out the parent's

</div>

`       res`
`           :wikitext('`

</div>

') -- XXX: hack due to lack of unclosed support in mw.html.

`           :node(tbl)`
`           :wikitext('`

<div>

') -- XXX: hack due to lack of unclosed support in mw.html.

`   else`
`       res`
`           :tag('table')`
`               :addClass('navbox')`
`               :css('border-spacing', 0)`
`               :cssText(args['내용모양'])`
`               :cssText(args['모양'])`
`               :tag('tr')`
`                   :tag('td')`
`                       :css('padding', '2px')`
`                       :node(tbl)`
`   end`

`   renderTrackingCategories(res)`

`   return tostring(res)`

end

function p.navbox(frame)

`   if not getArgs then`
`       getArgs = require('모듈:Arguments').getArgs`
`   end`
`   args = getArgs(frame, {wrappers = '틀:둘러보기 상자'})`

`   -- Read the arguments in the order they'll be output in, to make references number in the right order.`
`   local _`
`   _ = args['제목']`
`   _ = args['윗글']`
`   for i = 1, 20 do`
`       _ = args["묶음" .. tostring(i)]`
`       _ = args["내용" .. tostring(i)]`
`   end`
`   _ = args['아랫글']`

`   return p._navbox(args)`

end

return p