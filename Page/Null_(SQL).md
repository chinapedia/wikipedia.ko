> This article is converted from Wikipedia: [Null \(SQL\)](https://ko.wikipedia.org/wiki/Null_\(SQL\)).


[섬네일](https://ko.wikipedia.org/wiki/파일:Db-omega.svg "wikilink") **NULL**은 [구조적 질의 언어](https://ko.wikipedia.org/wiki/구조적_질의_언어 "wikilink") (SQL)에서 [데이터베이스](../Page/데이터베이스.md "wikilink") 내의 데이터 값이 존재하지 않는다는 것을 지시하는데 사용되는 특별한 표시어이다. 데이터베이스 [관계 모델의](https://ko.wikipedia.org/wiki/관계_모델 "wikilink") 창시자인 E. F. 콧(E. F. Codd)에 만들어진 개념으로, SQL NULL은 모든 true RDBMS가 빠진 정보와 적용할 수 없는 정보를 지원해야 한다는 요구사항을 충족시키는 역할을 한다. 콧은 또한 데이터베이스 이론에서 Null을 표현하기 위해 [그리스어](../Page/그리스어.md "wikilink")의 [오메가](https://ko.wikipedia.org/wiki/오메가 "wikilink")의 소문자(ω)를 이용할 것을 도입했다. NULL은 또한 SQL에서 Null 특수 표시를 구분하기 위해 사용되는 유보된 키워드이다.

Null은 SQL 조인에서 사용하기 위해 필수적인 [3치 자궁로](https://ko.wikipedia.org/wiki/3치_자궁 "wikilink") 인해 논란의 중심이 되어 왔다. 컴퓨터 과학자인 론 밴 더 메이든 교수는 그러한 여러 문제를 다음과 같이 요약했다. SQL 표준에서 비일관성은 SQL에서 널의 취급 문제를 직관적인 논리 어휘 탓으로 돌리는 것은 가능하지 않다는 것을 의미하는 것이다.\[1\] 이 문제를 해결하기 위해 여러 해법들이 제시되었지만, 대안의 복잡성은 폭넓은 이론 확산의 걸림돌이 되었다.

데이터베이스 비전문가들에게, 널이 뜻하는 바가 무엇인지 이해하는 좋은 방법은 정보적 측면을 기억하는 것이다. “값의 부족”은 0값과 동일한 의미가 아니며, 유사하게 ‘정답의 부족’이라는 말도 정답이 없다는 말과 같은 의미가 아니다. 예를 들어, 다음과 같은 질문을 예로 들어보자. “철수가 책을 몇 권 가지고 있지?” 답은 0(하나도 가지고 있지 않다는 것을 안다면) 또는 null(그가 가지고 있는지, 아닌지 또는 얼마나 가지고 있는 지 모름)일 것이다. 데이터베이스 테이블에서, 이러한 답을 가진 컬럼은 null 값으로 시작할 것이다. 그리고 철수가 책을 가지고 있다는 것이 확인되기 전까지는 0으로 수정되지 않을 것이다. 유사하게, 질문이 “철수가 차를 가지고 있어?”라는 질문에도 “모르겠는데”라는 정답은 “아니\!(No)”라는 것과 같은 의미가 아니다. 전자는 데이터베이스의 Null 목록을 생성하며, 후자는 데이터베이스 엔트리에서 No를 생성한다.

## 역사

E. F. 콧(E. F. Codd)은 1975년 그의 논문 《*FDT Bulletin of ACM-SIGMOD*》에서 널을 빠진 데이터를 나타내는 수단으로서 언급했다. SQL에서 채택된 Null을 설명하기 위해 가장 보편적으로 인용되는 콧의 논문은 1979년 논문이었던 《*[ACM Transactions on Database Systems](https://ko.wikipedia.org/wiki/:w:ACM_Transactions_on_Database_Systems "wikilink")*》으로 비록 이후의 논문에서 많은 제안들 대부분이 모호한 채로 남아있지만, 여기에서 그는 또는 [관계 모델](https://ko.wikipedia.org/wiki/관계_모델 "wikilink")/태즈매니아를 소개했다. 1979년 논문 2.3장에는 수학적 연산에서의 널 보급의 세부적인 사항과 널 값을 비교할 때, [3가 논리를](https://ko.wikipedia.org/wiki/3가_논리 "wikilink") 이용하는 비교도 소개를 했다. 여기에는 또한 다른 연산자 셋과 Null을 취급하는 것도 소개를 했으며, 후자의 이슈는 오늘 날에도 여전히 논란이 많은 문제이다. 데이터베이 이론계에서는, 1975년과 1979년 제안한 콧의 원래 이론들이 지금은 ‘콧의 테이블’로 언급되고 있다.\[2\] 콧은 이후에 모든 RDBMS가 빠진 데이터를 지시하기 위해 Null에 지원해야할 그의 요구사항을 [1985년](../Page/1985년.md "wikilink") 《컴퓨터월드 매거진》에 기고한 2개의 글을 통해 보강했다.\[3\]\[4\]

1986년 SQL 표준은 근본적으로 [IBM 시스템 R에서](../Page/IBM_시스템_R.md "wikilink") 수행 포로토타입 이후 콧의 제안을 채택했다. 비록 돈 챔벌린은 널 값을 SQL에서 가장 논쟁적인 특징으로 규정했지만, 그는 빠진 정보를 설명하는 가장 비용이 적게 드는 시스템 지원이라는 실용적인 측면을 들어 SQL에서 널의 설계를 옹호했다.

## Null 보급

### 수학적 연산

널은 데이터 값이 아니라, 미지의 값에 대한 표시일 뿐이기 때문에, Null에 수학적 연산을 사용하는 것은 미지의 값으로 나타난다.\[5\] 아래의 예에서, 10을 Null에 곱하면 결과값은 Null이 된다.:

``` sql
10 * NULL          -- 결과는 NULL
```

이것은 예기치 않은 결과를 야기한다. 예를 들어, 널을 0으로 나누려 한다면, 플랫폼은 ‘0으로 나눈’ 예상된 데이터 예외값을 던지는 대신, 널 값을 반환한다.\[6\] 비록 이러한 행위가 ISO SQL 표준으로 정의되어 있지는 않지만, 많은 DBMS 벤더들이 이러한 연산을 유사하게 다룬다. 예를 들어, 오라클, PostgreSQL, MySQL 서버, 그리고 마이크로소프트 SQL 서버 플랫폼은 모두 널 값을 아래와 같이 반환한다 :

``` sql
NULL / 0
```

### 문자열 연속

SQL에서 흔히 볼 수 있는 문자열 연속 연산 또한 연산자 중 하나가 Null 값일 때 Null 값으로 나타난다.\[7\] 아래의 예제는 SQL || 문자열 연속 연산자에 Null을 사용함으로써 널 값이 리턴되는 것을 보여준다.

``` sql
'생선' || NULL || '김치'   -- 결과는 NULL
```

모든 데이터베이스에서 이러한 것은 아니다. 오라클 RDBMS를 예로 들면, NULL 과 빈 문자열은 동일한 것으로 취급되어, '생선' || NULL || '김치'는 ‘생선 김치’로 나타난다.

## NULL과 3가 논리(3VL)의 비교

널은 데이터 도메인의 한 부분이 아니기 때문에, 값으로 여기지지는 않지만, 값의 부재를 표시하는 표시자서의 역할을 한다. 이러한 이유로 인해, 널과 비교를 하는 것은 ‘참’(T)도 ‘거짓(F)’도 아니며, 항상 제3의 값, ‘미지’(unknown)로 나타난다.\[8\] 10과 Null을 비교하는 아래 표현의 논리적 결과는 Unknown이다:

``` sql
SELECT 10 = NULL       -- 결과는 Unknown
```

그러나, 만약 Null 값이 연산의 결과물에 적합하지 않을 때 Null에 대한 어떤 연산은 값을 리턴할 수 있다. 아래의 예제를 보자 :

``` sql
SELECT NULL OR TRUE   -- 결과는 True
```

이 경우, OR의 왼쪽에 있는 값이 알 수 없다는 사실이 부적절하다. 왜냐하면, OR 연산의 결과가 왼쪽 값에 상관없이 참일 것이기 때문이다.

## 같이 보기

  - [널 문자](../Page/널_문자.md "wikilink")

## 각주

## 외부 링크

  - [Oracle NULLs](http://www.psoug.org/reference/null.html)
  - [The Third Manifesto](http://www.thethirdmanifesto.com/)
  - [Implications of NULLs in sequencing of data](https://web.archive.org/web/20130405060544/http://www.sqlexpert.co.uk/2006/05/treatment-of-nulls-by-oracle-sql.html)
  - [Java bug report about jdbc not distinguishing null and empty string, which Sun closed as "not a bug"](http://bugs.sun.com/bugdatabase/view_bug.do?bug_id=4032732)
  - [TheIntegrationEngineer](https://web.archive.org/web/20090125113338/http://www.theintegrationengineer.com/the-nature-of-null/) explains how NULL works and the logic behind it.

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")

1.  Ron van der Meyden, "[Logical approaches to incomplete information: a survey](http://books.google.com/books?id=gF0b85IuqQwC&pg=PA344)" in Chomicki, Jan; Saake, Gunter (Eds.) *Logics for Databases and Information Systems*, Kluwer Academic Publishers , p. 344; [PS preprint](http://www.cse.unsw.edu.au/~meyden/research/indef-review.ps) (note: page numbering differs in preprint from the published version)
2.
3.
4.
5.  .
6.
7.
8.