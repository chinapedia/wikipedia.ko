> This article is converted from Wikipedia: [ SQL](https://ko.wikipedia.org/wiki/_SQL).


**트랜잭트 SQL**()은 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")와 [사이베이스](https://ko.wikipedia.org/wiki/사이베이스 "wikilink")가 [SQL](https://ko.wikipedia.org/wiki/SQL "wikilink")(구조 질의어)에 기능을 확장한 것이다. T-SQL은 SQL 표준 상에서 확장하여 문자열 처리, 날짜 처리, 계산 등을 위한 다양한 지원 함수, [DELETE](https://ko.wikipedia.org/wiki/DELETE "wikilink") 및 [UPDATE](https://ko.wikipedia.org/wiki/UPDATE "wikilink") 문에 대한 변경, [절차적 프로그래밍](https://ko.wikipedia.org/wiki/절차적_프로그래밍 "wikilink"), [지역 변수를](https://ko.wikipedia.org/wiki/지역_변수 "wikilink") 포함한다. 이러한 부가 기능들은 트랜잭트 SQL을 [튜링 완전으로](https://ko.wikipedia.org/wiki/튜링_완전 "wikilink") 만든다.

참고로 SQL의 오라클판 확장은 [PL/SQL](https://ko.wikipedia.org/wiki/PL/SQL "wikilink")이다.

트랜잭트 SQL은 [마이크로소프트 SQL 서버](https://ko.wikipedia.org/wiki/마이크로소프트_SQL_서버 "wikilink") 사용 시에 주요하다. SQL 서버 인스턴스와 통신하는 모든 애플리케이션들은 애플리케이션의 사용자 인터페이스에 관계 없이 트랜잭트 SQL 문을 서버에 송신함으로써 이 일을 처리한다.

## 변수

트랜잭트 SQL의 흐름 제어 키워드로 BEGIN / END, BREAK, CONTINUE, GOTO, IF / ELSE, RETURN, WAITFOR, WHILE이 있다.

  - IF와 ELSE

<!-- end list -->

``` tsql
IF DATEPART(dw, GETDATE()) = 7 OR DATEPART(dw, GETDATE()) = 1
   PRINT 'It is the weekend.'
ELSE
   PRINT 'It is a weekday.'
```

  - BEGIN과 END

<!-- end list -->

``` tsql
IF DATEPART(dw, GETDATE()) = 7 OR DATEPART(dw, GETDATE()) = 1
BEGIN
   PRINT 'It is the weekend.'
   PRINT 'Get some rest on the weekend!'
END
ELSE
BEGIN
   PRINT 'It is a weekday.'
   PRINT 'Get to work on a weekday!'
END
```

  - WHILE

<!-- end list -->

``` tsql
DECLARE @i INT
SET @i = 0

WHILE @i < 5
BEGIN
   PRINT 'Hello world.'
   SET @i = @i + 1
END
```

## DELETE, UPDATE 문 변경

Idle 플래그에 속하는 모든 `users` 삭제의 예는 다음과 같다.

``` tsql
DELETE users
  FROM users AS u
  INNER JOIN user_flags AS f
    ON u.id = f.id
WHERE f.name = 'idle'
```

## BULK INSERT

BULK INSERT는 대량의 데이터 적재 처리, 여러 줄을 테이블로 삽입, 외부 시퀀스 파일로부터 데이터 읽기를 구현하는 트랜잭트 SQL 문이다.

## TRY CATCH

SQL 서버 2005를 기점으로 마이크로소프트는 TRY CATCH 추가 로직을 도입하여 예외 형 동작을 지원한다. 이러한 동작은 개발자들이 자신들의 코드를 단순화할 수 있게 하고 각 SQL 실행문 이후에 @@ERROR 검사를 남길 수 있게 한다.

``` tsql
-- begin transaction
BEGIN TRAN

BEGIN TRY
   -- execute each statement
   INSERT INTO MYTABLE(NAME) VALUES ('ABC')
   INSERT INTO MYTABLE(NAME) VALUES ('123')

   -- commit the transaction
   COMMIT TRAN
END TRY
BEGIN CATCH
   -- rollback the transaction because of error
   ROLLBACK TRAN
END CATCH
```

## 같이 보기

  - [PL/pgSQL](https://ko.wikipedia.org/wiki/PL/pgSQL "wikilink") (PotsgreSQL)
  - [어댑티브 서버 엔터프라이즈](https://ko.wikipedia.org/wiki/어댑티브_서버_엔터프라이즈 "wikilink")(Adaptive Server Enterprise, 사이베이스)
  - [PL/SQL](https://ko.wikipedia.org/wiki/PL/SQL "wikilink") (오라클)
  - [SQL/PSM](https://ko.wikipedia.org/wiki/SQL/PSM "wikilink") (ISO 표준)

## 외부 링크

  - [Sybase Transact-SQL User's Guide](http://infocenter.sybase.com/help/index.jsp?topic=/com.sybase.help.ase_15.0.sqlug/html/sqlug/title.htm)

  - \[<http://msdn2.microsoft.com/en-us/library/aa260642(SQL.80>).aspx Transact-SQL Reference for SQL Server 2000 (MSDN)\]

  - [Transact-SQL Reference for SQL Server 2005 (MSDN)](http://msdn2.microsoft.com/en-us/library/ms189826.aspx)

  - \[<http://msdn.microsoft.com/en-us/library/bb510741(SQL.100>).aspx Transact-SQL Reference for SQL Server 2008 (MSDN)\]

  - [Transact-SQL Reference for SQL Server 2012 (MSDN)](http://msdn.microsoft.com/en-us/library/bb510741.aspx)

  - [Transact-SQL Tutorial](http://www.tsql.info)

[분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink")