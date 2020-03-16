> This article is converted from Wikipedia: [2-OPT](https://ko.wikipedia.org/wiki/2-OPT).


[수학적 최적화에서](../Page/수학적_최적화.md "wikilink") **2-OPT**는 [외판원 문제를](../Page/외판원_문제.md "wikilink") 해결하기 위해 1958 년 Croes가 제안한 간단한 지역 탐색(Local Search) 알고리즘이다.

2-OPT를 통해 경로(Route)가 꼬인(Cross over itself) 노선을 재정렬(순서 변경)하여 풀어주고, 이를 통해 비용(Traveling Cost)을 개선할 수 있다는 게 주요 아이디어이다.

`- A   B -             - A - B -`
`    X         ==>`
`- C   D -             - C - D -`

전체 2-OPT 지역 검색은 가능한 모든 유효한 조합을 비교하고, 교환(swap)하는 메커니즘이다.

이 기술은 외판원 문제뿐만 아니라 많은 관련 문제에 적용될 수 있으며, 간단한 변경(minor modification)을 통해 [차량 경로 문제](https://ko.wikipedia.org/wiki/차량_경로_문제 "wikilink")(VRP:Vehicle Routing Problem)뿐만 아니라 capacitated VRP 에 적용할 수 있다.

아래는 2-OPT swap이 주어진 경로를 변경/개선하는 방식이다 :

`  2optSwap(route, i, k) {`
`      1. route[1]에서 route[i-1]까지 순서대로 new_route에 추가`
`      2. route[i]에서 route[k]까지 역순으로 new_route에 추가`
`      3. route[K + 1]에서 끝까지 순서대로 new_route에 추가`
`      return new_route;`
`  }`

위의 방식에 대한 아래 예시를 보면 간단히 이해할 수 있을 것이다.

`  example route: A ==> B ==> C ==> D ==> E ==> F ==> G ==> H ==> A`
`  example i = 4, example k = 7`
`  new_route:`
`      1. (A ==> B ==> C)`
`      2. A ==> B ==> C ==> (G ==> F ==> E ==> D)`
`      3. A ==> B ==> C ==> G ==> F ==> E ==> D (==> H ==> A)`

이러한 알고리즘은 아래와 같이 정리할 수 있다.

`  repeat until no improvement is made {`
`      start_again:`
`      best_distance = calculateTotalDistance(existing_route)`
`      for (i = 0; i < number of nodes eligible to be swapped - 1; i++) {`
`          for (k = i + 1; k < number of nodes eligible to be swapped; k++) {`
`              new_route = 2optSwap(existing_route, i, k)`
`              new_distance = calculateTotalDistance(new_route)`
`              if (new_distance < best_distance) {`
`                  existing_route = new_route`
`                  goto start_again`
`              }`
`          }`
`      }`
`  }`

참고 : 특정 노드에서 출발/도착하면, swap 후보 검색에서 이를 제거해야 한다. 그렇지 않으면 잘못된 경로를 생성한다.

예를 들어, 노드 A:

`  A ==> B ==> C ==> D ==> A`

노드\[0\]과 노드\[2\]의 swap을 하였다면

` C ==> B ==> A ==> D ==> A`

와 같이 유효하지 않은 경로를 생성한다. 출발/종료점이 정해져 있다면 이를 제외한 노드만을 swap후보로 선택할 수 있도록 해야한다.

## 각주

  -
## 같이 보기

  - [3-opt](https://ko.wikipedia.org/wiki/3-opt "wikilink")
  - [지역 탐색](https://ko.wikipedia.org/wiki/지역_탐색 "wikilink")
  - [린-커닝험 발견법](https://ko.wikipedia.org/wiki/린-커닝험_발견법 "wikilink")

## 외부 링크

  - [The Traveling Salesman Problem: A Case Study in Local Optimization](https://www.cs.ubc.ca/~hutter/previous-earg/EmpAlgReadingGroup/TSP-JohMcg97.pdf)
  - [Improving Solutions: 2-opt Exchanges](http://www-e.uni-magdeburg.de/mertens/TSP/node3.html)

[분류:최적화](https://ko.wikipedia.org/wiki/분류:최적화 "wikilink")