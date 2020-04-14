> This article is converted from Wikipedia: [PSPACE-완전](https://ko.wikipedia.org/wiki/PSPACE-완전).


[계산 복잡도 이론에서](../Page/계산_복잡도_이론.md "wikilink") **PSPACE-완전**은 [복잡도 종류이다](../Page/복잡도_종류.md "wikilink"). [판정 문제는](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") **[PSPACE](../Page/PSPACE.md "wikilink")**에 들어 있고, 모든 PSPACE 문제가 이 문제로 [다항 시간 다대일 환산될](https://ko.wikipedia.org/wiki/다항_시간_다대일_환산 "wikilink") 수 있으면 PSPACE-완전이 된다. PSPACE-완전에 드는 문제는 PSPACE에서 가장 어려운 문제로 볼 수 있다. 이 문제들은 [P나](../Page/P_\(복잡도\).md "wikilink") [NP의](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") 범위 바깥에 있을 것으로 보이지만, 아직 증명되지는 않았다. PSPACE-완전이 [NC](../Page/NC_\(복잡도\).md "wikilink") 바깥에 있다는 것은 증명되었다.

[NP-완전](../Page/NP-완전.md "wikilink")에 들어간다고 밝혀진 첫 문제는 [충족 가능성 문제](../Page/충족_가능성_문제.md "wikilink")()이다. 논리식이 참이 되도록 변수값을 할당할 수 있는지를 묻는 문제이다. 예를 들어, 다음 논리식을 참이 되게 할 수 있는지를 물을 수 있다.

  -
    \(\exists x_1 \, \exists x_2 \, \exists x_3 \, \exists x_4: (x_1 \lor \neg x_3 \lor x_4) \land (\neg x_2 \lor x_3 \lor \neg x_4)\)

SAT 문제는 [TQBF](https://ko.wikipedia.org/wiki/참_한정_불_식 "wikilink") 문제로 일반화할 수 있다. 이 문제는 가장 기본이 되는 PSPACE-완전 문제이다. 이 문제의 인스턴스는 전칭기호를 허용한다는 점을 빼면 SAT하고 비슷하다.

  -
    \(\exists x_1 \, \forall x_2 \, \exists x_3 \, \forall x_4: (x_1 \lor \neg x_3 \lor x_4) \land (\neg x_2 \lor x_3 \lor \neg x_4)\)

NP-완전 문제는 전형적인 퍼즐과 닮았다는 점을 주목할 필요가 있다. 전형적인 퍼즐은 문제를 풀기 위해 값을 끼워맞출 방법이 있는지를 묻는다. PSPACE-완전 문제는 게임을 닮았다. 게임은 상대방이 할 수 있는 *모든* 이동에 대해, 내가 *어떤* 이동을 할 수 있는지, 내가 이기기 위해 *어떤* 이동을 할 수 있는지를 묻는다. 이 질문은 존재기호나 전칭기호를 대신한다. 수많은 퍼즐이 NP-완전이고, 수많은 게임이 PSPACE-완전인 것은 놀라운 일이 아니다.

PSPACE-완전에 들어가는 게임(*n* × *n* 말판에서 할 수 있도록 일반화한 것)으로는 [헥스](https://ko.wikipedia.org/wiki/헥스_\(보드_게임\) "wikilink"), [리버시](https://ko.wikipedia.org/wiki/리버시 "wikilink"), 솔리테어 게임인 [러시아워](https://ko.wikipedia.org/wiki/러시아워_\(보드_게임\) "wikilink"), [마종](../Page/마작.md "wikilink"), [소코반](https://ko.wikipedia.org/wiki/소코반 "wikilink"), [아토믹스](https://ko.wikipedia.org/wiki/아토믹스 "wikilink") 들이 있다. 일반화한 다른 게임으로 [바둑](../Page/바둑.md "wikilink"), [체스](https://ko.wikipedia.org/wiki/체스 "wikilink"), [체커](../Page/체커.md "wikilink")는 [EXPTIME-완전](https://ko.wikipedia.org/wiki/EXPTIME-완전 "wikilink")에 들어간다. 완벽한 두 사람이 한다면 게임은 매우 길어질 수 있기 때문에 PSPACE에 들어갈 것으로 보이지 않는다.

PSPACE-완전의 정의는 *점근* 복잡도에 기반하고 있다. 크기 *n*인 문제를 푸는 데 걸리는 시간은 *n*이 커짐에 따라 한없이 늘어나는 한계 안에 있다. 이는 8 × 8 말판에서 하는 체커 같은 게임은 절대로 PSPACE-완전일 수 없다는 뜻이다. (사실, 아주 큰 [검색 테이블을](https://ko.wikipedia.org/wiki/검색_테이블 "wikilink") 쓰면 상수 시간에 풀 수 있다.) 이 때문에 게임을 *n* × *n* 말판으로 일반화하여 다룬다. 체스 같은 몇몇 경우에는 이러한 확장은 인위적이고 주관적이기도 하다.

다른 PSPACE-완전 문제로는 주어진 문자열이 [문맥-민감 문법으로](https://ko.wikipedia.org/wiki/문맥-민감_문법 "wikilink") 정의한 어떤 언어에 들어가는지를 판정하는 문제가 있다.

## 더 보기

  - [게임 복잡도](https://ko.wikipedia.org/wiki/게임_복잡도 "wikilink")

## 참고문헌

  -
  -
## 외부 링크

  - [게임과 퍼즐의 계산 복잡도](http://www.ics.uci.edu/~eppstein/cgt/hard.html)

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")