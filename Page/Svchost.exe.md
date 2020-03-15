> This article is converted from Wikipedia: [Svchost.exe](https://ko.wikipedia.org/wiki/Svchost.exe).


[윈도우 NT](https://ko.wikipedia.org/wiki/윈도우_NT "wikilink") 계열의 [운영 체제에서](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") **svchost.exe**는 서비스를 관할하기 위한 [프로세스](../Page/프로세스.md "wikilink")의 이름이며 관련 이미지 (실행 파일)이다. 이 서비스들은 [동적 링크 라이브러리](https://ko.wikipedia.org/wiki/동적_링크_라이브러리 "wikilink")(DLL)에 포함되어 있다.

## 서비스 및 설정 나열

서비스에 대한 정보는 [윈도우 레지스트리의](../Page/윈도우_레지스트리.md "wikilink") 서비스 레지스트리 키(HKLM\\SYSTEM\\CurrentControlSet\\Services)에 저장된다. 서비스 키의 ImagePath 설정이 svchost.exe를 가리키고 있으면 서비스는 레지스트리 키가 관할하고 있는 것이다. svchost.exe 프로세스는 HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\SvcHost라는 레지스트리 하부 키를 확인함으로써 자기가 서비스인지를 알아낸다. 여러 개의 서비스를 하나의 프로세스로 묶으면 컴퓨터 리소스를 보존할 수 있다. 그러나 서비스들 가운데 하나가 통제할 수 없는 예외를 일으킨다면 프로세스 전반이 충돌할 수 있다. 그뿐 아니라 구성 요소 서비스를 알아내는 것은 최종 사용자에게 더 어려울 수 있다. 윈도우 NT 5.1 (XP) 이후의 에디션에서 tasklist 명령어에 /svc 스위치를 사용하면 각 프로세스의 구성 요소 서비스 목록을 나열한다. 윈도우 6.0 (비스타) 이후에서는 윈도우 [작업 관리자의](https://ko.wikipedia.org/wiki/작업_관리자 "wikilink") "서비스" 탭에 서비스와 서비스 그룹, 그리고 프로세스 ID (PID)를 나열한다. 마이크로소프트의 [시스인터널스의](https://ko.wikipedia.org/wiki/윈인터널스 "wikilink") [프로세스 익스플로러를](../Page/프로세스_익스플로러.md "wikilink") 이용하여도 svchost.exe 프로세스에서 실행 중인 서비스에 대한 정보를 알 수 있다.

## 보안 문제

svchost.exe가 일반 시스템 프로세스로 쓰이기 때문에 일부 [악성 코드가](https://ko.wikipedia.org/wiki/악성_코드 "wikilink") 이따금씩 스스로를 가장하여 "svchost.exe"라는 프로세스 이름을 사용하는 경우가 있다. [윈도우 서버 업데이트 서비스](../Page/윈도우_서버_업데이트_서비스.md "wikilink") 3.0의 2007년 4월 30일판에서 100% CPU 사용률, 메모리 잡아먹기, 과도한 노트북 컴퓨터의 팬/전력 사용을 비롯한 svchost.exe 문제가 보고되었다.\[1\]

## 같이 보기

  - [윈도우 NT 시작 프로세스](https://ko.wikipedia.org/wiki/윈도우_NT_시작_프로세스 "wikilink")

## 각주

<references />

## 외부 링크

  - [svchost.exe의 마이크로소프트 지원 페이지](http://support.microsoft.com/?kbid=314056)
  - [How to find processes behind svchost.exe](http://www.happysysadm.com/2010/11/svchostexe.html)

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink")

1.  [Microsoft Automatic Updates Fix not Working - PCWorld](http://www.pcworld.com/article/131770-1/article.html?tk=nl_dnxnws)