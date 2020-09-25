> This article is converted from Wikipedia: [P진수](https://ko.wikipedia.org/wiki/P진수).


[수론](https://ko.wikipedia.org/wiki/수론 "wikilink")에서, **<i>p</i>진수**(p進數, *p*-adic number)는 [유리수](../Page/유리수.md "wikilink")의 체를 마치 어떤 [소수](../Page/소수_\(수론\).md "wikilink") *p*에 대한 [로랑 급수처럼](../Page/로랑_급수.md "wikilink") 해석하여 [완비시켜](../Page/완비_거리_공간.md "wikilink") 얻는 [체이다](../Page/체_\(수학\).md "wikilink"). 보다 구체적으로 설명하면, 임의의 소수 p에 대해, p진수들을 전부 모은 *p*진체는 유리수체의 [완비화이다](../Page/완비_거리_공간.md "wikilink"). 또한 *p*진수에는 *p*진 [값매김](https://ko.wikipedia.org/wiki/값매김 "wikilink")이 주어져 있기에 [거리 공간이](../Page/거리_공간.md "wikilink") 되며 따라서 [위상 공간이기도](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink") 하다. 이 거리 공간은 [완비 거리 공간](../Page/완비_거리_공간.md "wikilink")(즉, 모든 [코시 수열이](https://ko.wikipedia.org/wiki/코시_수열 "wikilink") 수렴한다)이며, 그렇기에 p진체 상에서 마치 실수체 상에서와 같은 [해석학을](../Page/해석학_\(수학\).md "wikilink") 전개할 수 있는 것이다. p진법 체계의 유용성은 상당 부분 이와 같은 [대수적](../Page/대수학.md "wikilink") 구조와 해석적 구조 사이의 상호 연관성에서 나온다.

## 개론

[유리수체](https://ko.wikipedia.org/wiki/유리수체 "wikilink") \(\mathbb Q\)는 표준 [노름](https://ko.wikipedia.org/wiki/노름 "wikilink") \(|a/b|\)에 대하여 [완비 거리 공간을](../Page/완비_거리_공간.md "wikilink") 이루지 않는다. 따라서, 이에 대하여 [코시 수열들의](https://ko.wikipedia.org/wiki/코시_수열 "wikilink") [동치류](https://ko.wikipedia.org/wiki/동치류 "wikilink")들을 취하여 이를 완비화할 수 있는데, 이렇게 하여 [실수체](https://ko.wikipedia.org/wiki/실수체 "wikilink") \(\mathbb R\)을 얻는다. 유리수체의 표준 노름은 매우 유용하지만, 원하면 유리수체에 다른 노름을 줄 수도 있다. 이러한 노름에 대하여 완비화하면 다른 체를 얻게 된다. *p*진수는 이렇게 정의되는 체 가운데 하나다.

수론에서, 유리수들을 어떤 주어진 [소수](../Page/소수_\(수론\).md "wikilink") *p*에 대한 형식적인 단항식으로 취급하게 되는 경우가 있다. 모든 0이 아닌 유리수는 \(p^n(a/b)\) (\(a\)와 \(b\)는 \(p\)로 나누어떨어지지 않음)의 꼴로 유일하게 나타낼 수 있다. 예를 들어, \(p=7\)이라고 하자. 그렇다면,

\[28/5=7\times(4/5)\]

\[-15/98=7^{-2}\times(-15/2)\] 이는 "변수" \(p=7\)에 대한 단항식 \((4/5)p\) 또는 \(-(15/2)p^{-2}\)와 유사하게 생각할 수 있다. 이제, \(p\)를 일종의 [무한소](https://ko.wikipedia.org/wiki/무한소 "wikilink")로 취급하면, \(p\)의 인수를 더 많이 포함할 수록 더 "작고", \(p^{-1}\)의 인수를 더 많이 포함할 수록 더 "크다"고 생각할 수 있다.

이와 같이 유리수체 \(\mathbb Q\) 위에 \(p\)의 인수를 더 많이 포함할 수록 더 노름이 작아지는 [노름](https://ko.wikipedia.org/wiki/노름 "wikilink")을 정의할 수 있다. *p*진체는 유리수체를 이 노름에 대하여 완비화한 체이다.

## 정의

*p*진수체 및 *p*진 정수환은 해석적인 기법 및 [가환대수학](../Page/가환대수학.md "wikilink")적 기법으로 정의할 수 있다.

### 해석적 정의

\(p\)가 [소수라고](../Page/소수_\(수론\).md "wikilink") 하자. [유리수체](https://ko.wikipedia.org/wiki/유리수체 "wikilink") \(\mathbb Q\)에 다음과 같은 [노름](https://ko.wikipedia.org/wiki/노름 "wikilink") \(|\cdot|_p\)를 정의할 수 있다.

\[|p^na/b|_p=p^{-n}\] (\(p\nmid a,b\))

\[|0|_p=0\] (모든 0이 아닌 유리수는 \(p^na/b\)와 같은 꼴로 유일하게 나타낼 수 있다.) 이 노름을 **<i>p</i>진 노름**()이라고 한다.

[유리수체](https://ko.wikipedia.org/wiki/유리수체 "wikilink") \(\mathbb Q\)를 이 노름에 대하여 [완비화시켜](../Page/완비_거리_공간.md "wikilink") 얻는 체를 **<i>p</i>진체** \(\mathbb Q_p\)라고 하며, 그 원소를 **<i>p</i>진수**라고 한다.

### 대수적 정의

*p*진 정수환 \(\mathbb Z_p\)는 [정수환](https://ko.wikipedia.org/wiki/정수환 "wikilink") \(\mathbb Z\)를 소 아이디얼 \((p)\)에서 [완비화한](../Page/완비화_\(환론\).md "wikilink") 것이다. 즉, 다음과 같은 [몫환](https://ko.wikipedia.org/wiki/몫환 "wikilink")들 사이에 자연스러운 [환 준동형이](https://ko.wikipedia.org/wiki/환_준동형 "wikilink") 존재하며,

\[\cdots\to\mathbb Z/p^3\to\mathbb Z/p^2\to\mathbb Z/p\to0\] *p*진 정수환은 이들의 [역극한](https://ko.wikipedia.org/wiki/역극한 "wikilink")이다.

\[\mathbb Z_p=\varprojlim_n\mathbb Z/(p^n)\] *p*진 정수환은 [정역](../Page/정역.md "wikilink")을 이루며, ***p*진수체** \(\mathbb Q_p\)는 *p*진 정수환의 [분수체](../Page/분수체.md "wikilink")이다.

\[\mathbb Q_p=\operatorname{Frac}(\mathbb Z_p)\]

보다 추상적으로, *p*진 정수환 \(\mathbb Z_p\)는 크기 \(p\)의 [유한체](../Page/유한체.md "wikilink") \(\mathbb F_p\) 위의 \(p\)진 [비트 벡터 환으로](https://ko.wikipedia.org/wiki/비트_벡터_환 "wikilink") 정의할 수도 있다.

### *p*진 복소수

**<i>p</i>진 복소수체** \(\mathbb C_p\)는 다음과 같이 정의한다.

1.  p진체 \(\mathbb Q_p\)는 [완비 거리 공간이지만](../Page/완비_거리_공간.md "wikilink") [대수적으로 닫힌 체가](../Page/대수적으로_닫힌_체.md "wikilink") 아니다. 그 [대수적 폐포를](https://ko.wikipedia.org/wiki/대수적_폐포 "wikilink") 취하여, 대수적으로 닫힌 체 \(\bar{\mathbb Q}_p\)를 얻을 수 있다.
2.  대수적 폐포 \(\bar{\mathbb Q}_p\)는 [대수적으로 닫힌 체이지만](../Page/대수적으로_닫힌_체.md "wikilink") [완비 거리 공간이](../Page/완비_거리_공간.md "wikilink") 아니다. 그 완비화를 취하여, \(\mathbb C_p\)라는 체를 얻는다. 이는 [대수적으로 닫힌 체이자](../Page/대수적으로_닫힌_체.md "wikilink") [완비 거리 공간이다](../Page/완비_거리_공간.md "wikilink"). 이를 **<i>p</i>진 복소수체**로 정의한다.

## 성질

### *p*진 노름

*p*진 노름은 다음과 같은 성질들을 만족시킨다. 아래에서, \(r,s\in\mathbb Q\)는 임의의 유리수다.

  - \(|r+s|_p\le\max\{|r|_p,|s|_p\}\)

<!-- end list -->

  -

      -
        이는 모든 [노름](https://ko.wikipedia.org/wiki/노름 "wikilink")들이 만족시키는 [삼각 부등식](https://ko.wikipedia.org/wiki/삼각_부등식 "wikilink") \(|r+s|\le|r|+|s|\)보다 더 강한 조건이다.

<!-- end list -->

  - \(\mathbb Q\)의 표준 노름을 \(|\cdot|_\infty\)라고 쓰자. 그렇다면,

\[|r|_\infty\prod_p|r|_p=1\]

  -
    이다.

### *p*진 정수환

*p*진 정수환 \(\mathbb Z_p\)의 [집합의 크기는](../Page/집합의_크기.md "wikilink") \(2^{\aleph_0}\)이다. 즉, [실수체](https://ko.wikipedia.org/wiki/실수체 "wikilink")의 크기와 같다.

[가환대수학](../Page/가환대수학.md "wikilink")적으로, *p*진 정수환은 [이산 값매김환이다](../Page/이산_값매김환.md "wikilink") (따라서, [주 아이디얼 정역이자](../Page/주_아이디얼_정역.md "wikilink") [유클리드 정역이며](../Page/유클리드_정역.md "wikilink"), [크룰 차원이](../Page/크룰_차원.md "wikilink") 1차원인 [국소환](https://ko.wikipedia.org/wiki/국소환 "wikilink")이다). 값군은 [무한 순환군](https://ko.wikipedia.org/wiki/무한_순환군 "wikilink") \(\mathbb Z\)이며, [값매김](https://ko.wikipedia.org/wiki/값매김 "wikilink")은 *p*진 노름 \(|\cdot|_p\colon\mathbb Q_p\to\mathbb Z\)이다.

*p*진 정수환의 [가역원군](https://ko.wikipedia.org/wiki/가역원군 "wikilink") \(\mathbb Z^\times_p\)은 다음과 같다.

\[\mathbb Z_p^\times=\mathbb Z_p\setminus(p)=\{a\in\mathbb Z_p\colon|a|_p=0\}\] *p*진 정수환의 모든 0이 아닌 원소는 다음과 같이 유일하게 나타낼 수 있다.

\[a=p^nu\qquad(n\in\mathbb N,u\in\mathbb Z^\times_p)\] 따라서, *p*진 정수환의 모든 아이디얼은 다음과 같은 두 꼴 가운데 하나이다.

  - \((p^n),\;n\in\mathbb N\)
  - \((0)\)

*p*진 정수환의 유일한 [극대 아이디얼은](../Page/극대_아이디얼.md "wikilink") \((p)\)이다. *p*진 정수환의 [소 아이디얼은](../Page/소_아이디얼.md "wikilink") 영 아이디얼과 \((p)\)이다.

*p*진 정수환의 [몫환](https://ko.wikipedia.org/wiki/몫환 "wikilink")은 다음과 같다.

\[\mathbb Z_p/(p^n)\cong\mathbb Z/(p^n)\]

\[\mathbb Z_p/(0)\cong\mathbb Z_p\]

*p*진 정수환은 [국소환](https://ko.wikipedia.org/wiki/국소환 "wikilink")이므로, 자연스러운 \((p)\)진 위상을 갖추어 [위상환](https://ko.wikipedia.org/wiki/위상환 "wikilink")을 이룬다. p진 정수의 덧셈 [위상군](../Page/위상군.md "wikilink")의 [폰트랴긴 쌍대군은](https://ko.wikipedia.org/wiki/폰트랴긴_쌍대군 "wikilink") ([이산 위상을](https://ko.wikipedia.org/wiki/이산_위상 "wikilink") 갖춘) [프뤼퍼 군](../Page/프뤼퍼_군.md "wikilink") \(\mathbb Z(p^\infty)\)이다.

### *p*진체

*p*진체 \(\mathbb Q_p\)는 다음과 같은 성질을 만족시킨다.

  - \(\mathbb Q_p\)의 [집합의 크기는](../Page/집합의_크기.md "wikilink") \(|\mathbb Q_p|=2^{\aleph_0}=\mathfrak c=|\mathbb R|\)이다. 즉, [실수체](https://ko.wikipedia.org/wiki/실수체 "wikilink")의 크기와 같다.
  - \(\mathbb Q_p\)는 [유리수체](https://ko.wikipedia.org/wiki/유리수체 "wikilink")를 부분체로 가지는 [체이다](../Page/체_\(수학\).md "wikilink"). 그 [체의 표수는](https://ko.wikipedia.org/wiki/체의_표수 "wikilink") 0이다.
  - \(\mathbb Q_p\)는 순서 구조를 가하여 [순서체](../Page/순서체.md "wikilink")로 만들 수 없다.
  - [위상 공간으로서](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink"), *p*진체 \(\mathbb Q_p\)는 [국소 콤팩트](https://ko.wikipedia.org/wiki/국소_콤팩트 "wikilink") [하우스도르프 공간이지만](../Page/하우스도르프_공간.md "wikilink"), [콤팩트하지](../Page/콤팩트_공간.md "wikilink") 않다.

### *p*진 복소수체

*p*진 복소수체 \(\mathbb C_p\)는 다음과 같은 성질을 만족시킨다.

  - \(\mathbb C_p\)는 대수학적으로 표준 복소수체 \(\mathbb C\)와 동형이다. 즉, \(\mathbb C_p\)는 \(\mathbb C\)에 비표준 [노름](https://ko.wikipedia.org/wiki/노름 "wikilink")을 준 것으로 생각할 수 있다.
      - 따라서, \(|\mathbb C_p|=|\mathbb C|=\mathfrak c\)이며, [대수적으로 닫힌 체임을](../Page/대수적으로_닫힌_체.md "wikilink") 일 수 있다.
  - [위상 공간으로서](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink"), \(\mathbb C_p\)는 [하우스도르프 공간이지만](../Page/하우스도르프_공간.md "wikilink") [국소 콤팩트하지](https://ko.wikipedia.org/wiki/국소_콤팩트 "wikilink") 않다.

## 예

*p*진수의 덧셈·뺄셈·곱셈은 *p*진법 실수의 덧셈·뺄셈·곱셈과 유사하며, 유일한 차이는 소숫점 왼쪽으로 무한한 수의 자릿수가 존재한다는 것 뿐이다. *p*진법 나눗셈은 조금 다른데, 이 경우 뺄셈을 할 때, 1의 자릿수가 0이 되게 하는 수를 찾아서 뺀다.

예를 들어, 3의 역수 ⅓을 5진수체로 표현하면 [순환](../Page/순환소수.md "wikilink") 5진 정수 \(1/3=\overline{13}2_5\)이다. (여기서 자릿수 위의 윗줄은 반복되는 자릿수를 나타낸다.) 이는 다음과 같이 증명할 수 있다.

\[\frac{5^2-1}{3}=\frac{44_5}3 = 13_5; \, \frac{5^4-1}3=\frac{4444_5}3 = 1313_5;\,
\frac{5^6-1}3=\frac{444444_5}3 = 131313_5;\cdots\]

\[\implies-\frac13=\overline{13}_5=\cdots1313_5\]

\[\implies-\frac23=\overline{13}_5 \times 2 = \overline{31}_5=\cdots3131_5\]

\[\implies\frac13 = -\frac23+1 = \overline{13}2_5=\cdots132_5\]

이는 직접 다음과 같이 계산할 수 있다.

\[\begin{array}{crl}
&\underline{\cdots3132_5}\\
3)&{\color{White}{\cdots000}}1_5\\
-&\underline{{\color{White}{\cdots00}}11_5}&(=3_5\times2)\\
&\cdots4440_5\\
-&\underline{{\color{White}{\cdots0}}14_5}{\color{White}{0}}&(=3_5\times3)\\
&\cdots430_5{\color{White}{0}}\\
-&\underline{{\color{White}{\cdots0}}3_5}{\color{White}{00}}&(=3_5\times1)\\
&\cdots40_5{\color{White}{00}}\\
-&\underline{\cdots4_5}{\color{White}{000}}&(=3_5\times3)\\
&\cdots0_5{\color{White}{000}}
\end{array}\] 이는

\[\begin{array}{cr}
\cdots&\overset21\overset13\overset21\overset13\overset21\overset132_5\\
\times&3_5\\
\hline\\
\cdots&000001_5\\
\end{array}\] 로 검산할 수 있다. (여기서 윗첨자는 올림()이다.) 소숫점 오른쪽의 자릿수가 모두 0이므로, 이는 5진 정수이다.

## 역사

[쿠르트 헨젤이](../Page/쿠르트_헨젤.md "wikilink") [1897년](../Page/1897년.md "wikilink")에 [대수적 수론에서](../Page/대수적_수론.md "wikilink") 사용하기 위하여 도입하였다.\[1\]

## 응용

원래 [수론](https://ko.wikipedia.org/wiki/수론 "wikilink")에서 도입되었지만, 오늘날 *p*진수는 초기의 목적에 비해 훨씬 더 다양한 분야에서 사용되고 있다. 예를 들어 [p진 해석학은](https://ko.wikipedia.org/wiki/p진_해석학 "wikilink") [미적분학](../Page/미적분학.md "wikilink")의 *p*진법 버전이라 할 수 있다.

[이론물리학](../Page/이론물리학.md "wikilink")에서도 *p*진수가 종종 사용된다.\[2\]\[3\]\[4\]\[5\]

[컴퓨터 과학에서는](../Page/컴퓨터_과학.md "wikilink") [유리수](../Page/유리수.md "wikilink")를 나타내는 한 방법으로 사용된다.\[6\]

## 참고 문헌

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
[분류:대수적 수론](https://ko.wikipedia.org/wiki/분류:대수적_수론 "wikilink")

1.
2.
3.
4.
5.
6.