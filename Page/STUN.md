> This article is converted from Wikipedia: [STUN](https://ko.wikipedia.org/wiki/STUN).


**STUN**(Session Traversal Utilities for NAT)은 실시간 음성, 비디오, 메시징 애플리케이션, 그리고 기타 상호작용 통신 부문에서 [네트워크 주소 변환](../Page/네트워크_주소_변환.md "wikilink")(NAT) 게이트웨이의 [트레버설을](https://ko.wikipedia.org/wiki/NAT_트레버설 "wikilink") 위한, 네트워크 프로토콜을 포함하는 메소드들의 표준화된 모임이다.

STUN은 [상호 연결 확립](https://ko.wikipedia.org/wiki/상호_연결_확립 "wikilink")(ICE), [세션 개시 프로토콜](../Page/세션_개시_프로토콜.md "wikilink")(SIP), [WebRTC](../Page/WebRTC.md "wikilink") 등의 기타 프로토콜들에 의해 사용되는 도구이다. 호스트가 네트워크 주소 변환기의 존재를 찾아내고 NAT의 원격 호스트에 대한 애플리케이션의 [사용자 데이터그램 프로토콜](../Page/사용자_데이터그램_프로토콜.md "wikilink")(UDP) 플로를 위해 할당된 매핑된 (보통은 퍼블릭) [인터넷 프로토콜](../Page/인터넷_프로토콜.md "wikilink")(IP) 주소와 포트 번호를 발견하기 위한 도구를 제공한다. 이 프로토콜은 대개 퍼블릭 [인터넷](../Page/인터넷.md "wikilink")인 NAT의 반대(퍼블릭)편에 위치한 서드파티 네트워크 서버(STUN 서버)로부터의 도움이 필요하다.

원래 STUN은 Simple Traversal of User Datagram Protocol (UDP) through Network Address Translators의 준말이었으나,\[1\] 이 제목은 STUN의 이름은 그대로 보존하되 RFC 5389로 출판된 업데이트된 메소드 방식 사양에서 변경되었다.\[2\]

## 설계

STUN은 통신 프로토콜들이 2개의 통신 종단점 사이의 경로에 위치한 네트워크 주소 변환기를 찾아내고 횡단할 수 있게 하는 도구이다. 가벼운 [클라이언트-서버](../Page/클라이언트_서버_모델.md "wikilink") 프로토콜로 구현되어 있으며, 일반적으로 [인터넷](../Page/인터넷.md "wikilink")인 쉽게 접근 가능한 네트워크에 위치한 서드파티 서버의 단순 쿼리 및 응답 구성 요소만 요구한다. 클라이언트 사이드는 [음성 인터넷 프로토콜](../Page/음성_인터넷_프로토콜.md "wikilink")(VoIP) 전화 또는 인스턴트 메신저 클라이언트 등의 사용자의 통신 애플리케이션에 구현되어 있다.

## 각주

## 외부 링크

  - [STUNTMAN - Open source STUN server code for RFC 5389 and RFC 3489](http://www.stunprotocol.org)
  - [STUNT](http://nutss.gforge.cis.cornell.edu/stunt.php) - "STUN and TCP too", which extends STUN to include TCP functionality
  - [Yahoo\! - Director of Engineering explaining STUN and TURN (Video)](https://www.youtube.com/watch?v=9MWYw0fltr0&eurl=http%3A%2F%2Fwww%2Evoip%2Dnews%2Ecom%2Ffeature%2Ftop%2Dvoip%2Dvideos%2D051707%2F)
  - [List of 267 public STUN servers from EmerCoin project. Tested 2017-08-08](https://web.archive.org/web/20190910164939/http://olegh.ftp.sh/public-stun.txt)

[분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:네트워크 주소 변환](https://ko.wikipedia.org/wiki/분류:네트워크_주소_변환 "wikilink") [분류:음성 인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:음성_인터넷_프로토콜 "wikilink")

1.  RFC 3489, *STUN - Simple Traversal of User Datagram Protocol (UDP) Through Network Address Translators (NATs)*, J. Rosenberg, J. Weinberger, C. Huitema, R. Mahy, The Internet Society (March 2003)
2.  RFC 5389, *Session Traversal Utilities for NAT (STUN)*, J. Rosenberg, R. Mahy, P. Matthews, D. Wing, The Internet Society (October 2008)