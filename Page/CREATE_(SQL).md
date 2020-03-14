> This article is converted from Wikipedia: [CREATE \(SQL\)](https://ko.wikipedia.org/wiki/CREATE_\(SQL\)).


SQL의 **CREATE** 문은 관계형 데이터베이스 관리시스템 (RDBMS)의 관리 하에 객체를 생성하는 [데이터 정의 언어](../Page/데이터_정의_언어.md "wikilink")(DDL) 명령이다. 사용하는 [RDBMS](https://ko.wikipedia.org/wiki/RDBMS "wikilink")의 구현을 통해 CREATE 문장으로 만들 수있는 개체의 유형은 다르다. 그러나 대부분의 RDBMS의 구현은 표([테이블](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink")), 정의 영역(도메인), 색인([인덱스](https://ko.wikipedia.org/wiki/인덱스_\(데이터베이스\) "wikilink")), 이용자(사용자), 별명(별칭), [저장프로시저](https://ko.wikipedia.org/wiki/저장프로시저 "wikilink") 및 [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink") 작성을 지원하고 있다. 일부 RDBMS 구현([PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL "wikilink"))에서는 [트랜잭션](https://ko.wikipedia.org/wiki/트랜잭션_\(데이터베이스\) "wikilink") 내에서 CREATE 문 및 다른 DDL 명령을 실행이며, 따라서 [롤백](https://ko.wikipedia.org/wiki/롤백 "wikilink")이 가능하다.

## 테이블 생성

아마도 가장 잘 알려지고, 사용 빈도가 높은 CREATE 명령은 CREATE TABLE 명령일 것이다. 기본적인 사용 방법은 다음과 같다.

` CREATE [TEMPORARY] TABLE  `*`[테이블명]`*`  (  `*`[기본``   ``테이블``   ``요소``   ``쉼표``   ``목록]`*`  )  `*`[표``   ``매개변수]`*

  - 기본 테이블 요소 쉼표 목록
    다음 중 하나로 구성된 정의로 쉼표로 구분된 목록이다.
      - 컬럼 정의: *\[컬럼명\]* ''\[데이터 형식\] *{NULL | NOT NULL}* *{컬럼 옵션}*
      - [기본 키](https://ko.wikipedia.org/wiki/기본_키 "wikilink") 정의: *PRIMARY KEY* ( *\[컬럼 컴마 목록\]* )
      - 제약: *{CONSTRAINT}* *\[제약정의\]*
      - RDBMS 특정한 기능

몇 개의 컬럼이 있는 "직원"이라는 테이블을 만드는 명령의 예를 나타낸다.

``` sql
CREATE TABLE 직원 (
    ID        INTEGER   PRIMARY KEY,
    성        CHAR(75)  not null,
    이름        CHAR(50)  null,
    생년월일  DATE      null
);
```

예제를 위해 한글로 ‘성’, ‘이름’, ‘생년월일’을 표시했지만, 마이크로소트프의 ACCESS와 같은 소규모의 데이터베이스를 제외하고는, 서버 단위의 데이터베이스에서는 실제로 컬럼명은 first_name, last_name, dateofbirth와 같이 1바이트 문자인 알파벳으로 표기를 하는 것이 가장 좋다.

## 기타 생성

  - CREATE Database ..... [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink")를 생성한다.
  - CREATE Index ..... \[\[인덱스 (데이터베이스)|

인덱스\]\]를 생성한다.

  - CREATE View ...... [뷰를](https://ko.wikipedia.org/wiki/뷰_\(SQL\) "wikilink") 생성한다.
  - CREATE StoredProcedure ...... [저장프로시저](https://ko.wikipedia.org/wiki/저장프로시저 "wikilink")를 생성한다.

## 삭제

반대로 삭제를 하고 싶다면, Drop 명령을 주면 된다. 마찬가지로, 데이터베이스, 테이블, 인덱스, 뷰를 삭제한다.

[SQL](https://ko.wikipedia.org/wiki/SQL "wikilink") 내의 **`DROP`** 구문은 [RDBMS](https://ko.wikipedia.org/wiki/RDBMS "wikilink")에서 객체를 제거한다. 지워질 수 있는 객체의 종류는 각 RDBMS마다 차이가 있지만, 대부분은 [테이블](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink"), [사용자](https://ko.wikipedia.org/wiki/사용자_\(데이터베이스\) "wikilink"), 그리고 [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink") 정도는 공통으로 허용한다. [PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL "wikilink")와 같은 일부 데이터베이스는 `DROP`과 다른 DDL 명령어를 [트랜잭션](https://ko.wikipedia.org/wiki/데이터베이스_트랜잭션 "wikilink") 내부에 일어나게 허용하여 [롤백을](https://ko.wikipedia.org/wiki/롤백_\(데이터베이스\) "wikilink") 가능하게 한다. 일반적인 형태는 단순히 다음과 같이 하면 된다:

``` sql
DROP TABLE employees;
```

` DROP  `*`객체형태`*`   `*`객체명`*.

[분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink")