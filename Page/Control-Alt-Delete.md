> This article is converted from Wikipedia: [Control-Alt-Delete](https://ko.wikipedia.org/wiki/Control-Alt-Delete).


[섬네일](https://ko.wikipedia.org/wiki/파일:Three-finger_salute.svg "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:GroenLinks_demonstration_20041002_CtrlAltDel-crop.JPG "wikilink") **Control-Alt-Delete** (컨트롤 알트 딜리트, 줄여서 **Ctrl-Alt-Del**)는 [PC 호환](../Page/IBM_PC_호환기종.md "wikilink") 시스템의 컴퓨터 키보드 명령으로, [도스](https://ko.wikipedia.org/wiki/도스 "wikilink")의 경우 컴퓨터를 다시 시동하거나, [마이크로소프트 윈도우](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink") 운영 체제의 경우 [작업 관리자](https://ko.wikipedia.org/wiki/작업_관리자 "wikilink") 및 윈도우 보안을 불러 오는 데에 쓰일 수 있다. [Control과](https://ko.wikipedia.org/wiki/Control_키 "wikilink") [Alt](https://ko.wikipedia.org/wiki/Alt_키 "wikilink") 키를 누르는 동안 [Delete](https://ko.wikipedia.org/wiki/Delete_키 "wikilink") 키를 누름으로써 명령을 내릴 수 있다.

이러한 키보드 조합은 [IBM PC를](https://ko.wikipedia.org/wiki/IBM_PC "wikilink") 설계한 [데이비드 브레들리가](https://ko.wikipedia.org/wiki/데이비드_브레들리 "wikilink") 도입한 것이다. 브레들리는 [소프트 다시 시동을](https://ko.wikipedia.org/wiki/시동 "wikilink") 불러 내기 위해 Control-Alt-[Escape를](https://ko.wikipedia.org/wiki/Esc_키 "wikilink") 설계했으나 키보드의 왼쪽에 위치해 있어 사용자가 실수로나 우발적으로 컴퓨터를 다시 시동시킬 가능성이 있음을 알게 된다. 그는 이 키를 Control-Alt-Delete로 바꿈으로써 한 손으로 이러한 작업을 할 수 없게 했다. (나중에 나온 키보드, 102 키 [PC/AT 키보드나](https://ko.wikipedia.org/wiki/기능_강화_키보드 "wikilink") [멜트론 키보드에는](https://ko.wikipedia.org/wiki/멜트론_키보드 "wikilink") 해당되지 않음) 더 고급 [운영 체제는](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 다양한 목적에서 사용하지만 특정한 구성이나 환경에서 소프트 다시 시동의 기능을 사용할 수 있게 해 놓았다. 브레들리는 이와 같은 말을 남기기도 했다: "저는 Control-Alt-Delete를 발명했을 뿐이지만, [빌 게이츠는](https://ko.wikipedia.org/wiki/빌_게이츠 "wikilink") 이를 널리 알리게 하였습니다."

## 도스 및 리얼 모드 시스템

[도스](https://ko.wikipedia.org/wiki/도스 "wikilink")나 [리얼 모드](../Page/리얼_모드.md "wikilink") 시스템에서 돌아가는 [PC에서](https://ko.wikipedia.org/wiki/개인용_컴퓨터 "wikilink"), 이러한 키 눌림 조합은 [바이오스](https://ko.wikipedia.org/wiki/바이오스 "wikilink")의 키보드 핸들링 코드에 의해 인지되어 [CPU의](https://ko.wikipedia.org/wiki/인텔_8086 "wikilink") [NMI](https://ko.wikipedia.org/wiki/NMI "wikilink") 신호(잘 쓰이지 않는 예외를 제외하고 소프트 다시 시동을 일으킴)로 처리된다.

## 윈도우

### DOS 기반 윈도우

[윈도우 3.0](../Page/윈도우_3.0.md "wikilink") 이하(와 표준 모드에서 돌아가는 [윈도우 3.1](https://ko.wikipedia.org/wiki/윈도우_3.1x "wikilink"))에서, Control-Alt-Delete는 단순히 MS-DOS 안에서 컴퓨터를 다시 시동시켰다. 386 확장 모드에서 돌아가는 윈도우 3.1, [윈도우 95](../Page/윈도우_95.md "wikilink"), [윈도우 98](../Page/윈도우_98.md "wikilink"), [윈도우 ME에서](https://ko.wikipedia.org/wiki/윈도우_Me "wikilink"), 이러한 키 눌림 조합은 윈도우 키보드 장치 드라이버에 의해 인지된다. system.ini의 \[386Enh\] 섹션 안에 있는 LocalReboot 옵션 값에 따라, 윈도우는 다음의 동작 가운데 하나를 응답하여 수행한다.:

  - `LocalReboot=Off`: [소프트 다시 시동을](https://ko.wikipedia.org/wiki/시동 "wikilink") 수행한다.
  - `LocalReboot=On`:
      - 윈도우 3.1은 시스템에 대한 응답이 멈춘 작업을 끝내기 위해 를 누르게끔 하는 [블루스크린](https://ko.wikipedia.org/wiki/블루스크린 "wikilink")을 방지하거나, 소프트 다시 시동을 수행하기 위해 Control-Alt-Delete키를 다시 누르게 한다.
      - 윈도우 95, 98, Me는 현재 실행되고 있는 [프로세스](../Page/프로세스.md "wikilink")를 나열하는 창이 열리지 않게 한다. 소프트 다시 시동을 수행하기 위해 Contrl-Alt-Delete키를 다시 누르게 한다.

프로그램이 [무한 반복에](https://ko.wikipedia.org/wiki/무한_반복 "wikilink") 들어갈 경우 작업/프로세스를 끝내는 것은 유용하다. 윈도우 3.1에서 이론적으로 리소스와 메모리 누수를 일으키는 시스템의 다른 프로세스들은 이러한 키 조합을 사용하여 끝냄으로써 정상적으로 계속 동작할 수 있다. 이러한 버전의 윈도우에서 프로세스를 끝내고 다른 응용 프로그램에서 작업 중인 자료를 저장하고 윈도우를 다시 시작하는 것을 강력히 권한다. 이러한 위험은 더 새로운 버전의 도스 기반 윈도우에서는 리소스 트랙킹 때문에 훨씬 일어날 가능성이 적다.

윈도우 9x에서, 프로세스 작업 창이 나타나지 않을 때 이러한 조합을 두 번 누르면 사용자가 조합 키를 3 번 누를 때까지 블루 스크린을 보여 준다.

### 윈도우 NT

[윈도우 NT와](https://ko.wikipedia.org/wiki/윈도우_NT "wikilink") 그 뒤의 운영체제 [윈도우 2000](../Page/윈도우_2000.md "wikilink"), [윈도우 XP](../Page/윈도우_XP.md "wikilink"), [윈도우 서버 2003](../Page/윈도우_서버_2003.md "wikilink"), [윈도우 비스타](../Page/윈도우_비스타.md "wikilink"), [윈도우 서버 2008에서](../Page/윈도우_서버_2008.md "wikilink") 키눌림 조합은 ("키보드 훅") [윈로그온](https://ko.wikipedia.org/wiki/윈로그온 "wikilink") 프로세스에 의해 인지되며, [GINA](https://ko.wikipedia.org/wiki/GINA "wikilink")를 통해 다음의 작업을 수행한다:

  - 아무도 로그인되어 있지 않으면, 로그인 대화 상자를 띄워서 사용자가 로그인할 수 있게 한다. 또한 컴퓨터가 잠궈져 있으면 잠금 해제 대화 상자를 띄운다.
  - 컴퓨터가 [도메인의](https://ko.wikipedia.org/wiki/윈도우_서버_도메인 "wikilink") 일부로 구성되어 있거나 윈도우 2000을 실행한다면, 키 조합은 "윈도우 보안" 대화상자를 띄워서 사용자가 컴퓨터를 잠그거나, 암호를 바꾸거나 로그 아웃하거나 컴퓨터를 끄거나 작업 관리자를 불러올 수 있게 한다. 이것은 컴퓨터가 도메인의 일부냐 아니냐에 관계 없이 윈도우 비스타와 윈도우 서버 2008의 기본 동작이다. 이 옵션들은 [그룹 정책](https://ko.wikipedia.org/wiki/그룹_정책 "wikilink")(역자 주: gpedit.msc)을 통해 제어할 수 있다.
  - [윈도우 XP가](../Page/윈도우_XP.md "wikilink") 도메인에 연결되어 있지 않은 경우
      - "새로운 시작" 화면과 [빠른 사용자 전환을](https://ko.wikipedia.org/wiki/빠른_사용자_전환 "wikilink") 켜고, Ctrl-Alt-Del은 [작업 관리자를](https://ko.wikipedia.org/wiki/작업_관리자 "wikilink") 불러온다.
      - "새로운 시작" 화면과 [빠른 사용자 전환을](https://ko.wikipedia.org/wiki/빠른_사용자_전환 "wikilink") 끄고, Ctrl-Alt-Del은 위에 언급한 바와 같이 윈도우 보안 대화 상자를 연다.

## OS/2

[OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")에서 이러한 키 조합은 OS/2 자판 장치 드라이버를 통해 인식되며 세션 관리자 프로세스에 이 신호를 전달한다. OS/2 버전 2.0 이후의 일반적인 세션 관리자 프로세스는 부모 프로세스 "워크플레이스 셸"이며 "시스템이 다시 시동합니다"라는 창을 보여주고 소프트 다시 시동을 일으키는 역할을 한다. 연속으로 두 번 누르면 OS/2는 세션 관리자 프로세스 응답을 기다리지 않고 즉시 소프트 다시 시동으로 들어간다.

## 리눅스

[리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")에서 이러한 키 조합은 [커널](https://ko.wikipedia.org/wiki/커널 "wikilink") 안의 자판 장치 드라이버를 통해 인식된다. 이 때 특별한 명령이 존재하지는 않은 까닭에 커널은 바로 소프트 다시 시동으로 넘어간다.

## 맥 OS

[맥 OS에서](https://ko.wikipedia.org/wiki/맥_OS "wikilink")  대신 사용되는  키를 조합하여 Control-Option-Delete를 눌러도, 아무 일도 일어나지 않는다. 윈도우에서처럼 강제로 시스템을 재시작하게 하기 위해서는 Control-Command-Power를 누른다. 시스템 프로세스를 재시작하는 창인 '응용 프로그램 강제 종료'를 열려면 Option-Command-Escape를 누른다. 오래된 애플 II나 애플 III에서, Control-Open Apple-Reset을 누르면 시스템은 소프트 시동으로 들어간다.

## 유명한 문화

컴퓨터가 어디든 존재하기 때문에 Control-Alt-Del 또한 유명하다. Ctrl-Alt-Del은 "버리다"라는 뜻으로 쓰이기도 한다.\[1\]

## 같이 보기

  - [윈로그온](https://ko.wikipedia.org/wiki/윈로그온 "wikilink") - Ctrl-Alt-Del을 찾아내고 그에 반응하는 윈도우 프로세스
  - [보안 키](https://ko.wikipedia.org/wiki/보안_키 "wikilink")

## 참고 문헌

<references />

### 일반 문헌

  - Windows 3.1 Resource Kit SYSTEM.INI 386ENH Section A-L, Microsoft's KnowledgeBase article, <http://support.microsoft.com./kb/q83435/>
  - Linux manual pages for kill(2) and reboot(2).

## 외부 링크

  - [데이비드 브레들리가 CTRL-ALT-DEL을 어떻게 발명했는지와 빌 게이츠가 이를 어떻게 널리 알렸는지를 서술해 준 영상](https://web.archive.org/web/20071029185546/http://www.worldspace.nu/The_origin_of_Control-Alt-Delete_-_David_Bradley_invented_CTRL-ALT-DEL_Bill_Gates_made_it_famous_avi:watch)

[분류:컴퓨터 자판](https://ko.wikipedia.org/wiki/분류:컴퓨터_자판 "wikilink") [분류:컴퓨터 키](https://ko.wikipedia.org/wiki/분류:컴퓨터_키 "wikilink") [분류:운영 체제 기술](https://ko.wikipedia.org/wiki/분류:운영_체제_기술 "wikilink")

1.  [Wordspy](http://www.wordspy.com/words/Ctrl-Alt-Delete.asp) cites the earliest such use as Chris Miksanek's December 18, 1995 Computerworld column titled, "Ctrl-Alt-Delete those holiday trinkets."