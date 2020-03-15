> This article is converted from Wikipedia: [Ext ](https://ko.wikipedia.org/wiki/Ext_).


[호몰로지 대수학에서](https://ko.wikipedia.org/wiki/호몰로지_대수학 "wikilink"), **Ext 함자**(Ext函子, )는 [아벨 범주의](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") 두 대상 사이를 잇는 [완전열](https://ko.wikipedia.org/wiki/완전열 "wikilink")들을 분류하는 [함자이다](https://ko.wikipedia.org/wiki/함자_\(수학\) "wikilink"). 사상군 함자의 [유도 함자와](../Page/유도_함자.md "wikilink") 같다.

## 정의

[Ext 함자는](../Page/Ext_함자.md "wikilink") 세 가지로 정의할 수 있다.

  - Ext 함자는 특정 [완전열](https://ko.wikipedia.org/wiki/완전열 "wikilink")들의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink") 집합으로 정의할 수 있다. 이는 가장 구체적이지만 복잡하며, 또 [집합론](https://ko.wikipedia.org/wiki/집합론 "wikilink")적 문제가 발생할 수 있다 (즉, Ext 함자의 값이 [고유 모임일](https://ko.wikipedia.org/wiki/고유_모임 "wikilink") 수 있다). 이 정의는 [요네다 노부오가](https://ko.wikipedia.org/wiki/요네다_노부오 "wikilink") 도입하였다.\[1\]
  - [단사 대상을 충분히 가지는 범주](https://ko.wikipedia.org/wiki/단사_대상을_충분히_가지는_범주 "wikilink") 또는 [사영 대상을 충분히 가지는 범주에서](https://ko.wikipedia.org/wiki/사영_대상을_충분히_가지는_범주 "wikilink"), Ext 함자는 [오른쪽 유도 함자](https://ko.wikipedia.org/wiki/오른쪽_유도_함자 "wikilink") 또는 [왼쪽 유도 함자를](https://ko.wikipedia.org/wiki/왼쪽_유도_함자 "wikilink") 사용하여 정의할 수 있다. 이 경우 집합론적 문제가 발생하지 않지만, 이는 [단사 대상](https://ko.wikipedia.org/wiki/단사_대상 "wikilink") 또는 [사영 대상이](https://ko.wikipedia.org/wiki/사영_대상 "wikilink") 부족한 [아벨 범주에서는](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") 사용할 수 없다.
  - [유도 범주의](../Page/유도_범주.md "wikilink") 개념을 사용하면 Ext 함자는 매우 간단하게 정의된다. 그러나 [유도 함자의](../Page/유도_함자.md "wikilink") 존재 역시 여러 집합론적 문제를 야기한다.

[대수학](https://ko.wikipedia.org/wiki/대수학 "wikilink")에서 가장 중요한 경우인 [환](https://ko.wikipedia.org/wiki/환_\(수학\) "wikilink") 위의 [가군](https://ko.wikipedia.org/wiki/가군 "wikilink") 범주의 경우 [단사 대상을 충분히 가지는 범주이자](https://ko.wikipedia.org/wiki/단사_대상을_충분히_가지는_범주 "wikilink") [사영 대상을 충분히 가지는 범주이므로](https://ko.wikipedia.org/wiki/사영_대상을_충분히_가지는_범주 "wikilink"), [유도 함자](../Page/유도_함자.md "wikilink") 정의를 사용할 수 있다.

### 완전열을 통한 정의

#### 0차 Ext

임의의 [아벨 범주](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") \(\mathcal A\)에 대하여, **0차 Ext 함자**는 다음과 같은 사상군 함자이다.

\[\operatorname{Ext}^0_{\mathcal A}(-,-)=\hom_{\mathcal A}(-,-)\colon\mathcal A^{\operatorname{op}}\times\mathcal A\to\operatorname{Ab}\]

#### 1차 Ext

임의 [아벨 범주](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") \(\mathcal A\)의 대상 \(A,B\in\mathcal A\)에 대하여, \(A\)의 \(B\)에 대한 **확대**()는 다음과 같은 [짧은 완전열이다](https://ko.wikipedia.org/wiki/짧은_완전열 "wikilink").

\[0\to B\to X\to A\to0\] 두 확대 사이에 다음 그림을 가환하게 만드는 사상 \(X\to X'\)이 존재한다면, 두 확대가 서로 **동치**라고 한다.

\[\begin{matrix}
0\to&B&\to&X&\to&A&\to0\\
&\|&&\downarrow\scriptstyle\wr&&\|\\
0\to&B&\to&X'&\to&A&\to0
\end{matrix}\] (이 사상 \(X\to X'\)은 [짧은 5항 보조정리에](https://ko.wikipedia.org/wiki/짧은_5항_보조정리 "wikilink") 따라서 항상 [동형 사상이다](https://ko.wikipedia.org/wiki/동형_사상 "wikilink").) 이는 확대에 대한 [동치 관계를](https://ko.wikipedia.org/wiki/동치_관계 "wikilink") 이룬다.

확대의 동치류들은 **베어 합**()이라는 연산 아래 [아벨 군을](https://ko.wikipedia.org/wiki/아벨_군 "wikilink") 이룬다.\[2\] 두 확대 \(0\to B\xrightarrow\iota X\xrightarrow\pi A\to0\), \(0\to B\xrightarrow{\iota'} X'\xrightarrow{\pi'} A\to0\)가 주어졌을 때, \(Y\)를 \(X\)와 \(X'\)의 \(A\)에 대한 [당김이라고](../Page/당김_\(범주론\).md "wikilink") 하자. [미첼 매장 정리를](https://ko.wikipedia.org/wiki/미첼_매장_정리 "wikilink") 사용하면, 이는 다음과 같다.

\[X\oplus X\supseteq Y=\{(x,x')\in X\oplus X'\colon \pi(x)=\pi'(x)\}\supseteq\iota(B)\oplus\iota'(B)\] 즉, \(Y\)는 \(B\)를 두 번 부분 대상으로 포함한다. 대각 사상 \(\operatorname{diag}_B\colon B\to B\oplus B\)사용하여, \(Y\)의 몫대상

\[X''=\frac Y{\left((\iota,-\iota')\circ\operatorname{diag}_B\right)(B)}\] 을 정의할 수 있다. 이는 \(Y\) 속에 존재하는 두 개의 \(B\)를 하나로 합치는 것이다. 그렇다면

\[0\to B\to X''\to A\to0\] 는 [짧은 완전열을](https://ko.wikipedia.org/wiki/짧은_완전열 "wikilink") 이룬다. \(0\to X\to X''\to A\to0\)의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")를 \(0\to B\xrightarrow\iota X\xrightarrow\pi A\to0\), \(0\to B\xrightarrow{\iota'} X'\xrightarrow{\pi'} A\to0\)의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")의 **베어 합**()이라고 한다. 확대의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")들은 베어 합 아래 [아벨 군을](https://ko.wikipedia.org/wiki/아벨_군 "wikilink") 이룬다. 베어 합의 항등원은 [분할 완전열](../Page/분할_완전열.md "wikilink") \(0\to B\to A\oplus B\to A\to0\)이며, 확대 \(0\to B\xrightarrow\iota X\xrightarrow\pi A\to0\)의 베어 합에 대한 역원은 \(0\to B\xrightarrow{-\iota}X\xrightarrow\pi A\to0\) 또는 \(0\to B\xrightarrow\iota X\xrightarrow{-\pi} A\to0\)이다. (이 둘은 서로 동치이다.)

\(\mathcal A\) 속의 대상 \(A,B\in\mathcal A\)에 대하여, **1차 Ext 함자** \(\operatorname{Ext}^1_{\mathcal A}(A,B)\)는 \(A\)의 \(B\)에 대한 확대들의 동치류 집합이다. 이는 베어 합 아래 [아벨 군을](https://ko.wikipedia.org/wiki/아벨_군 "wikilink") 이루며, 함자

\[\operatorname{Ext}^1_{\mathcal A}(-,-)\colon\mathcal A^{\operatorname{op}}\times\mathcal A\to\operatorname{Ab}\] 를 정의한다. 또한, 각 \(A\in\mathcal A\)에 대하여

\[\operatorname{Ext}^1_{\mathcal A}(A,-)\colon\mathcal A^{\operatorname{op}}\to\operatorname{Ab}\]

\[\operatorname{Ext}^1_{\mathcal A}(-,A)\colon\mathcal A^{\operatorname{op}}\to\operatorname{Ab}\] 는 둘 다 [가법 함자를](https://ko.wikipedia.org/wiki/가법_함자 "wikilink") 이룬다.

위 정의에서, [집합론](https://ko.wikipedia.org/wiki/집합론 "wikilink")적 문제를 무시하였다. 사실, ([국소적으로 작은](https://ko.wikipedia.org/wiki/국소적으로_작은_범주 "wikilink")) [아벨 범주의](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") 경우 1차 Ext 함자의 값이 [고유 모임일](https://ko.wikipedia.org/wiki/고유_모임 "wikilink") 수 있다.\[3\] 물론, [작은](../Page/작은_범주.md "wikilink") [아벨 범주에](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") 대해서는 이러한 문제가 생기지 않는다. 또한, [단사 대상을 충분히 가지는 범주나](https://ko.wikipedia.org/wiki/단사_대상을_충분히_가지는_범주 "wikilink") [사영 대상을 충분히 가지는 범주에서는](https://ko.wikipedia.org/wiki/사영_대상을_충분히_가지는_범주 "wikilink") [유도 함자를](../Page/유도_함자.md "wikilink") 통한 정의를 사용할 수 있으며, 이 경우 집합론적 문제가 발생하지 않는다.

#### 고차 Ext

2차 이상의 Ext 함자는 임의의 [아벨 범주에](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") 대하여 다음과 같이 정의할 수 있다.\[4\]\[5\]\[6\]\[7\]

[아벨 범주](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") \(\mathcal A\)가 주어졌다고 하자. \(\mathcal A\) 속의 대상 \(A\), \(B\)에 대하여, \(A\)의 \(B\)에 대한 \(n\)차 **확대**()는 다음과 같은 [완전열](https://ko.wikipedia.org/wiki/완전열 "wikilink")이다.

\[0\to B\to X_n\to X_{n-1}\to\cdots\to X_1\to A\to0\] 두 \(n\)차 확대 \((B,X_\bullet,A)\), \((B',X_\bullet',A')\) 사이에 다음과 같은 가환 그림이 존재한다면, \((B,X_\bullet,A)\)가 \((B',X_\bullet',A')\)의 **닮은 확대**()라고 한다.

\[\begin{matrix}
0\to &B&\to&X_n&\to&\cdots&\to&X_1&\to&A&\to0\\
&\|&&\downarrow&&\cdots&&\downarrow&&\|\\
0\to &B'&\to&X_n'&\to&\cdots&\to&X_1'&\to&A'&\to0
\end{matrix}\] 닮음 관계를 \((B,X_\bullet,A)\prec(B',X_\bullet',A')\)로 표기하자. 닮음 관계는 [추이적 관계이지만](https://ko.wikipedia.org/wiki/추이적_관계 "wikilink") [대칭 관계가](https://ko.wikipedia.org/wiki/대칭_관계 "wikilink") 아니다. 닮음 관계로 생성되는 [동치 관계를](https://ko.wikipedia.org/wiki/동치_관계 "wikilink") 생각하자. 즉, 두 \(n\)차 확대 \((B,X_\bullet,A)\), \((B',X_\bullet',A')\) 사이에 다음과 같은 \(n\)차 확대들의 [열](https://ko.wikipedia.org/wiki/수열 "wikilink")

\[(B,X_\bullet,A)=(B^{(0)},X_\bullet^{(0)},A^{(0)}),(B^{(1)},X_\bullet^{(1)},A^{(1)}),\dots,(B^{(k)},X_\bullet^{(k)},A^{(k)})=(B',X_\bullet',A')\] 이 존재하며, 이 열이 다음 조건을 만족시킨다면, \((B,X_\bullet,A)\)와 \((B',X_\bullet',A')\)가 서로 **동치**라고 하자.

  -
    모든 \(i=1,2,\dots,k\)에 대하여, \((B^{(i-1)},X_\bullet^{(i-1)},A^{(i-1)})\prec(B^{(i)},X_\bullet^{(i)},A^{(i)})\)이거나 또는 \((B^{(i)},X_\bullet^{(i)},A^{(i)})\prec(B^{(i-1)},X_\bullet^{(i-1)},A^{(i-1)})\)이다.

사실, 이 동치는 두 단계로 족하다. 즉, 다음 세 조건이 서로 [동치](https://ko.wikipedia.org/wiki/동치 "wikilink")이다.\[8\]

  - \((B,X_\bullet,A)\)와 \((B',X_\bullet',A')\)가 서로 동치이다.
  - \((B,X_\bullet,A)\prec(B'',X_\bullet'',A'')\succ(B',X_\bullet',A')\)인 \(n\)차 확대 \((B'',X_\bullet'',A'')\)가 존재한다.
  - \((B,X_\bullet,A)\succ(B'',X_\bullet'',A'')\prec(B',X_\bullet',A')\)인 \(n\)차 확대 \((B'',X_\bullet'',A'')\)가 존재한다.

그렇다면, \(n\)차 **Ext 함자** \(\operatorname{Ext}^n_{\mathcal A}(A,B)\)는 \(A\)의 \(B\)에 대한 \(n\)차 확대들의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink") 집합이다.

두 \(n\)차 확대 \((B,X_\bullet,A)\), \((B',X_\bullet',A')\)가 주어졌을 때, \(Y_i\)를 다음과 같이 정의하자.

  - \(i=1\)일 때, \(Y_1\)은 \(X_1\)과 \(X_1'\)의 \(A\)에 대한 [당김이다](../Page/당김_\(범주론\).md "wikilink").
  - \(1<i<n\)일 때, \(Y_i=X_1\oplus X_1'\)이다.
  - \(i=n\)일 때, \(X_n\xrightarrow f\tilde Y\xleftarrow{f'}X_n'\)를 \(B\xrightarrow\iota X_n\)과 \(B\xrightarrow{\iota'}X_n\)의 \(B\)에 대한 [밂이라고](../Page/밂_\(범주론\).md "wikilink") 하자. 그렇다면 대각 사상 \(\operatorname{diag}_B\colon B\to B\oplus B\)를 사용하여, \((f\circ\iota,-f'\circ\iota')\circ\operatorname{diag}_B\colon B\to\tilde Y\)를 정의할 수 있다. 그렇다면, \(Y_n=\tilde Y/((f\circ\iota,-f'\circ\iota')\circ\operatorname{diag}_B)(B)\)이다.

그렇다면 \((B,Y_\bullet',A)\)는 \(n\)차 확대를 이룬다. \((B,X_\bullet,A)\)의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")와 \((B',X_\bullet',A')\)의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")의 합을 \((B,Y_\bullet',A)\)의 [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")로 정의하자.

\[[(B,X_\bullet,A)]+[(B',X_\bullet',A')]=[(B,Y_\bullet',A)]\] 그렇다면, 이 합에 대하여 \(\operatorname{Ext}^n_{\mathcal A}(A,B)\)는 [아벨 군을](https://ko.wikipedia.org/wiki/아벨_군 "wikilink") 이룬다. 또한, 이는 [함자](https://ko.wikipedia.org/wiki/함자_\(수학\) "wikilink")

\[\operatorname{Ext}^n_{\mathcal A}(-,-)\colon\mathcal A^{\operatorname{op}}\times\mathcal A\to\operatorname{Ab}\] 를 이루며, 각 \(A\in\mathcal C\)에 대하여

\[\operatorname{Ext}^n_{\mathcal A}(A,-)\colon\mathcal A\to\operatorname{Ab}\]

\[\operatorname{Ext}^n_{\mathcal A}(-,A)\colon\mathcal A^{\operatorname{op}}\to\operatorname{Ab}\] 둘 다 [가법 함자를](https://ko.wikipedia.org/wiki/가법_함자 "wikilink") 이룬다.

#### 요네다 합성

Ext는 [가법 함자를](https://ko.wikipedia.org/wiki/가법_함자 "wikilink") 이루므로, [아벨 범주](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") \(\mathcal A\)의 대상 \(A,B,C\in\mathcal A\)에 대하여 다음과 같은 두 [군 준동형이](https://ko.wikipedia.org/wiki/군_준동형 "wikilink") 존재한다. (여기서 \(\otimes\)는 [아벨 군의](https://ko.wikipedia.org/wiki/아벨_군 "wikilink") [텐서곱](https://ko.wikipedia.org/wiki/텐서곱 "wikilink")이다.)

\[\operatorname{Ext}^n_{\mathcal A}(A,B)\otimes\hom_{\mathcal A}(B,C)\to\operatorname{Ext}^n_{\mathcal A}(A,C)\]

\[\hom_{\mathcal A}(A,B)\otimes\operatorname{Ext}^n_{\mathcal A}(B,C)\to\operatorname{Ext}^n_{\mathcal A}(A,C)\] 이는 \(\operatorname{Ext}^0_{\mathcal A}=\hom_{\mathcal A}\)와 \(\operatorname{Ext}^n_{\mathcal A}\)를 곱하는 것으로 볼 수 있다.

보다 일반적으로, 임의의 자연수 \(m,n\in\mathbb N\)에 대하여 다음과 같은, **요네다 합성**()이라는 [군 준동형들이](https://ko.wikipedia.org/wiki/군_준동형 "wikilink") 존재한다.\[9\]

\[\operatorname{Ext}^m_{\mathcal A}(A,B)\otimes\operatorname{Ext}^n_{\mathcal A}(B,C)\to\operatorname{Ext}^{m+n}_{\mathcal A}(A,C)\] 이는 구체적으로 다음과 같다. 두 [완전열](https://ko.wikipedia.org/wiki/완전열 "wikilink")

\[0\to A\to X_1\to\cdots\to X_m\xrightarrow\pi B\to 0\qquad(m\ge1)\]

\[0\to B\xrightarrow\iota Y_1\to\cdots\to Y_n\to C\to0\qquad(m\ge1)\] 이 주어졌을 때, 이들을 이어 다음과 같은 더 긴 [완전열](https://ko.wikipedia.org/wiki/완전열 "wikilink")을 정의할 수 있다.

\[0\to A\to X_1\to\cdots\to X_m\xrightarrow{\iota\circ\pi}Y_1\to\cdots\to Y_n\to C\to0\] 그렇다면 \((A,X_\bullet,B)\)의 동치류와 \((B,Y_\bullet,C)\)의 동치류의 **요네다 합성**은 \((A,X_\bullet,Y_\bullet,C)\)의 동치류이다.

요네다 합성을 사용하여, 자연수 등급 [아벨 군의](https://ko.wikipedia.org/wiki/아벨_군 "wikilink") 범주 \(\operatorname{GrAb}_{\mathbb N}\) 위의 [풍성한 범주](../Page/풍성한_범주.md "wikilink") \(\operatorname{Ext}\mathcal A\)를 다음과 같이 정의할 수 있다.

  - \(\operatorname{Ext}\mathcal A\)의 대상은 \(\mathcal A\)의 대상과 같다.
  - \(\operatorname{Ext}\mathcal A\)의 사상군은 다음과 같은 자연수 등급 아벨 군이다.
    \[\hom_{\operatorname{Ext}\mathcal A}(A,B)=\bigoplus_n\operatorname{Ext}^n_{\mathcal A}(A,B)\]
  - \(\operatorname{Ext}(\mathcal A\)에서 사상의 합성은 요네다 합성에 의하여 주어진다.
  - \(\operatorname{Ext}\mathcal A\)에서 항등 사상은 \(\mathcal A\)에서의 항등 사상과 같다.

\(\operatorname{Ext}\mathcal A\)에서, 각 사상군에서 양의 정수 등급 성분을 망각한다면, \(\operatorname{Ext}^0_{\mathcal A}=\hom_{\mathcal A}\)만 남으므로 원래 범주 \(\mathcal A\)를 얻는다.

특히, 대상 \(A\in\mathcal A\)에 대하여, \(\operatorname{Ext}\mathcal A\)에서의 [자기 사상](https://ko.wikipedia.org/wiki/자기_사상 "wikilink") 등급 아벨 군

\[\hom_{\operatorname{Ext}\mathcal A}(A,A)=\bigoplus_n\operatorname{Ext}^n_{\mathcal A}(A,A)\] 은 [자연수](https://ko.wikipedia.org/wiki/자연수 "wikilink") [등급환](https://ko.wikipedia.org/wiki/등급환 "wikilink")을 이룬다.

### 유도 함자를 통한 정의

[아벨 범주](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") \(\mathcal A\) 속의 대상 \(A\in\mathcal A\)에 대하여,

\[\hom_{\mathcal A}(A,-)\colon\mathcal A\to\operatorname{Ab}\] 는 [왼쪽 완전 함자이며](https://ko.wikipedia.org/wiki/왼쪽_완전_함자 "wikilink"),

\[\hom_{\mathcal A}(-,A)\colon\mathcal A^{\operatorname{op}}\to\operatorname{Ab}\] 는 [오른쪽 완전 함자이다](https://ko.wikipedia.org/wiki/오른쪽_완전_함자 "wikilink"). 따라서, 만약 \(\mathcal A\)가 [단사 대상을 충분히 가지는 범주라면](https://ko.wikipedia.org/wiki/단사_대상을_충분히_가지는_범주 "wikilink") \(\hom_{\mathcal A}(A,-)\)의 [오른쪽 유도 함자를](https://ko.wikipedia.org/wiki/오른쪽_유도_함자 "wikilink") **Ext 함자**라고 한다.

\[\operatorname{Ext}_{\mathcal C}^n(A,-)=\operatorname R^n\hom_{\mathcal C}(A,-)\] 만약 \(\mathcal A\)가 [사영 대상을 충분히 가지는 범주라면](https://ko.wikipedia.org/wiki/사영_대상을_충분히_가지는_범주 "wikilink") \(\hom_{\mathcal A}(-,A)\)의 [왼쪽 유도 함자를](https://ko.wikipedia.org/wiki/왼쪽_유도_함자 "wikilink") **Ext 함자**라고 한다.

\[\operatorname{Ext}_{\mathcal C}^n(-,A)=\operatorname L^n\hom_{\mathcal C}(-,A)\] 이 정의들은 (만약 존재한다면) 위의 일반적인 정의와 일치한다. 그러나 [아벨 범주는](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") [단사 대상이나](https://ko.wikipedia.org/wiki/단사_대상 "wikilink") [사영 대상을](https://ko.wikipedia.org/wiki/사영_대상 "wikilink") 충분히 가지지 않을 수 있으므로, 이 정의는 덜 일반적이다.

특히, [환](https://ko.wikipedia.org/wiki/환_\(수학\) "wikilink") \(R\) 위의 [왼쪽 가군들의](https://ko.wikipedia.org/wiki/왼쪽_가군 "wikilink") [아벨 범주](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") \(R\text{-Mod}\)는 [단사 대상을 충분히 가지는 범주이자](https://ko.wikipedia.org/wiki/단사_대상을_충분히_가지는_범주 "wikilink") [사영 대상을 충분히 가지는 범주이다](https://ko.wikipedia.org/wiki/사영_대상을_충분히_가지는_범주 "wikilink"). 이 경우 Ext 함자를 \(\operatorname{Ext}_R^n(-,-)\)로 표기한다.

### 유도 범주를 통한 정의

Ext 함자는 [유도 범주의](../Page/유도_범주.md "wikilink") 개념을 사용하여 간단하게 정의할 수 있다. [아벨 범주](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") \(\mathcal A\)가 주어졌다고 하자. \(\mathcal A\)의 대상을 하나의 성분만이 [영 대상이](https://ko.wikipedia.org/wiki/영_대상 "wikilink") 아닌 [사슬 복합체로](https://ko.wikipedia.org/wiki/사슬_복합체 "wikilink") 간주한다면, \(\mathcal A\)는 [사슬 복합체](https://ko.wikipedia.org/wiki/사슬_복합체 "wikilink") 범주 \(\operatorname{Ch}(\mathcal A)\)의 [충만한 부분 범주를](https://ko.wikipedia.org/wiki/충만한_부분_범주 "wikilink") 이룬다.

\(\mathcal A\) 속의 [사슬 복합체](https://ko.wikipedia.org/wiki/사슬_복합체 "wikilink") \(A\)에 대하여,

\[A[i]^\bullet=X^{\bullet+i}\]

\[d_{A[i]}=(-1)^nd|_A\] 로 정의하자. (여기서 모든 사슬 복합체의 경계 사상의 차수는 \(\deg d=+1\)이다.) 또한, \(\mathcal A\)의 [유도 범주가](../Page/유도_범주.md "wikilink") [국소적으로 작은 범주라고](https://ko.wikipedia.org/wiki/국소적으로_작은_범주 "wikilink") 하자. 그렇다면, \(\mathcal A\)의 두 대상 \(A,B\in\mathcal A\)에 대한 \(n\)차 **Ext 함자**는 [유도 범주](../Page/유도_범주.md "wikilink") \(\operatorname D(\mathcal A)\)의 다음과 같은 사상군이다.

\[\operatorname{Ext}^n_{\mathcal A}(A,B)=\hom_{\operatorname D(\mathcal A)}(A,B[i])\]

(이 경우, [집합론](https://ko.wikipedia.org/wiki/집합론 "wikilink")적 문제는 원래 [아벨 범주가](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") [국소적으로 작은 범주라고](https://ko.wikipedia.org/wiki/국소적으로_작은_범주 "wikilink") 해도, 그 [유도 범주는](../Page/유도_범주.md "wikilink") 일반적으로 [국소적으로 작은 범주가](https://ko.wikipedia.org/wiki/국소적으로_작은_범주 "wikilink") 아닐 수 있는 것이다.)

## 성질

만약 \(M\)이 [사영 가군이거나](../Page/사영_가군.md "wikilink") \(N\)이 [단사 가군이라면](../Page/단사_가군.md "wikilink"),

\[\operatorname{Ext}^n_R(M,N)=0\qquad\forall n>0\] 이다. 또한, 다음이 성립한다.

\[\operatorname{Ext}^n_R\left(\bigoplus_{i\in I}M_i,\prod_{j\in J}N_j\right)\cong\prod_{i\in I}\prod_{j\in J}\operatorname{Ext}^n_R(M_i,N_j)\]

## 예

### 벡터 공간

체 \(K\) 위의 [가군](https://ko.wikipedia.org/wiki/가군 "wikilink")의 범주에서의 Ext 함자를 생각해 보자. 체 위의 가군은 [벡터 공간이며](https://ko.wikipedia.org/wiki/벡터_공간 "wikilink"), 모든 벡터 공간은 [사영 가군이자](../Page/사영_가군.md "wikilink") [단사 가군이다](../Page/단사_가군.md "wikilink"). 즉, 벡터 공간 \(V\)의 단사 분해 및 사영 분해는 자명하다.

\[0\to V\to I^0=V\to0\]

\[0\to P^0=V\to V\to0\] 따라서, \(K\) 위의 벡터 공간 \(V\), \(W\)가 주어졌을 때, Ext 함자는 다음과 같다.

\[\operatorname{Ext}^0_K(V,W)=\hom(V,W)\]

\[\operatorname{Ext}^n_K(V,W)=0\qquad\forall n>0\]

### 아벨 군

[정수환](https://ko.wikipedia.org/wiki/정수환 "wikilink") \(\mathbb Z\) 위의 가군의 범주에서의 Ext 함자를 생각해 보자. 정수환 위의 가군은 [아벨 군이며](https://ko.wikipedia.org/wiki/아벨_군 "wikilink"), [사영 가군은](../Page/사영_가군.md "wikilink") [자유 아벨 군이며](../Page/자유_아벨_군.md "wikilink"), [단사 가군은](../Page/단사_가군.md "wikilink") [나눗셈군](../Page/나눗셈군.md "wikilink")이다. 모든 아벨 군은 길이가 1 이하인 단사 분해 및 사영 분해를 갖는다. 즉, 임의의 아벨 군 \(G\)는 [자유 아벨 군](../Page/자유_아벨_군.md "wikilink") \(P^0\)의 [몫군](https://ko.wikipedia.org/wiki/몫군 "wikilink") \(P^0/P^1\)으로 나타낼 수 있으며, [자유 아벨 군의](../Page/자유_아벨_군.md "wikilink") 모든 [부분군](https://ko.wikipedia.org/wiki/부분군 "wikilink")은 자유 아벨 군이므로 다음은 사영 분해이다.

\[0\to G\to P^0\to P^1\to0\] 마찬가지로, 임의의 아벨 군 \(G\)는 [나눗셈군](../Page/나눗셈군.md "wikilink") \(I^0\)의 [부분군](https://ko.wikipedia.org/wiki/부분군 "wikilink")으로 나타낼 수 있으며, 나눗셈군의 모든 [몫군](https://ko.wikipedia.org/wiki/몫군 "wikilink")은 나눗셈군이므로 다음은 단사 분해를 이룬다.

\[0\to G\to I^0\to I^1\to0\] [아벨 군](https://ko.wikipedia.org/wiki/아벨_군 "wikilink") \(G\), \(H\)가 주어졌을 때, Ext 함자는 다음과 같다. \(G\)의 사영 분해가 \(G\cong P^0/P^1\)이라면, Ext 함자는 다음 [사슬 복합체의](https://ko.wikipedia.org/wiki/사슬_복합체 "wikilink") [호몰로지 군이다](https://ko.wikipedia.org/wiki/호몰로지_군 "wikilink").

\[0\to\hom_{\operatorname{Ab}}(P^0,H) \xrightarrow{\operatorname{res}} \hom_{\operatorname{Ab}}(P^1,H)\to0\] 여기서 \(\operatorname{res}\colon\hom_{\operatorname{Ab}}(P^0,H)\to \hom_{\operatorname{Ab}}(P^1,H)\)은 포함 사상 \(P^1\hookrightarrow P^0\)으로부터 유도된다. 즉, 군 준동형을 부분군에 제약한 것이다. 따라서,

\[\operatorname{Ext}^0_{\mathbb Z}(G,H)\cong\hom_{\operatorname{Ab}}(G,H)\] 이며,

\[\operatorname{Ext}^1_{\mathbb Z}(G,H)\cong\hom_{\operatorname{Ab}}(P^1,H)/\operatorname{res}(\hom_{\operatorname{Ab}}(P^0,H))\] 는 [군의 확대](../Page/군의_확대.md "wikilink")

\[0\to H\to E\to G\to0\] 들의 동형류와 일대일 대응한다.

나머지 고차 Ext 함자는 모두 0이다.

\[\operatorname{Ext}^n_{\mathbb Z}(G,H)=0\qquad\forall n\ge2\]

또한, 임의의 [나눗셈군](../Page/나눗셈군.md "wikilink") \(H\)에 대하여

\[\operatorname{Ext}^1_{\mathbb Z}(G,H)=0\] 이다. 특히, [유리수](https://ko.wikipedia.org/wiki/유리수 "wikilink")의 군 \(\mathbb Q\)나 그 몫군 \(\mathbb Q/\mathbb Z\)은 나눗셈군이므로

\[\operatorname{Ext}^1_{\mathbb Z}(G,\mathbb Q)=\operatorname{Ext}^1_{\mathbb Z}(G,\mathbb Q/\mathbb Z)=0\] 이다.

| \(G\backslash H\) | \(\mathbb Z\) | \(\mathbb Z/(n)\)           | \(\mathbb Q\) |
| ----------------- | ------------- | --------------------------- | ------------- |
| \(\mathbb Z\)     | \(\mathbb Z\) | \(\mathbb Z/(n)\)           | \(\mathbb Q\) |
| \(\mathbb Z/(m)\) | 0             | \(\mathbb Z/(\gcd\{m,n\})\) | 0             |
| \(\mathbb Q\)     | 0             | 0                           | \(\mathbb Q\) |

\(\operatorname{Ext}^0_{\mathbb Z}(G,H)=\hom_{\operatorname{Ab}}(G,H)\)

| \(G\backslash H\) | \(\mathbb Z\)                       | \(\mathbb Z/(n)\)           | \(\mathbb Q\) |
| ----------------- | ----------------------------------- | --------------------------- | ------------- |
| \(\mathbb Z\)     | 0                                   | 0                           | 0             |
| \(\mathbb Z/(m)\) | \(\mathbb Z/(m)\)                   | \(\mathbb Z/(\gcd\{m,n\})\) | 0             |
| \(\mathbb Q\)     | \(\mathbb Q^{\oplus 2^{\aleph_0}}\) | 0                           | 0             |

\(\operatorname{Ext}^1_{\mathbb Z}(G,H)\)

### 리 대수 코호몰로지

[리 대수 코호몰로지는](../Page/리_대수_코호몰로지.md "wikilink") 리 대수의 [보편 포락 대수의](../Page/보편_포락_대수.md "wikilink") Ext 함자와 같다. 이를 통해 [리 군의](https://ko.wikipedia.org/wiki/리_군 "wikilink") [드람 코호몰로지를](https://ko.wikipedia.org/wiki/드람_코호몰로지 "wikilink") 계산할 수 있다.

### 층 코호몰로지

[위상 공간](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink") \(X\) 위의 아벨 군층 \(\mathcal F\)의 [층 코호몰로지는](../Page/층_코호몰로지.md "wikilink") 다음과 같이 Ext 함자의 특수한 경우이다.

\[\operatorname H^\bullet(X,\mathcal F) = \operatorname{Ext}^\bullet(\underline{\mathbb Z},\mathcal F)\] 여기서

  - Ext 함자는 \(X\) 위의 아벨 군층의 [아벨 범주에서](https://ko.wikipedia.org/wiki/아벨_범주 "wikilink") 취한 것이다.
  - \(\underline{\mathbb Z}\)는 [정수환](https://ko.wikipedia.org/wiki/정수환 "wikilink") 값의 [상수층](../Page/상수층.md "wikilink")이다.

스킴 \(X\) 위의 구조층의 코호몰로지에 대하여 다음이 성립한다.

\[\operatorname{Ext}^1(\mathcal O_X,\mathcal O_X) = \operatorname H^1(X,\mathcal O_X)\]

## 어원

‘Ext’는 (확대)의 약자다. 이는 Ext 함자가 [군의 확대와](../Page/군의_확대.md "wikilink") 관련있기 때문이다. 아벨 군 \(G\)를 다른 아벨 군 \(H\)로 확대한다면, 가능한 확대들은 \(\operatorname{Ext}^1_{\mathbb Z}(G,H)\)와 [일대일 대응한다](https://ko.wikipedia.org/wiki/일대일_대응 "wikilink").

## 같이 보기

  - [Tor 함자](../Page/Tor_함자.md "wikilink")
  - [그로텐디크 군](https://ko.wikipedia.org/wiki/그로텐디크_군 "wikilink")
  - [호몰로지 차원](../Page/호몰로지_차원.md "wikilink")

## 참고 문헌

  -
  -
## 외부 링크

  -
  -
  -
  -
[분류:호몰로지 대수학](https://ko.wikipedia.org/wiki/분류:호몰로지_대수학 "wikilink") [분류:이항연산](https://ko.wikipedia.org/wiki/분류:이항연산 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.