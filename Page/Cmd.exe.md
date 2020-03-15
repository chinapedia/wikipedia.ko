> This article is converted from Wikipedia: [Cmd.exe](https://ko.wikipedia.org/wiki/Cmd.exe).


**명령 프롬프트**(실행 파일이름: **`cmd.exe`**)는 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [윈도우 임베디드 컴팩트](https://ko.wikipedia.org/wiki/윈도우_임베디드_컴팩트 "wikilink") 그리고 [윈도우 NT](https://ko.wikipedia.org/wiki/윈도우_NT "wikilink") 5.0 이상 기반 시스템의 [명령어 인터프리터이다](https://ko.wikipedia.org/wiki/명령어_인터프리터 "wikilink"). [MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink")와 [윈도우 9x](../Page/윈도우_9x.md "wikilink") 시스템의 [`COMMAND.COM`](../Page/COMMAND.COM.md "wikilink") 또는 유닉스 시스템에서 쓰이던 [셸의](https://ko.wikipedia.org/wiki/유닉스_셸 "wikilink") 아날로그 형태이다.

## 확장

[Therese Stowell은](https://ko.wikipedia.org/wiki/Therese_Stowell "wikilink") `cmd.exe`의 첫 버전을 개발했다.\[1\] 일부 도스 명령어들이 지원되지 않거나 바뀌었음에도 불구하고 (예: 내용이 존재하는 디렉터리를 지우는 명령어 `deltree.exe`의 기능이 RD의 /S 매개 변수로 대체), `cmd.exe`는 수많은 내부 명령어들을 많이 가지고 있다.

OS/2와 윈도우 NT 버전의 `cmd.exe` 둘 다 `command.com`의 "명령 또는 파일 이름이 틀립니다(Bad command or file name)" 보다 더 자세한 오류 메시지를 제공한다. OS/2 버전의 `cmd.exe`에서는 오류가 현재의 시스템 언어가 무엇이든지 간에 보고된다. **help** 명령어는 오류 메시지의 번호와 함께 제공하여 더 자세한 정보를 얻을 수 있다.

[도스](https://ko.wikipedia.org/wiki/도스 "wikilink") 프로그램인 `COMMAND.COM`와 달리 `cmd.exe`는 플랫폼에 기본으로 제공되는 프로그램이다. 도스 프로그램들에는 쓸 수 없으나 네이티브 프로그램들이 플랫폼에서 사용할 수 있는 장점을 허락한다. 예를 들어, `cmd.exe`는 OS/2에서 네이티브 텍스트 모드 응용 프로그램이기 때문에 명령 파이프 줄에서 실제 파이프를 사용할 수 있고, 이로써 파이프라인의 두 면이 동시에 실행될 수 있다. 그 결과, `cmd.exe`의 표준 오류를 `COMMAND.COM`과 달리 리다이렉트할 수 있다. (`COMMAND.COM`은 임시 파일을 사용하며 두 면을 직렬로 사용한다.)

기술적으로, `cmd.exe`는 도스와 같은 명령 줄 해석기 역할을 하는 윈도우 프로그램이다. 일반적으로 호환되지만, `COMMAND.COM`에는 없었던 제한이 있는 확장을 제공한다:

  - `SETLOCAL`/`ENDLOCAL` 명령어들은 환경에 변화의 제약을 받는다
  - 내부 `CALL` 및 `GOTO` 레이블은 배치 파일이 작업의 일부를 수행할 필요를 줄여 준다.
  - `SET` 명령어에 대한 파일 이름을 나누는 확장은 [C 셸과](https://ko.wikipedia.org/wiki/C_셸 "wikilink") 호환된다.
  - 표현 평가 확장은 또한 `SET` 명령어에서 제공된다.

이 확장들은 사용하지 않을 수도 있고, 강력한 호환성 모드를 제공하기도 한다.

[윈도우 비스타와](../Page/윈도우_비스타.md "wikilink") [윈도우 서버 2008의](../Page/윈도우_서버_2008.md "wikilink") 일부로 남겨진 `cmd.exe`는 떨어진 호환성을 위해 [윈도우 파워셸을](https://ko.wikipedia.org/wiki/윈도우_파워셸 "wikilink") 사용하여 보충할 수 있다.

## 명령어

  - *cd*(디렉터리 이동 명령어)등으로 explorer.exe 없이 파일들을 탐색할 수 있다.

  - **color**등의 명령어로 간단히 프롬프트 디자인을 바꿀 수 있다.

  - 로 화면을 최대화할 수 있다. (윈도우 XP 이하와 윈도우 10에서 가능)

### 명령 프롬프트의 명령어 종류

1.  [ASSOC](https://ko.wikipedia.org/wiki/ASSOC "wikilink") 파일 확장명 연결을 보여주거나 수정합니다.
2.  ATTRIB 파일 속성을 표시하거나 바꿉니다.
3.  BREAK 확장된 CTRL+C 검사를 설정하거나 지웁니다.
4.  BCDEDIT 부팅 로딩을 제어하기 위해 부팅 데이터베이스에서 속성을 설정합니다.
5.  CACLS 파일의 액세스 컨트롤 목록(ACL)을 표시하거나 수정합니다.
6.  CALL 한 일괄 프로그램에서 다른 일괄 프로그램을 호출합니다.
7.  CD 현재 디렉터리 이름을 보여주거나 바꿉니다.
8.  CHCP 활성화된 코드 페이지의 번호를 표시하거나 설정합니다.
9.  CHDIR 현재 디렉터리 이름을 보여주거나 바꿉니다.
10. CHKDSK 디스크를 검사하고 상태 보고서를 표시합니다.
11. CHKNTFS 부팅하는 동안 디스크 확인을 화면에 표시하거나 변경합니다.
12. CLS 화면을 지웁니다.
13. CMD Windows 명령 인터프리터의 새 인스턴스를 시작합니다.
14. COLOR 콘솔의 기본색과 배경색을 설정합니다.
15. COMP 두 개 또는 여러 개의 파일을 비교합니다.
16. COMPACT NTFS 분할 영역에 있는 파일의 압축을 표시하거나 변경합니다.
17. CONVERT FAT 볼륨을 NTFS로 변환합니다. 현재 드라이브는 변환할 수 없습니다.
18. COPY 하나 이상의 파일을 다른 위치로 복사합니다.
19. DATE 날짜를 보여주거나 설정합니다.
20. DEL 하나 이상의 파일을 지웁니다.
21. DIR 디렉터리에 있는 파일과 하위 디렉터리 목록을 보여줍니다.
22. DISKPART 디스크 파티션 속성을 표시하거나 구성합니다.
23. DOSKEY 명령줄을 편집하고, Windows 명령을 다시 호출하고, 매크로를 만듭니다.
24. DRIVERQUERY 현재 장치 드라이버 상태와 속성을 표시합니다.
25. ECHO 메시지를 표시하거나 ECHO를 켜거나 끕니다.
26. ENDLOCAL 배치 파일에서 환경 변경의 지역화를 끝냅니다.
27. ERASE 하나 이상의 파일을 지웁니다.
28. EXIT CMD.EXE 프로그램(명령 인터프리터)을 종료합니다.
29. FC 두 파일 또는 파일 집합을 비교하여 다른 점을 표시합니다.
30. FIND 파일에서 텍스트 문자열을 검색합니다.
31. FINDSTR 파일에서 문자열을 검색합니다.
32. FOR 파일 집합의 각 파일에 대해 지정된 명령을 실행합니다.
33. FORMAT Windows에서 사용할 디스크를 포맷합니다.
34. FSUTIL 파일 시스템 속성을 표시하거나 구성합니다.
35. FTYPE 파일 확장명 연결에 사용되는 파일 형식을 표시하거나 수정합니다.
36. GOTO Windows 명령 인터프리터가 일괄 프로그램에서 이름표가 붙여진 줄로 이동합니다.
37. GPRESULT 컴퓨터 또는 사용자에 대한 그룹 정책 정보를 표시합니다.
38. GRAFTABL Windows가 그래픽 모드에서 확장 문자 세트를 표시할 수 있게 합니다.
39. HELP Windows 명령에 대한 도움말 정보를 제공합니다.
40. ICACLS 파일과 디렉터리에 대한 ACL을 표시, 수정, 백업 또는 복원합니다.
41. IF 일괄 프로그램에서 조건 처리를 수행합니다.
42. LABEL 디스크의 볼륨 이름을 만들거나, 바꾸거나, 지웁니다.
43. MD 디렉터리를 만듭니다.
44. MKDIR 디렉터리를 만듭니다.
45. MKLINK 바로 가기 링크와 하드 링크를 만듭니다.
46. MODE 시스템 장치를 구성합니다.
47. MORE 출력을 한번에 한 화면씩 표시합니다.
48. MOVE 하나 이상의 파일을 한 디렉터리에서 다른 디렉터리로 이동합니다.
49. OPENFILES 파일 공유에서 원격 사용자에 의해 열린 파일을 표시합니다.
50. PATH 실행 파일의 찾기 경로를 표시하거나 설정합니다.
51. PAUSE 배치 파일의 처리를 일시 중단하고 메시지를 표시합니다.
52. POPD PUSHD에 의해 저장된 현재 디렉터리의 이전 값을 복원합니다.
53. PRINT 텍스트 파일을 인쇄합니다.
54. PROMPT Windows 명령 프롬프트를 변경합니다.
55. PUSHD 현재 디렉터리를 저장한 다음 변경합니다.
56. RD 디렉터리를 제거합니다.
57. RECOVER 불량이거나 결함이 있는 디스크에서 읽을 수 있는 정보를 복구합니다.
58. REM 배치 파일 또는 CONFIG.SYS에 주석을 기록합니다.
59. REN 파일 이름을 바꿉니다.
60. RENAME 파일 이름을 바꿉니다.
61. REPLACE 파일을 바꿉니다.
62. RMDIR 디렉터리를 제거합니다.
63. ROBOCOPY 파일과 디렉터리 트리를 복사할 수 있는 고급 유틸리티입니다.
64. SET Windows 환경 변수를 표시, 설정 또는 제거합니다.
65. SETLOCAL 배치 파일에서 환경 변경의 지역화를 시작합니다.
66. SC 서비스(백그라운드 프로세스)를 표시하거나 구성합니다.
67. SCHTASKS 컴퓨터에서 실행할 명령과 프로그램을 예약합니다.
68. SHIFT 배치 파일에서 바꿀 수 있는 매개 변수의 위치를 바꿉니다.
69. SHUTDOWN 컴퓨터의 로컬 또는 원격 종료를 허용합니다.
70. SORT 입력을 정렬합니다.
71. START 지정한 프로그램이나 명령을 실행할 별도의 창을 시작합니다.
72. SUBST 경로를 드라이브 문자에 연결합니다.
73. SYSTEMINFO 컴퓨터별 속성과 구성을 표시합니다.
74. TASKLIST 서비스를 포함하여 현재 실행 중인 모든 작업을 표시합니다.
75. TASKKILL 실행 중인 프로세스나 응용 프로그램을 중단합니다.
76. TIME 시스템 시간을 표시하거나 설정합니다.
77. TITLE CMD.EXE 세션에 대한 창 제목을 설정합니다.
78. TREE 드라이브 또는 경로의 디렉터리 구조를 그래픽으로 표시합니다.
79. TYPE 텍스트 파일의 내용을 표시합니다.
80. VER Windows 버전을 표시합니다.
81. VERIFY 파일이 디스크에 올바로 기록되었는지 검증할지 여부를 지정합니다.
82. VOL 디스크 볼륨 레이블과 일련 번호를 표시합니다.
83. XCOPY 파일과 디렉터리 트리를 복사합니다.
84. WMIC 대화형 명령 셸 내의 WMI 정보를 표시합니다.

## 커맨드 라인 2.0 업데이트

[윈도우 10부터](../Page/윈도우_10.md "wikilink") 명령 프롬프트의 커맨드 라인 버전이 업데이트되었다. 명령 프롬프트의 속성에서 '레거시 콘솔 사용'을 해제하면 사용할 수 있는 기능들이 추가되었다.\[2\]

### 추가된 기능

  - 투명도 설정

  - 키의 일반적인 사용 설정

  - 사용 허용됨(Windows 7에서는 실행되지 않았다. 도 작동되지 않는다. Windows 10은 도 잘 작동한다(OS 단축키로 등록).)

## 같이 보기

  - [셸](https://ko.wikipedia.org/wiki/셸 "wikilink")
  - [도스박스](../Page/도스박스.md "wikilink")
  - [COMMAND.COM](../Page/COMMAND.COM.md "wikilink")

## 각주

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink") [분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:OS/2 명령어](https://ko.wikipedia.org/wiki/분류:OS/2_명령어 "wikilink") [분류:셸](https://ko.wikipedia.org/wiki/분류:셸 "wikilink")

1.
2.  [MS, 윈도우10에 커맨드라인 2.0 투입](http://www.zdnet.co.kr/news/news_view.asp?artice_id=20141014090625)