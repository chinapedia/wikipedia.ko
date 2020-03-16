> This article is converted from Wikipedia: [-P](https://ko.wikipedia.org/wiki/-P).


[계산 복잡도 이론에서](../Page/계산_복잡도_이론.md "wikilink") [복잡도 종류](../Page/복잡도_종류.md "wikilink") **\#P**는 개수를 세는 문제들로 이루어진 집합으로, 여기에 들어 있는 문제는 **[NP](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink")**에 속한 [판정 문제와](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") 연관된다. 다른 복잡도 종류하고 다르게 **\#P**는 판정문제가 아니라 [함수 문제의](https://ko.wikipedia.org/wiki/함수_문제 "wikilink") 집합이다.

**\#P**는 '샤프 피()'라고 읽는다. 어떤 문서에서는 '넘버 피()'라고 읽기도 한다.

**NP**문제는 "특정한 제약조건을 만족하는 해가 있는가?" 하는 형식인 경우가 많다. 예:

  - 주어진 정수 집합에 원소의 합이 0인 부분집합이 있는가? ([부분집합 합 문제](https://ko.wikipedia.org/wiki/부분집합_합_문제 "wikilink"))
  - 주어진 [그래프](https://ko.wikipedia.org/wiki/그래프 "wikilink")에서 비용이 100보다 작은 [해밀턴 순환이](https://ko.wikipedia.org/wiki/해밀턴_순환 "wikilink") 있는가? ([외판원 문제](../Page/외판원_문제.md "wikilink"))
  - 주어진 [CNF](https://ko.wikipedia.org/wiki/논리곱_표준형 "wikilink") 식을 만족하는 논리값이 있는가? ([충족 가능성 문제](../Page/충족_가능성_문제.md "wikilink"))

여기에 대응하는 **\#P**문제는 해가 '있는지'를 묻지 않고 '몇 개인지'를 묻는다. 예:

  - 주어진 정수 집합에서 원소의 합이 0인 부분집합은 몇 개인가?
  - 주어진 그래프에서 비용이 100보다 작은 해밀톤 회로가 몇 개인가?
  - 주어진 [CNF](https://ko.wikipedia.org/wiki/논리곱_표준형 "wikilink") 식을 만족하는 논리값이 몇 개인가?

좀 더 공식적으로 정의하면, **\#P**는 "f(x)를 계산"하는 꼴로 된 함수문제의 집합이다. 여기서 f는 NP 기계가 받아들이는 경로 개수를 뜻한다.

**\#P** 문제는 적어도 대응하는 **NP** 문제만큼 어려워야 한다는 것은 쉽게 알 수 있다. 답이 몇 개인지 쉽게 셀 수 있다면 답이 있는지 없는지도 쉽게 알 수 있다. 개수를 세어서 0보다 큰지만 살피면 된다. 따라서 **[NP-완전](../Page/NP-완전.md "wikilink")** 문제에 대응하는 **\#P** 문제는 반드시 **[NP-난해](../Page/NP-난해.md "wikilink")** 문제가 된다.

놀랍게도 어떤 **\#P** 문제는 대응하는 문제가 **[P](../Page/P_\(복잡도\).md "wikilink")** 문제라도 어려운 경우가 있다. (정확히 말하면, 어렵다고 추측하는 것이다. 아직 [P-NP 문제가](../Page/P-NP_문제.md "wikilink") 해결되지 않았으니까.) 이러한 문제에 관한 내용은 **[\#P-완전](https://ko.wikipedia.org/wiki/샤프-P-완전 "wikilink")**에 있다.

**\#P**에 가장 가까운 판정 문제 종류는 다수(과반수)인 계산 경로를 받아들였는지를 묻는 **[PP](https://ko.wikipedia.org/wiki/PP_\(복잡도\) "wikilink")**이다. 이것은 **\#P** 문제가 내는 답의 [최상위 비트를](https://ko.wikipedia.org/wiki/최상위_비트 "wikilink") 찾는다. 판정 문제 종류 중 **[⊕P](https://ko.wikipedia.org/wiki/패리티_P "wikilink")**는 [최하위 비트를](../Page/최하위_비트.md "wikilink") 찾는다.

[토다 정리](https://ko.wikipedia.org/wiki/토다_정리 "wikilink")(, ()의 이름을 땄다)에서 나오는 결론 중 하나는, **\#P** 신탁이 있는 다항 시간 기계(**P**<sup>**\#P**</sup>)는 **[PH](../Page/PH_\(복잡도\).md "wikilink")**에 속하는 모든 문제를 풀 수 있다는 것이다. 여기서 **PH**는 [다항 계층에](https://ko.wikipedia.org/wiki/다항_계층 "wikilink") 속하는 모든 복잡도 종류의 합집합이다. 실제로 다항 시간 기계는 **PH**에 속한 어떤 문제라도 **\#P** 질의 하나만으로 풀어낼 수 있다. 이런 까닭에 **\#P-완전** 문제를 정확히 풀기는 엄청나게 어려울 것으로 미루어 볼 수 있다.

## 외부 링크

  - [ZPP](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#zpp) - 복잡도 동물원

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")