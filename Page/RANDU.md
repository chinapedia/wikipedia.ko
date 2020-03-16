> This article is converted from Wikipedia: [RANDU](https://ko.wikipedia.org/wiki/RANDU).


[섬네일](https://ko.wikipedia.org/wiki/파일:Randu.png "wikilink") **RANDU**\[1\]는 [선형 합동 생성기를](../Page/선형_합동_생성기.md "wikilink") 사용한 [유사난수 생성기](https://ko.wikipedia.org/wiki/유사난수_생성기 "wikilink") 루틴으로, [1960년대](../Page/1960년대.md "wikilink")에 [IBM](../Page/IBM.md "wikilink") 메인프레임에서 널리 사용된 이후 다른 시스템에서도 널리 사용되었다. 이 루틴이 사용하는 유사난수 생성기는 다음과 같이 정의되었다.

  -
    \(X_{n+1} = 65539 X_n \mod {2^{31}}\), 단 \(X_0\)은 [홀수](https://ko.wikipedia.org/wiki/홀수 "wikilink")

RANDU는 역사상 최악으로 설계된 유사난수 생성기 중 하나로 알려져 있다. [조지 마서글리아는](https://ko.wikipedia.org/wiki/조지_마서글리아 "wikilink") [1968년](../Page/1968년.md "wikilink")에 선형 합동 생성기로 만들어진 난수들로 이루어진 좌표를 3차원 공간 상에 표시하였을 때 유한한 수의 2차원 [평면](../Page/평면.md "wikilink") 중 하나 위에 위치하게 된다는 점([마서글리아 효과](https://ko.wikipedia.org/wiki/마서글리아_효과 "wikilink"))을 밝혔는데, 그의 논문에 따르면 나눔수가 \(2^{31}\)인 생성기의 최대 평면 수는 1290개지만 RANDU는 15개의 평면 상에 모든 점들이 위치하게 된다.

## 상관 관계의 설명

RANDU의 곱함수는 컴퓨터 상에서 [비트 연산을](https://ko.wikipedia.org/wiki/비트_연산 "wikilink") 사용하여 빠르게 생성할 수 있도록 정해진 것이다. 실제로 [C 언어로](../Page/C_\(프로그래밍_언어\).md "wikilink") RANDU는 곱셈 및 나눗셈 없이 다음과 같이 구현할 수 있다.

``` c
#include <stdint.h>

uint32_t randu(uint32_t previous)
{
    return (previous + (previous << 1) + (previous << 16)) & 0x7fffffff;
}
```

하지만 이러한 특성은 난수의 품질에 결정적으로 영향을 미친다. 이를 알아 보기 위해서 \(X_n\)이 알려져 있을 때 그 다음 두 난수를 생성하면,

  -
    <math>\\begin{align}

X_{n+1} &{}= (2^{16} + 3) X_n \\mod {2^{31}} \\\\ X_{n+2} &{}= (2^{16} + 3) X_{n+1} \\mod {2^{31}} \\\\

`       &{}= (2^{16} + 3)^2 X_n \mod {2^{31}} \\`
`       &{}= (2^{32} + 6 \cdot 2^{16} + 9) X_n \mod {2^{31}} \\`
`       &{}= (6 \cdot (2^{16} + 3) - 9) X_n \mod {2^{31}} \\`
`       &{}= (6 X_{n+1} - 9 X_n) \mod {2^{31}}`

\\end{align}</math>

따라서 연속된 세 난수가 매우 강한 선형 상관 관계를 가지고 있음을 알 수 있다. (이 과정을 이해하기 위해서는 [합동 산술을](../Page/합동_산술.md "wikilink") 참고하라.) 대부분의 ‘좋은’ 선형 합동 생성기는 이보다 훨씬 큰 계수를 가진 선형 상관 관계를 이루기 때문에 비교적 큰 문제를 보이지 않는다.

## 영향

RANDU는 1970년대 초반까지 [몬테 카를로 시뮬레이션에](https://ko.wikipedia.org/wiki/몬테_카를로_시뮬레이션 "wikilink") 자주 사용되었으나, 다른 선형 합동 생성기보다도 못한 난수의 품질 때문에 당시 RANDU를 사용한 많은 실험 결과의 정확성에 큰 의문점을 안겨 주었다. 《Numerical Recipes》 시리즈에서 저자들은 다음과 같은 사례를 소개한 바 있다.

  -
    우리 중 한 사람은 단지 11개의 평면으로 이루어진 ‘무작위적인’ 그래프를 만든 뒤 그가 있던 컴퓨터 센터의 프로그래밍 컨설턴트가 난수 생성기를 잘못 사용했다고 말했던 일을 회고했다. “우리는 각 난수가 독립적으로 무작위적이라는 걸 보장하지, 둘 이상의 난수들이 무작위적이라는 건 보장하지 않습니다.”

## 참고 문헌

  - Donald E. Knuth, *The Art of Computer Programming, Volume 2*, 3rd edition (Addison-Wesley, Boston, 1998).
  - Marsaglia, George (1968), "Random Numbers Fall Mainly in the Planes," *Proc National Academy of Sciences* **61**, 25-28.
  - Press, William H., et al. (1992). *Numerical Recipes in Fortran 77: The Art of Scientific Computing*, 2nd edition. .

[분류:유사난수 생성기](https://ko.wikipedia.org/wiki/분류:유사난수_생성기 "wikilink") [분류:소프트웨어 버그](https://ko.wikipedia.org/wiki/분류:소프트웨어_버그 "wikilink")

1.  Compaq Fortran Language Reference Manual (Order Number: AA-Q66SD-TK) September 1999 (formerly DIGITAL Fortran and DEC Fortran 90)