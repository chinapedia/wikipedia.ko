> This article is converted from Wikipedia: [Windows.h](https://ko.wikipedia.org/wiki/Windows.h).


**windows.h**는 윈도우 개발자들이 필요한 모든 매크로들, 다양한 함수들과 서브시스템에서 사용되는 모든 데이터 타입들 그리고 [윈도우 API의](../Page/윈도우_API.md "wikilink") 함수들을 위한 정의를 포함하는 [윈도우의](../Page/마이크로소프트_윈도우.md "wikilink") [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 및 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 헤더 파일이다. 이것은 C에서도 사용될 수 있는 윈도우 용의 수 많은 함수들을 정의한다. Win32 API는 \<windows.h\>를 포함하고 적절한 라이브러리를 링킹함으로써 C 프로그래밍 프로젝트에 추가될 수 있다. *xxxx*.[dll의](../Page/동적_링크_라이브러리.md "wikilink") 함수를 사용하기 위해서는 프로그램은 반드시 *xxxx*.lib에 링크되어야 한다(또는 [MinGW](../Page/MinGW.md "wikilink")에서는 libxxxx.dll.a). 몇몇 헤더들은 .dll이 아닌 정적 라이브러리로 존재한다(예를들면 scrnsave.h는 scrnsave.lib를 필요로 한다).

## 자식 헤더 파일들

windows.h에 포함되는 많은 **자식 헤더 파일들**이 존재한다. 이러한 파일들 중 상당수는 의존성 때문에 간단하게 인클루드될 수 없다.

windows.h는 아마 다음의 헤더 파일들을 인클루드할 것이다:

  - excpt.h - [예외 처리](../Page/예외_처리.md "wikilink")
  - stdarg.h - 가변 인자 함수들(표준 C 헤더)
  - windef.h - 다양한 매크로와 타입들
  - winnt.h - 다양한 매크로와 타입들 ([윈도우 NT를](../Page/윈도우_NT.md "wikilink") 위한)
  - basetsd.h - 다양한 타입들
  - guiddef.h - [`GUID`](../Page/범용_고유_식별자.md "wikilink") 타입
  - [ctype.h](https://ko.wikipedia.org/wiki/ctype.h "wikilink") - 문자 분류 (표준 C 헤더)
  - [string.h](https://ko.wikipedia.org/wiki/string.h "wikilink") - 문자열과 버퍼들 (표준 C 헤더)
  - winbase.h - [kernel32.dll](../Page/윈도우_라이브러리_파일.md "wikilink"): 커널 서비스; advapi32.dll:커널 서비스(예를들면 CreateProcessAsUser 함수), 접근 제어(예를들면 AdjustTokenGroups 함수).
  - winerror.h - 윈도우 에러 코드
  - wingdi.h - [GDI](../Page/그래픽_장치_인터페이스.md "wikilink") (그래픽 장치 인터페이스)
  - winuser.h - user32.dll: 사용자 서비스
  - winnls.h - NLS (네이티브 언어 지원)
  - wincon.h - 콘솔 서비스
  - winver.h - 버전 정보
  - winreg.h - [윈도우 레지스트리](../Page/윈도우_레지스트리.md "wikilink")
  - winnetwk.h - WNet (윈도우 네트워킹)
  - winsvc.h - [윈도우 서비스와](../Page/윈도우_서비스.md "wikilink") [SCM](../Page/서비스_제어_관리자.md "wikilink") (서비스 제어 관리자)
  - imm.h - [IME](../Page/입력기.md "wikilink") (입력기)

### 추가적인 헤더 파일들

  - cderr.h - `CommDlgExtendedError` 함수 에러 코드
  - commdlg.h - 일반적인 대화 상자
  - dde.h - DDE (동적 데이터 교환)
  - ddeml.h - DDE 관리 라이브러리
  - dlgs.h - 일반 대화 상자를 위한 다양한 상수들
  - lzexpand.h - LZ (Lempel-Ziv) 압축/압축해제
  - mmsystem.h - 윈도우 멀티미디어
  - nb30.h - [NetBIOS](../Page/넷바이오스.md "wikilink")
  - rpc.h - [RPC](../Page/원격_프로시저_호출.md "wikilink") (원격 프로시저 호출)
  - shellapi.h - [윈도우 셸](../Page/윈도우_셸.md "wikilink") API
  - wincrypt.h - 암호화 API
  - winperf.h - 성능 모니터링
  - winresrc.h - 리소스에서 사용되는
  - winsock.h - Winsock (윈도우 소켓), 버전 1.1
  - winspool.h - [프린트 스풀러](../Page/스풀링.md "wikilink")
  - winbgim.h - [표준 그래픽 라이브러리](https://ko.wikipedia.org/wiki/표준_그래픽_라이브러리 "wikilink")

### OLE와 COM

  - ole2.h - [OLE](../Page/객체_연결_삽입.md "wikilink") (객체 연결 삽입)
  - objbase.h - [COM](../Page/컴포넌트_오브젝트_모델.md "wikilink") (컴포넌트 오브젝트 모델)
  - oleauto.h - [OLE 자동화](../Page/OLE_자동화.md "wikilink")
  - olectlid.h - 다양한 [GUID](../Page/범용_고유_식별자.md "wikilink") 정의들

## 매크로

여러 매크로들이 windows.h의 행위에 영향을 미친다.

  - UNICODE - 정의되었을 때 TCHAR를 CHAR 대신 [WCHAR로](../Page/확장_문자.md "wikilink") 사용되게 하며 모든 타입 관련 API 함수들과 텍스트와 관련된 메시지들을 -A 버전 대신 -W 버전으로 정의한다(이것은 윈도우 C 런타입의 _UNICODE 매크로와 비슷하다).
  - RC_INVOKED - C 컴파일러 대신 리소스 컴파일러(RC.EXE)가 사용될 때 정의된다.
  - WINVER - 새로운 운영 체제에서 사용 가능한 기능들을 활성화할 때 사용된다. [윈도우 XP의](../Page/윈도우_XP.md "wikilink") 경우에는 0x0501, [윈도우 비스타는](../Page/윈도우_비스타.md "wikilink") 0x0600이 정의된다.
  - WIN32_LEAN_AND_MEAN - 헤더 파일들의 크기를 줄이고 컴파일 속도를 향상시키기 위해 사용된다. 암호화, DDE, RPC, 윈도우 셸 그리고 Winsock 같은 것들을 배제한다.

## 같이 보기

[분류:C 라이브러리](https://ko.wikipedia.org/wiki/분류:C_라이브러리 "wikilink") [분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink")