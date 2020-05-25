> This article is converted from Wikipedia: [AKS 소수판별법](https://ko.wikipedia.org/wiki/AKS_소수판별법).


**AKS 소수판별법**은 어떤 [자연수](../Page/자연수.md "wikilink")가 [소수인지](../Page/소수_\(수론\).md "wikilink") 판별하는 [결정론적 알고리즘이다](../Page/결정론적_알고리즘.md "wikilink"). 2002년 8월 6일, [인도 공과대학교 칸푸르의](https://ko.wikipedia.org/wiki/인도_공과대학교_칸푸르 "wikilink") 컴퓨터 과학자 [마닌드라 아그라왈](https://ko.wikipedia.org/wiki/마닌드라_아그라왈 "wikilink"), [니라지 카얄](https://ko.wikipedia.org/wiki/니라지_카얄 "wikilink"), [니틴 삭세나가](https://ko.wikipedia.org/wiki/니틴_삭세나 "wikilink") 공동으로 출판한 논문 "PRIMES is in P"\[1\]에서 처음으로 발표되었다.

세 저자는 이 연구로 2006년 [괴델상](https://ko.wikipedia.org/wiki/괴델상 "wikilink"), [풀커슨상](../Page/풀커슨상.md "wikilink")을 포함 각종 상을 수상하였다.

## 중요성

AKS 소수판별법은 최초로 발견된 일반적이고, 무조건적이고, [결정론적인](../Page/결정론적_알고리즘.md "wikilink") [다항 시간](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 알고리즘이다. 4가지 가운데 3가지 특성을 가진 알고리즘은 존재했으나, 4가지 특성을 모두 가진 것은 AKS가 최초이다.

  - 일반적: AKS 알고리즘은 *모든* 자연수에 대해 그 수가 소수인지 합성수인지를 판별할 수 있다. 속도가 빠른 기존의 소수 판별 알고리즘들은 몇몇 특징을 가진 소수에 대해서만 작동하였다.

예를 들어 [루카스-레머 소수판별법은](https://ko.wikipedia.org/wiki/루카스-레머_소수판별법 "wikilink") [메르센 소수에](../Page/메르센_소수.md "wikilink") 대해서만 동작하며, [루카스-레머-리젤 소수판별법은](https://ko.wikipedia.org/wiki/루카스-레머-리젤_소수판별법 "wikilink") *k* ⋅ 2<sup>*n*</sup> − 1(k는 홀수)인 수에 대해서만 작동하고, [페팽 소수판별법은](https://ko.wikipedia.org/wiki/페팽_소수판별법 "wikilink") [페르마 수에](../Page/페르마_수.md "wikilink") 대해서만 동작한다.

  - [다항 시간](https://ko.wikipedia.org/wiki/다항_시간 "wikilink"): AKS 알고리즘의 [시간 복잡도는](../Page/시간_복잡도.md "wikilink") 최악의 경우에도 소수의 자리수에 대해 [다항 시간안에](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 완료된다. [타원곡선 소수판별법이나](https://ko.wikipedia.org/wiki/타원곡선_소수판별법 "wikilink") [APR 소수판별법은](https://ko.wikipedia.org/wiki/APR_소수판별법 "wikilink") 모든 자연수에 대해 다항 시간 안에 완료된다는 것이 증명되지 않았다.
  - [결정론적](../Page/결정론적_알고리즘.md "wikilink"): AKS 알고리즘은 자연수가 소수인지 합성수인지를 결정적으로 확인할 수 있다. [밀러-라빈 소수판별법이나](../Page/밀러-라빈_소수판별법.md "wikilink") [베일리-PSW 소수판별법은](https://ko.wikipedia.org/wiki/베일리-PSW_소수판별법 "wikilink") 모든 자연수에 대해 다항 시간 안에 완료되지만, 이 판별법으로 소수라는 답이 나오더라도 해당 자연수가 합성수일 확률이 존재한다.
  - 무조건적: AKS 소수판별법은 증명되지 않은 가설에 기반하고 있지 않다. [밀러 소수판별법은](https://ko.wikipedia.org/wiki/밀러_소수판별법 "wikilink") 결정론적이고, 모든 자연수에 대해 다항 시간 안에 완료되지만, 아직 증명되지 않은 [일반화 리만 가설이](https://ko.wikipedia.org/wiki/일반화_리만_가설 "wikilink") 참일 경우에만 참이라는 것이 증명되어 있다.

## 개요

AKS 소수판별법은 다음과 같은 정리를 이용한다

정수 *n* (≥ 2) 은, *n*과 [서로소](https://ko.wikipedia.org/wiki/서로소 "wikilink")인 모든 정수 *a*에 대해 다음 [합동식](https://ko.wikipedia.org/wiki/합동식 "wikilink")이 성립할 때만 소수이며, 그렇지 않으면 합성수이다.

\[(x - a)^{n} \equiv (x^{n} - a) \pmod{n} \qquad (1)\] 위 항등식에서 *x*는 [자유 변수이며](https://ko.wikipedia.org/wiki/자유_변수 "wikilink"), \((x-a)^{n}\)을 풀었을 때 좌변과 우변의 모든 계수가 일치해야 한다.\[2\]

위 정리는 [페르마의 소정리를](../Page/페르마의_소정리.md "wikilink") [다항식](../Page/다항식.md "wikilink")에 대해 일반화한 것으로, 다음 정리를 이용하여 쉽게 증명할 수 있다.

\[0<k<n\]인 모든 *k*에 대해 \({n \choose k} \equiv 0 \pmod{n}\)이면, *n*은 소수이며, 그렇지 않으면 합성수이다.

정리 (1)은 그 자체로 소수판별법이지만, 모든 정수에 대해 이 관계를 검증하는 것은 [지수 시간](https://ko.wikipedia.org/wiki/지수_시간 "wikilink") 알고리즘이다. 이 방법의 시간복잡도를 줄이기 위해, AKS 알고리즘은 다음 합동식을 이용한다.

\[(x - a)^{n} \equiv (x^{n} - a) \pmod{(n,x^{r}-1)} \qquad (2)\]

위 식은 다음 명제와 같은 의미를 갖는다.

\[(x - a)^n - (x^n - a) = nf + (x^r - 1)g\]를 만족하는 다항식 *f*와 *g*가 존재한다.

*r*의 크기가 *n*의 자리수에 대해 로그 복잡도를 가지므로, 다항식 *f*와 *g*의 존재를 찾는 것은 다항 시간 안에 완료할 수 있다.

## 알고리즘

AKS 알고리즘의 개요는 다음과 같다.

  -
    1보다 큰 정수 *n*을 입력으로 받는다.

<!-- end list -->

1.  \(n=a^b\)인 정수 *a* \> 1 와 *b* \> 1 가 존재하면, *합성수*를 출력한다.
2.  \(o_{r}(n) > \log^{2}(n)\)을 만족하는 가장 작은 *r*을 찾는다.
3.  만약 *a* ≤ *r*이고 1 \< [gcd](../Page/최대공약수.md "wikilink")(*a*, *n*) \< *n* 을 만족하는 정수 *a*가 존재하면, *합성수*를 출력한다.
4.  만약 *n* ≤ *r*이면 *소수*를 출력한다. 만약 n\>5690034이면 이 단계는 무시해도 된다.
5.  1에서 \(\scriptstyle\lfloor \scriptstyle{\sqrt{\varphi(r)}\log(n)} \scriptstyle\rfloor\)까지의 모든 정수 *a*에 대해,
      -
        \((x+a)^{n} \neq x^{n}+a \pmod{x^{r}-1, n}\)이면, *합성수*를 출력한다.
6.  *소수*를 출력한다

위 알고리즘에서 *o*<sub>*r*</sub>(*n*)은 곱의 차수, 즉 \(n^{k} \equiv 1 \pmod{r}\)을 만족하는 가장 작은 *k*이다. log는 이진 로그 함수이고, \(\phi (r)\)은 [오일러 피 함수이다](../Page/오일러_피_함수.md "wikilink").

## 예시

n=31을 소수판별하고 싶다고 하자.

1\. \(31^{\frac{1}{2}}, 31^{\frac{1}{3}}, 31^{\frac{1}{4}}\)는 모두 자연수가 아니다. (31의 1/5승부터는 거듭제곱들이 2 미만이 되므로 검사할 필요가 없다.)

2\. r = 29이다.

3\. gcd(2, 31)=1, gcd(3, 31)=1, ... , gcd(28, 31)=1, gcd(29, 31)=1이다.

4\. 31\>29이므로 5단계로 넘어간다.

5\. \((x+a)^{n} \equiv x^{n}+a \pmod{x^{r}-1, n}\)이 성립하려면 **(A)** \((x+a)^n\pmod{x^{29}-1, 31}\)에서 **(B)** \(x^n+a\pmod{x^{29}-1, 31}\)를 뺀 값이 (mod x<sup>r</sup>*-*1, n)에서 0이어야 한다. 따라서,

**(A)** \((x+a)^{31}\equiv x^{31}+31x^{30}a+465x^{29}a^2+\cdot\cdot\cdot+465x^2a^{29}+31xa^{30}+a^{31}\pmod{x^{29}-1, 31}\)이고, 이 전개한 식을 x<sup>29</sup>-1로 나눈 나머지는 \(a^{31}+465a^2+(31a+31a^{30})x+(1+465a^{29})x^2+\cdot\cdot\cdot+4495a^3x^{28}\)

가 되며 다시 이 식을 31로 나눈 나머지는 \(a^{31}+x^2\)가 된다. 따라서

**(A)** \((x+a)^{31}\equiv a^{31}+x^2\pmod{x^{29}-1, 31}\)

이 되고,

**(B)** \(x^{31}+a\equiv x^2+a\pmod{x^{29}-1, 31}\)

이 된다. 여기서 **(A) - (B)**는

\(a^{31}-a\equiv0\pmod{x^{29}-1, 31}\)

이 되며, a=1부터 a=\(\lfloor\sqrt{\varphi(29)}\log_{2}{31}\rfloor\)=26까지의 정수들에 대하여 \(a^{31}-a\equiv0\pmod{31}\)이 성립하므로 조건을 만족하는 모든 a에 대하여\((x+a)^{n} \equiv x^{n}+a \pmod{x^{r}-1, n}\)이 성립한다.

6\. 따라서 n=31은 소수가 된다.

## 각주

<references/>

## 참고문헌

  - H. W. Lenstra jr. 와 Carl Pomerance, "[Primality testing with Gaussian periods](http://www.math.dartmouth.edu/~carlp/aks041411.pdf)", 2011년 4월 12일

[분류:소수 판별법](https://ko.wikipedia.org/wiki/분류:소수_판별법 "wikilink")

1.
2.