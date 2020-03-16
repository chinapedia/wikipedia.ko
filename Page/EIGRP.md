> This article is converted from Wikipedia: [EIGRP](https://ko.wikipedia.org/wiki/EIGRP).


**EIGRP**(강화 내부 경로 제어 통신 규약, )는 [시스코](https://ko.wikipedia.org/wiki/시스코 "wikilink")사가 만든 원래의 [IGRP](https://ko.wikipedia.org/wiki/IGRP "wikilink")를 기반으로 한 개방형 [라우팅 프로토콜이다](../Page/라우팅_프로토콜.md "wikilink"). EIGRP는 라우터 내 대역폭 및 처리 능력의 이용뿐 아니라, 토폴로지(망 구성 방식)가 변경된 뒤에 일어나는 불안정한 [라우팅](../Page/라우팅.md "wikilink")을 최소화하는데 최적화된 고급 [거리 벡터 라우팅 프로토콜이다](https://ko.wikipedia.org/wiki/거리_벡터_라우팅_프로토콜 "wikilink"). EIGRP는 지원하는 라우터들은 32비트 EIGRP 메트릭을 24비트 IGRP 메트릭으로 변환함으로써 IGRP의 이웃 장비들에게 경로 정보를 자동으로 재분배한다. 라우팅 최적화 대부분이 [SRI사의](https://ko.wikipedia.org/wiki/SRI_인터내셔널 "wikilink") [확산 업데이트 알고리즘](https://ko.wikipedia.org/wiki/확산_업데이트_알고리즘 "wikilink")(DUAL, Diffusing update algorithm)의 처리에 기반을 두므로, 빠른 수렴(convergence)을 위한 매커니즘을 제공하고 [루프 문제에서](https://ko.wikipedia.org/wiki/라우팅_루프_문제 "wikilink") 자유롭다.

## 기본 동작

EIGRP는 데이터를 세 개의 테이블에 저장한다:

  - 이웃 테이블(Neighbor Table): 이웃 라우터들에 대한 데이터를 저장한다. (직접 연결된 인터페이스를 통해 직접 접근할 수 있는 데이터)
  - [토폴로지 테이블](https://ko.wikipedia.org/wiki/토폴로지_테이블 "wikilink"): 이름과는 다르게 완전한 네트워크 토폴로지의 개요를 저장하지는 않는다. 이 테이블에는 개별 매트릭과 더불어 EIGRP 라우티드 네트워크의 목적지 네트워크의 목록을 포함한다. 또, 모든 목적지에 대해 [석세서와](https://ko.wikipedia.org/wiki/#석세서 "wikilink") [피저블 석세서가](https://ko.wikipedia.org/wiki/#피저블_석세서 "wikilink") 식별되며 이들이 존재하면 테이블에 저장된다. 토폴로지 테이블 내의 모든 목적지는 "Passive"(라우팅이 안정적이고 라우터는 목적지에 대한 경로를 알고 있음) 또는 "Active"(토폴로지가 변경되어 라우터가 목적지에 대한 경로를 업데이트하는 과정에 있음)로 표시된다.
  - [라우팅 테이블](../Page/라우팅_테이블.md "wikilink"): 모든 목적지에 대한 실제 경로를 저장한다.

## EIGRP 컴포지트, 벡터 메트릭

EIGRP는 6개의 다른 벡터 메트릭을 개별 경로에 연합시켜, 컴포지트 메트릭 계산 시 벡터 메트릭 중 5개를 고려한다.

`Router>show ip eigrp topology 10.0.0.1 255.255.255.255`
`IP-EIGRP topology entry for 10.0.0.1/32`
`  State is Passive, Query origin flag is 1, 1 Successor(s), FD is 40640000`
`  Routing Descriptor Blocks:`
`  10.0.0.1 (Serial0/0/0), from 10.0.0.1, Send flag is 0x0`
`      Composite metric is (40640000/128256), Route is Internal`
`      Vector metric:`
`        Minimum bandwidth is 64 Kbit`
`        Total delay is 25000 microseconds`
`        Reliability is 255/255`
`        Load is 197/255`
`        Minimum MTU is 576`
`        Hop count is 2`

  - Bandwidth (대역): 라우터의 경로에서 목적지 망에 이르는 최소 대역 (킬로비트/초)
  - Load (부하): 1\~255까지의 수
  - Delay (지연): 라우터의 경로에서 목적지 망에 이르는 최대 지연 수
  - MTU ([최대 전송 단위](../Page/최대_전송_단위.md "wikilink")): 최소 경로의 최대 전송 단위 (메트릭 계산에는 쓰이지 않음)
  - Hop Count (홉의 개수): 원격 네트워크에 라우팅할 때 패킷이 통과하는 라우터의 수 (EIGRP AS를 제한하기 위해 사용된다)

## 석세서

어느 특정 목적지를 위한 석세서(successor, 최적의 경로)는 아래의 두 조건을 만족하는 다음의 홉 라우터를 가리킨다.

  - 목적지에 대한 최소 거리를 제공한다.
  - 동일한 [라우팅 루프의](https://ko.wikipedia.org/wiki/라우팅_루프_문제 "wikilink") 일부가 아님이 확실하다.

목적지에 대한 석세서는 [토폴로지 테이블에](https://ko.wikipedia.org/wiki/토폴로지_테이블 "wikilink") 기록되며 그 뒤에 이들은 해당 목적지에 대한 다음 홉으로서 라우팅 테이블을 상주시키는데 사용된다.

## 피저블 석세서

어느 특정 목적지를 위한 피저블 석세서(feasible successor, 차선 경로)는 아래의 조건을 만족하는 다음 홉 라우터이다.

  - 특정 [라우팅 루프의](https://ko.wikipedia.org/wiki/라우팅_루프_문제 "wikilink") 일부가 아님이 확실하다.

모든 석세서는 피저블 석세서이기도 하다. 그러나 EIGRP에 대한 대부분의 참조에서 피저블 석세서는 석세서가 아닌, 루프에서 자유로운 경로를 제공하는 라우터들로 한정하는데 사용된다. (예: 최저 거리를 제공하지 않음) 이러한 관점에서 도달 가능한 목적지의 경우 적어도 하나의 석세서가 존재하지만 피저블 석세서는 존재할 수도, 존재하지 않을 수도 있다.

## 거리 벡터로서의 EIGRP 분류

  - [거리 벡터 라우팅 프로토콜](https://ko.wikipedia.org/wiki/거리_벡터_라우팅_프로토콜 "wikilink")(Distance-vector routing protocols)
  - [링크 스테이트 라우팅 프로토콜](https://ko.wikipedia.org/wiki/링크_스테이트_라우팅_프로토콜 "wikilink")(Link-state routing protocols)

## 참고문헌

  - .

  - .

  - .

  - .

  - .

## 외부 링크

  - [Cisco IOS IPv6 Configuration Guide, Release 12.4: Implementing EIGRP for IPv6](http://www.cisco.com/en/US/docs/ios/ipv6/configuration/guide/ip6-eigrp.html)

  - [IGRP Metric](http://www.cisco.com/en/US/tech/tk365/technologies_tech_note09186a008009405c.shtml)

  - [Loop-free Routing Using Diffusing Computations](https://web.archive.org/web/20080511202045/http://www.soe.ucsc.edu/research/ccrg/publications/jj.dual.ton93.pdf)

  - [Termination Detection for Diffusing Computations](http://www.cs.utexas.edu/users/EWD/ewd06xx/EWD687a.PDF)

[분류:시스코 프로토콜](https://ko.wikipedia.org/wiki/분류:시스코_프로토콜 "wikilink") [분류:라우팅 프로토콜](https://ko.wikipedia.org/wiki/분류:라우팅_프로토콜 "wikilink")