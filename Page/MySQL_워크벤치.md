> This article is converted from Wikipedia: [MySQL 워크벤치](https://ko.wikipedia.org/wiki/MySQL_워크벤치).


**MySQL 워크벤치**(MySQL Workbench)는 SQL 개발과 관리, [데이터베이스 설계](../Page/데이터베이스_설계.md "wikilink"), 생성 그리고 유지를 위한 단일 개발 통합 환경을 제공하는 비주얼 [데이터베이스 설계 도구이다](https://ko.wikipedia.org/wiki/:en:Comparison_of_database_tools "wikilink"). fabFORCE.NET의 DBDesigner4의 후속 판이며, 이전 소프트웨어 패키지인 MySQL GUI 툴즈 번들을 대체한 것이다.

## 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:Dbd4_ss_simplemodel.png "wikilink")

### DBDesigner4

**DBDesigner4**는 [GPL로](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 만들어진 MySQL 데이터베이스를 위한 오픈 소스 비주얼 데이테베이스 설계와 질의 도구이다.\[1\] 2002년/2003년에 fabFORCE.net 플랫폼을 위해 오스트리아의 프로그래머 마이클 G. 진너에 의해 델파이 7 / Kylix 3로 만들어진 것이다.\[2\]\[3\]

단지 물리적인 모델링 도구일 뿐이었지만, DBDesigner4는 MySQL 데이터베이스의 리버스 엔지니어링과 모델-to-데이터베이스 동기화, 모델 포스터 출력, 스키마 모델의 기초적인 버전 관리 그리고 SQL 질의어 빌더 등의 편리한 종합적인 기능을 제공하였다.\[4\] 이 도구는 [리눅스](../Page/리눅스.md "wikilink")와 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 운영 체제를 지원했다.\[5\]

진너는 MySQL AB로부터 연락을 받아, 2003년 후반 그 회사에 입사를 하여 MySQL용 [그래픽 사용자 인터페이스](../Page/그래픽_사용자_인터페이스.md "wikilink")(GUI) 도구들을 개발하여 [MySQL GUI 툴즈 번들을](https://ko.wikipedia.org/wiki/MySQL_GUI_툴즈_번들 "wikilink") 개발하기에 이러렀다.\[6\]

### MySQL GUI 도구 번들

[섬네일](https://ko.wikipedia.org/wiki/파일:MySQLadministrator1.png "wikilink") **MySQL GUI 도구 번들**은 크로스 플랫폼 오픈 소스로된 MySQL 데이터베이스 서버용 데스크탑 애플리케이션 관리도구이다. MySQL AB에 의해 개발되었으며, 이후에는 [썬마이크로시스템즈](https://ko.wikipedia.org/wiki/썬마이크로시스템즈 "wikilink")에서 개발을 이어받아, GPL 저작권으로 개발 개발을 지원했다. GUI 도구 번들 개발은 중단되었으며, 현재는 MySQL 사이트의 자료실에서만 다운받을 수 있다.\[7\]

GUI 도구 번들은 MySQL 워크벤치에게 그 자리를 물려주었으며, MySQL 워크벤치 5.2가 나오자 개발이 중단되었고, 그 지위를 물려주었다.그러나 MySQL 지원팀은 2010년 6월 30일까지 그 번들에 대해 지속적인 서비스를 제공하였다.\[8\]

## 출시판

2005년 9월 최초의 MySQL 워크벤치 프리뷰 버전이 출시되었으며\[9\], MySQL GUI 툴즈 번들에 포함되어 나온 것은 아니었다. 2007년 개발이 재개되었으며, MySQL 워크벤치는 MySQL GUI 주력 제품이 되었다.\[10\]

판 번호는 DBDesigner4를 잇는 것으로 개발되었다는 것을 강조하기 위해 5.0으로 시작되었다.\[11\]

### MySQL 워크벤치 5.0과 5.1

MySQL 워크벤치 5.0 과 5.1은 MySQL 데이터베이스의 시각적인 설계 도구로 특화되었다. 비록 MySQL 워크벤치 5.0이 윈도 전용 제품이었지만, 크로스 플랫폼이 MySQL Workbench 5.1과 이후 버전에서 추가되었다.\[12\]\[13\]

### MySQL 워크벤치 5.2

MySQL 워크벤치 5.2부터, 애플리케이션은 종합 데이터베이스 GUI 애플리케이션으로 발전하였다. 데이터베이스 모델링 외에, 편집기, 데이터베이스 마이그레이션 도구, 그리고 데이터베이스 서버 관리 인터페이스를 추가하여 MySQL GUI 툴즈 번들을 대체하였다.

## 기능

두드러진 MySQL 워크벤치 5.2의 기능은 다음과 같다:

  - 종합
      - 데이터베이스 연결 & 인스턴스 관리
      - 위저드 위주의 동작 항목
      - [파이썬](../Page/파이썬.md "wikilink"), [루아로](../Page/루아_\(프로그래밍_언어\).md "wikilink") 완전한 스크립트 가능
      - 일반적인 플러그인 지원
  - SQL 편집기
      - 스키마 객체 탐색
      - SQL 문법 강조 기능 및 구문 파서
      - 다중 편집이 가능한 결과 집합(result set)
      - SQL 스니펫(snippets) 콜렉션
      - SSH 연결 터널링
      - 유니코드 지원
  - **[데이터베이스 모델링](https://ko.wikipedia.org/wiki/데이터베이스_모델링 "wikilink")**
      - ER 다이어그래밍
      - [드래그 앤 드롭](https://ko.wikipedia.org/wiki/드래그_앤_드롭 "wikilink") 비주얼 모델링
      - SQL 스크립트와 활성 데이터베이스에서 리버스 엔지니어링
      - SQL 스크립트와 활성 데이터베이스에서 포워드 엔지니어링
      - 스키마 동기화
      - 모델의 출력
      - fabFORCE.net DBDesigner4 가져오기
  - 데이터베이스 관리
      - 데이터베이스 인스턴스 시작과 중단
      - 인스턴스 환경설정
      - 데이터베이스 계정 관리
      - 인스턴스 변수 탐색
      - 로그 파일 브라우징
      - 데이터 덤프 내보내기/가져오기
  - 데이터베이스 마이그레이션(5.2.41판 기준)
      - 모든 ODBC 호환 데이터베이스
      - 내장 지원: [마이크로소프트 SQL 서버](../Page/마이크로소프트_SQL_서버.md "wikilink"), [PostgreSQL](../Page/PostgreSQL.md "wikilink"), [사이베이스](https://ko.wikipedia.org/wiki/사이베이스 "wikilink") ASE

## 각주

## 외부 링크

  - [MySQL Workbench Product home page](http://mysql.com/products/workbench/), MySQL.com. Retrieved 2010-03-26.

  - [The MySQL Workbench Community blog](http://mysqlworkbench.org/)

  - [Official documentation](http://dev.mysql.com/doc/workbench/en/index.html)

[분류:MySQL](https://ko.wikipedia.org/wiki/분류:MySQL "wikilink") [분류:데이터베이스 관리 도구](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_도구 "wikilink")

1.  [DBDesigner4 Webpage](http://www.fabforce.net/dbdesigner4/), fabFORCE.net. Retrieved 2010-03-26.
2.  [fabFORCE.net About Page](http://www.fabforce.net/about.php), fabFORCE.net. Retrieved 2010-03-26.
3.  [DBDesigner4 Source Code Download](http://www.fabforce.net/downloadfile.php?iddownloadfile=7), fabFORCE.net. Retrieved 2010-03-26.
4.  [DBDesigner4 Feature List](http://www.fabforce.net/dbdesigner4/features.php), fabFORCE.net. Retrieved 2010-03-26.
5.  [DBDesigner4 Download Page](http://www.fabforce.net/downloads.php), fabFORCE.net. Retrieved 2010-03-26.
6.  Arjen Lentz, ["Interview with Michael G. Zinner"](http://dev.mysql.com/tech-resources/interviews/mike-zinner.html) , MySQL.com. Retrieved 2010-03-26.
7.  [MySQL GUI Tools Bundle: Archived Downloads](http://dev.mysql.com/downloads/gui-tools/5.0.html), MySQL.com, Retrieved 2010-03-26.
8.  [MySQL Product Support EOL Announcements](http://dev.mysql.com/support/eol-notice.html) , MySQL.com, Retrieved 2010-03-26.
9.  [MySQL GUI Bundle announcement (without MySQL Workbench)](http://forums.mysql.com/read.php?3,146587,146587#msg-146587), MySQL.com Forum Archive, Retrieved 2010-03-26.
10. [Workbench Schedule Announcement](http://forums.mysql.com/read.php?113,142329,142329#msg-142329), MySQL.com Forum Archive, Retrieved 2010-03-26.
11. [MySQL Workbench FAQ - General](http://wb.mysql.com/?page_id=28), MySQL Workbench Blog, Retrieved 2010-03-26.
12. Michael G. Zinner, ["Why Release on Windows First"](http://wb.mysql.com/?p=19), MySQL Workbench Blog, Retrieved 2010-03-26.
13. [MySQL Workbench Releases](http://wb.mysql.com/?page_id=49), MySQL Workbench Blog, Retrieved 2010-03-26.