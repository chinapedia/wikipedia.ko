> This article is converted from Wikipedia: [MAX-SNP](https://ko.wikipedia.org/wiki/MAX-SNP).


[계산 복잡도 이론에서](https://ko.wikipedia.org/wiki/계산_복잡도_이론 "wikilink") **MAX-SNP**는 최적화 문제의 근사 가능성에 대한 [복잡도 종류이다](https://ko.wikipedia.org/wiki/복잡도_종류 "wikilink"). [SNP는](https://ko.wikipedia.org/wiki/SNP_\(복잡도\) "wikilink") 를 줄인 말이다. 엄격한()이라는 말이 앞에 붙은 이유는 MAX-SNP가 [NP에](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") 대한 약한 [검증자](https://ko.wikipedia.org/wiki/검증자 "wikilink")()와 관련되기 때문이다.

MAX-SNP 문제는 MAX-SNP<sub>0</sub> 이라는 문제로 [L-환산](https://ko.wikipedia.org/wiki/L-환산 "wikilink")()이 되는 최적화 문제의 집합이다. L-환산이란 [NP-난해](../Page/NP-난해.md "wikilink")를 증명할 때 쓰는 [다항 시간 환산과](https://ko.wikipedia.org/wiki/다항_시간_환산 "wikilink") 달리 근사 가능성까지 보존하는 [환산이다](../Page/환산_\(복잡도\).md "wikilink"). 따라서 MAX-SNP는 MAX-SNP<sub>0</sub>과 근사 가능성이 같은 문제의 집합이라고 볼 수 있다. 뒤에 나오는 결과를 써서 정리하면 이것은 최적해의 상수배 이내로 근사가 가능한 문제의 집합과 같다.

다른 복잡도 종류와 비슷하게 **[MAX-SNP-완전](https://ko.wikipedia.org/wiki/MAX-SNP-완전 "wikilink")**과 **[MAX-SNP-난해](https://ko.wikipedia.org/wiki/MAX-SNP-난해 "wikilink")** 복잡도 종류도 정의할 수 있다. [NP-완전](https://ko.wikipedia.org/wiki/NP-완전 "wikilink")이 [다항 시간에](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 풀리지 않을 것으로 예상되는 문제의 집합인 것과 비슷하게, MAX-SNP-완전 문제는 [PTAS](https://ko.wikipedia.org/wiki/PTAS "wikilink")를 가지지 않을 것으로 예상되는 문제의 집합이다. 만약 MAX-SNP-난해 문제 중 하나라도 PTAS를 가지면 다른 모든 MAX-SNP-난해 문제가 PTAS를 가질 뿐만 아니라 [P=NP까지](https://ko.wikipedia.org/wiki/P-NP_문제 "wikilink") 성립하게 된다. 현재 학계에서는 P와 NP는 다르다고 보고 있으므로, MAX-SNP-난해 문제 역시 PTAS를 가지지 않을 것으로 본다. 어떤 문제가 MAX-SNP-완전인지 아닌지는 주로 기본 문제인 [MAX3SAT](https://ko.wikipedia.org/wiki/MAX3SAT "wikilink")으로 L-환산을 해서 증명한다. 이는 NP-완전을 증명할 때 [충족 가능성 문제로](https://ko.wikipedia.org/wiki/충족_가능성_문제 "wikilink") [다항 시간 환산을](https://ko.wikipedia.org/wiki/다항_시간_환산 "wikilink") 하는 것과 비슷하다.

## 참고문헌

  - [복잡도 동물원 MaxSNP 우리](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#maxsnp)

  -
[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")