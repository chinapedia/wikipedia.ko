> This article is converted from Wikipedia: [P-NP 문제](https://ko.wikipedia.org/wiki/P-NP_문제).


[섬네일](https://ko.wikipedia.org/wiki/파일:Complexity_classes.png "wikilink")

**P-NP 문제**는 [복잡도 종류](../Page/복잡도_종류.md "wikilink") [P와](../Page/P_\(복잡도\).md "wikilink") [NP가](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") 같은지에 대한 [컴퓨터 과학의](../Page/컴퓨터_과학.md "wikilink") 미해결 문제로 컴퓨터로 풀이법이 빠르게 확인된 문제가 컴퓨터로 빠르게 풀리기도 할 것인가 아닌가를 묻고 있다. [1971년](../Page/1971년.md "wikilink") [스티븐 쿡이](../Page/스티븐_쿡.md "wikilink") 그의 논문 〈The Complexity of Theorem Proving Procedures〉(정리 증명 절차의 복잡성)에서 처음으로 제안하였고 [클레이 수학연구소에서](../Page/클레이_수학연구소.md "wikilink") 발표한 7개의 '밀레니엄 문제' 중 하나이며 컴퓨터 과학에서 중요한 위치를 차지하고 있다. 이것은 본래 1956년 [쿠르트 괴델이](../Page/쿠르트_괴델.md "wikilink") [존 폰 노이만에게](../Page/존_폰_노이만.md "wikilink") 썼던 편지에서 처음으로 언급되었다. 괴델은 어떤 NP 완전 문제가 2차 혹은 선형 시간 안에 풀릴 수 있는지 아닌지를 물었다.

P는 [결정론적 튜링 기계를](https://ko.wikipedia.org/wiki/결정론적_튜링_기계 "wikilink") 사용해 [다항 시간](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 내에 답을 구할 수 있는 문제의 집합이고, NP는 [비결정론적 튜링 기계를](../Page/비결정론적_튜링_기계.md "wikilink") 사용해 다항 시간 내에 답을 구할 수 있는 문제의 집합이다. 여기에서 결정론적 튜링 기계에 사용한 프로그램을 비결정론적 튜링 기계에 적용할 수 있으므로, P는 NP의 부분집합이 된다. 하지만 여기에서 P와 NP가 같은 집합인지, 아니면 P가 NP의 [진부분집합](https://ko.wikipedia.org/wiki/진부분집합 "wikilink")인지는 아직 밝혀지지 않았다. 현재 2000년에 클레이 수학연구소가 100만 달러를 걸었다.

​위에 사용된 일상적인 단어인 "빠르게"​는 [다항 시간안에](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 실행되는 작업을 위한 알고리즘의 존재를 의미한다. 다항시간 안에 답을 제공하는 알고리즘이 있는 문제들의 일반 류 general class(종합적인 모임)를 P류 혹은 [P라고](../Page/P_\(복잡도\).md "wikilink") 한다. 어떤 문제들은 빠르게 답을 찾을 수 있는 방법이 알려져 있지 않지만 답이 무엇인지를 나타내는 정보가 제공된다면 답을 빠르게 확인하는 것이 가능하다. 다항 시간 안에 확인할 수 있는 문제류를 [NP라고](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink") 한다.

​쉽게 풀이법이 확인될 수 있는 문제이지만 답을 계산하기는 어려울 수 있는 문제의 한 예인 [부분집합 합 문제를](https://ko.wikipedia.org/wiki/부분집합_합_문제 "wikilink") 예를 들어보면 다음과 같다. 어떤 정수의 집합이 주어졌을 때 공집합이 아닌 부분집합중 적어도 하나 이상의 부분집합의 합계가 0일 수 있는지, 예를 들면 {−2, −3, 15, 14, 7, −10}의 부분집합 중 어떤 것은 합계가 0일지 생각해보면 답은 그렇다 이다. 왜냐하면 부분집합 {−2, −3, −10, 15}의 합계가 0 이기 때문인데, 이것은 3회의 덧셈으로 빠르게 풀린다. 그런데도 그런 부분집합을 다항시간 안에 찾아내는 알고리즘은 알려져 있지 않다. 그런데 만약 P = NP​라면 [시간 복잡도](../Page/시간_복잡도.md "wikilink")(2<sup>*n*</sup>-n-1 회)안에 풀리는 이 문제를 다항시간에 풀 수 있는 알고리즘이 존재할 것이다. 이런 이유로 이 문제는 빠르게 확인가능한 NP안에 있지만 반드시 빠르게 풀 수 있는 P​안에 있지는 않다.

​P = NP​문제의 답은, 부분집합의 합계 문제와 같이 지수시간 안에 답을 계산할 수 있는 문제들이 다항시간안에도 답을 계산할 수 있는지를 결정할 것이다. 만약 P ≠ NP​인 것으로 드러난다면, NP안에는 풀이법을 확인하는 것보다 답을 계산하는 게 더 어려운 문제들이 있다는 것을 의미할 것이다. : 그것들은 다항시간 안에 풀 수 없지만 다항시간 안에 풀이법을 찾을 수는 있다.

컴퓨터 과학에서 이 문제의 중요성을 차치하더라도, 이 문제의 증명은 수학, 암호, 알고리즘 연구, 인공지능, 게임이론, 멀티미디어 프로세싱, 철학, 경제학등 다양한 분야에 엄청난 영향을 끼칠 것이다.

## 예상

2002년에 이론전산학자 100명을 대상으로 한 설문조사에서, 61명이 P와 NP가 다를 것이라고 답했고 29명은 같을 것이라고 답했다.\[1\] 10년이 지난 2012년에 150명을 대상으로 한 설문조사에서는 다를 것이라고 답하는 비율이 81퍼센트로 늘어났다.\[2\]

## NP-난해

어떤 문제가 주어졌을때, 다른 NP문제의 입력을 그 문제의 입력으로 변환할 수 있는 환산 알고리즘이 존재하고 이 환산 알고리즘은 수행시간이 무시될 수 있을 정도로 빠르다면 이 문제는 [NP-난해](../Page/NP-난해.md "wikilink")문제에 속한다. 이 집합이 중요한 이유는, NP-난해에 속하는 문제 중 하나라도 P에 속한다는 것을 밝힌다면 P=NP를 증명할 수 있기 때문이다.

## NP-완전

NP난해문제이면서 NP문제인 문제는 [NP-완전](../Page/NP-완전.md "wikilink")문제에 속한다.

## 참고 사항

  - [2003년](../Page/2003년.md "wikilink") [12월 23일](../Page/12월_24일.md "wikilink"), [전북대학교](https://ko.wikipedia.org/wiki/전북대학교 "wikilink") [김양곤](../Page/김양곤.md "wikilink") 교수는 [리 대수를](../Page/리_대수.md "wikilink") 이용하여 P≠NP 임을 증명하여 P-NP 문제를 해결하였다고 주장했다. 선택함수를 써서 다항식시간이내 아닌 무한시간 걸려야 풀리는 NP문제를 제시하였다고 주장하였다. 학계나 CMI 연구소에 검증을 요청하지는 않았기 때문에 학계에서는 인정하지 않고 있다.

## 같이 보기

  - [수학의 미해결 문제](https://ko.wikipedia.org/wiki/수학의_미해결_문제 "wikilink")
  - [컴퓨터 과학의 미해결 문제](https://ko.wikipedia.org/wiki/컴퓨터_과학의_미해결_문제 "wikilink")
  - [게임 복잡도](https://ko.wikipedia.org/wiki/게임_복잡도 "wikilink")

## 각주

<references />

[분류:밀레니엄 문제](https://ko.wikipedia.org/wiki/분류:밀레니엄_문제 "wikilink") [분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink") [분류:수학의 미해결 문제](https://ko.wikipedia.org/wiki/분류:수학의_미해결_문제 "wikilink") [분류:컴퓨터 과학의 미해결 문제](https://ko.wikipedia.org/wiki/분류:컴퓨터_과학의_미해결_문제 "wikilink") [분류:추측](https://ko.wikipedia.org/wiki/분류:추측 "wikilink")

1.  <http://www.cs.umd.edu/~gasarch/papers/poll.pdf>
2.  <http://www.newscientist.com/article/dn21578-poll-consensus-on-milliondollar-logic-problem.html>