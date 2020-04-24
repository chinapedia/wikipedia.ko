> This article is converted from Wikipedia: [C\* 대수](https://ko.wikipedia.org/wiki/C\*_대수).


[함수해석학](../Page/함수해석학.md "wikilink")에서, **C\* 대수**(시스타 대수, )는 [대합 대수와](../Page/대합_대수.md "wikilink") [복소수 바나흐 대수의](https://ko.wikipedia.org/wiki/복소수_바나흐_대수 "wikilink") 구조를 서로 호환되게 갖춘 수학 구조이다.

## 정의

C\* 대수의 개념은 다양한 방법으로 정의될 수 있다.

  - 추상적으로, [복소수 대합 대수와](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") [복소수 바나흐 대수의](https://ko.wikipedia.org/wiki/복소수_바나흐_대수 "wikilink") 구조가 서로 호환되게 주어진 [복소수 벡터 공간으로](https://ko.wikipedia.org/wiki/복소수_벡터_공간 "wikilink") 여길 수 있다.
  - 사실, [복소수 바나흐 공간](https://ko.wikipedia.org/wiki/복소수_바나흐_공간 "wikilink") 구조는 [복소수 대합 대수](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") 구조로부터 정의될 수 있다. 따라서, C\* 대수를 순수하게 대수학적으로 특별한 꼴의 복소수 [대합 대수로](../Page/대합_대수.md "wikilink") 정의할 수 있다.
  - 구체적으로, [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") 위의 [유계 작용소](https://ko.wikipedia.org/wiki/유계_작용소 "wikilink") 대수로 표현될 수 있는 [복소수 바나흐 대수로](https://ko.wikipedia.org/wiki/복소수_바나흐_대수 "wikilink") 여길 수 있다. 이 정의에서, [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") 위의 \*-표현은 C\* 대수의 정의에 포함되지 않는다.

이 정의들은 모두 서로 [동치](../Page/동치.md "wikilink")이다.

### 추상적 정의

[복소수 벡터 공간](https://ko.wikipedia.org/wiki/복소수_벡터_공간 "wikilink") \(A\) 위에 다음과 같은 두 구조가 주어졌다고 하자.

  - \((A,^*)\)는 (복소수 켤레를 부여한) [복소수체](https://ko.wikipedia.org/wiki/복소수체 "wikilink") 위의 (항등원을 갖는) [대합 대수이다](../Page/대합_대수.md "wikilink"). (즉, 임의의 \(a\in A\) 및 \(\lambda\in\mathbb C\)에 대하여 \((\lambda a)^*=\bar\lambda a^*\)이다.)
  - \((A,\|\|)\)는 [복소수 바나흐 대수이다](https://ko.wikipedia.org/wiki/복소수_바나흐_대수 "wikilink").

그렇다면, \((A,^*,\|\|)\)에 대하여 다음 두 조건이 서로 [동치](../Page/동치.md "wikilink")이며, 만약 \((A,^*,\|\|)\)가 이를 만족시킨다면 **C\* 대수**라고 한다.

  - (**C\* 항등식** ) \(\Vert x^*x\Vert=\Vert x\Vert\Vert x^*\Vert\)
  - (**B\* 항등식** ) \(\Vert x\Vert=\Vert x^*\Vert\)

(C\* 항등식이 B\* 항등식을 함의하는 것은 자명하지만, 반대 방향의 함의를 증명하는 것은 자명하지 않다.)

일부 문헌에서는 C\* 대수의 정의에서 항등원의 존재를 생략하기도 한다.

### 대수적 정의

(복소수 켤레를 부여한) [복소수체](https://ko.wikipedia.org/wiki/복소수체 "wikilink") 위의 (항등원을 갖는) [대합 대수](../Page/대합_대수.md "wikilink") \((A,^*)\)가 다음 조건을 만족시킨다면, **C\* 대수**라고 한다.

  - \(a\mapsto\sup\operatorname{sp}(a^*a)\)는 \(A\) 위의 [노름](https://ko.wikipedia.org/wiki/노름 "wikilink")을 이룬다. 즉, 다음이 성립한다.
      - 임의의 \(a\in A\)에 대하여, [스펙트럼](../Page/스펙트럼_\(함수해석학\).md "wikilink") \(\operatorname{sp}(a^*a)\subseteq\mathbb C\)는 [유계 집합이다](../Page/유계_집합.md "wikilink").
      - 임의의 \(a\in A\setminus\{0\}\)에 대하여, \(1+\lambda a^*a\)가 [가역원](../Page/가역원.md "wikilink")이 아니게 만드는 복소수 \(\lambda\in\mathbb C\)가 존재한다.
      - ([삼각 부등식](https://ko.wikipedia.org/wiki/삼각_부등식 "wikilink")) 임의의 \(a,b\in A\)에 대하여, \(\sup\operatorname{sp}(a^*a+b^*b+a^*b+b^*a)\le \sup\operatorname{sp}(a^*a)+\sup\operatorname{sp}(b^*b)\)이다.
  - \(a\mapsto\sup\operatorname{sp}(a^*a)\)는 [완비 노름을](../Page/완비_거리_공간.md "wikilink") 이룬다.

이 대수적 정의는 위의 정의와 [동치](../Page/동치.md "wikilink")이다. 구체적으로, C\* 항등식으로부터 노름이 항상 \(\|a\|=\sup\operatorname{sp}(a^*a)=\operatorname{sp}(aa^*)\)임을 보일 수 있으며, 반대로 임의의 [복소수 바나흐 대수에서](https://ko.wikipedia.org/wiki/복소수_바나흐_대수 "wikilink") \(\operatorname{sp}(ab)\cup\{0\}=\operatorname{sp}(ba)\cup\{0\}\)이므로 이는 B\* 항등식을 함의한다.

### 구체적 정의

[복소수 대합 대수](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") \(A\)의 **\*-표현**()은 다음과 같은 데이터로 구성된다.

  - [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") \(\mathcal H\)
  - [유계 작용소들의](https://ko.wikipedia.org/wiki/유계_작용소 "wikilink") [복소수 바나흐 대수](https://ko.wikipedia.org/wiki/복소수_바나흐_대수 "wikilink") \(\operatorname B(\mathcal H,\mathcal H)\)로 가는 [단사](../Page/단사_함수.md "wikilink") [복소수 대합 대수](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") 준동형 \(\iota\colon A\hookrightarrow \operatorname B(\mathcal H,\mathcal H)\). 즉, \(\iota\)는 [단사 함수이며](../Page/단사_함수.md "wikilink"), [복소수 선형 변환이며](https://ko.wikipedia.org/wiki/복소수_선형_변환 "wikilink"), (항등원을 보존하는) [환 준동형이며](https://ko.wikipedia.org/wiki/환_준동형 "wikilink"), [대합을](https://ko.wikipedia.org/wiki/대합_\(수학\) "wikilink") 보존한다 (즉, \(\iota(a^*)=\iota(a)*\;\forall a\in A\). 여기서 우변의 \((-)^*\)는 [유계 작용소의](https://ko.wikipedia.org/wiki/유계_작용소 "wikilink") [에르미트 수반이다](../Page/에르미트_수반.md "wikilink").)

만약 [복소수 대합 대수가](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") 그 [상이](../Page/상_\(수학\).md "wikilink") ([작용소 노름으로](../Page/작용소_노름.md "wikilink") 정의되는 [거리 위상에](https://ko.wikipedia.org/wiki/거리_위상 "wikilink") 대하여) [닫힌집합](https://ko.wikipedia.org/wiki/닫힌집합 "wikilink")인 \*-표현을 갖는다면, 이를 **C\* 대수**라고 한다. (마지막 조건을 노름 위상 대신 강한 [작용소 위상](https://ko.wikipedia.org/wiki/작용소_위상 "wikilink") 또는 약한 [작용소 위상에](https://ko.wikipedia.org/wiki/작용소_위상 "wikilink") 대한 [닫힌집합](https://ko.wikipedia.org/wiki/닫힌집합 "wikilink")인 것으로 강화시키면, 대신 [폰 노이만 대수의](../Page/폰_노이만_대수.md "wikilink") 개념을 얻는다.)

**겔판트-나이마르크 정리**(Гельфанд-Наймарк定理, )에 따르면, 임의의 (추상적 정의에 따른) C\* 대수 \(A\)의 경우, 어떤 [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") \(\mathcal H\) 위의 작용

\[\iota\colon A\to\operatorname B(\mathcal H,\mathcal H)\] 가 존재하며, 또한 이는 [단사 함수이자](../Page/단사_함수.md "wikilink") [복소수 선형 변환이자](https://ko.wikipedia.org/wiki/복소수_선형_변환 "wikilink") [등거리 변환이며](https://ko.wikipedia.org/wiki/등거리_변환 "wikilink"), 또한 수반 연산 \(^*\)에 대한 [준동형](../Page/준동형.md "wikilink")이며, 그 [상은](../Page/상_\(수학\).md "wikilink") C\* 대수의 구체적 정의에 부합한다.

### C\* 대수의 원소

\(A\)가 C\* 대수라고 하고, \(x\in A\)라고 하자.

  - 만약 \(y\in A\)가 존재하여 \(y^*y=x\)라면, \(x\)를 **음이 아닌 원소**(陰-元素, )라고 한다. 음이 아닌 원소들의 집합은 [볼록](https://ko.wikipedia.org/wiki/볼록집합 "wikilink") 뿔(convex cone)을 이룬다.
  - 만약 \(x=x^*\)라면, \(x\)를 **[자기 수반 원소](https://ko.wikipedia.org/wiki/자기_수반_원소 "wikilink")**라고 한다. 자기 수반 원소의 [스펙트럼은](../Page/스펙트럼_\(함수해석학\).md "wikilink") 모두 실수이다.
  - \(xx^*=x^*x=1\)이라면, \(x\)를 **[유니터리 원소](https://ko.wikipedia.org/wiki/유니터리_원소 "wikilink")**라고 한다. 유니터리 원소의 스펙트럼의 원소들의 [절댓값](../Page/절댓값.md "wikilink")은 항상 1이다.
  - \(x\)의 **[스펙트럼](../Page/스펙트럼_\(함수해석학\).md "wikilink")** \(\sigma(x)\subset\mathbb C\)는 \(\lambda\cdot1-x\)가 [가역원](../Page/가역원.md "wikilink")이 아니게 되는 \(\lambda\in\mathbb C\)들의 집합이다. 일반적으로, \(\sigma(x^*)=\bar\sigma(x)\)이다.
  - \(x\)의 스펙트럼의 [절댓값](../Page/절댓값.md "wikilink")들의 [상한](https://ko.wikipedia.org/wiki/상한 "wikilink") \(\sup|\sigma(x)|=\nu(x)\)를 \(x\)의 **[스펙트럼 반지름](../Page/스펙트럼_반지름.md "wikilink")**이라고 한다. 스펙트럼 반지름은 다음과 같이 정의할 수도 있다.
    \[\nu(x)=\lim_{n\to\infty}\Vert x^n\Vert^{1/n}\]

## 연산

### 직합

유한 또는 무한 개의 C\* 대수 \((A_i)_{i\in I}\)가 주어졌다고 하자. 그렇다면, 다음과 같은 [복소수 벡터 공간](https://ko.wikipedia.org/wiki/복소수_벡터_공간 "wikilink")

\[\widehat\bigoplus_{i\in I}A_i
\subseteq\prod_{i\in I}A_i\]

\[a\in \widehat\bigoplus_{i\in I}A_i
\iff \sup_{i\in I}\|a_i\|_{A_i}<\infty\] 위에 [균등 노름](https://ko.wikipedia.org/wiki/균등_노름 "wikilink")

\[\|a\|_{\widehat\bigoplus_i A_i}=\sup_{i\in I}\|a_i\|_{A_i}\] 및 성분별 곱셈

\[(ab)_i=a_ib_i\qquad(i\in I)\] 을 부여하면, 이는 C\* 대수를 이룬다. 이 경우 항등원은 \(1_{\widehat\bigoplus_iA_i}=(1_{A_i})_{i\in I}\) 이다.

물론, 만약 \(I\)가 유한 집합이라면, 이는 단순히 [직합](../Page/직합.md "wikilink") \(\textstyle\bigoplus_{i\in I}A_i\)과 같다.

### 몫대수

다음이 주어졌다고 하자.

  - C\* 대수 \(A\)
  - \(A\)의 [양쪽 아이디얼](https://ko.wikipedia.org/wiki/양쪽_아이디얼 "wikilink") \(\mathfrak I\subseteq A\). 또한, \(\mathfrak I\)가 [닫힌집합](https://ko.wikipedia.org/wiki/닫힌집합 "wikilink")이라고 하자.

그렇다면, 그 몫환 \(A/\mathfrak I\) 역시 C\* 대수를 이룬다.

### 행렬 대수

[C\* 대수](../Page/C*_대수.md "wikilink") \(A\) 및 [자연수](../Page/자연수.md "wikilink") \(n\in\mathbb N\)에 대하여, [행렬](../Page/행렬.md "wikilink") 대수 \(\operatorname{Mat}(n;A)\)는 \(A\) 성분의 \(n\times n\) [정사각 행렬들로](https://ko.wikipedia.org/wiki/정사각_행렬 "wikilink") 구성되며, 이 역시 C\* 대수를 이룬다. 만약 어떤 [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") \(V\)에 대하여 \(A\subseteq\operatorname B(V,V)\)라면, \(\operatorname{Mat}(n;A)\subseteq\operatorname B(V^{\oplus n},V^{\oplus n})\)으로 여길 수 있다.

만약 \(n=0\)일 경우, 이는 [자명환](https://ko.wikipedia.org/wiki/자명환 "wikilink")이다.

## 성질

### C\* 대수 사이의 사상

다음이 주어졌다고 하자.

  - (항등원을 갖는) 두 C\* 대수 \(A\), \(B\)
  - (항등원을 보존하는) [복소수 대합 대수](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") 준동형 \(f\colon A\to B\). 즉, \(f\)는 [복소수 선형 변환이자](https://ko.wikipedia.org/wiki/복소수_선형_변환 "wikilink") [환 준동형이며](https://ko.wikipedia.org/wiki/환_준동형 "wikilink"), 대합 연산을 보존한다 (\(f(a^*)=f(a)^*\;\forall a\in A\)).

그렇다면, \(f\)는 [작용소 노름이](../Page/작용소_노름.md "wikilink") 1 이하인 [유계 작용소이다](https://ko.wikipedia.org/wiki/유계_작용소 "wikilink").

<div class="mw-collapsible mw-collapsed toccolours">

**증명:**

<div class="mw-collapsible-content">

임의의 \(a\in A\)에 대하여, C\* 항등식에 따라

\[\|a\|_A^2=\|a^*a\|_A\] 이다. \(a^*a\)는 음이 아닌 원소이므로, 그 노름은 [스펙트럼 반지름과](../Page/스펙트럼_반지름.md "wikilink") 같다.

\[\|a^*a|_A=\operatorname{sp\,rad}_A(a^*a)\] \(A\)의 [가역원](../Page/가역원.md "wikilink")의 [상은](../Page/상_\(수학\).md "wikilink") \(B\)의 [가역원](../Page/가역원.md "wikilink")이므로 다음이 성립한다.

\[\operatorname{sp}_A(a^*a)\supseteq \operatorname{sp}_B(f(a^*a))\] 여기서 \(\operatorname{sp}(-)\)는 [스펙트럼이다](../Page/스펙트럼_\(함수해석학\).md "wikilink"). 특히

\[\operatorname{sp\,rad}_A(a^*a)\ge\operatorname{sp\,rad}_B(f(a^*a))\] 이다. 이에 따라

\[\|f(a)\|_B^2=\|f(a^*a)\|_B=\operatorname{sp\,rad}_B(f(a^*a))\le \operatorname{sp\,rad}_A(a^*a)=\|a^*a\|_A=\|a\|_A^2\] 이며, 즉 \(\|f\|\le1\)이다.

</div>

</div>

또한, 만약 \(f\)가 추가로 [단사 함수라면](../Page/단사_함수.md "wikilink"), 이는 [등거리 변환이다](https://ko.wikipedia.org/wiki/등거리_변환 "wikilink"). 즉, \(\|a\|_A=\|f(a)\|_B\;\forall a\in A\)이다.

이에 따라, C\* 대수와 [복소수 대합 대수](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") 준동형들은 [구체적 범주](../Page/구체적_범주.md "wikilink") \(\operatorname{C*Alg}\)를 이룬다.

### 스펙트럼

C\* 대수의 원소의 [스펙트럼은](../Page/스펙트럼_\(함수해석학\).md "wikilink") 항상 [공집합](../Page/공집합.md "wikilink")이 아니다. 또한, 임의의 C\* 대수 \(A\)의 원소 \(a\in A\)에 대하여

\[\operatorname{sp}(a^*)=\{\bar\lambda\colon\lambda\in\operatorname{sp}(a)\}\] 이다.

C\* 대수의 [자기 수반 원소의](https://ko.wikipedia.org/wiki/자기_수반_원소 "wikilink") [스펙트럼은](../Page/스펙트럼_\(함수해석학\).md "wikilink") 실수의 부분 집합이다. C\* 대수의 [유니터리 원소의](https://ko.wikipedia.org/wiki/유니터리_원소 "wikilink") 스펙트럼은 \(\{z\in\mathbb C\colon|z|=1\}\)의 부분 집합이다.

## 분류

모든 C\* 대수는 겔판트-나이마르크 정리에 의하여 어떤 [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") 속의 [유계 작용소](https://ko.wikipedia.org/wiki/유계_작용소 "wikilink") C\* 대수의 부분 대수로 나타내어진다. 특히, 이 C\* 대수를 포함하는 최소의 [폰 노이만 대수를](../Page/폰_노이만_대수.md "wikilink") 정의할 수 있으며, 원래 C\* 대수는 이 [폰 노이만 대수의](../Page/폰_노이만_대수.md "wikilink") 강한 [연산자 위상에서의](https://ko.wikipedia.org/wiki/연산자_위상 "wikilink") [조밀 집합을](../Page/조밀_집합.md "wikilink") 이룬다. [폰 노이만 대수의](../Page/폰_노이만_대수.md "wikilink") 경우 자세한 구조 이론이 알려져 있다.

## 예

### 자명한 C\* 대수

[한원소 집합](../Page/한원소_집합.md "wikilink") \(\{\bullet\}\) 위의 유일한 환 구조인 [자명환](https://ko.wikipedia.org/wiki/자명환 "wikilink")은 C\* 대수를 이룬다. 이는 유일한 0차원 C\* 대수이다.

### 유한 차원 C\* 대수

임의의 유한 차원 C\* 대수 \(A\)는 다음과 같은 꼴이다.

\[A=\bigoplus_{i\in I}\operatorname{Mat}(n,n;\mathbb C)\] 여기서 \(\operatorname{Mat}(n,n;\mathbb C)\)는 [작용소 노름이](../Page/작용소_노름.md "wikilink") 부여된, \(n\times n\) 복소수 [정사각 행렬들의](https://ko.wikipedia.org/wiki/정사각_행렬 "wikilink") C\* 대수이다.

### 가환 C\* 대수

(항등원을 갖는) 가환 C\* 대수 \(A\)의 **스펙트럼**()은 다음과 같은 집합이다. (이 개념은 C\* 대수의 원소의 [스펙트럼의](../Page/스펙트럼_\(함수해석학\).md "wikilink") 개념과 관계가 없다.)

\[\hat A=\hom(A,\mathbb C)\subseteq A^*\] 즉, \(A\to\mathbb C\) \*-준동형들의 집합이다. \*-준동형의 [작용소 노름은](../Page/작용소_노름.md "wikilink") 1 이하이므로,

\[\hat A\subseteq\operatorname{cl}\left(\operatorname{ball}_{A^*}(0,1)\right)\] 이다. (여기서 우변은 [연속 쌍대 공간](../Page/연속_쌍대_공간.md "wikilink") \(A^*\)의 [닫힌](https://ko.wikipedia.org/wiki/닫힌집합 "wikilink") 단위 공이다.) 우변에 [약한-\* 위상을](https://ko.wikipedia.org/wiki/약한-*_위상 "wikilink") 주고, 좌변을 그 부분 공간으로 간주하면, [바나흐-앨러오글루 정리에](https://ko.wikipedia.org/wiki/바나흐-앨러오글루_정리 "wikilink") 의하여 \(\hat A\)는 [콤팩트](../Page/콤팩트_공간.md "wikilink") [하우스도르프 공간을](../Page/하우스도르프_공간.md "wikilink") 이룬다. 이 연산은 [함자](../Page/함자_\(수학\).md "wikilink")

\[\hat{\color{White}{A}}\colon\operatorname{comC*Alg}\to\operatorname{CompHausTop}^{\operatorname{op}}\] 를 정의한다. 여기서

  - [정의역](https://ko.wikipedia.org/wiki/정의역 "wikilink")은 (항등원을 갖는) [가환](../Page/가환환.md "wikilink") C\* 대수와, \*-준동형들의 [구체적 범주이다](../Page/구체적_범주.md "wikilink").
  - [공역은](../Page/공역_\(수학\).md "wikilink") [콤팩트](../Page/콤팩트_공간.md "wikilink") [하우스도르프 공간과](../Page/하우스도르프_공간.md "wikilink") [연속 함수들의](../Page/연속_함수.md "wikilink") [구체적 범주의](../Page/구체적_범주.md "wikilink") [반대 범주이다](https://ko.wikipedia.org/wiki/반대_범주 "wikilink").

반대로, 다음과 같은 [함자](../Page/함자_\(수학\).md "wikilink")

\[\mathcal C^0(X,-)\colon\operatorname{CompHausTop}^{\operatorname{op}}\to\operatorname{comC^*Alg}\] 를 정의할 수 있다.

  - 임의의 [콤팩트](../Page/콤팩트_공간.md "wikilink") [하우스도르프 공간](../Page/하우스도르프_공간.md "wikilink") \(X\)에 대하여, \(\mathcal C^0(-,\mathbb C)\)는 복소수 값 [연속 함수들의](../Page/연속_함수.md "wikilink") 공간이다. 이 위에 ∞-[르베그 노름](../Page/르베그_공간.md "wikilink") \(\|f\|_\infty=\sup_{x\in X}|f|\) 및 점별 덧셈 · 곱셈 · 복소수 켤레를 부여하면, 이는 가환 C\* 대수를 이룬다.
  - 임의의 두 [콤팩트](../Page/콤팩트_공간.md "wikilink") [하우스도르프 공간](../Page/하우스도르프_공간.md "wikilink") \(X\), \(Y\) 사이의 [연속 함수](../Page/연속_함수.md "wikilink") \(f\colon X\to Y\)의 \(\mathcal C^0(-,\mathbb C)\)에 대한 [상은](../Page/상_\(수학\).md "wikilink") 다음과 같다.
    \[\mathcal C^0(f,\mathbb C)\colon\mathcal C^0(Y,\mathbb C)\to\mathcal C^0(X,\mathbb C)\]
    \[\mathcal C^0(f,\mathbb C)\colon\phi\mapsto\phi\circ f\]

**겔판트 표현 정리**(Гельфанд表現定理, )에 따르면, \(\mathcal C^0(-,\mathbb C)\)와 \(\hat{\color{White}{A}}\) 함자는 사실 두 [범주](../Page/범주_\(수학\).md "wikilink") \(\operatorname{comC*Alg}\)와 \(\operatorname{CompHausTop}^{\operatorname{op}}\) 사이의 [범주의 동치를](../Page/범주의_동치.md "wikilink") 정의한다.

특히, 모든 (항등원을 갖는) [가환](../Page/가환환.md "wikilink") C\* 대수 \(A\)에 대하여

\[A\cong\mathcal C^0(\hat A,\mathbb C)\] 이며, 모든 (항등원을 갖는) [가환](../Page/가환환.md "wikilink") C\* 대수 \(A\)는 위와 같은 꼴로 (유일하게) 표현된다.

### 유계 작용소 대수

임의의 [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") \(V\) 위의 모든 [유계 작용소들의](https://ko.wikipedia.org/wiki/유계_작용소 "wikilink") 집합 \(\operatorname B(V,V)\)은 [함수의 합성을](../Page/함수의_합성.md "wikilink") 곱셈으로 삼을 때 C\* 대수를 이룬다. (이는 특히 I종 [인자 대수이다](../Page/인자_대수.md "wikilink").) 특히, 만약 \(V=\mathbb C^n\)가 유한 차원이라면, 이는 \(n\times n\) [복소수 행렬들로](https://ko.wikipedia.org/wiki/복소수_행렬 "wikilink") 구성된다.

### 콤팩트 작용소 대수

임의의 [복소수 힐베르트 공간](https://ko.wikipedia.org/wiki/복소수_힐베르트_공간 "wikilink") \(V\) 위의 모든 [콤팩트 작용소들의](../Page/콤팩트_작용소.md "wikilink") 집합 \(\operatorname K(V,V)\)은 \(\operatorname B(V,V)\)의 [닫힌](https://ko.wikipedia.org/wiki/닫힌집합 "wikilink") [양쪽 아이디얼을](https://ko.wikipedia.org/wiki/양쪽_아이디얼 "wikilink") 이루며, 이에 대한 [몫환](https://ko.wikipedia.org/wiki/몫환 "wikilink")

\[\frac{\operatorname B(V,V)}{\operatorname K(V,V)}\] 은 C\* 대수를 이룬다. 이를 **콜킨 대수**()라고 한다.

## 응용

C\* 대수의 이론은 [양자장론](../Page/양자장론.md "wikilink")을 수학적으로 엄밀하게 정의하려는 시도에 사용된다.

겔판트 표현에 의하여, 가환 C\* 대수는 콤팩트 하우스도르프 공간에 대응되며, 만약 항등원을 가져야 하는 조건을 생략한다면, 이는 [국소 콤팩트](https://ko.wikipedia.org/wiki/국소_콤팩트 "wikilink") [하우스도르프 공간에](../Page/하우스도르프_공간.md "wikilink") 대응된다. 이에 대하여, 일반적 (비가환일 수 있는) C\* 대수 역시 일종의 ‘공간’으로 여길 수 있다. 이러한 수학적 분야를 [비가환 기하학이라고](../Page/비가환_기하학.md "wikilink") 한다.

## 참고 문헌

  -
  -
  -
  -
  -
## 외부 링크

  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
[분류:연산자 이론](https://ko.wikipedia.org/wiki/분류:연산자_이론 "wikilink") [분류:대수](https://ko.wikipedia.org/wiki/분류:대수 "wikilink")