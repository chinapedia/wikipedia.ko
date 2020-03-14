> This article is converted from Wikipedia: [:Footnotes](https://ko.wikipedia.org/wiki/:Footnotes).


f = {

`   args_default = {`
`       bracket_left = "",`
`       bracket_right = "",`
`       bracket_year_left = "",`
`       bracket_year_right = "",`
`       postscript = "",`
`       page = "",`
`       pages = "",`
`       location = "",`
`       page_sep = ", p. ",`
`       pages_sep = ", pp. ",`
`       ref = "",`
`       P1 = "",`
`       P2 = "",`
`       P3 = "",`
`       P4 = "",`
`       P5 = ""`
`   }`

};

function trim( str )

`   if str == nil then`
`       return nil;`
`   end`
`   return str:match( "^%s*(.-)%s*$");`

end

function core( args )

`   local result;`

`   if args.P5 ~= "" then`
`       result = args.P1 .. ' 외. ' .. args.bracket_year_left .. args.P5 .. `
`       args.bracket_year_right;`
`   elseif args.P4 ~= "" then`
`       result = args.P1 .. ', ' .. args.P2 .. ' & ' .. args.P3 .. ' ' .. `
`       args.bracket_year_left .. args.P4 .. args.bracket_year_right;`
`   elseif args.P3 ~= "" then`
`       result = args.P1 .. ' & ' .. args.P2 .. ' ' .. args.bracket_year_left .. `
`       args.P3 .. args.bracket_year_right;`
`   else`
`       result = trim( args.P1 .. ' ' .. args.bracket_year_left .. args.P2 .. `
`       args.bracket_year_right )`
`   end`

`   if args.ref ~= 'none' then`
`       if args.ref ~= "" then`
`           result = "`[`"``   ``..``   ``result``   ``..``   ``"`](https://ko.wikipedia.org/wiki/#"_.._mw.uri.anchorEncode\(args.ref\)_.._" "wikilink")`";`
`       else`
`           result = "`[`"``   ``..``   ``result``   ``..``   ``"`](https://ko.wikipedia.org/wiki/#CITEREF"_.._mw.uri.anchorEncode\(args.P1_.._args.P2_.._args.P3_.._args.P4_.._args.P5\)_.._" "wikilink")`";`
`       end`
`   end`

`   if args.page ~= "" then`
`       result = result .. args.page_sep .. args.page;`
`   elseif args.pages ~= "" then`
`       result = result .. args.pages_sep .. args.pages;`
`   end      `

`   if args.location ~= "" then`
`       result = result .. ", " .. args.location;`
`   end`

`   result = args.bracket_left .. result .. args.bracket_right .. args.postscript;`
`   return result;`

end

function f.harvard_core( frame )

`   local args = {};`
`   local pframe = frame:getParent();`

`   args.bracket_left = pframe.args.BracketLeft or "";`
`   args.bracket_right = pframe.args.BracketRight or "";`
`   args.bracket_year_left = pframe.args.BracketYearLeft or "";`
`   args.bracket_year_right = pframe.args.BracketYearRight or "";`
`   args.postscript = pframe.args.Postscript or "";`
`   if 'none' == args.postscript then`
`       args.postscript = '';`
`   end`

`   args.page = pframe.args.Page or "";`
`   args.pages = pframe.args.Pages or "";`
`   args.location = pframe.args.Location or "";`
`   args.page_sep = pframe.args.PageSep or "";`
`   args.pages_sep = pframe.args.PagesSep or "";`
`   args.ref = pframe.args.REF or "``";`
`   args.P1 = trim( pframe.args.P1 ) or "";`
`   args.P2 = trim( pframe.args.P2 ) or "";`
`   args.P3 = trim( pframe.args.P3 ) or "";`
`   args.P4 = trim( pframe.args.P4 ) or "";`
`   args.P5 = trim( pframe.args.P5 ) or "";`

`   return core( args );`

end

function f.harvard_citation( frame )

`   local args = f.args_default;`
`   pframe = frame:getParent();`

`   args.bracket_left = "(";`
`   args.bracket_right = ")";`
`   args.page = pframe.args.p or pframe.args.page or "";`
`   args.pages = pframe.args.pp or pframe.args.pages or "";`
`   args.location = pframe.args.loc or "";`
`   args.ref = pframe.args.ref or pframe.args.Ref or "";`
`   args.P1 = trim( pframe.args[1] ) or "";`
`   args.P2 = trim( pframe.args[2] ) or "";`
`   args.P3 = trim( pframe.args[3] ) or "";`
`   args.P4 = trim( pframe.args[4] ) or "";`
`   args.P5 = trim( pframe.args[5] ) or "";`

`   return core( args );`

end

function f.harvard_citation_no_bracket( frame )

`   local args = f.args_default;`
`   pframe = frame:getParent();`

`   args.page = pframe.args.p or pframe.args.page or "";`
`   args.pages = pframe.args.pp or pframe.args.pages or "";`
`   args.location = pframe.args.loc or "";`
`   args.ref = pframe.args.ref or pframe.args.Ref or "";`
`   args.P1 = trim( pframe.args[1] ) or "";`
`   args.P2 = trim( pframe.args[2] ) or "";`
`   args.P3 = trim( pframe.args[3] ) or "";`
`   args.P4 = trim( pframe.args[4] ) or "";`
`   args.P5 = trim( pframe.args[5] ) or "";`

`   return core( args );`

end

function f.sfn( frame )

`   local args = f.args_default;`
`   for k, v in pairs( frame.args ) do                                          -- for ``, override default with values provided in the #invoke:`
`       args[k] = v;       `
`   end`
`   `
`   pframe = frame:getParent();`

`   args.postscript = pframe.args.postscript or pframe.args.ps or ".";`
`   if 'none' == args.postscript then`
`       args.postscript = '';`
`   end`
`   args.page = pframe.args.p or pframe.args.page or "";`
`   args.pages = pframe.args.pp or pframe.args.pages or "";`
`   args.location = pframe.args.loc or "";`
`   args.ref = pframe.args.ref or pframe.args.Ref or "";`
`   args.P1 = trim( pframe.args[1] ) or "";`
`   args.P2 = trim( pframe.args[2] ) or "";`
`   args.P3 = trim( pframe.args[3] ) or "";`
`   args.P4 = trim( pframe.args[4] ) or "";`
`   args.P5 = trim( pframe.args[5] ) or "";`

`   local result = core( args );`
`   local name = "FOOTNOTE" .. args.P1 .. args.P2 .. `
`   args.P3 .. args.P4 .. args.P5 .. args.page .. args.pages .. args.location;`

`   result = frame:extensionTag{ name = "ref", args = {name=name}, content=result };`

`   return result;`

end

return f;