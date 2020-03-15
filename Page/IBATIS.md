> This article is converted from Wikipedia: [IBATIS](https://ko.wikipedia.org/wiki/IBATIS).


**iBATIS**(아이바티스)는 [SQL](../Page/SQL.md "wikilink")에 기반한 [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink")와 [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink"), [닷넷](https://ko.wikipedia.org/wiki/닷넷 "wikilink")(.NET), [루비](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink")(Ruby) 등을 연결시켜 주는 역할을 하는 [영속성 프레임워크](https://ko.wikipedia.org/wiki/영속성_프레임워크 "wikilink")(Persistence Framework)이다. 이러한 연결은 프로그램의 [소스코드](https://ko.wikipedia.org/wiki/소스코드 "wikilink")에서 [SQL](../Page/SQL.md "wikilink") 문장을 분리하여 별도의 [XML](https://ko.wikipedia.org/wiki/XML "wikilink") 파일로 저장하고 이 둘을 서로 연결시켜주는 방식으로 작동한다.

또 다른 영속성 프레임워크인 [하이버네이트](../Page/하이버네이트.md "wikilink")(Hibernate)와 비교하여 하이버네이트는 객체모델을 사용자가 생성을 하면 프레임워크에서 데이터베이스와 연결을 시켜주는 방식인데 반해 iBatis는 사용자가 [SQL](../Page/SQL.md "wikilink") 문장을 만들면 그에 적합한 객체모델을 생성하는 방식으로 작동한다.

## 프로젝트 상태

프로젝트는 2010년 5월 21일 자바와 닷넷 주요 개발자들을 포함한 팀 전원이 [아파치 소프트웨어 재단에서](../Page/아파치_소프트웨어_재단.md "wikilink") [구글 코드로](https://ko.wikipedia.org/wiki/구글_코드 "wikilink") 이전을 하기로 결정했다고 공표한 후 중단되었으며 같은 해 6월 16일에 기존 프로젝트는 [Apache Attic](http://attic.apache.org/projects/ibatis.html) 으로 옮겨졌으며 더 이상 개발되지 않는다. \[1\]

[구글 코드에서](https://ko.wikipedia.org/wiki/구글_코드 "wikilink") 새로이 만들어지는 프레임워크의 이름은 [MyBatis](https://ko.wikipedia.org/wiki/MyBatis "wikilink")로 변경되었다.

## 사용법

데이터베이스 테이블  및 자바 클래스 가 있다고 치자.  키에서 새로운  POJO로 제품 레코드를 읽으려면 다음의 매핑을 iBATIS XML 매핑 파일에 추가한다:

``` xml+velocity
    <select id="getProduct" parameterClass="java.lang.Long" resultClass="com.example.Product">
    select PROD_ID as id,
               PROD_DESC as description
          from PRODUCT
         where PROD_ID = #value#
    </select>
```

그러면 제품 번호 123에 대해 데이터베이스에서 새로운 자바 **Product** 오브젝트를 다음과 같이 검색한다:

``` java
    Product resultProduct = (Product) sqlMapClient.queryForObject("getProduct", 123);
```

## 같이 보기

  - [MyBatis](https://ko.wikipedia.org/wiki/MyBatis "wikilink")
  - [하이버네이트](../Page/하이버네이트.md "wikilink")
  - [영속성 프레임워크](https://ko.wikipedia.org/wiki/영속성_프레임워크 "wikilink")

## 각주

## 외부 링크

  - [Apache Attic의 iBatis 페이지](http://attic.apache.org/projects/ibatis.html)

  - [기존 공식 홈페이지](http://ibatis.apache.org)

[분류:아파치 소프트웨어 재단 프로젝트](https://ko.wikipedia.org/wiki/분류:아파치_소프트웨어_재단_프로젝트 "wikilink") [분류:객체 관계 매핑](https://ko.wikipedia.org/wiki/분류:객체_관계_매핑 "wikilink")

1.