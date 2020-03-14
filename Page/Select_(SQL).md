> This article is converted from Wikipedia: [Select \(SQL\)](https://ko.wikipedia.org/wiki/Select_\(SQL\)).


[SQL](https://ko.wikipedia.org/wiki/SQL "wikilink") **SELECT**문은 하나 또는 그 이상의 [테이블에서](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink") 데이터를 추출하는 [SQL](https://ko.wikipedia.org/wiki/SQL "wikilink")의 [데이터 조작 언어](../Page/데이터_조작_언어.md "wikilink")(DML) 중 하나이다. 이것은 [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink") 중 하나 또는 그 이상의 테이블에서 데이터를 추출하기 위한 명령으로 데이터 조작 언어 (DML)에서 가장 많이 사용된다. 프로그래머는 어떤 결과를 갖고 싶은 것인지를 SQL 문장으로 기술할 필요는 있지만, 그 결과를 얻기 위해 어떤 물리적인 작업이 수행되는 지를 지시하지 않아도, 데이터베이스 시스템(쿼리 최적화)이 SQL 문에서 최적의 쿼리 계획(실행 계획)을 작성한다.

덧붙여 "테이블"은 "표", "행"은 "레코드", "열"은 "항목"이라고 부르기도 한다. 다음과 같은 선택 절을 가진다.

  - `WHERE` : 어떤 열을 불러올 지를 지정.
  - `GROUP BY` : [연산 함수가](https://ko.wikipedia.org/wiki/연산_함수 "wikilink") 각 그룹에 적용되도록 하기 위해 속성을 그룹 열에 공유하는 것
  - `HAVING` : GROUP BY 절에서 정의된 그룹들 중에서 검색
  - `ORDER BY` : 반환하는 열에 순서를 지정

## 구문

``` sql
 SELECT [ALL | DISTINCT] 컬럼명 [,컬럼명...]
 FROM 테이블명 [,테이블명...]
 [WHERE 조건식]
 [GROUP BY 컬럼명 [HAVING 조건식]]
 [ORDER BY 컬럼명]
 GROUP BY 컬럼명[,컬럼명...]
 ORDER BY 컬럼명[,컬럼명...]
```

### SELECT 절

SELECT 문에서 필수 구성 절. 지정 열을 설명하는 것으로, 열을 보여준다. \*로 하면 모든 열이 표시된다. 또한 산술 연산자, 그룹 함수를 사용할 수 있다.

#### 유효성 검사

컬럼명 유효성 검사 주된 것으로는

  - 열 이름에 사용할 수 있는 문자는 영문자, 숫자 및 $, \#, _ (밑줄)이 있다.
  - 열 이름의 첫 글자는 영문 알파벳만 가능.
  - 문자 상한은 최대 30자까지.
  - 기본값은 대문자로 표시된다. 문자 등으로 표시하려면 단일 행 함수를 사용하거나, ""로 둘러 싸는 등의 처리가 필요하다.
  - 각종 DBMS의 예약어는 사용할 수 없는 경우가 있다.

#### 컬럼 별칭

  -
    컬럼명 \[AS\] 컬럼 별칭 (AS는 생략 가능)

로 컬럼을 다른 이름으로 표시할 수 있다. 단, WHERE 절, GROUP BY 절, HAVING 절은 컬럼 별칭은 없다. 또한 컬럼명 표시시 기본은 영문 대문자이다. 이것을 문자 등으로 표시할 경우 단일행 함수, 문자 함수를 사용하거나 ""로 묶어서 표시를 한다.

#### ALL / DISTINCT 지정

  - ALL --- 테이블에 동일한 데이터 행이 있는 경우에도 모든 데이터를 반환한다. 지정하지 않으면 ALL이 선택
  - DISTINCT (UNIQUE) --- 테이블에 동일한 데이터 행이있는 경우 중복을 제거한 1 개만을 돌려 준다.

그룹함수는 COUNT만 사용 가능

#### 단일행 함수

단일행 조작 함수에서 하나의 행에 대해 하나의 결과를 반환하는 함수. SELECT 절, WHERE 절, ORDER BY 절에서 사용할 수 있으며, 다음과 같은 종류가 있다. 또한 중첩에 제한은 없다.

  - 문자 함수(CHARACTER FUNCTION)

<!-- end list -->

  -
    문자를 조작하는 함수입니다. LOWER, UPPER, INITCAP, CONCAT, SUBSTR, INSTR, LENGTH, TRIM, REPLACE 등이 있다.

<!-- end list -->

  - 숫자 함수(NUMBER FUNCTION)

<!-- end list -->

  -
    숫자를 조작하는 함수입니다. ROUND (반올림), TRUNC (자르기), MOD (나머지)가 있다.

<!-- end list -->

  - 날짜 함수(DATE FUNCTION)

<!-- end list -->

  -
    날짜를 조작하는 함수입니다.

<!-- end list -->

  - 데이터 형식 변환 함수.(Data Type)

<!-- end list -->

  -
    특정 데이터 형식을 특정 데이터 형식으로 변환 할 수 있다. TO_CHAR, TO_NUMBER, TO_DATE가 있다.

#### 그룹 함수

그룹화를 한 행에 대해 하나의 결과를 반환하는 함수. SELECT 절 (단, GROUP BY 절에 지정된 열만) HAVING 절,​​ ORDER BY 절에서 사용할 수 있다. 중첩은 2단계까지 가능하다. 종류로는 AVG (평균), MAX (최댓값), MIN (최솟값), SUM (합계), COUNT (반환되는 행 수) 등이 있다.

#### 집합 연산

여러 테이블에서 질의 결과를 참조하는 복합문을 처리하기 위한 연산자를 이용한 구문. UNION (합집합), UNION ALL (전체 집합), INTERSECT (교집합), EXCEPT(예외) ​​또는 MINUS (차집합)이 있지만, DBMS 환경에서 사용할 수 없거나 연산자의 명칭이 다른 것도 있다. 각 연산자의 우선 순위가 아니라 왼쪽에서 오른쪽으로 순서대로 처리된다. 주요 조건으로 다음과 같다.

  - 이 행을 일치시킬 필요가 있다.
  - 각 SELECT 절에 해당하는 행의 데이터 타입을 일치시킬 필요가 있다 (일부 데이터 형식에서 호환성 있는).
  - 데이터 크기는 일치하지 않아도 된다.
  - 조건을 만족하면 열 이름은 달라도 상관없다.
  - UNION ALL 이외는 정렬되어 반환된다. 기본값은 전문의 제1열이 기준이 된다.

### FROM 절

SELECT 문에서 필수 구성 절. FROM 절에서 열 참조를 가진 테이블을 지정한다. 여러 테이블에서 지정하면 결합이 이루어진 JOIN을 이용하는 것 외에 WHERE 절은 공통 열 결합 관계를 지정하는 것도 가능(단, 이 경우 OUTER JOIN은 불가능하다. 그러나, OracleDBMS의 경우 (+)라는 특수 기호를 사용하여 외부 조인을 수행할 수 있다.). 또한, 표를 필요로 하지 않는 쿼리를 할 경우에도 DUAL 테이블과 같은 더미 표를 지정하는 것이 가능하지만, 이러한 경우 FROM을 생략 할 수 있는 확장이 행해진 처리계도 많이 존재한다.

이 FROM 절에서 테이블 별칭 지정이 가능하지만 일단 테이블 별칭을 지정하면 테이블 별명으로 묘사 해주지 않으면 에러가난다.

#### 결합 (JOIN 절)

여러 테이블에서 행을 참조하는 경우에 이용해 조인(JOIN)을 사용하는 경우가 많다. 종류로는 다음과 같은 것들이 있다.

  - 크로스 조인
  - 내부 조인 (등가결합 비균등 조인, 자연 조인, 자체 조인 포함)
  - 외부 조인

<!-- end list -->

  -
    한편 또는 쌍방의 값에 NULL 값을 포함하는 경우에 사용된다. 왼쪽 외부 조인, 오른쪽 외부 조인, 완전 외부 조인의 3종류가 있다.

등가 결합의 일반적인 형식은 아래와 같다.

``` sql
SELECT 임의테이블명.공통컬럼 FROM 테이블명A [INNER] JOIN 테이블명B ON 테이블A.공통컬럼 = 테이블B.공통컬럼;
```

여기에 테이블명은 설명의 간편화를 도모하기 위해 명칭을 표시하는 경우가 많다. 이 경우 일반적인 컬럼에는 반드시 테이블 별칭으로 설명하지 않으면 에러가 발생한다. 또한 SELECT 절에서 공통 컬럼은 반드시 어떤 표인지를 지정하지 않으면 안된다.(이것을 테이블 규정이라고 함) 기타 일반적이지 않은 컬럼은 반드시 테이블을 정하지 않아도 좋지만 성능이 저하되므로 테이블 규정하는 습관이 바람직하다고 여겨지고 있다.

기타 NATURAL JOIN (자연 조인) 또는 USING 절(공통열 한정)을 사용하는 경우가 있다. 이러한 경우에도 여러 가지 세세한 제약이 발생한다.

### WHERE 절

WHERE 절은 데이터를 추출하는 선택 조건식을 지정한다. 단일 식을 이용하는 것 외에도, 여러 조건을 조회하는 경우도 많다. 또한 테이블 간의 결합할 때 그 결합 관계를 지정한다. 이 WHERE 절에 그룹 함수를 사용해서는 안된다는 규칙이 존재한다.

#### 패턴 매칭 검색

SQL 문은 다음 도식을 이용하여 부분 일치 검색이 가능하다. 패턴 일치에 사용되는 와일드 카드에는 "%"가 있다. 형식은 아래와 같다.

  -
    WHERE 열 이름 LIKE 'A%'

열 이름의 'A'문자값이 해당 데이터 앞부분에 있다면 SELECT 된다.(EX. APPLE, CANON, DEAM등 )

'A'문자 뒤에 어떠한 값이 들어와도 검색이 된다.(아무 값도 없어도 된다.)

'%'는 문자 앞과 뒤에 모두 사용이 가능하다.

'%A' 또는 'A%' 또는 '%A%'

### GROUP BY 절

GROUP BY 절은 그룹화 열 또는 컬럼명을 포함하는 식을 지정한다. 컬럼 별명은 사용할 수 없다. 또한 SELECT 문에서 GROUP BY 절에서 그룹 함수를 제외하고 그룹화되지 않은 열이 존재하면 함께 작성해야 한다.

  -
    예 : SELECT A. B FROM LIST GROUP BY A, B;

(그룹화하는 것은 A지만 B 라인도 함께 설명하지 않으면 오류가 난다.)

또한 GROUP BY 절을 포함하면 뷰를 만들 수 없다. (SELECT 문에서 그룹 함수를 사용하는 경우 또는 DISTINCT 절을 사용하는 경우에도 동일)

### HAVING 절

HAVING 절은 GROUP BY 절에 집계한 결과에 조건을 정해줄 때 사용한다. 그룹 함수의 사용이 가능하다. 순서는 GROUP BY 절과 전후가 되어도 상관없다.

### ORDER BY 절

ORDER BY 절은 정렬할 컬럼 또는 컬럼을 포함하는 식을 지정하는 것으로 어떠한 경우에도 구문의 마지막에 지정한다. 쉼표로 구분하여 여러 열을 지정할 수 있다. 일반적으로 ASC (ascending order), 즉 오름차순 지정이며, 내림차순 지정하려면 DESC (descending order)로 표기한다. 또한 열 이름으로 지정이 가능하며, 서수 지정이 가능하다. (예를 들어, 두 번째 열에서 참조하고 싶은 경우, ORDER BY 2로 할 수 있다.)

여기에서 NULL은 무한대의 값으로 간주되어, 오름차순의 경우는 마지막에, 내림차순 경우 처음에 표시된다.

## 외부 링크

  - [Windowed Tables and Window function in SQL](http://wwwlgis.informatik.uni-kl.de/cms/fileadmin/courses/SS2008/NEDM/RDDM.Chapter.06.Windows_and_Query_Functions_in_SQL.pdf), Stefan Deßloch
  - [Oracle SELECT 구문.](http://download.oracle.com/docs/cd/B14117_01/server.101/b10759/statements_10002.htm)
  - [Firebird SELECT 구문.](http://www.firebirdsql.org/rlsnotesh/rlsnotes210.html#rnfb20x-dml-select-syntax)
  - [Mysql SELECT 구문.](http://dev.mysql.com/doc/refman/5.1/en/select.html)
  - [Postgres SELECT 구문.](http://www.postgresql.org/docs/current/static/sql-select.html)
  - [SQLite SELECT 구문.](http://www.sqlite.org/lang_select.html)

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")