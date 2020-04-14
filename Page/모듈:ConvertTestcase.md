> This article is converted from Wikipedia: [모듈:ConvertTestcase](https://ko.wikipedia.org/wiki/모듈:ConvertTestcase).


\-- Used to compare the current version of the convert template with the sandboxlua version

local function bag()

`   -- Return a table to hold lines of text.`
`   return {`
`       n = 0,`
`       add = function (self, s)`
`           self.n = self.n + 1`
`           self[self.n] = s`
`       end,`
`       join = function (self, sep)`
`           return table.concat(self, sep or '\n')`
`       end,`
`   }`

end

local function clean(s)

`   -- 2013-04-08: Template:Convert now appends text like`
`   -- "" to its output,`
`   -- so remove that also.`
`   s = s:gsub(" ", " ")`
`   s = s:gsub(" ", " ")`
`   s = s:gsub("_", " ")`
`   s = s:gsub("—", "—")`
`   s = s:gsub("–", "–")`
`   s = s:gsub("²", "`<sup>`2`</sup>`")`
`   s = s:gsub("³", "`<sup>`3`</sup>`")`
`   s = s:lower()`
`   s = s:gsub("%[%[category:.-%]%]", "")`

`   -- convert links with descriptions the same as the link to just a link`
`   -- for example `[`acre`](https://ko.wikipedia.org/wiki/acre "wikilink")` to `[`acre`](https://ko.wikipedia.org/wiki/acre "wikilink")
`   -- and `[`acre`](https://ko.wikipedia.org/wiki/acre "wikilink")s` to `[`acre`](https://ko.wikipedia.org/wiki/acre "wikilink")s
`   s = s:gsub("%[%[([^%[%]]-)|%1]]", "`[`%1`](https://ko.wikipedia.org/wiki/%1 "wikilink")`")`
`   s = s:gsub("%[%[([^%[%]]-)|%1s]]", "`[`%1`](https://ko.wikipedia.org/wiki/%1 "wikilink")s`")`
`   return s`

end

local function nolinks(s)

`   -- Remove wikilink target to test if difference is due to a link disagreement.`
`   -- Change, for example, "`[`acre`](https://ko.wikipedia.org/wiki/acre "wikilink")`" to "acre", then "`[`ha`](https://ko.wikipedia.org/wiki/hectare "wikilink")`" to "ha".`
`   s = s:gsub("%[%[([^%[%]|]-)%]%]", "%1")`
`   return s:gsub("%[%`[`^%[%`](https://ko.wikipedia.org/wiki/^%[% "wikilink")`-|(.-)%]%]", "%1")`

end

local function nospans(s)

`   -- Remove any html spans to test if difference is due to a span disagreement.`
`   return s:gsub("`

</?span.->

", "") end

local function showconvert(args)

`   return "``"  -- 123="{", 124="|"`

end

local function statusbox(label, color, align)

`   return "| style=\"text-align:" .. align .. ";color:white;background:" .. color .. ";\" | " .. label`

end

local function statusboxlinkspan(label)

`   return "| style=\"text-align:center;color:white;background-image: -moz-linear-gradient(left, olive, teal); background-image: -ms-linear-gradient(left, olive, teal); background-image: -webkit-linear-gradient(left, olive, teal); background-image: linear-gradient(left, olive, teal);\" | " .. label`

end

local function addresults(frame, voutput, template, args, vunit, title, args2)

`   local v1 = frame:expandTemplate{ title = title or "단위 변환/old", args = args }`
`   local v2 = frame:expandTemplate{ title = "단위 변환/sandboxlua", args = args2 or args }`
`   if vunit then`
`       voutput:add("| `[`"``   ``..``   ``vunit``   ``..``   ``"`](https://ko.wikipedia.org/wiki/Template:단위_변환/"_.._vunit_.._" "wikilink")`")`
`   end`
`   voutput:add("| " .. template)`
`   voutput:add("| " .. v1)`
`   voutput:add("| " .. v2)`
`   v1 = clean(v1)`
`   v2 = clean(v2)`
`   if v1 == v2 then`
`       voutput:add(statusbox("Exact Match", "green", "center"))`
`   elseif nolinks(v1) == nolinks(v2) then`
`       voutput:add(statusbox("Link", "olive", "left"))`
`   elseif nospans(v1) == nospans(v2) then`
`       voutput:add(statusbox("Span", "teal", "right"))`
`   elseif nospans(nolinks(v1)) == nospans(nolinks(v2)) then`
`       voutput:add(statusboxlinkspan("Link & Span"))`
`   else`
`       if mw.ustring.find(v1, "template:단위 변환", 1, true ) then`
`           voutput:add(statusbox("", "white", "center"))`
`       else`
`           voutput:add(statusbox("Different", "red", "center"))`
`       end`
`   end`

end

local function onerow(frame, voutput, vunit, vunit2, vbaseunit)

`   local insert = table.insert`
`   local args = {}`
`   insert(args, "1")`
`   if vbaseunit then`
`       insert(args, vbaseunit)`
`   end`
`   insert(args, vunit)`
`   if vunit2 then`
`       insert(args, "5")`
`       insert(args, vunit2)`
`   end`
`   local template = showconvert(args)`
`   args.lk = "on"`
`   addresults(frame, voutput, template, args, vunit)`
`   voutput:add("|-")`

end

local i = {}

function i.ConvertTestcaseHeader(frame)

`   local want_unit = frame.args.unit`
`   want_unit = (want_unit == nil or want_unit == 'yes')`
`   local colspan = frame.args.colspan or ''`
`   if colspan ~= '' then`
`       colspan = " colspan=2"`
`   end`
`   local voutput = bag()`
`   voutput:add("{| class=\"wikitable\"")`
`   if want_unit then`
`       voutput:add("! style=\"text-align:left;\" | Unit")`
`   end`
`   voutput:add("! style=\"text-align:left;\" | Convert Code")`
`   voutput:add("! style=\"text-align:left;\" " .. colspan .. "| Convert (Old)")`
`   voutput:add("! style=\"text-align:left;\" " .. colspan .. "| Convert (Sandboxlua)")`
`   voutput:add("! style=\"text-align:left;\" | Result")`
`   voutput:add("|-")`
`   return voutput:join()`

end

function i.ConvertTestcaseFooter(frame)

`   return "|}\n"`

end

function i.ConvertTestcase(frame)

`   local vtype = frame.args["type"]`
`   local vtoonly = frame.args["toonly"]`
`   local vfromonly = frame.args["fromonly"]`
`   local vunit = frame.args["unit"]`
`   local vunit2 = frame.args["unit2"]`
`   local voutput = bag()`
`   local vunits = {`
`         ["acceleration"] = "m/s2",`
`         ["area"] = "m2",`
`         ["density"] = "kg/m3",`
`         ["energy"] = "kJ",`
`         ["energypermass"] = "kJ/kg",`
`         ["energypervolume"] = "kJ/l",`
`         ["energyperlength"] = "kJ/km",`
`         ["exhaustemission"] = "kg/km",`
`         ["flow"] = "m3/s",`
`         ["force"] = "N",`
`         ["fuelconsumption"] = "l/km",`
`         ["gradient"] = "m/km",`
`         ["length"] = "m",`
`         ["lineardensity"] = "kg/m",`
`         ["mass"] = "g",`
`         ["power"] = "W",`
`         ["pressure"] = "Pa",`
`         ["population-density"] = "PD/km2",`
`         ["radioactivity"] = "Ci",`
`         ["speed"] = "m/s",`
`         ["temperature"] = "C",`
`         ["temperature-change"] = "C-change",`
`         ["time"] = "s",`
`         ["torque"] = "Nm",`
`         ["volume"] = "m3"`
`   }`
`   if vtoonly ~= "yes" then`
`       onerow(frame, voutput, vunit, vunit2)`
`   end`
`   if vfromonly ~= "yes" then`
`       local vbaseunit = vunits[vtype]`
`       if vbaseunit ~= nil and vbaseunit ~= vunit then`
`           onerow(frame, voutput, vunit, vunit2, vbaseunit)`
`      end`
`   end`
`   return voutput:join()`

end

local function make_given(argstr)

`   local insert = table.insert`
`   local args, show = {}, {}`
`   argstr = argstr .. "!"`
`   for item in argstr:gmatch( "(.-)!") do`
`       local p = item:find('=', 1, true)`
`       if p then`
`           args[item:sub(1, p-1)] = item:sub(p+1)`
`       else`
`           insert(args, item)`
`       end`
`       insert(show, item)`
`   end`
`   return showconvert(show), args`

end

function i.ConvertTestcaseGiven(frame)

`   -- Return a test case row from template arguments given in the form`
`   -- "100!in!cm!abbr=on" which means "``".`
`   local given = frame.args[1]`
`   if given == nil or given == '' then`
`       return ""`
`   end`
`   local voutput = bag()`
`   local template, args = make_given(given)`
`   addresults(frame, voutput, template, args)`
`   voutput:add("|-")`
`   return voutput:join()`

end

function i.ConvertTestcaseExtra(frame)

`   -- Return a test case row from template arguments given like`
`   -- "|x=spell |1=0.5!ha!acre |2=0.5!ha!acre!spell=in" which invokes:`
`   --     `
`   --     `
`   -- or like`
`   -- "|x=3 |1=1!x!2!x!3!ft!mm |2=1!*!2!*!3!ft!mm" which invokes:`
`   --     `
`   --     `
`   local extra, lhs, rhs = frame.args.x, frame.args[1], frame.args[2]`
`   if extra == nil or extra == '' or lhs == nil or lhs == '' or rhs == nil or rhs == '' then`
`       return ""`
`   end`
`   local voutput = bag()`
`   local template1, args1 = make_given(lhs)`
`   local template2, args2 = make_given(rhs)`
`   addresults(frame, voutput, template2, args1, nil, "convert/" .. extra, args2)`
`   voutput:add("|-")`
`   return voutput:join()`

end

return i

[Category:Pages_using_Template_Convert](https://ko.wikipedia.org/wiki/Category:Pages_using_Template_Convert "wikilink")