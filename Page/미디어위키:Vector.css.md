> This article is converted from Wikipedia: [미디어위키:Vector.css](https://ko.wikipedia.org/wiki/미디어위키:Vector.css).


/\* 대문에서 특정 요소를 숨김 \*/ .page-위키백과_대문 \#deleteconfirm, .page-위키백과_대문 \#t-cite, .page-위키백과_대문 \#footer-info-lastmod, .action-view.page-위키백과_대문 \#siteSub, .action-view.page-위키백과_대문 \#contentSub, .action-view.page-위키백과_대문 .firstHeading {

`   display: none !important;`

}

/\*\*

`*`
`* 특정 이름공간 문서의 배경을 하늘색, 비활성 탭의 색깔을 연한 하늘색으로 지정합니다.`
`*`
`* 적용 대상: 특수기능(-1), 토론(1), 사용자토론(3), 위키백과토론(5), 그림토론(7), 미디어위키(8), 미디어위키토론(9),`
`* 틀토론(11), 도움말토론(13), 분류토론(15), 들머리토론(101), 위키프로젝트토론(103)`
`*`
`**/`

.ns-1 \#content, .ns-1 \#p-cactions li a:hover, .ns-1 \#p-cactions li.selected a, .ns-3 \#content, .ns-3 \#p-cactions li a:hover, .ns-3 \#p-cactions li.selected a, .ns-5 \#content, .ns-5 \#p-cactions li a:hover, .ns-5 \#p-cactions li.selected a, .ns-6 \#content, .ns-6 \#p-cactions li a:hover, .ns-6 \#p-cactions li.selected a, .ns-7 \#content, .ns-7 \#p-cactions li a:hover, .ns-7 \#p-cactions li.selected a, .ns-8 \#content, .ns-8 \#p-cactions li a:hover, .ns-8 \#p-cactions li.selected a, .ns-9 \#content, .ns-9 \#p-cactions li a:hover, .ns-9 \#p-cactions li.selected a, .ns-11 \#content, .ns-11 \#p-cactions li a:hover, .ns-11 \#p-cactions li.selected a, .ns-13 \#content, .ns-13 \#p-cactions li a:hover, .ns-13 \#p-cactions li.selected a, .ns-15 \#content, .ns-15 \#p-cactions li a:hover, .ns-15 \#p-cactions li.selected a, .ns-101 \#content, .ns-101 \#p-cactions li a:hover, .ns-101 \#p-cactions li.selected a, .ns-103 \#content, .ns-103 \#p-cactions li a:hover, .ns-103 \#p-cactions li.selected a, .ns--1 \#content, .ns--1 \#p-cactions li a:hover, .ns--1 \#p-cactions li.selected a {

` background-color: #fafaff;`

}

1.  p-cactions li a {

`   background-color: #fbfbfb;`

}

1.  mw-subcategories table, \#mw-pages table {

`   background-color: transparent;`

}

/\* [위키백과토론:위키프로젝트 시스템/벡터 스킨\#IE8에서 사이드바 글자 짤림 현상](https://ko.wikipedia.org/wiki/위키백과토론:위키프로젝트_시스템/벡터_스킨#IE8에서_사이드바_글자_짤림_현상 "wikilink") 관련 - 2010년 4월 9일 (금) 10:05 [사용자:PuzzletChung](https://ko.wikipedia.org/wiki/사용자:PuzzletChung "wikilink") \*/

1.  mw-panel .portal .body ul li {

`padding: 0.25em 0;`

}

/\* 2단계 제목을 굵은 글꼴로 \*/ h2 {

` font-weight: bold;`

}

/\* 입력창 크기 버그 수정. 영어 위키백과에서 가져옴 \*/ /\* [bugzilla:20276](https://ko.wikipedia.org/wiki/bugzilla:20276 "wikilink") \*/

1.  wpSummary {

`width:100%;`

}

/\* 알찬 글, 보호 문서 등의 아이콘 위치 조정 \*/ div.topicon {

`position: absolute;`
`top: -3em;`
`margin-right: -10px;`
`display: block !important;`

}

body.ns-0 div.topicon, body.ns-1 div.topicon {

`top: -2em;`

}

/\* 문서 제목 밑의 ‘위키백과 ― 우리 모두의 백과사전.’ 모양 조절 \*/ body.ns-0 \#siteSub, body.ns-1 \#siteSub {

`   display: inline;`
`   font-size: 92%;`
`   font-weight: normal;`

}

/\*  \*/

1.  coordinates {

`   position: absolute;`
`   top: 0;`
`   right: 0;`
`   float: right;`
`   margin: 0;`
`   padding: 0;`
`   line-height: 1.5em;`
`   text-align: right;`
`   text-indent: 0;`
`   font-size: 85%;`
`   text-transform: none;`
`   white-space: nowrap;`

}

body.ns-0 \#coordinates, body.ns-1 \#coordinates {

`top: 0;`

}

/\* 편집 요약, 이유의 모양 설정.

`(기울임 대신 글자 크기 약간 작게 하여 구별) */`

.comment {

` font-style: normal !important;`
` font-size: 9pt;`

}

/\* 문서 목록과 주시문서 목록에서 넘겨주기의 모양 설정

`(연한 회색) */`

.allpagesredirect a, .watchlistredir a {

` color:#888888;`

}

/\* 로그인·계정 등록 깨짐 수정 \*/

1.  loginend, \#signupend {

`clear: both;`

}

/\* 계정 등록 폼 레이블 \*/ .mw-label {

`width: 6em;`

}

/\* 새내기들을 위해 윗부분 '편집' 버튼의 글씨를 언제나 굵게 \*/

1.  ca-edit a {

` font-weight: bold !important;`

}

/\* [MediaWiki:Edittools](https://ko.wikipedia.org/wiki/MediaWiki:Edittools "wikilink") 편집 입력 도구의 버튼 \*/ .my-buttons {

` padding: 0.5em;`

} .my-buttons a {

` color: black;`
` background-color: #ccddee !important;`
` font-weight: bold;`
` font-size: 0.9em;`
` text-decoration: none;`
` border: thin #006699 outset;`
` padding: 0 0.1em 0.1em 0.1em;`

} .my-buttons a:hover, .my-buttons a:active {

` background-color: #bbccdd;`
` border-style: inset;`

}

/\* [:m:Typography refresh에서](https://ko.wikipedia.org/wiki/:m:Typography_refresh "wikilink")  등에 italic 준 것 무효화 \*/ .rellink, .dablink {

` font-style: normal;`

}

/\* 다른 프로젝트 연결 아이콘 표시 \*/ /\* [fr:MediaWiki:Vector.css](https://ko.wikipedia.org/wiki/fr:MediaWiki:Vector.css "wikilink")에서 가져옴 \*/ /\* Icônes pour les liens interprojets \*/ li.wb-otherproject-link {

` background-repeat: no-repeat;`
` background-position: left center;`

}

div.portal\#p-wikibase-otherprojects div.body ul li.wb-otherproject-link {

` position: relative;`
` left: 0px;`
` padding-left: 20px;`

}

li.wb-otherproject-commons {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Commons-logo.svg/14px-Commons-logo.svg.png");`

}

li.wb-otherproject-wiktionary {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Wiktionary_small.svg/16px-Wiktionary_small.svg.png");`

}

li.wb-otherproject-wikibooks {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Wikibooks-logo.svg/16px-Wikibooks-logo.svg.png");`

}

li.wb-otherproject-wikiquote {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Wikiquote-logo.svg/15px-Wikiquote-logo.svg.png");`

}

li.wb-otherproject-wikisource {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Wikisource-logo.svg/15px-Wikisource-logo.svg.png");`

}

li.wb-otherproject-wikinews {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Wikinews_waves_Left.png/15px-Wikinews_waves_Left.png");`

}

li.wb-otherproject-wikispecies, li.wb-otherproject-species {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/d/df/Wikispecies-logo.svg/15px-Wikispecies-logo.svg.png");`

}

li.wb-otherproject-wikivoyage {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Wikivoyage-logo.svg/15px-Wikivoyage-logo.svg.png");`

}

li.wb-otherproject-wikiversity {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/9/91/Wikiversity-logo.svg/15px-Wikiversity-logo.svg.png");`

}

li.wb-otherproject-wikidata {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/f/ff/Wikidata-logo.svg/15px-Wikidata-logo.svg.png");`

}

li.wb-otherproject-meta {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/7/75/Wikimedia_Community_Logo.svg/15px-Wikimedia_Community_Logo.svg.png");`

}

li.wb-otherproject-incubator {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Incubator-logo.svg/15px-Incubator-logo.svg.png");`

}

li.wb-otherproject-mediawiki {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Mediawiki-logo.png/15px-Mediawiki-logo.png");`

}

li.wb-otherproject-wikimania {

` background-image: url("//upload.wikimedia.org/wikipedia/commons/thumb/5/57/Wikimania.svg/15px-Wikimania.svg.png");`

}

/\*

</source>

\*/