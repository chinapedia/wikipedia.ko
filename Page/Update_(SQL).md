> This article is converted from Wikipedia: [Update \(SQL\)](https://ko.wikipedia.org/wiki/Update_\(SQL\)).


**UPDATE** 문은 [구조화 질의어](https://ko.wikipedia.org/wiki/구조화_질의어 "wikilink") 중 하나로, [테이블이나](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink") 뷰에서 한 개 이상의 행을 바꾼다. 모든 행을 변경해야 되는 경우도 [조건절을](https://ko.wikipedia.org/wiki/조건절_\(SQL\) "wikilink") 사용하여 하위 집합을 선택할 수 있다.

`UPDATE` 문은 아래의 구문을 따른다:\[1\]

**`UPDATE`**` `*`table_name`*` `**`SET`**` `*`column_name`*` = `*`value`*` [, `*`column_name`*` = `*`value``   ``...`*`] [`**`WHERE`**` `*`condition`*`]`

`UPDATE`가 성공적으로 이루어진 경우, 사용자는 반드시 데이터 조작 특권 동작 (`UPDATE` 특권동작)을 반드시 테이블이나 컬럼에서 수행해야 하고 업데이트된 값은 제약 조건에 충돌하지 않아야 한다. 그 예를 들면 [고유 키](https://ko.wikipedia.org/wiki/고유_키 "wikilink"),[고유 인덱스](https://ko.wikipedia.org/wiki/고유_인덱스 "wikilink"), [`CHECK` 제약 조건](https://ko.wikipedia.org/wiki/Check_제약_조건 "wikilink"), 그리고 [`NOT NULL`](../Page/Null_\(SQL\).md "wikilink") 제약 조건 등이 있다.

어떤 데이터베이스 시스템은 예로 [PostgreSQL](../Page/PostgreSQL.md "wikilink")를 들자면, FROM 절이 존재하면 기본적으로 대상 테이블이 fromlist에 응답되는 테이블로 조인한다. 각각의 출력한 행의 조인은 대상 테이블의 업데이트를 의미한다. FROM을 쓸 때 생성된 최대 한 개의 각각의 출력 행이 조인되었는지 확인해야 한다. 다시 말해서, 대상 행은 다른 테이블에 한 개 이상의 행을 다른 테이블로부터 조인할 수 없다. 만약 그럴 경우 오직 하나의 행만 대상 테이블에 조인한다. 그런 후, 오직 하나의 조인된 행은 대상 행의 업데이트에 사용한다. 그러나 어떤 행을 썼는 지 예측하기는 어렵다. \[2\]

이 불확정성의 원인은 다른 테이블을 좀 더 안전한 서브셀렉트 범위에서만 참조하고, 종종 읽기가 좀 더 어렵고 조인이 좀 더 느려지기 때문이다. [섬네일](https://ko.wikipedia.org/wiki/파일:SQL_ANATOMY_wiki.svg "wikilink")

## 예제

*shboard* 테이블 중 *C2* 컬럼 값이 "a"인 모든 행에서 *C1* 컬럼을 1로 바꾼다.

``` sql
UPDATE shboard SET C1 = 1 WHERE C2 = 'a'
```

*T* 테이블 중 *C2* 컬럼 값이 "a"인 모든 행에서 *C1* 컬럼을 9로, *C3* 컬럼을 4로 바꾼다.

``` sql
UPDATE T SET C1 = 9, C3 = 4 WHERE C2 = 'a'
```

*C2* 컬럼 값이 "a"이면 *C1* 컬럼을 1 증가시킨다.

``` sql
UPDATE T SET C1 = C1 + 1 WHERE C2 = 'a'
```

*C2* 컬럼 값이 "a"이면 *C1* 컬럼 값을 "text" 문자열로 프리펜드한다.

``` sql
UPDATE T SET C1 = 'text' || C1 WHERE C2 = 'a'
```

*C2* 컬럼 값을 *C4* 컬럼 값이 0인 *T2* 테이블의 *C3* 컬럼 값의 서브 목록에서 찾아질 때만 *T1* 테이블의 *C1* 컬럼 값을 2로 바꾼다.

``` sql
UPDATE T1
SET C1 = 2
WHERE C2 IN ( SELECT C3
               FROM   T2
               WHERE  C4 = 0)
```

또한 여러 컬럼을 하나의 `UPDATE` 문으로 업데이트할 수 있다:

``` sql
UPDATE T SET C1 = 1, C2 = 2
```

조건절과 [`JOIN`](https://ko.wikipedia.org/wiki/JOIN_\(SQL\) "wikilink")문 또한 섞어쓸 수 있다:

``` sql
UPDATE T SET A = 1 WHERE C1 = 1 AND C2 = 2
```

``` sql
UPDATE a
SET a.updated_column = updatevalue
FROM articles a
JOIN classification c
ON a.articleID = c.articleID
WHERE c.classID = 1
```

또는 오라클 시스템에서 (여기서는 classification.articleID로 인덱스한 것을 가정함)

``` oracle8
UPDATE
(
  SELECT *
    FROM articles
    JOIN classification
      ON articles.articleID = classification.articleID
   WHERE classification.classID = 1
)
SET updated_column = updatevalue
```

## 참조

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")

1.  <http://dev.mysql.com/doc/refman/5.0/en/update.html> simplified from this page
2.  <http://www.postgresql.org/docs/8.1/static/sql-update.html>