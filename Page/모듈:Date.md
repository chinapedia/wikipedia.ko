> This article is converted from Wikipedia: [모듈:Date](https://ko.wikipedia.org/wiki/모듈:Date).


\--[This module is intended for processing of date strings. Please do not modify this code without applying the changes first at Module:Date/sandbox and testing at Module:Date/sandbox/testcases and Module talk:Date/sandbox/testcases. Authors and maintainers: \* User:Parent5446 - original version of the function mimicking template:ISOdate \* User:Jarekt - original version of the functions mimicking template:Date and template:ISOyear](https://ko.wikipedia.org/wiki/This_module_is_intended_for_processing_of_date_strings._Please_do_not_modify_this_code_without_applying_the_changes_first_at_Module:Date/sandbox_and_testing_at_Module:Date/sandbox/testcases_and_Module_talk:Date/sandbox/testcases._Authors_and_maintainers:_*_User:Parent5446_-_original_version_of_the_function_mimicking_template:ISOdate_*_User:Jarekt_-_original_version_of_the_functions_mimicking_template:Date_and_template:ISOyear "wikilink")

local p = {}

\-- ======================================= -- === Dependencies ====================== -- ======================================= --local i18n = require('Module:I18n/date') -- get localized translations of date formats --local Fallback = require('Module:Fallback') -- get fallback functions local yesno = require('Module:Yesno')

local i18n = { -- 다른 언어는 굳이 필요하지 않으니 한국어만 설정

`   DateLang = {`
`       ['ko'] = 'ko-form'`
`   },`
`   DateFormat = {`
`       ['ko-form'] = {`
`       YMDHMS='Y년 F j일, H:i:s',    `
`       YMDHM ='Y년 F j일, H:i',      `
`       YMD   ='Y년 F j일',       `
`       YM    ='Y년 F',      `
`       MD    ='F j일',      `
`       Y     ='Y년',`
`       M     ='F'`
`       }`
`   }`

} --\[=\[ ISOyear

This function returns year part of date string.

Usage: {{\#invoke:Date|ISOyear|target_string}}

Parameters

`   1: The date string `

Error Handling:

`  If the string does not look like it contain the year than the function will not return anything.`
`  That is the preferred treatment for the template:Creator which is the main (only?) template calling it.`

\]=\] function p.ISOyear( frame )

`   local input = frame.args[1]`
`   if not input then`
`       input = frame.args["s"]`
`   end`
`   input = mw.text.trim( input )`
`   `
`   -- if empty string then return it`
`   if input == "" then`
`       return input`
`   end`
`   `
`   -- if number then return it`
`   if tonumber( input ) then`
`       return mw.ustring.format( '%04i', input )`
`   end`
`   `
`   -- otherwise use regular expression match`
`   input = mw.ustring.match( input, '^(-?%d%d?%d?%d?)-' )`
`   if input then`
`       return mw.ustring.format( '%04i', input )`
`   else`
`       return ''`
`   end`

end

\--\[==\[ Date

This function is the core part of the ISOdate template.

Usage: {\#invoke:Date|Date|year=|month=|day=|hour=|minute=|second=|lang=en}}

Parameters:

`    year,month,day,hour,minute,second: broken down date-time component strings`
` lang: The language to display it in`
` case: Language format (genitive, etc.) for some languages`
`class: CSS class for the `<time>` node, use "" for no metadata at all`

`Error Handling:`

\]==\] function p.Date(frame)

`   return p._Date( `
`       { `
`           frame.args["year"] or '', `
`           frame.args["month"] or '',`
`           frame.args["day"] or '', `
`           frame.args["hour"] or '', `
`           frame.args["minute"] or '', `
`           frame.args["second"]or ''`
`       },`
`       frame.args["lang"] or 'ko',                  -- language`
`       frame.args["case"]  or '',           -- allows to specify grammatical case for the month for languages that use them`
`       frame.args["class"] or 'dtstart',    -- allows to set the html class of the time node where the date is included. This is useful for microformats.`
`       frame.args["trim_year"] or '100-999' -- by default pad one and 2 digit years to be 4 digit long, while keeping 3 digit years as is`
`   )   `

end

function p._Date(datavec, lang, case, class, trim_year)

`   -- if language is not provided than look up users language`
`   -- WARNING: This step should be done by the template as it does not seem to work as well here (cache issues?)`
`   if not lang or  not mw.language.isValidCode( lang ) then`
`       lang = 'ko'`
`   end`
`   `
`   -- Just in case someone broke the internationalization code than fix the english defaults`
`   if i18n.DateLang['ko'] == nil then`
`       i18n.DateLang['ko'] = 'ko-form'`
`   end `
`   if i18n.DateFormat['ko-form'] == nil then`
`       i18n.DateFormat['ko-form'] =  {`
`       YMDHMS='Y년 F j일, H:i:s',    `
`       YMDHM ='Y년 F j일, H:i',      `
`       YMD   ='Y년 F j일',       `
`       YM    ='Y년 F',      `
`       MD    ='F j일',      `
`       Y     ='Y년',`
`       M     ='F'`
`   }`
`   end`

`   -- create datecode based on which variables are provided and check for out of bound values`
`   local maxval = {9999, 12, 31, 23, 59, 60} -- max values for year, month, ...`
`   local c = {'Y', 'M', 'D', 'H', 'M', 'S'}`
`   local datecode = '' -- a string signifying which combination of variables was provided`
`   local datenum = {}  -- date-time encoded as a vector = [year, month, ... , second]`
`   for i, v in ipairs( datavec ) do`
`       if v~=nil and v~='' then`
`           datecode = datecode .. c[i]`
`           datenum[i] = tonumber(v)`
`           if datenum[i]==nil and i==2 then`
`               -- month is not a number -> check if it is a month name in English`
`               v = mw.language.new('en'):formatDate( "n", v)`
`               datenum[i] = tonumber(v)`
`           end`
`           if datenum[i]==nil or datenum[i]>maxval[i] then`
`               -- Some numbers are out of range -> abort and return the empty string`
`               return ''`
`           end`
`       end`
`   end`
`   `
`   -- create time stamp string (for example 2000-02-20 02:20:20) based on which variables were provided`
`   local timeStamp`
`   if datecode == 'YMDHMS' then`
`       timeStamp = string.format('%04i-%02i-%02i %02i:%02i:%02i', datenum[1], datenum[2], datenum[3], datenum[4], datenum[5], datenum[6] )`
`   elseif datecode == 'YMDHM' then`
`       timeStamp = string.format('%04i-%02i-%02i %02i:%02i', datenum[1], datenum[2], datenum[3], datenum[4], datenum[5] )`
`   elseif datecode:sub(1,3)=='YMD' then`
`       timeStamp = string.format('%04i-%02i-%02i', datenum[1], datenum[2], datenum[3] )`
`       datecode = 'YMD' -- 'YMD', 'YMDHMS' and 'YMDHM' are the only supported format starting with 'YMD'. All others will be converted to 'YMD'`
`   elseif datecode == 'YM' then`
`       timeStamp = string.format('%04i-%02i', datenum[1], datenum[2] )`
`   elseif datecode:sub(1,1)=='Y' then`
`       timeStamp = string.format('%04i', datenum[1] )`
`       datecode = 'Y' `
`   elseif datecode == 'M' then`
`       timeStamp = string.format('%04i-%02i-%02i', 2000, datenum[2], 1 )`
`       class = '' -- date not complete -> no html formating or micro-tagging of date string`
`   elseif datecode == 'MD' then`
`       timeStamp = string.format('%04i-%02i-%02i', 2000, datenum[2], datenum[3] )`
`       class = '' -- date not complete -> no html formating or micro-tagging of date string`
`   else`
`       return ''  -- format not supported`
`   end`

`   -- ==========================================================`
`   -- === Create Date String using in chosen language`
`   -- ==========================================================`
`   `
`   -- which form should the date take? `
`   -- Use Fallback module to handle rare languages which are more likely to use different for than default EN form`
`   local langDateForm = 'ko-form'`
`   `
`   -- special case of French and Gallic dates, which require different date format for the 1st day of the month`
`   if datenum[3]==1 and (langDateForm=='fr-form' or langDateForm=='ga-form') then`
`       langDateForm = langDateForm .. '1' -- ordinal form for the first day of the month`
`   end`
`   -- Look up country specific format input to {{#time}} function`
`   local dFormat = i18n.DateFormat[langDateForm][datecode]`
`   `
`   -- overwrite default grammatical case of the month (applies mostly to Slavic languages)`
`   if (case=='gen') then`
`       -- CAUTION: at the moment i18n.DateFormat uses "F" only as month name, but this might change and this operation does not check if 'F' is in "" brackets or not, so if some language starts using 'F'  in "" than this will not work for that language`
`       dFormat = dFormat:gsub("F", "xg"); `
`   end`
`   if (case=='nom') then`
`       -- CAUTION: at the moment i18n.DateFormat uses "xg" only as month name, but this might change and this operation does not check if 'xg' is in "" brackets or not, so if some language starts using 'xg'  in "" than this will not work for that language`
`       dFormat = dFormat:gsub("xg", "F");`
`   end`
`   if ((lang=='ru' or lang=='pl' or lang=='cs' or lang=='sl') and (case=='loc' or case=='ins')) or`
`       (lang=='fi' and (case=='ptv' or case=='ine'or case=='ela'or case=='ill') ) then`
`       local monthEn =  mw.language.new('en'):formatDate( "F", timeStamp) -- month name in English`
`       -- month name using proper case and language. It relies on messages stored in MediaWiki namespace for some cases and languages`
`       -- That is why this IF statement uses "lang" not "langDateForm" variable to decide`
`       local monthMsg =  mw.message.new( string.format('%s-%s', monthEn, case ) ):inLanguage( lang )`
`       if not monthMsg:isDisabled() then -- make sure it exists`
`           local month=monthMsg:plain()`
`           dFormat = dFormat:gsub('F', '"'..month..'"'); -- replace default month with month name we already looked up`
`           dFormat = dFormat:gsub('xg', '"'..month..'"');`
`       end`
`   end`
`   -- Special case related to Quechua and Kichwa languages`
`   -- see `<https://commons.wikimedia.org/wiki/Template_talk:Date#Quechua>` from 2014`
`   if (lang=='qu' or lang=='qug') and case=='nom' then`
`       dFormat = dFormat:gsub('F"pi"', 'F');`
`   end `

`   -- Lua only date formating using {{#time}} parser function (new)`
`       -- prefered call which gives "Lua error: too many language codes requested." on the `[`Module``   ``talk:Date/sandbox/testcases`](https://ko.wikipedia.org/wiki/Module_talk:Date/sandbox/testcases "wikilink")` page`
`       --local datestr = mw.language.new(lang):formatDate( dFormat, timeStamp) `
`   local datestr = mw.getCurrentFrame():callParserFunction( "#time", { dFormat, timeStamp, lang } )`
`   `
`   -- Another special case related to Thai solar calendar`
`   if lang=='th' and datenum[1]~= nil and datenum[1]<=1940 then`
`       -- As of 2014 {{#time}} parser function did not resolve those cases properly`
`       -- See `<https://en.wikipedia.org/wiki/Thai_solar_calendar#New_year>` for reference`
`       -- Disable once `<https://bugzilla.wikimedia.org/show_bug.cgi?id=66648>` is fixed`
`       if datecode=='Y' then -- date is ambiguous`
`           datestr = string.format('%04i หรือ %04i', datenum[1]+542, datenum[1]+543 ) `
`       elseif datenum[2]<=3 then -- year is wrong (one too many)`
`           datestr = datestr:gsub( string.format('%04i', datenum[1]+543), string.format('%04i', datenum[1]+542 ) )`
`       end`
`   end`
`   `
`   -- If year<1000 than either keep it padded to the length of 4 digits or trim it`
`   -- decide if the year will stay padded with zeros (for years in 0-999 range)`
`   if datenum[1]~= nil and datenum[1]<1000 then`
`       local trim = yesno(trim_year,nil)`
`       if trim == nil then`
`           local YMin, YMax = trim_year:match( '(%d+)-(%d+)' )`
`           trim = (YMin~=nil and datenum[1]>=tonumber(YMin) and datenum[1]<=tonumber(YMax)) `
`       end`
`   `
`       -- If the date form isn't the Thai solar calendar, don't zero pad years in the range of 100-999.  `
`       -- If at some point support for Islamic/Hebrew/Japanese years is added, they may need to be skipped as well. `
`       if trim then`
`           --local yearStr1 = mw.language.new(lang):formatDate( 'Y', timeStamp)`
`           local yearStr1 = mw.getCurrentFrame():callParserFunction( "#time", { 'Y', timeStamp, lang } )`
`           --local yearStr1 = datestr:match( '%d%d%d%d' ) -- 4 digits in a row (in any language) - that must be a year`
`           local yearStr2 = yearStr1`
`           local zeroStr = mw.ustring.sub(yearStr1,1,1)`
`           for i=1,3 do -- trim leading zeros`
`               if mw.ustring.sub(yearStr2,1,1)==zeroStr then`
`                   yearStr2 = mw.ustring.sub(yearStr2, 2, 5-i)`
`               else`
`                   break`
`               end`
`           end`
`           datestr = datestr:gsub( yearStr1, yearStr2 )`
`           --datestr = string.format('%s (%s, %s)', datestr, yearStr1, yearStr2 )`
`       end`
`   end`
`   `
`   -- html formating and tagging of date string`
`   if class ~= '' then`
`       local DateHtmlTags = '`<span style="white-space:nowrap"><time class="%s" datetime="%s">`%s`</time></span>`'`
`       datestr = DateHtmlTags:format(class, timeStamp, datestr)`
`   end`
`   return datestr`

end

\--\[===\[ ISOdate

This function is the core part of the ISOdate template.

Usage: {{\#invoke:Date|ISOdate|target_string|lang=}}

Parameters:

`    1: The date string `
` lang: The language to display it in`
` form: Language format (genitive, etc.) for some languages`
`class: CSS class for the `<time>` node`

`Error Handling:`
`  If the string does not look like it contain the proper ISO date than the function will return the original string.`
`  `
`  That is the preferred treatment for the template:Information (and similar templates) which calling it.`

\]===\] function p.ISOdate(frame)

`   local datevec = p._ISOdate( frame.args[1] )`
`   -- call p._Date function to format date string`
`   local succeded, datestr`
`   succeded, datestr = pcall( `
`       p._Date,                            -- call p._Date function with following arguments:`
`       datevec,                            -- {year, month, day, hour, minute, second} strings packed in a vector`
`       frame.args["lang"] or 'ko',                 -- language`
`       frame.args["case"]  or '',          -- allows to specify grammatical case for the month for languages that use them`
`       frame.args["class"] or 'dtstart',   -- allows to set the html class of the time node where the date is included. This is useful for microformats.`
`       frame.args["trim_year"] or '100-999'-- by default pad one and 2 digit years to be 4 digit long, while keeping 3 digit years as is`
`   )`
`   if succeded and datestr~='' then`
`       tail = mw.ustring.gsub(' ' .. tail, ' +', ' ')`
`       return mw.text.trim( datestr .. tail)`
`   else`
`       -- in case of errors return the original string`
`       return input`
`   end `

end

function p._ISOdate(d) -- Returns the vector for the date

`   -- pattern: regexp - regular expresion to test; dlen - number of date elements; tail = which element is a "tail" if any`
`   -- regexp hints:`
`   --  1) Strings starting with "^" and ending with "$" indicate whole string match`
`   --  2) optional tail part copied as-is and following the main parsed part of the date have to be separated from the date by a whitespace, so "(\s.+)?"`
`   local pattern = {`
`       -- strings starting with YYYY-MM-DD HH:MM:SS. Year 4 digits (if we know seconds than it was within the last 100 years), the rest 1-2`
`       -- date and time can be separated by space or "T" and there could be a "Z" on the end indicating "Zulu" time zone`
`       {dlen=6, tail=7, regexp="^(%d%d%d%d)-(%d%d?)-(%d%d?)[ T](%d%d?):(%d%d?):(%d%d?)Z?(%s.*)"}, `
`       {dlen=6, tail=0, regexp="^(%d%d%d%d)-(%d%d?)-(%d%d?)[ T](%d%d?):(%d%d?):(%d%d?)Z?$"}, `
`       -- strings starting with YYYY-MM-DD HH:MM. Year 4 digits, the rest 1-2`
`       {dlen=5, tail=6, regexp="^(%d%d%d%d)-(%d%d?)-(%d%d?)[ T](%d%d?):(%d%d?)(%s.+)"},`
`       {dlen=5, tail=0, regexp="^(%d%d%d%d)-(%d%d?)-(%d%d?)[ T](%d%d?):(%d%d?)$"},`
`       -- strings starting with YYYY-MM-DD. Year 3-4 digits, the rest 1-2`
`       {dlen=3, tail=4, regexp="^(%d%d?%d?%d?)-(%d%d?)-(%d%d?)(%s.+)"},`
`       {dlen=3, tail=0, regexp="^(%d%d?%d?%d?)-(%d%d?)-(%d%d?)$"},`
`       -- strings starting with YYYY-MM. Year 3-4 digits, month 1-2 digits`
`       {dlen=2, tail=3, regexp="^(%d%d?%d?%d?)-(%d%d?)(%s.+)"}, `
`       {dlen=2, tail=0, regexp="^(%d%d?%d?%d?)-(%d%d)$"}, `
`       -- string starts with a number -> it has to be 3 or 4 digit long to be a year`
`       {dlen=1, tail=2, regexp="^(%d%d%d%d?)(%s.+)"},  `
`        -- if whole string is a number (1-4 digit long) than it will be interpreted as a year`
`       {dlen=1, tail=0, regexp="^(%d%d?%d?%d?)$"},`
`   }`
`   `
`   -- create datevec based on which variables are provided`
`   local input = mw.text.trim( d )`
`   local datevec = {`*`,`*`,`*`,`*`,`*`,`*`}`
`   local tail = ''`
`   local vec, pat`
`   local debugStr = ''`
`   for i, pat in ipairs( pattern ) do`
`       vec = {input:match( pat.regexp )}`
`       if vec and vec[1]~=nil then`
`           for j=1,pat.dlen do`
`               datevec[j] = vec[j]`
`           end`
`           if pat.tail>0 and vec[pat.tail]~=nil then`
`               tail = vec[pat.tail]`
`           end`
`           debugStr = string.format(' (%i)', i)`
`           break`
`       end`
`   end `
`   if datevec[1]=='' or datevec[1]==nil then`
`       -- quickly return if input does not look like date (it could be a template)`
`       return input`
`   else`
`       return datevec`
`   end`

end

function p._isLeapYear( year )

`   if year % 400 == 0 then`
`       return 1`
`   elseif year % 100 == 0 and year % 400 ~= 0 then`
`       return 0`
`   elseif year % 4 == 0 and year % 100 ~= 0 then`
`       return 1`
`   else`
`       return 0`
`   end`

end

return p