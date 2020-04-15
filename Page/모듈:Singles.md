> This article is converted from Wikipedia: [모듈:Singles](https://ko.wikipedia.org/wiki/모듈:Singles).


local p = {}

\-- Ripped from Module:Infobox. TODO: Make a utility module that can do this kind of thing local function getArgNums(args, prefix)

`   -- Returns a table containing the numbers of the arguments that exist`
`   -- for the specified prefix. For example, if the prefix was 'data', and`
`   -- 'data1', 'data2', and 'data5' exist, it would return {1, 2, 5}.`
`   local nums = {}`
`   for k, v in pairs(args) do`
`       local num = tostring(k):match('^' .. prefix .. '([1-9]%d*)$')`
`       if num then table.insert(nums, tonumber(num)) end`
`   end`
`   table.sort(nums)`
`   return nums`

end

function p.main(frame)

`   local args = require('Module:Arguments').getArgs(frame, {wrappers = 'Template:Singles'})`
`   local out = [=[`

<tr>

<th style="text-align:center; background:]=] .. frame:expandTemplate{title = '음반 정보/색', args = {args.Type}} .. [=[;" colspan="3">

[Singles](https://ko.wikipedia.org/wiki/Single_\(music\) "wikilink") from *\]=\] .. (args.Name or mw.title.getCurrentTitle().prefixedText) .. \[=\[*

</th>

</tr>

<tr style="text-align:left; vertical-align:top;">

<td colspan="3">

\]=\]

`   local nums = getArgNums(args, '[Ss]ingle ')`
`   for _, num in ipairs(nums) do`
`       out = out .. '\n# `<span class="item"><span class="fn">`"' .. (args['Single ' .. num] or args['single ' .. num]) .. '"`</span>`'`
`       local date = args['Single ' .. num .. ' date'] or args['single ' .. num .. ' date']`
`       if date then`
`           out = out .. '`
`Released: ' .. date`
`       end`
`       out = out .. '`</span>`'`
`   end`
`   out = out .. [=[`

</td>

</tr>

\]=\]

`   return out`

end

return p