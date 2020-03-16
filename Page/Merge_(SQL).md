> This article is converted from Wikipedia: [Merge \(SQL\)](https://ko.wikipedia.org/wiki/Merge_\(SQL\)).


**MERGE** 문은 조건에 따라 [UPDATE](https://ko.wikipedia.org/wiki/UPDATE_\(SQL\) "wikilink") 또는 [INSERT를](https://ko.wikipedia.org/wiki/INSERT_\(SQL\) "wikilink") 실행한다. UPDATE 및 INSERT를 결합한 작업을 수행하기 때문에 UPSERT라는 별명을 가지고 있다.

## 표준 구문

[SQL : 2003에서](https://ko.wikipedia.org/wiki/SQL_:_2003 "wikilink") [표준 SQL에](https://ko.wikipedia.org/wiki/표준_SQL "wikilink") 도입된 구문은 다음과 같다.

``` sql
 MERGE INTO 주로 테이블 USING 서브 테이블 ON (조건)
   WHEN MATCHED THEN
     UPDATE SET 컬럼1 = 값1 [, 컬럼2 = 값2 ...]
   WHEN NOT MATCHED THEN
     INSERT (컬럼1 [, 컬럼2 ...]) VALUES (값1 [, 값2 ...])
```

  - [Oracle Database](https://ko.wikipedia.org/wiki/Oracle_Database "wikilink")\[1\]
  - [DB2](https://ko.wikipedia.org/wiki/DB2 "wikilink")\[2\]
  - [Microsoft SQL Server](https://ko.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")\[3\]
  - [Firebird](../Page/파이어버드_\(데이터베이스\).md "wikilink")\[4\]

## 비표준 구문

데이터베이스 제품 중 일부는 비표준 구문에서 유사한 기능을 제공하는 것도 있다.

  - [MySQL](../Page/MySQL.md "wikilink")은 INSERT ... ON DUPLICATE KEY UPDATE 및 REPLACE 구문을 채용하고 있다.\[5\]\[6\]
  - [SQLite](../Page/SQLite.md "wikilink")는 INSERT OR REPLACE INTO와 REPLACE 구문을 채용하고 있다.\[7\]

## 각주

## 외부 링크

  - [Oracle 11g Release 2 documentation](http://download.oracle.com/docs/cd/E14072_01/server.112/e10592/statements_9016.htm) on **`MERGE`**
  - [Firebird 2.1 documentation](http://www.firebirdsql.org/refdocs/langrefupd21-merge.html) on **`MERGE`**
  - [DB2 v9 MERGE statement](http://publib.boulder.ibm.com/infocenter/db2luw/v9/topic/com.ibm.db2.udb.admin.doc/doc/r0010873.htm)
  - [SQL Server 2008 documentation](http://msdn.microsoft.com/en-us/library/bb510625.aspx)
  - [H2 (1.2) SQL Syntax page](http://www.h2database.com/html/grammar.html#merge)

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")

1.
2.
3.
4.
5.
6.
7.