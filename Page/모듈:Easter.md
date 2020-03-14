> This article is converted from Wikipedia: [:Easter](https://ko.wikipedia.org/wiki/:Easter).


local m = {}

local EasterData = {

`   defaultMethod = 3,        -- default method of Easter date calculation when Easter type is not given`
`   defaultFormat = "Y-m-d",  -- default date output format`
`   noFormat      = "none",   -- prevent from final date formatting`
`   defaultOffset = 0,        -- the Easter date`
`   minimumOffset = -63,      -- Septuagesima`
`   maximumOffset = 68,       -- Feast of the Sacred Heart`

`   -- API`
`   apiEaster            = "계산", -- public function name`
`   argEasterYear        = 1,           -- index or name of the argument with year`
`   argEasterMethod      = "방법",    -- index or name of the argument with calculation method`
`   argEasterOffset      = "일",       -- index or name of the argument with offset in days relative to the calculated Easter Sunday`
`   argEasterFormat      = "형식",    -- index or name of the argument with date output format (#time style)`

`   -- errors`
`   errorMissingYear     = "Missing mandatory argument with year",`
`   errorInvalidYear     = "The argument with year value is incorrect: '%s'",`
`   errorInvalidOffset   = "Incorrect argument 'day': '%s'",`
`   errorInvalidMethod   = "Incorrect argument 'method': '%s'",`
`   errorYearOutOfRange  = "Easter dates are available between years 326 and 4099; year: %d",`
`   errorIncorrectMethod = "Western or Orthodox Easter exists since 1583; year: %d",`
`   errorUnknownMethod   = "Unknown method: %d",`

`   methods = {`
`       ["율리우스력"]   = 1,`
`       ["동양력"]       = 2,`
`       ["정교회력"]     = 2, -- alias for Eastern`
`       ["서양력"]       = 3,`
`       ["로마력"]       = 3, -- alias for Roman`
`   },`

`   relativeDates = {`
`       ["칠순주일"]      = -63,`
`       ["육순절"]        = -56,`
`       ["뚱뚱한 목요일"] = -52,`
`       ["오순주일"]      = -49,`
`       ["재의 수요일"]   = -46,`
`       ["성지주일"]      =  -7,`
`       ["성목요일"]      =  -3,`
`       ["성금요일"]      =  -2,`
`       ["성토요일"]      =  -1, `
`       ["부활절"]        =   0,`
`       ["부활절 다음날"] =   1,`
`       ["예수의 승천"]   =  39,`
`       ["오순절"]        =  49,`
`       ["성체축일"]      =  60,`
`   },`

}

local function formatEasterError(message, ...)

`   if select('#', ... ) > 0 then`
`       message = string.format(message, ...)`
`   end`
`   return "`<span class=\"error\">`" .. message .. "`</span>`"`

end

local function loadEasterYear(year)

`   if not year then`
`       return false, formatEasterError(EasterData.errorMissingYear)`
`   end`
`   local result = tonumber(year)`
`   if not result or math.floor(result) ~= result then`
`       return false, formatEasterError(EasterData.errorInvalidYear, year)`
`   end`

`   return true, result`

end

local function loadEasterMethod(method, year)

`   local result = EasterData.defaultMethod`
`   if method then`
`       result = EasterData.methods[method]`
`       if not result then`
`           return false, formatEasterError(EasterData.errorInvalidMethod, method)`
`       end`
`   end`

`   if year < 1583 then`
`       result = 1`
`   end`

`   return true, result`

end

local function loadEasterOffset(day)

`   if not day then`
`       return true, ""`
`   end`

`   local data = EasterData.relativeDates`
`   local offset = tonumber(day)`
`   if not offset then`
`       offset = data[day]`
`   end`
`   if not offset or offset ~= math.floor(offset) or offset < EasterData.minimumOffset or offset > EasterData.maximumOffset then`
`       return false, formatEasterError(EasterData.errorInvalidOffset, day)`
`   end`

`   if offset < -1 then`
`       return true, string.format(" %d days", offset)`
`   elseif offset == -1 then`
`       return true, " -1 day"`
`   elseif offset == 0 then`
`       return true, ""`
`   elseif offset == 1 then`
`       return true, " +1 day"`
`   else -- if offset > 1 then`
`       return true, string.format(" +%d days", offset)`
`   end`

end

local function loadEasterFormat(fmt)

`   if fmt == EasterData.noFormat then`
`       return true, nil`
`   elseif not fmt then`
`       return true, EasterData.defaultFormat`
`   else`
`       return true, fmt`
`   end`

end

\--[목적: This function returns Easter Sunday day and month for a specified year and method. 입력: 연도 - Any year between 326 and 4099. 방법 - 1 = the original calculation based on the Julian calendar 2 = the original calculation, with the Julian date converted to the equivalent Gregorian calendar 3 = the revised calculation based on the Gregorian calendar 출력: None. 돌려주는 값: 0, error message - Error; invalid arguments month, day - month and day of the Sunday NOTES: The code is translated from DN OSP 6.4.0 sources. The roots of the code might be found in http://www.gmarts.org/index.php?go=415 ORIGINAL NOTES: This algorithm is an arithmetic interpretation of the 3 step Easter Dating Method developed by Ron Mallen 1985, as a vast improvement on the method described in the Common Prayer Book Published Australian Almanac 1988 Refer to this publication, or the Canberra Library for a clear understanding of the method used Because this algorithm is a direct translation of the official tables, it can be easily proved to be 100% correct It's free\! Please do not modify code or comments\!](https://ko.wikipedia.org/wiki/목적:_This_function_returns_Easter_Sunday_day_and_month_for_a_specified_year_and_method._입력:_연도_-_Any_year_between_326_and_4099._방법_-_1_=_the_original_calculation_based_on_the_Julian_calendar_2_=_the_original_calculation,_with_the_Julian_date_converted_to_the_equivalent_Gregorian_calendar_3_=_the_revised_calculation_based_on_the_Gregorian_calendar_출력:_None._돌려주는_값:_0,_error_message_-_Error;_invalid_arguments_month,_day_-_month_and_day_of_the_Sunday_NOTES:_The_code_is_translated_from_DN_OSP_6.4.0_sources._The_roots_of_the_code_might_be_found_in_http://www.gmarts.org/index.php?go=415_ORIGINAL_NOTES:_This_algorithm_is_an_arithmetic_interpretation_of_the_3_step_Easter_Dating_Method_developed_by_Ron_Mallen_1985,_as_a_vast_improvement_on_the_method_described_in_the_Common_Prayer_Book_Published_Australian_Almanac_1988_Refer_to_this_publication,_or_the_Canberra_Library_for_a_clear_understanding_of_the_method_used_Because_this_algorithm_is_a_direct_translation_of_the_official_tables,_it_can_be_easily_proved_to_be_100%_correct_It's_free!_Please_do_not_modify_code_or_comments! "wikilink") local function calculateEasterDate(year, method)

`   if year < 326 or year > 4099 then`
`       -- Easter dates are valid for years between 326 and 4099`
`       return 0, formatEasterError(EasterData.errorYearOutOfRange, year)`
`   end`
`   if year < 1583 and method ~= 1 then`
`       -- Western or Orthodox Easter is valid since 1583`
`       return 0, formatEasterError(EasterData.errorIncorrectMethod, year)`
`   end`

`   -- intermediate result`
`   local firstDig = math.floor(year / 100)`
`   local remain19 = year % 19`
`   local temp = 0`
`   -- table A to E results`
`   local tA = 0`
`   local tB = 0`
`   local tC = 0`
`   local tD = 0`
`   local tE = 0`
`    -- Easter Sunday day`
`   local d = 0`

`   if method == 1 or method == 2 then`
`       -- calculate PFM date`
`       tA   = ((225 - 11 * remain19) % 30) + 21`
`       -- find the next Sunday`
`       tB   = (tA - 19) % 7`
`       tC   = (40 - firstDig) % 7`
`       temp = year % 100`
`       tD   = (temp + math.floor(temp / 4)) % 7`
`       tE   = ((20 - tB - tC - tD) % 7) + 1`
`       d    = tA + tE`
`       if method == 2 then`
`           -- convert Julian to Gregorian date`
`           -- 10 days were skipped in the Gregorian calendar from 5-14 Oct 1582`
`           temp = 10`
`           -- only 1 in every 4 century years are leap years in the Gregorian`
`           -- calendar (every century is a leap year in the Julian calendar)`
`           if year > 1600 then`
`               temp = temp + firstDig - 16 - math.floor((firstDig - 16) / 4)`
`           end`
`           d = d + temp`
`       end`
`   elseif method == 3 then`
`       -- calculate PFM date`
`       temp = math.floor((firstDig - 15) / 2)  + 202 - 11 * remain19`
`       if firstDig > 26 then`
`           temp = temp - 1`
`       end`
`       if firstDig > 38 then`
`           temp = temp - 1`
`       end`
`       if firstDig == 21 or firstDig == 24 or firstDig == 25 or firstDig == 33 or firstDig == 36 or firstDig == 37 then`
`           temp = temp - 1`
`       end`
`       temp = temp % 30`
`       tA   = temp + 21`
`       if temp == 29 then`
`           tA = tA - 1`
`       end`
`       if temp == 28 and remain19 > 10 then`
`           tA = tA - 1`
`       end`
`       -- find the next Sunday`
`       tB   = (tA - 19) % 7`
`       tC   = (40 - firstDig) % 4`
`       if tC == 3 then`
`           tC = tC + 1`
`       end`
`       if tC > 1 then`
`           tC = tC + 1`
`       end`
`       temp = year % 100`
`       tD   = (temp + math.floor(temp / 4)) % 7`
`       tE   = ((20 - tB - tC - tD) % 7) + 1`
`       d    = tA + tE`
`   else`
`       -- Unknown method`
`       return 0, formatEeasteError(EasterData.errorUnknownMethod, method)`
`   end`
`   if d > 61 then`
`       -- when the oryginal calculation os converted to the Gregorian`
`       -- calendar, Easter Sunday can occur in May`
`       return 5, d - 61`
`   elseif d > 31 then`
`       return 4, d - 31`
`   else`
`       return 3, d`
`   end`

end

local function Easter(args)

`   local ok`
`   local year`
`   ok, year = loadEasterYear(args[EasterData.argEasterYear])`
`   if not ok then`
`       return year`
`   end`

`   local method`
`   ok, method = loadEasterMethod(args[EasterData.argEasterMethod], year)`
`   if not ok then`
`       return method`
`   end`

`   local offset`
`   ok, offset = loadEasterOffset(args[EasterData.argEasterOffset])`
`   if not ok then`
`       return offset`
`   end`

`   local format`
`   ok, format = loadEasterFormat(args[EasterData.argEasterFormat])`
`   if not ok then`
`       return format`
`   end`

`   local month, day = calculateEasterDate(year, method)`
`   if month == 0 then`
`       return day`
`   end`

`   local result = string.format("%04d-%02d-%02d%s", year, month, day, offset)`
`   if format then`
`       result = mw.language.getContentLanguage():formatDate(format, result)`
`   end`

`   return result`

end

m\[EasterData.apiEaster\] = function (frame)

`   return Easter(frame.args)`

end

return m