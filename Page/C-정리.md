> This article is converted from Wikipedia: [C-](https://ko.wikipedia.org/wiki/C-).


[양자장론](../Page/양자장론.md "wikilink")에서, **c-정리**(c-定理, )는 2차원 [양자장론](../Page/양자장론.md "wikilink")들의 공간 위에서, 양자장론의 [자유도](https://ko.wikipedia.org/wiki/자유도 "wikilink")의 수를 나타내고, [재규격화군](../Page/재규격화군.md "wikilink") 흐름에 따라서 단조적으로 감소하는 함수 *c*가 존재한다는 정리다. 이는 재규격화군에 따라 높은 에너지의 물리가 잊혀지므로 그에 따라 자유도가 감소하는 것으로 해석할 수 있다. [재규격화군](../Page/재규격화군.md "wikilink")의 고정점에서, *c*는 [등각 장론의](../Page/등각_장론.md "wikilink") [비라소로 대수의](../Page/비라소로_대수.md "wikilink") 중심 전하가 된다.

## 정의

2차원 공간 위에서, 복소 좌표 \(z=x+iy\)를 사용하자. 2차원에서 [에너지-운동량 텐서는](../Page/에너지-운동량_텐서.md "wikilink") 대칭성에 의해 세 개의 독립된 성분을 가지는데, 이를 각각

\[T_{zz}(z,\bar z)=T(z,\bar z)\]

\[\bar T_{zz}(z,\bar z)=\bar T(z,\bar z)\]

\[T_{z\bar z}(z,\bar z)=\Theta(z,\bar z)\] 로 적자. [등각 장론의](../Page/등각_장론.md "wikilink") 경우 후자는 0이 된다.

양자장론은 일련의 [결합 상수](../Page/결합_상수.md "wikilink") \(g^i\in\mathcal G\) 및 [재규격화](../Page/재규격화.md "wikilink") 에너지 눈금 \(\Lambda\in\mathbb R^+\)에 의존하는 국소 라그랑지언 밀도 \(\mathcal L(g,\Lambda,z,\bar z)\)에 의해 정의된다. 양자장론이 [재규격화](../Page/재규격화.md "wikilink") 가능하다는 것은 다음 세 조건들을 의미한다.

  - **유동 결합 상수** \(\hat g\colon\mathbb R^+\to\mathcal G\)가 존재하여, 모든 \(\alpha\in\mathbb R^+\)에 대하여

\[\mathcal L(\hat g(\mu),\Lambda)=\mathcal L(\hat g(\alpha\mu),\alpha\Lambda)\]

  -
    가 성립한다.

<!-- end list -->

  - 유동 결합 상수는 자율적 1차 [상미분 방정식을](https://ko.wikipedia.org/wiki/상미분_방정식 "wikilink") 따른다. 즉, **베타 함수** \(\beta^i\in\Gamma(T\mathcal G)\)가 존재하여,

\[\frac{d\hat g(\mu)}{d\ln\mu}=\beta^i(\hat g(\mu))\]

  -
    이어야 한다.

<!-- end list -->

  - [에너지-운동량 텐서의](../Page/에너지-운동량_텐서.md "wikilink") 대각합 \(\Theta(z,\bar z)\)는 다음과 같다.

\[\Theta(g;z,\bar z)=
\frac d{d\ln\mu}\mathcal L(\hat g(g_0,\mu),\Lambda;z,\bar z)
=\beta^i\frac{\partial\mathcal L(g,\Lambda;z,\bar z)}{\partial g^i}\]

***c*-정리**에 따르면, 모든 재규격화 가능한 2차원 양자장론에 대하여 다음과 같은 함수 \(c\colon\mathcal G\to[0,\infty)\)가 존재한다.

  - (단조성) \(c(\hat g(\mu))\)는 \(\mu\)에 대한 증가함수이다.
  - (고정점에서의 등각 대칭) [재규격화군](../Page/재규격화군.md "wikilink")의 고정점 (\(\beta^i\)의 영점) \(g_0\in\mathcal G\)에서, 이론은 2차원 [비라소로 대수를](../Page/비라소로_대수.md "wikilink") 대칭으로 가진다. (즉, 단순한 축척 대칭 말고도, 모든 2차원 [등각 대칭에](../Page/등각_대칭.md "wikilink") 대하여 불변이다.)
  - (등각 중심 전하와의 일치) 재규격화군의 고정점 \(g_0\)에서, \(c(g_0)\)는 이에 대응하는 2차원 [등각 장론의](../Page/등각_장론.md "wikilink") [비라소로 대수의](../Page/비라소로_대수.md "wikilink") 중심 전하 *c*와 일치한다.

## *c*의 정의

다음과 같은 값들을 정의하자.

\[C(g)=2z^4\langle T(z_0,\bar z_0)T(0)\rangle\]

\[H(g)=z^3\bar z\left\langle T(z_0,\bar z_0)\Theta(0,0)\right\rangle\]

\[G(g)=z^2\bar z^2\left\langle\Theta(z_0,\bar z_0)\Theta(0,0)\right\rangle\] 이들은 모두 어떤 임의의 주어진 에너지 눈금 \(\Lambda_0=\sqrt{z_0\bar z_0}\)에서 정의된다. 정의에 따라 이들은 모두 차원이 0인 로런츠 스칼라이다. 또한,

\[G(g)=\beta^i(g)\beta^j(g)G_{ij}(g)\] 라고 놓으면, \(G_{ij}\)는 [양의 정부호인](https://ko.wikipedia.org/wiki/양의_정부호 "wikilink") 대칭 행렬이다. 이 구조에 따라서 \((\mathcal G,G_{ij})\)는 [리만 다양체를](../Page/리만_다양체.md "wikilink") 이루며, 또한 항상 \(G(g)=\beta(g)^2\ge 0\)이 된다.

그렇다면 \(c\colon\mathcal G\to\mathbb R\)는 다음과 같다.

\[c(g;\Lambda_0)=C(g;\Lambda_0)+4H(g;\Lambda_0)-6G(g;\Lambda_0)\] 이 경우, [캘런-쥐만치크 방정식에](https://ko.wikipedia.org/wiki/캘런-쥐만치크_방정식 "wikilink") 따라서

\[\frac d{d\ln\mu}c(\hat g(\mu))=12G(g)>0\] 이 된다.

## 역사

[존 카디는](../Page/존_카디.md "wikilink") 중심 원소 *c*가 계의 [자유도](https://ko.wikipedia.org/wiki/자유도 "wikilink")의 수를 나타내는 것을 보였다. 이후, [알렉산드르 자몰롯치코프가](../Page/알렉산드르_자몰롯치코프.md "wikilink") 1986년 〈2차원 장론의 [재규격화군](../Page/재규격화군.md "wikilink")의 "비가역성"〉이라는 제목의 논문\[1\]\[2\] 에서 c-정리를 증명하였다.\[3\]\[4\]

## 고차원에서의 c-정리

*c*-정리는 2차원의 경우에는 증명되었으나, 아직 고차원에서 성립하는지 알려지지 않았고, 특수한 경우에는 고차원에서의 반례도 발견되었다. 짝수 차원의 시공간에서, [존 카디는](../Page/존_카디.md "wikilink") *c*에 해당하는 값을 정의하였고,\[5\], 이는 *a*라고 불리게 되었다.\[6\] 카디는 *a*가 [재규격화군](../Page/재규격화군.md "wikilink") 흐름에 따라 항상 감소한다는 가설을 세웠다. 이를 ***a*-정리**()라고 한다. 4차원의 경우, *a*-정리는 2011년에 증명되었다.\[7\]\[8\]\[9\] 6차원의 경우는 아직 증명되지 않았다.\[10\]

2010년에는 3차원 등각 장론에 대하여 *F*라는 값이 정의되었다.\[11\]\[12\] 이는 3차원에서 *c* 또는 *a*에 대응하는 값으로 추측된다.

2010년에는 [홀로그래피 원리를](../Page/홀로그래피_원리.md "wikilink") 사용하여, 임의의 차원에서의 *c*-정리들이 제안되었다.\[13\] 이는 3차원에서 이미 정의된 *F*와 일치한다는 사실이 증명되었다.\[14\]

## 참고 문헌

## 외부 링크

  -
[분류:등각 장론](https://ko.wikipedia.org/wiki/분류:등각_장론 "wikilink") [분류:수리물리학](https://ko.wikipedia.org/wiki/분류:수리물리학 "wikilink") [분류:수리물리학 정리](https://ko.wikipedia.org/wiki/분류:수리물리학_정리 "wikilink") [분류:양자장론](https://ko.wikipedia.org/wiki/분류:양자장론 "wikilink")

1.
2.
3.
4.
5.
6.  [Renormalisation group flows in four dimensions and the ‘*a*-theorem’](http://www-thphys.physics.ox.ac.uk/people/JohnCardy/seminars/oxford2012.pdf)
7.
8.
9.
10.
11.
12.
13.
14.