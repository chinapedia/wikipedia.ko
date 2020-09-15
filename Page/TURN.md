> This article is converted from Wikipedia: [TURN](https://ko.wikipedia.org/wiki/TURN).


**TURN**(Traversal Using Relays around NAT)은 멀티미디어 애플리케이션을 위해 [네트워크 주소 변환](../Page/네트워크_주소_변환.md "wikilink")(NAT) 또는 [방화벽](https://ko.wikipedia.org/wiki/방화벽 "wikilink")에서 보조하는 [프로토콜이다](../Page/통신_프로토콜.md "wikilink"). [전송 제어 프로토콜](../Page/전송_제어_프로토콜.md "wikilink")(TCP) 및 [사용자 데이터그램 프로토콜](../Page/사용자_데이터그램_프로토콜.md "wikilink")(UDP)와 사용이 가능하다. [NAT](../Page/네트워크_주소_변환.md "wikilink") 장치 하의 네트워크 클라이언트에 유용하다. TURN은 NAT를 경유하는 사설 네트워크의 잘 알려진 포트 상의 [서버](../Page/서버.md "wikilink")를 구동하는데 도움을 주지 않는다. 예를 들어 전화에서처럼 NAT 뒤의 사용자가 하나의 피어에만 연결하는 것을 지원한다.

TURN은 "RFC 5766"에 의해 규정된다. [IPv6](../Page/IPv6.md "wikilink")용 TURN의 업데이트는 "RFC 6156"에 규정되어 있다. TURN URI 스킴은 "RFC 7065"에 문서화되어 있다.

## 개요

NAT는 수많은 장점을 제공하지만 수많은 단점이 따라오기도 한다. 해당 단점들 가운데 가장 큰 문제는 기존의 수많은 IP 애플리케이션의 동작을 막고 새로운 애플리케이션의 디플로이를 어렵게 만든다는 것이다. "NAT 친화" 프로토콜을 빌드하는 방법을 기술하는 여러 가이드라인이 개발되었으나 수많은 프로토콜들은 단순히 이 가이드라인을 따라 구성하는 것은 불가능하다. 이러한 프로토콜의 예로 멀티미디어 애플리케이션과 파일 공유를 들 수 있다.

[STUN](../Page/STUN.md "wikilink")은 애플리케이션이 NAT를 경유하는 수단을 제공한다. STUN은 클라이언트가 트랜스포트 주소(IP 주소와 포트)를 취득할 수 있게 하는데, 이는 피어로부터 패킷을 수신하는데 유용하게 만들어 준다. 그러나 STUN을 통해 취득한 주소는 모든 피어에 유용하지 않을 수 있다. 이러한 주소들은 네트워크 위상 조건에 따라 동작한다. 그러므로 STUN 그 자체는 NAT 경유를 위한 완전한 해결책을 제공하는 것은 아니다.

완전한 해결책에는 패킷을 공용 인터넷에 내보낼 수 있는 피어로부터 미디어를 수신할 수 있는 트랜스포트 주소를 클라이언트가 취득할 수 있는 수단을 요구한다. 이는 공용 인터넷에 상주하는 서버를 통해 데이터를 릴레이(relay)하는 방식으로만 달성할 수 있다. TURN은 이러한 릴레이로부터 IP 주소와 포트를 클라이언트가 취득할 수 있게 도와준다.

TURN이 클라이언트에 연결을 거의 항상 제공함에도 불구하고 TURN 서버 제공자에게는 리소스가 상당히 집중된다. 그러므로 마지막 수단으로만 TURN을 사용할 것이 권고되며 가능하면 다른 구조(STUN 또는 직접 연결)가 선호된다. 이를 달성하기 위해 [상호 연결 확립](https://ko.wikipedia.org/wiki/상호_연결_확립 "wikilink")(ICE) 방식을 사용하여 연결의 최적 수단을 감지해낼 수 있다.

## 외부 링크

  - RFC 5766
  - [Yahoo\! - Director of Engineering explaining STUN and TURN (Video)](https://www.youtube.com/watch?v=9MWYw0fltr0&eurl=http%3A%2F%2Fwww%2Evoip%2Dnews%2Ecom%2Ffeature%2Ftop%2Dvoip%2Dvideos%2D051707%2F)
  - [STUN, TURN and ICE (full explanation with graphics)](http://anyconnect.com/stun-turn-ice/)

[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink") [분류:네트워크 주소 변환](https://ko.wikipedia.org/wiki/분류:네트워크_주소_변환 "wikilink") [분류:음성 인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:음성_인터넷_프로토콜 "wikilink") [분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink")