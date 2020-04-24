> This article is converted from Wikipedia: [Akka](https://ko.wikipedia.org/wiki/Akka).


**Akka**는 [오픈 소스](../Page/오픈_소스.md "wikilink") 툴킷으로, [JVM](../Page/자바_\(소프트웨어_플랫폼\).md "wikilink") 상의 동시성과 분산 애플리케이션을 단순화하는 [런타임](../Page/런타임.md "wikilink")이다. Akka는 동시성을 위한 여러 프로그래밍 모델을 지원하지만, [Erlang으로부터](../Page/얼랭.md "wikilink") 영향을 받아 actor 기반의 동시성이 두드러진다.

[자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") [스칼라](https://ko.wikipedia.org/wiki/스칼라 "wikilink") 언어 모두로 작성이 가능하다. Akka는 스칼라 2.10로 작성되었으며, 스칼라 2.10의 Akka의 actor 구현은 스칼라 표준 라이브러리에 포함되어있다.\[1\]

## 역사

Philipp Haller에 의해 작성된 actor 구현은, 2006년 7월에 스칼라의 2.1.7의 일부로 릴리즈 되었다.\[2\] 2008년 스칼라는 복잡한 서버 애플리케이션에서의 사용에 대해 주목하였지만, 동시성은 아직도 [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink")(thread)-[공유 메모리](../Page/공유_메모리.md "wikilink")(shared memory)와 락(lock)을 필수적으로 사용하여 싱크를 맞추는-를 생성하는 전형적인 방식으로 이뤄지고 있다. 이러한 접근 방식으로 생겨나는 어려움을 인식하고 [얼랭](../Page/얼랭.md "wikilink") 프로그래밍 언어의 라이브러리가 지원하는 고도의 동시성 쓰기, 이벤트 주도 애플리케이션으로부터 영감을 얻어, Jonas Bonér가 스칼라와 자바에 유사한 기능을 도입하기위해 Akka를 만들었다. Bonér는 2009 년 초부터\[3\] Akka를 작업하기 시작했고, 그 해에 그것에 대한 그의 비전을 작성했다.\[4\] 첫 공식 릴리즈는 Akka 0.5로,\[5\] 2010년 1월에 발표되었다.\[6\] Akka 이제 Play 프레임워크, [스칼라](https://ko.wikipedia.org/wiki/스칼라 "wikilink") 프로그래밍 언어와와 함께 L[ightbend](http://www.lightbend.com/) 플랫폼의 일부이다.

## 특징

Akka actor를 기반으로하는 애플리케이션의 구별되는 특징은 다음과 같다:

  - 동시성은 메시지 기반이며 비동기 방식으로 이루어진다: 일반적으로 변형 가능한 데이터를 공유하거나 동기화되는 primitive를 사용해서는 안됩니다: Akka는 액터 모델을 구현한다.
  - 동일한 호스트든 분산된 호스트들이든, 직접 통신하든, 몇몇 혹은 다수의 스레드 상에서 동작하는 라우팅 채널을 이용하여 통신하든, 혹은 이외의 방법으로 통신을 하든 actor들이 상호작용하는 방식은 동일하다. 이러한 세부사항들은 프로그램이 수정 없이 스케일-업(더 성능이 뛰어난 서버를 사용)하거나 스케일-아웃(더 많은 서버를 사용)하기 위해 배포 시점의 구성 메카니즘에 따라 변경할 수 있다.
  - Actor들은 프로그램의 오류를 연관성에 따라 계층적으로 분류한다. 이 오류들은 actor의 supervisor의 이벤트로 처리된다(어느 actor가 오류를 발생했다는 메시지인지를 가리지 않음). 얼랭과는 대조적으로 Akka는 parental supervision을 강조한다. 이는 각 actor가 parent actor에 의해 생성되고 감독받는 것을 의미한다.

Akka는 actor를 제공하는 코어 모듈을 포함한 모듈 구조를 띄고 있다. 다른 모듈들은 actor의 네트워크 분산, [클러스터](../Page/컴퓨터_클러스터.md "wikilink") 지원, 명령과 이벤트 소싱, 다양한 서드 파티 시스템과의 통합(예, Apache Camel, ZeroMQ), 심지어 Futures, Agents같은 다른 병렬성 모델을 지원하는 것과 같은 기능을 추가하는 것이 가능하게 한다.

## 각주

[분류:자바 개발 도구](https://ko.wikipedia.org/wiki/분류:자바_개발_도구 "wikilink") [분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:스칼라로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:스칼라로_작성된_자유_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.