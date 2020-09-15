> This article is converted from Wikipedia: [XpressEngine](https://ko.wikipedia.org/wiki/XpressEngine).


**XpressEngine**(eXpress+press+Engine, 구 [제로보드](../Page/제로보드.md "wikilink") XE)은 고영수가 여러 자원 봉사자들과 함께 개발한 LGPL 기반 오픈 프로젝트로, [제로보드](../Page/제로보드.md "wikilink") 4나 zb5와는 별개로 완전히 새로 개발한 웹 프레임워크이다. 제로보드 4와는 달리 BBS, 블로그, 쇼핑몰, 위키 등 웹 사이트에 필요한 모든 것을 모듈로 구현해, 종합적인 웹 빌더로 사용할 수 있는 프레임워크를 목표로 개발이 진행 중이다. 이전 명칭은 '[제로보드](../Page/제로보드.md "wikilink") XE'였으나, 정식으로 CMS 기능을 갖춘 1.1.0 버전 안내를 공지하면서 '보드'의 개념과 상이하다며 명칭을 변경하였다.

[제로보드](../Page/제로보드.md "wikilink")의 명칭을 유지한 1.0.6 버전까지는 다양한 사이트와 블로그를 운영할 수 있는 홈빌더의 형태였으나, XpressEngine으로 명칭을 변경한 1.1.0 버전부터는 마이크로 블로그(플래닛) 패키지, 가상 사이트를 이용한 분양 시스템 등 더 폭넓고 다양한 기능이 탑재되어 있다.

구조는 기본 프로그램인 XE Core가 있고, 거기에 모듈이나 위젯, 애드온 등의 추가 프로그램을 올리는 방식이다. 덕분에 제로보드의 장점이었던 쉬운 개발 난이도는 정 반대로 어려워졌다는 평가를 받는다. 그러한 문제로 Core를 직접 수정하는 사용자들이, 개발자들의 비권장 공고에도 꾸준하게 유지되고 있다.

호환성이나 개발 난이도 때문에 그누보드와 비교되지만, [HHVM](../Page/HHVM.md "wikilink")이나 [라라벨](../Page/라라벨.md "wikilink") 같은 최신 PHP 프레임워크를 적극적으로 받아들이고 있으며, MVC 패턴 적용, RESTful API, 프론트엔드의 컴포넌트화 등등 최신 웹개발 트렌드를 따라잡는 행보는 높이 평가할만 하다.

XE의 글로벌 CMS 시장 점유율은 2020년 8월 기준으로 0.1%에 미치지 못하는 것으로 관측되고 있다.\[1\]

## 역사

  - 2007년 03월 14일 : Zeroboard XE 제작 시작
  - 2007년 06월 27일 : 클로즈 베타 시작
  - 2007년 08월 12일 : 오픈베타 시작 (0.1.0 버전 발표)\[2\]
  - 2008년 02월 28일 : 정식 발표 (1.0.0 버전 발표)
  - 2008년 11월 20일 : XpressEngine 으로 이름 변경
  - 2009년 07월 10일 : SVN저장소 각 프로젝트별로 분리 (개발엔진은 XpressEngine Core로 표기)
  - 2009년 10월 24일 : 제1회 XpressEngine CAMP 개최
  - 2009년 11월 11일 : XpressEngine Core 1.3.0 발표 (쉬운설치 베타 도입)\[3\]
  - 2010년 01월 04일 : XpressEngine 제1회 공모전\[4\]
  - 2010년 01월 28일 : XpressEngine Core ver 1.4.0 버전을 발표하며 사용권 문서가 GPL v.2에서 LGPL v.2로 변경되었다.\[5\]
  - 2011년 07월 26일 : 고영수(zero) XpressEngine 개발팀을 떠나 네이버 재팬에 장기 파견\[6\]
  - 2013년 11월 04일 : 프로젝트 운영 및 저장소를 Google Code에서 GitHub로 이전\[7\]
  - 2013년 12월 06일 : XE HUB 개소식\[8\]
  - 2015년 04월 08일 : XpressEngine Core ver 1.8.0 정식 배포\[9\]
  - 2015년 11월 14일 : XpressEngine Core ver 3.0 공개와 함께 개발자용 버전 배포\[10\]\[11\]
  - 2018년 12월 14일 : XpressEngine Core ver 3.0.0 공식 버전 배포

## 설치 환경

### Xpress Engine 3.0 이상

  - PHP
      - 필수 : PHP 5.5.9 이상
          - OpenSSL Extension 필요
          - Mbstring Extension 필요
          - Tokenizer Extension 필요

<!-- end list -->

  - 데이터베이스
      - MySQL 5.1 이상
      - MariaDB

### Xpress Engine 1.8 이상

  - PHP
      - 필수 : PHP 5.3.0 이상
          - PHP 5.5.0 이상 권장
          - session.auto_start = Off (php.ini)
      - 필수 : XML 라이브러리
      - 필수 : GD 라이브러리
      - 필수 : ICONV 라이브러리

<!-- end list -->

  - 데이터베이스
      - MySQL 4.1 이상
          - MySQL 5.x 이상 권장
      - MariaDB
      - Cubrid
      - MS-SQL

### Xpress Engine 1.7 이상 \~ 1.8 미만

  - PHP
      - 필수 : PHP 5.2.4 이상
          - PHP 5.3.10 이상 권장
      - 필수 : XML 라이브러리
      - 필수 : GD 라이브러리
      - 선택 : ICONV 라이브러리

<!-- end list -->

  - 데이터베이스
      - MySQL 4.1 이상
      - Cubrid
      - MS-SQL

### Xpress Engine 1.7 미만

  - PHP
      - 필수 : PHP 4.x \~ 5.x
          - 단, PHP 5.2.2 버전은 PHP의 자체 오류로 사용할 수 없음
      - 필수 : XML 라이브러리
      - 필수 : GD 라이브러리
      - 선택 : ICONV 라이브러리

<!-- end list -->

  - 데이터베이스
      - MySQL 4.1 이상
      - Cubrid
      - MS-SQL
      - Firebird
      - PostgreSQL
      - Sqlite2/Sqlite3

## 각주

<references />

## 같이 보기

  - [제로보드](../Page/제로보드.md "wikilink")
  - [그누보드](../Page/그누보드.md "wikilink")

## 외부 링크

  -

  - [XE Core Github 프로젝트](https://github.com/xpressengine/xe-core)

  - [XE Core 공식 매뉴얼](https://www.xpressengine.com/guide/README)

  - [XEHub 공식 홈페이지](http://www.xehub.io/)

[분류:인터넷 포럼 소프트웨어](https://ko.wikipedia.org/wiki/분류:인터넷_포럼_소프트웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:2008년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2008년_소프트웨어 "wikilink") [분류:네이버](https://ko.wikipedia.org/wiki/분류:네이버 "wikilink")

1.  [Usage of content management systems for websites](http://w3techs.com/technologies/overview/content_management/all)
2.  [제로보드XE 오픈베타를 시작합니다.](https://xe1.xpressengine.com/devlog/3947292)
3.  [XE Core 1.3.0 배포를 시작합니다.](https://xe1.xpressengine.com/devlog/18429157)
4.
5.  [1.4.0 변경사항](https://xe1.xpressengine.com/devlog/18652787)
6.  [XE개발팀 3개월 늦은 뉴스](https://xe1.xpressengine.com/forum/19897586)
7.  [XE 진행 상황 공유 & Github로의 저장소 이전 알림](https://xe1.xpressengine.com/devlog/22418242)
8.  [XE의 새로운 출발 - XE HUB 개소식](https://www.facebook.com/media/set/?set=a.417765695018796.1073741838.353497304778969&type=3&uploaded=1)
9.  [XE 1.8.0 정식 배포](https://www.xpressengine.com/devlog/22976509)
10. [XECon2015 개최를 알립니다 : XE3, Laravel, Modern Web](https://xe1.xpressengine.com/devlog/23088431)
11. [XE3 공식사이트](http://xpressengine.io/)