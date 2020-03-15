> This article is converted from Wikipedia: [IBM DB2](https://ko.wikipedia.org/wiki/IBM_DB2).


**IBM DB2**는 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")에서 1983년에 발표된 상업용 관계 [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink") 관리 시스템이다. MVS/XA와 MVS/370 운영체제에서 사용되며 [SQL](../Page/SQL.md "wikilink")을 데이터 언어로 사용하여 다수의 사용자들이 여러 개의 관계 데이터베이스를 동시에 접근할 수 있는 대형 데이터베이스를 위한 시스템이다.

## 역사

DB2는 그 뿌리의 시점은 1970년대 초로 거슬러 올라간다. IBM의 연구원 [에드거 F. 커드가](../Page/에드거_F._커드.md "wikilink") 관계형 데이터베이스 이론을 기술하고 1970년 6월 데이터 조작 모델을 출시하였다.\[1\]

DB2 (IBM 데이터베이스 2)라는 이름은 IBM이 DB2를 [MVS](../Page/MVS.md "wikilink") 메인프레임 플랫폼을 출시한 1983년에 [DBMS에](../Page/데이터베이스_관리_시스템.md "wikilink") 처음 사용되었다.\[2\]

## 현재 출시 중인 에디션

오늘날 DB2 계열에는 3가지 주요 제품이 있다: [DB2 for Linux, UNIX and Windows](https://ko.wikipedia.org/wiki/DB2_UDB "wikilink") (비공식적으로 DB2 LUW), DB2 for [z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink") (메인프레임), DB2 for iSeries (과거의 [OS/400](https://ko.wikipedia.org/wiki/OS/400 "wikilink")) 4번째 제품 DB2 for VM / VSE도 이용이 가능하다.

## 오류 처리

DB2 컴퓨터 프로그램의 중요한 기능으로 오류 처리가 있다. SQLCA(SQL communications area)는 [SQL](../Page/SQL.md "wikilink") 문이 실행된 이후마다 DB2 프로그램 내에 내부적으로 사용되어 오류 정보를 응용 프로그램에 반환한다. 주된 오류 진단은 SQLCA 블록 안에 위치한 [SQLCODE](https://ko.wikipedia.org/wiki/DB2_SQL_반환_코드 "wikilink") 필드에 담겨져 있다.

SQL 반환 코드 값은 다음과 같다:

  - 0은 성공적인 실행을 의미한다.
  - 양수는 하나 이상의 경고와 함께 성공적인 실행을 의미한다. 이를테면 `+100`은 로우가 없음을 뜻한다.
  - 음수는 오류와 함께 성공하지 못했음을 의미한다. 이를테면 `-911`은 데드락이 발생하여 롤백을 트리거(trigger)했음을 뜻한다.

## 버전

### LUW

  - v8.1 - v8.2 - 코드명 Stinger
  - v9.1 - 코드명 Viper
  - v9.5 - 코드명 Viper2
  - v9.7 - 코드명 Cobra
  - v9.8 - Only Pure Scale
  - v10.1 - 코드명 Galilleo
  - v10.5 - 코드명 Kepler (Blu Acceleration.)

## 같이 보기

  - [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")
  - [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)

## 참조

<references />

## 외부 링크

  - [DB2 홈페이지 - ibm.com](http://www-01.ibm.com/software/data/db2)

[분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [분류:IBM 소프트웨어](https://ko.wikipedia.org/wiki/분류:IBM_소프트웨어 "wikilink") [분류:관계형 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:관계형_데이터베이스_관리_시스템 "wikilink")

1.
2.