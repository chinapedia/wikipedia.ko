> This article is converted from Wikipedia: [카우치DB](https://ko.wikipedia.org/wiki/카우치DB).


**아파치 카우치DB**(Apache CouchDB)는 스케일러블 아키텍처를 쉽게 이용하고 보유하는데 초점을 둔 [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") 데이터베이스 소프트웨어이다. [도큐먼트 지향](https://ko.wikipedia.org/wiki/도큐먼트_지향_데이터베이스 "wikilink") [NoSQL](../Page/NoSQL.md "wikilink") 데이터베이스 구조를 갖추고 있으며 [얼랭](../Page/얼랭.md "wikilink")으로 구현되어 있다. [JSON](../Page/JSON.md "wikilink")을 사용하여 데이터를 저장하고, [자바스크립트](../Page/자바스크립트.md "wikilink")를 쿼리 언어로 사용([맵리듀스](../Page/맵리듀스.md "wikilink") 사용)하며 [API](../Page/API.md "wikilink")를 위해 [HTTP](../Page/HTTP.md "wikilink")를 사용한다.\[1\]

카우치DB는 2005년에 첫 출시되었으며 나중에 2008년에 [아파치 소프트웨어 재단](../Page/아파치_소프트웨어_재단.md "wikilink") 프로젝트로 되었다.

[관계형 데이터베이스과는](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink") 달리 카우치DB 데이터베이스는 테이블에 데이터와 관계를 저장하지 않는다. 그 대신 각 데이터베이스는 독립된 도큐먼트들의 모음집이 된다. 각 도큐먼트는 자신만의 데이터와 스스로 포함하는 스키마를 정비한다. 애플리케이션은 여러 개의 데이터베이스, 이를테면 사용자 휴대전화에 저장된 것과 서버에 저장된 것에 접근할 수 있다. 도큐먼트 메타데이터는 리비전 정보를 포함하고 있어서 데이터베이스의 접속이 끊긴 동안 발생할 수 있는 차이를 병합하는 것이 가능하다.

카우치DB는 [다중 버전 동시성 제어](../Page/다중_버전_동시성_제어.md "wikilink")(MVCC)의 형태를 구현하므로 쓰기 중에 데이터베이스 파일을 잠그지 않는다. 충돌은 애플리케이션이 해결하도록 내버려둔다. 충돌을 해결하는 것은 일반적으로 데이터를 처음에 도큐먼트 중 하나로 병합하여 오래된 것을 삭제하는 것을 수반한다.\[2\]

그 밖의 기능들로는 [결과 무결성을](https://ko.wikipedia.org/wiki/결과_무결성 "wikilink") 포함한 도큐먼트 수준의 [ACID](../Page/ACID.md "wikilink") 시맨틱, (증강) [맵리듀스](../Page/맵리듀스.md "wikilink"), (증강) 복제를 포함한다. 카우치DB의 독특한 기능 중 하나는 [멀티 마스터 복제](https://ko.wikipedia.org/wiki/멀티_마스터_복제 "wikilink")(multi-master replication)이며 여러 머신들로 하여금 스케일할 수 있게 함으로써 고성능 시스템을 구축할 수 있게 한다. Fauxton(과거 이름은 Futon)라는 이름의 내장된 웹 애플리케이션은 관리를 돕는다.

## 같이 보기

  - [카우치베이스 서버](../Page/카우치베이스_서버.md "wikilink")

## 각주

## 참고문헌

  -
  -
  -
  -
  -
  -
## 외부 링크

  -
  - [CouchDB: The Definitive Guide](https://web.archive.org/web/20090831050402/http://books.couchdb.org/relax/)

  - [Complete HTTP API Reference](https://web.archive.org/web/20160303172725/http://wiki.apache.org/couchdb/Complete_HTTP_API_Reference)

  - [Simple PHP5 library to communicate with CouchDB](https://github.com/1999/couchdb-php)

  - [Asynchronous CouchDB client for Java](https://code.google.com/p/async-couchdb-client/)

  - [Asynchronous CouchDB client for Scala](https://github.com/KimStebel/sprouch)

  -
  -
  -
[분류:아파치 소프트웨어 재단](https://ko.wikipedia.org/wiki/분류:아파치_소프트웨어_재단 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:분산 컴퓨팅 구조](https://ko.wikipedia.org/wiki/분류:분산_컴퓨팅_구조 "wikilink") [분류:NoSQL](https://ko.wikipedia.org/wiki/분류:NoSQL "wikilink") [분류:유닉스 네트워크 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_네트워크_관련_소프트웨어 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink")

1.
2.