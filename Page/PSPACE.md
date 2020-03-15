> This article is converted from Wikipedia: [PSPACE](https://ko.wikipedia.org/wiki/PSPACE).


[계산 복잡도 이론에서](https://ko.wikipedia.org/wiki/계산_복잡도_이론 "wikilink") **PSPACE**는 [결정론적 튜링 기계나](https://ko.wikipedia.org/wiki/결정론적_튜링_기계 "wikilink") [비결정론적 튜링 기계가](https://ko.wikipedia.org/wiki/비결정론적_튜링_기계 "wikilink") 시간은 얼마든지 쓸 수 있고, 공간은 다항 공간만 써서 풀 수 있는 [판정 문제들의](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") 집합이다. [사비치 정리에](https://ko.wikipedia.org/wiki/사비치_정리 "wikilink") 따르면 PSPACE는 **NSPACE**와 같기 때문에 튜링 기계가 결정론적이든 비결정론적이든 상관 없다.

[문맥-민감 언어가](https://ko.wikipedia.org/wiki/문맥-민감_언어 "wikilink") **PSPACE**의 진부분집합이다. 복잡도 종류 **[NL](https://ko.wikipedia.org/wiki/NL_\(복잡도\) "wikilink")**, **[P](https://ko.wikipedia.org/wiki/P_\(복잡도\) "wikilink")**, **[NP](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink")**, **PSPACE**, **[EXPSPACE](https://ko.wikipedia.org/wiki/EXPSPACE "wikilink")**가 갖는 관계는 이렇다:

\[\mathsf{NL} \subseteq \mathsf{P} \subseteq \mathsf{NP} \subseteq \mathsf{PSPACE}\]

\[\mathsf{NL} \subsetneq \mathsf{PSPACE} \subsetneq \mathsf{EXPSPACE}\]

첫째 줄에 \(\subseteq\) ([부분집합](https://ko.wikipedia.org/wiki/부분집합 "wikilink")) 기호가 세 개 있다. 셋 중 하나는 \(\subsetneq\)여야 하는데, 정확히 어느 것이 그런지는 알려진 바 없다. 수많은 사람들이 셋 모두 \(\subsetneq\)라고 추측하고 있다. **[P-NP 문제](https://ko.wikipedia.org/wiki/P-NP_문제 "wikilink")**(두 번째 \(\subseteq\)가 \(\subsetneq\)인지 아닌지 묻는 문제)에 대한 해법에는 [상금 백만 달러가](https://ko.wikipedia.org/wiki/클레이_수학연구소 "wikilink") 걸려 있다.

**PSPACE**에서 가장 어려운 문제들을 **PSPACE-완전**이라고 한다. **PSPACE**이고 **NP**는 아닐 것으로 예상되는 문제들을 알고 싶으면 **[PSPACE-완전](https://ko.wikipedia.org/wiki/PSPACE-완전 "wikilink")**을 보라.

## 다른 정의

**PSPACE**를 [교대 튜링 기계가](https://ko.wikipedia.org/wiki/교대_튜링_기계 "wikilink") 다항 시간에 판정할 수 있는 문제의 집합으로 정의하기도 한다. **APTIME** 아니면 그냥 **AP**라고도 한다.

논리학에 바탕을 둔 정의는, [이차 논리에](https://ko.wikipedia.org/wiki/이차_논리 "wikilink") [추이 닫힘](https://ko.wikipedia.org/wiki/추이_닫힘 "wikilink") 연산을 더해서 표현할 수 있는 문제의 집합을 **PSPACE**라고 한다. 완전한 추이 닫힘일 필요는 없다. 가환 추이 폐포나 더 약간 형태도 충분하다. 이 연산자를 추가함으로써 **PSPACE**와 **[PH](../Page/PH_\(복잡도\).md "wikilink")**를 구분할 수 있(을지도 모르)게 된다.

복잡도 이론의 중요한 결과 중 하나는, **PSPACE**를 특정 [대화형 증명 체계가](https://ko.wikipedia.org/wiki/대화형_증명_체계 "wikilink") 받아들일 수 있는 모든 언어로 특징지을 수 있다는 것이다. 이는 **[IP](https://ko.wikipedia.org/wiki/IP_\(복잡도\) "wikilink")**를 정의하는 특징이기도 하다. 이 체계에는 확률적 다항 시간 검증자가 주어진 언어에 어떤 문자열이 들어간다고 확신하게 하는 전능한 증명자가 있다. 문자열이 그 언어에 들어간다면, 검증자를 높은 확률로 확신시킬 수 있어야 한다. 그러나 들어가지 않는다면 낮은 확률로 예외가 생기는 경우를 빼고는 확신시킬 수 없어야 한다.

## 참고 문헌

  - [복잡도 동물원 PSPACE 우리](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#pspace)

  -
  -
[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")