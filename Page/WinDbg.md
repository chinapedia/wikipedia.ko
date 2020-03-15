> This article is converted from Wikipedia: [WinDbg](https://ko.wikipedia.org/wiki/WinDbg).


**WinDbg**는 [마이크로소프트 윈도우의](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink") 다용도 [디버거](https://ko.wikipedia.org/wiki/디버거 "wikilink")이다.\[1\] [디버깅은](https://ko.wikipedia.org/wiki/디버그 "wikilink") 시스템의 오류들을 찾고 분석하는 과정으로서, 또한 개발을 돕는 용도로서 소프트웨어의 내부 동작을 탐색하는 것도 포함한다. 이것은 [유저 모드](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink") 애플리케이션, [장치 드라이버](https://ko.wikipedia.org/wiki/장치_드라이버 "wikilink"), 그리고 [커널 모드에서](https://ko.wikipedia.org/wiki/보호_링 "wikilink") 운영체제 자체를 디버깅하는 데 사용될 수 있다. [비주얼 스튜디오 디버거](https://ko.wikipedia.org/wiki/비주얼_스튜디오_디버거 "wikilink") 처럼 [그래픽 사용자 인터페이스](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") (GUI)를 가지지만 더 강력하다.

WinDbg는 버그 체크 시 발생하는 [블루 스크린](https://ko.wikipedia.org/wiki/블루_스크린 "wikilink") 이후 생성되는 커널 모드 [메모리 덤프를](../Page/코어_덤프.md "wikilink") 디버깅할 때 사용될 수 있다.\[2\] 또한 유저 모드 충돌 덤프를 디버깅하는데도 사용될 수 있는데, 이것은 [사후 분석 디버깅이라고](https://ko.wikipedia.org/wiki/디버그 "wikilink") 알려져 있다.\[3\]

WinDbg는 SymSrv(SymSrv.dll)을 통해서 서버에서 다양한 표준(예를 들면 타임스탬프, CRC, 프로세서 버전)에 상응하는 [디버그 심볼](../Page/디버그_심볼.md "wikilink") 파일(예를 들면 PDB)들을 자동으로 로드할 수 있다(더 많은 시간을 소비하는 심볼 트리 생성 대신).\[4\] 전용 심볼 서버가 설정되면 심볼들은 소스코드와 연관된다. 디버그 호스트의 특정한 심볼 버전을 찾고 설치할 필요를 없애줌으로써 디버깅 대상에 설치된 다양한 버전들의 바이너리들에 의한 디버깅 문제들에 대한 부담을 경감시켜준다. 마이크로소프트는 윈도우 2000과 이후 버전의 대부분의 공개 심볼들을 가지며, [서비스 팩들을](https://ko.wikipedia.org/wiki/서비스_팩 "wikilink") 포함하는 공용 심볼 서버를 갖고 있다.\[5\]

## 확장

WinDbg는 디버거의 지원되는 명령어들을 늘려주고 특정한 디버깅 시나리오 시에 도움을 줄 수 있는 확장 DLL들을 로딩하는 것을 허용한다.\[6\] 이러한 확장들은 WinDbg를 강력한 디버거로 만들어 주는데 큰 부분을 차지한다. WinDbg는 마이크로소프트 제품 팀이 윈도우를 빌드하는 데 사용되며, 윈도우를 디버깅하는데 요구되는 모든 것들은 이런 확장 DLL들에 포함되어 있다.

확장 명령어들은 항상 **\! **접두어를 갖는다.

몇몇 확장 DLL들은 오직 마이크로소프트 안에서만 사용되지만, 대부분은 윈도우 패키지를 위한 공용 디버깅 툴들을 구성한다.

확장 모델은 윈도우의 디버깅 툴들에 포함된 help 파일 안에 문서화되어 있다.

### Ext.dll

Ext는 WinDbg와 함께 출시되며, 기본적으로 로드되는 표준 윈도우 디버거 확장이다.

#### \!analyze command

가장 많이 사용되는 명령어는 **\!analyze -v**\[7\]이며, 충돌이나 행 상태 시에 디버깅되는 프로그램의 현재 상태와 머신/프로세스 상태를 분석한다.

옵션 없이 사용하면 간단하게 분석 결과를 보여주며, **-v**와 **-vv**는 더 자세한 분석을 보여준다.

### Wow6432exts.dll

Wow6432exts는 WinDbg와 함께 출시되는 표준 윈도우 디버거 확장으로서, [WOW64](https://ko.wikipedia.org/wiki/WOW64 "wikilink") 내에서 실행중인 프로세스들을 디버깅할 때 사용된다.\[8\]

### SOS.dll

SOS (Son of Strike)\[9\] 디버깅 확장 (SOS.dll)은 내부 CLR (Common Language Runtime) 환경에 대한 정보를 제공함으로써 비주얼 스튜디오에서 관리되는 프로그램들이나 WinDbg의 디버깅 시 보조해주는 역할을 한다. SOS.dll은 .NET 프레임워크와 함께 자동으로 설치된다. 비주얼 스튜디오에서 SOS.dll을 사용하려면 WDK (윈도우즈 드라이버 키트)를 설치해야 한다.\[10\] 프로세스나 메모리 덤프를 디버깅하기 위해서는, sos.dll 버전이 .NET 프레임워크 버전과 일치해야 한다. Psscor2와 Psscor4는 SOS의 상위 집합이다.

### Psscor2.dll

Psscor2는 .NET CLR 버전 2.0을 사용하는 .NET 프레임워크 애플리케이션 디버깅 시 사용되는 윈도우 디버거 확장이다. Psscor2는 제품 지원 서비스들의 한 부분으로서 마이크로소프트 내에서 사용되기 위해 개발되었다.\[11\]

### Psscor4.dll

Psscor4는 .NET 프레임워크 4 애플리케이션의 디버깅에 사용되는 윈도우 디버거 확장이다.

## 가상 머신과의 연결

WinDbg는 [VM웨어](https://ko.wikipedia.org/wiki/VM웨어 "wikilink"), [윈도우 가상 PC](https://ko.wikipedia.org/wiki/윈도우_가상_PC "wikilink")(VPC) 또는 [페러럴즈](https://ko.wikipedia.org/wiki/페러럴즈 "wikilink") 같은 [명명된 파이프를](../Page/명명된_파이프.md "wikilink") 사용하는 [가상 머신](https://ko.wikipedia.org/wiki/가상_머신 "wikilink") 위에 돌아가는 윈도우 커널을 디버깅할 수 있다. 이것은 가상 COM port를 사용함으로써 가능해 진다.\[12\] [윈도우 8](https://ko.wikipedia.org/wiki/윈도우_8 "wikilink") 이후로는 특별한 설정 없이 빠른 [커널 디버깅을](../Page/커널_디버거.md "wikilink") 가능케 하면서, 네트워크를 통한 커널 디버깅이 허용된다.\[13\]

## 프로토콜

WinDbg 프로토콜은 문서화되어 있지 않지만, [IDA 프로와](../Page/IDA_프로.md "wikilink") [radare2](https://ko.wikipedia.org/wiki/radare2 "wikilink") [역어셈블러](../Page/역어셈블러.md "wikilink")에 의해 지원된다.

## 각주

## 외부 링크

  - Getting Started: [Install Instructions](http://blogs.msdn.com/johan/archive/2007/01/11/how-to-install-windbg-and-get-your-first-memory-dump.aspx), [Part 1](http://blogs.msdn.com/johan/archive/2007/11/13/getting-started-with-windbg-part-i.aspx), [Part 2](http://blogs.msdn.com/johan/archive/2007/11/26/getting-started-with-windbg-part-ii.aspx)
  - [Debugging Tools for Windows](https://web.archive.org/web/20110217084226/http://www.microsoft.com/whdc/devtools/debugging/default.mspx) - information and free downloads
  - [WinDbg.](http://windbg.info/doc/2-windbg-a-z.html)[From A to Z\!](http://windbg.info/doc/2-windbg-a-z.html) - Theory and examples, 111 slides
  - [Common WinDbg Commands (Thematically Grouped)](http://windbg.info/doc/1-common-cmds.html)
  - [Tutorial on solving system crashes using WinDbg](https://web.archive.org/web/20071012015505/http://www.networkworld.com/news/2005/041105-windows-crash.html)
  - [Symbols loading in WinDbg](https://web.archive.org/web/20110818233504/http://www.windowstipspage.com/2011/02/symbol-server-path-windbg-debugging.html)
  - [Windows Debuggers: Part 1: A WinDbg Tutorial](http://www.codeproject.com/KB/debug/windbg_part1.aspx)
  - [KD extension for fast VMWare and VirtualBox debugging](http://virtualkd.sysprogs.org/)
  - [SOS Debugging Extension (SOS.dll)](https://msdn.microsoft.com/en-us/library/bb190764.aspx)
  - [psscor4 (.](http://www.microsoft.com/en-us/download/details.aspx?id=21255)[NET 4.0)](http://www.microsoft.com/en-us/download/details.aspx?id=21255) or [psscor2 (.](https://web.archive.org/web/20130603092306/http://www.microsoft.com/en-us/download/details.aspx?id=1073)[NET 2.0-3.5)](https://web.archive.org/web/20130603092306/http://www.microsoft.com/en-us/download/details.aspx?id=1073) Replacement for SOS with a superset of commands
  - [1](http://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=36a2630f-5d56-43b5-b996-7633f2ec14ff) WinDBG v6.12.2.633 available via Windows Driver Kit Version 7.1.0
  - [Extension for python scripting (pykd)](http://pykd.codeplex.com)
  - [DbgKit: the first GUI extension for Debugging Tools for Windows](http://www.andreybazhan.com/dbgkit)

[분류:디버거](https://ko.wikipedia.org/wiki/분류:디버거 "wikilink")

1.  <https://msdn.microsoft.com/en-us/windows/hardware/hh852365.aspx>
2.  <http://www.techrepublic.com/blog/windows-and-office/how-do-i-use-windbg-debugger-to-troubleshoot-a-blue-screen-of-death/>
3.
4.  <https://support.microsoft.com/en-us/kb/311503/>
5.  <https://msdn.microsoft.com/en-us/library/windows/hardware/ff552208(v=vs.85>).aspx
6.  <https://msdn.microsoft.com/en-us/library/windows/hardware/ff563964(v=vs.85>).aspx
7.  <https://msdn.microsoft.com/en-us/library/windows/hardware/ff562112(v=vs.85>).aspx
8.  <https://msdn.microsoft.com/en-us/library/windows/desktop/aa384163(v=vs.85>).aspx
9.  <http://blogs.msdn.com/b/jasonz/archive/2003/10/21/53581.aspx>
10. <https://msdn.microsoft.com/en-us/library/bb190764.aspx>
11. <http://blogs.msdn.com/b/tess/archive/2010/03/30/new-debugger-extension-for-net-psscor2.aspx>
12. <http://virtualkd.sysprogs.org/>
13. <https://msdn.microsoft.com/en-us/library/windows/hardware/hh439346(v=vs.85>).aspx