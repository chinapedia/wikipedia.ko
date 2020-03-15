> This article is converted from Wikipedia: [HTTP 403](https://ko.wikipedia.org/wiki/HTTP_403).


[월드 와이드 웹에](../Page/월드_와이드_웹.md "wikilink") 쓰이는 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink") 프로토콜에서 **403 Forbidden**은 서버가 허용하지 않는 웹 페이지나 미디어를 사용자가 요청할 때 [웹 서버가](../Page/웹_서버.md "wikilink") 반환하는 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink") 상태 코드이다. 다시 말해, 클라이언트가 서버에 도달할 수 있어도 서버가 페이지 접근 허용을 거부했다는 것을 뜻한다. 이러한 응답은 디렉터리 나열이 비활성화되어 있을 때 [아파치](https://ko.wikipedia.org/wiki/아파치_웹_서버 "wikilink") 웹 서버가 반환한다. 마이크로소프트 [IIS](../Page/인터넷_정보_서비스.md "wikilink") 또한 디렉터리 나열이 거부되면 동일한 방식으로 응답한다. (클라이언트가 [웹DAV](https://ko.wikipedia.org/wiki/웹DAV "wikilink") PROFIND를 요청하는 경우에도 서버가 이러한 응답을 반환할 수 있다.)\[1\]

## 403 하부 오류 코드 메시지

아래의 메시지는 IIS 기준이다.

  - 403.1 - 실행 접근 금지.
  - 403.2 - 읽기 접근 금지.
  - 403.3 - 쓰기 접근 금지.
  - 403.4 - SSL 필요.
  - 403.5 - SSL 128 필요.
  - 403.6 - IP 주소 거부.
  - 403.7 - 클라이언트 인증서 필요.
  - 403.8 - 사이트 접근 거부.
  - 403.9 - 너무 많은 사용자.
  - 403.10 - 잘못된 구성.
  - 403.11 - 암호 변경.
  - 403.12 - 매퍼가 접근을 거부함.
  - 403.13 - 클라이언트 인증 철회(무효).
  - 403.14 - 디렉터리 나열 거부.
  - 403.15 - 클라이언트 접근 라이선스 수 초과.
  - 403.16 - 클라이언트 인증서를 신뢰할 수 없거나 유효하지 않음.
  - 403.17 - 클라이언트 인증서의 기간이 초과되었거나 아직 유효하지 않음.
  - 403.18 - 해당 응용 프로그램 풀로부터 요청을 실행할 수 없음.

## 각주

<references />

## 같이 보기

  - [.htaccess](https://ko.wikipedia.org/wiki/.htaccess "wikilink")
  - [HTTP 상태 코드](https://ko.wikipedia.org/wiki/HTTP_상태_코드 "wikilink")
  - [다시쓰기 엔진](https://ko.wikipedia.org/wiki/다시쓰기_엔진 "wikilink")

[분류:HTTP 상태 코드](https://ko.wikipedia.org/wiki/분류:HTTP_상태_코드 "wikilink")

1.