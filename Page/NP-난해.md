> This article is converted from Wikipedia: [NP-](https://ko.wikipedia.org/wiki/NP-).


**NP-난해**, **NP-hard**는 [NP에](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") 속하는 모든 [판정 문제를](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") [다항 시간에 다대일 환산할](https://ko.wikipedia.org/wiki/다항_시간_환산 "wikilink") 수 있는 문제들의 [집합](https://ko.wikipedia.org/wiki/집합 "wikilink")이다. 다시 말하면, NP-난해는 적어도 모든 NP 문제만큼은 어려운 문제들의 집합이다.

NP-난해 집합에 속하는 문제가 NP에도 속하면 [NP-완전](https://ko.wikipedia.org/wiki/NP-완전 "wikilink")에 속한다. 즉, NP-완전은 NP와 NP-난해의 교집합이다. 만약 [P-NP 문제가](https://ko.wikipedia.org/wiki/P-NP_문제 "wikilink") P=NP로 풀린다면 P=NP=NP-완전이므로 P와 NP는 NP-난해의 부분집합이 되고, P≠NP인 경우는 P와 NP-난해는 [서로소가](../Page/서로소_집합.md "wikilink") 된다.

NP-난해 집합은 NP에 속하지는 않는다. NP에 속하지 않는 NP-난해 문제의 한 예로는 [정지 문제가](https://ko.wikipedia.org/wiki/정지_문제 "wikilink") 있다. 또한, NP-난해 집합은 판정 문제 뿐만이 아니라 [최적화 문제](https://ko.wikipedia.org/wiki/최적화_문제 "wikilink") 등 다른 형태의 문제가 포함된다.

## 정의

수학적으로는 다음과 같이 정의한다.

  -
    언어 \(L\)이 \(\forall L^\prime\in \mathbf{NP}, L^\prime \leq_p L\!\)이면 \(L\)은 **NP-난해**이다.

## 예제

NP-난해 문제에 들어가는 판정 문제 가운데 대표적인 예로 [부분집합 합 문제](https://ko.wikipedia.org/wiki/부분집합_합_문제 "wikilink")(SUBSET-SUM)가 있다. 이 문제는 정수 집합이 하나 있을 때, 원소를 모두 더하면 0이 되는, 공집합이 아닌 부분집합이 있는지를 묻는 문제이다. 이 문제는 NP에 들어가므로 NP-완전도 된다.

NP-난해이지만 NP-완전은 아닌 판정 문제도 있다. 예를 들어 [정지 문제가](https://ko.wikipedia.org/wiki/정지_문제 "wikilink") 있다. "한 프로그램이 있고, 그 프로그램에 대한 입력이 있을 때, 이 프로그램은 영원히 돌 것인가?" 하는 문제이다. 정지 문제가 NP-난해인 것은 NP-완전 문제인 [충족 가능성 문제를](https://ko.wikipedia.org/wiki/충족_가능성_문제 "wikilink") 정지 문제로 환산하는 것으로 보일 수 있다. 이때 정지 문제의 입력으로 받는 [튜링 기계는](https://ko.wikipedia.org/wiki/튜링_기계 "wikilink") 입력으로 받은 식에 대해서 식을 만족하는 진리값을 발견할 때에만 멈추고 그렇지 않으면 무한 루프에 빠지도록 설계하면 된다. 또한 정지 문제는 NP에 속하지 않는데, 이것은 NP 문제는 유한 번의 연산으로 판정이 가능하지만 정지 문제는 그렇지 않기 때문이다.

## 다른 정의

NP-난해의 정의에서 다항 시간 다대일 환산을 다항 시간 [튜링 환산으로](https://ko.wikipedia.org/wiki/튜링_환산 "wikilink") 정의하는 경우도 있다. 이 정의가 앞에서의 정의와 같은지 다른지는 아직 해결되지 않은 문제이다. 이 방식은 판정 문제뿐만이 아니라 [함수 문제에](https://ko.wikipedia.org/wiki/함수_문제 "wikilink") 대해서도 형식화할 수 있다는 장점이 있다.

이 정의에서 어떤 문제 L이 NP-난해라는 것은 L에 대한 신탁을 주는 [신탁 기계를](https://ko.wikipedia.org/wiki/신탁_기계 "wikilink") 사용하여 NP에 속하는 모든 판정 문제 \(L' \in \mathbf{N}\)를 다항 시간 안에 풀 수 있다는 의미이다. 즉, L을 푸는 함수가 단위 시간만이 걸린다고 가정할 때 \(L'\)은 다항 시간 안에 풀 수 있다는 의미이다.

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")