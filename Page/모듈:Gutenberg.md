> This article is converted from Wikipedia: [모듈:Gutenberg](https://ko.wikipedia.org/wiki/모듈:Gutenberg).


local p = {}

function p.author(frame)

` local pframe = frame:getParent()`
` local args = pframe.args`

` local tname = "구텐베르크 저자"                                 -- name of calling template. Change if template is renamed.`

` local id       = nil                                             -- author name, or number. Name goes to search page, number goes direct to author page `
` local name     = nil                                             -- display name on Wikipedia (default: article title)`
` local url      = nil`
` local tagline  = "- `[`프로젝트``   ``구텐베르크`](../Page/프로젝트_구텐베르크.md "wikilink")`"`
` local urlheadname  = "`<https://www.gutenberg.org/author/>`"          `
` local urlheadnumb  = "`<https://www.gutenberg.org/ebooks/author/>`" `
` local urlhead  = nil`

` -- Argument |id=`
` id = trimArg(args[1]) or trimArg(args.id)`
` if not id then`
`   error("id 변수가 없습니다. `[`틀:"``   ``..``   ``tname``   ``..``   ``"`](https://ko.wikipedia.org/wiki/틀:"_.._tname_.._" "wikilink")` 설명문서를 참고하십시오")`
` else`
`   if tonumber(id) then -- it's a number`
`     urlhead = urlheadnumb`
`   else`
`     urlhead = urlheadname`
`     id = mw.ustring.gsub(id," ", "+")`
`   end`
` end `

` -- Argument |name=`
` name = trimArg(args[2]) or trimArg(args.name)`
` if not name then`
`   name = mw.title.getCurrentTitle().text:gsub('%s+%([^%(]-%)$', '') -- Current page name without the final parentheses`
` end`

` -- Argument |coda=`
` if trimArg(args.coda) then`
`   tagline = tagline .. " " .. trimArg(args.coda)`
` end`

` url = "[" .. urlhead .. id .. " " .. name .. "의 작품] " .. tagline`

` return url`

end

function p.Australia(frame)

` local pframe = frame:getParent()`
` local args = pframe.args`

` local tname = "구텐베르크 오스트레일리아"                              -- name of calling template. Change if template is renamed.`

` local id       = nil                                             -- ID. eg. `<http://gutenberg.net.au/plusfifty-n-z.html#shanks>` .. the ID = plusfifty-n-z.html#shanks`
`                                                                  -- ID is the same for linking an individual book title, or all books by the author.`
` local name     = nil                                             -- display name on Wikipedia (default: article title)`
` local author   = nil                                             -- flag if an author (default: no)`
` local url      = nil`
` local urlhead  = "`<http://gutenberg.net.au/>`"`
` local prefix   = ""`
` local tagline  = "- `[`프로젝트``   ``구텐베르크``   ``오스트레일리아`](https://ko.wikipedia.org/wiki/프로젝트_구텐베르크_오스트레일리아 "wikilink")`"`
` local italic   = "''"`

` -- Argument |id=`
` id = trimArg(args[1]) or trimArg(args.id)`
` if not id then`
`   error("id 변수가 없습니다. `[`틀:"``   ``..``   ``tname``   ``..``   ``"`](https://ko.wikipedia.org/wiki/틀:"_.._tname_.._" "wikilink")` 설명문서를 참고하십시오")`
` end `

` -- Argument |name=`
` name = trimArg(args[2]) or trimArg(args.name)`
` if not name then`
`   name = mw.title.getCurrentTitle().text:gsub('%s+%([^%(]-%)$', '') -- Current page name without the final parentheses`
` end`

` -- Argument |author=`
` author = trimArg(args.author)`
` if author then`
`   if mw.ustring.lower(author) == "yes" then`
`     prefix = "의 작품"`
`     italic = ""`
`   end`
` end`

` -- Argument |coda=`
` if trimArg(args.coda) then`
`   tagline = tagline .. " " .. trimArg(args.coda)`
` end`

` url = "[" .. urlhead .. id .. " " .. italic .. name .. italic .. prefix .. "] " .. tagline`

` return url`

end

function p.Canada(frame)

` local pframe = frame:getParent()`
` local args = pframe.args`

` local tname = "FadedPage"                                        -- name of calling template. Change if template is renamed.`

` local id       = nil                                             -- ID for author, eg. `<http://fadedpage.com/csearch.php?author=Shortt%2C%20Adam>` .. the id = Shortt, Adam`
`                                                                  -- ID for book titles, eg. `<http://fadedpage.com/showbook.php?pid=20160704>` .. the id = 20160704`
` local name     = nil                                             -- display name on Wikipedia (default: article title)`
` local author   = nil                                             -- flag if an author (default: no)`
` local url      = nil`
` local urlhead  = "`<https://fadedpage.com/>`"`
` local urlbook  = "showbook.php?pid="`
` local urlauth  = "csearch.php?author="`
` local prefix   = ""`
` local tagline  = "- `[`Faded``   ``Page`](https://ko.wikipedia.org/wiki/Distributed_Proofreaders_Canada "wikilink")` (캐나다)"`
` local italic   = "''"`

` -- Argument |id=`
` id = trimArg(args[1]) or trimArg(args.id)`
` if not id then`
`   error("id 변수가 없습니다. `[`틀:"``   ``..``   ``tname``   ``..``   ``"`](https://ko.wikipedia.org/wiki/틀:"_.._tname_.._" "wikilink")` 설명문서를 참고하십시오")`
` end `

` -- Argument |name=`
` name = trimArg(args[2]) or trimArg(args.name)`
` if not name then`
`   name = mw.title.getCurrentTitle().text:gsub('%s+%([^%(]-%)$', '') -- Current page name without the final parentheses`
` end`

` -- Argument |author=`
` author = trimArg(args.author)`
` if author then`
`   if mw.ustring.lower(author) == "yes" then`
`     id = mw.uri.encode( id, "PATH" )                                -- handle spaces within id argument string`
`     prefix = "의 작품"`
`     italic = ""`
`     url = "[" .. urlhead .. urlauth .. id .. " " .. italic .. name .. italic .. prefix .. "] " .. tagline`
`     return url`
`   end`
` end`

` url = "[" .. urlhead .. urlbook .. id .. " " .. italic .. name .. italic .. "의 작품] " .. tagline`

` return url`

end

function trimArg(arg)

` if arg == "" or arg == nil then`
`   return nil`
` else`
`   return mw.text.trim(arg)`
` end`

end

return p