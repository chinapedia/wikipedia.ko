> This article is converted from Wikipedia: [FASM](https://ko.wikipedia.org/wiki/FASM).


**FASM** (*flat 어셈블러*)는 x86 프로세서 용 [어셈블러](https://ko.wikipedia.org/wiki/어셈블러 "wikilink")이다. 이것은 [IA-32](../Page/IA-32.md "wikilink")와 [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") 컴퓨터 아키텍처 용 인텔 스타일 [어셈블리어](../Page/어셈블리어.md "wikilink")를 지원한다. FASM은 빠른 속도와 크기 최적화, [운영 체제](../Page/운영_체제.md "wikilink") 호환성 그리고 매크로 기능을 갖는다.\[1\]\[2\] 이것은 저 수준 어셈블러이며\[3\] 의도적으로 매우 적은 [명령 줄](https://ko.wikipedia.org/wiki/명령_줄 "wikilink") 옵션을 갖는다. [자유-오픈 소스 소프트웨어이다](../Page/자유-오픈_소스_소프트웨어.md "wikilink").

FASM의 모든 버전은 직접적으로 다음을 출력할 수 있다: flat "raw" [바이너리](../Page/이진_파일.md "wikilink") (DOS [COM executable](../Page/COM_파일.md "wikilink") 또는 SYS 드라이버로서 사용 가능한), 목적 파일: [ELF 파일 형식](https://ko.wikipedia.org/wiki/ELF_파일_형식 "wikilink") (ELF) 또는 COFF (클래식 또는 MS-전용), 또는 [MZ](../Page/MZ_실행_파일.md "wikilink"), ELF, [PE 포맷](../Page/PE_포맷.md "wikilink") (WDM 드라이버를 포함하며 커스텀 MZ DOS 스텁을 허용하는) 실행 파일. [ARM 아키텍처](../Page/ARM_아키텍처.md "wikilink")([FASMARM](http://arm.flatassembler.net))를 위한 비공식적인 포팅도 존재한다.\[4\]

## 설계

FASM은 [MASM이나](../Page/마이크로소프트_매크로_어셈블러.md "wikilink") [TASM](https://ko.wikipedia.org/wiki/TASM "wikilink") 처럼 많은 고 수준 선언문을 지원하지 않는다.\[5\] 대신 선언문들을 커스터마이즈하고 생성할 수 있게 해주는 문법 특징과 매크로들을 제공한다. 이것의 메모리 어드레싱 문법은 TASM의 ideal 모드나 [NASM과](../Page/넷와이드_어셈블러.md "wikilink") 비슷하다. 괄호는 두 어셈블러 처럼 메모리 오퍼랜드를 의미하지만, 크기는 NASM처럼 괄호의 밖에 있다.

FASM은 멀티 패스 어셈블러이다. 이것은 광범위한 코드 크기 최적화를 해주며 자유로는 사전 참조를 허용한다.\[6\] FASM의 특이한 구조로는 코드 내에서 사용될 때에만 프로시저를 정의하는 것이 있다. 이것은 대부분의 언어에서 [링커에](../Page/링커_\(컴퓨팅\).md "wikilink") 의해 오브젝트 단위로 수행된다.

FASM은 "같은 소스, 같은 결과" 원리에 기반한다: 결과 파일의 내용은 커맨드 라인에 의해 영향을 받지 않는다. 이러한 접근법은 FASM을 다른 많은 어셈블리 프로젝트에서 존재하는 컴파일 문제로부터 구해준다. 반면에 이것은 각각 다양하게 컴파일된 소스 파일들이나 또는 언어가 섞인 프로젝트들에서는 프로젝트를 유지보수하기 어렵게 한다. 하지만 FA라고 불리는 Win32 래퍼가 존재하고 이것은 이 문제를 완화시켜 준다.\[7\] FASM 프로젝트들은 링킹 단게 없이 소스 파일에서 직접적으로 실행 파일을 만들 수 있다.

## Fresh IDE

**Fresh**(John Found에 의해 시작된 인터넷 커뮤니티 지원 프로젝트)는 FASM을 위한 [통합 개발 환경](../Page/통합_개발_환경.md "wikilink")(IDE)이다. Fresh의 목표는 다른 시각적인 언어들 처럼 프로그래밍을 빠르고 효율적으로 할 수 있게 하며 동시에 작은 애플리케이션 크기와 어셈블리어의 raw 파워를 희생시키지 않는 것이다. Fresh는 윈도우 프로그래밍에서 사용될 수 있지만 또한 FASM을 지원하는 운영 체제를 위한 프로그램도 개발할 수 있다 – [도스](../Page/도스.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink"), [BeOS](../Page/BeOS.md "wikilink"), [미뉴엣OS](../Page/미뉴엣OS.md "wikilink").

## 사용

FASM으로 개발된 운영 체제들:

  - DexOS - Ville Turijanmaa\[8\]
  - [MenuetOS](../Page/미뉴엣OS.md "wikilink")\[9\] – 32 - [64비트](../Page/64비트.md "wikilink") GUI 운영 체제
  - [KolibriOS](../Page/KolibriOS.md "wikilink")

FASM을 백엔드로 사용하는 컴파일러들:

  - PureBasic
  - [High Level Assembly](https://ko.wikipedia.org/wiki/High_Level_Assembly "wikilink") (HLA)
  - BlitzMax

## 같이 보기

  - [어셈블러 비교](https://ko.wikipedia.org/wiki/어셈블러_비교 "wikilink")

## 각주

## 외부 링크

  - FASM project:
  - [FASMLIB](http://fasmlib.x86asm.net/) 0.8.0 – portable 32-bit x86 asm lib for FASM/MASM/YASM/NASM/GASM
  - [FASMARM](http://arm.flatassembler.net) – FASM for ARM processors, <small> v1.27, </small>
  - [The Fresh IDE](http://fresh.flatassembler.net/)

[분류:1999년 도입](https://ko.wikipedia.org/wiki/분류:1999년_도입 "wikilink") [분류:어셈블러](https://ko.wikipedia.org/wiki/분류:어셈블러 "wikilink") [분류:어셈블리어](https://ko.wikipedia.org/wiki/분류:어셈블리어 "wikilink") [분류:도스용 소프트웨어](https://ko.wikipedia.org/wiki/분류:도스용_소프트웨어 "wikilink") [분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.