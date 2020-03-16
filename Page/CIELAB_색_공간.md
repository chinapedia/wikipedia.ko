> This article is converted from Wikipedia: [CIELAB  ](https://ko.wikipedia.org/wiki/CIELAB__).


[섬네일](https://ko.wikipedia.org/wiki/파일:Lab_color_space.png "wikilink") 에 해당하는 영역만을 보여주는 그림. 각 사각형은 -128에서 128까지의 영역을 나타낸다.\]\]

**Lab 색 공간**은 인간 시각의 길항 이론에 의거하여, [CIE XYZ 색 공간을](../Page/CIE_1931_색_공간.md "wikilink") 비선형 변환하여 만들어진 [색 공간이다](../Page/색_공간.md "wikilink").

원래 Lab 색 공간이라는 용어는 **Hunter 1948 Lab 색 공간**을 가리켰으나, 현대에 들어 **CIE 1976 L\*a\*b\* 색 공간**을 가리키게 되었다. 두 색 공간 모두 인간의 색채 지각에 대한 연구를 바탕으로 한 CIE XYZ 색 공간을 변환하여 만들어졌다. 두 색 공간의 차이는, Hunter 1948 색 공간은 2차함수를 바탕으로 한 변환이며, CIE 1976 색 공간은 3차함수를 바탕으로 한 변환이라는 차이가 있다. 또한, 양쪽 모두 [먼셀 색 체계에](https://ko.wikipedia.org/wiki/먼셀_색_체계 "wikilink") 영향을 받아, XYZ 색 공간보다 균일한 색 체계를 목표로 하였다. 여기서 균일한 색 체계는, 색 공간에서 같은 거리만큼 떨어진 색채가, 인간의 눈에 같은 크기만큼의 색 차이로 인지되는 것을 목표로 했다는 의미이다.

Lab 색 공간은 XYZ에서 정의된 흰색에 대한 상대값으로 정의되어 있다. 따라서 흰색의 값에 따라 서로 다른 색을 가리킬 수 있다. 보통 [CIE 표준 광원인](https://ko.wikipedia.org/wiki/CIE_표준_광원 "wikilink") D50이 많이 쓰이지만, 환경에 따라 서로 다른 광원을 사용할 수 있다.

L\*a\*b\* 색 공간은 [RGB나](../Page/RGB_가산혼합.md "wikilink") [CMYK가](https://ko.wikipedia.org/wiki/CMYK_감산혼합 "wikilink") 표현할 수 있는 모든 [색역](../Page/색역.md "wikilink")을 포함하며, 인간이 지각할 수 없는 색깔도 포함하고 있다.

## 장점

Lab 색 공간의 가장 큰 장점은 RGB나 CMYK와 달리 매체에 독립적이라는 것이다. 디스플레이 장비나 인쇄 매체에 따라 색이 달라지는 색 공간과 달리 L\*a\*b\* 색 공간은 인간의 시각에 대한 연구를 바탕으로 정의되었다. 특히 휘도 축인 L 값은 인간이 느끼는 밝기에 대응하도록 설계되었다.

Lab 색 공간의 색역은 컴퓨터 디스플레이나 인쇄 매체는 물론 인간이 지각할 수 있는 색 영역보다도 훨씬 크다. 따라서 RGB나 CMYK보다 더 정밀한 값으로 표현해야 한다. 80년대까지 대부분의 이미지 포맷은 8비트만을 지원하였으므로 Lab 색 공간을 표현하기에 부적합했으나, 지금은 대부분의 포맷이 16비트 이미지를 지원하므로 이러한 문제가 없다.

## CIE L\*a\*b\*

CIE L\*a\*b\* 색 공간에서 *L\** 값은 밝기를 나타낸다. *L\** = 0 이면 검은색이며, *L\** = 100 이면 흰색을 나타낸다. *a\**은 빨강과 초록 중 어느쪽으로 치우쳤는지를 나타낸다. *a\**이 음수이면 초록에 치우친 색깔이며, 양수이면 빨강/보라 쪽으로 치우친 색깔이다. *b\**은 노랑과 파랑을 나타낸다. *b\**이 음수이면 파랑이고 *b\**이 양수이면 노랑이다.

또한, 인간의 색 지각이 비선형이라는 연구 결과에 따라, L\*a\*b\* 색 공간은 실제 빛의 파장과 비선형적 관계를 갖는다. 또한 L\*a\*b\* 공간에서 서로 다른 두 색의 거리는 인간이 느끼는 색깔의 차이와 비례하도록 설계되었다.

RGB 및 CMYK 색 공간은 매체에 독립적이지 않기 때문에, 이들 색 공간을 L\*a\*b\* 색 공간으로 변환하려면 먼저 [sRGB](https://ko.wikipedia.org/wiki/sRGB "wikilink")나 [어도비 RGB](https://ko.wikipedia.org/wiki/어도비_RGB "wikilink") 등의 절대 색 공간으로 변환해야 한다.

## CIEXYZ 와의 관계

### 변환

\[\begin{align}
  L^\star &= 116 f(Y/Y_n) - 16\\
  a^\star &= 500 \left[f(X/X_n) - f(Y/Y_n)\right]\\
  b^\star &= 200 \left[f(Y/Y_n) - f(Z/Z_n)\right]
\end{align}\]

여기서 *f*(*t*)는 다음과 같다

\[f(t) = \begin{cases}
  t^{1/3} & \text{if } t > (\frac{6}{29})^3 \\
  \frac13 \left( \frac{29}{6} \right)^2 t + \frac{4}{29} & \text{otherwise}
\end{cases}\]

*X*<sub>*n*</sub>, *Y*<sub>*n*</sub> 및 *Z*<sub>*n*</sub> 은 CIE XYZ를 표준 흰색에 대해 정규화한 값이다.

### 역변환

역변환은 위의 'f'' 함수의 역을 취하여 계산할 수 있다.

\[\begin{align}
  Y &= Y_n f^{-1}\left(\tfrac{1}{116}\left(L^*+16\right)\right)\\
  X &=  X_n f^{-1}\left(\tfrac{1}{116}\left(L^*+16\right) + \tfrac{1}{500}a^*\right)\\
  Z &=  Z_n f^{-1}\left(\tfrac{1}{116}\left(L^*+16\right) - \tfrac{1}{200}b^*\right)\\
\end{align}\]

\[f^{-1}(t) = \begin{cases}
  t^3 & \text{if } t > \tfrac{6}{29} \\
3\left(\tfrac{6}{29}\right)^2\left(t - \tfrac{4}{29}\right) & \text{otherwise}
\end{cases}\]

[\*](https://ko.wikipedia.org/wiki/분류:색_공간 "wikilink")