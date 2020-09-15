> This article is converted from Wikipedia: [자바 EE 커넥터 아키텍처](https://ko.wikipedia.org/wiki/자바_EE_커넥터_아키텍처).


**JCA**(풀네임: )는 [웹 애플리케이션 서버와](../Page/웹_애플리케이션_서버.md "wikilink") 레가시 시스템과 연동할 수 있도록 하는 자바 기반 기술이다. 또한 [JDBC](../Page/JDBC.md "wikilink")는 [웹 애플리케이션 서버와](../Page/웹_애플리케이션_서버.md "wikilink") [데이터베이스](../Page/데이터베이스.md "wikilink")와의 연동에 사용된다면, JCA는 [웹 애플리케이션 서버와](../Page/웹_애플리케이션_서버.md "wikilink") 레거시 시스템(데이터베이스 포함)과 연동하는 보다 일반적인 방법이다. 또한 JCA 1.0는 [자바 커뮤니티 프로세스의](../Page/자바_커뮤니티_프로세스.md "wikilink") JSR 16에 의해 개발됐으며, JCA의 최신 버전은 JCA 1.5 (JSR 112)이다.

## 배경

JCA는 [ERP](https://ko.wikipedia.org/wiki/ERP "wikilink")나 레거시 정보 시스템 등을 포함하는 비 [WAS](https://ko.wikipedia.org/wiki/WAS "wikilink") 환경 서비스(이하 EIS; Enterprise Information System)와의 연동을 위해 정의된 표준 프레임 워크이다. JCA 이전까지는 이들 EIS와의 연동을 위해서 각 벤더의 EIS 및 [WAS](https://ko.wikipedia.org/wiki/WAS "wikilink")마다 별도의 인터페이스를 구현하는 커스텀 드라이버를 구현하여 사용했으므로 특정 제품간에 연동 자체가 불가능 해지는 것을 제외하더라도 각각의 드라이버에 따라 다양한 인터페이스와 개발 방식을 따라야 하는 문제가 있었다.

이른바 N \* M 문제라고 불리는 이 상황은 기본적으로 코드 레벨의 수정없는 연동을 불가능하게 만들고, 이로 인하여 [J2EE](https://ko.wikipedia.org/wiki/J2EE "wikilink") 환경의 이식성과 확장성에 심각한 제약을 가한다.

이 문제를 해결하기 위하여 JCA 스펙은 리소스 어댑터와 WAS 사이의 인터페이스와 상호작용을 확정하여 표준에 맞는 WAS와 리소스 어댑터라면 코드 레벨의 수정없이 상호 호환성 있게 동작하는 것을 목표로 발전되었다. 각 EIS 벤더마다의 커스텀 드라이버를 표준화된 아키텍처로 대체함으로써 이전에 발생하였던 N \* M 연동 문제를 N + M 으로 줄일 수 있게 되었다.

## JCA와 Java EE의 관계

J2EE 1.3 기반의 [웹 애플리케이션 서버는](../Page/웹_애플리케이션_서버.md "wikilink") JCA 1.0을 지원하였으나, J2EE 1.4에 이르러 인플로우 메시지 처리를 포함한 여러 가지 확장된 기능을 포함하여 JCA 1.5로 발전하게 되었다.

## 버전 역사

| JCA version | 발표 | 자바 플랫폼    | 중요한 변화                                                  |
| ----------- | -- | --------- | ------------------------------------------------------- |
| JCA 1.6     |    | Java EE 6 | [JSR](https://ko.wikipedia.org/wiki/JSR "wikilink") 322 |
| JCA 1.5     |    | Java EE 5 | [JSR](https://ko.wikipedia.org/wiki/JSR "wikilink") 112 |
| JCA 1.0     |    | J2EE 1.3  | [JSR](https://ko.wikipedia.org/wiki/JSR "wikilink") 16  |

JCA API 역사

## 외부 링크

  - [JCA 소개](http://java.sun.com/j2ee/connector)
  - [JCA 1.5 규격 다운로드](http://java.sun.com/j2ee/download.html#connectorspec)

[분류:자바 플랫폼, 엔터프라이즈 에디션](https://ko.wikipedia.org/wiki/분류:자바_플랫폼,_엔터프라이즈_에디션 "wikilink")