> This article is converted from Wikipedia: [ \(SQL\)](https://ko.wikipedia.org/wiki/_\(SQL\)).


[데이터베이스 쿼리에서](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink") 다양한 [SQL](https://ko.wikipedia.org/wiki/SQL "wikilink") 구현체들은 [데이터베이스 엔진에](../Page/데이터베이스_엔진.md "wikilink") 쿼리 실행 방법을 지시하는 SQL 표준의 추가분으로서 **힌트**()를 사용한다. 이를테면 힌트는 엔진에게 가능한 메모리를 덜 쓰도록 지시할 수도 있고(쿼리가 느리게 동작하더라도), [색인의](https://ko.wikipedia.org/wiki/인덱스_\(데이터베이스\) "wikilink") 사용 여부를 알릴 수도 있다([쿼리 최적화에](https://ko.wikipedia.org/wiki/쿼리_최적화 "wikilink") 관계 없이).

## 구현체

여러 데이터베이스 엔진들은 힌트 구현 시 각기 다른 접근 방식을 사용한다.

  - [MySQL](https://ko.wikipedia.org/wiki/MySQL "wikilink")은 SQL 표준의 자체 확장을 사용하는데, [테이블](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink") 이름 뒤에 USE INDEX, FORCE INDEX , IGNORE INDEX 키워드가 올 수 있다.\[1\]
  - [오라클은](https://ko.wikipedia.org/wiki/오라클_데이터베이스 "wikilink") 특별히 제작된 코멘트(comment)를 + 기호로 시작하는 쿼리 안에 사용함으로써 SQL 호환성에 영향을 미치지 않음과 동시에 힌트를 구현한다.\[2\]
  - Postgres Plus® Advanced Server([엔터프라이즈DB](https://ko.wikipedia.org/wiki/엔터프라이즈DB "wikilink")에서 출시된 [PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL "wikilink")의 사유 버전)는 오라클과 동일하게 호환되는 힌트들을 제공한다.\[3\]\[4\]

## 참조

<references />

[분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink")

1.  MySQL 5.5 Reference Manual: [12.2.9.3 Index Hint Syntax](http://dev.mysql.com/doc/refman/5.5/en/index-hints.html)
2.  [Mike Ault](https://ko.wikipedia.org/wiki/Mike_Ault "wikilink"): [Oracle SQL Hints Tuning](http://www.dba-oracle.com/t_sql_hints_tuning.htm)
3.  [Postgres Plus Advanced Server Performance and Scalability Guide: Query Optimization Hints](http://www.enterprisedb.com/docs/en/9.2/perffeat/Postgres_Plus_Advanced_Server_Performance_Guide-33.htm)
4.