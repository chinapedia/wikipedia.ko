> This article is converted from Wikipedia: [SQL](https://ko.wikipedia.org/wiki/SQL).


[섬네일](https://ko.wikipedia.org/wiki/파일:SQL_ANATOMY_wiki.svg "wikilink")

**SQL**(,\[1\] or , \[2\]\[3\]\[4\]\[5\], 구조화 질의어, S-Q-L\[6\])는 [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)의 데이터를 관리하기 위해 설계된 특수 목적의 [프로그래밍 언어이다](../Page/프로그래밍_언어.md "wikilink"). 관계형 데이터베이스 관리 시스템에서 자료의 검색과 관리, [데이터베이스 스키마](https://ko.wikipedia.org/wiki/데이터베이스_스키마 "wikilink") 생성과 수정, 데이터베이스 객체 접근 조정 관리를 위해 고안되었다. 많은 수의 데이터베이스 관련 프로그램들이 SQL을 표준으로 채택하고 있다.

## 역사

SQL은 [IBM](../Page/IBM.md "wikilink")에서 1970년대 초에 [도널드 D. 챔벌린과](https://ko.wikipedia.org/wiki/도널드_D._챔벌린 "wikilink") [레이먼드 F. 보이스가](https://ko.wikipedia.org/wiki/레이먼드_F._보이스 "wikilink") 처음 개발하였다. 초기에는 **SEQUEL**(Structured English Query Language, 구조 영어 질의어)라는 이름으로 시작하였으며, IBM의 준 관계형 데이터베이스 관리 시스템 [시스템 R에](../Page/IBM_시스템_R.md "wikilink") 저장된 데이터를 조작하고 수신하기 위해 고안되었다.\[7\] SEQUEL은 나중에 SQL로 바뀌었는데, 그 까닭은 SEQUEL이 [영국](../Page/영국.md "wikilink")의 [호커 시들리](https://ko.wikipedia.org/wiki/호커_시들리 "wikilink") 항공사의 상표였기 때문이다.\[8\]

## 설계

SQL은 [관계형 모델과](../Page/관계형_모델.md "wikilink") 그것의 [튜플 해석이라는](https://ko.wikipedia.org/wiki/튜플_관계_해석 "wikilink") 이론적 기초로부터 파생되었다. 해당 모델에서 테이블은 튜플의 집합이지만, SQL에서는 테이블과 쿼리 결과는 열의 목록이다. 같은 열은 여러 번 발생할 수 있고 열의 순서는 쿼리에 의해 나타난다. (예: LIMIT 절)

## SQL 구문

### 명령어 종류

[데이터베이스 언어](../Page/데이터베이스_언어.md "wikilink") SQL 문법의 종류는 다음 세 가지로 대별된다.

  - [데이터 정의 언어](../Page/데이터_정의_언어.md "wikilink") (DDL : Data Definition Language)
  - [데이터 조작 언어](../Page/데이터_조작_언어.md "wikilink") (DML : Data Manipulation Language)
  - [데이터 제어 언어](../Page/데이터_제어_언어.md "wikilink") (DCL : Data Control Language)

기타 이러한 명령의 적용 범위를 보완하기 위한 기능으로 SQL 문을 실행 시에 해석하는 "동적 SQL"과 [내장 SQL에](https://ko.wikipedia.org/wiki/내장_SQL "wikilink") 대한 지침이 포함되어 있다. [관계형 데이터베이스 관리시스템](https://ko.wikipedia.org/wiki/관계형_데이터베이스_관리시스템 "wikilink")(RDBMS) 이전의 [데이터베이스 관리 시스템](../Page/데이터베이스_관리_시스템.md "wikilink")(DBMS)에서 이들은 반드시 동일한 언어가 아니었다. 데이터 정의 언어는 존재하지 않고, 모든 전용 명령에 매개 변수를 사용하여 실행하는 구현도 존재했다.

### 명령어 문법

#### 데이터 정의 언어

  - [CREATE](../Page/CREATE_\(SQL\).md "wikilink") (데이터베이스 개체 (테이블, 인덱스, 제약조건 등)의 정의)
  - [DROP](https://ko.wikipedia.org/wiki/DROP_\(SQL\) "wikilink") (데이터베이스 개체 삭제)
  - [ALTER](../Page/ALTER_\(SQL\).md "wikilink") (데이터베이스 개체 정의 변경)

[데이터 정의 언어는](../Page/데이터_정의_언어.md "wikilink") [테이블과](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink") [인덱스](../Page/인덱스_\(데이터베이스\).md "wikilink") 구조를 관리한다. DDL의 가장 기본적인 요소는 [CREATE](../Page/CREATE_\(SQL\).md "wikilink"), [ALTER](../Page/ALTER_\(SQL\).md "wikilink"), [RENAME](https://ko.wikipedia.org/wiki/RENAME_\(SQL\) "wikilink"), [DROP과](https://ko.wikipedia.org/wiki/DROP_\(SQL\) "wikilink") [TRUNCATE](../Page/TRUNCATE_\(SQL\).md "wikilink") 구문이다:

[CREATE는](../Page/CREATE_\(SQL\).md "wikilink") 데이터베이스에서 객체(예, 테이블)를 생성한다. 예를 들어:

``` sql
CREATE TABLE My_table(
 my_field1 INT,
 my_field2 VARCHAR(50),
 my_field3 DATE NOT NULL,
 PRIMARY KEY (my_field1, my_field2)
);
```

  - [`ALTER`](https://ko.wikipedia.org/wiki/Alter_\(SQL\) "wikilink")는 다양한 방법으로 현존하는 객체의 구조를 변경한다. 예를 들어, 현재의 테이블에 컬럼을 추가하거나 제한을 추가한다. 예를 들면:

<!-- end list -->

``` sql
ALTER TABLE My_table ADD my_field4 NUMBER(3) NOT NULL;
```

  - [`TRUNCATE`](https://ko.wikipedia.org/wiki/Truncate_\(SQL\) "wikilink")는 테이블에서 모든 데이터를 빠르게 삭제한다. 내부 테이블의 데이터를 삭제하는 것이지, 테이블 자체를 삭제하는 것은 아니다. 이 과정은 보통 순차적인 [COMMIT](../Page/COMMIT.md "wikilink") 연산을 내포한다. 예를 들어, 이것은 롤백되지 않는다. (DELETE와는 달리 이후 롤백을 위한 로그가 기록되지 않는다.).

<!-- end list -->

``` sql
TRUNCATE TABLE My_table;
```

  - [`DROP`](https://ko.wikipedia.org/wiki/Drop_\(SQL\) "wikilink")은 데이터베이스에서 객체를 삭제하며, 보통 [롤백을](../Page/롤백_\(데이터_관리\).md "wikilink") 통해 복원할 수 없다. 예를 들어:

<!-- end list -->

``` sql
DROP TABLE My_table;
```

#### 데이터 조작 언어

  - [INSERT](https://ko.wikipedia.org/wiki/INSERT_\(SQL\) "wikilink") INTO (행 데이터 또는 테이블 데이터의 삽입)
  - [UPDATE](https://ko.wikipedia.org/wiki/UPDATE_\(SQL\) "wikilink") \~ SET (표 업데이트)
  - [DELETE](https://ko.wikipedia.org/wiki/DELETE_\(SQL\) "wikilink") FROM (테이블에서 특정 행 삭제)
  - [SELECT](https://ko.wikipedia.org/wiki/SELECT_\(SQL\) "wikilink") \~ FROM \~ WHERE (테이블 데이터의 검색 결과 집합의 취득)

<!-- end list -->

  -
    뒷부분의 “동적 SQL”에서 SELECT 문은 한 번 실행에 1행의 결과를 얻는 “단일행 SELECT 문장”과 커서로 여러 줄의 결과를 얻는 “커서 SELECT 문”이 있다.

#### 데이터 제어 언어

  - GRANT (특정 데이터베이스 사용자에게 특정 작업을 수행 권한을 부여)
  - REVOKE (특정 데이터베이스 이용자로부터 이미 준 권한을 박탈 함.)
  - SET TRANSACTION ( 트랜잭션 모드 설정 (동시 트랜잭션 격리 수준 (ISOLATION MODE) 등))
  - BEGIN ([트랜잭션](https://ko.wikipedia.org/wiki/트랜잭션 "wikilink") 시작)
  - [COMMIT](../Page/COMMIT.md "wikilink") (트랜잭션의 실행)
  - [ROLLBACK](../Page/롤백_\(데이터_관리\).md "wikilink") (트랜잭션 취소)
  - [SAVEPOINT](../Page/SAVEPOINT.md "wikilink") (무작위로 롤백 지점을 설정)
  - LOCK (표 등의 자원을 차지)

#### 커서 정의 및 사용

‘커서’는 SELECT 문장 등에 의한 데이터베이스 검색에 의한 검색 실행 결과를 한 줄씩 검색하고, 처리하기 위해 데이터베이스 서버 측의 결과 집합과 행 획득 위치를 나타내는 개념을 말한다. 커서의 정의와 그 작업은 주로 응용 프로그램 등의 절차적 언어에서의 SQL 실행시 사용한다.

  - DECLARE CURSOR (커서 정의)
  - OPEN (커서 열기)
  - FETCH (커서 포인터가 가리키는 위치의 행 데이터를 검색하고 포인터를 일행 분 진행)
  - UPDATE (커서 포인터가 가리키는 위치의 행 데이터 업데이트)
  - DELETE (커서 포인터가 가리키는 위치의 행 데이터 삭제)
  - CLOSE (커서 닫기)

### 연산자

| 연산자         | 설명                |
| ----------- | ----------------- |
| \=          | 같음                |
| \<\> 또는 \!= | 같지 않음             |
| \>          | 보다 큼              |
| \<          | 보다 작음             |
| \>=         | 보다 크거나 같음         |
| \<=         | 보다 작거나 같음         |
| BETWEEN     | 일정 범위 사이          |
| LIKE        | 패턴 검색             |
| IN          | 컬럼의 여러 가능한 값들을 지정 |
|             |                   |

### 조건 표현

SQL은 `case/when/then/else/end` 표현을 가지고 있으며, 이것은 [SQL-92](https://ko.wikipedia.org/wiki/SQL-92 "wikilink")에서 도입되었다. 일반적인 형식에서, 이것은 SQL 표준에서 "searched case"라고 불리며, 다른 프로그램 언어에서 [else if와](https://ko.wikipedia.org/wiki/Conditional_\(programming\)#Else_if "wikilink") 같은 역할을 수행한다:

``` sql
CASE WHEN n > 0 THEN 'positive' WHEN n < 0 THEN 'negative' ELSE 'zero' END
```

`WHEN` 조건은 소스에서 등장하는 순서에서 시험된다. 아무런 `ELSE` 표현식이 지정되지 않으면, `ELSE NULL`을 기본값으로 하게 된다. [switch statement을](https://ko.wikipedia.org/wiki/switch_statement "wikilink") 미러링하는 약어 구문도 존재한다. 이것은 SQL 표준에서 "simple case"라고 불린다:

``` sql
CASE n WHEN 1 then 'one' WHEN 2 THEN 'two' ELSE 'i cannot count that high' END
```

이 구문은 [NULL과 비교하는 통상적인 경고을](https://ko.wikipedia.org/wiki/Null_\(SQL\)#CASE_expressions "wikilink") 이용하여 내포적 특질 비교를 이용한다.

오라클 SQL 구문에서 후자는 `DECODE` 구문으로 축약될 수 있다:

``` oracle8
SELECT DECODE(n, 1, "one", 2, "two", "i cannot count that high") FROM some_table;
```

마지막 값은 default이다; 아무것도 지정되지 않으면, `NULL`이 기본값이 된다. 그러나 표준 "simple case"와는 달리 오라클의 `DECODE`는 2개의 `NULL`을 서로 동일한 것으로 간주한다.\[9\]

## 자료형

SQL 테이블에서 각 컬럼은 컬럼이 포함하는 [자료형](../Page/자료형.md "wikilink")(data type)을 선언한다. ANSI SQL은 다음과 같은 데이터형을 포함하고 있다.\[10\]

#### 문자열

  - `CHARACTER(`<var>`n`</var>`)` 또는 `CHAR(`<var>`n`</var>`)`: 고정폭 <var>n</var>-문자열, (필요한만큼 공백으로 채워진다.)
  - `CHARACTER VARYING(`<var>`n`</var>`)` 또는 `VARCHAR(`<var>`n`</var>`)`: 가변폭 문자열 (<var>n</var> 문자의 최대 크기를 가진)
  - `NATIONAL CHARACTER(`<var>`n`</var>`)` 또는 `NCHAR(`<var>`n`</var>`)`: 국제 문자셋을 지원하는 고정폭 문자열
  - `NATIONAL CHARACTER VARYING(`<var>`n`</var>`)` 또는 `NVARCHAR(`<var>`n`</var>`)`: 가변폭 `NCHAR` 문자열

#### 비트 열

  - `BIT(`<var>`n`</var>`)`: <var>n</var> 비트의 배열
  - `BIT VARYING(`<var>`n`</var>`)`: <var>n</var> 비트까지의 배열

#### 수

  - `INTEGER` 와 `SMALLINT`
  - `FLOAT`, `REAL` 과 `DOUBLE PRECISION`
  - `NUMERIC(`<var>`precision`</var>` ,  `<var>`scale`</var>`)` 또는 `DECIMAL(`<var>`precision`</var>` ,  `<var>`scale`</var>`)`

예를 들어, 숫자 123.45는 5라는 precision(정밀도, 자리값)과 2라는 scale(소수점 이하 자릿수)을 포함하고 있다. <var>precision</var>은 특정 진법(이진법 또는 십진법)에서 중요한 10자리수를 결정하는 양의 정수값이다. <var>scale</var>은 음이 아닌 정수이다. 0의 scale은 그 수가 정수임을 지시하는 숫자이다. S 자릿수를 가진 10진법에서, 정확한 숫자값은 10<sup>S</sup>로 나눈 중요한 10진법 정수값이다.

SQL은 숫자, 날짜를 반올림해주는 `TRUNC` (인포믹스, DB2, PostgreSQL, 오라클 그리고 MySQL에서) 또는 `ROUND` (인포믹스, SQLite, Sybase, Oracle, PostgreSQL and Microsoft SQL Server) 함수를 제공한다.\[11\]

#### 날짜와 시간

  - `DATE`: 날짜 값 (예, `2011-05-03`)
  - `TIME`: 시간 값 (예, `15:51:36`). 시간 값은 보통 *tick* (100 nanoseconds)이다.
  - `TIME WITH TIME ZONE` or `TIMETZ`: `TIME`과 같지만, 해당 지역의 시간대 정보를 포함하고 있다.
  - `TIMESTAMP`: 이것은 `DATE` 와 `TIME`이 하나의 변수로 결합된 것이다. (예, `2011-05-03 15:51:36`).
  - `TIMESTAMP WITH TIME ZONE` or `TIMESTAMPTZ`: `TIMESTAMP`와 동일하지만, 해당 지역의 시간대에 대한 상세 정보를 포함하고 있다.

SQL은 날짜 / 시간 변수를 생성하는 여러 개의 함수를 date / time 열 (`TO_DATE`, `TO_TIME`, `TO_TIMESTAMP`)로부터 제공한다. 또한 그러한 각각의 변수 항목 (예를 들면, 초)을 통해 추출할 수도 있다. 현재 데이터베이스 서버 시스템의 날짜 / 시간은 `NOW`와 같은 함수를 통해 호출할 수 있다.

## SQL 기타

### 동적 SQL

동적 SQL은 일반적으로 SQL문을 RDBMS에 보낼 때마다 데이터베이스 엔진에서 실행 가능한 내부 중간 코드로 번역하는 작업을 미리 수행하여 변환된 SQL 코드를 재사용하여, SQL 분석 오버헤드를 줄이고, SQL 문을 소스 코드로 고정하지 않고 데이터베이스에 액세스할 때마다 구문을 다시 할 경우 유용하다. [데이터 조작 언어](../Page/데이터_조작_언어.md "wikilink")(DML)도 물론 수행할 수 있지만, [데이터 정의 언어](../Page/데이터_정의_언어.md "wikilink") (DDL)와 같이 데이터베이스 제품의 기능 업데이트에 의해 새로운 명령이 추가되는 것은 전처리 해당 작업이 부담이 되기 때문에, 대부분의 데이터베이스 제품에서는 DDL 문은 동적 SQL에서 실행하는 것이 일반적이다.

  - PREPARE (문자열로 준 SQL 문을 해석, 번역)
  - EXECUTE (PREPARE로 번역한 SQL 문을 실행)

### 임베디드 SQL

임베디드 SQL(또는 내장 SQL)은 원래 커서가 포함된 SQL에서 호스트 언어에서 결과 집합을 얻기 위해 더 편리한 방법으로 고안된 것이다. 데이터베이스와 통신하기 위한 자원 할당 확보와 개방한 줄에 호스트 언어의 반복으로 가져 오기위한 명령 (FETCH) 등이 있다.

  - ALLOCATE (DEALLOCATE) DESCRIPTOR (데이터베이스 및 호스트 언어 간 통신 영역의 확보와 개방)
  - WHENEVER (오류 발생시의 동작을 정의)
  - SQLSTATE (SQL 문 실행 후 상태가 저장되는 영역)

### 3값 논리

SQL에서 사용되는 논리값은 컴퓨터 세계에서 가장 널리 이용되는 ‘2값 논리’(TRUE, FALSE) 대신 ‘3값 논리’(TRUE, FALSE, UNKNOWN)이 있다.

## 언어 요소

  - 절(clauses)
  - 식(expressions)
  - 술어(predicates)
  - 질의(queries)
  - 문(statements)

## 표준화

SQL 표준은 다음과 같은 많은 개정을 거쳤다:

| 년도   | 명칭                                                            | 별칭                                                                                             | 설명                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ---- | ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1986 | SQL-86                                                        | SQL-87                                                                                         | ANSI에 의한 최초의 표준화.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 1989 | SQL-89                                                        | [FIPS](https://ko.wikipedia.org/wiki/Federal_Information_Processing_Standard "wikilink") 127-1 | 마이너 개정, integrity constraints가 추가. FIPS 127-1에서 채택.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 1992 | [SQL-92](https://ko.wikipedia.org/wiki/SQL-92 "wikilink")     | SQL2, FIPS 127-2                                                                               | 매이저 개정 (ISO 9075), *Entry Level* SQL-92은 FIPS 127-2로 채택.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 1999 | [SQL:1999](https://ko.wikipedia.org/wiki/SQL:1999 "wikilink") | SQL3                                                                                           | 정규 표현식 매칭 추가, [재귀 쿼리](https://ko.wikipedia.org/wiki/재귀_쿼리 "wikilink") (예, [이행적 폐쇄](https://ko.wikipedia.org/wiki/이행적_폐쇄 "wikilink")), [데이터베이스 트리거](../Page/데이터베이스_트리거.md "wikilink"), 절차적, 통제흐름 구문 지원, 비규격 타입 그리고 객체지향형 특징 지원(예, [구조화 타입](https://ko.wikipedia.org/wiki/구조화_타입 "wikilink")). 자바에서 [내장 SQL](https://ko.wikipedia.org/wiki/내장_SQL "wikilink") 지원([SQL/OLB](https://ko.wikipedia.org/wiki/SQL/OLB "wikilink")) 그리고 ([SQL/JRT](https://ko.wikipedia.org/wiki/SQL/JRT "wikilink")). |
| 2003 | [SQL:2003](https://ko.wikipedia.org/wiki/SQL:2003 "wikilink") | SQL 2003                                                                                       | [XML](../Page/XML.md "wikilink") 관련 특징 도입 ([SQL/XML](https://ko.wikipedia.org/wiki/SQL/XML "wikilink")), *window functions*, 자동생성값에 대한 표준화된 시퀀스와 컬럼(아이덴티티 컬럼 포함).                                                                                                                                                                                                                                                                                                                              |
| 2006 | [SQL:2006](https://ko.wikipedia.org/wiki/SQL:2006 "wikilink") | SQL 2006                                                                                       | ISO/IEC 9075-14:2006은 XML과 결합되어 SQL이 사용되는 방법을 정의하고 있다. 여기에는 SQL 데이터베이스 내의 XML 데이터의 불러오기와 저장하는 방법을 정의하고 있으며, 데이터베이스 내에서 조작하여 XML 형식의 전통적 SQL 자료와 XML 형식 모두로 출력하는 방법을 제시한다. 게다가, 여기에서는 W3C에 의해 제안된 XML 쿼리 언어, [Xquery](https://ko.wikipedia.org/wiki/Xquery "wikilink")를 이용하여 SQL 코드로 애플리케이션을 통합할 수 있도록 하여, 보통의 SQL 데이터와 XML 문서에 접근할 수 있게 한다.\[12\]                                                                                                                                              |
| 2008 | [SQL:2008](../Page/SQL:2008.md "wikilink")                    | SQL 2008                                                                                       | 커서 정의 외부의 ORDER BY를 합법화 . INSTEAD OF [트리거](../Page/데이터베이스_트리거.md "wikilink") 추가. [TRUNCATE](../Page/TRUNCATE_\(SQL\).md "wikilink") 구문 추가.\[13\]                                                                                                                                                                                                                                                                                                                                               |
| 2011 | [SQL:2011](../Page/SQL:2011.md "wikilink")                    | SQL 2011                                                                                       | [임시 데이터베이스에](https://ko.wikipedia.org/wiki/임시_데이터베이스 "wikilink") 대한 지원 향상                                                                                                                                                                                                                                                                                                                                                                                                                      |

### 표준 구조

  - ISO/IEC 9075-1:2011 Part 1: 프레임워크 (SQL/Framework)
  - ISO/IEC 9075-2:2011 Part 2: 파운데이션 (SQL/Foundation)
  - ISO/IEC 9075-3:2008 Part 3: 호출 수준 인터페이스 ([SQL/CLI](https://ko.wikipedia.org/wiki/SQL/CLI "wikilink"))
  - ISO/IEC 9075-4:2008 Part 4: 지속 저장 모듈 ([SQL/PSM](https://ko.wikipedia.org/wiki/SQL/PSM "wikilink"))
  - ISO/IEC 9075-9:2008 Part 9: 외부 데이터 관리 ([SQL/MED](https://ko.wikipedia.org/wiki/SQL/MED "wikilink"))
  - ISO/IEC 9075-10:2008 Part 10: 오브젝트 언어 결합 ([SQL/OLB](https://ko.wikipedia.org/wiki/SQL/OLB "wikilink"))
  - ISO/IEC 9075-11:2011 Part 11: 정보 및 정의 스키마 ([SQL/Schemata](https://ko.wikipedia.org/wiki/SQL/Schemata "wikilink"))
  - ISO/IEC 9075-13:2008 Part 13: 자바 프로그래밍 언어를 이용한 SQL 루틴 및 형식([SQL/JRT](https://ko.wikipedia.org/wiki/SQL/JRT "wikilink"))
  - ISO/IEC 9075-14:2011 Part 14: XML 관련 규격 ([SQL/XML](https://ko.wikipedia.org/wiki/SQL/XML "wikilink"))

ISO/IEC 9075은 ISO/IEC 13249 SQL 멀티미디어 및 응용 프로그램 패키지로 보충된다.

  - ISO/IEC 13249-1:2007 Part 1: 프레임워크
  - ISO/IEC 13249-2:2003 Part 2: 전문(Full-Text)
  - ISO/IEC 13249-3:2011 Part 3: 공간
  - ISO/IEC 13249-5:2003 Part 5: 정적 이미지
  - ISO/IEC 13249-6:2006 Part 6: 데이터 마이닝
  - ISO/IEC 13249-8:xxxx Part 8: 메타데이터 등록 (MDR) (진행 중)

## 같이 보기

  - [관계대수](https://ko.wikipedia.org/wiki/관계대수 "wikilink")
  - [NoSQL](../Page/NoSQL.md "wikilink")

## 참조

<references />

## 외부 링크

  - [*1995 SQL Reunion: People, Projects, and Politics*, by Paul McJones (ed.)](http://www.mcjones.org/System_R/SQL_Reunion_95/sqlr95.html): transcript of a reunion meeting devoted to the personal history of relational databases and SQL.
  - [American National Standards Institute. X3H2 Records, 1978–1995](http://special.lib.umn.edu/findaid/xml/cbi00168.xml) [Charles Babbage Institute](https://ko.wikipedia.org/wiki/Charles_Babbage_Institute "wikilink") Collection documents the H2 committee's development of the NDL and SQL standards.
  - [Oral history interview with Donald D. Chamberlin](http://purl.umn.edu/107215) [Charles Babbage Institute](https://ko.wikipedia.org/wiki/Charles_Babbage_Institute "wikilink") In this oral history Chamberlin recounts his early life, his education at [Harvey Mudd College](https://ko.wikipedia.org/wiki/Harvey_Mudd_College "wikilink") and [Stanford University](https://ko.wikipedia.org/wiki/Stanford_University "wikilink"), and his work on relational database technology. Chamberlin was a member of the System R research team and, with [Raymond F. Boyce](https://ko.wikipedia.org/wiki/Raymond_F._Boyce "wikilink"), developed the SQL database language. Chamberlin also briefly discusses his more recent research on XML query languages.
  - [Comparison of Different SQL Implementations](http://troels.arvin.dk/db/rdbms/) This comparison of various SQL implementations is intended to serve as a guide to those interested in porting SQL code between various RDBMS products, and includes comparisons between SQL:2008, PostgreSQL, DB2, MS SQL Server, MySQL, Oracle, and Informix.

[SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink") [분류:선언형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:선언형_프로그래밍_언어 "wikilink") [분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [분류:질의어](https://ko.wikipedia.org/wiki/분류:질의어 "wikilink") [분류:관계형 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:관계형_데이터베이스_관리_시스템 "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:데이터 모델링 언어](https://ko.wikipedia.org/wiki/분류:데이터_모델링_언어 "wikilink")

1.
2.
3.  From Oxford Dictionaries: "Definition of SQL - abbreviation, Structured Query Language, an international standard for database manipulation."
4.
5.  From Microsoft: "Structured Query Language, invented at IBM in the 1970s. It is more commonly known by its acronym, SQL .."
6.
7.
8.
9.  <http://docs.oracle.com/cd/B19306_01/server.102/b14200/functions040.htm>
10. {{ 저널 인용 | url = <http://www.contrib.andrew.cmu.edu/~shadow/sql/sql1992.txt> | 제목 = Information Technology: Database Language SQL | publisher = CMU }} (proposed revised text of DIS 9075)\].
11. Arie Jones, Ryan K. Stephens, Ronald R. Plew, Alex Kriegel, Robert F. Garrett (2005), *SQL Functions Programmer's Reference*. Wiley, 127 pages.
12. {{ 서적 인용 | 제목=SQL/XML:2006 - Evaluierung der Standardkonformität ausgewählter Datenbanksysteme | last=Wagner | first=Michael | coauthors= | year=2010 | publisher=Diplomica Verlag | isbn=3-8366-9609-6 | page=100 | chapter= | quote=}}
13. {{ 저널 인용 | date = 2008-7 | 제목 = SQL:2008 now an approved ISO international standard | publisher = Sybase | url = <http://iablog.sybase.com/paulley/2008/07/sql2008-now-an-approved-iso-international-standard/> | 확인날짜 = 2011년 6월 28일 | 보존url = <https://web.archive.org/web/20110628130925/http://iablog.sybase.com/paulley/2008/07/sql2008-now-an-approved-iso-international-standard/> | 보존날짜 = 2011년 6월 28일 | url-status = dead }}.