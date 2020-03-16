> This article is converted from Wikipedia: [Kp  ](https://ko.wikipedia.org/wiki/Kp__).


[응집물질물리학](../Page/응집물질물리학.md "wikilink")에서, ***k·p* 섭동 이론**()은 [띠구조](../Page/띠구조.md "wikilink")를 다루는 [섭동 이론의](../Page/섭동_이론_\(양자역학\).md "wikilink") 하나다.

## 전개

위치 에너지 \(\ V(\vec{r})\) 속에 있는 [전자](../Page/전자.md "wikilink")의 [해밀토니언은](../Page/해밀토니언_\(양자역학\).md "wikilink") 다음과 같다.

\[H_0=\mathbf p^2/2m+V(\mathbf r)+\frac1{4m^2c^2}(\boldsymbol{\sigma}\times\nabla V)\cdot\mathbf p\]. 전자 [파동 함수](../Page/파동_함수.md "wikilink") \(\psi(\mathbf r)\)는 [슈뢰딩거 방정식](../Page/슈뢰딩거_방정식.md "wikilink")

\[H_0\psi(\mathbf r)=E\psi(\mathbf r)\] 을 만족한다.

[위치 에너지](../Page/위치_에너지.md "wikilink") \(\ V(\vec{r})\)은 [브라베 격자의](../Page/브라베_격자.md "wikilink") 주기성을 지닌다. 따라서 [파동 함수를](../Page/파동_함수.md "wikilink") [블로흐 파](../Page/블로흐_파.md "wikilink")

\[\psi(\mathbf r)=\sum_{\mathbf k}\exp(i\mathbf k\cdot\mathbf r)u_{\mathbf k}(\mathbf r)\] 로 나타내자. 여기서 \(u_{\mathbf k}\)는 [브라베 격자의](../Page/브라베_격자.md "wikilink") 주기성을 지닌다. 그렇다면 [슈뢰딩거 방정식을](../Page/슈뢰딩거_방정식.md "wikilink") 다음과 같이 쓸 수 있다.

\[H_{\mathbf k}u_{\mathbf k}(\mathbf r)=E_{\mathbf k}u_{\mathbf k}(\mathbf r)\]. 여기서

\[H_{\mathbf k}=H_0+H'_{\mathbf k}=H_0+\hbar\mathbf k\cdot\mathbf p/m+\hbar^2\mathbf k^2/2m+
\frac1{4m^2c^2}(\boldsymbol{\sigma}\times\nabla V)\cdot\mathbf k\] 이다. 이제 \(H_0\)을 제외한 항들 \(H'_{\mathbf k}\)를 원래 해밀토니언 \(H_0\)에 대한 [섭동항으로](../Page/섭동_이론_\(양자역학\).md "wikilink") 간주하여 [섭동 이론을](../Page/섭동_이론_\(양자역학\).md "wikilink") 전개할 수 있다. 이 섭동 이론을 ***k·p* 섭동 이론**이라고 한다.

### 기본적인 경우

가장 기본적인 경우로, [스핀-궤도 결합](https://ko.wikipedia.org/wiki/스핀-궤도_결합 "wikilink") \((\boldsymbol{\sigma}\times\nabla V)\cdot\mathbf p\)를 무시한 경우를 생각히 보자. 만약 [결정 구조가](../Page/결정_구조.md "wikilink") 원점 대칭을 가진다면, parity에 의해 \(\langle n0| \vec{p} |0n \rangle = 0\) 이 성립한다. 즉, 에너지 1차 섭동은 0이다. 에너지 2차 섭동은 다음과 같다.

\[\varepsilon_n(\vec{k}) = \varepsilon_n(0) + {\vec{k}^2 \over 2m} + {1 \over m^2} \sum_{\delta\neq n}{\langle n0|p_{\mu}k_{\mu}|0\delta\rangle\langle\delta0|p_{\nu}k_{\nu}|0n\rangle\over \varepsilon_{n0} - \varepsilon_{\delta0}}\]

이 때, 고유함수를 1차항까지 전개하면,

\[|\vec{k}n \rangle = exp(i\vec{k}\cdot \vec{r}) (|0n\rangle + {1 \over m}\sum_{\delta\neq n}{\langle\delta 0|\vec{k}\cdot \vec{p} |0 n\rangle\over \varepsilon_{n0} - \varepsilon_{\delta 0}})\].

[유효 질량의](https://ko.wikipedia.org/wiki/유효_질량 "wikilink") 정의는 다음과 같다.

\[({1 \over m^*})_{\mu\nu} = {\partial \over\partial{k_{\mu}}}{\partial\over\partial{k_{\nu}}}\varepsilon_n(\vec{k})\]

이 정의를 이용해 \(\varepsilon_n(\vec{k})\)를 이차항까지 아래와 같은 꼴로 적어 준다.

\[\varepsilon_n(\vec{k}) = \varepsilon_n(0) + {1 \over 2m}({m \over m^*})_{\mu\nu} k_{\mu}k_{\nu}\] 이 식과 앞에서 구한, 섭동에 따른 전개식을 사용하면, 다음과 같은 결과에 도달하게 된다.

\[({m \over m^*})_{\mu\nu} = \delta_{\mu\nu} + {2\over m}\sum_{\delta\neq n}{\langle n0|p_{\mu}|0\delta\rangle\langle\delta0|p_{\nu}|0n\rangle\over \varepsilon_{n0} - \varepsilon_{\delta0}}\]

우변의 분모가 매우 작은 경우, 유효 질량 \(m^*\)이 실제 질량 \(m\)보다 매우 작게 된다. 예를 들어, [반도체](../Page/반도체.md "wikilink") Cd<sub>*x*</sub>Hg<sub>1−*x*</sub>Te (\(x = 0.136\))의 경우, [전도띠](https://ko.wikipedia.org/wiki/전도띠 "wikilink")의 [바닥 상태에서는](https://ko.wikipedia.org/wiki/바닥_상태 "wikilink") 유효 질량이 \(m^*/m\le 4*10^{-4}\)으로 매우 작다.

### 스핀-궤도 결합

[스핀-궤도 결합](https://ko.wikipedia.org/wiki/스핀-궤도_결합 "wikilink") 효과를 고려하는 경우에는 보통 다음과 같은 **역학적 운동량**() \(\boldsymbol\pi\)를 정의한다.

\[\boldsymbol\pi = \mathbf p +\frac1{mc^2} \boldsymbol\sigma \times \nabla V(\mathbf r)\]. 그렇다면 섭동 해밀토니언 \(H'_{\mathbf k}\)는 다음과 같다.

\[H'_{\mathbf k}=\hbar\mathbf k\cdot\boldsymbol\pi/m+\hbar^2\mathbf k^2/2m.\] 즉, 스핀-궤도 결합을 고려하려면 모든 공식에서 바른틀 운동량 \(\mathbf p\)를 역학적 운동량 \(\boldsymbol\pi\)로 치환하기만 하면 된다.

### 겹침이 있는 경우의 k·p 섭동 이론

[겹침이](https://ko.wikipedia.org/wiki/겹침_\(물리학\) "wikilink") 있는 경우 *k·p* 섭동 이론은 더 복잡해진다. 기본적인 방법은 겹침이 없는 경우와 같으나, 기저를 새롭게 잡아서 해밀토니언의 섭동항의 대각 성분만 살려주도록 해야 한다. 경우에 따라 그 방법이 다양하다.\[1\]

## 참고 문헌

  -
[분류:응집물질물리학](https://ko.wikipedia.org/wiki/분류:응집물질물리학 "wikilink") [분류:반도체](https://ko.wikipedia.org/wiki/분류:반도체 "wikilink")

1.