> This article is converted from Wikipedia: [A\* 알고리즘](https://ko.wikipedia.org/wiki/A\*_알고리즘).


[정보과학](../Page/정보과학.md "wikilink") 분야에 있어서, **A\* 알고리즘**()은 주어진 출발 꼭짓점에서부터 목표 꼭짓점까지 가는 최단 [경로를](../Page/경로_\(그래프_이론\).md "wikilink") 찾아내는(다시 말해 주어진 목표 꼭짓점까지 가는 최단 경로임을 판단할 수 있는 테스트를 통과하는) [그래프 탐색 알고리즘](https://ko.wikipedia.org/wiki/그래프_탐색_알고리즘 "wikilink") 중 하나이다. 이 알고리즘은 [다익스트라 알고리즘과](https://ko.wikipedia.org/wiki/다익스트라_알고리즘 "wikilink") 유사하나 차이점은 각 꼭짓점 \(x\)에 대해 그 꼭짓점을 통과하는 최상의 경로를 추정하는 순위값인 "휴리스틱 추정값 " \(h(x)\) 을 매기는 방법을 이용한다는 것이다. 이 알고리즘은 이 휴리스틱 추정값의 순서로 꼭짓점을 방문한다. 그러므로 A\* 알고리즘을 [너비 우선 탐색의](../Page/너비_우선_탐색.md "wikilink") 한 예로 분류할 수 있다.

이 알고리즘은 1968년 [피터 하트](https://ko.wikipedia.org/wiki/피터_하트_\(컴퓨터_과학자\) "wikilink"), [닐스 닐슨](https://ko.wikipedia.org/wiki/닐스_닐슨 "wikilink"), [버트램 라팰이](https://ko.wikipedia.org/wiki/버트램_라팰 "wikilink") 처음 기술하였다. 그 3명의 논문에서, 이 알고리즘은 A 알고리즘()이라고 불렸다. 적절한 [휴리스틱](https://ko.wikipedia.org/wiki/휴리스틱 "wikilink")을 가지고 이 알고리즘을 사용하면 최적(optimal)이 된다. 그러므로 A\* 알고리즘이라고 불린다.

A\* 알고리즘은 출발 꼭짓점으로부터 목표 꼭짓점까지의 최적 경로를 탐색하기 위한 것이다. 이를 위해서는 각각의 꼭짓점에 대한 평가 함수를 정의해야 한다. 이를 위한 평가 함수 \(f(n)\)은 다음과 같다.

\[f(n) = g(n) + h(n)\]

:\* \(g(n)\) : 출발 꼭짓점으로부터 꼭짓점 \(n\)까지의 경로 가중치

:\* \(h(n)\) : 꼭짓점 \(n\)으로부터 목표 꼭짓점까지의 추정 경로 가중치

## 예제: 8-퍼즐 문제

3 x 3의 숫자판에 1\~8까지의 숫자와 빈칸이 주어져 있다고 하자. 숫자를 인접한 빈칸으로 옮기는 작업을 반복함으로써 주어진 숫자 배열로부터 목표가 되는 숫자 배열로 바꾸되, 숫자의 총 이동 횟수를 최소로 하고자 한다. 이 문제를 A\* 알고리즘으로 푸는 과정은 다음과 같다. [왼쪽](https://ko.wikipedia.org/wiki/파일:8-puzzle_by_ddong.jpg "wikilink")  {{-}}

## 구현

### [의사코드](../Page/의사코드.md "wikilink")

    pq.enqueue(start_node, g(start_node) + h(start_node))       // 우선순위 큐에 시작 노드를 삽입한다.

    while pq is not empty       // 우선순위 큐가 비어있지 않은 동안
        node = pq.dequeue       // 우선순위 큐에서 pop한다.

        if node == goal_node    // 만약 해당 노드가 목표 노드이면 반복문을 빠져나온다.
            break

        for next_node in (next_node_begin...next_node_end)       // 해당 노드에서 이동할 수 있는 다음 노드들을 보는 동안
            pq.enqueue(next_node, g(node) + cost + h(next_node)) // 우선순위 큐에 다음 노드를 삽입한다.

    return goal_node_dist       // 시작 노드에서 목표 노드까지의 거리를 출력한다.

### [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")

``` cpp
// 이 소스 코드의 그래프는 인접 리스트 방식으로 그래프를 표현하였다.
using ii = pair<int, int>;

priority_queue<ii, greater<ii>, vector<ii> > pq;
/// N_VER은 그래프의 정점의 개수를 의미한다.
int dist[N_VER], cost[N_VER][N_VER]; /// dist[i]는 i번째 정점까지 가는 최단 거리를 의미한다.
vector<ii> edges[N_VER]; /// edges[i]는 i와 연결된 정점과 가중치를 묶어 저장하는 벡터이다.

int minDist(int src, int dst) {
    pq.push({0, src});
    bool success = false;
    while (!pq.empty()) {
        int v = pq.top(); pq.pop();
        if (v == dst) {
            success = true;
            break;
        }
        for (ii adj: edges[v]) {
            if (dist[adj.first] < g(v) + adj.second + h(adj.first)) {
                dist[adj.first] = g(v) + adj.second + h(adj.first); // 이완 (relaxation)
                pq.push({dist[adj], adj}); // 다음 정점 후보에 탐색하고 있는 정점을 넣는다.
            }
        }
    }
    if (!success) return -1;
    else return dist[dst];
}
```

[분류:그래프 알고리즘](https://ko.wikipedia.org/wiki/분류:그래프_알고리즘 "wikilink") [분류:검색 알고리즘](https://ko.wikipedia.org/wiki/분류:검색_알고리즘 "wikilink") [분류:라우팅 알고리즘](https://ko.wikipedia.org/wiki/분류:라우팅_알고리즘 "wikilink")