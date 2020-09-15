> This article is converted from Wikipedia: [CUBRID](https://ko.wikipedia.org/wiki/CUBRID).


**CUBRID**은 [관계형 데이터베이스 관리 시스템의](../Page/관계형_데이터베이스_관리_시스템.md "wikilink") 이름이며, [오픈 소스](../Page/오픈_소스.md "wikilink") 소프트웨어이다. DBMS 엔진 부분은 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink") v2 라이선스가 적용되고 인터페이스 부분은 [BSD](../Page/BSD.md "wikilink") 라이선스가 적용되었으며, [국제표준화기구](https://ko.wikipedia.org/wiki/국제표준화기구 "wikilink")의 [표준 구조화 조회 언어를](../Page/SQL.md "wikilink") 지원한다. 2008년 11월 CUBRID 2008 (CUBRID 8)이 출시되면서 오픈소스 DBMS로 전환되었으며, 최신 안정화 버전은 CUBRID 10.2.1이다.

## 제품 라이선스 정보

CUBRID는 오픈 소스 라이선스를 채택하며, 서버 엔진에는 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink") v2 or later, GUI 기반 도구 및 응용 인터페이스에는 [버클리 소프트웨어 배포판](../Page/BSD.md "wikilink") 라이선스가 각각 적용된다. 즉, 응용 인터페이스(API)에 BSD 라이선스를 채택하여 소프트웨어 벤더가 보다 자유롭게 CUBRID 기반의 응용 프로그램을 개발 또는 배포할 수 있도록 하였다.\[1\]\[2\]

## 개발 언어 및 지원 플랫폼

  - CUBRID 서버 및 공식 라이브러리는 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 또는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 구현되어 있으며, GUI 도구인 CUBRID Manager는 [자바로](../Page/자바_\(프로그래밍_언어\).md "wikilink") 구현되어 있다.
  - CUBRID 지원 OS는 [리눅스](../Page/리눅스.md "wikilink") 및 [윈도우이며](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), 응용 프로그램을 위한 인터페이스로 [JDBC](../Page/JDBC.md "wikilink"), [PHP](../Page/PHP.md "wikilink"), [ODBC](../Page/ODBC.md "wikilink"), [OLEDB](https://ko.wikipedia.org/wiki/OLEDB "wikilink"), [ADO.NET](../Page/ADO.NET.md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"), [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink"), [node.js](https://ko.wikipedia.org/wiki/node.js "wikilink") 등을 제공한다.
  - SQL 실행을 위하여 커맨트 라인 도구인 CSQL를 지원한다.
  - GUI 기반 통합 운영 도구(CUBRID Manager), DB 마이그레이션 도구(CUBRID Migration Toolkit)를 지원한다.\[3\]

## 제품 주요 기능

  - SQL 92 표준 지원, 확장된 SQL 구문 지원
  - 트랜잭션 [ACID](../Page/ACID.md "wikilink") 지원
  - MVCC (Multiversion Concurrency Control) 지원
  - 비용 기반 옵티마이저 지원(CBO)
  - HA/[복제](https://ko.wikipedia.org/wiki/복제 "wikilink") 환경에서 트랜잭션 일치성 보장
  - 고가용성 기능 지원(High Availability)
  - 인덱스(Multi-Range/Covered/Reverse/Skip-Scan/Function based/Filtered Index) 지원
  - 온라인/오프라인/증분/압축/병렬 [백업](../Page/백업.md "wikilink")
  - 계층형 쿼리(Hierarchical Query)
  - 쿼리 플랜 캐시
  - View, Trigger 지원
  - Java Stored Procedure 지원

\[4\]

## 제품 출시 정보

  - 2008.10. CUBRID 2008 R1.0 출시
  - 2008.11. CUBRID 2008 R1.1 출시
  - 2009.01. CUBRID 2008 R1.2 출시
  - 2009.02. CUBRID 2008 R1.3 출시
  - 2009.03. CUBRID 2008 R1.4 출시
  - 2009.08. CUBRID 2008 R2.0 출시
  - 2009.12. CUBRID 2008 R2.1 출시
  - 2010.05. CUBRID 2008 R2.2 출시
  - 2010.10. CUBRID 2008 R3.0 출시
  - 2011.01. CUBRID 2008 R3.1 출시
  - 2011.06. CUBRID 2008 R4.0 출시
  - 2012.02. CUBRID 2008 R4.1 출시
  - 2012.11. CUBRID 2008 R4.3 출시
  - 2013.03. CUBRID 9.1 출시
  - 2013.09. CUBRID 9.2 출시
  - 2014.05. CUBRID 9.3 출시
  - 2017.08. CUBRID 10.1 출시
  - 2019.12. CUBRID 10.2 출시

\[5\]

## 참조

<references/>

## 외부 링크

  - [CUBRID 웹사이트(한글)](http://www.cubrid.com)
  - [CUBRID Foundation 웹사이트(영문)](http://www.cubrid.org)
  - [CUBRID 오픈소스 프로젝트(GitHub)](https://github.com/cubrid)
  - [CUBRID 이슈 관리 시스템(Jira)](http://jira.cubrid.org/projects/CBRD/issues/CBRD-23704?filter=allissues&orderby=created+DESC)
  - [PHP API Manual for CUBRID](http://php.net/cubrid)

[분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:네이버](https://ko.wikipedia.org/wiki/분류:네이버 "wikilink") [분류:관계형 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:관계형_데이터베이스_관리_시스템 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink")

1.
2.
3.
4.
5.