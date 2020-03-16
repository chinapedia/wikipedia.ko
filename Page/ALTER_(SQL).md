> This article is converted from Wikipedia: [ALTER \(SQL\)](https://ko.wikipedia.org/wiki/ALTER_\(SQL\)).


SQL의 **ALTER**문은 [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)의 관리 하에 이미 존재하는 개체의 특성을 변경하는 [데이터 정의 언어](../Page/데이터_정의_언어.md "wikilink")(DDL) 명령이다. 사용하는 RDBMS의 구현을 통해 ALTER 문에 의해 변경될 수 있는 개체 유형(테이블, 컬럼)은 다르다. ALTER 구문은 주로 컬럼명을 바꾸는데 사용하며, 오라클, 큐브리드 등 대체로 테이블명 변경은 RENAME을 사용한다.

## 구문

기본적인 사용 방법은 다음과 같다.

`ALTER `*`개체형식``   ``개체명``   ``[매개변수]`*

## 예제

### 컬럼

"Employee"라는 이름으로 이미 존재하는 테이블에 대해 "Birthday"라는 열을 추가 (그리고 삭제)하는 명령의 예를 나타낸다.

``` sql
ALTER TABLE Employee ADD Birthday DATE;
ALTER TABLE Employee DROP COLUMN Birthday;
```

### 테이블

오라클과 MySQL 등의 데이터베이스에서 테이블명을 변경할 때 다음과 같이 한다.

`ALTER TABLE `*`Old_Table_Name`*` RENAME TO `*`New_Table_Name`*`;`

### 데이터베이스

데이터베이스 이름 변경은 각 데이터베이스 제품마다 차이가 있다.

#### Microsoft SQL Server

`ALTER DATABASE `*`Old_DB`*` MODIFY NAME=New_DB`
`sp_renamedb 'Old_DB','New_DB'`

#### MySQL

기본적으로 데이터베이스명 변경을 허용하지 않다가 5.1.7 버전에서 rename database 구문을 등록한 후 위험 가능성이 높은 구문으로 판단하고 5.1.23 버전에서 다시 제거 됐다. 그러나 아래와 같은 방법으로 셸에서 데이터베이스명을 변경할 수 있다.

``` mysql
create database new_database;
rename table old_database.table to new_database.table
```

## 같이 보기

  - [RENAME (SQL)](https://ko.wikipedia.org/wiki/RENAME_\(SQL\) "wikilink")

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")