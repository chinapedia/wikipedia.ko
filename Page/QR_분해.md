> This article is converted from Wikipedia: [QR ](https://ko.wikipedia.org/wiki/QR_).


[선형대수학](https://ko.wikipedia.org/wiki/선형대수학 "wikilink")에서, **QR 분해**()는 [실수](https://ko.wikipedia.org/wiki/실수 "wikilink") [행렬](https://ko.wikipedia.org/wiki/행렬 "wikilink")을 [직교 행렬과](https://ko.wikipedia.org/wiki/직교_행렬 "wikilink") [상삼각 행렬의](https://ko.wikipedia.org/wiki/상삼각_행렬 "wikilink") 곱으로 나타내는 [행렬 분해이다](../Page/행렬_분해.md "wikilink").\[1\] [그람-슈미트 과정이나](../Page/그람-슈미트_과정.md "wikilink") [하우스홀더 행렬이나](https://ko.wikipedia.org/wiki/하우스홀더_행렬 "wikilink") [기븐스 회전을](../Page/기븐스_회전.md "wikilink") 통해 얻을 수 있으며, [선형 최소 제곱법이나](https://ko.wikipedia.org/wiki/선형_최소_제곱법 "wikilink") [QR 알고리즘에서](https://ko.wikipedia.org/wiki/QR_알고리즘 "wikilink") 쓰인다.

## 정의

실수체 또는 복소수체 \(\mathbb K\) 성분의 \(m\times n\) (\(m\ge n\)) 행렬 \(A\)는 다음과 같이 분해할 수 있으며, 이를 \(A\)의 **QR 분해**라고 한다.

\[A=QR\] 여기서

  - \(Q\)는 \(\mathbb K\) 성분의 \(m\times n\) [유니터리 행렬이다](../Page/유니터리_행렬.md "wikilink").
  - \(R\)는 \(\mathbb K\) 성분의 \(n\times n\) [상삼각 행렬이다](https://ko.wikipedia.org/wiki/상삼각_행렬 "wikilink").

몇 가지 특수한 경우는 다음과 같다.

  - \(\mathbb K=\mathbb R\)일 경우, \(Q\)는 [직교 행렬이](https://ko.wikipedia.org/wiki/직교_행렬 "wikilink") 된다.
  - \(A\)가 [가역 행렬일](https://ko.wikipedia.org/wiki/가역_행렬 "wikilink") 경우, \(Q\)의 열들은 항상 \(A\)의 열공간의 [정규 직교 기저를](https://ko.wikipedia.org/wiki/내적_공간#정규_직교_기저 "wikilink") 이룬다. 또한 \(R\)의 모든 대각 원소가 양수인 QR 분해는 유일하다.

## 방법

### 그람-슈미트 과정

벡터 \(\mathbf{a}_1,\mathbf{a}_2,\cdots,\mathbf{a}_n\in\mathbb{R}^m\)이 [일차독립](https://ko.wikipedia.org/wiki/일차독립 "wikilink")이라 하자. 행렬 \(A = [\begin{array}{llll}\mathbf{a}_1 &\mathbf{a}_2 &\cdots &\mathbf{a}_n\end{array}]\) 에 대해, 그람-슈미트 직교정규화를 사용하면

\[\mathrm{proj}_{\mathbf{e}}\mathbf{a} = \frac{\left\langle\mathbf{e},\mathbf{a}\right\rangle}{\left\langle\mathbf{e},\mathbf{e}\right\rangle}\mathbf{e}\] 인 [사영](https://ko.wikipedia.org/wiki/사영 "wikilink") 연산자를 이용해서

\[\mathbf{u}_i = \mathbf{a}_i - \sum_{j=1}^{i-1} \mathrm{proj}_{\mathbf{u}_j} \mathbf{a}_i\]

\[\mathbf{e}_i = \frac {\mathbf{u}_i} {\|\mathbf{u}_i\|}\] 와 같이 직교정규기저 \(\{\mathbf{e}_1, \mathbf{e}_2, \cdots, \mathbf{e}_n\}\)를 얻을 수 있다.

\[{\langle \cdot,\cdot \rangle}\]은 [내적](../Page/내적_공간.md "wikilink") \(,\;\;  {\|{ }\|}\)는 [노름](https://ko.wikipedia.org/wiki/노름 "wikilink") 위 식을 다시 정리하면

\[\mathbf{a}_i = \sum_{j=1}^{i} \langle \mathbf{e}_j, \mathbf{a}_i \rangle \mathbf{e}_j\] 가 되므로,

\[Q = [\begin{array}{llll}\mathbf{e}_1& \mathbf{e}_2& \cdots& \mathbf{e}_n\end{array}]\]

\[R = \begin{pmatrix} \langle\mathbf{e}_1,\mathbf{a}_1\rangle & \langle\mathbf{e}_1,\mathbf{a}_2\rangle & \langle\mathbf{e}_1,\mathbf{a}_3\rangle & \ldots \\0 & \langle\mathbf{e}_2,\mathbf{a}_2\rangle & \langle\mathbf{e}_2,\mathbf{a}_3\rangle & \ldots \\0&0& \langle\mathbf{e}_3,\mathbf{a}_3\rangle & \ldots \\ \vdots&\vdots&\vdots&\ddots\end{pmatrix}\] 와 같이 놓으면 \(A = QR\)이 성립한다.

#### 예

\[A =
\begin{pmatrix}
12 & -51 & 4 \\
6 & 167 & -68 \\
-4 & 24 & -41
\end{pmatrix}\]

정규 [직교 행렬](https://ko.wikipedia.org/wiki/직교_행렬 "wikilink") \(Q\) 는 \(Q^T \,Q = I\)의 성질을 갖고있고,

따라서, \(Q\)는 다음과 같이 그람-슈미트 절차를 따라서,

\[U =
\begin{pmatrix}
 u_1 & u_2 &  u_3
\end{pmatrix}
=
\begin{pmatrix}
12 & -69 & -58/5 \\
6  & 158 & 6/5 \\
-4 &  30 & -33
\end{pmatrix}\]

\[Q =
\begin{pmatrix}
{{ u_1}\over{\| u_1\|}} &
{{ u_2}\over{\| u_2\|} }&
{{ u_3}\over{\| u_3\|}}
\end{pmatrix}
=
\begin{pmatrix}
     12/14    &    -69/175   &   -58/\left(5\times35\right)   \\
     6/14    &    158/175   &     6/\left(5\times35\right)   \\
    -4/14    &      30/175    &   -33/\left(1\times35\right)
\end{pmatrix}
=
\begin{pmatrix}
     6/7    &    -69/175   &   -58/175   \\
     3/7    &    158/175   &     6/175   \\
    -2/7    &      6/35    &   -33/35
\end{pmatrix}\] 그리고,

\[Q^{T} A = Q^{T}Q\,R = R\]

\[R = Q^{T}A =

\begin{pmatrix}
    14  &  21          &            -14 \\
     0  & 175          &           -70 \\
     0  &   0          &           35
\end{pmatrix}\] 확인해보면,

\[A= QR\]이므로,

\[\begin{pmatrix}
     6/7    &    -69/175   &   -58/175   \\
     3/7    &    158/175   &     6/175   \\
    -2/7    &      6/35    &   -33/35
\end{pmatrix}
\cdot
\begin{pmatrix}
    14  &  21          &            -14 \\
     0  & 175          &           -70 \\
     0  &   0          &           35
\end{pmatrix}=
\begin{pmatrix}
12 & -51 & 4 \\
6 & 167 & -68 \\
-4 & 24 & -41
\end{pmatrix}\]

\[QR=A\]이다.

\[QR\]분해 된다. 그러나,

[분수](https://ko.wikipedia.org/wiki/분수 "wikilink")에의한 [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink")연산이 관계함으로 오차가 발생할 수 있다.

#### RQ 분해와의 관계

\(RQ\) 분해는 행렬 \(A\) 를 [상삼각행렬](https://ko.wikipedia.org/wiki/상삼각행렬 "wikilink")\(R\) (직각 삼각형이라고도 함) 및 직교 행렬\(Q\) 의 곱으로 변환한다. \(QR\)분해와의 유일한 차이점은 행렬의 순서이다.

\(QR\)분해는 첫 번째 열에서 시작된 \(A\) 행렬의 열의 그람-슈미트 직교화이다.

\(RQ\) 분해는 마지막 행에서 시작하는 \(A\) 행렬의 행의 그람-슈미트 직교화이다.

#### 장점과 단점

그람-슈미트 프로세스는 본질적으로 수치적으로 불안정할 수 있다. 투영법의 적용에는 직교화에 대한 주요한 기하학적 유추가 있지만 직교화 자체는 수치 오류가 발생하기 쉽다. 그러나 구현의 용이함이 중요한 장점이다. 사전 작성된 선형 대수 라이브러리(library)를 사용할 수 없거나 용이하지 않은 경우, 이 알고리즘을 프로토타입(prototype)에 사용할 수있는 유용한 알고리즘으로 적용할 수 있다.

### 하우스홀더 방법

[하우스홀더 리플렉터](../Page/하우스홀더_변환.md "wikilink")(하우스홀더 변환,Householder reflection)를 이용하여 한 열씩을 [상삼각행렬](https://ko.wikipedia.org/wiki/상삼각행렬 "wikilink")로 바꾸어감으로써 \(Q\)와\(R\)을 구할 수 있다. 이 방법은 \(Q\)행렬을 하우스홀더 행렬의 곱으로 구해주기 때문에, 직접 \(Q\)를 구할 필요가 없을 때 유용하다. 또, 그람-슈미트 방법과는 달리, [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink") 연산에서도 오차가 누적되지 않기 때문에, 실제로 더 많이 활용된다.

#### 예

  -
    <math>A = \\begin{pmatrix}

12 & -51 & 4 \\\\ 6 & 167 & -68 \\\\ -4 & 24 & -41 \\end{pmatrix}</math>

먼저 행렬 \(A\) 의 첫 번째 열을 벡터로 변환하는 리플렉션을 찾아야한다.

\[\|{a}_1\| \;{e}_1 = (14, 0, 0)^T\]에서,

  -
    벡터 \({a}_1 = (12, 6, -4)^T\)

<!-- end list -->

  -
    \({u} = {x} - \alpha{e}_1\)

<!-- end list -->

  -
    \({v} = {{u}\over\|{u}\|}\)
      -
        \(\alpha = 14\)
        \({x} = {a}_1 = (12, 6, -4)^T\)
    따라서,
      -
        \({u} = (-2, 6, -4)^T=({2})(-1, 3, -2)^T\)
        \({v} = {{(-1, 3, -2)^T} \over {\sqrt{14}} }\)

[하우스홀더 행렬](https://ko.wikipedia.org/wiki/하우스홀더_행렬 "wikilink") \(Q = I - 2{{{v v^T}}\over{1}}\) 에서,

\[Q_1 = I - 2{{\begin{pmatrix} -1 \\ 3 \\ -2 \end{pmatrix}} \over \sqrt{14} }{{\begin{pmatrix} -1 & 3 & -2 \end{pmatrix}} \over \sqrt{14} }\]

\[Q_1 = I - {2 \over \sqrt{14} \sqrt{14}} \begin{pmatrix} -1 \\ 3 \\ -2 \end{pmatrix}\begin{pmatrix} -1 & 3 & -2 \end{pmatrix}\]

\[= I - {1 \over 7}\begin{pmatrix}
1 & -3  & 2 \\
-3 & 9 & -6 \\
2  & -6  & 4
\end{pmatrix}\]

\[= \begin{pmatrix}
6/7 & 3/7   &  -2/7 \\
3/7  &-2/7  &  6/7 \\
-2/7 & 6/7  &   3/7 \\
\end{pmatrix}.\]

확인해보면,

\[Q_1A = \begin{pmatrix}
14 & 21 & -14 \\
0 & -49 & -14 \\
0 & 168 & -77 \end{pmatrix}\] 삼각행렬에 접근하고 있음을 알수있다. \(3\)행\(2\)열에서 \((3, 2)\)의 성분 값을 \(0\)으로 만들면 [상삼각행렬](https://ko.wikipedia.org/wiki/상삼각행렬 "wikilink")을 얻게 된다.

\((1, 1)\) [소행렬식](../Page/소행렬식.md "wikilink")에서 다시 위의 절차를 반복해보면,

\[A' = M_{11} = \begin{pmatrix}
-49 & -14 \\
168 & -77 \end{pmatrix}\] 위와 같은 방법으로 하우스홀더 변환(Householder transformation)된 행렬을 얻고,

\[Q_2 = \begin{pmatrix}
1 & 0 & 0 \\
0 & -7/25 & 24/25 \\
0 & 24/25 & 7/25 \end{pmatrix}\]

\[Q_1 , Q_2\]에서 각각 [전치행렬](https://ko.wikipedia.org/wiki/전치행렬 "wikilink")을 수행한 후 프로세스가 올바르게 작동하는지 확인해보고, \(Q_1 = Q_1^T ,  Q_2 = Q_2^T\) 그리고나서,

\[Q=Q_1^T Q_2^T=\begin{pmatrix}
6/7 & -69/175 & 58/175 \\
3/7 & 158/175 & -6/175 \\
-2/7 & 6/35 & 33/35 \end{pmatrix}\] 그리고,

\[Q=Q_1^T Q_2^T=\begin{pmatrix}
0.8571 & -0.3943 & 0.3314 \\
0.4286 &  0.9029 & -0.0343 \\
-0.2857 & 0.1714 & 0.9429 \end{pmatrix}\]

\[R=Q_2Q_1A=Q^T A=\begin{pmatrix}
14 & 21 & -14 \\
0 & 175 & -70 \\
0 & 0 & -35 \end{pmatrix}\] 행렬 \(Q\) 는 [직교행렬](../Page/직교행렬.md "wikilink")이고 \(R\) 은 [상삼각행렬](https://ko.wikipedia.org/wiki/상삼각행렬 "wikilink")이되고 \(QR=A\)로 \(QR\) 분해된다.

### 기븐스 회전

[기븐스 행렬은](../Page/기븐스_행렬.md "wikilink") 특정위치에서 성분값을 \(0\) 으로 조작할 수 있는 방법으로 [기븐스 회전을](../Page/기븐스_회전.md "wikilink") 제공한다.

이것은 임의의 행렬을 [직교행렬](../Page/직교행렬.md "wikilink")과 특정위치의 성분값이 \(0\) 인 [상삼각행렬](https://ko.wikipedia.org/wiki/상삼각행렬 "wikilink")로 분해되게 유도할 수 있게된다.

#### 예

  -
    <math>A = \\begin{pmatrix}

a_{11} & a_{12} & a_{13} \\\\ a_{21} & a_{22} & a_{23}\\\\ a_{31} & a_{32} & a_{33}

`\end{pmatrix}`</math>

  -
    <math>A = \\begin{pmatrix}

12 & -51 & 4 \\\\ 6 & 167 & -68 \\\\ -4 & 24 & -41 \\end{pmatrix}</math>

\[\mathbf{a}_{31} = -4\]

\[G_1 , (12,-4)\]

\[\theta = \arctan\left({-(-4) \over 12}\right)\]

\[G_1 = \begin{pmatrix}
\cos(\theta) & 0 & -\sin(\theta) \\
0 & 1 & 0 \\
\sin(\theta) & 0  & \cos(\theta)
\end{pmatrix}\]

\[= \begin{pmatrix}
0.94868... & 0 & -0.31622... \\
0 & 1 & 0 \\
0.31622... & 0 & 0.94868...
\end{pmatrix}\]

\[G_1 \cdot A\] 는 \(\mathbf{a}_{31} =0\)으로 조작된다.

\[G_1A = \begin{pmatrix}
12.64911... & -55.97231... & 16.76007... \\
6 & 167 & -68 \\
0 & 6.64078... & -37.6311...
\end{pmatrix}\]

\(G_2\) 그리고 \(G_3\) 도 이러한 절차를 반복한다.

\[a_{21}=0\] 그리고 \(a_{32}=0\)으로 조작된다. 결과로 상삼각행렬\(R\)을 얻는다. 따라서,

\[G_3 \cdot G_2 \cdot G_1=Q^T\]

\[G_3G_2G_1A= Q^TA = R\]

\[\left( Q^T \right)^T = Q\] 직교행렬에서,

\[Q^T = Q^{-1}, Q Q^T = Q^T Q = I\] 그리고, \(QR=A\)이다.

\[A=QR\]로 분해된다.

## 같이 보기

  - [LU 분해](../Page/LU_분해.md "wikilink")
  - [특잇값 분해](https://ko.wikipedia.org/wiki/특잇값_분해 "wikilink")

## 각주

## 참고 문헌

  -
[분류:행렬 분해](https://ko.wikipedia.org/wiki/분류:행렬_분해 "wikilink") [분류:수치선형대수학](https://ko.wikipedia.org/wiki/분류:수치선형대수학 "wikilink")

1.