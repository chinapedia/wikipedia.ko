> This article is converted from Wikipedia: [PCP \(\)](https://ko.wikipedia.org/wiki/PCP_\(\)).


**PCP**는 확률적으로 검사할 수 있는 증명()을 할 수 있는 [판정 문제들의](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") [복잡도 종류이다](https://ko.wikipedia.org/wiki/복잡도_종류 "wikilink").

## 정의

복잡도 이론에서 **PCP** 체계는 [대화형 증명 체계로](https://ko.wikipedia.org/wiki/대화형_증명_체계 "wikilink") 볼 수 있다. 여기에서 증명자()는 무기억 신탁(, 주로 문자열)이고 검증자()는 다항 시간 [확률적 알고리즘이다](https://ko.wikipedia.org/wiki/확률적_알고리즘 "wikilink"). 언어에 속하는 입력('예'인 보기)에 대해서는 검증자가 확실성()을 갖고 받아들이는 신탁(즉, 증명)이 있다. '아니오'인 보기에 대해서는 신탁이 무엇이든 검증자가 적어도 1/2 확률로 거부한다. (이 설명을 **[co-RP](https://ko.wikipedia.org/wiki/RP_\(복잡도\) "wikilink")** 쪽과 비교해 보라.)

**PCP**란 **[NP](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink")**를 강화한 것이라고 보는 관점도 있다. **NP**에 들어 있는 언어는 증명을 검증하는 데 걸리는 시간이 적어도 증명 자체만큼 길다. **PCP**에 들어 있는 문제들은 꼭 그럴 필요는 없다. 다시 말해서, **PCP**문제에 대한 증명은 **NP**문제에 대한 것보다 훨씬 길 수도 있다.

앞에서 살펴본 바와 같이, 검증자가 만들 수 있는 신탁 질의의 수에는 제한을 두지 않는다. **PCP** 체계의 능력에 영향을 줄 수 있는 다른 요소는 검증자가 만들 수 있는 난수 개수이다. 임의성을 높게 할수록 검증자가 증명을 확인하기 위해 해 볼 수 있는 것도 다양해진다. 따라서 **PCP**는 단순히 복잡도 종류 중 하나를 넘어, 다른 복잡도 종류를 분류하는 데에도 쓰인다.(이 개념을 메타-종류라는 용어로 나타낼 수 있다.) **PCP**는 함수 두 개로 복잡도 종류를 분류한다.

## 예

**PCP** 알고리즘은 대부분 정확하게 설명하기 어렵지만, [3-CNF-SAT](https://ko.wikipedia.org/wiki/3-CNF-SAT "wikilink")을 푸는 알고리즘에 대한 간단한 발상이 있다. 3-CNF-SAT은 [충족 가능성 문제](https://ko.wikipedia.org/wiki/충족_가능성_문제 "wikilink") 중 [논리곱 정규형에서](https://ko.wikipedia.org/wiki/논리곱_정규형 "wikilink") 각 절에 리터럴이 세 개씩 있는 경우이다.

변수 *m*개와 절 *n*개로 된 식 *F*가 있다고 하자. 증명자한테 변수 *m*개 모두를 만족하는 값을 할당해 보라고 한다. 모든 *m*을 살펴 보는 대신 임의의 O(log *n*) 비트를 써서 절을 임의로 뽑는다. 그러고 나서 이 절이 쓰는 변수를 살펴 보고, 그 값을 신탁 질의 세 개만으로 알아낸다. 알아낸 값을 넣었을 때 절이 만족되면 검증자가 그 절을 선택한 것이므로, 1/*n* 확률로 할당이 만족되는 것을 믿을 수 있다. 알고리즘을 *n*번 반복하면 O(*n* log *n*) 난수 비트와 3*n* 신탁 질의만으로 상수 오차 한계를 얻을 수 있다. 이것을 **NP-완전** 문제로 보면 모든 **NP** 문제는 **PCP**(*n* log *n*, *n*)에 들어간다.

## 결과

간단하고도 특별한 예 (*다항*은 다항 양, *log*는 로그 양을 나타낸다.)

  - PCP(0, 0) =[P](https://ko.wikipedia.org/wiki/P_\(복잡도\) "wikilink")
  - PCP(다항, 0) = [co-RP](https://ko.wikipedia.org/wiki/RP_\(복잡도\) "wikilink")
  - PCP(0, 다항) = [NP](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink")

주목할 만한 사실:

  - PCP(다항, 다항) = [NEXP](https://ko.wikipedia.org/wiki/NEXPTIME "wikilink")
  - NP = PCP(o(log), o(log))이면 NP = P
  - NP = PCP(log, 다항)

복잡도 이론이 거둔 큰 성과로 [PCP 정리가](https://ko.wikipedia.org/wiki/PCP_정리 "wikilink") 있다.

  -
    **NP** = **PCP**(log, O(1)).

이것은 [근사 알고리즘이](https://ko.wikipedia.org/wiki/근사_알고리즘 "wikilink") 얼마나 어려운지를 증명할 때 쓸 만하다.

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")