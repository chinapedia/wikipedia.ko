> This article is converted from Wikipedia: [DB](https://ko.wikipedia.org/wiki/DB).


**파운데이션DB**(FoundationDB)는 [셰어드 낫싱 아키텍처의](https://ko.wikipedia.org/wiki/셰어드_낫싱_아키텍처 "wikilink") [멀티 모델](https://ko.wikipedia.org/wiki/멀티_모델_데이터베이스 "wikilink") [NoSQL](../Page/NoSQL.md "wikilink") 데이터베이스이다.\[1\] 이 제품은 "코어"(core) 데이터베이스 위주로 개발되었으며 "레이어"(layer)에서 제공되는 추가 기능들이 포함된다.\[2\] 코어 데이터베이스는 [트랜잭션과](https://ko.wikipedia.org/wiki/데이터베이스_트랜잭션 "wikilink") 더불어 순서가 정해진 [키-값 스토어를](https://ko.wikipedia.org/wiki/키-값_데이터베이스 "wikilink") 노출한다.\[3\] 이 트랜잭션들은 [ACID](https://ko.wikipedia.org/wiki/ACID "wikilink")의 특성을 완전히 지원하면서 클러스터의 머신에 저장된 여러 키들을 읽고 쓸 수 있다.\[4\] 트랜잭션들을 사용하면 레이어를 통해 다양한 데이터 모델을 구현할 수 있다.

파운데이션DB 알파 프로그램은 2012년 1월에 시작하여 2013년 3월 4일 퍼블릭 베타 릴리스로 결론났다.\[5\] 1.0 버전이 2013년 8월 29일 정식 출시되었다. 최신 안정판 5.1.7은 2018년 4월 19일 출시되었다.

2015년 3월 25일, [애플은](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 이 기업을 인수하였다고 보고하였다.\[6\] 파운데이션DB 웹사이트의 고지에 따르면 이 기업은 임무를 완수하였기 때문에 더 이상 이 소프트웨어의 다운로드를 제공하지 않을 것이라고 언급하였다.\[7\]

2018년 4월 19일, 애플은 이 소프트웨어를 오픈 소스로 공개하였으며 라이선스는 아파치 2.0을 따른다.\[8\]

## 설계적 제약

파운데이션DB의 설계는 몇 가지 제한이 있다:

  - 긴 트랜잭션
    파운데이션DB는 5초를 초과하여 실행하는 트랜잭션은 지원하지 않는다.

<!-- end list -->

  - 큰 트랜잭션
    트랜잭션의 크기는 기록되는 모든 키와 값의 10 MB를 초과할 수 없다.

<!-- end list -->

  - 큰 키와 값
    키의 크기는 10 kB를 초과할 수 없다. 값의 크기는 100 kB를 초과할 수 없다.

## 같이 보기

  - [ACID](https://ko.wikipedia.org/wiki/ACID "wikilink")
  - [NoSQL](../Page/NoSQL.md "wikilink")
  - [데이터베이스 트랜잭션](https://ko.wikipedia.org/wiki/데이터베이스_트랜잭션 "wikilink")
  - [분산 데이터베이스](../Page/분산_데이터베이스.md "wikilink")
  - [분산 트랜잭션](https://ko.wikipedia.org/wiki/분산_트랜잭션 "wikilink")

## 각주

## 외부 링크

  -
  -
  - [FoundationDB blog](https://web.archive.org/web/20130521021528/http://blog.foundationdb.com/)

  - [FoundationDB sample layers](https://github.com/FoundationDB/python-layers)

[분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [분류:분산 컴퓨팅 구조](https://ko.wikipedia.org/wiki/분류:분산_컴퓨팅_구조 "wikilink") [분류:NoSQL](https://ko.wikipedia.org/wiki/분류:NoSQL "wikilink") [분류:트랜잭션 처리](https://ko.wikipedia.org/wiki/분류:트랜잭션_처리 "wikilink") [분류:사유 소프트웨어](https://ko.wikipedia.org/wiki/분류:사유_소프트웨어 "wikilink") [분류:애플 인수 기업](https://ko.wikipedia.org/wiki/분류:애플_인수_기업 "wikilink")

1.  [Database House Wants You to Stop Dropping ACID](https://www.wired.com/wiredenterprise/2013/03/foundationdb/)
2.  [FoundationDB Releases Beta of its 'NoSQL/YesACID' Database](http://www.h-online.com/developer/news/item/FoundationDB-releases-beta-of-its-NoSQL-YesACID-database-1816279.html)
3.
4.  [FoundationDB's NoSQL Breakthrough Challenges Relational Database Dominance](http://readwrite.com/2013/03/08/foundationdbs-nosql-breakthrough-challenges-relational-database-dominance)
5.
6.  [Apple Acquires Durable Database Company FoundationDB](https://techcrunch.com/2015/03/24/apple-acquires-durable-database-company-foundationdb/)
7.
8.