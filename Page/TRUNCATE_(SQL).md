> This article is converted from Wikipedia: [TRUNCATE \(SQL\)](https://ko.wikipedia.org/wiki/TRUNCATE_\(SQL\)).


**TRUNCATE** 또는 **TRUNCATE TABLE** 문은 [테이블에서](https://ko.wikipedia.org/wiki/데이터베이스_테이블 "wikilink") 모든 행을 삭제하는 [데이터 정의 언어](../Page/데이터_정의_언어.md "wikilink")(DDL) 이다. 데이터베이스가 가지고 있는 무결성을 유지하는 메커니즘을 생략하여 빠른 제거를 실현하고 있는 경우가 많다. 삭제할 행 각각을 기록하는 [트랜잭션 로그의](../Page/트랜잭션_로그.md "wikilink") 출력을 방지함으로써 효율적으로 모든 행을 삭제할 수 있다.

## TRUNCATE 와 DELETE

‘TRUNCATE TABLE 테이블명’은 ‘DELETE FROM 테이블명’과 거의 동일하지만 다음과 같은 점에서 다르다.

  - WHERE 절을 지정할 수 없습니다. 모든 행은 일괄 삭제된다.
  - 대상 테이블 단독 잠금을 얻을 수 있다.
  - [외래 키에서](https://ko.wikipedia.org/wiki/외래_키 "wikilink") 참조되는 테이블에서 실행할 수 없다. 외래 키의 무결성을 확인하지 않기 때문이다.
  - [Oracle Database와](https://ko.wikipedia.org/wiki/Oracle_Database "wikilink") [MySQL](https://ko.wikipedia.org/wiki/MySQL "wikilink")의 일부 스토리지 엔진은 TRUNCATE 후 자동으로 [커밋](https://ko.wikipedia.org/wiki/커밋 "wikilink")을 한다. TRUNCATE의 삭제는 [롤백할](../Page/롤백_\(데이터_관리\).md "wikilink") 수 없다.
      - [PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL "wikilink") 처럼, TRUNCATE를 트랜잭션 내에서 실행할 수 있으며, 롤백이 가능한 데이터베이스도 존재한다. 대상 테이블을 "이전 버전"으로 트랜잭션이 완료 될 때까지 유지하는 것으로 실현되고 있다.
  - [Microsoft SQL Server에서는](https://ko.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") TRUNCATE TABLE 문은 복제 및 로그 전달 대상이 되고 있는 테이블에 대해 실행할 수 없다. 모두 원격 데이터베이스의 일관성을 유지하기 위해 [트랜잭션 로그를](../Page/트랜잭션_로그.md "wikilink") 이용하기 때문이다.\[1\]

## 구문

``` sql
TRUNCATE [TABLE] 테이블명 [, 테이블명]
```

많은 데이터베이스 제품에서 `TABLE`은 생략 가능하다.

## 각주

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")

1.