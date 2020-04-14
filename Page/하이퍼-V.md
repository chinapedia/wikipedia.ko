> This article is converted from Wikipedia: [하이퍼-V](https://ko.wikipedia.org/wiki/하이퍼-V).


마이크로소프트 **하이퍼 V**(Hyper-V, 코드이름 Viridian\[1\])는 [x64](https://ko.wikipedia.org/wiki/x64 "wikilink") 시스템을 위한 [하이퍼바이저](../Page/하이퍼바이저.md "wikilink") 기반의 [가상화](../Page/가상화.md "wikilink") 시스템이다.\[2\] **윈도우 서버 가상화**(Windows Server Virtualization)라는 이름으로도 알려져 있다. 하이퍼 V 베타 버전은 [윈도우 서버 2008](../Page/윈도우_서버_2008.md "wikilink") x64 에디션에도 추가되어 있으며 마지막 버전은(윈도우 업데이트를 통해 자동으로 업데이트됨) [2008년](../Page/2008년.md "wikilink") [6월 26일에](../Page/6월_26일.md "wikilink") 공개되었다.

"마이크로소프트 하이퍼-V 서버 2008"이라 불리는 독립형 하이퍼 V 버전은 하이퍼 V 기능을 완전히 다룰 수 있는 [윈도우 서버 2008](../Page/윈도우_서버_2008.md "wikilink") "코어"의 변종으로 [2008년](../Page/2008년.md "wikilink") [10월 1일에](../Page/10월_1일.md "wikilink") 공개되었다. 다른 윈도우 서버 규칙은 비활성화되어 있으며 제한된 윈도우 서비스가 제공된다.\[3\] 그 뒤 [윈도우 서버 2012에서](../Page/윈도우_서버_2012.md "wikilink") 한 번 더 업데이트되었다.\[4\]

## 버전

하이퍼-V에는 명확히 구별되는 두 가지 버전이 있다.

  - 마이크로소프트 하이퍼-V 서버 2012 (현재 판의 하이퍼 V가 포함되어 있음) 및 마이크로소프트 하이퍼-V 서버 2008 R2 (독립형 제품)
  - [윈도우 서버 2012](../Page/윈도우_서버_2012.md "wikilink"), [마이크로소프트 윈도우 서버 2008 R2](../Page/윈도우_서버_2008_R2.md "wikilink"), [윈도우 서버 2008의](../Page/윈도우_서버_2008.md "wikilink") 일부

### 하이퍼-V 서버

하이퍼-V 서버(Hyper-V Server)는 2008년 10월 1일에 공개되었다. [윈도우 서버 2008](../Page/윈도우_서버_2008.md "wikilink") "코어"의 변형이며 완전한 하이퍼-V 기능이 포함되어 있다. 다른 윈도우 2008 서버 롤(Role)은 사용하지 못하지만 제한된 윈도우 서비스를 사용할 수 있다.\[5\] 무료로 나온 64비트 하이퍼-V "코어" 버전은 명령 줄 인터페이스 (CLI)에 제한을 받는데 여기서 호스트나 부모 (하이퍼-V 코어 서버) 운영 체제, 물리 하드웨어 및 소프트웨어를 셸 명령을 사용하여 구성할 수 있다. 새로운 메뉴로 동작하는 CLI 인터페이스는 초기 구성을 상당히 단순화시켰으며 일부 무료로 내려받을 수 있는 스크립트 파일은 이 개념을 확장하고 있다. 호스트 (하이퍼-V 코어 서버 운영 체제)와 게스트 또는 가상 운영체제의 관리와 구성은 일반적으로 확장 관리 콘솔을 내려 받은 뒤 윈도우 비스타 PC나 윈도우 2008 서버(32 / 64비트)에 설치하여 사용할 수 있다. 다른 윈도우 2008 서버의 경우 하이퍼 V "롤"을 설치하여 관리 콘솔을 리다이렉트하여 사용할 수 있다. 윈도우 하이퍼-V 코어 서버의 또다른 관리 및 구성은 원격 윈도우 데스크톱 RDP 세션을 사용(여전히 CLI를 이용)하거나 비스타 PC나 완전한 버전의 윈도우 2008 서버에 있는 컴퓨터 관리, 그룹 정책 (로컬)과 같은 리다이렉트된 표준 관리 콘솔(MMC)를 사용하여 이용할 수 있다. 이로써 가리켜 클릭하는 구성과 하이퍼-V 코어 서버의 감시가 더 용이하게 되었다. 하이퍼-V 코어 서버 릴리즈 2 (R2)는 2009년 9월부터 사용할 수 있으며 이는 [윈도우 파워셸](https://ko.wikipedia.org/wiki/윈도우_파워셸 "wikilink") v2 및 업데이트된 윈도우 2008 코드 기반의 주된 기능이다.

## 시스템 요구 사양

1.  윈도우 서버 2008 스탠다드, 윈도우 서버 2008 엔터프라이즈, 윈도우 서버 2008 데이터센터의 x64 버전을 실행하고 있는 x64 기반의 프로세서
2.  [하드웨어 보조 가상화](https://ko.wikipedia.org/wiki/x86_가상화 "wikilink"). 이 기능은 가상화 옵션을 포함하고 있는 프로세서에서 사용할 수 있다. 이를테면 인텔 VT나 AMD 가상화 (AMD-V)를 말한다.
3.  [NX 비트](../Page/NX_비트.md "wikilink") 호환 CPU를 사용할 수 있어야 하며 하드웨어 [데이터 실행 방지](../Page/데이터_실행_방지.md "wikilink") (DEP)도 켜져 있어야 한다.
4.  최소 2 GB의 메모리. (각 가상 운영 체제는 저만의 메모리를 요구하므로 현실적으로 더 많은 메모리가 필요하다.)
5.  윈도우 2008 스탠다드 (64 비트) 하이퍼 V 코어는 거의 3 GB의 디스크 공간을 요구한다 (설치 용량)
6.  윈도우 2008 스탠다드 (64 비트) 하이퍼 V 완전 GUI 제품은 거의 8 GB 의 디스크 공간을 요구한다 (설치 용량)
7.  윈도우 2008 스탠다드 (64 비트) 하이퍼 V 완전 GUI 또는 코어는 최대 31 GB의 메모리를 VM 실행을 위해 지원하며 하이퍼 V 부모 운영 체제에서는 1 GB를 지원한다.\[6\]
8.  윈도우 2008 스탠다드 (64 비트) 하이퍼 V 완전 GUI 또는 코어는 최대 1, 2, 4개의 코어를 갖춘 최대 4개의 프로세서를 지원한다
9.  윈도우 2008 스탠다드 (64 비트) 하이퍼 V 완전 GUI 또는 코어 최대 128개의 "게스트 운영 체제"를 지원한다\[7\]
10. 윈도우 2008 스탠다드 (64 비트) 하이퍼 V 완전 GUI 또는 코어는 32비트 (x86) 및 64비트 (x64) 게스트 VM을 지원한다

독립형 하이퍼 V 서버는 윈도우 서버 2008의 기존 설치본을 요구하지 않으며 최소 1Gb의 메모리와 2Gb의 여유 디스크 공간을 요구한다.

## 지원 게스트 운영 체제

지원되는 게스트 운영체제는 다음을 포함한다:\[8\]

  - [윈도우 10](../Page/윈도우_10.md "wikilink")
  - [윈도우 8](../Page/윈도우_8.md "wikilink")
  - [윈도우 서버 2008](../Page/윈도우_서버_2008.md "wikilink") x86/x64
  - [윈도우 HPC 서버 2008](../Page/윈도우_HPC_서버_2008.md "wikilink")
  - [윈도우 서버 2003](../Page/윈도우_서버_2003.md "wikilink")
  - [윈도우 2000](../Page/윈도우_2000.md "wikilink") 서버 SP4 및 어드밴스드 서버 SP4\[9\]
  - [윈도우 비스타](../Page/윈도우_비스타.md "wikilink") SP1 (홈 에디션 제외)
  - [윈도우 XP](../Page/윈도우_XP.md "wikilink") 프로페셔널 SP2/SP3/x64
  - [수세 리눅스 엔터프라이즈 서버](https://ko.wikipedia.org/wiki/수세_리눅스_엔터프라이즈_서버 "wikilink") 10 SP1/SP2

### 리눅스 지원

하이퍼-V는 리눅스 게스트 운영 체제에 대한 기본적인 가상화 지원을 제공한다. 그러나 반가상화 지원은 [리눅스 통합 구성 요소](http://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=ab7f4983-93c5-4a70-8c79-0642f0d59ec2)와 [Satori InputVSC](https://web.archive.org/web/20100402083924/http://www.xen.org/download/satori.html) 드라이버를 설치함으로써 사용할 수 있다. 2009년 7월 20일에 마이크로소프트는 리눅스 커널에 들어간 이 세 개의 드라이버들을 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")로 공개하여\[10\] 2.6.32 이상의 커널은 자체적으로 하이퍼 V 반가상화 지원을 포함하고 있다. 또한 마이크로소프트에서 Linux Integration Service Version 이라는 이름으로 Redhat 계열의 리눅스를 위한 드라이버를 제공하고 있으며 해당 프로그램을 다운로드 하여 설치할수 있다.

## 구조

[450px](https://ko.wikipedia.org/wiki/파일:Hyper-V.png "wikilink")

{{-}}

## 각주

## 서적

  - Morimoto, Rand; Jeff Guillet. Windows Server 2008 Hyper-V Unleashed. .

## 외부 링크

  -
  - [하이퍼 V 구조](http://www.serhatakinci.com/?p=1559)

  - [하이퍼 V 기능 규격](http://www.microsoft.com/downloads/details.aspx?FamilyID=91e2e518-c62c-4ff2-8e50-3a37ea4100f5&displaylang=en)

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink") [분류:가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:가상화_소프트웨어 "wikilink") [분류:윈도우 서버 2008](https://ko.wikipedia.org/wiki/분류:윈도우_서버_2008 "wikilink")

1.  [Microsoft to ship Windows Server 2008, over time, in eight flavors | ZDNet](http://blogs.zdnet.com/microsoft/?p=935)
2.
3.  [Microsoft Helps Customers Overcome Barriers to Virtualization and Get Virtual Now: Microsoft Hyper-V Server 2008 released; company announces new services and training offering...](http://www.microsoft.com/presspass/press/2008/oct08/10-01HyperVRTM08PR.mspx)
4.
5.
6.  [Memory Limits for Windows Releases (Windows)](http://msdn.microsoft.com/en-us/library/aa366778.aspx#physical_memory_limits_윈도우_server_2008)
7.  [Microsoft Hyper-V Server: Overview](http://www.microsoft.com/servers/hyper-v-server/overview.mspx)
8.  [Supported Guest OS on Windows Server 2008 Hyper-V](http://www.microsoft.com/windowsserver2008/en/us/hyperv-supported-guest-os.aspx)
9.
10. [Microsoft Contributes Linux Drivers to Linux Community: Roundtable Q\&A: Sam Ramji, senior director of Platform Strategy at Microsoft, and Tom Hanrahan, director of Microsoft’s...](http://www.microsoft.com/presspass/features/2009/Jul09/07-20LinuxQA.mspx)