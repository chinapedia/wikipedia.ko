> This article is converted from Wikipedia: [  API](https://ko.wikipedia.org/wiki/__API).


**자바 퍼시스턴스 API**또는 **자바 [지속성](../Page/지속성.md "wikilink") API**(Java Persistence API, **JPA**) 는 [자바 플랫폼 SE와](../Page/자바_플랫폼,_스탠더드_에디션.md "wikilink") [자바 플랫폼 EE를](../Page/자바_플랫폼,_엔터프라이즈_에디션.md "wikilink") 사용하는 응용프로그램에서 관계형 [데이터베이스](../Page/데이터베이스.md "wikilink")의 관리를 표현하는 자바 [API](../Page/API.md "wikilink")이다.

기존에 [EJB](https://ko.wikipedia.org/wiki/EJB "wikilink")에서 제공되던 엔터티 빈(Entity Bean)을 대체하는 기술이다. **자바 퍼시스턴스 API**는 JSR 220에서 정의된 EJB 3.0 스펙의 일부로 정의가 되어 있지만 EJB 컨테이너에 의존하지 않으며 EJB, 웹 모듈 및 [Java SE](https://ko.wikipedia.org/wiki/Java_SE "wikilink") 클라이언트에서 모두 사용이 가능하다. 또한, 사용자가 원하는 퍼시스턴스 프로바이더 구현체를 선택해서 사용할 수 있다.

JPA 2.1을 위한 [참조 구현은](https://ko.wikipedia.org/wiki/참조_구현 "wikilink") [EclipseLink](https://ko.wikipedia.org/wiki/EclipseLink "wikilink")이다.

## 구성요소

자바 퍼시스턴스 API는 아래의 세 가지 영역으로 구성된다.

  - `javax.persistance` 패키지로 정의 된 API 그 자체
  - [자바 퍼시스턴스 쿼리 언어](https://ko.wikipedia.org/wiki/자바_퍼시스턴스_쿼리_언어 "wikilink") (JPQL)
  - 객체/관계 메타데이터

## 버전의 역사

JPA 1.0 사양은 2006년 5월 11일, [자바 커뮤니티 프로세스](../Page/자바_커뮤니티_프로세스.md "wikilink") JSR220에서 최종 배포되었다. JPA 2.0 사양은 2009년 12월 10일에 배포되었다. JPA2.1은 2013년 4월 22일에 배포 되었다.

| JPA version | 발표   | 자바 플랫폼    | 중요한 변화 |
| ----------- | ---- | --------- | ------ |
| JPA 2.1     | 2013 |           |        |
| JPA 2.0     | 2009 | Java EE 6 |        |
| JPA 1.0     | 2006 | Java EE 5 |        |

자바 퍼시스턴스 API 역사

## 엔티티

퍼시스턴스 [엔티티](https://ko.wikipedia.org/wiki/엔티티 "wikilink")는 [관계형 데이터베이스의](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink") 테이블로 지속되는 경량 [자바 클래스이다](https://ko.wikipedia.org/wiki/자바_클래스 "wikilink"). 이러한 엔티티는 테이블에서 개개의 행에 해당한다. 엔티티는 일반적으로 다른 엔티티들과 관계가 있으며 이러한 관계는 객체/관계형 메타 데이터를 통해 표현된다. 객체/관계형 메타데이터는 어노테이션을 사용하여 엔티티 클래스 파일에 직접 명시하거나 응용프로그램과 함께 배포되는 별도의 XML 설명자 파일에서 지정할 수 있다.

## JPQL

[자바 퍼시스턴스 쿼리 언어](https://ko.wikipedia.org/wiki/자바_퍼시스턴스_쿼리_언어 "wikilink")(Java Persistence Query Language, JPQL)는 관계형 데이터베이스에 저장된 엔티티에 대한 쿼리들을 작성한다. 쿼리들은 구문에서 [SQL](../Page/SQL.md "wikilink") 쿼리와 유사하지만, 데이터베이스 테이블에 직접적으로 처리하지 않고 엔티티 개체에 대하여 처리된다.

## 관련 기술

### 엔터프라이즈 자바빈즈

EJB 3.0 사양( Java EE 5 플랫폼)은 자바 퍼지스턴스 API의 정의를 포함하고 있다. 하지만 최종 사용자는 이 JPA를 사용하는 응용프로그램을 구동하기 위해 EJB 컨테이너 또는 자바 EE 응용프로그램 서버를 필요로 하지 않는다. 자바 퍼시스턴스 API의 향후 버전에서는 EJB JSR/사양 에서 JSR과 사양을 구분하여 정의될 것이다.

### 자바 데이터 오브젝트 API

자바 퍼시스턴스 API는 자바 데이터 오브젝트 API와 EJB 2.0 컨테이너 관리 퍼시스턴스(Contatiner Managed Persistenc, CMP) API를 통합하기 위한 일부로서 개발되었다.

### 서비스 데이터 오브젝트 API

JPA의 설계자는 하이버네이트(Hibernate) 및 탑링크(TopLink)와 같은 객체-관계형 매핑 도구가져온 많은 주요 영역과 함께 관계형 퍼시스턴스의 제공을 목표로 한다.

### 하이버네이트

하이버네이트(Hibernate)는 자바를 위한 오픈소스 객체-관계 매핑 프레임워크를 제공한다. 버전 3.2와 그 이후 버전에서는 JPA를 위한 구현을 제공한다.

## JPA 2.0

JPA 2.0 새 버전의 개발은 2007년 자바 커뮤니티 프로세스에서 JSR317 로써 시작되었다. JPA 2.0의 최종 버전은 2009년 12월 10일에 승인 되었다.

포함된 주요 기능:

  - 확장된 객체-관계형 매핑 기능
      - ORM과 다대일 관계로 연결된 내장 객체들의 콜랙션 지원
      - 리스트 정렬
      - 접근 유형 조합
  - Criteria 쿼리 API
  - [SQL 힌트의](../Page/힌트_\(SQL\).md "wikilink") 표준화
  - DDL 생성 지원을 위한 추가적인 메타데이터 표준화
  - 유효성검증 지원
  - 공유 객체 캐시 지원

JPA 2.0을 지원하는 벤더들:

  - Batoo JPA
  - DataNucleus (구, JPOX)
  - EclipseLink (구, Oracle TopLink)
  - IBM, WebSphere WAS
  - JBoss(Hibernate)
  - Kundera
  - ObjectDB
  - OpenJPA
  - OrientDB
  - Versant Corporation JPA

## JPA 2.1

JPA 2.1 새 버전의 개발은 2011년 7월, 자바 커뮤니티 프로세스에서 JSR338로써 시작되었다. JPA 2.1의 최종 버전은 2013년 5월 22일에 승인되었다.

포함된 주요 기능:

  - 변환기 - 데이터베이스와 객체 유형간의 사용자정의 코드 변환기를 허용됨
  - Criteria 갱신/삭제 - Criteria API를 통해 대용량 갱신 과 삭제가 허용됨
  - 엔티티 그래프 - 객체의 부분적 또는 선택적 갱신 또는 병합 허용
  - JPQL/Criteria 개선 - 산술적 서브 쿼리, 일반적 데이터베이스 함수, JOIN ON 구절, TREAT 옵션
  - 스키마 생성
  - 저장 프로시저 - 데이터베이스 저장 프로시저를 정의하기 위한 쿼리를 허용

JPA 2.1을 지원하는 벤더들:

  - DataNucleus
  - EclipseLink
  - Hibernate

## 외부 링크

### 일반 정보

  - [EJB 3 사양에 대한 최종버전을 위한 문서(JSR220)](http://jcp.org/aboutJava/communityprocess/final/jsr220/index.html)

  - [GlassFish의 퍼시스턴스 문서](http://glassfish.dev.java.net/javaee5/persistence/)

  - [JCP 퍼시스턴스 문서](http://jcp.org/aboutJava/communityprocess/final/jsr317/index.html)

### 튜토리얼

  - [Java EE 6 퍼시스턴스 API 자바문서](http://docs.oracle.com/javaee/6/api/javax/persistence/package-summary.html)
  - [Java EE 6 퍼시스턴스 API 튜토리얼](http://docs.oracle.com/javaee/6/tutorial/doc/bnbpy.html)
  - [Java EE 7 퍼시스턴스 API 자바문서](http://docs.oracle.com/javaee/7/api/javax/persistence/package-summary.html)
  - [Java EE 7 퍼시스턴스 API 튜토리얼](http://docs.oracle.com/javaee/7/tutorial/partpersist.htm)

[분류:자바 API](https://ko.wikipedia.org/wiki/분류:자바_API "wikilink") [분류:자바 플랫폼, 엔터프라이즈 에디션](https://ko.wikipedia.org/wiki/분류:자바_플랫폼,_엔터프라이즈_에디션 "wikilink") [분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:지속성](https://ko.wikipedia.org/wiki/분류:지속성 "wikilink") [분류:객체 관계 매핑](https://ko.wikipedia.org/wiki/분류:객체_관계_매핑 "wikilink")