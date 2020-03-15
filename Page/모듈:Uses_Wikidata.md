> This article is converted from Wikipedia: [:Uses Wikidata](https://ko.wikipedia.org/wiki/:Uses_Wikidata).


local p = {}

function p.usesProperty(frame)

`   local args = frame.getParent(frame).args or nil`
`   if mw.text.trim(args[1] or '') == '' then`
`       args = frame.args`
`   end`
`   local result = ''`
`   local ii = 1`
`   while true do`
`       local p_num = mw.text.trim(args[ii] or '')`
`       if p_num ~= '' then`
`           local label = mw.wikibase.label(p_num) or "NO LABEL"`
`           result = result .. "`

  - [middle](https://ko.wikipedia.org/wiki/파일:Disc_Plain_blue_dark.svg "wikilink") <b>[" .. label .. " <small>(" .. string.upper(p_num) .. ")</small>](https://ko.wikipedia.org/wiki/d:Property:"_.._p_num_.._" "wikilink")</b>
    (<span class='plainlinks'>\[<https://query.wikidata.org/embed.html#SELECT%20%3FWikiData_item_%20%3FWikiData_item_Label%20%3Fvalue%20%3FvalueLabel%20%3FKorean_WikiPedia_article%20%23Show%20data%20in%20this%20order%0A%7B%0A%09%3FWikiData_item_%20wdt%3A>" .. p_num .. "%20%3Fvalue%20.%20%23Collecting%20all%20items%20which%20have%20" .. p_num .. "%20data%2C%20from%20whole%20WikiData%20item%20pages%0A%09OPTIONAL%20%7B%3FKorean_WikiPedia_article%20schema%3Aabout%20%3FWikiData_item_%3B%20schema%3AisPartOf%20%3Chttps%3A%2F%2Fko.wikipedia.org%2F%3E%20.%7D%20%23If%20collected%20item%20has%20link%20to%20Korean%20WikiPedia%2C%20show%20that%0A%09SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22ko%22%20%20%7D%20%23Show%20label%20in%20this%20language.%20%22ko%22%20is%20Korean.%20%20%20%0A%7D%0ALIMIT%201000 사용 현황\]</span>)

"

`           ii = ii + 1`
`       else break`
`       end`
`   end`
`   return result`

end

return p