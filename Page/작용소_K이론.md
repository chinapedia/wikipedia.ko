> This article is converted from Wikipedia: [작용소 K이론](https://ko.wikipedia.org/wiki/작용소_K이론).


수학에서, **작용소 K이론**(作用素K異論, )는 [C\* 대수에](../Page/C*_대수.md "wikilink") 대응되는 [K이론](../Page/K이론.md "wikilink")이다. 주기 2의 보트 주기성을 가지며, 가환 [C\* 대수의](../Page/C*_대수.md "wikilink") 경우 [겔판트 표현 정리에](https://ko.wikipedia.org/wiki/겔판트_표현_정리 "wikilink") 의하여 이는 [위상 K이론과](../Page/위상_K이론.md "wikilink") 일치한다.

## 정의

### 사영원

(항등원을 갖는) [복소수 대합 대수](https://ko.wikipedia.org/wiki/복소수_대합_대수 "wikilink") \(A\)의 원소 \(a\in A\)가 만약 \(a^2=a^*=a\)를 만족시킨다면, \(a\)를 **사영원**()이라고 한다. 사영원의 집합을 \(\operatorname P(A)\)로 표기하자.

원소 \(a\in A\)에 대하여, 만약 \(a^*a\in\operatorname P(A)\)라면, \(a\)를 **부분 등거리원**()이라고 한다. 만약 \(a\)가 부분 등거리원이라면, \(a^*\) 역시 부분 등거리원이다. 부분 등거리원들의 집합을 \(\operatorname{PI}(A)\)로 표기하자.

\(\operatorname P(A)\) 위에 다음과 같은 [동치 관계를](https://ko.wikipedia.org/wiki/동치_관계 "wikilink") 정의할 수 있다.

\[a\sim b\iff \exists c\in\operatorname{PI}(A)\colon a=c^*c,\; b=cc^*\]

### 무한 행렬 공간

(항등원을 갖는) [C\* 대수](../Page/C*_대수.md "wikilink") \(A\)가 주어졌다고 하자. 그렇다면, \(A\)성분의 \(n\times n\) [정사각 행렬들의](https://ko.wikipedia.org/wiki/정사각_행렬 "wikilink") [C\* 대수](../Page/C*_대수.md "wikilink") \(\operatorname{Mat}(n;A)\)를 정의할 수 있다. \(n\times n\) 행렬에 모든 성분이 0인 \(n+1\)번째 행 및 열을 추가하는 사상을

\[\iota_n\colon\operatorname{Mat}(n;A)\to\operatorname{Mat}(n+1;A)\] 라고 하면, 이들을 통해 다음과 같은 [귀납적 극한을](../Page/귀납적_극한.md "wikilink") 취할 수 있다.

\[\operatorname{Mat}(\infty;A)=\lim_{n\to\infty}\operatorname{Mat}(n;A)\] 이는 그러나 항등원을 갖지 않아 [환이](../Page/환_\(수학\).md "wikilink") 아니다. \(\operatorname{Mat}(\infty;A)\) 위에 이항 연산

\[M\oplus N=\begin{pmatrix}
M&0_{m\times n}\\
0_{n\times m}&N
\end{pmatrix}\qquad(M\in\operatorname{Mat}(m;A),\;N\in\operatorname{Mat}(n;A))\] 을 정의하자.

\(\operatorname{Mat}(\infty;A)\) 위에 다음과 같은 [동치 관계를](https://ko.wikipedia.org/wiki/동치_관계 "wikilink") 정의하자.

\[M\sim N\iff\exists P\in\operatorname{Mat}(m,n;A)\colon M=PP^*,\;N=P^*P\qquad(M\in\operatorname{Mat}(m;A),\;N\in\operatorname{Mat}(n;A))\] 그렇다면, \(\operatorname{Mat}(\infty;A)/\sim\)는 [가환 모노이드를](https://ko.wikipedia.org/wiki/가환_모노이드 "wikilink") 이룬다. 이를 \(\operatorname D(A)\)로 표기하자. \(\operatorname D(A)\)의 [그로텐디크 군을](../Page/그로텐디크_군.md "wikilink") \(A\)의 **0차 K군**이라고 하며, \(\operatorname K_0(A)\)로 표기한다.

### K<sub>1</sub>

마찬가지로, \(A\)계수의 [일반 선형군](https://ko.wikipedia.org/wiki/일반_선형군 "wikilink")

\[\operatorname{GL}(n;A)=\operatorname{Unit}\left(\operatorname{Mat}(n;A)\right)\] 및

\[\operatorname{GL}(\infty;A)=\lim_{n\to\infty}\operatorname{GL}(n;A)\] 를 정의하자. (\(\operatorname{GL}(\infty;A)\)는 항등원을 갖지 않아 사실 [군이](../Page/군_\(수학\).md "wikilink") 아니다.) 이 경우, \(A\)의 **\(i\)차 K군**은 다음과 같다.

\[\operatorname K_i(A)=\pi_{i-1}(\operatorname{GL}(\infty;A))\qquad(i\ge1)\]

## 성질

보트 주기성에 따라

\[\operatorname K_{i+2}(A)=\operatorname K_i(A)\] 이다.

## 예

1차원 [C\* 대수](../Page/C*_대수.md "wikilink") \(\mathbb C\)를 생각하자. \(\operatorname K_0(\mathbb C)\)는 다음과 같다.

\[\operatorname D(\mathbb C)\cong\mathbb N\]

\[\operatorname K_0(\mathbb C)\cong\mathbb Z\] 구체적으로,

\[n\mapsto[1_{n\times n}]\qquad(n\in\mathbb N)\] 이다. 이는 복소수 [정사각 행렬](https://ko.wikipedia.org/wiki/정사각_행렬 "wikilink") \(M\in\operatorname{Mat}(n;\mathbb C)\) 가운데 \(M^2=1\)이라면

\[M=\operatorname{diag}(e_1,e_2,\dotsc,e_n)\]

\[e_1,\dotsc,e_n\in\{0,1\}\] 의 꼴이기 때문이다.

## 참고 문헌

  -
  -
  -
## 외부 링크

  -
  -
  -
  -
[분류:K이론](https://ko.wikipedia.org/wiki/분류:K이론 "wikilink") [분류:연산자 이론](https://ko.wikipedia.org/wiki/분류:연산자_이론 "wikilink")