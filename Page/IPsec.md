> This article is converted from Wikipedia: [IPsec](https://ko.wikipedia.org/wiki/IPsec).


**IPsec**(Internet Protocol Security)은 통신 세션의 각 IP패킷을 암호화하고 인증하는 안전한 [인터넷 프로토콜](../Page/인터넷_프로토콜.md "wikilink")(IP) 통신을 위한 인터넷 [프로토콜 스위트이다](../Page/인터넷_프로토콜_스위트.md "wikilink"). 이 보안은 통신 세션의 개별 [IP 패킷을](https://ko.wikipedia.org/wiki/IP_패킷 "wikilink") [인증](../Page/인증.md "wikilink")하고 [암호화](../Page/암호화.md "wikilink")함으로써 처리된다. IPsec은 세션의 시작에서 에이전트들 사이에서 상호 인증을 확립하거나 세션을 맺는 중에 사용될 암호화 키의 협상을 위한 프로토콜을 포함한다. IPsec은 호스트 한쌍 사이(Host와 host), 보안 게이트웨이 사이(네트워크와 네트워크), 보안 게이트웨이와 호스트 사이(네트워크와 호스트)에 데이터 흐름을 보호하기 위해 사용된다. Internet Protocol security (IPsec)은 Internet Protocol 네트워크 사이에 통신을 지키기 위해 암호의 보안 서비스를 사용한다.

## 보안 구조

IPsec 스위트는 [개방형 표준이다](../Page/개방형_표준.md "wikilink"). IPsec는 다음의 [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")을 사용하여 다양한 기능들을 수행한다:\[1\]\[2\]

  - 인증 헤더(AH)
  - 보안 페이로드 캡슐화 (ESP)
  - 보안 연관 (SA)

## 동작 방식

  - 전송 모드(Transport mode)
  - 터널 모드(Tunnel mode)

## 암호화 알고리즘

  - [HMAC](https://ko.wikipedia.org/wiki/HMAC "wikilink")-[SHA-1](https://ko.wikipedia.org/wiki/SHA-1 "wikilink")
  - [HMAC](https://ko.wikipedia.org/wiki/HMAC "wikilink")-[SHA-2](../Page/SHA-2.md "wikilink")
  - [Triple DES](https://ko.wikipedia.org/wiki/Triple_DES "wikilink")-[CBC](../Page/블록_암호_운용_방식.md "wikilink")
  - [AES](../Page/고급_암호화_표준.md "wikilink")-CBC
  - [AES](../Page/고급_암호화_표준.md "wikilink")-GCM

더 자세한 정보는 RFC 4835 를 참조.

## 참조

<references />

## 같이 보기

  - [정보 보안](../Page/정보_보안.md "wikilink")

## 외부 링크

  -
[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:네트워크 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_계층_프로토콜 "wikilink") [분류:암호 프로토콜](https://ko.wikipedia.org/wiki/분류:암호_프로토콜 "wikilink") [분류:가상사설망](https://ko.wikipedia.org/wiki/분류:가상사설망 "wikilink")

1.  RFC 2411
2.  RFC 4308