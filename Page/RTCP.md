> This article is converted from Wikipedia: [RTCP](https://ko.wikipedia.org/wiki/RTCP).


**RTCP**(RTP Control Protocol)는 [실시간 전송 프로토콜](../Page/실시간_전송_프로토콜.md "wikilink")(RTP)의 자매 프로토콜이다. 기본 기능과 패킷 구조는 "RFC 3550"에 정의되어 있다. RTCP는 RTP 세션의 대역 외(out-of-band) 통계 및 제어 정보를 제공한다. 멀티미디어 데이터의 전달, 패키징 시에 RTP와 함께 사용하지만 RTCP가 직접 미디어 데이터를 전송하지는 않는다.

RTCP의 주 기능은 미디어 배급 시 전송되는 [옥텟](../Page/옥텟_\(컴퓨팅\).md "wikilink") 및 패킷 카운트, [패킷 손실](https://ko.wikipedia.org/wiki/패킷_손실 "wikilink"), [패킷 지연 변화](https://ko.wikipedia.org/wiki/패킷_지연_변화 "wikilink"), [왕복 지연 시간](https://ko.wikipedia.org/wiki/왕복_지연_시간 "wikilink") 등의 통계 정보를 스트리밍 멀티미디어 세션 참여자들에게 주기적으로 보냄으로써 [QoS](../Page/QoS.md "wikilink")의 피드백을 제공하는 것이다. 애플리케이션은 이 정보를 사용하여 흐름을 제한하거나 다른 [코덱](../Page/코덱.md "wikilink")을 사용하는 일 등을 수행함으로써 QoS 변수를 통제할 수 있다.

## 패킷 헤더

| 오프셋 | 옥텟 | 0    | 1 | 2  | 3  |
| --- | -- | ---- | - | -- | -- |
| 옥텟  | 비트 | 0    | 1 | 2  | 3  |
|     | 0  | 버전   | P | RC | PT |
|     | 32 | SSRC |   |    |    |
|     |    |      |   |    |    |

RTCP 패킷 헤더

## 표준 문서

  - RFC 3550, Standard 64, *RTP: A Transport Protocol for Real-Time Applications*

## 같이 보기

  - [스트리밍](../Page/스트리밍.md "wikilink")
  - [QoS](../Page/QoS.md "wikilink")
  - [음성 인터넷 프로토콜](../Page/음성_인터넷_프로토콜.md "wikilink")

## 각주

  - 내용주

## 참고 문헌

  -
  -
  -
[분류:스트리밍](https://ko.wikipedia.org/wiki/분류:스트리밍 "wikilink") [분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink")