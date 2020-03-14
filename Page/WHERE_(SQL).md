> This article is converted from Wikipedia: [WHERE \(SQL\)](https://ko.wikipedia.org/wiki/WHERE_\(SQL\)).


SQL에서 **WHERE** 구문은 [SQL](https://ko.wikipedia.org/wiki/SQL "wikilink") [데이터 조작 언어](../Page/데이터_조작_언어.md "wikilink")(DML)가 특정한 기준을 충족하는 행(row)에만 영향을 미치도록 지정한다. 기준은 구문의 형태로 표현된다. WHERE 구문은 SQL DML에서 의무 사항이 아니라, SQL DML 구문 또는 쿼리에 의해 반환된 결과물에 의해 영향을 받는 열의 수를 제한하도록 사용할 수 있다.

## 개요

WHERE는 SQL 예약어이다.

WHERE 구문은 SQL DML 구문의 한정에 사용되며, 다음과 같은 일반적인 형태를 가진다.

``` sql
SQL-DML-Statement
FROM table_name
WHERE predicate
```

WHERE 구문이 참인 한정어에 모든 열이 SQL DML 구문이나 질의어에 영향을 받는다. (또는 결과값을 반환하거나) 한정어가 거짓 또는 미지(NULL)이라고 판단한 열은 DML 구문이나 질의어에 영향을 받지 않는다.

아래 질의어는 *mycol*이라는 컬럼 속에 자료가 100 이상일 때 *mytable*에서 단지 그러한 열만 반환을 한다.

``` sql
SELECT *
FROM   mytable
WHERE  mycol > 100
```

아래의 DELETE 구문은 *mycol*이라는 컬럼이 NULL이거나 100 값만 가질 때 *mytable*에서 단지 그러한 열만 제거한다.

``` sql
DELETE
FROM   mytable
WHERE  mycol IS NULL OR mycol = 100
```

SQL Where 구문을 쓰는 적절한 공식은 다음과 같다\[1\]

<span style="color:blue; font-size:114%;">`SELECT `<span style="color:red; font-size:100%;">`<`<column list>`>`</span>` FROM `<span style="color:red; font-size:100%;">`table`</span>` WHERE `<span style="color:red; font-size:100%;">`column `</span><span style="color:#c0504d;">`operatorvalue`</span></span>

## 한정어

단순 한정어(predicate)은 =, \<\>, \>, \>=, \<, \<=, IN, BETWEEN, LIKE, IS NULL 또는 IS NOT NULL 중 하나의 연산자를 사용한다.

한정어는 필요하면 괄호로 둘러쌀 수 있다. 키워드 AND 그리고 OR는 2개의 한정어를 새로운 것으로 결합하기 위해 사용될 수 있다. 다중 결합이 적용되면, 결합을 묶어서 값의 순서를 지정하기 위해 괄호가 사용될 수 있다. 괄호가 없으면, AND 연산자가 OR보다 더 강력한 순위를 가진다.

다음의 예는 *mycol*이라는 컬럼 값이 100 이상이며, **그리고** 항목의 값이 'Hammer'라는 문자열과 일치할 때 해당값을 삭제한다

``` sql
DELETE
FROM   mytable
WHERE  mycol > 100 AND item = 'Hammer'
```

### IN

`IN`은 후보 셋 내에 있는 어떤 값을 찾을 것이다.

``` sql
SELECT ename WHERE ename IN ('value1', 'value2', ...)
```

## 각주

## 외부 링크

  - [PSOUG Home Puget Sound Oracle Users Group](http://www.psoug.org/reference/conditions.html) gives several examples of SELECT statements with WHERE clauses.

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")

1.