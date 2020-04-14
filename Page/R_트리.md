> This article is converted from Wikipedia: [R 트리](https://ko.wikipedia.org/wiki/R_트리).


**R 트리**는 [B 트리와](../Page/B_트리.md "wikilink") 비슷한데 다차원의 공간 데이터를 저장하는 [색인이다](https://ko.wikipedia.org/wiki/트리_구조 "wikilink"). 이를테면, 지리학에서 R 트리는 "현재 위치에서 200km 이내의 모든 도시를 찾아라"와 같은 [질의](https://ko.wikipedia.org/wiki/질의 "wikilink")에 대해 빠르게 답을 줄 수 있다.

이 [자료 구조는](../Page/자료_구조.md "wikilink") 공간을 최소 경계 사각형(MBR, Minimum Bounding Rectangle) 들로 분할하여 저장한다. MBR끼리 겹칠 수도 있고, 상위 레벨의 MBR 은 하위 레벨의 MBR들을 포함하는 계층적인 트리 구조이다. 각 노드는 미리 정의된 범위내에서 유동적인 개수의 자식 노드들의 정보 (MBR과 포인터)를 가진다.

R-트리의 저장과 삭제 [알고리즘](../Page/알고리즘.md "wikilink")은 가까운 데이터들은 되도록 같은 [단말 노드](https://ko.wikipedia.org/wiki/단말_노드 "wikilink")(leaf)에 두려고 한다. 그럼으로써 R 트리는 굳건하게 MBR을 유지할 수 있고, 검색 성능이 좋아지게 된다. 검색 알고리즘들(intersection, containment, nearest neighbor)이 이러한 MBR 들을 사용하여, 하위 레벨의 자식 노드를 검색할 것인지를 결정하기 때문이다.

## 변종 R-트리들

  - [R\* 트리](https://ko.wikipedia.org/wiki/R*_트리 "wikilink")
  - [R+ 트리](https://ko.wikipedia.org/wiki/R+_트리 "wikilink")

## 알고리즘

### 검색 (search)

#### 교차 질의(Intersection)

최소 경계 사각형 MBR 을 질의 입력으로 받지만, 검색은 [B-트리](https://ko.wikipedia.org/wiki/B-트리 "wikilink")와 상당히 유사하다. 검색은 루트 노드로부터 시작하는데, 단말 노드를 제외한 모든 중간의 비단말 노드들은 자식 노드의 MBR을 포함하는 MBR을 가지며, 단말 노드들의 MBR은 단말 노드가 가리키는 공간 데이터들을 둘러싸는 최소 경계 사각형이다. 따라서, 모든 노드들은 질의 입력 MBR과 자식 노드들의 MBR을 비교하여 교차되는 영역이 있는 자식 노드들에게만 질의를 전달한다. 이러한 검색은 재귀 함수로 구현할 수 있다.

#### 포함 질의(Containment)

교차 질의와 유사하나, 교차되는 영역이 있는 자식노드가 아닌, 질의를 포함하는 자식노드들만 검색한다.

#### 근접 이웃 질의(Nearest Neighbor)

점 좌표와 거리를 입력으로 받는다. 특정 점 좌표로부터 가장 가까운 거리에 위치한 데이터를 찾는 알고리즘이 필요하다.

### 삽입 (insertion)

부적절한 상태에 있는 노드란, 적절한 범위에서 벗어난 수의 항목을 가지고 있다는 것을 의미한다.

1.  우선, 노드가 어느 위치로 삽입될지 찾는다. 그리고 값을 해당 노드에 삽입한다.
2.  부적절한 상태의 노드가 없다면, 삽입을 종료한다.
3.  만약, 어떤 노드가 너무 많은 항목을 가지고 있다면, 이를 두 노드로 분리한다. 이 과정을 반복적으로 트리를 타고 올라가며 진행한다. 만약 루트 노드를 분리하였다면, 새로운 루트 노드를 만든다.
4.  [B-트리](https://ko.wikipedia.org/wiki/B-트리 "wikilink") 와는 달리, 노드 분리(node split) 시에 공간의 특성을 고려하여야 한다. 분리된 MBR들의 겹침(overlap) 정도를 고려하여 분리할 차원(dimension)을 결정하는데, 선형(linear), 사각형(quadratic), 소모적(exhaustive) 분리 알고리즘이 있다.

### 삭제 (deletion)

1.  우선, 지울 값의 위치를 찾는다. 그리고 그 값을 가진 노드를 삭제한다.
2.  부적절한 상태의 노드가 없다면, 삭제 과정을 종료한다.
3.  만약 부적절한 상태의 노드가 있다면, [B-트리](https://ko.wikipedia.org/wiki/B-트리 "wikilink")와 유사하게 해결한다.

## 참고 문헌

  - [Antonin Guttman](https://ko.wikipedia.org/wiki/Antonin_Guttman "wikilink"): *R-Trees: A Dynamic Index Structure for Spatial Searching*, Proc. ACM SIGMOD International Conference on Management of Data,

## 외부 링크

  - [R-tree portal](http://www.rtreeportal.org/)
  - [R-Trees: A Dynamic Index Structure for Spatial Searching](https://web.archive.org/web/20070221040031/http://www-db.deis.unibo.it/courses/SI2/papers/R3.pdf)

[분류:트리 구조](https://ko.wikipedia.org/wiki/분류:트리_구조 "wikilink")