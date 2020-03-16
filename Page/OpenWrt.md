> This article is converted from Wikipedia: [OpenWrt](https://ko.wikipedia.org/wiki/OpenWrt).


**OpenWrt**(오픈더블유알티)는 [무선랜](../Page/무선랜.md "wikilink") [라우터](../Page/라우터.md "wikilink")를 위한 비실시간(Non-Real-Time) [리눅스](../Page/리눅스.md "wikilink") 기반의 [오픈 소스](../Page/오픈_소스.md "wikilink") [운영 체제이다](../Page/운영_체제.md "wikilink"). 원래는 Linksys사의 가정용 무선랜 라우터 모델인 WRT54G 시리즈의 성능을 강화하기 위한 커스텀 운영 체제로서 개발이 시작되었다가, 이후 점차 다른 무선랜 라우터들을 지원하기 시작하여 지금은 대부분의 라우터 플랫폼을 지원하고 있다. 무선랜 라우터 기능을 지원하는 임베디드 보드들은 대개 제한된 처리 능력과 메모리를 가지기 때문에 일반 PC에서와 같이 리눅스의 모든 기능을 구현하는 것이 불가능하며 라우터로서 반드시 필요한 기능들만 선택적으로 설치되어야 한다. OpenWrt는 무선랜 라우터에 필요한 리눅스의 기능들을 패키지 형태로 제공함으로써 사용자들에게 편의를 제공한다. 초기에 OpenWrt는 배포 버전인 와이트 러시안(White Russian)과 개발 버전인 카미카제(Kamikaze)로 따로 관리되다가 2007년 2월에 카미카제로 통합되었다.

## 특징

OpenWrt는 일반 [게이트웨이](../Page/게이트웨이.md "wikilink") 장비에 내장된 펌웨어가 제공하는 여러 기능들, 예를 들어 [DHCP](https://ko.wikipedia.org/wiki/DHCP "wikilink") 서비스나 [WEP](https://ko.wikipedia.org/wiki/WEP "wikilink"), [WPA](https://ko.wikipedia.org/wiki/WPA "wikilink"), [WPA2](https://ko.wikipedia.org/wiki/WPA2 "wikilink") 같은 무선 보안 기능들을 기본적으로 제공한다. 또한 이런 기본적인 기능 이외에 기본 펌웨어에서 제공하지 않는 다음과 같은 여러가지 기능들을 추가로 제공한다.

  - [NAT](https://ko.wikipedia.org/wiki/NAT "wikilink") 뒤에 있는 컴퓨터로 들어오는 외부 트래픽에 대한 [포트포워딩](https://ko.wikipedia.org/wiki/포트포워딩 "wikilink") 기능.
  - 동적 포트포워딩을 위한 [UPnP](https://ko.wikipedia.org/wiki/UPnP "wikilink") 기능.
  - 정적인 [DHCP](https://ko.wikipedia.org/wiki/DHCP "wikilink") 할당.
  - 강력한 [방화벽](https://ko.wikipedia.org/wiki/방화벽 "wikilink")과 [라우터](../Page/라우터.md "wikilink") 설정.
  - [VoIP](https://ko.wikipedia.org/wiki/VoIP "wikilink"), 온라인 게임, 멀티미디어 스트리밍 서비스를 위한 [QoS](../Page/QoS.md "wikilink") 설정.
  - [무선 리피터](https://ko.wikipedia.org/wiki/무선_리피터 "wikilink"), [AP](https://ko.wikipedia.org/wiki/AP "wikilink"), [무선 브릿지등으로](https://ko.wikipedia.org/wiki/무선_브릿지 "wikilink") 다양하게 장비를 설정할 수 있음. 이들 설정을 조합하여 사용하는 것도 가능하게 해줌.
  - [메시 네트워킹](https://ko.wikipedia.org/wiki/메시_네트워킹 "wikilink")
  - 고정 IP를 제공하지 않는 [ISP](../Page/인터넷_서비스_제공자.md "wikilink") 사용자를 위한 [다이나믹 DNS](https://ko.wikipedia.org/wiki/다이나믹_DNS "wikilink") 기능.
  - [SSH나](../Page/시큐어_셸.md "wikilink") [telnet을](../Page/텔넷.md "wikilink") 통한 명령 줄 접근
  - USB 포트를 지원하는 장치의 경우 프린터 공유나 윈도 호환 파일 공유 ([SAMBA](https://ko.wikipedia.org/wiki/SAMBA "wikilink")), USB 오디오 등 연결 가능한 여러 장치 지원.
  - 실시간 네트워크 감시
  - 강력한 [AJAX](https://ko.wikipedia.org/wiki/AJAX "wikilink") 웹 인터페이스.
  - 가장 중요한 것으로, 규칙적인 버그 수정과 업데이트. 제조사가 더이상 지원하지 않는 장비도 지원.

OpenWrt의 또 한가지 훌륭한 장점은 파일 시스템을 자유롭게 사용하는 것이 가능하다는 것이다. ipkg (최신 버전에서는 opkg) 라는 패키지 관리 시스템을 사용해서 사용자가 자유롭게 여러가지 소프트웨어를 설치해서 OpenWrt를 매우 다양한 방식으로 사용할 수 있다. 다른 리눅스 기반 펌웨어들은 대체로 읽기만 가능한 [SquashFS](https://ko.wikipedia.org/wiki/SquashFS "wikilink") 같은 파일 시스템을 사용하기 때문에 사용자가 새로운 소프트웨어를 추가하고 싶은 경우 펌웨어 이미지 전체를 새로 빌드하고 플래시에 올려서 사용해야 한다. 이것이 다른 리눅스 기반 펌웨어와 비교해서 OpenWrt가 갖는 가장 큰 장점이다. OpenWrt는 배포 정책에 따라 읽기만 가능한 [SquashFS](https://ko.wikipedia.org/wiki/SquashFS "wikilink")이나 읽고 쓰기가 모두 가능한 [JFFS2](../Page/JFFS2.md "wikilink") 중 알맞은 것으로 이미지를 만들 수 있다.

### 웹 인터페이스

8.09 이전 버전의 OpenWrt에서는 간단한 웹 인터페이스만 제공했다. 8.09 이후 버전의 경우 매우 훌륭한 웹 인터페이스가 기본 설치되어있다. 이 인터페이스는 [Lua](https://ko.wikipedia.org/wiki/Lua "wikilink") 언어로 작성된 [MVC](https://ko.wikipedia.org/wiki/MVC "wikilink") 프레임워크인 LuCi 프로젝트를 기반으로 만들어진 것이다.

## 파생 프로젝트

OpenWrt 프로젝트를 기반으로 하여 다음과 같은 프로젝트들이 파생되었다.

  - Chillifire - 무선 hotspot 관리에 중점을 둔 OpenWrt 기반 펌웨어
  - PacketProtector - [IDS](https://ko.wikipedia.org/wiki/IDS "wikilink"), [IPS](https://ko.wikipedia.org/wiki/IPS "wikilink"), [VPN](https://ko.wikipedia.org/wiki/VPN "wikilink"), 웹 안티 바이러스 등의 기능을 제공하는 OpenWrt 기반 보안 배포판.
  - Coova - 무선 hotspot 관리에 중점을 둔 OpenWrt 기반 펌웨어.
  - Freifunk - OLSR 무선 메시 네트워크를 지원하는 OpenWrt 기반의 독일 소프트웨어. 다른 언어도 지원.
  - RO.B.IN - ROBIN (ROuting Batman INside)은 OpenWrt 카미카제를 기반으로하여 Atheros AP51 라우터에서 돌아가는 오픈 소스 메시 네트워크 프로젝트이다. B.A.T.M.A.N. 라우팅 알고리즘을 사용한다.
  - FON - hotspot으로 동작하는 OpenWrt 기반 무선 라우터. 툴체인과 소스 코드는 fonosfera.org 에서 받을 수 있다.

## Sveasoft 논란

2006-03-11 OpenWrt 개발자들은 [Sveasoft](https://ko.wikipedia.org/wiki/Sveasoft "wikilink")가 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink") 라이센스를 위반했으며 계속되는 Sveasoft의 OpenWrt 배포를 금지한다고 공식 발표했다.\[1\] 이에대한 응답으로 Sveasoft는 Sveasoft와 [Broadcom](https://ko.wikipedia.org/wiki/Broadcom "wikilink")이 권리를 가지고 있는 소프트웨어를 OpenWrt 쪽에서 불법적으로 재배포 했으며 저작권자의 허락없이 GPL 라이센스 하에 두었다고 주장했다.\[2\] 각 그룹은 각자 상대방의 혐의를 부인했다.

## 작명

OpenWrt의 주요 버전명은 칵테일 이름에서 따왔다. SSH 로그인 화면에 제조법이 나와 있다.

  - 0.9 : [화이트러시안 (칵테일)](https://ko.wikipedia.org/wiki/화이트러시안_\(칵테일\) "wikilink")
  - 08.09 : [카미카제 (칵테일)](https://ko.wikipedia.org/wiki/카미카제_\(칵테일\) "wikilink")
  - 10.03 : [백파이어 (칵테일)](https://ko.wikipedia.org/wiki/백파이어_\(칵테일\) "wikilink")

## 참조

## 외부 링크

  - [OpenWrt 공식 웹사이트](https://openwrt.org/)
  - [OpenWrt Wiki](http://wiki.openwrt.org)

[분류:리눅스 배포판](https://ko.wikipedia.org/wiki/분류:리눅스_배포판 "wikilink") [분류:커스텀 펌웨어](https://ko.wikipedia.org/wiki/분류:커스텀_펌웨어 "wikilink") [분류:와이파이](https://ko.wikipedia.org/wiki/분류:와이파이 "wikilink") [분류:임베디드 리눅스 배포판](https://ko.wikipedia.org/wiki/분류:임베디드_리눅스_배포판 "wikilink") [분류:데비안 기반 배포판](https://ko.wikipedia.org/wiki/분류:데비안_기반_배포판 "wikilink")

1.
2.