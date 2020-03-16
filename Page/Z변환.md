> This article is converted from Wikipedia: [Z](https://ko.wikipedia.org/wiki/Z).


**Z 변환**(Z-transform)은 [수학](../Page/수학.md "wikilink")이나 [신호 처리에서](https://ko.wikipedia.org/wiki/신호_처리 "wikilink") [실 수열](../Page/수열.md "wikilink") 또는 [복소 수열로](https://ko.wikipedia.org/wiki/복소_수열 "wikilink") 나타나는 시간 영역의 신호를 복소 [주파수 영역의](../Page/주파수_영역.md "wikilink") 표현으로 변환한다.

Z 변환은 연속 시간 신호에 대한 [라플라스 변환에](../Page/라플라스_변환.md "wikilink") 대응하는 이산 시간 영역에서의 변환으로 볼 수 있다.

## 역사

Z 변환에 대한 기본적인 생각은 [라플라스](https://ko.wikipedia.org/wiki/라플라스 "wikilink")도 알고 있었고, 1947년에 [W. Hurewicz에](https://ko.wikipedia.org/wiki/wikipedia:Witold_Hurewicz "wikilink") 의해 선형 상수 계수 [차분 방정식을](../Page/점화식.md "wikilink") 푸는 유용한 수단으로 다시 알려졌다.\[1\] Z 변환이라는 이름은 1952년에 [콜롬비아 대학의](https://ko.wikipedia.org/wiki/콜롬비아_대학 "wikilink") sampled-data control group에 속한 [Ragazzini와](https://ko.wikipedia.org/wiki/wikipedia:John_R._Ragazzini "wikilink") [Zadeh로](https://ko.wikipedia.org/wiki/wikipedia:Lotfi_A._Zadeh "wikilink") 부터 유래되었다.\[2\]\[3\]

[고등 Z 변환은](https://ko.wikipedia.org/wiki/wikipedia:Advanced_Z-transform "wikilink") 후에 [Jury에](https://ko.wikipedia.org/wiki/wikipedia:Eliahu_I._Jury "wikilink") 의해 개발되고 대중화 되었다.

## 정의

다른 [적분 변환들과](../Page/적분_변환.md "wikilink") 마찬가지로 Z 변환은 단방향 또는 양방향 변환으로 정의될 수 있다.

### 양방향 Z 변환

연속시간 신호 \(x[n]\)의 양방향 Z 변환은 \(X(z)\)로 표현되는 [formal power series로](https://ko.wikipedia.org/wiki/wikipedia:formal_power_series "wikilink"), 다음과 같이 정의된다.

\[X(z) = \mathcal{Z}\{x[n]\} = \sum_{n=-\infty}^{\infty} x[n] z^{-n}.\]

여기서 \(n\)은 정수이고 \(z\)는 일반적으로 [복소수](../Page/복소수.md "wikilink")이다. 즉, \(z\)는 [복소수의 크기](../Page/절댓값.md "wikilink") \(A\)와 [허수 단위](../Page/허수_단위.md "wikilink") \(j\), 그리고 [편각](https://ko.wikipedia.org/wiki/wikipedia:Complex_argument "wikilink") \(\phi\)를 통해 다음과 같이 표현할 수 있다.

\[z = A e^{j\phi} = A(\cos{\phi}+j\sin{\phi})\,\]

### 단방향 Z 변환

만약 \(x[n]\)이 \(n \ge 0\)에 대해서만 정의되어 있다면 단방향 Z 변환은 다음과 같이 정의된다.

\[X(z) = \mathcal{Z}\{x[n]\} = \sum_{n=0}^{\infty} x[n] z^{-n}.\]

이러한 정의는 [신호 처리에서](https://ko.wikipedia.org/wiki/신호_처리 "wikilink") [이산 시간](https://ko.wikipedia.org/wiki/wikipedia:Discrete_time "wikilink") [causal system의](https://ko.wikipedia.org/wiki/wikipedia:Causal_system "wikilink") [단위 펄스 응답의](https://ko.wikipedia.org/wiki/wikipedia:Finite_impulse_response "wikilink") Z 변환을 구하는데 사용될 수 있다. 여기서부터는 별도의 언급이 없는 한 단방향 Z 변환을 고려하기로 한다.

#### 예제

  - [단위 계단 신호](../Page/단위_계단_함수.md "wikilink")

다음과 같은 신호를 생각해 보자.

\[x[n] = 1,\quad n = 0,1,2,\ldots.\]

그러면 \(x[n]\)의 Z 변환은 다음과 같이 구해진다.

\[X(z) = 1 + z^{-1} + z^{-2} + \cdots = \frac{z}{z - 1},\quad 1<|z|.\]

  - [등비수열](../Page/등비수열.md "wikilink")

다음과 같은 신호를 생각해 보자.

\[x[n] = a^{n},\quad n = 0,1,2,\ldots.\]

그러면 \(x[n]\)의 Z 변환은 다음과 같이 구해진다.

\[X(z) = 1 + (z/a)^{-1} + (z/a)^{-2} + \cdots = \frac{z}{z - a},\quad a<|z|.\]

## 성질

### 선형성 (Linearity)

두 이산 시간 신호 \(x_{1}[n]\), \(x_{2}[n]\)의 Z 변환을 각각 \(X_{1}(z)\), \(X_{2}(z)\)라 두면, 상수 \(a_{1}\), \(a_{2}\)에 대해 \(x[n] = a_{1}x_{1}[n] + a_{2}x_{2}[n]\)의 Z 변환은 다음과 같다

\[\begin{align}
X(z) &= \sum_{n=-\infty}^{\infty} (a_1x_1[n]+a_2x_2[n])z^{-n} \\
 &= a_1\sum_{n=-\infty}^{\infty} x_1[n]z^{-n} + a_2\sum_{n=-\infty}^{\infty}x_2[n]z^{-n} \\
 &= a_1X_1(z) + a_2X_2(z).
\end{align}\]

### 시간에 대한 평행 이동 (Time shifting)

#### 양방향 Z 변환의 경우

이산 시간 신호 \(x[n]\)의 Z 변환을 \(Z\{x[n]\}\)라 두면 정수 \(k\)에 대해 \(x[n-k]\)의 Z 변환은 다음과 같다.

\[\begin{align}
\mathcal{Z}\{x[n-k]\} &= \sum_{n=-\infty}^{\infty} x[n-k]z^{-n}\\
&= \sum_{m=-\infty}^{\infty} x[m]z^{-(m+k)},\quad m = n-k \\
&= \sum_{m=-\infty}^{\infty} x[m]z^{-m}z^{-k} \\
&= z^{-k}\sum_{m=-\infty}^{\infty}x[m]z^{-m}\\
&= z^{-k}X(z).
\end{align}\]

#### 단방향 Z 변환의 경우

단방향 Z 변환의 경우 조금 다르다. 만약 \(k \ge 1\)인 경우

\[\begin{align}
\mathcal{Z}\{x[n-k]\} &= \sum_{n=0}^{\infty} x[n-k]z^{-n}\\
&= \sum_{m=-k}^{\infty} x[m]z^{-(m+k)},\quad m = n-k \\
&= \sum_{m=-k}^{\infty} x[m]z^{-m}z^{-k} \\
&= \sum_{m=-k}^{-1} x[m]z^{-m}z^{-k} + z^{-k}\sum_{m=0}^{\infty} x[m]z^{-m} \\
&= \sum_{m=-k}^{-1} x[m]z^{-(m+k)} + z^{-k}X(z),
\end{align}\]

\(k \le -1\)인 경우

\[\begin{align}
\mathcal{Z}\{x[n-k]\} &= \sum_{n=0}^{\infty} x[n-k]z^{-n}\\
&= \sum_{m=-k}^{\infty} x[m]z^{-(m+k)},\quad m = n-k \\
&= \sum_{m=-k}^{\infty} x[m]z^{-m}z^{-k} \\
&= -\sum_{m=0}^{-k-1} x[m]z^{-m}z^{-k} + z^{-k}\sum_{m=0}^{\infty} x[m]z^{-m} \\
&= -\sum_{m=0}^{-k-1} x[m]z^{-(m+k)} + z^{-k}X(z).
\end{align}\]

## Z 역변환

Z 역변환은 다음과 같이 구해진다.

\[x[n] = \mathcal{Z}^{-1} \{X(z) \}= \frac{1}{2 \pi j} \oint_{C} X(z) z^{n-1} dz,\]

여기서 \(C\)는 원점을 반시계방향으로 둘러 싸면서 [수렴 반경](https://ko.wikipedia.org/wiki/wikipedia:Radius_of_convergence "wikilink") 안에 있는 닫힌 경로이다.

하지만 [라플라스 역변환의](../Page/라플라스_변환.md "wikilink") 경우와 유사하게 대부분의 경우 Z 역변환은 [부분분수](../Page/부분분수.md "wikilink") 분해를 통해 구해진다. 예를 들어 다음과 같은 Z 변환을 생각하자.

\[X(z) = \frac{3z^{2} - 7z}{z^{2} - 5z + 6}.\]

[부분분수](../Page/부분분수.md "wikilink") 분해를 통해 \(X(z)/z\)는 다음과 같이 표현된다.

\[\frac{X(z)}{z} = \frac{1}{z-2} + \frac{2}{z-3}.\]

따라서, \(X(z) = z/(z-2) + 2z/(z-3)\)이고 Z 변환의 선형성으로부터 \(x[n]\)은 다음과 같이 구해진다.

\[x[n] = 2^{n} + 2 \cdot 3^{n},\quad n = 0,1,\ldots.\]

## 수렴 반경

## 응용

### 차분방정식의 풀이

다음과 같이 주어진 상수 계수를 갖는 선형 [차분방정식을](../Page/점화식.md "wikilink") 생각하자.

\[x[n-2] - 5x[n-1] + 6x[n] = 0,\quad x[-1] = 1,\; x[-2] = 0.\]

양변에 Z 변환을 취하면 다음을 얻는다.

\[\begin{align}
&z^{-2}X(z) + x[-2] + z^{-1}x[-1] - 5z^{-1}X(z) - 5x[-1] + 6X(z) = 0,\\
&\frac{X(z)}{z} = \frac{5z-1}{(3z-1)(2z-1)},\\
&X(z) = -\frac{2}{3}\frac{z}{z - \frac{1}{3}} + \frac{3}{2}\frac{z}{z - \frac{1}{2}}.
\end{align}\]

따라서, \(x[n] = -\frac{2}{3} \left(\frac{1}{3}\right)^{n} + \frac{3}{2} \left(\frac{1}{2}\right)^{n}\)이다.

## Z 변환 표

## 각주

## 같이 보기

  - [라플라스 변환](../Page/라플라스_변환.md "wikilink")
  - [푸리에 변환](../Page/푸리에_변환.md "wikilink")
  - [이산 시간 푸리에 변환](https://ko.wikipedia.org/wiki/:en:Discrete-time_Fourier_transform "wikilink")
  - [이산 푸리에 변환](https://ko.wikipedia.org/wiki/이산_푸리에_변환 "wikilink")

<!-- end list -->

1.  Kamen, E.; Heck, B. (2000), *Fundamentals of Signals and Systems: With MATLAB Examples* (2nd ed.); Prentice Hall; , 9780130172938.
2.  Ingle, V. K.; Proakis, J. G. (2007), *Digital Signal Processing Using Matlab* (2nd ed., Int. Stud. Ed.); Thomson.
3.  Nekoogar, F. and Moriarty, G. (1999), *Digital control using digital signal processing*; Prentice Hall.

[분류:해석학 (수학)](https://ko.wikipedia.org/wiki/분류:해석학_\(수학\) "wikilink") [분류:신호 처리](https://ko.wikipedia.org/wiki/분류:신호_처리 "wikilink")

1.
2.
3.