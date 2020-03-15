> This article is converted from Wikipedia: [ W ](https://ko.wikipedia.org/wiki/_W_).


[thumb](https://ko.wikipedia.org/wiki/파일:Lambert-w.svg "wikilink") [수학](https://ko.wikipedia.org/wiki/수학 "wikilink")에서, **람베르트 W 함수**()는 [복소함수](https://ko.wikipedia.org/wiki/복소함수 "wikilink") \(f(w)=we^w\)의 [역관계의](../Page/관계_\(수학\).md "wikilink") 일부인 함수들의 [집합](https://ko.wikipedia.org/wiki/집합 "wikilink")이며, 다음과 같은 공식을 가진다.

\[z = W(z)e^{W(z)}\] \(f\)가 [전사 함수가](https://ko.wikipedia.org/wiki/전사_함수 "wikilink") 아니기 때문에, 관계 W는 z=0일 때를 제외하고 여러 값을 가질 수 있다.

람베르트 W 함수는 [초등 함수로](https://ko.wikipedia.org/wiki/초등_함수 "wikilink") 나타낼 수 없다. 람베르트 W 함수는 [조합론](../Page/조합론.md "wikilink")에서, 또는 [지수](https://ko.wikipedia.org/wiki/지수 "wikilink")를 포함한 다양한 [방정식](https://ko.wikipedia.org/wiki/방정식 "wikilink")을 푸는 데 사용되며, [지연미분방정식](../Page/지연미분방정식.md "wikilink")의 해에서 나타나기도 한다.

## 역사

[요한 람베르트가](https://ko.wikipedia.org/wiki/요한_람베르트 "wikilink") "람베르트 초월방정식"이라고 불리는 방정식을 1758년 처음 연구하였다.\[1\] 1783년 [레온하르트 오일러는](https://ko.wikipedia.org/wiki/레온하르트_오일러 "wikilink") 이 방정식의 특수한 경우인 \(x=we^w\)에 대한 논문을 발표하였다.\[2\] 람베르트 W 함수 자체는 1925년 처음 언급되었다.\[3\]

## 성질

### 도함수

[음함수의 미분을](https://ko.wikipedia.org/wiki/음함수와_양함수#음함수의_미분 "wikilink") 사용하여, 임의의 *W*의 가지가 [상미분방정식](../Page/상미분방정식.md "wikilink")

\[z(1+W)\frac{{\rm d}W}{{\rm d}z}=W\quad\text{for }z\neq -1/e\]

를 만족시킴을 안다.(*W*는 *z* = −1/*e*에서 미분가능하지 않다.) 따라서, *W*에 대한 다음 공식을 얻는다.

\[\frac{{\rm d}W}{{\rm d}z}=\frac{W(z)}{z(1 + W(z))}\quad\text{for }z\not\in\{0,-1/e\}\] 한편, ''z ''= 0에서 *W*의 미분계수는

\[\left.\frac{{\rm d}W}{{\rm d}z}\right|_{z=0}=1\] 이다.

### 부정적분

함수 *W*(*x*)와 *W*(*x*)를 포함하는 많은 식들은 [치환적분](https://ko.wikipedia.org/wiki/치환적분 "wikilink")을 이용하여 [적분](https://ko.wikipedia.org/wiki/적분 "wikilink")할 수 있다.

\[\int W(x)\,{\rm d}x = x \left( W(x) - 1 + \frac{1}{W(x)} \right) + C\]

### 다른 공식들

\[\int_{0}^{\pi} W\bigl( 2\cot^2(x) \bigr)\sec^2(x)\;\mathrm dx = 4\sqrt{\pi}\]

\[\int_{0}^{\infty} W\left(\frac{1}{x^2}\right)\;\mathrm dx = \sqrt{2\pi}\]

\[\int_{0}^{\infty} \frac{W(x)}{x\sqrt{x}}\mathrm dx = 2\sqrt{2\pi}\]

## 그래프

파일:LambertWRe.png| *z* = Re(W<sub>0</sub>(*x* + *i* *y*)) 파일:LambertWIm.png| *z* = Im(W<sub>0</sub>(*x* + *i* *y*)) 파일:LambertWAbs.png| *z* = abs(W<sub>0</sub>(*x* + *i* *y*)) 파일:LambertWAll.png

## 참고 문헌

## 외부 링크

  - [MathWorld - Lambert *W*-Function](http://mathworld.wolfram.com/LambertW-Function.html)

  - [National Institute of Science and Technology Digital Library - Lambert W](http://dlmf.nist.gov/4.13)

[분류:특수 함수](https://ko.wikipedia.org/wiki/분류:특수_함수 "wikilink")

1.
2.
3.