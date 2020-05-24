> This article is converted from Wikipedia: [모듈:Infobox television season name](https://ko.wikipedia.org/wiki/모듈:Infobox_television_season_name).


local match = require("Module:String")._match

local p = {}

\--[Local function which is used to create an pipped article link. --](https://ko.wikipedia.org/wiki/Local_function_which_is_used_to_create_an_pipped_article_link._-- "wikilink") local function createArticleTitleWithPipedLink(article, pipedLink)

`   if (pipedLink == nil or pipedLink == "") then`
`       return "`[`"``   ``..``   ``article``   ``..``   ``"`](https://ko.wikipedia.org/wiki/"_.._article_.._" "wikilink")`"`
`   else`
`       return "`[`"``   ``..``   ``pipedLink``   ``..``   ``"`](https://ko.wikipedia.org/wiki/"_.._article_.._" "wikilink")`"`
`   end`

end

\--[Local helper function which is used to get the current season number and modified show name from the show name. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_get_the_current_season_number_and_modified_show_name_from_the_show_name._-- "wikilink") local function getModifiedShowNameAndCurrentSeasonNumberFromShowName(showName)

`   local _, _, showNameModified, seasonNumber = string.find(showName, "(.*)%s+(%d+)")`
`   return showNameModified, seasonNumber`

end

\--[Local helper function which is used to get the current season number from the disambiguation. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_get_the_current_season_number_from_the_disambiguation._-- "wikilink") local function getCurrentSeasonNumberFromDisambiguation(shortDisambiguation)

`   return match(shortDisambiguation , "%d+", 1, -1, false, "")`

end

\--[Local helper function which is used to get the type of word used for "season" in the disambiguation. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_get_the_type_of_word_used_for_"season"_in_the_disambiguation._-- "wikilink") local function getSeasonType(shortDisambiguation)

`   local seasonType  = string.find(shortDisambiguation , "시리즈")`
`   if (seasonType) then`
`       seasonType = "시리즈"`
`   else`
`       seasonType = "시즌"`
`   end`
`   return seasonType`

end

\--[Local helper function which is used to get the short disambiguation, without the "(년도) 텔레비전 프로그램," part, which can cause issues later on. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_get_the_short_disambiguation,_without_the_"\(년도\)_텔레비전_프로그램,"_part,_which_can_cause_issues_later_on._-- "wikilink") local function getShortDisambiguation(disambiguation)

`   return string.gsub(disambiguation, "%d+년 텔레비전 프로그램, ", "")`

end

\--[Local helper function which is used to get the disambiguation from the title. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_get_the_disambiguation_from_the_title._-- "wikilink") local function getDisambiguation(title)

`   local disambiguation = match(title, "%s%((.-)%)", 1, -1, false, "")`
`   if (disambiguation == "") then`
`       return nil`
`   else`
`       return disambiguation`
`   end`

end

\--[Local helper function which is used to get the show name from the title. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_get_the_show_name_from_the_title._-- "wikilink") local function getShowName(title)

`   return mw.ustring.gsub(title, "%s+%b()$", "")`

end

\--[Local function which is used to check if the given article exists. The function returns "true" in the following cases: -- A season article exists. -- A redirect exists to a season section. The function returns nil in the following cases: -- A season article or redirect do not exist. -- A redirect exists, but it is a general redirect and not for any specific season section.](https://ko.wikipedia.org/wiki/Local_function_which_is_used_to_check_if_the_given_article_exists._The_function_returns_"true"_in_the_following_cases:_--_A_season_article_exists._--_A_redirect_exists_to_a_season_section._The_function_returns_nil_in_the_following_cases:_--_A_season_article_or_redirect_do_not_exist._--_A_redirect_exists,_but_it_is_a_general_redirect_and_not_for_any_specific_season_section. "wikilink")-- local function checkArticle(articleTitle)

`   local article = mw.title.new(articleTitle)`
`   if (article ~= nil and article.exists) then`
`       local redirectTarget = article.redirectTarget`
`       if (redirectTarget) then`
`           local fullLink = redirectTarget.fullText`
`           local isSection = fullLink:find("#")`
`           if (isSection) then`
`               return "true"                               -- Article is a section redirect; Valid link.`
`           else`
`               return nil                                  -- Article is a general redirect; Not a valid link.`
`           end`
`       else`
`           return "true"                                   -- Article exists and is not a redirect; Valid link.`
`       end`
`   else`
`       return nil                                          -- Article or redirect do not exist; Not a valid link.`
`   end`

end

\--[Local function which returns a season article title and a piped link. The following are the supported season naming styles: -- \<showName\> (\<seasonType\> \<seasonNumber\>) Example: Lost (season 2). -- \<showName\> (\<country\> \<seasonType\> \<seasonNumber\>) Example: The Office (American season 2). Example: X Factor (British series 2). -- \<showName\> (\<country\> \<seasonType\>) Example: Big Brother 2 (American season). -- \<showName\> (\<year\> TV series, \<seasonType\> \<seasonNumber\>) Example: Teenage Mutant Ninja Turtles (1987 TV series, season 2) -- \<showName\> (\<country\> TV series, \<seasonType\> \<seasonNumber\>) Example: Love Island (British TV series, series 2) --](https://ko.wikipedia.org/wiki/Local_function_which_returns_a_season_article_title_and_a_piped_link._The_following_are_the_supported_season_naming_styles:_--_\<showName\>_\(\<seasonType\>_\<seasonNumber\>\)_Example:_Lost_\(season_2\)._--_\<showName\>_\(\<country\>_\<seasonType\>_\<seasonNumber\>\)_Example:_The_Office_\(American_season_2\)._Example:_X_Factor_\(British_series_2\)._--_\<showName\>_\(\<country\>_\<seasonType\>\)_Example:_Big_Brother_2_\(American_season\)._--_\<showName\>_\(\<year\>_TV_series,_\<seasonType\>_\<seasonNumber\>\)_Example:_Teenage_Mutant_Ninja_Turtles_\(1987_TV_series,_season_2\)_--_\<showName\>_\(\<country\>_TV_series,_\<seasonType\>_\<seasonNumber\>\)_Example:_Love_Island_\(British_TV_series,_series_2\)_-- "wikilink") local function getArticleTitle(title, prevOrNextSeasonNumber)

`   local showName = getShowName(title)`
`   local disambiguation = getDisambiguation(title)`
`   `
`   local shortDisambiguation`
`   local seasonType`
`   local seasonNumber = ""`
`   local pipedLink = ""`
`   if (disambiguation) then`
`       shortDisambiguation = getShortDisambiguation(disambiguation)`
`       seasonType = getSeasonType(shortDisambiguation)`
`       seasonNumber = getCurrentSeasonNumberFromDisambiguation(shortDisambiguation)`
`       pipedLink = seasonType:gsub("^%l", string.upper) .. " "`
`   end`

`   local showNameModified`
`   if (seasonNumber == "") then`
`       if (string.match(showName , "%s+(%d+)")) then`
`           showNameModified, seasonNumber = getModifiedShowNameAndCurrentSeasonNumberFromShowName(showName)`
`       else`
`           return "" -- Not a valid next/prev season link`
`       end`
`   end`
`   `
`   if (tonumber(seasonNumber) == nil) then`
`       return ""`
`   else`
`       seasonNumber = seasonNumber + prevOrNextSeasonNumber`
`       pipedLink = pipedLink .. seasonNumber`
`       -- Titles such as "Big Brother 1 (American season)""`
`       if (showNameModified and disambiguation) then`
`           return showNameModified .. " " .. seasonNumber .. " (" .. disambiguation  .. ")", pipedLink`

`       -- Titles such as "Big Brother Brasil 1"`
`       elseif (showNameModified) then`
`           return showNameModified .. " " .. seasonNumber, nil`
`           `
`       -- Standard titles such as "Lost (season 1)"`
`       else`
`           disambiguation = string.gsub(disambiguation, "%d+$", seasonNumber)`
`           return showName .. " (" .. disambiguation .. ")", pipedLink`
`       end`
`   end`

end

\--[Local helper function which is used to get the title, either from args (usually from /testcases) or from the page itself. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_get_the_title,_either_from_args_\(usually_from_/testcases\)_or_from_the_page_itself._-- "wikilink") local function getTitle(frame)

`   local getArgs = require('Module:Arguments').getArgs`
`   local args = getArgs(frame)`
`   local title = args.title`
`   if (not title) then`
`       title = mw.title.getCurrentTitle().text`
`   end`

`   return title`

end

\--[Local helper function which is called to create a TV season title for the next or previous season. Passes the value "1" or -1" to increment or decrement the current season number. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_called_to_create_a_TV_season_title_for_the_next_or_previous_season._Passes_the_value_"1"_or_-1"_to_increment_or_decrement_the_current_season_number._-- "wikilink") local function createArticleTitleHelper(frame, number)

`   local title = getTitle(frame)`
`   return getArticleTitle(title, number)`

end

\--[Local helper function which is used to check if a season article exists. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_check_if_a_season_article_exists._-- "wikilink") local function checkSeason(frame, number)

`   local articleTitle = createArticleTitleHelper(frame, number)`
`   return checkArticle(articleTitle)`

end

\--[Local helper function which is used to create a season article link. --](https://ko.wikipedia.org/wiki/Local_helper_function_which_is_used_to_create_a_season_article_link._-- "wikilink") local function getSeasonArticleLink(frame, number)

`   local articleTitle, pipedLink = createArticleTitleHelper(frame, number)`
`   return createArticleTitleWithPipedLink(articleTitle, pipedLink)`

end

\--[Public function which is used to check if the next season has a valid created article or redirect. --](https://ko.wikipedia.org/wiki/Public_function_which_is_used_to_check_if_the_next_season_has_a_valid_created_article_or_redirect._-- "wikilink") function p.checkNextSeason(frame)

`   return checkSeason(frame, 1)`

end

\--[Public function which is used to check if the previous season has a valid article or redirect. --](https://ko.wikipedia.org/wiki/Public_function_which_is_used_to_check_if_the_previous_season_has_a_valid_article_or_redirect._-- "wikilink") function p.checkPrevSeason(frame)

`   return checkSeason(frame, -1)`

end

\--[Public function which is used to check if the next or previous season have a valid article or redirect. Parameters: --](https://ko.wikipedia.org/wiki/Public_function_which_is_used_to_check_if_the_next_or_previous_season_have_a_valid_article_or_redirect._Parameters:_-- "wikilink") function p.checkAll(frame)

`   if (p.checkPrevSeason(frame) == "true") then`
`       return "true"`
`   else`
`       return p.checkNextSeason(frame)`
`   end`

end

\--[Public function which is used to get the next season article title. --](https://ko.wikipedia.org/wiki/Public_function_which_is_used_to_get_the_next_season_article_title._-- "wikilink") function p.getNextSeasonArticle(frame)

`   return getSeasonArticleLink(frame, 1)`

end

\--[Public function which is used to get the previous season article title. --](https://ko.wikipedia.org/wiki/Public_function_which_is_used_to_get_the_previous_season_article_title._-- "wikilink") function p.getPrevSeasonArticle(frame)

`   return getSeasonArticleLink(frame, -1)`

end

\--[Public function which is used to get the type of season word used - "season" or "series". --](https://ko.wikipedia.org/wiki/Public_function_which_is_used_to_get_the_type_of_season_word_used_-_"season"_or_"series"._-- "wikilink") function p.getSeasonWord(frame)

`   local title = getTitle(frame)`
`   local disambiguation = getDisambiguation(title)`
`   if (disambiguation) then`
`       local shortDisambiguation = getShortDisambiguation(disambiguation)`
`       return getSeasonType(shortDisambiguation)`
`   else`
`       return ""`
`   end`

end

\--[Public function which is used to return the relevant text for the sub-header field. The text is returned in the format of \<code\>Season \#\</code\> or \<code\>Series \#\</code\>, depending on either what the article disambiguation uses, or on manually entered parameters of the infobox. --](https://ko.wikipedia.org/wiki/Public_function_which_is_used_to_return_the_relevant_text_for_the_sub-header_field._The_text_is_returned_in_the_format_of_\<code\>Season_#\</code\>_or_\<code\>Series_#\</code\>,_depending_on_either_what_the_article_disambiguation_uses,_or_on_manually_entered_parameters_of_the_infobox._-- "wikilink") function p.getInfoboxSubHeader(frame)

`   local getArgs = require('Module:Arguments').getArgs`
`   local args = getArgs(frame)`

`   local title = getTitle(frame)`
`   local showName = getShowName(title)`
`   local disambiguation = getDisambiguation(title)`
`   if (not seasonNumber and disambiguation) then`
`       local shortDisambiguation = getShortDisambiguation(disambiguation)`

`       seasonType = getSeasonType(shortDisambiguation)`
`       seasonType = seasonType:sub(1, 1):upper() .. seasonType:sub(2)`
`       seasonNumber = getCurrentSeasonNumberFromDisambiguation(shortDisambiguation)`
`   end`

`   if (seasonNumber and seasonNumber ~= "") then`
`       return seasonType .. " " .. seasonNumber`
`   end`
`   `
`   return nil`

end

return p