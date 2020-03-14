> This article is converted from Wikipedia: [:Navbar](https://ko.wikipedia.org/wiki/:Navbar).


local p = {}

local getArgs

function p._navbar(args)

`   local titleArg = 1`

`   if args.collapsible then`
`       titleArg = 2`
`       if not args.plain then`
`           args.mini = 1`
`       end`
`       if args.fontcolor then`
`           args.fontstyle = 'color:' .. args.fontcolor .. ';'`
`       end`
`       args.style = 'float:left; text-align:left'`
`   end`

`   local titleText = args[titleArg] or (':' .. mw.getCurrentFrame():getParent():getTitle())`
`   local title = mw.title.new(mw.text.trim(titleText), '틀');`

`   if not title then`
`       error(titleText .. ' 문서가 존재하지 않습니다.')`
`   end`

`   local talkpage = title.talkPageTitle and title.talkPageTitle.fullText or '';`

`   local div = mw.html.create():tag('div')`
`   div`
`       :addClass('plainlinks')`
`       :addClass('hlist')`
`       :addClass('navbar')`
`       :cssText(args.style)`

`   if args.mini then div:addClass('mini') end`

`   if not (args.mini or args.plain) then`
`       div`
`           :tag('span')`
`               :css('word-spacing', 0)`
`               :cssText(args.fontstyle)`
`               :wikitext(args.text or 'This box:')`
`               :wikitext(' ')`
`   end`

`   if args.brackets then`
`       div`
`           :tag('span')`
`               :css('margin-right', '-0.125em')`
`               :cssText(args.fontstyle)`
`               :wikitext('[ ')`
`   end`

`   local ul = div:tag('ul');`

`   ul`
`       :tag('li')`
`           :addClass('nv-view')`
`           :wikitext('[[' .. title.fullText .. '|')`
`           :tag(args.mini and 'abbr' or 'span')`
`               :attr('title', '이 틀을 보기')`
`               :cssText(args.fontstyle)`
`               :wikitext(args.mini and 'v' or '보기')`
`               :done()`
`           :wikitext(']]')`
`           :done()`
`       :tag('li')`
`           :addClass('nv-talk')`
`           :wikitext('[[' .. talkpage .. '|')`
`           :tag(args.mini and 'abbr' or 'span')`
`               :attr('title', '이 틀에 대한 토론')`
`               :cssText(args.fontstyle)`
`               :wikitext(args.mini and 'd' or '토론')`
`               :done()`
`           :wikitext(']]');`

`   if not args.noedit then`
`       ul`
`           :tag('li')`
`               :addClass('nv-edit')`
`               :wikitext('[' .. title:fullUrl('action=edit') .. ' ')`
`               :tag(args.mini and 'abbr' or 'span')`
`                   :attr('title', '이 틀을 편집하기')`
`                   :cssText(args.fontstyle)`
`                   :wikitext(args.mini and 'e' or '편집')`
`                   :done()`
`               :wikitext(']');`
`   end`

`   if not args.history then`
`       ul`
`           :tag('li')`
`               :addClass('nv-history')`
`               :wikitext('[' .. title:fullUrl('action=history') .. ' ')`
`               :tag(args.mini and 'abbr' or 'span')`
`                   :attr('title', '이 틀의 역사')`
`                   :cssText(args.fontstyle)`
`                   :wikitext(args.mini and 'h' or '역사')`
`                   :done()`
`               :wikitext(']');`
`   end`
`   `
`   if args.brackets then`
`       div`
`           :tag('span')`
`               :css('margin-left', '-0.125em')`
`               :cssText(args.fontstyle)`
`               :wikitext(' ]')`
`   end`

`   if args.collapsible then`
`       div`
`           :done()`
`       :tag('div')`
`           :css('font-size', '114%')`
`           :css('margin', args.mini and '0 4em' or '0 7em')`
`           :cssText(args.fontstyle)`
`           :wikitext(args[1])`
`   end`

`   return tostring(div:done())`

end

function p.navbar(frame)

`   if not getArgs then`
`       getArgs = require('Module:Arguments').getArgs`
`   end`
`   return p._navbar(getArgs(frame))`

end

return p