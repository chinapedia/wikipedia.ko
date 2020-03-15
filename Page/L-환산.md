> This article is converted from Wikipedia: [L-](https://ko.wikipedia.org/wiki/L-).


**L-환산**(, linear reduction)은 [최적화 문제](https://ko.wikipedia.org/wiki/최적화_문제 "wikilink") 간의 근사 비율을 선형 보존하는 [환산이다](../Page/환산_\(복잡도\).md "wikilink"). 여기에서 'L'의 의미는 선형(linear)을 가리킨다.

## 정의

최적화 문제 \(A, B\)와 각 문제의 비용 함수 \(c_A, c_B\)에 대해서, 함수 \(f, g\)와 양수 \(\alpha, \beta\)가 다음의 조건을 만족할 경우 \((f, g, \alpha, \beta)\)를 A에서 B로의 **L-환산**이라고 정의한다.

  - 두 함수 \(f, g\)는 다항 시간에 계산가능하다.
  - 문제 \(A\)에 속하는 입력 \(x\)에 대해, \(f(x)\)는 문제 \(B\)의 입력이다.
  - 문제 \(B\)에 속하는 입력 \(f(x)\)의 해가 \(y\)일 때, \(g(y)\)는 문제 \(A\)의 입력 \(x\)에 해당하는 해이다.
  - 입력 \(x\)에 대한 최적 비용이 \(OPT_A(x)\)일 때, 모든 \(x\)에 대해 \(\mathrm{OPT_B}(f(x)) \le \alpha \mathrm{OPT_A}(x)\)를 만족하는 양수 \(\alpha\)가 존재한다.
  - 입력 \(f(x)\)의 해가 \(y\)일 때, 모든 \(y\)에 대해 \(|\mathrm{OPT_A}(x)-c_A(g(y))| \le \beta |\mathrm{OPT_B}(f(x))-c_B(y)|\)를 만족하는 양수 \(\beta\)가 존재한다.

L-환산이 존재할 경우, 만약 A에 대한 \(\epsilon\)-[근사 알고리즘이](../Page/근사_알고리즘.md "wikilink") 존재한다면 그 알고리즘은 B에 대한 \(\alpha\beta\epsilon\)-근사 알고리즘으로도 사용할 수 있다. 즉, B에 대한 [다항 시간 근사 해법](../Page/다항_시간_근사_해법.md "wikilink")(PTAS)이 존재하게 된다.

[분류:근사 알고리즘](https://ko.wikipedia.org/wiki/분류:근사_알고리즘 "wikilink")