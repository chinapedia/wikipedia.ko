> This article is converted from Wikipedia: [Chord](https://ko.wikipedia.org/wiki/Chord).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **Chord**(코드)는 [peer-to-peer](../Page/P2P.md "wikilink") [분산 해시 테이블에](../Page/분산_해시_테이블.md "wikilink") 대한 프로토콜 및 [알고리즘](../Page/알고리즘.md "wikilink")이다. 분산 해시 테이블은 다른 컴퓨터(노드)에 키를 할당하여 [키-값 쌍을](https://ko.wikipedia.org/wiki/연관_배열 "wikilink") 저장한다 (노드는 그것이 담당하는 모든 키에 대한 값을 저장한다). Chord는 노드에 키가 할당되는 방법과 주어진 키에 해당하는 첫번째 노드를 찾아 해당 키에 대한 값을 해당 노드가 찾을 수 있는 방법을 정한다.

Chord는 CAN, Tapestry 그리고 Pastry와 함께, 4개의 원조 [분산 해시 테이블](../Page/분산_해시_테이블.md "wikilink") 프로토콜 중 하나이다. 이 프로토콜은 Ion Stoica, Robert Morris, David  Karger, Frans Kaashoek, Hari Balakrishnan가 도입했으며, [MIT에서](../Page/매사추세츠_공과대학교.md "wikilink") 개발되었다.\[1\]

## 개요

[오른쪽](https://ko.wikipedia.org/wiki/파일:Chord_project.svg "wikilink") 노드와 키는 [일관된 해싱을](../Page/일관된_해싱.md "wikilink") 통해 -비트 식별자를 할당 받는다. SHA-1 알고리즘은 일관된 해싱을 위한 기반 [해싱 함수이다](../Page/해시_함수.md "wikilink"). 일관된 해싱은 Chord의 견고함과 성능을 위해 필수적인데, 이는 키와 노드(정확히는 노드의 [IP 주소](../Page/IP_주소.md "wikilink"))가 동일한 식별 공간 내에 무시할 만한 충돌 가능성과 함께 균일하게 분산되기 때문이다. 따라서, 방해 없이 노드를 네트워크에 참가시키거나 내보내는 것이 가능하다. 해당 프로토콜 내에서, 노드라는 용어는 모호할 것 없이 노드 자체와 그것의 식별자(ID) 모두를 가리킨다. '키'라는 용어도 마찬가지이다.

Chord 탐색 프로토콜을 사용하면, 노드와 키는 \(0\)에서 \(2^m - 1\)까지의 범위를 가지는 식별 서클 (Identifier circle) 내에 할당된다(여기서 \(m\)은 충돌을 피할 수 있을 만큼 충분히 커야 한다). 이러한 노드 중 일부는 컴퓨터 나 키에 매핑되는 반면 다른 노드는 대부분 비어 있다.

각 노드는 '다음 노드(successor)'와 '이전 노드(predecessor)'를 가지고 있다. 다음 노드는 식별 서클 내에서 시계 방향에 있는 노드이다. 이전 노드는 시계 반대 방향에 있는 노드이다. 모든 ID 각각에 대해 하나의 노드가 있는 경우 노드 0의 다음 노드는 노드 1이며, 노드 0의 이전 노드는 노드 \(2^m - 1\)이다. 그러나 보통 시퀀스 내에는 "구멍"이 있다. 예를 들어, 노드 154부터 노드 166까지 존재하지 않으면 노드 153의 다음 노드는 노드 167가 되며 노드 167의 이전 노드는 노드 153가 된다.

다음 노드에 대한 개념은 키의 경우에도 사용될 수 있다. 키 \(k\) 의 다음 노드는 아이디가 \(k\) 와 같거나 식별 서클 내에서 \(k\) 다음에 오는 첫번째 노드로, \(successor(k)\) 로 표시한다. 모든 키는 그것의 다음 노드에 할당되므로, 키 \(k\) 를 탐색하는 것은 \(successor(k)\) 를 조회하는 것이다.

한 노드의 다음 노드(혹은 이전 노드)가 (오류나 이탈로 인해) 네트워크에서 사라질 수도 있기 때문에, 각 노드는 서클 내에서 자신과 인접한 세그먼트 전체를 기록한다. 이 리스트는 문제의 네트워크가 높은 오류율을 겪고 있더라도, 높은 확률로 자신의 다음 노드 혹은 이전 노드를 정확하게 찾게 해준다.

## 프로토콜 상세

[대체글=In a 16-node Chord network, the nodes are arranged in a circle. Each node is connected to other nodes at distances 1, 2, 4, and 8 away.](https://ko.wikipedia.org/wiki/파일:Chord_network.png "wikilink")

### 기본적인 조회

Chord 프로토콜의 핵심 용도는 클라이언트(노드)에서 키를 조회, 즉 \(successor(k)\)를 찾는 것이다. 기본적인 해결책은 근처에서 키를 찾지 못한 경우, 노드의 다음 노드에 쿼리를 전달하는 것이다. 이는 \(O(N)\) 조회 시간을 따르는데, 여기서 \(N\) 은 링 내 머신의 개수이다.

### 핑거 테이블

위에서 선형 검색을 피하기 위해, Chord는 각 노드가 \(m\) 개의 엔트리를 포함하는 핑거 테이블을 유미하도록 함으로써 더 빠른 검색 메서드를 구현한다. 여기서, \(m\) 은 해시키에 있는 비트수이다. 노드 \(n\) 의 \(i^{th}\) 엔트리는 \(successor((n+2^{i-1})\,\bmod\,2^m)\)를 포함한다. 핑거 테이블의 첫번째 엔트리는 실제로 노드에 인접한 다음 노드이다 (그러므로 다음 노드에 대한 여분의 필드를 필요로 하지 않다). 노드가 키 \(k\) 를 탐색하려고 할 때마다, 핑거 테이블(ID가 \(k\) 보다 더 작은 서클 상에서 "가장 큰" 것) 내 에서 \(k\) 의 가장 가까운 다음 노드 또는 이전 노드에 쿼리를 전달한다.

그런 핑거 테이블을 사용해, N-노드 네트워크 내에서 다음 노드를 찾기 위해 반드시 접촉되어야 하는 노드의 개수는 \(O(\log N)\)이다. (아래에서 증명한다)

### 노드 조인

새로운 노드가 들어올 때면, 세 가지 불변 사항들이 유지되어야 한다(첫 두 가지는 정확성을 보장하는 것이고 마지막 것은 조회를 빠르게 유지한다):

1.  각 노드의 다음 노드는 인접하는 다음 노드를 정확하게 가리킨다.
2.  각 키는 \(successor(k)\) 내에 저장된다.
3.  각 노드의 핑거 테이블은 정확해야 한다.

이 세 가지 불변 사항들을 만족하려면, 각 노드에 대해 'predecessor' 필드가 유지되어야 한다. 다음 노드가 핑거 테이블의 첫번째 엔트리이므로, 이 필드를 개별적으로 유지할 필요가 전혀 없다. 다음 작업들이 새로 들어오는 노드 \(n\) 에 대해 이루어져야 한다:

1.  노드 \(n\) 을 초기화한다(이전 노드와 핑거 테이블).
2.  다른 노드들에게 그들의 이전 노드와 핑거 테이블의 갱신을 알린다.
3.  새로운 노드는 그것의 다음 노드로부터 책임져야 할 키를 전달받는다.

\(n\) 의 이전 노드는\(successor(n)\) (이전 서클 내에서)의 이전 노드로부터 쉽게 얻을 수 있다. 핑거 테이블에는 다양한 초기화 메서드가 있다. 가장 간단한 것은 모든 \(m\) 의 엔트리에 대해 다음 노드 찾기 쿼리를 실행하는 것인데, \(O(M\log N)\) 초기화 시간이 걸립니다. 더 나은 메서드는 핑거 테이블 내 \(i^{th}\) 개의 엔트리가 \((i+1)^{th}\) 엔트리에 대해 여전히 올바른지를 검사하는 것이다. 이것은 \(O(\log^2 N)\). 최고의 메서드는 인접하는 이웃 노드로부터 핑거 테이블을 초기화하고 갱신하는 것인데, \(O(\log N)\) 이 걸립니다.

### 안정화

정확한 탐색을 보장하기 위해, 모든 다음 노드를은 항상 최신으로 유지되어야 한다. =\> 백그라운드에서 주기적으로 실행되는 안정화 프로토콜. 핑거 테이블과 다음 노드 포인터의 갱신. 안정화 프로토콜: Stabilize(): n은 자신의 다음 노드에게 이전 노드 p에 대해 묻고 대신해서 p가 이전 노드가 되어야 하는지 결정한다(이는 p가 최근에 시스템에 들어온 경우를 말한다. Notify(): \(n\) 의 존재를 다음 노드에게 알려줘서, 그것의 이전 노드를 \(n\) 으로 변경할 수 있다. Fix_fingers(): 핑거 테이블을 갱신한다.

## 잠재적인 용도

  - 협력적인 미러링: 로컬 네트워크 외부의 컴퓨터에서 사용할 수 있는 정보를 호스팅하는 로컬 네트워크의 [로드 밸런싱](../Page/부하분산.md "wikilink") 매커니즘. 이 스킴으로 개발자들은 중앙 서버 대신 많은 서버 간의 부하량의 균형을 맞춰 제품의 고가용성을 보장할 수 있다.
  - 시간 공유 스토리지: 네트워크 내에서, 하나의 컴퓨터가 네트워크가 들어오고 나면, 해당 컴퓨터가 네트워크으로부터 연결 해제될 때 검색을 위해 가용한 데이터가 네트워크 도처에 분산된다. 다른 컴퓨터의 데이터 또한 그들이 더 이상 네트워크에 연결되어 있지 않은 경우 오프라인 검색을 위해 해당 컴퓨터에 전송된다. 주로 네트워크에 풀타임으로 연결할 능력이 없는 노드의 경우에 해당한다.
  - 분산 인덱스: 검색 가능한 데이터베이스 간의 네트워크를 통한 파일 검색(예: P2P 파일 전송 클라이언트).
  - 대규모 조합 검색: 문제에 대한 후보 솔루션인 키와, 솔루션으로든 아니든 그것들을 평가할 책임이 있는 노드 또는 컴퓨터에 대한 각 키의 매핑(예: 코드 분할)

## 증명 스케치

[대체글=If two nodes are at a distance 11 apart along the ring (i.e., there are 10 nodes between them), it takes three hops to send a message from one to the other. The first hop covers a distance of 8 units, the second 2 units, and the final hop 1 unit.](https://ko.wikipedia.org/wiki/파일:Chord_route.png "wikilink") '높은 개연성을 가지고, Chord는 \(O(\log N)\)' '개의 노드에 접근해\(N\)-노드 네트워크 내에서 다음 노드를 찾는다.'

노드 \(n\) 이 키 \(k\) 에 대한 다음 노드를 찾으려고 한다고 가정해보겠다. \(p\) 가 \(k\) 의 이전 노드라고 해보자. 메시지를 \(n\) 에서 \(p\) 로 라우팅하는데 몇 단계가 걸리는지, 그 상한선을 찾고자 한다. 노드 \(n\) 은 핑거 테이블을 검사하여 그것이 가진 \(k\) 의 가장 인접한 이전 노드에게 요청을 라우팅한다. 이 노드를 \(f\) 라고 해보자. 만약 \(f\) 가 \(n\) 의 핑거 테이블의 \(i^{th}\) 번째 엔트리라면, \(f\) 와 \(p\) 는 \(n\) 으로부터 \(2^{i-1}\) 와 \(2^{i}\) 사이의 거리에 있다. 따라서, 이 서클을 따른 \(f\) 와 \(p\) 사이의 거리는 최대 \(2^{i-1}\)이다. 따라서, \(f\) 에서 \(p\) 까지의 거리는 \(n\) 에서 \(f\) 까지의 거리보다 더 작다. \(p\) 까지의 새로운 거리는 초기 거리의 절반 이하이다.

남은 거리를 반으로 나누는 이 과정이 반복되므로, \(t\) 단계 이후에, \(p\) 까지의 남은 거리는 최대 \(2^m / 2^t\) 가 된다. 특히, \(\log N\) 단계 이후에, 남은 거리는 최대 \(2^m / N\) 가 된다. 노드가 무작위로 식별 서클을 따라 고르게 분산되기 때문에, 이 길이 구간에 속하는 예상 노드의 수는 1이며, 그런 노드가 \(\log N\) 개 보다 더 적게 있을 확률이 높다. 메시지가 항상 적어도 하나 이상의 노드에 의해 진행되기 때문에, 남은 거리를 탐색하는 메시지의 경우 \(\log  N\) 단계가 소요된다. 그래서 총 예상 라우팅 시간은 \(O(\log N)\)이 된다.

Chord가 \(r = O(\log N)\) 개의 이전 노드 및 다음 노드에 대한 트래킹을 유지할 경우, 또 각 노드가 실패할 확률이 1/4인 경우, find_successor (아래 참고)와 find_predecessor (see below)가 정확한 노드를 반환할 확률이 높다.

단순히, 모든 \(r\) 노드가 실패할 확률은 \(\left({{1}\over{4}}\right)^r = O\left({{1}\over{N}}\right)\)이며, 이는 낮은 확률이다. 그러므로 그들 중 한 개는 살아있고 노드는 정확한 포인터를 가질 가능성이 높다.

## 의사 코드

  - 의사 코드를 위한 정의

:; finger\[k\]

:: \((n+2^{k-1})  \mbox{ mod } 2^m, 1 \leq k \leq m\) 를 만족하는 첫번째 노드

:; successor

:: 식별 링 상에서 해당 노드의 다음 노드

:; predecessor

  -

      -
        식별 링 상에서 해당 노드의 이전 노드

아이디에 대한 'successor' 노드를 찾는 의사 코드는 다음과 같다:

``` numberLines
// ask node n to find the successor of id
 n.find_successor(id)
   //Yes, that should be a closing square bracket to match the opening parenthesis.
   //It is a half closed interval.
   if (id ∈ (n, successor] )
     return successor;
   else
     // forward the query around the circle
     n0 = successor.closest_preceding_node(id);
     return n0.find_successor(id);
```

``` numberLines
// search the local table for the highest predecessor of id
 n.closest_preceding_node(id)
   for i = m downto 1
     if (finger[i]∈(n,id))
       return finger[i];
   return n;
```

노드 참가나 이탈 이후 Chord 링 혹은 서클을 안정화하는 의사 코드는 다음과 같다:

``` numberLines
// create a new Chord ring.
 n.create()
   predecessor = nil;
   successor = n;
```

``` numberLines
// join a Chord ring containing node n'.
 n.join(n')
   predecessor = nil;
   successor = n'.find_successor(n);
```

``` numberLines
// called periodically. n asks the successor
 // about its predecessor, verifies if n's immediate
 // successor is consistent, and tells the successor about n
 n.stabilize()
   x = successor.predecessor;
   if (x∈(n, successor))
     successor = x;
   successor.notify(n);
```

``` numberLines
// n' thinks it might be our predecessor.
 n.notify(n')
   if (predecessor is nil or n'∈(predecessor, n))
     predecessor = n';
```

``` numberLines
// called periodically. refreshes finger table entries.
 // next stores the index of the finger to fix
 n.fix_fingers()
   next = next + 1;
   if (next > m)
     next = 1;
   finger[next] = find_successor(n+2^{next-1});
```

``` numberLines
// called periodically. checks whether predecessor has failed.
 n.check_predecessor()
   if (predecessor has failed)
     predecessor = nil;
```

## 함께 볼만한 것

  - Kademlia
  - Koorde
  - OverSim - the overlay simulation framework
  - SimGrid - a toolkit for the simulation of distributed applications -

## 참조

## 외부 링크

  - [The Chord Project](https://web.archive.org/web/20171210111820/https://github.com/sit/dht/wiki) (redirect from: <http://pdos.lcs.mit.edu/chord/>)
  - [Open Chord - An Open Source Java Implementation](http://open-chord.sourceforge.net/)
  - [Chordless - Another Open Source Java Implementation](https://archive.is/20121225180044/http://chordless.wiki.sourceforge.net/)
  - [jDHTUQ- An open source java implementation. API to generalize the implementation of peer-to-peer DHT systems. Contains GUI in mode data structure](http://sourceforge.net/projects/jdhtuq//)

[분류:검색 알고리즘](https://ko.wikipedia.org/wiki/분류:검색_알고리즘 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink")

1.