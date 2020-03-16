> This article is converted from Wikipedia: [WebDAV](https://ko.wikipedia.org/wiki/WebDAV).


**WebDAV**(Web Distributed Authoring and Versioning, 웹 분산 저작 및 버전 관리)는 [하이퍼텍스트 전송 프로토콜](https://ko.wikipedia.org/wiki/하이퍼텍스트_전송_프로토콜 "wikilink")(HTTP)의 확장으로, [월드 와이드 웹](../Page/월드_와이드_웹.md "wikilink") 서버에 저장된 문서와 파일을 편집하고 관리하는 사용자들 사이에 협업을 손쉽게 만들어 준다. [국제 인터넷 표준화 기구](../Page/국제_인터넷_표준화_기구.md "wikilink")(IETF)의 [작업 그룹은](https://ko.wikipedia.org/wiki/작업_그룹 "wikilink") RFC 4918로 WebDAV를 정의한다.

WebDAV 프로토콜은 웹을 읽고 쓰기가 가능한 매개체로 만든다.\[1\] 또, 사용자가 서버(일반적으로 웹 서버나 웹 공유) 의 문서를 만들고 변경하고 이동할 수 있는 프레임워크를 제공한다. WebDAV 프로토콜의 가장 중요한 기능에는 만든이나 수정 날짜에 대한 속성 관리,이름 공간 관리, 정보 수집, 덮어쓰기 보호를 포함한다. 속성 관리에는 파일 정보의 작성, 제거, 조회 등을 포함한다. 이름 공간 관리는 서버의 이름 공간 안에서 웹 페이지를 복사하고 이동할 수 있는 기능을 관할한다. 정보 수집은 다양한 자원의 작성, 제거, 나열을 관할한다. 끝으로, 덮어쓰기 보호는 파일 잠금과 관련된 측면들을 관리한다.

WebDAV 워킹 그룹은 [IESG](https://ko.wikipedia.org/wiki/IESG "wikilink")가 RFC 2518로의 증분 업데이트를 받아들인 뒤인 2007년 3월 그들의 작업은 종결되었다.

2011년 기준으로 현대의 수많은 [운영 체제는](../Page/운영_체제.md "wikilink") WebDAV 지원을 기본 내장하고 있다. WebDAV의 포트는 80, 443이며, RFC 2518, RFC 4918을 소유한다. OSI 계층은 애플리케이션 계층에 속한다.

## 역사

WebDAV는 [짐 화이트헤드가](https://ko.wikipedia.org/wiki/짐_화이트헤드 "wikilink") [W3C](../Page/W3C.md "wikilink")와 [월드 와이드 웹에서](../Page/월드_와이드_웹.md "wikilink") [분산 저작](https://ko.wikipedia.org/wiki/협업 "wikilink") 문제를 논의하기 위해 작업한 1996년에 시작되었다.\[2\]\[3\] [팀 버너스 리의](https://ko.wikipedia.org/wiki/팀_버너스_리 "wikilink") 원래의 웹 비전은 읽고 쓰기를 둘 다 하기 위한 매개체에 대한 것이었다. 버너스 리의 최초의 [웹 브라우저](../Page/웹_브라우저.md "wikilink") [월드와이드웹](../Page/월드와이드웹.md "wikilink")은 [웹 페이지를](../Page/웹_페이지.md "wikilink") 보고 편집하는 것이 가능했다. 그러나 웹이 성장함에 따라 대부분의 사용자들에게는 읽기 전용의 매개체가 되었다. 화이트헤드 및 그와 한 마음이 된 다른 사람들은 이러한 제한을 수정하길 바랐다.\[4\]

W3C 회의에서는 이러한 새로운 노력을 통해 [HTTP](../Page/HTTP.md "wikilink")의 확장으로서 IETF에서 표준화될 것으로 보고 [IETF](../Page/국제_인터넷_표준화_기구.md "wikilink") 작업 그룹을 창설하기로 결정하였다.

프로토콜에 대한 작업이 시작되었는데, 분산 저작 및 [버전 관리](../Page/버전_관리.md "wikilink") 둘 다 관리하는 것이 너무 많은 수고를 들일 수 밖에 없게 되어 작업이 분리될 것임이 분명해졌다. WebDAV 그룹은 분산 저작에 초점을 맞추었고 버전 관리는 나중으로 미루었다. 그 뒤 버전 관리는 델타-V 확장을 통해 추가되었다.

이 프로토콜은 HTTP에서 이용하기 위한 새로운 메소드와 헤더의 집합을 이룬다. 추가된 메소드는 다음과 같다:

  - PROPFIND
  - PROPPATCH
  - MKCOL
  - COPY
  - MOVE
  - LOCK
  - UNLOCK

## 같이 보기

  - [분산 파일 시스템](https://ko.wikipedia.org/wiki/분산_파일_시스템 "wikilink")
  - [콘텐츠 관리](../Page/콘텐츠_관리.md "wikilink")
  - [CalDAV](https://ko.wikipedia.org/wiki/CalDAV "wikilink")

## 참조

<references />

## 외부 링크

  - [WebDAV Resources](https://web.archive.org/web/20120626092812/http://webdav.org/)

  - [Davfs2 project](http://savannah.nongnu.org/projects/davfs2)

  - [Fusedav project](http://0pointer.de/lennart/projects/fusedav)

  - [WebDAV Apache modules](http://httpd.apache.org/docs/2.4/mod/mod_dav.html)

[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:작업 그룹](https://ko.wikipedia.org/wiki/분류:작업_그룹 "wikilink") [분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink") [분류:네트워크 파일 시스템](https://ko.wikipedia.org/wiki/분류:네트워크_파일_시스템 "wikilink")

1.
2.
3.
4.