> This article is converted from Wikipedia: [ANSI C](https://ko.wikipedia.org/wiki/ANSI_C).


**ANSI C**, **ISO C**, **표준 C**(Standard C)는 [미국 국립 표준 협회](https://ko.wikipedia.org/wiki/미국_국립_표준_협회 "wikilink")(ANSI)와 [국제 표준화 기구](../Page/국제_표준화_기구.md "wikilink")(ISO)가 출판한 [C 프로그래밍 언어의](../Page/C_\(프로그래밍_언어\).md "wikilink") 이후 표준들을 가리킨다. 역사적으로 이 이름들은 오리지널의 가장 잘 지원되는 버전의 표준(C89 또는 C90)을 가리켰다. C로 개발하는 소프트웨어 개발자들은 표준을 따르는 것을 권고받으며 그렇게 함으로써 컴파일러 간 [이식에](../Page/이식_\(컴퓨팅\).md "wikilink") 도움을 줄 수 있다.

## 역사

C를 위한 최초 표준은 ANSI에 의해 출판되었다. 이 문서가 최종적으로 [국제 표준화 기구](../Page/국제_표준화_기구.md "wikilink")(ISO)에 채택되었고 ISO가 게시한 최종 수정판들을 ANSI가 채택했음에도 불구하고 수많은 프로그래머들은 표준 참조를 위해 ANSI C를 사용하고 있다. 일부 소프트웨어 개발자들은 ISO C라는 용어를 사용하지만 표준화 기구에 상대적으로 중립적인 다른 이들은 표준 C로 부른다.

### C89

1983년, ANSI는 X3J11이라는 이름의 위원회를 설립하여 C의 표준 사양을 확립하였다. 이 표준은 1989년에 완성되어 ANSI X3.159-1989 "프로그래밍 언어 C"(Programming Language C)로 승인되었다. 이 버전의 언어는 ANSI C로 불리기도 한다. 나중에 C89라는 레이블을 사용하여 C99과 구별하게 된다.

### C90

서식 변화만을 제외하고 C89와 동일한 표준이 국제 표준화 기구에 의해 ISO/IEC 9899:1990로 승인되었으며,\[1\] C90으로 불리기도 한다. 그러므로 "C89"와 "C90"은 근본적으로 동일한 언어를 가리킨다.

이 표준은 ANSI/INCITS\[2\]와 ISO/IEC에 의해 철회되었다.\[3\]

### C95

1995년에 [ISO는](../Page/국제_표준화_기구.md "wikilink") ANSI-C 표준에 대한 개정 제1판인 확장판을 출판하였다. 최종 이름은 ISO/IEC 9899/AMD1:1995이며 별칭은 C95이다. 오류 정정 외에 언어 기능에 대한 추가적인 변경사항이 있었으며,\[4\]\[5\] 이를테면 다음과 같다:

  - 표준 라이브러리에서의 개선된 멀티바이트 및 [확장 문자](../Page/확장_문자.md "wikilink") 지원: `<wchar.h>`, `<wctype.h>` 및 [멀티바이트](https://ko.wikipedia.org/wiki/멀티바이트_문자_집합 "wikilink") [I/O](../Page/입출력.md "wikilink").
  - 언어에 대한 [이중 글자](https://ko.wikipedia.org/wiki/이중_글자 "wikilink") 추가
  - 연산자의 대체 사양을 위한 표준 매크로 사양 (예: `&&`의 경우 `and`)
  - 표준 매크로 `__STDC_VERSION__`의 사양

개정판 외에도 C90에 대해 2가지 기술적 정오표가 ISO에 의해 출판되었다:

  - ISO/IEC 9899 TCOR1 (1995년)
  - ISO/IEC 9899 TCOR2 (1996년)

#### C95 호환성을 위한 전처리기 테스트

``` c
#if defined(__STDC_VERSION__) && __STDC_VERSION__ >= 199409L

/* C95 compatible source code. */
#elif defined(__ANSI__)
/* C89 compatible source code. */
#endif
```

### C99

### C11

### C18

### 기타 관련 ISO 출판

  - ISO/IEC TR 19769:2004,\[6\] on library extensions to support Unicode transformation formats, integrated into C11
  - ISO/IEC TR 24731-1:2007,\[7\] on library extensions to support bounds-checked interfaces, integrated into C11
  - ISO/IEC TR 18037:2008,\[8\] on embedded C extensions
  - ISO/IEC TR 24732:2009,\[9\] on [decimal floating point](https://ko.wikipedia.org/wiki/decimal_floating_point "wikilink") arithmetic, superseded by ISO/IEC TS 18661-2:2015
  - ISO/IEC TR 24747:2009,\[10\] on special mathematical functions,
  - ISO/IEC TR 24731-2:2010,\[11\] on library extensions to support dynamic allocation functions
  - ISO/IEC TS 17961:2013,\[12\] on secure coding in C
  - ISO/IEC TS 18661-1:2014,\[13\] on [IEC 60559:2011](../Page/IEEE_754.md "wikilink")-compatible binary floating-point arithmetic
  - ISO/IEC TS 18661-2:2015,\[14\] on IEC 60559:2011-compatible [decimal floating point](https://ko.wikipedia.org/wiki/decimal_floating_point "wikilink") arithmetic
  - ISO/IEC TS 18661-3:2015,\[15\] on IEC 60559:2011-compatible interchange and extended floating-point types
  - ISO/IEC TS 18661-4:2015,\[16\] on IEC 60559:2011-compatible supplementary functions

TS 18661의 5번째 및 최종 부분, 소프트웨어 트랜잭셔널 메모리 사양, 병렬 라이브러리 확장을 포함하여 더 많은 기술 사양이 개발 중이며 승인을 대기하고 있다.\[17\]

## ANSI C를 지원하는 컴파일러

  - [Amsterdam Compiler Kit](https://ko.wikipedia.org/wiki/Amsterdam_Compiler_Kit "wikilink") (C K\&R 및 C89/90)
  - [ARM](../Page/ARM_홀딩스.md "wikilink") 리얼뷰(RealView)
  - [클랭](../Page/클랭.md "wikilink"): [LLVM](../Page/LLVM.md "wikilink") 백엔드 사용
  - [GCC](../Page/GNU_컴파일러_모음.md "wikilink") (완전한 C89/90, C99, C11)
  - HP C/ANSI C 컴파일러 (C89 및 C99)\[18\]
  - [IBM XL C/C++](https://ko.wikipedia.org/wiki/IBM_XL_C/C++ "wikilink") (C11, 버전 12.1부터 시작)\[19\]
  - [인텔의 ICC](../Page/인텔_C++_컴파일러.md "wikilink")
  - [LabWindows/CVI](https://ko.wikipedia.org/wiki/LabWindows/CVI "wikilink")
  - [LCC](https://ko.wikipedia.org/wiki/LCC_\(컴파일러\) "wikilink")
  - [오픈왓콤](https://ko.wikipedia.org/wiki/오픈왓콤 "wikilink") (C89/90 및 일부 C99)
  - [마이크로소프트 비주얼 C++](https://ko.wikipedia.org/wiki/비주얼_C++ "wikilink") (C89/90 및 일부 C99)
  - [Pelles C](https://ko.wikipedia.org/wiki/Pelles_C "wikilink") (C99 및 C11. 윈도우 전용)
  - [vbcc](https://ko.wikipedia.org/wiki/vbcc "wikilink") (C89/90 및 C99)
  - [타이니 C 컴파일러](https://ko.wikipedia.org/wiki/타이니_C_컴파일러 "wikilink") (C89/90 및 일부 C99)

## 같이 보기

  - [C18](https://ko.wikipedia.org/wiki/C18 "wikilink"), [C11](https://ko.wikipedia.org/wiki/C11 "wikilink"), [C99](../Page/C99.md "wikilink"), [C95](https://ko.wikipedia.org/wiki/C95 "wikilink"), [C90](https://ko.wikipedia.org/wiki/C90 "wikilink"), [C89](https://ko.wikipedia.org/wiki/C89 "wikilink")
  - [C와 C++의 호환성](https://ko.wikipedia.org/wiki/C와_C++의_호환성 "wikilink")
  - [C++20](../Page/C++20.md "wikilink"), [C++17](../Page/C++17.md "wikilink"), [C++14](../Page/C++14.md "wikilink"), [C++11](../Page/C++11.md "wikilink"), [C++TR1](../Page/C++_기술_보고서_1.md "wikilink"), [C++03](https://ko.wikipedia.org/wiki/C++03 "wikilink"), [C++98](https://ko.wikipedia.org/wiki/C++98 "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")

## 각주

## 외부 링크

  - [ISO C working group](http://www.open-std.org/jtc1/sc22/wg14/)

  - [*Draft ANSI C Standard* (ANSI X3J11/88-090)](https://web.archive.org/web/20161223125339/http://flash-gordon.me.uk/ansi.c.txt) (May 13, 1988), [Third Public Review](https://groups.google.com/group/comp.lang.c/msg/20b174b18cdd919d?hl=en)

  - [*Draft ANSI C Rationale* (ANSI X3J11/88-151)](https://docs.google.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BxVCLS4f8Sg5NWZmM2NjZWEtYmExMS00Y2EzLWE3ZTMtNzFmYjYwYzBiOTIw&hl=en_US) (Nov 18, 1988)

  - [*C Information Bulletin \#1* (ANSI X3J11/93-007)](https://docs.google.com/viewer?a=v&pid=explorer&chrome=true&srcid=0B-3PfyBhOSOxOTdjYmM1N2ItMmE0ZC00OGE3LTllODUtZDNkMDMzYWU3NDlk&hl=en_US) (May 27, 1992)

  - [ANSI C Yacc grammar](http://www.quut.com/c/ANSI-C-grammar-y.html)

      - [ANSI C grammar, Lex specification](http://www.lysator.liu.se/c/ANSI-C-grammar-l.html)

  -
  - {{

  -
[분류:ANSI 표준](https://ko.wikipedia.org/wiki/분류:ANSI_표준 "wikilink") [분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:프로그래밍 언어 표준](https://ko.wikipedia.org/wiki/분류:프로그래밍_언어_표준 "wikilink")

1.
2.  <http://www.techstreet.com/cgi-bin/detail?doc_no=incits_iso_iec%7C9899;product_id=232462>
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17. See a list at <http://en.cppreference.com/w/c/experimental> Visited 16 January 2016.
18.
19. [Support for ISO C11 added to IBM XL C/C++ compilers](http://www.ibm.com/developerworks/rational/library/support-iso-c11/index.html)