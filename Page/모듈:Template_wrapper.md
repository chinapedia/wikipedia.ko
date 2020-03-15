> This article is converted from Wikipedia: [:Template wrapper](https://ko.wikipedia.org/wiki/:Template_wrapper).


require('Module:No globals');

local error_msg = '<span style=\"font-size:100%\" class=\"error\">\<code style=\\"color:inherit; border:inherit; padding:inherit;\\"\>|_template=</code> missing or empty</span>';

\--[--------------------------\< I S _ I N _ T A B L E \>-------------------------------------------------------- scan through tbl looking for value; return true if found, false else](https://ko.wikipedia.org/wiki/--------------------------\<_I_S_I_N_T_A_B_L_E_\>--------------------------------------------------------_scan_through_tbl_looking_for_value;_return_true_if_found,_false_else "wikilink")

local function is_in_table (tbl, value)

`   for k, v in pairs (tbl) do`
`       if v == value then return true end`
`   end`
`   return false;`

end

\--[--------------------------\< A D D _ P A R A M E T E R \>---------------------------------------------------- adds parameter name and its value to args table according to the state of boolean list argument; kv pair for template execution; k=v string for template listing.](https://ko.wikipedia.org/wiki/--------------------------\<_A_D_D_P_A_R_A_M_E_T_E_R_\>----------------------------------------------------_adds_parameter_name_and_its_value_to_args_table_according_to_the_state_of_boolean_list_argument;_kv_pair_for_template_execution;_k=v_string_for_template_listing. "wikilink")

local function add_parameter (k, v, args, list)

`   if list then`
`       table.insert( args, table.concat ({k, '=', v}));                        -- write parameter names and values to args table as string`
`   else`
`       args[k] = v;                                                            -- copy parameters to args table`
`   end`

end

\--\[\[--------------------------\< F R A M E _ A R G S _ G E T \>--------------------------------------------------

Fetch the wrapper template's 'default' and control parameters; adds default parameters to args

returns content of |_template= parameter (name of the working template); nil else

\]\]

local function frame_args_get (frame_args, args, list)

`   local template;`

`   for k, v in pairs (frame_args) do                                           -- here we get the wrapper template's 'default' parameters`
`       if 'string' == type (k) and (v and ('' ~= v)) then                      -- do not pass along positional or empty parameters`
`           if '_template' == k then`
`               template = v;                                                   -- save the name of template that we are wrapping`
`           elseif '_exclude' ~= k and '_include-positional' ~= k then          -- these already handled so ignore here; `
`               add_parameter (k, v, args, list);                               -- add all other parameters to args in the style dictated by list`
`           end`
`       end`
`   end`

`   return template;                                                            -- return contents of |_template= parameter`

end

\--[--------------------------\< P F R A M E _ A R G S _ G E T \>------------------------------------------------ Fetches the wrapper template's 'live' parameters; adds live parameters that aren't members of the exclude table to args table; positional parameters may not be excluded no return value](https://ko.wikipedia.org/wiki/--------------------------\<_P_F_R_A_M_E_A_R_G_S_G_E_T_\>------------------------------------------------_Fetches_the_wrapper_template's_'live'_parameters;_adds_live_parameters_that_aren't_members_of_the_exclude_table_to_args_table;_positional_parameters_may_not_be_excluded_no_return_value "wikilink")

local function pframe_args_get (pframe_args, args, exclude, _include_positional, list)

`   for k, v in pairs (pframe_args) do`
`       if 'string' == type (k) and not is_in_table (exclude, k) then           -- do not pass along excluded parameters`
`           if v and ('' ~= v) then                                             -- pass along only those parameters that have assigned values`
`               if 'unset' == v:lower() then                                    -- special keyword to unset 'default' parameters set in the wrapper template`
`                   v = '';                                                     -- unset the value in the args table`
`               end`
`               add_parameter (k, v, args, list)                                -- add all other parameters to args in the style dictated by list`
`           end`
`       end`
`   end`

`   if _include_positional then`
`       for i, v in ipairs (pframe_args) do                                     -- pass along positional parameters`
`           if 'unset' == v:lower() then                                        -- special keyword to unset 'default' parameters set in the wrapper template`
`               v = '';                                                         -- unset the value in the args table`
`           end`
`           add_parameter (i, v, args, list);`
`       end`
`   end`

end

\--[--------------------------\< _ M A I N \>-------------------------------------------------------------------- Collect the various default and live parameters into args styled according to boolean list. returns name of the working or listed template or nil for an error message](https://ko.wikipedia.org/wiki/--------------------------\<_M_A_I_N_\>--------------------------------------------------------------------_Collect_the_various_default_and_live_parameters_into_args_styled_according_to_boolean_list._returns_name_of_the_working_or_listed_template_or_nil_for_an_error_message "wikilink")

local function _main (frame, args, list)

`   local template;`
`   local exclude = {};                                                         -- table of parameter names for parameters that are not passed to the working template`
`   local _include_positional;`
`   `
`   if frame.args._exclude and ('' ~= frame.args._exclude) then                 -- if there is |_exclude= and it's not empty`
`       exclude = mw.text.split (frame.args._exclude, "%s*,%s*");               -- make a table from its contents`
`   end`

`   template = frame_args_get (frame.args, args, list);                         -- get parameters provided in the {{#invoke:template wrapper|...|...}}`
`   if nil == template or '' == template then                                   -- this is the one parameter that is required by this module`
`       return nil;                                                             -- not present, tell calling function to emit an error message`
`   end`
`   `
`   _include_positional = 'yes' == frame.args['_include-positional'];           -- when true pass all positional parameters along with non-excluded named parameters to ...`
`                                                                               -- ... the working template; positional parameters are not excludable`
`                                                                               `
`   local pframe = frame:getParent();                                           -- here we get the wrapper template's 'live' parameters from pframe.args`
`   pframe_args_get (pframe.args, args, exclude, _include_positional, list);    -- add parameters and values to args that are not listed in the exclude table`

`   return template;                                                            -- args now has all default and live parameters, return working template name`

end

\--[--------------------------\< W R A P \>---------------------------------------------------------------------- Template entry point. Call this function to 'execute' the working template](https://ko.wikipedia.org/wiki/--------------------------\<_W_R_A_P_\>----------------------------------------------------------------------_Template_entry_point._Call_this_function_to_'execute'_the_working_template "wikilink")

local function wrap (frame)

`   local args = {};                                                            -- table of default and live parameters and their values to be passed to the wrapped template`
`   local template;                                                             -- the name of the working template`

`   template = _main (frame, args, false);                                      -- get default and live parameters and the name of the working template`
`   if not template then                                                        -- template name is required`
`       return error_msg;                                                       -- emit error message and abandon if template name not present`
`   end`
`   `
`   return frame:expandTemplate {title=template, args=args};                    -- render the working template`

end

\--[--------------------------\< L I S T \>---------------------------------------------------------------------- Template entry point. Call this function to 'display' the source for the working template. This function added as a result of a TfD here: Wikipedia:Templates_for_discussion/Log/2018_April_28\#Module:PassArguments This function replaces a similarly named function which was used in {{cite compare}} and {{cite compare2}} Values in the args table are numerically indexed strings in the form 'name=value'](https://ko.wikipedia.org/wiki/--------------------------\<_L_I_S_T_\>----------------------------------------------------------------------_Template_entry_point._Call_this_function_to_'display'_the_source_for_the_working_template._This_function_added_as_a_result_of_a_TfD_here:_Wikipedia:Templates_for_discussion/Log/2018_April_28#Module:PassArguments_This_function_replaces_a_similarly_named_function_which_was_used_in_{{cite_compare}}_and_{{cite_compare2}}_Values_in_the_args_table_are_numerically_indexed_strings_in_the_form_'name=value' "wikilink")

local function list (frame)

`   local args = {};                                                            -- table of default and live parameters and their values to be passed to the listed template`
`   local template;                                                             -- the name of the listed template`

`   template = _main (frame, args, true);                                       -- get default and live parameters and the name of the listed template`
`   if not template then                                                        -- template name is required`
`       return error_msg;                                                       -- emit error message and abandon if template name not present`
`   end`

`   return frame:preprocess (table.concat ({'{{', template, ' |', table.concat( args, ' |' ), '}}'}));    -- render the template`

end

\--[--------------------------\< E X P O R T E D F U N C T I O N S \>------------------------------------------](https://ko.wikipedia.org/wiki/--------------------------\<_E_X_P_O_R_T_E_D_F_U_N_C_T_I_O_N_S_\>------------------------------------------ "wikilink")

return {

`   list = list,`
`   wrap = wrap,`
`   };`