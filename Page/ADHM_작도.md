> This article is converted from Wikipedia: [ADHM ](https://ko.wikipedia.org/wiki/ADHM_).


[수리물리학](https://ko.wikipedia.org/wiki/수리물리학 "wikilink")에서, **ADHM 작도**(ADHM作圖, )는 [선형대수학](https://ko.wikipedia.org/wiki/선형대수학 "wikilink")만을 사용하여 4차원 유클리드 공간의 [양-밀스 순간자들을](https://ko.wikipedia.org/wiki/양-밀스_순간자 "wikilink") 작도하는 방법이다.

## 전개

SO(4)=SU(2)<sub>L</sub>×SU(2)<sub>R</sub>이다. 편의상 바일 스피너 표기법을 사용하자. 즉, SU(2)<sub>L</sub>의 기본 표현 **2**의 지수는 \(\alpha,\beta,\dots=1,2\)로, SU(2)<sub>R</sub>의 기본 표현 **2**의 지수는 \(\dot\alpha,\dot\beta,\dots=1,2\)로 쓴다. 이렇게 하면, SO(4)의 기본 표현은 **4**=(**2**,**2**)이므로, 4차원 벡터의 지표는 \(a\dot a\)가 된다.

통상적으로,

\[\psi^{\dot\alpha}=\epsilon^{\dot\alpha\dot\beta}\psi_{\dot\beta}\]

\[\psi^{\alpha}=\epsilon^{\alpha\beta}\psi_\beta\] 이다.

### ADHM 데이터

SU(*N*) [양-밀스 이론에서](https://ko.wikipedia.org/wiki/양-밀스_이론 "wikilink"), 순간자수가 \(k\)인 상태를 작도한다고 하자. 그렇다면 **ADHM 작도**는 다음과 같은 데이터로 주어진다.

  - \(X_\mu\in\hom(\mathbb R^k,\mathbb R^k)\). 이는 \(X_{\alpha\dot\alpha}=\sigma^\mu_{\alpha\dot\alpha}X_\mu\)로 적을 수 있다.
  - \(W_{\dot\alpha}\in\hom(\mathbb C^N,\mathbb C^k)\). 이는 \(k\times N\) 복소 행렬로 나타낼 수 있다.

이 데이터는 다음 조건을 만족시켜야 한다. 이를 **ADHM 방정식**()이라고 한다.

\[W_{\dot\alpha}(W_{\dot\beta})^\dagger=iC\epsilon_{\dot\alpha\dot\beta}+i\epsilon^{\alpha\beta}X_{\alpha\dot\alpha}(X_{\beta\dot\beta})^\dagger\] 여기서 \(C\in\mathfrak{u}(k)\)는 임의의 \(k\times k\) [에르미트 행렬이다](https://ko.wikipedia.org/wiki/에르미트_행렬 "wikilink").

### 작도

이 데이터로, 순간자 \(A_\mu\)를 다음과 같이 작도할 수 있다.

시공간 좌표 \(x\in\mathbb R^4\)는 4차원 벡터이므로,

\[x_{\alpha\dot\alpha}=x_\mu \sigma^\mu_{\alpha\dot\alpha}\] 로 적을 수 있다. 여기서 \(\sigma^\mu\)는 [파울리 행렬이다](https://ko.wikipedia.org/wiki/파울리_행렬 "wikilink").

\(2k\times(N+2k)\) 복소행렬 \(\Delta\)를 다음과 같이 정의하자.

\[\Delta_{\dot\alpha}(x)=W_{\dot\alpha}\]

\[\Delta_{\alpha\dot\alpha}(x)=X_{\alpha\dot\alpha}+x_{\alpha\dot\alpha}\otimes I_{k\times k}\]

\[\Delta=\begin{pmatrix}
\Delta_{\dot 1}&\Delta_{1\dot 1}&\Delta_{2\dot 1}\\
\Delta_{\dot 2}&\Delta_{1\dot 2}&\Delta_{2\dot 2}
\end{pmatrix}\] 위 조건에 따라서, \(2k\times 2k\) 행렬 \(\Delta(x)\Delta^\dagger(x)\)는 다음과 같은 꼴이다.

\[\Delta(x)\Delta^\dagger(x)=\begin{pmatrix}F^{-1}(x)&0_{k\times k}\\0_{k\times k}&F^{-1}(x)\end{pmatrix}\] \(\Delta(x)\)는 \(\mathbb C^{N+2k}\)에 작용한다. [거의 모든](https://ko.wikipedia.org/wiki/거의_모든 "wikilink") \(x_{\alpha\dot\alpha}\)에 대하여, \(\ker\Delta(x)\)는 \(N\)차원이다. 따라서, \(\Delta\)의 규칙화 영 모드들을 \((2k+N)\times N\) 행렬 \(U(x)\)로 적자.

\[\Delta(x)U(x)=0\]

\[U^\dagger(x)U(x)=I_{N\times N}\] 그렇다면 [순간자](https://ko.wikipedia.org/wiki/순간자 "wikilink") [게이지 퍼텐셜](https://ko.wikipedia.org/wiki/게이지_퍼텐셜 "wikilink") \(A_\mu\)는 다음과 같다.

\[A_\mu=iU^\dagger(x)\frac{\partial}{\partial x^\mu}U(x)\]

### 모듈러스 공간의 차원

\(X_\mu\)는 \(4k^2\)개의 실수 매개변수, \(W_{\dot\alpha}\)는 \(4Nk\)개의 실수 매개변수를 기여한다. ADHM 방정식은 \(3k^2\)개의 제약을 가하고, 또한 임의의 \(M\in\operatorname{U}(k)\)에 대하여

\[W_{\dot\alpha}\to MW_{\dot\alpha}\]

\[X_{\alpha\dot\alpha}\mapsto MX_{\alpha\dot\alpha}M^{-1}\] 와 같이 회전을 가해도 같은 순간자를 얻으므로, 모듈러스 공간의 차원은 \(4Nk\)이다.

### 끈 이론에서의 해석

ADHM 작도는 [끈 이론으로](https://ko.wikipedia.org/wiki/끈_이론 "wikilink") 자연스럽게 해석할 수 있다.\[1\] 이 경우, *N*개의 겹친 [D3-막에](https://ko.wikipedia.org/wiki/D-막 "wikilink") 녹아 있는 *k*개의 [D(−1)-막들을](https://ko.wikipedia.org/wiki/D-막 "wikilink") 고려한다. 이 경우 D(−1)-막에 존재하는 \(\mathcal N=2\) (16개 초전하) [초대칭 게이지 이론을](https://ko.wikipedia.org/wiki/초대칭_게이지_이론 "wikilink") 고려한다. 이 게이지 이론은 쿨롱 상과 힉스 상 두 가지의 [상이](https://ko.wikipedia.org/wiki/상_\(물리학\) "wikilink") 존재한다.

  - 쿨롱 상에서는 D(−1)-막들이 D3-막에서 분리돼 각각 자유롭게 움직인다.
  - 힉스 상에서는 D(−1)-막들이 D3-막 속에 녹아, D3-막 위에 존재하는 [초대칭 게이지 이론의](https://ko.wikipedia.org/wiki/초대칭_게이지_이론 "wikilink") [순간자](https://ko.wikipedia.org/wiki/순간자 "wikilink")를 이룬다.

따라서, 다음과 같은 대응 관계를 얻는다.

| 기호                 | ADHM 작도           | 끈 이론 해석                                                                                 |
| ------------------ | ----------------- | --------------------------------------------------------------------------------------- |
| *N*                | 게이지 군 SU(*N*)의 계수 | 겹친 D3-막의 수                                                                              |
| *k*                | 순간자수              | D(−1)-막의 수                                                                              |
|                    | ADHM 방정식          | D(−1)-막 위에 존재하는 이론의 퍼텐셜의 D-항 및 F-항                                                      |
| \(W_{\dot\alpha}\) |                   | D3-막과 D(−1)-막을 잇는 [끈으로](https://ko.wikipedia.org/wiki/끈_\(물리학\) "wikilink") 발생하는 스칼라장   |
| \(X_\mu\)          |                   | D(−1)-막의 (비가환) 위치                                                                       |
|                    | 순간자 모듈러스 공간       | D(−1)-막 세계부피 이론의 힉스 가지 [모듈러스 공간](https://ko.wikipedia.org/wiki/모듈러스_\(물리학\) "wikilink") |

## 역사

[마이클 아티야](https://ko.wikipedia.org/wiki/마이클_아티야 "wikilink"), [블라디미르 드린펠트](https://ko.wikipedia.org/wiki/블라디미르_드린펠트 "wikilink"), [나이절 히친](../Page/나이절_히친.md "wikilink"), [유리 마닌이](https://ko.wikipedia.org/wiki/유리_마닌 "wikilink") 발표하였다.\[2\] 이름은 발견자들의 성의 머릿자를 딴 것이다.

## 참고 문헌

  -
  -
  -
## 외부 링크

  -
[분류:양자장론](https://ko.wikipedia.org/wiki/분류:양자장론 "wikilink") [분류:미분기하학](https://ko.wikipedia.org/wiki/분류:미분기하학 "wikilink") [분류:양자색역학](https://ko.wikipedia.org/wiki/분류:양자색역학 "wikilink")

1.
2.