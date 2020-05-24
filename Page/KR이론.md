> This article is converted from Wikipedia: [KR이론](https://ko.wikipedia.org/wiki/KR이론).


수학에서, **KR이론**(KR理論, )은 [대합을](https://ko.wikipedia.org/wiki/대합_\(수학\) "wikilink") 갖춘 [위상 공간](https://ko.wikipedia.org/wiki/위상_공간 "wikilink") 위의 안정 [벡터 다발을](../Page/벡터_다발.md "wikilink") 분류하는, [위상 K이론의](../Page/위상_K이론.md "wikilink") 일종이다.

## 정의

**대합 공간**() \((X,\tau)\)은 다음과 같은 데이터로 주어진다.

  - [콤팩트](../Page/콤팩트_공간.md "wikilink") [하우스도르프 공간](../Page/하우스도르프_공간.md "wikilink") \(X\)
  - [대합인](https://ko.wikipedia.org/wiki/대합_\(수학\) "wikilink") [연속](../Page/연속_함수.md "wikilink") [자기 함수](https://ko.wikipedia.org/wiki/자기_함수 "wikilink") \(\tau\colon X\to X\), \(\tau\circ\tau = \operatorname{id}_X\)

대합 공간 \((X,\tau)\) 위의 **대합 벡터 다발**()은 다음과 같은 데이터로 주어진다.

  - [복소수 벡터 다발](../Page/복소수_벡터_다발.md "wikilink") \(\pi\colon E \twoheadrightarrow X\)
  - \(E\) 위의 연속 대합 \(\tau_E\colon E \to E\)

이는 다음 두 조건을 만족시켜야 한다.

  - 영단면을 \(0_E \colon X \to E\)라고 하면, \(\pi\circ \tau_E\circ 0_E = \tau\)이다.
    :<math>\\begin{matrix}

E&\\overset{\\tau_E}\\to\&E\\\\ {\\scriptstyle\\\!\\\!\\\!\\\!0_E}\\uparrow{\\scriptstyle\\color{White}0_E\\\!\\\!\\\!\\\!}&&{\\scriptstyle\\color{White}\\\!\\\!\\\!\\\!\\pi}\\downarrow{\\scriptstyle\\pi\\\!\\\!\\\!\\\!}\\\\ X&\\underset\\tau\\to\&X \\end{matrix}</math>

  - \(\tau_E\colon E\to E\)는 (\(\tau\colon X\to X\) 위의) 실수 벡터 다발의 동형 사상이며, 임의의 \(x\in E\)에 대하여 \((\tau_E\restriction E_x)\colon E_x \to E_{\tau(x)}\)는 [복소수 벡터 공간의](https://ko.wikipedia.org/wiki/복소수_벡터_공간 "wikilink") 반선형 변환이다. 즉, \(v\in E_x\) 및 \(\lambda\in\mathbb C\)에 대하여 \(\tau_E(\lambda v) = \bar\lambda\tau_E(v)\)이다.

대합 공간 위의 대합 벡터 다발들의 직합을 취할 수 있으며, 이에 따라서 주어진 대합 공간 위의 대합 벡터 다발의 동형류는 [가환 모노이드를](https://ko.wikipedia.org/wiki/가환_모노이드 "wikilink") 이룬다. 이 가환 모노이드의 [그로텐디크 구성을](https://ko.wikipedia.org/wiki/그로텐디크_구성 "wikilink") 대합 공간의 **KR군**이라고 한다.

## 성질

### 다른 K이론과의 관계

복소수 벡터 다발의 [위상 K군](https://ko.wikipedia.org/wiki/위상_K군 "wikilink") \(\operatorname{KU}^0(-)\)과 실수 벡터 다발의 [위상 K군](https://ko.wikipedia.org/wiki/위상_K군 "wikilink") \(\operatorname{KO}^0(-)\)은 KR군의 특별한 경우로 주어진다.

콤팩트 하우스도르프 공간 \(X\) 위에 [항등 함수인](../Page/항등_함수.md "wikilink") [대합](https://ko.wikipedia.org/wiki/대합_\(수학\) "wikilink") \(\operatorname{id}_X\)을 부여하자. 그렇다면, 이 대합 공간 위의 대합 벡터 다발 \((E,\tau_E)\)이 주어졌을 때, 항상 실수 벡터 다발

\[E_{\mathbb R} = \{v\in E\colon \tau_E(v) = v \}\]

\[E \cong E_{\mathbb R} \otimes \mathbb C\] 을 정의할 수 있으며, 따라서 그 위의 대합 벡터 다발(의 동형류)은 \(X\) 위의 실수 벡터 다발(의 동형류)과 동치이다. 따라서, 이 경우 KR군은 KO군과 같다.

\[\operatorname{KR}^0(X,\operatorname{id}_X) = \operatorname{KO}^0(X)\]

콤팩트 하우스도르프 공간 \(X\)가 주어졌을 때, \(X\times\{\pm1\}\) 위에 대합

\[(x,\pm1)\mapsto(x,\mp1)\] 을 부여하자. 그렇다면, \(X\times\{\pm1\}\) 위의 대합 벡터 다발은 \(X\) 위의 복소수 벡터 다발과 동치이다. 따라서, 이 경우 \(X\times\{\pm1\}\)의 KR군은 \(X\)의 KU군과 같다.

\[\operatorname{KR}^0(X\times\{\pm1\},(x,\pm1)\mapsto(x,\mp1)) = \operatorname{KU}^0(X)\]

### 보트 주기성

일반 위상 K이론과 마찬가지로, **축소 KR군**() \(\operatorname{\widetilde{KR}}^{0,0}(X)\)을 정의할 수 있다.

[유클리드 공간](../Page/유클리드_공간.md "wikilink") \(\mathbb R^{m+n}\) 위에 대합

\[(x,y)\mapsto(x,-y)\qquad(x\in\mathbb R^m,\;y\in\mathbb R^n)\] 을 부여한 것을 \(\mathbb R^{m,n}\)으로 표기하자. 그 속의 \(m+n-1\)차원 공 및 [초구](../Page/초구.md "wikilink")를 다음과 같이 표기하자.

\[\mathbb D^{m,n}=\{(x,y)\in\mathbb R^{m,n}\colon \|x\|^2+\|y\|^2\le1\} \cong \mathbb D^{m+n}\]

\[\mathbb S^{m,n}=\{(x,y)\in\mathbb R^{m,n}\colon \|x\|^2+\|y\|^2=1\} \cong \mathbb S^{m+n-1}\] 그렇다면, 다음과 같이 두 개의 등급을 갖는 (축소) KR군들을 정의할 수 있다.

\[\operatorname{KR}^{m,n}(X)=\operatorname{KR}^{0,0}(X\times \mathbb D^{m,n})\]

\[\operatorname{\widetilde{KR}}^{m,n}(X)=\operatorname{\widetilde{KR}}^{0,0}(X\wedge \mathbb D^{m,n})\] (여기서 \(\wedge\)는 [분쇄곱](../Page/분쇄곱.md "wikilink")이다.) 그렇다면, 다음과 같은 **보트 주기성**()이 성립한다.

\[\operatorname{KR}^{m,n}(X) \cong \operatorname{KR}^{m+1,n+1}(X) \cong \operatorname{KR}^{m+8,n}(X)\] 즉, KR군은 오직 \((m-n)\bmod8\)에만 의존한다. 보통

\[\operatorname{\widetilde{KR}}^{m,n}(X) = \operatorname{\widetilde{KR}}^{n-m}(X)\] 으로 표기한다. 특히, \(\mathbb S^{m,n}\)은 ‘\(m-n-1\)차원 초구’로 해석되며, 이를 통하여 음의 차원의 초구를 생각할 수 있다.

실수 · 복소수 K이론의 보트 주기성은 KR이론의 보트 주기성의 특수한 경우이다.

## 응용

[끈 이론에서](../Page/끈_이론.md "wikilink"), [오리엔티폴드](../Page/오리엔티폴드.md "wikilink")가 주어진 [시공간](../Page/시공간.md "wikilink")은 대합 공간을 이루며, 그 위의 [D-막](../Page/D-막.md "wikilink")들은 KR군에 의하여 분류된다.\[1\]

## 역사

1966년에 [마이클 아티야가](../Page/마이클_아티야.md "wikilink") 도입하였다.\[2\] 이름 ‘KR’에서, ‘K’는 원래 [K이론](../Page/K이론.md "wikilink")에서 딴 것이다. (이는 의 첫 글자이다.) ‘R’는 의 첫 글자이다.

## 참고 문헌

## 외부 링크

  -
[분류:K이론](https://ko.wikipedia.org/wiki/분류:K이론 "wikilink")

1.
2.