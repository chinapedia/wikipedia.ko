> This article is converted from Wikipedia: [MQTT](https://ko.wikipedia.org/wiki/MQTT).


**MQTT**\[1\](메시지 큐잉 텔레메트리 트랜스포트, Message Queuing Telemetry Transport)는 [ISO 표준](../Page/국제_표준화_기구.md "wikilink")(ISO/IEC PRF 20922)\[2\] [발행-구독](../Page/발행-구독_모델.md "wikilink") 기반의 메시징 프로토콜이다. [TCP/IP 프로토콜](../Page/인터넷_프로토콜_스위트.md "wikilink") 위에서 동작한다. "작은 코드 공간"(small code footprint)이 필요하거나 네트워크 대역폭이 제한되는 원격 위치와의 연결을 위해 설계되어 있다. [발행-구독 메시징 패턴은](../Page/발행-구독_모델.md "wikilink") [메시지 브로커가](../Page/메시지_브로커.md "wikilink") 필요하다.

[IBM](../Page/IBM.md "wikilink")의 [앤디 스탠퍼드 클락과](https://ko.wikipedia.org/wiki/앤디_스탠퍼드_클락 "wikilink") 시러스 링크의 알렌 니퍼(Arlen Nipper)가 1999년 이 프로토콜의 최초 버전을 만들었다.\[3\]

2013년, IBM은 MQTT v3.1을 [OASIS](../Page/OASIS_\(기관\).md "wikilink") 표준화 단체에 제출하였다.\[4\] MQTT-SN\[5\]은 [직비](../Page/직비.md "wikilink")와 같은 비 TCP/IP 네트워크의 임베디드 장치에 초점을 둔 메인 프로토콜의 일종이다.

역사적으로, MQTT의 MQ는 [IBM 웹스피어 MQ](../Page/IBM_웹스피어_MQ.md "wikilink")(당시 'MQSeries') [메시지 큐](https://ko.wikipedia.org/wiki/메시지_큐 "wikilink") 제품 계열에서 비롯된 것이다.\[6\] 그러나 모든 상황에서 표준 기능으로서 큐잉 그 자체를 지원하는 것은 필수가 아니다.\[7\]

## 메시지 유형

### 연결하기

[섬네일](https://ko.wikipedia.org/wiki/파일:MQTT_protocol_example_without_QoS.svg "wikilink") 서버와의 연결 수립을 기다린 다음 노드 간 링크를 만든다.

### 연결 끊기

MQTT 클라이언트가 해야 할 일을 기다리고 [인터넷 프로토콜 스위트](../Page/인터넷_프로토콜_스위트.md "wikilink") 세션의 연결이 끊어지기를 기다린다.

### 발행하기

MQTT 클라이언트에 요청이 전달된 직후 애플리케이션 스레드에 즉시 반환한다.

## 서비스 품질 (QoS)

브로커에 대한 각 연결은 QoS 기준을 지정할 수 있다. 부하가 늘어나는 순서에 따라 다음과 같이 분류된다:

  - 최대 한 차례 - 메시지는 한 번만 보내면 클라이언트와 브로커는 전달 확인 응답을 위한 추가 단계를 밟지 않는다. (보낸 다음 잊어버림)
  - 최소 한 차례 - 메시지는 확인 응답을 수신할 때까지 여러 번 송신자로부터 재시도된다. (확인 응답을 거치는 전달)
  - 정확히 한 번 - 송신자와 수신자는 2단계 핸드셰이크에 참여함으로써 오직 하나의 메시지 사본만을 수신하는 것을 보장한다. (보장된 전달)\[8\]

이 필드는 기반이 되는 TCP 데이터 전송의 처리에 영향을 주지 않으며, MQTT 송신자와 수신자 간에만 사용된다.

## 같이 보기

  - [RabbitMQ](../Page/RabbitMQ.md "wikilink")
  - [AMQP](../Page/AMQP.md "wikilink")

## 각주

## 외부 링크

  -
[분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:데이터 전송](https://ko.wikipedia.org/wiki/분류:데이터_전송 "wikilink") [MQ](https://ko.wikipedia.org/wiki/분류:IBM_웹스피어 "wikilink") [분류:메시지 지향 미들웨어](https://ko.wikipedia.org/wiki/분류:메시지_지향_미들웨어 "wikilink") [분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.