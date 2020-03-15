> This article is converted from Wikipedia: [AVL ](https://ko.wikipedia.org/wiki/AVL_).


| AVL 트리의 시간복잡도 |
| ------------- |
| |             |
| 공간            |
| 검색            |
| 삽입            |
| 삭제            |

**AVL 트리**(AVL tree)는 가장 초기에 나온 균형 잡힌(balanced) [이진 탐색 트리이다](https://ko.wikipedia.org/wiki/이진_탐색_트리 "wikilink"). 1962년 G.M. Adelson-Velskii와 E.M. Landis 가 그들의 논문 "An algorithm for the organization of information"\[1\] 을 통해 발표했고 그들의 이름을 따서 지어졌다. AVL 트리는 각각의 노드(node, 분기점)마다 왼쪽과 오른쪽 부분 트리(sub-tree)의 높이 차이에 대한 정보를 가지며 부분 트리의 높이 차이가 1보다 크지 않은 성질을 가진다. 균형 잡힌 AVL 트리는 n개의 원소가 있을 때 [O](https://ko.wikipedia.org/wiki/점근_표기법 "wikilink")(log *n*) 의 시간복잡도로 검색, 삽입, 삭제를 할 수 있다. 그러나 삽입과 삭제를 할 때에는 원하는 노드를 찾기 위해 2개의 경로가 필요하기 때문에 [레드-블랙 트리](../Page/레드-블랙_트리.md "wikilink") 만큼 효율이 좋지 않아 자주 쓰이지는 않는다.\[2\]

## 정의와 성질

  - **높이 균형 성질**(height-balance property): 트리 \(T\)의 모든 내부 노드(internal node) \(v\)에 대하여 \(v\)의 자식 노드들의 높이 차이가 최대 1이다.

<!-- end list -->

  - 임의의 이진 탐색 트리 \(T\)가 높이 균형 성질을 만족할 때 AVL 트리라고 한다.

높이 균형 성질(height-balance property)로 부터 \(n\)개의 원소를 갖는 AVL 트리의 높이는 \(log n\)이라는 사실을 알 수 있다.

이진 탐색 트리에서의 검색 시간복잡도는 트리의 높이 이므로 AVL 트리의 검색 시간이 \(O(\log n)\) 임을 알 수 있다.

## 동작

AVL 트리에서 노드를 일반적인 이진 탐색 트리처럼 삽입, 삭제 시키면 높이 균형 성질을 만족하지 않게 된다. 노드가 삽입, 삭제될 때 회전(rotation)을 통해 트리를 재구성하여 높이 균형 성질을 유지시킨다.

### 삽입

AVL 트리 T에 새로운 노드 d를 삽입(Insertion)하는 방법은 T에서 d가 단말 노드(leaf node)로 삽입될 수 있도록 하는 노드 w를 찾고 w의 자식으로 d를 삽입한다.

d를 삽입하면 불균형해질 수 있는데 세 노드를 기준으로 회전(rotation)시킴으로써 균형을 맞춘다.

### 회전

트리 \(T\)의 재구성 작업을 회전(Rotation)이라 한다.

회전의 기준이 되는 세 노드 \(x\), \(y\), \(z\)는 다음과 같다. \(z\)는 \(w\)로부터 root로 가는 경로상에 가장 처음으로 위치한 불균형한 노드이다. \(y\)는 \(z\)의 자식 중에서 가장 큰 높이를 갖는 노드이다. \(x\)는 \(y\)의 자식 중에서 가장 큰 높이를 갖는 노드이다.

\(x\)가 이진 탐색 트리 \(T\)의 노드이고 \(y\)가 부모, \(z\)가 할아버지 노드일 때 다음과 같이 재구성한다.

1.  \(x\), \(y\), \(z\) 를 왼쪽-오른쪽 순서 (inorder)로 나열 한 순서대로 \(a\), \(b\), \(c\) 라고 하고, \(x\), \(y\), \(z\)의 4개의 부분 트리들을 왼쪽-오른쪽 순서 (inorder)로 나열한 것을 \(T_{0}\), \(T_{1}\), \(T_{2}\), \(T_{3}\) 라고 하자.
2.  \(z\)가 root인 부분 트리를 \(b\)를 root로 하는 새로운 부분 트리로 바꾼다.
3.  \(a\)가 \(b\)의 왼쪽 자식이 되고 \(T_{0}\), \(T_{1}\)은 각각 \(a\)의 왼쪽, 오른쪽 자식이 된다.
4.  \(c\)가 \(b\)의 오른쪽 자식이 되고, \(T_{2}\), \(T_{3}\)는 각각 \(c\)의 왼쪽, 오른쪽 자식이 된다.

이 작업을 구상화하면 \(b=y\) 일 때 \(y\)를 \(z\)와 회전시키는 것처럼 보인다. 이 작업을 single rotation이라고 한다.

\(b=x\) 일 때 \(x\)를 \(y\)와 회전시키고 다시 \(z\)와 회전시키는 것처럼 보인다. 이 작업을 double rotation이라고 한다.

이 재구성 방법은 \(T\)의 부모-자식 관계만을 바꾸는 것이기 때문에 \(O(1)\) 시간이 걸린다.

### 삭제

AVL 트리 \(T\)에서 노드 \(d\)를 삭제(Removal)하는 방법은 root부터 \(d\)를 검색한다. \(d\)가 단말 노드가 아니라면 자신의 왼쪽 부분 트리 중에서 최댓값을 갖는 노드나 오른쪽 부분 트리 중에서 최솟값을 갖는 노드를 \(d\)와 바꾼다. 이 작업을 \(d\)가 단말 노드가 될 때까지 반복하여 단말 노드 \(d\)를 삭제한다.

삭제 역시 트리가 불균형해질 수 있는데 삽입과 동일한 방법으로 \(d\)의 부모를 \(w\)라고 한 뒤 회전시켜 균형을 맞춘다.

## 각주

## 참고 문헌

  - Robert Lafore(1998), *Data Structures & Algorithms in JAVA*, Sams,
  - Michael T.Goodrich, Roberto Tamassia(2006), *Data Structures & Algorithms in JAVA(4th edition)*, John Wiley & Sons,

[분류:이진 트리](https://ko.wikipedia.org/wiki/분류:이진_트리 "wikilink") [분류:소련의 발명품](https://ko.wikipedia.org/wiki/분류:소련의_발명품 "wikilink")

1.   (Russian) English translation by Myron J. Ricci in *Soviet Math. Doklady*, 3:1259–1263, 1962.
2.  Robert Lafore(1998), *Data Structures & Algorithms in JAVA*, Sams, p. 334.