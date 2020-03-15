> This article is converted from Wikipedia: [:Submit an edit request](https://ko.wikipedia.org/wiki/:Submit_an_edit_request).


\-- This module implements .

local CONFIG_MODULE = 'Module:Submit an edit request/config'

\-- Load necessary modules local mRedirect = require('Module:Redirect') local cfg = mw.loadData(CONFIG_MODULE) local effectiveProtectionLevel = require('Module:Effective protection level')._main local lang = mw.language.getContentLanguage()

local p = {}

local validLevels = {

`   semi = 'semi',`
`   extended = 'extended',`
`   template = 'template',`
`   full = 'full'`

}

local function message(key, ...)

`   local params = {...}`
`   local msg = cfg[key]`
`   if #params < 1 then`
`       return msg`
`   else`
`       return mw.message.newRawMessage(msg):params(params):plain()`
`   end`

end

local function isTranscludedOnMainPage(titleObj)

`   local mainPage = message('main-page')`
`   for i, source in ipairs(titleObj.cascadingProtection.sources) do`
`       if source == mainPage then`
`           return true`
`       end`
`   end`
`   return false`

end

local function validateLevel(level)

`   return level and validLevels[level] or 'full'`

end

local function getLevelInfo(level, field)

`   return cfg.protectionLevels[level][field]`

end

local function resolveRedirect(page)

`   return mRedirect.luaMain(page)`

end

local function isProtected(page)

`   local action = mw.title.new(page).exists and 'edit' or 'create'`
`   return effectiveProtectionLevel(action, page) ~= '*'`

end

function p.makeRequestUrl(level, titleObj)

`   titleObj = titleObj or mw.title.getCurrentTitle()`
`   if isTranscludedOnMainPage(titleObj) then`
`       return tostring(mw.uri.fullUrl(message('main-page-request-page')))`
`   end`
`   local talkPageName = resolveRedirect(titleObj.talkPageTitle.prefixedText)`
`   if isProtected(talkPageName) then`
`       return tostring(mw.uri.fullUrl(message('protected-talk-page-request-page')))`
`   end`
`   level = validateLevel(level)`
`   local url = mw.uri.fullUrl(talkPageName, {`
`       action = 'edit',`
`       editintro = getLevelInfo(level, 'editintro'),`
`       preload = message('preload-template'),`
`       preloadtitle = message(`
`           'preload-title-text',`
`           getLevelInfo(level, 'levelText'),`
`           lang:formatDate(message('preload-title-date-format'))`
`       ),`
`       section = 'new'`
`   })`
`   url = tostring(url)`

`   -- Add the preload parameters. @TODO: merge this into the mw.uri.fullUrl`
`   -- query table once `[`phab:T93059`](https://ko.wikipedia.org/wiki/phab:T93059 "wikilink")` is fixed.`
`   local function encodeParam(key, val)`
`       return string.format('&%s=%s', mw.uri.encode(key), mw.uri.encode(val))`
`   end`
`   url = url .. encodeParam('preloadparams[]', getLevelInfo(level, 'requestTemplate'))`
`   url = url .. encodeParam('preloadparams[]', titleObj.prefixedText)`

`   return url`

end

function p._link(args)

`   return string.format(`
`       '`<span class="plainlinks">`[%s %s]`</span>`',`
`       p.makeRequestUrl(args.type),`
`       args.display or message('default-display-value')`
`   )`

end

function p._button(args)

`   return require('Module:Clickable button 2').luaMain{`
`       [1] = args.display or message('default-display-value'),`
`       url = p.makeRequestUrl(args.type),`
`       class = 'mw-ui-progressive'`
`   }`

end

local function makeInvokeFunc(func, wrapper)

`   return function (frame)`
`       local args = require('Module:Arguments').getArgs(frame, {`
`           wrappers = {wrapper}`
`       })`
`       return func(args)`
`   end`

end

p.link = makeInvokeFunc(p._link, message('link-wrapper-template')) p.button = makeInvokeFunc(p._button, message('button-wrapper-template'))

return p