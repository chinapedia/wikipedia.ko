> This article is converted from Wikipedia: [ K](https://ko.wikipedia.org/wiki/_K).


[대수적 위상수학에서](../Page/대수적_위상수학.md "wikilink"), **위상 K이론**(位相K理論, )은 [위상 공간](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink") 위의 [벡터 다발을](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") 연구하는 분야이다.\[1\] 보다 일반적인 [K이론](../Page/K이론.md "wikilink")의 특수한 경우다.

## 정의

### 벡터 다발을 통한 정의

#### 0차 K군

다음이 주어졌다고 하자.

  - [콤팩트](https://ko.wikipedia.org/wiki/콤팩트_공간 "wikilink") [하우스도르프 공간](https://ko.wikipedia.org/wiki/하우스도르프_공간 "wikilink") \(X\)
  - 기호 \(G \in \{\operatorname O,\operatorname U,\operatorname{Sp}\}\). 이에 대하여,
      - \(\operatorname O\)-벡터 다발은 \(X\) 위의 (유한 차원, 연속) 실수 [벡터 다발이다](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink"). (O는 [직교군](https://ko.wikipedia.org/wiki/직교군 "wikilink")을 뜻한다.)
      - \(\operatorname U\)-벡터 다발은 \(X\) 위의 (유한 차원, 연속) [복소수 벡터 다발이다](https://ko.wikipedia.org/wiki/복소수_벡터_다발 "wikilink"). (U는 [유니터리 군을](https://ko.wikipedia.org/wiki/유니터리_군 "wikilink") 뜻한다.)
      - \(\operatorname{Sp}\)-벡터 다발은 \(X\) 위의 (유한 차원, 연속) 실수 짝수 차원 [벡터 다발](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") 가운데, (만약 \(2n\)차원이라면) \(\operatorname{Sp}(2n;\mathbb R)\)--[주다발](https://ko.wikipedia.org/wiki/주다발 "wikilink")의 [연관 벡터 다발로](https://ko.wikipedia.org/wiki/연관_벡터_다발 "wikilink") 표현되는 것이다. (Sp는 [심플렉틱 군을](https://ko.wikipedia.org/wiki/심플렉틱_군 "wikilink") 뜻한다.)

그렇다면, \(X\) 위의 \(G\)-[벡터 다발](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink")

\[E \twoheadrightarrow X\] 들의 동형류들의 집합을 생각할 수 있다. 이는 직합을 통하여 [가환 모노이드를](https://ko.wikipedia.org/wiki/가환_모노이드 "wikilink") 이루며, \(G \in \{\operatorname O,\operatorname U\}\)인 경우 텐서곱을 통하여 [가환 반환을](https://ko.wikipedia.org/wiki/가환_반환 "wikilink") 이룬다. ([직합](https://ko.wikipedia.org/wiki/직합 "wikilink")에 대한 항등원은 자명한 0차원 벡터 다발이며, 텐서곱에 대한 항등원은 자명한 1차원 실수 또는 복소수 벡터 다발이다.)

\(X\)의 \(G\)에 대한 **K군**() \(\mathrm KG^0(X)\)는 \(X\) 위의 \(G\)-[벡터 다발들의](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") [그로텐디크 군이다](https://ko.wikipedia.org/wiki/그로텐디크_군 "wikilink"). 만약 \(G \in \{\operatorname O,\operatorname U\}\)라면, 이는 [가환환](https://ko.wikipedia.org/wiki/가환환 "wikilink")을 이룬다.

흔히, 만약 \(G\)를 생략하였다면, \(G = \operatorname U\)를 뜻한다.

#### 축소 K군

\((X,x_0)\)가 [점을 가진 공간이라고](../Page/점을_가진_공간.md "wikilink") 하자. 그렇다면 **축소 K군**(縮小K群, ) \(\operatorname{\tilde K}^0(X,x_0)\)는 다음과 같다. 다음과 같은 [준동형](https://ko.wikipedia.org/wiki/준동형 "wikilink")이 존재한다.

\[\phi\colon\operatorname K^0(X)\to\operatorname  K^0(\{x_0\})\] 그렇다면

\[\operatorname {\tilde K}^0(X,x_0)=\ker\phi=\operatorname K^0(X)/\operatorname K^0(\{x_0\})\] 이다.

[벡터 다발의](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") 차원에 해당하는, 다음과 같은 [군 준동형이](https://ko.wikipedia.org/wiki/군_준동형 "wikilink") 존재한다.

\[\dim\colon\operatorname  K^0(X)\to\operatorname{\check H}^0(X,\mathbb Z)\] 여기서 \(\check H^0(X,\mathbb Z)\)는 정수 계수를 가지는 [체흐 코호몰로지다](https://ko.wikipedia.org/wiki/체흐_코호몰로지 "wikilink"). 만약 \(X\)가 [연결 공간이라면](https://ko.wikipedia.org/wiki/연결_공간 "wikilink") \(\check H^0(X,\mathbb Z)=\mathbb Z\)이다. 이 경우 \(\dim\colon K^0(X)\to\mathbb Z\)이며, [벡터 공간](https://ko.wikipedia.org/wiki/벡터_공간 "wikilink") \(K_n^0(X)=\dim^{-1}(n)\)은 \(n\)차원 벡터 다발들이 이루는 [그로텐디크 군이다](https://ko.wikipedia.org/wiki/그로텐디크_군 "wikilink").

**상대 K군**()은 [상대 호몰로지와](https://ko.wikipedia.org/wiki/상대_호몰로지 "wikilink") 유사한 개념으로, 다음과 같다. \(A\subseteq X\)가 부분 공간이라고 하자. 그렇다면 \(X\)의 \(A\)에 대한 **상대 K군** \(\operatorname K^0(X,A)\)는 다음과 같다.

\[\operatorname K^0(X,A)=\operatorname{\tilde K}^0(X/A)\] 여기서 \(X/A\)의 점은 물론 \(A/A\in X/A\)이다.

\(X\)가 (콤팩트하지 않을 수 있는) [국소 콤팩트](https://ko.wikipedia.org/wiki/국소_콤팩트 "wikilink") [하우스도르프 공간이라고](https://ko.wikipedia.org/wiki/하우스도르프_공간 "wikilink") 하자. 그렇다면, **[콤팩트 지지](https://ko.wikipedia.org/wiki/콤팩트_지지 "wikilink") K군**() \(\operatorname K_{\text{c}}^0(X)\)는 그 [알렉산드로프 콤팩트화](../Page/알렉산드로프_콤팩트화.md "wikilink") \(X^+\)의 축소 K군이다.

\[\operatorname K_{\text{c}}^0(X)=\operatorname {\tilde K}^0(X^+)\] 물론, 만약 \(X\)가 콤팩트 하우스도르프 공간이라면,

\[\operatorname K_{\text{c}}^0(X)=\operatorname {\tilde K}^0(X^+)=\operatorname {\tilde K}^0(X\sqcup\{\bullet\})=\operatorname K^0(X)\] 이다.

#### 고차 K군

**−n차 축소 K군** \(\operatorname K^{-n}(X)\)는 다음과 같다.

\[\operatorname{\tilde K}^{-n}(X)=\operatorname{\tilde K}(\mathbb S^n\wedge X)\] 여기서 \(\wedge\)는 위상 공간의 [분쇄곱](../Page/분쇄곱.md "wikilink")이고, \(\mathbb S^n\)은 \(n\)차원 [초구](https://ko.wikipedia.org/wiki/초구 "wikilink")다. 여기서 \(S^0\wedge X\cong X\)이므로, \(\operatorname {\tilde K}^0(X)\)의 정의는 일관적이다. 또한 \(\mathbb S^m\wedge\mathbb S^n\cong\mathbb S^{m+n}\)이므로, \(\tilde K^{-m-n}(X)=\tilde K^{-m}(S^n\wedge X)\)이다.

**−n차 (비축소) K군** \(\operatorname K^{-n}(X)\)는 그 [알렉산드로프 콤팩트화](../Page/알렉산드로프_콤팩트화.md "wikilink") \(X^+=X\sqcup\{\infty\}\)의 축소 K군이다.

\[\operatorname K^{-n}(X)=\operatorname{\tilde K}^{-n}(X^+)\]

고차 축소 K군들은 주기적이다. 즉, 다음이 성립한다.

  - \(\operatorname {\tilde KU}^{-n-2}(X)=\operatorname{\tilde KU}^{-n}(X)\)
  - \(\operatorname {\tilde KO}^{-n-8}(X)=\operatorname{\tilde KO}^{-n}(X)\).

이를 [보트 주기성](https://ko.wikipedia.org/wiki/보트_주기성 "wikilink")()이라고 한다. 보트 주기성을 사용하여 양의 정수차 K군 \(K^1\), \(K^2\) 등을 정의할 수 있다.

### 안정 벡터 다발을 통한 정의

[콤팩트](https://ko.wikipedia.org/wiki/콤팩트_공간 "wikilink") [하우스도르프 공간](https://ko.wikipedia.org/wiki/하우스도르프_공간 "wikilink") \(X\)가 주어졌다고 하자. \(X\) 위의 두 (유한 차원, 연속) [복소수 벡터 다발](https://ko.wikipedia.org/wiki/복소수_벡터_다발 "wikilink") \(E\), \(F\) 사이에 다음과 같은 [동치 관계를](https://ko.wikipedia.org/wiki/동치_관계 "wikilink") 정의하자.

\[E \sim F \iff \exists n \in\mathbb N\colon E\oplus\mathbb C^n \cong F\oplus\mathbb C^n\] 여기서 \(\mathbb C^n\)은 \(n\)차원 자명한 [복소수 벡터 다발이며](https://ko.wikipedia.org/wiki/복소수_벡터_다발 "wikilink"), 우변의 \(\cong\)은 연속 복소수 벡터 다발의 동형이다.

이 [동치 관계에](https://ko.wikipedia.org/wiki/동치_관계 "wikilink") 대한 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")를 **안정 벡터 다발**(安定vector다발, )이라고 한다. 안정 벡터 다발들은 직합에 대하여 [가환 모노이드를](https://ko.wikipedia.org/wiki/가환_모노이드 "wikilink") 이루며, 이는 사실 [아벨 군이다](https://ko.wikipedia.org/wiki/아벨_군 "wikilink"). 이를 \(X\)의 0차 **축소 K군** \(\operatorname{\widetilde{KU}}^0(X)\)이라고 한다.

### 분류 공간을 통한 정의

기호 \(G \in \{\operatorname O,\operatorname U,\operatorname{Sp}\}\)가 주어졌다고 하자. 그렇다면, [리 군의](https://ko.wikipedia.org/wiki/리_군 "wikilink") 포함 관계

\[G(0) \hookrightarrow G(1) \hookrightarrow \dotsb\] 에 대한 [분류 공간의](../Page/분류_공간.md "wikilink") 포함 관계

\[\mathrm BG(0) \to \mathrm BG(1) \to \mathrm BG(2) \to \dotsb\] 가 존재한다. 구체적으로, 이는 어떤 위상 공간 \(X\) 위의 \(G(n)\)-[벡터 다발](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") \(E\twoheadrightarrow X\)가 주어졌을 때, \(\operatorname G(n+1)\)-벡터 다발 \(E\oplus\mathbb K\)를 취하는 것이다 (\(\mathbb K\)는 자명한 1차원 또는 2차원 벡터 다발). 이에 따라서, [귀납적 극한](https://ko.wikipedia.org/wiki/귀납적_극한 "wikilink")

\[\varinjlim \mathrm BG(\infty)\] 를 취할 수 있다.

이들은 구체적으로 다음과 같이 표현된다. [직교군](https://ko.wikipedia.org/wiki/직교군 "wikilink") \(\operatorname O(n)\)의 [분류 공간](../Page/분류_공간.md "wikilink") \(\operatorname{BO}(n)\)은 무한 차원 실수 벡터 공간에서 원점을 지나는 \(n\)차원 부분 공간들의 공간([그라스만 다양체](../Page/그라스만_다양체.md "wikilink"))이며, [유니터리 군](https://ko.wikipedia.org/wiki/유니터리_군 "wikilink") \(\operatorname U(n)\)의 [분류 공간](../Page/분류_공간.md "wikilink") \(\operatorname{BU}(n)\)은 무한 차원 복소수 벡터 공간에서 원점을 지나는 복소수 \(n\)차원 부분 공간들의 공간이다.

\(X\)가 [CW 복합체와](https://ko.wikipedia.org/wiki/CW_복합체 "wikilink") [호모토피 동치인](https://ko.wikipedia.org/wiki/호모토피_동치 "wikilink") 위상 공간이라고 하자. 그렇다면, \(X\)의 **K군**은 다음과 같다.

\[\mathrm KG(X) = [X,\mathbb Z\times\mathrm BG(\infty)]\] 여기서 \([X,Y]\)는 \(X\to Y\) [호모토피류](https://ko.wikipedia.org/wiki/호모토피류 "wikilink")들의 집합이다.

만약, \(X\)가 \(n\)차원 [연결 공간이고](https://ko.wikipedia.org/wiki/연결_공간 "wikilink") \(k>n/2\)일 때,

\[\operatorname{\widetilde{KO}}(X)\cong[X,\operatorname{BO}(k)]\]

\[\operatorname{\widetilde{KU}}(X)\cong[X,\operatorname{BU}(k)]\] 이 성립한다.

## 성질

### 함자성

\(\mathcal C\)가 적절한 위상 공간의 범주(예를 들어, [콤팩트 생성](../Page/콤팩트_생성_공간.md "wikilink") [약한 하우스도르프 공간의](https://ko.wikipedia.org/wiki/약한_하우스도르프_공간 "wikilink") 범주)라고 하자. 그렇다면, 위상 K이론은 다음과 같은 [함자를](https://ko.wikipedia.org/wiki/함자_\(수학\) "wikilink") 정의한다.

\[\operatorname{KO}\colon\operatorname{ho}(\mathcal C) \to \operatorname{CRing}^{\operatorname{op}}\]

\[\operatorname{KU}\colon\operatorname{ho}(\mathcal C) \to \operatorname{CRing}^{\operatorname{op}}\]

\[\operatorname{KSp}\colon\operatorname{ho}(\mathcal C) \to \operatorname{Ab}^{\operatorname{op}}\] 여기서

  - \(\operatorname{ho}(\mathcal C)\)는 위상 공간의 [호모토피 범주이다](https://ko.wikipedia.org/wiki/호모토피_범주 "wikilink").
  - \(\operatorname{CRing}\)은 [가환환](https://ko.wikipedia.org/wiki/가환환 "wikilink")의 범주이다.
  - \(\operatorname{Ab}\)은 [가환군](https://ko.wikipedia.org/wiki/가환군 "wikilink")의 범주이다.
  - \((-)^{\operatorname{op}}\)은 [반대 범주이다](https://ko.wikipedia.org/wiki/반대_범주 "wikilink").

즉, [연속 함수](https://ko.wikipedia.org/wiki/연속_함수 "wikilink") \(X\to Y\)가 주어지면, 이에 따라 [환 준동형](https://ko.wikipedia.org/wiki/환_준동형 "wikilink") \(K(Y)\to K(X)\)가 존재한다.

또한, 축소 위상 K이론은 다음과 같이 [점을 가진 공간의](../Page/점을_가진_공간.md "wikilink") 범주 위의 함자를 정의한다.

\[\operatorname{\widetilde{KO}}\colon\operatorname{ho}(\mathcal C/\bullet) \to \operatorname{CRing}^{\operatorname{op}}\]

\[\operatorname{\widetilde{KU}}\colon\operatorname{ho}(\mathcal C/\bullet) \to \operatorname{CRing}^{\operatorname{op}}\]

\[\operatorname{\widetilde{KSp}}\colon\operatorname{ho}(\mathcal C/\bullet) \to \operatorname{Ab}^{\operatorname{op}}\]

특히, 위상 K이론은 [호모토피](https://ko.wikipedia.org/wiki/호모토피 "wikilink") 불변량이다. 즉, 서로 [호모토피 동치인](https://ko.wikipedia.org/wiki/호모토피_동치 "wikilink") 공간들의 K군들은 동형이다.

### 보트 주기성

다음이 성립한다.

\[\operatorname{\widetilde{KU}}^{\bullet+2}(X) \cong \operatorname{\widetilde{KU}}^\bullet(X)\]

\[\operatorname{\widetilde{KO}}^{\bullet+8}(X) \cong \operatorname{\widetilde{KO}}^\bullet(X)\]

\[\operatorname{\widetilde{KSp}}^{\bullet+8}(X) \cong \operatorname{\widetilde{KSp}}^\bullet(X)\]

[분류 공간으로서](../Page/분류_공간.md "wikilink"), 이는 다음과 같은 호모토피 동치에서 기인한다.

\[\Omega^8\mathrm{BO}(\infty) \simeq \mathbb Z \times \mathrm{BO}(\infty)\]

\[\Omega^2\mathrm{BU}(\infty) \simeq \mathbb Z \times \mathrm{BU}(\infty)\]

\[\Omega^8\mathrm{Sp}(\infty) \simeq \mathbb Z \times \mathrm{BSp}(\infty)\]

### 코호몰로지

위상 K이론은 [코호몰로지](https://ko.wikipedia.org/wiki/코호몰로지 "wikilink")에 대한 [에일렌베르크-스틴로드 공리들을](../Page/에일렌베르크-스틴로드_공리.md "wikilink") 차원 공리를 제외하고 모두 만족시킨다. 따라서, 위상 K이론은 특수(extraordinary) 코호몰로지 이론을 이룬다. (차원 공리에 따르면 \(H^n(\{\bullet\})=0\forall n>0\)이어야 하지만, K이론에서는 \(\operatorname{KU}^{2n}(\{\bullet\})=\mathbb Z\)이다.)

### 천 지표

[천 지표](../Page/천_지표.md "wikilink") \(\operatorname{ch}\colon\operatorname{Vect}(X)\to\operatorname H^\bullet(X)\)는 \(X\) 위의 [벡터 다발들의](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") [가환 모노이드](https://ko.wikipedia.org/wiki/가환_모노이드 "wikilink") \(\operatorname{Vect}(X)\)로부터 짝수 차수 유리수 코호몰로지 \(\operatorname H^0(X)\oplus\operatorname H^2(X)\oplus\dotsb\subset\operatorname H^\bullet(X;\mathbb Q)\)로 가는 [모노이드 준동형이다](https://ko.wikipedia.org/wiki/모노이드_준동형 "wikilink").\[2\]\[3\] 이는 [그로텐디크 군](https://ko.wikipedia.org/wiki/그로텐디크_군 "wikilink") 연산을 통해, 다음과 같은 [환 준동형](https://ko.wikipedia.org/wiki/환_준동형 "wikilink") \(\operatorname{ch}\colon K^0(X)\to H^\bullet(X;\mathbb Q)\)로 확장된다. 즉, \([E],[F]\in K^0(X)\)라고 하면,

\[\operatorname{ch}([E]\oplus[F])=\operatorname{ch}([E])+\operatorname{ch}([F])\]

\[\operatorname{ch}([E]\otimes[F])=\operatorname{ch}([E])\smile\operatorname{ch}([F])\]

\[\operatorname{ch}(-[E])=-\operatorname{ch}([E])\]

\[\operatorname{ch}([\mathbb C^{\oplus k}])=k\] 이다. 다시 말해, 천 지표는 K이론에서 코호몰로지로 가는 준동형이다. 마찬가지로, 축소 K이론에서 축소 코호몰로지로 가는 준동형 \(\operatorname{ch}\colon\tilde K^0(X)\to\tilde H^\bullet(X;\mathbb Q)\) 또한 존재한다.

고차 K이론의 경우에도 천 지표를 정의할 수 있다.\[4\]

\[\operatorname{\widetilde{KU}}^1(X)=\operatorname{KU}^0(\mathbb S^1\wedge X)\]

\[\operatorname{\tilde H}^{2k}(X;\mathbb Q)\cong\operatorname H^{2k+1}(\mathbb S^1\wedge X;\mathbb Q)\] 이므로, 이를 사용하여 천 지표를

\[\operatorname K^\bullet(X)\to\operatorname H^\bullet(X;\mathbb Q)\] 로 확장시킬 수 있다. 대부분(유한 [CW 복합체](https://ko.wikipedia.org/wiki/CW_복합체 "wikilink"))의 경우, 천 지표는 \(K^\bullet(X)\otimes\mathbb Q\)와 \(H^\bullet(X;\mathbb Q)\) 사이의 [동형 사상이다](https://ko.wikipedia.org/wiki/동형_사상 "wikilink"). 즉, 다음과 같은 동형 사상이 성립한다.\[5\]

\[\operatorname{KU}^0(X)\otimes\mathbb Q=\bigoplus_k\operatorname H^{2k}(X;\mathbb Q)\]

\[\operatorname{KU}^1(X)\otimes\mathbb Q=\bigoplus_k\operatorname H^{2k+1}(X;\mathbb Q)\] 마찬가지로, 실수 K군의 경우 다음이 성립한다.\[6\]

\[\operatorname{KO}^0(X)\otimes\mathbb Q=\bigoplus_k\operatorname H^{4k}(X;\mathbb Q)\]

## 예

### 축약 가능 공간

하나의 점을 포함하는 공간 \(\{\bullet\}\)의 K군들은 다음과 같다.

\[K^0(\{\bullet\})=\mathbb Z\]

\[\tilde K^0(\{\bullet\})=0\]

\[K^1(\{\bullet\})=\tilde K^1(\{\bullet\})=0\] K이론은 [호모토피](https://ko.wikipedia.org/wiki/호모토피 "wikilink") 불변량이므로, 모든 [콤팩트](https://ko.wikipedia.org/wiki/콤팩트_공간 "wikilink") [하우스도르프](https://ko.wikipedia.org/wiki/하우스도르프_공간 "wikilink") [축약 가능 공간의](../Page/축약_가능_공간.md "wikilink") K군은 1점 공간 \(\{\bullet\}\)의 K군과 같다.

이에 따라, 축소 K군의 경우

\[K^0(X)\cong\tilde K^0(X)\oplus\mathbb Z\]

\[K^1(X)\cong\tilde K^1(X)\] 임을 알 수 있다.

### 초구

[초구](https://ko.wikipedia.org/wiki/초구 "wikilink") \(S^n\)의 (비축소) 복소수 K군들은 다음과 같다.\[7\]

\[\operatorname{KU}^0(\mathbb S^{2n})=\mathbb Z^2\]

\[\operatorname{KU}^1(\mathbb S^{2n})=0\]

\[\operatorname{KU}^0(\mathbb S^{2n+1})=\mathbb Z\]

\[\operatorname{KU}^1(\mathbb S^{2n+1})=\mathbb Z\] 초구의 축소 복소수 K군들은 다음과 같다.

\[\operatorname{\widetilde{KU}}^0(\mathbb S^{2n})=\operatorname{\widetilde{KU}}^1(\mathbb S^{2n+1})=\mathbb Z\]

\[\operatorname{\widetilde{KU}}^1(\mathbb S^{2n})=\operatorname{\widetilde{KU}}^0(\mathbb S^{2n+1})=0\] 초구의 축소 실수 K군들은 다음과 같다.\[8\]

\[\operatorname{\widetilde{KO}}^m(\mathbb S^n) =
\begin{cases}
\mathbb Z&n-m\equiv 0,4\pmod8\\
\mathbb Z/(2)&n-m\equiv 1,2\pmod8\\
0&n-m\equiv 3,5,6,7\pmod8
\end{cases}\]

### 기타 공간

복소수 [사영 공간](https://ko.wikipedia.org/wiki/사영_공간 "wikilink") \(\mathbb{CP}^n\)의 K군들은 다음과 같다.

\[K^0(\mathbb{CP}^n)=\mathbb Z^{n+1}\]

\[K^1(\mathbb{CP}^n)=0\] [원환면](https://ko.wikipedia.org/wiki/원환면 "wikilink") \(\mathbb T^n\)의 K군들은 다음과 같다.

\[K^0(\mathbb T^n)=\mathbb Z^{2^{n-1}}\]

\[K^1(\mathbb T^n)=\mathbb Z^{2^{n-1}}\]

## 역사

[마이클 아티야와](https://ko.wikipedia.org/wiki/마이클_아티야 "wikilink") [프리드리히 히르체브루흐가](https://ko.wikipedia.org/wiki/프리드리히_히르체브루흐 "wikilink") 1950년대 말에 창시하였다.\[9\]

## 참고 문헌

  -
[분류:대수적 위상수학](https://ko.wikipedia.org/wiki/분류:대수적_위상수학 "wikilink") [분류:K이론](https://ko.wikipedia.org/wiki/분류:K이론 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.