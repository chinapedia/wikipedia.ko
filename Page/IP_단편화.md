> This article is converted from Wikipedia: [IP ](https://ko.wikipedia.org/wiki/IP_).


[IP는](../Page/인터넷_프로토콜.md "wikilink") **IP 단편화**를 통해 데이터그램의 크기를 MTU이하로 작게 만들어 전송할 수 있도록 한다. RFC 791은 IP 단편화, 데이터그램의 전송, 재조립을 위한 프로시져를 기술한다. RFC 815는 호스트에서 쉽게 구현할 수 있는 간단한 재조립 알고리즘을 기술한다. Identification 필드와 Fragment offset 필드는 Don't Fragment 플래그, More Fragment 플래그와 함께 IP 데이터그램의 단편화와 재조립을 위해 사용된다.

[라우터](../Page/라우터.md "wikilink")가 다음 홉의 MTU보다 큰 크기의 [PDU](https://ko.wikipedia.org/wiki/PDU "wikilink")을 수신했을 때, 라우터에게는 두 가지 선택이 가능하다. 먼저 해당 PDU를 폐기하고 "Packet too Big"을 의미하는 [ICMP](https://ko.wikipedia.org/wiki/ICMP "wikilink") 메시지를 보내는 방법이 있고, 다른 방법으로 IP 패킷을 단편화하여 MTU보다 작은 링크를 통해 패킷을 전송하는 방법이 있다.

수신자가 단편화된 IP 패킷을 받았을 때, 이 호스트는 해당 IP 패킷을 재조립하여 상위 계층으로 전달해야 한다. 재조립은 오직 수신 호스트에서만 이루어진다. RFC 815는 IP 데이터그램의 재조립을 위한 간단한 알고리즘을 소개한다. 단편화 기법의 상세 동작 및 단편화를 위한 구조적인 접근은 [IPv4](../Page/IPv4.md "wikilink")와 [IPv6](../Page/IPv6.md "wikilink")에서 각각 다르다. IPv4와 IPv6는 서로 다른 헤더 필드를 가지지만, 단편화를 위한 필드는 유사하다. 따라서 단편화 및 재조립 알고리즘은 쉽게 재사용될 수 있다.

단편화된 패킷들이 유실되고 TCP와 같은 프로토콜에서 이들 단편들에 대한 재전송을 요구할 경우, IP 단편화는 상당한 재전송을 일으키게 된다.\[1\] 그러므로 IP 데이터그램의 크기를 정하기 전, 송신자는 일반적으로 두 가지 방법을 사용한다. 첫 번째는 IP 데이터그램의 크기를 첫 번째 홉의 MTU와 같게 하는 방법이 있다. 두 번째 방법은 RFC 1191에 기술된 *Path MTU discovery* 알고리즘을 사용하여 두 호스트간 path MTU을 구하여 IP 단편화를 피하는 방법이 있다.

## 외부 링크

  - RFC 791 Internet Protocol
  - RFC 815 IP Datagrams Reassembly Algorithms
  - RFC 1191 Path MTU Discovery
  - [IP Fragmentation](https://web.archive.org/web/20071225234433/http://penguin.dcs.bbk.ac.uk/academic/networks/network-layer/fragmentation/index.php)

## 관련 문헌

<references/>

[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink")

1.  Christopher A. Kent, Jeffrey C. Mogul, [Fragmentation Considered Harmful](http://citeseer.ist.psu.edu/335647.html)