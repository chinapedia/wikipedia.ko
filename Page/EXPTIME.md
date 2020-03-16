> This article is converted from Wikipedia: [EXPTIME](https://ko.wikipedia.org/wiki/EXPTIME).


[계산 복잡도 이론에서](../Page/계산_복잡도_이론.md "wikilink") [복잡도 종류](../Page/복잡도_종류.md "wikilink") **EXPTIME**(**EXP**라고도 한다)은 [결정론적 튜링 기계가](https://ko.wikipedia.org/wiki/결정론적_튜링_기계 "wikilink") [\({\color{Blue}O}(2^{p(n)})\)시간에](https://ko.wikipedia.org/wiki/대문자_O_표기법 "wikilink") 풀 수 있는 모든 [판정 문제의](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") [집합](../Page/집합.md "wikilink")이다. 여기서 \(p(n)\)은 \(n\)에 대한 다항함수이다.

[DTIME](https://ko.wikipedia.org/wiki/DTIME "wikilink")에 대한 식으로 정리하면 이렇다:

\[\mbox{EXPTIME} = \bigcup_{k \in \mathbb{N} } \mbox{ DTIME } \left( 2^{ n^k } \right) .\]

다음과 같은 사실이 알려져 있다.

  -
    [P](../Page/P_\(복잡도\).md "wikilink") ⊆ [NP](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") ⊆ [PSPACE](../Page/PSPACE.md "wikilink") ⊆ EXPTIME ⊆ [NEXPTIME](https://ko.wikipedia.org/wiki/NEXPTIME "wikilink") ⊆ [EXPSPACE](../Page/EXPSPACE.md "wikilink")

또한, [시간 위계 정리와](https://ko.wikipedia.org/wiki/시간_위계_정리 "wikilink") [공간 위계 정리에](https://ko.wikipedia.org/wiki/공간_위계_정리 "wikilink") 따르면 아래와 같다.

  -
    P \(\subsetneq\) EXPTIME  이고  NP \(\subsetneq\) NEXPTIME  이고   PSPACE \(\subsetneq\) EXPSPACE이다

따라서 앞쪽 세 포함관계 중 적어도 하나는 진부분집합이어야 한다. 뒤쪽 세 포함관계도 마찬가지이다. 그러나 어느 것이 진부분집합 관계인지는 알려져 있지 않다. 전문가들은 모든 포함관계가 진부분집합 관계일 것으로 보고 있다. 만약 P = NP라면 EXPTIME = [NEXPTIME](https://ko.wikipedia.org/wiki/NEXPTIME "wikilink")이 성립한다는 사실도 알려져 있다. NEXPTIME은 [비결정론적 튜링 기계가](../Page/비결정론적_튜링_기계.md "wikilink") 지수 시간에 풀 수 있는 문제의 집합이다.\[1\] 더 정확히 말하면, EXPTIME ≠ NEXPTIME이고 오직 그럴 때만 NP 중에 P가 아닌 [희소 언어가](https://ko.wikipedia.org/wiki/희소_언어 "wikilink") 존재한다.\[2\]

EXPTIME은 [교대 튜링 기계가](../Page/교대_튜링_기계.md "wikilink") 다항 공간을 써서 풀 수 있는 문제들의 집합인 [APSPACE](https://ko.wikipedia.org/wiki/APSPACE "wikilink")로 다시 쓸 수 있다. 이것은 PSPACE ⊆ EXPTIME임을 보이는 방법이기도 하다. 교대 튜링 기계는 최소한 결정 튜링 기계보다는 강력하기 때문이다.\[3\]

## EXPTIME-완전

어떤 [판정 문제가](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") EXPTIME에 속하고, EXPTIME의 모든 문제가 그 문제로 [다항 시간 다대일 환산될](https://ko.wikipedia.org/wiki/다항_시간_다대일_환산 "wikilink") 때 그 문제를 EXPTIME-완전이라 한다. 다시 말해서, 다른 어떤 EXPTIME 문제의 인스턴스도 답을 똑같이 유지하면서 그 판정 문제의 인스턴스로 다항 시간에 환산할 수 있는 [알고리즘](../Page/알고리즘.md "wikilink")이 존재한다는 뜻이다. EXPTIME-완전에 속하는 문제는 EXPTIME에서 가장 어려운 문제로 볼 수 있다. NP가 P에 속하는지 아닌지는 아직 모르지만, EXPTIME-완전 문제가 P에 속하지 않는다는 것은 증명되어 있다.

[계산가능성 이론에서](https://ko.wikipedia.org/wiki/계산가능성_이론 "wikilink") 기본적인 결정 불가능 문제 중 하나는 [결정론적 튜링 기계가](https://ko.wikipedia.org/wiki/결정론적_튜링_기계 "wikilink") 특정한 입력 하나를 받아들일지 말지를 판정하는 것이다. 기본적인 EXPTIME-완전 문제 중 하나는 결정론적 튜링 기계가 어떤 입력을 최대 \(k\) 단계에 받아들이는지 아닌지를 묻는 문제이다. 이 문제가 EXPTIME인 이유는 단순한 \(O(k)\)시간 시뮬레이션 방법이 있고, 입력 \(k\)가 \(O(\log k)\)비트를 써서 인코딩되기 때문이다.\[4\] 이 문제가 EXPTIME-완전인 이유는 이 문제를 써서 어떤 기계가 EXPTIME 문제를 지수 단계 안에 받아들일지를 판정할 수 있기 때문이다.

이밖에도 [체스](https://ko.wikipedia.org/wiki/체스 "wikilink"), [체커](../Page/체커.md "wikilink") 등 여러 보드 게임 문제가 EXPTIME-완전 문제이다.

## 외부 링크

  - [복잡도 동물원](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#exp)

## 참고문헌

<references />

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")

1.
2.  Juris Hartmanis, Neil Immerman, Vivian Sewelson. Sparse Sets in NP-P: EXPTIME versus NEXPTIME. *Information and Control*, volume 65, issue 2/3, pp.158–181. 1985. [At ACM Digital Library](http://portal.acm.org/citation.cfm?id=808769)
3.  파파디미트리우 (1994), 20장 1절, 따름정리 3, 495쪽.
4.   슬라이드 24.