> This article is converted from Wikipedia: [Zeroconf](https://ko.wikipedia.org/wiki/Zeroconf).


**Zeroconf** (Zero configuration networking)은 사람손에 의한 조작없이, 또한 특별한 설정서버를 사용하지 않고, 이용가능한 인터넷프로토콜(IP) 네트워크를 자동적으로 작성 하는 일종의 기법이다. Zero configuration networking은 컴퓨터나 프린터와 같은 장치를 자동적으로 네트워크에 접속하는것이 가능하게 한다. zeroconf가 없는 경우, 네트워크 관리자가 Dynamic Host Configuration Protocol (DHCP) 나 Domain Name System (DNS) 와 같은 서비스의 설정을 할 필요가 있고, 경우에 따라서는 각각 컴퓨터의 네트워크설정을 사람손으로 변경할 필요가 있고, 시간이 걸리고 귀찮다.

zeroconf 는 다음 3가지의 기술을 기반으로 하고 있다.

  - 네트워크 장치로의 네트워크 주소 할당
  - 컴퓨터 hostname의 자동 해석과 자동 배포
  - 프린터와 같은 네트워크 장치의 위치를 자동 감지

## 주소 선택

[IPv4](https://ko.wikipedia.org/wiki/IPv4 "wikilink")와[IPv6](https://ko.wikipedia.org/wiki/IPv6 "wikilink")는 [IP 주소를](https://ko.wikipedia.org/wiki/IP_주소 "wikilink") 자동설정하는 표준 방법이 존재한다.링크 로컬 이라고 불리는 그 주소 설정을 두고, IPv4에서는 RFC 3927 에 규정되어 있는 특별한 블럭 `169.254.0.0/16` 을 사용하고, IPv6에서는 prefix `fe80::/10` 를 사용한다.

거의 모든 IPv4 호스트는 링크로컬의 Address 설정(IPv4LL)을 DHCP서버가 이용할 수 없을 때 최후의 수단으로서만 사용한다.통상, IPv4호스트는 글로벌인지 링크로컬인지를 묻지않고 DHCP에서 할당 받은 Address를 사용하고 있다.그 이유중의 하나는 IPv4호스트가 인터페이스당 1개의 Address밖에 필요로 하지않기 때문이다.또 하나의 이유는 모든 IPv4호스트가 분산이름해석기능(예를 들어, [멀티케스트DNS](https://ko.wikipedia.org/wiki/멀티케스트DNS "wikilink"))을 쓰지는 않기 때문에, 그 때문에 네트워크위의 다른 호스트의 자동설정된 링크로컬 Address를 발견하는것이 곤란하기 때문이다.그러나, DHCP가 다른호스트에 할당 된 Address를 발견한 경우에도, 분산이름해석기능이 필요한 정보를 가진[유니캐스트](../Page/유니캐스트.md "wikilink")방식의DNS서버를 필요로 하고, 일부 네트워크는 DHCP로 할당받은 호스트 Address에 관하는 정보로 자동적으로 갱신 되는 DNS서버를 갖추고 있다.

IPv6호스트는 인터페이스마다 여러개의 Address를 서포트해야 된다.그것 뿐만 아니라, IPv6 호스트는 전역 주소가 이용가능한 경우에도 링크로컬 Address를 설정 할 수 없으면 안된다.게다가 IPv6호스트는 여러 개의 Router advertisement・message 의 수신에 응하여 여러 개의 전역 주소를 스스로 설정하는것이 가능하고, 그때문에 DHCP6서버가 필요없어지게 된다..자세히는 RFC 4862 을 참고.

IPv4에서도IPv6에서도, 자동설정 어드레스의 호스트고유부분은 무작위로 생성 될 수 있다.IPv6호스트는 일반적으로 최대64비트의 prefix와 제조될 때 할당받는 48비트의 [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") [MAC 주소로부터](../Page/MAC_주소.md "wikilink") 파생된 64비트의 EUI-64 를 결합한다.호스트는 통상 브로드케스트 쿼리를 통해, 생성하는 Address를 그 로컬네트워크 내의 다른 호스트가 사용하지 않는것을 보증할 필요가 있다.

RFC 3927 에서는 이 방법을「링크로컬」 주소 할당이라고 부른다. 그러나, [Microsoft](https://ko.wikipedia.org/wiki/Microsoft "wikilink")에서는 그것을 [Automatic Private IP Addressing (APIPA)](https://ko.wikipedia.org/wiki/APIPA "wikilink") 또는 *Internet Protocol Automatic Configuration* (IPAC) 라고 칭하고 있다(늦어도 [Windows 98](https://ko.wikipedia.org/wiki/Microsoft_Windows_98 "wikilink") 부터 서포트 하고 있다\[1\]).

## 각주

<references />

[분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink") [분류:도메인 네임 시스템](https://ko.wikipedia.org/wiki/분류:도메인_네임_시스템 "wikilink") [분류:컴퓨터 설정](https://ko.wikipedia.org/wiki/분류:컴퓨터_설정 "wikilink") [분류:애플의 소프트웨어](https://ko.wikipedia.org/wiki/분류:애플의_소프트웨어 "wikilink")

1.  [자동 TCP/IP Address 지정으로 DHCP 서버를 사용하는 방법](http://support.microsoft.com/kb/220874)