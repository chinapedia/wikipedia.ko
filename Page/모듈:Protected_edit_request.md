> This article is converted from Wikipedia: [모듈:Protected edit request](https://ko.wikipedia.org/wiki/모듈:Protected_edit_request).


require('Module:No globals')

local yesno = require('Module:Yesno') local makeMessageBox = require('Module:Message box').main local getArgs

local activeBox -- lazily initialized if we get an active request

-----

\-- Box class definition

-----

local box = {} box.__index = box

function box.new(protectionType, args)

`   local obj = {}`
`   setmetatable(obj, box)`
`   obj.tmboxArgs = {} -- Used to store arguments to be passed to tmbox by the box:export method.`
`   -- Set data fields.`
`   obj.tmboxArgs.attrs = { ['data-origlevel'] = protectionType }`
`   return obj`

end

function box:setArg(key, value)

`   -- This sets a value to be passed to tmbox.`
`   if key then`
`       self.tmboxArgs[key] = value`
`   end`

end

function box:export()

`   if not mw.title.getCurrentTitle().isTalkPage and not self.demo then`
`       return '`<span class="error">`오류: 보호 편집 요청은 토론 문서에서만 할 수 있습니다.`</span>`'`
`   end`
`   self:setArg('smalltext', "`**`이``   `[`편집``   ``요청은`](https://ko.wikipedia.org/wiki/:분류:보호_편집_요청 "wikilink")`   ``검토되었습니다.`**` 요청을 재활성화하려면 |처리= 변수를 지워주세요.")`
`   self:setArg('small', true)`
`   self:setArg('class', 'editrequest')`
`   return makeMessageBox('tmbox', self.tmboxArgs)`

end

-----

\-- Process arguments and initialise objects

-----

local p = {}

function p._main(protectionType, args)

`   local boxType = box`
`   -- if not yesno(args.answered or args.ans, true) then`
`   if args["처리"] == '예' then`
`       if not activeBox then`
`           activeBox = require('Module:Protected edit request/active')(box, yesno, makeMessageBox)`
`       end`
`       boxType = activeBox`
`   end`
`   local requestBox = boxType.new(protectionType, args)`
`   return requestBox:export()`

end

local mt = {}

function mt.__index(t, k)

`   if not getArgs then`
`       getArgs = require('Module:Arguments').getArgs`
`   end`
`   return function (frame)`
`       return t._main(k, getArgs(frame, {wrappers = {'틀:보호 편집 요청', '틀:준보호 편집 요청', '틀:틀 보호 편집 요청', '틀:장기 보호 편집 요청', '틀:인터페이스 보호 편집 요청'}}))`
`   end`

end

return setmetatable(p, mt)