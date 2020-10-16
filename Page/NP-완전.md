> This article is converted from Wikipedia: [NP-완전](https://ko.wikipedia.org/wiki/NP-완전).


[thumb](https://ko.wikipedia.org/wiki/파일:P_np_np-complete_np-hard.svg "wikilink") **NP-완전**(NP-complete, **NP-C**, **NPC**)은 [NP](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") 집합에 속하는 [결정 문제](https://ko.wikipedia.org/wiki/결정_문제 "wikilink") 중에서 가장 어려운 문제의 부분집합으로, 모든 NP 문제를 다항 시간 내에 NP-완전 문제로 [환산할](../Page/환산_\(복잡도\).md "wikilink") 수 있다. NP-완전 문제 중 하나라도 [P에](../Page/P_\(복잡도\).md "wikilink") 속한다는 것을 증명한다면 모든 NP 문제가 P에 속하기 때문에, [P-NP 문제가](../Page/P-NP_문제.md "wikilink") P=NP의 형태로 풀리게 된다. 반대로 NP-완전 문제 중의 하나가 P에 속하지 않는다는 것이 증명된다면 P=NP에 대한 반례가 되어 P-NP 문제는 P≠NP의 형태로 풀리게 된다.

## 정의

NP-완전은 다음의 조건을 만족하는 [결정 문제](https://ko.wikipedia.org/wiki/결정_문제 "wikilink") *C*의 집합이다:

1.  *C*가 NP에 속한다.
2.  NP에 속하는 모든 문제를 [다항 시간](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 안에 *C*로 변환할 수 있다. 즉, 다항 시간 [환산을](../Page/환산_\(복잡도\).md "wikilink") 할 수 있다.

여기에서 두 번째 조건은 [NP-난해](../Page/NP-난해.md "wikilink")의 정의이고, 즉 NP-완전은 NP-난해 중 NP인 문제들의 집합이다. 또한 위 정의에서 알 수 있듯이, NP-완전인 *C*를 다항시간 안에 풀 수 있다면 모든 NP-완전 문제를 다항시간 안에 풀 수 있다.

## 역사

NP-완전이라는 개념은 [1971년](../Page/1971년.md "wikilink")에 [스티븐 쿡이](../Page/스티븐_쿡.md "wikilink") 제시했지만, 그가 용어를 처음 만든 것은 아니다. 쿡은 [충족 가능성 문제](../Page/충족_가능성_문제.md "wikilink")(SAT)가 위 정의의 두 가지 조건을 모두 만족한다는 것을 증명했다([쿡-레빈 정리](../Page/쿡-레빈_정리.md "wikilink")). [1972년](../Page/1972년.md "wikilink")에 [리처드 카프는](https://ko.wikipedia.org/wiki/리처드_카프 "wikilink") 21가지의 다른 문제들도 마찬가지로 위 두 가지 조건을 만족한다는 것을 증명했다. 쿡이 최초의 NP-완전 문제를 발견한 이후로, 많은 사람들이 NP-완전 문제라고 이미 알려진 문제로부터 환산하는 방법으로 수많은 문제들 역시 NP-완전임을 증명했다. [게리와](https://ko.wikipedia.org/wiki/마이클_게리 "wikilink") [존슨이](https://ko.wikipedia.org/wiki/데이비드_S._존슨 "wikilink") [1979년](../Page/1979년.md "wikilink")에 *Computers and Intractability: A Guide to NP-Completeness*를 통해 여러 NP-완전 문제들을 소개하였다.

## 근사 알고리즘

현재 NP-완전 문제를 다항 시간 안에 푸는 알고리즘은 발견되지 않았고, 또한 그러한 알고리즘이 존재할 것인지도 알려지지 않았다. 대신, 특정한 NP-완전 문제에 대한 [근사 알고리즘이](../Page/근사_알고리즘.md "wikilink") 알려져 있다.

## NP-완전 문제의 예

  - [해밀턴 경로](../Page/해밀턴_경로.md "wikilink") 문제
  - [충족 가능성 문제](../Page/충족_가능성_문제.md "wikilink")(SAT)
  - [외판원 문제](../Page/외판원_문제.md "wikilink")
  - [그래프 색칠 문제](https://ko.wikipedia.org/wiki/그래프_색칠_문제 "wikilink")
  - [시간표 짜기](https://ko.wikipedia.org/wiki/시간표_짜기 "wikilink")

## 참조

  - [P-NP 문제](../Page/P-NP_문제.md "wikilink")

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink") [\*](https://ko.wikipedia.org/wiki/분류:NP-완전_문제 "wikilink")