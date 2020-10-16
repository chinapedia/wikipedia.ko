> This article is converted from Wikipedia: [모듈:Track listing](https://ko.wikipedia.org/wiki/모듈:Track_listing).


\-- This module implements [Template:Track listing](https://ko.wikipedia.org/wiki/Template:Track_listing "wikilink")

local yesno = require('Module:Yesno') local checkType = require('libraryUtil').checkType

local SHOW_WARNINGS = false local INPUT_ERROR_CATEGORY = '입력 오류가 있는 곡 목록' local COLLAPSED_PARAMETER_CATEGORY = '숨김 변수를 사용하는 곡 목록 '

\-- 로컬 변수 보관을 위해 사용 local localArgs

-----

\-- Helper functions

-----

\-- Add a mixin to a class. local function addMixin(class, mixin)

`   for k, v in pairs(mixin) do`
`       if k ~= 'init' then`
`           class[k] = v`
`       end`
`   end`

end

-----

\-- Validation mixin

-----

local Validation = {}

function Validation.init(self)

`   self.warnings = {}`
`   self.categories = {}`

end

function Validation:addWarning(msg, category)

`   table.insert(self.warnings, msg)`
`   table.insert(self.categories, category)`

end

function Validation:addCategory(category)

`   table.insert(self.categories, category)`

end

function Validation:getWarnings()

`   return self.warnings`

end

function Validation:getCategories()

`   return self.categories`

end

\-- Validate a track length. If a track length is invalid, a warning is added. -- A type error is raised if the length is not of type string or nil. function Validation:validateLength(length)

`   checkType('validateLength', 1, length, 'string', true)`
`   if length == nil then`
`       -- Do nothing if no length specified`
`       return nil`
`   end`

`   local hours, minutes, seconds`

`   -- Try to match times like "1:23:45".`
`   hours, minutes, seconds = length:match('^(%d+):(%d%d):(%d%d)$')`
`   if hours and hours:sub(1, 1) == '0' then`
`       -- Disallow times like "0:12:34"`
`       self:addWarning(string.format(`
`           "유효하지 않은 시간 '%s' ('h:mm:ss' 형식의 시간은 0으로 시작할 수 없습니다)",`
`           mw.text.nowiki(length)`
`       ), INPUT_ERROR_CATEGORY)`
`       return nil`
`   end`

`   if not seconds then`
`       -- The previous attempt didn't match. Try to match times like "1:23".`
`       minutes, seconds = length:match('^(%d?%d):(%d%d)$')`
`       if minutes and minutes:find('^0%d$') then`
`           -- Special case to disallow lengths like "01:23". This check has to`
`           -- be here so that lengths like "1:01:23" are still allowed.`
`           self:addWarning(string.format(`
`               "유효하지 않은 시간 '%s' ('mm:ss' 형식의 시간은 0으로 시작할 수 없습니다)",`
`               mw.text.nowiki(length)`
`           ), INPUT_ERROR_CATEGORY)`
`           return nil`
`       end`
`   end`

`   -- Add a warning and return if we did not find a match.`
`   if not seconds then`
`       self:addWarning(string.format(`
`           "유효하지 않은 시간 '%s' (시간은 'm:ss', 'mm:ss', 'h:mm:ss' 형식이어야 합니다)",`
`           mw.text.nowiki(length)`
`       ), INPUT_ERROR_CATEGORY)`
`       return nil`
`   end`

`   -- Check that the minutes are less than 60 if we have an hours field.`
`   if hours and tonumber(minutes) >= 60 then`
`       self:addWarning(string.format(`
`           "유효하지 않은 재생 시간 '%s' (시간을 지정하는 경우 분 숫자는 60보다 작아야 합니다)",`
`           mw.text.nowiki(length)`
`       ), INPUT_ERROR_CATEGORY)`
`       return nil`
`   end`
`   `
`   -- Check that the seconds are less than 60`
`   if tonumber(seconds) >= 60 then`
`       self:addWarning(string.format(`
`           "유효하지 않은 곡 길이 '%s' (초 숫자는 60보다 작아야 합니다)",`
`           mw.text.nowiki(length)`
`       ), INPUT_ERROR_CATEGORY)`
`   end`

`   return nil`

end

-----

\-- Track class

-----

local Track = {} Track.__index = Track addMixin(Track, Validation)

Track.fields = {

`   number = true,`
`   title = true,`
`   note = true,`
`   length = true,`
`   lyrics = true,`
`   music = true,`
`   writer = true,`
`   extra = true,`

}

\-- 한국어 변수 목록 fieldTranslations = {

`   -- Track.fields`
`   number = '#',`
`   title = '제목',`
`   note = '주',`
`   length = '재생시간',`
`   lyrics = '작사',`
`   music = '작곡',`
`   writer = '작사작곡',`
`   extra = '기타',`
`   `
`   -- TrackListing.fields`
`   all_writing = '전체작사작곡',`
`   all_lyrics = '전체작사',`
`   all_music = '전체작곡',`
`   collapsed = '숨김',`
`   headline = '표제',`
`   extra_column = '기타정보',`
`   total_length = '총재생시간',`
`   title_width = '제목너비',`
`   writing_width = '작사작곡너비',`
`   lyrics_width = '작사너비',`
`   music_width = '작곡너비',`
`   extra_width = '추가너비',`
`   category = '분류',`
`   `
`   -- TrackListing.deprecatedFields`
`   writing_credits = '작사작곡표시',`
`   lyrics_credits = '작사표시',`
`   music_credits = '작곡표시',`
`   arrangements_credits = '편곡표시',`
`   all_arrangements = '전체편곡'`

}

Track.cellMethods = {

`   number = 'makeNumberCell',`
`   title = 'makeTitleCell',`
`   writer = 'makeWriterCell',`
`   lyrics = 'makeLyricsCell',`
`   music = 'makeMusicCell',`
`   extra = 'makeExtraCell',`
`   length = 'makeLengthCell',`

}

function Track.new(data)

`   local self = setmetatable({}, Track)`
`   Validation.init(self)`
`   for field in pairs(Track.fields) do`
`       self[field] = data[field]`
`   end`
`   self.number = assert(tonumber(self.number))`
`   self:validateLength(self.length)`
`   return self`

end

function Track:getLyricsCredit()

`   return self.lyrics`

end

function Track:getMusicCredit()

`   return self.music`

end

function Track:getWriterCredit()

`   return self.writer`

end

function Track:getExtraField()

`   return self.extra`

end

\-- Note: called with single dot syntax function Track.makeSimpleCell(wikitext)

`   return mw.html.create('td')`
`       :css('vertical-align', 'top')`
`       :wikitext(wikitext or ' ')`

end

function Track:makeNumberCell()

`   local numberCell = mw.html.create('td')`
`   numberCell`
`       :css('padding-right', '10px')`
`       :css('text-align', 'right')`
`       :css('vertical-align', 'top')`
`       :css('white-space', 'nowrap') -- 사용자 지정 곡 번호가 잘리지 않도록 수정`

`   -- number 및 #을 사용하는 변수에 대해 트랙 번호를 변경할 수 있도록 조치`
`   local customNum = localArgs['#' .. self.number] or localArgs['number' .. self.number] or ''`
`   if (string.len(customNum) > 0) then`
`       numberCell`
`           :wikitext(customNum .. '.')`
`   else`
`       numberCell`
`           :wikitext(self.number .. '.')`
`   end`

`   return numberCell`

end

function Track:makeTitleCell()

`   local titleCell = mw.html.create('td')`
`   titleCell`
`       :css('vertical-align', 'top')`
`       :wikitext(self.title and string.format('"%s"', self.title) or '무제')`
`   if self.note then`
`       titleCell`
`           :wikitext(' ')`
`           :tag('span')`
`               :wikitext(string.format('(%s)', self.note))`
`   end`
`   return titleCell`

end

function Track:makeWriterCell()

`   return Track.makeSimpleCell(self.writer)`

end

function Track:makeLyricsCell()

`   return Track.makeSimpleCell(self.lyrics)`

end

function Track:makeMusicCell()

`   return Track.makeSimpleCell(self.music)`

end

function Track:makeExtraCell()

`   return Track.makeSimpleCell(self.extra)`

end

function Track:makeLengthCell()

`   return mw.html.create('td')`
`       :css('padding-right', '10px')`
`       :css('text-align', 'right')`
`       :css('vertical-align', 'top')`
`       :wikitext(self.length or ' ')`

end

function Track:exportRow(options)

`   options = options or {}`
`   local columns = options.columns or {}`
`   local row = mw.html.create('tr')`
`   row:css('background-color', options.color or '#fff')`
`   for i, column in ipairs(columns) do`
`       local method = Track.cellMethods[column]`
`       if method then`
`           row:node(self[method](self))`
`       end`
`   end`
`   return row`

end

-----

\-- TrackListing class

-----

local TrackListing = {} TrackListing.__index = TrackListing addMixin(TrackListing, Validation)

TrackListing.fields = {

`   headline = true,`
`   all_writing = true,`
`   all_lyrics = true,`
`   all_music = true,`
`   extra_column = true,`
`   total_length = true,`
`   title_width = true,`
`   writing_width = true,`
`   lyrics_width = true,`
`   music_width = true,`
`   extra_width = true,`
`   category = true,`

}

TrackListing.deprecatedFields = {

`   writing_credits = true,`
`   lyrics_credits = true,`
`   music_credits = true,`
`   arrangements_credits = true, -- 편곡표시`
`   all_arrangements = true, -- 전체편곡`

}

function translateFields(param)

`   if param ~= nil then`
`       if string.find(param, '^[a-zA-Z _]+$') then`
`           return param`
`       end`
`   `
`       for k,v in pairs(fieldTranslations) do`
`           if type(v) == 'table' then`
`               for _,vv in v do`
`                   if vv == param then`
`                       return k`
`                   end`
`               end`
`           elseif v == param then`
`               return k`
`           end`
`       end`
`   end`
`   `
`   return param`

end

function TrackListing.new(data)

`   local self = setmetatable({}, TrackListing)`
`   Validation.init(self)`

`   -- Check for deprecated arguments`
`   for deprecatedField in pairs(TrackListing.deprecatedFields) do`
`       if data[deprecatedField] then`
`           self:addCategory('구식 변수를 사용하는 곡 목록')`
`           break`
`       end`
`   end`

`   -- Validate total length`
`   if data.total_length then`
`       self:validateLength(data.total_length)`
`   end`
`   `
`   -- Add properties`
`   for field in pairs(TrackListing.fields) do`
`       self[field] = data[field]`
`   end`
`   `
`   -- Evaluate boolean properties`
`   self.showCategories = yesno(self.category) ~= false`
`   self.category = nil`

`   -- Make track objects`
`   self.tracks = {}`
`   for i, trackData in ipairs(data.tracks or {}) do`
`       table.insert(self.tracks, Track.new(trackData))`
`   end`

`   -- Find which of the optional columns we have.`
`   -- We could just check every column for every track object, but that would`
`   -- be no fun^H^H^H^H^H^H inefficient, so we use four different strategies`
`   -- to try and check only as many columns and track objects as necessary.`
`   do`
`       local optionalColumns = {}`
`       local columnMethods = {`
`           lyrics = 'getLyricsCredit',`
`           music = 'getMusicCredit',`
`           writer = 'getWriterCredit',`
`           extra = 'getExtraField',`
`       }`
`       local doneWriterCheck = false`
`       for i, trackObj in ipairs(self.tracks) do`
`           for column, method in pairs(columnMethods) do`
`               if trackObj[method](trackObj) then`
`                   optionalColumns[column] = true`
`                   columnMethods[column] = nil`
`               end`
`           end`
`           if not doneWriterCheck and optionalColumns.writer then`
`               doneWriterCheck = true`
`               optionalColumns.lyrics = nil`
`               optionalColumns.music = nil`
`               columnMethods.lyrics = nil`
`               columnMethods.music = nil`
`           end`
`           if not next(columnMethods) then`
`               break`
`           end`
`       end`
`       self.optionalColumns = optionalColumns`
`   end`

`   return self`

end

function TrackListing:makeIntro()

`   if self.all_writing then`
`       return string.format(`
`           '전체 작사·작곡: %s',`
`           self.all_writing`
`       )`
`   elseif self.all_lyrics and self.all_music then`
`       return string.format(`
`           '전체 작사: %s. 전체 작곡: %s',`
`           self.all_lyrics,`
`           self.all_music`
`       )`
`   elseif self.all_lyrics then`
`       return string.format(`
`           '전체 작사: %s',`
`           self.all_lyrics`
`       )`
`   elseif self.all_music then`
`       return string.format(`
`           '전체 작곡: %s',`
`           self.all_music`
`       )`
`   else`
`       return ''`
`   end`

end

function TrackListing:renderTrackingCategories()

`   if not self.showCategories or mw.title.getCurrentTitle().namespace ~= 0 then`
`       return ''`
`   end`

`   local ret = ''`

`   local function addCategory(cat)`
`       ret = ret .. string.format('`[`분류:%s`](https://ko.wikipedia.org/wiki/분류:%s "wikilink")`', cat)`
`   end`

`   for i, category in ipairs(self:getCategories()) do`
`       addCategory(category)`
`   end`

`   for i, track in ipairs(self.tracks) do`
`       for j, category in ipairs(track:getCategories()) do`
`           addCategory(category)`
`       end`
`   end`

`   return ret`

end

function TrackListing:renderWarnings()

`   if not SHOW_WARNINGS then`
`       return ''`
`   end`

`   local ret = {}`

`   local function addWarning(msg)`
`       table.insert(ret, string.format(`
`           '`<strong class="error">`곡 목록 오류: %s`</strong>`',`
`           msg`
`       ))`
`   end`

`   for i, warning in ipairs(self:getWarnings()) do`
`       addWarning(warning)`
`   end`

`   for i, track in ipairs(self.tracks) do`
`       for j, warning in ipairs(track:getWarnings()) do`
`           addWarning(warning)`
`       end`
`   end`

`   return table.concat(ret, '`
`')`

end

function TrackListing:__tostring()

`   -- Find columns to output`
`   local columns = {'number', 'title'}`
`   if self.optionalColumns.writer then`
`       columns[#columns + 1] = 'writer'`
`   else`
`       if self.optionalColumns.lyrics then`
`           columns[#columns + 1] = 'lyrics'`
`       end`
`       if self.optionalColumns.music then`
`           columns[#columns + 1] = 'music'`
`       end`
`   end`
`   if self.optionalColumns.extra then`
`       columns[#columns + 1] = 'extra'`
`   end`
`   columns[#columns + 1] = 'length'`

`   -- Find colspan and column width`
`   local nColumns = #columns`
`   local nOptionalColumns = nColumns - 3`
`   local titleColumnWidth`
`   if nColumns >= 5 then`
`       titleColumnWidth = 40`
`   elseif nColumns >= 4 then`
`       titleColumnWidth = 60`
`   else`
`       titleColumnWidth = 100`
`   end`
`   local optionalColumnWidth = (100 - titleColumnWidth) / nOptionalColumns`
`   titleColumnWidth = titleColumnWidth .. '%'`
`   optionalColumnWidth = optionalColumnWidth .. '%'`

`   -- Root of the output`
`   local root = mw.html.create()`

`   -- Intro`
`   root:node(self:makeIntro())`

`   -- Start of track listing table`
`   local tableRoot = root:tag('table')`
`   tableRoot`
`       :addClass('tracklist')`
`       :css('display', 'block')`
`       :css('border-spacing', '0px')`
`       `
`   -- Header row`
`   if self.headline then`
`       tableRoot:tag('caption')`
`           :addClass('tlheader mbox-text')`
`           :attr('colspan', nColumns)`
`           :css('text-align', 'left')`
`           :css('background-color', '#fff')`
`           :css('font-weight', '700')`
`           :wikitext(self.headline or '곡 목록')`
`   end`
`   `
`   -- Deprecated collapsed parameter`
`   if self.collapsed or localArgs["숨김"] == '예' or localArgs["숨김"] == 'yes'`
`   or localArgs["collapsed"] == '예' or localArgs["collapsed"] == 'yes'`
`   then`
`       self:addWarning("구식 숨김 변수를 사용 중", COLLAPSED_PARAMETER_CATEGORY);`
`   end`

`   -- Headers`
`   local headerRow = tableRoot:tag('tr')`

`   ---- Track number`
`   headerRow`
`       :tag('th')`
`           :addClass('tlheader')`
`           :attr('scope', 'col')`
`           :css('width', '2em')`
`           :css('padding-left', '10px')`
`           :css('padding-right', '10px')`
`           :css('text-align', 'right')`
`           :css('background-color', '#eee')`
`           :tag('abbr')`
`               :attr('title', '번호')`
`               :wikitext('#')`

`   ---- Title`
`   headerRow:tag('th')`
`       :addClass('tlheader')`
`       :attr('scope', 'col')`
`       :css('width', self.title_width or titleColumnWidth)`
`       :css('text-align', 'left')`
`       :css('background-color', '#eee')`
`       :wikitext('제목')`

`   ---- Optional headers: writer, lyrics, music, and extra`
`   local function addOptionalHeader(field, headerText, width)`
`       if self.optionalColumns[field] then`
`           headerRow:tag('th')`
`               :addClass('tlheader')`
`               :attr('scope', 'col')`
`               :css('width', width or optionalColumnWidth)`
`               :css('text-align', 'left')`
`               :css('background-color', '#eee')`
`               :wikitext(headerText)`
`       end`
`   end`
`   addOptionalHeader('writer', '작사·작곡', self.writing_width)`
`   addOptionalHeader('lyrics', '작사', self.lyrics_width)`
`   addOptionalHeader('music', '작곡', self.music_width)`
`   addOptionalHeader(`
`       'extra',`
`       self.extra_column or '``',`
`       self.extra_width`
`   )`

`   ---- Track length`
`   headerRow:tag('th')`
`       :addClass('tlheader')`
`       :attr('scope', 'col')`
`       :css('width', '4em')`
`       :css('padding-right', '10px')`
`       :css('text-align', 'right')`
`       :css('background-color', '#eee')`
`       :css('white-space', 'nowrap') -- '재생 시간'이 잘리지 않도록 수정`
`       :wikitext('재생 시간')`

`   -- Tracks`
`   for i, track in ipairs(self.tracks) do`
`       tableRoot:node(track:exportRow({`
`           columns = columns,`
`           color = i % 2 == 0 and '#f7f7f7' or '#fff'`
`       }))`
`   end`

`   -- Total length`
`   if self.total_length then`
`       tableRoot`
`           :tag('tr')`
`               :tag('td')`
`                   :attr('colspan', nColumns - 1)`
`                   :css('padding', 0)`
`                   :tag('span')`
`                       :css('width', '7.5em')`
`                       :css('float', 'right')`
`                       :css('padding-left', '10px')`
`                       :css('background-color', '#eee')`
`                       :css('margin-right', '2px')`
`                       :wikitext("`**`총``   ``재생``   ``시간:`**`")`
`                       :done()`
`                   :done()`
`               :tag('td')`
`                   :css('padding', '0 10px 0 0')`
`                   :css('text-align', 'right')`
`                   :css('background-color', '#eee')`
`                   :wikitext(string.format("`**`%s`**`", self.total_length))`
`   end`
`   `
`   -- Warnings and tracking categories`
`   root:wikitext(self:renderWarnings())`
`   root:wikitext(self:renderTrackingCategories())`

`   return tostring(root)`

end

-----

\-- Exports

-----

local p = {}

function p._main(args)

`   -- 로컬 변수 보관을 위해 사용`
`   localArgs = args`

`   -- Process numerical args so that we can iterate through them.`
`   local data, tracks = {}, {}`
`   for k, v in pairs(args) do`
`       if type(k) == 'string' then`
`           local prefix, num = k:match('^(%D.-)(%d+)$')`
`           prefix = translateFields(prefix)`
`           if prefix and Track.fields[prefix] and (num == '0' or num:sub(1, 1) ~= '0') then`
`               -- Allow numbers like 0, 1, 2 ..., but not 00, 01, 02...,`
`               -- 000, 001, 002... etc.`
`               num = tonumber(num)`
`               tracks[num] = tracks[num] or {}`
`               tracks[num][prefix] = v`
`           else`
`               data[translateFields(k)] = v`
`           end`
`       end`
`   end`
`   data.tracks = (function (t)`
`       -- Compress sparse array`
`       local ret = {}`
`       for num, trackData in pairs(t) do`
`           trackData.number = num`
`           table.insert(ret, trackData) `
`       end`
`       table.sort(ret, function (t1, t2)`
`           return t1.number < t2.number`
`       end)`
`       return ret`
`   end)(tracks)`

`   return tostring(TrackListing.new(data))`

end

function p.main(frame)

`   local args = require('Module:Arguments').getArgs(frame, {`
`       wrappers = '틀:곡 목록'`
`   })`
`   return p._main(args)`

end

return p