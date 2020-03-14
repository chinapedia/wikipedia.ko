> This article is converted from Wikipedia: [:Countdown](https://ko.wikipedia.org/wiki/:Countdown).


\--\[=\[ Countdown functions 현재 시각에서 목표 시각까지 남은 시간을 표출합니다. 사용법: {{\#invoke:Countdown|countdown|목표 날짜(필수, ISO 형식 - YYYY-MM-DD)|목표 시각(필수, hh:mm 형식, 24시간제)|종료문자열=목표 시각 경과시 표출할 문자열(선택)}} 예시: {{\#invoke:Countdown|countdown|2013-12-25|14:00}} 유지 관리: [사용자:Kwj2772](https://ko.wikipedia.org/wiki/사용자:Kwj2772 "wikilink")

`]=]`

local p = {} local datem = require('Module:Date') local mathm = require('Module:Math')

function p._getCurrentTime ()

`   return os.time()`

end

function p._ISOdate ( s )

`   local split = mw.text.split(s, '%-')`
`   local year = tonumber(split[1])`
`   local month = tonumber(split[2])`
`   local day = tonumber(split[3])`
`   local out = {`
`       ['year'] = year,`
`       ['month'] = month,`
`       ['day'] = day`
`   }`
`   return out`

end

function p._validate( s )

`   local d = p._ISOdate(s)`
`   local days = { 31,28,31,30,31,30,31,31,30,31,30,31 }`
`   if datem._isLeapYear(d.year) == 1 then`
`       days[2] = 29`
`   end`
`   local errors = 0`
`   if d.year <= 0 then`
`       errors = errors + 1 -- the year zero which does not exist or BC`
`   end`
`   if d.month ~= nil then`
`       if d.month > 12 or d.month < 1 then`
`           errors = errors + 10 -- 12월을 넘길 수 없음`
`       end`
`   end`
`   if d.month ~= nil and d.day ~= nil and d.day > days[d.month] then`
`       errors = errors + 100`
`   end`
`   if s:match('[^%d%-]') ~= nil then -- 예상치 못한 문자열 검출(숫자나 - 외의 문자)`
`       errors = errors + 1000`
`   end`
`   local sp = mw.text.split(s, '%-')`
`   if #sp > 3 or #sp < 1 then`
`       errors = errors + 10000`
`   end`
`   return errors`

end

function p._getDestTime(dates,timel) -- format: YYYY-MM-DD, hh:mm

`   if p._validate(dates) ~= 0 then`
`       return 'Error'`
`   end`
`   local obj = p._ISOdate(dates)`
`   local hour, minute = timel:match("^(%d+):(%d+)$")`
`   hour = tonumber(hour)`
`   minute = tonumber(minute)`
`   if (hour > 23 or hour < 0) or (minute > 59 or minute < 0) then`
`       return 'Error'`
`   end`
`   obj.hour = hour`
`   obj.min = minute`
`   return os.time(obj)`

end

function p._timeDiff(t2, t1)

`   local utc_offset_plus = 9`
`   return t2-t1-3600*utc_offset_plus`

end

function p._processStr(d,h,m)

`   if d == 0 then`
`       p1 = ''`
`   else`
`       p1 = d..'일 '`
`   end`
`   if h == 0 then`
`       p2 = ''`
`   else`
`       p2 = tostring(h)..'시간 '`
`   end`
`   local out = p1..p2..tostring(m)..'분'`
`   return out`

end

function p.countdown (frame)

`   local date_input_dest = frame.args[1] or frame.args['date'] or frame.args['종료날짜']`
`   local time_input_dest = frame.args[2] or frame.args['time'] or frame.args['종료시각']`
`   local zerostr = frame.args['종료문자열'] or '시간 경과'`
`   if p._getDestTime(date_input_dest, time_input_dest) == 'Error' then return 'Error' end`
`   local timeDiff = p._timeDiff(p._getDestTime(date_input_dest, time_input_dest), os.time())`
`   if timeDiff <= 0 then`
`       return zerostr`
`   else`
`       local days_left = math.floor(timeDiff/86400)`
`       local mods_h = timeDiff-86400*days_left`
`       local hours_left = math.floor(mods_h/3600)`
`       local mods_m = mods_h - 3600*hours_left`
`       local minutes_left = mathm._round(mods_m/60, 0)`
`       if days_left == 0 and hours_left == 0 and minutes_left == 0 then`
`           return '1분 미만'`
`       else`
`           return p._processStr(days_left,hours_left,minutes_left)`
`       end`
`   end`

end

return p