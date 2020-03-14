> This article is converted from Wikipedia: [XY ](https://ko.wikipedia.org/wiki/XY_).


[통계역학](https://ko.wikipedia.org/wiki/통계역학 "wikilink")에서, **XY 모형**(XY模型, ) 또는 **고전 회전자 모형**()은 주기적인 스칼라 보손을 나타내는 [격자 모형이다](https://ko.wikipedia.org/wiki/격자_모형 "wikilink"). **코스털리츠-사울리스 전이**(-轉移, )를 비롯한 여러 흥미로운 현상을 보인다.

## 정의

\(D\)차원의 격자 \(\Lambda\)위의 **XY 모형**은 다음과 같은 자유도 및 [해밀토니언으로](https://ko.wikipedia.org/wiki/해밀토니언_\(양자역학\) "wikilink") 정의되는 통계역학 모형이다.

  - 각 격자점 \(i\in\Lambda\)에 대하여, 자유도는 각도 \(\theta_i\in\operatorname U(1)\}\)이다.
  - 해밀토니언은 다음과 같다. 여기서 \(J\) 및 \(h_i\)는 임의의 상수이다. \(J\)는 스핀, \(h_i\)는 외부 자기장으로 해석할 수 있다.
    \[H=-J\sum_{\langle ij\rangle}\cos(\theta_i-\theta_j)-\sum_ih_i\cos\theta_i\]

위 식에서, \(\textstyle\sum_{\langle ij\rangle}\)은 격자에서 서로 이웃한 격자점의 쌍에 대한 합을 뜻한다. \(J>0\)인 경우는 [강자성](https://ko.wikipedia.org/wiki/강자성 "wikilink"), \(J<0\)인 경우는 [반강자성](https://ko.wikipedia.org/wiki/반강자성 "wikilink")에 해당한다.

## 성질

XY 모형의 성질은 차원 \(D\)에 따라 다르다.

### 1차원

외부 자기장이 없을 때, 1차원 XY 모형은 다음과 같이 정확히 풀 수 있다. 편의상 \(N+1\)개의 격자점 \(i=0,1,\dots,N\)이 존재하고, 양끝에는 경계 조건을 부여하지 않는다고 하자. 자유도를 다음과 같은 변수로 나타내자.

\[\phi_i=\theta_i-\theta_{i-1}\qquad(i=1,\dots,N)\] 그렇다면 해밀토니언은

\[H=-J\sum_{i=1}^N\cos\phi_i\] 이며, 그 [분배 함수는](https://ko.wikipedia.org/wiki/분배_함수_\(통계역학\) "wikilink") 다음과 같다.

\[Z(\beta J)=\left(\int_0^{2\pi}\exp(\beta J\cos\phi)\,d\phi\right)^N
=(2\pi I_0(\beta J))^N\] 여기서 \(I_0(x)\)는 제1종 [변형 베셀 함수이다](https://ko.wikipedia.org/wiki/변형_베셀_함수 "wikilink").

### 2차원

2차원 XY 모형은 **코스털리츠-사울리스 전이**()라는 [상전이](https://ko.wikipedia.org/wiki/상전이 "wikilink")를 보인다. 높은 온도에서는 스핀의 기댓값은 0이며, 스핀의 상관 함수는 긴 거리에서 지수적으로 0으로 수렴한다.

\[\lim_{\beta\to0}\langle\exp(i\theta)\rangle_\beta=0\]

\[\langle\exp(i\theta_i-\theta_j)\rangle_\beta
\sim \exp(-c(\beta)|i-j|)\qquad(\beta\ll1)\] 여기서 \(c(\beta)\)는 온도에 의존하는 상수이다.

[머민-바그너 정리로](../Page/머민-바그너_정리.md "wikilink") 인하여 2차원에는 [자발 대칭 깨짐이](https://ko.wikipedia.org/wiki/자발_대칭_깨짐 "wikilink") 부재하므로, 절대 영도에서도 스핀의 기댓값은 0이다. 그러나 스핀의 상관 함수는 낮은 온도에서 지수 법칙 대신 거듭제곱 법칙을 따른다.

\[\langle\exp(i\theta)\rangle_{\beta=\infty}=0\]

\[\langle\exp(i(\theta_i-\theta_j))\rangle_\beta
\sim |i+j|^{-\eta(\beta)}\] 여기서 \(\eta(\beta)\) 역시 온도에 의존하는 상수이다.

코스털리츠-사울리스 전이는 스핀의 상관 함수가 지수 법칙에서 거듭제곱 법칙으로 바뀌는 현상이다. 이는 높은 온도에서는 소용돌이()와 반소용돌이()가 자유롭게 존재할 수 있지만, 낮은 온도에서는 이들이 오직 소용돌이-반소용돌이 쌍으로서만 존재할 수 있기 때문이다. 코스털리츠-사울리스 임계 온도에서는 소용돌이들이 이와 같이 속박된다.

2차원 XY 모형의 저에너지 극한은 자유 주기 보손의 [2차원 등각 장론이다](https://ko.wikipedia.org/wiki/2차원_등각_장론 "wikilink").

### 3차원

3차원 XY 모형은 자유 아벨 [게이지 이론의](https://ko.wikipedia.org/wiki/게이지_이론 "wikilink") 격자화로 해석할 수 있다. 3차원에서 게이지장 \(F_{ij}\)는 한 개의 자유도를 가지며, 구체적으로 이는 쌍대화

\[4\pi g^2\partial_i\theta=\epsilon_{ijk}F_{jk}\] 를 통해 나타낼 수 있다. 이렇게 정의한 스칼라장 \(\theta\)는 게이지 변환에 의하여 주기적이며, 따라서 XY 모형의 각도로 해석할 수 있다.

낮은 온도에서는 [U(1)](https://ko.wikipedia.org/wiki/U\(1\) "wikilink") 게이지 대칭의 [자발 대칭 깨짐으로](https://ko.wikipedia.org/wiki/자발_대칭_깨짐 "wikilink") 인하여, 스핀이 기댓값을 갖는다.

\[\langle\exp(i\theta)\rangle_\beta\ne0\qquad(\beta\gg1)\] 따라서 가능한 바닥 상태들의 집합은 원 모양이다.

높은 온도에서는 게이지 대칭이 회복된다. 즉, 스핀의 기댓값은 0이며, 상관 함수는 지수적으로 감소한다.

\[\lim_{\beta\to0}\langle\exp(i\theta)\rangle_\beta=0\]

\[\langle\exp(i(\theta_i-\theta_j))\rangle_\beta
\sim \exp(-c(\beta)|i-j|)\qquad(\beta\ll1)\] 이 두 상 사이에서는 어떤 임계 온도 \(T_{\text{c}}\)에서 [상전이](https://ko.wikipedia.org/wiki/상전이 "wikilink")([자발 대칭 깨짐](https://ko.wikipedia.org/wiki/자발_대칭_깨짐 "wikilink"))가 발상한다.

3차원에서도 상전이는 [솔리톤](https://ko.wikipedia.org/wiki/솔리톤 "wikilink")과 관계있다. 고온 상에서는 여차원이 1인 소용돌이가 발생하며, 주기 스칼라장 \(\theta\)는 소용돌이 둘레에 자명하지 않은 [모노드로미](https://ko.wikipedia.org/wiki/모노드로미 "wikilink")를 갖는다. 반면, 저온 상에서는 소용돌이가 억제된다.

## 참고 문헌

  -
  -
  -
## 외부 링크

  -
  -
  -
## 같이 보기

  - [이징 모형](https://ko.wikipedia.org/wiki/이징_모형 "wikilink")
  - [포츠 모형](../Page/포츠_모형.md "wikilink")
  - [슈윙거 모형](../Page/슈윙거_모형.md "wikilink")

[분류:격자 모형](https://ko.wikipedia.org/wiki/분류:격자_모형 "wikilink")