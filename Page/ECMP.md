> This article is converted from Wikipedia: [ECMP](https://ko.wikipedia.org/wiki/ECMP).


**ECMP**는 Equal-cost multi-path routing의 약자로 하나의 목적지로 패킷 라우팅을 수행하면서 여러 개의 경로를 선택하는 라우팅 기법이다. ECMP는 다음 홉에 대한 선택을 단일 라우터로 국한시킬 수 있기 때문에 대부분의 라우팅 프로토콜과 결합하여 사용할 수 있다. ECMP는 다중 경로를 통해 트래픽을 분산시킴으로써 잠재적으로 대역폭의 증가를 가져온다. 하지만 실제 적용에 있어서는 많은 문제점이 발생할 수 있다. RFC 2991에서는 다중 경로 라우팅에 대한 일반적인 내용을 기술하고 있다.

패킷 별 다중 경로 라우팅을 통한 부하 균등(load balancing)은 빠르게 변하는 지연(latency), 패킷 재정렬(packet reordering), MTU 변동으로 인해 일반적으로 좋은 평가를 받지 못하고 있으며, 특히 TCP, path MTU discovery와 같은 [인터넷 프로토콜의](../Page/인터넷_프로토콜.md "wikilink") 동작에 혼란을 가져온다. RFC 2992는 패킷 헤더 내 플로우 관련 데이터의 해싱을 통해 플로우를 할당하여 플로우 간의 부하 균등을 유지하면서 앞서 제시된 문제점을 해결할 수 있는 다중 경로 라우팅 기법을 소개하고 있다.

실제로 많은 상황에서, ECMP는 좋은 성능을 제공하지 못할 수 있다. 예를 들어 여러 개의 경로를 통해 전송되던 데이터 흐름이 어느 순간 하나의 경로로 수렴할 경우, ECMP는 대역폭의 증가없이 트래픽 경로의 복잡도만 증가시키게 된다. 또한 시스템의 물리적인 토폴로지와 논리적 토폴로지가 다를 경우 (예를 들어, L2 계층에 [VLAN](https://ko.wikipedia.org/wiki/VLAN "wikilink")가 적용되었거나 [ATM](../Page/비동기_전송_방식.md "wikilink"), [MPLS](https://ko.wikipedia.org/wiki/MPLS "wikilink")와 같은 virtual circuit-based 구조의 시스템), ECMP는 다른 라우팅 프로토콜과 제대로 연동되지 않을 수 있다.

## 같이 보기

  - [다중 경로 라우팅](https://ko.wikipedia.org/wiki/다중_경로_라우팅 "wikilink")
  - [IEEE 802.1aq](https://ko.wikipedia.org/wiki/IEEE_802.1aq "wikilink") - [Shortest Path Bridging](https://ko.wikipedia.org/wiki/Shortest_Path_Bridging "wikilink") (SPB)

[분류:컴퓨터 네트워킹](https://ko.wikipedia.org/wiki/분류:컴퓨터_네트워킹 "wikilink") [\*](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink") [분류:라우팅 알고리즘](https://ko.wikipedia.org/wiki/분류:라우팅_알고리즘 "wikilink")