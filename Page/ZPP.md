> This article is converted from Wikipedia: [ZPP](https://ko.wikipedia.org/wiki/ZPP).


[계산 복잡도 이론에서](https://ko.wikipedia.org/wiki/계산_복잡도_이론 "wikilink") [복잡도 종류](https://ko.wikipedia.org/wiki/복잡도_종류 "wikilink") **ZPP**(오차 없는 확률적 다항시간, **Z**ero-error **P**robabilistic **P**olynomial time)는 다음과 같은 성질을 지니는 [확률적 튜링 기계가](https://ko.wikipedia.org/wiki/확률적_튜링_기계 "wikilink") 존재하는 문제로 이루어진 집합이다.

  - 항상 올바른 '예' 또는 '아니오' 답을 내놓는다.
  - 최대 실행시간은 정해져 있지 않으나, 어떠한 입력에 대해서도 평균 다항 시간에 실행한다.

이는 문제 크기가 *n*이면 평균 실행 시간이 *p*(*n*)보다 작게 되는 다항식 *p*(*n*)이 존재한다는 뜻도 된다. (평균 실행 시간이 그렇다는 것이고, 각 실행은 훨씬 오래 걸릴 수 있다.)

**ZPP**에 속한 알고리즘은 항상 올바른 답을 내놓는다. (이러한 알고리즘을 [라스베이거스 알고리즘이라고](https://ko.wikipedia.org/wiki/라스베이거스_알고리즘 "wikilink") 한다.)

다른 식으로 정의할 수도 있다. **ZPP**란 다음과 같은 성질을 지니는 확률적 튜링 기계가 존재하는 문제의 복잡도 종류이다.

  - 항상 다항 시간에 실행을 마친다.
  - '예', '아니오', '알 수 없음' 중 하나를 답으로 내놓는다.
  - 답은 '알 수 없음'이거나 정답이어야 한다.
  - 정답이 '예'라면 1/2 확률로 '예'를 답으로 내놓는다.
  - 정답이 '아니오'라면 1/2 확률로 '아니오'를 답으로 내놓는다.

이 정의는 앞에서 제시한 정의와 동등하다.

**ZPP**의 정의는 확률적 튜링 기계에 바탕을 둔다. **[BPP](https://ko.wikipedia.org/wiki/BPP "wikilink")**나 **[RP](https://ko.wikipedia.org/wiki/RP_\(복잡도\) "wikilink")**도 바탕을 같이한다. 그러나 **[BQP](https://ko.wikipedia.org/wiki/BQP "wikilink")** 같은 복잡도 종류는 다른 종류의 확률적 기계인 [양자 컴퓨터에](https://ko.wikipedia.org/wiki/양자_컴퓨터 "wikilink") 바탕을 두고 있다.

## 교집합으로 한 정의

**ZPP**는 **[RP](https://ko.wikipedia.org/wiki/RP_\(복잡도\) "wikilink")**와 **co-RP**의 교집합과 정확히 일치한다. 이것을 **ZPP**의 정의로 삼기도 한다. 이것을 보이기 위해서는 먼저, **RP**와 **co-RP**에 둘 다 속하는 문제라면 모두 아래 설명한 [라스베이거스 알고리즘이](https://ko.wikipedia.org/wiki/라스베이거스_알고리즘 "wikilink") 존재한다는 점을 언급할 필요가 있다.

1.  **RP** 알고리즘 A와 **co-RP** 알고리즘 B를 받아들이는 언어 L이 존재한다고 하자. (A와 B는 완전히 다른 알고리즘일 수도 있다.)
2.  L에 입력이 하나 들어오면 먼저 A 알고리즘을 실행한다. 결과가 '예'라면 답도 반드시 '예'이다.
3.  A 알고리즘의 결과가 '예'가 아니면 같은 입력에 대해 B 알고리즘을 실행한다. 결과가 '아니오'이면 답은 반드시 '아니오'이다.
4.  B 알고리즘의 결과가 '아니오'가 아니면 A 알고리즘을 실행하는 단계로 돌아간다.

두 기계 중 하나만 틀린 답을 내 놓을 수 있고, 한 반복에서 틀린 답이 나올 확률은 50%이다. 이것은 **k**번째 반복까지 갈 확률이 **k**에 대해 지수적으로 줄어듦을 뜻하고, 실행 시간의 [기댓값](https://ko.wikipedia.org/wiki/기댓값 "wikilink")은 다항 시간이 된다. 그러므로 **RP**와 **co-RP**의 교집합은 **ZPP**에 포함된다.

반대 방향으로 **ZPP**가 **RP**와 **co-RP**의 교집합에 포함됨을 보이기 위해서, ZPP에 속하는 라스베이거스 알고리즘 C가 있다고 가정하자. 그러면 다음과 같은 **RP** 알고리즘을 만들 수 있다.

  - C를 적어도 평균 실행 시간의 두 배만큼 실행한다. 만약 답이 나오면, 그것을 답으로 내놓는다. 나오지 않으면 '아니오'를 답으로 낸다.

[마르코프 부등식에](https://ko.wikipedia.org/wiki/마르코프_부등식 "wikilink") 따르면 이 알고리즘이 멈출 때까지 C가 답을 못 낼 확률은 1/2 이하이다. 이것은 답이 '예'인 입력이 왔을 때, 실행을 멈추고 '아니오'라는 틀린 답을 낼 확률이 1/2을 넘지 않는다는 뜻이다. 이는 **RP**의 정의에 딱 맞는다. C가 답을 내지 못했을 때 '예'를 출력하는 것으로 바꾸면, ZPP가 **co-RP**에 속한다는 것도 같은 식으로 증명할 수 있다.

## 관련 복잡도 종류

**ZPP**=**RP** ∩ **co-RP**이기 때문에 **ZPP**는 **RP**와 **co-RP** 둘 다에 속한다.

**[P](https://ko.wikipedia.org/wiki/P_\(복잡도\) "wikilink")**는 **ZPP**에 속하고, 몇몇 컴퓨터 과학자는 **P**=**ZPP**일 것으로 추측한다. 즉, 모든 [라스베이거스 알고리즘에는](https://ko.wikipedia.org/wiki/라스베이거스_알고리즘 "wikilink") 동등한 결정론적 다항 시간 알고리즘이 존재한다는 것이다.

**ZPP** = **[EXPTIME](https://ko.wikipedia.org/wiki/EXPTIME "wikilink")**인지는 아직 밝혀지지 않았다. (같을 가능성은 거의 없어 보인다.) **P** ≠ **EXPTIME**이므로 **P**=**ZPP**임이 밝혀지면 **ZPP** ≠ **[EXPTIME](https://ko.wikipedia.org/wiki/EXPTIME "wikilink")**임이 증명된다.

## 외부 링크

  - [ZPP](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#zpp) - 복잡도 동물원의 ZPP 우리

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")