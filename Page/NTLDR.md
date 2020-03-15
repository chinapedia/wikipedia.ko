> This article is converted from Wikipedia: [NTLDR](https://ko.wikipedia.org/wiki/NTLDR).


**NTLDR**는 **NT 로더**(*NT Loader*)의 준말로, [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink") [윈도우 NT](https://ko.wikipedia.org/wiki/윈도우_NT "wikilink") 계열 [운영 체제를](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 위한 [시동 로더이다](https://ko.wikipedia.org/wiki/시동 "wikilink"). 이를테면 [윈도우 XP와](../Page/윈도우_XP.md "wikilink") [윈도우 서버 2003을](../Page/윈도우_서버_2003.md "wikilink") 들 수 있다. NTLDR은 보통 원본의 [하드 디스크 드라이브에서](https://ko.wikipedia.org/wiki/하드_디스크_드라이브 "wikilink") 실행되지만 [CD-ROM](../Page/CD-ROM.md "wikilink"), [USB 플래시 드라이브](../Page/USB_플래시_드라이브.md "wikilink"), 플로피 디스크와 같은 휴대용 기억 장치에서도 실행할 수 있다. NTLDR은 또한 어떠한 파일의 적절한 [시동 섹터가](https://ko.wikipedia.org/wiki/시동_섹터 "wikilink") 주어진다면 NT 기반이 아닌 운영 체제를 불러들일 수도 있다.

NTLDR은 적어도, 시스템 볼륨 위에 다음의 두 개의 파일들이 필요하다:

  - `NTLDR`: 기본 시동 로더 자체이다.
  - `boot.ini`: 시동 메뉴를 위한 구성 옵션을 포함하고 있다. ([윈도우 비스타](../Page/윈도우_비스타.md "wikilink") 이후의 운영 체제부터는 이를 포함하지 않는다.)

NT 기반의 운영 체제에서 로드할 경우 [ntdetect.com](https://ko.wikipedia.org/wiki/ntdetect.com "wikilink")이 반드시 존재해야 한다. (정확히 말하면 NTLDR만이 실제로 필요하지만 boot.ini가 존재하지 않으면 NTLDR은 기본적으로 첫 하드 드라이브의 첫 파티션에 있는 c:\\windows 디렉터리를 잡게 된다. 가정의 많은 데스크톱 컴퓨터들은 이러한 구성을 따르며 boot.ini 파일이 없어지면 이러한 파일이 존재하지 않는다는 오류와 C:\\windows로 부팅하겠습니다. 라는 메시지가 출력되며 윈도우로 성공적으로 시동된다.)

윈도우 NT [포맷](../Page/디스크_포맷.md "wikilink") 명령에 의해 디스크에 기록된 [볼륨 시동 레코드는](https://ko.wikipedia.org/wiki/볼륨_시동_레코드 "wikilink") NTLDR 프로그램을 불러들이고 실행한다.

[윈도우 비스타와](../Page/윈도우_비스타.md "wikilink") [윈도우 서버 2008의](../Page/윈도우_서버_2008.md "wikilink") 경우, NTLDR이 아닌 다른 시동 로더를 사용한다. 시동 로더 기능은 다음의 두 가지 새로운 구성요소로 대체되어 있다.

  - [winload.exe](https://ko.wikipedia.org/wiki/윈도우_비스타_시작_프로세스#winload.exe "wikilink")
  - [윈도우 시동 관리자](https://ko.wikipedia.org/wiki/윈도우_비스타_시작_프로세스 "wikilink")

## 시작 프로세스

시동할 때, 로드 프로그램의 NTLDR은 다음의 순서를 따른다:

1.  시동 드라이브의 파일 시스템에 접근한다. (현재로써는 [FAT](../Page/파일_할당_테이블.md "wikilink") 또는 NT 파일 시스템 [NTFS](../Page/NTFS.md "wikilink"))
2.  *hiberfil.sys*를 발견하여 최대 절전 모드의 이미지를 찾는다면, 이에 대한 내용은 메모리로 불러들이고 시스템이 꺼질 때 재개된다.
3.  *hiberfil.sys*를 발견하지 않은 경우, *boot.ini*를 읽어내고 (역자 주: 여러 개의 운영 체제가 설치되어 있는 등의 경우) 시동 메뉴를 사용자에게 보여준다.
4.  NT 기반이 아닌 운영 체제가 선택되면, NTLDR은 *boot.ini* 안에 나열된 연결 파일을 불러들이고 제어권을 제공한다. 도스 기반의 도스로 시동하거나 연결 파일을 따로 지정하지 않으면 연결 파일로 bootsect.dos를 찾는다.
5.  NT 기반의 운영 체제가 선택되면, NTLDR은 *ntdetect.com*을 실행하여 사용자 컴퓨터의 하드웨어에 대한 정보를 얻는다. (ntdetect가 하드웨어 감지 도중에 멈추는 것을 대비하여, 마이크로소프트 지원\[[https://web.archive.org/web/20060109212835/http://www.microsoft.com/windows2000/techinfo/reskit/tools/existing/ntdetect-o.asp\]에서](https://web.archive.org/web/20060109212835/http://www.microsoft.com/windows2000/techinfo/reskit/tools/existing/ntdetect-o.asp%5D에서) 찾을 수 있는 ntdetect.chk라고 불리는 디버그 버전이 있다.)
6.  *[Ntoskrnl.exe](https://ko.wikipedia.org/wiki/Ntoskrnl.exe "wikilink")*를 실행하여 *ntdetect.com*가 반환한 정보를 내보낸다.\[1\]

## 단점

(윈도우 XP 이전 운영 체제에서) 사용자의 실수 혹은 바이러스 이외의 환경요인으로 인해서 NTLDR 파일이 삭제되거나 변형되면 외관상으로는 아무런 문제도 없어 보이지만, 운영 체제를 다시 시작하면 부팅에 실패하게 되고, 'NTLDR is missing, Press Ctrl+Alt+Del to restart' 이라는 메시지가 출력된다.

그러나 저 메시지가 뜬다고 반드시 NTLDR 파일이 삭제되었다고 보기엔 어렵다(파일을 불러오는 중에 알 수 없는 이유로 일시적인 오류를 일으켜 나타나는 메시지일 가능성도 있기 때문이다.) 하지만 출력된 메시지의 방법으로도(재부팅을 해도) 부팅에 실패하고 같은 메시지가 나온다면, 삭제 혹은 변형을 의심할 수 있다. 이러면 윈도우 원본 설치 시디로 복구콘솔을 사용하여 복구하면 된다.

이런 문제로 인해 [윈도우 비스타](../Page/윈도우_비스타.md "wikilink") 이상 운영 체제부터는 새로운 부트 로더를 사용한다.

## boot.ini

NTLDR은 사용자가 어느 운영 체제로 시동할 것인지 메뉴를 띄워 준다. 윈도우 NT 및 NT 기반 운영 체제에서는, 커널에 대해 사용자가 미리 구성한 옵션들을 무시할 수도 있다. 이러한 메뉴 옵션들은 *boot.ini*에 저장되는데, NTLDR과 같은 곳(같은 디스크의 루트)에 위치해 있다.

NT 기반의 운영 체제에서, 운영 체제의 위치는 [고급 RISC 컴퓨팅](https://ko.wikipedia.org/wiki/고급_RISC_컴퓨팅 "wikilink") (ARC) 경로로 쓰여져 있다.

boot.ini는 다음의 [파일 특성을](https://ko.wikipedia.org/wiki/파일_특성 "wikilink") 가지면서 사용자 구성을 보호한다.: 시스템, 숨김, 읽기 전용. 이 파일의 내용을 편집하기 위해서는 다음의 과정을 따르면 된다.

  - 콘솔에서 다음의 명령어를 입력한다: `attrib -s -h -r boot.ini` (-s는 시스템 특성을, -h는 숨김 특성을, -r은 읽기 전용 특성을 없앤다)
  - 폴더 옵션에서 "숨김 파일 및 폴더 보기"에 체크하고 "보호된 운영 체제 파일 숨김"의 체크를 없앤 다음, 루트 디렉터리에 표시되는 boot.ini 파일의 특성을 속성에서 변경한다.
  - 더 보안적인 기능의 편집을 위해서는 콘솔에서 *bootcfg* 명령어를 사용하는 것이다.
  - 시작→실행→msconfig를 사용하여 시스템 구성 유틸리티의 시동 환경을 수정할 수 있다. 이것은 boot.ini가 없는 윈도우 비스타에서도 마찬가지이다.

bootsect.dos는 도스를 불러들이기 위해 NTLDR이 불러들이는 시동 섹터이다. 특정한 파일이 지정되지 않으면, NTLDR은 bootsect.dos를 불러들인다.

### 예

*boot.ini* 파일의 예:

``` ini
[boot loader]
timeout=30
default=multi(0)disk(0)rdisk(0)partition(2)\WINDOWS
[operating systems]
multi(0)disk(0)rdisk(0)partition(2)\WINDOWS="Microsoft Windows XP Professional" /fastdetect
C:\bootsect.dos="Microsoft Windows 98"
```

boot.ini 안의 시동 로더 타임아웃 옵션이 0이면, NTLDR 시동 메뉴는 뜨지 않는다. 다만, 운영 체제가 시동에 실패하고 다시 시동되면, 오류 정보를 보여 주거나 시동 메뉴를 띄울 수 있다.

### NT 커널 스위치

아래의 항목들에 대한 완전한 설명은 \[[http://support.microsoft.com/default.aspx?scid=kb;ko-kr;833721\]에서](http://support.microsoft.com/default.aspx?scid=kb;ko-kr;833721%5D에서) 볼 수 있다.

  - /3gb
  - /basevideo
  - /baudrate=nnn
  - /bootlog
  - /burnmemory
  - /channel
  - /crashdebug
  - /debug
  - /debugport=comx
  - /fastdetect
  - /HAL=파일 이름
  - /kernel=파일 이름
  - /maxmem=숫자
  - /minint
  - /nodebug
  - /noexecute=optin ([DEP](https://ko.wikipedia.org/wiki/데이터_실행_방지 "wikilink"))
  - /noguiboot
  - /nopae ([물리 주소 확장](https://ko.wikipedia.org/wiki/물리_주소_확장 "wikilink") 지원 안 함)
  - /noserialmice:comn (이를테면, /noserialmice:com3)
  - /numproc=CPU의 수
  - /onecpu
  - /pae ([물리 주소 확장](https://ko.wikipedia.org/wiki/물리_주소_확장 "wikilink") 지원)
  - /pcilock
  - /redirect
  - /safeboot ([안전 모드](../Page/안전_모드.md "wikilink") 실행)
      - /safeboot:dsrepair
      - /safeboot:minimal
      - /safeboot:minimal(alternateshell)
      - /safeboot:network
  - /usepmtimer
  - /userva
  - /sos
  - /w95
  - /w95dos
  - /year

## 같이 보기

  - [ntdetect.com](https://ko.wikipedia.org/wiki/ntdetect.com "wikilink")
  - [Ntoskrnl.exe](https://ko.wikipedia.org/wiki/Ntoskrnl.exe "wikilink")
  - [긴급 관리 서비스](https://ko.wikipedia.org/wiki/긴급_관리_서비스 "wikilink") (EMS)
  - [부트 로더](https://ko.wikipedia.org/wiki/부트_로더 "wikilink")

## 각주

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink") [분류:시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:시스템_소프트웨어 "wikilink")

1.