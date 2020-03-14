> This article is converted from Wikipedia: [VIEW \(SQL\)](https://ko.wikipedia.org/wiki/VIEW_\(SQL\)).


**뷰**(view)는 [관계 데이터베이스의](https://ko.wikipedia.org/wiki/관계_데이터베이스 "wikilink") [데이터베이스 언어](../Page/데이터베이스_언어.md "wikilink") [SQL](https://ko.wikipedia.org/wiki/SQL "wikilink")에서 하나 이상의 테이블 (또는 다른 뷰)에서 원하는 모든 데이터를 선택하여, 그들을 사용자 정의하여 나타낸 것이다. [관계 데이터베이스의](https://ko.wikipedia.org/wiki/관계_데이터베이스 "wikilink") [관계 모델의](https://ko.wikipedia.org/wiki/관계_모델 "wikilink") 관계의 일종인 도출 관계에 해당한다. 여러 테이블(기본 관계) 또는 뷰의 데이터를 연결하여 조합할 수 있다. 보기에 표시되는 데이터의 선택 기준을 지정할 수도 있다.

뷰는 기본 테이블(table)과 같이 행(column)과 열(row)로 구성되지만, 다른 테이블에 있는 데이터를 보여줄 뿐이며, 실제 테이블과 달리 데이터 자체를 포함하고 있는 것은 아니다. 뷰를 사용하면 여러 테이블이나 뷰를 하나의 테이블인 것처럼 볼 수 있다.

표준 SQL 규격으로는 SQL89에서 사용 가능해 졌다. [SQL89](https://ko.wikipedia.org/wiki/SQL89 "wikilink")에서는 뷰를 만들 수 있지만, DROP 문이 없기 때문에 삭제할 수 없었지만, [SQL92](https://ko.wikipedia.org/wiki/SQL92 "wikilink")에서는 CHECK OPTION, LOCAL, CASCADE 기능 확장이 이루어지고 있다. [SQL99](https://ko.wikipedia.org/wiki/SQL99 "wikilink")에서는 더욱 기능 강화되었으며, 특정 조건 하에서 뷰에서 기본 테이블의 데이터 업데이트가 가능하게 되었다.

정의된 정렬 순서가 모자란 기본적인 테이블의 열처럼, 뷰를 통해 생성된 열도 특정 순서로 정렬되어 나타나지 않는다. 뷰는 관계 테이블이며, 관계 모델은 테이블을 일련의 열로 정의를 한다. 그러한 세트는 (정의를 내림으로써) 정렬되지 않기 때문에, 뷰의 테이블도 마찬가지다. 따라서 [ORDER BY](https://ko.wikipedia.org/wiki/ORDER_BY "wikilink") 구문은 뷰의 정의에서 무의미하며, 표준 [SQL2003](https://ko.wikipedia.org/wiki/SQL2003 "wikilink")에서는 ORDER BY 구문을 CREATE VIEW 명령의 옵션에서 허용하지 않았으며, 마찬가지로 [CREATE](../Page/CREATE_\(SQL\).md "wikilink") TABLE 구문에서 거분된 것이다. 그러나 정렬된 데이터는 다른 테이블로서 동일한 방법으로 뷰를 통해 획득할 수 있다. 그럼에도 불구하고 [오라클 데이터베이스와](https://ko.wikipedia.org/wiki/오라클_데이터베이스 "wikilink") 같은 일부 DBMS에서는 이러한 SQL 표준 제한을 따르지 않고, 허용하고 있다.

## 구문

### 생성

뷰 생성 시에 다음과 같이 SQL 문을 작성한다. 기존에 있던 테이블에 있는 컬럼에서 원하는 자료만 조회하는 것이기 때문에, 만들 때도 SELECT 문을 통해 생성한다.

``` sql
CREATE VIEW 뷰이름 AS SELECT 구문;
```

### 삭제

뷰 자체를 삭제하는 것은 다음과 같이 [DROP](https://ko.wikipedia.org/wiki/DROP_\(SQL\) "wikilink") SQL 문을 작성한다.

``` sql
DROP VIEW 뷰이름;
```

뷰를 만드는 사람은 뷰를 [읽기전용](https://ko.wikipedia.org/wiki/읽기전용 "wikilink")(read-only)과 업데이트 가능(updatable) 상태로 정의할 수 있다. 만약 데이터베이스가 뷰의 스키마에서 내장된 기본 테이블의 스키마로 역 매핑을 결정할 수 있다면, 뷰는 업데이트 가능하다. [INSERT](https://ko.wikipedia.org/wiki/INSERT_\(SQL\) "wikilink"), [UPDATE](https://ko.wikipedia.org/wiki/UPDATE_\(SQL\) "wikilink"), [DELETE](https://ko.wikipedia.org/wiki/DELETE_\(SQL\) "wikilink") 동작은 업데이트 가능 뷰에서 실행될 수 있다. 원 테이블에 변경을 매핑하지 않기 때문에 읽기전용에서는 그러한 동작을 지원하지 않는다. 뷰 업데이트는 키 보존에 의해 실행된다.

일부 시스템은 뷰에서 [INSTEAD OF](https://ko.wikipedia.org/wiki/INSTEAD_OF "wikilink") [트리거를](https://ko.wikipedia.org/wiki/TRIGGER_\(SQL\) "wikilink") 지원한다. 이런 기술은 뷰에서 실행되는 Insert, update, delete의 위치에서 실행되는 다른 로직 정의를 가능하게 한다. 그리하여 데이터베이스 시스템은 뷰의 읽기전용에 기반한 데이터 수정 작업을 실행할 수 있다. 그러나 INSTEAD OF 트리거는 뷰 자체의 읽기전용이나 업데이트가능 속성을 변경하지는 못한다.

### 상응

뷰는 원 소스의 쿼리와 동일하다. 뷰와 같은 쿼리가 실행되면, 쿼리는 수정되어 버린다. 예를 들어, 다음과 같은 accounts_view라는 이름의 쿼리가 있다고 하자:

  - accounts_view:

<!-- end list -->

``` sql
SELECT name,
       money_received,
       money_sent,
       (money_received - money_sent) AS balance,
       address,
 ...
  FROM table_customers c
  JOIN accounts_table a
    ON a.customer_id = c.customer_id
```

그러면, 애플리케이션에서 다음과 같은 간단한 쿼리를 실행할 수 있다고 가정하자:

  - 간단한 쿼리

<!-- end list -->

``` sql
SELECT name,
       balance
  FROM accounts_view
```

그러면 RDBMS는 간단한 쿼리를 취해서, 동일한 뷰를 치환해 버리며, 아래의 것을 [쿼리 최적화도구로](https://ko.wikipedia.org/wiki/쿼리_최적화도구 "wikilink") 전송한다:

  - 선 실행 쿼리:

<!-- end list -->

``` sql
SELECT name,
       balance
  FROM (SELECT name,
               money_received,
               money_sent,
               (money_received - money_sent) AS balance,
               address,
 ...
          FROM table_customers c JOIN accounts_table a
               ON a.customer_id = c.customer_id        )
```

이 시점에서의 최적화도구는 쿼리를 취해서 필요없는 복잡함을 제거하며(예: 주소를 읽는 것은 필요치 않다, 부모 자원이 그것을 이용하지 않기 때문에), 프로세싱을 위해 SQL 엔진에 그 쿼리를 전송한다.

## 외부 링크

  - [DB2 내의 자원화된 질의 테이블](http://publib.boulder.ibm.com/infocenter/dzichelp/v2r2/index.jsp?topic=/com.ibm.db2z10.doc.intro/src/tpc/db2z_typesoftables.htm)
  - [마이크로소트프 SQL 서버 내의 뷰](http://msdn.microsoft.com/en-us/library/ms187956.aspx)
  - [MySQL의 뷰들](http://dev.mysql.com/doc/refman/5.1/en/views.html)
  - [PostgreSQL에서의 뷰](http://www.postgresql.org/docs/current/interactive/tutorial-views.html)
  - [Views in SQLite](http://www.sqlite.org/lang_createview.html)
  - [오라클 11.2에서의 뷰](https://web.archive.org/web/20110407005721/http://download.oracle.com/docs/cd/E11882_01/server.112/e17118/statements_8004.htm#SQLRF01504)
  - [CouchDB에서의 뷰](https://web.archive.org/web/20111011082405/http://wiki.apache.org/couchdb/Introduction_to_CouchDB_views)
  - [오라클 11.2에서의 자원화된 뷰](https://web.archive.org/web/20111028124916/http://download.oracle.com/docs/cd/E11882_01/server.112/e17118/statements_6002.htm#SQLRF01302)

[분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink") [분류:데이터 모델링](https://ko.wikipedia.org/wiki/분류:데이터_모델링 "wikilink") [분류:데이터베이스 이론](https://ko.wikipedia.org/wiki/분류:데이터베이스_이론 "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink")