> This article is converted from Wikipedia: [RP \(복잡도\)](https://ko.wikipedia.org/wiki/RP_\(복잡도\)).


[복잡도 이론에서](../Page/계산_복잡도_이론.md "wikilink"), **RP** (확률적 다항시간, randomized polynomial time)은 다음과 같은 성질을 만족하는 [확률적 튜링 기계가](https://ko.wikipedia.org/wiki/확률적_튜링_기계 "wikilink") 존재하는 문제들의 [복잡도 종류이다](../Page/복잡도_종류.md "wikilink").

  - 확률적 튜링 기계의 실행시간은 입력의 크기를 기준으로 다항시간이어야 한다.
  - 실제 결과가 '아니오'일 때, 확률적 튜링 기계의 실행결과는 항상 '아니오'이다.
  - 실제 결과가 '예'일 때, 확률적 튜링 기계의 실행결과는 최소 1/2의 확률로 '예'라는 결과를 내놓는다.

[알고리즘](../Page/알고리즘.md "wikilink")으로 표현하자면, [확률적으로](../Page/확률적_알고리즘.md "wikilink") 진행하면서 실제 결과가 '예'일 때만 '예'라는 답을 내놓는 알고리즘이다. 그러므로 알고리즘 실행결과 '예'라는 결과가 나왔으면, 실제 결과는 항상 '예'이다. 그러나 알고리즘 실행결과 '아니오'가 나왔으면 실제로는 '예'일 수도 있고 '아니오'일 수도 있다.

일부 사람들은 이 복잡도 종류를 RP 대신 **R**이라고 하는 경우도 있으나, [R은](https://ko.wikipedia.org/wiki/R_\(복잡도\) "wikilink") 보통 [재귀 언어](https://ko.wikipedia.org/wiki/재귀_언어 "wikilink") 종류를 가리킬 때 사용한다.

## 관련 복잡도 종류

  - RP에 속하는 문제는 '예'라는 답이 나오면 언제나 옳은 결과가 나온 것이지만, '아니오'라는 답이 나오면 일반적으로 옳은 결과가 나온 것이다. 즉, YES instance는 모두 accept하지만 NO instance는 accept하거나 reject하는 것이다. **co-RP**도 비슷하게 정의할 수 있는데, 이 경우에는 '아니오'라는 답이 나오는 경우는 언제나 옳은 결과가 나온 것이지만 '예'라는 답이 나오면 일반적으로 옳은 결과가 나온 것이다.
  - 일부에서는 RP를 R이라고 하는 경우가 있는데, 이때 마찬가지로 co-RP를 co-R이라고 부른다.
  - [BPP](https://ko.wikipedia.org/wiki/BPP "wikilink")는 '예' '아니오'의 답이 나오는 경우 모두 잘못된 답이 나올 수 있는 알고리즘의 집합이다.
  - RP와 co-RP의 교집합은 [ZPP](../Page/ZPP.md "wikilink")라고 한다.

## P-NP 문제와 연관성

[P는](../Page/P_\(복잡도\).md "wikilink") RP의 부분집합이며, RP는 [NP의](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") 부분집합이다. 마찬가지로, P는 co-RP의 부분집합이고, co-RP는 [co-NP](https://ko.wikipedia.org/wiki/co-NP "wikilink")의 부분집합이다. 이런 부분집합 관계가 [진부분집합](https://ko.wikipedia.org/wiki/진부분집합 "wikilink")인지는 아직 알려지지 않았다. 그러나 P ≠ RP이거나 RP ≠ NP일 것으로 추측되고 있다. 이렇지 않다면 P = NP가 성립하는데, 일반적으로 P는 NP와 같지 않을 것으로 예상되기 때문이다. 마찬가지로 RP = co-RP인지, 또 RP가 NP와 co-NP의 교집합에 포함되는지도 알려지지 않았다.

## 같이 보기

  - [확률적 알고리즘](../Page/확률적_알고리즘.md "wikilink")

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")