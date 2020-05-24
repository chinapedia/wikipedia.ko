> This article is converted from Wikipedia: [Franca IDL](https://ko.wikipedia.org/wiki/Franca_IDL).


**프랑카 인터페이스 정의 언어**(Franca Interface Definition Language, **Franca IDL**)는 정형적으로 정의된(formally defined) 텍스트 기반의 [인터페이스 정의 언어](../Page/인터페이스_정의_언어.md "wikilink")(IDL)이다. Franca IDL은 소프트웨어 인터페이스를 정의(definition)하고 변형(transformation)하는 **Franca** 프레임워크의 일부분이다. Franca는 모델 변형([model transformation](https://ko.wikipedia.org/wiki/:en:model_transformation "wikilink")) 기술을 적용해서 다양한 IDL과 상호운용한다(예: [D-Bus](https://ko.wikipedia.org/wiki/:en:D-Bus "wikilink") Introspection language, [Apache Thrift](https://ko.wikipedia.org/wiki/:en:Apache_Thrift "wikilink") IDL, [Fibex](https://ko.wikipedia.org/wiki/:en:Fibex "wikilink") Services).

## 역사

Franca의 첫 버전은 제니비([GENIVI_Alliance](https://ko.wikipedia.org/wiki/:en:GENIVI_Alliance "wikilink"))컨소시엄에 의해 2011년 개발된 공용 인터페이스 정의 언어(Common Interface Description Language)이며, 자동차 내장 인포테인먼트([In-vehicle_infotainment](https://ko.wikipedia.org/wiki/:en:In-vehicle_infotainment "wikilink"))플랫폼의 표준으로 사용된다. 2012년 3월 [Eclipse_Public_License](https://ko.wikipedia.org/wiki/:en:Eclipse_Public_License "wikilink") 1.0으로 처음 공개되었다. Franca IDL은 2013년에 [이클립스 (소프트웨어)](../Page/이클립스_\(소프트웨어\).md "wikilink") 재단의 공식 프로젝트가 되었다.\[1\] Franca의 주 개발사는 독일의 Itemis사이다.\[2\]

## 기능

Franca IDL은 다음과 같은 SW 인터페이스 스펙을 제공한다.

  - 인터페이스 구성요소의 선언: 속성(attribute), 함수(methods), 전송(broadcasts)
  - major/minor 버전 스킴(scheme)
  - Finite-state machine([유한 상태 기계](../Page/유한_상태_기계.md "wikilink"))에 기반한 동적 행위(dynamic behaviour)의 스펙을 정의함.(**Protocol State Machines**, 줄여서: **PSM**)
  - specification of the dynamic behaviour of interfaces based on [finite-state_machine](https://ko.wikipedia.org/wiki/:en:finite-state_machine "wikilink") (**Protocol State Machines**, short: **PSM**)
  - 구조적인 커멘트(structured comments)를 통한 메타 정보의 저장 (e.g., 저자(author), 설명(description), links)
  - 사용자 정의 데이터 타입(data type,[자료형](../Page/자료형.md "wikilink")) (i.e., 배열(array), 열거(enumeration), 구조체(structure), 공용체(union), map, 타입 별명 type alias)
  - 인터페이스, 열거형, 구조체의 상속 (inheritance for interfaces, enumerations and structures)

## 구조

Franca는 text기반의 Interface이외에 [HTML](../Page/HTML.md "wikilink") documentation generator도 제공한다. Franca IDL은 [Eclipse (software)](https://ko.wikipedia.org/wiki/:en:Eclipse_\(software\) "wikilink") 플랫폼 기반으로 구현되어 있다. [Xtext](https://ko.wikipedia.org/wiki/:en:Xtext "wikilink") 프레임워크를 사용하여 Franca IDL을 정의한다.

## 같이 보기

  - [Model transformation](https://ko.wikipedia.org/wiki/:en:Model_transformation "wikilink")
  - [Automatic programming](https://ko.wikipedia.org/wiki/:en:Automatic_programming "wikilink")
  - [Eclipse (software)](https://ko.wikipedia.org/wiki/:en:Eclipse_\(software\) "wikilink")
  - [Eclipse Modeling Framework](https://ko.wikipedia.org/wiki/:en:Eclipse_Modeling_Framework "wikilink")
  - [Xtext](https://ko.wikipedia.org/wiki/:en:Xtext "wikilink")

## 각주

<references />

## 외부 링크

  -
[분류:객체 지향 프로그래밍](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍 "wikilink") [분류:데이터 모델링 언어](https://ko.wikipedia.org/wiki/분류:데이터_모델링_언어 "wikilink")

1.  <http://www.eclipse.org/proposals/modeling.franca>
2.  [itemis](http://www.itemis.com)