> This article is converted from Wikipedia: [:UnitTests](https://ko.wikipedia.org/wiki/:UnitTests).


\-- UnitTester는 다른 루아 스크립트에 사용할 수 있는 유닛 테스트 도구를 -- 제공합니다. 자세한 것은 [위키백과:루아\#유닛 테스트를](https://ko.wikipedia.org/wiki/위키백과:루아#유닛_테스트 "wikilink") 참조하세요. -- 사용자를 위한 설명서는 상단의 설명문서를 참고해주세요. local UnitTester = {}

local frame, tick, cross local result_table_header = "{|class=\\"wikitable\\"\\n\! \!\! 테스트 구문 \!\! 기댓값 \!\! 실젯값" local result_table = '' local num_failures = 0

function first_difference(s1, s2)

`   if s1 == s2 then return '' end`
`   local max = math.min(#s1, #s2)`
`   for i = 1, max do`
`       if s1:sub(i,i) ~= s2:sub(i,i) then return i end`
`   end`
`   return max + 1`

end

function UnitTester:preprocess_equals(text, expected, options)

`   local actual = frame:preprocess(text)`
`   if actual == expected then`
`       result_table = result_table .. '| ' .. tick`
`   else`
`       result_table = result_table .. '| ' .. cross`
`       num_failures = num_failures + 1`
`   end`
`   local maybe_nowiki = (options and options.nowiki) and mw.text.nowiki or function(...) return ... end`
`   local differs_at = self.differs_at and (' \n| ' .. first_difference(expected, actual)) or ''`
`   result_table = result_table .. ' \n| ' .. mw.text.nowiki(text) .. ' \n| ' .. maybe_nowiki(expected) .. ' \n| ' .. maybe_nowiki(actual) .. differs_at .. "\n|-\n"`

end

function UnitTester:preprocess_equals_many(prefix, suffix, cases, options)

`   for _, case in ipairs(cases) do`
`       self:preprocess_equals(prefix .. case[1] .. suffix, case[2], options)`
`   end`

end

function UnitTester:preprocess_equals_preprocess(text1, text2, options)

`   local actual = frame:preprocess(text1)`
`   local expected = frame:preprocess(text2)`
`   if actual == expected then`
`       result_table = result_table .. '| ' .. tick`
`   else`
`       result_table = result_table .. '| ' .. cross`
`       num_failures = num_failures + 1`
`   end`
`   local maybe_nowiki = (options and options.nowiki) and mw.text.nowiki or function(...) return ... end`
`   local differs_at = self.differs_at and (' \n| ' .. first_difference(expected, actual)) or ''`
`   result_table = result_table .. ' \n| ' .. mw.text.nowiki(text1) .. ' \n| ' .. maybe_nowiki(expected) .. ' \n| ' .. maybe_nowiki(actual) .. differs_at .. "\n|-\n"`

end

function UnitTester:preprocess_equals_preprocess_many(prefix1, suffix1, prefix2, suffix2, cases, options)

`   for _, case in ipairs(cases) do`
`       self:preprocess_equals_preprocess(prefix1 .. case[1] .. suffix1, prefix2 .. (case[2] and case[2] or case[1]) .. suffix2, options)`
`   end`

end

function UnitTester:equals(name, actual, expected, options)

`   if actual == expected then`
`       result_table = result_table .. '| ' .. tick`
`   else`
`       result_table = result_table .. '| ' .. cross`
`       num_failures = num_failures + 1`
`   end`
`   local maybe_nowiki = (options and options.nowiki) and mw.text.nowiki or function(...) return ... end`
`   local differs_at = self.differs_at and (' \n| ' .. first_difference(expected, actual)) or ''`
`   result_table = result_table .. ' \n| ' .. name .. ' \n| ' .. maybe_nowiki(tostring(expected)) .. ' \n| ' .. maybe_nowiki(tostring(actual)) .. differs_at .. "\n|-\n"`

end

local function deep_compare(t1, t2, ignore_mt)

`   local ty1 = type(t1)`
`   local ty2 = type(t2)`
`   if ty1 ~= ty2 then return false end`
`   if ty1 ~= 'table' and ty2 ~= 'table' then return t1 == t2 end`

`   local mt = getmetatable(t1)`
`   if not ignore_mt and mt and mt.__eq then return t1 == t2 end`

`   for k1, v1 in pairs(t1) do`
`       local v2 = t2[k1]`
`       if v2 == nil or not deep_compare(v1, v2) then return false end`
`   end`
`   for k2, v2 in pairs(t2) do`
`       local v1 = t1[k2]`
`       if v1 == nil or not deep_compare(v1, v2) then return false end`
`   end`

`   return true`

end

function val_to_str(v)

`   if type(v) == 'string' then`
`       v = mw.ustring.gsub(v, '\n', '\\n')`
`       if mw.ustring.match(mw.ustring.gsub(v, '[^\'"]', ''), '^"+$') then`
`           return "'" .. v .. "'"`
`       end`
`       return '"' .. mw.ustring.gsub(v, '"', '\\"' ) .. '"'`
`   else`
`       return type(v) == 'table' and table_to_str(v) or tostring(v)`
`   end`

end

function table_key_to_str(k)

`   if type(k) == 'string' and mw.ustring.match(k, '^[_%a][_%a%d]*$') then`
`       return k`
`   else`
`       return '[' .. val_to_str(k) .. ']'`
`   end`

end

function table_to_str(tbl)

`   local result, done = {}, {}`
`   for k, v in ipairs(tbl) do`
`       table.insert(result, val_to_str(v))`
`       done[k] = true`
`   end`
`   for k, v in pairs(tbl) do`
`       if not done[k] then`
`           table.insert(result, table_key_to_str(k) .. '=' .. val_to_str(v))`
`       end`
`   end`
`   return '{' .. table.concat(result, ',') .. '}'`

end

function UnitTester:equals_deep(name, actual, expected, options)

`   if deep_compare(actual, expected) then`
`       result_table = result_table .. '| ' .. tick`
`   else`
`       result_table = result_table .. '| ' .. cross`
`       num_failures = num_failures + 1`
`   end`
`   local maybe_nowiki = (options and options.nowiki) and mw.text.nowiki or function(...) return ... end`
`   local actual_str = val_to_str(actual)`
`   local expected_str = val_to_str(expected)`
`   local differs_at = self.differs_at and (' \n| ' .. first_difference(expected_str, actual_str)) or ''`
`   result_table = result_table .. ' \n| ' .. name .. ' \n| ' .. maybe_nowiki(expected_str) .. ' \n| ' .. maybe_nowiki(actual_str) .. differs_at .. "\n|-\n"`

end

function UnitTester:run(frame_arg)

`   frame = frame_arg`
`   self.frame = frame`
`   self.differs_at = frame.args['differs_at']`
`   tick = frame:preprocess('``')`
`   cross = frame:preprocess('``')`

`   local table_header = result_table_header`
`   if self.differs_at then`
`       table_header = table_header .. ' !! 값이 다르기 시작한 위치'`
`   end`

`   -- ABC, 가나다순으로 결과 정렬`
`   local self_sorted = {}`
`   for key,value in pairs(self) do`
`       if key:find('^test') then`
`           table.insert(self_sorted, key)`
`       end`
`   end`
`   table.sort(self_sorted)`
`   -- 결과 표에 결과들을 추가`
`   for i,value in ipairs(self_sorted) do`
`       result_table = result_table .. "`**`"``   ``..``   ``value``   ``..``   ``"`**`:\n" .. table_header .. "\n|-\n"`
`       self[value](self)`
`       result_table = result_table .. "|}\n\n"`
`   end`

`   return (num_failures == 0 and "`<span style=\"color:green\;font-weight:bold;\">`모든 테스트를 통과했습니다.`</span>`" or "`<span style=\"color:maroon;font-weight:bold;\">`" .. num_failures .. "개의 테스트를 통과하지 못했습니다.`</span>`") .. "\n\n" .. frame:preprocess(result_table)`

end

function UnitTester:new()

`   local o = {}`
`   setmetatable(o, self)`
`   self.__index = self`
`   return o`

end

local p = UnitTester:new() function p.run_tests(frame) return p:run(frame) end return p