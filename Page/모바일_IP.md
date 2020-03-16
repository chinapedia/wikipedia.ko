> This article is converted from Wikipedia: [ IP](https://ko.wikipedia.org/wiki/_IP).


**모바일 IP**(Mobile IP)는 [IETF](https://ko.wikipedia.org/wiki/IETF "wikilink") 표준 [통신](../Page/통신.md "wikilink") [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")로, 이동 기기 사용자로 하여금 한 네트워크에서 다른 네트워크로 이동하면서 IP 주소를 유지하도록 하기 위해 고안되었다. 모바일 [IPv4](../Page/IPv4.md "wikilink")는 IETF RFC 3344(RFC 3220과 RFC 2002의 진화된 문서)에 기술되어 있고 최신의 내용은 IETF RFC 4721에 추가되었다. 모바일 [IPv6](../Page/IPv6.md "wikilink")는 IETF RFC 3775에 기술되어 있다.

## 개요

모바일 IP 프로토콜은 위치에 구애받지 않고 IP 데이터그램을 전송하도록 한다. 각각의 이동 단말은 인터넷 상의 위치와는 무관하게 자신의 *home address*로 식별된다. 자신의 *home network*에서 벗어날 경우 이동 단말은 *care-of address*와 연관되는데 이 주소로 단말의 현재 위치가 식별되며 *home agent*로 연결되는 터널의 끝단에서 *care-of address*는 *home address*와 매핑된다. 모바일 IP는 어떻게 이동 단말이 *home agent*에 등록하는지, *home agent*는 어떻게 데이터그램을 터널을 통해 이동 단말로 전달하는지에 대해 기술하고 있다.

모바일 IP는 인터넷 상에서 [로밍](https://ko.wikipedia.org/wiki/로밍 "wikilink")을 수행함에 있어서 효과적이고, 확장성있는 방법을 제시한다. 모바일 IP를 사용하여 이동 단말은 자신의 *home IP address*를 바꾸지 않고 접속 지점을 바꿀 수 있다. 이는 로밍을 수행하면서 전송 계층 및 상위 계층의 연결을 유지할 수 있다는 것을 의미한다. 이와 같은 이동성은 인터넷 라우팅 기법을 통한 해당 호스트에 대한 경로 전파 과정없이 실현된다.

## 응용

모바일 IP는 이동 단말이 여러 LAN 서브넷을 이동하는 일이 많은 유무선 환경에서 광범위하게 사용된다. 예를 들어, [DVB](https://ko.wikipedia.org/wiki/DVB "wikilink"), [WLAN](https://ko.wikipedia.org/wiki/WLAN "wikilink"), [WiMAX](https://ko.wikipedia.org/wiki/WiMAX "wikilink"), [BWA](https://ko.wikipedia.org/wiki/BWA "wikilink")와 같은 서로 다른 무선 네트워크 시스템이 중첩된 경우에도 이들 간의 로밍시 적용 가능하다. 현재 이동 통신 시스템은 고유의 [핸드오버](https://ko.wikipedia.org/wiki/핸드오버 "wikilink") 및 로밍 기법을 가지고 있기 때문에 모바일 IP는 [3G](https://ko.wikipedia.org/wiki/3G "wikilink")와 같은 이동 통신 시스템 내부의 이동성 제공을 위해 사용되진 않는다. 하지만, 모바일 IP는 서로 다른 [Packet Data Serving Node](https://ko.wikipedia.org/wiki/PDSN_\(Packet_Data_Serving_Node\) "wikilink") 도메인 간의 원활한 IP 이동성을 위해 종종 사용된다.

그 밖에 [VPN](https://ko.wikipedia.org/wiki/VPN "wikilink"), [VoIP](https://ko.wikipedia.org/wiki/VoIP "wikilink")와 같은 많은 응용에서 네트워크 연결 및 IP 주소의 갑작스런 변경은 많은 문제를 야기할 수 있기 때문에 모바일 IP는 이러한 문제를 해결할 중요한 기법이라고 볼 수 있다.

## 동작 원리

이동 단말은 두 개의 주소-*home address*와 *care-of address(CoA)*-를 가지며 단말이 타 망으로 이동 시 이 둘은 서로 연관된다. 모바일 IP에는 아래와 같이 두 종류의 구성요소로 이루어진다.

  - *Home agent*는 자신의 망에 속하는 *home address*를 갖는 단말에 대한 정보를 저장한다.
  - *Foreign agent*는 자신의 망에 방문(접속)한 단말에 대한 정보를 저장한다. *Foreign agent*는 또한 모바일 IP의 동작을 위해 필요한 *care-of address*를 광고한다.

이동 단말과 통신하길 원하는 노드는 해당 이동 단말의 *home address*를 목적지 주소로 지정하여 패킷을 전송한다. *Home address*는 *home agent*가 위치한 네트워크에 소속된 주소이므로 일반적인 [IP 라우팅](https://ko.wikipedia.org/wiki/IP_라우팅 "wikilink") 과정을 통해 패킷은 *home agent*로 전달된다. 이때 *home agent*는 이 패킷을 동일 네트워크 내 물리적인 목적지 주소로 전달하는 대신 IP 터널을 통해 *foreign agent*로 전달한다. 이때 데이터그램은 *care-of address*가 기입된 또다른 IP 헤더로 감싸여져 전달된다. 반대로 이동 단말이 데이터를 전송할 때에는 데이터는 *home agent*를 거치지 않고 *foreign agent*를 거쳐 바로 목적지 노드로 전달된다. 이때 발신지 주소는 이동 단말의 *home address*로 설정되고 이와 같은 방식을 *triangular* 라우팅이라고 한다. 필요에 따라 *foreign agent*는 *reverse tunneling*을 적용하여 이동 단말의 데이터를 바로 목적지 노드로 전송하는 대신 *home agent*로 전송할 수 있다. *Reverse tunneling*은 네트워크 내 [게이트웨이](../Page/게이트웨이.md "wikilink") [라우터](../Page/라우터.md "wikilink")가 [인그레스 필터링을](https://ko.wikipedia.org/wiki/인그레스_필터링 "wikilink") 가동하여 이동 단말의 발신지 IP 주소가 *foreign network*의 서브넷에 속해야 할 경우 필요하다. 만일 인그레스 필터링이 동작하는 상황에서 발신지 IP 주소가 *foreign network*의 서브넷에 속하지 않은 경우 이 패킷은 삭제된다.

모바일 IP 프로토콜은 다음에 대하여 정의한다.

  - 이동 단말이 자신의 *care-of address*를 *home agent*에 알리는 등록 절차
  - [ICMP 라우터 탐색의](https://ko.wikipedia.org/wiki/ICMP_라우터_탐색 "wikilink") 연장선으로, 차후 사용할 *home agent* 및 *foreign agent*의 탐색 방법
  - 이동 단말에서 송수신되는 패킷에 대한 라우팅 기법 (필수적으로 제공되어야 할 터널링 기법 및 선택적인 터널링 기법을 포함)

### 차후 개발 방향

현재 모바일 IP는 [모바일 IPv6](https://ko.wikipedia.org/wiki/모바일_IPv6 "wikilink"), [Hierarchical MIPv6](https://ko.wikipedia.org/wiki/Hierarchical_MIPv6 "wikilink") 등의 다양한 형태로 발전되면서 더욱 안전하면서 효과적인 방향으로 개발되고 있다. 모바일 IP는 어떠한 사전 설비없이 네트워크 간의 이동성을 지원하기 위한 방향으로 개발되고 있으며 그 한 예가 [Interactive Protocol for Mobile Networking (IPMN)](https://web.archive.org/web/20100701160513/http://medianet.kent.edu/ipmn/main.html) 이다.

## 용어 정의

  - Home network
    이동 단말에게 *home address*를 부여 받은 네트워크를 그 단말의 *home network*라고 한다.

<!-- end list -->

  - Home address
    *Home network*내에서 이동 단말에 부여된 주소를 지칭한다.

<!-- end list -->

  - Foreign network
    이동 단말이 *home network*에서 벗어나 다른 네트워크로 이동하였을 때 그 네트워크를 *foreign network*라고 한다.

<!-- end list -->

  - Care-of address
    이동 단말이 *foreign network*에 접속했을 때 해당 서브넷에서의 물리적인 IP 주소를 지칭한다.

<!-- end list -->

  - Home agent
    이동 단말의 *home network*에 위치한 라우터로 이동 단말의 IP 주소를 유지시키면서 이동 단말로 데이터를 송수신한다.

<!-- end list -->

  - Foreign agent
    이동 단말이 접속한 네트워크에 위치한 라우터로 이동 단말에 대한 정보를 보관하는 동시에 *care-of address*를 광고한다.

<!-- end list -->

  - Binding
    *Home address*와 *care-of address*의 연관을 지칭한다.

## 같이 보기

  - [핸드오프](https://ko.wikipedia.org/wiki/핸드오프 "wikilink")
  - [로밍](https://ko.wikipedia.org/wiki/로밍 "wikilink")
  - [GPRS 터널링 프로토콜](https://ko.wikipedia.org/wiki/GPRS_터널링_프로토콜 "wikilink")
  - [모바일 IPv6](https://ko.wikipedia.org/wiki/모바일_IPv6 "wikilink")
  - [프록시 모바일 IP](https://ko.wikipedia.org/wiki/프록시_모바일_IP "wikilink")

## 외부 링크

  - RFC 3344 - IPv4에서의 IP 이동성 지원
  - RFC 4721 - 모바일 IPv4 Challenge/Response 확장
  - RFC 3024 - 모바일 IP에서의 Reverse Tunneling

[분류:네트워크 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_계층_프로토콜 "wikilink")