> This article is converted from Wikipedia: [AUTOEXEC.BAT](https://ko.wikipedia.org/wiki/AUTOEXEC.BAT).


**AUTOEXEC.BAT**는 [MS-DOS](../Page/MS-DOS.md "wikilink") [운영 체제에서](../Page/운영_체제.md "wikilink") 찾을 수 있는 시스템 파일의 이름이다. 순수 문자열이 담긴 배치 파일이며 시동 장치의 [루트 디렉터리에](https://ko.wikipedia.org/wiki/루트_디렉터리 "wikilink") 위치해 있다. 이 파일의 이름은 "automatic (자동)"과 "execution (실행)"을 합친 것이며, 시스템이 시작할 때 자동으로 [명령어들을](../Page/명령어_\(컴퓨팅\).md "wikilink") 실행할 수 있도록 도와 주는 기능을 제공한다.

## 사용법

[윈도 95와](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") [윈도 98에서](https://ko.wikipedia.org/wiki/윈도_98 "wikilink") 쓰이는 MS-DOS 버전 7.x을 포함한 모든 버전의 도스는 컴퓨터가 시동하면 **AUTOEXEC.BAT**를 불러들인다. [윈도 ME는](https://ko.wikipedia.org/wiki/윈도_ME "wikilink") 환경 변수만 읽어 들이고 나머지 부분들을 사용하지 않지만 일종의 패치를 사용하여 **AUTOEXEC.BAT**의 모든 내용을 불러올 수 있다.

도스에서 이 파일은 운영 체제가 시동되면서 [CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink")가 처리된 뒤에 실행된다. [윈도 NT와](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") 그것을 잇는 [윈도 XP와](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") [윈도 비스타는](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") 사용자가 로그온할 때 **AUTOEXEC.BAT**의 일부 내용만을 불러 실행한다. [윈도 ME의](https://ko.wikipedia.org/wiki/윈도_ME "wikilink") 경우 환경 변수만 읽어 들이고 나머지는 읽어 들이지 않는다. CONFIG.SYS와 달리 **AUTOEXEC.BAT**의 명령어들은 도스 프롬프트에서 입력할 수도 있다. 컴퓨터가 켜지면 자동으로 실행되게끔 도와 주는데 내용에는 표준 명령어들로 이루어져 있을 뿐이며 일괄 파일을 포함할 수 있다.

**AUTOEXEC.BAT**는 [키보드](../Page/컴퓨터_자판.md "wikilink"), [사운드 카드](../Page/사운드_카드.md "wikilink"), [프린터](../Page/프린터.md "wikilink"), 그리고 임시 파일의 위치와 같은 환경 변수를 설정하는 데에 가장 흔히 사용된다.

  -
    **낮은 수준의 시스템 유틸리티들을 실행하는 데에도 쓰일 수 있다**:
      - 바이러스 검사 프로그램
      - 디스크 캐시 소프트웨어 - SMARTDRV.EXE (시스템의 속도가 빨라진다)
      - 마우스 드라이버 - 보통 MOUSE.COM
      - 키보드 드라이버
      - CD 드라이버 - 보통 MSCDEX.EXE
      - 기타 장치 드라이버

도스가 흔히 쓰이던 당시, 한국에는 많은 컴퓨터들이 [Mdir](../Page/Mdir.md "wikilink")을 사용하였는데 컴퓨터가 시동되자마 마자 Mdir이 실행되곤 했다. 이것도 AUTOEXEC.BAT의 마지막 줄에 Mdir이라는 프로그램이 등록되어 있었기 때문이다.

## 예

### MS-DOS

초기 버전의 도스에서, `AUTOEXEC.BAT`는 기본적으로 매우 단순하였다. XT 계열의 컴퓨터들은 배터리 백업형 [실시간 시계를](../Page/실시간_시계.md "wikilink") 기본으로 채용하고 있지 않았으므로, 초기 PC에는 DATE와 TIME 명령어가 필수적으로 들어가 있었다.

``` dos
 ECHO OFF
 CLS
 DATE
 TIME
 VER
```

미국 외 국가들에선 키보드 드라이버 (프랑스어 키보드를 위한 KEYBFR와 같이) 또한 포함되었다. 나중에 나온 버전들은 자주 수많은 서드 파티 장치 드라이버들과 더불어 확장되었다. 아래에는 기본 도스 5.x 형식의 `AUTOEXEC.BAT` 구성이며, 필수적인 명령어들만 포함하고 있다:

``` dos
 @ECHO OFF
 PROMPT $P$G
 PATH=C:\DOS;C:\WINDOWS
 SET TEMP=C:\TEMP
 SET BLASTER=A220 I7 D1 T2
 LH SMARTDRV.EXE
 LH DOSKEY
 LH MOUSE.COM /Y
 WIN
```

이러한 구성은 윈도 시작 전에 공통 환경 변수를 설정하고, 디스크 캐시 [SMARTDRIVE](https://ko.wikipedia.org/wiki/SMARTDRIVE "wikilink")를 불러들이며 (6째줄), 공통 디렉터리를 기본 [경로](../Page/경로.md "wikilink")로 설정하고, 도스 마우스 및 키보드 드라이버를 시작한다. PROMPT 명령어($P$G 변수 포함)는 [도스 프롬프트를](https://ko.wikipedia.org/wiki/도스_프롬프트 "wikilink") 기본적인 "C\>" 대신에 "C:\\\>"로 설정해 준다.

일반적으로 .sys 파일들은 `CONFIG.SYS`에서 호출되며, MS-DOS 5x에서 제공했던 SMARTDRIVE와 같은 디스크 캐시 소프트웨어와 같은 .exe 프로그램들은 `AUTOEXEC.BAT` 파일에서 불러들였다. 마우스와 같은 일부 장치들은 `CONFIG.SYS` 안에서 .sys 파일로 불러들이거나 `AUTOEXEC.BAT` 에서 .com 파일로 불러들일 수 있다[1](http://support.microsoft.com/kb/96706). 이는 제조업체에 따라 다르다.

"REM" 문자열로 시작하는 줄은 주석을 뜻하며 `AUTOEXEC.BAT`에서 이 줄을 일시적으로 사용하지 않겠다는 것을 말한다. 이와 비슷한 대체 문자열로 두 개의 콜론 (**::**)을 사용할 수 있다.

MS-DOS 6 이상에서, 도스 시동 메뉴를 설정할 수 있다. 다양한 프로그램들을 위한 최적의 시동 구성을 사용자가 정할 수 있기 때문에 큰 도움이 된다. 이를테면 도스 게임을 위한 메뉴와 윈도를 위한 메뉴를 따로 지정할 수 있다. ([CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink") 글에서 이어짐)

``` dos
 @ECHO OFF
 PROMPT $P$G
 PATH=C:\DOS;C:\WINDOWS
 SET TEMP=C:\TEMP
 SET BLASTER=A220 I7 D1 T2
 GOTO %CONFIG%
 :WIN
  LH SMARTDRV.EXE
  LH MOUSE.COM /Y
  WIN
 GOTO END
 :XMS
  LH SMARTDRV.EXE
  LH DOSKEY
  GOTO END
 :END
```

GOTO %CONFIG% 줄은 도스가 CONFIG.SYS 안에 정의해 둔 메뉴 항목을 찾아 본다. 그 뒤에, 이러한 프로파일들은 여기에 이름이 붙여져서 원하는 지정 드라이버와 유틸리티로 구성된다. 각 지정 구성의 끝에, GOTO 명령어를 사용하여(GOTO END로 지정되어 있음) 도스가 :END 섹션으로 끝나게 된다. :END 뒤의 항목은 모든 프로파일에서 쓰인다.

## 문제점

도스 위에 윈도 버전을 실행할 때 문제점들 가운데 하나는 기본 메모리의 부족이다. 이것은 초기 x86 프로세서의 아키텍처 설계에 기인한 것이며 1024 킬로바이트, 곧 효과적인 640킬로바이트의 메모리에 주소를 매길 수 있다. 이것이 나중에 새로운 프로세서 모드가 포함된 반면, 도스는 낮은 수준의 AUTOEXEC.BAT 형식 드라이버를 확장 메모리로 불러오지는 못했다. 이를 위해 사용자들은 LH 명령어를 사용해야 했다.

## 관련 항목

  - [COMMAND.COM](../Page/COMMAND.COM.md "wikilink")
  - [MS-DOS](../Page/MS-DOS.md "wikilink")

## 외부 링크

  - [Windows 98 CONFIG.TXT file](http://support.microsoft.com/?kbid=232557)

[분류:도스용 파일](https://ko.wikipedia.org/wiki/분류:도스용_파일 "wikilink") [분류:설정 파일](https://ko.wikipedia.org/wiki/분류:설정_파일 "wikilink")