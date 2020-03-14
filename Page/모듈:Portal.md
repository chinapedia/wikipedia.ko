> This article is converted from Wikipedia: [:Portal](https://ko.wikipedia.org/wiki/:Portal).


\--\[==\[ This module is a Lua implementation of the old  template. As of August 2013 it is used on nearly 5,000,000 articles. -- Please take care when updating it\! It outputs two functions: p.portal, which generates a table of portals, and p.image, which -- produces the image name for an individual portal.

\-- The portal image data is kept in submodules of [Module:Portal/그림](https://ko.wikipedia.org/wiki/Module:Portal/그림 "wikilink"), listed below: -- [Module:Portal/그림/가](https://ko.wikipedia.org/wiki/Module:Portal/그림/가 "wikilink") - for portal names beginning with "가"\~"끼". -- ... -- [Module:Portal/그림/하](https://ko.wikipedia.org/wiki/Module:Portal/그림/하 "wikilink") - for portal names beginning with "하"\~"히". -- [Module:Portal/그림/기타](https://ko.wikipedia.org/wiki/Module:Portal/그림/기타 "wikilink") - for portal names beginning with any other letters. This includes numbers, -- letters with diacritics, and letters in non-Latin alphabets. -- [Module:Portal/그림/별칭](https://ko.wikipedia.org/wiki/Module:Portal/그림/별칭 "wikilink") - for adding aliases for existing portal names. Use this page for variations -- in spelling and diacritics, etc., no matter what letter the portal begins with. -- -- The images data pages are separated by the first letter to reduce server load when images are added, changed, or removed. -- Previously all the images were on one data page at [Module:Portal/images](https://ko.wikipedia.org/wiki/Module:Portal/images "wikilink"), but this had the disadvantage that all -- 5,000,000 pages using this module needed to be refreshed every time an image was added or removed. \]==\]

local p = {}

local function firstLetterClass(s)

`   local firstLetter = mw.ustring.sub(s, 1, 1)`

`   if firstLetter == nil then return nil end`

`   if firstLetter >= '가' and firstLetter <= '힣' then`
`       local codepoint = mw.ustring.codepoint(firstLetter)`
`       local class = (codepoint - 0xAC00) / 588`
`       return mw.ustring.sub('가가나다다라마바바사사아자자차카타파하', class+1, class+1)`
`   end`

`   return nil`

end

local function matchImagePage(s)

`   -- Finds the appropriate image subpage given a lower-case`
`   -- portal name plus the first letter of that portal name.`
`   if type(s) ~= 'string' or #s < 1 then return end`
`   local firstLetter = firstLetterClass(s)`
`   local imagePage`
`   if firstLetter then`
`       imagePage = 'Module:Portal/그림/' .. firstLetter`
`   else`
`       imagePage = 'Module:Portal/그림/기타'`
`   end`
`   return mw.loadData(imagePage)[s]`

end

local function getAlias(s)

`   -- Gets an alias from the image alias data page.`
`   local aliasData = mw.loadData('Module:Portal/그림/별칭')`
`   for portal, aliases in pairs(aliasData) do`
`       for _, alias in ipairs(aliases) do`
`           if alias == s then`
`               return portal`
`           end`
`       end`
`   end`

end

local function getImageName(s)

`   -- Gets the image name for a given string.`
`   if type(s) ~= 'string' or #s < 1 then`
`       return 'Portal-puzzle.svg'`
`   end`
`   s = mw.ustring.lower(s)`
`   return matchImagePage(s) or matchImagePage(getAlias(s)) or 'Portal-puzzle.svg'`

end

function p._portal(portals, args)

`   -- This function builds the portal box used by the `` template.`
`   local root = mw.html.create('div')`
`       :addClass('noprint portal')`
`       :addClass(args.left and 'tleft' or 'tright')`
`       :css('border', 'solid #aaa 1px')`
`       :css('margin', args.margin or (args.left == 'yes' and '0.5em 1em 0.5em 0') or '0.5em 0 0.5em 1em')`
`       :newline()`

`   -- Start the table. This corresponds to the start of the wikitext table in the old `[`Template:Portal`](https://ko.wikipedia.org/wiki/Template:Portal "wikilink")`.`
`   local tableroot = root:tag('table')`
`       :css('background', '#f9f9f9')`
`       :css('font-size', '85%')`
`       :css('line-height', '110%')`
`       :css('max-width', '175px')`
`       :css('width', type(args.boxsize) == 'string' and (args.boxsize .. 'px') or nil)`

`   -- If no portals have been specified, display an error and add the page to a tracking category.`
`   if not portals[1] then`
`       tableroot:wikitext('`<strong class="error">`No portals specified: please specify at least one portal`</strong>[`분류:변수없이``   ``사용된``   ``포털``   ``틀`](https://ko.wikipedia.org/wiki/분류:변수없이_사용된_포털_틀 "wikilink")`')`
`   end`

`   -- Display the portals specified in the positional arguments.`
`   for _, portal in ipairs(portals) do`
`       local image = getImageName(portal)`

`       -- Generate the html for the image and the portal name.`
`       tableroot`
`           :newline()`
`           :tag('tr')`
`               :css('vertical-align', 'middle')`
`               :tag('td')`
`                   :css('text-align', 'center')`
`                   :wikitext(string.format('`[`%s`](https://ko.wikipedia.org/wiki/File:%s "fig:%s")`', image))`
`                   :done()`
`               :tag('td')`
`                   :css('padding', '0 0.2em')`
`                   :css('vertical-align', 'middle')`
`                   :css('font-weight', 'bold')`
`                   :css( 'white-space', 'nowrap' )`
`                   :wikitext(string.format('`[`%s%s포털`](https://ko.wikipedia.org/wiki/포털:%s "wikilink")`', portal, portal, args['break'] and '`
`' or ' '))`
`   end`
`   return tostring(root)`

end

function p._image(portals)

`   -- Wrapper function to allow getImageName() to be accessed through #invoke.`
`   return getImageName(portals[1])`

end

local function getAllImageTables()

`   -- Returns an array containing all image subpages (minus aliases) as loaded by mw.loadData.`
`   local images = {}`
`   for i, subpage in ipairs{'가', '나', '다', '라', '마', '바', '사', '아', '자', '차', '카', '타', '파', '하', '기타'} do`
`       images[i] = mw.loadData('Module:Portal/그림/' .. subpage)`
`   end`
`   return images`

end

function p._displayAll(portals, args)

`   -- This function displays all portals that have portal images. This function is for maintenance purposes and should not be used in`
`   -- articles, for two reasons: 1) there are over 1500 portals with portal images, and 2) the module doesn't record how the portal`
`   -- names are capitalized, so the portal links may be broken.`
`   local lang = mw.language.getContentLanguage()`
`   local count = 1`
`   for _, imageTable in ipairs(getAllImageTables()) do`
`       for portal in pairs(imageTable) do`
`           portals[count] = lang:ucfirst(portal)`
`           count = count + 1`
`       end`
`   end`
`   return p._portal(portals, args)`

end

function p._imageDupes()

`   -- This function searches the image subpages to find duplicate images. If duplicate images exist, it is not necessarily a bad thing,`
`   -- as different portals might just happen to choose the same image. However, this function is helpful in identifying images that`
`   -- should be moved to a portal alias for ease of maintenance.`
`   local exists, dupes = {}, {}`
`   for _, imageTable in ipairs(getAllImageTables()) do`
`       for portal, image in pairs(imageTable) do`
`           if not exists[image] then`
`               exists[image] = portal`
`           else`
`               table.insert(dupes, string.format('The image "`[`%s`](https://ko.wikipedia.org/wiki/:File:%s "wikilink")`" is used for both portals "%s" and "%s".', image, image, exists[image], portal))`
`           end`
`       end`
`   end`
`   if #dupes < 1 then`
`       return 'No duplicate images found.'`
`   else`
`       return 'The following duplicate images were found:\n* ' .. table.concat(dupes, '\n* ')`
`   end`

end

local function processPortalArgs(args)

`   -- This function processes a table of arguments and returns two tables: an array of portal names for processing by ipairs, and a table of`
`   -- the named arguments that specify style options, etc. We need to use ipairs because we want to list all the portals in the order`
`   -- they were passed to the template, but we also want to be able to deal with positional arguments passed explicitly, for example`
`   -- ``. The behaviour of ipairs is undefined if nil values are present, so we need to make sure they are all removed.`
`   args = type(args) == 'table' and args or {}`
`   local portals = {}`
`   local namedArgs = {}`
`   for k, v in pairs(args) do`
`       if type(k) == 'number' and type(v) == 'string' then -- Make sure we have no non-string portal names.`
`           table.insert(portals, k)`
`       elseif type(k) ~= 'number' then`
`           namedArgs[k] = v`
`       end`
`   end`
`   table.sort(portals)`
`   for i, v in ipairs(portals) do`
`       portals[i] = args[v]`
`   end`
`   return portals, namedArgs`

end

local function makeWrapper(funcName)

`   -- Processes external arguments and sends them to the other functions.`
`   return function (frame)`
`       -- If called via #invoke, use the args passed into the invoking`
`       -- template, or the args passed to #invoke if any exist. Otherwise`
`       -- assume args are being passed directly in from the debug console`
`       -- or from another Lua module.`
`       local origArgs`
`       if type(frame.getParent) == 'function' then`
`           origArgs = frame:getParent().args`
`           for k, v in pairs(frame.args) do`
`               origArgs = frame.args`
`               break`
`           end`
`       else`
`           origArgs = frame`
`       end`
`       -- Trim whitespace and remove blank arguments.`
`       local args = {}`
`       for k, v in pairs(origArgs) do`
`           if type(v) == 'string' then`
`               v = mw.text.trim(v)`
`           end`
`           if v ~= '' then`
`               args[k] = v`
`           end`
`       end`
`       return p[funcName](processPortalArgs(args)) -- passes two tables to func: an array of portal names, and a table of named arguments.`
`   end`

end

for _, funcName in ipairs{'portal', 'image', 'imageDupes', 'displayAll'} do

`   p[funcName] = makeWrapper('_' .. funcName)`

end

return p