> This article is converted from Wikipedia: [HIMEM.SYS](https://ko.wikipedia.org/wiki/HIMEM.SYS).


**HIMEM.SYS**는 도스 프로그램들이 연속 확장 메모리 규격 (XMS)을 통해 [연속 확장 메모리에](../Page/연속_확장_메모리.md "wikilink") 데이터를 저장할 수 있게 도와준다. 특별히 이 장치 드라이버는 중요한데, 다양한 버전의 (역자 주: 운영 체제가 아닌) 마이크로스프트 윈도가 도스 운영 체제 위에서 돌릴 수 있는 것은 HIMEM.SYS가 로드된 뒤이기 때문이다.

MS-DOS 5.0에서 **HIMEM.SYS**가 소개되었으며 사용할 수 있는 [기본 메모리를](../Page/기본_메모리.md "wikilink") 늘리기 위해 [CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink")에다 DOS=HIGH라는 구문을 집어 넣음으로써 도스 커널 코드를 [고위 메모리 영역](../Page/고위_메모리_영역.md "wikilink") (HMA)으로 로드해서 쓸 수 있었다.

HIMEM.SYS는 첫 1 메가바이트 이상의 메모리 공간에 접근할 수 있고 윈도 9x/ME가 운영 체제의 그래픽 부분을 불러내는 데에도 필요하다. [프리도스](../Page/프리도스.md "wikilink")에서 **HIMEM.EXE**라는 파일이 있는데 이것은 프리도스 구성 파일인 **FDCONFIG.SYS** 또는 **CONFIG.SYS**에서 불러올 수 있다.

HIMEM이 시스템에서 사용되고 있지 않는 경우, EMM386과 같은 EMS 메모리 관리자는 사용할 수 없다.

## HIMEM.SYS의 스위치

대부분의 경우는 아래와 같이 하나하나 스위치 옵션을 추가하지 않아도 된다. HIMEM.SYS의 기본값은 대부분의 하드웨어에서 정상 동작하도록 설계되어 있기 때문이다.\[1\]

  -
    <small>DEVICE=\[드라이브:\]\[경로\]HIMEM.SYS \[/A20CONTROL:ON|OFF\] \[/CPUCLOCK:ON|OFF\] \[/EISA\] \[/HMAMIN=숫자\] \[/INT15=숫자\] \[/NUMHANDLES=숫자\] \[/MACHINE:숫자\] \[/SHADOWRAM:ON|OFF\] \[/TESTMEM:ON|OFF\] \[/VERBOSE\]</small>

<!-- end list -->

  - **/A20CONTROL:ON|OFF**

<!-- end list -->

  -
    HIMEM이 A20 라인의 제어권을 얻을 것인지를 지정한다. A20 핸들러는 컴퓨터 접근에 HMA를 제공한다. /A20CONTROL:OFF를 지정할 경우, HIMEM은 A20이 꺼져 있는 경우에만 A20의 제어권을 얻는다. 기본값은 /A20CONTROL:ON이다.

<!-- end list -->

  - **/CPUCLOCK:ON|OFF**

<!-- end list -->

  -
    HIMEM이 컴퓨터의 클럭 속도에 영향을 미칠지 지정한다. HIMEM을 설치할 때 컴퓨터 클럭 속도가 바뀐다면, /CPUCLOCK:ON을 지정하여 이 문제를 수정할 수 있다. 그러나 이 옵션을 켜게 되면 HIMEM의 속도를 떨어트린다. 기본값은 /CPUCLOCK:OFF이다.

<!-- end list -->

  - **/EISA**

<!-- end list -->

  -
    HIMEM이 사용 가능한 모든 확장 메모리를 할당할 것인지 지정한다. 이 스위치는 16메가 바이트 메모리 이상을 장착한 EISA 컴퓨터에서만 필수적이다. 다른 컴퓨터의 경우, HIMEM은 자동으로 사용 가능한 모든 확장 메모리를 할당한다.

<!-- end list -->

  - **/HMAMIN=숫자**

<!-- end list -->

  -
    HIMEM이 응용 프로그램에게 HMA를 사용할 수 있도록, 한 응용 프로그램이 요구하는 메모리의 양(단위: 킬로바이트)을 지정한다. 한 응용 프로그램은 한 번에 HMA를 사용할 수 있다. HIMEM은 이 옵션에 상응하는 첫 응용 프로그램에 HMA를 할당한다. 0에서 63까지 지정할 수 있다. 기본값은 /HMAMIN=0이다. 이 옵션을 0으로 두거나 사용하지 않는 경우, HIMEM은 이 기능이 필요한 첫 응용 프로그램에 무조건 HMA를 할당하도록 지정된다. 윈도가 386 확장 모드에서 실행되고 있는 경우 이 옵션은 아무런 영향을 미치지 않는다.

<!-- end list -->

  - **/INT15=숫자**

<!-- end list -->

  -
    인터럽트 15h 인터페이스를 위해 보유할 확장 메모리(단위: 킬로바이트)를 할당한다.

<!-- end list -->

  - **/NUMHANDLES=숫자**

<!-- end list -->

  -
    동시에 처리할 수 있는 확장 메모리 블록 (EMB)의 최대 수를 지정한다. 1에서 128까지 지정할 수 있다. 기본값은 /NUMHANDLES=32이다. 윈도가 386 확장 모드에서 실행되고 있을 경우 /NUMHANDLES 옵션은 아무런 영향을 미치지 않는다.

<!-- end list -->

  - **/MACHINE:숫자**

<!-- end list -->

  -
    사용 중인 컴퓨터의 종류를 지정한다. 보통 HIMEM은 사용자 컴퓨터의 종류를 성공적으로 알아낸다. 그러나 일부 컴퓨터의 경우 HIMEM이 찾아내지 못한다. 이러한 시스템에서 HIMEM은 기본 시스템 유형(IBM AT 호환)을 사용한다. HIMEM이 적절하게 시스템 종류를 사용할 수 있게 하려면, /MACHINE 옵션을 사용해야 한다.
    :\*1: at, IBM AT 호환
    :\*2: ps2, IBM PS/2
    :\*3: ptlcascade, Phoenix Cascade BIOS
    :\*4: hpvectra, HP Vectra (A & A+)
    :\*5: att6300plus, AT\&T 6300 Plus
    :\*6: acer1100, Acer 1100
    :\*7: toshiba, Toshiba 1600 & 1200XE
    :\*8: wyse, Wyse 12.5 Mhz 286
    :\*9: tulip, Tulip SX
    :\*10: zenith, Zenith ZBIOS
    :\*11: at1, IBM PC/AT (alternative delay)
    :\*12: at2, IBM PC/AT (alternative delay)
    :\*12: css, CSS Labs
    :\*13: at3, IBM PC/AT (alternative delay)
    :\*13: philips, Philips
    :\*14: fasthp, HP Vectra
    :\*15: ibm7552, IBM 7552 Industrial Computer
    :\*16: bullmicral, Bull Micral 60
    :\*17: dell, Dell XBIOS

<!-- end list -->

  - **/SHADOWRAM:ON|OFF**

<!-- end list -->

  -
    섀도 RAM을 사용하지 않을 것인지(SHADOWRAM:OFF), 아니면 램에서 실행 중인 ROM 코드를 남길 것인지(SHADOWRAM:ON) 지정한다.

<!-- end list -->

  - **/TESTMEM:ON|OFF**

<!-- end list -->

  -
    HIMEM이 컴퓨터가 시작될 때 메모리 테스트를 수행할지 결정한다. 기본값은 /TESTMEM:ON이다.

<!-- end list -->

  - **/VERBOSE**

<!-- end list -->

  -
    HIMEM이 로드하는 동안 상태 메시지와 오류 메시지를 보여 줄 지 결정한다. 기본적으로 HIMEM은 오류가 일어나도 메시지를 띄우지 않는다. 줄여서 /V 옵션을 사용할 수도 있다.

## 같이 보기

  - [기본 메모리](../Page/기본_메모리.md "wikilink")
  - [고위 메모리 영역](../Page/고위_메모리_영역.md "wikilink")
  - [연속 확장 메모리](../Page/연속_확장_메모리.md "wikilink")

## 참조

<references />

[분류:도스용 파일](https://ko.wikipedia.org/wiki/분류:도스용_파일 "wikilink") [분류:도스용 드라이버](https://ko.wikipedia.org/wiki/분류:도스용_드라이버 "wikilink") [분류:도스 메모리 관리](https://ko.wikipedia.org/wiki/분류:도스_메모리_관리 "wikilink")

1.