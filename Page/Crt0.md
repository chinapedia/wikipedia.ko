> This article is converted from Wikipedia: [Crt0](https://ko.wikipedia.org/wiki/Crt0).


**`crt0`** (또는 **`c0`**)는 C로 작성된 프로그램의 메인 함수를 호출하기 전에 필요한 초기화를 수행하는 루틴(execution startup routines)의 집합으로 프로그램에 링크되어 있다. 이것은 보통 `crt0.o`라고 불리는 [목적 파일](https://ko.wikipedia.org/wiki/목적_파일 "wikilink") 형태로, 흔히 [어셈블리어](https://ko.wikipedia.org/wiki/어셈블리어 "wikilink")로 작성되며, 빌드 시에 [링커에](https://ko.wikipedia.org/wiki/링커_\(컴퓨팅\) "wikilink") 의해 자동으로 [실행 파일에](https://ko.wikipedia.org/wiki/실행_파일 "wikilink") 포함된다.\[1\]

`crt0`는 [런타임 라이브러리의](https://ko.wikipedia.org/wiki/런타임_라이브러리 "wikilink") 가장 기본적인 부분을 포함한다. 정확히 하는 일은 프로그램의 컴파일러, 운영체제 그리고 [C 표준 라이브러리의](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") 구현에 달려 있다.\[2\] 환경과 [툴체인](https://ko.wikipedia.org/wiki/툴체인 "wikilink")에 필요한 초기화 작업 외에도, crt0는 C++의 전역 [생성자](https://ko.wikipedia.org/wiki/생성자 "wikilink")나 [GCC의](https://ko.wikipedia.org/wiki/GNU_컴파일러_모음 "wikilink") ((constructor)) 속성을 포함하는 C 함수를 실행하는 것 같이 프로그래머에 의해 정의된 추가적인 작업을 할 수 있다.\[3\]\[4\]

"crt"는 "C runtime"을, 0은 "맨 처음"을 의미한다. 이러한 이름을 가졌지만, GCC로 컴파일된, C가 아닌 언어의 프로그램에도 사용된다. 특수한 경우에는 crt0를 대체하는 버전이 사용되기도 한다. 예를 들면 [gprof](https://ko.wikipedia.org/wiki/gprof "wikilink") 프로파일러를 컴파일하려면 gcrt0이 필요하다.\[5\]

## 같이 보기

  - [엔트리 포인트](../Page/엔트리_포인트.md "wikilink")
  - [런타임 시스템](https://ko.wikipedia.org/wiki/런타임_시스템 "wikilink")

## 각주

## 외부 링크

  - [crt0.o vs crt1.o](http://lists.uclibc.org/pipermail/uclibc/2002-December/025943.html)
  - [Linux x86 program start-up](http://dbp-consulting.com/tutorials/debugging/linuxProgramStartup.html)
  - [Hello from a libc-free world\!](https://blogs.oracle.com/ksplice/entry/hello_from_a_libc_free)[(Part 1)](https://blogs.oracle.com/ksplice/entry/hello_from_a_libc_free), March 16, 2010
  - [Start Up Code란?](http://itsys.hansung.ac.kr/lec/assem/cstartupcode.html#3)

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.
2.
3.
4.
5.