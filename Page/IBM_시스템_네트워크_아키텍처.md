> This article is converted from Wikipedia: [IBM   ](https://ko.wikipedia.org/wiki/IBM___).


**시스템 네트워크 아키텍처**(, SNA)는 1974년에 만들어진 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")의 사유 [네트워크](https://ko.wikipedia.org/wiki/컴퓨터_네트워크 "wikilink") 아키텍처이다.\[1\] [컴퓨터](https://ko.wikipedia.org/wiki/컴퓨터 "wikilink")와 자신의 자원 간 상호 연결을 위한 완전한 [프로토콜 스택이다](https://ko.wikipedia.org/wiki/프로토콜_스택 "wikilink"). 포맷과 프토토콜을 기술하며, 그 자체가 소프트웨어의 일종은 아니다. SNA 구현을 통해 다양한 통신 패키지(가장 저명한 것으로, SNA 통신용 [메인프레임](https://ko.wikipedia.org/wiki/메인프레임 "wikilink") 패키지인 [VTAM](https://ko.wikipedia.org/wiki/VTAM "wikilink"))의 형태를 취한다.

## 역사

SNA는 1974년 9월, 새로운 통신 제품의 SNA/SDLC(동기 데이터 링크 제어) 프로토콜의 구현을 포함한, IBM의 "Advanced Function for Communications" 발표의 일부로 공개되었다.

  - [IBM 3767](https://ko.wikipedia.org/wiki/IBM_3767 "wikilink") 통신 터미널 (프린터)
  - [IBM 3770](https://ko.wikipedia.org/wiki/IBM_3770 "wikilink") 데이터 통신 시스템

IBM 3704/3705 통신 컨트롤러와, 그 컨트롤러에 소속된 네트워크 제어 프로그램, 또 시스템/370 및 이에 소속된 VTAM과 더불어 CICS, IMS 등의 기타 소프트웨어가 이들을 지원한다.

SNA는 주로 IBM 시스템 개발 부서 연구소가 설계한 것으로, 자세한 사항은 IBM의 시스템 참조 라이브러리 매뉴얼과 IBM 시스템 저널을 통해 참조가 가능하다.

SNA는 현재 은행과 기타 금융 트랜잭션 네트워크, 수많은 정부 기관에서 널리 사용된다.

2008년 IBM 출판물에 따르면: TCP/IP의 인기와 상승과 더불어, SNA는 참된 네트워크 아키텍처에서 "애플리케이션 및 애플리케이션 접근 아키텍처"로 변화하고 있다. 다시 말해, SNA에서 통신할 필요가 있는 응용 프로그램들이 다수 있지만, 필요한 SNA 프로토콜은 IP 네트워크를 통해 전달된다.\[2\]

## 주요 구성 요소 및 기술

SNA의 가장 중요한 요소는 다음을 포함한다:

  - [IBM 네트워크 컨트롤 프로그램](https://ko.wikipedia.org/wiki/IBM_네트워크_컨트롤_프로그램 "wikilink")(NCP): SNA가 정의하는 패킷 교환 프로토콜을 구현하는, [3705와](https://ko.wikipedia.org/wiki/IBM_3705 "wikilink") 이후 [37xx](https://ko.wikipedia.org/wiki/IBM_37xx "wikilink") 통신 프로세서 위에서 실행되는 통신 프로그램.
  - [동기 데이터 링크 제어](https://ko.wikipedia.org/wiki/동기_데이터_링크_제어 "wikilink")(Synchronous Data Link Control, SDLC): 싱글 링크 상에서 데이터 전송의 효율성을 상당히 높여주는 프로토콜.
  - [VTAM](https://ko.wikipedia.org/wiki/VTAM "wikilink"): 메인프레임 내에서 로그인, 세션 유지, 라우팅 서비스를 제공하는 소프트웨어 패키지.

## 네트워크 주소 지정 가능 단위

SNA 네트워크에서 네트워크 주소 지정 가능 단위(Network Addressable Units, NAU)는 주소로 할당되어 정보를 송수신할 수 있는 구성 요소이다. 이들은 더 나아가 다음과 같이 구별된다:

  - SSCP(System Services Control Point): 하위망에서 사용자를 위한 리소스 관리 및 기타 세션 서비스를 제공한다.<ref name="IBMSSCP">

Retrieved on 3 October 2015.</ref>

  - PU(Physical Unit): 다른 노드에 대한 링크를 제어하는 하드웨어와 소프트웨어 구성 요소의 복합체이다.<ref name="IBMPU">

Retrieved on 3 October 2015.</ref>

  - LU(Logical Unit): 사용자와 네트워크 간 중간다리 역할을 한다.<ref name="IBMLU">

Retrieved on 3 October 2015.</ref>

## 참고 문헌

  -
  -
  -
  -
  -
  -
  -
## 각주

## 외부 링크

  - [Cisco article on SNA](http://docwiki.cisco.com/wiki/IBM_Systems_Network_Architecture_Protocols)

  - [SNA protocols](http://www.protocols.com/pbook/sna.htm) quite technical

[분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink") [분류:IBM의 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM의_운영_체제 "wikilink")

1.  .
2.