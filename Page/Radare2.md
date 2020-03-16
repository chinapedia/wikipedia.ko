> This article is converted from Wikipedia: [Radare2](https://ko.wikipedia.org/wiki/Radare2).


**Radare2** (또는 **r2**)는 바이너리를 [리버스 엔지니어링하고](../Page/리버스_엔지니어링.md "wikilink") 분석하기 위한 완전한 [프레임워크](https://ko.wikipedia.org/wiki/프레임워크 "wikilink")이다. 이것은 같이 사용되거나 [명령 줄 인터페이스에서](../Page/명령_줄_인터페이스.md "wikilink") 독립적으로 사용될 수 있는 조그만 유틸리티들의 집합으로 이루어져 있다. [역어셈블러](../Page/역어셈블러.md "wikilink") 위주로 만들어진 이것은 여러 [프로세서](https://ko.wikipedia.org/wiki/프로세서 "wikilink")들과 [운영 체제들을](../Page/운영_체제.md "wikilink") 위한 다양한 [실행 파일](../Page/실행_파일.md "wikilink") 포맷을 지원한다.

## 특징과 사용

Radare2는 [그래픽 사용자 인터페이스를](../Page/그래픽_사용자_인터페이스.md "wikilink") 갖지 않기 때문에 배우기 어렵다. 원래 헥사 에디터 위주로 만들어졌지만 지금은 많은 툴들과 특징들을 가지며 또한 여러 언어들을 위한 바인딩도 제공한다.\[1\]

### 정적 분석

Radare2는 많은 것들을 어셈블하고 역어셈블할 수 있으며 또한 그래프를 이용한 [바이너리 디핑과](https://ko.wikipedia.org/wiki/Diff "wikilink") 재배치 심볼과 데이터의 여러 다른 타입들 같은 정보를 추출할 수 있다.\[2\] 내부적으로 이것은 분석 정보를 놓치지 않기 위해 [sdb](https://medium.com/@trufae/everything-is-a-string-9d626c98e59f)로 불리는 [NoSQL](../Page/NoSQL.md "wikilink") 데이터베이스를 사용한다. 이것은 radare2에 의해 추론될 수 있으며 또한 사용자에 의해 직접적으로 추가될 수도 있다. Radare2가 기형적인 바이너리들을 다룰 수 있기 때문에 [소프트웨어 보안](https://ko.wikipedia.org/wiki/소프트웨어_보안 "wikilink") 연구자들에 의해 분석을 목적으로 사용될 수도 있다.\[3\]\[4\]\[5\]

### 동적 분석

Radare2는 빌트인 디버거를 가지는데, 이것은 [GDB보다](../Page/GNU_디버거.md "wikilink") 저수준이다. 그러나 GNU 디버거와 사용될수 있으며 심지어는 윈도우 바이너리를 디버그하기 위해 [WineDBG](../Page/와인_\(소프트웨어\).md "wikilink")\[6\]와도 사용될 수 있다. 심지어는 VM웨어와 함께 [커널 디버거로서](../Page/커널_디버거.md "wikilink") 사용될 수도 있다. 또한 [WinDbg](../Page/WinDbg.md "wikilink") 프로토콜을 위한 지원도 존재한다.

### 소프트웨어 취약점 공격

radare2가 역어셈블러와 저수준 디버거의 특징을 갖기 때문에, 또한 취약점 개발자들에게 유용하게 사용될 수 있다. 이 소프트웨어는 [ROP](../Page/반환_지향형_프로그래밍.md "wikilink") 가젯 검색 엔진과 완화 탐지 같은 취약점 개발을 보조하는 특징을 갖는다. Radare2는 또한 [메타스플로이트와](../Page/메타스플로이트_프로젝트.md "wikilink") 비슷하게, 이것의 'ragg2' 툴을 이용해서 [셸코드](https://ko.wikipedia.org/wiki/셸코드 "wikilink")를 생성하는 것을 도울 수 있다.

## 지원되는 아키텍처/포맷

  - 인식되는 파일 포맷
      - COFF 계열, Win32/64/일반 [PE](../Page/PE_포맷.md "wikilink") 포함.
      - [ELF](https://ko.wikipedia.org/wiki/ELF_파일_형식 "wikilink") 계열
      - Mach-O ([Mach](../Page/Mach_\(커널\).md "wikilink")) 계열
      - [게임보이](../Page/게임보이.md "wikilink")와 [게임보이 어드밴스](../Page/게임보이_어드밴스.md "wikilink") 카트리지
      - [MZ](../Page/MZ_실행_파일.md "wikilink") ([MS-DOS](../Page/MS-DOS.md "wikilink"))
      - Java class
      - dyld 캐시 덤프\[7\]
      - Dex ([달빅](../Page/달빅_\(소프트웨어\).md "wikilink") 실행 파일)
      - Xbox xbe 포맷\[8\]
      - [플랜9](../Page/플랜_9_\(운영_체제\).md "wikilink") 바이너리
      - [Winrar](../Page/WinRAR.md "wikilink") 가상 머신\[9\]
      - [파일 시스템](../Page/파일_시스템.md "wikilink") ([ext](../Page/Ext4.md "wikilink"), ReiserFS, [HFS+](../Page/HFS_플러스.md "wikilink"), [NTFS](../Page/NTFS.md "wikilink"), [FAT](../Page/파일_할당_테이블.md "wikilink"), ...)
      - 추가적인 디버그 정보를 저장하기 위한 DWARF와 PDB 파일 포맷
      - Raw 바이너리

<!-- end list -->

  - 명령어
      - [인텔](../Page/인텔.md "wikilink") x86 계열
      - [ARM 아키텍처](../Page/ARM_아키텍처.md "wikilink")
      - Atmel AVR 시리즈
      - [브레인퍽](../Page/브레인퍽.md "wikilink")
      - Motorola 68k and H8
      - [리코 5A22](https://ko.wikipedia.org/wiki/리코_5A22 "wikilink")
      - [MOS 6502](../Page/MOS_6502.md "wikilink")
      - Smartcard PSOS 가상 머신
      - 자바 가상 머신
      - MIPS: mipsb/mipsl/mipsr/mipsrl/r5900b/r5900l
      - [파워PC](../Page/파워PC.md "wikilink")
      - [SPARC](../Page/SPARC.md "wikilink") 계열
      - TMS320Cxxx 시리즈
      - Argonaut RISC Core
      - Intel 51 시리즈: 8051/80251b/80251s/80930b/80930s
      - [자일로그 Z80](../Page/자일로그_Z80.md "wikilink")
      - CR16
      - 케임브리지 실리콘 라디오 (CSR)
      - 안드로이드VM 달빅
      - DCPU-16
      - [EFI bytecode](../Page/통일_확장_펌웨어_인터페이스.md "wikilink")
      - 게임보이 (z80-like)
      - 자바 바이트코드
      - Malebolge
      - [MSIL/CIL](../Page/공통_중간_언어.md "wikilink")
      - Nios II
      - [슈퍼H](https://ko.wikipedia.org/wiki/슈퍼H "wikilink")
      - [SPC700](https://ko.wikipedia.org/wiki/SPC700 "wikilink")
      - Systemz
      - TMS320
      - V850
      - [화이트스페이스](../Page/화이트스페이스_\(프로그래밍_언어\).md "wikilink")
      - XCore

## 각주

## 더 읽어보기

  -
  - [The r2-book](https://web.archive.org/web/20150423052558/http://maijin.github.io/radare2book/)

## 외부 링크

  - [공식 웹사이트](http://radare.org)
  - [Radare2's blog](http://radare.today)
  - [Git repository](https://github.com/radare/radare2)

[분류:디버거](https://ko.wikipedia.org/wiki/분류:디버거 "wikilink") [분류:역어셈블러](https://ko.wikipedia.org/wiki/분류:역어셈블러 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:LGPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:LGPL_라이선스_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink")

1.  [Git repository for radare2's bindings](https://github.com/radare/radare2-bindings)
2.  ["Binary Diffing" visual en Linux con Radare2](http://chatsubo-labs.blogspot.com/2013/10/binary-diffing-visual-en-linux-con.html)
3.
4.  [Craig Heffner - Finding and Reversing Backdoors in Consumer Firmware](http://www.devttys0.com/wp-content/uploads/2014/04/FindingAndReversingBackdoors.pdf)
5.  PHDays IV, May 21, 2014, 'Anton Kochkov', *Application of radare2 illustrated by Shylock/Caphaw.*
6.
7.  [Dydl cache - iphonedevwiki.net](http://iphonedevwiki.net/index.php/Dyld_shared_cache)
8.
9.  [Tavis Ormandy - Fun with Constrained Programming](http://blog.cmpxchg8b.com/2012/09/fun-with-constrained-programming.html)