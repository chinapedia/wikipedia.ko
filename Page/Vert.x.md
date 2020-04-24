> This article is converted from Wikipedia: [Vert.x](https://ko.wikipedia.org/wiki/Vert.x).


**버텍스**(Vert.X)는 이벤트 드리븐(영어: event-driven) 방식의 자바 버추얼 머신(영어: Java Virtual Machine) 위에서 동작하는 어플리케이션 프레임워크이다.

자바스크립트의 Node.js, 파이선의 Twisted, 펄의 Perl Objected Environment, C의 libevent, PHP의 reactPHP 나 amphp 그리고 루비의 EventMachine 등과 비슷하다.

## 예제

"Hello from Vert.x\!"를 서비스하는 웹 서버는 자바로 작성이 가능하다:

``` java
import io.vertx.core.AbstractVerticle;

public class Server extends AbstractVerticle {
  public void start() {
    vertx.createHttpServer().requestHandler(req -> {
      req.response()
        .putHeader("content-type", "text/plain")
        .end("Hello from Vert.x!");
    }).listen(8080);
  }
}
```

[자바스크립트](../Page/자바스크립트.md "wikilink")로는 다음과 같다:

``` javascript
vertx.createHttpServer()
  .requestHandler(function (req) {
    req.response()
      .putHeader("content-type", "text/plain")
      .end("Hello from Vert.x!");
}).listen(8080);
```

## 특징

1.  Scale: 버텍스는 이벤트 드리븐(\[1\]), 논 블럭킹(non blocking) 방식이다. 이로써 적은 커널 쓰레드를 사용하여 여러 동시성을 확보할수 있다.
2.  Polyglot: Java, JavaScript, Groovy, Ruby, Ceylon, Scala, Kotlin 등의 여러 언어에서 사용가능하다.

## 각주

## 외부 링크

  - <http://vertx.io/>

[분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:자바 가상 머신](https://ko.wikipedia.org/wiki/분류:자바_가상_머신 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.  event driven