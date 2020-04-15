> This article is converted from Wikipedia: [모듈:Dts](https://ko.wikipedia.org/wiki/모듈:Dts).


local yesno = require('Module:Yesno') local lang = mw.language.getContentLanguage() local N_YEAR_DIGITS = 12 local MAX_YEAR = 10^N_YEAR_DIGITS - 1

-----

\-- Dts class

-----

local Dts = {} Dts.__index = Dts

Dts.months = {

`   "1월",`
`   "2월",`
`   "3월",`
`   "4월",`
`   "5월",`
`   "6월",`
`   "7월",`
`   "8월",`
`   "9월",`
`   "10월",`
`   "11월",`
`   "12월"`

}

Dts.monthsAbbr = {

`   "1월",`
`   "2월",`
`   "3월",`
`   "4월",`
`   "5월",`
`   "6월",`
`   "7월",`
`   "8월",`
`   "9월",`
`   "10월",`
`   "11월",`
`   "12월"`

}

function Dts._makeMonthSearch(t)

`   local ret = {}`
`   for i, month in ipairs(t) do`
`       ret[month:lower()] = i`
`   end`
`   return ret`

end Dts.monthSearch = Dts._makeMonthSearch(Dts.months) Dts.monthSearchAbbr = Dts._makeMonthSearch(Dts.monthsAbbr) Dts.monthSearchAbbr\['sept'\] = 9 -- Allow "Sept" to match September

Dts.formats = {

`   ymd = true,`
`   dmy = true,`
`   mdy = true,`
`   ym = true,`
`   dm = true,`
`   md = true,`
`   my = true,`
`   y = true,`
`   m = true,`
`   d = true,`
`   hide = true`

}

function Dts.new(args)

`   local self = setmetatable({}, Dts)`

`   -- Parse date parameters.`
`   -- In this step we also record whether the date was in DMY or YMD format,`
`   -- and whether the month name was abbreviated.`
`   if args[2] or args[3] or args[4] then`
`       self:parseDateParts(args[1], args[2], args[3], args[4])`
`   elseif args[1] then`
`       self:parseDate(args[1])`
`   end`

`   -- Raise an error on invalid values`
`   if self.year then`
`       if self.year == 0 then`
`           error('연도는 0이 될 수 없습니다', 0)`
`       elseif self.year < -MAX_YEAR then`
`           error(string.format(`
`               '연도는 %s보다 적을 수 없습니다',`
`               lang:formatNum(-MAX_YEAR)`
`           ), 0)`
`       elseif self.year > MAX_YEAR then`
`           error(string.format(`
`               '연도는 %s보다 클 수 없습니다',`
`               lang:formatNum(MAX_YEAR)`
`           ), 0)`
`       elseif math.floor(self.year) ~= self.year then`
`           error('연도는 정수이어야 합니다', 0)`
`       end`
`   end`
`   if self.month and (`
`       self.month < 1`
`       or self.month > 12`
`       or math.floor(self.month) ~= self.month`
`   ) then`
`       error('월은 1과 12 사이의 정수이어야 합니다', 0)`
`   end`
`   if self.day and (`
`       self.day < 1`
`       or self.day > 31`
`       or math.floor(self.day) ~= self.day`
`   ) then`
`       error('일은 1과 31 사이의 정수이어야 합니다', 0)`
`   end`

`   -- Set debug mode`
`   if args.debug then`
`       self.isdebug = args.debug`
`   end`

`   -- Set the format string`
`   if args.format then`
`       self.format = args.format`
`   else`
`       self.format = self.format or 'ymd'`
`   end`
`   if not Dts.formats[self.format] then`
`       error(string.format(`
`           "'%s'는 유효한 형식이 아닙니다",`
`           tostring(self.format)`
`       ), 0)`
`   end`

`   -- Set addkey. This adds a value at the end of the sort key, allowing users`
`   -- to manually distinguish between identical dates.`
`   if args.addkey then`
`       self.addkey = tonumber(args.addkey)`
`       if not self.addkey or`
`           self.addkey < 0 or`
`           self.addkey > 9999 or`
`           math.floor(self.addkey) ~= self.addkey`
`       then`
`           error("'addkey' 변수는 0부터 9999 사이의 정수여야 합니다", 0)`
`       end`
`   end`

`   -- Set whether the displayed date is allowed to wrap or not.`
`   self.isWrapping = args.nowrap == 'off' or yesno(args.nowrap) == false`

`   -- Set whether the abbreviated is set or not.`
`   self.isAbbreviated = args.abbr == 'on' or yesno(args.abbr) == true`

`   -- Check for deprecated parameters.`
`   if args.link then`
`       self.hasDeprecatedParameters = true`
`   end`

`   return self`

end

function Dts:hasDate()

`   return (self.year or self.month or self.day) ~= nil`

end

\-- Find the month number for a month name, and set the isAbbreviated flag as -- appropriate. function Dts:parseMonthName(s)

`   s = s:lower()`
`   local month = Dts.monthSearch[s]`
`   if month then`
`       return month`
`   else`
`       month = Dts.monthSearchAbbr[s]`
`       if month then`
`           self.isAbbreviated = true`
`           return month`
`       end`
`   end`
`   return nil`

end

\-- Parses separate parameters for year, month, day, and era. function Dts:parseDateParts(year, month, day, bc)

`   if year then`
`       self.year = tonumber(year)`
`       if not self.year then`
`           error(string.format(`
`               "'%s'는 유효한 연도가 아닙니다",`
`               tostring(year)`
`           ), 0)`
`       end`
`   end`
`   if month then`
`       if tonumber(month) then`
`           self.month = tonumber(month)`
`       elseif type(month) == 'string' then`
`           self.month = self:parseMonthName(month)`
`       end`
`       if not self.month then`
`           error(string.format(`
`               "'%s'는 유효한 월이 아닙니다",`
`               tostring(month)`
`           ), 0)`
`       end`
`   end`
`   if day then`
`       self.day = tonumber(day)`
`       if not self.day then`
`           error(string.format(`
`               "'%s'는 유효한 일이 아닙니다",`
`               tostring(day)`
`           ), 0)`
`       end`
`   end`
`   if bc then`
`       local bcLower = type(bc) == 'string' and bc:lower()`
`       if bcLower == 'bc' or bcLower == 'bce' then`
`           if self.year and self.year > 0 then`
`               self.year = -self.year`
`           end`
`       elseif bcLower ~= 'ad' and bcLower ~= 'ce' then`
`           error(string.format(`
`               "'%s'는 유효한 연호가 아닙니다 (예측된 값: 'BC', 'BCE', 'AD', 'CE')",`
`               tostring(bc)`
`           ), 0)`
`       end`
`   end`

end

\-- This method parses date strings. This is a poor man's alternative to -- mw.language:formatDate, but it ends up being easier for us to parse the date -- here than to use mw.language:formatDate and then try to figure out after the -- fact whether the month was abbreviated and whether we were DMY or MDY. function Dts:parseDate(date)

`   -- Generic error message.`
`   local function dateError()`
`       error(string.format(`
`           "'%s'는 유효하지 않은 날짜입니다",`
`           date`
`       ), 0)`
`   end`

`   local function parseDayOrMonth(s)`
`       if s:find('^%d%d?$') then`
`           return tonumber(s)`
`       end`
`   end`

`   local function parseMonth(s)`
`       if s:find('^%d%d?$') and tonumber(s) >=1 and tonumber(s) <= 12 then`
`           return tonumber(s)`
`       end`
`   end`

`   local function parseDay(s)`
`       if self.month then`
`           lastday = {31, 29, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31}`
`           if s:find('^%d%d?$') and tonumber(s) >=1 and tonumber(s) <= lastday[self.month] then`
`               return tonumber(s)`
`           end`
`       end`
`   end`

`   local function parseYear(s)`
`       if s:find('^%d%d?%d?%d?$') then`
`           return tonumber(s)`
`       end`
`   end`

`   -- Deal with year-only dates first, as they can have hyphens in, and later`
`   -- we need to split the string by all non-word characters, including`
`   -- hyphens. Also, we don't need to restrict years to 3 or 4 digits, as on`
`   -- their own they can't be confused as a day or a month number.`
`   self.year = tonumber(date)`
`   if self.year then`
`       return`
`   end`

`   -- Split the string using non-word characters as boundaries.`
`   date = tostring(date)`
`   local parts = mw.text.split(date, '%W+')`
`   local nParts = #parts`
`   if parts[1] == '' or parts[nParts] == '' or nParts > 3 then`
`       -- We are parsing a maximum of three elements, so raise an error if we`
`       -- have more. If the first or last elements were blank, then the start`
`       -- or end of the string was a non-word character, which we will also`
`       -- treat as an error.`
`       dateError()`
`   elseif nParts < 1 then`
`       -- If we have less than one element, then something has gone horribly`
`       -- wrong.`
`       error(string.format(`
`           "날짜 '%s'를 분석하던 중 알 수 없는 오류가 발생했습니다",`
`           date`
`       ), 0)`
`   end`

`   if nParts == 1 then`
`       -- This can be either a month name or a year.`
`       self.month = self:parseMonthName(parts[1])`
`       if not self.month then`
`           self.year = parseYear(parts[1])`
`           if not self.year then`
`               dateError()`
`           end`
`       end`
`   elseif nParts == 2 then`
`       -- This can be any of the following formats:`
`       -- DD Month`
`       -- Month DD`
`       -- Month YYYY`
`       -- YYYY-MM`
`       -- MM-DD`
`       self.month = self:parseMonthName(parts[1])`
`       if self.month then`
`           -- This is either Month DD or Month YYYY.`
`           self.year = parseYear(parts[2])`
`           if not self.year then`
`               -- This is Month DD.`
`               self.format = 'mdy'`
`               self.day = parseDayOrMonth(parts[2])`
`               if not self.day then`
`                   dateError()`
`               end`
`           end`
`       else`
`           self.month = self:parseMonthName(parts[2])`
`           if self.month then`
`               -- This is DD Month.`
`               self.format = 'ymd'`
`               self.day = parseDayOrMonth(parts[1])`
`               if not self.day then`
`                   dateError()`
`               end`
`           else`
`               -- This is MM-DD.`
`               self.month = parseMonth(parts[1])`
`               if self.month then`
`                   self.day = parseDay(parts[2])`
`               else`
`                   -- This is YYYY-MM.`
`                   self.year = parseYear(parts[1])`
`                   self.month = parseMonth(parts[2])`
`                   if not (self.year and self.month) then`
`                       dateError()`
`                   end`
`               end`
`           end`
`       end`
`   elseif nParts == 3 then`
`       -- This can be any of the following formats:`
`       -- DD Month YYYY`
`       -- Month DD, YYYY`
`       -- YYYY-MM-DD`
`       -- DD-MM-YYYY`
`       self.month = self:parseMonthName(parts[1])`
`       if self.month then`
`           -- This is Month DD, YYYY.`
`           self.format = 'mdy'`
`           self.day = parseDayOrMonth(parts[2])`
`           self.year = parseYear(parts[3])`
`           if not self.day or not self.year then`
`               dateError()`
`           end`
`       else`
`           self.day = parseDayOrMonth(parts[1])`
`           if self.day then`
`               self.month = self:parseMonthName(parts[2])`
`               if self.month then`
`                   -- This is DD Month YYYY.`
`                   self.format = 'ymd'`
`                   self.year = parseYear(parts[3])`
`                   if not self.year then`
`                       dateError()`
`                   end`
`               else`
`                   -- This is DD-MM-YYYY.`
`                   self.format = 'ymd'`
`                   self.month = parseDayOrMonth(parts[2])`
`                   self.year = parseYear(parts[3])`
`                   if not self.month or not self.year then`
`                       dateError()`
`                   end`
`               end`
`           else`
`               -- This is YYYY-MM-DD`
`               self.year = parseYear(parts[1])`
`               self.month = parseDayOrMonth(parts[2])`
`               self.day = parseDayOrMonth(parts[3])`
`               if not self.year or not self.month or not self.day then`
`                   dateError()`
`               end`
`           end`
`       end`
`   end`

end

function Dts:makeSortKey()

`   local year, month, day`
`   local nYearDigits = N_YEAR_DIGITS`
`   if self:hasDate() then`
`       year = self.year or os.date("*t").year`
`       if year < 0 then`
`           year = -MAX_YEAR - 1 - year`
`           nYearDigits = nYearDigits + 1 -- For the minus sign`
`       end`
`       month = self.month or 1`
`       day = self.day or 1`
`   else`
`       -- Blank `` transclusions should sort last.`
`       year = MAX_YEAR`
`       month = 99`
`       day = 99`
`   end`
`   return string.format(`
`       '%0' .. nYearDigits .. 'd-%02d-%02d-%04d',`
`       year, month, day, self.addkey or 0`
`   )`

end

function Dts:getMonthName()

`   if not self.month then`
`       return ''`
`   end`
`   if self.isAbbreviated then`
`       return self.monthsAbbr[self.month]`
`   else`
`       return self.months[self.month]`
`   end`

end

function Dts:makeDisplay()

`   if self.format == 'hide' then`
`       return ''`
`   end`
`   local hasYear = self.year and self.format:find('y')`
`   local hasMonth = self.month and self.format:find('m')`
`   local hasDay = self.day and self.format:find('d')`
`   local ret = {}`
`   if hasYear then`
`       if self.year < 0 then`
`           ret[#ret + 1] = '기원전'`
`       end`
`       local displayYear = math.abs(self.year)`
`       displayYear = displayYear > 9999 and lang:formatNum(displayYear) or tostring(displayYear)`
`       ret[#ret + 1] = displayYear`
`       ret[#ret + 1] = '년 '`
`   end`
`   if hasMonth then`
`       ret[#ret + 1] = self.month`
`       ret[#ret + 1] = '월 '`
`   end`
`   if hasDay then`
`       ret[#ret + 1] = self.day`
`       ret[#ret + 1] = '일'`
`   end`
`   return table.concat(ret)`

end

function Dts:makeDisplayAbbr()

`   if self.format == 'hide' then`
`       return ''`
`   end`
`   local hasYear = self.year and self.format:find('y')`
`   local hasMonth = self.month and self.format:find('m')`
`   local hasDay = self.day and self.format:find('d')`
`   local ret = {}`
`   if hasYear then`
`       if self.year < 0 then`
`           ret[#ret + 1] = 'BC'`
`       end`
`       local displayYear = math.abs(self.year)`
`       displayYear = displayYear > 9999 and lang:formatNum(displayYear) or tostring(displayYear)`
`       ret[#ret + 1] = displayYear`
`       if hasMonth or hasDay then`
`           ret[#ret + 1] = '/'`
`       end`
`   end`
`   if hasMonth then`
`       ret[#ret + 1] = self.month`
`       if hasDay then`
`           ret[#ret + 1] = '/'`
`       end`
`   end`
`   if hasDay then`
`       ret[#ret + 1] = self.day`
`   end`
`   return table.concat(ret)`

end

function Dts:makeDisplayAbbrOrNoAbbr()

`   if self.isAbbreviated then`
`       return self:makeDisplayAbbr()`
`   else`
`       return self:makeDisplay()`
`   end`

end

function Dts:renderTrackingCategories()

`   if self.hasDeprecatedParameters then`
`       return '`[`분류:Dts틀의``   ``사용하지``   ``않는``   ``변수를``   ``사용함`](https://ko.wikipedia.org/wiki/분류:Dts틀의_사용하지_않는_변수를_사용함 "wikilink")`'`
`   else`
`       return ''`
`   end`

end

function Dts:__tostring()

`   local root = mw.html.create()`

`   -- Sort key`
`   if self.isdebug then`
`       root:tag('span')`
`           :css('border', 'dotted 1px')`
`           :wikitext(self:makeSortKey())`
`   else`
`       root:tag('span')`
`           :addClass('sortkey')`
`           :css('display', 'none')`
`           :css('speak', 'none')`
`           :wikitext(self:makeSortKey())`
`   end`
`   `
`   -- Display`
`   if self:hasDate() then`
`       if self.isWrapping then`
`           root:wikitext(self:makeDisplayAbbrOrNoAbbr())`
`       else`
`           root:tag('span')`
`               :css('white-space', 'nowrap')`
`               :wikitext(self:makeDisplayAbbrOrNoAbbr())`
`       end`
`   end`

`   -- Tracking categories`
`   root:wikitext(self:renderTrackingCategories())`

`   return tostring(root)`

end

-----

\-- Exports

-----

local p = {}

function p._exportClasses()

`   return {`
`       Dts = Dts`
`   }`

end

function p._main(args)

`   local success, ret = pcall(function ()`
`       local dts = Dts.new(args)`
`       return tostring(dts)`
`   end)`
`   if success then`
`       return ret`
`   else`
`       ret = string.format(`
`           '`<strong class="error">[`틀:Dts`](https://ko.wikipedia.org/wiki/틀:Dts "wikilink")` 오류: %s`</strong>`',`
`           ret`
`       )`
`       if mw.title.getCurrentTitle().namespace == 0 then`
`           -- Only categorise in the main namespace`
`           ret = ret .. '`[`분류:Dts``   ``틀``   ``오류`](https://ko.wikipedia.org/wiki/분류:Dts_틀_오류 "wikilink")`'`
`       end`
`       return ret`
`   end`

end

function p.main(frame)

`   local args = require('Module:Arguments').getArgs(frame, {`
`       wrappers = 'Template:Dts',`
`   })`
`   return p._main(args)`

end

return p