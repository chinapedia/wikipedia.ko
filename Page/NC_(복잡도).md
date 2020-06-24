> This article is converted from Wikipedia: [NC \(복잡도\)](https://ko.wikipedia.org/wiki/NC_\(복잡도\)).


[계산 복잡도 이론에서](../Page/계산_복잡도_이론.md "wikilink") **NC**(Nick's Class)는 프로세서가 다항 개인 [병렬 컴퓨터가](https://ko.wikipedia.org/wiki/병렬_컴퓨터 "wikilink") 다항로그 시간에 판정할 수 있는 [판정 문제의](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") 집합이다. 다시 말해서, 어떤 문제가 **NC**라는 것은, 이 문제를 상수 \(c\)와 \(k\)에 대해서 병렬 프로세서 \(O(n^k)\)개를 써서 \(O(\log^c n)\)시간에 풀 수 있다는 뜻이다. [스티븐 쿡은](../Page/스티븐_쿡.md "wikilink") 회로를 다항로그 깊이와 다항 크기에 대해서 연구를 많이 한 [닉 피펜저의](https://ko.wikipedia.org/wiki/닉_피펜저 "wikilink") 이름을 따서 라는 이름을 지었다.

**[P](../Page/P_\(복잡도\).md "wikilink")**를 결정론적 튜링 기계가 다룰 수 있는 문제들로 보는 것과 마찬가지로, **NC**도 병렬 컴퓨터가 효율 있게 다룰 수 있는 문제로 볼 수 있다. 병렬 컴퓨터는 순차 컴퓨터가 시뮬레이트할 수 있기 때문에 **NC**는 **P**의 부분집합이다. **NC** = **P**인지는 아직 밝혀지지 않았지만, 학계에서는 이 명제가 거짓일 것으로 보고 있다. "본래 순차"이기 때문에 병렬화해서 빠르게 할 수 없는 문제가 존재할 것이라는 뜻이다. **[NP-완전](../Page/NP-완전.md "wikilink")**을 "다룰 수 없을 것 같은" 문제로 보는 것과 같다. 따라서 **[P-완전](../Page/P-완전.md "wikilink")**도 "병렬화할 수 없을 것 같은", "본래 순차일 것 같은" 문제로 생각할 수 있다.

이 정의에서 병렬 컴퓨터는 *병렬이고 임의로 접근할 수 있는 기계*([PRAM](https://ko.wikipedia.org/wiki/병렬_임의_접근_기계 "wikilink"))라고 볼 수 있다. 이 기계는 메모리를 공유하는 병렬 컴퓨터로, 어떤 프로세서도 메모리에 있는 임의의 비트를 상수 시간에 접근할 수 있다. **NC**의 정의는 PRAM이 여러 프로세서가 동시에 한 비트에 접근하는 방법을 어떻게 제어하는지에 영향을 받지 않는다. 그 방법에는 CRCW, CREW, EREW 등이 있다. 이러한 모델에 대한 설명은 [PRAM을](https://ko.wikipedia.org/wiki/병렬_임의_접근_기계 "wikilink") 참고하라.

이와 동등하게 **NC**는 [다항로그](https://ko.wikipedia.org/wiki/다항로그 "wikilink") 깊이에 [게이트가](https://ko.wikipedia.org/wiki/논리_게이트 "wikilink") 다항개인 [균일 불 회로가](https://ko.wikipedia.org/wiki/불_회로 "wikilink") 판정할 수 있는 판정 문제들로 정의할 수 있다.

\(\mathbf{NC}^i\)는 게이트가 다항개이고 깊이가 \(O(\log^i n)\)인 균일 불 회로로 판정할 수 있는 판정 문제의 복잡도 종류이다. 즉, 프로세서가 다항개인 병렬 컴퓨터로 \(O(\log^i n)\) 시간에 풀 수 있는 판정 문제의 집합이다.

**NC**를 공간 복잡도인 **[L](https://ko.wikipedia.org/wiki/L_\(복잡도\) "wikilink")** and **[NL](https://ko.wikipedia.org/wiki/NL_\(복잡도\) "wikilink")**와 관련지을 수 있다. [크리스토스 파파디미트리우가](../Page/크리스토스_파파디미트리우.md "wikilink") 지은 《계산 복잡도》에 나오는 정리 16.1에 따르면 다음 관계가 성립한다고 한다.

\(\mathbf{NC_1 \subseteq L \subseteq NL \subseteq NC_2}\)

이와 비슷하게, \(\mathbf{NC}^i\)는 [교대 튜링 기계가](../Page/교대_튜링_기계.md "wikilink") \(O(\log n)\) 공간을 쓰고 \(\log ^{O(1)} n\)만큼 교대를 해서 풀 수 있는 문제의 집합과 같다.

## 참고 문헌

  - Greenlaw, Raymond, James Hoover, and Walter Ruzzo. *Limits To Parallel computation; P-Completeness Theory*.

  - Heribert Vollmer. *[Introduction to Circuit Complexity -- A Uniform Approach](https://web.archive.org/web/20061231011947/http://www.thi.uni-hannover.de/forschung/publikationen/cc/index.en.php)*.

  -
  -
[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink") [분류:회로 복잡도](https://ko.wikipedia.org/wiki/분류:회로_복잡도 "wikilink")