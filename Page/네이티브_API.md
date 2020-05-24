> This article is converted from Wikipedia: [네이티브 API](https://ko.wikipedia.org/wiki/네이티브_API).


**네이티브 API**()는 [윈도우 NT와](../Page/윈도우_NT.md "wikilink") 사용자 모드의 응용 프로그램에서 사용되는 [API](../Page/API.md "wikilink")이다. 다른 윈도우 구성 요소들이 사용되기 힘들 때 사용되며, 주로 시스템 부팅 시나 kernel32.dll 같은 [윈도 API를](https://ko.wikipedia.org/wiki/윈도_API "wikilink") 구현하는 용도로 쓰인다. ntdll.dll의 [엔트리 포인트는](../Page/엔트리_포인트.md "wikilink") **LdrInitializeThunk**이다. 대부분의 네이티브 API의 호출은 [ntoskrnl.exe](https://ko.wikipedia.org/wiki/ntoskrnl.exe "wikilink")에서 구현되며, ntdll.dll에 의해서 [사용자 모드로](https://ko.wikipedia.org/wiki/사용자_모드 "wikilink") 노출된다. 어떤 경우에는 사용자 모드에서 ntdll.dll 내부의 네이티브 API가 직접 호출되기도 한다.

네이티브 API 호출은 [SSDT를](../Page/시스템_서비스_서술자_테이블.md "wikilink") 통해서 [커널에](../Page/윈도우_NT_아키텍처.md "wikilink") 의해 관리된다.

대부분의 마이크로소프트 윈도우가 잘 정의된 [윈도 API에](https://ko.wikipedia.org/wiki/윈도_API "wikilink") 의해 구현된 반면, [클라이언트/서버 런타임 하위 시스템같은](https://ko.wikipedia.org/wiki/클라이언트/서버_런타임_하위_시스템 "wikilink") 소수의 구성 요소들은 네이티브 API로 구현된다. 왜냐하면 이것이 [윈도 NT 시작 프로세스](https://ko.wikipedia.org/wiki/윈도_NT_시작_프로세스 "wikilink") 전에 호출되는데, 이 때는 WIndows API가 아직 사용 가능하지 않기 때문이다.

## 함수 그룹

네이티브 API는 많은 함수들로 이루어져 있다. strlen(), sprintf() 등이 있고 floor() 같은 기본적인 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 런타임 실행을 위해 [C 런타임 함수들을](../Page/C_표준_라이브러리.md "wikilink") 포함한다. malloc(), printf(), scanf() 같은 공통 프로시저들은 빠졌다. 대다수의 네이티브 API들은 관행적으로 아래와 같은 접두사를 갖는다.

  - **Nt** 또는 **Zw**는 ntdll.dll과 ntoskrnl.exe에서 선언된 [시스템 호출이다](../Page/시스템_호출.md "wikilink"). 사용자 모드의 ntdll.dll에서 호출되면, 이 그룹들은 다음과 같은 면에서 거의 같다. [커널 모드에](https://ko.wikipedia.org/wiki/보호_링#수퍼바이저_모드 "wikilink") 들어가서 [SSDT를](../Page/시스템_서비스_서술자_테이블.md "wikilink") 통해 ntoskrnl.exe의 같은 의미를 가진 함수를 호출한다. ntoskrnl.exe에서 직접적으로 호출될 경우(커널 모드에서만 가능)에는 Zw는 Nt와 달리 커널 모드인 것을 보장한다.\[1\] Zw 접두사는 아무것도 의미하지 않는다.\[2\]
  - **Rtl**은 ntdll 함수 중에서 두번째로 많은 그룹이다. 이것은 (확장된) C 런타임 라이브러리를 구성하고 있다. (확장된) C 런타임 라이브러리는 (커널 지원을 직접적으로 포함하지 않지만) 네이티브 응용 프로그램들에 쓰이는 많은 유틸리티 함수를 포함한다.
  - **Csr**은 Win32 하위 시스템 프로세스([csrss.exe](https://ko.wikipedia.org/wiki/csrss.exe "wikilink"))와 통신할 때 사용되는 클라이언트-서버 함수들이다.
  - **Dbg**는 소프트웨어 [브레이크포인트](../Page/브레이크포인트.md "wikilink") 같은 [디버깅](../Page/디버그.md "wikilink") 함수들이다.
  - **Ki**는 [APC](https://ko.wikipedia.org/wiki/비동기_프로시저_호출 "wikilink") 디스패칭 같은 이벤트들을 위한 커널 모드에서의 upcall들이다.
  - **Ldr**은 새로운 프로세스들을 시작시키는 것을 다루는 [PE](../Page/PE_포맷.md "wikilink") 파일을 위한 로더 함수들이다.
  - **Nls**는 [네이티브 언어 지원을](../Page/국제화와_지역화.md "wikilink") 위해 사용된다.
  - **Pfx**는 prefix를 다루기 위해 사용된다.

user32.dll과 gdi32.dll은 커널 모드로 가는 다른 호출도 포함한다. 이것은 과거에 하드웨어의 성능 문제로 인해 그래픽 서브 시스템을 커널 모드로 보내기로 결정했기 때문이다. 0x1000\~0x1FFF 범위의 시스템 호출들은 win32k.sys용이며, user32.dll과 gdi32.dll에서 정의된다. 이런 함수들은 **NtUser**, **NtGdi** 접두사가 붙는다.

또한 ntoskrnl.exe에서 나온 많은 그룹들이 있으며, 그 이유로 오직 커널 모드에서만 사용될 수 있다. 이것들은 네이티브 API에 포함되기도 하고, 되지 않기도 한다. **Cc**(cache controller), **Ex**([Windows Executive](https://ko.wikipedia.org/wiki/Architecture_of_Windows_NT "wikilink")), **FsRtl**(file system runtime), **Io**(I/O manager), **Ke**(core kernel routines), **Ks**(kernel streaming), **Lpc**([로컬 프로시저 호출](../Page/로컬_프로시저_호출.md "wikilink")), **Lsa**([로컬 보안 인증](../Page/로컬_보안_인증_하위_시스템_서비스.md "wikilink")), **Mm**(memory management), **Ob**([객체 관리자](../Page/객체_관리자.md "wikilink")), **Ps**([Process management](../Page/프로세스.md "wikilink")), **Se**(security), **Po**(power management) 등이 있다.\[3\]\[4\]\[5\]\[6\]\[7\]\[8\]

## 사용

  - 특권 부여와 회수 (RtlAdjustPrivilege)
  - 다른 세션에서 실행 중인 프로세스 내부에서 원격 쓰레드 생성 (RtlCreateUserThread)
  - 네이티브 응용 프로그램 실행 (RtlCreateUserProcess)
  - 강제 종료 (NtShutdownSystem)

## 같이 보기

  - [마이크로소프트 윈도 구성 요소 목록](https://ko.wikipedia.org/wiki/마이크로소프트_윈도_구성_요소_목록 "wikilink")
  - [윈도 API](https://ko.wikipedia.org/wiki/윈도_API "wikilink")

## 각주

## 외부 링크

  - [대부분의 네이티브 API 함수들이 정리된 웹사이트](http://undocumented.ntinternals.net/)
  - [Inside Native Applications](http://technet.microsoft.com/sysinternals/bb897447.aspx)
  - [Inside the Native API](https://web.archive.org/web/20121224002314/http://netcode.cz/img/83/nativeapi.html)
  - [Open source native applications development framework](http://zenwinx.sourceforge.net/)
  - [Native shell - Windows command prompt which can start before Winlogon and Win32 subsystem](http://hex.pp.ua/nt-native-applications-shell-eng.php)
  - [Windows NT Native Tools - A free native applications development util](http://sourceforge.net/projects/nativetools/)

[분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:윈도우 NT](https://ko.wikipedia.org/wiki/분류:윈도우_NT "wikilink") [분류:윈도우 NT 커널](https://ko.wikipedia.org/wiki/분류:윈도우_NT_커널 "wikilink") [분류:운영 체제 API](https://ko.wikipedia.org/wiki/분류:운영_체제_API "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.