> This article is converted from Wikipedia: [MIMD](https://ko.wikipedia.org/wiki/MIMD).


[right](https://ko.wikipedia.org/wiki/파일:MIMD.svg "wikilink")  **복수명령-복수자료**()은 전산에서 병렬화의 한 기법이다. MIMD를 사용하는 기계는 비동기적이면서 독립적으로 동작하는 여러개의 프로세서가 있다. 언제든지 각각의 다른 프로세서들은 각기 다른 데이터를 이용하는 각기 다른 여러 명령어들이 실행할 수 있다. MIMD기계는 [공유 메모리이거나](https://ko.wikipedia.org/wiki/공유_메모리 "wikilink") [분산 메모리이며](https://ko.wikipedia.org/wiki/분산_메모리 "wikilink") 이러한 분류는 MIMD가 어떻게 메모리를 이용하느냐에 따라 나뉜다. 공유 메모리 기계는 [버스](https://ko.wikipedia.org/wiki/버스 "wikilink")기반, 확장 또는 [계층](https://ko.wikipedia.org/wiki/계층 "wikilink")적인 형태일 수 있다. 분산 메모리 기계는 [하이퍼큐브](https://ko.wikipedia.org/wiki/하이퍼큐브 "wikilink")나 [메시](https://ko.wikipedia.org/wiki/메시_네트워킹 "wikilink") 상호연결 기법을 사용한다. MIMD 는 [플린의 분류학에서](https://ko.wikipedia.org/wiki/병렬_컴퓨팅#플린의_분류학 "wikilink") 정의된 4개 분류중의 하나이다.

## 공유 메모리 모델

프로세서들은 모두 소프트웨어적으로 또는 하드웨어적으로 전역 가능한 메모리에 연결되어 있다. [운영 체제는](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") [메모리 일관성](https://ko.wikipedia.org/wiki/메모리_일관성 "wikilink")(Memory coherence)을 유지한다.\[1\] 프로그래머의 관점에서 이 메모리 모델은 분산 메모리 모델보다 이해하기가 쉬운 장점이 있다. 또 다른 장점은 메모리 일관성은 프로그램에 의해서가 아니라 OS에 의해서 관리된다. 두가지 알려진 단점은, 첫째는 서른두개 이상의 확장성이 어려우며, 둘째는 분산 메모리 모델보다 유연하지가 않다.\[2\] 기타 다른 공유 메모리 모델로는 UMA(Uniform Memory Access), COMA(Cached Only Memory Access) 와 [NUMA](https://ko.wikipedia.org/wiki/불균일_기억_장치_접근 "wikilink")()가 있다.\[3\]

### 버스 기반

공유 메모리가 있는 MIMD기계는 중앙에 위치한 공통의 메모리를 가지고 있는 프로세서들이 있다. 가장 간단한 형태에서, 모든 프로세서들은 메모리를 연결하는 버스에 연결되어 있다. 이러한 배치를 버스기반 점(bus-base point)이라 하며, 버스에서 많은 충돌이 생기는 지점이다.

### 계층

계층적 공유 메모리 구조의 MIMD기계는 프로세서에게 각기 다른 메모리를 사용하게 하기 위해서 계층적 버스를 사용한다. 다른 보드에 있는 프로세서들은 내부-중심 버스들을 통해서 통신을 하게된다. 버스들은 보드간의 통신을 지원한다. 이런 형태의 구조로 기계는 구천개 이상의 프로세서들을 지원할 수 있다.

## 분산 메모리

분산 메모리 MIMD기계에서는 각 프로세서는 각각의 자신만의 메모리 영역이 있으며, 각 프로세서는 다른 프로세서의 메모리에 대해서 접근할 방법이 없다. 데이터를 공유하기 위해서는 하나의 프로세서에서 다른 프로세서로 메시지로서 전달되어야 한다. 이러한 기계에서는 공유 메모리가 없기 때문에 충돌은 커다란 문제가 되지 않는다. 서로 서로 직접적으로 많은 수의 프로세서들을 연결하는 것은 경제성면에서 실현성이 없다. 이러한 많은 직접 연결을 피하기 위한 방법은 각 프로세서를 적은 수의 프로세서와 연결하는 것이다. 이러한 설계 방법은 비효율적일 수 있다. 왜냐하면 하나의 프로세서에서 다른 프로세서로 메시지 연결통로로 메시지를 전달하기 위해서는 추가적인 시간이 필요하기 때문이다. 단순한 메시지 전달에도 많은 시간이 필요하다. 이러한 시간 낭비를 줄이기 위해서 하이퍼큐브나 메시 네트워킹 방법을 사용한다. 분산 메모리의 예는 [MPP](https://ko.wikipedia.org/wiki/MPP "wikilink")(massively parallel processors)와 COW (Clusters of Workstations)이다. MPP는 복잡하고 비싸다. 많은 슈퍼컴퓨터들은 [광대역 네트워크에](https://ko.wikipedia.org/wiki/광대역_네트워크 "wikilink") 연결되어 있다. 예를 들면 하이퍼큐브나 메시 상호연결 등이다. COW는 MPP의 몇분의 일가격밖에 안 된다.\[4\]

### 초입방체 상호연결 네트워크

4차원 이상에서 모든 변의 길이가 같은 도형을 [초입방체](https://ko.wikipedia.org/wiki/초입방체 "wikilink")라고 한다. 네개의 프로세서가 [초입방체](https://ko.wikipedia.org/wiki/초입방체 "wikilink")로 연결되어있는 MIMD 분산 메모리 기계에서, 각 프로세서와 메모리 모듈은 각 정사각형의 꼭짓점에 위치해 있다. **시스템의 직경**은 하나의 프로세서가 가장 먼 곳에 있는 프로세서로 메시지를 전달하는 데 걸리는 최소 단계 수를 말한다. 예를 들면 2-초입방체의 직경은 1이다. 여덟개의 프로세서가 있는 초입방체에서는 각각의 프로세서와 메모리는 [정육면체](https://ko.wikipedia.org/wiki/정육면체 "wikilink")의 각 꼭짓점에 위치해 있으며 직경은 3이다. 일반적으로 2<sup>N</sup>개의 프로세서가 있는 시스템은 N개의 다른 프로세서들과 직접 연결되어 있으며 시스템의 직경은 N이다. 하나의 단점은 2의 제곱으로 구성되어야 한다는 것이다. 따라서 기계는 응용 프로그램이 실제로 필요한 프로세서 수보다 더 많은 프로세서로 구성되어야 하는 경우가 생긴다.

### 메시 상호연결 네트워크

메시 상호연결 네트워크로 연결된 MIMD 분산 메모리 기계에서 프로세서들은 2차원 그리드에 위치한다. 각 프로세서는 4개의 바로 옆 프로세서에 연결된다. 하이퍼큐브대비 장점은 2의 제곱으로 구성되지 않아도 된다는 것이다. 단점은 시스템의 직경이 네개 이상의 프로세서가 있는 시스템에서 하이퍼큐브 시스템보다 크다는 것이다.

## 같이 보기

  - [SMP](https://ko.wikipedia.org/wiki/대칭형_다중_처리 "wikilink")
  - [NUMA](https://ko.wikipedia.org/wiki/불균일_기억_장치_접근 "wikilink")
  - [멀티 코어](../Page/멀티_코어.md "wikilink")
  - [슈퍼스칼라](https://ko.wikipedia.org/wiki/슈퍼스칼라 "wikilink")
  - [VLIW](https://ko.wikipedia.org/wiki/VLIW "wikilink")

## 각주

[분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink") [분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink")

1.  Ibaroudene, Djaffer. "Parallel Processing, EG6370G: Chapter 1, Motivation and History." Lecture Slides. [St Mary's University](https://ko.wikipedia.org/wiki/St._Mary's_University,_Texas "wikilink"), [San Antonio, Texas](https://ko.wikipedia.org/wiki/San_Antonio,_Texas "wikilink"). Spring 2008.
2.
3.  Tanenbaum, Andrew S. Organizacion de Computadoras Un Enfoque Estructurado, pag 551
4.  Tanenbaum, Andrew S. Organizacion de Computadoras, Un Enfoque Estructurado, pag 551