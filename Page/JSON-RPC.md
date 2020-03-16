> This article is converted from Wikipedia: [JSON-RPC](https://ko.wikipedia.org/wiki/JSON-RPC).


**JSON-RPC**는 [JSON](../Page/JSON.md "wikilink")으로 인코딩된 [원격 프로시저 호출이다](../Page/원격_프로시저_호출.md "wikilink"). 매우 간단한 프로토콜([XML-RPC](../Page/XML-RPC.md "wikilink")와 매우 흡사함)로서, 소량의 데이터 타입과 명령들만을 정의하고 있다. JSON-RPC는 알림(notification, 서버로 데이터가 전송되고 응답을 요구하지 않음)을 허용하며, 다수의 호출이 서버로 전송되고 순서없이 응답되는 것을 허용한다.

## 사용

JSON-RPC는 이 프로토콜을 구현하는 서버로 요청을 보내는 것에 의해 동작한다. 이 때 클라이언트는 통상 리모트 시스템의 메소드 하나를 호출하려는 소프트웨어이다. 다수의 입력 파라미터가 배열 혹은 객체의 형태로 리모트 메소드로 전달될 수 있고, 메소드 자신은 다수의 출력 데이터를 마찬가지로 리턴할 수 있다. (구현 버전에 따라 다르다.)

하나의 리모트 메소드는 [HTTP](../Page/HTTP.md "wikilink") 혹은 [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink") 소켓 (버전 2.0으로 시작하는)을 사용해 리모트 서비스로 요청을 보내는 것에 의해 호출된다. HTTP를 사용할 때는 [content-type이](https://ko.wikipedia.org/wiki/MIME#Content-Type "wikilink") `application/json`.\[1\]로 정의될 수도 있다.

모든 전송 타입은 JSON을 사용해 직렬화한 단일 객체이다.\[2\] 하나의 요청은 리모트 시스템에 의해 제공되는 특정한 메소드에 대한 호출이다. 이는 다음 3가지의 속성을 포함해야 한다:

  - `method` - 호출될 메소드의 이름 문자열.
  - `params` - 정의된 메소드에 대한 파라미터로서 전달될 객체들의 배열.
  - `id` - 임의 타입의 값. 이것은 요청에 대해 대응되는 응답을 매치시킨다.

요청의 수신자는 모든 수신된 요청에 대해 유효한 응답으로 답해야 한다. 응답은 아래에서 언급한 속성 들을 포함해야 한다.

  - `result` - 호출된 메소드에 의해 반환되는 데이터. 메소드 호출 중 에러가 발생했다면, 이 값은 null이어야 한다.
  - `error` - 메소드 호출 중 에러가 있었으면, 특정한 에러 코드. 아니면`null`.
  - `id` - 응답하는 요청의 id.

응답이 필요없거나 처음부터 요구되지도 않는 상황들이 있기 때문에, 알림(notification)이 도입되었다. 알림은 id가 없는 요청과 유사하다. 응답이 리턴되지 않을 것이기 때문에 id가 필요없는 것이다. 이 경우, `id` 속성은 생략(버전 2.0)되거나 `null`(버전 1.0)이어야 한다.

## 같이 보기

  - [원격 프로시저 호출](../Page/원격_프로시저_호출.md "wikilink") (RPC)
  - [JSON](../Page/JSON.md "wikilink")

## 참고 자료

<references/>

## 외부 링크

  -
  - [JSON-RPC Google Group](http://groups.google.com/group/json-rpc) 이 프로토콜에 관한 토론 주제들

  - [JSON-RPC specifications, links etc.](http://www.simple-is-better.org/json-rpc/)

  - [Official JSON-RPC 1.0 homepage](http://json-rpc.org/) (currently outdated)

[분류:JSON](https://ko.wikipedia.org/wiki/분류:JSON "wikilink") [분류:웹 서비스](https://ko.wikipedia.org/wiki/분류:웹_서비스 "wikilink")

1.  [RFC 4627](https://tools.ietf.org/html/rfc4627)
2.