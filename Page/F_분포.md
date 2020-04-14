> This article is converted from Wikipedia: [F 분포](https://ko.wikipedia.org/wiki/F_분포).


{(d_1\\,x+d_2)^{d_1+d_2}}}} {x\\,\\mathrm{B}\\\!\\left(\\frac{d_1}{2},\\frac{d_2}{2}\\right)}\\\!</math> | cdf = \(I_{\frac{d_1 x}{d_1 x + d_2}}(d_1/2, d_2/2)\!\) | 기대값 = \(\frac{d_2}{d_2-2}\!\) for \(d_2 > 2\) | 중앙값 = | 최빈값 = \(\frac{d_1-2}{d_1}\;\frac{d_2}{d_2+2}\!\) for \(d_1 > 2\) | 분산 = \(\frac{2\,d_2^2\,(d_1+d_2-2)}{d_1 (d_2-2)^2 (d_2-4)}\!\) for \(d_2 > 4\) | 왜도 = \(\frac{(2 d_1 + d_2 - 2) \sqrt{8 (d_2-4)}}{(d_2-6) \sqrt{d_1 (d_1 + d_2 -2)}}\!\)
for \(d_2 > 6\) | 첨도 = 본문 참조 | mgf = 존재하지 않음 | 특성함수 = 본문 참조 }}

**F 분포**(F-distribution 또는 Snedecor's F distribution 또는 Fisher–Snedecor distribution)은 [통계학](../Page/통계학.md "wikilink")에서 사용되는 [연속 확률 분포로](https://ko.wikipedia.org/wiki/연속_확률_분포 "wikilink"), [F 검정과](https://ko.wikipedia.org/wiki/F테스트 "wikilink") [분산분석](https://ko.wikipedia.org/wiki/분산분석 "wikilink") 등에서 주로 사용된다.

두 [확률변수](https://ko.wikipedia.org/wiki/확률변수 "wikilink") \(V_1, V_2\)가 각각 [자유도가](https://ko.wikipedia.org/wiki/자유도_\(통계학\) "wikilink") \(k_1, k_2\)이고 서로 [독립인](../Page/독립_\(확률론\).md "wikilink") [카이제곱 분포를](../Page/카이제곱_분포.md "wikilink") 따른다고 할 때, 다음과 같이 정의되는 확률변수 F는 자유도가 (\(k_1, k_2\))인 F-분포를 따른다고 한다.

\(F=\frac{V_1/k_1}{V_2/k_2} \sim F(k_1,k_2)\)

F분포 *F*(*d*<sub>1</sub>, *d*<sub>2</sub>)를 따르는 무작위 변수의 [확률 밀도 함수는](https://ko.wikipedia.org/wiki/확률_밀도_함수 "wikilink") 다음과 같다.

\[g(x) = \frac{1}{\mathrm{B}(d_1/2, d_2/2)} \; \left(\frac{d_1\,x}{d_1\,x + d_2}\right)^{d_1/2} \; \left(1-\frac{d_1\,x}{d_1\,x + d_2}\right)^{d_2/2} \; x^{-1}\]

  -
    여기서 [실수](https://ko.wikipedia.org/wiki/실수 "wikilink") *x* ≥ 0에 대해 *d*<sub>1</sub>과 *d*<sub>2</sub>는 양의 정수이며, B는 [베타 함수이다](../Page/베타_함수.md "wikilink").

[누적 분포 함수는](../Page/누적_분포_함수.md "wikilink") 다음과 같다.

\[G(x) = I_{\frac{d_1 x}{d_1 x + d_2}}(d_1/2, d_2/2)\] 여기에서 *I*는 정규화 [불완전 베타 함수이다](https://ko.wikipedia.org/wiki/불완전_베타_함수 "wikilink").

[특성함수는](../Page/특성함수_\(확률론\).md "wikilink") 다음과 같다.

\[\varphi^F_{\nu_1, \nu_2} = M\left(\frac{\nu_1}{2}, -\frac{\nu_2}{2}, -i\frac{\nu_2}{\nu_1}t \right)\]

## 같이 보기

  - [분산 분석](../Page/분산_분석.md "wikilink")(analysis of variance, ANOVA)
  - [회귀 분석](../Page/회귀_분석.md "wikilink")(regression analysis)

[분류:연속분포](https://ko.wikipedia.org/wiki/분류:연속분포 "wikilink") [분류:분산 분석](https://ko.wikipedia.org/wiki/분류:분산_분석 "wikilink")