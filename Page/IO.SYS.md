> This article is converted from Wikipedia: [IO.SYS](https://ko.wikipedia.org/wiki/IO.SYS).


**IO.SYS**는 [MS-DOS](../Page/MS-DOS.md "wikilink")와 [윈도 9x](https://ko.wikipedia.org/wiki/윈도_9x "wikilink") 계열의 운영체제에서 없어서는 안 되는 부분이다. 기본 MS-DOS [장치 드라이버](../Page/장치_드라이버.md "wikilink") (하드웨어 인터페이스 방식)와 도스 초기화 프로그램을 포함하고 있다. 기본적으로 이 파일은 시동할 수 있는 드라이브의 루트에 위치해 있으며 (보통 C:\\), 특성이 숨김, 읽기 전용, 시스템 파일로 설정이 되어 있다.

[개인용 컴퓨터의](../Page/개인용_컴퓨터.md "wikilink") 시동 순서에서, 시동 디스크의 첫 섹터는 메모리로 불러들이고 실행된다. 도스 [시동 섹터에](https://ko.wikipedia.org/wiki/시동_섹터 "wikilink") 있으면, IO.SYS의 첫 3 개의 섹터를 메모리로 불러들인 뒤 제어권을 IO.SYS에 전송한다. IO.SYS는 그러므로 다음과 같은 작업을 한다:

1.  남은 부분을 메모리 안으로 불러들인다.
2.  각 기본 [장치 드라이버를](../Page/장치_드라이버.md "wikilink") [콘솔](https://ko.wikipedia.org/wiki/콘솔 "wikilink"), 디스크, [직렬 포트](../Page/직렬_포트.md "wikilink") 등 안에서 순서대로 초기화한다. 이 점에서 기본 장치들을 사용할 수 있게 된다.
3.  도스 커널을 불러들이고 그것의 초기화 방식을 호출한다. 커널은 MS-DOS의 [MSDOS.SYS](../Page/MSDOS.SYS.md "wikilink")와 윈도 9x의 IO.SYS에 저장되어 있다. 여기서 "일반" 파일 접근을 사용할 수 있다.
4.  윈도 9x와 더불어 MSDOS.SYS 파일을 처리한다.
5.  MS-DOS 2.0 이후와 윈도 9x에서 [CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink")를 처리한다.
6.  [COMMAND.COM](../Page/COMMAND.COM.md "wikilink")을 불러들인다. (다른 [운영 체제 셸이](https://ko.wikipedia.org/wiki/운영_체제_셸 "wikilink") 지정되어 있으면 이것도 불러들인다)
7.  윈도 9x에서는 [부트스플래시](https://ko.wikipedia.org/wiki/부트스플래시 "wikilink")를 보여 준다. [Logo.sys](https://ko.wikipedia.org/wiki/Logo.sys "wikilink")가 존재하면, 이것이 부트스플래시로 사용된다. 이 파일이 없으면 IO.SYS 안에 있는 부트스플래시가 사용된다. (부트스플래시는 시동시 띄우는 로고의 그림)

[DR DOS와](https://ko.wikipedia.org/wiki/DR_DOS "wikilink") 다른 일부 도스 운영 체제들은 `IO.SYS`을 사용하지 않고 [IBMBIO.COM](https://ko.wikipedia.org/wiki/IBMBIO.COM "wikilink") 파일을 사용한다.

## 같이 보기

  - [MSDOS.SYS](../Page/MSDOS.SYS.md "wikilink")

## 외부 링크

  - [MS-DOS Device Driver Names Cannot be Used As File Names](http://support.microsoft.com/kb/74496/en-us) — includes list of default device drivers.

  - [SYS.COM Requirements in MS-DOS Versions 2.0-6.0](http://support.microsoft.com/kb/66530/en-us) — includes requirements for IO.SYS to be loaded.

[분류:도스용 파일](https://ko.wikipedia.org/wiki/분류:도스용_파일 "wikilink")