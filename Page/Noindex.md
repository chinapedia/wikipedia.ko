> This article is converted from Wikipedia: [Noindex](https://ko.wikipedia.org/wiki/Noindex).


HTML 로봇 메타 태그 중 **noindex** 값은 자동화 인터넷 봇이 [웹 페이지의](../Page/웹_페이지.md "wikilink") 색인(인덱스) 처리를 하지 못하도록 요청한다.\[1\]<ref>\[<http://www.robotstxt.org/meta.html> About the Robots

<META>

tag\]</ref> 이 메타 태그를 사용하는 이유로는 로봇이 매우 큰 데이터베이스, 매우 변화가 많은 웹 페이지, 개발 중인 웹 페이지, 조금 더 비공개로 유지하기를 원하는 웹 페이지, 프린터/모바일 친화 버전의 페이지를 색인 처리하지 못하게 하는 일이 포함된다. 웹사이트 noindex 태그를 검사하는 책임은 검색 로봇의 개발자에게 부여되기 때문에 이 태그들은 무시되기도 한다. 또, noindex 태그를 해석하는 방식은 검색 엔진 회사마다 조금씩 다른 경우가 있다.

## 모든 문서의 noindex 처리

``` html4strict
<html>
<head>
  <meta name="robots" content="noindex">
  <title>Don't index this page</title>
</head>
```

메타 태크 콘텐츠의 이용 가능한 값은 다음과 같다: "none", "all", "index", "noindex", "nofollow", "follow". 값들의 조합 또한 가능한데,\[2\] 예를 들면 다음과 같다:

``` html4strict
<meta name="robots" content="noindex, follow">
```

### 봇 특화 디렉티브

noindex 디렉티브는 메타 태그에 각기 다른 "name" 값을 지정함으로써 특정 봇에만 한정하여 제한시킬 수 있다.

이를테면, 구글 봇만 특정해서 차단하려면,\[3\] 다음과 같이 지정한다:

``` html4strict
<meta name="googlebot" content="noindex">
```

야후의 봇을 차단하려면,\[4\] 다음과 같이 지정한다:

``` html4strict
<meta name="slurp" content="noindex">
```

MSN의 봇을 차단하려면 다음을 지정한다:

``` html4strict
<meta name="msnbot" content="noindex">
```

### robots.txt 파일

[robots.txt](../Page/로봇_배제_표준.md "wikilink") 파일을 사용하여 크롤링을 차단할 수 있다.

## 페이지 일부의 noindex 처리

이를테면 내비게이션 텍스트처럼 웹페이지의 일부분을 색인 처리하지 못하도록 배제시키는 것이 가능하다. 이를 위한 다양한 기법들이 있으며 조합하여 여러 개를 사용할 수 있다. 구글의 주 인덱싱 스파이더 [구글봇](../Page/구글봇.md "wikilink")은 이 기법들을 인식하는 것으로 확인되지는 않고 있다.

### <noindex> 태그

러시아의 검색 엔진 [얀덱스](../Page/얀덱스.md "wikilink")는 태그 간 내용의 색인 처리를 방지하는 \<noindex\> 태그를 선보였다. 소스 코드 확인을 허용하기 위해, \<\!--noindex--\>를 대신 사용할 수 있다:\[5\]

``` html4strict
<p>
이 텍스트는 색인 처리된다.
<noindex>이 텍스트는 색인 처리되지 않는다.</noindex>
<!--noindex-->이 텍스트는 색인 처리되지 않는다.<!--/noindex-->
</p>
```

[Atomz](https://ko.wikipedia.org/wiki/Atomz "wikilink")를 포함한 다른 [인덱싱 스파이더](../Page/웹_크롤러.md "wikilink") 또한 \<noindex\> 태그를 인식한다.\[6\]

### 마이크로포맷

동일한 기능을 갖춘 2005년 [마이크로포맷](../Page/마이크로포맷.md "wikilink") 초안 사양이 있다. 로봇 배제 프로파일은 HTML 태그의 *class="robots-noindex"*의 속성과 값을 찾는다:\[7\]

``` html4strict
<p>이 텍스트는 색인 처리된다.</p>
<div class="robots-noindex">이 텍스트는 색인 처리되지 않는다.</div>
<span class="robots-noindex">이 텍스트는 색인 처리되지 않는다.</span>
<p class="robots-noindex">이 텍스트는 색인 처리되지 않는다.</p>
```

여러 값들을 조합하는 것도 가능한데,\[8\] 이를테면 다음과 같다:

``` html4strict
<div class="robots-noindex robots-follow">텍스트.</div>
```

### 야후\!

2007년, [야후\!](../Page/야후!.md "wikilink")는 자사의 스파이더에 마이크로포맷과 비슷한 기능을 도입했다. 그러나 야후\!의 스파이더는 *class="robots-nocontent"* 값과는 호환되지 않으며 다음의 값만 찾는다:\[9\]

``` html4strict
<p>이 텍스트는 색인 처리된다.</p>
<div class="robots-nocontent">이 텍스트는 색인 처리되지 않는다.</div>
<span class="robots-nocontent">이 텍스트는 색인 처리되지 않는다.</span>
<p class="robots-nocontent">이 텍스트는 색인 처리되지 않는다.</p>
```

### 셰어포인트

[셰어포인트](../Page/셰어포인트.md "wikilink") 2010의 iFilter는 *class="noindex"*의 속성과 값이 있는 \<div\> 태그 내부의 내용을 배제시킨다. 내부 \<div\>는 내부적으로는 배제되지 않으나 변경된 상태일 수 있다. 속성이 \<div\> 이외의 태그에 적용될 수 있는지의 여부는 알려져 있지 않다.\[10\]

``` html4strict
<p>이 텍스트는 색인 처리된다.</p>
<div class="noindex">이 텍스트는 색인 처리되지 않는다.</div>
```

### 구조화된 코멘트

[구글 검색 어플라이언스는](https://ko.wikipedia.org/wiki/구글_검색_어플라이언스 "wikilink") 구조화된 코멘트를 사용한다:\[11\]

``` html4strict
<p>
이 텍스트는 색인 처리된다.
<!--googleoff: all-->
이 텍스트는 색인 처리되지 않는다.
<!--googleon: all-->
</p>
```

다른 인덱싱 스파이더는 자신만의 구조화된 코멘트를 사용한다.

## 같이 보기

  - [nofollow](https://ko.wikipedia.org/wiki/nofollow "wikilink") 링크 속성
  - [로봇 배제 표준](../Page/로봇_배제_표준.md "wikilink")

## 각주

[분류:월드 와이드 웹](https://ko.wikipedia.org/wiki/분류:월드_와이드_웹 "wikilink")

1.  [Robots and the META element](http://www.w3.org/TR/html401/appendix/notes.html#h-B.4.1.2), Official W3 specification
2.
3.  [Using meta tags to block access to your site](http://www.google.com/support/webmasters/bin/answer.py?hl=en&answer=93710), Google Webmasters Tools Help
4.  [How to Prevent Yahoo\! Search From Indexing Specific Pages](http://help.yahoo.com/l/us/yahoo/search/indexing/slurp-04.html), Yahoo\! Search Help
5.
6.
7.
8.
9.
10.
11.