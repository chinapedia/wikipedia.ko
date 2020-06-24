> This article is converted from Wikipedia: [ABAP](https://ko.wikipedia.org/wiki/ABAP).


[섬네일](https://ko.wikipedia.org/wiki/파일:abap1.jpg "wikilink") **ABAP** (**A**dvanced **B**usiness **A**pplication **P**rogramming, originally **A**llgemeiner **B**erichts-**A**ufbereitungs-**P**rozessor = general report creation processor)는 협업 비즈니스 솔루션 회사 [SAP AG가](https://ko.wikipedia.org/wiki/SAP_AG "wikilink") 개발한 [고급 프로그래밍 언어이다](../Page/고급_프로그래밍_언어.md "wikilink"). 고급 비즈니스 응용 프로그램을 만드는 언어이기도 하다.

## 개요

ABAP이라는 프로그래밍 언어는 4세대 언어로, 기존의 3세대 언어 C나 C++, JAVA 보다 자연어에 더 가깝다. 이 언어는 SAP사에서 제공하는 [ERP 소프트웨어인](https://ko.wikipedia.org/wiki/전사적_자원_관리 "wikilink") [SAP R/3](https://ko.wikipedia.org/wiki/SAP_R/3 "wikilink") 시스템을 회사에 맞게 구축하는 데 쓰이는 SAP R/3에 기반을 둔 언어이다. 오른쪽의 그림은 SAP R/3 시스템 구조이다. ABAP 프로그래밍은 데이터베이스를 짜거나 구성 요소를 만드는 것이 아니라 [GUI](../Page/그래픽_사용자_인터페이스.md "wikilink") 계층과 응용 프로그램 계층 사이에서 비즈니스 프로세스(Business process)에 따라 사용자가 원하는 기능을 가진 프로그램을 제공하도록 개발하는 것이다.

## ABAP 프로그램 구조 및 흐름

구조적인 측면에서 ABAP은 선언, 모듈, 이벤트, 서브루틴으로 나눌 수 있다. 선언부에서는 다른 언어와 마찬가지로 변수의 자료형이나 참조부분을 정의해 주는 부분이다. Dialog 모듈은 입출력에 대한 처리, 이벤트 부분은 실질적은 프로그램 코딩 부분이며 이벤트의 시작점이다. [서브루틴](https://ko.wikipedia.org/wiki/서브루틴 "wikilink")은 사용자(개발자)가 정의한 함수를 말한다. ABAP 프로그램의 기본적인 흐름을 살펴보면, 먼저 프로그램을 시작하고, 초기화, 개발자가 구성한 입력조건 화면을 생성한 뒤 사용자가 검색하고자 하는 조건을 입력하면 그것을 개발자가 검색 내용에 알맞은 내용을 데이터베이스에서 검색하여 사용자가 볼 수 있도록 출력하는 흐름을 가진다.

## [헬로 월드 프로그램](https://ko.wikipedia.org/wiki/헬로_월드_프로그램 "wikilink")

``` abap
REPORT TEST.
WRITE 'Hello World'.
```

## ABAP 개발도구

ABAP를 위한 부가적인 개발도구로 다음과 같은 것이 있다.

  - ABAP Editor(SE38)-보통 소스를 편집하는 도구로서 프로그램을 생성하거나 수정, 조회, 속성을 정의할 수 있다.
  - ABAP Dictionary(SE11)-테이블, 자료형 등을 정의하고 수정, 삭제할 수 있는 도구이다.
  - Screen Painter(SE51)-사용자가 사용하는 대화 상자 화면을 만들 수 있는 도구이다
  - Menu Painter(SE41)-대화 상자를 꾸밀 수 있는 도구이다.
  - Function Builder(SE37)-function 모듈을 생성, 수정, 삭제하는 도구이다.
  - Class Builder(SE24)-global 클래스와 인터페이스를 유지하기 위한 도구이다.
  - **Object Navigator(SE80)**-위의 모든 것을 사용할 수 있는 만능 도구이다.

## 같이 보기

  - [ERP 소프트웨어](https://ko.wikipedia.org/wiki/전사적_자원_관리 "wikilink")
  - [통합 인증](../Page/통합_인증.md "wikilink")

## 각주

[분류:4세대 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:4세대_프로그래밍_언어 "wikilink") [분류:프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:프로그래밍_언어 "wikilink") [분류:SAP SE](https://ko.wikipedia.org/wiki/분류:SAP_SE "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink")