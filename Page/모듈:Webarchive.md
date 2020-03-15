> This article is converted from Wikipedia: [:Webarchive](https://ko.wikipedia.org/wiki/:Webarchive).


\--[---------------------------------- Lua module implementing the {{webarchive}} template. A merger of the functionality of three templates: {{wayback}}, {{webcite}} and {{cite archives}}](https://ko.wikipedia.org/wiki/----------------------------------_Lua_module_implementing_the_{{webarchive}}_template._A_merger_of_the_functionality_of_three_templates:_{{wayback}},_{{webcite}}_and_{{cite_archives}} "wikilink")

local p = {}

\--[--------------------------\< inlineError \>----------------------- Critical error. Render output completely in red. Add to tracking category.](https://ko.wikipedia.org/wiki/--------------------------\<_inlineError_\>-----------------------_Critical_error._Render_output_completely_in_red._Add_to_tracking_category. "wikilink")

local function inlineError(arg, msg)

` track["분류:웹아카이브 틀 오류"] = 1`
` return '`<span style="font-size:100%" class="error citation-comment">`웹아카이브 틀에 오류가 있습니다: |' .. arg .. '= 값을 확인하십시오. ' .. msg .. '`</span>`'`

end

\--[--------------------------\< inlineRed \>----------------------- Render a text fragment in red, such as a warning as part of the final output. Add tracking category.](https://ko.wikipedia.org/wiki/--------------------------\<_inlineRed_\>-----------------------_Render_a_text_fragment_in_red,_such_as_a_warning_as_part_of_the_final_output._Add_tracking_category. "wikilink")

local function inlineRed(msg, trackmsg)

` if trackmsg == "warning" then`
`   track["분류:웹아카이브 틀 경고"] = 1 `
` elseif trackmsg == "error" then`
`   track["분류:웹아카이브 틀 오류"] = 1 `
` end`

` return '`<span style="font-size:100%" class="error citation-comment">`' .. msg .. '`</span>`'`

end

\--[--------------------------\< trimArg \>----------------------- trimArg returns nil if arg is "" while trimArg2 returns 'true' if arg is "" trimArg2 is for args that might accept an empty value, as an on/off switch like nolink=](https://ko.wikipedia.org/wiki/--------------------------\<_trimArg_\>-----------------------_trimArg_returns_nil_if_arg_is_""_while_trimArg2_returns_'true'_if_arg_is_""_trimArg2_is_for_args_that_might_accept_an_empty_value,_as_an_on/off_switch_like_nolink= "wikilink")

local function trimArg(arg)

` if arg == "" or arg == nil then`
`   return nil`
` else`
`   return mw.text.trim(arg)`
` end`

end local function trimArg2(arg)

` if arg == nil then`
`   return nil`
` else`
`   return mw.text.trim(arg)`
` end`

end

\--[--------------------------\< base62 \>----------------------- Convert base-62 to base-10 Credit: https://de.wikipedia.org/wiki/Modul:Expr](https://ko.wikipedia.org/wiki/--------------------------\<_base62_\>-----------------------_Convert_base-62_to_base-10_Credit:_https://de.wikipedia.org/wiki/Modul:Expr "wikilink")

local function base62( value )

`   local r = 1`

`   if value:match( "^%w+$" ) then`
`       local n = #value`
`       local k = 1`
`       local c`
`       r = 0`
`       for i = n, 1, -1 do`
`           c = value:byte( i, i )`
`           if c >= 48  and  c <= 57 then`
`               c = c - 48`
`           elseif c >= 65  and  c <= 90 then`
`               c = c - 55`
`           elseif c >= 97  and  c <= 122 then`
`               c = c - 61`
`           else    -- How comes?`
`               r = 1`
`               break    -- for i`
`           end`
`           r = r + c * k`
`           k = k * 62`
`       end -- for i`
`   end`
`   return r`

end

\--[--------------------------\< tableLength \>----------------------- Given a 1-D table, return number of elements](https://ko.wikipedia.org/wiki/--------------------------\<_tableLength_\>-----------------------_Given_a_1-D_table,_return_number_of_elements "wikilink")

local function tableLength(T)

` local count = 0`
` for _ in pairs(T) do count = count + 1 end`
` return count`

end

\--[--------------------------\< dateFormat \>----------------------- Given a date string, return its format: dmy, mdy, iso, ymd If unable to determine return nil](https://ko.wikipedia.org/wiki/--------------------------\<_dateFormat_\>-----------------------_Given_a_date_string,_return_its_format:_dmy,_mdy,_iso,_ymd_If_unable_to_determine_return_nil "wikilink")

local function dateFormat(date)

` local dt = {}`
` dt.split = {}`

` dt.split = mw.text.split(date, "-")`
` if tableLength(dt.split) == 3 then`
`   if tonumber(dt.split[1]) > 1900 and tonumber(dt.split[1]) < 2200 and tonumber(dt.split[2]) and tonumber(dt.split[3]) then`
`     return "iso"`
`   else`
`     return nil`
`   end`
` end  `

` dt.split = mw.text.split(date, " ")`
` if tableLength(dt.split) == 3 then`
`   if tonumber(dt.split[3]) then`
`     if tonumber(dt.split[3]) > 1900 and tonumber(dt.split[3]) < 2200 then`
`       if tonumber(dt.split[1]) then`
`         return "dmy"`
`       else`
`         return "mdy"`
`       end `
`     else`
`       if tonumber(dt.split[1]) then`
`         if tonumber(dt.split[1]) > 1900 and tonumber(dt.split[1]) < 2200 then`
`           return "ymd"`
`         end`
`       end`
`     end`
`   end`
` end`
` return nil`

end

\--[--------------------------\< makeDate \>----------------------- Given a zero-padded 4-digit year, 2-digit month and 2-digit day, return a full date in df format df = mdy, dmy, iso, ymd](https://ko.wikipedia.org/wiki/--------------------------\<_makeDate_\>-----------------------_Given_a_zero-padded_4-digit_year,_2-digit_month_and_2-digit_day,_return_a_full_date_in_df_format_df_=_mdy,_dmy,_iso,_ymd "wikilink")

local function makeDate(year, month, day, df)

` if not year or year == "" or not month or month == "" or not day or day == "" then`
`   return nil`
` end`

` local zmonth = month                                                      -- month with leading 0`
` month = month:match("0*(%d+)")                                            -- month without leading 0`
` if tonumber(month) < 1 or tonumber(month) > 12 then`
`   return year`
` end`
` local nmonth = os.date("%B", os.time{year=2000, month=month, day=1} )     -- month in name form       `
` if not nmonth then`
`   return year`
` end`

` local zday = day`
` day = zday:match("0*(%d+)")`
` if tonumber(day) < 1 or tonumber(day) > 31 then`
`   if df == "mdy" or df == "dmy" then`
`     return nmonth .. " " .. year`
`   elseif df == "iso" then`
`     return year .. "-" .. zmonth `
`   elseif df == "ymd" then`
`     return year .. " " .. nmonth`
`   else`
`     return nmonth .. " " .. year`
`   end`
` end                                       `

` if df == "mdy" then`
`   return nmonth .. " " .. day .. ", " .. year         -- September 1, 2016`
` elseif df == "dmy" then`
`   return day .. " " .. nmonth .. " " .. year          -- 1 September 2016`
` elseif df == "iso" then`
`   return year .. "-" .. zmonth .. "-" .. zday         -- 2016-09-01`
` elseif df == "ymd" then`
`   return year .. " " .. nmonth .. " " .. cday          -- 2016 September 1`
` else`
`   return nmonth .. " " .. day .. ", " .. year         -- September 1, 2016`
` end`

end

\--[--------------------------\< decodeWebciteDate \>----------------------- Given a URI-path to Webcite (eg. /67xHmVFWP) return the encoded date in df format](https://ko.wikipedia.org/wiki/--------------------------\<_decodeWebciteDate_\>-----------------------_Given_a_URI-path_to_Webcite_\(eg._/67xHmVFWP\)_return_the_encoded_date_in_df_format "wikilink") local function decodeWebciteDate(path, df)

`   local dt = {}`
`   dt.split = {}`

`   dt.split = mw.text.split(path, "/")`

`   -- valid URL formats that are not base62`

`   -- `<http://www.webcitation.org/query?id=1138911916587475>
`   -- `<http://www.webcitation.org/query?url=http>`..&date=2012-06-01+21:40:03`
`   -- `<http://www.webcitation.org/1138911916587475>
`   -- `<http://www.webcitation.org/cache/73e53dd1f16cf8c5da298418d2a6e452870cf50e>
`   -- `<http://www.webcitation.org/getfile.php?fileid=1c46e791d68e89e12d0c2532cc3cf629b8bc8c8e>

`   if mw.ustring.find( dt.split[2], "query", 1, plain) or `
`      mw.ustring.find( dt.split[2], "cache", 1, plain) or`
`      mw.ustring.find( dt.split[2], "getfile", 1, plain) or`
`      tonumber(dt.split[2]) then`
`     return "query"`
`   end`

`   dt.full = os.date("%Y %m %d", string.sub(string.format("%d", base62(dt.split[2])),1,10) )`
`   dt.split = mw.text.split(dt.full, " ")`
`   dt.year = dt.split[1]`
`   dt.month = dt.split[2]`
`   dt.day = dt.split[3]`

`   if not tonumber(dt.year) or not tonumber(dt.month) or not tonumber(dt.day) then`
`     return inlineRed("[날짜 오류] (1)", "error")`
`   end`

`   if tonumber(dt.month) > 12 or tonumber(dt.day) > 31 or tonumber(dt.month) < 1 then`
`     return inlineRed("[날짜 오류] (2)", "error")`
`   end`
`   if tonumber(dt.year) > tonumber(os.date("%Y")) or tonumber(dt.year) < 1900 then`
`     return inlineRed("[날짜 오류] (3)", "error")`
`   end`

`   fulldate = makeDate(dt.year, dt.month, dt.day, df)`
`   if not fulldate then`
`     return inlineRed("[날짜 오류] (4)", "error")`
`   else`
`     return fulldate`
`   end`

end

\--[--------------------------\< snapDateToString \>----------------------- Given a URI-path to Wayback (eg. /web/20160901010101/http://example.com ) return the formatted date eg. "September 1, 2016" in df format Handle non-digits in snapshot ID such as "re_" and "-" and "\*"](https://ko.wikipedia.org/wiki/--------------------------\<_snapDateToString_\>-----------------------_Given_a_URI-path_to_Wayback_\(eg._/web/20160901010101/http://example.com_\)_return_the_formatted_date_eg._"September_1,_2016"_in_df_format_Handle_non-digits_in_snapshot_ID_such_as_"re_"_and_"-"_and_"*" "wikilink")

local function decodeWaybackDate(path, df)

`   local snapdate, snapdatelong, currdate, fulldate`

`   local safe = path`
`   snapdate = string.gsub(safe, "^/w?e?b?/?", "")                      -- Remove leading "/web/" or "/"`
`   safe = snapdate`
`   local N = mw.text.split(safe, "/")`
`   snapdate = N[1]`
`   if snapdate == "*" then                                             -- eg. /web/*/http..`
`     return "index"`
`   end`
`   safe = snapdate`
`   snapdate = string.gsub(safe, "[a-z][a-z]_[0-9]?$", "")              -- Remove any trailing "re_" from date `
`   safe = snapdate`
`   snapdate = string.gsub(safe, "[-]", "")                             -- Remove dashes from date eg. 2015-01-01 `
`   safe = snapdate`
`   snapdate = string.gsub(safe, "[*]$", "")                            -- Remove trailing "*" `

`   if not tonumber(snapdate) then`
`     return inlineRed("[날짜 오류] (2)", "error")`
`   end`
`   local dlen = string.len(snapdate)`
`   if dlen < 4 then`
`     return inlineRed("[날짜 오류] (3)", "error")`
`   end`
`   if dlen < 14 then`
`     snapdatelong = snapdate .. string.rep("0", 14 - dlen)`
`   else`
`     snapdatelong = snapdate`
`   end`
`   local year = string.sub(snapdatelong, 1, 4)`
`   local month = string.sub(snapdatelong, 5, 6)`
`   local day = string.sub(snapdatelong, 7, 8)`
`   if not tonumber(year) or not tonumber(month) or not tonumber(day) then`
`     return inlineRed("[날짜 오류] (4)", "error")`
`   end`
`   if tonumber(month) > 12 or tonumber(day) > 31 or tonumber(month) < 1 then`
`     return inlineRed("[날짜 오류] (5)", "error")`
`   end`
`   currdate = os.date("%Y")`
`   if tonumber(year) > tonumber(currdate) or tonumber(year) < 1900 then`
`     return inlineRed("[날짜 오류] (6)", "error")`
`   end`

`   fulldate = makeDate(year, month, day, df)`
`   if not fulldate then`
`     return inlineRed("[날짜 오류] (7)", "error")`
`   else`
`     return fulldate`
`   end`

end

\--[--------------------------\< serviceName \>----------------------- Given a domain extracted by mw.uri.new() (eg. web.archive.org) set tail string and service ID](https://ko.wikipedia.org/wiki/--------------------------\<_serviceName_\>-----------------------_Given_a_domain_extracted_by_mw.uri.new\(\)_\(eg._web.archive.org\)_set_tail_string_and_service_ID "wikilink")

local function serviceName(host, nolink)

` local tracking = "분류:웹아카이브 틀 기타 아카이브"`

` local bracketopen = "`[`"``   ``local``   ``bracketclose``   ``=``   ``"`](https://ko.wikipedia.org/wiki/"_local_bracketclose_=_" "wikilink")`"`
` if nolink then`
`   bracketopen = ""`
`   bracketclose = ""`
` end`

` ulx.url1.service = "other"`
` ulx.url1.tail = " - " .. ulx.url1.host .. " " .. inlineRed("오류: 알 수 없는 아카이브 URL")`

` if mw.ustring.find( host, "archive.org", 1, plain ) then`
`   ulx.url1.service = "wayback"`
`   ulx.url1.tail = " - " .. bracketopen .. "웨이백 머신" .. bracketclose`
`   tracking = "분류:웹아카이브 틀 웨이백 링크"`
` elseif mw.ustring.find( host, "webcitation.org", 1, plain ) then`
`   ulx.url1.service = "webcite"`
`   ulx.url1.tail = " - " .. bracketopen .. "WebCite" .. bracketclose`
`   tracking = "분류:웹아카이브 틀 웹인용 링크"`
` elseif mw.ustring.find( host, "archive.is", 1, plain ) then`
`   ulx.url1.service = "archiveis"`
`   ulx.url1.tail = " - " .. bracketopen .. "Archive.is" .. bracketclose`
`   tracking = "분류:웹아카이브 틀 archiveis 링크"`
` elseif mw.ustring.find( host, "archive.fo", 1, plain ) then`
`   ulx.url1.service = "archiveis"`
`   ulx.url1.tail = " - " .. bracketopen .. "Archive.is" .. bracketclose`
`   tracking = "분류:웹아카이브 틀 archiveis 링크"`
` elseif mw.ustring.find( host, "archive.today", 1, plain ) then`
`   ulx.url1.service = "archiveis"`
`   ulx.url1.tail = " - " .. bracketopen .. "Archive.is" .. bracketclose`
`   tracking = "분류:웹아카이브 틀 archiveis 링크"`
` elseif mw.ustring.find( host, "archive.il", 1, plain ) then`
`   ulx.url1.service = "archiveis"`
`   ulx.url1.tail = " - " .. bracketopen .. "Archive.is" .. bracketclose`
`   tracking = "분류:웹아카이브 틀 archiveis 링크"`
` elseif mw.ustring.find( host, "archive.ec", 1, plain ) then`
`   ulx.url1.service = "archiveis"`
`   ulx.url1.tail = " - " .. bracketopen .. "Archive.is" .. bracketclose`
`   tracking = "분류:웹아카이브 틀 archiveis 링크"`
` elseif mw.ustring.find( host, "archive[-]it.org", 1, plain ) then`
`   ulx.url1.service = "archiveit"`
`   ulx.url1.tail = " - " .. bracketopen .. "Archive-It" .. bracketclose`
` elseif mw.ustring.find( host, "arquivo.pt", 1, plain) then`
`   ulx.url1.tail = " - " .. "포르투갈어 웹 아카이브" `
` elseif mw.ustring.find( host, "loc.gov", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "미국 의회도서관" .. bracketclose`
` elseif mw.ustring.find( host, "webharvest.gov", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "미국 국립문서기록관리청" .. bracketclose`
` elseif mw.ustring.find( host, "bibalex.org", 1, plain ) then`
`   ulx.url1.tail = " - " .. "`[`신``   ``알렉산드리아``   ``도서관`](https://ko.wikipedia.org/wiki/신_알렉산드리아_도서관 "wikilink")`"`
` elseif mw.ustring.find( host, "collectionscanada", 1, plain ) then`
`   ulx.url1.tail = " - " .. "캐나다 정부 웹 아카이브"`
` elseif mw.ustring.find( host, "haw.nsk", 1, plain ) then`
`   ulx.url1.tail = " - " .. "크로아티아어 웹 아카이브 (HAW)"`
` elseif mw.ustring.find( host, "veebiarhiiv.digar.ee", 1, plain ) then`
`   ulx.url1.tail = " - " .. "에스토니아어 웹 아카이브"`
` elseif mw.ustring.find( host, "vefsafn.is", 1, plain ) then`
`   ulx.url1.tail = " - " .. "`[`아이슬란드``   ``국립``   ``및``   ``대학도서관`](https://ko.wikipedia.org/wiki/아이슬란드_국립_및_대학도서관 "wikilink")`"`
` elseif mw.ustring.find( host, "proni.gov", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "북아일랜드 기록보관소" .. bracketclose`
` elseif mw.ustring.find( host, "uni[-]lj.si", 1, plain ) then`
`   ulx.url1.tail = " - " .. "슬로베니아어 웹 아카이브"`
` elseif mw.ustring.find( host, "stanford.edu", 1, plain ) then`
`   ulx.url1.tail = " - " .. "`[`스탠퍼드``   ``웹``   ``아카이브`](https://ko.wikipedia.org/wiki/스탠퍼드_대학교_도서관 "wikilink")`"`
` elseif mw.ustring.find( host, "nationalarchives.gov.uk", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "영국 정부 웹 아카이브" .. bracketclose`
` elseif mw.ustring.find( host, "parliament.uk", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "영국 의회 웹 아카이브" .. bracketclose`
` elseif mw.ustring.find( host, "webarchive.org.uk", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "영국 웹 아카이브" .. bracketclose`
` elseif mw.ustring.find( host, "nlb.gov.sg", 1, plain ) then`
`   ulx.url1.tail = " - " .. "웹 아카이브 싱가포르" `
` elseif mw.ustring.find( host, "pandora.nla.gov.au", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "판도라 아카이브" .. bracketclose `
` elseif mw.ustring.find( host, "perma.cc", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "Perma.cc" .. bracketclose`
` elseif mw.ustring.find( host, "perma-archives.cc", 1, plain ) then`
`   ulx.url1.tail = " - " .. bracketopen .. "Perma.cc" .. bracketclose`
` elseif mw.ustring.find( host, "screenshots.com", 1, plain ) then`
`   ulx.url1.tail = " - 스크린샷" `
` elseif mw.ustring.find( host, "wikiwix.com", 1, plain ) then`
`   ulx.url1.tail = " - 위키윅스" `
` elseif mw.ustring.find( host, "freezepage.com", 1, plain ) then`
`   ulx.url1.tail = " - 프리즈페이지" `
` elseif mw.ustring.find( host, "webcache.googleusercontent.com", 1, plain ) then`
`   ulx.url1.tail = " - 구글 캐시" `
` else`
`   tracking = "분류:웹아카이브 틀 알 수 없는 아카이브"`
` end`

` track[tracking] = 1`

end

\--\[\[--------------------------\< parseExtraArgs \>-----------------------

`    Parse numbered arguments starting at 2, such as url2..url10, date2..date10, title2..title10`
`      For example: `
`        Three url arguments not in numeric sequence (1..4..7). `
`        Function only processes arguments numbered 2 or greater (in this case 4 and 7)`
`        It creates numeric sequenced table entries like:`
`          urlx.url2.url = `<argument value for url4>
`          urlx.url3.url = `<argument value for url7>
`      Returns the number of URL arguments found numbered 2 or greater (in this case returns "2")`

`]]`

local function parseExtraArgs()

` local i, j, argurl, argurl2, argdate, argtitle`

` j = 2`
` for i = 2, maxurls do`
`   argurl = "url" .. i`
`   if trimArg(args[argurl]) then`
`     argurl2 = "url" .. j`
`     ulx[argurl2] = {}`
`     ulx[argurl2]["url"] = args[argurl]`
`     argdate = "date" .. j`
`     if trimArg(args[argdate]) then`
`       ulx[argurl2]["date"] = args[argdate]`
`     else`
`       ulx[argurl2]["date"] = inlineRed("[날짜가 없음]", "warning")`
`     end`
`     argtitle = "title" .. j`
`     if trimArg(args[argtitle]) then`
`       ulx[argurl2]["title"] = args[argtitle]`
`     else`
`       ulx[argurl2]["title"] = nil`
`     end`
`     j = j + 1`
`   end`
` end`

` if j == 2 then`
`   return 0`
` else`
`   return j - 2`
` end`

end

\--[--------------------------\< comma \>----------------------- Given a date string, return "," if it's MDY](https://ko.wikipedia.org/wiki/--------------------------\<_comma_\>-----------------------_Given_a_date_string,_return_","_if_it's_MDY "wikilink")

local function comma(date)

` local N = mw.text.split(date, " ")`
` local O = mw.text.split(N[1], "-") -- for ISO`
` if O[1] == "index" then return "" end`
` if not tonumber(O[1]) then`
`   return ","`
` else`
`   return ""`
` end`

end

\--\[\[--------------------------\< createTracking \>-----------------------

`    Return data in track[] ie. tracking categories`

` ]]`

local function createTracking()

` local sand = ""`
` if tableLength(track) > 0 then                        `
`   for key,_ in pairs(track) do`
`     sand = sand .. "`[`"``   ``..``   ``key``   ``..``   ``"`](https://ko.wikipedia.org/wiki/"_.._key_.._" "wikilink")`"`
`   end`
` end`
` return sand`

end

\--\[\[--------------------------\< createRendering \>-----------------------

`    Return a rendering of the data in ulx[][]`

` ]]`

local function createRendering()

`   local sand, displayheader, displayfield`

`   local period1 = ""   -- For backwards compat with `
`   local period2 = "."                                                            `
` `
`   local indexstr = "보존일"`
`   if ulx.url1.date == "index" then`
`     indexstr = "보존"`
`   end  `
`                                                                                         -- For ``, `

`   if ulx.url1.format == "none" then                                                     `
`     if not ulx.url1.title and not ulx.url1.date then                                    -- No title. No date`
`       sand = "[" .. ulx.url1.url .. " Archived]" .. ulx.url1.tail`
`     elseif not ulx.url1.title and ulx.url1.date then                                    -- No title. Date.`
`       if ulx.url1.service == "wayback" then `
`         period1 = "."`
`         period2 = "" `
`       end`
`       sand = "[" .. ulx.url1.url .. " Archived] " .. ulx.url1.date .. comma(ulx.url1.date) .. ulx.url1.tail .. period1`
`     elseif ulx.url1.title and not ulx.url1.date then                                    -- Title. No date.`
`       sand = "[" .. ulx.url1.url .. " " .. ulx.url1.title .. "]" .. ulx.url1.tail`
`     elseif ulx.url1.title and ulx.url1.date then                                        -- Title. Date.`
`       sand = "[" .. ulx.url1.url .. " " .. ulx.url1.title .. "]" .. ulx.url1.tail .. " (" .. indexstr .. " " .. ulx.url1.date .. ")"`
`     else`
`       return nil`
`     end`
`     if ulx.url1.extraurls > 0 then                                                      -- For multiple archive URLs`
`       local tot = ulx.url1.extraurls + 1`
`       sand = sand .. period2 .. " Additional archives: "`
`       for i=2,tot do`
`         local indx = "url" .. i`
`         if ulx[indx]["title"] then `
`           displayfield = "title"`
`         else`
`           displayfield = "date"`
`         end`
`         sand = sand .. "[" .. ulx[indx]["url"] .. " " .. ulx[indx][displayfield] .. "]"`
`         if i == tot then`
`           sand = sand .. "."`
`         else`
`           sand = sand .. ", "`
`         end`
`       end`
`     else`
`       return sand  `
`     end`
`     return sand`
`                                                                                         -- For `

`   else                                                                  `
`     if ulx.url1.format == "addlarchives" then                           -- Multiple archive services `
`       displayheader = "Additional archives: "`
`     else                                                                -- Multiple pages from the same archive `
`       displayheader = "Additional pages archived on " .. ulx.url1.date .. ": "`
`     end`
`     local tot = 1 + ulx.url1.extraurls`
`     local sand = displayheader`
`     for i=1,tot do`
`       local indx = "url" .. i`
`       displayfield = ulx[indx]["title"]`
`       if ulx.url1.format == "addlarchives" then`
`         if not displayfield then `
`           displayfield = ulx[indx]["date"]`
`         end`
`       else`
`         if not displayfield then `
`           displayfield = "Page " .. i`
`         end`
`       end`
`       sand = sand .. "[" .. ulx[indx]["url"] .. " " .. displayfield .. "]"`
`       if i == tot then`
`         sand = sand .. "."`
`       else`
`         sand = sand .. ", "`
`       end`
`     end`
`     return sand`
`   end`

end

function p.webarchive(frame)

` args = frame.args`
` if (args[1]==nil) and (args["url"]==nil) then           -- if no argument provided than check parent template/module args`
`   args = frame:getParent().args `
` end`

` local tname = "웹아카이브"                                -- name of calling template. Change if template rename.`
` ulx = {}                                                -- Associative array to hold template data `
` track = {}                                              -- Associative array to hold tracking categories`
` maxurls = 10                                            -- Max number of URLs allowed. `
` local verifydates = "yes"                               -- See documentation. Set "no" to disable.`

`                                                         -- URL argument (first)`

` local url1 = trimArg(args.url) or trimArg(args.url1)           `
` if not url1 then`
`   return inlineError("url", "비어 있음.") .. createTracking()`
` end`
` if mw.ustring.find( url1, "`<https://web.http>`", 1, plain ) then    -- track bug `
`   track["분류:웹아카이브 틀 오류"] = 1 `
`   return inlineError("url", "`<https://web.http>`") .. createTracking()`
` end `
` if url1 == "`<https://web.archive.org/http:/>`" then                 -- track bug`
`   track["분류:웹아카이브 틀 오류"] = 1 `
`   return inlineError("url", "유효하지 않은 URL") .. createTracking()`
` end`

` ulx.url1 = {}`
` ulx.url1.url = url1`
` local uri1 = mw.uri.new(ulx.url1.url)`
` ulx.url1.host = uri1.host`
` ulx.url1.extraurls = parseExtraArgs()`

`                                                         -- Nolink argument `

` local nolink = trimArg2(args.nolink)`

` serviceName(uri1.host, nolink)`

`                                                         -- Date argument`

` local date = trimArg(args.date) or trimArg(args.date1)`
` if date == "*" and ulx.url1.service == "wayback" then`
`   date = "index"`
` elseif date and ulx.url1.service == "wayback" and verifydates == "yes" then `
`   local ldf = dateFormat(date)`
`   if ldf then`
`     local udate = decodeWaybackDate( uri1.path, ldf )`
`     if udate ~= date then`
`       date = udate .. inlineRed("`<sup>`[날짜``   ``불일치]`</sup>`", "warning")       `
`     end`
`   end`
` elseif date and ulx.url1.service == "webcite" and verifydates == "yes" then `
`   local ldf = dateFormat(date)`
`   if ldf then`
`     local udate = decodeWebciteDate( uri1.path, ldf )`
`     if udate == "query" then -- skip`
`     elseif udate ~= date then`
`       date = udate .. inlineRed("`<sup>`[날짜``   ``불일치]`</sup>`", "warning")      `
`     end`
`   end`
` elseif not date and ulx.url1.service == "wayback" then`
`   date = decodeWaybackDate( uri1.path, "iso" )`
`   if not date then `
`     date = inlineRed("[날짜 오류] (1)", "error") `
`   end`
` elseif not date and ulx.url1.service == "webcite" then`
`   date = decodeWebciteDate( uri1.path, "iso" )`
`   if date == "query" then`
`     date = inlineRed("[날짜 없음]", "warning")`
`   elseif not date then `
`     date = inlineRed("[날짜 오류] (1)", "error")`
`   end`
` elseif not date then`
`   date = inlineRed("[날짜 없음]", "warning")`
` end`
` ulx.url1.date = date`

`                                                         -- Format argument `

` local format = trimArg(args.format)`
` if not format then`
`   format = "none"`
` else`
`   if format == "addlpages" then`
`     if not ulx.url1.date then`
`       format = "none"`
`     end`
`   elseif format == "addlarchives" then`
`     format = "addlarchives"`
`   else`
`     format = "none"`
`   end`
` end`
` ulx.url1.format = format`

`                                                         -- Title argument `

` local title = trimArg(args.title) or trimArg(args.title1)`
` ulx.url1.title = title`
` `

` local rend = createRendering()`
` if not rend then`
`   rend = '`<span style="font-size:100%" class="error citation-comment">[`:틀:'``   ``..``   ``tname``   ``..``   ``'`](https://ko.wikipedia.org/wiki/:틀:'_.._tname_.._' "wikilink")` 안에 오류가 있습니다: 알 수 없는 문제. 틀토론 문서에 보고해 주십시오.`</span>`'`
`   track["분류:웹아카이브 틀 오류"] = 1 `
` end`

` return rend .. createTracking()`

end

return p