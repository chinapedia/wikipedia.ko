> This article is converted from Wikipedia: [Pcap](https://ko.wikipedia.org/wiki/Pcap).


**pcap**(**p**acket **cap**ture, 패킷 캡처)은 [컴퓨터](../Page/컴퓨터.md "wikilink") [네트워크 관리](https://ko.wikipedia.org/wiki/네트워크_관리 "wikilink") 분야에서 [네트워크 트래픽 포착용](https://ko.wikipedia.org/wiki/패킷_가로채기 "wikilink") [API](../Page/API.md "wikilink")를 구성하고 있다. [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제들은 **libpcap** 라이브러리에 pcap을 포함하고 있다. [윈도는](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") **WinPcap**이라는 libpcap [포팅을](../Page/이식_\(컴퓨팅\).md "wikilink") 이용한다.

감시 소프트웨어는 libpcap이나 WinPcap을 이용하여 [네트워크](https://ko.wikipedia.org/wiki/컴퓨터_네트워크 "wikilink") 상에 떠돌아다니는 [패킷](https://ko.wikipedia.org/wiki/패킷 "wikilink")을 포착할 수 있으며 새로운 버전에서는 [링크 레이어](https://ko.wikipedia.org/wiki/링크_레이어 "wikilink") 상의 네트워크 패킷을 전송할 수 있을뿐 아니라 libpcap이나 WinPcap과 함께 이용할 수 있는 네트워크 인터페이스 목록을 가져올 수 있다.

pcap API는 [C로](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 작성되었으며 [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink"), [닷넷](https://ko.wikipedia.org/wiki/마이크로소프트_닷넷 "wikilink") 언어, [스크립트 언어와](../Page/스크립트_언어.md "wikilink") 같은 다른 언어들은 일반적으로 [래퍼를](../Page/래퍼_라이브러리.md "wikilink") 이용한다. 이러한 래퍼들은 libpcap이나 WinPcap 자체적으로 제공되지는 않는다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 프로그램들은 C API에 직접 연결할 수도 있다. 오직 하나의 부분적인 객체 지향 C++ 래퍼는 현재 외부 소스로부터 이용할 수 있다.

## 각주

## 외부 링크

  - [libpcap (+tcpdump) 공식 웹사이트](http://www.tcpdump.org/)
  - [WinPcap (+WinDump) 공식 웹사이트](https://web.archive.org/web/20111008015701/http://www.winpcap.org/)

[분류:네트워크 분석기](https://ko.wikipedia.org/wiki/분류:네트워크_분석기 "wikilink") [분류:유닉스 네트워크 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_네트워크_관련_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")