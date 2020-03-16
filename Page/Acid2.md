> This article is converted from Wikipedia: [Acid2](https://ko.wikipedia.org/wiki/Acid2).


[섬네일](https://ko.wikipedia.org/wiki/파일:Acid2_reference.png "wikilink")

**Acid2**는 [웹 표준 프로젝트가](https://ko.wikipedia.org/wiki/웹_표준_프로젝트 "wikilink") [HTML](../Page/HTML.md "wikilink")을 렌더링하는 [웹 브라우저와](../Page/웹_브라우저.md "wikilink") 다른 응용 프로그램들에서 [웹 페이지](../Page/웹_페이지.md "wikilink") [렌더링](../Page/렌더링.md "wikilink") 결점을 파악하기 위해 고안한 테스트 제품군이다. Acid2는 [2005년](../Page/2005년.md "wikilink") [4월 12일에](../Page/4월_12일.md "wikilink") 출시되었다. [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink") 표준에 순응하는 상대적으로 편협적인 테스트인 [Acid1](../Page/Acid1.md "wikilink")의 정신을 이어받아 개발하였다. 모든 웹 acid 테스트와 같이, 웹 브라우저의 표시 방식이 참조 렌더링과 비슷하면 렌더링 결과물이 가장 잘 표시되었다고 할 수 있다. 두 개의 그림이 일치하면 브라우저는 테스트를 통과한다고 판단 받는다.

Acid2 테스트는 HTML, 특히 CSS의 기능을 다룬다. 이러한 기능들을 테스트하는 목적은 HTML을 렌더링하는 응용 프로그램의 표준 준수 부족을 알아내는 것이다. Acid2 테스트는 [W3C](../Page/W3C.md "wikilink") HTML와 CSS 2.0 규격을 따르는 브라우저라면 올바르게 렌더링해야 한다.

[2005년](../Page/2005년.md "wikilink") [10월 31일에](../Page/10월_31일.md "wikilink") [사파리](../Page/사파리_\(웹_브라우저\).md "wikilink") 2.0.2가 이 테스트를 가장 먼저 통과한 브라우저가 되었다. [오페라](../Page/오페라_\(웹_브라우저\).md "wikilink"), [컨커러](https://ko.wikipedia.org/wiki/컨커러 "wikilink"), [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 등이 그 뒤를 이었다. 이 테스트를 아직 통과하지 못한 유일한 주된 브라우저는 [인터넷 익스플로러이지만](../Page/인터넷_익스플로러.md "wikilink") [인터넷 익스플로러 8은](../Page/인터넷_익스플로러_8.md "wikilink") Acid2를 준수하였다.

## 테스트 받는 표준

Acid2는 웹 페이지가 기록되는 언어인 [HTML](../Page/HTML.md "wikilink")과 관련한 다양한 [웹 표준과](../Page/웹_표준.md "wikilink") 포맷을 지정하는 데 선호되는 방식인 [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink"), 스타일, HTML 레이아웃을 테스트한다.\[1\]

  - [PNG](../Page/PNG.md "wikilink") 포맷 이미지의 [알파 투명도](../Page/알파_채널.md "wikilink")
  - [객체 요소](../Page/HTML_요소.md "wikilink")
  - [data: URI scheme](https://ko.wikipedia.org/wiki/data:_URI_scheme "wikilink")
  - 절대적, 상대적, 고정 CSS 위치 제어
  - CSS 상자 모델
  - CSS 표
  - CSS가 만들어 낸 콘텐츠
  - CSS 파싱
  - 그리기 순서
  - 떠다니는 효과

Acid2가 완전한 테스트는 아니기 때문에 특정한 표준의 완전한 준수를 보증하지 않는다. URI 지원은 웹 표준 프로젝트에서 이용할 수 있다.\[2\]

## 파싱 조건

파싱 점수는 브라우저의 기본값을 사용할 때에만 유효하다고 판단한다. 글꼴 크기를 바꾸고, 크기를 조절하고 사용자 정의 스타일시트를 적용하는 등의 동작들은 테스트의 표시를 망가트릴 수 있다. 이는 예측된 바이며 브라우저의 테스트 준수와는 관계가 없다.\[3\]

다음의 브라우저 설정들과 사용자 동작들은 테스트를 무효로 만든다:\[4\]

  - 스크롤링
  - 브라우저 창 크기 조절
  - 확대/축소
  - 그림 사용 안함
  - 오페라의 "Fit to Width", "Small Screen Rendering modes" 사용
  - 사용자 정의 글꼴, 색, 스타일 등 적용
  - 사용자 자바스크립트나 [Greasemonkey](https://ko.wikipedia.org/wiki/Greasemonkey "wikilink") 스크립트

## 호환되지 않는 응용 프로그램

파일:Ieacid2.png|[인터넷 익스플로러 6](../Page/인터넷_익스플로러_6.md "wikilink") 파일:Ie7acid2.png|[인터넷 익스플로러 7](../Page/인터넷_익스플로러_7.md "wikilink") 파일:Acid2 NS72.png|[파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 1.0, [모질라](../Page/모질라_애플리케이션_스위트.md "wikilink") 1.7.13, [카미노](../Page/카미노.md "wikilink") 1.6, [넷스케이프](../Page/넷스케이프_\(웹_브라우저\).md "wikilink") 7.2 파일:Firefoxacid2.png|[파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 1.5 및 2.0, [씨몽키](https://ko.wikipedia.org/wiki/씨몽키 "wikilink") 1.1 파일:Opera 8.0 Acid2.png|[오페라](../Page/오페라_\(웹_브라우저\).md "wikilink") 8.0 파일:Opera 8.54 Acid2.png|[오페라](../Page/오페라_\(웹_브라우저\).md "wikilink") 8.54 파일:Konqueror 3.4.1 Acid2.png|[캉커러](../Page/캉커러.md "wikilink") 3.4 파일:Netsurf-1.2-acid2.png|[넷서프](../Page/넷서프.md "wikilink") 1.2 파일:NetSurf-3.0-acid2.png|2011년 2분기의 [넷서프](../Page/넷서프.md "wikilink") 3.0 파일:Acid2 in Opera Mini 4.png|[오페라 미니](../Page/오페라_미니.md "wikilink") 4 파일:Nokia Nst-4 Acid2.png|[Nst OS](../Page/심비안_OS.md "wikilink") 3.1.9에서의 Nokia Nst-4 파일:Acid2iPod.png|[MobileSafari](../Page/사파리_\(웹_브라우저\).md "wikilink") 3.1 파일:BBStormAcid2.jpg|[블랙베리 스톰 브라우저](https://ko.wikipedia.org/wiki/블랙베리_스톰 "wikilink") 4.7.0.122 파일:WebOS v1.4.0 Acid2.png|[Palm Pre / webOS](https://ko.wikipedia.org/wiki/webOS "wikilink") v1.4.0

[오페라 미니가](../Page/오페라_미니.md "wikilink") [개인 컴퓨터를](https://ko.wikipedia.org/wiki/개인_컴퓨터 "wikilink") 위한 [오페라와](../Page/오페라_\(웹_브라우저\).md "wikilink") 같은 렌더링 엔진을 기반으로 하고 있지만 Acid2 테스트를 통과하지는 못하였다.\[5\]\[6\] 왜냐하면 오페라 미니는 의도적으로 웹 페이지의 포맷을 바꿈으로써 작은 화면이 있는 장치에 알맞게 바꾸어 놓기 때문이다. \[7\]\[8\]

## 같이 보기

  - [Acid1](../Page/Acid1.md "wikilink")
  - [Acid3](../Page/Acid3.md "wikilink")
  - [레이아웃 엔진](https://ko.wikipedia.org/wiki/레이아웃_엔진 "wikilink")

## 각주

<references />

## 외부 링크

  - [Acid2 테스트](http://acid2.acidtests.org/#top)
  - [Acid2 테스트 결과](https://web.archive.org/web/20080726023904/http://acidtests.googletoad.com/)
  - [Acid2 테스트 정보](http://www.webstandards.org/action/acid2/)
  - [주요 브라우저의 Acid 2](http://www.howtocreate.co.uk/acid/)
  - [웹 표준 프로젝트의 Acid 테스트 모음](http://www.acidtests.org/)
  - [2005년 4월 13일: 웹 표준 프로젝트 언론 공개](http://www.webstandards.org/press/releases/20050413//)
  - [Acid2 테스트를 제안하는 CNET 문서](http://www.news.com/The-Acid2-challenge-to-Microsoft/2010-1032_3-5618723.html)
  - [Acid2 - 사파리, iCab, 컨커러에 대한 사실](http://www.snailshell.de/blog/archives/2005/11/entry_22.html)
  - [Acid2 타임라인](http://www.hyperborea.org/journal/archives/2005/11/01/acid2-timeline/)

[분류:Acid 테스트](https://ko.wikipedia.org/wiki/분류:Acid_테스트 "wikilink") [분류:웹 디자인](https://ko.wikipedia.org/wiki/분류:웹_디자인 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.