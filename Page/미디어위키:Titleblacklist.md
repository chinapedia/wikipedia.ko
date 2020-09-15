> This article is converted from Wikipedia: [미디어위키:Titleblacklist](https://ko.wikipedia.org/wiki/미디어위키:Titleblacklist).


`# 문서 이름 금지 목록을 적는 곳입니다. `[`정규``   ``표현식과`](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink")` 일치하는 문서나 사용자명에 대한 행동이 제한됩니다.`
`# 기능 사용법에 대해서는 `[`mw:Extension:TitleBlacklist/ko`](https://ko.wikipedia.org/wiki/mw:Extension:TitleBlacklist/ko "wikilink")을` 참고해주세요. 구체적인 사용에 대해서는 `[`미디어위키토론:Titleblacklist`](https://ko.wikipedia.org/wiki/미디어위키토론:Titleblacklist "wikilink")를` 참고해주세요.`
`# 주석은 #로 시작합니다. 각 문장에는 맨 앞에 한 칸씩 띄어 주세요.`
`# 규칙을 추가할 때에는 추가하는 이유와 서명을 추가해주세요.`
`# 개인정보에 관련된 내용은 여기에 작성하기에 적합하지 않습니다. `[`특수기능:AbuseFilter`](https://ko.wikipedia.org/wiki/특수기능:AbuseFilter "wikilink")를` 사용해주세요.`

`# `[`위키백과:관리자``   ``권한``   ``회수의`](../Page/위키백과:관리자_권한_회수.md "wikilink")` 하위문서 생성 제한`
`위키백과:관리자 권한 회수\/.* <errmsg=titleblacklist-forbidden-rfasubpage>`

`# 위에 맞추어 `[`위키백과:비활동``   ``관리자``   ``권한``   ``회수의`](../Page/위키백과:비활동_관리자_권한_회수.md "wikilink")` 하위문서 생성 제한`
`위키백과:비활동 관리자 권한 회수\/.* <errmsg=titleblacklist-forbidden-rfasubpage>`

`# `[`위키백과:알찬``   ``글``   ``후보`](../Page/위키백과:알찬_글_후보.md "wikilink")`, `[`위키백과:좋은``   ``글``   ``후보의`](../Page/위키백과:좋은_글_후보.md "wikilink")` 준보호 생성 제한 --관인생략`
`위키백과:알찬 글 후보\/.* <autoconfirmed|errmsg=titleblacklist-forbidden-rfasubpage>`
`위키백과:좋은 글 후보\/.* <autoconfirmed|errmsg=titleblacklist-forbidden-rfasubpage>`
`위키백과:알찬 글 재검토\/.* <autoconfirmed|errmsg=titleblacklist-forbidden-rfasubpage>`
`위키백과:좋은 글 재검토\/.* <autoconfirmed|errmsg=titleblacklist-forbidden-rfasubpage>`

`# IP 사용자 문서 생성 제한`
`사용자:([1-9]?\d|1\d\d|2([0-4]\d|5[0-5]))\.([1-9]?\d|1\d\d|2([0-4]\d|5[0-5]))\.([1-9]?\d|1\d\d|2([0-4]\d|5[0-5]))\.([1-9]?\d|1\d\d|2([0-4]\d|5[0-5]))(\/.*)? <errmsg=titleblacklist-forbidden-anonymoususerpage>`

`# IPv6 사용자 문서 생성 제한`
`사용자:[0-9A-Fa-f]{0,10}:([0-9A-Fa-f]{0,10}:)*([0-9A-Fa-f]{0,10})?(?:\/(12[0-8]|1[01][0-9]|[1-9]?\d))? <errmsg=titleblacklist-forbidden-anonymoususerpage>`

`# 관리자 사칭 가능성이 있는 계정 가입 제한`
`.*(\ba|A)(?i:dmin).* `<newaccountonly>
`.*(\bs|S)(?i:ysop).* `<newaccountonly>
`.*(\bm|M)(?i:oderator).* `<newaccountonly>
`.*(\ba|A)(?i:rbitrator).* `<newaccountonly>
`.*(\bc|C)(?i:heckuser).* `<newaccountonly>

`# 편집 안내 틀 생성 보호. `[`ChongDae`](https://ko.wikipedia.org/wiki/사용자:ChongDae "wikilink")` (`[`토론`](https://ko.wikipedia.org/wiki/사용자토론:ChongDae "wikilink")`) 2012년 11월 15일 (목) 16:11 (KST)`
`틀:편집[ _]안내\/.* <noedit|errmsg=titleblacklist-custom-editnotice>`

`# 감탄사 반복. `[`ChongDae`](https://ko.wikipedia.org/wiki/사용자:ChongDae "wikilink")` (`[`토론`](https://ko.wikipedia.org/wiki/사용자토론:ChongDae "wikilink")`) 2012년 11월 22일 (목) 18:27 (KST)`
`.*[!?‽¿]{4}(?<!!!!).*`
`.*[!?‽¿]{3}(?<!!!!).* `<moveonly>
`.*[!?‽¿]\s+[!?‽¿].*`
`.*‽‽.* `<moveonly>` `
`.*¿¿.* `<moveonly>
`.*[\p{Z}]{2}.* # Disallows two adjacent "separator" characters (mostly funky spaces)`
`.*[^\p{L}\d ]{6}.* # Disallows six consecutive characters that are not letters (in any script), numbers, or spaces`
`.*([^0])\1{4}.* `<moveonly>` # Disallows four or more of the same character from page moves`
`.*(.)\1{10}.* `<newaccountonly>` # Disallows eleven or more of the same character repeated in usernames`
`.{40,} `<newaccountonly>
`# .*\p{Lu}(\P{L}*\p{Lu}){9}.* <casesensitive | moveonly>  # Disallows moves with more than nine consecutive capital letters`