> This article is converted from Wikipedia: [HTML ](https://ko.wikipedia.org/wiki/HTML_).


**HTML 요소**(HTML 엘리먼트, HTML element)는 [HTML](../Page/HTML.md "wikilink") 문서나 [웹 페이지를](../Page/웹_페이지.md "wikilink") 이루는 개별적인 요소를 의미하며, [문서 객체 모델](../Page/문서_객체_모델.md "wikilink")(DOM)으로 파싱된다. HTML은 [트리나](https://ko.wikipedia.org/wiki/트리_구조 "wikilink") HTML [노드](https://ko.wikipedia.org/wiki/노드 "wikilink")(텍스트 노드 등)로 구성된다. 각 노드는 [HTML 속성을](../Page/HTML_속성.md "wikilink") 지정할 수 있다. 노드들은 기타 노드와 텍스트를 포함한 콘텐츠도 소유할 수 있다. 수많은 HTML 노드들은 [시맨틱이나](../Page/의미론.md "wikilink") 의미를 표현한다. 이를테면 `title` 노드는 문서의 제목을 나타낸다.

## 개념

### 문서와 DOM

HTML 문서들은 "문서"(document)로 전달된다.\[1\] 이들은 [구문 분석](../Page/구문_분석.md "wikilink") 과정을 거쳐 웹 브라우저 내에서 [문서 객체 모델](../Page/문서_객체_모델.md "wikilink")(DOM) 내부 표현으로 변환된다.\[2\]

화면과 같은 웹 브라우저의 표현이라든지 자바스크립트의 접근은 그 다음에 이 내부 모델에서 수행되며 원래의 문서에서 수행되지는 않는다.

초기의 HTML 문서들은 오늘날 어느 정도는 크게 [유효하지 않은 HTML이었으며](https://ko.wikipedia.org/wiki/태그_숩 "wikilink") 문법 오류 투성이었다. 가능한 이러한 오류를 해결하기 위해 파싱 과정도 필요했다. 그 결과의 모델은 정확하지는 않지만(이를테면 주의깊은 코더가 원래 의도한 바를 표현하지 못하는 등) 적어도 HTMl 표준에 따라 [유효하다](https://ko.wikipedia.org/wiki/유효한_HTML "wikilink"). 유효한 모델은 제공되는 [태그 숩이](https://ko.wikipedia.org/wiki/태그_숩 "wikilink") 얼마나 나쁜지에 관계 없이 만들어진다. 극소수의 경우에만 파서가 파싱을 포기한다.

### 요소와 태그

요소와 태그는 널리 혼동되는 용어들이다. HTML 문서들은 태그를 포함하지만 요소를 포함하지는 않는다. 요소는 구문 분석 단계 "이후"에 이 태그들로부터 생성된다.

요소의 위치는 시작 태그로부터 신장되며 일부 차일드 콘텐츠를 포함할 수 있으며 종료 태그로 종료된다.\[3\] HTML 문서 내의 다수의 요소에 해당되지만 모든 요소에 해당되는 것은 아니다.

HTML이 [SGML](../Page/SGML.md "wikilink")에 기반을 두므로\[4\] 구문 분석 또한 [DTD](https://ko.wikipedia.org/wiki/문서_형식_정의 "wikilink"), 특히 HTML 4.01의 것과 같은 HTML DTD의 사용에 의존한다.\[5\]\[6\] DTD는 어느 요소 유형이 가능한지 규정하며(예: HTML을 이루는 요소 유형의 집합을 정의) 문서에서 나타나는 유효한 결합도 규정한다.

HTML의 문서의 일부는

  -

다음과 동등한 것으로 추론한다:

  -

### SGML과 XML

SGML은 복잡하며 폭넓은 채택과 이해에 제한이 있다. 더 단순한 대안으로 [XML](../Page/XML.md "wikilink")이 개발되었다. XML은 DTD 매커니즘을 사용하여 지원 요소 및 허가된 결합을 문서 구조로 정의한다는 면에서 SGML과 비슷하다. XML 구문 분석은 더 단순하다.

#### `%block;`과 box

CSS 표현 동작의 일부는 [박스 모델의](https://ko.wikipedia.org/wiki/CSS_박스_모델 "wikilink") 개념이다. 이것은 CSS가 블록 요소로 간주되는 요소들에 적용되며 CSS  선언을 통해 설정된다.

HTML 또한 차이는 있지만 유사 개념이 있으며 이 둘이 종종 혼동된다. `%block;`과 `%inline;`은 "block-level" 또는 "inline"으로 요소들을 묶는 HTML DTD 내의 그룹들이다.\[7\] 이것을 사용하면 네스팅(nesting) 동작을 정의할 수 있다: block-level 요소들은 inline 컨텍스트에 추가할 수 없다.\[8\] 이 동작은 변경할 수 없고 DTD 안에 고정된다.

## 개요

### 문법

\\mathtt{= *}\\\!\\underbrace\\mathtt{foo}_\\mathsf{\\color{White}{Attr} \\atop \\color{Black}value}*\\mathtt{\\color{BrickRed}\>}}^\\mathsf{Start\\ tag}

` \overbrace\mathtt{\color{Green}This\ is\ a\ paragraph.}^\mathsf{Content}`
` \overbrace\mathtt{\color{BrickRed}<\!/p\!>}^\mathsf{End \atop tag}`

}^\\mathsf{Element} </math> }} HTML 문법에서 대부분의 요소들은 시작 태그와 종료 태그로 작성되며 그 사이에 내용이 들어간다. HTML 태그는 요소 이름, 또 그 요소를 둘러싸는 [꺾쇠괄호로](https://ko.wikipedia.org/wiki/괄호 "wikilink") 이루어진다. 종료 태그 또한 꺾쇠괄호를 연 뒤 슬래시를 넣어 시작 태그와 구별한다. 이를테면 `p` 요소로 대표되는 문단은 다음과 같이 작성한다:

``` html4strict
<p>In the HTML syntax, most elements are written ...</p>
```

그러나 모든 요소에 종료 태그가 "필수"인 것은 아니며 시작 태그 또한 마찬가지이다. 이른바 빈 요소(empty elements, void elements)로 불리는 일부 요소들은 종료 태그가 없다. 일반적인 예가 `br` 요소이며, 주소나 시와 같은 곳에서 중요한 [줄 나눔을](https://ko.wikipedia.org/wiki/하드_리턴 "wikilink") 표현한다. 빈 요소의 동작은 미리 정의되므로 어떠한 내용이나 다른 요소가 포함될 수 없다. 이를테면 주소는 다음과 같이 쓸 수 있다:

``` html4strict
<p>P. Sherman<br>42 Wallaby Way<br>Sydney</p>
```

[XHTML](../Page/XHTML.md "wikilink") [DTD를](https://ko.wikipedia.org/wiki/문서_형식_정의 "wikilink") 사용할 때 하나의 태그로 요소를 열고 닫아야 한다. 빈 요소임을 지정하려면 "/"를 태그 끝에 포함시킨다. (닫는 태그의 시작부의 "/"와 혼동하지 말 것)

``` html4strict
<p>P. Sherman<br />42 Wallaby Way<br />Sydney</p>
```

[HTML 속성은](../Page/HTML_속성.md "wikilink") 시작 태그 안에 지정한다. 이를테면 `abbr` 요소는 [축약](https://ko.wikipedia.org/wiki/축약 "wikilink")을 의미하며 `title` 속성이 여는 태그 안에 있을 것이라 예측하는 예는 다음과 같다:

``` html4strict
<abbr title="abbreviation">abbr.</abbr>
```

여러 조율의 [HTML](../Page/HTML.md "wikilink") 요소가 있다: 빈 요소(void elements), 순수 텍스트 요소(raw text elements), 일반 요소(normal elements).

**빈 요소**는 [HTML 속성만](../Page/HTML_속성.md "wikilink") 담고있는 시작 태그만 있다. 텍스트나 다른 요소들과 같은 칠드런은 포함하지 않는다. 그림 () 요소와 같은 외부 링크를 참조하는 요소를 위한 플레이스 홀더 역할을 하기도 한다. 요소에 포함되는 속성들은 그 뒤 외부 파일을 가리키게 된다. 빈 요소의 다른 예는  요소이며 이를 위한 문법은 다음과 같다:

``` html4strict
<link rel="stylesheet" href="fancy.css" type="text/css">
```

이  요소는 HTML 문서를 사용자에게 표시할 때 사용하기 위한 [스타일시트](https://ko.wikipedia.org/wiki/스타일시트 "wikilink")의 브라우저를 가리킨다. HTML 문법에서 속성은 특정 문자열(문자, 숫자, 하이픈 마이너스, 마침표)만 구성하고 있다면 인용부호를 사용할 필요가 없다. 한편 [XML](../Page/XML.md "wikilink") 문법([XHTML](../Page/XHTML.md "wikilink"))을 사용할 때 모든 속성은 인용 부호로 감싸야 하며 마지막 꺾쇠 괄호 앞에 [슬래시](https://ko.wikipedia.org/wiki/슬래시 "wikilink")를 추가해야 한다:

``` xml
<link rel="stylesheet" href="fancy.css" type="text/css" />
```

**순수 텍스트 요소**는 다음으로 구성된다:

  - 시작 태그 (): 요소의 시작을 알리며 수많은 [HTML 속성을](../Page/HTML_속성.md "wikilink") 포함할 수 있다.
  - 요소(모든 태그는 콘텐츠로 해석됨)가 없는 어느 정도 분량의 텍스트 내용.
  - 종료 태그: 요소 이름은 슬래시로 구분한다() 일부 HTML 버전에서 종료 태그는 일부 요소들에게 선택사항이다. 종료 태그는 [XHTML](../Page/XHTML.md "wikilink")에서는 필수이다.

**일반 요소**는 보통 시작 태그와 종료 태그를 갖고 있으나 일부 요소들의 경우 종료 태그 또는 시작 태그와 종료 태그를 둘 다 생략할 수 있다. 비슷한 방식으로 구성되어 있다:

  - 시작 태그 (): 요소의 시작을 알리며 수많은 [HTML 속성을](../Page/HTML_속성.md "wikilink") 포함할 수 있다.
  - 텍스트와 기타 요소들을 포함하는 어느 정도 분량의 내용.
  - 종료 태그: 요소 이름은 슬래시로 구분한다()

## HTML 태그 목록

HTML 요소를 표현하기 위한 HTML 태그 목록은 다음과 같다.\[9\]

  - `<a>`
  - `<abbr>`
  - `<acronym>`
  - `<address>`
  - `<applet>`
  - `<area>`
  - `<article>`
  - `<aside>`
  - `<audio>`
  - `<b>`
  - `<base>`
  - `<basefont>`
  - `<bdi>`
  - `<bdo>`
  - `<big>`
  - `<blockquote>`
  - `<body>`
  - `<br>`
  - `<canvas>`
  - `<caption>`
  - `<center>`
  - `<cite>`
  - `<code>`
  - `<col>`
  - `<colgroup>`
  - `<command>`
  - `<datalist>`
  - `<dd>`
  - `<del>`
  - `<details>`
  - `<dfn>`
  - `<dialog>`
  - `<dir>`
  - `<div>`
  - `<dl>`
  - `<dt>`
  - `<em>`
  - `<embed>`
  - `<fieldset>`
  - `<figcaption>`
  - `<figure>`
  - `<font>`
  - `<footer>`
  - `<form>`
  - `<frame>`
  - `<frameset>`
  - `<h1>` to \<h6\></code>
  - `<head>`
  - `<header>`
  - `<hgroup>`
  - `<hr>`
  - `<html>`
  - `<i>`
  - `<iframe>`
  - `<img>`
  - `<input>`
  - `<ins>`
  - `<kbd>`
  - `<keygen>`
  - `<label>`
  - `<legend>`
  - `<li>`
  - `<link>`
  - `<map>`
  - `<mark>`
  - `<menu>`
  - `<meta>`
  - `<meter>`
  - `<nav>`
  - `<noframes>`
  - `<noscript>`
  - `<object>`
  - `<ol>`
  - `<optgroup>`
  - `<option>`
  - `<output>`
  - `<p>`
  - `<param>`
  - `<pre>`
  - `<progress>`
  - `<q>`
  - `<rp>`
  - `<rt>`
  - `<ruby>`
  - `<s>`
  - `<samp>`
  - `<script>`
  - `<section>`
  - `<select>`
  - `<small>`
  - `<source>`
  - `<span>`
  - `<strike>`
  - `<strong>`
  - `<style>`
  - `<sub>`
  - `<summary>`
  - `<sup>`
  - `<table>`
  - `<tbody>`
  - `<td>`
  - `<textarea>`
  - `<tfoot>`
  - `<th>`
  - `<thead>`
  - `<time>`
  - `<title>`
  - `<tr>`
  - `<track>`
  - `<tt>`
  - `<u>`
  - `<ul>`
  - `<var>`
  - `<video>`
  - `<wbr>`

## 주석 처리

{{-}}

  -

HTML(및 XML, SGML, SHTML)의 [주석은](../Page/주석_\(프로그래밍\).md "wikilink") doctype에 따라 [SGML](../Page/SGML.md "wikilink")이나 [XML](../Page/XML.md "wikilink")의 주석과 동일한 문법을 사용한다.

마크업 은 `Xbegin`를 만들어낸다.

주석은 문서 내 어디든 올 수 있으며 doctype 선언 이전에도 올 수 있다.

## 같이 보기

  - [문서 객체 모델](../Page/문서_객체_모델.md "wikilink")(DOM)
  - [자바스크립트](../Page/자바스크립트.md "wikilink")

## 각주

  - 내용주

## 외부 링크

  - HTML 4.01 (Dec 24, 1999): [elements](http://www.w3.org/TR/html401/index/elements.html) and [attributes](http://www.w3.org/TR/html401/index/attributes.html)

  - (Oct 28, 2014): [elements and attributes](http://www.w3.org/TR/html5/index.html)

[분류:HTML](https://ko.wikipedia.org/wiki/분류:HTML "wikilink")

1.  "Document" may refer interchangeably to either a file stored on a computer filesystem, usually on disk, or to a document delivered across the Web by [HTTP](../Page/HTTP.md "wikilink"). Such documents may equally be copies of disk files stored on the web server, or they may be generated on demand.
2.  The term "web browser" here is used for simplicity. It does of course include other sorts of [web user agent](https://ko.wikipedia.org/wiki/web_user_agent "wikilink"), such as search engine [web crawlers](../Page/웹_크롤러.md "wikilink"), automatic news-feed retrievers etc.
3.
4.
5.
6.  HTML 4.01 is one of a small number of well-known HTML DTDs. It is chosen here as the best illustrative example, although the same behavior applies to the other W3C-published DTDs for HTML.
7.
8.  Although see <object> for the inevitable exception.
9.  출처: <http://www.w3schools.com/tags/default.asp>