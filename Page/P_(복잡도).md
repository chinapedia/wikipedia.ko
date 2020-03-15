> This article is converted from Wikipedia: [P \(\)](https://ko.wikipedia.org/wiki/P_\(\)).


**P**(**PTIME** 또는 **[DTIME](https://ko.wikipedia.org/wiki/DTIME "wikilink")**(*n*<sup>O(1)</sup>))는 [결정론적 튜링 기계로](https://ko.wikipedia.org/wiki/결정론적_튜링_기계 "wikilink") [다항 시간](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 안에 풀 수 있는 [판정 문제를](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") 모아 놓은 [복잡도 종류이다](../Page/복잡도_종류.md "wikilink"). [선형 계획](https://ko.wikipedia.org/wiki/선형_계획법 "wikilink") 제품, [최대공약수](../Page/최대공약수.md "wikilink") 문제 등이 P에 포함되며, [2002년](../Page/2002년.md "wikilink")에는 주어진 숫자가 [소수인지](../Page/소수_\(수론\).md "wikilink") 판별하는 문제도 P에 속한다는 것이 증명되었다\[1\]

보통 P는 효율적으로 다룰 수 있는 문제의 집합으로 생각되지만, [RP나](https://ko.wikipedia.org/wiki/RP_\(복잡090ㅣ0도\) "wikilink") [BPP](https://ko.wikipedia.org/wiki/BPP "wikilink")와 같은 더 큰 집합의 문제도 효율적으로 다룰 수 있다. 또한 P에 속한다고 해서 항상 실용적인 것은 아닌데, 이론적으로는 다항 시간 내에 풀 수 있지만 실제 걸리는 시간이 비효율적일 가능성도 충분히 있기 때문이다.

## 다른 복잡도 종류와의 관계

[NP는](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") [비결정론적 튜링 기계로](https://ko.wikipedia.org/wiki/비결정론적_튜링_기계 "wikilink") 다항 시간 안에 풀 수 있는 판정 문제들의 집합으로, 이 문제들은 결정론적 튜링 기계로 다항 시간 안에 답을 검증 가능할 수 있다. P는 NP의 부분집합이지만, P와 NP가 같은지 아닌지는 아직 알려지지 않았다. 이에 대한 문제는 [P-NP 문제라고](../Page/P-NP_문제.md "wikilink") 부른다.

[L는](https://ko.wikipedia.org/wiki/L_\(복잡도\) "wikilink") 결정론적 튜링 기계로 [로그](https://ko.wikipedia.org/wiki/로그함수 "wikilink") [메모리 공간을](https://ko.wikipedia.org/wiki/메모리_공간 "wikilink") 사용하여 풀 수 있는 판정 문제들의 집합으로, 이 집합은 P의 부분집합으로 알려져 있지만 P와 L이 같은지 아닌지는 아직 미해결 상태이다.

[ALOGSPACE](https://ko.wikipedia.org/wiki/ALOGSPACE "wikilink")는 [교대 튜링 기계가](../Page/교대_튜링_기계.md "wikilink") 메모리를 로그만큼 써서 풀 수 있는 문제들의 집합으로, P=ALOGSPACE라는 것은 증명되어 있다. 또한 [PSPACE](../Page/PSPACE.md "wikilink")는 다항 공간을 사용하여 풀 수 있는 판정 문제의 집합으로, P는 PSPACE의 부분집합이지만 이 두 집합이 같은지에 대해서는 아직 미해결 상태이다. L이 PSPACE의 진부분집합이라는 것은 증명되어 있다.

[EXPTIME](../Page/EXPTIME.md "wikilink")은 [지수](https://ko.wikipedia.org/wiki/지수함수 "wikilink") 시간 안에 풀 수 있는 판정 문제들의 집합으로, P는 EXPTIME의 [진부분집합](https://ko.wikipedia.org/wiki/진부분집합 "wikilink")이라는 것이 증명되어 있다. 또한 모든 EXPTIME-난해 문제는 P에 속하지 않는다.

이를 수식으로 표기하면 다음과 같다.

\[\mbox{L} \subseteq \mbox{ALOGSPACE} = \mbox{P} \subseteq \mbox{NP} \subseteq \mbox{PSPACE} \subseteq \mbox{EXPTIME}\] 또한 위 관계에서 P가 EXPTIME과 같지 않기 때문에, \(\mbox{P} \subseteq \mbox{NP}\), \(\mbox{NP} \subseteq \mbox{PSPACE}\), \(\mbox{PSPACE} \subseteq \mbox{EXPTIME}\) 중 최소한 하나는 진부분집합 관계여야 한다.

P에 속한 가장 어려운 문제는 [P-완전](../Page/P-완전.md "wikilink") 문제이다.

P를 일반화한 것에는 P/poly도 있다. **P/poly**는 **비균일 다항시간**(非均一 多項時間, )이라고도 한다. P/poly에 속한 문제는 입력의 길이에 의존하는 조언 문자열이 주어지면 결정론적 다항시간에 풀 수 있다. 그러나 NP와 달리 다항시간기계가 검증기계가 아니므로 거짓 조언 문자열인지 찾아낼 필요는 없다. P/poly는 거의 모든 효율적인 알고리즘을 포함하는 큰 집합이다. 모든 [BPP](https://ko.wikipedia.org/wiki/BPP "wikilink")도 P/poly에 포함된다. 만약 NP도 P/poly에 포함되면, [다항 위계](https://ko.wikipedia.org/wiki/다항_위계 "wikilink") 전체가 오직 두 단계로 줄어든다. 반면에, 모든 판정불가능 문제들의 단항 버전 같은 일부 [판정불가능](https://ko.wikipedia.org/wiki/판정불가능성 "wikilink") 문제도 P/poly에 포함된다.

P에 대응하는 [함수 문제](https://ko.wikipedia.org/wiki/함수_문제 "wikilink") 복잡도 종류에는 [FP가](https://ko.wikipedia.org/wiki/FP_\(복잡도\) "wikilink") 있다.

## 성질

다항시간 알고리즘은 합성()에 대해 닫혀 있다. 직관적으로 설명하면, 다항시간 안에 실행되는 함수를 만들어서 이 함수를 상수번 만큼 불러서 사용하고, 함수를 불러서 사용하는 알고리즘도 다항시간의 시간이 걸리면 전체 실행시간은 여전히 다항시간이다. 이런 이유로 **P**는 자기 자신에 대해서 [낮다](https://ko.wikipedia.org/wiki/낮음_\(복잡도\) "wikilink"). 이런 이유로 **P**는 어떤 기계에서 정의되든지 같은 계산 능력을 가진다. 예를 들어서 [임의 접근이](https://ko.wikipedia.org/wiki/임의_접근 "wikilink") 가능한 특정한 기계는 메모리에 접근하는 다항시간 과정을 메모리에 순서대로 접근하는 다항시간으로 흉내낼 수 있기 때문에 순차접근 기계를 합성하여 임의 접근 기계를 만들 수 있다.

## 참고문헌

<references />

  - C. Papadimitriou. Computational Complexity. Addison-Wesley, 1994. .

  - Complexity Zoo: [P](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#p), [P/poly](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#pslashpoly)

  - Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest, and Clifford Stein. *[Introduction to Algorithms](../Page/Introduction_to_Algorithms.md "wikilink")*, Second Edition. MIT Press and McGraw-Hill, 2001. . Section 34.1: Polynomial time, pp.971–979.

  - Michael Sipser, *Introduction to the Theory of Computation*, PWS Publishing, . Section 7.2: The Class P, pp.234 – 241.

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")

1.  4