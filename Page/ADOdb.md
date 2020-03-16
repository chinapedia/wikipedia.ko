> This article is converted from Wikipedia: [ADOdb](https://ko.wikipedia.org/wiki/ADOdb).


**ADOdb**는 [PHP](../Page/PHP.md "wikilink") 및 [파이썬](../Page/파이썬.md "wikilink") 용의 데이터베이스 추상화 라이브러리이다. [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 [액티브엑스 데이터 오브젝트와](../Page/액티브엑스_데이터_오브젝트.md "wikilink") 비슷한 개념이이다.

프로그래머들은 밑단에 데이터베이스를 무엇으로 쓰든지 상관 없이 ADOdb를 써서 응용 프로그램을 꽤 일관적인 방법으로 작성할 수 있다. 프로그래머들은 데이터베이스 부분 쪽 코드를 수정할 필요없이 데이터베이스를 바꿔칠 수 있다.

[ADOdb 웹사이트](http://adodb.sourceforge.net/) 및 개발자 사이트 자료에 의하면, ADOdb는 다음과 같은 데이터베이스를 지원하는 것으로 알려져 있다.

  - [마이크로소프트 액세스](https://ko.wikipedia.org/wiki/마이크로소프트_액세스 "wikilink")
  - [액티브엑스 데이터 오브젝트](../Page/액티브엑스_데이터_오브젝트.md "wikilink")
  - [DB2](../Page/IBM_DB2.md "wikilink")
  - [파이어버드 (데이터베이스)](../Page/파이어버드_\(데이터베이스\).md "wikilink")
  - [Foxpro](https://ko.wikipedia.org/wiki/Foxpro "wikilink")
  - [FrontBase](https://ko.wikipedia.org/wiki/FrontBase "wikilink")
  - [Informix](https://ko.wikipedia.org/wiki/Informix "wikilink")
  - [Interbase](https://ko.wikipedia.org/wiki/Interbase "wikilink")
  - [LDAP](../Page/LDAP.md "wikilink")
  - [마이크로소프트 SQL 서버](../Page/마이크로소프트_SQL_서버.md "wikilink")
  - [MySQL](../Page/MySQL.md "wikilink")
  - [Netezza](https://ko.wikipedia.org/wiki/Netezza "wikilink")
  - [오라클 데이터베이스](../Page/오라클_데이터베이스.md "wikilink")
  - [PostgreSQL](../Page/PostgreSQL.md "wikilink")
  - [SAP DB](https://ko.wikipedia.org/wiki/SAP_DB "wikilink")
  - [SQLite](../Page/SQLite.md "wikilink")
  - [Sybase](https://ko.wikipedia.org/wiki/Sybase "wikilink")
  - [Teradata](https://ko.wikipedia.org/wiki/Teradata "wikilink")
  - [발렌티나](https://ko.wikipedia.org/wiki/발렌티나_\(데이터베이스\) "wikilink")
  - 일반 [ODBC](../Page/ODBC.md "wikilink") 그리고 [ODBTP](https://ko.wikipedia.org/wiki/ODBTP "wikilink")

## 특징

ADOdb는 [SQL](../Page/SQL.md "wikilink")을 사용한다. 각각의 데이터베이스가 SQL을 조금씩 다르게 구현한다. 때문에 개발자들은 포터빌리티를 유지하고 싶다면 특정 데이터베이스에만 있는 기능 및 함수들을 주의해야 한다. ADOdb는 어떤 형식의 일자(date) 형을 만들어 SQL에 집어 넣고 특정 DBMS에 적절한 형식으로 만들어 넣을 수 있도록 변환 함수를 제공한다. 데이터베이스에 상관없는 SQL에 조금 더 다가간 기능이다.

일부 데이터베이스는 "limit" 구문을 지원한다. limit 구문은 MySQL에서 처음 나와서 현재는 SQL에 포함되어 있다. ADOdb의 SelectLimit( ) 는 각각의 데이터베이스에 맞는 메커니즘으로 변환되며, ADOdb는 네이티브한 limit 지원이 없는 데이터베이스에서도 limit 기능을 에뮬레이트해준다. 메커니즘 변환 방식을 쓰면 비교적 빠른 시간 안에 결과를 받을 수 있다. 에뮬레이션 방식을 쓰면서 꽤 많은 행을 반환 받은 뒤 limit에 맞는 행만 이용하는 경우, 속도가 비교적 느려지게 된다.

ADOdb 특정 기능을 위해 만들어 놓은 올바른 SQL 문을 변수로 갖고 있다. 예를 들면, ADOdb에는 null에 대한 올바른 SQL 정의가 변수 하나에 들어 있다. 어떠한 데이터베이스에든 이와 null 체크를 가능케 해준다.

## 같이 보기

  - [ADOdb 라이트](https://ko.wikipedia.org/wiki/ADOdb_라이트 "wikilink")
  - [PHP 데이터 오브젝트](https://ko.wikipedia.org/wiki/PHP_데이터_오브젝트 "wikilink")

## 외부 링크

  - [ADOdb 홈페이지](http://adodb.sourceforge.net/)
  - [데이터베이스 추상화 층 대조표](https://web.archive.org/web/20050317035748/http://phplens.com/lens/adodb/), ADOdb 포함

[분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [분류:PHP 라이브러리](https://ko.wikipedia.org/wiki/분류:PHP_라이브러리 "wikilink") [분류:파이썬 라이브러리](https://ko.wikipedia.org/wiki/분류:파이썬_라이브러리 "wikilink")