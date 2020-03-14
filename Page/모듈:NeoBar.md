> This article is converted from Wikipedia: [:NeoBar](https://ko.wikipedia.org/wiki/:NeoBar).


\-- 틀을 개선하는  틀을 만들기 위한 모듈입니다 --사용가능한 함수는 bar입니다. local function drawBar (color, length, round) --막대를 그리는 함수 (막대의 색, 길이, 올림/내림/반올림)

`   local t = require("모듈:Coutput")`
`   `
`   if length > 5000 then return ''     end --길이가 5000보다 큰 경우에는 아무것도 그리지 않습니다.`
`   if length <= 0 then return ''       end --길이가 0보다 작은 경우에도 아무것도 그리지 않습니다.`
`   `
`   local rest_length = --그리고 남은 길이, 즉, 그려야 할 나머지 길이,`
`       round == 'up' and  math.ceil(length) or -- 올림의 경우`
`       round == 'down' and math.floor(length) or --버림의 경우`
`       math.floor(length+.5) --  기본적으로는 반올림`
`       `
`   while rest_length >= 100 do t:print('`[`링크=`](https://ko.wikipedia.org/wiki/파일:'\):print\(color\):print\('100.png "wikilink")`')rest_length = rest_length - 100 end`
`   while rest_length >= 50 do t:print('`[`링크=`](https://ko.wikipedia.org/wiki/파일:'\):print\(color\):print\('50.png "wikilink")`') rest_length = rest_length - 50 end`
`   while rest_length >= 30 do t:print('`[`링크=`](https://ko.wikipedia.org/wiki/파일:'\):print\(color\):print\('30.png "wikilink")`') rest_length = rest_length - 30 end`
`   while rest_length >= 10 do t:print('`[`링크=`](https://ko.wikipedia.org/wiki/파일:'\):print\(color\):print\('10.png "wikilink")`') rest_length = rest_length - 10 end`
`   while rest_length >= 5 do t:print('`[`링크=`](https://ko.wikipedia.org/wiki/파일:'\):print\(color\):print\('05.png "wikilink")`') rest_length = rest_length - 5 end`
`   while rest_length >= 3 do t:print('`[`링크=`](https://ko.wikipedia.org/wiki/파일:'\):print\(color\):print\('03.png "wikilink")`') rest_length = rest_length - 3 end `
`   while rest_length >= 1 do t:print('`[`링크=`](https://ko.wikipedia.org/wiki/파일:'\):print\(color\):print\('01.png "wikilink")`') rest_length = rest_length - 1 end     `
`   `
`   return t:printall()`

end

local function bar(frame)

`   local color = frame.args[1] or '무'`
`   local length = tonumber(frame:preprocess('{{#iferror: {{#expr:'..  frame.args[2] ..'}} | 0 }}')) or 0`
`   local round = frame.args.round or '' -- i. e. frame.args['round']`
`   return drawBar (color, length, round)`

end

return {bar=bar, drawBar=drawBar}