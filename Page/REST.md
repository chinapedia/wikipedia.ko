> This article is converted from Wikipedia: [REST](https://ko.wikipedia.org/wiki/REST).


**REST**(Representational State Transfer)는 [월드 와이드 웹과](../Page/월드_와이드_웹.md "wikilink") 같은 분산 [하이퍼미디어](https://ko.wikipedia.org/wiki/하이퍼미디어 "wikilink") 시스템을 위한 [소프트웨어 아키텍처의](https://ko.wikipedia.org/wiki/소프트웨어_아키텍처 "wikilink") 한 형식이다. 이 용어는 로이 필딩(Roy Fielding)의 2000년 박사학위 논문에서 소개되었다. 필딩은 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")의 주요 저자 중 한 사람이다. 이 개념은 네트워킹 문화에 널리 퍼졌다.

엄격한 의미로 **REST**는 네트워크 아키텍처 원리의 모음이다. 여기서 '네트워크 아키텍처 원리'란 자원을 정의하고 자원에 대한 주소를 지정하는 방법 전반을 일컫는다. 간단한 의미로는, 웹 상의 자료를 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")위에서 [SOAP](https://ko.wikipedia.org/wiki/SOAP "wikilink")이나 쿠키를 통한 세션 트랙킹 같은 별도의 전송 계층 없이 전송하기 위한 아주 간단한 인터페이스를 말한다. 이 두 가지의 의미는 겹치는 부분과 충돌되는 부분이 있다. 필딩의 **REST** 아키텍처 형식을 따르면 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")나 [WWW](https://ko.wikipedia.org/wiki/WWW "wikilink")이 아닌 아주 커다란 소프트웨어 시스템을 설계하는 것도 가능하다. 또한, [리모트 프로시저 콜](https://ko.wikipedia.org/wiki/리모트_프로시저_콜 "wikilink") 대신에 간단한 [XML](https://ko.wikipedia.org/wiki/XML "wikilink")과 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink") 인터페이스를 이용해 설계하는 것도 가능하다.

필딩의 **REST** 원리를 따르는 시스템은 종종 RESTful이란 용어로 지칭된다. 열정적인 REST 옹호자들은 스스로를 RESTafrians 이라고 부른다.

## 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:Roy_Fielding_at_OSCON_2008.jpg "wikilink") [로이 필딩](https://ko.wikipedia.org/wiki/로이_필딩 "wikilink")(Roy Fielding)은 2000년에 [UC 어바인에서](https://ko.wikipedia.org/wiki/캘리포니아_대학교_어바인 "wikilink") "Architectural Styles and the Design of Network-based Software Architectures"라는 제목의 2000년 박사 학위 논문에 REST를 정의하였다.\[1\] 그는 1996년부터 1999년까지 HTTP 1.0의 기존 디자인에 기반을 둔 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink") 1.1와 병행하여 REST 구조의 스타일을 개발하였다.\[2\]

## 원리

### REST 아키텍처에 적용되는 6가지 제한 조건

다음 제한 조건을 준수하는 한 개별 컴포넌트는 자유롭게 구현할 수 있다.

  - [클라이언트/서버 구조](https://ko.wikipedia.org/wiki/:en:Client%E2%80%93server "wikilink"): 일관적인 인터페이스로 분리되어야 한다
  - [무상태(Stateless)](https://en.wikipedia.org/wiki/Stateless_server): 각 요청 간 클라이언트의 콘텍스트가 서버에 저장되어서는 안 된다
  - [캐시 처리 가능(Cacheable)](https://ko.wikipedia.org/wiki/웹_캐시 "wikilink"): WWW에서와 같이 클라이언트는 응답을 캐싱할 수 있어야 한다.
      - 잘 관리되는 캐싱은 클라이언트-서버 간 상호작용을 부분적으로 또는 완전하게 제거하여 scalability와 성능을 향상시킨다.
  - [계층화(Layered System)](https://en.wikipedia.org/wiki/Layered_system): 클라이언트는 보통 대상 서버에 직접 연결되었는지, 또는 중간 서버를 통해 연결되었는지를 알 수 없다. 중간 서버는 [로드 밸런싱](https://ko.wikipedia.org/wiki/로드_밸런싱 "wikilink") 기능이나 [공유 캐시](https://ko.wikipedia.org/wiki/공유_캐시 "wikilink") 기능을 제공함으로써 시스템 규모 확장성을 향상시키는 데 유용하다.
  - [Code on demand (optional)](https://en.wikipedia.org/wiki/Client-side_scripting) - 자바 애플릿이나 자바스크립트의 제공을 통해 서버가 클라이언트가 실행시킬 수 있는 로직을 전송하여 기능을 확장시킬 수 있다.
  - 인터페이스 일관성: 아키텍처를 단순화시키고 작은 단위로 분리(decouple)함으로써 클라이언트-서버의 각 파트가 독립적으로 개선될 수 있도록 해준다..

### REST 인터페이스의 원칙에 대한 가이드

#### 자원의 식별

요청 내에 기술된 개별 자원을 식별할 수 있어야 한다. 웹 기반의 REST 시스템에서의 [URI](https://ko.wikipedia.org/wiki/URI "wikilink")의 사용을 예로 들 수 있다. 자원 그 자체는 클라이언트가 받는 문서와는 개념적으로 분리되어 있다. 예를 들어, 서버는 데이터베이스 내부의 자료를 직접 전송하는 대신, 데이터베이스 레코드를 HTML, XML이나 JSON 등의 형식으로 전송한다.

#### 메시지를 통한 리소스의 조작

클라이언트가 어떤 자원을 지칭하는 메시지와 특정 메타데이터만 가지고 있다면 이것으로 서버 상의 해당 자원을 변경·삭제할 수 있는 충분한 정보를 가지고 있는 것이다.

#### 자기서술적 메시지

각 메시지는 자신을 어떻게 처리해야 하는지에 대한 충분한 정보를 포함해야 한다. 예를 들어 MIME type과 같은 인터넷 미디어 타입을 전달한다면, 그 메시지에는 어떤 파서를 이용해야 하는지에 대한 정보도 포함해야 한다. 미디어 타입만 가지고도, 클라이언트는 어떻게 그 내용을 처리해야할 지 알 수 있어야 한다. 메시지를 이해하기 위해 그 내용까지 살펴봐야 한다면, 그 메시지는 자기서술적이 아니다. 예를 들어, 단순히 "application/xml"이라는 미디어 타입은, 실제 내용을 다운로드 받지 않으면 그 메시지만 가지고는 무엇을 해야할지에 대해 충분히 알려주지 못한다.

#### 애플리케이션의 상태에 대한 엔진으로서 하이퍼미디어

만약에 클라이언트가 관련된 리소스에 접근하기를 원한다면, 리턴되는 지시자에서 구별될 수 있어야 한다. 충분한 콘텍스트 속에서의 URI를 제공해주는 하이퍼텍스트 링크의 예를 들 수 있겠다.

### REST 의 주요한 목표

  - 구성 요소 상호작용의 규모 확장성(scalability of component interactions)
  - 인터페이스의 범용성 (Generality of interfaces)
  - 구성 요소의 독립적인 배포(Independent deployment of components)
  - 중간적 구성요소를 이용해 응답 지연 감소, 보안을 강화, 레거시 시스템을 인캡슐레이션 (Intermediary components to reduce latency, enforce security and encapsulate legacy systems)

## 같이 보기

  - [원격 프로시저 호출](https://ko.wikipedia.org/wiki/원격_프로시저_호출 "wikilink")
  - [XML-RPC](https://ko.wikipedia.org/wiki/XML-RPC "wikilink")/[JSON-RPC](../Page/JSON-RPC.md "wikilink")
  - [SOAP](https://ko.wikipedia.org/wiki/SOAP "wikilink")
  - [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")

## 각주

## 외부 링크

  -
<!-- end list -->

  -
<!-- end list -->

  -
[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink")

1.
2.