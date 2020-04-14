> This article is converted from Wikipedia: [GNU 어셈블러](https://ko.wikipedia.org/wiki/GNU_어셈블러).


**GNU 어셈블러**(GNU Assembler, 보통 **gas** 또는 간단히 **as**로 불리는)는 [GNU 프로젝트에서](../Page/GNU_프로젝트.md "wikilink") 사용되는 [어셈블러](https://ko.wikipedia.org/wiki/어셈블러 "wikilink")이다. 이것은 [GCC](https://ko.wikipedia.org/wiki/GCC "wikilink")의 기본 [백엔드](https://ko.wikipedia.org/wiki/백엔드 "wikilink")이며 [GNU 운영 체제와](https://ko.wikipedia.org/wiki/GNU_운영_체제 "wikilink") [리눅스 커널](../Page/리눅스_커널.md "wikilink") 그리고 다양한 다른 소프트웨어를 어셈블하는데 사용된다. GNU 어셈블러는 [GNU 바이너리 유틸리티의](../Page/GNU_바이너리_유틸리티.md "wikilink") 한 부분이다.

GAS [실행 파일은](../Page/실행_파일.md "wikilink") 이름이 as이며 [유닉스](../Page/유닉스.md "wikilink") 어셈블러의 표준 이름이다. GAS는 [크로스 플랫폼이며](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") 여러 다양한 컴퓨터 구조에서 실행되고 어셈블을 할 수 있다. [GNU 일반 공중 사용 허가서](../Page/GNU_일반_공중_사용_허가서.md "wikilink") v3 하에 배포되며 도한 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink").

## 일반적인 문법

GAS는 지원되는 모든 구조에서 동작하는 일반 문법을 지원한다. 이 일반 문법은 어셈블러 지시자와 주석의 방식을 포함한다.

### 지시자

GAS는 [C 언어에서](https://ko.wikipedia.org/wiki/C_언어 "wikilink") 전처리문과 비슷하게 동작하는, 키워드인 어셈블러 지시자를 사용한다. 대부분의 사용 가능한 어셈블러 지시자들이 대상 구조와 상관 없이 사용 가능하지만 몇몇 지시자들은 기게에 의존적이기도 하다.\[1\]

### 지원하는 주석

GAS는 두 스타일의 주석을 지원한다:\[2\]

#### 다중 라인 주석

C 멀티 라인 주석 처럼 사선과 별표 쌍을 사용해 시작과 끝을 표시한다:

`  `
` /*`
` 주석`
` */`
` `

#### 단일 라인 주석

단일 라인 주석은 어셈블되는 아키텍처에 따라서 몇몇의 다른 포맷들이 존재한다.

  - [해시 기호](https://ko.wikipedia.org/wiki/해시_기호 "wikilink")(\#)는 다음과 같은 플랫폼에서 사용된다: [i386](../Page/인텔_80386.md "wikilink"), [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink"), [i960](../Page/인텔_i960.md "wikilink"), 68HC11, 68HC12, VAX, V850, M32R, [파워PC](../Page/파워PC.md "wikilink"), [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink") 그리고 M880x0.
  - [쌍반점](../Page/쌍반점.md "wikilink")(;)은 다음에서 사용된다: AMD 29k 패밀리, ARC, H8/300 패밀리, [HPPA](../Page/PA-RISC.md "wikilink"), PDP-11, picoJava, 모토롤라, 그리고 [M32C](../Page/르네사스_테크놀로지.md "wikilink").
  - [골뱅이표](../Page/골뱅이표.md "wikilink")(@)는 ARM 플랫폼에서 사용된다.
  - 쌍 [빗금](../Page/빗금.md "wikilink")(//)은 [AArch64](../Page/ARM_아키텍처.md "wikilink") 플랫폼에서 사용된다.

## 사용

GCC라는 유명한 컴파일러의 백엔드로서 GNU 어셈블러는 현대 오픈 소스 소프트웨어를 컴파일할 때 매우 폭넓게 사용된다. GAS는 GNU 소프트웨어와 함께 GNU/리눅스 운영 체제에서 어셈블러로 사용된다. GAS의 수정된 버전은 또한 [매킨토시](../Page/매킨토시.md "wikilink") 운영 체제의 개발 툴 패키지에서도 볼 수 있다.

## 예시 프로그램

[IA-32](../Page/IA-32.md "wikilink") [리눅스](../Page/리눅스.md "wikilink")에서 표준 AT\&T 문법을 사용하는 표준 “Hello, world\!” 프로그램:

``` asm
.global _start

.text
_start:
    movl $4, %eax
    movl $1, %ebx
    movl $msg, %ecx
    movl $len, %edx
    int $0x80

    movl $1, %eax
    movl $0, %ebx
    int $0x80
.data
msg:
    .ascii "Hello, world!\n"
    len = . - msg
```

## 비판

인텔 문법에 익숙한 이들은 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")과 [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") 플랫폼에서의 어셈블리에 대한 인텔 문법을 지원하지 않는 다는 것이 문제가 된다고 주장한다.

그러나 버전 2.10부터 인텔 문법이 `.intel_syntax` 지시자의 사용을 통해 사용 가능해 졌다.\[3\]\[4\]\[5\]

## 같이 보기

  - [GNU 툴체인](https://ko.wikipedia.org/wiki/GNU_툴체인 "wikilink")
  - [바이너리 파일 디스크립터 라이브러리](../Page/바이너리_파일_디스크립터_라이브러리.md "wikilink")

## 각주

## 외부 링크

  -
  - [Gas manual](http://sourceware.org/binutils/docs/as/)

  -
[분류:어셈블러](https://ko.wikipedia.org/wiki/분류:어셈블러 "wikilink") [분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.
2.
3.
4.
5.