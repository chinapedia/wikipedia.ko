> This article is converted from Wikipedia: [JDBC](https://ko.wikipedia.org/wiki/JDBC).


**JDBC**(Java Database Connectivity)는 [자바에서](../Page/자바_\(프로그래밍_언어\).md "wikilink") [데이터베이스](../Page/데이터베이스.md "wikilink")에 접속할 수 있도록 하는 [자바 API이다](https://ko.wikipedia.org/wiki/자바_API "wikilink"). JDBC는 데이터베이스에서 자료를 쿼리하거나 업데이트하는 방법을 제공한다.

## 역사

썬 마이크로시스템즈는 1997년 2월 19일 JDBC를 [JDK](https://ko.wikipedia.org/wiki/JDK "wikilink") 1.1의 일부로 출시하였다.\[1\] 그 뒤로 이제까지 [자바 SE의](../Page/자바_플랫폼,_스탠더드_에디션.md "wikilink") 일부로 되고 있다.

JDBC 클래스는 [자바 패키지](../Page/자바_패키지.md "wikilink") java.sql과 javax.sql에 포함되어 있다.

버전 3.1을 기점으로 JDBC는 [자바 커뮤니티 프로세스를](../Page/자바_커뮤니티_프로세스.md "wikilink") 통해 개발되고 있다. JSR 54는 JDBC 3.0을 규정(J2SE 1.4에 포함됨)하고, JSR 114는 JDBC Rowset addition을 규정하며, JSR 221은 JDBC 4.0의 사양(자바 SE 6에 포함됨)이다.\[2\]

JDBC 4.1은 JSR 221의 유지보수판 1에 규정되어 있고\[3\], 자바 SE 7에 포함되어 있다.\[4\]

최신 버전은 JDBC 4.2는 JSR 221의 유지보수판 2에 규정되어 있고\[5\], 자바 SE 8에 포함되어 있다.\[6\]

| JDBC 버전  | 발표 | 자바 플랫폼      | 중요한 변화                                                  |
| -------- | -- | ----------- | ------------------------------------------------------- |
| JDBC 4.0 |    | JavaEE 6 예정 | [JSR](https://ko.wikipedia.org/wiki/JSR "wikilink") 221 |
| JDBC 3.0 |    | JavaEE 5    | [JSR](https://ko.wikipedia.org/wiki/JSR "wikilink") 54  |
| JDBC 2.0 |    |             |                                                         |
| JDBC 1.0 |    | J2SE 1.1    |                                                         |

JDBC API 역사

## 예제

자바 애플리케이션이 데이터베이스 연결이 필요할 때 `DriverManager.getConnection()` 메소드들 가운데 하나를 사용하여 JDBC 연결을 만들게 된다. 사용된 URL은 특정 데이터베이스와 JDBC 드라이버에 의존한다. "jdbc:" 프로토콜로 무조건 시작하지만 나머지 부분은 특정 벤더에 따라 다르다.

``` java5
Connection conn = DriverManager.getConnection(
     "jdbc:somejdbcvendor:other data needed by some jdbc vendor",
     "myLogin",
     "myPassword" );
try {
     /* you use the connection here */
} finally {
    //It's important to close the connection when you are done with it
    try { conn.close(); } catch (Throwable e) { /* Propagate the original exception
instead of this one that you want just logged */ logger.warn("Could not close JDBC Connection",e); }
}
```

자바 SE 7을 기점으로 자바의 [try-with-resources](http://docs.oracle.com/javase/tutorial/essential/exceptions/tryResourceClose.html) 문을 사용하여 위의 코드를 더 깔끔하게 정리할 수 있다:

``` java5
try (Connection conn = DriverManager.getConnection(
     "jdbc:somejdbcvendor:other data needed by some jdbc vendor",
     "myLogin",
     "myPassword" ) ) {
     /* you use the connection here */
}  // the VM will take care of closing the connection
```

연결이 확립되면 다음과 같은 문을 작성할 수 있다.

``` java5
try (Statement stmt = conn.createStatement()) {
    stmt.executeUpdate( "INSERT INTO MyTable( name ) VALUES ( 'my name' ) " );
}
```

## JDBC 드라이버

JDBC 드라이버들은 자바 프로그램의 요청을 DBMS가 이해할 수 있는 프로토콜로 변환해주는 클라이언트 사이드 [어댑터이다](../Page/어댑터_패턴.md "wikilink"). (서버가 아닌 클라이언트 머신에 설치)

### 타입

상용 및 자유 드라이버들은 대부분의 관계형 데이터베이스 서버로의 연결을 제공한다. 이 드라이버들은 다음의 타입 중 하나에 속한다:

  - 타입 1: 로컬에서 사용 가능한 ODBC 드라이버의 네이티브 코드를 호출한다.
  - 타입 2: 클라이언트 사이드의 데이터베이스 벤더 네이티브 라이브리를 호출한다. 그러면 이 코드는 네트워크 상의 데이터베이스와 통신하게 된다.
  - 타입 3: 서버 사이드 미들웨어와 통신하는 순수 자바 드라이버로서, 이후에 데이터베이스와 통신한다.
  - 타입 4: 데이터베이스 네이티브 프로토콜을 사용하는 순수 자바 드라이버이다.

## 같이 보기

  - [ODBC](../Page/ODBC.md "wikilink")

## 각주

## 외부 링크

  - This documentation has examples where the JDBC resources are not closed appropriately (swallowing primary exceptions and being able to cause NullPointerExceptions) and has code prone to [SQL injection](https://ko.wikipedia.org/wiki/SQL_인젝션 "wikilink")

  - API [Javadoc](https://ko.wikipedia.org/wiki/Javadoc "wikilink") documentation

  - API Javadoc documentation

[분류:자바 플랫폼, 스탠더드 에디션](https://ko.wikipedia.org/wiki/분류:자바_플랫폼,_스탠더드_에디션 "wikilink") [분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:자바 API](https://ko.wikipedia.org/wiki/분류:자바_API "wikilink")

1.
2.  [JDBC API Specification Version: 4.0](http://java.sun.com/products/jdbc/download.html#corespec40).
3.  [JSR-000221 JDBC API Specification 4.1 (Maintenance Release 1)](http://jcp.org/aboutJava/communityprocess/mrel/jsr221/index.html)
4.  <http://docs.oracle.com/javase/7/docs/technotes/guides/jdbc/jdbc_41.html>
5.  [JSR-000221 JDBC API Specification 4.2 (Maintenance Release 2)](https://jcp.org/aboutJava/communityprocess/mrel/jsr221/index2.html)
6.  <http://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/jdbc_42.html>