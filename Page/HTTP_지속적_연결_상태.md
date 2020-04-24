> This article is converted from Wikipedia: [HTTP 지속적 연결 상태](https://ko.wikipedia.org/wiki/HTTP_지속적_연결_상태).


**HTTP 지속적 연결 상태**, **HTTP 영구 접속**(HTTP persistent connection) 또는 **HTTP 킵얼라이브**(HTTP keep-alive), **HTTP 연결 재사용**(HTTP connection reuse)은 하나의 [TCP](../Page/전송_제어_프로토콜.md "wikilink") 연결을 사용하여 복수의 [HTTP 요청](../Page/HTTP.md "wikilink")/응답을 주고받는다는 개념으로, 매 요청/응답 쌍마다 새로운 요청을 여는 것과는 반대되는 개념이다. 더 새로운 [HTTP/2](https://ko.wikipedia.org/wiki/HTTP/2 "wikilink") 프로토콜은 동일한 개념을 사용하며 더 나아가 하나의 연결 복수의 동시 요청/응답을 다중화하는 것이 가능하다.

## 웹 브라우저에서의 사용

[섬네일](https://ko.wikipedia.org/wiki/파일:HTTP_persistent_connection.svg "wikilink") [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink"), [모질라 파이어폭스](../Page/모질라_파이어폭스.md "wikilink"), [인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") (4.01 이후), [오페라](../Page/오페라_\(웹_브라우저\).md "wikilink") (4.0 이후)\[1\], [사파리](../Page/사파리_\(웹_브라우저\).md "wikilink") 등 현대의 모든 웹 브라우저는 영구 접속을 지원한다.

기본적으로 [인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") 버전 6과 7은 2개의 영구 접속을 사용하는 반면 버전 8은 6개를 사용한다.\[2\] 영구 접속 타임아웃은 비활동 후 60초이며 이 수치는 윈도우 레지스트리를 통해 변경이 가능하다.\[3\]

[모질라 파이어폭스에서](../Page/모질라_파이어폭스.md "wikilink") 동시 접속 수는 사용자가 직접 지정할 수 있다.(서버별, 프록시별, 또는 전체적으로) 영구 접속 타임아웃은 비활동 후 115초이며 구성을 통해 변경이 가능하다.\[4\]

## 같이 보기

  - [HTTP 파이프라이닝](https://ko.wikipedia.org/wiki/HTTP_파이프라이닝 "wikilink")
  - [HTTP/2](https://ko.wikipedia.org/wiki/HTTP/2 "wikilink")

## 각주

## 외부 링크

  - [Hypertext Transfer Protocol (HTTP/1.1): Message Syntax and Routing, Connection Management, Persistence](http://tools.ietf.org/html/rfc7230#section-6.3)
  - [Persistent Connection Behavior of Popular Browsers (dated)](http://www.cs.wisc.edu/~cao/papers/persistent-connection.html)
  - [Apache HTTPD Keep-Alive Support](http://httpd.apache.org/docs/current/mod/core.html#keepalive)
  - [Network Performance Effects of HTTP/1.1, CSS1, and PNG](http://conferences.sigcomm.org/sigcomm/1997/papers/p102.html)

[분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink")

1.
2.
3.
4.