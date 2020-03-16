> This article is converted from Wikipedia: [FM ](https://ko.wikipedia.org/wiki/FM_).


[전자공학](../Page/전자공학.md "wikilink")에서 **FM 알고리즘**(Fiduccia Mattheyses algorithm)은 Physical Design의 작업 중 하나인 Circuit Partitioning 공정의 하나이다. 다른 공정으로는 K-L(Kernighan-Lin)알고리즘, Simulated Annealing 등이 있다. F-M(fiduccia-mattheyses) 알고리즘은 Fiduccia\[1982\]와 Mattheyes에 의해 노드연결 분리문제(hypergraph bipartitioning problem)를 해결하기 위해 고안된 반복해석 기법이다.

**입력데이터분석**: [하이퍼그래프](https://ko.wikipedia.org/wiki/하이퍼그래프 "wikilink")로 이루어진 벌텍스(vertex, 디지털 Gate를 변환하면 만들어진 블록)와 하이퍼엣지([Hyperedge](https://ko.wikipedia.org/wiki/Hyperedge "wikilink"), 블록에 연결된 선), 예) Net1 C1, C2, C3, C4

n(i): Net 에 연결된 Cell(셀)의 숫자 예) n(1) = 4: net 1번에 연결되어 있는 Cell의 숫자는 4개다. 4개의 Gate가 연결되어 있다.\]

s(i): i Cell의 크기(어떤 Cell은 한개의 크기가 다른 것의 2,3배가 되기 때문에 Cutset을 할때 이것을 고려해야한다.)

p(i): i Cell에 연결된 핀즉 Net선의 개수; e.g., p(1) = 4 은 1번 Cell에는 4개의 선이 연결되었다는 의미이며, 즉 연결된 Net 4개라는 의미가 된다

C: 회로에 주어진 총 Cell의 개수; e.g., C = 13 총 C1, C2, .... C13 까지 있다는 의미이다.

N: 회로에 주어진 Net의 개수 이다. e.g., N= 4 는 즉 Net1, Net2, Net3, Net4가 있다는 의미이다.

P: Net과 Cell 사이에 연결된 총 Pin의 개수; P= p(1) + … + p(C) = n(1) + … + n(N) 즉 각각의 Cell의 연결된 Pin의 개수는 각 Net에 연결된 Pin의 개수와 당연히 일치한다.

r: Cutset을 위해 요구되는 Balance Factor 이다. 0\< r\<1

**출력데이터** Output: 2 partitions A& Bs.t. Cutset size 는 최적의 수가 되어야 한다. 제일 작은 수가 되어야 한다. 이것이 우리가 원하는 첫 번째 목적이다. 주어진 회로를 2-way or Muti-Way를 하는데 있어서 가장 적은 Cutsize로 잘라야 한다.

Balance Factor: r = |A|/(|A|+|B|) - 균형의 인자는 2-way로 나뉜 Net-Cut의 Weight 즉 균형점의 값이 된다. FM은 K-L 알고리즘과 달리 임의적으로 나누수 있다. 그렇다고 두개의 Net-Cut을 극단적으로 10:90으로 나누면 한쪽의 CPU가 처리해야하는 용량이 너무 많으므로 최대한 으로 가능한 균형값을 정해 줄 필요가 있는데 이것을 Balance Factor라 한다.

**반복횟수**: O(P)은 Operation Time은 P 즉 총 Pin의 개수 만큼 반복해야 한다.

최적 minimum Cutset Size는 O(P) 횟수 만큼 Cell를 옮겨서 각각의 G(i)의 값의 합을 구하고 이 중에서 가장 큰 값 max sum of G(i)가 우리가 찾고자 하는 최적의 Condition 이 되는 것이다.

[right](https://ko.wikipedia.org/wiki/파일:FM-Sample.png "wikilink")

## 같이 보기

  - [전자 설계 자동화](https://ko.wikipedia.org/wiki/전자_설계_자동화 "wikilink")

[분류:전자공학](https://ko.wikipedia.org/wiki/분류:전자공학 "wikilink") [분류:전자 설계 자동화](https://ko.wikipedia.org/wiki/분류:전자_설계_자동화 "wikilink")