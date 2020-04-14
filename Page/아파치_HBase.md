> This article is converted from Wikipedia: [아파치 HBase](https://ko.wikipedia.org/wiki/아파치_HBase).


**아파치 HBase**()는 [하둡](https://ko.wikipedia.org/wiki/하둡 "wikilink") 플랫폼을 위한 공개 [비관계형](../Page/NoSQL.md "wikilink") 분산 [데이터 베이스이다](https://ko.wikipedia.org/wiki/데이터_베이스 "wikilink"). [구글](../Page/구글.md "wikilink")의 [빅테이블](../Page/빅테이블.md "wikilink")(BigTable)을 본보기로 삼았으며 [자바로](../Page/자바_\(프로그래밍_언어\).md "wikilink") 쓰여졌다. [아파치 소프트웨어 재단의](../Page/아파치_소프트웨어_재단.md "wikilink") 아파치 하둡 프로젝트 일부로서 개발되었으며 하둡의 [분산 파일 시스템인](https://ko.wikipedia.org/wiki/분산_파일_시스템 "wikilink") [HDFS](https://ko.wikipedia.org/wiki/HDFS "wikilink")위에서 동작을 한다. 대량의 흩어져 있는 데이터 저장을 위한 [무정지](https://ko.wikipedia.org/wiki/무정지 "wikilink") 방법을 제공하는 구글의 빅테이블과 비슷한 기능을 한다.

HBase는 압축, 인메모리 처리, 초기 빅테이블에 제시되어 있는 [Bloom 필터](../Page/블룸_필터.md "wikilink") 기능을 제공한다.\[1\] HBase에 있는 테이블들은 하둡에서 동작하는 [맵리듀스](../Page/맵리듀스.md "wikilink") 작업을 위한 입출력을 제공하며 자바 [API](../Page/API.md "wikilink")나 [REST](../Page/REST.md "wikilink"), [Avro](../Page/아파치_아브로.md "wikilink") 또는 [Thrift](https://ko.wikipedia.org/wiki/Thrift "wikilink") 게이트웨이를 통하여 접근할 수 있다.

HBase는 기존의 [SQL](../Page/SQL.md "wikilink") 데이터 베이스를 직접적으로 대체하지는 않지만 [페이스북](../Page/페이스북.md "wikilink")의 메시징 플랫폼\[2\]과 같은 데이터를 많이 사용하는 웹사이트에서 사용된다.\[3\]\[4\]\[5\]

## 같이 보기

  - [몽고DB](../Page/몽고DB.md "wikilink")
  - [아파치 스쿱](../Page/아파치_스쿱.md "wikilink")
  - [아파치 주키퍼](../Page/아파치_주키퍼.md "wikilink")
  - [아파치 피그](../Page/아파치_피그.md "wikilink")
  - [아파치 하이브](../Page/아파치_하이브.md "wikilink")
  - [아파치 카산드라](../Page/아파치_카산드라.md "wikilink")
  - [하둡](https://ko.wikipedia.org/wiki/하둡 "wikilink")
  - [Apache Accumulo](https://ko.wikipedia.org/wiki/Apache_Accumulo "wikilink")
  - [Hypertable](https://ko.wikipedia.org/wiki/Hypertable "wikilink")
  - [NoSQL](../Page/NoSQL.md "wikilink")

## 참조

## 외부 링크

  - [아파치 HBase 공식 홈페이지](http://hbase.apache.org/)

  - [공식 아파치 하둡 홈페이지](http://hadoop.apache.org/)

  - [Understanding HBase](https://web.archive.org/web/20090220000026/http://jimbojw.com/wiki/index.php?title=Understanding_HBase_and_BigTable)

  - [A vendor-independent comparison of NoSQL databases: Cassandra, HBase, MongoDB, Riak](http://www.networkworld.com/news/tech/2012/102212-nosql-263595.html) (NetworkWorld)

[HBase](https://ko.wikipedia.org/wiki/분류:아파치_소프트웨어_재단 "wikilink") [HBase](https://ko.wikipedia.org/wiki/분류:하둡 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink")

1.  [Chang, et al. (2006). Bigtable: A Distributed Storage System for Structured Data](https://db.usenix.org//events/osdi06/tech/chang/chang_html/)
2.  [The Underlying Technology of Messages](https://www.facebook.com/notes/facebook-engineering/the-underlying-technology-of-messages/454991608919)
3.
4.  [StumbleUpon HBase Presentation](http://www.docstoc.com/docs/9912857/HBase-nosql-presentation)
5.  [Facebook: Why our 'next-gen' comms ditched MySQL](http://www.theregister.co.uk/2010/12/17/facebook_messages_tech/) Retrieved: 17 December 2010