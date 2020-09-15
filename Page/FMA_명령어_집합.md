> This article is converted from Wikipedia: [FMA 명령어 집합](https://ko.wikipedia.org/wiki/FMA_명령어_집합).


**FMA 명령어 집합**()은 [단일 곱셈-누산기](../Page/단일_곱셈-누산기.md "wikilink")(FMA)계산을 하기위한 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 마이크로프로세서 명령어 집합에서의 128비트 SIMD명령어들이다. 여기에는 두가지의 종류가 있다.

  - **FMA3**는 [인텔](../Page/인텔.md "wikilink")의 [해스웰](https://ko.wikipedia.org/wiki/해스웰_\(마이크로아키텍처\) "wikilink") 마이크로아키텍처에서부터 지원된다.
  - **FMA4**는 2011년에 발표하는 [AMD의](../Page/어드밴스트_마이크로_디바이시스.md "wikilink") AMD 프로세서에서부터 지원될 예정이다.

## 새 명령어들

FMA3와 FMA4 명령어 집합은 기능면에서는 거의 동일하지만 상호 호환은 되지 않는다. 이 둘은 부동소수점 연산과 [SIMD](../Page/SIMD.md "wikilink")연산을 위한 [단일 곱셈-누산기](../Page/단일_곱셈-누산기.md "wikilink")(FMA) 명령어들이다.

## 호환성 문제

FMA3와 FMA4의 차이점은 명령어가 세개의 피연산자(operand)를 갖느냐 네개의 피연산자를 갖느냐이다. 이 차이점은 호환성 문제를 야기한다. [단일 곱셈-누산기](../Page/단일_곱셈-누산기.md "wikilink")(FMA)는 다음과 같은 형태로 이루어진다.

\(d=a+b\times c\)

FMA4는 네개의 피연산자가 네개의 [프로세서 레지스터를](../Page/프로세서_레지스터.md "wikilink") 사용하고 FMA3는 세개의 피연산자와 세개의 레지스터를 사용한다. 따라서 d 가 a와 같다. FMA3는 코드가 좀 더 짧게 되며 하드웨어의 구현이 좀 더 단순한반면 FMA4는 프로그램의 유연성을 제공한다.

## FMA3 명령어 집합

### FMA3지원 CPU

  - [인텔](../Page/인텔.md "wikilink")
      - 인텔은 22nm공정기술을 사용하는 하스웰부터 지원한다.
  - AMD
      - FMA3 지원은 호환성을 위해 [파일드라이버_(마이크로아키텍처)](../Page/파일드라이버_\(마이크로아키텍처\).md "wikilink")부터 시작되었다.\[1\]\[2\] 트리니티를 기반으로 한 2세대 APU는 2012년 5월 15일 이후 출시된 제품에 FMA3 명령어를 지원이 추가되었다. [파일드라이버_(마이크로아키텍처)](../Page/파일드라이버_\(마이크로아키텍처\).md "wikilink") 기반 2세대 불도저 아키텍처는 2012년 10월 23일부터 출시된 이후 제품부터 FMA3 명령어를 지원한다.

### Excerpt from FMA3

| Mnemonic (AT\&T) | 피연산자               | 연산               |
| ---------------- | ------------------ | ---------------- |
| VFMADD132PDx     | xmm, xmm, xmm/m128 | $0 = $0\*$2 + $1 |
| VFMADD132PDy     | ymm, ymm, ymm/m256 | $0 = $0\*$2 + $1 |
| VFMADD213PDx     | xmm, xmm, xmm/m128 | $0 = $1\*$0 + $2 |
| VFMADD213PDy     | ymm, ymm, ymm/m256 | $0 = $1\*$0 + $2 |
| VFMADD231PDx     | xmm, xmm, xmm/m128 | $0 = $1\*$2 + $0 |
| VFMADD231PDy     | ymm, ymm, ymm/m256 | $0 = $1\*$2 + $0 |
| VFMADD132PSx     | xmm, xmm, xmm/m128 | $0 = $0\*$2 + $1 |
| VFMADD132PSy     | ymm, ymm, ymm/m256 | $0 = $0\*$2 + $1 |
| VFMADD213PSx     | xmm, xmm, xmm/m128 | $0 = $1\*$0 + $2 |
| VFMADD213PSy     | ymm, ymm, ymm/m256 | $0 = $1\*$0 + $2 |
| VFMADD231PSx     | xmm, xmm, xmm/m128 | $0 = $1\*$2 + $0 |
| VFMADD231PSy     | ymm, ymm, ymm/m256 | $0 = $1\*$2 + $0 |
| VFMADD132SD      | xmm, xmm, xmm/m64  | $0 = $0\*$2 + $1 |
| VFMADD213SD      | xmm, xmm, xmm/m64  | $0 = $1\*$0 + $2 |
| VFMADD231SD      | xmm, xmm, xmm/m64  | $0 = $1\*$2 + $0 |
| VFMADD132SS      | xmm, xmm, xmm/m32  | $0 = $0\*$2 + $1 |
| VFMADD213SS      | xmm, xmm, xmm/m32  | $0 = $1\*$0 + $2 |
| VFMADD231SS      | xmm, xmm, xmm/m32  | $0 = $1\*$2 + $0 |

## FMA4 명령어 집합

### FMA4지원 CPU

  - AMD
      - 2011년에 양산될 불도저 프로세서 코어\[3\].
  - 인텔
      - 인텔 프로세서에서 FMA4를 지원할지는 미정.

### Excerpt from FMA4

| Mnemonic (AT\&T) | 피연산자                         | 연산               |
| ---------------- | ---------------------------- | ---------------- |
| VFMADDPDx        | xmm, xmm, xmm/m128, xmm/m128 | $0 = $1\*$2 + $3 |
| VFMADDPDy        | ymm, ymm, ymm/m256, ymm/m256 | $0 = $1\*$2 + $3 |
| VFMADDPSx        | xmm, xmm, xmm/m128, xmm/m128 | $0 = $1\*$2 + $3 |
| VFMADDPSy        | ymm, ymm, ymm/m256, ymm/m256 | $0 = $1\*$2 + $3 |
| VFMADDSD         | xmm, xmm, xmm/m64, xmm/m64   | $0 = $1\*$2 + $3 |
| VFMADDSS         | xmm, xmm, xmm/m32, xmm/m32   | $0 = $1\*$2 + $3 |

## 내력

인텔과 AMD는 양사간에 FMA3와 FMA4의 코딩 기법에 대한 협력없이 서로의 지원 계획을 바꿈으로서 호환성 문제가 발생했다. AMD는 FMA3에서 FMA4로 변경을 했고 이와 거의 동시에 인텔은 FMA4에서 FMA3로 계획을 변경했다. 대략적인 내력은 다음과 같다.

  - 2007년 8월: AMD는 FMA3를 지원하는 SSE5 명령어 집합을 발표함. 세 피연산자를 갖는 명령어를 허용하는 새로운 코딩 기법(DREX)이 소개되었다.\[4\].
  - 2008년 4월: [인텔](../Page/인텔.md "wikilink")은 FMA4를 포함하는 [AVX와](../Page/고급_벡터_확장.md "wikilink") FMA명령어 집합을 발표함. 이 명령어들의 코딩은 AMD의 DREX보다 더 유연한 새로운 [VEX](https://ko.wikipedia.org/wiki/VEX "wikilink") 코딩 기법을 사용한다.\[5\].
  - 2008년 12월: 인텔은 FMA명령어 사양을 네개 피연산자에서 세개 피연산자로 변경함. VEX 코딩 기법은 여전히 유효\[6\].
  - 2009년 5월: AMD는 FMA명령어 사양을 세개 피연산자에서 네개 피연산자 VEX형태로 변경함. 그렇지만 이것은 2008년 12월 인텔 사양과 호환되는 것이 아니라 2008년 4월 인텔 사양과 호환됨.\[7\].

## 같이 보기

  - [SSE](https://ko.wikipedia.org/wiki/SSE "wikilink")
  - [SSE2](../Page/SSE2.md "wikilink")
  - [SSE3](../Page/SSE3.md "wikilink")
  - [SSE4](../Page/SSE4.md "wikilink")
  - [AVX](../Page/고급_벡터_확장.md "wikilink")

## 각주

[분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink") [분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink") [분류:SIMD 컴퓨팅](https://ko.wikipedia.org/wiki/분류:SIMD_컴퓨팅 "wikilink")

1.
2.
3.
4.
5.
6.
7.