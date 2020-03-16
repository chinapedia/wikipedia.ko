> This article is converted from Wikipedia: [L-](https://ko.wikipedia.org/wiki/L-).


[수학](../Page/수학.md "wikilink")에서, **L<sub>∞</sub>-대수**() 또는 **호모토피 리 대수**()는 \(\mathbb Z\) 등급을 갖는 대수이다.\[1\]\[2\]\[3\] [리 대수의](../Page/리_대수.md "wikilink") 개념에서, [야코비 항등식이](https://ko.wikipedia.org/wiki/야코비_항등식 "wikilink") 오직 호모토피에 대하여 성립하도록 약화시킨 것이다.

## 정의

### 괄호를 통한 정의

[표수 0의](https://ko.wikipedia.org/wiki/표수_0 "wikilink") 체 \(K\)가 주어졌다고 하자. \(K\) 위의 [초벡터 공간](https://ko.wikipedia.org/wiki/초벡터_공간 "wikilink") \(V=V_+\oplus V_-\)이 주어졌을 때, 다음을 정의하자.

\[\bigwedge V =
\frac{\operatorname T(V)}{\mathfrak I}\] 여기서 \(\mathfrak I\) 는 [텐서 대수](../Page/텐서_대수.md "wikilink") \(\operatorname T(V)\)의, 다음 부분 집합으로 생성되는 [아이디얼](../Page/아이디얼.md "wikilink")이다.

\[\mathfrak I = \left(v_1\otimes v_2\otimes\dotsb\otimes v_n - (-)^\sigma(-)^{\sigma,\vec v} v_{\sigma(1)}\otimes v_{\sigma(2)}\otimes\dotsb\otimes v_{\sigma(n)} \colon \sigma \in\operatorname{Sym}(n),\;v_1,\dotsc,v_n \in V_+ \cup V_- \right)\] 여기서

  - \((-)^\sigma\in\{\pm1\}\)는 순열의 부호수, 즉 [군 준동형](https://ko.wikipedia.org/wiki/군_준동형 "wikilink") \(\operatorname{Sym}(n) \to \operatorname{Sym}(2)\)에 대한 [상이다](../Page/상_\(수학\).md "wikilink").
  - \((-)^{\sigma,\vec v}\in\{\pm1\}\)는 \(\sigma\)가 \((v_1,\dotsc,v_n)\)에 [작용할](../Page/군의_작용.md "wikilink") 때, \(V_-\)에 속하는 두 원소를 교환할 때의 수가 짝수인 경우 \(+1\), 홀수일 경우 \(-1\)이다.

물론 \(\textstyle\bigwedge V\)는 자연수 등급을 갖는다.

\(K\) 위의 **L<sub>∞</sub>-대수** \(A\)는 다음과 같은 일련의 연산이 주어진, \(K\) 위의 \(\mathbb Z\)-[등급 벡터 공간](https://ko.wikipedia.org/wiki/등급_벡터_공간 "wikilink")

\[A=\bigoplus_{i\in\mathbb Z}A^i\] 이다.

  - 각 \(n\ge1\)에 대하여, 등급 반대칭 \(n\)항 연산 \([-,-,\dotsc,-]\colon \textstyle\bigwedge^n V \to K\). 그 등급은 \(n-2\)이다. (즉, 2항 괄호의 등급이 0이며, 1항 괄호는 등급 −1의 미분을 이룬다.)
    \[\deg[a_1,\dotsc,a_n]_n = n -2 + \sum_{i=1}^n\deg a_i\]

이는 다음과 같은 [야코비 항등식을](https://ko.wikipedia.org/wiki/야코비_항등식 "wikilink") 만족시켜야 한다.

\[0=\sum_{i+j=n+1}\sum_{\sigma\in\operatorname{Sh}(i,n-i)} e(\sigma)(-1)^{\sigma+i(j-1)}[[a_{\sigma(1)},\dots,a_{\sigma(i)}]_i,a_{\sigma(i+1)},\dots,a_{\sigma(n)}]_j\] 여기서

  - \(\operatorname{Sh}(i,n-i)\)는 \((i,n-i)\)-[셔플 순열의](../Page/셔플_순열.md "wikilink") 집합이다.
  - \(e(\sigma)\)는 순열 \(\sigma\)가 홀수 등급을 갖는 원소쌍을 서로 짝수 번 뒤바꾸었을 때 \(+1\), 홀수 번 뒤바꾸었을 때 \(-1\)이다. 이를 **코쥘 부호**()라고 한다.

### 미분 등급 대수를 통한 정의

만약 각 등급별 차원이 유한하다면, L<sub>∞</sub>-대수는 다음과 같이 정의될 수도 있다.

[표수 0의](https://ko.wikipedia.org/wiki/표수_0 "wikilink") [체](../Page/체_\(수학\).md "wikilink") \(K\) 위의 위의 **호모토피 리 대수**는 다음과 같은 데이터로 주어진다.

  - \(K\) 위의 양의 정수 [등급 벡터 공간](https://ko.wikipedia.org/wiki/등급_벡터_공간 "wikilink") \(A=\textstyle\bigoplus_{i\in\mathbb Z^+}A_i\). 이로부터 다음을 정의할 수 있다.
      - \(A^*\)는 \(A\)의 [대수적 쌍대 공간이다](https://ko.wikipedia.org/wiki/대수적_쌍대_공간 "wikilink").
      - \(\operatorname{Sym}(A^*)\)은 등급 벡터 공간 \(A^*\) 위의 대칭 대수이며, 이는 [자연수](../Page/자연수.md "wikilink") [등급 대수를](../Page/등급_대수.md "wikilink") 이룬다.
  - \(\mathrm d \colon \operatorname{Sym}(V^*)\to\operatorname{Sym}(V^*)\)는 \(\operatorname{Sym}(V^*)\) 위의, 등급 +1의 [연속](../Page/연속_함수.md "wikilink") [미분이다](https://ko.wikipedia.org/wiki/미분_\(대수학\) "wikilink"). 즉, 다음 조건들을 만족시킨다.
      - \(\mathrm d\)는 \(K\)-[선형 변환이다](https://ko.wikipedia.org/wiki/선형_변환 "wikilink").
      - \(\mathrm d\circ \mathrm d = 0\)
      - \(\mathrm d(ab) = (\mathrm da)b + (-)^{\deg a} a\mathrm db\)이다. 여기서 \(a\)는 동차 성분이다.
      - \(\deg(\mathrm da) = 1+\deg a\). 여기서 \(a\)는 동차 성분이다.

이는 다음 조건을 추가로 만족시켜야 한다.

  - 표준 사영 \((\operatorname{Sym}(V^*),\mathrm d) \to (K,0)\)는 [미분 등급 대수의](../Page/미분_등급_대수.md "wikilink") [준동형](../Page/준동형.md "wikilink")이다.

(만약 이 조건을 생략한다면, 굽은 L<sub>∞</sub>-대수의 개념을 얻는다.)

### 두 정의 사이의 관계

이 두 정의 사이의 관계는 다음과 같다. 우선, 괄호 \([-,-,\dotsc,-]_\bullet\)를 통한 정의에서, \(A\)의 임의의 기저

\[A = \operatorname{Span}_K\{t_i\}_{i\in I}\] 를 잡자. 그 쌍대 기저는

\[A^* = \operatorname{Span}_K\{t^i\}_{i\in I}\] 이며, 또한

\[\deg t^i = \deg t_i + 1\] 로 놓자. 그렇다면,

\[\mathrm d \colon t^i \mapsto -\sum_{n=0}^\infty \frac1{n!}t^i([t_{i_1},\dotsc,t_{i_n}]_n) t^{i_1}  t^{i_2} \dotsm t^{i_n}\] 이다. 이 경우, 멱영 조건

\[\mathrm d^2 = 0\] 을 전개하고 등급별로 분해하면, 괄호에 대한 조건들과 동치임을 알 수 있다.

## 예

### 미분 등급 리 대수

L<sub>∞</sub>-대수 \(\mathfrak g\)에서, 만약 오직 2항 이하 괄호만이 0이 아닌 경우, 이는 [미분 등급 리 대수를](../Page/미분_등급_리_대수.md "wikilink") 이룬다. 즉, 이 경우

\[[a]_1 = \mathrm da\]

\[[a,b]_2 = [a,b]\]

\[[a,b,\dotsc,]_k = 0\qquad(k\ge3)\] 로 놓으면, \((\mathfrak g,\mathrm d,[-,-])\)가 만족시켜야 하는 항등식들은 [미분 등급 리 대수의](../Page/미분_등급_리_대수.md "wikilink") 정의와 일치한다. 즉, 3항 이상의 괄호들이 모두 0이라면, 2항 괄호의 [야코비 항등식이](https://ko.wikipedia.org/wiki/야코비_항등식 "wikilink") 정확히 성립한다.

특히, 만약 추가로 \([-]_1 = \mathrm d = 0\)일 경우, 이는 등급 [리 초대수를](../Page/리_초대수.md "wikilink") 이루며, 만약 모든 등급이 짝수라면 이는 등급 [리 대수를](../Page/리_대수.md "wikilink") 이룬다.

### 리 \(n\)-대수

L<sub>∞</sub>-대수에서, 모든 생성원의 등급이 \(\{0,1,\dotsc,n\}\)에 속하는 경우를 **리 \(n\)-대수**라고 한다. 이 경우,

\[n \ge \deg [a_1,\dotsc,a_k]_k \ge k-2\] 이므로,

\[[-,\dotsc,-]_k = 0 \qquad(k> n+2)\] 이다.

예를 들어, \(n=1\)일 경우, 오직 1항 · 2항 · 3항 연산만이 자명하지 않다.

특히, \(n=0\)인 경우, 1항 연산 또한 등급에 의하여 0이 되므로, 이 개념은 [리 대수의](../Page/리_대수.md "wikilink") 개념과 [동치](../Page/동치.md "wikilink")이다.

### 거스틴해버 대수

모든 [거스틴해버 대수는](../Page/거스틴해버_대수.md "wikilink") L<sub>∞</sub>-대수를 이룬다.

## 참고 문헌

## 외부 링크

  -
  -
[분류:대수 구조](https://ko.wikipedia.org/wiki/분류:대수_구조 "wikilink") [분류:호모토피 이론](https://ko.wikipedia.org/wiki/분류:호모토피_이론 "wikilink")

1.
2.
3.