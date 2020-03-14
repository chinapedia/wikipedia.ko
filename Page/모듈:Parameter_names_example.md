> This article is converted from Wikipedia: [:Parameter names example](https://ko.wikipedia.org/wiki/:Parameter_names_example).


\-- 이 모듈은 를 실행시킵니다.

local p = {}

local function makeParam(s)

`   local lb = '{'`
`   local rb = '}'`
`   return lb:rep(3) .. s .. rb:rep(3)`

end

local function italicize(s)

`   return "`*`"``   ``..``   ``s``   ``..``   ``"`*`"`

end

local function plain(s)

`   return s`

end

function p._main(args, frame)

`   -- Find how we want to format the arguments to the template.`
`   local formatFunc`
`   if args._display == 'italics' or args._display == 'italic' then`
`       formatFunc = italicize`
`   elseif args._display == 'plain' then`
`       formatFunc = plain`
`   else`
`       formatFunc = makeParam`
`   end`

`   -- Build the table of template arguments.`
`   local targs = {}`
`   for k, v in pairs(args) do`
`       if type(k) == 'number' then`
`           targs[v] = formatFunc(v)`
`       elseif not k:find('^_') then`
`           targs[k] = v`
`       end`
`   end`

`   -- Find the template name.`
`   local template`
`   if args._template then`
`       template = args._template`
`   else`
`       local currentTitle = mw.title.getCurrentTitle()`
`       if currentTitle.prefixedText:find('/sandbox$') then`
`           template = currentTitle.prefixedText`
`       else`
`           template = currentTitle.basePageTitle.prefixedText`
`       end`
`   end`

`   -- Call the template with the arguments.`
`   frame = frame or mw.getCurrentFrame()`
`   local success, result = pcall(`
`       frame.expandTemplate,`
`       frame,`
`       {title = template, args = targs}`
`   )`
`   if success then`
`       return result`
`   else`
`       return ''`
`   end`

end

function p.main(frame)

`   local args = require('모듈:Arguments').getArgs(frame, {`
`       wrappers = '틀:변수 이름 미리보기'`
`   })`
`   return p._main(args, frame)`

end

return p