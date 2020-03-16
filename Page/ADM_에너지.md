> This article is converted from Wikipedia: [ADM ](https://ko.wikipedia.org/wiki/ADM_).


**ADM 질량**() 또는 **ADM 에너지**()는 [ADM 형식에서](../Page/ADM_형식.md "wikilink") 자연스럽게 등장하는 일종의 [해밀토니언](https://ko.wikipedia.org/wiki/해밀토니언 "wikilink")의 값이다.\[1\]\[2\]

## 정의

\(\mathbb R^4\) 위의, 로런츠 부호수의 계량 \(g_{\mu\nu}\)가 주어졌다고 하고, 또한 [계량 텐서가](https://ko.wikipedia.org/wiki/계량_텐서 "wikilink") 공간의 무한에서 [점근적으로 평탄하다고](../Page/점근적_평탄_다양체.md "wikilink") 가정하자.

이에 따라,

\[g_{\mu\nu}=\eta_{\mu\nu}+h_{\mu\nu}\] 를 정의하자. 그렇다면, 그 **ADM 질량**은 다음과 같다.\[3\]\[4\]\[5\]

\[M=\frac1{16\pi G}\lim_{r\to\infty}\oint_r(\delta^{ij}\partial_ih_{jk}-\delta^{ij}\partial_kh_{ij})\hat n^k\;\sqrt{\gamma^{(2)}}\mathrm dx^2\] 여기서

  - \(\textstyle\oint_r\)은 원점에서 반지름이 \(r\)인 구면에 대하여 계산되는 적분이다.
  - \(\hat n^k\)는 구면에 대한 수직 단위 벡터이다.
  - \(\textstyle\sqrt{\gamma^{(2)}}\;\mathrm dx^2\)는 구면의 넓이 원소이다.
  - 계수 \(1/(16\pi)\)는 [슈바르츠실트 계량의](../Page/슈바르츠실트_계량.md "wikilink") 질량과 비교하여 고정된 것이다.

마찬가지로, **ADM 운동량**(ADM運動量, )을 정의할 수 있으며, 다음과 같다.\[6\]

\[P^i=-\frac1{8\pi G}\lim_{r\to\infty}\oint_r\delta_{jk}\pi^{ij}\hat n^k\;\sqrt{\gamma^{(2)}}\mathrm dx^2\]

고차원 시공간에서도 마찬가지 정의가 가능하다.

## 성질

ADM [에너지-운동량](https://ko.wikipedia.org/wiki/에너지-운동량 "wikilink") \(P^\mu\)는 점근적 [로런츠 변환에](../Page/로런츠_변환.md "wikilink") 대하여 [4차원 벡터로](https://ko.wikipedia.org/wiki/4차원_벡터 "wikilink") 변환한다.\[7\]\[8\]

### 존재 조건

만약 계량이 공간의 무한에서 점근적으로 평탄하지 않다면 (예를 들어, [우주 상수가](https://ko.wikipedia.org/wiki/우주_상수 "wikilink") 존재한다면), 위 적분들은 수렴하지 않을 수 있다.

구체적으로, \(D>2\)차원 [리만 다양체](../Page/리만_다양체.md "wikilink") \((\Sigma,g)\)가 주어졌으며, \(\Sigma\)는 [유클리드 공간의](../Page/유클리드_공간.md "wikilink") [부분 집합](https://ko.wikipedia.org/wiki/부분_집합 "wikilink")

\[\mathbb R^D\setminus\operatorname{ball}(0,1;\mathbb R^D)\] 와 [미분 동형이라고](https://ko.wikipedia.org/wiki/미분_동형 "wikilink") 하자 (\(\operatorname{ball}(0,1;\mathbb R^D)\)는 \(\mathbb R^D\) 속의 단위 [초구](../Page/초구.md "wikilink")). 즉, 이 경우 위 [미분 동형 사상에](https://ko.wikipedia.org/wiki/미분_동형_사상 "wikilink") 의하여 좌표계 \((x^i)_{i=1,\dots,D}\) 및 함수 \(r=\sqrt{\delta_{ij}x^ix^j}\)를 정의할 수 있다. \((\Sigma,g)\)의 ADM 질량이 유한하게 존재할 [충분 조건은](https://ko.wikipedia.org/wiki/충분_조건 "wikilink"), 다음 부등식들을 만족시키는 상수 \(\alpha\)가 존재하는 것이다.\[9\]

\[|g_{ij}-\delta_{ij}|\in O\left(r^{-\alpha}\right)\qquad\forall i,j\in\{1,\dots,D\}\]

\[|\partial_k g_{ij}|\in O(r^{-\alpha-1})\qquad\forall i,j,k\in\{1,\dots,D\}\]

\[R\in\operatorname L^1(\Sigma;\mathbb R)\]

\[\alpha>\frac{D-2}2\] 여기서 \(\alpha\)는 인 임의의 상수이며, \(R\colon\Sigma\to\mathbb R\)는 [스칼라 곡률](https://ko.wikipedia.org/wiki/스칼라_곡률 "wikilink") 함수이며, \(\operatorname L^1(\Sigma;\mathbb R)\)는 \(\Sigma\) 위의 절댓값 적분 가능 실함수들의 집합(즉, [L<sup>*p*</sup> 공간의](https://ko.wikipedia.org/wiki/Lp_공간 "wikilink") 특수한 경우)이다.

### 양 에너지 정리

**양 에너지 정리**(陽energy定理, )에 따르면, 다음이 성립한다.\[10\]\[11\]

  - ① [우세 에너지 조건을](https://ko.wikipedia.org/wiki/우세_에너지_조건 "wikilink") 만족시키고, ② 점근적으로 평탄한 4차원 시공간의 ADM 에너지는 음이 아닌 실수이며,
  - ①과 ②를 만족시키며, ③ ADM 에너지가 0인 4차원 시공간은 [민코프스키 공간](../Page/민코프스키_공간.md "wikilink") 밖에 없다.

#### 리만-펜로즈 부등식

점근적으로 평탄한 3차원 [리만 다양체](../Page/리만_다양체.md "wikilink") \((\Sigma,\gamma)\)가 주어졌다고 하고, (시간 불변 시공간으로 간주하였을 때) 그 ADM 질량이 \(m\)이라고 하자. 또한, \(\Sigma\)의 [극소 곡면](https://ko.wikipedia.org/wiki/극소_곡면 "wikilink") 가운데 제일 바깥에 있는 것의 넓이가 \(A\)라고 하자. (이러한 [극소 곡면은](https://ko.wikipedia.org/wiki/극소_곡면 "wikilink") [연결 공간이](../Page/연결_공간.md "wikilink") 아닐 수 있다.) 그렇다면, **리만-펜로즈 부등식**(Riemann-Penrose不等式, )에 따르면, 다음이 성립한다.

\[Gm\ge\sqrt{A/16\pi}\] 이는 양 에너지 정리의 일반화이다.

## 역사

[thumb](https://ko.wikipedia.org/wiki/파일:ArnowittDeserMisner2009_01.jpg "wikilink") 리처드 루이스 아노윗(, 1928\~2014) · 스탠리 데세르(, 1931\~) · 찰스 미스너(, 1932\~)가 1959년\~1961년에 도입하였다.\[12\]\[13\]\[14\]\[15\]\[16\]\[17\]\[18\]\[19\]\[20\]\[21\]

양 ADM 에너지 정리는 1979년에 리처드 멜빈 셰인()과 [야우싱퉁](../Page/야우싱퉁.md "wikilink")이 최초로 증명하였다.\[22\] 이후 1981년에 [에드워드 위튼이](../Page/에드워드_위튼.md "wikilink") [순간자](../Page/순간자.md "wikilink")를 통한 새 증명을 제시하였고,\[23\] 이듬해에 토머스 파커()와 클리퍼드 헨리 토브스()가 위튼의 증명을 수학적으로 엄밀하게 보완하였다.\[24\]

리만-펜로즈 부등식은 1973년에 [로저 펜로즈가](../Page/로저_펜로즈.md "wikilink") 물리학을 사용하여 추측하였으며,\[25\] 2001년에 휴버트 루이스 브레이() · 게르하르트 후이스켄(, 1958\~) · 톰 일매넌(, 1961\~)이 수학적으로 엄밀히 증명하였다.\[26\]\[27\]

## 참고 문헌

[분류:일반 상대성이론](https://ko.wikipedia.org/wiki/분류:일반_상대성이론 "wikilink") [분류:리만 기하학](https://ko.wikipedia.org/wiki/분류:리만_기하학 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.