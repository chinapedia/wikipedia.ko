> This article is converted from Wikipedia: [GNU C 라이브러리](https://ko.wikipedia.org/wiki/GNU_C_라이브러리).


[섬네일는](https://ko.wikipedia.org/wiki/파일:Linux_API.svg "wikilink") 리눅스 커널의 시스템 콜 인터페이스, GNU C 라이브러리([GNU](../Page/GNU.md "wikilink")), libdrm, [libalsa](../Page/고급_리눅스_사운드_아키텍처.md "wikilink") 그리고 libevdev ([freedesktop.org](https://ko.wikipedia.org/wiki/freedesktop.org "wikilink"))에 의해 구성된다.\]\] [섬네일](https://ko.wikipedia.org/wiki/파일:Linux_kernel_System_Call_Interface_and_glibc.svg "wikilink") [섬네일과](https://ko.wikipedia.org/wiki/파일:Linux_API_and_Linux_ABI.svg "wikilink") **GNU C 라이브러리**는 함께 리눅스 API를 형성한다. 컴파일 이후 바이너리는 [ABI를](../Page/응용_프로그램_이진_인터페이스.md "wikilink") 제공한다.\]\] **GNU C 라이브러리**는 일반적으로 **glibc**로 알려진, [GNU 프로젝트가](../Page/GNU_프로젝트.md "wikilink") [C 표준 라이브러리를](../Page/C_표준_라이브러리.md "wikilink") 구현한 것이다. 이름과는 달리 현재는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")도 지원한다. 이것은 1990년대 초반 [자유 소프트웨어 재단](../Page/자유_소프트웨어_재단.md "wikilink")(FSF)이 자신의 [GNU](../Page/GNU.md "wikilink") 운영 체제를 위해 시작되었다.

[GNU 약소 일반 공중 사용 허가서](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink") 하에 배포되는 glibc는 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink").

## 역사

Glibc 프로젝트는 초기의 1980년대에 FSF에서 일하던 Roland McGrath에 의해 대부분 쓰여졌다.

1988년 2월 FSF는 glibc를 ANSI C가 요구하는 기능을 거의 완벽하게 갖는다고 주장하였다.\[1\] 1992년 이것은 구현된 ANSI C-1989와 POSIX.1-1990을 가졌으며 POSIX.2의 방식으로 동작하였다.\[2\]

1995년 9월 Ulrich Drepper는 glibc 프로젝트에 대한 그의 첫 기여를 하였고 1990년대 들어 점차적으로 glibc의 핵심 기여자와 유지인이 되었다.\[3\] Drepper는 수 년동안 유지 관리를 하는 위치였으며 2012년 프로젝트의 전체 커밋 중 63%를 차지하였다.\[4\]

### "리눅스 libc"의 분기

1990년대 초반 리눅스 커널의 개발자들은 glibc로 분기하였다. "리눅스 libc"로 불리는 이 분기는 릴리즈 버전 2부터 5까지 독립적으로 유지되었다.

FSF가 glibc 2.0을 릴리즈하였을 때 이것은 더 많은 완전한 POSIX 표준과 더 나은 [국제화와 지역화](../Page/국제화와_지역화.md "wikilink"), 다중언어 함수, [IPv6](../Page/IPv6.md "wikilink") 역량, 64비트 데이터 접근, 멀티스레드 애플리케이션을 위한 기능을 가졌으며 코드는 더 이식가능해졌다.\[5\] 이 시점에서 리눅스 커널 개발자들은 자신들의 분기를 중단하고 다시 FSF의 glibc로 돌아왔다.\[6\]

리눅스 libc의 최신 버전은 내부 이름([soname](https://ko.wikipedia.org/wiki/soname "wikilink")) `libc.so.5`를 가진다. 이 이후로 리눅스의 glibc 2.x는 soname `libc.so.6`를 사용한다.\[7\]

[리처드 스톨만에](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink") 따르면, 코드의 저자가 불분명하고 GNU 프로젝트가 저작권과 저자를 기록하는 것에 엄격하기 때문에 리눅스 libc에서 만들어진 변화는 다시 glibc로 병합될 수 없다고 한다.\[8\]

### 운영 위원회의 설치

2001년부터 라이브러리의 개발은 위원회에 의해 감독되며\[9\], 특히  Ulrich Drepper\[10\]가 주요 기여자와 유지인으로서 활동한다.<span class="cx-segment" data-segmentid="157"></span>

### git으로 전환

이전의 [CVS](../Page/CVS.md "wikilink") 저장소 대신, 2009년 glibc는 *Sourceware*의 [깃](../Page/깃_\(소프트웨어\).md "wikilink") 저장소로 옮겼다.\[11\]

### 버전 역사

대부분의 시스템에서, glibc의 버전은 lib 파일을 실행함으로써 획득할 수 있다(예를 들면, /lib/libc.so.6).

| 버전            | 날자               | 설명                                                                                                                                                                                          | 채택                                                                                                                                                                                                           |
| ------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 0.1 – 0.6     | 1991/10 – 1992/2 |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 1.0           | 1992/2           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 1.01 – 1.09.3 | 1992/3 – 1994/12 |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 1.90 – 1.102  | 1996/5 – 1997/1  |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.0           | 1997/1           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.0.1         | 1997/1           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.0.2         | 1997/2           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.0.91        | 1997/12          |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.0.95        | 1998/7           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.1           | 1999/2           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.1.1         | 1999/3           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.2           | 2000/11          |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.2.1         | 2001/1           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.2.2         | 2001/2           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.2.3         | 2001/3           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.2.4         | 2001/7           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.3           | 2002/10          |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.3.1         | 2002/10          |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.3.2         | 2003/2           |                                                                                                                                                                                             | [데비안](../Page/데비안.md "wikilink") 3.1 (Sarge)                                                                                                                                                                 |
| 2.3.3         | 2003/12          |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.3.4         | 2004/12          | [리눅스 기본 규격](../Page/리눅스_기본_규격.md "wikilink") (LSB) 3.0 표준                                                                                                                                   | [RHEL 4 (업데이트 5)](../Page/레드햇_엔터프라이즈_리눅스.md "wikilink")                                                                                                                                                      |
| 2.3.5         | 2005/4           |                                                                                                                                                                                             | [SLES 9](https://ko.wikipedia.org/wiki/수세_리눅스_엔터프라이즈_서버 "wikilink")                                                                                                                                          |
| 2.3.6         | 2005/11          |                                                                                                                                                                                             | [데비안](../Page/데비안.md "wikilink") 4.0 (Etch)                                                                                                                                                                  |
| 2.4           | 2006/3           | [LSB 4.0](../Page/리눅스_기본_규격.md "wikilink") 표준, 초기 [inotify](https://ko.wikipedia.org/wiki/inotify "wikilink") 지원                                                                            | [SLES 10](https://ko.wikipedia.org/wiki/수세_리눅스_엔터프라이즈_서버 "wikilink")                                                                                                                                         |
| 2.5           | 2006/9           | 전체 [inotify](https://ko.wikipedia.org/wiki/inotify "wikilink") 지원                                                                                                                           | [RHEL 5](../Page/레드햇_엔터프라이즈_리눅스.md "wikilink")                                                                                                                                                               |
| 2.6           | 2007/5           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.7           | 2007/10          |                                                                                                                                                                                             | [데비안](../Page/데비안.md "wikilink") 5 (Lenny), [우분투](../Page/우분투_\(운영_체제\).md "wikilink") 8.04                                                                                                                  |
| 2.8           | 2008/4           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.9           | 2008/11          |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.10          | 2009/5           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.11          | 2009/10          |                                                                                                                                                                                             | [SLES 11](https://ko.wikipedia.org/wiki/수세_리눅스_엔터프라이즈_서버 "wikilink"), 우분투 10.04, 데비안 6 (Squeeze)에서 사용되는 [eglibc](https://ko.wikipedia.org/wiki/eglibc "wikilink")                                            |
| 2.12          | 2010/5           |                                                                                                                                                                                             | [RHEL 6](../Page/레드햇_엔터프라이즈_리눅스.md "wikilink")                                                                                                                                                               |
| 2.13          | 2011/1           |                                                                                                                                                                                             | 데비안 7 (Wheezy)에서 사용되는 [eglibc](https://ko.wikipedia.org/wiki/eglibc "wikilink") 2.13                                                                                                                         |
| 2.14          | 2011/6           |                                                                                                                                                                                             |                                                                                                                                                                                                              |
| 2.15          | 2012/3           |                                                                                                                                                                                             | 우분투 12.04와 12.10                                                                                                                                                                                             |
| 2.16          | 2012/6           | [x32 ABI](https://ko.wikipedia.org/wiki/x32_ABI "wikilink") 지원, [C11](https://ko.wikipedia.org/wiki/C11 "wikilink") 컴플라이언스, [SystemTap](https://ko.wikipedia.org/wiki/SystemTap "wikilink") |                                                                                                                                                                                                              |
| 2.17          | 2012/12          | [ARMv-A](https://ko.wikipedia.org/wiki/ARMv-A "wikilink") 지원                                                                                                                                | 우분투 13.04, [RHEL 7](../Page/레드햇_엔터프라이즈_리눅스.md "wikilink")                                                                                                                                                    |
| 2.18          | 2013/8           | 향상된 [C++11](../Page/C++11.md "wikilink") 지원.                                                                                                                                                | 페도라 20                                                                                                                                                                                                       |
| 2.19          | 2014/2           |                                                                                                                                                                                             | 우분투 14.04, 데비안 8 (Jessie)에서 사용되는 [eglibc](https://ko.wikipedia.org/wiki/eglibc "wikilink") 2.19, [오픈수세 13](../Page/오픈수세.md "wikilink"), [SLES 12](https://ko.wikipedia.org/wiki/수세_리눅스_엔터프라이즈_서버 "wikilink") |
| 2.20          | 2014/9           | 파일 서술 잠금 지원                                                                                                                                                                                 | 페도라 21                                                                                                                                                                                                       |
| 2.21          | 2015/2           | 새로운 세마포어 구현                                                                                                                                                                                 | 우분투 15.04, 페도라 22                                                                                                                                                                                            |
| 2.22          | 2015/8           | [구글 네이티브 클라이언트](../Page/구글_네이티브_클라이언트.md "wikilink") (NaCl) 지원, [유니코드](../Page/유니코드.md "wikilink") 7.0                                                                                      | 페도라 23                                                                                                                                                                                                       |
| 2.23          | 2016/2           | [유니코드](../Page/유니코드.md "wikilink") 8.0                                                                                                                                                      |                                                                                                                                                                                                              |

## 기능

glibc는 [단일 유닉스 규격과](../Page/단일_유닉스_규격.md "wikilink") [POSIX](../Page/POSIX.md "wikilink") (1c, 1d, 1j)가 요구하는 기능들을 제공하며, [ISO](../Page/국제_표준화_기구.md "wikilink") [C11](https://ko.wikipedia.org/wiki/C11 "wikilink"), [ISO](../Page/국제_표준화_기구.md "wikilink") [C99](../Page/C99.md "wikilink"), [버클리 유닉스](../Page/BSD.md "wikilink") (BSD) 인터페이스 등에서 요구하는 몇몇 기능들도 제공한다.

추가적으로 glibc는 또한 GNU 개발에 필요하다고 여겨지거나 유용한 확장들도 제공한다.

### 지원되는 하드웨어와 커널

Glibc는 수많은 여러 커널들과 여러 하드웨어 아키텍처에서 돌아간다. 그러나 가장 흔한 사용은 x86 하드웨어 상의 리눅스 커널에서의 사용이다. 공식적으로 지원되는 하드웨어는\[12\] : [ARM 아키텍처](../Page/ARM_아키텍처.md "wikilink"), [알파 프로세서](https://ko.wikipedia.org/wiki/알파_프로세서 "wikilink"), [PA-RISC](../Page/PA-RISC.md "wikilink"), IA-64, Motorola m68k, MicroBlaze, [MIPS 아키텍처](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink"), Nios II, [파워PC](../Page/파워PC.md "wikilink"), [s390](../Page/IBM_시스템_z.md "wikilink"), [SPARC](../Page/SPARC.md "wikilink"), [타일64](../Page/타일64.md "wikilink"), 그리고 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")이다. 이것은 [Hurd와](../Page/GNU_허드.md "wikilink") [리눅스 커널을](../Page/리눅스_커널.md "wikilink") 지원한다.

### 작은 장치에서의 사용

glibc는 과거 [리누스 토발즈](https://ko.wikipedia.org/wiki/리누스_토발즈 "wikilink")\[13\]와 임베디드 리눅스 프로그래머들에 의해 크고 느리다는 비판을 받아왔다. 이 이유로 여러 대체 C 표준 라이브러리들이 만들어졌다. 대체 libcs로 Bionic ([안드로이드](../Page/안드로이드_\(운영_체제\).md "wikilink")\[14\]에서 사용되는), [dietlibc](https://ko.wikipedia.org/wiki/dietlibc "wikilink"), [uClibc](https://ko.wikipedia.org/wiki/uClibc "wikilink"), Newlib, [Klibc](../Page/Klibc.md "wikilink"), 그리고 musl이 있다.

## 대안

이것의 대안으로, 다른 C 표준 라이브러리는 다음과 같다: Bionic libc, [dietlibc](https://ko.wikipedia.org/wiki/dietlibc "wikilink"), [EGLIBC](https://ko.wikipedia.org/wiki/임베디드_GNU_C_라이브러리 "wikilink"), [klibc](https://ko.wikipedia.org/wiki/klibc "wikilink"), musl, Newlib, 그리고 [uClibc](https://ko.wikipedia.org/wiki/uClibc "wikilink").

## 호환성 계층

[안드로이드와](../Page/안드로이드_\(운영_체제\).md "wikilink") [윈도우](../Page/마이크로소프트_윈도우.md "wikilink") 같이 다른 시스템을 위해 쓰여진 프로그램들을 시스템이 제공하는 glibc 인터페이스에서 돌아가게 하는 [호환성 계층이](https://ko.wikipedia.org/wiki/호환성_계층 "wikilink") 존재한다. [와인도](../Page/와인_\(소프트웨어\).md "wikilink") [Win32 API](../Page/윈도우_API.md "wikilink")/ABI에서 glibc로의 호환성 계층으로 여겨진다.

## 같이 보기

  - Gnulib
  - [리눅스 커널 API](https://ko.wikipedia.org/wiki/리눅스_커널_API "wikilink")

## 각주

## 외부 링크

  - [GNU libc 홈페이지](https://www.gnu.org/software/libc/)
  - [GNU libc 개발자 페이지](https://web.archive.org/web/20151203204332/http://www.gnu.org/software/libc/development.html)

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink") [분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:리눅스 커널의 인터페이스](https://ko.wikipedia.org/wiki/분류:리눅스_커널의_인터페이스 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.
2.
3.  [glibc changelog](https://github.com/lattera/glibc/blob/master/ChangeLog.5) on [GitHub](../Page/깃허브.md "wikilink").
4.
5.
6.
7.
8.
9.
10.
11. [glibc repo](https://sourceware.org/glibc/wiki/GlibcGit) on Sourceware.com
12.
13.
14.