> This article is converted from Wikipedia: [MyISAM](https://ko.wikipedia.org/wiki/MyISAM).


**MyISAM**은 [MySQL](../Page/MySQL.md "wikilink") [관계형 데이터베이스 관리시스템](https://ko.wikipedia.org/wiki/관계형_데이터베이스_관리시스템 "wikilink") 5.5 버전 이전의 기본 스토리지 엔진이다. 이것은 옛 ISAM 코드를 기반으로 했지만, 더 많은 유용한 확장성 가지고 있었다. MyISAM의 가장 부족한 점은 트랜잭션의 지원 부재였다. MySQL 5.5과 이후 판은 [참조 무결성](../Page/참조_무결성.md "wikilink") 제한과 더 높은 동시성을 보장하기 위해 [InnoDB](../Page/InnoDB.md "wikilink") 엔진으로 전환되었다.

각 MyISAM 테이블은 디스크에 3개의 파일로 저장이 되었다. 이 파일들은 테이블 이름과 동일한 이름으로 시작하고, 파일 형식을 지정하는 확장자를 가지고 있다. MySQL은 .frm 파일을 테이블 정의를 저장하는데 사용하지만, 이 파일은 MyISAM 엔진의 일부가 아니라 서버의 일부이다. 데이터 파일은 .MYD (MYData) 확장자를 가지며, 인덱스 파일은 .MYI (MYIndex) 확장자를 가진다. 즉, 각 테이블마다 다음과 같은 파일이 존재한다.

  - .frm - 테이블 정의 파일
  - .MYD - 데이터 파일
  - .MYI - 인덱스 파일

## 외부 링크

  - [MySQL Documentation on MyISAM Storage Engine](http://dev.mysql.com/doc/mysql/en/myisam-storage-engine.html)
  - [MyISAM's open files limit and table-cache problem explained](http://www.geeksww.com/tutorials/database_management_systems/mysql/installation/mysql_tablecache_informationschema_and_open_files_limit.php)
  - [The article about problems which will occur in using MyISAM](http://www.mysqlperformanceblog.com/2006/06/17/using-myisam-in-production/)

[분류:데이터베이스 엔진](https://ko.wikipedia.org/wiki/분류:데이터베이스_엔진 "wikilink") [분류:MySQL](https://ko.wikipedia.org/wiki/분류:MySQL "wikilink")