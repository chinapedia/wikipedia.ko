> This article is converted from Wikipedia: [LwIP](https://ko.wikipedia.org/wiki/LwIP).


**lwIP**(**lightweight IP**)는 [임베디드 시스템에서](../Page/임베디드_시스템.md "wikilink") 널리 사용되는 [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") [TCP/IP 스택이다](../Page/인터넷_프로토콜_스위트.md "wikilink"). lwIP는 스웨덴 컴퓨터 과학 연구소 (Swedish Institute of Computer Science)의 Adam Dunkels 에 의해 처음 개발되었으며 현재는 전 세계 개발자 네트워크에 의해 개발 및 유지 관리되고 있다.

lwIP는 많은 임베디드 시스템 제조업체에서 사용한다. 예로 [알테라](../Page/알테라.md "wikilink") (니오스 II [운영체제](../Page/운영_체제.md "wikilink")), [아날로그 디바이스](../Page/아날로그_디바이스.md "wikilink") ([블랙 핀](../Page/블랙핀.md "wikilink") [DSP의](../Page/디지털_신호_처리_장치.md "wikilink") 칩),<ref>

<div>

" [Blackfin 프로세서를 사용하여 복잡한 VDK / LwIP 애플리케이션 구현하기", Kaushal Sanghai, Analog Devices Inc. 2008년 9월](http://www.analog.com/static/imported-files/application_notes/EE-312_Rev2.pdf)

</div>

</ref> [자일링스](../Page/자일링스.md "wikilink"),<ref>

<div>

[Siva Velusamy, LightWeight IP (lwIP) 애플리케이션 예제, 자일링스, 2009년 6월](http://www.xilinx.com/support/documentation/application_notes/xapp1026.pdf)

</div>

</ref> [하니웰](../Page/허니웰.md "wikilink") (FAA 인증 항법 시스템의 일부)과 [프리 스케일 세미컨덕터](../Page/프리스케일_세미컨덕터.md "wikilink") (자동차 마이크로 컨트롤러용 이더넷 스트리밍 SW)가 있다.

## lwIP 네트워크 스택

lwIP 네트워크 스택 구현의 초점은 풀 스케일 TCP 스택을 사용하면서도 리소스 사용을 줄이는 것이다.\[1\] 따라서 lwIP는 수십 킬로바이트의 여유 RAM과 코드를 위한 약 40킬로바이트 이상의 ROM이 있는 임베디드 시스템에서 사용하기에 적합하다.

## lwIP 프로토콜 구현

[TCP/IP 스택](../Page/인터넷_프로토콜_스위트.md "wikilink") 외에도 lwIP에는 네트워크 인터페이스, 운영 체제 에뮬레이션 계층, 버퍼 및 메모리 관리 섹션과 같은 몇 가지 중요한 부분이 있다. 운영 체제 에뮬레이션 계층과 네트워크 인터페이스를 통해 lwIP 모듈과 [운영 체제 커널](../Page/커널_\(컴퓨팅\).md "wikilink") 간에 공통 인터페이스를 제공하므로 lwIP 모듈을 운영 체제에 이식 할 때 lwIP의 네트워크 스택이 제대로 작동 할 수 있다.\[2\]

[인터넷 계층에서](../Page/인터넷_계층.md "wikilink") lwIP의 네트워크 스택에는 여러 네트워크 인터페이스를 통한 패킷 전달을 처리 할 수 있는 [IP](../Page/인터넷_프로토콜.md "wikilink") (Internet Protocol) 구현이 포함된다.\[3\] [IPv4](../Page/IPv4.md "wikilink") 와 [IPv6](../Page/IPv6.md "wikilink") 모두 lwIP v2.0.0부터 듀얼 스택을 지원한다. 네트워크의 유지 보수 및 디버깅을 위해 lwIP는 구현 [ICMP](../Page/인터넷_제어_메시지_프로토콜.md "wikilink") (인터넷 제어 메시지 프로토콜)을 도입한다.\[4\] [IGMP](https://ko.wikipedia.org/wiki/인터넷_그룹_관리_프로토콜 "wikilink") (Internet Group Management Protocol)는 멀티 캐스트 트래픽 관리를 지원한다. MLD를 포함한 [ICMPv6](../Page/ICMPv6.md "wikilink") 은 IPv6 사용을 지원하기 위해 구현된다.

[데이터 링크 계층에서](https://ko.wikipedia.org/wiki/데이터_링크_계층 "wikilink") [이더넷](../Page/이더넷.md "wikilink") 용 lwIP의 인터넷 프로토콜 (IP)을 지원하려면 IPv4 [ARP](../Page/주소_결정_프로토콜.md "wikilink") (Address Resolution Protocol) 구현이 필요하며 IPv6 Neighbor Discovery Protocol이 필요한다. lwIP는 데이터 링크 계층에서 [PPP](../Page/점대점_프로토콜.md "wikilink") (Point-to-Point Protocol) 구현 위에서 작동 될 수도 있다. [전송 계층에서](../Page/전송_계층.md "wikilink") lwIP는 [혼잡 제어](../Page/혼잡_제어.md "wikilink"), RTT 추정 및 빠른 복구/ 빠른 재전송을 사용하여 [TCP](../Page/전송_제어_프로토콜.md "wikilink") (전송 제어 프로토콜)를 구현한다.\[5\] [UDP](../Page/사용자_데이터그램_프로토콜.md "wikilink") (사용자 데이터그램 프로토콜)는 실험적인 UDP-Lite 확장으로 구현된다.

### API 및 소켓

lwIP는 향상된 네트워크 스택 성능을 위한 특수한 no-copy API ([Application Programming Interface](../Page/API.md "wikilink"))를 제공한다. 버클리 소켓 API 는 선택 사항이다.\[6\] [원시 소켓](https://ko.wikipedia.org/wiki/네트워크_소켓 "wikilink") 또는 원시 pcb는 사용 된 API에 따라 제공된다.<ref>

<div>

[lwIP 함수 문서](http://www.nongnu.org/lwip/)

</div>

</ref>

### 응용 계층 지원

응용 계층에서 lwIP 네트워크 스택은 다음 프로토콜의 구현을 통해 지원 될 수 있다. 개인 MIB ( 관리 정보 기반 원 및 MIB 컴파일러가있는 v1, v2 또는 v3의 [SNMP](../Page/간이_망_관리_프로토콜.md "wikilink") (단순 네트워크 관리 프로토콜) 에이전트, [DNS](../Page/도메인_네임_시스템.md "wikilink") (Domain Name System)가 지원된다.

lwIP TCP/IP 스택을 구현하는 운영 체제는 응용 계층에서 IPv4 [DHCP](../Page/동적_호스트_구성_프로토콜.md "wikilink") (동적 호스트 구성 프로토콜) 클라이언트 또는 IPv4 링크-로컬 주소 (일명. 자동 IP)와 같은 다양한 지원 클라이언트 및 서버를 제공 할 수 있다. 특수화 된 원시 API 응용 프로그램에는 [HTTP](../Page/HTTP.md "wikilink") 서버, [SNTP](../Page/네트워크_타임_프로토콜.md "wikilink") 클라이언트, [SMTP](../Page/간이_우편_전송_프로토콜.md "wikilink") 클라이언트, [NetBIOS](../Page/넷바이오스.md "wikilink") 네임 서버, mDNS 응답자, [MQTT](../Page/MQTT.md "wikilink") 클라이언트 및 [TFTP](../Page/TFTP.md "wikilink") 서버가 포함된다.

## OS 구현

lwIP는 [ReactOS](https://ko.wikipedia.org/wiki/ReactOS "wikilink") 와 Genode\[7\] 에서 네트워크 스택으로 사용되며 [Minix](../Page/미닉스.md "wikilink") 와 [GNU Hurd](../Page/GNU_허드.md "wikilink") 에서 네트워크 서버를 구현하는 데 사용할 수 있다.

## 관련 문서

  - 마이크로 IP ( uIP )

## 참고 문헌

## 외부 링크

  - [Adam Dunkels' initial Lwip paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.109.1795&rep=rep1&type=pdf)
  - [lwIP 개발](http://savannah.nongnu.org/projects/lwip/)
  - [lwIP 문서 위키](http://lwip.wikia.com/wiki/LwIP_Wiki)
  - [lwIP 함수 홈페이지](http://www.nongnu.org/lwip/)
  - [lwIP former homepage (obsolete)](https://web.archive.org/web/20010604054508/http://www.sics.se/~adam/lwip/)

[분류:임베디드 시스템](https://ko.wikipedia.org/wiki/분류:임베디드_시스템 "wikilink")

1.
2.
3.
4.
5.
6.
7.