> This article is converted from Wikipedia: [HeidiSQL](https://ko.wikipedia.org/wiki/HeidiSQL).


**HeidiSQL**(하이디SQL)은 이전에는 ‘*MySQL Front*’로 알려졌던 제품이며, [자유 소프트웨어](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink") 그리고 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") 클라이언트 또는 MySQL 프론트엔드 제품이다. 독일 프로그래머 안스가르 베커와 다른 기여자들이 [마리아DB](https://ko.wikipedia.org/wiki/마리아DB "wikilink")나 퍼코나 서버처럼, 델파이로 만든 MySQL 프론트의 [포크](../Page/포크_\(소프트웨어_개발\).md "wikilink") 제품이다. 하이디SQL로 데이터베이스를 관리하기 위해서는 MySQL 로컬 서버나 원격서버에 세션을 만들 수 있는 계정을 가지고 있어야 한다. 이 세션으로 사용자는 접속된 데이터베이스 서버 내의 MySQL 데이터베이스를 관리하고, 작업이 끝나면 접속을 종료할 것이다. 그 기능들은 대부분의 보통 그리고 숙련된 [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink"), [테이블](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink"), 그리고 데이터 레코드 작동 관리를 위해 충분하지만 MySQL 프론트엔드가 기대하는 완전한 기능을 위해 계속해서 개발 중에 있다.

## 역사

안스가르 베커(Ansgar Becker)는 1999년 “*MySQL-Front”*라는 프로젝트 이름을 가진 MySQL 프론트엔드 개발을 시작했다. MySQL 서버와 내장된 데이터베이스의 인터페이스를 구성하기 위해 매티어스 프치너(Matthias Fichtner)가 작성한 직접 API 레어를 사용했다.\[1\]

개인적인 개발은 2006년 4월에 나온 2.5 판까지 계속되었으며, [SourceForge](https://ko.wikipedia.org/wiki/SourceForge "wikilink") 상의 공개 소프트로, 이후 “*HeidiSQL*”이라는 이름으로 개명을 하였다. 하이디SQL은 새롭고, 훨씬 더 인기있는 데이터베이스 레어인 ZeosLib\[2\] 를 이용하여 재설계 되었다. 이것은 2006년 6월에 나온 3.0 버전부터 적용이되었다.

SourceForge 프로젝트 호스팅의 단점과 기타 비교 우위적 장점(성능이나 기능 같은)으로 인해, 안스가르는 HeidiSQL의 코드 레퍼지터리와 버그/기능 트래커 호스팅을 2008년 5월 [구글 코드로](https://ko.wikipedia.org/wiki/구글_코드 "wikilink") 변경하였다. HeidiSQL은 그때 일반 데이터베이스 인터페이스 수행을 이용하기 위해 기존의 라이버러리를 이용하기보다는 다시 작성되었다.

## 기능

하이디SQL은 다음과 같은 GUI 기능과 특징을 가지고 있다.\[3\]\[4\]

  - **서버 연결**
      - 다중 접속과 내부의 다중 계정 접속
      - 호환 서버를 위한 압축된 클리어언트/서버 프로토콜
      - [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink"), [명명된 파이프](https://ko.wikipedia.org/wiki/명명된_파이프 "wikilink") (소켓) 또는 [터널링 프로토콜](https://ko.wikipedia.org/wiki/터널링_프로토콜 "wikilink") (SSH)을 통한 서버 인터페이스 제공
      - 하나의 윈도 내에 다중 병렬 활성 세션
      - 서버 내 유저 관리: 추가, 삭제 그리고 유저 편집과 권한 설정
      - 전역 또는 데이터베이스별 이용자 권한 설정 관리
      - 데이터베이스를 SQL 파일 또는 다른 서버로 내보내기
      - 다중 쿼리 탭, 각각이 배치 결과에 따라 하위탭을 가질 수 있다.
  - **서버 호스트**
      - 모든 서버 변수의 보기와 필터 (예, system_time_zone)
      - 현재 세션 또는 전역 서버 변수 편집
      - 서버 통계 변수 보기, 시간당 초당 평균값 보기
      - 수행된 SQL 분석과 나쁜 프로세스를 죽이기 위한 현재 프로세스 보기
      - SQL 명령당 명령어 통계보기 (% 단위로)
  - **데이터베이스**
      - 서버 상 모든 데이터베이스 보기, 테이블과 데이터 작업을 위한 단일 데이터베이스 연결
      - 연결된 데이터베이스 보기' 데이터베이스 /테이블 트리 구조 내의 전체 또는 테이블 크기를 KB/MB/GB로 보기
      - 신규 데이터베이스 생성, 기존 데이터베이스명, 문자셋, 협업 등 바꾸기, 데이터베이스 삭제하기
  - **테이블 뷰, 프로시저, 트리거와 이벤트**
      - 선택된 데이터베이스 내의 모든 객체보기, 비우기, 이름바꾸기, 그리고 객체 삭제
      - [데이터베이스 테이블](https://ko.wikipedia.org/wiki/데이터베이스_테이블 "wikilink") [컬럼](../Page/컬럼_\(데이터베이스\).md "wikilink"), [인덱스](https://ko.wikipedia.org/wiki/인덱스_\(데이터베이스\) "wikilink"), [외래 키](https://ko.wikipedia.org/wiki/외래_키 "wikilink") 편집. [마리아DB](https://ko.wikipedia.org/wiki/마리아DB "wikilink") 서버의 [가상 컬럼](https://ko.wikipedia.org/wiki/가상_컬럼 "wikilink") 지원
      - [VIEW](https://ko.wikipedia.org/wiki/뷰_\(SQL\) "wikilink") 쿼리 편집과 세팅
      - [프로시저](https://ko.wikipedia.org/wiki/저장_프로시저 "wikilink") SQL 본문과 변수 수정
      - [트리거](../Page/데이터베이스_트리거.md "wikilink") SQL 본문과 세팅 수정
      - 예약 이벤트 SQL 본문 시간 설정 수정

## jHeidi

자바 판 하이디SQL이며, 맥과 리눅스에서 작동하도록 설계되었다. jHeidi 프로젝트는 2010년 3월 이후 중단되었다. ([홈페이지 참고](https://web.archive.org/web/20081107072239/http://www.heidisql.com/jheidi/))

## 같이 보기

  - [MySQL](https://ko.wikipedia.org/wiki/MySQL "wikilink")
  - [MySQL 워크벤치](../Page/MySQL_워크벤치.md "wikilink")
  - [phpMyAdmin](https://ko.wikipedia.org/wiki/phpMyAdmin "wikilink")

## 각주

## 외부 링크

  - [공식 웹사이트](http://www.heidisql.com)
  - [HeidiSQL 프로젝트 페이지](http://code.google.com/p/heidisql/) on [구글 코드](https://ko.wikipedia.org/wiki/구글_코드 "wikilink")

[분류:데이터베이스 관리 도구](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_도구 "wikilink") [분류:윈도우 전용 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_전용_자유_소프트웨어 "wikilink") [분류:마이크로소프트 데이터베이스 소프트웨어](https://ko.wikipedia.org/wiki/분류:마이크로소프트_데이터베이스_소프트웨어 "wikilink") [분류:2006년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2006년_소프트웨어 "wikilink") [분류:파스칼 소프트웨어](https://ko.wikipedia.org/wiki/분류:파스칼_소프트웨어 "wikilink")

1.  [mysql.pas - Client API for MySQL Database Servers](http://www.fichtner.net/delphi/mysql.delphi.phtml) , by Matthias Fichtner
2.  [ZeosLib - Delphi database components for MySQL, PostgreSQL, Interbase, Firebird, MS SQL, Sybase, Oracle and SQLite](http://sourceforge.net/projects/zeoslib/), SourceForge
3.  [Partial list of major features](http://www.heidisql.com/), HeidiSQL.com
4.  [Screenshots of GUI features and descriptions](http://www.heidisql.com/screenshots.php), HeidiSQL.com