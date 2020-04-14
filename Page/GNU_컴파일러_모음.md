> This article is converted from Wikipedia: [GNU 컴파일러 모음](https://ko.wikipedia.org/wiki/GNU_컴파일러_모음).


**GNU 컴파일러 모음**(, 줄여서 **GCC**)는 [GNU 프로젝트의](../Page/GNU_프로젝트.md "wikilink") 일환으로 개발되어 널리 쓰이고 있는 [컴파일러](../Page/컴파일러.md "wikilink")이다.

[자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink") 중에 가장 잘 알려진 것들 중 하나인 GCC는 원래 [C만을](../Page/C_\(프로그래밍_언어\).md "wikilink") 지원했던 컴파일러로 이름도 "GNU C 컴파일러"였다. 이러한 까닭에 현재에도 GCC는 GNU 컴파일러 모음의 일부인 **GNU C 컴파일러**()의 줄임말로 쓰이기도 한다. 그러나 나중에 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [포트란](../Page/포트란.md "wikilink"), [에이다](https://ko.wikipedia.org/wiki/에이다 "wikilink") 등 여러 언어를 컴파일할 수 있게 되면서, 현재의 이름으로 바뀌게 되었다.

## 개요

GCC는 [리처드 스톨만이](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink") 1987년 GNU 프로젝트의 컴파일러로 작성했다. GNU 프로젝트에 컴파일러가 없었기 때문에 이 개발은 자유 소프트웨어 재단이 후원하였다. 1997년 개발 과정은 공개되었으며, 속도 또한 빨라졌다. 1999년 첫 버전이 나왔다. 현재 GCC는 전 세계적으로 관리되고 있으며, 다양한 중앙 처리 장치를 처리할 수 있게 되었다.

GNU 시스템의 공식 컴파일러이므로 GCC는 많은 컴파일러와 운영 체제를 만드는 데 사용되었다. 한편, 시스템 네이티브 컴파일러를 사용했을 때 비해서 GCC를 사용하면 같은 파서로 코드를 처리하므로 이식성을 향상시킬 수 있다. GCC는 상용 컴파일러에 비해서 느린 코드를 생성했지만 최근 많이 개선되었다.

## 지원 프로그래밍 언어

4.6 이후의 표준 컴파일러 릴리즈에는 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") (`gcc`), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") (`g++`), [오브젝티브 C](https://ko.wikipedia.org/wiki/오브젝티브_C "wikilink"), [오브젝티브 C++](https://ko.wikipedia.org/wiki/오브젝티브_C++ "wikilink"), [포트란](../Page/포트란.md "wikilink") ([`gfortran`](https://ko.wikipedia.org/wiki/gfortran "wikilink")), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") ([`gcj`](https://ko.wikipedia.org/wiki/gcj "wikilink")), [에이다](https://ko.wikipedia.org/wiki/에이다 "wikilink") ([GNAT](../Page/GNAT.md "wikilink")), [고](https://ko.wikipedia.org/wiki/고_\(프로그래밍_언어\) "wikilink") (`gccgo`)를 위한 프론트엔드가 포함되어 있다.\[1\] 또, 이용은 가능하지만 표준에는 포함되지 않은 것으로 [파스칼](../Page/파스칼_\(프로그래밍_언어\).md "wikilink") ([`gpc`](../Page/GNU_파스칼.md "wikilink")), [머큐리](../Page/머큐리_\(프로그래밍_언어\).md "wikilink"), [Modula-2](https://ko.wikipedia.org/wiki/Modula-2 "wikilink"), [Modula-3](https://ko.wikipedia.org/wiki/Modula-3 "wikilink"), [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink"), [D](../Page/D_\(프로그래밍_언어\).md "wikilink") (`gdc`),\[2\] [VHDL](../Page/VHDL.md "wikilink") (`ghdl`)가 있다. 잘 알려진 병렬 언어 확장 [OpenMP](../Page/OpenMP.md "wikilink")도 지원한다.

포트란 프론트엔드는 [포트란 77만](https://ko.wikipedia.org/wiki/포트란_77 "wikilink") 지원했던 버전 4.0 이전까지 `g77`였다. 새로운 버전에서 `g77`는 [포트란 2003의](https://ko.wikipedia.org/wiki/포트란_2003 "wikilink") 일부와 [포트란 95를](https://ko.wikipedia.org/wiki/포트란_95 "wikilink") 지원하는 새로운 [`gfortran`](https://ko.wikipedia.org/wiki/gfortran "wikilink") 프론트엔드를 선호하게 되면서 지원이 중단되었다.\[3\] 나중의 포트란 표준이 F77 표준을 포함하면서 표준 호환 F77 코드가 표준 호환 F90/95 코드가 되어 gfortran에서 문제 없이 컴파일이 가능하다. [CHILL](https://ko.wikipedia.org/wiki/CHILL "wikilink")을 위한 프론트엔드는 유지 보수 부족으로 개발이 중단되었다.\[4\]

일부 실험적인 브랜치들은 추가적인 언어들을 지원하기도 하는데, 이를테면 GCC UPC 컴파일러가 있다.\[5\]

## 지원 아키텍처

버전 4.3을 기준으로 GCC는 다음의 프로세서 계열을 대상으로 한다:

  - [알파](../Page/DEC_알파.md "wikilink")
  - [ARM](../Page/ARM_아키텍처.md "wikilink")
  - [AVR](https://ko.wikipedia.org/wiki/Atmel_AVR "wikilink")
  - [블랙핀](../Page/블랙핀.md "wikilink")
  - [Epiphany](https://ko.wikipedia.org/wiki/:en:Adapteva#Products "wikilink") (GCC 4.8)
  - [H8/300](https://ko.wikipedia.org/wiki/히타치_H8 "wikilink")
  - [HC12](https://ko.wikipedia.org/wiki/HC12 "wikilink")
  - [IA-32](../Page/IA-32.md "wikilink") ([x86](https://ko.wikipedia.org/wiki/x86 "wikilink"))
  - [IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink") (인텔 아이테니엄)
  - [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink")
  - [모토로라 68000](../Page/모토로라_68000.md "wikilink")
  - [PA-RISC](../Page/PA-RISC.md "wikilink")
  - [PDP-11](../Page/PDP-11.md "wikilink")
  - [PowerPC](https://ko.wikipedia.org/wiki/PowerPC "wikilink")
  - [R8C](https://ko.wikipedia.org/wiki/R8C "wikilink") / [M16C](https://ko.wikipedia.org/wiki/M16C "wikilink") / [M32C](https://ko.wikipedia.org/wiki/M32C "wikilink")
  - [SPARC](../Page/SPARC.md "wikilink")
  - [SPU](https://ko.wikipedia.org/wiki/:en:Synergistic_Processing_Unit "wikilink")
  - [SuperH](https://ko.wikipedia.org/wiki/SuperH "wikilink")
  - [시스템/390](https://ko.wikipedia.org/wiki/시스템/390 "wikilink") / [z시리즈](https://ko.wikipedia.org/wiki/z시리즈 "wikilink")
  - [VAX](../Page/VAX.md "wikilink")
  - [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink")

표준 릴리즈에서 지원되는, 위보다 잘 알려지지 않은 프로세서는 다음을 포함한다:

  - [68HC11](https://ko.wikipedia.org/wiki/68HC11 "wikilink")
  - [A29K](https://ko.wikipedia.org/wiki/A29K "wikilink")
  - [CR16](https://ko.wikipedia.org/wiki/CR16 "wikilink")
  - [C6x](https://ko.wikipedia.org/wiki/C6x "wikilink")
  - [D30V](https://ko.wikipedia.org/wiki/D30V "wikilink")
  - [DSP16xx](https://ko.wikipedia.org/wiki/DSP16xx "wikilink")
  - [ETRAX CRIS](https://ko.wikipedia.org/wiki/ETRAX_CRIS "wikilink")
  - [FR-30](https://ko.wikipedia.org/wiki/후지쯔_FR "wikilink")
  - [FR-V](https://ko.wikipedia.org/wiki/FR-V "wikilink")
  - [인텔 i960](../Page/인텔_i960.md "wikilink")
  - [IP2000](https://ko.wikipedia.org/wiki/IP2000 "wikilink")
  - [M32R](https://ko.wikipedia.org/wiki/M32R "wikilink")
  - [MCORE](https://ko.wikipedia.org/wiki/MCORE "wikilink")
  - [MIL-STD-1750A](https://ko.wikipedia.org/wiki/MIL-STD-1750A "wikilink")
  - [MMIX](../Page/MMIX.md "wikilink")
  - [MN10200](https://ko.wikipedia.org/wiki/MN10200 "wikilink")
  - [MN10300](https://ko.wikipedia.org/wiki/MN10300 "wikilink")
  - [모토로라 88000](https://ko.wikipedia.org/wiki/모토로라_88000 "wikilink")
  - [NS32K](https://ko.wikipedia.org/wiki/NS320xx "wikilink")
  - [ROMP](https://ko.wikipedia.org/wiki/ROMP "wikilink")
  - [RL78](https://ko.wikipedia.org/wiki/RL78 "wikilink")
  - [Stormy16](https://ko.wikipedia.org/wiki/Stormy16 "wikilink")
  - [V850](https://ko.wikipedia.org/wiki/V850 "wikilink")
  - [Xtensa](https://ko.wikipedia.org/wiki/Xtensa "wikilink")

FSF 버전과는 별개로 GCC 버전이 지원하고 있는 추가 프로세서들은 다음과 같다:

  - [Cortus APS3](https://ko.wikipedia.org/wiki/Cortus_APS3 "wikilink")
  - [ARC](https://ko.wikipedia.org/wiki/ARC_인터내셔널 "wikilink")
  - [AVR32](https://ko.wikipedia.org/wiki/AVR32 "wikilink")
  - [C166](https://ko.wikipedia.org/wiki/C166 "wikilink"), [C167](https://ko.wikipedia.org/wiki/C167 "wikilink")
  - [D10V](https://ko.wikipedia.org/wiki/D10V "wikilink")
  - [EISC](../Page/EISC.md "wikilink")
  - [eSi-RISC](https://ko.wikipedia.org/wiki/eSi-RISC "wikilink")
  - [헥사곤](https://ko.wikipedia.org/wiki/헥사곤_\(프로세서\) "wikilink")\[6\]
  - [LatticeMico32](https://ko.wikipedia.org/wiki/LatticeMico32 "wikilink")
  - [LatticeMico8](https://ko.wikipedia.org/wiki/LatticeMico8 "wikilink")
  - [MeP](https://ko.wikipedia.org/wiki/MeP "wikilink")
  - [MicroBlaze](https://ko.wikipedia.org/wiki/MicroBlaze "wikilink")
  - [모토로라 6809](https://ko.wikipedia.org/wiki/모토로라_6809 "wikilink")
  - [MSP430](https://ko.wikipedia.org/wiki/MSP430 "wikilink")
  - [NEC SX 아키텍처](https://ko.wikipedia.org/wiki/NEC_SX_아키텍처 "wikilink")\[7\]
  - [Nios II](https://ko.wikipedia.org/wiki/Nios_II "wikilink"), [Nios](https://ko.wikipedia.org/wiki/:en:Nios_embedded_processor "wikilink")
  - [오픈RISC](https://ko.wikipedia.org/wiki/오픈RISC "wikilink")
  - [PDP-10](../Page/PDP-10.md "wikilink")
  - [PIC24/dsPIC](https://ko.wikipedia.org/wiki/PIC30 "wikilink")
  - [PIC32](https://ko.wikipedia.org/wiki/PIC30 "wikilink")
  - [프로펠러](https://ko.wikipedia.org/wiki/패럴렉스_프로펠러 "wikilink")
  - [시스템/370](https://ko.wikipedia.org/wiki/시스템/370 "wikilink")
  - [TIGCC](https://ko.wikipedia.org/wiki/TIGCC "wikilink") ([m68k](https://ko.wikipedia.org/wiki/m68k "wikilink")의 변종)
  - [TriCore](https://ko.wikipedia.org/wiki/TriCore "wikilink")
  - [Z8000](https://ko.wikipedia.org/wiki/Z8000 "wikilink")

[gcj](https://ko.wikipedia.org/wiki/gcj "wikilink") 자바 컴파일러는 순수 기계어 아키텍처나 [자바 가상 머신의](../Page/자바_가상_머신.md "wikilink") [자바 바이트코드만을](../Page/자바_바이트코드.md "wikilink") 대상으로 할 수 있다.\[8\] 새로운 플랫폼으로 GCC의 대상으로 변경할 때에는 bootstrap이 자주 쓰인다.

## 호환 IDE

[리눅스](../Page/리눅스.md "wikilink") 및 일부 운영 체제용으로 개발된 대부분의 [통합 개발 환경은](../Page/통합_개발_환경.md "wikilink") GCC를 지원한다. 이를테면 다음을 포함한다.

  - [Anjuta](https://ko.wikipedia.org/wiki/Anjuta "wikilink")
  - [Code::Blocks](../Page/Code::Blocks.md "wikilink")
  - [코드라이트](https://ko.wikipedia.org/wiki/코드라이트 "wikilink")(CodeLite)
  - [Dev-C++](../Page/Dev-C++.md "wikilink")
  - [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")
  - [geany](https://ko.wikipedia.org/wiki/geany "wikilink")
  - [KDevelop](../Page/KDevelop.md "wikilink")
  - [NetBeans](https://ko.wikipedia.org/wiki/NetBeans "wikilink")
  - [Qt 크리에이터](https://ko.wikipedia.org/wiki/Qt_크리에이터 "wikilink")
  - [Xcode](https://ko.wikipedia.org/wiki/Xcode "wikilink") (엑스코드 4.1.0까지만 지원. 그 뒤에는 llvm-gcc라는 프론트엔드가 대신한다.)

## 버전 역사

| 버전         | 출시일\[9\]\[10\]         |
| ---------- | ---------------------- |
| 7.1.0      | 2017-05-02             |
| 6.3.0      | 2016-12-21             |
| 6.2.0      | 2016-08-22             |
| 4.9.4      | 2016-08-03             |
| 5.4.0      | 2016-06-03             |
| 6.1.0      | 2016-04-27             |
| 5.3.0      | 2015-12-04             |
| 5.2.0      | 2015-07-16             |
| 4.9.3      | 2015-06-26             |
| 4.8.5      | 2015-06-23             |
| 5.1.0      | 2015-04-22             |
| 5.0.0      | 2014-12-23             |
| 4.8.4      | 2014-12-19             |
| 4.9.2      | 2014-10-30             |
| 4.9.1      | 2014-07-16             |
| 4.7.4      | 2014-06-12             |
| 4.8.3      | 2014-05-22             |
| 4.9.0      | 2014-04-22             |
| 4.8.2      | 2013-10-16             |
| 4.8.1      | 2013-05-31             |
| 4.6.4      | 2013-04-12             |
| 4.7.3      | 2013-04-11             |
| 4.8.0      | 2013-03-22             |
| 4.7.2      | 2012-09-20             |
| 4.5.4      | 2012-07-02             |
| 4.7.1      | 2012-06-14             |
| 4.7.0      | 2012-03-22             |
| 4.4.7      | 2012-03-13             |
| 4.6.3      | 2012-03-01             |
| 4.6.2      | 2011-10-26             |
| 4.6.1      | 2011-06-27             |
| 4.3.6      | 2011-06-27             |
| 4.5.3      | 2011-04-28             |
| 4.4.6      | 2011-04-16             |
| 4.6.0      | 2011-03-25\[11\]       |
| 4.5.2      | 2010-12-16             |
| 4.4.5      | 2010-10-01             |
| 4.5.1      | 2010-07-31             |
| 4.3.5      | 2010-05-22             |
| 4.4.4      | 2010-04-29             |
| 4.5.0      | 2010-04-14             |
| 4.4.3      | 2010-01-21             |
| 4.4.2      | 2009-10-15             |
| 4.3.4      | 2009-08-04             |
| 4.4.1      | 2009-07-22             |
| 4.4.0      | 2009-04-21             |
| 4.3.3      | 2009-01-24             |
| 4.3.2      | 2008-08-27             |
| 4.3.1      | 2008-06-06             |
| 4.2.4      | 2008-05-19             |
| 4.3.0      | 2008-03-05             |
| 4.2.3      | 2008-02-01             |
| 4.2.2      | 2007-10-07             |
| 4.2.1      | 2007-07-18             |
| 4.2.0      | 2007-05-13             |
| 4.1.2      | 2007-02-13             |
| 4.0.4      | 2007-01-31             |
| 4.1.1      | 2006-05-24             |
| 4.0.3      | 2006-03-10             |
| 3.4.6      | 2006-03-06             |
| 4.1.0      | 2006-02-28             |
| 3.4.5      | 2005-11-30             |
| 4.0.2      | 2005-09-28             |
| 4.0.1      | 2005-07-07             |
| 3.4.4      | 2005-05-18             |
| 3.3.6      | 2005-05-03             |
| 4.0.0      | 2005-04-20\[12\]       |
| 3.4.3      | 2004-11-04             |
| 3.3.5      | 2004-09-30             |
| 3.4.2      | 2004-09-06             |
| 3.4.1      | 2004-07-01             |
| 3.3.4      | 2004-05-31             |
| 3.4.0      | 2004-04-18             |
| 3.3.3      | 2004-02-14             |
| 3.3.2      | 2003-10-17             |
| 3.3.1      | 2003-08-08             |
| 3.3        | 2003-05-13             |
| 3.2.3      | 2003-04-22             |
| 3.2.2      | 2003-02-05             |
| 3.2.1      | 2002-11-19             |
| 3.2        | 2002-08-14             |
| 3.1.1      | 2002-07-25             |
| 3.1        | 2002-05-15\[13\]       |
| 3.0.4      | 2002-02-20             |
| 3.0.3      | 2001-12-20             |
| 3.0.2      | 2001-10-25             |
| 3.0.1      | 2001-08-20             |
| 3.0        | 2001-06-18\[14\]\[15\] |
| 2.95.3     | 2001-03-16             |
| 2.95.2     | 1999-10-24             |
| 2.95.1     | 1999-08-19             |
| 2.95       | 1999-07-31\[16\]       |
| egcs 1.1.2 | 1999-03-15             |
| egcs 1.1.1 | 1998-12-01             |
| egcs 1.1   | 1998-09-03             |
| egcs 1.0.3 | 1998-05-15             |
| egcs 1.0.2 | 1998-03-16             |
| 2.8.1      | 1998-03-02             |
| 2.8.0      | 1998-01-07             |
| egcs 1.0.1 | 1998-01-06             |
| egcs 1.0   | 1997-12-03\[17\]       |
| 2.7.2.3    | 1997-08-22             |
| 2.7.2.2    | 1997-01-29             |

| 버전         | 출시일              |
| ---------- | ---------------- |
| 2.7.2.1    | 1996-06-29       |
| 2.7.2      | 1995-11-26       |
| 2.7.1      | 1995-11-12       |
| 2.7.0      | 1995-06-16       |
| 2.6.3      | 1994-11-30       |
| 2.6.2      | 1994-11-12       |
| 2.6.1      | 1994-11-01       |
| 2.6.0      | 1994-07-14       |
| 2.5.8      | 1994-01-24       |
| 2.5.7      | 1993-12-12       |
| 2.5.6      | 1993-12-03       |
| 2.5.5      | 1993-11-27       |
| 2.5.4      | 1993-11-16       |
| 2.5.3      | 1993-11-11       |
| 2.5.2      | 1993-11-01       |
| 2.5.1      | 1993-10-31       |
| 2.5.0      | 1993-10-22       |
| 2.4.5      | 1993-06-20       |
| 2.4.4      | 1993-06-19       |
| 2.4.3      | 1993-06-01       |
| 2.4.2      | 1993-05-31       |
| 2.4.1      | 1993-05-26       |
| 2.4.0      | 1993-05-17       |
| 2.3.3      | 1992-12-26       |
| 2.3.2      | 1992-11-27       |
| 2.3.1      | 1992-11-01       |
| 2.3        | 1992-10-31       |
| 2.2.2      | 1992-06-14       |
| 2.2.1      | 1992-06-09       |
| 2.2        | 1992-06-08       |
| 2.1        | 1992-03-24       |
| 2.0        | 1992-02-22\[18\] |
| g++ 1.42.0 | 1992-09-20       |
| 1.42       | 1992-09-20       |
| 1.41       | 1992-08-27       |
| g++ 1.41.0 | 1992-07-13       |
| g++ 1.40.3 | 1991-10-19       |
| 1.40       | 1991-06-01       |
| g++ 1.39.1 | 1991-05-04       |
| 1.39       | 1991-01-16       |
| 1.38       | 1990-12-21       |
| g++ 1.37.1 | 1990-03-01       |
| g++ 1.37.0 | 1990-02-28       |
| 1.37.1     | 1990-02-21       |
| 1.37       | 1990-02-11       |
| g++ 1.36.4 | 1990-01-30       |
| g++ 1.36.3 | 1990-01-16       |
| 1.36       | 1989-09-24       |
| 1.35       | 1989-04-26       |
| 1.34       | 1989-02-23       |
| 1.33       | 1989-02-01       |
| 1.32       | 1988-12-21       |
| 1.31       | 1988-11-19       |
| 1.30       | 1988-10-13       |
| 1.29       | 1988-10-06       |
| 1.28       | 1988-09-14       |
| 1.27       | 1988-09-05       |
| 1.26       | 1988-08-18       |
| 1.25       | 1988-08-03       |
| 1.24       | 1988-07-02       |
| 1.23       | 1988-06-26       |
| 1.22       | 1988-05-22       |
| 1.21       | 1988-05-01       |
| 1.20       | 1988-04-19       |
| 1.19       | 1988-03-29       |
| 1.18       | 1988-02-04       |
| 1.17       | 1988-01-09       |
| 1.16       | 1987-12-19       |
| g++ 1.15.3 | 1987-12-18       |
| 1.15       | 1987-11-28       |
| 1.14       | 1987-11-06       |
| 1.13       | 1987-10-12       |
| 1.12       | 1987-10-03       |
| 1.11       | 1987-09-05       |
| 1.10       | 1987-08-22       |
| 1.9        | 1987-08-18       |
| 1.8        | 1987-08-10       |
| 1.7        | 1987-07-21       |
| 1.6        | 1987-07-02       |
| 1.5        | 1987-06-18       |
| 1.4        | 1987-06-13       |
| 1.3        | 1987-06-10       |
| 1.2        | 1987-06-01       |
| 1.1        | 1987-05-24       |
| 1.0        | 1987-05-23       |
| 0.9        | 1987-03-22       |

## 참고 자료

  - [Richard M. Stallman](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink"): *[Using and Porting the GNU Compiler Collection](http://gcc.gnu.org/onlinedocs/gcc-2.95.3/gcc.html)*, [Free Software Foundation](../Page/자유_소프트웨어_재단.md "wikilink"),
  - Richard M. Stallman: *[Using Gcc: The Gnu Compiler Collection Reference](http://gcc.gnu.org/onlinedocs/gcc-3.3.1/gcc/)*, Free Software Foundation,
  - [Brian J. Gough](https://ko.wikipedia.org/wiki/Brian_J._Gough "wikilink"): *[An Introduction to GCC](https://archive.is/20121205072412/http://www.network-theory.co.uk/gcc/intro/)*, Network Theory Ltd.,

## 각주

  - 참조주

<!-- end list -->

  - 내용주

## 외부 링크

  - [GCC 홈페이지](http://gcc.gnu.org/)

  - [GCC 매뉴얼 목록](http://gcc.gnu.org/onlinedocs/)

  - [GCC 위키](http://gcc.gnu.org/wiki)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:C 컴파일러](https://ko.wikipedia.org/wiki/분류:C_컴파일러 "wikilink") [분류:C++ 컴파일러](https://ko.wikipedia.org/wiki/분류:C++_컴파일러 "wikilink") [분류:1987년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1987년_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink") [분류:파스칼 컴파일러](https://ko.wikipedia.org/wiki/분류:파스칼_컴파일러 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.  ["GCC Front Ends"](http://gcc.gnu.org/frontends.html), gnu.org, Retrieved November 25, 2011.
2.  {{ 웹 인용 |url=<http://bitbucket.org/goshawk/gdc/> |제목=gdc project on bitbucket |accessdate=3 July 2010 }}
3.  {{ 웹 인용|url=[http://gcc.gnu.org/wiki/Fortran2003|제목=Fortran](http://gcc.gnu.org/wiki/Fortran2003%7C제목=Fortran) 2003 Features in GNU Fortran }}
4.  [\[PATCH](http://gcc.gnu.org/ml/gcc-patches/2002-04/msg00887.html) Remove chill\], gcc.gnu.org, Retrieved July 29, 2010.
5.  {{ 웹 인용|url=<http://www.gccupc.org/> |제목=GCC UPC (GCC Unified Parallel C) | <http://www.gccupc.org/> |publisher=<http://www.gccupc.org/>\<\! |date=2006-02-20 |accessdate=2009-03-11 }}
6.  {{ 웹 인용|제목=Hexagon Project Wiki|url=<https://www.codeaurora.org/xwiki/bin/Hexagon/> }}
7.  {{ 웹 인용|제목=sx-gcc: port gcc to nec sx vector cpu|url=<http://code.google.com/p/sx-gcc/> }}
8.
9.  [GCC Releases](http://www.gnu.org/software/gcc/releases.html), gnu.org. Accessed on line Mar. 26, 2014.
10. [GCC Development Plan](http://www.gnu.org/software/gcc/develop.html), gnu.org. Accessed on line Mar. 26, 2014.
11. Support added for the Go language.
12. Fortran front end changed from g77 to [gfortran](https://ko.wikipedia.org/wiki/gfortran "wikilink").
13. Added Ada compiler (gnat).
14. CHILL compiler removed.
15. [Downloading GCC](https://web.archive.org/web/20011120200544/http://gcc.gnu.org/install/download.html), gnu.org, archived by archive.org as of November 20, 2001. Accessed on line March 26, 2014.
16. Included front ends for C, C++, Objective C, CHILL, Fortran (g77), and Java (gcj).
17. Added FORTRAN front end (g77). However, g77 was not included with releases 2.8.0 or 2.8.1.
18. Supported C, C++, and Objective C. Prior to this the C++ compiler was released separately from the C compiler.