> This article is converted from Wikipedia: [BQP](https://ko.wikipedia.org/wiki/BQP).


**BQP**는 [계산 복잡도 이론](https://ko.wikipedia.org/wiki/계산_복잡도_이론 "wikilink") 용어로 '유계오차 양자 다항시간'(有界誤差 量子 多項時間, **B**ounded error, **Q**uantum, **P**olynomial time)의 약자이다. BQP는 모든 풀이에 대해 최대 1/4의 확률로 잘못된 결과를 내놓으면서 [양자 컴퓨터가](../Page/양자_컴퓨터.md "wikilink") 다항시간 안에 풀 수 있는 문제의 집합이다. 양자컴퓨터에서 다항시간의 실행시간을 가지는 [알고리즘](../Page/알고리즘.md "wikilink")의 집합으로 생각할 수 있다. 1/4이라는 확률로 잘못된다는 것은 '예'라는 답을 잘못 내놓는 경우와 '아니오'라는 답을 잘못 내놓는 경우 모두를 포함한 것이다.

BQP에서 확률을 1/4로 제한하는 데 특별한 의미가 있는 것은 아니다. 이 상수를 0 \< <var>k</var> \< 1/2 인 임의의 [실수](https://ko.wikipedia.org/wiki/실수 "wikilink") <var>k</var>로 바꾸어도 BQP [집합](../Page/집합.md "wikilink")이 변하는 것은 아니다. 어느 정도 잘못된 결과가 나올 확률이 있어도, 알고리즘을 여러 번 시행하면 잘못된 결과가 많이 나올 확률이 기하급수적으로 감소하기 때문이다.

컴퓨터의 [큐비트](../Page/큐비트.md "wikilink") 수는 보통 입력값의 크기에 대한 함수 값을 가진다. 예를 들어, 2*n*개의 큐비트로 *n*비트 정수를 [소인수 분해하는](https://ko.wikipedia.org/wiki/소인수_분해 "wikilink") [알고리즘](../Page/알고리즘.md "wikilink")이 알려져 있다.

실용적으로 널리 사용되는 문제의 일부가 [P에는](https://ko.wikipedia.org/wiki/P_\(복잡도\) "wikilink") 속하지 않을 것 같지만 BQP에 속한다는 것이 알려지면서, 최근 양자컴퓨터에 대해 관심이 높아지고 있다. P에는 속하지 않을 것 같지만 BQP에 속하는 문제 중 현재까지 알려진 것은 다음 세 가지밖에 없다.

  - [소인수 분해](https://ko.wikipedia.org/wiki/소인수_분해 "wikilink") ([쇼어 알고리즘](https://ko.wikipedia.org/wiki/쇼어_알고리즘 "wikilink") 참고)
  - [이산 대수](https://ko.wikipedia.org/wiki/이산_대수 "wikilink")
  - 양자체계의 시뮬레이션 ([범용 양자컴퓨터](https://ko.wikipedia.org/wiki/범용_양자컴퓨터 "wikilink") 참고)

BQP는 양자 컴퓨터를 위해 정의된 복잡도 종류이다. 일반적인 [튜링 기계에서](../Page/튜링_기계.md "wikilink") 확률적으로 시행되는 알고리즘의 집합은 **[BPP](https://ko.wikipedia.org/wiki/BPP "wikilink")**이다.

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink") [분류:양자정보과학](https://ko.wikipedia.org/wiki/분류:양자정보과학 "wikilink") [분류:양자 컴퓨터](https://ko.wikipedia.org/wiki/분류:양자_컴퓨터 "wikilink")