> This article is converted from Wikipedia: [미디어위키:Vector.css](https://ko.wikipedia.org/wiki/미디어위키:Vector.css).


/\* 대문에서 특정 요소를 숨김 \*/ .page-위키백과_대문 \#deleteconfirm, .page-위키백과_대문 \#t-cite, .page-위키백과_대문 \#footer-info-lastmod, .action-view.page-위키백과_대문 \#siteSub, .action-view.page-위키백과_대문 \#contentSub, .action-view.page-위키백과_대문 .firstHeading {

`   display: none !important;`

}

/\* Position coordinates \*/

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

} /\* correct position for VE \*/ .ve-ce-surface-enabled \#coordinates {

`   margin-right: 2em;`
`   margin-top: -1em;`

} .mw-indicator \#coordinates {

`   position: absolute;`
`   top: 3em;`
`   right: 0;`
`   line-height: 1.6;`
`   text-align: right;`
`   font-size: 92%;`
`   white-space: nowrap;`

}

1.  p-cactions li a {

`   background-color: #fbfbfb;`

}

1.  mw-subcategories table, \#mw-pages table {

`   background-color: transparent;`

}

/\* 2단계 제목을 굵은 글꼴로 \*/ h2 {

` font-weight: bold;`

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

/\* FR topicon position \*/ .flaggedrevs_short {

`   position: absolute;`
`   top: -3em;`
`   right: 100px;`
`   z-index: 1;`

}

/\* 문서 제목 밑의 ‘위키백과 ― 우리 모두의 백과사전.’ 모양 조절 \*/

1.  siteSub {

`   font-size: 92%;`

}

/\* Move page status indicators down slightly \*/ .mw-body .mw-indicators {

`   padding-top: 0.4em;`

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

`   clear: both;`

}

/\* 계정 등록 폼 레이블 \*/ .mw-label {

`   width: 6em;`

}

/\* 새내기들을 위해 윗부분 '편집' 버튼의 글씨를 언제나 굵게 \*/

1.  ca-edit a {

`   font-weight: bold !important;`

}

/\* [MediaWiki:Edittools](https://ko.wikipedia.org/wiki/MediaWiki:Edittools "wikilink") 편집 입력 도구의 버튼 \*/ .my-buttons {

`   text-align: left;`
`   font-size: 110%;`

}

.my-buttons a {

`   color: black;`
`   background-color: #f9f9f9 !important;`
`   text-decoration: none;`
`   border: 1px solid #dddddd;`
`   margin: 0.25em;`
`   padding-left: 3px;`
`   padding-right: 3px;`

}

/\* [:m:Typography refresh에서](https://ko.wikipedia.org/wiki/:m:Typography_refresh "wikilink")  등에 italic 준 것 무효화 \*/ .rellink, .dablink {

` font-style: normal;`

}

/\* 다른 프로젝트 연결 아이콘 표시 \*/ /\* [:fr:MediaWiki:Vector.css](https://ko.wikipedia.org/wiki/:fr:MediaWiki:Vector.css "wikilink")에서 가져옴 \*/ /\* Icônes pour les liens interprojets \*/ li.wb-otherproject-link {

` background-repeat: no-repeat;`
` background-position: left center;`

}

1.  p-wikibase-otherprojects div.body ul li.wb-otherproject-link {

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