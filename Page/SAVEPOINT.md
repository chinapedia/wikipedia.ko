> This article is converted from Wikipedia: [SAVEPOINT](https://ko.wikipedia.org/wiki/SAVEPOINT).


**SAVEPOINT**는 하위 [트랜잭션](https://ko.wikipedia.org/wiki/데이터베이스_트랜잭션 "wikilink") (중첩 트랜잭션이라고도 함)을 실현하기 위한 [데이터베이스 언어](../Page/데이터베이스_언어.md "wikilink") SQL 구문 중 하나이다. 트랜잭션의 특정 지점에 이름을 지정하고, 그 지점 이전에 수행 한 작업에 영향을 주지 않고 그 지점 이후에 수행한 작업을 [롤백](https://ko.wikipedia.org/wiki/롤백 "wikilink")(ROLLBACK)할 수 있다. 단일 트랜잭션에서 여러 SAVEPOINT를 만들 수도 있다.

SAVEPOINT는 데이터베이스를 이용하는 응용 프로그램에서 복잡한 오류 복구 처리를 실현하는데 효과적이다. 여러 문이 갖춰진 트랜잭션 도중에 에러가 발생했을 경우, SAVEPOINT를 사용하면 전체 트랜잭션을 [롤백](https://ko.wikipedia.org/wiki/롤백 "wikilink")하지 않고 오류에서 복귀할 수 있다.

SAVEPOINT의 사용 예는 다음과 같다. SAVEPOINT name에서 지점에 이름을 지정하고 ROLLBACK TO SAVEPOINT name으로 롤백하면 된다. 설정한 SAVEPOINT는 RELEASE SAVEPOINT name 또는 트랜잭션이 종료될 때 해제된다.

``` sql
BEGIN;
  INSERT INTO tbl VALUES (1);
SAVEPOINT savepoint_example;
  INSERT INTO tbl VALUES (2);
ROLLBACK TO SAVEPOINT savepoint_example;
  INSERT INTO tbl VALUES (3);
COMMIT;
-- 1과 3이 삽입된 형태가 된다.
```

SAVEPOINT는 [표준 SQL에도](https://ko.wikipedia.org/wiki/표준_SQL "wikilink") 채용하고 있으며, [PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL "wikilink"), [Oracle Database](https://ko.wikipedia.org/wiki/오라클_데이터베이스 "wikilink"), [마이크로소프트 SQL 서버](https://ko.wikipedia.org/wiki/마이크로소프트_SQL_서버 "wikilink"), [MySQL](https://ko.wikipedia.org/wiki/MySQL "wikilink"), [DB2](https://ko.wikipedia.org/wiki/DB2 "wikilink"), [SQLite](https://ko.wikipedia.org/wiki/SQLite "wikilink")(3.6.8 이상), [파이어버드](https://ko.wikipedia.org/wiki/파이어버드 "wikilink"), [Informix Dynamic Server](https://ko.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink") (11.50xC3 이상) 등 많은 관계 데이터베이스 관리 시스템이 지원하고 있다.

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:데이터 관리](https://ko.wikipedia.org/wiki/분류:데이터_관리 "wikilink") [분류:트랜잭션 처리](https://ko.wikipedia.org/wiki/분류:트랜잭션_처리 "wikilink")