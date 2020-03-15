> This article is converted from Wikipedia: [CFosSpeed](https://ko.wikipedia.org/wiki/CFosSpeed).


**cFosSpeed**는 cFos Software GmbH에서 개발한 [트래픽 셰이핑](https://ko.wikipedia.org/wiki/트래픽_셰이핑 "wikilink") 소프트웨어이다. [윈도용으로](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 개발되었으며 데이터 전송량을 유지하면서도 데이터 트래픽을 최적화시킴으로써 넷망 응답 지연 시간(latency)을 개선시키는데 효과가 있다. 개별의 윈도 네트워크 장치 드라이버를 제공함으로써 패킷 검사(packet inspection)와 layer-7 프로토콜(protocol) 분석을 실행한다. 특히 온라인 게임 및 [VoIP](https://ko.wikipedia.org/wiki/VoIP "wikilink") 사용자들에게 유용한 프로그램이다.

## 작동 원리

이 소프트웨어는 데이터 패킷을 나눠서 각각 다른 트래픽 클래스에 할당시킨다. 이것은 사용자가 직접 설정한 필터링에 따라서 이루어진다. 이로인해 원하는 프로그램이름, layer-7protocol, [TCP](https://ko.wikipedia.org/wiki/TCP "wikilink") 혹은 [UDP](https://ko.wikipedia.org/wiki/UDP "wikilink") 포트, [DSCP](https://ko.wikipedia.org/wiki/DSCP "wikilink") 태그 등 수많은 방법을 사용해서 데이터 트래픽 할당량 우선순위를 정할 수 있다.

## 외부 링크

  - [공식 웹사이트](http://www.cfos.de/en/cfosspeed/cfosspeed.htm)

[분류:네트워크 소프트웨어](https://ko.wikipedia.org/wiki/분류:네트워크_소프트웨어 "wikilink")