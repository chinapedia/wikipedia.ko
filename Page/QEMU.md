> This article is converted from Wikipedia: [QEMU](https://ko.wikipedia.org/wiki/QEMU).


**QEMU**는 [가상화](../Page/가상화.md "wikilink") 소프트웨어 가운데 하나다. Fabrice Bellard가 만들었으며 x86 이외의 기종을 위해 만들어진 소프트웨어 스택 전체를 가상머신 위에서 실행할 수 있다는 특징이 있다. [동적 변환기](https://ko.wikipedia.org/wiki/동적_변환기 "wikilink")(Portable dynamic translation)를 사용한다.

## 허가서

[여기](https://web.archive.org/web/20081120004436/http://bellard.org/qemu/license.html) 를 볼 것.

  - 소프트웨어 자체, 가속기: [GNU 일반 공중 사용 허가서](../Page/GNU_일반_공중_사용_허가서.md "wikilink")
  - 가상 CPU 중심부 라이브러리: [GNU 약소 일반 공중 사용 허가서](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink")
  - 하드웨어 장치 모듈: [BSD 허가서](../Page/BSD_허가서.md "wikilink")

[마이크로소프트 윈도에서](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 실행할 때는 독점 라이브러리인 [FMOD](../Page/FMOD.md "wikilink")를 쓰기도 한다.

## 지원 모드

QEMU는 두 가지 운영 모드가 있다:

  - 사용자 모드 에뮬레이션
    이 모드에서 QEMU는 다른 명령어 집합으로 컴파일된 단일 [리눅스](../Page/리눅스.md "wikilink"), [다윈](../Page/다윈_\(운영_체제\).md "wikilink")/[맥 오에스 X](https://ko.wikipedia.org/wiki/맥_오에스_X "wikilink") 프로세스를 실행할 수 있다. 시스템 콜은 엔디언과 32/64비트 미일치를 위해 주소 변환 된다. [와인과](../Page/와인_\(소프트웨어\).md "wikilink") [DOSEMU](../Page/DOSEMU.md "wikilink")는 QEMU의 주요 대상이다.
  - 완전한 컴퓨터 시스템 모드 에뮬레이션
    QEMU 는 프로세서와 가상 주변 기기들을 포함한 완전한 컴퓨터 시스템을 에뮬레이트한다. 한 컴퓨터에 여러 개의 가상 컴퓨터의 가상 호스팅을 제공하는 데 쓸 수 있다. QEMU는 리눅스 윈도, 도스, BSD와 같은 많은 게스트 운영 체제들을 시동할 수 있다. 여러 개의 x86, amd64, alpha, mips, 그리고 sparc과 같은 하드웨어 플랫폼들의 에뮬레이션을 지원한다.

프로그램의 대부분은 [LGPL](https://ko.wikipedia.org/wiki/LGPL "wikilink")을 따른다. - 사용자 모드 에뮬레이션은 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")을 따른다. (윈도 포트가 [FMOD](../Page/FMOD.md "wikilink") 사운드 계층을 사용하지만)\[1\].

## 기능

  - [IA-32](../Page/IA-32.md "wikilink") (x86) PC, [AMD64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") PC, [MIPS](https://ko.wikipedia.org/wiki/MIPS_테크놀로지스 "wikilink") R4000, 선 [SPARC](../Page/SPARC.md "wikilink") sun4m, 선 [SPARC](../Page/SPARC.md "wikilink") sun4u, [ARM](../Page/ARM_아키텍처.md "wikilink") 개발 보드 (Integrator/CP, Versatile/PB), SH4 SHIX 보드, [파워피씨](https://ko.wikipedia.org/wiki/파워피씨 "wikilink") ([PReP](https://ko.wikipedia.org/wiki/PReP "wikilink") 및 [파워 매킨토시](https://ko.wikipedia.org/wiki/파워_매킨토시 "wikilink")), [ETRAX CRIS](https://ko.wikipedia.org/wiki/ETRAX_CRIS "wikilink") 아키텍처의 에뮬레이션 지원.
  - 호스트 시스템과 에뮬레이트 시스템 두 곳에서 다른 아키텍처 지원 (자세한 것은 홈페이지를 참조하라).
  - 속도 개선: 어떠한 응용 프로그램은 실시간에 가깝게 실행할 수 있다.
  - Copy-On-Write 디스크 이미지 포맷 추가. 수 기가바이트의 가상 드라이브를 선언할 수 있으며, 이 드라이브의 디스크 이미지는 실제로 사용되는 만큼만 용량을 차지할 것이다.
  - 오버레이 이미지 추가. 게스트 운영 체제의 스냅샷을 유지하고 별도의 이미지 파일에 변경 사항을 기록할 수 있다. 게스트 운영 체제에 문제가 생기면 해당 스냅샷으로 되돌릴 수 있다.
  - 다른 아키텍처에서 돌아가는 리눅스 바이너리 파일 실행 지원.
  - 컴퓨터의 상태를 저장하고 저장한 상태로 되돌아갈 수 있다.
  - 가상 네트워크 카드 에뮬레이션.
  - SMP 지원.
  - 게스트 운영 체제는 패치나 수정이 필요 없다.
  - 0.11.x 판까지는 KQEMU 커널 모듈이 쓰일 때 성능이 개선되나, 그 이후 판에서는 사용할 수 없다.
  - 명령 줄 도구는 X11을 돌리지 않고도 QEMU를 완전하게 제어할 수 있게 도와 준다.
  - 가상으로 구현된 컴퓨터를 통합 VNC 서버를 거쳐 원격으로 제어한다.
  - USB 태블릿 지원: "-usb -usbdevice tablet"로 활성화하여 사용할 수 있다.
  - 관리자 권한은 따로 필요하지 않다.

## 가상 구현 시스템

QEMU는 [CPU를](../Page/중앙_처리_장치.md "wikilink") 제외하고 다음의 시스템을 가상으로 구현한다.

  - i440FX 호스트 PCI 브리지, PIIX3 PCI to ISA 브리지
  - 시러스 CLGD 5446 PCI VGA 카드 또는 Bochs VESA 확장을 지원하는 더미 VGA 카드 (비표준 모드를 포함하는 하드웨어 수준).
  - PS/2 마우스 및 키보드
  - 하드 디스크와 CD-ROM을 지원하는 2 개의 PCI IDE 인터페이스
  - 플로피 디스크
  - NE2000 PCI 네트워크 어댑터
  - 직렬 포트
  - 애드립(OPL2) - 야마하 YM3812 호환 칩
  - 크리에이티브 사운드 블라스터 16 사운드 카드
  - 엔소닉 오디오PCI ES1370 사운드 카드
  - 그라비스 울트라사운드
  - 인텔 HD 오디오\[2\]
  - PCI UHCI USB 컨트롤러 및 가상 USB 허브.

## 가속기

### KQEMU

페브리스 벨러드(Fabrice Bellard)는 KQEMU (QEMU 가속기)라는 이름으로 [리눅스 커널](../Page/리눅스_커널.md "wikilink") [모듈을](https://ko.wikipedia.org/wiki/로더블_커널_모듈 "wikilink") 작성하였다. i386 플랫폼에서 i386 에뮬레이션 속도를 눈에 띄게 개선해 준다. [사용자 모드](../Page/사용자_공간.md "wikilink") 코드를 호스트 컴퓨터의 CPU에서 바로 실행하고 [커널 모드와](../Page/보호_링.md "wikilink") [리얼 모드](../Page/리얼_모드.md "wikilink") 코드에만 주변 기기와 프로세서의 에뮬레이션을 사용함으로써 속도 개선을 달성할 수 있다. KQEMU는 또 호스트 CPU에서 커널 모드 코드의 일부를 실행하는 커널 에뮬레이션 모드를 지원한다. QEMU의 가속기 모듈인 KQEMU는 원래 무료로 배포되긴 했지만, [클로즈드 소스](https://ko.wikipedia.org/wiki/클로즈드_소스 "wikilink") 제품으로 공개되었다. 그러다가 [2007년](../Page/2007년.md "wikilink") [2월 5일에](../Page/2월_5일.md "wikilink") 버전 1.3.0pre10이 공개되면서\[3\] GNU 일반 공중 라이선스를 통해 소스가 공개되었다. KQEMU는 Win4Lin Pro Desktop 제품을 통해 [Win4Lin](https://ko.wikipedia.org/wiki/Win4Lin "wikilink")으로 라이선스되어 왔다. KVM과 달리, KQEMU는 호스트 CPU가 하드웨어 가상화를 지원하지 않더라도 수많은 게스트 운영 체제의 코드를 실행할 수 있고, 나중에 하드웨어 확장 지원이 예정되어 있었지만\[4\], 0.12.0 판 이후 QEMU에서 기본으로 확장 메모리를 지원(large memory supported)하면서 KQEMU 지원을 중단하였다.

### QVM86

QVM86은 QEMU [에뮬레이터](../Page/에뮬레이터.md "wikilink")에 [x86 가상화](https://ko.wikipedia.org/wiki/x86_가상화 "wikilink") 기능을 제공하는 [리눅스 커널](../Page/리눅스_커널.md "wikilink") 모듈이었다. 가상화는 CPU 보호 계획을 사용하여 권한 이벤트를 가로채거나 가상으로 구현하여 에뮬레이션 코드가 호스트 [CPU에](../Page/중앙_처리_장치.md "wikilink") 네이티브로 실행할 수 있게 도와 준다. GNU [GPLv2](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 라이선스로 공개되었다. 원래 GPL 라이선스의 클로즈드 소스 [KQEMU](https://ko.wikipedia.org/wiki/KQEMU "wikilink")의 대안으로 개발되었다. QVM86의 개발자는 [버추얼박스](../Page/버추얼박스.md "wikilink")의 공개로 인해 [2007년](../Page/2007년.md "wikilink") [1월 21일에](../Page/1월_21일.md "wikilink") 개발을 중단하였다.

## 최신 버전

위치는 공식 저장소, 기종은 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink"), 버전은 최신 안정 버전 기준입니다.

  - 공식 저장소: **0.11.0-rc1**(2009년 7월 30일 출시)
  - [데비안](../Page/데비안.md "wikilink"): **0.9.1-10lenny1**
  - [우분투](../Page/우분투_\(운영_체제\).md "wikilink")(통상): **0.10.0-1ubuntu1**
  - 우분투(장기 지원 - dapper): **0.8.0-3ubuntu1**
  - 우분투(장기 지원 - hardy): **0.9.1-1ubuntu1**
  - [페도라](https://ko.wikipedia.org/wiki/페도라 "wikilink"): **0.10.6**
  - [오픈수세](../Page/오픈수세.md "wikilink"): **0.10.1**
  - [아치](../Page/아치_리눅스.md "wikilink"): **0.10.6-1**
  - [젠투](../Page/젠투_리눅스.md "wikilink"): **0.11.1**

## 함께 보기

  - [가상 머신](../Page/가상_머신.md "wikilink")
  - [FreeOsZoo](https://ko.wikipedia.org/wiki/FreeOsZoo "wikilink")
  - [OpenBIOS](https://ko.wikipedia.org/wiki/OpenBIOS "wikilink")
  - QEMU 포트와 프론트엔드
      - [Q](https://ko.wikipedia.org/wiki/Q_\(emulator\) "wikilink")
      - [QVM86](https://ko.wikipedia.org/wiki/QVM86 "wikilink")
      - [Win4Lin](https://ko.wikipedia.org/wiki/Win4Lin "wikilink")
      - [다윈](../Page/다윈_\(운영_체제\).md "wikilink")
  - 다른 가상 머신
      - [Bochs](../Page/Bochs.md "wikilink")
      - [Cooperative Linux](https://ko.wikipedia.org/wiki/Cooperative_Linux "wikilink")
      - [KVM](../Page/커널_기반_가상_머신.md "wikilink")
      - [Microsoft Virtual PC](https://ko.wikipedia.org/wiki/Microsoft_Virtual_PC "wikilink")
      - [Parallels Workstation](https://ko.wikipedia.org/wiki/Parallels_Workstation "wikilink")
      - [Simics](https://ko.wikipedia.org/wiki/Simics "wikilink")
      - [User-mode Linux](https://ko.wikipedia.org/wiki/User-mode_Linux "wikilink")
      - [VirtualBox](https://ko.wikipedia.org/wiki/VirtualBox "wikilink")
      - [VMware](https://ko.wikipedia.org/wiki/VMware "wikilink")

## 각주

## 외부 링크

  - [QEMU 홈페이지](http://www.qemu.org/)
  - [QEMU 포럼](https://web.archive.org/web/20071014010053/http://qemu-forum.ipi.fi/)
  - [윈도에서의 QEMU](https://web.archive.org/web/20060925091601/http://www.h7.dion.ne.jp/~qemu-win/)
  - [우분투에서의 QEMU](https://wiki.ubuntu.com//WindowsXPUnderQemuHowTo)
  - [오픈솔라리스를 위한 QEMU](https://web.archive.org/web/20071029111817/http://www.opensolaris.org/os/project/qemu/)
  - [젠투에서의 QEMU](https://web.archive.org/web/20071027125550/http://gentoo-wiki.com/HOWTO:_Qemu)
  - [QVM86 프로젝트 페이지](http://savannah.nongnu.org/projects/qvm86/)
  - [QEMU 포럼에서의 QVM86](https://web.archive.org/web/20070930193315/http://qemu-forum.ipi.fi/viewforum.php?f=18)

[분류:가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:가상화_소프트웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:안드로이드 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:안드로이드_에뮬레이션_소프트웨어 "wikilink") [분류:리눅스 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_에뮬레이션_소프트웨어 "wikilink") [분류:윈도우 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_에뮬레이션_소프트웨어 "wikilink") [분류:X86 에뮬레이터](https://ko.wikipedia.org/wiki/분류:X86_에뮬레이터 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_에뮬레이션_소프트웨어 "wikilink") [분류:자유 가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_가상화_소프트웨어 "wikilink")

1.  [FMOD music & sound effects system](http://www.fmod.org/)
2.
3.  [KQEMU 1.3.0pre10 released - under the GPL \[LWN.net](http://lwn.net/Articles/220807/) \]
4.  ~~<https://web.archive.org/web/20070206215404/http://fabrice.bellard.free.fr/qemu/kqemu-tech.html#SEC1>~~