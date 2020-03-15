> This article is converted from Wikipedia: [:Modern.css](https://ko.wikipedia.org/wiki/:Modern.css).


/\*

``` css
 */

/* 글자 크기 조절 */
.portlet h5,
.portlet ul,
#toc .toctoggle {
  font-size: 100%;
}

/* 개인 도구 */
#p-personal li {
  text-transform: none !important;
}

/* 본문 글자 크기 */
#mw_contentholder {
  font-size:118%;
}

/* 글자 크기 조정에 따른 레이아웃 보정 */
#mw_contentholder {
margin-right: 0.15em;
margin-left: 0.15em;
}

/* 본문 문단 */
#mw_contentholder p {
  margin: 0.4em 0 0.5em 0;
  line-height: 1.5em;
}

/* 그림 */
img {
  border: none;
  vertical-align: middle;
}

/* 들여쓰기 */
dd {
  margin-left: 2em;
}

/* topbox */

.mw-topbox {
font-weight: normal !important;
font-size: 75% !important;
}

/* 위키백과 - 우리 모두의 백과사전 */
#siteSub {
  display: block;
}

/* 대문에서 몇가지의 요소 숨기기 */
body.page-위키백과_대문 #t-cite,
body.page-위키백과_대문 #lastmod,
body.page-위키백과_대문 #siteSub {
  display: none !important;
}

/* [[미디어위키토론:Modern.css#좌표·보호_틀_관련_스타일_추가_요청|미디어위키토론:Modern.css#좌표·보호 틀 관련 스타일 추가 요청]] --[[사용자:PuzzletChung|Puzzlet Chung]] ([[사용자토론:PuzzletChung|토론]]) 2010년 4월 17일 (토) 19:03 (KST) */
#coordinates {
    position: absolute;
    z-index: 1;
    border: none;
    background: none;
    right: 30px;
    top: 46px;
    float: right;
    margin: 0;
    padding: 0;
    line-height: 1.5em;
    text-align: right;
    text-indent: 0;
    font-size: smaller;
    text-transform: none;
    white-space: nowrap;
}

/* [[미디어위키토론:Modern.css#좌표·보호_틀_관련_스타일_추가_요청|미디어위키토론:Modern.css#좌표·보호 틀 관련 스타일 추가 요청]] --[[사용자:PuzzletChung|Puzzlet Chung]] ([[사용자토론:PuzzletChung|토론]]) 2010년 4월 17일 (토) 19:03 (KST) */
.topicon {
    position: absolute;
    z-index: 10;
    top: 5px;
    display: block !important;
}

.FA {
  list-style-image: url("//upload.wikimedia.org/wikipedia/commons/d/d4/Monobook-bullet-star.png");
}
.GA {
  list-style-image: url("//upload.wikimedia.org/wikipedia/commons/5/58/Monobook-bullet-star-ga.png");
}
/*
```

\*/