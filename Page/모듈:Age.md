> This article is converted from Wikipedia: [:Age](https://ko.wikipedia.org/wiki/:Age).


\-- Implement various "age of" and other date-related templates.

local _Date, _current_date local function get_exports(frame)

`   -- Return objects exported from the date module or its sandbox.`
`   if not _Date then`
`       local sandbox = frame:getTitle():find('sandbox', 1, true) and '/sandbox' or ''`
`       local datemod = require('Module:Date' .. sandbox)`
`       _Date = datemod._Date`
`       _current_date = datemod._current`
`   end`
`   return _Date, _current_date`

end

local function collection()

`   -- Return a table to hold items.`
`   return {`
`       n = 0,`
`       add = function (self, item)`
`           self.n = self.n + 1`
`           self[self.n] = item`
`       end,`
`       join = function (self, sep)`
`           return table.concat(self, sep)`
`       end,`
`   }`

end

local function strip_to_nil(text)

`   -- If text is a string, return its trimmed content, or nil if empty.`
`   -- Otherwise return text (which may, for example, be nil).`
`   if type(text) == 'string' then`
`       text = text:match('(%S.-)%s*$')`
`   end`
`   return text`

end

local function yes(parameter)

`   -- Return true if parameter should be interpreted as "yes".`
`   -- Do not want to accept mixed upper/lowercase unless done by current templates.`
`   -- Need to accept "on" because "round=on" is wanted.`
`   return ({ y = true, yes = true, on = true })[parameter]`

end

local function message(msg, nocat)

`   -- Return formatted message text for an error.`
`   -- Can append "#FormattingError" to URL of a page with a problem to find it.`
`   local anchor = '`<span id="FormattingError"></span>`'`
`   local category`
`   if not nocat and mw.title.getCurrentTitle():inNamespaces(0, 10) then`
`       -- Category only in namespaces: 0=article, 10=template.`
`       category = ''`
`   else`
`       category = ''`
`   end`
`   return anchor ..`
`       '`<strong class="error">`Error: ' ..`
`       mw.text.nowiki(msg) ..`
`       '`</strong>`' ..`
`       category`

end

local function formatnumber(number)

`   -- Return the given number formatted with commas as group separators,`
`   -- given that the number is an integer.`
`   local numstr = tostring(number)`
`   local length = #numstr`
`   local places = collection()`
`   local pos = 0`
`   repeat`
`       places:add(pos)`
`       pos = pos + 3`
`   until pos >= length`
`   places:add(length)`
`   local groups = collection()`
`   for i = places.n, 2, -1 do`
`       local p1 = length - places[i] + 1`
`       local p2 = length - places[i - 1]`
`       groups:add(numstr:sub(p1, p2))`
`   end`
`   return groups:join(',')`

end

local function make_sort(value, sortable)

`   -- Return a sort key in a span if specified.`
`   -- Assume value is a valid number which has not overflowed.`
`   if sortable == 'sortable_on' or sortable == 'sortable_debug' then`
`       local sortkey`
`       if value == 0 then`
`           sortkey = '5000000000000000000'`
`       else`
`           local mag = math.floor(math.log10(math.abs(value)) + 1e-14)`
`           local prefix`
`           if value > 0 then`
`               prefix = 7000 + mag`
`           else`
`               prefix = 2999 - mag`
`               value = value + 10^(mag+1)`
`           end`
`           sortkey = string.format('%d', prefix) .. string.format('%015.0f', math.floor(value * 10^(14-mag)))`
`       end`
`       local lhs = sortable == 'sortable_debug' and`
`           '`<span style="border:1px solid;display:inline;" class="sortkey">`' or`
`           '`<span style="display:none" class="sortkey">`'`
`       return lhs .. sortkey .. '♠`</span>`'`
`   end`

end

local translate_parameters = {

`   abbr = {`
`       off = 'abbr_off',`
`       on = 'abbr_on',`
`   },`
`   disp = {`
`       age = 'disp_age',`
`       raw = 'disp_raw',`
`   },`
`   format = {`
`       raw = 'format_raw',`
`       commas = 'format_commas',`
`   },`
`   round = {`
`       on = 'on',`
`       yes = 'on',`
`       months = 'ym',`
`       weeks = 'ymw',`
`       days = 'ymd',`
`       hours = 'ymdh',`
`   },`
`   sep = {`
`       comma = 'sep_comma',`
`       [','] = 'sep_comma',`
`       serialcomma = 'sep_serialcomma',`
`       space = 'sep_space',`
`   },`
`   show = {`
`       hide = { id = 'hide' },`
`       y = { 'y', id = 'y' },`
`       ym = { 'y', 'm', id = 'ym' },`
`       ymd = { 'y', 'm', 'd', id = 'ymd' },`
`       ymw = { 'y', 'm', 'w', id = 'ymw' },`
`       ymwd = { 'y', 'm', 'w', 'd', id = 'ymwd' },`
`       yd = { 'y', 'd', id = 'yd', keepzero = true },`
`       m = { 'm', id = 'm' },`
`       md = { 'm', 'd', id = 'md' },`
`       w = { 'w', id = 'w' },`
`       wd = { 'w', 'd', id = 'wd' },`
`       h = { 'H', id = 'h' },`
`       hm = { 'H', 'M', id = 'hm' },`
`       hms = { 'H', 'M', 'S', id = 'hms' },`
`       d = { 'd', id = 'd' },`
`       dh = { 'd', 'H', id = 'dh' },`
`       dhm = { 'd', 'H', 'M', id = 'dhm' },`
`       dhms = { 'd', 'H', 'M', 'S', id = 'dhms' },`
`       ymdh = { 'y', 'm', 'd', 'H', id = 'ymdh' },`
`       ymdhm = { 'y', 'm', 'd', 'H', 'M', id = 'ymdhm' },`
`       ymwdh = { 'y', 'm', 'w', 'd', 'H', id = 'ymwdh' },`
`       ymwdhm = { 'y', 'm', 'w', 'd', 'H', 'M', id = 'ymwdhm' },`
`   },`
`   sortable = {`
`       off = false,`
`       on = 'sortable_on',`
`       debug = 'sortable_debug',`
`   },`

}

local function date_extract(frame)

`   -- Return part of a date after performing an optional operation.`
`   local Date = get_exports(frame)`
`   local args = frame:getParent().args`
`   local parms = {}`
`   for i, v in ipairs(args) do`
`       parms[i] = v`
`   end`
`   if yes(args.fix) then`
`       table.insert(parms, 'fix')`
`   end`
`   if yes(args.partial) then`
`       table.insert(parms, 'partial')`
`   end`
`   local date = Date(unpack(parms))`
`   if not date then`
`       return message('Need valid date')`
`   end`
`   local add = strip_to_nil(args.add)`
`   if add then`
`       for item in add:gmatch('%S+') do`
`           date = date + item`
`           if not date then`
`               return message('Cannot add "' .. item .. '"')`
`           end`
`       end`
`   end`
`   local prefix, result`
`   local sortable = translate_parameters.sortable[args.sortable]`
`   if sortable then`
`       local value = (date.partial and date.partial.first or date).jdz`
`       prefix = make_sort(value, sortable)`
`   end`
`   local show = strip_to_nil(args.show) or 'dmy'`
`   if show ~= 'hide' then`
`       result = date[show]`
`       if result == nil then`
`           result = date:text(show)`
`       elseif type(result) == 'boolean' then`
`           result = result and '1' or '0'`
`       else`
`           result = tostring(result)`
`       end`
`   end`
`   return (prefix or '') .. (result or '')`

end

local function make_text(values, components, names, options)

`   -- Return wikitext representing an age or duration.`
`   local text = collection()`
`   local count = #values`
`   local sep = names.sep or ''`
`   for i, v in ipairs(values) do`
`       -- v is a number (say 4 for 4 years), or a table ({4,5} for 4 or 5 years).`
`       local islist = type(v) == 'table'`
`       if (islist or v > 0) or (text.n == 0 and i == count) or (text.n > 0 and components.keepzero) then`
`           local fmt, vstr`
`           if i == 1 and options.format == 'format_commas' then`
`               -- Numbers after the first should be small and not need formatting.`
`               fmt = formatnumber`
`           else`
`               fmt = tostring`
`           end`
`           if islist then`
`               local join = options.range == 'dash' and '–' or ' or '`
`               vstr = fmt(v[1]) .. join .. fmt(v[2])`
`           else`
`               vstr = fmt(v)`
`           end`
`           local name = names[components[i]]`
`           if name then`
`               local plural = names.plural`
`               if not plural or (islist and v[2] or v) == 1 then`
`                   plural = ''`
`               end`
`               text:add(vstr .. sep .. name .. plural)`
`           else`
`               text:add(vstr)`
`           end`
`       end`
`   end`
`   local first, last`
`   if options.join == 'sep_space' then`
`       first = ' '`
`       last = ' '`
`   elseif options.join == 'sep_comma' then`
`       first = ', '`
`       last = ', '`
`   elseif options.join == 'sep_serialcomma' and text.n > 2 then`
`       first = ', '`
`       last = ', and '`
`   else`
`       first = ', '`
`       last = ' and '`
`   end`
`   for i, v in ipairs(text) do`
`       if i < text.n then`
`           text[i] = v .. (i + 1 < text.n and first or last)`
`       end`
`   end`
`   local sign = ''`
`   if options.isnegative then`
`       -- Do not display negative zero.`
`       if text.n > 1 or (text.n == 1 and text[1]:sub(1, 1) ~= '0' ) then`
`           if options.format == 'format_raw' then`
`               sign = '-'  -- plain hyphen so result can be used in a calculation`
`           else`
`               sign = '−'  -- Unicode U+2212 MINUS SIGN`
`           end`
`       end`
`   end`
`   return`
`       (options.prefix or '') ..`
`       sign ..`
`       text:join() ..`
`       (options.suffix or '')`

end

local function date_difference(parms)

`   -- Return a formatted date difference using the given parameters`
`   -- which have been validated.`
`   local names = {`
`       abbr_off = {`
`           plural = 's',`
`           sep = ' ',`
`           y = 'year',`
`           m = 'month',`
`           w = 'week',`
`           d = 'day',`
`           H = 'hour',`
`           M = 'minute',`
`           S = 'second',`
`       },`
`       abbr_on = {`
`           y = 'y',`
`           m = 'm',`
`           w = 'w',`
`           d = 'd',`
`           H = 'h',`
`           M = 'm',`
`           S = 's',`
`       },`
`       abbr_infant = {      -- for `
`           plural = 's',`
`           sep = ' ',`
`           y = 'yr',`
`           m = 'mo',`
`           w = 'wk',`
`           d = 'day',`
`           H = 'hr',`
`           M = 'min',`
`           S = 'sec',`
`       },`
`       abbr_raw = {},`
`   }`
`   local diff = parms.diff  -- must be a valid date difference`
`   local show = parms.show  -- may be nil; default is set below`
`   local abbr = parms.abbr or 'abbr_off'`
`   local default_join`
`   if abbr ~= 'abbr_off' then`
`       default_join = 'sep_space'`
`   end`
`   if not show then`
`       show = 'ymd'`
`       if parms.disp == 'disp_age' then`
`           if diff.years < 3 then`
`               default_join = 'sep_space'`
`               if diff.years >= 1 then`
`                   show = 'ym'`
`               else`
`                   show = 'md'`
`               end`
`           else`
`               show = 'y'`
`           end`
`       end`
`   end`
`   if type(show) ~= 'table' then`
`       show = translate_parameters.show[show]`
`   end`
`   if parms.disp == 'disp_raw' then`
`       default_join = 'sep_space'`
`       abbr = 'abbr_raw'`
`   elseif parms.want_sc then`
`       default_join = 'sep_serialcomma'`
`   end`
`   local diff_options = {`
`       round = parms.round,`
`       duration = parms.want_duration,`
`       range = parms.range and true or nil,`
`   }`
`   local prefix`
`   if parms.sortable then`
`       local value = diff.age_days + (parms.want_duration and 1 or 0)  -- days and fraction of a day`
`       if diff.isnegative then`
`           value = -value`
`       end`
`       prefix = make_sort(value, parms.sortable)`
`   end`
`   local text_options = {`
`       prefix = prefix,`
`       suffix = parms.suffix,  -- not currently used`
`       format = parms.format,`
`       join = parms.sep or default_join,`
`       isnegative = diff.isnegative,`
`       range = parms.range,`
`   }`
`   if show.id == 'hide' then`
`       return prefix or ''`
`   end`
`   local values = { diff:age(show.id, diff_options) }`
`   if values[1] then`
`       return make_text(values, show, names[abbr], text_options)`
`   end`
`   return message('Parameter show=' .. show.id .. ' is not supported here')`

end

local function get_dates(frame, getopt)

`   -- Parse template parameters and return one of:`
`   -- * date         (a date table, if single)`
`   -- * date1, date2 (two date tables, if not single)`
`   -- * text         (a string error message)`
`   -- A missing date is replaced with the current date.`
`   -- If want_mixture is true, a missing date component is replaced`
`   -- from the current date, so can get a bizarre mixture of`
`   -- specified/current y/m/d as has been done by some "age" templates.`
`   -- Some results may be placed in table getopt.`
`   local Date, current_date = get_exports(frame)`
`   getopt = getopt or {}`
`   local fix = getopt.fix and 'fix' or ''`
`   local partial = getopt.range and 'partial' or ''`
`   local args = frame:getParent().args`
`   local fields = {}`
`   local is_named = args.year or args.year1 or args.year2 or`
`       args.month or args.month1 or args.month2 or`
`       args.day or args.day1 or args.day2`
`   if is_named then`
`       fields[1] = args.year1 or args.year`
`       fields[2] = args.month1 or args.month`
`       fields[3] = args.day1 or args.day`
`       fields[4] = args.year2`
`       fields[5] = args.month2`
`       fields[6] = args.day2`
`   else`
`       for i = 1, 6 do`
`           fields[i] = args[i]`
`       end`
`   end`
`   local imax = 0`
`   for i = 1, 6 do`
`       fields[i] = strip_to_nil(fields[i])`
`       if fields[i] then`
`           imax = i`
`       end`
`   end`
`   local single = getopt.single`
`   local dates = {}`
`   if is_named or imax > 2 then`
`       local nr_dates = single and 1 or 2`
`       if getopt.want_mixture then`
`           -- Cannot be partial since empty fields are set from current.`
`           local components = { 'year', 'month', 'day' }`
`           for i = 1, nr_dates * 3 do`
`               fields[i] = fields[i] or current_date[components[i > 3 and i - 3 or i]]`
`           end`
`           for i = 1, nr_dates do`
`               local index = i == 1 and 1 or 4`
`               dates[i] = Date(fields[index], fields[index+1], fields[index+2])`
`           end`
`       else`
`           for i = 1, nr_dates do`
`               local index = i == 1 and 1 or 4`
`               local y, m, d = fields[index], fields[index+1], fields[index+2]`
`               if (partial and y) or (y and m and d) then`
`                   dates[i] = Date(fix, partial, y, m, d)`
`               elseif not (y or m or d) then`
`                   dates[i] = Date('currentdate')`
`               end`
`           end`
`       end`
`   else`
`       getopt.textdates = true`
`       dates[1] = Date(fix, partial, fields[1] or 'currentdate')`
`       if not single then`
`           dates[2] = Date(fix, partial, fields[2] or 'currentdate')`
`       end`
`   end`
`   if not dates[1] then`
`       return message('Need valid year, month, day')`
`   end`
`   if single then`
`       return dates[1]`
`   end`
`   if not dates[2] then`
`       return message('Second date should be year, month, day')`
`   end`
`   return dates[1], dates[2]`

end

local function age_generic(frame)

`   -- Return the result required by the specified template.`
`   -- Can use sortable=x where x = on/off/debug in any supported template.`
`   -- Some templates default to sortable=on but can be overridden with sortable=off.`
`   local name = frame.args.template`
`   if not name then`
`       return message('The template invoking this must have "|template=x" where x is the wanted operation')`
`   end`
`   local args = frame:getParent().args`
`   local specs = {`
`       age_days = {                -- `
`           show = 'd',`
`           disp = 'disp_raw',`
`       },`
`       age_days_nts = {            -- `
`           show = 'd',`
`           disp = 'disp_raw',`
`           format = 'format_commas',`
`           sortable = 'on',`
`       },`
`       duration_days = {           -- `
`           show = 'd',`
`           disp = 'disp_raw',`
`           duration = true,`
`       },`
`       duration_days_nts = {       -- `
`           show = 'd',`
`           disp = 'disp_raw',`
`           format = 'format_commas',`
`           sortable = 'on',`
`           duration = true,`
`       },`
`       age_full_years = {          -- `
`           show = 'y',`
`           abbr = 'abbr_raw',`
`       },`
`       age_full_years_nts = {      -- `
`           show = 'y',`
`           abbr = 'abbr_raw',`
`           format = 'format_commas',`
`           sortable = 'on',`
`       },`
`       age_in_years = {            -- `
`           show = 'y',`
`           abbr = 'abbr_raw',`
`           negative = 'error',`
`           range = 'dash',`
`       },`
`       age_in_years_nts = {        -- `
`           show = 'y',`
`           abbr = 'abbr_raw',`
`           negative = 'error',`
`           range = 'dash',`
`           format = 'format_commas',`
`           sortable = 'on',`
`       },`
`       age_infant = {              -- `
`           -- Do not set show because special processing is done later.`
`           abbr = yes(args.abbr) and 'abbr_infant' or 'abbr_off',`
`           disp = 'disp_age',`
`           sep = 'sep_space',`
`           sortable = 'on',`
`       },`
`       age_m = {                   -- `
`           show = 'm',`
`           disp = 'disp_raw',`
`       },`
`       age_w = {                   -- `
`           show = 'w',`
`           disp = 'disp_raw',`
`       },`
`       age_wd = {                  -- `
`           show = 'wd',`
`       },`
`       age_yd = {                  -- `
`           show = 'yd',`
`           format = 'format_commas',`
`           sep = args.sep ~= 'and' and 'sep_comma' or nil,`
`           sortable = 'on',        -- temporarily use sortable for compatibility with old template; talk proposes removing this`
`       },`
`       age_yd_nts = {              -- `
`           show = 'yd',`
`           format = 'format_commas',`
`           sep = args.sep ~= 'and' and 'sep_comma' or nil,`
`           sortable = 'on',`
`       },`
`       age_ym = {                  -- `
`           show = 'ym',`
`           sep = 'sep_comma',`
`       },`
`       age_ymd = {                 -- `
`           show = 'ymd',`
`           range = true,`
`       },`
`       age_ymwd = {                -- `
`           show = 'ymwd',`
`           want_mixture = true,`
`       },`
`   }`
`   local spec = specs[name]`
`   if not spec then`
`       return message('The specified template name is not valid')`
`   end`
`   if name == 'age_days' then`
`       local su = strip_to_nil(args['show unit'])`
`       if su then`
`           if su == 'abbr' or su == 'full' then`
`               spec.disp = nil`
`               spec.abbr = su == 'abbr' and 'abbr_on' or nil`
`           end`
`       end`
`   end`
`   local range = spec.range or yes(args.range) or (args.range == 'dash' and 'dash' or nil)`
`   local getopt = {`
`       fix = yes(args.fix),`
`       range = range,`
`       want_mixture = spec.want_mixture,`
`   }`
`   local date1, date2 = get_dates(frame, getopt)`
`   if type(date1) == 'string' then`
`       return date1`
`   end`
`   local format = strip_to_nil(args.format)`
`   if format then`
`       format = 'format_' .. format`
`   elseif name == 'age_days' and getopt.textdates then`
`       format = 'format_commas'`
`   end`
`   local parms = {`
`       diff = date2 - date1,`
`       want_duration = spec.duration or yes(args.duration),`
`       range = range,`
`       want_sc = yes(args.sc),`
`       show = args.show == 'hide' and 'hide' or spec.show,`
`       abbr = spec.abbr,`
`       disp = spec.disp,`
`       format = format or spec.format,`
`       round = yes(args.round),`
`       sep = spec.sep,`
`       sortable = translate_parameters.sortable[args.sortable or spec.sortable],`
`   }`
`   if (spec.negative or frame.args.negative) == 'error' and parms.diff.isnegative then`
`       return message('The second date should not be before the first date')`
`   end`
`   return date_difference(parms)`

end

local function date_to_gsd(frame)

`   -- This implements ``.`
`   -- Return Gregorian serial date of the given date, or the current date.`
`   -- The returned value is negative for dates before 1 January 1 AD`
`   -- despite the fact that GSD is not defined for such dates.`
`   local date = get_dates(frame, { want_mixture=true, single=true })`
`   if type(date) == 'string' then`
`       return date`
`   end`
`   return tostring(date.gsd)`

end

local function jd_to_date(frame)

`   -- Return formatted date from a Julian date.`
`   -- The result includes a time if the input includes a fraction.`
`   -- The word 'Julian' is accepted for the Julian calendar.`
`   local Date = get_exports(frame)`
`   local args = frame:getParent().args`
`   local date = Date('juliandate', args[1], args[2])`
`   if date then`
`       return date:text()`
`   end`
`   return message('Need valid Julian date number')`

end

local function date_to_jd(frame)

`   -- Return Julian date (a number) from a date which may include a time,`
`   -- or the current date ('currentdate') or current date and time ('currentdatetime').`
`   -- The word 'Julian' is accepted for the Julian calendar.`
`   local Date = get_exports(frame)`
`   local args = frame:getParent().args`
`   local date = Date(args[1], args[2], args[3], args[4], args[5], args[6], args[7])`
`   if date then`
`       return tostring(date.jd)`
`   end`
`   return message('Need valid year/month/day or "currentdate"')`

end

local function time_interval(frame)

`   -- This implements ``.`
`   -- There are two positional arguments: date1, date2.`
`   -- The default for each is the current date and time.`
`   -- Result is date2 - date1 formatted.`
`   local Date = get_exports(frame)`
`   local args = frame:getParent().args`
`   local parms = {`
`       want_duration = yes(args.duration),`
`       range = yes(args.range) or (args.range == 'dash' and 'dash' or nil),`
`       want_sc = yes(args.sc),`
`   }`
`   local fix = yes(args.fix) and 'fix' or ''`
`   local date1 = Date(fix, 'partial', strip_to_nil(args[1]) or 'currentdatetime')`
`   if not date1 then`
`       return message('Invalid start date in first parameter')`
`   end`
`   local date2 = Date(fix, 'partial', strip_to_nil(args[2]) or 'currentdatetime')`
`   if not date2 then`
`       return message('Invalid end date in second parameter')`
`   end`
`   parms.diff = date2 - date1`
`   for argname, translate in pairs(translate_parameters) do`
`       local parm = strip_to_nil(args[argname])`
`       if parm then`
`           parm = translate[parm]`
`           if parm == nil then  -- test for nil because false is a valid setting`
`               return message('Parameter ' .. argname .. '=' .. args[argname] .. ' is invalid')`
`           end`
`           parms[argname] = parm`
`       end`
`   end`
`   if parms.round then`
`       local round = parms.round`
`       local show = parms.show`
`       if round ~= 'on' then`
`           if show then`
`               if show.id ~= round then`
`                   return message('Parameter show=' .. args.show .. ' conflicts with round=' .. args.round)`
`               end`
`           else`
`               parms.show = translate_parameters.show[round]`
`           end`
`       end`
`       parms.round = true`
`   end`
`   return date_difference(parms)`

end

return {

`   age_generic = age_generic,         -- can emulate several age templates`
`   gsd = date_to_gsd,                 -- Template:Gregorian_serial_date`
`   extract = date_extract,            -- Template:Extract`
`   jd_to_date = jd_to_date,           -- Template:?`
`   JULIANDAY = date_to_jd,            -- Template:JULIANDAY`
`   time_interval = time_interval,     -- Template:Time_interval`

}

[Category:Age_error](https://ko.wikipedia.org/wiki/Category:Age_error "wikilink")