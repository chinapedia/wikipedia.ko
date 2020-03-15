> This article is converted from Wikipedia: [Little Snitch](https://ko.wikipedia.org/wiki/Little_Snitch).


**Little Snitch**는 [오스트리아](https://ko.wikipedia.org/wiki/오스트리아 "wikilink")의 Objective Development 에서 개발하는 [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")에서 사용되는 [소프트웨어 방화벽이다](https://ko.wikipedia.org/wiki/방화벽_\(네트워킹\)#소프트웨어_방화벽 "wikilink"). Little Snitch는 애플리케이션의 네트워크 상태를 모니터링 하며, 방화벽 규칙에 따라 붙어있는 네트워크의 연결을 거부하거나 허락한다.

상태 기반 방화벽과 달리, Little Snitch는 들어오는 트래픽으로부터의 공격으로부터 시스템을 보호하도록 본질적으로 설계되어 있으며, 나가는 트래픽을 제한하여 프라이버시를 보호하도록 되어 있기도 하다.\[1\] Little Snitch는 이를 위해 서명된 [커널 확장을](../Page/적재_가능_커널_모듈.md "wikilink") 사용하여 애플 사에서 제공한 공식 [API를](https://ko.wikipedia.org/wiki/응용_프로그램_프로그래밍_인터페이스 "wikilink") 사용하고 있다.\[2\]

애플리케이션이나 프로세스에서 네트워크 연결을 수립하게 되면, Little Snitch 측에서는 이 연결을 보호하게 된다. 그리고 창을 통해 이 연결을 거부할 것인지 혹은 허가할것인지 등의 결정을 사용자가 결정하게 된다. 이 창에서 사용자는 연결 하나만 제한하거나 혹은 특정 포트, 프로토콜 혹은 도메인 전체에 제약을 걸수 있다.

## 참고 문헌

[분류:방화벽 소프트웨어](https://ko.wikipedia.org/wiki/분류:방화벽_소프트웨어 "wikilink") [분류:macOS 소프트웨어](https://ko.wikipedia.org/wiki/분류:macOS_소프트웨어 "wikilink")

1.  [Objective Development. Main page.](https://www.obdev.at/products/littlesnitch/index.html)
2.