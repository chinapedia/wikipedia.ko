> This article is converted from Wikipedia: [몽고DB](https://ko.wikipedia.org/wiki/몽고DB).


[섬네일](https://ko.wikipedia.org/wiki/파일:Robomongo_0.8.5_-_insertion.png "wikilink") **몽고DB**(MongoDB<small>←HUMONGOUS</small>)는 크로스 플랫폼 [도큐먼트 지향 데이터베이스](https://ko.wikipedia.org/wiki/도큐먼트_지향_데이터베이스 "wikilink") 시스템이다. [NoSQL](../Page/NoSQL.md "wikilink") 데이터베이스로 분류되는 몽고DB는 [JSON](../Page/JSON.md "wikilink")과 같은 동적 스키마형 도큐먼트들(몽고DB는 이러한 포맷을 [BSON](https://ko.wikipedia.org/wiki/BSON "wikilink")이라 부름)을 선호함에 따라 전통적인 테이블 기반 [관계형 데이터베이스](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink") 구조의 사용을 삼간다. 이로써 특정한 종류의 애플리케이션을 더 쉽고 더 빠르게 데이터 통합을 가능케 한다. [아페로 GPL과](https://ko.wikipedia.org/wiki/아페로_GPL "wikilink") [아파치 라이선스를](../Page/아파치_라이선스.md "wikilink") 결합하여 공개된 몽고DB는 [자유-오픈 소스 소프트웨어이다](../Page/자유-오픈_소스_소프트웨어.md "wikilink").

뉴욕시에 기반을 둔 회사인 10gen (현재의 [몽고DB](https://ko.wikipedia.org/wiki/몽고DB_\(기업\) "wikilink"))에서 2007년 10월, 계획된 [PaaS](https://ko.wikipedia.org/wiki/PaaS "wikilink")(서비스로서의 플랫폼) 제품의 구성 요소로 처음 개발하였으며 10gen이 상용 지원 및 기타 서비스를 제공한 2009년에 오픈 소스 개발 모델로 전향하였다.\[1\] 그 뒤로 몽고DB는 [크레이그리스트](../Page/크레이그리스트.md "wikilink"), [이베이](../Page/이베이.md "wikilink"), [포스퀘어](../Page/포스퀘어.md "wikilink"), [소스포지](../Page/소스포지.md "wikilink"), [뉴욕 타임즈](https://ko.wikipedia.org/wiki/뉴욕_타임즈 "wikilink"), [구글](../Page/구글.md "wikilink"), [페이스북](../Page/페이스북.md "wikilink")와 같은 수많은 주요 웹사이트 및 서비스에 [백엔드](https://ko.wikipedia.org/wiki/백엔드 "wikilink") 소프트웨어로 채택되고 있다. 몽고DB는 가장 유명한 NoSQL 데이터베이스 시스템이다.\[2\]

## 역사

10gen 소프트웨어 기업은 2007년에 [PaaS](../Page/서비스로서의_플랫폼.md "wikilink") 제품으로서 몽고DB의 개발을 시작했다. 2009년, 이 기업은 오픈 소스 개발 모델로 전환했으며 기업은 상용 지원과 기타 서비스를 제공하는 방식을 채택하였다. 2013년, 10gen은 사명을 MongoDB Inc.로 변경하였다.\[3\]

2017년 10월 20일, 몽고DB는 주식 공개 기업이 되었으며 NASDAQ에 MDB라는 심볼로 등재되었으며 IPO 가격은 한 주에 24달러였다.\[4\]

## 주요 기능

### 애드혹 쿼리

몽고DB는 필드, 레인지 쿼리, [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 검색을 지원한다.\[5\] 쿼리는 특정 필드의 도큐먼트를 반환할 수 있으며 사용자 지정 [자바스크립트](../Page/자바스크립트.md "wikilink") 함수를 포함할 수도 있다. 쿼리는 주어진 크기의 임의의 결과 샘플을 반환하도록 설정할 수도 있다.

### 색인

몽고DB 도큐먼트의 필드는 프라이머리(primary) 인덱스와 세컨더리(secondary) 인덱스로 인덱싱할 수 있다.

### 리플리케이션

몽고DB는 리플리카 세트(replica set)와 함께 고가용성을 제공한다.\[6\] 리플리카 세트는 둘 이상의 데이터 사본으로 구성된다. 각 리플리카 세트 멤버는 어느 시점에서나 프라이머리나 세컨더리 리플리카 역할을 수행할 수 있다. 모든 쓰기와 읽기는 기본값으로 프라이머리 리플리카에서 수행된다. 세컨더리 리플리카는 내장된 리플리케이션 기능을 사용하여 프라이머리의 데이터의 사본을 관리한다. 프라이머리 리플리카가 실패하면 리플리카 세트는 어느 세컨더리가 프라이머리가 되면 좋을지 결정하기 위해 선거 과정을 자동으로 수행한다. 세컨더리 리플리카들은 선택적으로 읽기 조작을 서비스할 수 있으나 해당 데이터는 기본적으로 일관성을 유지한다.

### 로드 밸런싱

몽고DB는 [샤딩을](../Page/샤드_\(데이터베이스_아키텍처\).md "wikilink") 사용하여 수평으로 스케일링한다.\[7\] 사용자는 컬렉션 안의 데이터의 배포 방식을 결정하는 샤드 키를 선택하게 된다. 데이터는 여러 레인지(샤드 키에 따라)로 분리되며 여러 샤드로 배포된다. (샤드는 하나 이상의 리플리카가 존재하는 마스터이다)

몽고DB는 여러 개의 서버 위에서 실행할 수 있고 [부하분산](../Page/부하분산.md "wikilink")이라든지, 기동 중 데이터 복제, 하드웨어 고장 시 수행이 가능하다.

### 파일 스토리지

몽고DB는 파일 저장을 위해 여러 머신에 로드 밸런싱, 데이터 리플리케이션 기능과 더불어 [GridFS](https://ko.wikipedia.org/wiki/GridFS "wikilink")라는 이름의 [파일 시스템으로](../Page/파일_시스템.md "wikilink") 사용할 수 있다.

이 기능은 [그리드 파일 시스템이라고](https://ko.wikipedia.org/wiki/그리드_파일_시스템 "wikilink") 부르며\[8\] 몽고DB 드라이버에 포함되어 있다. 몽고DB는 파일 조작의 기능과 콘텐츠를 개발자들에게 노출한다. GridFS는 mongofiles 유틸리티나 [Ngnix](https://ko.wikipedia.org/wiki/Ngnix "wikilink") 플러그인\[9\], [Lighttpd](../Page/Lighttpd.md "wikilink")를 사용하여 접근할 수 있다.\[10\] GridFS는 파일 하나를 여러 부분이나 덩어리(chunk)로 분리시키며 해당 덩어리들 각각을 별도의 도큐먼트로 저장한다.\[11\]

### 애그리게이션

몽고DB는 애그리게이션 수행을 위해 3가지 수단을 제공한다: 애그리게이션 파이프라인(aggregation pipeline), 맵리듀스 기능(map-reduce function), 단일 목적 애그리게이션 방식(single-purpose aggregation method).\[12\]

데이터 처리와 애그리게이션 조작을 위해 [맵리듀스](../Page/맵리듀스.md "wikilink")를 사용할 수 있다. 그러나 몽고DB의 문서에 따르면 애그리게이션 파이프라인이 대부분의 애그리게이션 조작에 더 나은 성능을 제공한다.\[13\]

애그리게이션 프레임워크를 사용하면 사용자들이 [SQL](../Page/SQL.md "wikilink") GROUP BY 절이 사용되는 결과의 종류를 취득할 수 있다. 애그리게이션 연산자들은 하나로 묶어서 하나의 파이프라인을 형성할 수 있는데, 이는 [유닉스 파이프와](../Page/파이프_\(유닉스\).md "wikilink") 비슷하다. 애그리게이션 프레임워크는 여러 도큐먼트로부터 도큐먼트들을 조인(join)할 수 있는 $lookup 연산자를 포함하고 있으며 표준 편차 등의 통계 연산자를 포함한다.

### 서버 사이드 자바스크립트 실행

자바스크립트를 쿼리, 애그리게이션 기능([맵리듀스](../Page/맵리듀스.md "wikilink") 등)에 사용할 수 있으며 직접 데이터베이스로 보내어 실행할 수 있다.

### 캡트 컬렉션

몽고DB는 캡트 컬렉션(capped collection)이라는 이름의 고정 크기의 컬렉션을 지원한다. 이러한 유형의 컬렉션은 삽입 순서를 관리하고 특정 크기에 도달하면 [원형 버퍼처럼](https://ko.wikipedia.org/wiki/원형_버퍼 "wikilink") 동작하게 만들 수 있다.

### 트랜잭션

멀티 도큐먼트 [ACID](../Page/ACID.md "wikilink") 트랜잭션 지원이 2018년 6월 4.0 릴리스의 GA(General Availability)와 더불어 몽고DB에 추가되었다.\[14\]

## 참조

## 외부 링크

  -

[분류:도큐먼트 지향 데이터베이스](https://ko.wikipedia.org/wiki/분류:도큐먼트_지향_데이터베이스 "wikilink") [분류:분산 컴퓨팅 구조](https://ko.wikipedia.org/wiki/분류:분산_컴퓨팅_구조 "wikilink") [분류:NoSQL](https://ko.wikipedia.org/wiki/분류:NoSQL "wikilink") [분류:2009년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2009년_소프트웨어 "wikilink") [분류:GNU AGPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_AGPL_라이선스_소프트웨어 "wikilink")

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