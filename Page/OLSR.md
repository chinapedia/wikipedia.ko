> This article is converted from Wikipedia: [OLSR](https://ko.wikipedia.org/wiki/OLSR).


[섬네일](https://ko.wikipedia.org/wiki/파일:Olsr-overview.pdf "wikilink") **OLSR**(Optimized Link State Routing Protocol)\[1\]은 [모바일 애드혹 네트워크에](https://ko.wikipedia.org/wiki/애드혹_네트워크 "wikilink") 최적화된 [IP](https://ko.wikipedia.org/wiki/인터넷_프로토콜 "wikilink") 라우팅 프로토콜이다. 무선 애드혹 네트워크에서도 사용될 수 있다. OLSR은 실제 데이터 전송 요청이 발생하기 전에 미리 경로를 계산하여 라우팅 테이블을 생성하는 프로액티브 방식의 링크 상태 라우팅 프로토콜(link-state routing protocol)로서, 모바일 애드혹 네트워크상에서 주변 노드들을 발견하고 링크 상태 정보를 전파하기 위해 *헬로*(hello) 및 *토폴로지 컨트롤*(topology control) 메시지를 사용한다. 이를 통해 개별 노드들은 네트워크의 토폴로지 정보를 확보하여 다른 모든 노드들에 대해 데이터를 전달하기 위한 최단경로를 계산한다.

## 특징

OSPF(Open Shortest Path First)와 IS-IS같은 링크-상태 라우팅 프로토콜들은 토폴로지 정보의 범람을 수행하기 위해 모든 링크에서 지정된 라우터를 선택한다. 무선 애드훅 네트워크에서는, 링크의 개념이 다르다. 패킷은 같은 인터페이스로 갈수 있고 가기도 한다. 그런 이유로, 프로세스의 범람을 최적화하기 위해 다른 접근이 필요하다. Hello 메시지를 사용하여, 각 노드의 OLSR 프로토콜은 2-홉 이웃 정보를 발견하고, MPRs(Multipoint relays: 다점 교체)의 집합의 분산 선택을 수행한다.

## 장점

선행 프로토콜은 알려진 네트워크의 모든 목적지에 보내고 사용전에 유지 보수한다. 루트들을 갖는 것은 새로운 루트를 찾는 것과 관련한 루트 탐색 지연을 없애는 것 같이 표준 라우팅 테이블이 몇몇 시스템과 네트워크 애플리케이션이 유용하게 하는 것을 가능하게 한다.

## 단점

OLSR의 원래 정의는 링크 퀄리티를 감지하기위한 어떠한 준비 행동도 포함하지 않는다.이것은 링크가 살아서 작동하고있고 만약 hello 패킷의 수가 최근에 받아들여지고 있었다면 간단하게 가정해 볼수 있다. 이것은 링크들이 종종 중간정도의 패킷 손실을 보이는 무선 네트워크의 경우에는 필요 없는 bi-modal이라는 것을 가정한다. 오픈소스 OLSRd(주로 리눅스 기반의 대형 라우터들에 쓰임)와 같은 수행들은 링크 퀄리티 감지와 함께 확장되어 왔다.

## 메시지

OLSR은 헬로 메시지에 대한 응답을 통해 각 노드들이 이웃한 한 홉(hop) 노드 및 두 홉 노드를 찾는다. 그리고 메시지를 송신한 노드는 주변의 한 홉 노드들 중 두 홉 노드들에 대한 가장 좋은 경로를 제공하는 노드를 찾아 멀티포인트 릴레이(multipoint relay, MPR)를 선택한다. 이러한 방식으로 각각의 노드들이 모두 MPR 집합을 보유한다. OLSR은 토폴로지 컨트롤(topology control, TC) 메시지와 MPR 포워딩 정보를 사용하여 전체 네트워크에 이웃 노드 정보를 전파한다. 또한 OLSR은 *호스트 및 네트워크 연결*(host and network association, HNA) 메시지를 이용해 네트워크 경로 광고(advertisement)를 전파하며, 이는 TC 메시지가 호스트 경로를 전파하는 것과 같은 원리로 동작한다.

### 헬로

[파일:olsr-hello-packet.png](https://ko.wikipedia.org/wiki/파일:olsr-hello-packet.png "wikilink")

### 토폴로지 컨트롤

[파일:Olsr-tc-packet.png](https://ko.wikipedia.org/wiki/파일:Olsr-tc-packet.png "wikilink")

## 다른 접근

애드훅 무선 네트워크에서의 라우팅 문제는 활발히 연구되고 있고, OLSR은 여러 방법으로 제안된 솔루션 들 중 하나이다.

## OLSRv2

ORSRv2는 현재 IETF안에서 개발되고 있는 것이다. 이것은 MPR 선택과 보급을 포함한 수 많은 원본의 키 특징을 유지한다. 키의 차이는 공유된 요소들을 사용하는 유동적이고 모듈화된 디자인이다. 이러한 요소들은 다음 세대의 IETF MANET 프로토콜로 일반적으로 디자인되고 있다. 노드들을 가능하게 한 다중 주소와 인터페이스를 다루는 것에 있어서의 차이는 OLSR과 OLSRv2 사이 또한 표현하고 있다.

## 각주

[분류:무선 네트워크](https://ko.wikipedia.org/wiki/분류:무선_네트워크 "wikilink") [분류:라우팅 알고리즘](https://ko.wikipedia.org/wiki/분류:라우팅_알고리즘 "wikilink")

1.  RFC 3626