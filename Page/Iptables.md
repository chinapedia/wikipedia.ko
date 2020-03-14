> This article is converted from Wikipedia: [Iptables](https://ko.wikipedia.org/wiki/Iptables).


**iptables**는 [시스템 관리자가](https://ko.wikipedia.org/wiki/시스템_관리자 "wikilink") [리눅스 커널](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") [방화벽](https://ko.wikipedia.org/wiki/방화벽_\(네트워킹\) "wikilink")(다른 [넷필터](../Page/넷필터.md "wikilink") 모듈로 구현됨)이 제공하는 테이블들과 그것을 저장하는 체인, 규칙들을 구성할 수 있게 해주는 [사용자 공간](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink") 응용 프로그램이다. 각기 다른 커널 모듈과 프로그램들은 현재 다른 프로토콜을 위해 사용되는데, iptables는 IPv4에, ip6tables는 IPv6에, arptables는 [ARP에](https://ko.wikipedia.org/wiki/주소_결정_프로토콜 "wikilink"), ebtables는 [이더넷 프레임에](https://ko.wikipedia.org/wiki/이더넷_프레임 "wikilink") 적용된다.

iptables는 동작을 위해 상승된 권한을 요구하며 사용자 [루트가](https://ko.wikipedia.org/wiki/슈퍼_유저 "wikilink") 실행하여야 하는데, 그렇지 않으면 작동하지 않는다. 리눅스 시스템에서 iptables는 /usr/sbin/iptables에 설치되며, man iptables를 이용하여 열면 표시되는 [man page에](https://ko.wikipedia.org/wiki/man_page "wikilink") 문서화되어 있다. /sbin/iptables에서도 볼 수 있지만 iptables는 필수적인 이진 파일이라기 보다는 서비스에 더 가깝기 때문에 선호되는 위치는 /usr/sbin이다.

iptables라는 용어는 커널 수준의 구성 요소를 아울러 가리킬 때에도 흔히 사용된다. *x_tables*는 4개의 모듈이 사용하는 공유된 코드 일부를 전달하는 커널 모듈의 이름이며, 확장을 위해 사용되는 API를 제공한다. 즉, Xtables는 대체적으로 방화벽 (v4, v6, arp, eb) 구조 전반을 가리키는데 쓰인다.

iptables의 후임자는 nftables이며, 이것은 커널 버전 3.13 이후에 리눅스 커널에 통합되었다.\[1\]

## 개요

Xtables는 시스템 관리자가 패킷을 다루기 위한 *규칙(rules)*의 *체인(chains)*를 포함하는 *tables*를 정의할 수 있게 한다. 패킷들은 체인에 존재하는 규칙을 순회함으로써 처리된다. 체인의 규칙은 goto나 jump를 다른 체인으로 유발할 수 있으며, 이것은 어떤 수준의 네스팅이 요구되더라도 반복적으로 수행될 수 있다. jump는 "call"과 비슷한데, 점프한 위치가 저장된다. 컴퓨터에서 나가거나 들어오는 모든 네트워크 패킷은 적어도 하나의 체인을 순회한다. [섬네일](https://ko.wikipedia.org/wiki/파일:Netfilter-packet-flow.svg "wikilink") 패킷의 원본은 초기에 순회할 체인을 고른다. 비록 테이블이 모든 체인들을 갖지는 않지만, 5개의 미리 정의된 체인들이 존재한다. 미리 정의된 체인들은 정책(*policy*)을 갖는데, 예를 들면 DROP이 있다. 시스템 관리자는 요구되는 만큼 다른 체인들을 만들 수 있다. 이러한 체인들은 정책을 갖지 않는다; 만약 패킷이 체인의 끝에 도달하면 이것은 호출했던 체인으로 돌아간다. 체인은 비어있을 수 있다.

  - `PREROUTING`: 패킷들은 라우팅 결정이 만들어지기 전에 이 체인에 들어갈 것이다.
  - `INPUT`: 패킷이 로컬상에서 전달될 경우, 이것은 열린 소켓을 가진 프로세스들과 아무런 상관이 없다; 로컬 전달은 "local-delivery"라우팅 테이블에 의해 제어된다: `ip route show table local`.
  - `FORWARD`: 라우팅되고 로컬 전달이 아닌 모든 패킷들은 이 체인을 순회한다.
  - `OUTPUT`: 기계 자체에서 보내진 패킷들은 이 체인을 마주칠 것이다.
  - `POSTROUTING`: 라우팅 결정이 만들어 졌을 때, 패킷들은 하드웨어에 보내지기 전에 이 체인에 들어온다.

체인에서 각 규칙들은 어떤 패킷들이 매치되는지의 명시를 포함한다. 이것은 또한 확장에 사용되는 대상(*target*) 또는 빌트인 결정 중 하나인 *verdict*를 포함할 수 있다. 패킷이 체인을 순회할 때, 각 규칙은 차례로 검사된다. 만약 규칙이 패킷과 맞지 않다면 패킷은 다음 규칙으로 전달된다. 만약 규칙이 패킷에 맞다면 규칙은 대상/verdict에 지시된 행동을 취하며, 이것은 패킷을 허용할지 아닐지의 결과로 나타난다. 매치들은 패킷들이 테스트될 조건들을 포함함으로써 룰셋들의 큰 부분을 이룬다. 이것들은 OSI 모델 들 중 어느 단계에서도 일어날 수 있다. 예를 들면 `--mac-source` 와 `-p tcp --dport` 파라미터들이 있으며, 또한 프로토콜에 독립적인 매치들도 있는데 이것의 예로는 `-m time`이 있다.

패킷은 다음의 경우까지 체인을 순회한다

1.  규칙이 패킷에 매치되며 궁극적인 운명을 결정한다. 예를 들면 `ACCEPT` 또는 `DROP`의 호출, 또는 이러한 궁극적인 운명을 반환하는 모듈
2.  규칙이 `RETURN` verdict를 호출하며, 그런 경우에 처리는 호출하는 체인에 반환된다
3.  체인의 끝에 도달된다; 순회는 부모 체인에서 지속되거나 (만약 `RETURN`가 사용된 경우), 궁극적인 운명인 기본 정책이 사용된다.

대상들은 또한 `ACCEPT` (`NAT` 이 이렇게 한다) 또는 `DROP` (예를 들면 `REJECT` 모듈) 같은 verdict를 반환하지만, 또한 대상/verdict가 전혀 맞지 않을 때 다음 규칙을 지속하기 위해 `CONTINUE` (예를 들면 `LOG` 모듈; `CONTINUE`는 내부 이름이다)를 함축할 수 있다.

## 사용자 공간 유틸리티

### 프론트엔드

iptables를 위한 규칙을 설정하는 것을 가능하게 하는 수많은 타사 응용 소프트웨어가 존재한다. 프론트엔드는 텍스트 또는 그래픽일 수 있다. 이것은 사용자가 클릭함으로써 간단하게 룰셋을 만들 수 있고, 스크립트는 일반적으로 셸 스크립트를 가리키는데, 이것은 iptables나 `iptables-restore`를 미리 정의된 규칙들이나 템플릿에서 확장된 규칙들과 함께 호출한다. 리눅스 배포판들은 일반적으로 템플릿 방식을 사용하는데, 이러한 템플릿 기반 접근법은 규칙 생성기의 제한된 형태이며, 이러한 생성기는 또한 PHP 웹 페이지들처럼 독자적으로 존재한다.

이러한 프론트엔드들, 생성기들 그리고 스크립트들은 종종 그들의 빌트인 템플릿 시스템에 의해 제한된다. 또한 생성된 규칙들은 일반적으로 사용자가 원하는 특정한 방화벽 효과를 위해 최적화되어있지 않아서 개발자들에게 유지 보수 비용을 끌어올리는 경향이 있다.

### 다른 툴들

  - IPFire은 리눅스 기반 방화벽 배포판이며 웹 기반 사용자 인터페이스가 방화벽 규칙 설정을 위해 제공되는데, 이것은 명령 줄 라인의 사용 없이 iptables 규칙들을 생성할 수 있게 한다.
  - NuFW는 넷필터에 대한 방화벽 확장이다.
  - [abyle-firewall](https://code.google.com/p/abyle-firewall/source/browse/)은 파이썬/xml 기반 iptable 래퍼이다.([wiki](https://web.archive.org/web/20140506015423/http://scuq.abyle.org/wiki/doku.php/abyle-firewall:start))

## 같이 보기

  - [NPF](https://ko.wikipedia.org/wiki/NPF "wikilink")
  - [PF (방화벽)](https://ko.wikipedia.org/wiki/PF_\(방화벽\) "wikilink")
  - [ipfw](https://ko.wikipedia.org/wiki/ipfw "wikilink")
  - [ipfilter](https://ko.wikipedia.org/wiki/ipfilter "wikilink")

## 각주

## 외부 링크

  - [The netfilter/iptables project Web page](http://www.netfilter.org/)
  - [iptables](http://freecode.com/projects/iptables/)<span> at </span>Freecode
  - [The netfilter/iptables documentation page](http://www.netfilter.org/documentation/index.html) (outdated)
  - [Detecting and deceiving network scans](http://inai.de/documents/Chaostables.pdf) - countermeasures against nmap
  - [The IPTables ManPage for syntax help](http://ipset.netfilter.org/iptables.man.html)
  - [Iptables Tutorial 1.2.2 by Oskar Andreasson](http://www.frozentux.net/iptables-tutorial/iptables-tutorial.html)
  - [Acceleration of iptables Linux Packet Filtering using GPGPU](http://www.researchgate.net/profile/Mahmood_Ahmadi/publication/261550748_Acceleration_of_IPTABLES_Linux_Packet_Filtering_using_GPGPU/links/0c96053494b348cf52000000)

[분류:방화벽 소프트웨어](https://ko.wikipedia.org/wiki/분류:방화벽_소프트웨어 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink")

1.