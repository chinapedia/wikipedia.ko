> This article is converted from Wikipedia: [SQL 삽입](https://ko.wikipedia.org/wiki/SQL_삽입).


**SQL 삽입**(, SQL 인젝션, SQL 주입)은 응용 프로그램 보안 상의 허점을 의도적으로 이용해, 악의적인 [SQL](../Page/SQL.md "wikilink")문을 실행되게 함으로써 데이터베이스를 비정상적으로 조작하는 [코드 인젝션](../Page/코드_인젝션.md "wikilink") 공격 방법이다.

## 예

다음과 같이 사용자의 아이디와 비밀번호를 확인하고 일치하면 로그인을 하는 [PHP](../Page/PHP.md "wikilink") 프로그램이 있다고 하자.

``` php
$username = $_POST["username"];
$password = $_POST["password"];

$mysqli->query("SELECT * FROM users WHERE username='{$username}' AND password='{$password}'");
```

위의 코드는 사용자로부터 아이디와 비밀번호를 입력받아서 일치하는 행을 선택하고 있다. 하지만 공격자가 만약 유저네임에 `admin`, 패스워드에 `password' OR 1=1 --` 을 입력하면 쿼리문은 아래와 같이 된다.

``` sql
SELECT * FROM users WHERE username='admin' and password='password' OR 1=1 --'
```

`1=1`은 항상 참이므로 이 방법으로 공격자는 비밀번호를 입력하지 않고 로그인할 수 있게 된다.

## Blind SQL 삽입

*Blind SQL 삽입*은 평범한 SQL 삽입과 같이 원하는 데이터를 가져올 쿼리를 삽입하는 기술이다. 이것은 웹에서 SQL 삽입에 취약하나 [데이터베이스](../Page/데이터베이스.md "wikilink") 메시지가 공격자에게 보이지 않을 때 사용한다. 하지만 평범한 SQL 삽입과 다른점은 평범한 SQL 삽입은 쿼리를 삽입하여 원하는 데이터를 한번에 얻어낼 수 있는 데에 비해 Blind SQL 삽입은 참과 거짓, 쿼리가 참일때와 거짓일 때의 서버의 반응 만으로 데이터를 얻어내는 기술이다. 즉, 쿼리를 삽입하였을 때, 쿼리의 참과 거짓에 대한 반응을 구분할 수 있을때에 사용되는 기술이다. Blind SQL 삽입은 위 두 함수를 이용하여 쿼리의 결과를 얻어, 한글자씩 끊어온 값을 아스키코드로 변환시키고 임의의 숫자와 비교하여 참과 거짓을 비교하는 과정을 거쳐가며 계속 질의를 보내어 일치하는 아스키코드를 찾아낸다. 그러한 과정을 반복하여 결과들을 조합하여 원하는 정보를 얻어냄으로써 공격을 이루어지게 한다. 많은 비교과정이 필요하기 때문에 악의적인 목적을 가진 크래커들은 Blind SQL 삽입 공격을 시도할때에 자동화된 툴을 사용하여 공격한다. 취약점이 발견된다면 순식간에 많은 정보들이 변조되거나 크래커의 손에 넘어가게 된다.\[1\]

## 방어

### 준비된 선언

준비된 선언(Prepared statement)을 사용하면 사용자의 입력이 쿼리문(SQL 선언 템플릿)으로부터 분리되기 때문에 SQL 삽입을 효과적으로 방어할 수 있다. 준비된 선언은 다음과 같은 단계에 따라 실행된다:

1.  준비: 쿼리문이 [데이터베이스 관리 시스템](../Page/데이터베이스_관리_시스템.md "wikilink")(DBMS)으로 전송된다. 이 때 사용자 입력 값은 전송되지 않는 대신 플레이스홀더로 표시된다.
2.  DBMS가 쿼리문을 분석하고 최적화를 진행한다.
3.  실행: 플레이스홀더에 입력할 사용자 입력 값이 전송되고 DBMS가 쿼리문을 실행한다.

PHP에서는 PDO 또는 MySQLi 중 하나로 준비된 선언을 사용할 수 있다.

``` php
$username = $_POST["username"];
$password = $_POST["password"];

$pdo = new PDO('mysql:dbname=testdb;host=127.0.0.1', 'user', 'password');
$pdo->setAttribute(PDO::ATTR_EMULATE_PREPARES, false);

$st = $pdo->prepare('SELECT * FROM users WHERE username=:username AND password=:password'); // 준비
$st->bindParam(':username', $username); // 사용자 입력 값 할당
$st->bindParam(':password', $password); // 사용자 입력 값 할당
$st->execute(); // 실행

var_dump($st->fetchObject());
```

### 이스케이프

SQL에서 특별한 의미를 갖는 문자들을 이스케이프해서 SQL 삽입을 방어할 수도 있다. 예를들어 PHP에서는 이스케이프를 위해 `mysqli_real_escape_string();` 함수를 사용할 수 있다.

``` php
$username = $mysqli->real_escape_string($_POST["username"]);
$password = $mysqli->real_escape_string($_POST["password"]);

$mysqli->query("SELECT * FROM users WHERE username='{$username}' AND password='{$password}'");
```

## 같이 보기

  - [사이트 간 스크립팅](../Page/사이트_간_스크립팅.md "wikilink")
  - [코드 인젝션](../Page/코드_인젝션.md "wikilink")
  - [안전한 입출력 처리](../Page/안전한_입출력_처리.md "wikilink")

## 각주

<references/>

## 외부 링크

  - [Complete Reference Guide to SQL Injection, Attack and Prevention Method of SQL Injection](https://web.archive.org/web/20131203001402/http://www.worldofhacker.com/2013/09/complete-reference-guide-to-sqli-how-to.html) by WorldofHacker.
  - [Manual Sql Injection Tutorial](http://www.techyfreaks.com/2012/05/manual-sql-injection-tutorial.html) By The Ajay Devgan
  - [SQL Injection Knowledge Base](http://www.websec.ca/kb/sql_injection), by Websec.
  - [SQL Injection Wiki](https://web.archive.org/web/20151115203638/http://www.sqlinjectionwiki.com/)
  - [Blind Sql injection with Regular Expression](http://www.ihteam.net/papers/blind-sqli-regexp-attack.pdf)
  - [WASC Threat Classification - SQL Injection Entry](http://projects.webappsec.org/SQL-Injection), by the Web Application Security Consortium.
  - [Why SQL Injection Won't Go Away](https://web.archive.org/web/20121109235333/http://docs.google.com/leaf?id=0BykNNUTb95yzYTRjMjNjMWEtODBmNS00YzgwLTlmMGYtNWZmODI2MTNmZWYw&sort=name&layout=list&num=50), by Stuart Thomas.
  - [SQL Injection Attacks by Example](https://web.archive.org/web/20151107080700/http://www.unixwiz.net/techtips/sql-injection.html), by Steve Friedl
  - [SQL Injection Prevention Cheat Sheet](https://web.archive.org/web/20151116090859/https://www.owasp.org/index.php/SQL_Injection_Prevention_Cheat_Sheet), by OWASP.
  - [SQL Injection Tutorial](https://web.archive.org/web/20141211215029/http://www.breakthesecurity.com/2010/12/hacking-website-using-sql-injection.html), by BTS.
  - [SQL 인젝션 공격 방어 방법](https://web.archive.org/web/20190403053150/https://codeclu.com/questions/43/mysql-sql-%EC%9D%B8%EC%A0%9D%EC%85%98-%EA%B3%B5%EA%B2%A9-%EB%B0%A9%EC%96%B4-%EB%B0%A9%EB%B2%95)
  - [sqlmap: automatic SQL injection and database takeover tool](http://sqlmap.org/)
  - [SDL Quick security references on SQL injection](http://go.microsoft.com/?linkid=9707610) by Bala Neerumalla.
  - [Backdoor Web-server using MySQL SQL Injection](https://web.archive.org/web/20130402121201/http://www.greensql.com/articles/backdoor-webserver-using-mysql-sql-injection) By Yuli Stremovsky
  - [Defacing website with SQL injection](https://web.archive.org/web/20160405080934/http://www.sploitswiki.com/2011/02/deface-website-sql-injection.html) by sploitswiki
  - [Attacking web App with SQL injection](http://slides.com/abhinavsejpal/sql-injection-for-beginners#/) by Abhinav Sejpal

[분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [분류:취약점 공격](https://ko.wikipedia.org/wiki/분류:취약점_공격 "wikilink") [분류:보안](https://ko.wikipedia.org/wiki/분류:보안 "wikilink") [분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink")

1.