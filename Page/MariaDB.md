> This article is converted from Wikipedia: [MariaDB](https://ko.wikipedia.org/wiki/MariaDB).


[섬네일](https://ko.wikipedia.org/wiki/파일:LAMP_software_bundle.svg "wikilink")\]\] **MariaDB**는 [오픈 소스의](../Page/오픈_소스.md "wikilink") [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)이다. [MySQL](../Page/MySQL.md "wikilink")과 동일한 소스 코드를 기반으로 하며, GPL v2 라이선스를 따른다. [오라클](https://ko.wikipedia.org/wiki/오라클 "wikilink") 소유의 현재 불확실한 MySQL의 라이선스 상태에 반발하여 만들어졌으며, 배포자는 [몬티 프로그램 AB](https://ko.wikipedia.org/wiki/몬티_프로그램_AB "wikilink")(Monty Program AB)와 저작권을 공유해야 한다.\[1\] 이것은 MySQL과 높은 호환성을 유지하기 위함이며, MySQL [API](../Page/API.md "wikilink")와 명령에 정확히 매칭하여, 라이브러리 바이너리와 상응함을 제공하여 교체 가능성을 높이고자 함이다.\[2\] 마리아 DB에는 새로운 저장 엔진인 [아리아(Aria)뿐만](https://ko.wikipedia.org/wiki/Aria_\(저장_엔진\) "wikilink") 아니라, [InnoDB](../Page/InnoDB.md "wikilink")를 교체할 수 있는 [XtraDB](https://ko.wikipedia.org/wiki/XtraDB "wikilink") 저장 엔진을 포함하고 있다.\[3\] 이것은 트랜잭션과 비트랜잭션 엔진 그리고 미래에 나올 MySQL 판에 대응하고자 함일 것이다.\[4\]

마리아 DB의 주요 개발자는 MySQL과 몬티 프로그램 AB를 설립한 [몬티 와이드니어스](../Page/몬티_와이드니어스.md "wikilink")(Michael Monty Widenius)이다. 그는 이전에 자신의 회사, MySQL AB를 [썬 마이크로시스템즈에](../Page/썬_마이크로시스템즈.md "wikilink") 10억 달러에 판매를 한 적이 있으며, 마리아 DB는 그의 둘째 딸인 마리아의 이름을 딴 것이다.\[5\]

## 역사

[MySQL](../Page/MySQL.md "wikilink")의 창업자 중 한 명이자 핵심 개발자였던 [몬티 와이드니어스는](../Page/몬티_와이드니어스.md "wikilink") [MySQL AB를](https://ko.wikipedia.org/wiki/MySQL_AB "wikilink") 인수한 [썬 마이크로시스템즈가](../Page/썬_마이크로시스템즈.md "wikilink") [오라클](https://ko.wikipedia.org/wiki/오라클 "wikilink")에 인수되면서 개발지침 등에 대한 의견 차이가 생겼다. 그는 그의 입장을 다음과 같이 이야기했다.\[6\]

2009년 동료 몇 명과 함께 썬을 떠나 [Monty Program AB사를](https://ko.wikipedia.org/wiki/Monty_Program_AB "wikilink") 설립하고 MariaDB 개발을 시작했다. Maria는 MySQL과 마찬가지로 몬티 와이드니어스의 딸 이름에서 따왔다.\[7\]

마리아DB의 버전은 5.5까지는 MySQL의 번호를 따랐다. 그리하여 마리아 5.5를 쓰고 있다면, MySQL 5.5의 모든 특징을 가지고 있음을 알게 된다. 특히 MySQL 5.1과 5.5에는 차이가 존재하지만, 마리아DB는 5.2와 5.3에 핵심을 내놨다.

5.5 이후에는 개발판을 10.x로 수를 붙이기로 결정을 하였다. 이러한 변화는 마리아DB가 조만간 MySQL 5.6에서 모든 특징들을 불러오지 않을 것이며(마리아DB의 표준에 안정성이 떨어진다고 판단하여 또는 자신만의 특징을 드러내기 위해), 이것은 마리아DB의 색깔을 더 분명히 하고자 함이다. 새로운 특징적 기능들이 개발되면, 새로운 번호가 필요하기 때문이다.\[8\]\[9\]

## 특징

### MySQL과의 호환성

마리아DB는 MySQL과 소스코드를 같이 하므로 사용방법과 구조가 MySQL과 동일하다.\[10\] 이름만 다르지 명령어나 사용방법 (5.5까지) 모두 MySQL과 동일하다. 편의를 위해 마리아DB는 동일한 MySQL 버전과 바이너리 드롭인 교체를 지원한다. 예를 들어, MySQL 5.1은 마리아DB 5.1과 5.2, 5.3과 호환된다. MySQL 5.5는 마리아DB 5.5와 호환되는 식이다. 이것은 다음과 같은 것을 의미한다.\[11\]

  - 데이터와 테이블 정의 파일(.frm) 파일이 바이너리 호환이 된다.
  - 모든 클라이언트 API, 프로토콜 그리고 구조가 동일하다.
  - 모든 파일이름과 바이너리, 경로, 포트, 소켓 그리고 기타 등등이 동일하다.
  - 모든 MySQL 커넥터(PHP, Perl, 파이썬, 자바, .NET, MyODBC, Ruby, MySQL C 코넥터 등)가 마리아 DB와 동일하게 작동한다. [PHP5에는 알아둬야할 약간의 설치 문제](https://web.archive.org/web/20120908075445/http://kb.askmonty.org/en/installation-issues-with-php5/) 가 있다.

근본적인 차이점은 마리아DB는 GPL v2 라이선스를 따르는 순수한 오픈소스 프로젝트이기에 [오라클](https://ko.wikipedia.org/wiki/오라클 "wikilink")로부터 자유롭다. 마리아DB의 모든 코드는 GPL, LGPL, LPGL, BSD의 라이선스로 만들어져 있다. 누구나 필요로 하면 커뮤니티를 통해 마리아DB를 내려받아 쓸 수 있다.\[12\]

  - 리눅스에서는 이러한 완전한 호환성으로 인해 \(\mathsf{mariadb}\)에대해서 mysql과 구별하기위해\(\mathsf{mysql{\color{green}{d}}}\)로 mysql.server는mysqld_safef로 각 각 대응되어 사용되도록 표현하기도한다.

### 성능

마리아DB 커뮤니티는 MySQL과 비교해 애플리케이션 부분 속도가 약 4\~5천배 정도 빠르며, MySQL이 가지고 있는 모든 제품의 기능을 완벽히 구현하면서도 성능 면에서는 최고 70%의 향상을 보이고 있다고 주장한다.\[13\]

### 기능

기존에 MySQL 엔터프라이즈에서 플러그인으로 제공한 쓰레드풀 기능이 내장됐으며, 스토리지 엔진을 활용한 샤딩 기술을 제공한다. 즉, MySQL의 오픈소스 버전을 넘어 (5.5까지) 모든 버전을 대체할 수 있는 특징들을 갖추고 있다.\[14\]

  - 가상 컬럼 - 5.2에서 추가
  - Table 제거 - 5.2에서 추가
  - 스토리지 엔진 지정 CREATE TABLE - 5.2에서 추가
  - GIS 기능 지원 - 5.3 이상
  - 멀티 소스 리플리케이션 - 10.3 이상
  - SHOW EXPLAIN - 다른 쓰레드에서 작동되는 EXPLAIN 플랜 제시

## 엔진

MariaDB는 원칙적으로 MySQL과 거의 동일한 [데이터베이스 엔진](../Page/데이터베이스_엔진.md "wikilink")(스토리지 엔진)에 대응하고 있다. 해당 데이터베이스 엔진은 다음과 같다.

  - [Aria](https://ko.wikipedia.org/wiki/Aria_\(저장_엔진\) "wikilink") - [MyISAM](../Page/MyISAM.md "wikilink") 파생 엔진 대체용 (이전 명칭은 Maria)
  - [XtraDB](https://ko.wikipedia.org/wiki/:w:XtraDB "wikilink") - [오라클](https://ko.wikipedia.org/wiki/오라클 "wikilink") [InnoDB](../Page/InnoDB.md "wikilink")를 대체하기 위해 만든 [InnoDB](../Page/InnoDB.md "wikilink") 파생 [포크](../Page/포크_\(소프트웨어_개발\).md "wikilink")
  - [FederatedX](https://ko.wikipedia.org/wiki/FederatedX "wikilink") - [MySQL Federated](../Page/MySQL_Federated.md "wikilink") 파생 엔진, 트랜잭션 제공
  - [OQGRAPH](https://ko.wikipedia.org/wiki/OQGRAPH "wikilink") - 버전 5.2 이상에서 지원
  - [SphinxSE](https://ko.wikipedia.org/wiki/SphinxSE "wikilink") - 버전 5.2 이상에서 지원, Full-Text Searching이 필요할 때 사용할 수 있는 스토리지 엔진
  - [IBMDB21](https://ko.wikipedia.org/wiki/IBMDB21 "wikilink") - 오라클은 이것을 MySQL 5.1.55에서 제거했지만, 마리아DB에서는 5.5까지 유지
  - [Cassandra](https://ko.wikipedia.org/wiki/Cassandra "wikilink") - 10.0에서 포함. 기타 비 sql 저장 엔진을 끌어들이려는 시도
  - [PBXT](https://ko.wikipedia.org/wiki/PBXT "wikilink") - 트랜잭션 제공, 5.5부터는 더 이상 유지보수를 제공하지 않음. 기본 스토리지 엔진에서 제외
  - [TokuDB](https://ko.wikipedia.org/wiki/TokuDB "wikilink") - MariaDB에서 Load해야지 쓸 수 있습니다. 장점은 다른 엔진보다 압축률이 높습니다.

## 제3자 소프트웨어

### 연결 클라이언트

MariaDB는 MySQL을 위해 설계된 데이터베이스 연결 클라이언트를 사용할 수 있다. 대표적인 예는 다음과 같다.

  - DBEdit 2 오픈 소스 데이터베이스 연결 클라이언트
  - SQLyog 윈도, 리눅스 상의 데이터베이스 관리 애플리케이션
  - Navicat 독점 데이터베이스 연결 클라이언트
  - MonYog 그리고 [SQLYog](https://ko.wikipedia.org/wiki/SQLYog "wikilink") - 그래픽 데이터베이스 관리자와 모니터 & 어드바이저
  - HeidiSQL - 윈도 상의 MySQL용 자유 그리고 공개 소스 클라이언트. 마리아DB 5.2.7판부터 윈도 MSI 패키지를 통해 지원\[15\]\[16\]

### API

  - [node-mariasql](https://github.com/mscdex/node-mariasql) 마리아DB의 비블러킹 운영을 수행하는 node.js용 API

### SQL 라이브러리

### 애플리케이션

아래의 애플리케이션들은 마리아DB를 공식적으로 지원하는 것들이다.\[17\]

  - [Drupal](https://ko.wikipedia.org/wiki/Drupal "wikilink")
  - [Kajona](https://ko.wikipedia.org/wiki/:w:Kajona "wikilink")
  - [미디어위키](../Page/미디어위키.md "wikilink")
  - [phpMyAdmin](https://ko.wikipedia.org/wiki/phpMyAdmin "wikilink")
  - [Plone](https://ko.wikipedia.org/wiki/:w:Plone "wikilink")
  - [SaltOS](https://ko.wikipedia.org/wiki/SaltOS "wikilink")
  - [워드프레스](../Page/워드프레스.md "wikilink")
  - Zend Framework
  - [XpressEngine](../Page/XpressEngine.md "wikilink") (설치시 지원)

## 주요 사용자

  - [위키백과](../Page/위키백과.md "wikilink")는 2012년 12월 MySQL에서 MariaDB로의 전환을 발표했다.\[18\]
  - [페도라](https://ko.wikipedia.org/wiki/페도라_\(운영_체제\) "wikilink") 역시 전환을 검토하고 있다.\[19\]
  - [구글](../Page/구글.md "wikilink")도 2013년 9월 MySQL 에서 MariaDB로 전환을 발표했다.\[20\]
  - [카카오톡](../Page/카카오톡.md "wikilink")은 2013년 MySQL에서 마리아DB 5.5로 전환하였다.\[21\]

## 같이 보기

  - [NoSQL](../Page/NoSQL.md "wikilink")
  - [SkySQL](https://ko.wikipedia.org/wiki/:w:SkySQL "wikilink")
  - [MySQL](../Page/MySQL.md "wikilink")

## 각주

## 외부 링크

  -
  - \- [구글](../Page/구글.md "wikilink")에서 몬티 위데니어스 강좌

[분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:2009년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2009년_소프트웨어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink") [분류:MySQL](https://ko.wikipedia.org/wiki/분류:MySQL "wikilink") [분류:소프트웨어 포크](https://ko.wikipedia.org/wiki/분류:소프트웨어_포크 "wikilink")

1.  [Contributing Code](http://kb.askmonty.org/en/contributing-code/#propose-branch) , AskMonty Knowledgebase
2.  [MariaDB versus MySQL - Compatibility](http://kb.askmonty.org/en/mariadb-versus-mysql-compatibility) , AskMonty KnowledgeBase
3.  [About XtraDB](http://kb.askmonty.org/en/about-xtradb) , AskMonty KnowledgeBase
4.  [Aria FAQ](http://kb.askmonty.org/en/aria-faq) , AskMonty KnowledgeBase
5.  [Why is the project called MariaDB?](https://kb.askmonty.org/en/why-is-the-project-called-mariadb/) , AskMonty KnowledgeBase
6.  [MySQL 개발자 “오라클, 잘못 가고 있다”](http://www.bloter.net/archives/142487), 블로터닷넷, 2013년 2월 3일, 이지영 기자
7.  [MySQL의 여동생, MariaDB와 친구되기](http://www.dbguide.net/knowledge.db?mobile&cmd=view&boardUid=168508&boardConfigUid=20&boardStep=&categoryUid=$categoryUid), 한국데이터베이스진흥원
8.  [Explanation on MariaDB 10.0](http://blog.mariadb.org/explanation-on-mariadb-10-0/), 2012년 8월 13일, rasmus
9.  [현재의 MariaDB와 MySQL 5.6 사이엔 뭐가 나올까?](http://blog.mariadb.org/what-comes-in-between-mariadb-now-and-mysql-5-6/), 2012년 5월 28일
10. [MariaDB versus MySQL - 특징](https://kb.askmonty.org/en/mariadb-versus-mysql-features/) , 2013년 4월 9일 확인
11. [MariaDB versus MySQL - 호환성](https://kb.askmonty.org/en/mariadb-versus-mysql-compatibility/) , 2013년 4월 8일 확인
12.
13.
14.
15. [MariaDB 5.2.7 shipped with HeidiSQL](http://www.heidisql.com/forum.php?t=8714)
16. [MariaDB 5.2.7 released\!](http://askmonty.org/blog/mariadb-5-2-7-released/) , Monty Program Group Blog
17.
18. [위키피디아, 마이SQL 걷어낸다](http://www.zdnet.co.kr/news/news_view.asp?artice_id=20121218090539&type=xml), ZDNet Korea
19. [레드햇, 위키피디아 이어 마이SQL 버리나](http://www.zdnet.co.kr/news/news_view.asp?artice_id=20130126010627&type=xml), ZDNet Korea
20. [Google swaps out MySQL, moves to MariaDB](http://www.theregister.co.uk/2013/09/12/google_mariadb_mysql_migration), The Register
21. <http://media.daum.net/digital/others/newsview?newsid=20130904114110569>