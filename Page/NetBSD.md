> This article is converted from Wikipedia: [NetBSD](https://ko.wikipedia.org/wiki/NetBSD).


**NetBSD**는 [BSD](../Page/BSD.md "wikilink") 계열의 [오픈 소스](../Page/오픈_소스.md "wikilink") [운영 체제이다](../Page/운영_체제.md "wikilink"). 64비트 [옵테론](../Page/옵테론.md "wikilink") [서버](../Page/서버.md "wikilink") 같은 최신 [하드웨어](https://ko.wikipedia.org/wiki/하드웨어 "wikilink") 뿐 아니라 구식 하드웨어, 심지어 [임베디드 시스템에](../Page/임베디드_시스템.md "wikilink") 이르기까지 사용할 수 있을 정도로 폭넓은 [이식성](https://ko.wikipedia.org/wiki/이식성 "wikilink")이 특징이다. NetBSD는 4.3BSD로부터 갈라져 나왔으며, [1995년](../Page/1995년.md "wikilink") 말에 [OpenBSD](../Page/OpenBSD.md "wikilink")가 NetBSD로부터 파생되었다.

NetBSD는 다양한 아키텍처로 이식되어, 같은 소스로부터 54가지 이상의 아키텍처용 바이너리를 만들 수 있다.

자체 패키지 시스템으로 12,000개가 넘는 패키지를 제공하는 [pkgsrc](https://ko.wikipedia.org/wiki/pkgsrc "wikilink")가 있다.

## 역사

NetBSD는 자매프로젝트인 [FreeBSD](../Page/FreeBSD.md "wikilink")와 같이 [캘리포니아 대학교 버클리의](../Page/캘리포니아_대학교_버클리.md "wikilink") 4.3BSD로부터 파생되었으며 Networking/2와 386BSD 릴리즈를 통해 출시되었다.

NetBSD 프로젝트는 운영체제 개발에서 386BSD 내부의 개발자들의 시각 차이로 인한 결과로부터 시작되었다. 프로젝트에는 4명의 주도자 Chris Demetriou, Charles Hannum, Adam Glass, Theo de Raadt가 있었다.

그들은 개발모델이 프로젝트에 더 많은 이익을 가져다 줄 수 있어야 했고, 개방적이어야 한다는 것을 절감하였다. 또한 개발모델은 코드 이식의 용이성과 간결함이 중요시되었다. 4인의 창립자들은 단일화, 다중 플랫폼, 더 좋은 품질의 BSD기반의 운영체제의 제작을 목적으로 했다.

NetBSD 개발은 [인터넷](../Page/인터넷.md "wikilink")에서의 분산-협력이 특성이다. 네트워크의 중요성으로 인해 de Raadt는 이름을 "NetBSD"로 제안했고 다른 창립자들도 그 이름을 받아들였다. NetBSD의 소스코드 저장소는 1993년 3월 21일에 개설되었고 1993년 4월에 제작된 NetBSD 0.8 버전이 처음으로 공식 출시되었다. 이 버전은 386BSD 0.1에서 파생되었으며 비공식 패치인 0.2.2를 덧붙였다. 또한, 386BSD에서 빠진 Net/2 릴리즈의 몇몇 프로그램이 다시 포함되었으며, 여러 가지 다른 개선점도 들어갔다.

1993년 8월 NetBSD 0.9버전이 출시되었다. 여러 가지 개선 사항들과 버그수정이 포함되었다. 비록 다른 아키텍처를 지원하기 위한 노력들이 있었지만 아직까지는 PC 플랫폼만이 지원되었다.

NetBSD 1.0은 1994년 10월에 출시되었다. 이는 NetBSD 최초로 다중 플랫폼을 지원했으며 그것은 다음과 같다.

  - (일반적인) PC
  - HP9000 시리즈 300
  - 아미가
  - 68000 매킨토시
  - Sun-4c 시리즈
  - PC532

이 버전에서는 또한 USL 대 BSDi의 법정 분쟁으로 인해 Net/2기반의 코드를 4.4BSD Lite2 기반의 코드로 대체하였다.

[1994년](../Page/1994년.md "wikilink") 여러 가지 이유로 인해 창립 멤버인 Theo de Raadt가 프로젝트에서 밀려나왔고, [1995년](../Page/1995년.md "wikilink") 말 NetBSD 1.0을 기반으로 OpenBSD 프로젝트를 새롭게 창설하였다.

NetBSD 1.x는 대략 1년 간격으로 출시되었으며 그 사이에 패치들을 공개했다. "pkgsrc" 패키지 모음은 1998년 NetBSD 1.3에서 처음 소개되었으며 1999년까지 NetBSD는 1.4버전이 릴리즈 되었고 16개의 다른 플랫폼을 지원했다.

[2004년](../Page/2004년.md "wikilink") [12월](../Page/12월.md "wikilink") NetBSD는 2.0을 릴리즈 했다. 메이저 버전의 변동 사항으로는 모든 플랫폼에서의 Scheduler Activations model을 기반으로 한) Native Thread의 구현 도입이 눈에 띈다. 또한 몇몇 다른 CPU 아키텍처에서 SMP를 지원한다. 그리고 NetBSD 2.0 바이너리 릴리즈에서는 단지 6개의 소스코드 형식을 가지고 48개의 플랫폼을 지원했다.

2.0 릴리즈 이후로부터는 메이저 버전 번호가 증가하고 있다. 또한 그와 같이 빠르게 발전하고 있다. 이전의 마이너 릴리즈 번호는 이젠 안정버전의 유지와 보안에 민감한 버그들을 고친 릴리즈로 분화되었다.

현재 NetBSD 릴리즈 버전은 [2019년](../Page/2019년.md "wikilink") [3월 31일에](../Page/3월_31일.md "wikilink") 발표한 NetBSD 8.1이다.

## 이식성

NetBSD의 모토는 "Of course, it runs NetBSD."이다. 이 말은, 어떤 플랫폼이든지 실행할 수 있다는 것으로 해석할 수 있다. NetBSD는 다수의 32비트 혹은 64비트 아키텍처에 포팅되었다. (VAX 미니컴퓨터로부터 PocketPC PDA에 이르기까지) 현재 지원되는 54종 이상의 하드웨어 플랫폼의 커널과 사용자 영역은 CVS가 관리하는 중앙집중화된 소스 트리에서 빌드된다.

중앙집중식 소스코드 관리로 인해 이식성 높은 설계가 가능하고 이는 플랫폼에 즉각적으로 반영된다. 장치 드라이버의 개발 역시 플랫폼 독립적으로 이루어진다. 예를 들어, PCI 카드 드라이버는 어떤 플랫폼의 PCI 슬롯에 장착이 되어있건 간에 동작할 것이다. 대부분 NetBSD 장치 드라이버는 특정 버스 코드를 제거해 버스 중립성을 가지고 있고, 각기 다른 버스로 운영되는 장치에 (PCI이건 ISA이건 PCMCIA이건) 단 하나의 드라이버만 있으면 된다. 이러한 플랫폼 독립성은 임베디드 시스템 개발 (특히 NetBSD 1.6으로 시작할 경우)에서 매우 유용할 것이다. 이는 (크로스) 컴파일러, 어셈블러, 링커가 뒷받침해 준다.

NetBSD의 이식성은 단일한 모듈 이식성 계층(Modular Portability Layer, 이하 MPL)에서 나온다. 장치 드라이버는 MPL을 사용하며, MPL은 다음 문제를 드라이버 아래에서 해결한다.

  - 하드웨어 플랫폼
  - 입출력 인스트럭션 여부
  - Interlocking
  - 재시도 오류 복구
  - Bounce buffers
  - 메모리 타입 경계
  - Scatter/Gather maps in host bridges
  - 의사 DMA 사용 여부

NetBSD를 사용하는 일부 임베디드 시스템은 툴체인을 타겟 플랫폼에 재호스트 할 필요가 없다. 그래서, NetBSD를 사용하는 토스터 프로젝트가 탄생할 수 있었다.([사진](http://www.flickr.com/photos/laughingsquid/sets/738459/))

## 라이선스

NetBSD 커널과 사용자영역의 핵심 소스코드들 대다수가 [BSD 허가서로](../Page/BSD_허가서.md "wikilink") 릴리즈되고 있다. 이 외에도 [GPL과](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 기타 오픈소스 라이선스로 배포되는 패키지가 있다.

## 다른 운영체제와의 호환성

NetBSD의 소스 코드는 전체적으로 [POSIX](../Page/POSIX.md "wikilink").1 ([IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") 1003.1 \~ 1990) 표준과 유사하다. 다른 POSIX 계열 운영체제 형식 실행 파일을 자유롭게 실행할 수 있다.

NetBSD는 아래와 같은 다양한 파일시스템을 지원한다.

  - [FAT](../Page/파일_할당_테이블.md "wikilink") (FAT, VFAT와 FAT32를 포함해서)
  - NTFS
  - Ext2 (리눅스)
  - HFS,UFS ([맥 OS X](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink"))
  - RISC OS FileCore/ADFS
  - AmigaOS Fast File System (FFS)

## "pkgsrc" 패키지 모음

NetBSD는 응용 프로그램 패키지를 [pkgsrc](https://ko.wikipedia.org/wiki/pkgsrc "wikilink")로 관리하며 2013년 11월 현재 대략 12,000개가 넘는 패키지가 있다. 이 시스템은 소스를 가져와서 컴파일을 쉽게 하도록 도와 주며, 바이너리 패키지도 존재한다. 다른 패키지 시스템처럼 의존성 문제를 해결할 수 있다. pkgsrc의 특징 상, Autoconf를 사용할 수 있는 다른 시스템으로도 이식할 수 있다. 또한 이 시스템은 [DragonFly BSD의](../Page/DragonFly_BSD.md "wikilink") 공식 패키지 시스템이기도 하다.

## 로고

NetBSD의 "깃발" 로고는 Grant Bisset이 디자인했으며 2004년 처음 소개되었다. 1994년 Shawn Mueller가 디자인한 예전의 로고를 추상화한 것이다.

## 호스팅

NetBSD 프로젝트는 Internet System Consortium Inc.과 헬싱키 공과 대학교, [컬럼비아 대학교에서](../Page/컬럼비아_대학교.md "wikilink") 호스팅하고 있다. 전 세계 프로젝트 참가자들이 미러 또한 제공한다.

## 외부 링크

  - [NetBSD 프로젝트](https://web.archive.org/web/20051111143335/http://www.netbsd.org/ko/)
  - [NetBSD 패키지 컬렉션](http://www.pkgsrc.org/) (pkgsrc)
  - [Jibbed](https://web.archive.org/web/20190118013435/http://www.jibbed.org/) LiveCD
  - [NetBSD Wiki](https://web.archive.org/web/20080723193832/http://wiki.netbsd.se/)

[분류:BSD](https://ko.wikipedia.org/wiki/분류:BSD "wikilink") [분류:ARM 운영 체제](https://ko.wikipedia.org/wiki/분류:ARM_운영_체제 "wikilink") [분류:파워PC 운영 체제](https://ko.wikipedia.org/wiki/분류:파워PC_운영_체제 "wikilink") [분류:자유 소프트웨어 운영 체제](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_운영_체제 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")