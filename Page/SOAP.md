> This article is converted from Wikipedia: [SOAP](https://ko.wikipedia.org/wiki/SOAP).


[섬네일](https://ko.wikipedia.org/wiki/파일:SOAP.svg "wikilink") **SOAP**(Simple Object Access Protocol)은 일반적으로 널리 알려진 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink"), [HTTPS](https://ko.wikipedia.org/wiki/HTTPS "wikilink"), [SMTP](https://ko.wikipedia.org/wiki/SMTP "wikilink") 등을 통해 [XML](https://ko.wikipedia.org/wiki/XML "wikilink") 기반의 메시지를 컴퓨터 네트워크 상에서 교환하는 [프로토콜이다](https://ko.wikipedia.org/wiki/통신_프로토콜 "wikilink"). SOAP은 [웹 서비스에서](https://ko.wikipedia.org/wiki/웹_서비스 "wikilink") 기본적인 메시지를 전달하는 기반이 된다. SOAP에는 몇가지 형태의 메시지 패턴이 있지만, 보통의 경우 원격 프로시져 호출(Remote Procedure Call:RPC) 패턴으로, 네트워크 노드(클라이언트)에서 다른 쪽 노드(서버)쪽으로 메시지를 요청 하고, 서버는 메시지를 즉시 응답하게 된다. SOAP는 XML-RPC와 WDDX에서 envelope/header/body로 이루어진 구조와 전송(transport)과 상호 중립성(interaction neutrality)의 개념을 가져왔다.

**SOAP**은 XML을 근간으로 헤더와 바디를 조합하는 디자인 패턴으로 설계되어 있다. 「헤더」는 선택사항으로 반복이나 보안 및 트랜잭션을 정보로 하는 메타 정보를 가지고 있다. 「바디」부분은 주요한 정보인 정보를 가지고 있다.

## 역사

**SOAP**는 'Simple Object Access Protocol'의 약어이지만, 버전 1.2부터는 그 의미가 퇴색되었다. 2003년 6월 24일, W3C에서 버전 1.2 권고안이 나왔으며, [서비스 지향 아키텍처](../Page/서비스_지향_아키텍처.md "wikilink")(SOA:Service-oriented architecture)와 그 의미가 종종 혼용된다. 그러나 엄연히 SOAP와 SOA는 다르다. SOAP는 데이브 위너(Deabe Winer), 돈 박스(Don Box), 밥 액킨슨(Bob Atkinson) 그리고 모슨 얼 고세인(Mohsen Al-Ghosein) 등이 1998년 액킨슨과 얼 고세인이 그 당시 일하고 있던 마이크로소프트의 후원으로 객체 접근 규약(Object Access Protocol)로서 처음으로 디자인했다. SOAP의 표준화 작업은 현재 [W3C](https://ko.wikipedia.org/wiki/W3C "wikilink")의 [XML protocol Working Group이](https://ko.wikipedia.org/wiki/XML_protocol_Working_Group "wikilink") 관리하고 있다.

## 전송 방식

**SOAP**는 인터넷 애플리케이션 계층에 있는 프로토콜을 전송계층의 프로토콜로 사용할 수 있게 만든다. 혹자는 이러면 프로토콜의 의도된 목적과 역할이 맞지 않아 부정 이용이 된다고 비판하지만, SOAP의 지지자들은 [터널링](https://ko.wikipedia.org/wiki/터널링 "wikilink")을 위한 다양한 계층(level)에 쓰이고 있는 다른 프로토콜들과 비슷하다고 말하고 있다. [SMTP](https://ko.wikipedia.org/wiki/SMTP "wikilink")와 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")에서 애플리케이션 계층 프로토콜로 트랜스포트 계층의 역할을 대신하는 것이 SOAP의 올바른 이용이라 할 수 있으나, [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")는 오늘날 인터넷 인프라와 매우 잘 동작하여 더욱 폭넓은 지원을 가능하게 한다. 특히나, HTTP는 방화벽이 작동하는 네트워크 안에서도 문제 없이 작동한다. SOAP는 [HTTPS](https://ko.wikipedia.org/wiki/HTTPS "wikilink")(애플리케이션 계층에서는 HTTP와 동일하나 트랜스포트 계층 아래에서는 암호화됨)에서도 간략하게 또는 상호적으로 사용된다.

이는 [WS-I](https://ko.wikipedia.org/wiki/WS-I "wikilink")방식으로 [Basic Profile](https://ko.wikipedia.org/wiki/Basic_Profile "wikilink") 1.1에서 서술된 것과 같이 웹 서비스의 보안을 제공하고 있다. 이 점은, [GIOP](https://ko.wikipedia.org/wiki/GIOP "wikilink")/[IIOP](https://ko.wikipedia.org/wiki/IIOP "wikilink") 혹은 [DCOM](https://ko.wikipedia.org/wiki/DCOM "wikilink") 등과 같은 방화벽에서 쉽게 필터링 당하는 여타의 배포 프로토콜등과의 비교 우위를 점하고 있다.

## 메시지 형식

[XML](https://ko.wikipedia.org/wiki/XML "wikilink")은 대다수 회사들과 오픈 소스 개발 진영의 노력에 힘입어 광범위하게 사용되는 메시지 형식이므로 표준으로 선택되었다. 게다가 광범위하게 무료로 사용 가능한 툴이 상당수 포진하고 있는 점은 SOAP-기반 구현으로 옮겨가기 쉽게 하였다. XML의 문법은 다소 긴데, 이에는 장단점이 있다. 사람이 쉽게 읽을 수 있는 반면, 불필요한 정보때문에 처리속도가 늦어질 수 있다. [CORBA](https://ko.wikipedia.org/wiki/CORBA "wikilink"), [GIOP](https://ko.wikipedia.org/wiki/GIOP "wikilink"), [ICE](https://ko.wikipedia.org/wiki/ICE "wikilink"), [DCOM](https://ko.wikipedia.org/wiki/DCOM "wikilink")은 이진 메시지 포맷을 사용하므로 전송량이 훨씬 적다. 그러나 XML 메시지 처리는 하드웨어로 빠르게 할 수 있다.\[1\]\[2\] [이진 XML은](https://ko.wikipedia.org/wiki/이진_XML "wikilink") 스트리밍 전송에 대한 대안으로 (속도를 높이는 수단으로) 검토되고 있다.

## 장단점 비교

다양한 비평자들과 전문가들이 기술적인 대안과 the context of its intended use에 대하여 SOAP의 기술적인 장단점들에 대한 토의가 있어왔다.

### 장점

  - SOAP을 사용한 HTTP는 기존 원격 기술들에 비해서 프록시와 방화벽에 구애받지 않고 쉽게 통신 가능하다.
  - SOAP은 융통성있게도 각각 다른 트랜스포트 프로토콜들의 사용을 허용하고 있다. 표준 스택에서는 트랜스 포트 프로토콜로 HTTP를 사용하지만, 다른 프로토콜 역시 사용가능 하다.
  - SOAP은 플랫폼 독립적이다.
  - SOAP은 프로그래밍 언어에 독립적이다.
  - SOAP은 확장가능하다.

분산환경 하에서 정보교환을 하기 위한 하나의 프로토콜인 SOAP은 다음과 같은 장점을 가지고 있다(안현수, 2003).

1.  SOAP은 전송(Transport) 매체로서 HTTP를 사용하기 때문에 인터넷에서 널리 사용할 수 있다. 실제로 SOAP은 인터넷에서 원격 객체를 액세스하기 위해 고안된 프로토콜이다.
2.  SOAP은 HTTP와 XML을 사용하기 때문에 개발도구나 플랫폼에 구애받지 않고 SOAP 서버 혹은 클라이언트를 개발할 수 있다. 이처럼 SOAP 서버 혹은 클라이언트를 보다 쉽게 개발할 수 있도록 해주는 COM 컴포넌트, 유틸리티 등으로 구성된 SOAP 툴킷(toolkit)도 제공되고 있다. 또한 HTTP와 XML이 갖는 장점을 모두 포함하면서 컴포넌트의 상호운용성을 높일 수도 있다.
3.  SOAP은 컴포넌트를 활성화하는 방법이나 호출하는 방법에 대해 전혀 관여하지 않으며 이에 대한 상세한 사항은 HTTP Request를 수신하는 수신자에게 위임하고 있다. 따라서 객체지향기술이나 컴포넌트 기술을 사용하지 않는 애플리케이션일지라도 SOAP을 통해 객체서비스를 제공하거나 제공받을 수가 있다.\[3\]

### 단점

  - XML 포맷은 태그 형태로 보내기 때문에 [CORBA](https://ko.wikipedia.org/wiki/CORBA "wikilink")같은 미들웨어 기술과 비교해서 상대적으로 느리다. 이것은 전송할 메시지가 적을때에는 문제 되지 않을 수 있다. 성능을 향상시키기 위해서 바이너리 객체를 포함시킨 특별한 경우의 XML(바이너리 XML을 말하는듯)로 메시지 전송 최적화 메커니즘(Message Transmission Optimization Mechanism; [MTOM](https://ko.wikipedia.org/wiki/MTOM "wikilink"))이 나왔다. 게다가 일반적인 XML의 성능을 향상시키기 위해, VTD-XML과 같은 emerging non-extractiv XML 처리 모델이 있다.

## SOAP 샘플

``` xml
 <SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
 <SOAP-ENV:Body>
 <getProductDetails ns="http://warehouse.example.com/ws">
 <productId>827635</productId>
 </getProductDetails>
 </SOAP-ENV:Body>
 </SOAP-ENV:Envelope>
```

## 각주

<references/>

## 참고 자료

  - [W3C SOAP 페이지](http://www.w3.org/TR/soap/)

[분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:데이터 직렬화 포맷](https://ko.wikipedia.org/wiki/분류:데이터_직렬화_포맷 "wikilink")

1.  [IBM 데이터파워](http://www-306.ibm.com/software/integration/datapower/xa35/)
2.  [IBM 취리히 XML 가속 엔진](http://www.research.ibm.com/XML/IBM_Zurich_XML_Accelerator_Engine_paper_2004May04.pdf)
3.  이수상, 디지털도서관 운영론. 서울: 한국도서관 협회. 2013. P.281