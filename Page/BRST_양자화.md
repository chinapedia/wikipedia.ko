> This article is converted from Wikipedia: [BRST 양자화](https://ko.wikipedia.org/wiki/BRST_양자화).


**BRST 양자화**() 또는 **베키-루에-스토라-튜틴 양자화**()는 [게이지 이론을](../Page/게이지_이론.md "wikilink") [양자화하는](../Page/양자화_\(물리학\).md "wikilink") 한 방법이다. 게이지 이론은 비물리적인 대칭 (게이지 대칭)을 지녀 그냥 양자화하기 어렵다. 게이지 대칭을 무시하고 그냥 양자화하면 그 [힐베르트 공간이](../Page/힐베르트_공간.md "wikilink") 양의 정부호의 내적을 얻지 못한다. 따라서 상태공간에 차수(grading)를 붙이고 [코호몰로지](https://ko.wikipedia.org/wiki/코호몰로지 "wikilink")를 만들어 물리적 힐베르트 공간을 얻는다.

## 역사

카를로 베키(), 알랭 루에(), 레몽 스토라()\[1\]\[2\], 러시아의 물리학자 이고리 빅토로비치 튜틴()\[3\] 이 1970년대에 도입하였다.

## 전개

게이지 이론의 상태공간 \(H\)는 ℤ₂×ℝ차수가 붙은 벡터 공간 (graded vector space)을 이룬다. 여기서 ℤ₂는 [반전성](https://ko.wikipedia.org/wiki/반전성 "wikilink")이고, ℝ은 **유령수**()다. 상태공간 위에 정의된 연산자도 마찬가지로 ℤ₂×ℝ차수가 붙어 있는데, 예를 들어 BRST 연산자 \(Q\)는 반전성 \(-1\) (홀수), 유령수 1을 가진다.

\(H_n\)이 유령수 \(n\)을 가진 상태공간의 부분공간이라고 하자. 그러면 \(Q:H_n\to H_{n+1}\)이다. \(Q^2=0\)이므로, 이는 [코호몰로지](https://ko.wikipedia.org/wiki/코호몰로지 "wikilink")를 이룬다. 이를 **BRST 코호몰로지**라고 한다.

실재하는 상태는 \(Q\)의 코호몰로지, 즉 [벡터 공간](../Page/벡터_공간.md "wikilink") \(\ker Q_{n+1}/\operatorname{Im}Q_n\)의 원소다.

### 일반적 게이지 이론의 양자화

일련의 장 \(\phi_i\)와 게이지 대칭 \(\delta_\alpha\)를 생각하자. 이들이 [리 대수](../Page/리_대수.md "wikilink")

\[[\delta_\alpha,\delta_\beta]={f_{\alpha\beta}}^\gamma\delta_\gamma\] 를 만족한다고 하자. 경로적분을 위하여 게이지 고정 조건 \(F^A(\phi_i)=0\)을 가하자. 원래 이론의 (게이지 고정 전) 작용이 \(S_0\)이라고 하면, 이론의 경로적분은 다음과 같다.

\[\frac1{V_\text{gauge}}\int D\phi\;\exp(-S_0)=\int D\phi\;DB_A;Db_ADc^\alpha \exp(-S)\] 여기서 새 작용은 다음과 같다.

\[S=S_0+i\int B_AF^A(\phi)+\int b(\delta_\alpha F^A)c^\alpha\] 여기서 \(b_A\), \(c^\alpha\)는 그라스만 장이다.

게이지 고정한 작용 \(S\)는 다음과 같은 BRST 대칭을 만족한다.

\[\delta \phi_i=-i\epsilon c^\alpha\delta_\alpha\phi_i\]

\[\delta b_A=-\epsilon B_A\]

\[\delta c^\alpha=-\frac12\epsilon c^\beta c^\gamma{f_{\beta\gamma}}^\alpha\]

\[\delta B_A=0\] 여기서 \(\epsilon\)은 그라스만 도움변수다. 이 연산자를 \(Q\)라고 부르자. 이는 \(Q^2=0\)을 만족한다. 따라서 실재하는 상태는 \(\ker Q/\operatorname{Im}Q\)이다.

### 양-밀스 이론의 양자화

[리 대수](../Page/리_대수.md "wikilink") \(\mathfrak g\)의 게이지군을 가진 양-밀스 이론을 생각하자. 즉 게이지장은 \(\mathfrak g\)의 값을 지닌 장이다. 게이지 고정 조건 \(G^a=\xi\partial^\mu A^a_\mu\)을 도입하자. 이렇게 하면 게이지장 밖에 [파데예프-포포프 유령장](../Page/파데예프-포포프_유령.md "wikilink") \(b^a\)와 \(c^a\)가 필요하다. 여기에 [보조장](../Page/보조장.md "wikilink") \(B^a\)를 추가하자.

그러면 작용은 다음과 같다.

\[\mathcal{L}=-{1\over 4g^2} \operatorname{Tr}[F^{\mu\nu}F_{\mu\nu}]+{1\over 2g^2} \operatorname{Tr}[BB]-{1\over g^2} \operatorname{Tr}[BG]-{\xi\over g^2} \operatorname{Tr}[\partial^\mu b D_\mu c]\]

여기에 BRST 연산자 \(Q\)를 다음과 같이 정의하자.

\[QA=Dc\]

\[Qc={i\over 2}[c,c]_L\]

\[QB=0\]

\[Qb=B\]

## 참고 문헌

  -
  -
  -
  -
  -
  -
## 같이 보기

  - [바탈린-빌코비스키 대수](../Page/바탈린-빌코비스키_대수.md "wikilink")

[분류:양자장론](https://ko.wikipedia.org/wiki/분류:양자장론 "wikilink") [분류:양자색역학](https://ko.wikipedia.org/wiki/분류:양자색역학 "wikilink")

1.
2.
3.