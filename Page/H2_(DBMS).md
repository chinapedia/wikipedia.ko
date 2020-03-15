> This article is converted from Wikipedia: [H2 \(DBMS\)](https://ko.wikipedia.org/wiki/H2_\(DBMS\)).


**H2**는 [자바로](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") 작성된 [관계형 데이터베이스 관리 시스템이다](https://ko.wikipedia.org/wiki/관계형_데이터베이스_관리_시스템 "wikilink"). 자바 애플리케이션에 임베드하거나 클라이언트-서버 모드에서 구동할 수 있다.\[1\]

이 소프트웨어는 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") 소프트웨어 [모질라 공용 허가서](https://ko.wikipedia.org/wiki/모질라_공용_허가서 "wikilink") 2.0 또는 오리지널 [이클립스 공용 허가서로](../Page/이클립스_공용_허가서.md "wikilink") 이용이 가능하다.

## 주요 기능

[SQL](https://ko.wikipedia.org/wiki/SQL "wikilink") 표준의 일부가 지원된다. 주 프로그래밍 APi는 SQL과 [JDBC](https://ko.wikipedia.org/wiki/JDBC "wikilink")이지만 데이터베이스 또한 PostgreSQL 서버처럼 동작하기 위해 [PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL "wikilink") [ODBC](https://ko.wikipedia.org/wiki/ODBC "wikilink")를 사용하여 지원한다.\[2\]

인메모리 테이블과 디스크 기반 테이블을 둘 다 생성할 수 있다. 테이블은 영구적이거나 일시적일 수 있다. 인덱스 타입은 인메모리 테이블의 경우 해시 테이블이거나 트리로 사용 가능하며, 디스크 기반 테이블에는 [B 트리를](https://ko.wikipedia.org/wiki/B_트리 "wikilink") 사용할 수 있다. 모든 데이터 조작은 [트랜잭션에](https://ko.wikipedia.org/wiki/데이터베이스_트랜잭션 "wikilink") 기반한다. 테이블 수준의 잠금과 [다중 버전 동시성 제어](../Page/다중_버전_동시성_제어.md "wikilink")(MVCC)가 구현되어 있다. [2단계 커밋 프로토콜](../Page/2단계_커밋_프로토콜.md "wikilink") 프로토콜도 지원하지만 분산 트랜잭션을 위한 표준 API는 구현되어 있지 않다.

## 역사

H2 데이터베이스 엔진의 개발은 2004년 5월에 시작되었으며 첫 판은 2005년 12월에 출시되었다. 데이터베이스 엔진은 Thomas Mueller가 작성하였다. 그는 자바 데이터베이스 엔진 하이퍼소닉 SQL(Hypersonic SQL)을 개발하였다.\[3\] 2001년, 하이퍼소닉 SQL 프로젝트는 중단되었고 [HSQLDB](https://ko.wikipedia.org/wiki/HSQLDB "wikilink") 그룹이 창설되어 하이퍼소닉 SQL 코드에 대한 작업을 계속해나갔다. H2라는 이름은 하이퍼소닉 2(Hypersonic 2)를 뜻하지만 H2는 하이퍼소닉 SQL 또는 HSQLDB와 코드를 공유하지 않는다. H2는 완전히 새로 개발된 것이다.\[4\]

## 같이 보기

  - [아파치 더비](https://ko.wikipedia.org/wiki/아파치_더비 "wikilink")

## 각주

  - <http://www.mastertheboss.com/jboss-server/jboss-datasource/h2-database-tutorial>

## 외부 링크

  - [H2 Database Engine](http://www.h2database.com)
  - [H2Sharp Ado.Net Provider for H2](https://archive.is/20130124215651/http://h2sharp.googlecode.com/)

[분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:모질라 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:모질라_라이선스_소프트웨어 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink")

1.
2.
3.  [Hypersonic SQL project page](http://hsql.sourceforge.net/index.html) at [소스포지](https://ko.wikipedia.org/wiki/소스포지 "wikilink")
4.