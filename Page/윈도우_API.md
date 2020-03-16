> This article is converted from Wikipedia: [ API](https://ko.wikipedia.org/wiki/_API).


**윈도우 API**()는 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 운영 체제들이 사용하는 [API](../Page/API.md "wikilink")이다. [C](../Page/C_\(프로그래밍_언어\).md "wikilink")/[C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 프로그램에서 직접 운영 체제와 상호 작용할 수 있도록 만들어졌으며, 그보다 더 낮은 수준의 제어는 Ntdll.dll을 사용한 낮은 수준의 DLL로 가능하다.

## 개요

윈도우 API가 제공하는 기능은 다음과 같이 여덟 가지이다.\[1\]

  - 기본 서비스\[2\]: 이용할 수 있는 중요한 리소스를 윈도우 시스템에서 사용할 수 있게 도와 준다. [파일 시스템](../Page/파일_시스템.md "wikilink"), [장치](../Page/컴퓨터_하드웨어.md "wikilink"), [프로세스](../Page/프로세스.md "wikilink"), [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink"), [오류 처리와](../Page/예외_처리.md "wikilink") 같은 것들을 포함한다. 이러한 기능들은 16비트 윈도우의 경우 `kernel.exe`, `krnl286.exe`, `krnl386.exe` 파일에, 32비트 윈도우의 경우 [`kernel32.dll`](https://ko.wikipedia.org/wiki/kernel32.dll "wikilink")에 상주한다.
    고급 서비스
    부가 기능을 커널에 사용할 수 있게 도와 준다. [윈도 레지스트리](https://ko.wikipedia.org/wiki/윈도_레지스트리 "wikilink"), 시스템 종료/다시 시작 (또는 중단), [윈도 서비스](https://ko.wikipedia.org/wiki/윈도_서비스 "wikilink") 시작/중지/만들기, 사용자 계정 만들기와 같은 것들을 포함한다. 이러한 기능들은 32비트 윈도우의 `advapi32.dll`에 상주한다.

  - [그래픽 장치 인터페이스](../Page/그래픽_장치_인터페이스.md "wikilink") (GDI)\[3\]: 출력되는 그래픽 콘텐츠를 [모니터](https://ko.wikipedia.org/wiki/컴퓨터_디스플레이 "wikilink"), [프린터](../Page/프린터.md "wikilink"), 기타 [출력 장치에](https://ko.wikipedia.org/wiki/출력_장치 "wikilink") 전달하는 기능을 제공한다. 16비트 윈도우의 경우 `gdi.exe`에, 사용자 모드에서의 32비트 윈도우의 경우 [`gdi32.dll`](https://ko.wikipedia.org/wiki/gdi32.dll "wikilink")에 상주한다. 커널 모드 GDI 지원은 그래픽 드라이버와 직접 통신하는 `win32k.sys`가 제공한다.\[4\]
    [사용자 인터페이스](https://ko.wikipedia.org/wiki/윈도_사용자 "wikilink")\[5\]: 화면 [창뿐](../Page/창_\(컴퓨팅\).md "wikilink") 아니라 단추와 스크롤바와 같은 가장 기본적인 컨트롤을 만들어 관리하고, 마우스와 키보드 입력을 받는 기능, 윈도우의 [GUI와](../Page/그래픽_사용자_인터페이스.md "wikilink") 연동하는 기능을 제공한다. 이 기능은 16비트 윈도의 경우 `user.exe`에, 32비트 윈도의 경우 [`user32.dll`](https://ko.wikipedia.org/wiki/user32.dll "wikilink")에 상주한다. [윈도 XP](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") 버전 이후로 기본 컨트롤은 공통 컨트롤(공통 컨트롤 라이브러리)과 함께 [`comctl32.dll`](https://ko.wikipedia.org/wiki/comctl32.dll "wikilink")에 상주한다.
    공통 대화 상자 라이브러리\[6\]: 응용 프로그램에 파일 열기 및 저장, 색 및 글꼴 선택 등을 위한 표준 [대화 상자를](https://ko.wikipedia.org/wiki/대화_상자 "wikilink") 제공한다. 16비트 윈도의 경우 `commdlg.dll`에, 32비트 윈도의 경우 [`comdlg32.dll`](https://ko.wikipedia.org/wiki/comdlg32.dll "wikilink")에 상주한다. 이 라이브러리는 API의 "사용자 인터페이스" 집합에 들어 있다.
    공통 컨트롤 라이브러리\[7\]: 응용 프로그램이 운영 체제가 제공하는 일부 고급 컨트롤에 접근할 수 있게 도와 준다. 여기에는 [상태 표시줄](https://ko.wikipedia.org/wiki/상태_표시줄 "wikilink"), [진행 표시줄](https://ko.wikipedia.org/wiki/진행_표시줄 "wikilink"), [도구 모음](../Page/도구_모음.md "wikilink"), [탭을](../Page/탭_브라우징.md "wikilink") 포함한다. 이 라이브러리는 [DLL](../Page/동적_링크_라이브러리.md "wikilink") 파일에 상주하는데, 16비트 윈도의 경우 [`commctrl.dll`](https://ko.wikipedia.org/wiki/commctrl.dll "wikilink")에, 32비트 윈도의 경우 `comctl32.dll`에 상주한다. 이 라이브러리는 API의 "사용자 인터페이스" 집합에 들어 있다.
    윈도 셸\[8\]\[9\]: 윈도 API의 구성 요소는 응용 프로그램이 [운영 체제 셸이](https://ko.wikipedia.org/wiki/운영_체제_셸 "wikilink") 제공하는 기능에 접근하고 변경하고 강화할 수 있게 도와 준다. 이 구성 요소는 16비트 윈도의 경우 [`shell.dll`](https://ko.wikipedia.org/wiki/shell.dll "wikilink")에, 32비트 윈도의 경우 [`shell32.dll`](https://ko.wikipedia.org/wiki/shell32.dll "wikilink")에 상주한다. 셸 라이트웨이트(Shell Lightweight) 유틸리티 기능은 [`shlwapi.dll`](https://ko.wikipedia.org/wiki/shlwapi.dll "wikilink")에 있다. 이 라이브러리는 API의 "사용자 인터페이스" 집합에 들어 있다.
    네트워크 서비스\[10\]: 다양한 [네트워킹](../Page/컴퓨터_네트워크.md "wikilink") 기능을 운영 체제에 제공한다. [넷바이오스](../Page/넷바이오스.md "wikilink"), [윈속](https://ko.wikipedia.org/wiki/윈속 "wikilink"), [NetDDE](https://ko.wikipedia.org/wiki/NetDDE "wikilink"), [RPC](../Page/원격_프로시저_호출.md "wikilink") 등을 포함한다.

### 웹

[인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") 웹 브라우저 또한 응용 프로그램에 자주 쓰이는 수많은 API를 노출하며 이러한 것들은 윈도 API의 일부로 간주할 수 있다. 인터넷 익스플로러는 [윈도 98 SE](https://ko.wikipedia.org/wiki/윈도_98_SE "wikilink") 이후의 운영 체제부터 포함되어 왔으며 [윈도 98](https://ko.wikipedia.org/wiki/윈도_98 "wikilink") 이후로 웹 관련 서비스를 제공하고 있다.\[11\] 구체적으로 다음과 같은 가능을 제공하는 데에 쓰인다:

  - 추가할 수 있는 웹 브라우저 컨트롤: [`shdocvw.dll`](https://ko.wikipedia.org/wiki/shdocvw.dll "wikilink") 및 [`mshtml.dll`](https://ko.wikipedia.org/wiki/Trident_\(layout_engine\) "wikilink")에 포함되어 있음.
  - URL 모니터 서비스: COM 오브젝트를 응용 프로그램에 제공하는 `urlmon.dll`가 관할함. 응용 프로그램은 자체 URL 핸들러를 제공할 수 있다.
  - 다중 언어 및 국제 텍스트 지원 보조 라이브러리 (mlang.dll).
  - DirectX 변형 (이미지 필터 구성 요소 집합).
  - XML 지원 (MSXML 구성 요소, `msxml*.dll`가 관할).
  - 윈도 주소록에 접속.

## [Hello world 프로그램](https://ko.wikipedia.org/wiki/Hello_world_프로그램 "wikilink")

``` c
#include <Windows.h>
#include <tchar.h>

int APIENTRY _tWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPTSTR lpCmdLine, int nCmdShow)
{
    MessageBox(NULL, TEXT("Hello, world"), TEXT("App"), MB_OK);
    return 0;
}
```


\=== 멀티미디어 === 마이크로소프트는 [윈도 95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") OSR2 이후로 [DirectX](../Page/DirectX.md "wikilink") 집합의 API를 모든 윈도 설치본의 일부로 제공하고 있다. DirectX는 멀티미디어와 게임 서비스를 제공한다:

  - [Direct3D](../Page/Direct3D.md "wikilink"): 3차원 하드웨어 그래픽 가속.
  - [DirectDraw](https://ko.wikipedia.org/wiki/DirectDraw "wikilink"): 2차원 프레임버퍼 하드웨어 가속. DirectX 8에서 이 구성 요소는 Direct3D의 선호로 배제되었다.
  - [DirectSound](https://ko.wikipedia.org/wiki/DirectSound "wikilink"): 낮은 수준의 사운드 카드 가속.
  - [DirectInput](https://ko.wikipedia.org/wiki/DirectInput "wikilink"): 조이스틱과 게임패드와 같은 입력 장치와 통신.
  - [DirectPlay](https://ko.wikipedia.org/wiki/DirectPlay "wikilink"): 멀티플레이어 게임 인프라 역할.
  - [DirectShow](https://ko.wikipedia.org/wiki/DirectShow "wikilink"): 일반적인 멀티미디어 파이프라인을 만들고 실행.
  - [DirectMusic](https://ko.wikipedia.org/wiki/DirectMusic "wikilink"): MIDI 파일을 재생하는 데 이용하였으나 지금은 배제됨.

## 버전

모든 윈도 운영 체제들은 버전마다 새로운 API 함수를 추가했으나, 이들을 가리키는 이름은 구조가 크게 변화할 때만 바뀌었다. 나중에 마이크로소프트는 이전 버전과 현재 버전, 그리고 나중에 발표될 버전의 API를 통틀어서 ‘윈도 API’라는 이름으로 부르기 시작했다.

  - **Win16**은 [16비트](../Page/16비트.md "wikilink") 버전의 마이크로소프트 윈도에서 사용했다. 대부분의 Win16 API는 kernel.exe(또는 krnl286.exe나 krnl386.exe), user.exe, gdi.exe에 구현되어 있으며, [확장자가](../Page/파일_확장자.md "wikilink") .exe이지만 실제로 이들은 [동적 링크 라이브러리이다](../Page/동적_링크_라이브러리.md "wikilink").
  - **Win32**는 [32비트](../Page/32비트.md "wikilink") 버전의 마이크로소프트 윈도에서 사용하며, 현재 널리 쓰이고 있는 버전이다. Win32 API의 핵심 DLL은 [kernel32.dll](https://ko.wikipedia.org/wiki/kernel32.dll "wikilink"), [user32.dll](https://ko.wikipedia.org/wiki/user32.dll "wikilink"), [gdi32.dll](https://ko.wikipedia.org/wiki/gdi32.dll "wikilink")이다.
  - **[Win32s](../Page/Win32s.md "wikilink")**(Win32 subset)는 [윈도 3.1x](https://ko.wikipedia.org/wiki/윈도_3.1 "wikilink") 버전에서 Win32 API를 일부 구현한 확장이다.
  - **64비트 윈도를 위한 Win32**(Win32 for 64-bit Windows, 이전에는 **Win64**)는 [64비트](../Page/64비트.md "wikilink") 버전([IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink")와 [AMD64](https://ko.wikipedia.org/wiki/AMD64 "wikilink") 둘 다)의 마이크로소프트 윈도에서 사용한다. 실제로는 [하드웨어 가상 계층](https://ko.wikipedia.org/wiki/하드웨어_가상_계층 "wikilink") 때문에 Win32와 큰 차이가 없으며, 32비트용 실행 파일을 64비트 윈도에서도 수정 없이 돌릴 수 있다. ([WOW64](../Page/WOW64.md "wikilink"))

## 다른 구현물

마이크로소프트의 윈도 API 구현물은 저작권으로 보호 받지만, 일반적으로 이 구현물을 모방하여 독자적인 구현물을 만들면 법적인 문제를 피할 수 있다고 알려져 있다. 대표적으로 [와인](../Page/와인_\(소프트웨어\).md "wikilink")(Wine) 프로젝트는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제에서 Win32의 [호환성 계층을](https://ko.wikipedia.org/wiki/호환성_계층 "wikilink") 구현하고 있으며, 더 나아가 [ReactOS](https://ko.wikipedia.org/wiki/ReactOS "wikilink")는 와인의 많은 부분을 함께 쓰면서 완전한 윈도 운영 체제를 모방하고 있다.

## 각주

<references />

## 같이 보기

  - [닷넷 프레임워크](../Page/닷넷_프레임워크.md "wikilink")
  - [오브젝트 윈도 라이브러리](https://ko.wikipedia.org/wiki/오브젝트_윈도_라이브러리 "wikilink")
  - [MFC](../Page/마이크로소프트_파운데이션_클래스_라이브러리.md "wikilink")

## 외부 링크

  - [Microsoft Developer Network Windows API development guide](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/windows_api_start_page.asp)

[분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink")

1.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (July 2005). *[Overview of the Windows API.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/overview_of_the_windows_api.asp)* Retrieved August 28, 2005.
2.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (July 2005). *[Base Services.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/base_services.asp)* Retrieved August 28, 2005.
3.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (July 2005). *[Graphics Device Interface.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/graphics_device_interface.asp)* Retrieved August 28, 2005.
4.
5.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (July 2005). *[User Interface.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/user_interface.asp)* Retrieved August 28, 2005.
6.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (2005). *[Common Dialog Box Library.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winui/winui/windowsuserinterface/userinput/commondialogboxlibrary.asp)* Retrieved September 22, 2005.
7.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (July 2005). *[Common Control Library.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/common_control_library.asp)* Retrieved August 28, 2005.
8.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (July 2005). *[Windows Shell.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/windows_shell.asp)* Retrieved August 28, 2005.
9.  [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (2005). *[Shell Programmer's Guide.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/shellcc/platform/shell/programmersguide/shell_intro.asp)* Retrieved August 28, 2005.
10. [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (July 2005). *[Network Services.](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winprog/winprog/network_services.asp)* Retrieved August 28, 2005.
11. [마이크로소프트 개발자 네트워크](../Page/마이크로소프트_개발자_네트워크.md "wikilink") (January 2006); *[Programming and reusing the browser](http://msdn.microsoft.com/library/default.asp?url=/workshop/browser/prog_browser_node_entry.asp) * Retrieved January 22, 2006.