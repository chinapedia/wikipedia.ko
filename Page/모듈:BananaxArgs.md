> This article is converted from Wikipedia: [모듈:BananaxArgs](https://ko.wikipedia.org/wiki/모듈:BananaxArgs).


\-- Sample Module demonstrating how to access arguments. -- For more about the Frame object, see <http://www.mediawiki.org/wiki/Extension:Scribunto/Lua_reference_manual#Frame_object> -- Unit tests at Module:BananasArgs/tests

local p = require("모듈:Coutput")

\-- No arguments, used like: {{\#invoke:BananaxArgs|hello_world}} function p.hello_world()

`   p:print("Hello, world!")`
`   return p:printall()`

end

\-- One argument, used like: {{\#invoke:BananaxArgs|hello|Fred}} function p.hello(frame)

`   local name = frame.args[1]`
`   p:printf("Hello, %s!", name)`
`   return p:printall()`

end

\-- Two arguments, used like: {{\#invoke:BananaxArgs|add|5|3}} function p.add(frame)

`   local num1 = tonumber(frame.args[1])`
`   local num2 = tonumber(frame.args[2])`
`   return num1 + num2`

end

\-- Named arguments, used like: {{\#invoke:BananaxArgs|count_fruit|bananas=5|apples=3}} function p.count_fruit(frame)

`   local num_bananas = tonumber(frame.args['bananas'])`
`   local num_apples = tonumber(frame.args['apples'])`
`   p:printf('I have %d bananas and %d apples', num_bananas, num_apples)`
`   return p:printall()`

end

\-- Mixing regular args with named args and optional named args -- Used like: {{\#invoke:BananaxArgs|has_fruit|Fred|bananas=5|cherries=7}} function p.has_fruit(frame)

`   local name = frame.args[1]`
`   local num_bananas = tonumber(frame.args['bananas'])`
`   local num_apples = tonumber(frame.args['apples'])`
`   local num_cherries = tonumber(frame.args['cherries'])`

`   p:print(name):print(' has:')`
`   if num_bananas then p:printf(' %d bananas', num_bananas) end`
`   if num_apples then p:printf(' %d apples', num_apples) end`
`   if num_cherries then p:printf(' %d num_cherries', num_cherries) end`
`   return p:printall()`

end

\-- Iterating over args, used like: {{\#invoke:BananaxArgs|custom_fruit|pineapples=10|kiwis=5}} function p.custom_fruit(frame)

`   p:print('I have')`
`   for name, value in pairs(frame.args) do`
`       p:printf(' %d %s', tonumber(value), name)`
`   end`
`   return p:printall()`

end

\-- Iterating over args with separate mandatory args -- Used like: {{\#invoke:BananaxArgs|custom_fruit_2|Fred|pineapples=10|kiwis=5}} function p.custom_fruit_2(frame)

`   local name = frame.args[1]`
`   p:printf('%s has', name)`
`   for name, value in pairs(frame.args) do`
`       if name ~= 1 then`
`       p:printf(' %d %s', tonumber(value), name)`
`       end`
`   end`
`   return p:printall()`

end

return p