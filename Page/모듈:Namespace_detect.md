> This article is converted from Wikipedia: [모듈:Namespace detect](https://ko.wikipedia.org/wiki/모듈:Namespace_detect).


\--[-------------------------------------------------------------------------------- -- -- -- NAMESPACE DETECT -- -- -- -- This module implements the {{namespace detect}} template in Lua, with a -- -- few improvements: all namespaces and all namespace aliases are supported, -- -- and namespace names are detected automatically for the local wiki. The -- -- module can also use the corresponding subject namespace value if it is -- -- used on a talk page. Parameter names can be configured for different wikis -- -- by altering the values in the "cfg" table in -- -- Module:Namespace detect/config. -- -- -- -------------------------------------------------------------------------------- --](https://ko.wikipedia.org/wiki/--------------------------------------------------------------------------------_--_--_--_NAMESPACE_DETECT_--_--_--_--_This_module_implements_the_{{namespace_detect}}_template_in_Lua,_with_a_--_--_few_improvements:_all_namespaces_and_all_namespace_aliases_are_supported,_--_--_and_namespace_names_are_detected_automatically_for_the_local_wiki._The_--_--_module_can_also_use_the_corresponding_subject_namespace_value_if_it_is_--_--_used_on_a_talk_page._Parameter_names_can_be_configured_for_different_wikis_--_--_by_altering_the_values_in_the_"cfg"_table_in_--_--_Module:Namespace_detect/config._--_--_--_--------------------------------------------------------------------------------_-- "wikilink")

local data = mw.loadData('Module:Namespace detect/data') local argKeys = data.argKeys local cfg = data.cfg local mappings = data.mappings

local yesno = require('Module:Yesno') local mArguments -- Lazily initialise Module:Arguments local mTableTools -- Lazily initilalise Module:TableTools local ustringLower = mw.ustring.lower

local p = {}

local function fetchValue(t1, t2)

`   -- Fetches a value from the table t1 for the first key in array t2 where`
`   -- a non-nil value of t1 exists.`
`   for i, key in ipairs(t2) do`
`       local value = t1[key]`
`       if value ~= nil then`
`           return value`
`       end`
`   end`
`   return nil`

end

local function equalsArrayValue(t, value)

`   -- Returns true if value equals a value in the array t. Otherwise`
`   -- returns false.`
`   for i, arrayValue in ipairs(t) do`
`       if value == arrayValue then`
`           return true`
`       end`
`   end`
`   return false`

end

function p.getPageObject(page)

`   -- Get the page object, passing the function through pcall in case of`
`   -- errors, e.g. being over the expensive function count limit.`
`   if page then`
`       local success, pageObject = pcall(mw.title.new, page)`
`       if success then`
`           return pageObject`
`       else`
`           return nil`
`       end`
`   else`
`       return mw.title.getCurrentTitle()`
`   end`

end

\-- Provided for backward compatibility with other modules function p.getParamMappings()

`   return mappings`

end

local function getNamespace(args)

`   -- This function gets the namespace name from the page object.`
`   local page = fetchValue(args, argKeys.demopage)`
`   if page == '' then`
`       page = nil`
`   end`
`   local demospace = fetchValue(args, argKeys.demospace)`
`   if demospace == '' then`
`       demospace = nil`
`   end`
`   local subjectns = fetchValue(args, argKeys.subjectns)`
`   local ret`
`   if demospace then`
`       -- Handle "demospace = main" properly.`
`       if equalsArrayValue(argKeys.main, ustringLower(demospace)) then`
`           ret = mw.site.namespaces[0].name`
`       else`
`           ret = demospace`
`       end`
`   else`
`       local pageObject = p.getPageObject(page)`
`       if pageObject then`
`           if pageObject.isTalkPage then`
`               -- Get the subject namespace if the option is set,`
`               -- otherwise use "talk".`
`               if yesno(subjectns) then`
`                   ret = mw.site.namespaces[pageObject.namespace].subject.name`
`               else`
`                   ret = 'talk'`
`               end`
`           else`
`               ret = pageObject.nsText`
`           end`
`       else`
`           return nil -- return nil if the page object doesn't exist.`
`       end`
`   end`
`   ret = ret:gsub('_', ' ')`
`   return ustringLower(ret)`

end

function p._main(args)

`   -- Check the parameters stored in the mappings table for any matches.`
`   local namespace = getNamespace(args) or 'other' -- "other" avoids nil table keys`
`   local params = mappings[namespace] or {}`
`   local ret = fetchValue(args, params)`
`   --`[`--``   ``If``   ``there``   ``were``   ``no``   ``matches,``   ``return``   ``parameters``   ``for``   ``other``   ``namespaces.``   ``--``   ``This``   ``happens``   ``if``   ``there``   ``was``   ``no``   ``text``   ``specified``   ``for``   ``the``   ``namespace``   ``that``   ``--``   ``was``   ``detected``   ``or``   ``if``   ``the``   ``demospace``   ``parameter``   ``is``   ``not``   ``a``   ``valid``   ``--``   ``namespace.``   ``Note``   ``that``   ``the``   ``parameter``   ``for``   ``the``   ``detected``   ``namespace``   ``must``   ``be``   ``--``   ``completely``   ``absent``   ``for``   ``this``   ``to``   ``happen,``   ``not``   ``merely``   ``blank.``   ``--`](https://ko.wikipedia.org/wiki/--_If_there_were_no_matches,_return_parameters_for_other_namespaces._--_This_happens_if_there_was_no_text_specified_for_the_namespace_that_--_was_detected_or_if_the_demospace_parameter_is_not_a_valid_--_namespace._Note_that_the_parameter_for_the_detected_namespace_must_be_--_completely_absent_for_this_to_happen,_not_merely_blank._-- "wikilink")
`   if ret == nil then`
`       ret = fetchValue(args, argKeys.other)`
`   end`
`   return ret`

end

function p.main(frame)

`   mArguments = require('Module:Arguments')`
`   local args = mArguments.getArgs(frame, {removeBlanks = false})`
`   local ret = p._main(args)`
`   return ret or ''`

end

function p.table(frame)

`   --`[`--``   ``Create``   ``a``   ``wikitable``   ``of``   ``all``   ``subject``   ``namespace``   ``parameters,``   ``for``   ``--``   ``documentation``   ``purposes.``   ``The``   ``talk``   ``parameter``   ``is``   ``optional,``   ``in``   ``case``   ``it``   ``--``   ``needs``   ``to``   ``be``   ``excluded``   ``in``   ``the``   ``documentation.``   ``--`](https://ko.wikipedia.org/wiki/--_Create_a_wikitable_of_all_subject_namespace_parameters,_for_--_documentation_purposes._The_talk_parameter_is_optional,_in_case_it_--_needs_to_be_excluded_in_the_documentation._-- "wikilink")
`   `
`   -- Load modules and initialise variables.`
`   mTableTools = require('Module:TableTools')`
`   local namespaces = mw.site.namespaces`
`   local cfg = data.cfg`
`   local useTalk = type(frame) == 'table' `
`       and type(frame.args) == 'table' `
`       and yesno(frame.args.talk) -- Whether to use the talk parameter.`
`   `
`   -- Get the header names.`
`   local function checkValue(value, default)`
`       if type(value) == 'string' then`
`           return value`
`       else`
`           return default`
`       end`
`   end`
`   local nsHeader = checkValue(cfg.wikitableNamespaceHeader, 'Namespace')`
`   local aliasesHeader = checkValue(cfg.wikitableAliasesHeader, 'Aliases')`

`   -- Put the namespaces in order.`
`   local mappingsOrdered = {}`
`   for nsname, params in pairs(mappings) do`
`       if useTalk or nsname ~= 'talk' then`
`           local nsid = namespaces[nsname].id`
`           -- Add 1, as the array must start with 1; nsid 0 would be lost otherwise.`
`           nsid = nsid + 1 `
`           mappingsOrdered[nsid] = params`
`       end`
`   end`
`   mappingsOrdered = mTableTools.compressSparseArray(mappingsOrdered)`

`   -- Build the table.`
`   local ret = '{| class="wikitable"'`
`       .. '\n|-'`
`       .. '\n! ' .. nsHeader`
`       .. '\n! ' .. aliasesHeader`
`   for i, params in ipairs(mappingsOrdered) do`
`       for j, param in ipairs(params) do`
`           if j == 1 then`
`               ret = ret .. '\n|-'`
`                   .. '\n| ' .. param .. ''`
`                   .. '\n| '`
`           elseif j == 2 then`
`               ret = ret .. '' .. param .. ''`
`           else`
`               ret = ret .. ', ' .. param .. ''`
`           end`
`       end`
`   end`
`   ret = ret .. '\n|-'`
`       .. '\n|}'`
`   return ret`

end

return p