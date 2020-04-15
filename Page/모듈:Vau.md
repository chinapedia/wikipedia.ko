> This article is converted from Wikipedia: [모듈:Vau](https://ko.wikipedia.org/wiki/모듈:Vau).


local p = {}

\--\[\[ 사용법: {{\#invoke:Vau|ref|unit=유닛 이름|distinction=식별 번호|link=링크|add=추가 설명|group=ref 태그의 group 속성}}

unit - 필수 distinction - 임의 (초깃값 '') link - 임의 (초깃값 '') add - 임의 (초깃값 '') group - 임의 (초깃값 '구성원') list - 임의 (초깃값 '') \]\] function p.ref(frame)

`   -- 변수를 얻는다`
`   local unit = frame.args.unit`
`   local distinction = frame.args.distinction`
`   local link = frame.args.link`
`   local add = frame.args.add`
`   local list = frame.args.list`
`   local ref = {name = '', group = frame.args.group}`
`   `
`   -- 비각주 부분을 작성한다`
`   local noref = mw.text.nowiki(unit)`
`   noref = (link == '') and noref or '`[`'``   ``..``   ``noref``   ``..``   ``'`](https://ko.wikipedia.org/wiki/'_.._link_..' "wikilink")`'`
`   `
`   -- 유닛 이름+식별 번호를 유닛 목록에서 검색한다`
`   local search = (distinction == '') and unit or (unit .. '|' .. distinction)`
`   search = mw.text.unstripNoWiki(frame:expandTemplate{title = 'Vau/유닛 목록'}):match('(;%s*' .. search:gsub('%p', '%%p') .. '%s*\n.-:%s*.-)%s*\n[:;={]')`
`   `
`   local member = '' -- 구성원(ref content)`
`   local error = true`
`   if search then`
`       ref.name, member = search:match('.*;%s*(.-)%s+:%s*(.-)%s*[:;={]?$')`
`       ref.name = (ref.group == '구성원' ) and 'vau-' .. ref.name or 'vau-add-' .. ref.name .. add`
`       if not member:find('`<strong class="error">`') then`
`           -- 구성원이 에러가 없을 때: 문서의 성우를 굵은 글씨로 한다, add를 추가한다`
`           local bold = frame:preprocess('``')`
`           local avoid_suffix = {'의 작품', '의 음반 목록'}`
`           for k, v in ipairs(avoid_suffix) do`
`               bold = bold:gsub(v, '')`
`           end`
`           member = member:gsub('%[%[' .. bold .. '|(.-)]]', '`<b>`%1`</b>`'):gsub('%[%[' .. bold .. ']]', '`<b>`' .. bold .. '`</b>`') .. add`
`           error = false`
`       elseif member:find('끝에 추가해주세요') then`
`           -- 구성원이 동음이의어일 때: 비주얼 에디터용의 설명을 추가`
`           local d_code, i = {}, 0`
`           for value in member:gmatch('|(.-)') do`
`               i = i + 1`
`               d_code[i] = value`
`           end`
`           member = '`

<dl class="hlist" style="display:inline;">

<dt>

' .. unit .. '

</dt>

<dd style="white-space:normal;">

' .. member:gsub('</strong>$', '<small>비주얼 에디터로 편집하고 있는 경우에는 ‘식별 번호’ 필드에 각각 `' .. table.concat(d_code, '`、`') .. '`를 지정해주세요.</small></strong>') .. '

</dd>

</dl>

'

`       end`
`   else`
`       member = '`<strong class="error">`Vau 정의 에러: 유닛'.. mw.text.nowiki(unit) .. '에 대해서는 정의되어 있지 않습니다. 자세하게는 `[`틀:Vau#에러가``   ``발생했을``   ``때에는을`](https://ko.wikipedia.org/wiki/틀:Vau#에러가_발생했을_때에는 "wikilink")` 참조.`</strong>`'`
`   end`
`   `
`   -- 목록 형식`
`   if list ~= '' then`
`       ref = {name = 'vau-list-' .. list .. '-' .. unit, group = ref.group .. ' 목록 ' .. list .. ''}`
`       member = '`

<dl style="display:inline; margin-left:0;">

<dt style="display:inline;">

<dfn>' .. mw.text.nowiki(unit) .. '</dfn>

</dt>

<dd style="display:inline; margin-left:0;">

<span style="padding:0 0.5em;">-</span>' .. member .. '

</dd>

</dl>

'

`   end`
`   -- 출력한다`
`   if error then`
`       if frame:preprocess('``') == '' then`
`           -- 미리보기`
`           return member, '`

<div class="previewnote nomobile" style="position:absolute; top:-2em; left:0;">

<strong class="error" style="background:#fff; margin:0 ' .. (#tostring(mw.title.getCurrentTitle()) * 0.6 + 11.8) .. 'em;">[<span style="color:#c00;">틀:Vau</span>의](https://ko.wikipedia.org/wiki/틀:Vau "wikilink") 호출 에러가 발생하고 있습니다</strong>

</div>

'

`       else`
`           -- 목록`
`           return '`<span class="vau-error">`' .. noref .. '`</span>`', '`[`분류:Vau``   ``틀에``   ``의한``   ``오류가``   ``있는``   ``문서`](https://ko.wikipedia.org/wiki/분류:Vau_틀에_의한_오류가_있는_문서 "wikilink")`'`
`       end`
`   else`
`       return '`<span class="vau">`' .. noref .. frame:extensionTag('ref', member, ref) .. '`</span>`'`
`   end`

end

return p