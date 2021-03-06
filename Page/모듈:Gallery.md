> This article is converted from Wikipedia: [모듈:Gallery](https://ko.wikipedia.org/wiki/모듈:Gallery).


\-- This module implements

local p = {}

local templatestyles = 'Template:Gallery/styles.css' local yesno = require('Module:Yesno')

local function trim(s)

`   return mw.ustring.gsub(mw.ustring.gsub(s, '%s', ' '), '^%s*(.-)%s*$', '%1')`

end

local tracking, preview

local function checkarg(k,v)

`   if k and type(k) == 'string' then`
`       if k == 'align' or k == 'state' or k == 'style' or k == 'caption' or k == 'title' or`
`           k == 'width' or k == 'height' or k == 'lines' or k == 'whitebg' or k == 'class' or`
`           k == 'mode' or k == 'footer' or k == 'perrow' or k == 'noborder' or`
`           k:match('^alt%d+$') or k:match('^%d+$') then`
`           -- valid`
`       elseif k == 'captionstyle' then`
`           if not v:match('^text%-align%s*:%s*center[;%s]*$') then`
`               table.insert(tracking, '')`
`           end`
`       else`
`           -- invalid`
`           local vlen = mw.ustring.len(k)`
`           k = mw.ustring.sub(k, 1, (vlen < 25) and vlen or 25) `
`           k = mw.ustring.gsub(k, '[^%w\-_ ]', '?')`
`           table.insert(tracking, '')`
`           table.insert(preview, '"' .. k .. '"')`
`       end`
`   end`

end

function p.gallery(frame)

`   -- If called via #invoke, use the args passed into the invoking template.`
`   -- Otherwise, for testing purposes, assume args are being passed directly in.`
`   local origArgs = (type(frame.getParent) == 'function') and frame:getParent().args or frame`
`   `
`   -- ParserFunctions considers the empty string to be false, so to preserve the previous `
`   -- behavior of ``, change any empty arguments to nil, so Lua will consider`
`   -- them false too.`
`   local args = {}`
`   tracking, preview = {}, {}`
`   for k, v in pairs(origArgs) do`
`       if v ~= '' then`
`           args[k] = v`
`           checkarg(k,v)`
`       end`
`   end`
`   `
`   if (args.mode or '') == 'packed' and (args.align or '') == '' then`
`       args.align = 'center'`
`   end`

`   local tbl = mw.html.create('div')`
`   tbl:addClass('mod-gallery')`
`   `
`   if args.state then`
`       tbl`
`           :addClass('mod-gallery-collapsible')`
`           :addClass('collapsible')`
`           :addClass(args.state)`
`   end`
`   `
`   if args.style then`
`       tbl:cssText(args.style)`
`   else`
`       tbl:addClass('mod-gallery-default')`
`   end`
`   `
`   if args.align then`
`       tbl:addClass('mod-gallery-' .. args.align:lower())`
`   end`
`   `
`   if args.class then`
`       tbl:addClass(args.class)`
`   end`
`   `
`   if args.title or args.caption then`
`       tbl:tag('div')`
`           :addClass('title')`
`               :tag('div')`
`                   :wikitext('`

<dl>

<dd>

' .. (args.title or args.caption) .. '

</dd>

</dl>

')

`   end`
`   `
`   local gargs = {}`
`   gargs['class'] = 'nochecker' .. (args.noborder and '' or ' bordered-images')`
`   gargs['widths'] = tonumber(args.width) or 180`
`   gargs['heights'] = tonumber(args.height) or 180`
`   gargs['style'] = args.captionstyle`
`   gargs['perrow'] = args.perrow`
`   gargs['mode'] = args.mode`
`   gargs['showfilename'] = args.showfilename`
`   if yesno(args.whitebg or 'yes') then`
`       gargs['class'] = gargs['class'] .. ' whitebg'`
`   end`
`   `
`   local gallery = {}`
`   `
`   local imageCount = math.ceil(#args / 2)`

`   for i = 1, imageCount do`
`       local img = trim(args[i*2 - 1] or '')`
`       local caption = trim(args[i*2] or '')`
`       local alt = trim(args['alt' .. i] or '')`
`       if img ~= '' then`
`           table.insert(gallery, img .. (alt ~= '' and ('|alt=' .. alt) or '') .. '|' .. caption )`
`       end`
`   end`
`   `
`   tbl:tag('div')`
`       :addClass('main')`
`       :tag('div')`
`           :wikitext(`
`               frame:extensionTag{ name = 'gallery', content = '\n' .. table.concat(gallery,'\n'), args = gargs}`
`               )`
`   `
`   if args.footer then`
`       tbl:tag('div')`
`           :addClass('footer')`
`               :tag('div')`
`                   :wikitext('`

<dl>

<dd>

' .. args.footer .. '

</dd>

</dl>

')

`   end`

`   local trackstr = (#tracking > 0) and table.concat(tracking, '') or ''`
`   if #preview > 0 and frame:preprocess( "``" ) == "" then`
`       trackstr = tostring(mw.html.create('div')`
`           :addClass('hatnote')`
`           :css('color','red')`
`           :tag('strong'):wikitext('Warning:'):done()`
`           :wikitext('알 수 없는 변수: ' .. table.concat(preview, '; ')))`
`   end`
`   `
`   return frame:extensionTag{ name = 'templatestyles', args = { src = templatestyles} } .. tostring(tbl) .. trackstr`

end

return p

[Category:Pages_using_gallery_with_the_captionstyle_parameter](https://ko.wikipedia.org/wiki/Category:Pages_using_gallery_with_the_captionstyle_parameter "wikilink") [Category:Pages_using_gallery_with_unknown_parameters](https://ko.wikipedia.org/wiki/Category:Pages_using_gallery_with_unknown_parameters "wikilink")