> This article is converted from Wikipedia: [GNU ](https://ko.wikipedia.org/wiki/GNU_).


보통은 **GDB**라고 부르는 **GNU 디버거**(GNU Debugger)는 [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") 소프트웨어 시스템을 위한 기본 [디버거](https://ko.wikipedia.org/wiki/디버거 "wikilink")이다. GDB는 다양한 유닉스 기반의 시스템에서 동작하는 이식성있는 디버거로, [에이다](https://ko.wikipedia.org/wiki/에이다_프로그래밍_언어 "wikilink"), [C](https://ko.wikipedia.org/wiki/C언어 "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [포트란](https://ko.wikipedia.org/wiki/포트란 "wikilink") 등의 여러 [프로그래밍 언어를](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink") 지원한다.

## 역사

GDB는 [1988년](https://ko.wikipedia.org/wiki/1988년 "wikilink")에서 [리처드 스톨만이](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink") 처음 작성한 것으로, [GNU 일반 공중 사용 허가서하에](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 배포되는 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink").

1990년부터 1993년까지는 시그너스 솔루션즈에서 근무하는 [존 길모어가](https://ko.wikipedia.org/wiki/존_길모어 "wikilink") 관리하였다.

## 기술적인 세부 사항

### 기능

GDB는 [컴퓨터 프로그램의](https://ko.wikipedia.org/wiki/컴퓨터_프로그램 "wikilink") 실행을 추적하고 수정할 수 있는 많은 기능들을 제공한다. 사용자는 프로그램의 내부 [변수](https://ko.wikipedia.org/wiki/변수 "wikilink")들의 값을 주시하거나 변경할 수 있으며, 프로그램의 일반적인 실행 과정과 독립적으로 [함수를](https://ko.wikipedia.org/wiki/함수_\(프로그래밍\) "wikilink") 호출할 수도 있다.

GDB는 ([2003년](https://ko.wikipedia.org/wiki/2003년 "wikilink") 현재) [알파](https://ko.wikipedia.org/wiki/알파_프로세서 "wikilink"), [ARM](https://ko.wikipedia.org/wiki/ARM_아키텍처 "wikilink"), [H8/300](https://ko.wikipedia.org/wiki/H8/300 "wikilink"), [시스템/370](https://ko.wikipedia.org/wiki/시스템/370 "wikilink"), [시스템 390](https://ko.wikipedia.org/wiki/시스템_390 "wikilink"), [X86](https://ko.wikipedia.org/wiki/X86 "wikilink"), [IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink") "아이테니엄", [모토로라 68000](https://ko.wikipedia.org/wiki/모토로라_68000 "wikilink"), [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink"), [PA-RISC](../Page/PA-RISC.md "wikilink"), [PowerPC](https://ko.wikipedia.org/wiki/PowerPC "wikilink"), [SuperH](https://ko.wikipedia.org/wiki/SuperH "wikilink"), [SPARC](https://ko.wikipedia.org/wiki/SPARC "wikilink"), [VAX](../Page/VAX.md "wikilink")와 같은 다양한 머신들을 지원한다.

표준 릴리즈에 포함된 덜 알려진 대상 프로세서로는 [A29K](https://ko.wikipedia.org/wiki/A29K "wikilink"), [ARC](https://ko.wikipedia.org/wiki/Advanced_RISC_Computing "wikilink"), [AVR](https://ko.wikipedia.org/wiki/아트멜_AVR "wikilink"), [CRIS](https://ko.wikipedia.org/wiki/CRIS "wikilink"), [D10V](https://ko.wikipedia.org/wiki/D10V "wikilink"), [D30V](https://ko.wikipedia.org/wiki/D30V "wikilink"), [FR-30](https://ko.wikipedia.org/wiki/FR-30 "wikilink"), [FR-V](https://ko.wikipedia.org/wiki/FR-V "wikilink"), [인텔 i960](https://ko.wikipedia.org/wiki/인텔_i960 "wikilink"), [M32R](https://ko.wikipedia.org/wiki/M32R "wikilink"), [68HC11](https://ko.wikipedia.org/wiki/모토로라_68HC11 "wikilink"), [모토로라 88000](https://ko.wikipedia.org/wiki/모토로라_88000 "wikilink"), [MCORE](https://ko.wikipedia.org/wiki/MCORE "wikilink"), [MN10200](https://ko.wikipedia.org/wiki/MN10200 "wikilink"), [MN10300](https://ko.wikipedia.org/wiki/MN10300 "wikilink"), [NS32K](https://ko.wikipedia.org/wiki/320xx_마이크로프로세서 "wikilink"), [Stormy16](https://ko.wikipedia.org/wiki/Stormy16 "wikilink"), [V850](https://ko.wikipedia.org/wiki/V850 "wikilink"), [VAX](../Page/VAX.md "wikilink"), [Z8000](https://ko.wikipedia.org/wiki/자일로그_Z8000 "wikilink"), [EISC](https://ko.wikipedia.org/wiki/EISC "wikilink")과 같은 것들이 있으며 이들 중에는 새 릴리즈에 포함되지 않은 것들도 있다.

GDB는 내부에 M32R이나 V850과 같은 거의 알려지지 않은 타겟 프로세서들에 대한 [시뮬레이터](https://ko.wikipedia.org/wiki/시뮬레이터 "wikilink")도 포함하고 있다.

### 원격 디버깅

GDB는 임베디드 시스템을 디버깅할 때 사용되는 '원격' 모드를 지원한다. 원격 디버깅은 GDB가 한 머신 상에서 동작하고, 디버그할 프로그램은 다른 머신 상에서 동작하는 것을 말한다. GDB는 GDB 프로토콜을 알고 있는 원격지의 'stub'과 직렬 포트 혹은 TCP/IP를 통해 통신할 수 있다.

이 원격 디버깅 모드는 [리눅스 커널에](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 사용되는 소스 수준의 디버거인 [KGDB](https://ko.wikipedia.org/wiki/KGDB "wikilink")에서도 사용된다. KGDB를 사용하면 커널 개발자는 일반 응용 프로그램과 마찬가지로 커널을 디버깅할 수 있다. KGDB는 커널 코드내에 중단점을 삽입하는 것이 가능하며, 코드를 한 단계씩 실행(step)시키거나, 변수의 값을 관찰하는 것이 가능하다. 하드웨어 디버깅 레지스터를 포함하고 있는 프로세서에서는 감시점(watchpoint)을 설정하여 특정 메모리 주소가 접근되거나 실행될 때 [중단점](https://ko.wikipedia.org/wiki/중단점 "wikilink")을 설정할 수 있다. KGDB는 디버깅할 머신에 [직렬 케이블이나](https://ko.wikipedia.org/wiki/직렬_케이블 "wikilink") [이더넷](https://ko.wikipedia.org/wiki/이더넷 "wikilink")을 통해 연결될 또 다른 머신을 필요로 한다. [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink")에서는 [파이어와이어](https://ko.wikipedia.org/wiki/IEEE_1394 "wikilink") [DMA를](https://ko.wikipedia.org/wiki/기억_직접_접근 "wikilink") 이용한 디버깅도 가능하다.

### 제한 사항

GDB는 자체적인 [GUI를](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 포함하고 있지 않으며 기본적으로 [명령행](https://ko.wikipedia.org/wiki/명령행 "wikilink") 인터페이스를 사용한다. [DDD](../Page/데이터_디스플레이_디버거.md "wikilink"), [GDBk](https://ko.wikipedia.org/wiki/GDBk "wikilink")/[Insight](https://ko.wikipedia.org/wiki/Insight "wikilink")와 같은 몇 가지 프론트엔드들이 있으며, [Emacs](https://ko.wikipedia.org/wiki/Emacs "wikilink")에서도 "GUD"모드를 지원한다. 이들은 [통합 개발 환경에서](https://ko.wikipedia.org/wiki/통합_개발_환경 "wikilink") 제공하는 것과 비슷한 디버깅 기능들을 제공한다.

[메모리 누수](https://ko.wikipedia.org/wiki/메모리_누수 "wikilink") 탐지기와 같이 GDB와 연동하여 사용할 수 있는 툴들도 존재한다.

## 명령어 사용 예

`gdb prog.out      prog.out를 디버깅..`
`gdb > run         프로그램 실행`

## 예제

    GNU gdb Red Hat Linux (6.3.0.0-1.21rh)
    Copyright 2004 Free Software Foundation, Inc.
    GDB is free software, covered by the GNU General Public License, and you are
    welcome to change it and/or distribute copies of it under certain conditions.
    Type "show copying" to see the conditions.
    There is absolutely no warranty for GDB. Type "show warranty" for details.
    This GDB was configured as "i386-redhat-linux-gnu"...Using host libthread_db library "/lib/libthread_db.so.1".

    (gdb) run
    Starting program: /home/sam/programming/crash
    Reading symbols from shared object read from target memory...done.
    Loaded system supplied DSO at 0xc11000
    This program will demonstrate gdb

    Program received signal SIGSEGV, Segmentation fault.
    0x08048428 in function_2 (x=24) at crash.c:22
    22 return *y;
    (gdb) edit
    (gdb) shell gcc crash.c -o crash -gstabs+
    (gdb) run
    The program being debugged has been started already.
    Start it from the beginning? (y or n) y
    warning: cannot close "shared object read from target memory": File in wrong format
    `/home/sam/programming/crash' has changed; re-reading symbols.
    Starting program: /home/sam/programming/crash
    Reading symbols from shared object read from target memory...done.
    Loaded system supplied DSO at 0xa3e000
    This program will demonstrate gdb
    24
    Program exited normally.
    (gdb) quit

먼저 프로그램을 실행시키고 세그먼트 폴트의 원인을 찾은 후에 올바른 동작을 하도록 수정(edit)하였다. 수정된 프로그램은 [GCC를](https://ko.wikipedia.org/wiki/GNU_컴파일러_모음 "wikilink") 통해 다시 컴파일된 후 실행되었다. ...

## 참고 문헌

  - [Richard M. Stallman](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink"), [Roland Pesch](https://ko.wikipedia.org/wiki/Roland_Pesch "wikilink"), [Stan Shebs](https://ko.wikipedia.org/wiki/Stan_Shebs "wikilink"), et al., *Debugging with GDB* ([자유 소프트웨어 재단](https://ko.wikipedia.org/wiki/자유_소프트웨어_재단 "wikilink"), 2002)

## 외부 링크

  - [GDB 홈페이지](http://www.gnu.org/software/gdb/)
  - [gdb 문서: "Debugging with GDB"](http://sources.redhat.com/gdb/current/onlinedocs/gdb.html) (html 과 400 페이지 이상의 PDF로 제공)
  - [GDB Internals](https://web.archive.org/web/20080616054054/http://sources.redhat.com/gdb/current/onlinedocs/gdbint.html)
  - [GDB 강좌](https://web.archive.org/web/20071017044810/http://users.actcom.co.il/~choo/lupg/tutorials/debugging/debugging-with-gdb.html)
  - [kgdb, 리눅스 커널을 디버깅하기 위한 gdb 백엔드](https://web.archive.org/web/20130517035414/http://kgdb.linsyssoft.com/)
  - [Peter Jay Salzman's excellent GDB guide](https://web.archive.org/web/20061004141706/http://www.dirac.org/linux/gdb/)
  - [GDB를 GUI로 쉽게 조작하는 프론트엔드 프로그램 MyGDB](https://web.archive.org/web/20100829051021/http://kldp.net/projects/mygdb/)

[분류:디버거](https://ko.wikipedia.org/wiki/분류:디버거 "wikilink") [디버거](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink")