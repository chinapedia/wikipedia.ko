> This article is converted from Wikipedia: [BF ](https://ko.wikipedia.org/wiki/BF_).


[이론물리학](https://ko.wikipedia.org/wiki/이론물리학 "wikilink")에서, **BF 모형**(BF模型, )은 [시바르츠형 위상 양자장론의](https://ko.wikipedia.org/wiki/시바르츠형_위상_양자장론 "wikilink") 간단한 예이다.\[1\]\[2\] [게이지 이론의](../Page/게이지_이론.md "wikilink") 매우 간단한 형태이다.

## 정의

\(M\)이 \(d\)차원 [매끄러운 다양체이고](../Page/매끄러운_다양체.md "wikilink"), 그 위에 올이 [리 군](../Page/리_군.md "wikilink") \(G\)인 [주다발](../Page/주다발.md "wikilink") \(P\twoheadrightarrow M\)이 주어졌다고 하자. 또한, \(G\)의 [리 대수](../Page/리_대수.md "wikilink") \(\mathfrak g\) 위에 [비퇴화 쌍선형 형식](https://ko.wikipedia.org/wiki/비퇴화_쌍선형_형식 "wikilink") \(K\colon\mathfrak g\times\mathfrak g\to\mathbb R\)이 존재한다고 하자. (보통 [킬링 형식의](https://ko.wikipedia.org/wiki/킬링_형식 "wikilink") 스칼라배를 사용한다.)

**BF 모형**은 다음과 같은 두 장으로 구성되는 [양자장론](../Page/양자장론.md "wikilink")이다.

  - \(A\)는 \(P\)의 [주접속](../Page/주접속.md "wikilink")이다. 즉, [게이지 보손에](../Page/게이지_보손.md "wikilink") 해당한다.
  - \(B\in\Omega^{d-2}(M;\mathfrak g)\)는 \(M\) 위에 정의된, 리 대수 \(\mathfrak g\)에 값을 갖는 \((d-2)\)차 [미분 형식이다](../Page/미분_형식.md "wikilink").

두 장 모두 [게이지 대칭을](https://ko.wikipedia.org/wiki/게이지_대칭 "wikilink") 가진다.\[3\]

\[A\mapsto A+\mathrm d\alpha + [A,\alpha]\]

\[B\mapsto B+[B,\alpha] + \mathrm d\Lambda+[A,\Lambda]\] 여기서 \(\alpha\in\Omega^1(M;\mathfrak g)\)이며, \(\Lambda\in\Omega^{d-3}(M;\mathfrak g)\)이다. 즉, \(B\)는 [미분 형식 전기역학에서의](../Page/미분_형식_전기역학.md "wikilink") 퍼텐셜과 유사한 게이지 대칭을 가진다.

BF 모형의 [작용은](../Page/작용_\(물리학\).md "wikilink") 다음과 같다.

\[S=\int_MK(B\wedge F)\] 여기서 \(F=d_AA\)는 \(A\)의 [곡률](../Page/곡률.md "wikilink") (장세기)이다.

만약 \(d=3,4\)일 경우, 특별히 다음과 같은 “[우주 상수](https://ko.wikipedia.org/wiki/우주_상수 "wikilink")” \(\lambda\) 항을 추가할 수 있다.\[4\]

\[S=\int_MK(B\wedge F + \lambda B\wedge B)\qquad(d=4)\]

\[S=\int_MK(B\wedge F + \lambda B\wedge B\wedge B)\qquad(d=3)\]

## 성질

### 장방정식

[우주 상수](https://ko.wikipedia.org/wiki/우주_상수 "wikilink") 항이 없을 때, BF 작용의 [오일러-라그랑주 방정식은](../Page/오일러-라그랑주_방정식.md "wikilink") 다음과 같다.

  - \(F=0\)
  - \(d_AB=0\)

따라서, 고전적으로 \(A\)는 [평탄 주접속이고](../Page/평탄_주접속.md "wikilink"), \(B\)는 [닫힌 미분 형식이다](https://ko.wikipedia.org/wiki/닫힌_미분_형식 "wikilink").

우주 상수 항을 추가하면, \(d=4\)에서 [오일러-라그랑주 방정식은](../Page/오일러-라그랑주_방정식.md "wikilink") 대신 다음과 같다.

\[F+2\lambda B = 0\]

\[d_AB = 0\]

### 양자화

편의상, 시공간

\[M=\mathbb R\times\Sigma\]

\[\dim\Sigma=d-1\] 을 생각하자. 그렇다면, \(M\)은 \(\Sigma\)와 [호모토피 동치이므로](../Page/호모토피_동치.md "wikilink"), 사실 \(\Sigma\) 위에 \(G\)-[주다발](../Page/주다발.md "wikilink") \(P\twoheadrightarrow\Sigma\)이 주어졌다고 가정할 수 있다.

이 위에서 BF 모형의 양자화를 생각하자. 이 경우, [위상 공간](../Page/위상_공간_\(물리학\).md "wikilink") \(\mathcal M_\Sigma\)은 다음과 같다.

\[\mathcal M_\Sigma = \mathrm T^*\mathcal A^{\text{flat}}_\Sigma\] 여기서

  - \(\mathcal A^{\text{flat}}_\Sigma\)는 \(P\twoheadrightarrow\Sigma\)의 [평탄 주접속들의](../Page/평탄_주접속.md "wikilink") 공간이다.

이 경우, [주접속](../Page/주접속.md "wikilink") \(A_\mu^a\)에 대응하는 [일반화 운동량은](../Page/일반화_운동량.md "wikilink") \(B^a_{\mu_1\dotsb\mu_{d-2}}\)이다. 즉, 정준 교환 관계는 다음과 같다.

\[\{
B^a_{\mu_1\dotso\mu_{d-2}}(x),A_{b\mu_{d-1}}(y)
\} = \delta^a_b \operatorname{vol}^\Sigma_{\mu_1\dotso\mu_{d-1}} \delta(x,y)\] 여기서

  - \(\operatorname{vol}^\Sigma_{\mu_1\dotso\mu_{d-1}}\)는 \(\Sigma\)의 [부피 형식이다](../Page/부피_형식.md "wikilink").

따라서, 그 [힐베르트 공간은](../Page/힐베르트_공간.md "wikilink") 단순히

\[\mathcal H=\operatorname L^2(\mathcal A^{\text{flat}}_\Sigma)\] 이다.

[천-사이먼스 이론과](../Page/천-사이먼스_이론.md "wikilink") 비교했을 때, 천-사이먼스 이론의 경우 3차원에서 \(\Sigma\)가 [리만 곡면의](../Page/리만_곡면.md "wikilink") 구조를 가지므로, \(\mathcal A^{\text{flat}}_\Sigma\)는 이미 [켈러 다양체의](../Page/켈러_다양체.md "wikilink") 구조를 가지며, \(\mathcal A^{\text{flat}}_\Sigma\) 자체가 [위상 공간이며](../Page/위상_공간_\(물리학\).md "wikilink"), \(A\)는 스스로의 [일반화 운동량이](../Page/일반화_운동량.md "wikilink") 된다. 그러나 BF 이론에서는 \(\mathcal A^{\text{flat}}_\Sigma\)는 위상 공간이 아니라 배위 공간이다.

### 우주 상수 항이 있는 경우의 양자화

우주 상수 항이 있을 경우, 양자화는 다음과 같이 달라진다. 우선, 더 이상 \(F=0\)이 아니게 된다. 우선, (평탄하거나 평탄하지 않을 수 있는) 주접속의 (무한 차원) 공간을 \(\mathcal A_\Sigma\)라고 하자. 그렇다면, [위상 공간은](../Page/위상_공간_\(물리학\).md "wikilink") \(\mathrm T^*\mathcal A_\Sigma\) 속에서,

\[F+2\lambda B = 0\] 을 만족시키는 점들의 공간이다. 즉, 파동 함수는 \(G\)에 대한 [게이지 변환에](https://ko.wikipedia.org/wiki/게이지_변환 "wikilink") 대하여 불변인, \(\mathcal A_\Sigma\) 위의 함수 \(\psi\) 가운데,

\[0=\left(F_{\mu\nu}^a - 2\mathrm i\lambda\operatorname{vol}_{\mu\nu\rho}^\Sigma \frac\delta{\delta A_{\rho a}}\right)\psi\] 을 만족시키는 것이다. 만약 \(\Sigma\) 위의 \(G\)-[주다발](../Page/주다발.md "wikilink")이 (위상수학적으로) [자명한 올다발이라면](https://ko.wikipedia.org/wiki/자명한_올다발 "wikilink"), 이 [편미분 방정식은](https://ko.wikipedia.org/wiki/편미분_방정식 "wikilink") 하나의 [일차 독립](https://ko.wikipedia.org/wiki/일차_독립 "wikilink") 해를 가지며, 이는 구체적으로

\[\psi(A) = \exp\left(-\mathrm iS_{\text{CS}}(A)/4\lambda\right)\] 이다. 여기서

\[S_{\text{CS}}(A)=\int_\Sigma \operatorname{tr}\left(A\wedge\mathrm dA+\frac23A\wedge A\wedge A\right)\] 는 \(\Sigma\) 위의 [천-사이먼스 이론의](../Page/천-사이먼스_이론.md "wikilink") 작용([천-사이먼스 형식](../Page/천-사이먼스_형식.md "wikilink"))이다. 이는

\[\frac{\delta S_{\text{CS}}}{\delta A_{\rho a}} = \operatorname{vol}_\Sigma^{\mu\nu\rho}F_{\mu\nu}^a\] 이기 때문이다.

## 성질

### 양-밀스 이론과의 관계

BF 모형은 부피가 0인 다양체 위의 [양-밀스 이론으로](../Page/양-밀스_이론.md "wikilink") 생각할 수 있다.\[5\]

[양-밀스 이론의](../Page/양-밀스_이론.md "wikilink") 작용은

\[S_\text{YM}=\int_M\frac1{g^2}K(F\wedge*F)\] 이다. 여기서 \(g^2\)는 [결합 상수이고](../Page/결합_상수.md "wikilink"), \(*\)는 [호지 쌍대이다](../Page/호지_쌍대.md "wikilink"). 여기에 [보조장](../Page/보조장.md "wikilink") \(B\)를 도입하자. 그렇다면, 양-밀스 이론은 다음과 같이 동등하게 나타낼 수 있다.

\[S_\text{YM}'=\int_M(K(B\wedge F)+\frac12g^2K(B\wedge*B))\] 이제, 결합 상수를 0으로 보내자.

\[g^2\to0\] 그렇다면

\[\lim_{g^2\to0}S_\text{YM}'=\int_MK(B\wedge F)=S_{BF}\] 가 되어, BF 모형이 됨을 알 수 있다.

[호지 쌍대](../Page/호지_쌍대.md "wikilink") \(*\)를 대신 [부피 형식](../Page/부피_형식.md "wikilink") \(\omega\)와 내적

\[\langle X,Y\rangle\omega=K(X\wedge*Y)\] 로 쓰자. 그렇다면

\[S_\text{YM}'=\int_M(K(B\wedge F)+\frac12g^2\omega\langle B,B\rangle)\] 이 된다. 이는

\[\omega'=g^2\omega\] 에만 의존하게 된다. 이는 다양체 \(M\)의 "부피"

\[\operatorname{vol}(M)=\int_M\omega'=\int_Mg^2\omega\] 로 생각할 수 있다. 그렇다면 BF 모형의 극한은 \(\omega'\)로 측정한 부피가 0으로 가는 극한으로 생각할 수 있다.

### 초대칭 BF 모형

BF 모형에 [초대칭](../Page/초대칭.md "wikilink")을 추가하여 **초대칭 BF 모형**()을 정의할 수 있다. 이는 더 이상 [시바르츠형 위상 양자장론이](https://ko.wikipedia.org/wiki/시바르츠형_위상_양자장론 "wikilink") 아니며, 대신 [위튼형 위상 양자장론이다](https://ko.wikipedia.org/wiki/위튼형_위상_양자장론 "wikilink"). 이 경우, 장들은 다음과 같다. 모든 장은 \(G\)의 [딸림표현](../Page/딸림표현.md "wikilink")을 따른다.

  - 게이지 초장 \((A,\psi)\). 여기서 \(A\)는 U(1) 게이지 보손이며, \(\psi\)는 벡터 페르미온이다. 이 경우 \(QA=\psi\)이다.
  - 라그랑주 승수 초장 \((\chi,B)\). 여기서 \(B\)는 \((d-2)\)차 미분 형식인 보손이며, \(\chi\) 역시 \((d-2)\)차 미분 형식인 페르미온이다. 이 경우 \(Q\chi=B\)이다.
  - 유령 초장 \((\bar\phi,\eta)\). \(Q\bar\phi=\eta\)이며 \(Q\eta=[\bar\phi,\phi]\)이다.

이에 따라, 작용은 다음과 같다.\[6\]

\[S=Q\int(\chi F+\bar\phi d*\psi)=\int \left(BF+(-1)^d\chi d\psi+\eta d*\psi+\bar\phi[\psi,*\psi]-\bar\phi d*d\phi\right)\] 초대칭이 없는 경우와 마찬가지로, 이 경우 이론은 \(M\) 위의 \(G\)-[평탄 주접속들의](../Page/평탄_주접속.md "wikilink") [모듈라이 공간의](../Page/모듈라이_공간.md "wikilink") 특성을 계산한다.

만약 시공간이 3차원일 경우 (\(d=3\)), 이 이론은 추가로 \(\mathcal N_T=2\) 위상 초대칭을 갖는다.\[7\]\[8\] 즉, 두 개의 스칼라 초전하(BRST 연산자)를 가지며, 이 둘을 섞는 SU(2) [R대칭](../Page/R대칭.md "wikilink")이 존재하며, 이 아래 \((\chi,\psi)\)는 SU(2)의 2차원 기본 표현을 따른다. 이 이론은 3차원 \(\mathcal N=4\) 게이지 이론의 A-뒤틂과 같으며, 이는 [도널드슨 이론을](https://ko.wikipedia.org/wiki/도널드슨_이론 "wikilink") 3차원으로 [축소화](../Page/축소화.md "wikilink")한 것과 같다.\[9\]

## 참고 문헌

## 외부 링크

  -
  -
  -
[분류:양자장론](https://ko.wikipedia.org/wiki/분류:양자장론 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.