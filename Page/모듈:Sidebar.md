> This article is converted from Wikipedia: [모듈:Sidebar](https://ko.wikipedia.org/wiki/모듈:Sidebar).


\-- -- 이 모듈은 에 적용되는 모듈입니다. -- require('Module:No globals')

local p = {}

local getArgs = require('Module:Arguments').getArgs local navbar = require('Module:Navbar')._navbar

local function trimAndAddAutomaticNewline(s)

`   -- 예쁜 디자인을 위해 {{#if}}를 통해 파라미터를 넘겨서 흰색 공백을 다듬는`
`   -- ``와의 호환성을 위해 추가됨. 줄바꿈을 자동으로 해줌.`
`   -- (`[`meta:Help:Newlines``   ``and``   ``spaces#Automatic``   ``newline`](https://ko.wikipedia.org/wiki/meta:Help:Newlines_and_spaces#Automatic_newline "wikilink")`)`
`   s = mw.ustring.gsub(s, "^%s*(.-)%s*$", "%1")`
`   if mw.ustring.find(s, '^[#*:;]') or mw.ustring.find(s, '^{|') then`
`       return '\n' .. s`
`   else`
`       return s`
`   end`

end

local function hasSubgroup(s)

`   if mw.ustring.find(s, 'vertical%-navbox%-subgroup') then`
`       return true`
`   else`
`       return false`
`   end`

end

\-- 공통 (p.sidebar, p.collapsible) local param_ko_common = {

`   ['기본모양'] = 'basestyle', -- 본래 틀에 없던 항목`
`   ['윗제목모양'] = 'abovestyle',`
`   ['아랫글모양'] = 'belowstyle',`
`   ['안내바모양'] = 'navbarstyle',`
`   ['안내바'] = 'navbar',`
`   ['이름'] = 'name',`
`   -- [''] = 'tnavbarstyle',  -- 본래 틀에 없던 항목`

}

\-- p.sidebar 전용 local param_ko_sidebar = {

`   ['자식'] = 'child',`
`   --[''] = 'wraplinks',`
`   ['전체속성'] = 'bodyclass',`
`   ['속성'] = 'class',`
`   --[''] = 'float',`
`   ['너비'] = 'width',`
`   ['전체모양'] = 'bodystyle',`
`   ['모양'] = 'style',`
`   ['제목'] = 'title',`
`   ['큰제목'] = 'outertitle',`
`   ['큰제목속성'] = 'outertitleclass',`
`   ['큰제목모양'] = 'outertitlestyle',`
`   ['윗그림'] = 'topimage',`
`   ['윗그림속성'] = 'topimageclass',`
`   ['윗그림모양'] = 'topimagestyle',`
`   ['윗그림설명'] = 'topcaption',`
`   ['윗그림설명모양'] = 'topcaptionstyle',`
`   ['앞제목'] = 'pretitle',`
`   ['앞제목속성'] = 'pretitleclass',`
`   ['앞제목모양'] = 'pretitlestyle',`
`   ['제목속성'] = 'titleclass',`
`   ['제목모양'] = 'titlestyle',`
`   ['그림'] = 'image',`
`   ['그림속성'] = 'imageclass',`
`   ['그림모양'] = 'imagestyle',`
`   ['그림설명'] = 'caption',`
`   ['그림설명모양'] = 'captionstyle',`
`   ['윗제목'] = 'above',`
`   ['윗제목속성'] = 'aboveclass',`
`   ['묶음속성'] = 'headingclass',`
`   ['묶음모양'] = 'headingstyle',`
`   ['내용속성'] = 'contentclass',`
`   ['내용모양'] = 'contentstyle',`
`   ['아랫글'] = 'below',`
`   ['아랫글속성'] = 'belowclass',`
`   --[''] = 'tnavbar',`
`   --[''] = 'navbarfontstyle',`
`   --[''] = 'tnavbarfontstyle',`

}

\-- p.collapsible 전용 local param_ko_collapsible = {

`   ['확장'] = 'expanded',`
`   ['목록틀모양'] = 'listframestyle',`
`   ['목록제목속성'] = 'listtitleclass',`
`   ['목록제목모양'] = 'listtitlestyle',`
`   ['목록속성'] = 'listclass',`
`   ['목록모양'] = 'liststyle'`

}

local function localname(parameter, koArgs)

`   return koArgs[parameter] or parameter`

end

local function i18nConv(localArgs, koArgs)

`   local tmpLocalArgs = {}`
`   for k, v in pairs(localArgs) do`
`       if v ~= '' then`
`           tmpLocalArgs[localname(k, koArgs)] = v`
`       end`
`   end`
`   return tmpLocalArgs`

end

function p.sidebar(frame, args)

`   if not args then`
`       args = getArgs(frame)`
`   end`
`   args = i18nConv(args, param_ko_common)`
`   args = i18nConv(args, param_ko_sidebar)`
`   local root = mw.html.create()`
`   local child = args.child and mw.text.trim(args.child) == 'yes'`

`   root = root:tag('table')`
`   if not child then`
`       root `
`           :addClass('vertical-navbox')`
`           :addClass(args.wraplinks ~= 'true' and 'nowraplinks' or nil)`
`           :addClass(args.bodyclass or args.class)`
`           :css('float', args.float or 'right')`
`           :css('clear', (args.float == 'none' and 'both') or args.float or 'right')`
`           :css('width', args.width or '22.0em')`
`           :css('margin', args.float == 'left' and '0 1.0em 1.0em 0' or '0 0 1.0em 1.0em')`
`           :css('background', '#f9f9f9')`
`           :css('border', '1px solid #aaa')`
`           :css('padding', '0.2em')`
`           :css('border-spacing', '0.4em 0')`
`           :css('text-align', 'center')`
`           :css('line-height', '1.4em')`
`           :css('font-size', '88%')`
`           :cssText(args.bodystyle or args.style)`

`       if args.outertitle then`
`           root`
`               :tag('caption')`
`                   :addClass(args.outertitleclass)`
`                   :css('padding-bottom', '0.2em')`
`                   :css('font-size', '125%')`
`                   :css('line-height', '1.2em')`
`                   :css('font-weight', 'bold')`
`                   :cssText(args.outertitlestyle)`
`                   :wikitext(args.outertitle)`
`       end`

`       if args.topimage then`
`           local imageCell = root:tag('tr'):tag('td')`

`           imageCell`
`               :addClass(args.topimageclass)`
`               :css('padding', '0.4em 0')`
`               :cssText(args.topimagestyle)`
`               :wikitext(args.topimage)`

`           if args.topcaption then`
`               imageCell`
`                   :tag('div')`
`                       :css('padding-top', '0.2em')`
`                       :css('line-height', '1.2em')`
`                       :cssText(args.topcaptionstyle)`
`                       :wikitext(args.topcaption)`
`           end`
`       end`

`       if args.pretitle then`
`           root`
`               :tag('tr')`
`                   :tag('td')`
`                       :addClass(args.pretitleclass)`
`                       :cssText(args.basestyle)`
`                       :css('padding-top', args.topimage and '0.2em' or '0.4em')`
`                       :css('line-height', '1.2em')`
`                       :cssText(args.pretitlestyle)`
`                       :wikitext(args.pretitle)`
`       end`
`   else`
`       root`
`           :addClass('vertical-navbox-subgroup')`
`           :css('width', '100%')`
`           :css('margin', '0px')`
`           :css('border-spacing', '0px')`
`           :addClass(args.bodyclass or args.class)`
`           :cssText(args.bodystyle or args.style)`
`   end`

`   if args.title then`
`       if child then`
`           root`
`               :wikitext(args.title)`
`       else`
`           root`
`               :tag('tr')`
`                   :tag('th')`
`                       :addClass(args.titleclass)`
`                       :cssText(args.basestyle)`
`                       :css('padding', '0.2em 0.4em 0.2em')`
`                       :css('padding-top', args.pretitle and 0)`
`                       :css('font-size', '145%')`
`                       :css('line-height', '1.2em')`
`                       :cssText(args.titlestyle)`
`                       :wikitext(args.title)`
`       end`
`   end`

`   if args.image then`
`       local imageCell = root:tag('tr'):tag('td')`

`       imageCell`
`           :addClass(args.imageclass)`
`           :css('padding', '0.2em 0 0.4em')`
`           :cssText(args.imagestyle)`
`           :wikitext(args.image)`

`       if args.caption then`
`           imageCell`
`               :tag('div')`
`                   :css('padding-top', '0.2em')`
`                   :css('line-height', '1.2em')`
`                   :cssText(args.captionstyle)`
`                   :wikitext(args.caption)`
`       end`
`   end`

`   if args.above then`
`       root`
`           :tag('tr')`
`               :tag('td')`
`                   :addClass(args.aboveclass)`
`                   :css('padding', '0.3em 0.4em 0.3em')`
`                   :css('font-weight', 'bold')`
`                   :cssText(args.abovestyle)`
`                   :newline() -- 점 목록(*) 동작을 위해 줄바꿈 필요`
`                   :wikitext(args.above)`
`   end`

`   local rowNums = {}`
`   for k, v in pairs(args) do`
`       k = '' .. k`
`       local num = k:match('^heading(%d+)$') or k:match('^content(%d+)$') or k:match('^묶음(%d+)$') or k:match('^내용(%d+)$')`
`       if num then table.insert(rowNums, tonumber(num)) end`
`   end`
`   table.sort(rowNums)`
`   -- 리스트에서 중복된 것을 없애줌 (ex. 묶음3과 내용3에는 3이 중복)`
`   for i = #rowNums, 1, -1 do`
`       if rowNums[i] == rowNums[i - 1] then`
`           table.remove(rowNums, i)`
`       end`
`   end`

`   for i, num in ipairs(rowNums) do`
`       local heading = args['heading' .. num] or args['묶음' .. num]`
`       if heading then`
`           root`
`               :tag('tr')`
`                   :tag('th')`
`                       :addClass(args.headingclass)`
`                       :css('padding', '0.1em')`
`                       :cssText(args.basestyle)`
`                       :cssText(args.headingstyle)`
`                       :cssText(args['heading' .. num .. 'style'] or args['묶음' .. num .. '모양'])`
`                       :newline()`
`                       :wikitext(heading)`
`       end`

`       local content = args['content' .. num] or args['내용' .. num]`
`       if content then`
`           root`
`               :tag('tr')`
`                   :tag('td')`
`                       :addClass(args.contentclass)`
`                       :css('padding', hasSubgroup(content) and '0.1em 0 0.2em' or '0 0.1em 0.4em')`
`                       :cssText(args.contentstyle)`
`                       :cssText(args['content' .. num .. 'style'] or args['내용' .. num .. '모양'])`
`                       :newline()`
`                       :wikitext(content)`
`                       :done()`
`                   :newline() -- `

</td>

뒤에 줄바꿈이 없으면, "\* "처럼 얽혀있는 list들이 parse를 제대로 못함.

`       end`
`   end`

`   if args.below then`
`       root`
`           :tag('tr')`
`               :tag('td')`
`                   :addClass(args.belowclass)`
`                   :css('padding', '0.3em 0.4em 0.3em')`
`                   :css('font-weight', 'bold')`
`                   :cssText(args.belowstyle)`
`                   :newline()`
`                   :wikitext(args.below)`
`   end`

`   if not child then`
`       local navbarArg = args.navbar or args.tnavbar`
`       if navbarArg ~= 'none' and navbarArg ~= 'off' and (args.name or frame:getParent():getTitle():gsub('/연습장$', '') ~= '틀:사이드바') then`
`           root`
`               :tag('tr')`
`                   :tag('td')`
`                       :css('text-align', 'right')`
`                       :css('font-size', '115%')`
`                       :cssText(args.navbarstyle or args.tnavbarstyle)`
`                       :wikitext(navbar{`
`                           args.name,`
`                           mini = 1,`
`                           fontstyle = args.navbarfontstyle or args.tnavbarfontstyle`
`                       })`
`       end`
`   end`

`   return tostring(root) .. (child and '`[`분류:자식``   ``변수를``   ``사용하는``   ``사이드바가``   ``있는``   ``문서`](https://ko.wikipedia.org/wiki/분류:자식_변수를_사용하는_사이드바가_있는_문서 "wikilink")`' or '')`

end

function p.collapsible(frame)

`   local args = getArgs(frame)`

`   args = i18nConv(args, param_ko_common)`
`   args = i18nConv(args, param_ko_collapsible)`

`   args.abovestyle = 'border-top: 1px solid #aaa; border-bottom: 1px solid #aaa;' .. (args.abovestyle or '')`
`   args.belowstyle = 'border-top: 1px solid #aaa; border-bottom: 1px solid #aaa;' .. (args.belowstyle or '')`
`   args.navbarstyle = 'padding-top: 0.6em;' .. (args.navbarstyle or args.tnavbarstyle or '')`
`   if not args.name and frame:getParent():getTitle():gsub('/연습장$', '') == '틀:접이식 사이드바' then`
`       args.navbar = 'none'`
`   end`

`   local contentArgs = {}`

`   for k, v in pairs(args) do`
`       local num = string.match(k, '^list(%d+)$') or string.match(k, '^목록(%d+)$')`
`       if num then`
`           local expand = args.expanded and (args.expanded == 'all' or args.expanded == args['list' .. num .. 'name'] or args.expanded == args['목록' .. num .. '이름'])`

`           local row = mw.html.create('div')`
`           row`
`               :addClass('NavFrame')`
`               :addClass((not expand) and 'collapsed' or nil)`
`               :css('border', 'none')`
`               :css('padding', 0)`
`               :cssText(args.listframestyle)`
`               :cssText(args['list' .. num .. 'framestyle'] or args['목록' .. num .. '틀모양'])`
`               :tag('div')`
`                   :addClass('NavHead')`
`                   :addClass(args.listtitleclass)`
`                   :css('font-size', '105%')`
`                   :css('background', 'transparent')`
`                   :css('text-align', 'left')`
`                   :cssText(args.basestyle)`
`                   :cssText(args.listtitlestyle)`
`                   :cssText(args['list' .. num .. 'titlestyle'] or args['목록' .. num .. '제목모양'])`
`                   :wikitext(trimAndAddAutomaticNewline(args['list' .. num .. 'title'] or args['목록' .. num .. '제목'] or '목록'))`
`                   :done()`
`               :tag('div')`
`                   :addClass('NavContent')`
`                   :addClass(args.listclass)`
`                   :addClass(args['list' .. num .. 'class'] or args['목록' .. num .. '속성'])`
`                   :css('font-size', '105%')`
`                   :css('padding', '0.2em 0 0.4em')`
`                   :css('text-align', 'center')`
`                   :cssText(args.liststyle)`
`                   :cssText(args['list' .. num .. 'style'] or args['목록' .. num .. '모양'])`
`                   :wikitext(trimAndAddAutomaticNewline(args['list' .. num] or args['목록' .. num]))`

`           contentArgs['content' .. num] = tostring(row)`
`       end`
`   end`

`   for k, v in pairs(contentArgs) do`
`       args[k] = v`
`   end`

`   return p.sidebar(frame, args)`

end

return p