> This article is converted from Wikipedia: [Time to live](https://ko.wikipedia.org/wiki/Time_to_live).


**타임 투 리브**()는 [컴퓨터](../Page/컴퓨터.md "wikilink")나 [네트워크](https://ko.wikipedia.org/wiki/네트워크 "wikilink")에서 데이터의 유효 기간을 나타내기 위한 방법이다. TTL은 [계수기](../Page/계수기.md "wikilink")나 [타임스탬프](../Page/타임스탬프.md "wikilink")의 형태로 데이터에 포함되며, 정해진 유효기간이 지나면 데이터는 폐기된다. [컴퓨터 네트워크에서](https://ko.wikipedia.org/wiki/컴퓨터_네트워크 "wikilink") TTL은 패킷의 무한 순환을 방지하는 역할을 한다. 컴퓨터 애플리케이션에서 TTL은 [캐시](https://ko.wikipedia.org/wiki/캐시 "wikilink")의 성능이나 프라이버시 수준을 향상시키는 데에 사용되기도 한다.

## IP 패킷

[인터넷 프로토콜에서](https://ko.wikipedia.org/wiki/인터넷_프로토콜 "wikilink") TTL은 8비트 크기의 필드이다. [IPv4](https://ko.wikipedia.org/wiki/IPv4 "wikilink") 헤더에서 TTL은 20 [옥텟](https://ko.wikipedia.org/wiki/옥텟_\(컴퓨팅\) "wikilink") 중 8번째 옥텟이며, [IPv6](https://ko.wikipedia.org/wiki/IPv6 "wikilink") 헤더에서는 40 옥텟 중 8번째 옥텟이다. TTL의 최댓값은 단일 옥텟의 최댓값에 해당하는 255이다. 권장되는 초기값은 64이다.\[1\]\[2\]

TTL값은 IP [데이터그램이](https://ko.wikipedia.org/wiki/패킷 "wikilink") 인터넷 시스템 내에서 존재할 수 있는 시간의 상한선으로 볼 수 있다. TTL 필드는 데이터그램의 송신자에 의해 설정되며, 목적지까지의 전송 경로에 있는 모든 [라우터](../Page/라우터.md "wikilink")들에 의해 그 값이 감소된다. 목적지에 다다르기 전에 TTL 필드의 값이 0이 되면 해당 데이터그램은 폐기되고 [ICMP](https://ko.wikipedia.org/wiki/ICMP "wikilink") 에러 데이터그램 11 - Time Exceeded가 송신자에게 보내진다. TTL 필드의 목적은 전달되지 못한 데이터그램이 인터넷 시스템 내에서 지속적으로 순환하여 넘쳐나게 되는 상황을 방지하는 데에 있다.

[IPv4](https://ko.wikipedia.org/wiki/IPv4 "wikilink") 환경에서 TTL 값의 단위는 [초이며](https://ko.wikipedia.org/wiki/초_\(시간\) "wikilink"), 이론적으로 이 값은 목적지까지의 경로에서 경유하게 되는 모든 호스트에서 1 이상의 양만큼 감소될 수 있다. 그러나 실제 적용에서 TTL 값은 매 홉(hop)마다 1씩만 감소된다. 이러한 상황을 고려하여, [IPv6](https://ko.wikipedia.org/wiki/IPv6 "wikilink")에서 이 필드의 명칭은 홉 리미트(hop limit)로 변경되었다.

## DNS 레코드

TTL은 [도메인 네임 시스템](https://ko.wikipedia.org/wiki/도메인_네임_시스템 "wikilink")(DNS)에서도 사용된다. DNS에서 권한있는(authoritative) 네임서버는 특정 리소스 레코드의 TTL 값을 설정한다. 재귀적(recursive) 캐시 네임서버가 권한있는 네임서버에 질의를 보낼 때, 캐시 네임서버는 그 레코드를 TTL 값에 해당하는 시간동안 캐시에 저장해 둔다. 추후 스터브 리졸버(stub resolver)가 캐시 네임서버에 동일한 레코드에 대한 질의를 보냈을 때, 해당 레코드의 TTL 값이 아직 만료되지 않았다면 캐시 네임서버는 권한있는 네임서버에 질의를 보낼 필요 없이 캐시에 저장된 정보를 이용해 바로 응답을 하게 된다. 네임서버는 특정 도메인이 존재하지 않음을 나타내는 NXDOMAIN 응답에 대해서도 TTL 값을 가질 수 있다. 다만 이 경우에는 일반적으로 그 값이 최대 3시간 정도로 짧다.

TTL 값이 짧으면 상위의 권한있는 네임서버에 가해지는 부하가 커진다는 단점이 있지만, 반면에 메일 교환 레코드(mail exchange record)와 같이 주소 변경에 민감한 서비스에 적합하다는 장점을 가진다. 이 때문에 특정 서비스의 주소가 옮겨지는 경우, 이로 인한 혼란을 최소화하기 위해 DNS 관리자는 관련 레코드의 TTL 값을 낮춘다.

DNS에서 사용되는 TTL 값의 단위는 [초이다](https://ko.wikipedia.org/wiki/초_\(시간\) "wikilink"). 과거에 주로 사용되었던 값은 86400초(24시간)인데, 이는 권한있는 네임서버가 DNS 레코드를 변경했을 때 전 세계에 흩어져 있는 DNS 서버들이 최대 24시간동안 업데이트되지 않은 옛 주소를 갖고 있을 수 있음을 의미한다.

오늘날의 새로운 DNS 방식은 [재해 복구 시스템의](https://ko.wikipedia.org/wiki/재해_복구 "wikilink") 일부분으로서, 의도적으로 매우 낮게 설정된 TTL 값을 가질 수 있다. 예를 들어, TTL 값이 300초일 경우 해당 레코드는 5분 후에 만료되어 빠르게 갱신될 수 있으며, 이를 통해 관리자는 레코드를 제때에 수정하고 업데이트하는 것이 가능하다. TTL 값은 레코드 단위로 할당되며, 전 세계의 모든 표준 DNS 시스템은 특정 레코드의 TTL 값을 개별적으로 설정하는 것을 허용한다. 단, 이런 경우 다수의 DNS 네임서버들이 권한있는 네임서버로부터 받은 레코드에 관계 없이 각자 TTL을 설정할 경우, TTL이 만료된 이후에 그 하위 DNS 서버들이 새로운 레코드를 제대로 업데이트 받지 못할 가능성이 생긴다는 문제가 있다.

## 각주

<references/>

[분류:인터넷 구조](https://ko.wikipedia.org/wiki/분류:인터넷_구조 "wikilink")

1.
2.