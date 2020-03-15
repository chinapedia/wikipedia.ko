> This article is converted from Wikipedia: [:IPAc-en](https://ko.wikipedia.org/wiki/:IPAc-en).


\-- 이 모듈은 [틀:IPAc-en](https://ko.wikipedia.org/wiki/틀:IPAc-en "wikilink")을 구현합니다.

local data = mw.loadData('Module:IPAc-en/data') local p = {}

\-- Global container for tracking categories local categories = {}

\-- Trims whitespace from a string local function trim(s)

`   return s:match('^%s*(.-)%s*$')`

end

\-- This implements [Template:Nowrap](https://ko.wikipedia.org/wiki/Template:Nowrap "wikilink"). local function makeNowrapSpan(s)

`   local span = mw.html.create('span')`
`       :addClass('nowrap')`
`       :wikitext(s)`
`   return tostring(span)`

end

local function makePronunciationText(id)

`   id = id and string.lower(trim(id))`
`   if id and id ~= '' and data.pronunciation[id] then`
`       return data.pronunciation[id].text`
`   end`

end

local function getFilepath(file)

`   return mw.getCurrentFrame():callParserFunction('filepath', file)`

end

local function makeAudioLink(file)

`   categories["Articles including recorded pronunciations"] = true`
`   local span = mw.html.create('span')`
`   span`
`       :addClass('noexcerpt')`
`       :wikitext(string.format(`
`           '`[`Speakerlink-new.svg`](https://ko.wikipedia.org/wiki/File:Speakerlink-new.svg "fig:Speakerlink-new.svg")`',`
`           getFilepath(file)`
`       ))`
`       :tag('sup')`
`           :tag('span')`
`               :css('color', '#00e')`
`               :css('font', 'bold 80% sans-serif')`
`               :css('padding', '0 .1em')`
`               :addClass('IPA')`
`               :wikitext(string.format('`[`i`](https://ko.wikipedia.org/wiki/:File:%s "wikilink")`', file))`
`   return tostring(span)`

end

\-- This adds a tooltip icon to a label. It implements [Template:H:title](https://ko.wikipedia.org/wiki/Template:H:title "wikilink"). local function makeTooltip(label, tooltip)

`   local span = mw.html.create('span')`
`       :attr('title', tooltip)`
`       :wikitext(label)`
`   return tostring(span)`

end

local function formatPhonemeGroup(phonemes)

`   if #phonemes > 0 then`
`       local span = mw.html.create('span')`
`           :css('border-bottom', '1px dotted')`
`           :wikitext(table.concat(phonemes))`
`       return tostring(span)`
`   else`
`       return ''`
`   end`

end

local function renderCategories()

`   local ret = {}`
`   for cat in pairs(categories) do`
`       table.insert(ret, string.format('', cat))`
`   end`
`   table.sort(ret)`
`   return table.concat(ret)`

end

function p._main(args)

`   local ret = {}`
`   local i = 0 -- Keeps track of numbered args`

`   -- Pronunciation`
`   do`
`       local pron = {}`
`       while true do`
`           i = i + 1`
`           local pronItem = makePronunciationText(args[i])`
`           if pronItem then`
`               pron[#pron + 1] = pronItem`
`               pron[#pron + 1] = ' '`
`           else`
`               break`
`           end`
`       end`
`       if #pron > 0 then`
`           ret[#ret + 1] = string.format(`
`               '`<small>`%s`</small>`',`
`               table.concat(pron)`
`           )`
`       end`
`   end`

`   -- Audio link`
`   do`
`       local file = args.audio and trim(args.audio)`
`       if file and file ~= '' then`
`           ret[#ret + 1] = makeAudioLink(file)`
`       end`
`   end`

`   -- Phonemes`
`   do`
`       -- Loop through the numbered args, separating them into phoneme groups`
`       -- and separator strings (both called "words" for convenience). We only`
`       -- underline the phoneme groups, not the separators.`
`       local words = {}`
`       words[#words + 1] = '/' -- Opening slash`
`       i = i - 1 -- Set up i again as it was changed in the pronunciation loop`
`       local id`
`       repeat`
`           local phonemes = {}`
`           local isWordEnd = false`
`           while not isWordEnd do`
`               i = i + 1`
`               id = args[i]`
`               id = id and trim(id)`
`               if not id then`
`                   isWordEnd = true`
`                   words[#words + 1] = formatPhonemeGroup(phonemes)`
`               elseif id ~= '' then`
`                   local t = data.phonemes[id]`
`                   if not t then`
`                       -- We were passed an invalid id.`
`                       isWordEnd = true`
`                       categories["Ill-formatted IPAc-en transclusions"] = true`
`                       words[#words + 1] = formatPhonemeGroup(phonemes)`
`                       words[#words + 1] = makeTooltip(`
`                           "`**`[unsupported``   ``input]`**`",`
`                           'Unrecognized symbol'`
`                       )`
`                   elseif not t.label then`
`                       -- The data module contains bad data, so throw an error.`
`                       error(string.format(`
`                           "no label was found for id '%s'",`
`                           tostring(id)`
`                       ))`
`                   elseif t.tooltip then`
`                       -- We are dealing with a regular phoneme.`
`                       phonemes[#phonemes + 1] = makeTooltip(`
`                           t.label,`
`                           t.tooltip`
`                       )`
`                   else`
`                       -- We are dealing with a separator.`
`                       isWordEnd = true`
`                       words[#words + 1] = formatPhonemeGroup(phonemes)`
`                       words[#words + 1] = t.label                     `
`                   end`
`               end`
`           end`
`       until not id`
`       words[#words + 1] = '/' -- Closing slash`

`       -- Wrap the words in a link to IPA help.`
`       local span = mw.html.create('span')`
`           :addClass('IPA nopopups')`
`           :wikitext(string.format(`
`               '`[`%s`](https://ko.wikipedia.org/wiki/:en:Help:IPA_for_English "wikilink")`',`
`               table.concat(words)`
`           ))`

`       ret[#ret + 1] = tostring(span)`
`   end`

`   -- Nowrap and categories`
`   ret = makeNowrapSpan(table.concat(ret)) .. renderCategories()`

`   -- Reset the categories table in case we are run again.`
`   categories = {}`

`   return ret`

end

function p.main(frame)

`   return p._main(frame:getParent().args)`

end

return p

[Category:%s](https://ko.wikipedia.org/wiki/Category:%s "wikilink")