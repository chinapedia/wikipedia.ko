> This article is converted from Wikipedia: [AMQP](https://ko.wikipedia.org/wiki/AMQP).


**AMQP**(Advanced Message Queuing Protocol, 어드밴스트 메시지 큐잉 프로토콜)는 [메시지 지향 미들웨어를](../Page/메시지_지향_미들웨어.md "wikilink") 위한 [개방형 표준](../Page/개방형_표준.md "wikilink") [응용 계층](../Page/응용_계층.md "wikilink") 프로토콜이다. AMQP의 정의 기능들은 메시지 지향, 큐잉, 라우팅(P2P 및 [발행-구독](../Page/발행-구독_모델.md "wikilink")), 신뢰성, 보안이다.\[1\]

AMQP는 메시징 제공자와 클라이언트의 동작에 대해 각기 다른 벤더들의 구현체가 상호 운용될 수 있는 정도로까지 권한을 주며, 이는 SMTP, HTTP, FTP 등이 상호 운용이 가능한 시스템을 만든다는 점에서 동일하다. 과거의 [미들웨어](../Page/미들웨어.md "wikilink") 표준들은 API 레벨(예: [JMS](../Page/자바_메시지_서비스.md "wikilink"))에서 등장하였으며 여러 구현체 간 상호 운용성을 제공하지 않고 각기 다른 미들웨어 구현체와의 프로그래머 통신을 표준화하는데 초점을 두었다.\[2\] API, 그리고 메시징 구현체가 제공해야 하는 행위의 모임을 정의하는 JMS와는 달리 AMQP는 [와이어 레벨 프로토콜이다](https://ko.wikipedia.org/wiki/와이어_프로토콜 "wikilink"). 와이어 레벨 프로토콜은 [바이트](../Page/옥텟_\(컴퓨팅\).md "wikilink") 스트림으로 네트워크를 경유하며 송신되는 데이터의 형식을 기술한다. 그러므로 이러한 데이터 형식을 따르는 메시지를 만들고 해석할 수 있는 도구라면 구현 언어에 관계 없이 다른 호환 도구와 상호 운용이 가능하다.

## 역사

AMQP의 아이디어는 2003년 [런던](../Page/런던.md "wikilink") [JP모간 체이스의](../Page/JP모간_체이스.md "wikilink") John O'Hara에 의해 추진되었다.\[3\]

## 같이 보기

  - [P2P](../Page/P2P.md "wikilink")
  - [메시지 큐](https://ko.wikipedia.org/wiki/메시지_큐 "wikilink")
  - [메시지 큐잉 서비스](https://ko.wikipedia.org/wiki/메시지_큐잉_서비스 "wikilink")

## 각주

## 외부 링크

  - [AMQP website](https://web.archive.org/web/20110720093016/http://www.amqp.org/)
  - [OASIS AMQP technical committee](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=amqp)
  - [High-level Overview of AMQP and the AMQP Model (version 0-9-1)](http://www.rabbitmq.com/tutorials/amqp-concepts.html)

[분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:프로세스 간 통신](https://ko.wikipedia.org/wiki/분류:프로세스_간_통신 "wikilink") [분류:메시지 지향 미들웨어](https://ko.wikipedia.org/wiki/분류:메시지_지향_미들웨어 "wikilink") [분류:미들웨어](https://ko.wikipedia.org/wiki/분류:미들웨어 "wikilink") [분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink") [분류:개방형 표준](https://ko.wikipedia.org/wiki/분류:개방형_표준 "wikilink")

1.
2.
3.