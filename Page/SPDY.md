> This article is converted from Wikipedia: [SPDY](https://ko.wikipedia.org/wiki/SPDY).


**SPDY**(스피디/*speedy*/로 발음)\[1\] 는 웹 콘텐츠를 전송할 목적으로 [구글](../Page/구글.md "wikilink")이 개발한 비표준 개방형 [네트워크 프로토콜이다](https://ko.wikipedia.org/wiki/네트워크_프로토콜 "wikilink"). SPDY는 [웹 페이지](../Page/웹_페이지.md "wikilink") 부하 레이턴시를 줄이고 [웹 보안을](../Page/월드_와이드_웹.md "wikilink") 개선하는 목표 면에서 [HTTP](../Page/HTTP.md "wikilink")와 비슷하다. SPDY는 압축, [다중화](https://ko.wikipedia.org/wiki/다중화 "wikilink"), 우선 순위 설정을 통한 레이턴시 감소를 달성한다.\[2\] "SPDY"는 구글의 [상표](../Page/상표.md "wikilink")이며 두문자어는 아니다.\[3\]

2015년 2월 구글은 [HTTP 2.0](https://ko.wikipedia.org/wiki/HTTP_2.0 "wikilink") [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")의 이점이 크기 때문에 2016년 5월 15일 부터 [크롬](https://ko.wikipedia.org/wiki/크롬 "wikilink") 브라우저에서의 SPDY 지원 기능을 제거하고 [TLS](https://ko.wikipedia.org/wiki/TLS "wikilink") 확장기능인 [NPN](https://ko.wikipedia.org/wiki/NPN "wikilink")과 그 후속버전인 [ALPN](https://ko.wikipedia.org/wiki/ALPN "wikilink") 기능을 제거할 것이라고 밝혔다.\[4\].

## 설계

SPDY는 웹 페이지의 로딩 시간을 줄이기 위한 목적으로 설계되었다.\[5\] 이를 위해 SPDY 클라이언트는 하나의 소켓 연결을 통해 페이지를 구성하는 여러개의 하위 요소를 한꺼번에 전송받을 수 있도록 만들어졌다.\[6\] 또한 항상 사람이 읽을 수 있는 형태의 헤더를 보내는 HTTP와 달리, SPDY 헤더는 [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink") 또는 [DEFLATE](../Page/DEFLATE.md "wikilink") 알고리즘으로 압축되어 적은 용량을 차지한다.\[7\] SPDY 서버는 클라이언트의 요청을 기다리지 않고, 페이지의 내용이 변경되었음을 클라이언트에 알리거나 새 변경내용을 직접 전송할 수 있다.

SPDY는 암호화되지 않은 연결을 지원하지 않으며, 반드시 [SSL](https://ko.wikipedia.org/wiki/SSL "wikilink") 또는 [TLS로](../Page/전송_계층_보안.md "wikilink") 암호화되어야 한다.

## HTTP 와의 관계

SPDY는 HTTP를 대체하는 프로토콜이 아니라, HTTP가 전송 계층을 통해 전송되는 방식을 재정의하는 프로토콜이다.\[8\] 따라서 전송 계층의 구현만 변경하면 기존 HTTP 서버 프로그램을 그대로 SPDY에서 사용할 수 있다.

SPDY는 HTTP 헤더를 해석하고 단순화하여 압축 전송한다. SPDY는 기존에 보냈던 HTTP 헤더와 같은 내용의 헤더가 재전송될 경우 다시 보내지 않고, 다른 내용의 헤더는 압축 전송함으로써 전송 시간을 절약한다.

[HTTP 2.0의](https://ko.wikipedia.org/wiki/HTTP_2.0 "wikilink") 초안에서 SPDY 규격이 참고되었다.\[9\]

## 표준화

2012년 7월에 SPDY 개발 그룹은 [인터넷 초안으로](https://ko.wikipedia.org/wiki/인터넷_초안 "wikilink") 이용 가능한 표준화 작업을 진행하고 있다고 발표했으나,\[10\] [HTTP 2.0](https://ko.wikipedia.org/wiki/HTTP_2.0 "wikilink") 초안 작업이 진행되면서 표준화 작업은 무산되었다. 구글은 [HTTP 2.0이](https://ko.wikipedia.org/wiki/HTTP_2.0 "wikilink") SPDY를 대체할 것이라고 밝힌 바 있다.

## 지원

SPDY는 [크로미엄](../Page/크로미엄_\(웹_브라우저\).md "wikilink")\[11\], [모질라 파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink")\[12\], [오페라](../Page/오페라_\(웹_브라우저\).md "wikilink")\[13\], [아마존 실크](https://ko.wikipedia.org/wiki/아마존_실크 "wikilink"), [인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink")\[14\], [사파리](../Page/사파리_\(웹_브라우저\).md "wikilink")\[15\] 등의 브라우저에 구현되어 있다.

## 같이 보기

  - [마이크로소프트 SM](https://ko.wikipedia.org/wiki/마이크로소프트_SM "wikilink")
  - [웹소켓](../Page/웹소켓.md "wikilink")

## 참조

<references />

## 외부 링크

  - [SPDY 문서](http://www.chromium.org/spdy)

  - [SPDY: Google wants to speed up the web by ditching HTTP](http://arstechnica.com/web/news/2009/11/spdy-google-wants-to-speed-up-the-web-by-ditching-http.ars)

  - [SPDY 백서](http://dev.chromium.org/spdy/spdy-whitepaper)

  - [아파치 SPDY 모듈](http://code.google.com/p/mod-spdy)

  - [SPDY 리뷰 및 분석](https://web.archive.org/web/20131127165400/https://www.varnish-cache.org/docs/trunk/phk/http20.html)

  - [SPDY 프로토콜 - RFC draft ietf httpbis http2-00](http://tools.ietf.org/html/draft-ietf-httpbis-http2-00)

[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:세션 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:세션_계층_프로토콜 "wikilink") [분류:월드 와이드 웹](https://ko.wikipedia.org/wiki/분류:월드_와이드_웹 "wikilink") [분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink")

1.
2.
3.
4.  <http://http2.github.io/faq/#whats-the-relationship-with-spdy>
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.