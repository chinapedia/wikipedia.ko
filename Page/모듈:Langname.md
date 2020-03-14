> This article is converted from Wikipedia: [:Langname](https://ko.wikipedia.org/wiki/:Langname).


\--[This module provides a language name handling operations based on ISO 639 and Unicode CLDR information. - ChongDae](https://ko.wikipedia.org/wiki/This_module_provides_a_language_name_handling_operations_based_on_ISO_639_and_Unicode_CLDR_information._-_ChongDae "wikilink")

local lang = {}

local langdata = mw.loadData('Module:Langname/data') local lang_name = langdata.lang_name local lang_autonym = langdata.lang_autonym local lang_article = langdata.lang_article local lang_wikipedia = langdata.lang_wikipedia

\--[-- Helper functions --](https://ko.wikipedia.org/wiki/--_Helper_functions_-- "wikilink") local function getCldrName(code)

`   local name = mw.language.fetchLanguageName(code, 'ko')`

`   if name == '' then`
`       return nil`
`   elseif string.match(name, '[(),A-Za-z]') then       -- 이름에 영문자나 괄호, 쉼표가 들어간 경우는 오류 처리함.`
`       return nil`
`   else`
`       return name`
`   end`

end

function getCldrAutonym(code)

`   local lang = string.match(code, '([a-z]+)') -- get 'en' from 'en-us'`

`   return lang_autonym[code] or mw.language.fetchLanguageName(code, lang)`

end

local function getLanguageName(code)

`   return lang_name[code] or getCldrName(code)`

end

function lang.name(frame)

`   local code = string.lower(frame.args.code)`
`   `
`   return getLanguageName(code) or '언어 오류(' .. code .. ')'`

end

function lang.autonym(frame)

`   local code = string.lower(frame.args.code)`

`   return getCldrAutonym(code) or '언어 오류(' .. code .. ')'`

end

function lang.article(frame)

`   local code = string.lower(frame.args.code)`
`   `
`   return lang_article[code] or getLanguageName(code) or '언어 오류'`

end

function lang.wikipedia(frame)

`   local code = string.lower(frame.args.code)`
`   `
`   return lang_wikipedia[code] or getLanguageName(code) or '언어 오류(' .. code .. ')'`

end

function lang.link(frame)

`   local code = string.lower(frame.args.code)`
`   local link = frame.args.link`
`   local article = lang_article[code]`
`   local name = getLanguageName(code)`

`   if link == 'no' then`
`       return name or '`[`언어``   ``오류('``   ``..``   ``code``   ``..``   ``')`](https://ko.wikipedia.org/wiki/언어_오류 "wikilink")`'`
`   elseif article then`
`       return '`[`'``   ``..``   ``name``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._article_.._' "wikilink")`'`
`   elseif name then`
`       return '`[`'``   ``..``   ``name``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._name_.._' "wikilink")`'`
`   else`
`       return '`[`언어``   ``오류('``   ``..``   ``code``   ``..``   ``')`](https://ko.wikipedia.org/wiki/언어_오류 "wikilink")`'`
`   end`

end

return lang