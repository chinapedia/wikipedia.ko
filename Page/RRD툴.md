> This article is converted from Wikipedia: [RRD](https://ko.wikipedia.org/wiki/RRD).


**RRD툴**(, )은 시간에 따른 자료를 다룰 수 있는 도구이다. 그림 형식으로 시각화 해주는 기능도 있다.

[MRTG](https://ko.wikipedia.org/wiki/MRTG "wikilink")를 모방해 일반화 하여 개발한 도구이며 자료 수집에 관한 일부분이 빠져 완전한 대체물은 아니지만, 네트워크 모니터링 분야에서 매우 인기있는 도구이다.

[펄](../Page/펄.md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"), [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink"), [Tcl](../Page/Tcl.md "wikilink"), [PHP](../Page/PHP.md "wikilink")를 지원한다.

기본적으로 유닉스/리눅스에서 작동하지만 윈도용도 일부 버전을 지원한다. 공식적으로는 이진파일 없이 소스코드만 배포한다.

## 라운드 로빈 데이터베이스

**라운드 로빈 데이터베이스**(Round Robin Database, RRD)는 Tobias Oetiker에 의해 제작되었으며 현재는 전 세계의 수많은 사람들의 참여로 진행되고 있는 오픈 소스 기반의 소프트웨어이다. Round Robin은 고정된 크기의 데이터와 현재 element에 대한 포인터로 동작하는 기술로 현재 데이터를 읽고 쓸 때 포인터는 다음 element로 이동하게 된다. 시작과 끝이 없는 원과 같이, Round Robin 기술을 사용하면 계속해서 데이터를 읽고 쓰는 작업이 가능하다. 사용하는 중에도 모든 가용 위치에 대한 사용이 가능하며, 자동적으로 이전의 위치에 대한 재사용이 가능하다. 이러한 방법으로 데이터베이스는 크기는 증가하지 않지만 어떠한 인위적인 작업 없이 사용 가능하게 된다.

RRDTool은 이러한 Round Robin 기술을 이용한 데이터베이스를 구현하고 있으며, 데이터의 저장 및 검색이 가능하다. RRDTool에 대해 보충하자면, 일정한 기간 동안 특정 포인트에서의 측정데이터를 취급하기에 유용한 데이터베이스이다. RRDTool은 MRTG(Multi Router Traffic Grapher)에서 유래되었다. MRTG는 인터넷 회선의 사용량을 [SNMP](https://ko.wikipedia.org/wiki/SNMP "wikilink")(Simple Network Management Protocol)를 통해 수집한 정보를 저장하고 수집된 데이터를 스크립트를 이용해 그래프로 표현하는 툴이다. 이에 비해 RRDTool는 좀 더 일반적 데이터인 현재 온도, 속도, 전압 등의 측정 데이터를 수집하여 저장하고 이를 그래프로 표현하는 툴로 알려져있다. RRDTool은 기본적으로 데이터베이스에 대한 생성, 데이터의 저장, 데이터에 대한 검색 그리고 회선에 대한 평균 사용량 및 최대 사용량을 GIR/PNG 그래프로 표현한다.

마지막 업데이트 된 버전으로는 2013년 3월 23일 rrdtool-1.4.8 버전이 발표 되었다..

## 외부 링크

  - [공식 웹사이트](http://oss.oetiker.ch/rrdtool/)

[분류:응용 소프트웨어](https://ko.wikipedia.org/wiki/분류:응용_소프트웨어 "wikilink") [분류:1999년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1999년_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink") [분류:인터넷 프로토콜 기반 네트워크 소프트웨어](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜_기반_네트워크_소프트웨어 "wikilink") [분류:시계열 소프트웨어](https://ko.wikipedia.org/wiki/분류:시계열_소프트웨어 "wikilink")