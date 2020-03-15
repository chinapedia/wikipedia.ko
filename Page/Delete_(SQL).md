> This article is converted from Wikipedia: [Delete \(SQL\)](https://ko.wikipedia.org/wiki/Delete_\(SQL\)).


구조화 질의어([SQL](../Page/SQL.md "wikilink"))에서, **DELETE** 문은 [테이블](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink") 또는 뷰에서 한개 이상의 행을 삭제한다. 하위 집합은 삭제에 대한 조건을 정의할 수 있으며, 정의하지 않으면 모든 행이 삭제된다.\[1\]

## 사용법

`DELETE` 문은 다음 구문을 따른다

  -
    **`DELETE`** `FROM` *테이블_또는_뷰_이름* \[**`WHERE`** 조건\]

[`WHERE` 조건에](../Page/WHERE_\(SQL\).md "wikilink") 맞는 모든 행은 테이블에서 삭제된다. `WHERE` 절을 생략하면, 모든 행을 삭제한다.\[2\]`DELETE`문은 어떤 행이라도 리턴하지 않으며, [결과 집합을](https://ko.wikipedia.org/wiki/결과_집합 "wikilink") 발생시키지도 않는다.

`DELETE` 문을 실행하는 것은 다른 테이블을 삭제하게끔 실행하는 [트리거가](../Page/데이터베이스_트리거.md "wikilink") 발생할 수 있다. 예를 들면, 두 테이블이 [외래 키로](https://ko.wikipedia.org/wiki/외래_키 "wikilink") 연결되어 있고 행이 참조된 테이블에서 삭제된다면, [참조 무결성이](../Page/참조_무결성.md "wikilink") 유지되도록 참조하고 있는 테이블에도 공통적으로 삭제된다.

## 예제

  - *pies* 테이블에서 *flavor* 열과 *Lemon Meringue* 열에서 행이 같으면 삭제한다:

<!-- end list -->

``` sql
DELETE FROM pies WHERE flavor='Lemon Meringue';
```

  - *trees* 테이블에서, *height* 값이 80보다 작으면 행을 삭제한다:

<!-- end list -->

``` sql
DELETE FROM trees WHERE height < 80;
```

  - *mytable*에서 모든 행을 삭제한다:

<!-- end list -->

``` sql
DELETE FROM mytable;
```

  - *mytable*에서 where 조건에 서브쿼리를 사용해 행을 삭제한다:

<!-- end list -->

``` sql
DELETE FROM mytable WHERE id IN (SELECT id FROM mytable2)
```

  - *mytable*에서 값 목록을 사용하여 행을 삭제한다:

<!-- end list -->

``` sql
DELETE FROM mytable WHERE id IN (value1, value2, value3, value4, value5)
```

## 참조

## 외부 링크

  - [MySQL 사용자 설명서](http://www.mysqltutorial.org)

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")

1.
2.