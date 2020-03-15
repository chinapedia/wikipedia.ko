> This article is converted from Wikipedia: [:Reply to](https://ko.wikipedia.org/wiki/:Reply_to).


local p = {}

function p.replyto(frame)

`   local origArgs = frame:getParent().args`
`   local args = {}`
`   local maxArg = 1`
`   local usernames = 0`
`   for k, v in pairs(origArgs) do`
`       if type(k) == 'number' then`
`           if mw.ustring.match(v,'%S') then`
`               if k > maxArg then maxArg = k end`
`               usernames = usernames + 1`
`               local title = mw.title.new(v)`
`               if not title then return '`<strong class="error">[`틀:답장`](https://ko.wikipedia.org/wiki/틀:답장 "wikilink")` 오류: 사용이 금지된 글자가 변수에 포함되어 있습니다.`</strong>`' end`
`               args[k] = title.rootText`
`           end`
`       elseif v == '' and k:sub(0,5) == 'label' then`
`           args[k] = '​'`
`       else`
`           args[k] = v`
`       end`
`   end`

`   if usernames > (tonumber(frame.args.max) or 50) then`
`       return string.format(`
`           '`<strong class="error">[`틀:답장`](https://ko.wikipedia.org/wiki/틀:답장 "wikilink")` 오류: %s 이상의 변수가 지정되었습니다.`</strong>`',`
`           tostring(frame.args.max or 50)`
`       )`
`   else`
`       if usernames < 1 then`
`           if frame.args.example then args[1] = frame.args.example else return '`<strong class="error">[`틀:답장`](https://ko.wikipedia.org/wiki/틀:답장 "wikilink")` 오류: 사용자 이름이 지정되지 않았습니다.`</strong>`' end`
`       end`
`       local isfirst = true`
`       local outStr = ''`
`       for i = 1, maxArg do`
`           if args[i] then`
`               if isfirst then`
`                   outStr = string.format(`
`                       '`<span class="template-ping">`%s`[`%s`](https://ko.wikipedia.org/wiki/사:%s "wikilink")`',`
`                       args['prefix'] or '@',`
`                       args[i],`
`                       (args['label1'] or args['label']) or args[i]`
`                   )`
`                   isfirst = false`
`               else`
`                   if ( (usernames >= 2) ) then outStr = outStr..',' end`
`                   outStr = string.format(`
`                       '%s `[`%s`](https://ko.wikipedia.org/wiki/사:%s "wikilink")`',`
`                       outStr,`
`                       args[i],`
`                       args['label'..tostring(i)] or args[i]`
`                   )`
`               end`
`           end`
`       end`
`       outStr = outStr..(args['p'] or ':')..'`</span>`'`
`       return outStr`
`   end`

end

return p