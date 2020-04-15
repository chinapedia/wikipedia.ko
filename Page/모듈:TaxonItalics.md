> This article is converted from Wikipedia: [모듈:TaxonItalics](https://ko.wikipedia.org/wiki/모듈:TaxonItalics).


\--[========================================================================= Italicize a taxon name appropriately by invoking italicizeTaxonName. The algorithm used is: \* If the name has italic markup at the start or the end, do nothing. \* Else \* Remove (internal) italic markup. \* If the name is made up of four words and the third word is a botanical connecting term, de-italicize the connecting term and add italic markup to the outside of the name. \* Else if the name is made up of three words and the second word is a botanical connecting term or a variant of "cf.", de-italicize the connecting term and add italic markup to the outside of the name. \* Else just add italic markup to the outside of the name. =============================================================================](https://ko.wikipedia.org/wiki/=========================================================================_Italicize_a_taxon_name_appropriately_by_invoking_italicizeTaxonName._The_algorithm_used_is:_*_If_the_name_has_italic_markup_at_the_start_or_the_end,_do_nothing._*_Else_*_Remove_\(internal\)_italic_markup._*_If_the_name_is_made_up_of_four_words_and_the_third_word_is_a_botanical_connecting_term,_de-italicize_the_connecting_term_and_add_italic_markup_to_the_outside_of_the_name._*_Else_if_the_name_is_made_up_of_three_words_and_the_second_word_is_a_botanical_connecting_term_or_a_variant_of_"cf.",_de-italicize_the_connecting_term_and_add_italic_markup_to_the_outside_of_the_name._*_Else_just_add_italic_markup_to_the_outside_of_the_name._============================================================================= "wikilink")

local p = {}

local cTerms3 = {

`   subspecies = "subsp.",`
`   ["subsp."] = "subsp.",`
`   subsp = "subsp.",`
`   ["ssp."] = "subsp.",`
`   ssp = "subsp.",`
`   varietas = "var.",`
`   ["var."] = "var.",`
`   var = "var.",`
`   subvarietas = "subvar.",`
`   ["subvar."] = "subvar.",`
`   subvar = "subvar.",`
`   forma = "f.",`
`   ["f."] = "f.",`
`   f = "f.",`
`   subforma = "subf.",`
`   ["subf."] = "subf.",`
`   subf = "subf."`
`   }`

local cTerms2 = {

`   subgenus = "subg.",`
`   ["subg."] = "subg.",`
`   subg = "subg.",`
`   section = "sect.",`
`   ["sect."] = "sect.",`
`   ["cf."] = "cf.",`
`   cf = "cf.",`
`   ["c.f."] = "cf."`
`   }`

\--[========================================================================= Italicize a taxon name appropriately. =============================================================================](https://ko.wikipedia.org/wiki/=========================================================================_Italicize_a_taxon_name_appropriately._============================================================================= "wikilink") function p.main(frame)

`   local name = frame.args[1] or ''`
`   local linked = frame.args['linked'] == 'yes'`
`   return p.italicizeTaxonName(name, linked)`

end

function p.italicizeTaxonName(name, linked)

`   local italMarker = "''"`
`   -- trim the name and replace any use of the HTML italic tags by Wikimedia markup`
`   name = string.gsub(string.gsub(mw.text.trim(name), "`<i>`", italMarker), "`</i>`", italMarker)`
`   local result = name`
`   if name ~= '' then`
`       if string.sub(name, 1, 2) == "`*`"``   ``or``   ``string.sub(name,``   ``-2)``   ``==``   ``"`*`" then`
`           -- do nothing if the name already has italic markers at the start or end`
`       else`
`           name = string.gsub(name, "''", "") -- first remove internal italics`
`           local words = mw.text.split(name, " ", true)`
`           local deitalicized = false`
`           if #words == 4 then`
`               -- test for the third word of a four word name being a connecting term`
`               if cTerms3[words[3]] then`
`                   -- de-italicize the connecting term by adding internal italic markup`
`                   result = words[1] .. " " .. words[2] .. italMarker .. " " .. cTerms3[words[3]] .. italMarker .. " " .. words[4]`
`                   deitalicized = true`
`               end`
`           elseif #words == 3 then`
`               -- test for the second word of a three word name being a connecting term`
`               if cTerms2[words[2]] then`
`                   -- de-italicize the connecting term by adding internal italic markup`
`                   result = words[1] .. " " .. italMarker .. cTerms2[words[2]] .. italMarker .. " " .. words[3]`
`                   deitalicized = true`
`               end`
`           else`
`               -- do nothing`
`               result = name`
`           end`
`           -- add outside markup`
`           if linked then`
`               if deitalicized then`
`                   result = "`[`"``   ``..``   ``italMarker``   ``..``   ``result``   ``..``   ``italMarker``   ``..``   ``"`](https://ko.wikipedia.org/wiki/"_.._name_.._" "wikilink")`"`
`               else`
`                   result = italMarker .. "`[`"``   ``..``   ``name``   ``..``   ``"`](https://ko.wikipedia.org/wiki/"_.._name_.._" "wikilink")`" .. italMarker`
`               end`
`           else`
`               result = italMarker .. result .. italMarker`
`           end`
`       end`
`   end`
`   return result`

end

return p