> This article is converted from Wikipedia: [J-불변량](https://ko.wikipedia.org/wiki/J-불변량).


[right](https://ko.wikipedia.org/wiki/파일:KleinInvariantJ.jpg "wikilink") [수학](../Page/수학.md "wikilink")에서, **\(j\)-불변량**(j-不變量, )은 [모듈러 함수의](https://ko.wikipedia.org/wiki/모듈러_함수 "wikilink") 하나다. \(j\)-불변량의 모든 [유리 함수](../Page/유리_함수.md "wikilink") 또한 [모듈러 함수이며](https://ko.wikipedia.org/wiki/모듈러_함수 "wikilink"), 모든 모듈러 함수는 \(j\)-불변량의 유리 함수로 나타낼 수 있다.

## 정의

[상반평면](https://ko.wikipedia.org/wiki/상반평면 "wikilink") \(\tau\in\mathbb H\)에 대하여, 다음과 같은 함수들을 정의하자.

\[g_2(\tau)=60\sum_{(m,n)\ne(0,0)}(m+n\tau)^{-4}\]

\[g_3(\tau)=140\sum_{(m,n)\ne(0,0)}(m+n\tau)^{-6}\] 그렇다면 다음과 같은 함수를 정의할 수 있다.

\[j(\tau)=1728\frac{g_2(\tau)^3}{g_2(\tau)^3-27g_3(\tau)^2}\] 이를 **\(j\)-불변량**이라고 한다. 일부 문헌에서는 \(j(\tau)\) 대신 \(J(\tau)=j(\tau)/1728\)을 사용하기도 한다.

## 특별한 값

특별한 점에서 \(j\)-불변량의 값은 다음과 같다.

| *τ*      | *i*  | exp(2*πi*/3) | exp(2*πi*/6) | *i*∞ | \((1+i\sqrt{7})/2\) | \((1+i\sqrt{11})/2\) | \((1+i\sqrt{19})/2\) | \((1+i\sqrt{43})/2\) | \((1+i\sqrt{67})/2\) | \((1+i\sqrt{163})/2\) |
| -------- | ---- | ------------ | ------------ | ---- | ------------------- | -------------------- | -------------------- | -------------------- | -------------------- | --------------------- |
| *j*(*τ*) | 1728 | 0            | 0            | ∞    | −15<sup>3</sup>     | −32<sup>3</sup>      | −96<sup>3</sup>      | −960<sup>3</sup>     | −5280<sup>3</sup>    | −640320<sup>3</sup>   |

이 가운데, 7, 11, 19, 43, 67은 [헤그너 수이다](../Page/헤그너_수.md "wikilink").

### 헤그너 수와 라마누잔 상수

\(d\)가 [헤그너 수라면](../Page/헤그너_수.md "wikilink") \(j((1+i\sqrt d)/2)\)는 [정수](../Page/정수.md "wikilink")이다. 따라서, 그 [푸리에 급수에](../Page/푸리에_급수.md "wikilink") 따라서

\[j((1+i\sqrt d)/2)=\frac1q + 744 + 196884 q +\cdots\] 이다. 여기서 \(d\)가 크다면

\[q=-\exp(-\pi\sqrt d)\] 의 절댓값은 매우 작다. 따라서 푸리에 급수의 고차항을 버리고, 다음과 같은 근사식을 쓸 수 있다.

\[\exp(\pi\sqrt d)+744\approx j((1+i\sqrt d)/2)\in\mathbb Z\] 즉, \(\exp(\pi\sqrt d)\)는 정수에 매우 가까운 [초월수](../Page/초월수.md "wikilink")이다. 가장 큰 헤그너 수 \(d=163\)을 사용하면

  -
    \(e^{\pi \sqrt{163}} = 262\,537\,412\,640\,768\,743.999\,999\,999\,999\,25\cdots\)

이다. 이는 [스리니바사 라마누잔이](../Page/스리니바사_라마누잔.md "wikilink") 발견하였고, [라마누잔 수](https://ko.wikipedia.org/wiki/라마누잔_상수 "wikilink")()라고 한다.

## 푸리에 급수와 가공할 헛소리

j-불변량의 [푸리에 급수는](../Page/푸리에_급수.md "wikilink") \(q=\exp(2\pi i\tau)\)를 사용하여 적으면 다음과 같다

\[j(\tau) = \frac1q + 744 + 196884 q + 21493760 q^2 + 864299970 q^3 + 20245856256 q^4 + 333202640600q^5+\cdots\] 이 계수들은 가장 큰 예외적 유한 [단순군](../Page/단순군.md "wikilink")인 [괴물군의](../Page/괴물군_\(수학\).md "wikilink") [기약 표현들의](https://ko.wikipedia.org/wiki/기약_표현 "wikilink") 차원과 관계있다.

\[\begin{align}
1 & = 1 \\
196884 & = 196883 + 1 \\
21493760 & = 21296876 + 196883 + 1 \\
864299970 & = 842609326 + 21296876 + 2\cdot 196883 + 2\cdot 1 \\
20245856256&=18538750076+2\cdot842609326+21296876+3\cdot196883+3\cdot1\\
&=19360062527+842609326+2\cdot21296876+3\cdot196883+2\cdot1\\
333202640600 & =293553734298+2\cdot 18538750076+3\cdot 842609326+2\cdot 21296876+5\cdot 196883+5\cdot 1\\
& =293553734298+19360062527+ 18538750076+2\cdot 842609326+3\cdot 21296876+5\cdot 196883+4\cdot 1\\
4252023300096 & =3879214937598+293553734298+4\cdot 18538750076+6\cdot842609326+2\cdot21296876+7\cdot196883+7\cdot1 \\
& {}\,\,\, \vdots
\end{align}\] 이 관계를 [가공할 헛소리](../Page/가공할_헛소리.md "wikilink")()라고 한다. 여기서 (가공할, 말도 안 되는)는 괴물 군()에 대한 말장난이다. 이 놀라운 관계는 원래 존 매케이(, 1939–)가 1970년대에 최초로 발견하였고, [존 호턴 콘웨이가](../Page/존_호턴_콘웨이.md "wikilink") 이러한 이름을 붙였다. 이 사실은 [리처드 보처즈가](../Page/리처드_보처즈.md "wikilink") [리치 격자](https://ko.wikipedia.org/wiki/리치_격자 "wikilink")(Leech lattice)에 [축소화](../Page/축소화.md "wikilink")한 [보손 끈 이론을](../Page/보손_끈_이론.md "wikilink") 사용해 설명하였고, 이 공로로 [필즈상](../Page/필즈상.md "wikilink")을 수상하였다.

## 함께보기

  - [바이어슈트라스 제타 함수](../Page/바이어슈트라스_제타_함수.md "wikilink")
  - [자기동형 형식](../Page/보형_형식.md "wikilink")
  - [클래스 넘버 문제](https://ko.wikipedia.org/wiki/클래스_넘버_문제 "wikilink")

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
[분류:모듈러 형식](https://ko.wikipedia.org/wiki/분류:모듈러_형식 "wikilink") [분류:타원함수](https://ko.wikipedia.org/wiki/분류:타원함수 "wikilink")