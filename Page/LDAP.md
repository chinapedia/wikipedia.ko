> This article is converted from Wikipedia: [LDAP](https://ko.wikipedia.org/wiki/LDAP).


**경량 디렉터리 액세스 프로토콜**()은 [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink") 위에서 [디렉터리 서비스를](https://ko.wikipedia.org/wiki/디렉터리_서비스 "wikilink") 조회하고 수정하는 [응용 프로토콜이다](../Page/응용_계층.md "wikilink").

디렉터리는 논리, 계급 방식 속에서 조직화된, 비슷한 특성을 가진 객체들의 모임이다. 가장 일반적인 예로는 전화 번호부(telephone directory)가 있는데 가나다 순의 일련의 이름을 가지고 있고, 이름마다 전화 번호와 주소가 포함되어 있다. 이러한 기본 설계 때문에 LDAP는 인증을 위한 다른 서비스에 의해 자주 사용된다.

[LDAP 디렉터리 트리는](https://ko.wikipedia.org/wiki/디렉터리_정보_트리 "wikilink") 선택된 모델에 따라 다양한 정치적, 지질학적, 조직적 경계를 반영하기도 한다. 오늘날 LDAP의 배치는 최상위 수준의 계급을 구조화하기 위해 [도메인 이름 서비스의](https://ko.wikipedia.org/wiki/도메인_이름_서비스 "wikilink") 이름을 사용하는 경향이 있다. 디렉터리 안에 들어가면 들어갈수록 사람들, 조직, 프린터, 문서, 그룹 등을 대표하는 항목들이 나타난다.

LDAP의 현재 버전은 LDAPv3이다.

## 프로토콜 개요

클라이언트는 다음의 작업을 요청할 수 있다:

  - StartTLS — 보안 접속을 위해 LDAPv3 [TLS](https://ko.wikipedia.org/wiki/TLS "wikilink") 확장을 사용한다
  - Bind — LDAP 프로토콜 버전의 [인증](../Page/인증.md "wikilink") 및 지정한다
  - Search — 디렉터리 엔트리의 검색 및 확인한다
  - Compare — 명명된 엔트리가 주어진 특성 값을 포함하는지 시험한다
  - 새로운 엔트리를 추가한다
  - 엔트리를 지운다
  - 엔트리를 수정한다
  - DN(Distinguished Name)을 수정한다 — 엔트리를 이동하거나 엔트리의 이름을 바꾼다
  - Abandon — 이전의 요청을 중단한다
  - Extended Operation — 다른 오퍼레이션을 정의하기 위해 사용되는 일반적인 오퍼레이션
  - Unbind — 연결을 닫는다 (Bind의 반대가 아님)

## URI 스킴

클라이언트가 다양한 정도로 지원하는 LDAP [URI](../Page/통합_자원_식별자.md "wikilink") 스킴이 있으며 서버는 참조에 의거하여 반환한다. (RFC 4516 참고)

<ldap://host:port/DN?attributes?scope?filter?extensions>

## 같이 보기

  - [디렉터리 서비스](https://ko.wikipedia.org/wiki/디렉터리_서비스 "wikilink")
  - [X.500](../Page/X.500.md "wikilink")

## 더 읽기

  -
  -
  -
  -
  -
  -
[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:오픈 그룹 표준](https://ko.wikipedia.org/wiki/분류:오픈_그룹_표준 "wikilink")