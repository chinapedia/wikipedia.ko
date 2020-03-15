> This article is converted from Wikipedia: [SoftEther VPN](https://ko.wikipedia.org/wiki/SoftEther_VPN).


**SoftEther VPN**은 자유 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink"), 크로스 플랫폼, 멀티 프로토콜 [VPN](https://ko.wikipedia.org/wiki/가상_사설망 "wikilink") 클라이언트이자 VPN 서버 소프트웨어의 하나로, [쓰쿠바 대학의](https://ko.wikipedia.org/wiki/쓰쿠바_대학 "wikilink") 노보리 다이유의 박사 논문 연구의 일환으로서 개발되었다. SSL VPN, [L2TP](https://ko.wikipedia.org/wiki/L2TP "wikilink")/[IPsec](https://ko.wikipedia.org/wiki/IPsec "wikilink"), [오픈VPN](../Page/오픈VPN.md "wikilink"), 마이크로소프트 [시큐어 소켓 터널링 프로토콜과](https://ko.wikipedia.org/wiki/시큐어_소켓_터널링_프로토콜 "wikilink") 같은 VPN 프로토콜들이 하나의 VPN 서버에서 제공된다. 2014년 1월 4일 [GNU 일반 공중 사용권](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용권 "wikilink") 라이선스를 사용하여 출시되었다.

SoftEther VPN은 [NAT traversal을](https://ko.wikipedia.org/wiki/NAT_traversal "wikilink") 지원함으로써 [가정용 게이트웨이](https://ko.wikipedia.org/wiki/가정용_게이트웨이 "wikilink"), 기업용 [라우터](https://ko.wikipedia.org/wiki/라우터 "wikilink"), [방화벽](https://ko.wikipedia.org/wiki/방화벽_\(네트워킹\) "wikilink") 뒤의 컴퓨터 상에 VPN 서버를 구동하기 유용하게 만들어준다. [심층 패킷 검사를](https://ko.wikipedia.org/wiki/심층_패킷_검사 "wikilink") 수행하는 방화벽들은 SoftEther의 VPN 트랜스포트 패킷을 VPN 터널로 감지할 수 없는데, 그 까닭은 HTTPS를 사용하여 이 연결을 은폐하기 때문이다.

SoftEther VPN은 풀 이더넷 프레임 활용을 사용하고 메모리 복사 작업을 감소시키며, 병렬 전송, 클러스터링을 사용함으로써 성능을 최적화한다. 이와 더불어 스루풋을 증가시키면서 VPN 연결에 일반적으로 관련된 레이턴시를 줄인다.

[thumb](https://ko.wikipedia.org/wiki/파일:softethervpn_stack.jpg "wikilink")

## 상호 운용성

SoftEther VPN 서버와 VPN 브리지는 [마이크로소프트 윈도우](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), 최대 [OS X 마운틴 라이언까지의](https://ko.wikipedia.org/wiki/OS_X_마운틴_라이언 "wikilink") [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink"), [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 운영 체제에서 실행된다. SoftEther VPN 클라이언트는 [마이크로소프트 윈도우](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")에서 실행된다.

SoftEther VPN 서버는 SoftEther VPN 프로토콜을 서비스하지만 [오픈VPN](../Page/오픈VPN.md "wikilink"), 마이크로소프트 [시큐어 소켓 터널링 프로토콜](https://ko.wikipedia.org/wiki/시큐어_소켓_터널링_프로토콜 "wikilink")(SSTP), SSL VPN, EtherIP, [L2TPv3](https://ko.wikipedia.org/wiki/L2TPv3 "wikilink"), [IPsec](https://ko.wikipedia.org/wiki/IPsec "wikilink")도 서비스한다. [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink"), [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink"), 윈도우 폰([L2TP](https://ko.wikipedia.org/wiki/L2TP "wikilink")/[IPsec](https://ko.wikipedia.org/wiki/IPsec "wikilink") 경유)을 실행하는 모바일 장치도 지원한다.

다른 VPN 프로토콜을 지원하는 VPN 클라이언트와 엔드포인트도 사용할 수 있다. 여기에는 시스코, 주니퍼, 링크시스([DD-WRT](https://ko.wikipedia.org/wiki/DD-WRT "wikilink")와 함께), 아수스 등 수많은 라우터들이 포함된다.

## 같이 보기

  - [오픈VPN](../Page/오픈VPN.md "wikilink") - 오픈 소스 VPN 프로그램

## 각주

## 외부 링크

  -
  - [Multi-Protocol SoftEther VPN Becomes Open Source](http://www.linuxtoday.com/upload/multi-protocol-softether-vpn-becomes-open-source-140107065009.html) (리눅스 투데이)

[분류:가상사설망](https://ko.wikipedia.org/wiki/분류:가상사설망 "wikilink") [분류:네트워크 보안](https://ko.wikipedia.org/wiki/분류:네트워크_보안 "wikilink") [분류:2014년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2014년_소프트웨어 "wikilink")