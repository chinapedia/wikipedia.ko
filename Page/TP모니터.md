> This article is converted from Wikipedia: [TP모니터](https://ko.wikipedia.org/wiki/TP모니터).


**TP모니터**(TP-monitor, Transaction Processing Monitor, Teleprocessing monitor)는 트랜잭션이 온전하게 처리되고 있는지, 오류가 발생하면 적절한 조치를 취하는지에 대해 여러 개의 로컬, 원격 [터미널](https://ko.wikipedia.org/wiki/텍스트_터미널 "wikilink") 간의 데이터 전송을 감시하는 통제 프로그램이다.\[1\] 각종 프로토콜에서 동작하는 세션과 시스템과 [데이터베이스](../Page/데이터베이스.md "wikilink") 사이의 최소 처리단위인 [트랜잭션](https://ko.wikipedia.org/wiki/트랜잭션 "wikilink")을 감시하여 일관성있게 보관 유지하는 역할을 하는 트랜잭션 관리 [미들웨어](../Page/미들웨어.md "wikilink")이다. 시장분석 기관인 [가트너](../Page/가트너.md "wikilink")(Gartner)에서는 TPM으로 표시하고 있고, 또 다른 시장분석 기관인 [IDC](https://ko.wikipedia.org/wiki/IDC "wikilink")에서는 ASSP의 일부로 분류하고 있다.

## 개요

각종 컴퓨터 시스템에서 사용자와 애플리케이션과의 다수의 자원(데이터베이스 등) 사이의 [분산 트랜잭션을](../Page/분산_트랜잭션.md "wikilink") 실현하는 프로그램 모듈( 복수 자원에 걸친 처리단위인 트랜잭션에 대해 ACID 특성을 보관 유지하는 역할을 담당하는 프로그램 모듈)을 **TP모니터**라고 한다.

X/Open 모델에서는 "트랜잭션 관리자" 또는 WS-Transaction 모델의 "트랜잭션 조정자"와 동의어이다.

다만, X/Open 모델을 따르지 않는 좁은 의미의 "트랜잭션 관리"는 단일 자원 내부의 로컬 트랜잭션을 처리하는 부분을 의미하므로 주의할 필요가 있다. 여기서 "트랜잭션 모니터"라고 하면 개별 자원의 외부에서 복수의 "자원 관리" 또는 복수 노드의 "자원 관리"를 이르는 분산 트랜잭션을 관리하는 독립한 프로그램 모듈을 가리키는 것이다.

## 제품

### 상용 제품

  - [티맥스](https://ko.wikipedia.org/wiki/티맥스 "wikilink")(Tmax) : 한국 [티맥스소프트](https://ko.wikipedia.org/wiki/티맥스소프트 "wikilink")사 제품
  - [턱시도](https://ko.wikipedia.org/wiki/턱시도 "wikilink")(Tuxedo) : 미국 [오라클사](../Page/오라클_\(기업\).md "wikilink") 제품

## 같이 보기

  - [트랜잭션 처리](../Page/트랜잭션_처리.md "wikilink")
  - [미들웨어](../Page/미들웨어.md "wikilink")
  - [온라인 트랜잭션 처리](https://ko.wikipedia.org/wiki/온라인_트랜잭션_처리 "wikilink")
  - [클라이언트 서버 시스템](https://ko.wikipedia.org/wiki/클라이언트_서버_시스템 "wikilink")
  - [콘텐츠 매니지먼트 시스템](https://ko.wikipedia.org/wiki/콘텐츠_매니지먼트_시스템 "wikilink")
  - [웹 브라우저](../Page/웹_브라우저.md "wikilink")
  - [웹 서버](../Page/웹_서버.md "wikilink")
  - [웹 애플리케이션 서버](../Page/웹_애플리케이션_서버.md "wikilink")

## 각주

[분류:시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:시스템_소프트웨어 "wikilink") [분류:분산 컴퓨팅](https://ko.wikipedia.org/wiki/분류:분산_컴퓨팅 "wikilink") [분류:소프트웨어 구조](https://ko.wikipedia.org/wiki/분류:소프트웨어_구조 "wikilink") [분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [미들웨어](https://ko.wikipedia.org/wiki/분류:미들웨어 "wikilink")

1.  [Definition on bitpipe.com](http://www.bitpipe.com/tlist/TP-Monitors.html)