> This article is converted from Wikipedia: [MySQL Federated](https://ko.wikipedia.org/wiki/MySQL_Federated).


[MySQL](../Page/MySQL.md "wikilink") [관계형 데이터베이스 관리 시스템용](../Page/관계형_데이터베이스_관리_시스템.md "wikilink") **MySQL Federated** [저장 엔진은](../Page/데이터베이스_엔진.md "wikilink") 유저가 외부(또는 원격) 테이블을 로컬로 보여주는 테이블을 생성할 수 있게 해주는 저장 엔진이다. 이것은 MySQL 클라이언트 라이브러리 API를 데이터 통로로 이용하여, 원격의 데이터 소스를 동일하게 다른 저장 엔진으로 취급하여 로컬 데이터 자료를 MYD 파일([MyISAM](../Page/MyISAM.md "wikilink")), 메모리(클러스터, 힙) 또는 테이블스페이스([InnoDB](../Page/InnoDB.md "wikilink"))에 상관없이 취급한다. 그곳에 규정된 각 Federated 테이블은 하나의 .frm (데이터 소스 URL과 같은 정보를 포함한 데이터 정의 파일)이다. 실제 데이터는 로컬 또는 원격의 MySQL 인스턴스에 존재한다.

Federated 테이블을 생성하기 위해서는 "CONNECTION" 문자열에서 URL을 지정해주어야 한다 :

``` mysql
create table t1 (
 a int,
 b varchar(32))
ENGINE=FEDERATED CONNECTION='mysql://user@hostname/test/t1'
```

연결 URL 포맷은 다음과 같이 되어야 한다 :

`scheme://user:pass@host:port/schema/tablename`

Federated 테이블을 만들면, 유저는 원격 데이터 소스가 실제로 존재해야 하며, 그렇지 않으면 에러가 발생할 것이다.

MySQL Federated 저장 엔진은 패트릭 갈브래이드(Patrick Galbraith)와 브라이언 애커(Brian Aker)가 만들었고, 현재는 패트릭 갤브래이드와 앤토니 커피스에 의해 유지되고 있다. 최초로 소개된 것은 2005년 MySQL 5.0 때 처음 소개되었다.

## 외부 링크

  - [MySQL Documentation on Federated 저장 엔진](http://dev.mysql.com/doc/refman/5.0/en/federated-storage-engine.html)

[분류:데이터베이스 엔진](https://ko.wikipedia.org/wiki/분류:데이터베이스_엔진 "wikilink") [분류:MySQL](https://ko.wikipedia.org/wiki/분류:MySQL "wikilink")