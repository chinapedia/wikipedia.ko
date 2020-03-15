> This article is converted from Wikipedia: [CONFIG.SYS](https://ko.wikipedia.org/wiki/CONFIG.SYS).


**CONFIG.SYS**는 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink")와 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink") [운영 체제를](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 위한 원초적인 설정 구성 파일이다. [컴퓨터](../Page/컴퓨터.md "wikilink") [시스템](https://ko.wikipedia.org/wiki/시스템 "wikilink")의 설정과 구성의 명령이 담겨 있는 특별한 파일이다. [컴퓨터](../Page/컴퓨터.md "wikilink")가 시동하자마자 이 파일을 불러내며, 각종 [하드웨어](https://ko.wikipedia.org/wiki/하드웨어 "wikilink")들의 드라이버를 불러오고, [연속 확장 메모리 규격이나](https://ko.wikipedia.org/wiki/연속_확장_메모리_규격 "wikilink") [중첩 확장 메모리 규격을](https://ko.wikipedia.org/wiki/중첩_확장_메모리_규격 "wikilink") 사용하거나, 버퍼나 파일의 수를 지정할 수 있다.

이 [파일을](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") 불러들인 다음에 [COMMAND.COM](../Page/COMMAND.COM.md "wikilink") 파일과 [AUTOEXEC.BAT](../Page/AUTOEXEC.BAT.md "wikilink") 파일을 불러낸다. [윈도 ME에서는](https://ko.wikipedia.org/wiki/윈도_ME "wikilink") 특별한 패치를 사용하지 않는 한 이 파일을 로드하지 않는다.

[셸](https://ko.wikipedia.org/wiki/셸 "wikilink") 명령어의 파일 위치를 바꾸려면 shell= 에다 위치를 지정하면 된다.

## 예

### MS-DOS

윈도 3.xx에 포함된 MS-DOS를 위한 CONFIG.SYS의 보기:

``` ini
 device=c:\dos\himem.sys
 device=c:\dos\emm386.exe ram
 dos=high,umb
 devicehigh=c:\windows\mouse.sys
 devicehigh=c:\dos\setver.exe
 country=044,437,c:\dos\country.sys
 shell=c:\dos\command.com c:\dos /e:512 /p
```

  - 첫 줄은 [himem.sys](https://ko.wikipedia.org/wiki/HIMEM "wikilink") 드라이버를 불러들여 도스가 [HMA](https://ko.wikipedia.org/wiki/HMA "wikilink")를 사용할 수 있게 한다.
  - 두 번째 줄은 [EMM386](https://ko.wikipedia.org/wiki/EMM386 "wikilink") 메모리 관리자를 불여들여 확장 메모리를 가상으로 구현해 낸다. 명령 줄 변수 *ram*은 [UMA](https://ko.wikipedia.org/wiki/UMA "wikilink")의 사용을 허용하는 것을 뜻한다. 다른 변수로는 *noems*가 있는데 이것은 고위 메모리를 사용하되 확장 메모리는 사용하지 않는다. noems 변수는 또한 UMB 블록의 여유 공간을 늘려 주기도 하며, 일부 응용 프로그램이 EMS의 존재 때문에 실행되지 못하는 문제를 해결하기도 한다.
  - 세 번째 줄은 가능하면 도스가 HMA와 UMA를 사용하게끔 설정하는 것이며, 응용 프로그램들이 사용할 [기본 메모리의](https://ko.wikipedia.org/wiki/기본_메모리 "wikilink") 여유 공간을 늘려 준다.
  - 네 번째, 다섯 번째 줄은 [장치 드라이버를](../Page/장치_드라이버.md "wikilink") UMA로 불러 들인다.
      - 네 번째 줄은 마이크로소프트사가 제공하는 마우스 드라이버이다.
      - 다섯 번째 줄은 도스 버전을 관리하는 호환 프로그램이다. (setver로 일부 도스 프로그램이 "Incorrect DOS version." 오류 메시지가 뜨지 않도록 할 수 있다)
  - 여섯 째 줄은 국제화 설정으로 [코드 페이지 437을](https://ko.wikipedia.org/wiki/코드_페이지_437 "wikilink") 설정하고 영국 코드 077를 사용하도록 한 예이다. 한국어 코드 페이지는 949이다.
  - 마지막 줄은 기본 셸 [COMMAND.COM](../Page/COMMAND.COM.md "wikilink")을 불러들이는 것으로 작업 디렉터리를 c:\\dos에서 시작하고 512 바이트의 환경 크기를 사용한다. /p 옵션은 부모(parent) 처리를 뜻하며 exit 명령어를 사용하여 프롬프트를 나갈 수 없게 한다.

MS-DOS 버전 6의 경우, 도스 시동 메뉴를 구성할 수 있는 옵션을 제공한다. 이로써 사용자는 수많은 시동 구성을 사용하여 시작 메뉴를 구성할 수 있다. 다양한 도스 응용 프로그램들이 선호하는 최적 기능의 설정값이 따르기 때문에 이러한 메뉴 구성은 큰 도움이 된다. 특히, [윈도 9x에서](https://ko.wikipedia.org/wiki/윈도_9x "wikilink") 16 비트 도스 드라이버와 유틸리티를 되도록 불러들이지 않는 것이 최상인데, 이때 이러한 메뉴 구성의 도움을 받는 것이 좋다.

MS-DOS 6 이상의 시동 메뉴가 포함된 CONFIG.SYS의 보기:

``` ini
 [menu]
  menuitem=WIN, Windows
  menuitem=XMS, DOS with only Extended Memory
  menudefault=WIN, 10
 [common]
  device=c:\dos\himem.sys
  dos=high,umb
  shell=c:\dos\command.com c:\dos /e:512 /p
  country=044,437,c:\dos\country.sys
 [WIN]
  device=c:\dos\emm386.exe ram
  devicehigh=c:\windows\mouse.sys
  devicehigh=c:\dos\setver.exe
 [XMS]
  device=c:\dos\emm386.exe noems
```

도스 시동 메뉴의 구조는 잘 조직화되어 있다. "\[menu\]" 섹션은 메뉴의 항목을 정의한다. "menudefault" 옵션은 시스템을 시작하기 전에 카운트다운 타이머로 기본 선택 사항을 사용하는 것을 허용한다. (여기서는 10초로 되어 있음) "\[common\]" 영역은 모든 메뉴 선택을 시작하는 줄이다. 반면 "\[WIN\]"과 "\[XMS\]" 영역은 저마다의 구성을 사용한다.

나중에 시동 파일, autoexec.bat는 CONFIG.SYS로부터 프로파일 메뉴를 받아서 따로 구성하는 것도 가능하다.

### 프리도스

프리도스의 최근 FDCONFIG.SYS 및 CONFIG.SYS:

``` ini
 screen=0x12
 device=c:\dos\himem.exe
 device=c:\dos\emm386.exe
 dos=high,umb
 country=044,437,c:\dos\country.sys
 shell=c:\dos\freecom.com c:\dos /e:512 /p
```

일반 .sys 파일들은 config.sys 안에서 위와 같이 호출되며, MS-DOS 6.x가 제공하는 [SMARTDRIVE](https://ko.wikipedia.org/wiki/SMARTDRIVE "wikilink") (역자 주: 스마트 드라이브는 하드 디스크의 속도를 빠르게 해 주는 유틸리티), 프리 도스의 LBACACHE(아까와 비슷한 성질을 가진 유틸리티)과 같은 .exe 프로그램들은 autoexec.bat 파일 안에서 불러들인다. 그러나, 명령 줄에서도 시스템 파일로서 .EXE뿐 아니라 .SYS 를 불러들이는 방법들이 있다. (역자 주: 시스템 장치 드라이버를 불러들이는 유틸리티는 명령 프롬프트에서 사용할 수 있는데 반드시 프리도스에서만 사용할 수 있는 것은 아니다.)

## 문제점

[섬네일가](https://ko.wikipedia.org/wiki/파일:PC-MOS-386_boot_screen.jpg "wikilink") 를 발견하지 못했다는 메시지를 출력하고 있다\]\] 시스템은 이러한 시스템 파일들(CONFIG.SYS, AUTOEXEC.BAT)이 분실되거나 손상되어도 시동할 수 있다. 그러나 이러한 두 개의 파일은 도스 운영 체제의 완전한 시동 과정에 필수적이다. 이러한 파일들은 개인용으로 운영 체제를 변경하는 데 쓰이는 정보를 포함하고 있다. 또 이러한 파일들은 다른 응용 소프트웨어 꾸러미들을 위한 요구 사항들도 포함하고 있다. 도스 시스템은 이러한 파일들이 손상된 경우 문제 해결을 요구할 수도 있다.

## 관련 항목

  - [AUTOEXEC.BAT](../Page/AUTOEXEC.BAT.md "wikilink")
  - [COMMAND.COM](../Page/COMMAND.COM.md "wikilink")
  - [HIMEM](https://ko.wikipedia.org/wiki/HIMEM "wikilink")
  - [프리도스](../Page/프리도스.md "wikilink")
  - [IO.SYS](https://ko.wikipedia.org/wiki/IO.SYS "wikilink")
  - [MSDOS.SYS](https://ko.wikipedia.org/wiki/MSDOS.SYS "wikilink")
  - [MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink")
  - [ANSI.SYS](https://ko.wikipedia.org/wiki/ANSI.SYS "wikilink")

## 외부 링크

  - [Information about the AUTOEXEC.BAT and the CONFIG.SYS](http://www.computerhope.com/ac.htm)

  - [Description of Windows 98 / MS-DOS 7.10 CONFIG.SYS directives](http://support.microsoft.com/?kbid=232557)

  - [Description of DR-DOS 7 CONFIG.SYS directives (incomplete)](https://web.archive.org/web/20160607164317/http://www.drdos.net/documentation/usergeng/09ugch9.htm#807)

  - [Description of FreeDOS CONFIG.SYS directives](http://help.fdos.org/en/hhstndrd/cnfigsys/index.htm)

  - [PTS-DOS 2000 Pro User Manual including a description of PTS-DOS CONFIG.SYS directives (incomplete)](http://download.paragon-software.com/doc/manual_dos_eng.pdf)

  - [Inoffizielle deutschsprachige PTS-DOS-FAQ (PTS/FAQD), inofficial German PTS-DOS FAQ as of 2004-04-25, including more CONFIG.SYS directives](http://www.almnet.de/ptsdos/ptsfaqd.html)

[분류:도스용 파일](https://ko.wikipedia.org/wiki/분류:도스용_파일 "wikilink") [분류:설정 파일](https://ko.wikipedia.org/wiki/분류:설정_파일 "wikilink")