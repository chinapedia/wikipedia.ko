> This article is converted from Wikipedia: [NNTP](https://ko.wikipedia.org/wiki/NNTP).


**NNTP**(Network News Transfer Protocol, 네트워크 뉴스 전송 프로토콜)는 [뉴스 서버](https://ko.wikipedia.org/wiki/뉴스_서버 "wikilink") 간에 [유즈넷](https://ko.wikipedia.org/wiki/유즈넷 "wikilink") 뉴스 기사(netnews)를 전송하고 최종 사용자 클라이언트 애플리케이션에 의해 기사를 구독, 게시할 수 있게 하기 위한 애플리케이션 [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")의 하나이다. 1986년 3월, [캘리포니아 대학교 샌디에이고의](https://ko.wikipedia.org/wiki/캘리포니아_대학교_샌디에이고 "wikilink") 브라이언 캔터(Brian Kantor)와 [캘리포니아 대학교 버클리의](https://ko.wikipedia.org/wiki/캘리포니아_대학교_버클리 "wikilink") [필 랩슬리가](https://ko.wikipedia.org/wiki/필_랩슬리 "wikilink") NNTP의 사양인 "RFC 977"을 만들었다. 다른 기여자들로는 [베일러 의과 대학의](https://ko.wikipedia.org/wiki/베일러_의과_대학 "wikilink") 스탠 O. 바버와 [애플 컴퓨터의](https://ko.wikipedia.org/wiki/애플_컴퓨터 "wikilink") 에릭 페어가 있다.

[잘 알려진 TCP 포트 119가](https://ko.wikipedia.org/wiki/TCP/UDP의_포트_목록 "wikilink") NNTP를 위해 예비되었다. 하나의 서버에서 다른 서버로 대량의 기사를 전송할 경우 TCP 포트 433(**NNSP**)을 사용할 수 있다. 클라이언트가 뉴스 서버에 [전송 계층 보안](https://ko.wikipedia.org/wiki/전송_계층_보안 "wikilink")(TLS)로 접속할 때, TCP 포트 563이 종종 사용된다. (이를 가끔 **NNTPS**로 부른다.) 대안으로, 포트 119을 경유한 플레인 텍스트 연결은 STARTTLS 명령을 실행, TLS를 사용하는 것으로 변경할 수 있다.

2006년 10월, IETF는 NNTP를 업데이트하고 RFC 977 이후로 수년에 걸쳐 만들어놓은 추가 사항 중 다수를 편성한 "RFC 3977"을 출시하였다. 동시에, IETF는 또한 [STARTTLS](https://ko.wikipedia.org/wiki/STARTTLS "wikilink")를 실행, NNTP를 경유하는 [전송 계층 보안](https://ko.wikipedia.org/wiki/전송_계층_보안 "wikilink")(TLS)의 사용을 규정한 "RFC 4642"를 출시하였다.

## 같이 보기

  - [뉴스 서버](https://ko.wikipedia.org/wiki/뉴스_서버 "wikilink")
  - [뉴스그룹](https://ko.wikipedia.org/wiki/뉴스그룹 "wikilink")

## 외부 링크

  - Kantor, Brian and Phil Lapsley. RFC 977 "Network News Transfer Protocol: A Proposed Standard for the Stream-Based Transmission of News." 1986.

  -
  -
[분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:인터넷 표준](https://ko.wikipedia.org/wiki/분류:인터넷_표준 "wikilink") [분류:유즈넷](https://ko.wikipedia.org/wiki/분류:유즈넷 "wikilink")