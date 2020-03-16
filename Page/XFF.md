> This article is converted from Wikipedia: [XFF](https://ko.wikipedia.org/wiki/XFF).


**XFF**(X-Forwarded-For)는 [HTTP 헤더](https://ko.wikipedia.org/wiki/HTTP_헤더 "wikilink") 중 하나로, 원래의 [IP 주소를](../Page/IP_주소.md "wikilink") 식별하기 위한 표준 헤더이다.

## 형식

필드의 일반적인 형식은 다음과 같다:

  -
    `X-Forwarded-For: client, proxy1, proxy2`\[1\]

## 대안

2014년을 기준으로 RFC 7239는 비슷한 목적에 XFF 대비 더 많은 기능을 제공하는 새로운 포워드 헤더를 표준화하였다.\[2\] 포워드 헤더의 문법의 예는 다음과 같다:

`Forwarded: for=192.0.2.60;proto=http;by=203.0.113.43`

HAProxy는 "XFF"의 대안을 도입하였고 이는 래퍼 PROXY 프로토콜의 파싱에 더 효율적이다.\[3\] 여러 전송 프로토콜에 사용 가능하며 내부 프로토콜의 점검이 필요하지 않으므로 HTTP에 국한되지 않는다.

## 같이 보기

  - [인터넷 프라이버시](../Page/인터넷_프라이버시.md "wikilink")

## 각주

[분류:익명](https://ko.wikipedia.org/wiki/분류:익명 "wikilink") [분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink")

1.
2.
3.  [Willy Tarreau: The PROXY protocol](http://haproxy.1wt.eu/download/1.5/doc/proxy-protocol.txt). haproxy.1wt.eu. Retrieved on 2012-12-24.