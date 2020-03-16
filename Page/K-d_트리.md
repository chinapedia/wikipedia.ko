> This article is converted from Wikipedia: [K-d ](https://ko.wikipedia.org/wiki/K-d_).


[thumb](https://ko.wikipedia.org/wiki/파일:3dtree.png "wikilink")

[컴퓨터 과학에서](../Page/컴퓨터_과학.md "wikilink"), ***k*-d 트리** (, *k-차원(dimensional) [트리](https://ko.wikipedia.org/wiki/트리_구조 "wikilink")*)는 *k*차원 [공간의](../Page/유클리드_공간.md "wikilink") [점들을](../Page/점_\(기하학\).md "wikilink") 구조화 하는 [공간 분할](https://ko.wikipedia.org/wiki/공간_분할법 "wikilink") [자료 구조이다](../Page/자료_구조.md "wikilink"). *k*-d 트리는 다차원 탐색 키에 관련된 탐색 같은 적용분야에 유용한 자료구조이다(예: [범위 탐색과](https://ko.wikipedia.org/wiki/범위_탐색 "wikilink") [최근접 이웃 탐색](https://ko.wikipedia.org/wiki/최근접_이웃_탐색 "wikilink")). *k*-d 트리는 [이진 공간 분할](../Page/이진_공간_분할법.md "wikilink") 트리의 특수한 경우이다.

## 비공식적 설명

*k*-d 트리는 모든 노드가 *k*차원 점인 [이진 트리이다](../Page/이진_트리.md "wikilink"). 모든 리프 노드는 암시적으로 공간을 [반평면](https://ko.wikipedia.org/wiki/반평면 "wikilink")의 두 부분으로 나누는 분할 [초평면](https://ko.wikipedia.org/wiki/초평면 "wikilink")을 만드는 것으로 생각할 수 있다. 이 초평면의 왼쪽은 그 노드의 왼쪽 부분 트리를 나타내고 오른쪽은 오른쪽 부분 트리를 나타낸다. 초평면의 방향은 다음과 같이 결정된다: 트리에 있는 모든 노드는 k차원 중 하나와 연관되어 있으며, 그 초평면은 그 차원축에 수직한다. 따라서 예를 들어 보면, 수직 분할할 대상으로 "x"축을 선택했으면 노드보다 더 작거나 같은 "x"값을 가지는 부분트리의 모든 점은 왼쪽 부분트리에 속하고 더 큰 점은 오른쪽에 속한다.

[분류:자료 구조](https://ko.wikipedia.org/wiki/분류:자료_구조 "wikilink")