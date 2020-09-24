> This article is converted from Wikipedia: [모듈:Side box](https://ko.wikipedia.org/wiki/모듈:Side_box).


\-- This module implements .

local yesno = require('Module:Yesno')

local p = {}

function p.main(frame)

`   local origArgs = frame:getParent().args`
`   local args = {}`
`   for k, v in pairs(origArgs) do`
`       v = v:match('%s*(.-)%s*$')`
`       if v ~= '' then`
`           args[k] = v`
`       end`
`   end`
`   return p._main(args)`

end

function p._main(args)

`   local data = p.makeData(args)`
`   return p.renderSidebox(data)`

end

function p.makeData(args)

`   local data = {}`

`   -- Main table classes`
`   data.classes = {}`
`   if yesno(args.metadata) ~= false then`
`       table.insert(data.classes, 'metadata')`
`   end`
`   if args.position and args.position:lower() == 'left' then`
`       table.insert(data.classes, 'mbox-small-left')`
`   elseif args['위치'] and args['위치']:lower() == 'left' then`
`       table.insert(data.classes, 'mbox-small-left')`
`   else`
`       table.insert(data.classes, 'mbox-small')`
`   end`
`   table.insert(data.classes, args.class)`
`   `
`   -- Image`
`   if args.image and args.image ~= 'none' then`
`       data.image = args.image`
`   elseif args['그림'] and args['그림'] ~= 'none' then`
`       data['그림'] = args['그림']`
`   end`

`   -- Copy over data that doesn't need adjusting`
`   local argsToCopy = {`
`       -- Styles`
`       'style',`
`       'textstyle',`
`       '양식',`
`       '내용양식',`

`       -- Above row`
`       'above',`
`       'abovestyle',`
`       '윗글',`
`       '윗글양식',`

`       -- Body row`
`       'text',`
`       'imageright',`
`       '내용',`
`       '오른쪽그림',`

`       -- Below row`
`       'below',`
`       '아랫글',`
`   }`
`   for i, key in ipairs(argsToCopy) do`
`       data[key] = args[key]`
`   end`

`   return data`

end

function p.renderSidebox(data)

`   -- Renders the sidebox HTML.`

`   -- Table root`
`   local root = mw.html.create('table')`
`   root:attr('role', 'presentation')`
`   for i, class in ipairs(data.classes or {}) do`
`       root:addClass(class)`
`   end`
`   root:css{border = '1px solid #aaa', ['background-color'] = '#f9f9f9', color = '#000'}`
`   if (data.style or data['양식']) then`
`       root:cssText(data.style or data['양식'])`
`   end`

`   -- The "above" row`
`   if (data.above or data['윗글']) then`
`       local aboveCell = root:newline():tag('tr'):tag('td')`
`       aboveCell`
`           :attr('colspan', (data.imageright or data['오른쪽그림']) and 3 or 2)`
`           :addClass('mbox-text')`
`       if (data.textstyle or data['내용양식']) then`
`           aboveCell:cssText(data.textstyle or data['내용양식'])`
`       end`
`       if (data.abovestyle or data['윗글양식']) then`
`           aboveCell:cssText(data.abovestyle or data['윗글양식'])`
`       end`
`       aboveCell`
`           :newline()`
`           :wikitext(data.above or data['윗글'])`
`   end`

`   -- The body row`
`   local bodyRow = root:newline():tag('tr'):newline()`
`   if (data.image or data['그림']) then`
`       bodyRow:tag('td')`
`           :addClass('mbox-image')`
`           :wikitext(data.image or data['그림'])`
`   else`
`       bodyRow:tag('td'):css('width', '1px')`
`   end`
`   local textCell = bodyRow:newline():tag('td')`
`   textCell:addClass('mbox-text plainlist')`
`   if (data.textstyle or data['내용양식']) then`
`       textCell:cssText(data.textstyle or data['내용양식'])`
`   end`
`   textCell:wikitext(data.text or data['내용'])`
`   if (data.imageright or data['오른쪽그림']) then`
`       bodyRow:newline():tag('td')`
`           :addClass('mbox-imageright')`
`           :wikitext(data.imageright or data['오른쪽그림'])`
`   end`

`   -- The below row`
`   if (data.below or data['아랫글']) then`
`       local belowCell = root:newline():tag('tr'):tag('td')`
`       belowCell`
`           :attr('colspan', (data.imageright or data['오른쪽그림']) and 3 or 2)`
`           :addClass('mbox-text')`
`       if (data.textstyle or data['내용양식']) then`
`           belowCell:cssText(data.textstyle or data['내용양식'])`
`       end`
`       belowCell:wikitext(data.below or data['아랫글'])`
`   end`

`   root:newline()`
`   return tostring(root)`

end

return p