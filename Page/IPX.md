> This article is converted from Wikipedia: [IPX](https://ko.wikipedia.org/wiki/IPX).


**IPX**(Internetwork Packet Exchange의 준말)는 [IPX/SPX](https://ko.wikipedia.org/wiki/IPX/SPX "wikilink") [프로토콜 스택](https://ko.wikipedia.org/wiki/프로토콜_스택 "wikilink") 안에 있는 [OSI 모델](https://ko.wikipedia.org/wiki/OSI_모델 "wikilink") [네트워크 계층](../Page/네트워크_계층.md "wikilink") [프로토콜이다](../Page/통신_프로토콜.md "wikilink").

IPX/SPX 프로토콜 스택은 [노벨사의](https://ko.wikipedia.org/wiki/노벨_\(기업\) "wikilink") [넷웨어](https://ko.wikipedia.org/wiki/노벨_넷웨어 "wikilink") [네트워크 운영 체제의](../Page/네트워크_운영_체제.md "wikilink") 지원을 받는다. 넷웨어가 1980년대 후반부터 1990년대 중반까지 인기가 있자, IPX는 [인터네트워킹](https://ko.wikipedia.org/wiki/인터네트워킹 "wikilink") 프로토콜로 잘 알려지게 되었다. 노벨은 IPX를 [제록스 네트워크 서비스](https://ko.wikipedia.org/wiki/제록스_네트워크_서비스 "wikilink") IDP 프로토콜에서 가져온 것이다.

[인터넷](../Page/인터넷.md "wikilink") 붐에 따른 [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink")의 인기로 인해, IPX는 쇠퇴의 길을 걷고 만다. 컴퓨터와 네트워크는 여러 개의 네트워크 프로토콜을 실행할 수 있기에 거의 모든 IPX 사이트는 인터넷 연결을 위해 TCP/IP로 돌아가게 된다. 또한 넷웨어 버전이 5 이상으로 올라가면서 IPX와 TCP/IP 둘 다 지원하게 되자, 노벨사의 제품은 IPX 없이 실행할 수도 있다.

## IPX의 주소매김

  - 논리 네트워크는 32비트 고유 [16진수](https://ko.wikipedia.org/wiki/16진법 "wikilink") 주소를 할당 받는다. (범위 0x1 부터 0xFFFFFFFE까지)
  - 호스트는 48비트 노드 주소를 가진다. 기본적으로 랜 카드의 [맥 주소로](https://ko.wikipedia.org/wiki/맥_주소 "wikilink") 설정된다. 이 노드 주소는 네트워크 주소에 추가하여 네트워크 호스트를 위한 고유 인증자를 만든다.
  - 네트워크 주소 00:00:00:00은 현재의 네트워크 주소임을 뜻한다.
  - 브로드캐스트(전체로 뿌리는)주소는 FF:FF:FF:FF이다.

### IP와의 유사성

IPX 네트워크 주소는 개념상 [IP 주소의](../Page/IP_주소.md "wikilink") 네트워크 일부와 동일하다. ([넷마스크](https://ko.wikipedia.org/wiki/서브네트워크 "wikilink") 비트가 1로 설정되는 부분) 노드 주소는 "넷마스크 비트가 1로 설정된 IP 주소의 비트"와 뜻이 일치한다. 노드 주소가 보통 네트워크 어댑터의 맥 주소와 동일하므로 [주소 결정 프로토콜은](../Page/주소_결정_프로토콜.md "wikilink") 필요하지 않다.

[라우팅](../Page/라우팅.md "wikilink")의 경우, IPX [라우팅 테이블의](../Page/라우팅_테이블.md "wikilink") 항목은 IP 라우팅 테이블과 비슷하다. 라우팅은 네트워크 주소를 통해 완성되며 각 네트워크 주소의 경우 다음 라우터의 네트워크:노드가, IP 주소/넷마스크가 IP 라우팅 테이블 안에서 지정되는 것과 비슷한 방식으로 지정된다.

### 이더넷 위의 IPX

IPX는 다음과 같이 4가지 형태를 사용하여 이더넷을 통해 전송할 수 있다.

  - [802.3](https://ko.wikipedia.org/wiki/IEEE_802.3 "wikilink") (원본)
  - [802.2](https://ko.wikipedia.org/wiki/IEEE_802.2 "wikilink") (노벨)
  - [802.2](https://ko.wikipedia.org/wiki/IEEE_802.2 "wikilink") ([SNAP](https://ko.wikipedia.org/wiki/서브네트워크_접근_프로토콜 "wikilink"))
  - [이더넷 2](https://ko.wikipedia.org/wiki/이더넷_2_프레이밍 "wikilink")

## 외부 링크

  - [RFC 1132 - A Standard for the Transmission of 802.2 Packets over IPX Networks](http://tools.ietf.org/html/rfc1132)

[분류:네트워크 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_계층_프로토콜 "wikilink")