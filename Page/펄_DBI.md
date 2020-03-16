> This article is converted from Wikipedia: [ DBI](https://ko.wikipedia.org/wiki/_DBI).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **펄 DBI**(펄 데이터베이스 인터페이스, Perl Database Interface)는 [펄](../Page/펄.md "wikilink") [프로그래밍 언어를](../Page/프로그래밍_언어.md "wikilink") 사용하는 [프로그래머들이](https://ko.wikipedia.org/wiki/컴퓨터_프로그래머 "wikilink") 자신들의 프로그램 안에 [데이터베이스](../Page/데이터베이스.md "wikilink") 통신을 임베드하는 표준화된 방식을 제공한다. CPAN의 최신 펄 DBI 모듈은 [운영 체제](../Page/운영_체제.md "wikilink") 범위에서 실행이 가능하다.

## 역사

[Tim Bunce는](https://ko.wikipedia.org/wiki/Tim_Bunce "wikilink") 1992년 다른 사람들과 협업하여 DBI를 지정하는 것을 시작했다.\[1\] 2010년 기준으로 펄 커뮤니티는 [오픈 소스](../Page/오픈_소스.md "wikilink") 모델과 연계하여 [CPAN](../Page/CPAN.md "wikilink") 모듈로 DBI를 유지보수한다. DBD(데이터베이스 드라이버) 모듈들은 DBI의 [플러그인](../Page/플러그인.md "wikilink") 역할을 함으로써 프로그래머들이 데이터베이스와 거의 독립적인 [SQL](../Page/SQL.md "wikilink") 코드를 자신의 응용 프로그램에 사용할 수 있게 한다. 또, 프로그래머들은 SQL을 작성할 필요 없이 데이터베이스와 더 독립적인 코드를 쓸 수 있도록 펄에 사용할 수 있는 [객체 관계형 매퍼들](https://ko.wikipedia.org/wiki/객체_관계형_매퍼 "wikilink") 중 하나(예: [DBIx::Class](https://ko.wikipedia.org/wiki/DBIx::Class "wikilink"))를 이용하여 DBI와 DBD 모듈들을 간접적으로 사용할 수 있다.

## 기능

DBI와 DBD 펄 패키지들은 펄 프로그래머들이 표준화된 방식으로 수많은 데이터베이스 환경에 접근할 수 있게 한다. 시스템은 각각의 지원되는 데이터베이스 환경을 DBD 드라이버로 구현하며, 이는 마치 여러 업체의 하드웨어 장치들이 각기 다른 [CPU](../Page/중앙_처리_장치.md "wikilink") 플랫폼에서 동작할 수 있는 것과 동일하다. DBD 사용자들은 인터넷으로부터 DBD 구현체를 다운로드할 수 있다. DBD 구현체들은 [IBM DB2](../Page/IBM_DB2.md "wikilink"), [마이크로소프트 SQL 서버](../Page/마이크로소프트_SQL_서버.md "wikilink"), [오라클](../Page/오라클_데이터베이스.md "wikilink") 등의 사유 제품들과 [SQLite](../Page/SQLite.md "wikilink"), [PostgreSQL](../Page/PostgreSQL.md "wikilink"), [파이어버드](https://ko.wikipedia.org/wiki/파이어버드 "wikilink"), [MySQL](../Page/MySQL.md "wikilink") 등의 [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink") 데이터베이스를 위해 존재한다.

## 유사 프로젝트

[PHP](../Page/PHP.md "wikilink") 5는 PDO(PHP 데이터 오브젝트)라는 이름의 비슷한 인터페이스가 있다.\[2\] 자바의 [JDBC](../Page/JDBC.md "wikilink") 또한 유사하다.

## 각주

## 외부 링크

  -
  - [DBI module documentation](http://metacpan.org/module/DBI) on MetaCPAN

  - [DBD drivers](http://metacpan.org/search?q=dbd) on MetaCPAN

[분류:펄 모듈](https://ko.wikipedia.org/wiki/분류:펄_모듈 "wikilink")

1.
2.  <http://www.php.net/manual/en/intro.pdo.php>