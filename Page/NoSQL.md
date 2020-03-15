> This article is converted from Wikipedia: [NoSQL](https://ko.wikipedia.org/wiki/NoSQL).


**NoSQL** 데이터베이스는 전통적인 [관계형 데이터베이스](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink") 보다 덜 제한적인 [일관성 모델을](https://ko.wikipedia.org/wiki/일관성_모델 "wikilink") 이용하는 데이터의 저장 및 검색을 위한 매커니즘을 제공한다. 이러한 접근에 대한 동기에는 디자인의 단순화, [수평적 확장성](https://ko.wikipedia.org/wiki/확장성 "wikilink"), 세세한 통제를 포함한다. NoSQL 데이터베이스는 단순 검색 및 추가 작업을 위한 매우 최적화된 키 값 저장 공간으로, 레이턴시와 [스루풋](https://ko.wikipedia.org/wiki/스루풋 "wikilink")과 관련하여 상당한 성능 이익을 내는 것이 목적이다. NoSQL 데이터베이스는 [빅데이터](https://ko.wikipedia.org/wiki/빅데이터 "wikilink")와 [실시간 웹](https://ko.wikipedia.org/wiki/실시간_웹 "wikilink") 애플리케이션의 상업적 이용에 널리 쓰인다. 또, NoSQL 시스템은 [SQL](https://ko.wikipedia.org/wiki/SQL "wikilink") 계열 쿼리 언어를 사용할 수 있다는 사실을 강조한다는 면에서 "Not only SQL"로 불리기도 한다.\[1\]\[2\]

이러한 접근의 동기는 다음을 포함한다: 설계의 단순성, 머신들의 [클러스터에](https://ko.wikipedia.org/wiki/클러스터_컴퓨팅 "wikilink") 대한 더 단순한 [수평 확장](https://ko.wikipedia.org/wiki/확장성 "wikilink")(관계형 데이터베이스의 문제),\[3\] 이용성에 대한 더 세밀한 통제. NoSQL 데이터베이스에 의해 사용되는 자료 구조(예: 키-값, 와이드 컬럼, 그래프, 도큐먼트)들은 관계형 데이터베이스에서 기본적으로 사용되는 것들과는 다르며 일부 작업들은 NoSQL에서 속도가 더 빠른 편이다. 주어진 NoSQL 데이터베이스의 특정한 적합 여부는 해결해야 하는 문제에 따라 다르다. NoSQL 데이터베이스에 쓰이는 자료 구조들은 관계형 데이터베이스 테이블보다 "더 유연한" 것으로 간주되기도 한다.\[4\]

수많은 NoSQL 스토어들은 이용성, 파티션 내구성, 속도의 선호로 ([CAP 정리](https://ko.wikipedia.org/wiki/CAP_정리 "wikilink") 측면에서) [일관성](https://ko.wikipedia.org/wiki/일관성 "wikilink")을 타협한다. NoSQL 스토어를 채용하는 데 생기는 장벽에는 저급의 쿼리 언어의 사용(SQL 사용 대신. 예: 테이블을 경유하여 애드혹 조인-join을 수행하는 기능이 부족), 표준화된 인터페이스의 부족, 기존 관계형 데이터베이스의 상당한 개선이 포함된다.\[5\] 대부분의 NoSQL 스토어는 진정한 [ACID](https://ko.wikipedia.org/wiki/ACID "wikilink") 트랜잭션이 결여되어 있으나 [마크로직](https://ko.wikipedia.org/wiki/마크로직 "wikilink"), [에어로스파이크](https://ko.wikipedia.org/wiki/에어로스파이크_데이터베이스 "wikilink"), 페어컴(FairCom) [c-treeACE](https://ko.wikipedia.org/wiki/c-treeACE "wikilink"), 구글 [스패너](https://ko.wikipedia.org/wiki/스패너_\(데이터베이스\) "wikilink")(기술적으로 [NewSQL](https://ko.wikipedia.org/wiki/NewSQL "wikilink") 데이터베이스이긴 하지만), Symas [LMDB](https://ko.wikipedia.org/wiki/Lightning_Memory-Mapped_Database "wikilink"), [OrientDB](https://ko.wikipedia.org/wiki/OrientDB "wikilink") 등의 일부 데이터베이스들은 이를 염두에 두고 설계하였다.

그 대신, 대부분의 NoSQL 데이터베이스들은 "궁극적인 일관성" 개념을 제공함으로써 데이터베이스의 변경사항이 모든 노드에 "궁극적으로"(일반적으로 밀리초 내) 전파되므로 데이터에 대한 모든 쿼리들이 즉각 업데이트된 데이터를 반환하지 않을 수 있고 정확하지 않은 데이터를 읽는 결과가 발생할 수 있는데 이 문제를 스테일 리드(stale read)라고 부른다.\[6\] 게다가 일부 NoSQL 시스템들은 손실된 쓰기(write)와 기타 형태의 [데이터 손실을](https://ko.wikipedia.org/wiki/데이터_손실 "wikilink") 보이는 경우도 있다.\[7\] 일부 NoSQL 시스템들은 [로그 선행 기입과](../Page/로그_선행_기입.md "wikilink") 같은 개념들을 제공하여 데이터 손실을 막는다.\[8\] 여러 데이터베이스를 거치는 [분산 트랜잭션 처리의](https://ko.wikipedia.org/wiki/분산_트랜잭션_처리 "wikilink") 경우 데이터 일관성은 NoSQL과 관계형 데이터베이스에게 훨씬 더 큰 도전이 된다. 현행의 관계형 데이터베이스들 조차도 데이터베이스 스팬을 위한 참조 무결성 제약(referential integrity constraint)을 허용하지 않는다.\[9\] 분산 트랜잭션 처리를 위해 [ACID](https://ko.wikipedia.org/wiki/ACID "wikilink") 트랜잭션과 [X/Open XA](https://ko.wikipedia.org/wiki/X/Open_XA "wikilink") 표준을 모두 준수하는 시스템들도 일부 있다.

## 역사

[섬네일|NoSQL 이니셔티브의 최초의 시각적 표현.\[10\]](https://ko.wikipedia.org/wiki/파일:NoSQL_early_schema_2009.jpg "wikilink") 카를로 스트로찌(Carlo Strozzi)는 1998년 표준 SQL 인터페이스를 채용하지 않은 자신의 경량 오픈 소스 관계형 데이터베이스를 *NoSQL*이라고 명명했다.\[11\] 스트로찌는 현재의 NoSQL 운동이 “전반적인 관계형 모델에서 점차 멀어지고 있으므로” NoREL로 부르는 것이 더 적절하다고 언급했다.\[12\]

2009년 초에 [라스트 FM의](https://ko.wikipedia.org/wiki/라스트_FM "wikilink") 요한 오스칼손(Johan Oskarsson)이 오픈 소스 [분산 데이터베이스를](../Page/분산_데이터베이스.md "wikilink") 논하기 위한 미트업 행사를 조직하면서, 이와 같은 데이터베이스를 NoSQL이라고 불렀다.\[13\] 고전적인 관계형 데이터베이스 시스템의 주요 특성을 보장하는 [ACID](https://ko.wikipedia.org/wiki/ACID "wikilink") 제공을 주로 시도하지 않은 수많은 비관계형, 분산 데이터 자료 공간의 등장에 따라 이 이름이 사용되었다.\[14\]

## NoSQL 데이터베이스의 예

NoSQL 데이터베이스를 분류하는 접근 방식은 분류와 하위 분류와 함께 다양하다. 다양한 접근 방식으로 인해 비관계형 데이터베이스를 포괄적으로 파악하는 데에는 어려움이 있다. 그럼에도 동의할만한 수준의 기본적인 분류는 데이터 모델에 기반을 둔다. 이 가운데 몇 가지와 이들이 가진 프로토타입은 다음과 같다:

  - 컬럼: [H베이스](https://ko.wikipedia.org/wiki/H베이스 "wikilink"), [아큐물로](https://ko.wikipedia.org/wiki/아파치_아큐물로 "wikilink")
  - 도큐먼트: [몽고DB](../Page/몽고DB.md "wikilink"), [카우치베이스](https://ko.wikipedia.org/wiki/카우치베이스 "wikilink")
  - 키 값: [다이나모](https://ko.wikipedia.org/wiki/다이나모 "wikilink"), [리악](https://ko.wikipedia.org/wiki/리악 "wikilink"), [레디스](../Page/레디스.md "wikilink"), [캐시](https://ko.wikipedia.org/wiki/MemcacheDB "wikilink"), [프로젝트 볼드모트](https://ko.wikipedia.org/wiki/프로젝트_볼드모트 "wikilink")
  - 그래프: [Neo4J](https://ko.wikipedia.org/wiki/Neo4J "wikilink"), [AgensGraph](https://ko.wikipedia.org/wiki/비트나인 "wikilink"), [알레그로그래프](https://ko.wikipedia.org/wiki/알레그로그래프 "wikilink"), [버투오소](https://ko.wikipedia.org/wiki/버투오소_유니버설_서버 "wikilink")

스티븐 옌은 자신의 블로그의 글 "NoSQL is a Horseless Carriage"에서 NoSQL 데이터베이스들을 다음과 같이 분류했다.\[15\]

| 용어                               | 연관 데이터베이스                                                                                                                                                                                                                    |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| KV Store                         | Keyspace, Flare, SchemaFree, RAMCloud, Oracle NoSQL Database (OnDB)                                                                                                                                                          |
| KV Store - Eventually consistent | Dynamo, [Voldemort](https://ko.wikipedia.org/wiki/:en:Voldemort_\(distributed_data_store\) "wikilink"), Dynomite, SubRecord, Mo8onDb, DovetailDB                                                                             |
| KV Store - Hierarchical          | GT.m, Cache                                                                                                                                                                                                                  |
| KV Store - Ordered               | TokyoTyrant, Lightcloud, NMDB, Luxio, MemcacheDB, Actord                                                                                                                                                                     |
| KV Cache                         | [Memcached](https://ko.wikipedia.org/wiki/Memcached "wikilink"), Repcached, Coherence, [Hazelcast](https://ko.wikipedia.org/wiki/Hazelcast "wikilink"), Infinispan, EXtremeScale, JBossCache, Velocity, Terracotta           |
| Tuple Store                      | Gigaspaces, Coord, Apache River                                                                                                                                                                                              |
| Object Database                  | ZopeDB, DB40, Shoal                                                                                                                                                                                                          |
| Document Store                   | CouchDB, Cloudant, [Couchbase](https://ko.wikipedia.org/wiki/Couchbase "wikilink"), [MongoDB](https://ko.wikipedia.org/wiki/MongoDB "wikilink"), Jackrabbit, XML-Databases, ThruDB, CloudKit, Prsevere, Riak-Basho, Scalaris |
| Wide Columnar Store              | BigTable, HBase, [Apache Cassandra](https://ko.wikipedia.org/wiki/Apache_Cassandra "wikilink"), [Hypertable](https://ko.wikipedia.org/wiki/하이퍼테이블 "wikilink"), KAI, OpenNeptune, Qbase, KDI                                  |

## 성능

벤 스코필드는 여러 유형의 NoSQL 데이터베이스의 등급을 다음과 같이 평가했다:\[16\]

| 데이터 모델      | 성능  | 확장성      | 유연성 | 복잡성 | 기능                                                        |
| ----------- | --- | -------- | --- | --- | --------------------------------------------------------- |
| 키-값 스토어     | 높음  | 높음       | 높음  | 없음  | 가변적 (없음)                                                  |
| 컬럼 지향 스토어   | 높음  | 높음       | 준수  | 낮음  | 최소                                                        |
| 도큐먼트 지향 스토어 | 높음  | 가변적 (높음) | 높음  | 낮음  | 가변적 (낮음)                                                  |
| 그래프 데이터베이스  | 가변적 | 가변적      | 높음  | 높음  | [그래프 이론](https://ko.wikipedia.org/wiki/그래프_이론 "wikilink") |
| 관계형 데이터베이스  | 가변적 | 가변적      | 낮음  | 준수  | [관계대수](https://ko.wikipedia.org/wiki/관계대수 "wikilink")     |

성능과 확장성 비교는 종종 [YCSB](https://ko.wikipedia.org/wiki/YCSB "wikilink") 벤치마크를 통해 이루어진다.

## 같이 보기

  - [CAP 정리](https://ko.wikipedia.org/wiki/CAP_정리 "wikilink")
  - [트리플스토어](https://ko.wikipedia.org/wiki/트리플스토어 "wikilink")

## 참조

<references />

## 더 읽기

  -
  -
  -
  -
  -
## 외부 링크

  -
  -
  -
  -
  -
[NoSQL](https://ko.wikipedia.org/wiki/분류:NoSQL "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:데이터 관리](https://ko.wikipedia.org/wiki/분류:데이터_관리 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15. [A Yes for a NoSQL Taxonomy](http://highscalability.com/blog/2009/11/5/a-yes-for-a-nosql-taxonomy.html). High Scalability (2009-11-05). Retrieved on 2013-09-18.
16.