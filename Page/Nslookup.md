> This article is converted from Wikipedia: [Nslookup](https://ko.wikipedia.org/wiki/Nslookup).


**nslookup**은 네트워크 관리 [명령 줄 인터페이스](../Page/명령_줄_인터페이스.md "wikilink") 도구로서 많은 컴퓨터 [운영 체제에서](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 사용 가능하며, [도메인 네임을](https://ko.wikipedia.org/wiki/도메인_네임 "wikilink") 얻거나 IP 주소 매핑 또는 다른 특정한 [DNS 레코드를](https://ko.wikipedia.org/wiki/DNS_레코드 "wikilink") [도메인 네임 시스템](https://ko.wikipedia.org/wiki/도메인_네임_시스템 "wikilink")(DNS)에 질의할 때 사용된다.

[BIND](https://ko.wikipedia.org/wiki/BIND "wikilink") 9의 개발 이전에 인터넷 시스템 컨소시엄은 nslookup을 반대하고 [host](https://ko.wikipedia.org/wiki/host "wikilink")와 [dig](https://ko.wikipedia.org/wiki/dig "wikilink")로 대체하려고 계획하였다. 그러나 이 결정은 2004년에 BIND 9.3의 배포와 함께 번복되었고\[1\] 이후 nslookup은 완전하게 지원되고 있다.

## 배경

"nslookup"의 이름은 "name server lookup"을 의미한다. nslookup은 운영 체제의 로컬 도메인 네임 시스템 리졸버 라이브러리를 사용해서 자신의 쿼리를 수행하지 않으므로 dig와는 다른 행동을 한다. 추가적으로 벤더에 의해 제공된 버전들은 다른 이름 정보의 소스의 결과를 사용하거나 포함함으로써 혼란을 일으킬 수 있다. ([호스트 파일](../Page/Hosts.md "wikilink"), [네트워크 정보 서비스](../Page/네트워크_정보_서비스.md "wikilink") 같은) 몇몇 행동들은 [resolv.conf](https://ko.wikipedia.org/wiki/resolv.conf "wikilink") 파일의 내용에 따라 수정될 수 있다.\[2\]

## 사용

nslookup은 상호 또는 비 상호 모드로 동작한다. 인자 없이 또는 첫 번째 인자를 -(마이너스)로, 두 번째 인자를 네임 서버의 [호스트명](../Page/호스트명.md "wikilink")이나 인터넷 주소 넣은 경우 상호작용을 하게 되며 사용자는 nslookup 프롬프트(\>)에서 파라미터 설정을 하거나 요청을 할 수 있다. 인자가 주어지지 않은 경우, 명령어는 기본 서버에 질의한다. -(마이너스)는 명령 줄에서 특정되는 부명령어를 유발하며, nslookup 명령어에 선행되어야 한다. 비 상호 모드에서, 즉 첫 번째 인자가 검색할 호스트의 이름이나 IP 주소인 경우 파라미터들과 질의는 화면에서 결과로 나온다. 비 상호 모드는 기본 네임 서버를 사용해서 특정한 호스트의 정보를 검색한다.\[3\]

## 같이 보기

  - [whois](https://ko.wikipedia.org/wiki/후이즈 "wikilink") : 인터넷 도메인과 IP 주소를 질의하기 위한 툴

## 각주

## 외부 링크

  - 마이크로소프트 윈도우
      - [nslookup](http://technet.microsoft.com/en-us/library/bb490721.aspx) – [마이크로소프트 테크넷](https://ko.wikipedia.org/wiki/마이크로소프트_테크넷 "wikilink") 라이브러리
      - [Using NSlookup.exe](http://support.microsoft.com/kb/200525/), Microsoft Knowledge Base
  - 유닉스 계열 운영체제
      -
  - 기타
      - (nslookup의 웹 버전 포함)

[분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:DNS 소프트웨어](https://ko.wikipedia.org/wiki/분류:DNS_소프트웨어 "wikilink") [분류:인터넷 프로토콜 기반 네트워크 소프트웨어](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜_기반_네트워크_소프트웨어 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")

1.
2.
3.