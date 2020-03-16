> This article is converted from Wikipedia: [DLL ](https://ko.wikipedia.org/wiki/DLL_).


[컴퓨터 프로그래밍에서](../Page/컴퓨터_프로그래밍.md "wikilink"), **DLL 인젝션**(DLL injection)은 다른 프로세스의 주소 공간 내에서 DLL을 강제로 로드시킴으로써 코드를 실행시키는 기술이다.\[1\] DLL 인젝션은 외부 프로그램을 통해 다른 프로그램에 저작자가 의도하거나 예상하지 않은 영향을 미치기 위해 사용된다.\[2\]\[3\]\[4\] 예를 들면 삽입된 코드는 시스템 함수 호출을 [후킹](../Page/후킹.md "wikilink") 하거나\[5\]\[6\] 또는 보통 방식으로는 읽을 수 없는 [패스워드](https://ko.wikipedia.org/wiki/암호 "wikilink") 텍스트 박스의 내용을 읽을 수 있다.\[7\] 임의적인 코드를 삽입하는데 사용되는 프로그램을 **DLL injector**라고 부른다.

## 마이크로소프트 윈도우에서의 접근

[마이크로소프트 윈도우에는](../Page/마이크로소프트_윈도우.md "wikilink") 프로세스에게 DLL의 코드를 로드하고 실행시키는 여러 방법이 있다.

  - [레지스트리](https://ko.wikipedia.org/wiki/레지스트리 "wikilink") 엔트리 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Windows\AppInit_DLLs` 에 목록화 된 DLL들은 User32.dll(이것이 프로세스에 부착되는 순간)을 로드하는 모든 프로세스에서 로드된다.\[8\]\[9\]\[10\]\[11\] [윈도우 비스타를](../Page/윈도우_비스타.md "wikilink") 시작으로, AppInit_DLL들은 기본 설정으로 비활성화 되어 있다.\[12\] Windows 7 이후로, AppInit_DLL 하부 구조는 code signing을 지원한다.
  - 레지스트리 키  `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\AppCertDLLs` 아래 목록화 된 DLL들은 Win32 API 함수들인 CreateProcess, CreateProcessAsUser, CreateProcessWithLogonW, CreateProcessWithTokenW 그리고 WinExec를 호출할 때 로드된다.
  - CreateRemoteThread 같은 프로세스 조작 함수들은 실행 중인 프로그램에 DLL을 삽입하기 위해서 사용될 수 있다.\[13\]\[14\]\[15\]\[16\]\[17\]\[18\]
    1.  타겟 프로세스의 handle을 오픈한다. 이것은 프로세스를 생겨나게 하거나<ref>

</ref>\[19\] 프로세스에 의해 생겨났으며 존재한다고 알려진 것(예를 들면 예상 가능한 타이틀을 가진 [윈도우](../Page/창_\(컴퓨팅\).md "wikilink")\[20\])을 키 오프하거나, 실행중인 프로세스들\[21\]의 목록을 얻고 타겟 실행 파일의 이름을 조사함으로써 이루어된다.\[22\]

\*\# 타겟 프로세스에서 메모리를 할당하고,\[23\] 할당받은 메모리에 인젝트될 DLL의 이름을 쓴다.\[24\]\[25\]

\*\#: 이 단계는 만약 적절한 DLL 이름이 이미 타겟 프로세스 안에서 사용 가능하다면 건너뛸 수 있다. 예를 들면, 프로세스가 ‘User32.dll’, ‘GDI32.dll’, ‘[Kernel32.dll](../Page/윈도우_라이브러리_파일.md "wikilink")’ 또는 ‘32.dll’로 끝나는 다른 라이브러리와 링크되어 있다면, 로드하는 것이 가능하다. 이 기술은 과거에는 DLL 인젝션에서 프로세스들을 지키는 방식에 대해 효과적이라고 입증되었다.\[26\]

\*\# 타겟 프로세스에 새로운 [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink")를\[27\] (스레드의 시작 주소는 LoadLibrary의 주소로, 인수는 타겟에 업로드되는 문자열의 주소로 해서) 생성한다.\[28\]\[29\]

\*\#: 로드될 DLL의 이름을 쓰고 LoadLibrary에서 새로운 스레드를 시작하는 것 대신, 실행 가능한 코드를 타겟에 넣고, 그 코드를 실행시키는 것도 가능하다.\[30\]

\*\# 운영체제는 이제 삽입된 DLL에서 DllMain을 호출할 것이다.\[31\]\[32\]

\*: 경계 없이, 이 접근은 (스레드 시작 시 모든 로드된 모듈에 보내지는) DLL_THREAD_ATTACH 알림 때문에 타겟 프로세스에게 발견될 수 있다.\[33\]

  - SetWindowsHookEx 같은 윈도우 [후킹](../Page/후킹.md "wikilink") 함수.\[34\]\[35\]\[36\]\[37\]\[38\]\[39\]
  - 모든 스레드들을 중지시키기 위해 SuspendThread 또는 NtSuspendThread 함수를 사용하고 삽입된 코드를 실행할 목적으로, 존재하는 응용 프로그램 내의 스레드의 문맥을 수정하기 위해 SetThreadContext나 NtSetContextThread 함수를 사용하면 DLL이 로드된다.\[40\]\[41\]\[42\]
  - 익스플로잇은 윈도우에서 한계치들을 디자인하고 모든 검증된 DLL 경로 명시 없이 LoadLibrary() 함수를 호출하는 응용 프로그램들을 로드된다.\[43\]
  - 응용 프로그램에 명시된 DLL을 원본 같이 똑같은 함수 호출을 내보내게 구현된 로그 교체로 대체하는 것.\[44\]

## 유닉스 계열에서의 접근

[유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영체제에서 (ld.so (on [BSD](../Page/BSD.md "wikilink")) 또는 ld-linux.so (on [리눅스](../Page/리눅스.md "wikilink"))를 기반으로 한 동적 링커와 함께) 임의적인 라이브러리들은 LD_PRELOAD 환경 변수 내에 있는라이브러리의 경로 이름을 줌으로써 새로운 프로세스에 링크될 수 있다. 이것은 한 프로세스 안에서 전역적으로 또는 개별적으로 세팅될 수 있다.\[45\]

예를 들면, [배시 셸에서](../Page/배시_\(유닉스_셸\).md "wikilink"), 이 명령어는 실행 시 링크되는 "test.so" 파일에서 공유 라이브러리와 함께 "prog" 명령어를 실행한다.

`LD_PRELOAD="./test.so" prog`

이러한 라이브러리는 [GCC에](../Page/GNU_컴파일러_모음.md "wikilink") 의해서 -fpic or -fPIC 옵션을 통해 링크될 새로운 전역변수를 포함하는 소스 파일을 컴파일하고,\[46\] `-shared` 옵션으로 링크함으로써 생성될 수 있다.\[47\] 이 라이브러리는 프로그램에서 선언된 외부 심볼들에 대한 접근을 갖는다.

또한 디버거 기반 기술도 사용 가능하다.\[48\]

## 각주

## 외부 링크

  - [Spying Internet Explorer 8.0 by DLL injection - Brian Mariani](https://www.htbridge.com/publications/spying_internet_explorer_8_0.html)

[분류:라이브러리](https://ko.wikipedia.org/wiki/분류:라이브러리 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink") [분류:스레드](https://ko.wikipedia.org/wiki/분류:스레드 "wikilink") [분류:DLL 인젝션](https://ko.wikipedia.org/wiki/분류:DLL_인젝션 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12. [AppInit_DLLs in Windows 7 and Windows Server 2008 R2](http://download.microsoft.com/download/7/E/7/7E7662CF-CBEA-470B-A97E-CE7CE0D98DC2/AppInit_Win7.docx)
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.