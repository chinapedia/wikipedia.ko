> This article is converted from Wikipedia: [LU 분해](https://ko.wikipedia.org/wiki/LU_분해).


**LU 분해**()는 [수치 해석](https://ko.wikipedia.org/wiki/수치_해석 "wikilink") 분야에서 [하삼각행렬](https://ko.wikipedia.org/wiki/하삼각행렬 "wikilink")과 [상삼각행렬](https://ko.wikipedia.org/wiki/상삼각행렬 "wikilink")의 곱으로 표현하는 것이다. L과 U는 각각 Lower와 Upper를 의미한다. 때때로 [치환행렬](https://ko.wikipedia.org/wiki/치환행렬 "wikilink")(permutation matrix)도 함께 곱으로 나타내기도 한다. LU 분해는 [가우스 소거법에서](../Page/가우스_소거법.md "wikilink") 많이 이용된다. LU 분해는 [앨런 튜링에](../Page/앨런_튜링.md "wikilink") 의해 소개됐다.

일반적인 행렬 \(\, A \,\)를 예약한다면,

\[A = LU \,\]

\[L\] 은 [하삼각행렬](../Page/삼각행렬.md "wikilink")(lower triangular matrix)

\[U\] 는 [상삼각행렬](../Page/삼각행렬.md "wikilink")(upper triangular matrix)

## 분해의 예

  - \(3 \times 3 matrix\)

\[\begin{pmatrix}
           a_{11} & a_{12} & a_{13} \\
           a_{21} & a_{22} & a_{23} \\
           a_{31} & a_{32} & a_{33}
        \end{pmatrix} =
      \begin{pmatrix}
           l_{11} & 0 & 0 \\
           l_{21} & l_{22} & 0 \\
           l_{31} & l_{32} & l_{33}
        \end{pmatrix}
        \begin{pmatrix}
           u_{11} & u_{12} & u_{13} \\
           0 & u_{22} & u_{23} \\
           0 & 0 & u_{33}
        \end{pmatrix}\]

\[\begin{pmatrix}
           a_{11} & a_{12} & a_{13} \\
           a_{21} & a_{22} & a_{23} \\
           a_{31} & a_{32} & a_{33}
        \end{pmatrix}
       \begin{pmatrix}
           x_1  \\
           x_2  \\
           x_3
        \end{pmatrix} =

       \begin{pmatrix}
           y_1  \\
           y_2  \\
           y_3
        \end{pmatrix}\]

## 계산

  - \(2 \times 2 matrix\)

\[\begin{pmatrix}
           4 & 3 \\
           6 & 3
        \end{pmatrix} =
      \begin{pmatrix}
           l_{11} & 0 \\
           l_{21} & l_{22}
        \end{pmatrix}
        \begin{pmatrix}
           u_{11} & u_{12} \\
           0 & u_{22}
        \end{pmatrix}\]

\[l_{11} \cdot u_{11} + 0 \cdot 0 = 4\]

\[l_{11} \cdot u_{12} + 0 \cdot u_{22} = 3\]

\[l_{21}\cdot u_{11} + l_{22} \cdot 0 = 6\]

\[l_{21}\cdot u_{12} + l_{22} \cdot u_{22} = 3\]

[하부 삼각행렬](../Page/삼각행렬.md "wikilink") \(L\) 의 [주대각선](../Page/주대각선.md "wikilink")을 \(1\)로 놓음으로써,

\[l_{11} = 1\]

\[l_{22} = 1\] 다음을 얻을수있다.

\[l_{21} = 1.5\]

\[u_{11} = 4\]

\[u_{12} = 3\]

\[u_{22} = -1.5\] 따라서,

\[\begin{pmatrix}
           4 & 3 \\
           6 & 3
        \end{pmatrix} =
      \begin{pmatrix}
           1 & 0 \\
           1.5 & 1
        \end{pmatrix}
        \begin{pmatrix}
           4 & 3 \\
           0 & -1.5
        \end{pmatrix}\]

## \(LU\) 분해

[사다리꼴행렬](../Page/사다리꼴행렬.md "wikilink")을 이용한 \(LU\) 분해

\[I =   \begin{pmatrix}
   1 & 0 & 0  \\
   0 & 1 & 0  \\
   0 & 0 & 1
\end{pmatrix} ,
A=  \begin{pmatrix}
   2 & 1 & 1   \\
   4 & -6 & 0   \\
   -2 & 7 & 2
\end{pmatrix}\]

\[\begin{pmatrix}
   1 & 0 & 0  \\
   2 & 1 & 0  \\
   0 & 0 & 1
\end{pmatrix}
 \begin{pmatrix}
   2 & 1 & 1   \\
   0 & -8 & -2   \\
   -2 & 7 & 2
\end{pmatrix}\]

\[\begin{pmatrix}
   1 & 0 & 0  \\
   2 & 1 & 0  \\
   -1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
   2 & 1 & 1   \\
   0 & -8 & -2   \\
   0 & 8 & 3
\end{pmatrix}\]

\[\begin{pmatrix}
   1 & 0 & 0  \\
   2 & 1 & 0  \\
   -1 & -1 & 1
\end{pmatrix}
\begin{pmatrix}
   2 & 1 & 1  \\
   0 & -8 & -2  \\
   0 & 0 & 1
\end{pmatrix}\]

\[L=\begin{pmatrix}
   1 & 0 & 0  \\
   2 & 1 & 0  \\
   -1 & -1 & 1
\end{pmatrix}
U=\begin{pmatrix}
   2 & 1 & 1  \\
   0 & -8 & -2  \\
   0 & 0 & 1
\end{pmatrix}\]

\[LU = A\] 이다.

\[I =   \begin{pmatrix}
   1 & 0 & 0  \\
   0 & 1 & 0  \\
   0 & 0 & 1
\end{pmatrix} ,
A= \begin{pmatrix}
   -1 & 1 & 2  \\
   3 & -1 & 1  \\
   -1 & 3 & 4
\end{pmatrix}\]

\[\begin{pmatrix}
  1 & 0 & 0  \\
   3 & 1 & 0  \\
   0 & 0 & 1
\end{pmatrix}
   \begin{pmatrix}
    -1 & 1 & 2  \\
   0 & 2 & 7  \\
   -1 & 3 & 4
\end{pmatrix}\]

\[\begin{pmatrix}
   1 & 0 & 0  \\
   3 & 1 & 0  \\
   -1 & 0 & 1
\end{pmatrix}
   \begin{pmatrix}
    -1 & 1 & 2  \\
   0 & 2 & 7  \\
   0 & 4 & 6
\end{pmatrix}\]

\[\begin{pmatrix}
    1 & 0 & 0  \\
   3 & 1 & 0  \\
   -1 & 2 & 1
\end{pmatrix}
   \begin{pmatrix}
    -1 & 1 & 2  \\
   0 & 2 & 7  \\
   0 & 0 & -8
\end{pmatrix}\]

\[L=\begin{pmatrix}
    1 & 0 & 0  \\
   3 & 1 & 0  \\
   -1 & 2 & 1
\end{pmatrix}
U=   \begin{pmatrix}
    -1 & 1 & 2  \\
   0 & 2 & 7  \\
   0 & 0 & -8
\end{pmatrix}\]

\[\begin{pmatrix}
    1 & 0 & 0  \\
   3 & 1 & 0  \\
   -1 & 2 & 1
\end{pmatrix}
   \begin{pmatrix}
    -1 & 1 & 2  \\
   0 & 2 & 7  \\
   0 & 0 & -8
\end{pmatrix}

=\begin{pmatrix}
   -1 & 1 & 2  \\
   3 & -1 & 1  \\
   {\color{red}{1}} & 3 & 4
\end{pmatrix}
\neq
\begin{pmatrix}
   -1 & 1 & 2  \\
   3 & -1 & 1  \\
   {\color{red}{-1}} & 3 & 4
\end{pmatrix}\] 항상 \(A = LU\) 가 성립하는 것은 아니다.

## 역행렬과정의 불완전한 LU분해

[가우스 소거법을](../Page/가우스_소거법.md "wikilink") 사용해서, 다음과 같은 행렬 \(M\)의 [단위행렬](../Page/단위행렬.md "wikilink") \(I\)을 [첨가 행렬로](../Page/첨가_행렬.md "wikilink") 계산하면, 역행렬\(M^{-1}\)를 얻을수있다.

\[M = \begin{pmatrix}
   -1 & 1 & 2  \\
   3 & -1 & 1  \\
   -1 & 3 & 4
\end{pmatrix}\] [기본행연산을](https://ko.wikipedia.org/wiki/기본행렬#기본행연산 "wikilink") 가하면, 다음과 같다.

\[\begin{align}
  \begin{pmatrix}
   \ I & \vert& M
\end{pmatrix}  &\to \left( \left. \begin{matrix}
  1 & 0 & 0  \\
   0 & 1 & 0  \\
   0 & 0 & 1  \\
\end{matrix} \ \ \right| \ \ \begin{matrix}

  -1 & 1 & 2  \\
   3 & -1 & 1  \\
   -1 & 3 & 4  \\
\end{matrix} \right)\\
 &\to\left(\left. \begin{matrix}
  1 & 0 & 0  \\
   3 & 1 & 0  \\
   -1 & 0 & 1  \\
\end{matrix} \right| \begin{matrix}
    -1 & 1 & 2  \\
   0 & 2 & 7  \\
   0 & 2 & 2  \\
\end{matrix} \right)\\
 &\to\left(\left. \begin{matrix}
    1 & {\color{red}{0}} & {\color{red}{0}}  \\
   3 & 1 & {\color{red}{0}} \\
   -4 & -1 & 1  \\
\end{matrix} \right| \begin{matrix}
  -1 & 1 & 2  \\
  {\color{red}{0}} & 2 & 7  \\
   {\color{red}{0}} & {\color{red}{0}} & -5  \\
\end{matrix}\right)\\
&\to\left( \left. \begin{matrix}
   -1 & {0} & {0}  \\
   1.5 & 0.5 & {0}  \\
   0.8 & 0.2 & -0.2  \\
\end{matrix} \right| \begin{matrix}
   1 & -1 & -2  \\
  {0} & 1 & 3.5  \\
  {0} & {0} & 1  \\
\end{matrix} \right)\\
 &\to\left( \left. \begin{matrix}
    0.6 & 0.4 & -0.4  \\
   -1.3 & -0.2 & 0.7  \\
   0.8 & 0.2 & -0.2  \\
\end{matrix} \ \ \right| \ \ \begin{matrix}
  1 & -1 & 0  \\
   0 & 1 & 0  \\
   0 & 0 & 1  \\
\end{matrix} \right) \\
 & \to \left( \left. \begin{matrix}
    -0.7 & 0.2 & 0.3  \\
   -1.3 & -0.2 & 0.7  \\
   0.8 & 0.2 & -0.2  \\
\end{matrix} \ \ \right| \ \ \begin{matrix}
  1 & 0 & 0  \\
   0 & 1 & 0  \\
   0 & 0 & 1  \\
\end{matrix} \right)
\end{align}\] 따라서 \(M^{-1}\)은 다음과 같다.

\[M^{-1}=\begin{pmatrix}
   -0.7 & 0.2 & 0.3  \\
   -1.3 & -0.2 & 0.7  \\
   0.8 & 0.2 & -0.2
\end{pmatrix}\] 사다리꼴행렬의 역행렬 중간 과정은 유사한 LU 분해를 보여주지만

그러나, 이것은 완전한 LU 분해가 아니다.

\[\left(\left. \begin{matrix}
   1 & {\color{red}{0}} & {\color{red}{0}}  \\
   3 & 1 & {\color{red}{0}} \\
   -4 & -1 & 1  \\
\end{matrix} \right|  \begin{matrix}
   -1 & 1 & 2  \\
  {\color{red}{0}} & 2 & 7  \\
   {\color{red}{0}} & {\color{red}{0}} & -5  \\
\end{matrix}\right)

= \begin{pmatrix}
   1 & {\color{red}{0}} & {\color{red}{0}}  \\
   3 & 1 & {\color{red}{0}} \\
   -4 & -1 & 1  \\
\end{pmatrix}
 \begin{pmatrix}
   -1 & 1 & 2  \\
  {\color{red}{0}} & 2 & 7  \\
   {\color{red}{0}} & {\color{red}{0}} & -5  \\
\end{pmatrix}

\neq \begin{pmatrix}
   -1 & 1 & 2  \\
   3 & -1 & 1  \\
   -1 & 3 & 4
\end{pmatrix} =M\]

그러나 이러한 역행렬 과정을 통해 추가적인 조작으로 \(LU\)분해 를 유도할수있다.

## 응용

### 선형 연립방정식의 풀이

다음 선형 연립방정식이 주어져 있다.

\[Ax=b\] 계수 행렬 \(A\)를 행 교환을 허용한 가우스 소거법을 통해 LU 분해하면 다음과 같은 꼴로 분해된다. 여기서 \(P\)는 [치환행렬](https://ko.wikipedia.org/wiki/치환행렬 "wikilink")이다.

\[PA=LU\] 따라서 연립방정식은 다음과 같이 나타낼 수 있다.

\[PAx=Pb \iff LUx=Pb\] 연립방정식의 해는 2단계에 걸쳐서 풀이한다.

1.  **전진 대입**: \(Ly=Pb\)를 y에 대해 풀고,
2.  **후진 대입**: \(Ux=y\)를 x에 대해서 푼다.

LU 분해를 통한 풀이는 계수 행렬이 같고 \(b\)만이 달라질 때, 매번 첨가행렬의 가우스 소거법을 통해 연립방정식의 해를 구하는 것보다 간편하다. 그러나 LU 분해를 하는 과정 자체는 가우스 소거법과 동일한 과정을 거치게 된다.

### 행렬식 계산

[삼각행렬](../Page/삼각행렬.md "wikilink")의 [행렬식](../Page/행렬식.md "wikilink")은 주대각 성분의 곱이 행렬식과 같다는 점을 이용하면 LU 분해를 통해 행렬식을 쉽게 계산할 수 있다. 치환행렬은 \(P^{-1}=P^{T}\)를 만족하는 직교 행렬이므로 \(\det{P^{-1}}=\det{P}\)이라는 점을 이용할 수 있다.

\[PA=LU \implies A=P^{-1}LU \implies \det{A}=\det{P}\det{L}\det{U}=(-1)^{S}\left( \prod_{i=1}^n l_{ii} \right) \left( \prod_{i=1}^n u_{ii} \right)\] 여기서 *S*는 LU 분해를 할 때 행 교환을 시행한 횟수이다.

## 함께 보기

  - [가우스 소거법](../Page/가우스_소거법.md "wikilink")
  - [사다리꼴행렬](../Page/사다리꼴행렬.md "wikilink")
  - [QR 분해](../Page/QR_분해.md "wikilink")
  - [행렬 분해](../Page/행렬_분해.md "wikilink")
  - [가우스-자이델 방법](../Page/가우스-자이델_방법.md "wikilink")
  - [숄레스키 분해](../Page/숄레스키_분해.md "wikilink")(촐레스키 분해)

## 참고

  - (매스월드)http://mathworld.wolfram.com/LUDecomposition.html

[분류:행렬 분해](https://ko.wikipedia.org/wiki/분류:행렬_분해 "wikilink") [분류:선형대수학](https://ko.wikipedia.org/wiki/분류:선형대수학 "wikilink")