> This article is converted from Wikipedia: [IEEE 754](https://ko.wikipedia.org/wiki/IEEE_754).


**[IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") 754**는 [전기 전자 기술자 협회](../Page/전기_전자_기술자_협회.md "wikilink")(IEEE)에서 개발한 [컴퓨터](../Page/컴퓨터.md "wikilink")에서 [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink")을 표현하는 가장 널리 쓰이는 [표준](https://ko.wikipedia.org/wiki/표준 "wikilink")이다. ±[0](https://ko.wikipedia.org/wiki/0 "wikilink") 등의 수와 [무한](https://ko.wikipedia.org/wiki/무한 "wikilink"), [NaN](https://ko.wikipedia.org/wiki/NaN "wikilink") 등의 기호를 표시하는 법과 이러한 수에 대한 연산을 정의하고 있다. 가장 최신 버전인 IEEE 754-2019가 2019년 6월에 배포되었다. IEEE 754-2019는 2008년 8월에 배포된 직전 버전인 [IEEE 754-2008의](https://ko.wikipedia.org/wiki/IEEE_754-2008 "wikilink") 일부가 수정된 버전이다. IEEE 754-2008은 [IEEE 754-1985의](https://ko.wikipedia.org/wiki/IEEE_754-1985 "wikilink") 거의 대부분과 [IEEE 854-1987 Standard for Radix-independent Floating-Point Arithmetic을](https://ko.wikipedia.org/wiki/IEEE_854-1987 "wikilink") 포함하고 있다.

IEEE 754에는 32 비트 단정도(single-precision), 64 비트 배정도(double-precision), 43 비트 이상의 확장단정도(거의 쓰이지 않음), 79 비트 이상의 확장배정도(일반적으로 80비트로 구현됨)에 대한 형식을 정의하고 있다. 이중 32 비트 단정도는 반드시 구현해야 하며, 다른 형식은 선택사항이다. 많은 프로그래밍 언어에서 IEEE 표준을 따르도록 정의하고 있다. 예를 들어 [C에서는](../Page/C_\(프로그래밍_언어\).md "wikilink") `float`는 단정도, `double`은 배정도와 대응된다.

## 정의

IEEE 754 부동 소수점 표기 표준은 다음과 같이 항목들을 정의한다.

  - 산술 형식: 유한한 수들(0을 포함한)과 무한대와 NaN(Not a number)값으로 구성된 2진수와 10진수의 부동 소수점 데이터 집합
  - 형식의 교환: 부동 소수점 데이터를 효율적이고 압축적으로 전환할 수도 있는 인코딩
  - 반올림 규칙: 산수와 전환의 과정에서 반올림을 할 때의 성질
  - 작동: 산수와 산술 형식의 처리 방법 형식
  - 예외 처리: 예외적인 조건의 표기 (0으로의 나누는 작업, 오버플로우 등)

IEEE 754에 이 외에도 더 복잡한 예외 처리, 추가적인 작업(삼각함수 등), 표현의 평가, 그리고 생산 가능한 결과의 성취를 위한 여러 방법이 포함되어 있다.

## 구조

IEEE 754의 부동 소수점 표현은 크게 세 부분으로 구성되는데, [최상위 비트는](https://ko.wikipedia.org/wiki/최상위_비트 "wikilink") 부호를 표시하는 데 사용되며, 지수 부분(exponent)과 가수 부분(fraction/mantissa)이 있다.

[center](https://ko.wikipedia.org/wiki/파일:General_floating_point_ko.svg "wikilink")

  - 예시

−118.625 (십진법)을 IEEE 754 (32비트 단정도)로 표현해 보자.

  - 음수이므로, 부호부는 1이 된다.
  - 그 다음, [절댓값](https://ko.wikipedia.org/wiki/절댓값 "wikilink")을 [이진법](https://ko.wikipedia.org/wiki/이진법 "wikilink")으로 나타내면 1110110.101<sub>(2)</sub>이 된다.
  - 소수점을 왼쪽으로 이동시켜, 왼쪽에는 1만 남게 만든다. 예를 들면 1110110.101<sub>(2)</sub>=1.110110101<sub>(2)</sub>×2⁶ 과 같다. 이것을 정규화된 부동소수점 수라고 한다.
  - 가수부는 소수점의 오른쪽 부분으로, 부족한 비트 수 부분만큼 0으로 채워 23비트로 만든다. 결과는 11011010100000000000000 이 된다.
  - 지수는 6이므로, Bias를 더해야 한다. 32비트 IEEE 754 형식에서는 Bias는 127이므로 6+127 = 133이 된다. 이진법으로 변환하면 10000101<sub>(2)</sub>이 된다.

이 결과를 정리해서 표시하면 다음과 같다.\[1\]

[파일:Float point example frac.svg](https://ko.wikipedia.org/wiki/파일:Float_point_example_frac.svg "wikilink")

## 각주

[분류:컴퓨터 산술](https://ko.wikipedia.org/wiki/분류:컴퓨터_산술 "wikilink") [분류:IEEE 표준](https://ko.wikipedia.org/wiki/분류:IEEE_표준 "wikilink") [분류:부동소수점](https://ko.wikipedia.org/wiki/분류:부동소수점 "wikilink")

1.