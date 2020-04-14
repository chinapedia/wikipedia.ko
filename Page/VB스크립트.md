> This article is converted from Wikipedia: [VB스크립트](https://ko.wikipedia.org/wiki/VB스크립트).


**VB스크립트**(VBScript)는 [마이크로소프트](../Page/마이크로소프트.md "wikilink")가 개발한 [액티브 스크립트](https://ko.wikipedia.org/wiki/액티브_스크립트 "wikilink") 언어이다. 이 언어의 구문은 마이크로소프트의 [비주얼 베이직](../Page/비주얼_베이직.md "wikilink") 프로그래밍 언어 계통의 일부를 반영한다.

VB스크립트는 [윈도우 98](../Page/윈도우_98.md "wikilink") 이후의 여러 윈도우 운영 체제에서 기본으로 설치되어 있으며\[1\], [윈도우 서버](../Page/윈도우_서버.md "wikilink") 운영 체제의 경우 [윈도우 NT 4.0](../Page/윈도우_NT_4.0.md "wikilink") 옵션 팩 이후로 이용이 가능하다.\[2\] 또, 실행 중인 장치의 목적과 구성에 따라 [윈도우 CE에서도](https://ko.wikipedia.org/wiki/윈도우_CE "wikilink") 선택적으로 이용이 가능하다.

초기에는 1970년대 말에 처음 개발된 배치 언어보다 더 강력한 자동화 도구 검색에 대한 지원을 윈도우 관리자로부터 받았다. VB스크립트는 호스트 환경 안에서 실행되어야 하며, 어떠한 환경에서는 마이크로소프트 윈도우의 표준 설치([윈도우 스크립트 호스트](../Page/윈도우_스크립트_호스트.md "wikilink"), [윈도우 인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink")) 위에 제공된다. 게다가 VB스크립트 호스트 환경은 마이크로소프트 스크립트 컨트롤(*msscript.ocx*)과 같은 기술을 통해 다른 프로그램에 이식되는 경우가 있다.

## 예제

다음 예제는 Microsoft Windows NT 시스템의 WMI(Windows Management Instrumentation) 서비스를 이용하여 [메모장](https://ko.wikipedia.org/wiki/메모장 "wikilink") 프로그램의 프로세스(notepad.exe)를 종료시킨다.

``` vb
Option Explicit ' 변수 선언 요구
On Error Resume Next ' 오류가 발생해도 속행
Const ProcessToKill = "notepad.exe" ' 종료할 프로세스 명 지정 (notepad.exe)
Dim oWMI, oQuery, oProc, iCount ' 변수 선언
Set oWMI = GetObject("winmgmts:") ' 로컬 컴퓨터의 WMI 서비스에 접속하여 WMI 서비스 개체 취득
If Not IsObject(oWMI) Or oWMI Is Nothing Then ' WMI 서비스 개체를 얻는 데에 실패했다면
    ' 오류 메시지 출력
    MsgBox "WMI 서비스가 실행 중이 아닙니다." & vbCrLf & vbCrLf & _
    "이 스크립트는 윈도우 NT 이상, WMI 서비스가 실행 중인 컴퓨터에서만 실행 가능합니다.", vbCritical

    ' 종료 코드 1번으로 스크립트 실행 종료
    WScript.Quit 1
End If

' WMI 서비스에 쿼리를 보내 ProcessToKill 상수에 지정된 프로세스와 같은 프로세스 개체를 검색함
Set oQuery = oWMI.ExecQuery("SELECT * FROM win32_process WHERE Name = '" & ProcessToKill & "'")
iCount = 0 ' 프로세스 카운트 변수 초기화
' 쿼리 내에 검색된 각각의 모든 개체(프로세스 개체) oProc 들에 대해
For Each oProc In oQuery
    oProc.Terminate ' 프로세스를 강제로 종료
    iCount = iCount + 1 ' 프로세스 카운트를 하나 증가
Next ' oProc

' 결과를 사용자에게 출력
If iCount > 0 Then
    WScript.Echo "총 " & iCount & " 개의 메모장 프로세스가 종료되었습니다."
Else
    WScript.Echo "컴퓨터에 실행 중인 메모장 프로세스를 발견할 수 없었습니다."
End If

' 개체의 인스턴스를 해제함
Set oProc = Nothing
Set oQuery = Nothing
Set oWMI = Nothing
```

## 같이 보기

  - [액티브 스크립트](https://ko.wikipedia.org/wiki/액티브_스크립트 "wikilink")
  - [J스크립트](../Page/J스크립트.md "wikilink")
  - [J스크립트 닷 넷](https://ko.wikipedia.org/wiki/J스크립트_닷_넷 "wikilink")
  - [윈도우 스크립트 파일](https://ko.wikipedia.org/wiki/윈도우_스크립트_파일 "wikilink")
  - [윈도우 스크립트 호스트](../Page/윈도우_스크립트_호스트.md "wikilink")
  - [HTML 구성 요소](https://ko.wikipedia.org/wiki/HTML_구성_요소 "wikilink")

## 각주

<references />

## 외부 링크

  - [VBScript](https://web.archive.org/web/20080115205534/http://msdn2.microsoft.com/en-us/library/t0aew7h6.aspx) (마이크로소프트 개발자 네트워크)

[분류:베이직 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:베이직_프로그래밍_언어_계열 "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink") [분류:인터넷 익스플로러](https://ko.wikipedia.org/wiki/분류:인터넷_익스플로러 "wikilink") [분류:1996년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1996년_개발된_프로그래밍_언어 "wikilink")

1.  \[<http://msdn2.microsoft.com/en-us/library/x66z77t4(VS.85>).aspx *WSH Version Information*\], on MSDN
2.  [*VBScript Version Information*](http://msdn.microsoft.com/en-us/library/4y5y7bh5.aspx), on MSDN