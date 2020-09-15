> This article is converted from Wikipedia: [모듈:Iucn](https://ko.wikipedia.org/wiki/모듈:Iucn).


require('Module:No globals');

local p = {}

local data = { -- these data entries will ultimately go in data subpage or series of data subpages \*\*NOT USED\*\*

`   iucn = {`
`       ['_template'] = "저널 인용", -- use cite journal`
`       ['_exclude'] = "amended, url" ,  -- do not pass these to `
`               --_alias-map: associate ``-specific parameter names with cs1|2-standard parameter names`
`       ['_alias-map'] =  "assessors : authors, vassessors : vauthors, assessor# : last#, assessor#-link : author#-link,assessor-link# : author-link#, assessorlink# : authorlink#, assessor#-mask : author#-mask, assessor-mask# : author-mask#, assessormask# : authormask#, display-assessors : display-authors, displayassessors : displayauthors, last-assessor-amp : last-author-amp, lastassessoramp : lastauthoramp, assessment_year : year, taxon : title, downloaded : access-date"`
`   }`

}

local function getArgs (frame, args)

`   local parents = mw.getCurrentFrame():getParent()`

`   for k,v in pairs(parents.args) do`

`       --aliases`
`       if type(k) == 'string' then`
`           k = k:gsub("assessor","author")  -- convert assessor parameters to author parameters`
`               :gsub("taxon", "title")`
`               :gsub("downloaded","access-date")`
`       end`

`       --check content`
`       if v and v ~= "" then`
`           args[k]=v --parents.args[k]`
`       end`
`   end`

end

\--\[\[--------------------------\< I U C N _ I D E N T I F I E R S _ G E T \>--------------------------------------

cs1|2 templates cite single sources; when the identifiers in |doi=, |id=, and |page= are different from each other then the template is attempting to cite multiple sources. This function evaluates the identifier portions of these parameters. returns seven values: identifyier parts (or nil when parameter not used) and a message (nil on success, error message else)

the identifier portions of the several parameters must be properly formed

\]\]

local function iucn_identifiers_get (args)

`   local doi_taxon_ID, doi_assesment_ID`
`   local page_taxon_ID, page_assesment_ID`
`   local id_taxon_ID, id_assesment_ID`
`   local url_taxon_ID, url_assesment_ID`
`   local msg`
`   `
`   if args.doi then`
`       doi_taxon_ID, doi_assesment_ID = args.doi:match ('T(%d+)A(%d+)%.en$')`
`       if not doi_taxon_ID then`
`           msg = 'malformed |doi= identifier'`
`       end`
`   end`
`   if args.page then`
`       page_taxon_ID, page_assesment_ID = args.page:match ('^e%.T(%d+)A(%d+)$')`
`       if not page_taxon_ID then`
`           msg = 'malformed |page= identifier'`
`       end`
`   end`
`   if args.id then`
`       id_taxon_ID, id_assesment_ID = args.id:match ('^(%d+)/(%d+)$')`
`       if not id_taxon_ID then`
`           msg = 'malformed |id= identifier'`
`       end`
`   end`
`   if args.url then`
`       if args.url:match ('`<https://www.iucnredlist.org/species/>`') then         -- must be a 'new-form' url`
`           url_taxon_ID, url_assesment_ID = args.url:match ('/species/(%d+)/(%d+)')`
`           if not url_taxon_ID then`
`               msg = 'malformed |url= identifier'`
`           end`
`       end`
`   end`

`   if not msg then`
`       if doi_taxon_ID and page_taxon_ID then`
`           if not (doi_taxon_ID == page_taxon_ID and doi_assesment_ID == page_assesment_ID) then`
`               msg = '|doi= / |page= mismatch'`
`           end`
`       end`
`       if doi_taxon_ID and id_taxon_ID then`
`           if not (doi_taxon_ID == id_taxon_ID and doi_assesment_ID == id_assesment_ID) then`
`               msg = '|doi= / |id= mismatch'`
`           end`
`       end`
`       if doi_taxon_ID and url_taxon_ID then`
`           if not (doi_taxon_ID == url_taxon_ID and doi_assesment_ID == url_assesment_ID) then`
`               msg = '|doi= / |url= mismatch'`
`           end`
`       end`
`       `
`       if page_taxon_ID and id_taxon_ID then`
`           if not (page_taxon_ID == id_taxon_ID and page_assesment_ID == id_assesment_ID) then`
`               msg = '|page= / |id= mismatch'`
`           end`
`       end`
`       if page_taxon_ID and url_taxon_ID then`
`           if not (page_taxon_ID == url_taxon_ID and page_assesment_ID == url_assesment_ID) then`
`               msg = '|page= / |url= mismatch'`
`           end`
`       end`

`       if id_taxon_ID and url_taxon_ID then`
`           if not (id_taxon_ID == url_taxon_ID and id_assesment_ID == url_assesment_ID) then`
`               msg = '|id= / |url= mismatch'`
`           end`
`       end`
`   end`

`   if msg then`
`       msg = '`<span class="error" style="font-size:100%">`: error: ' .. msg .. ' (`[`도움말`](https://ko.wikipedia.org/wiki/틀:Cite_iucn "wikilink")`)`</span>`'`
`   end`
`   `
`   return doi_taxon_ID, doi_assesment_ID, page_taxon_ID, page_assesment_ID, id_taxon_ID, id_assesment_ID, msg`

end

\--\[\[--------------------------\< I U C N _ V O L U M E _ C H E C K \>--------------------------------------------

compares volume in |volume= (if present) against year in |date= or |year= (if present) against volume in |doi= (if present)

returns nil if all that are present are correct; message else

\]\]

local function iucn_volume_check (args)

`   local vol = args.volume;`
`   local date = args.date or args.year;`
`   local doi = args.doi and args.doi:match ('IUCN%.UK%.(%d%d%d%d)')`
`   local msg`
`   `
`   if vol and date then`
`       msg = (vol ~= date) and '|volume= / |date= mismatch' or msg`
`   end`
`   if vol and doi then`
`       msg = (vol ~= doi) and '|volume= / |doi= mismatch' or msg`
`   end`
`   if date and doi then`
`       msg = (doi ~= date) and '|date= / |doi= mismatch' or msg`
`   end`
`   `
`   return msg`

end

\--\[\[ function p.cite() - function wrapping

`    takes cite journal parameters but updates old style url using electronic page number`
`    page should be in format e.T13922A45199653`
`    the url uses                13922/45199653`
`    so we need to extract the number between T and A and the number after A`
`    the target url is `<https://www.iucnredlist.org/species/13922/45199653>
`    usage: {{#invoke:iucn|cite}}`
`    template: `

\--\]\] function p.cite(frame)

`   local error_msgs = {};                                                      -- holds error messages for rendering`
`   local maint_msgs = {};                                                      -- holds hidden maint messages for rendering`
`   local namespace = mw.title.getCurrentTitle().namespace;                     -- used for categorization`
`   local templateArgs = {}                                                     -- local copy of template arguments`
`   `
`   getArgs (frame, templateArgs)                                               -- fetch template arguments`

`   local missing_title = not templateArgs.title                                -- special case that results from script writing `` template from bare iucn url`
`                                                                               -- don't duplicate cs1|2 error message; don't duplicate `` error cat`

`   local doi_taxon_ID, doi_assesment_ID                                        -- all of these contain the same identifying info in slightly`
`   local page_taxon_ID, page_assesment_ID                                      -- different forms. when any combination of these is present,`
`   local id_taxon_ID, id_assesment_ID                                          -- they must all agree`
`   local msg                                                                   -- this holds error messages; nil on success`

`   doi_taxon_ID, doi_assesment_ID, page_taxon_ID, page_assesment_ID, id_taxon_ID, id_assesment_ID, msg = iucn_identifiers_get (templateArgs);`
`   if msg then`
`       table.insert (error_msgs, msg);                                         -- malformed or mismatched identifiers`
`   end`
`   templateArgs['id'] = nil                                                    -- unset; no longer needed if it was set`

`   local url_taxon_ID = page_taxon_ID or id_taxon_ID or doi_taxon_ID;          -- select for use in url that we will create`
`   local url_assesment_ID = page_assesment_ID or id_assesment_ID or doi_assesment_ID`
`   `
`   local url = templateArgs.url`
`   if url then`
`       if url:find ('iucnredlist.org/details/', 1, true) then                  -- old-form url`
`           if url_taxon_ID then                                                -- when there is an identifier`
`               url = nil                                                       -- unset; we'll create new url below`
`           else                                                                -- here when old-form but no identifier that we can use to create new url`
`               templateArgs.url = templateArgs.url:gsub ("http:", "https:")    -- sometimes works with redirect on iucn site`
`           end`
`           table.insert (maint_msgs, 'old-form url')                           -- announce that this template has has an old-form url`
`       elseif url:find ('iucnredlist.org/species/', 1, true) then              -- new-form url`

\-- table.insert (maint_msgs, 'new-form url') --TODO: restore this line when most new-form urls have been removed from article space -- announce that this template has has an new-form url

`       else`
`           table.insert (maint_msgs, 'unknown url')                            -- announce that this template has has some sort of url we don't recognize`
`       end`
`   end`

`   if not url then                                                             -- when no url or unset old-form url`
`       if url_taxon_ID then`
`           templateArgs.url = "`<https://www.iucnredlist.org/species/>`" .. url_taxon_ID .. '/' .. url_assesment_ID`
`       else`
`           table.insert (maint_msgs, 'no identifier')                          -- TODO: raise this to  error status?`
`       end`
`   end`

`   -- add journal if not provided (TODO decide if this should override provided value)`
`   if not templateArgs['journal'] and not templateArgs['work'] then`
`       templateArgs['journal'] = "`[`IUCN``   ``적색``   ``목록`](../Page/IUCN_적색_목록.md "wikilink")`"`
`   end`

`   templateArgs.publisher = '`[`IUCN`](https://ko.wikipedia.org/wiki/IUCN "wikilink")`'                                            -- do this here so the templates don't have to`
`   `
`   msg = iucn_volume_check (templateArgs);                                     -- |volume=, |year= (|date=), |doi= must all refer to the same volume`
`   if msg then`
`       table.insert (maint_msgs, msg);`
`   end`

`   if not templateArgs.volume and (templateArgs.year or templateArgs.date) then`
`       templateArgs.volume = templateArgs.year or templateArgs.date`
`   end`
`                                                                               -- add free-to-read icon to mark a correctly formed doi`
`   templateArgs['doi-access'] = templateArgs.doi and templateArgs.doi:match ('10%.2305/IUCN.+T%d+A%d+%.en') and 'free' or nil`
`       `
`   return frame:expandTemplate{ title = '저널 인용', args = templateArgs } ..                  -- the template`
`       (((0 == #error_msgs) and missing_title) and (' ') or '') ..        -- special case to not duplicate cs1|2 err msg or cite iucn error cat`
`       ((0 < #error_msgs) and table.concat (error_msgs, ', ') or '') ..                            -- the error messages`
`       (((0 < #error_msgs) and (0 == namespace)) and (' ') or '') ..  -- error category when in mainspace`
`       ((0 < #maint_msgs) and ('`<span class="citation-comment" style="display: none; color: #33aa33; margin-left: 0.3em;">`' .. table.concat (maint_msgs, ', ') .. '`</span>`') or '') .. -- the maint messages`
`       (((0 < #maint_msgs) and (0 == namespace)) and (' ') or '')       -- maint category when in mainspace`

end

\-- version using template wrapper for cite journal function p.cite2(frame)

`   -- now use wrapper template`

`   --[[this doesn't work`
`   frame.args['_alias-map'] =  "assessors : authors, vassessors : vauthors, assessor# : last#, assessor#-link : author#-link,assessor-link# : author-link#, assessorlink# : authorlink#, assessor#-mask : author#-mask, assessor-mask# : author-mask#, assessormask# : authormask#, display-assessors : display-authors, displayassessors : displayauthors, last-assessor-amp : last-author-amp, lastassessoramp : lastauthoramp, assessment_year : year, taxon : title, downloaded : access-date"`
`   frame.args['_template'] = "cite journal"`
`   but the following does ]]`

`   local wrapperArgs ={}`
`   wrapperArgs['_template'] = "저널 인용"`
`   --|_exclude=id, version, new, IUCN_Year, iucn_year, criteria-version `
`   wrapperArgs['_exclude'] = "amended, url" -- exclude url (from parent) as we wanted updated version`
`   --|_alias-map= `
`   wrapperArgs['_alias-map'] =  "assessors : authors, vassessors : vauthors, assessor# : last#, assessor#-link : author#-link,assessor-link# : author-link#, assessorlink# : authorlink#, assessor#-mask : author#-mask, assessor-mask# : author-mask#, assessormask# : authormask#, display-assessors : display-authors, displayassessors : displayauthors, last-assessor-amp : last-author-amp, lastassessoramp : lastauthoramp, assessment_year : year, taxon : title, downloaded : access-date"`

`   local templateArgs = {}   -- need a copy to alter and pass to citation template`
`   getArgs (frame, templateArgs)`

`   --we only want to make changes if there is old-style url, i.e. one containing "/details/"`
`   local url = templateArgs['url'] or ""`
`   local replace = string.find( url, "details" , 1, true)    -- replace url if contains "details"`
`   if url == "" and templateArgs['page'] then replace = true end -- if no url and page number available,`

`   if replace  then`
`       local page = templateArgs['page'] or ""`
`       local speciesID = string.match( page, "T(%d+)A" )`
`       local speciesAssessment = string.match( page, "A(%d+)" )`
`       if speciesID  and speciesAssessment then -- set new style url`
`           wrapperArgs['url'] = "`<https://www.iucnredlist.org/species/>`" .. speciesID .. '/' .. speciesAssessment`
`       end`
`   else`
`       wrapperArgs['url']=templateArgs['url']`
`   end`
`   if url == "" and templateArgs['id'] then -- use oldstyle url`
`       wrapperArgs['url'] = "`<http://oldredlist.iucnredlist.org/details/>`" .. templateArgs['id']`
`       wrapperArgs['journal'] = '`[`IUCN``   ``Red``   ``List``   ``of``   ``Threatened``   ``Species`](https://ko.wikipedia.org/wiki/IUCN_Red_List_of_Threatened_Species "wikilink")`'`
`       wrapperArgs['volume'] = 'Version ' .. templateArgs['version']`
`   end`
`   if templateArgs['amended'] then wrapperArgs['trans-title']=templateArgs['amended'] end -- use translated title parameter to add amended text, e.g. "amended version of 2016 assessment", which will be added in square brackets after title`
`   --wrapperArgs['trans-title'] = templateArgs['trans-title']`

`   frame.args=wrapperArgs --set the wrapper arguments`

`   local wrapper = require("Module:Template wrapper")`

`   --local xframe = frame --mw.clone(frame)  --mw.getCurrentFrame()`
`   --frame.args.metatable['_template'] = "cite journal"`
`   --local parents = xframe:getParent() --mw.getCurrentFrame():getParent()`
`   --parents.args['_template'] = "cite journal"`

`   --mw.logObject(frame)`
`   --return  mw.dumpObject(wrapperArgs)`
`   return wrapper.wrap(frame)`

end --[main}} --](https://ko.wikipedia.org/wiki/function_to_replace_iucn_templates_test_template:_Template:IUCN/sandbox/lua_usage:_{{#invoke:iucn "wikilink") function p.main(frame)

`   local templateArgs = {}   -- need a copy to alter and pass to citation template`
`   getArgs (frame, templateArgs)`

\-- local parents = mw.getCurrentFrame():getParent()

`   local reference = ""`
`   local taxon =templateArgs['title']  -- now aliased`

`   reference = '``'`

`   return frame:preprocess(reference)`
`   --return reference`

end

return p