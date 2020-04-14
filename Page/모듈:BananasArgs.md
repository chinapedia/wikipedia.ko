> This article is converted from Wikipedia: [모듈:BananasArgs](https://ko.wikipedia.org/wiki/모듈:BananasArgs).


\-- 매개변수에 어떻게 접근하는지 보여주는 예제 모듈 -- Frame 객체에 대해 더 자세히 알고 싶으시면, <http://www.mediawiki.org/wiki/Extension:Scribunto/Lua_reference_manual#Frame_object를> 참고하세요. -- 유닛 테스트는 [모듈:BananasArgs/시험장](https://ko.wikipedia.org/wiki/모듈:BananasArgs/시험장 "wikilink")에 있습니다.

local p = {}

\-- 매개변수 없음 -- 이런 식으로 씀: {{\#invoke:BananasArgs|hello_world}} function p.hello_world()

`   return "Hello, world!"`

end

\-- 한개의 매개변수 -- 이런 식으로 씀: {{\#invoke:BananasArgs|hello|민준}} function p.hello(frame)

`   local name = frame.args[1]`
`   return "안녕하세요, " .. name .. "님!"`

end

\-- 두개의 매개변수 -- 이런 식으로 씀: {{\#invoke:BananasArgs|add|5|3}} function p.add(frame)

`   local num1 = tonumber(frame.args[1])`
`   local num2 = tonumber(frame.args[2])`
`   return num1 + num2`

end

\-- 이름을 가진 매개변수 -- 이런 식으로 씀: {{\#invoke:BananasArgs|count_fruit|바나나=5|사과=3}} function p.count_fruit(frame)

`   local num_bananas = frame.args['바나나']`
`   local num_apples = frame.args['사과']`
`   return '저는 바나나 ' .. num_bananas .. '개와 사과 ' .. num_apples .. '개를 가지고 있습니다.'`

end

\-- 일반적인 매개변수와 이름을 가진 매개변수를 혼합해서 사용하기 -- 이런 식으로 씀: {{\#invoke:BananasArgs|has_fruit|민준|바나나=5|체리=7}} function p.has_fruit(frame)

`   local name = frame.args[1]`
`   local num_bananas = frame.args['바나나']`
`   local num_apples = frame.args['사과']`
`   local num_cherries = frame.args['체리']`

`   local result = name .. '님은'`
`   if num_bananas then result = result .. ' 바나나 ' .. num_bananas .. '개' end`
`   if num_apples then result = result .. ' 사과 ' .. num_apples .. '개' end`
`   if num_cherries then result = result .. ' 체리 ' .. num_cherries .. '개' end`
`   result = result .. '를 가지고 있습니다.'`
`   return result`

end

\-- 매개변수를 반복해서 읽기 -- 이런 식으로 씀: {{\#invoke:BananasArgs|custom_fruit|파인애플=10|키위=5}} function p.custom_fruit(frame)

`   local result = '저는'`
`   for name, value in pairs(frame.args) do`
`       result = result .. ' ' .. name .. ' ' .. value .. '개'`
`   end`
`   result = result .. '를 가지고 있습니다.'`
`   return result`

end

\-- 별도로 써야하는 매개변수와 함께 매개변수를 반복해서 읽기 -- 이런 식으로 씀: {{\#invoke:BananasArgs|custom_fruit_2|민준|파인애플=10|키위=5}} function p.custom_fruit_2(frame)

`   local name = frame.args[1]`
`   local result = name .. '님은'`
`   for name, value in pairs(frame.args) do`
`       -- name이 1이 아니라면(~=)`
`       if name ~= 1 then`
`           result = result .. ' ' .. name .. ' ' .. value .. '개'`
`       end`
`   end`
`   result = result .. '를 가지고 있습니다.'`
`   return result`

end

return p