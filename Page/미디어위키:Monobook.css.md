> This article is converted from Wikipedia: [미디어위키:Monobook.css](https://ko.wikipedia.org/wiki/미디어위키:Monobook.css).


/\*

``` css
 */

/**
 *
 * 위키백과 모노북 스킨에서 적용되는 CSS입니다.
 * 제안 및 질문은 [[미디어위키토론:Monobook.css|미디어위키토론:Monobook.css]] 또는 [[위키백과토론:위키프로젝트_시스템|위키백과토론:위키프로젝트 시스템]]에서
 *
 * 편집 요약을 꼭 적어주고, 새 코드를 추가할 때에는 해당 코드의 출처, 간단한 설명, (요청이 있었을 경우) 해당 요청의 위치 등을 주석에 적어주세요.
 * 또한 각 코드 조각의 범위를 알아보기 쉽도록 정렬해주세요.
 *
 **/

/**
 *
 * 특정 이름공간 문서의 배경을 하늘색, 비활성 탭의 색깔을 연한 하늘색으로 지정합니다.
 *
 * 적용 대상: 특수기능(-1), 토론(1), 사용자토론(3), 위키백과토론(5), 그림토론(7), 미디어위키(8), 미디어위키토론(9),
 * 틀토론(11), 도움말토론(13), 분류토론(15), 들머리토론(101), 위키프로젝트토론(103)
 *
 **/

.ns-1 #content, .ns-1 #p-cactions li a:hover, .ns-1 #p-cactions li.selected a,
.ns-3 #content, .ns-3 #p-cactions li a:hover, .ns-3 #p-cactions li.selected a,
.ns-5 #content, .ns-5 #p-cactions li a:hover, .ns-5 #p-cactions li.selected a,
.ns-6 #content, .ns-6 #p-cactions li a:hover, .ns-6 #p-cactions li.selected a,
.ns-7 #content, .ns-7 #p-cactions li a:hover, .ns-7 #p-cactions li.selected a,
.ns-8 #content, .ns-8 #p-cactions li a:hover, .ns-8 #p-cactions li.selected a,
.ns-9 #content, .ns-9 #p-cactions li a:hover, .ns-9 #p-cactions li.selected a,
.ns-11 #content, .ns-11 #p-cactions li a:hover, .ns-11 #p-cactions li.selected a,
.ns-13 #content, .ns-13 #p-cactions li a:hover, .ns-13 #p-cactions li.selected a,
.ns-15 #content, .ns-15 #p-cactions li a:hover, .ns-15 #p-cactions li.selected a,
.ns-101 #content, .ns-101 #p-cactions li a:hover, .ns-101 #p-cactions li.selected a,
.ns-103 #content, .ns-103 #p-cactions li a:hover, .ns-1031 #p-cactions li.selected a,
.ns--1 #content, .ns--1 #p-cactions li a:hover, .ns--1 #p-cactions li.selected a {
  background-color: #fafaff;
}
#p-cactions li a {
    background-color: #fbfbfb;
}
#mw-subcategories table, #mw-pages table {
    background-color: transparent;
}

/* 문서 제목 밑의 ‘위키백과 ― 우리 모두의 백과사전.’ 모양 조절 */
#siteSub {
  display: inline;
  font-size: small;
  font-weight: normal;
}
#bodyContent #siteSub a {
  color: #000;
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  padding-right: 0;
}

/* 알찬 글, 보호 문서 등의 아이콘 위치 조정 */
div.topicon {
    position: absolute;
    z-index: 10;
    top: 10px;
    display: block !important;
}

/* 새내기들을 위해 윗부분 '편집' 버튼의 글씨를 언제나 굵게 */
#ca-edit a {
  font-weight: bold !important;
}

/* 로그인 상자의 모양 조절. */
#pt-login {
  font-weight: bold;
  font-size: 110%;
}
form#userlogin {
  float: left;
  padding: 1em 1em .7em 1em;
  background-color: #ffffe6;
  border: 2px solid #fc6;
  color: #000;
  margin-right: 2em;
}
form#userlogin table {
  background-color: #ffffe6;
  color: #000;
}
form#userlogin2 {
  float: left;
  padding: 1em 1em .7em 1em;
  background-color: #ffffe6;
  border: 2px solid #fc6;
  color: #000;
  margin-right: 2em;
}
form#userlogin2 table {
  background-color: #ffffe6;
  color: #000;
}

/* 한국어 글꼴에 맞춰 글자 크기 조절(118% 증가) */
#bodyContent {
  font-size:118%;
}

/* 글자 크기 조절 */
.portlet h5,
.portlet ul,
#toc .toctoggle {
    font-size: 100%;
}
.pBody,
#footer,
div.thumb div {
  font-size: 95%;
}
h2 {
  font-weight: bold;
}

/* 대문에서 특정 요소를 숨김 */
.page-위키백과_대문 #deleteconfirm,
.page-위키백과_대문 #t-cite,
.page-위키백과_대문 #footer-info-lastmod,
.action-view.page-위키백과_대문 #siteSub,
.action-view.page-위키백과_대문 #contentSub,
.action-view.page-위키백과_대문 .firstHeading {
    display: none !important;
}

/* [[MediaWiki:Edittools|MediaWiki:Edittools]] 편집 입력 도구의 버튼 */
.my-buttons {
  padding: 0.5em;
}
.my-buttons a {
  color: black;
  background-color: #ccddee !important;
  font-weight: bold;
  font-size: 0.9em;
  text-decoration: none;
  border: thin #006699 outset;
  padding: 0 0.1em 0.1em 0.1em;
}
.my-buttons a:hover, .my-buttons a:active {
  background-color: #bbccdd;
  border-style: inset;
}

#siteNotice {
  margin-top: 5px;
  background-color: transparent;
  font-style: normal;
  text-align: center;
}
#mw-dismissable-notice {
  background-color: transparent;
}

/* 보호/알찬 글 표시 위치 */
/* For positioning icons at top-right, used in Templates
   "Spoken Article" and "Featured Article" */
div.topicon {
    position: absolute;
    z-index: 10;
    top: 10px;
    display: block !important;
}

/* {{틀|Coord}} 관련 스타일 */
#coordinates {
    position: absolute;
    z-index: 1;
    border: none;
    background: none;
    right: 30px;
    top: 3.7em;
    float: right;
    margin: 0.0em;
    padding: 0.0em;
    line-height: 1.5em;
    text-align: right;
    text-indent: 0;
    font-size: 85%;
    text-transform: none;
    white-space: nowrap;
}

/* 환경 설정에서 도움말 부분 글씨를 너무 작지 않게 조정. [[사용자:Klutzy|klutzy]] ([[사용자토론:Klutzy|토론]]) 2009년 11월 9일 (월) 02:45 (KST) */
body.page-특수기능_환경설정 .htmlform-tip { font-size: small; }

li.FA {
  list-style-image: url("//upload.wikimedia.org/wikipedia/commons/d/d4/Monobook-bullet-star.png");
}
li.GA {
  list-style-image: url("//upload.wikimedia.org/wikipedia/commons/5/58/Monobook-bullet-star-ga.png");
}

/*
```

\*/