> This article is converted from Wikipedia: [Join \(SQL\)](https://ko.wikipedia.org/wiki/Join_\(SQL\)).


**join(조인)** 또는 **결합 구문**은 한 [데이터베이스](https://ko.wikipedia.org/wiki/데이터베이스 "wikilink") 내의 여러 [테이블의](https://ko.wikipedia.org/wiki/테이블_\(데이터베이스\) "wikilink") 레코드를 조합하여 하나의 열로 표현한 것이다. 따라서 조인은 테이블로서 저장되거나, 그 자체로 이용할 수 있는 결과 셋을 만들어 낸다. JOIN은 2개의 테이블에서 각각의 공통값을 이용함으로써 필드를 조합하는 수단이 된다. ANSI 표준 SQL은 네가지 유형의 JOIN을 규정한다.

  - INNER JOIN
  - OUTER JOIN
  - LEFT JOIN
  - RIGHT JOIN

마케팅 특별한 경우 테이블(기본 테이블, 뷰, 또는 조인된 테이블)은 자기 자신에게 JOIN할 수 있다.

프로그래머는 JOIN 절을 조인을 위한 레코드를 구분하는데 쓴다. 만약 값을 가진 구문이 참이라면, 결합된 레코드는 예상한 형식(레코드셋 또는 임의의 테이블)으로 생성된다.

## 예제 테이블

관계 데이터베이스는 종종 객체가 1 : 다의 관계를 가질 때, 정보의 중복을 제거하기 위해 [정규화](https://ko.wikipedia.org/wiki/정규화 "wikilink")시킨다. 예를 들어, 부서(Department)라는 것은 다수의 다른 직원(Employee)들과 연관되어 있다. 효과적으로 2개의 테이블을 결합시키는 것은 2개의 테이블 모두에서 결합된 정보를 가진 또 다른 테이블을 만든다. 이것은 결합을 계산하는데 소요되는 시간적 측면에서 어느 정도 자원을 소요한다. 속도가 중요하다면, 탈정규화된 테이블을 단순히 유지시키는 것이 가능하지만, 중복된 데이터가 이후에 변경된다면 중복된 정보는 추가 비용을 발생시켜, 비용을 증가시키고, [데이터 무결성을](https://ko.wikipedia.org/wiki/데이터_무결성 "wikilink") 유지하는데 있어서 복잡성을 야기한다.

이 글에서 결합 형식에 대한 모든 부가적인 설명은 다음의 두 테이블을 예제로 이용한다. 이러한 테이블에서의 열은 다른 유형의 결합과 결합 서술문의 결과를 설명하는 역할을 할 것이다. 다음의 테이블에서 Department 테이블의 Department ID 컬럼(Department.Department ID로 표현할 수 있다.)이 [기본 키이며](../Page/기본_키.md "wikilink"), Employee.Department ID가 [외래 키이다](https://ko.wikipedia.org/wiki/외래_키 "wikilink").

<table>
<caption>Employee 테이블</caption>
<thead>
<tr class="header">
<th><p>LastName</p></th>
<th><p>DepartmentID</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>Robinson</p></td>
<td><p>34</p></td>
</tr>
<tr class="odd">
<td><p>Smith</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>John</p></td>
<td></td>
</tr>
</tbody>
</table>

| <u>DepartmentID</u> | DepartmentName |
| ------------------- | -------------- |
| <u>31</u>           | 영업부            |
| <u>33</u>           | 기술부            |
| <u>34</u>           | 사무부            |
| <u>35</u>           | 마케팅            |

Department 테이블


**주의**: 위의 Employee 테이블에서, "John"이라는 직원은 아직 어떤 부서에도 할당되지 않았다. 또한 어떠한 직원도 "마케팅" 부서에 할당되지 않았음을 유의해라.

위에서 언급된 테이블을 생성하는 SQL이다.

``` sql
CREATE TABLE department
(
 DepartmentID INT,
 DepartmentName VARCHAR(20)
);

CREATE TABLE employee
(
 LastName VARCHAR(20),
 DepartmentID INT
);

INSERT INTO department(DepartmentID, DepartmentName) VALUES(31, '영업부');
INSERT INTO department(DepartmentID, DepartmentName) VALUES(33, '기술부');
INSERT INTO department(DepartmentID, DepartmentName) VALUES(34, '사무부');
INSERT INTO department(DepartmentID, DepartmentName) VALUES(35, '마케팅');

INSERT INTO employee(LastName, DepartmentID) VALUES('Rafferty', 31);
INSERT INTO employee(LastName, DepartmentID) VALUES('Jones', 33);
INSERT INTO employee(LastName, DepartmentID) VALUES('Steinberg', 33);
INSERT INTO employee(LastName, DepartmentID) VALUES('Robinson', 34);
INSERT INTO employee(LastName, DepartmentID) VALUES('Smith', 34);
INSERT INTO employee(LastName, DepartmentID) VALUES('John', NULL);
```

## 교차 조인

`CROSS JOIN` 절은 조인되는 두 테이블에서 [곱집합](https://ko.wikipedia.org/wiki/곱집합 "wikilink")을 반환한다. 즉, 두 번째 테이블로부터 각 행과 첫 번째 테이블에서 각 행이 한번씩 결합된 열을 만들 것이다. 예를 들어 m행을 가진 테이블과 n행을 가진 테이블이 교차 조인되면 m\*n 개의 행을 생성한다.\[1\]

교차 조인의 명시적 예는 다음과 같다:

``` sql
SELECT *
FROM employee CROSS JOIN department;
```

크로스 조인을 암묵적으로 사용한 예는 다음과 같다:

``` sql
SELECT *
FROM employee, department;
```

이 두 쿼리는 동일한 결과를 반환한다.

<table>
<thead>
<tr class="header">
<th><p>Employee.LastName</p></th>
<th><p>Employee.DepartmentID</p></th>
<th><p>Department.DepartmentName</p></th>
<th><p>Department.DepartmentID</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="odd">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td><p>Smith</p></td>
<td><p>34</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="odd">
<td><p>Robinson</p></td>
<td><p>34</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td><p>John</p></td>
<td></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="odd">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>Smith</p></td>
<td><p>34</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Robinson</p></td>
<td><p>34</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>John</p></td>
<td></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="odd">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>Smith</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="odd">
<td><p>Robinson</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>John</p></td>
<td></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="odd">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
<td><p>마케팅</p></td>
<td><p>35</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
<td><p>마케팅</p></td>
<td><p>35</p></td>
</tr>
<tr class="odd">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
<td><p>마케팅</p></td>
<td><p>35</p></td>
</tr>
<tr class="even">
<td><p>Smith</p></td>
<td><p>34</p></td>
<td><p>마케팅</p></td>
<td><p>35</p></td>
</tr>
<tr class="odd">
<td><p>Robinson</p></td>
<td><p>34</p></td>
<td><p>마케팅</p></td>
<td><p>35</p></td>
</tr>
<tr class="even">
<td><p>John</p></td>
<td></td>
<td><p>마케팅</p></td>
<td><p>35</p></td>
</tr>
</tbody>
</table>

크로스 조인은 결합된 테이블에서 레코드를 걸러내기 위해 어떠한 서술어도 적용하지 않는다. 프로그래머는 크로스 조인된 결과를 WHERE 구문을 사용하여 더 걸러낼 수 있다.

SQL:2011 표준에서, 크로스 조인은 F401, 확장 조인 테이블(Extended joined table)의 선택사항이다.

## 내부 조인

내부 조인(inner join)은 여러 애플리케이션에서 사용되는 가장 흔한 결합 방식이며, 기본 조인 형식으로 간주된다. 내부 조인은 조인 구문에 기반한 2개의 테이블(A, B)의 컬럼 값을 결합함으로써 새로운 결과 테이블을 생성한다. 그 질의어는 조인 구문을 충족하는 모든 일치되는 결과 열을 찾기 위해 A 테이블의 각 열을 B 테이블의 각 열과 비교를 한다. 조인 구문이 충족되면, A, B 테이블에서 일치된 각 열의 컬럼 값은 결과 열로 결합된다. 조인으로 도출된 결과 값은 (테이블 A 내의 모든 레코드와 테이블 B에 있는 모든 레코드가 결합하여) 테이블에 존재하는 모든 레코드(또는 크로스 조인)의 최초의 곱집합의 결과값으로 정의될 수 있으며, 그런 이후 조인 구문을 충족시키는 모든 레코드 값을 반환한다. 실제 SQL 실행은 보통 곱집합의 연산이 매우 비효율적이기 때문에 실행 가능한 해쉬 조인 또는 소트-머지(sort-merge) 조인과 같은 다른 접근법을 사용한다.

SQL은 **‘명시적 조인 표현’**(explicit)과 **‘암시적 조인 표현’**(implicit) 2개의 다른 조인식 구문을 지정한다.

**‘명시적 조인 표현’**에서는 테이블에 조인을 하라는 것을 지정하기 위해 JOIN 키워드를 사용하며, 그리고 나서 다음의 예제와 같이 ON 키워드를 조인에 대한 구문을 지정하는데 사용한다.

``` sql
SELECT *
FROM employee INNER JOIN department
  ON employee.DepartmentID = department.DepartmentID;
```

**‘암시적 조인 표현’**은 SELECT 구문의 FROM 절에서 그것들을 분리하는 컴마를 사용해서 단순히 조인을 위한 여러 테이블을 나열하기만 한다. 그리하여 그것은 교차 조인(cross join)을 지정하면, WHERE 절은 추가적인 필터 구문(명시적 구문에서 조인 구문을 비교하는 역할을 하는)을 적용할 것이다.

다음의 예제는 전자의 것과 동일한 예이지만, 이번에는 암시적 조인 구문을 사용했다.

``` sql
SELECT *
FROM employee, department
WHERE employee.DepartmentID = department.DepartmentID;
```

위의 예에서 제시한 질의어는 두 테이블의 DepartmentID 컬럼을 이용해서 Employee 와 Department 테이블을 조인할 것이다. 이 두 테이블에서 DepartmentID가 일치하는 곳(즉, 조인 구문이 충족되는 곳)에서 쿼리는 LastName, DepartmentID 와 DepartmentName 컬럼을 결과 열로 결합할 것이다. DepartmentID 가 일치하지 않는다면, 어떠한 결과 값도 생성되지 않을 것이다.

그리하여 위 예제의 2개의 질의 중 하나의 수행 결과는 다음과 같을 것이다.

| Employee.LastName | Employee.DepartmentID | Department.DepartmentName | Department.DepartmentID |
| ----------------- | --------------------- | ------------------------- | ----------------------- |
| Robinson          | 34                    | 사무부                       | 34                      |
| Jones             | 33                    | 기술부                       | 33                      |
| Smith             | 34                    | 사무부                       | 34                      |
| Steinberg         | 33                    | 기술부                       | 33                      |
| Rafferty          | 31                    | 영업부                       | 31                      |
|                   |                       |                           |                         |

**주의**: 프로그래머는 조인 조건이 명시적으로 IS NULL 또는 IS NOT NULL과 같은 추가 구문을 사용하지 않는다면 NULL은 어떠한 값도 일치하지 않으므로(심지어 NULL 자체도) NULL 값이 포함될 수 있는 테이블을 조인하는데 있어서 특별한 주의를 기울여야 한다.

John이라는 직원과 마케팅이라는 부서가 쿼리 수행 결과에서 나타나지 않음을 유의하자. 이것들 중 어느 것도 다른 테이블에서 일치되는 레코드를 가지고 있지 않다 : John은 부서와 연관이 없으며, 어떤 직원도 department ID 35 ("마케팅")에 배속되어 있지 않다. 희망하는 결과값에 따라, 이러한 행위는 약간 버그가 있을 수도 있으며, 그리고 그것은 외부 조인에서는 회피될 수 있는 것이다.

내부 조인을 더 세부적으로 분류하여 **동일 조인**(Equi-Join), **자연 조인**(natural join), 또는 **교차 조인**(cross-join)으로도 나눌 수 있다.

### 동일 조인

**동일 조인**(Equi-Join)은 특별한 유형의 *비교자 기반의 조인*이며, 이것은 조인 구문에서 동등비교만을 사용한다. 다른 비교 연산자(`<`와 같은)를 사용하는 것은 동일 조인으로서의 조인의 자격을 박탈하는 것이다. 위에서 보여준 쿼리는 이미 동일 조인의 예시가 제시되었다.

``` sql
SELECT *
FROM employee JOIN department
  ON employee.DepartmentID = department.DepartmentID;
```

우리는 동일 조인을 아래와 같이 쓸 수 있다.

``` sql
SELECT *
FROM employee, department
WHERE employee.DepartmentID = department.DepartmentID;
```

만약 동일 조인 내에 있는 컬럼들이 동일한 이름을 가지고 있다면, [SQL-92](https://ko.wikipedia.org/wiki/SQL-92 "wikilink")는 `USING`을 추가함으로써 동일 조인을 표현하기 위한 속기적 개념을 선택적으로 제공한다 :\[2\]

``` sql
SELECT *
FROM employee INNER JOIN department USING (DepartmentID);
```

`USING` 구문은 단순한 [설탕구문](https://ko.wikipedia.org/wiki/설탕구문 "wikilink")이지만, 결과 값이 명시적 구문에 의한 결과 값과는 다르다. 특히 `USING` 목록 속에 언급된 어떤 컬럼들은 조인에서 각 테이블에 한번 등장하기 보다는, 권한이 없는 이름으로 단 한번만 등장할 것이다. 위의 사례에서, 단인 `DepartmentID` 컬럼이 해당하고, `employee.DepartmentID` 또는 `department.DepartmentID`은 해당되지 않는다.

`USING` 구문은 MS SQL Server와 Sybase에서는 지원하지 않는다.

#### 자연 조인

**[자연 조인](https://ko.wikipedia.org/wiki/자연_조인 "wikilink")**(natural join)은 동일 조인의 한 유형으로 조인 구문이 조인된 테이블에서 동일한 컬럼명을 가진 2개의 테이블에서 모든 컬럼들을 비교함으로써, 암시적으로 일어나는 구문이다. 결과적으로 나온 조인된 테이블은 동일한 이름을 가진 컬럼의 각 쌍에 대한 단 하나의 컬럼만 포함하고 있다.

대부분의 전문가들은 NATURAL JOIN이 위험한 것이며, 그러므로 이것의 사용을 강력하게 비권장하고 있다.\[3\] 그러한 위험은 다른 테이블에 다른 컬럼으로 동일한 이름을 가진 새로운 컬럼을 무심코 추가하는데서 오는 것이다.

현존하는 자연 조인은 자연스럽게 (다른 컬럼에서 온) 이전보다 다른 기준을 이용해서 비교를 위해 비교를 하거나 일치하는 것을 찾아서 새로운 컬럼을 이용할 것이다. 그리하여 테이블 내에 있는 데이터가 변경되지 않고, 증가만 해도 현존하는 질의어는 다른 결과물을 생성할 것이다.

위의 내부 조인을 위한 예제 질의는 다음과 같은 방법으로 자연 조인으로서 표현될 수 있을 것이다.

``` sql
SELECT *
FROM employee NATURAL JOIN department;
```

명시적인 `USING` 구문을 사용해서, 단지 하나의 DepartmentID 컬럼이 조인된 테이블 내에 권한자 없이 생성된다 :

| DepartmentID | Employee.LastName | Department.DepartmentName |
| ------------ | ----------------- | ------------------------- |
| 34           | Smith             | 사무부                       |
| 33           | Jones             | 기술부                       |
| 34           | Robinson          | 사무부                       |
| 33           | Steinberg         | 기술부                       |
| 31           | Rafferty          | 영업부                       |

PostgreSQL, MySQL 그리고 오라클 데이터베이스는 자연 조인을 지원하지만, Microsoft T-SQL 또는 IBM DB2는 지원되지 않는다. 조인에 사용된 컬럼들은 암시적이어서, 조인 코드가

기대 컬럼이 어떤 것인지를 보여주지 않으며, 컬럼의 변화는 결과를 바꿀 것이다. 동일한 필드명을 가진 2개의 테이블에서 실행된 내부 조인 은 동일한 결과물을 가진다.\[4\] [SQL:2011](https://ko.wikipedia.org/wiki/SQL:2011 "wikilink") 표준에서, 자연 조인은 F401 (확장 조인된 테이블) 패키지의 선택적 부분이다.

## 외부 조인

### 왼쪽 외부 조인

왼쪽 외부 조인의 예, 부가적인 결과 열 (내부 조인과 비교하여)은 이탤릭체:

``` sql
SELECT *
FROM employee LEFT OUTER JOIN department
  ON employee.DepartmentID = department.DepartmentID;
```

<table>
<thead>
<tr class="header">
<th><p>Employee.LastName</p></th>
<th><p>Employee.DepartmentID</p></th>
<th><p>Department.DepartmentName</p></th>
<th><p>Department.DepartmentID</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Jones</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="odd">
<td><p>Robinson</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>Smith</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="odd">
<td><p><em>John</em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
</tbody>
</table>

오라클은 대체 구문을 제공한다:

``` oracle8
SELECT *
FROM employee, department
WHERE employee.DepartmentID = department.DepartmentID(+)
```

사이베이스가 제공하는 대체 구문은 다음과 같다:

``` tsql
SELECT *
FROM employee, department
WHERE employee.DepartmentID *= department.DepartmentID
```

### 오른쪽 외부 조인

아래는 오른쪽 외부 조인의 예이며, 부가적인 결과 열은 이탤릭체로 되어있다:

``` sql
SELECT *
FROM employee RIGHT OUTER JOIN department
  ON employee.DepartmentID = department.DepartmentID;
```

<table>
<thead>
<tr class="header">
<th><p>Employee.LastName</p></th>
<th><p>Employee.DepartmentID</p></th>
<th><p>Department.DepartmentName</p></th>
<th><p>Department.DepartmentID</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Smith</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Robinson</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p><em>마케팅</em></p></td>
<td><p><em>35</em></p></td>
</tr>
</tbody>
</table>

오라클이 제공하는 대체 구문은 다음과 같다:

``` sql
SELECT *
FROM employee, department
WHERE employee.DepartmentID(+) = department.DepartmentID
```

오른쪽과 왼쪽 외부 조인은 기능적으로 동일하다. 양자 모두 다른 것들이 하지 않는 어떠한 기능도 제공하지 않는다. 그래서 오른쪽과 왼쪽 외부 조인은 테이블 순서가 변경되기만 하면, 서로 대체할 수 있다.

### 완전 외부 조인

완전 외부 조인의 예는 다음과 같다:

``` sql
SELECT *
FROM employee FULL OUTER JOIN department
  ON employee.DepartmentID = department.DepartmentID;
```

<table>
<thead>
<tr class="header">
<th><p>Employee.LastName</p></th>
<th><p>Employee.DepartmentID</p></th>
<th><p>Department.DepartmentName</p></th>
<th><p>Department.DepartmentID</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Smith</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Robinson</p></td>
<td><p>34</p></td>
<td><p>사무부</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p><em>John</em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
<td><p>기술부</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
<td><p>영업부</p></td>
<td><p>31</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><em>마케팅</em></p></td>
<td><p><em>35</em></p></td>
</tr>
</tbody>
</table>

일부 데이터베이스 시스템은 완전 외부 조인 기능을 직접적으로 지원하지 않지만, 좌우 테이블에서 각각 단일 테이블 열의 내부 조인과 UNION ALL select의 사용을 통해 비슷하게 구현할 수 있다. 동일한 예제를 다음과 같이 표현할 수 있다:

``` sql
SELECT employee.LastName, employee.DepartmentID,
       department.DepartmentName, department.DepartmentID
FROM employee
INNER JOIN department ON employee.DepartmentID = department.DepartmentID

UNION ALL

SELECT employee.LastName, employee.DepartmentID,
       cast(NULL as varchar(20)), cast(NULL as integer)
FROM employee
WHERE NOT EXISTS (
    SELECT * FROM department
             WHERE employee.DepartmentID = department.DepartmentID)

UNION ALL

SELECT cast(NULL as varchar(20)), cast(NULL as integer),
       department.DepartmentName, department.DepartmentID
FROM department
WHERE NOT EXISTS (
    SELECT * FROM employee
             WHERE employee.DepartmentID = department.DepartmentID)
```

## 자가 조인

**자가 조인**(self-join)은 한 테이블에서 자기 자신에 조인을 시키는 것이다.\[5\]

### 예제

같은 나라에서 2명의 직원의 모든 쌍을 찾기 위한 질의어가 필요하다. 만약 2개의 별개의 직원 테이블이 있고, 동일한 국적을 가진 두 번째 테이블에 있는 직원이, 첫 번째 테이블에서 직원을 찾는 쿼리가 있다면, 보통의 조인 동작이 테이블에 답하기 위해 사용될 수 있을 것이다. 그러나 모든 직원 정보는 하나의 거대한 테이블에 포함되어 있다.\[6\]

다음과 같이 수정된 `Employee` 테이블이 있다고 하자:

<table>
<caption>Employee Table</caption>
<thead>
<tr class="header">
<th><p>EmployeeID</p></th>
<th><p>LastName</p></th>
<th><p>Country</p></th>
<th><p>DepartmentID</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>123</p></td>
<td><p>Rafferty</p></td>
<td><p>호주</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td><p>124</p></td>
<td><p>Jones</p></td>
<td><p>호주</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>145</p></td>
<td><p>Steinberg</p></td>
<td><p>호주</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>201</p></td>
<td><p>Robinson</p></td>
<td><p>미국</p></td>
<td><p>34</p></td>
</tr>
<tr class="odd">
<td><p>305</p></td>
<td><p>Smith</p></td>
<td><p>독일</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>306</p></td>
<td><p>John</p></td>
<td><p>독일</p></td>
<td></td>
</tr>
</tbody>
</table>


상기 예의 해답 질의어는 다음과 같을 것이다 :

``` sql
SELECT F.EmployeeID, F.LastName, S.EmployeeID, S.LastName, F.Country
FROM Employee F INNER JOIN Employee S ON F.Country = S.Country
WHERE F.EmployeeID < S.EmployeeID
ORDER BY F.EmployeeID, S.EmployeeID;
```

이것은 아래와 같이 생성된 테이블로 이어질 것이다.

| EmployeeID | LastName | EmployeeID | LastName  | Country |
| ---------- | -------- | ---------- | --------- | ------- |
| 123        | Rafferty | 124        | Jones     | 호주      |
| 123        | Rafferty | 145        | Steinberg | 호주      |
| 124        | Jones    | 145        | Steinberg | 호주      |
| 305        | Smith    | 306        | John      | 독일      |

Employee Table after Self-join by Country


이러한 예제를 위해:

  - `F` 와 `S` 는 employee 테이블의 첫 번째, 두 번째를 위한 [앨리어스이다](https://ko.wikipedia.org/wiki/alias_\(SQL\) "wikilink").
  - 조건 `F.Country = S.Country`는 다른 국적의 직원들 사이의 쌍을 배제한다. 예제 질문은 단지 동일 국적의 직원 쌍만 원한다.
  - 조건 `F.EmployeeID < S.EmployeeID` excludes pairings where the `EmployeeID` of the first employee is greater than or equal to the `EmployeeID` of the second employee. In other words, the effect of this condition is to exclude duplicate pairings and self-pairings. 그것이 없다면, 다음과 같이 유용성이 떨어지는 테이블이 생성될 것이다 (아래의 예제 테이블은 단지 결과 중 "독일" 부분만 보여준다):

| EmployeeID | LastName | EmployeeID | LastName | Country |
| ---------- | -------- | ---------- | -------- | ------- |
| 305        | Smith    | 305        | Smith    | 독일      |
| 305        | Smith    | 306        | John     | 독일      |
| 306        | John     | 305        | Smith    | 독일      |
| 306        | John     | 306        | John     | 독일      |


원래의 질문을 충족시키기 위해 중간 쌍의 단지 하나만 필요로 하며, 최상위 그리고 최하위는 이 예제에서 전혀 관심의 대상이 아니다.

## 병합 열

여러 줄을 하나의 열로 병합하기 위해서는 그룹 컨캣 표기법(group_concat notation)을 사용한다.

[MySQL](https://ko.wikipedia.org/wiki/MySQL "wikilink") 과 [CUBRID](https://ko.wikipedia.org/wiki/CUBRID "wikilink")는 그러한 목표를 얻기 위해 `group_concat` 키워드를 사용하며, [PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL "wikilink") 9.0은 `string_agg` 함수를 사용한다. 9.0 이전의 판은 다음과 같이 해야 한다.

`array_to_string(array_agg(value),', ')`

또는 집합 함수를 생성해야 한다.

<table>
<caption>Employee 테이블 사용:</caption>
<thead>
<tr class="header">
<th><p>LastName</p></th>
<th><p>DepartmentID</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Rafferty</p></td>
<td><p>31</p></td>
</tr>
<tr class="even">
<td><p>Jones</p></td>
<td><p>33</p></td>
</tr>
<tr class="odd">
<td><p>Steinberg</p></td>
<td><p>33</p></td>
</tr>
<tr class="even">
<td><p>Robinson</p></td>
<td><p>34</p></td>
</tr>
<tr class="odd">
<td><p>Smith</p></td>
<td><p>34</p></td>
</tr>
<tr class="even">
<td><p>John</p></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>다음의 결과 테이블을 얻기 위해</caption>
<thead>
<tr class="header">
<th><p>DepartmentID</p></th>
<th><p>LastNames</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>John</p></td>
</tr>
<tr class="even">
<td><p>31</p></td>
<td><p>Rafferty</p></td>
</tr>
<tr class="odd">
<td><p>33</p></td>
<td><p>Jones, Steinberg</p></td>
</tr>
<tr class="even">
<td><p>34</p></td>
<td><p>Robinson, Smith</p></td>
</tr>
</tbody>
</table>


\=== MySQL===

``` mysql
SELECT DepartmentID, group_concat(LastName) as LastNames
FROM employee
GROUP BY DepartmentID;
```

### Oracle 11g R2

``` oracle11
SELECT DepartmentID,
  listagg(LastName, ', ') WITHIN GROUP (ORDER BY LastName) as LastNames
FROM employee
GROUP BY DepartmentID;
```

### CUBRID

``` sql
SELECT DepartmentID,
  GROUP_CONCAT(LastName ORDER BY LastName SEPARATOR ',') as LastNames
FROM employee
GROUP BY DepartmentID;
```

### PostgreSQL

우선 질의를 하기 전 함수 _group_concat 과 집합 group_concat이 생성되어야 한다.

``` postgresql
CREATE OR REPLACE FUNCTION _group_concat(text, text)
RETURNS text AS $$
SELECT CASE
WHEN $2 IS NULL THEN $1
WHEN $1 IS NULL THEN $2
ELSE $1 operator(pg_catalog.||) ', ' operator(pg_catalog.||) $2
END
$$ IMMUTABLE LANGUAGE SQL;

error// Join SQL
CREATE AGGREGATE group_concat (
BASETYPE = text,
SFUNC = _group_concat,
STYPE = text
);

SELECT DepartmentID, group_concat(LastName) as LastNames
FROM employee
GROUP BY DepartmentID;
```

9.0 버전에서는:

``` postgresql
SELECT DepartmentID, string_agg(LastName, ', ') as LastNames
FROM employee
GROUP BY DepartmentID;
```

### Microsoft T-SQL

Microsoft SQL Server 2005 이전 버전에서, group_concat 함수는 그러한 쿼리를 날리기 전에 사용자 정의 집합 함수로 만들어져야 한다. 아래에 C\#으로 만든 예제가 있다.

``` csharp
using System;
using System.Collections.Generic;
using System.Data.SqlTypes;
using System.IO;
using Microsoft.SqlServer.Server;

[Serializable]
[SqlUserDefinedAggregate(Format.UserDefined, MaxByteSize=8000)]
public struct group_concat : IBinarySerialize{
 private List values;

 public void Init() {
  this.values = new List();
 }

 public void Accumulate(SqlString value) {
  this.values.Add(value.Value);
 }

 public void Merge(strconcat value) {
  this.values.AddRange(value.values.ToArray());
 }

 public SqlString Terminate() {
  return new SqlString(string.Join(", ", this.values.ToArray()));
 }

 public void Read(BinaryReader r) {
  int itemCount = r.ReadInt32();
  this.values = new List(itemCount);
  for (int i = 0; i < itemCount; i++) {
   this.values.Add(r.ReadString());
  }
 }

 public void Write(BinaryWriter w) {
  w.Write(this.values.Count);
  foreach (string s in this.values) {
   w.Write(s);
  }
 }
}
```

그러면 다음과 같은 쿼리를 이용할 수 있다:

``` tsql
SELECT DepartmentID, dbo.group_concat(LastName) as LastNames
FROM employee
GROUP BY DepartmentID;
```

2005 버전에서는, 이 작업을 FOR XML PATH를 사용하면 된다:

``` tsql
SELECT DepartmentID,
 STUFF(
 (SELECT
 ',' + LastName
 FROM (
 SELECT LastName
 FROM employee e2
 WHERE e1.DepartmentID=e2.DepartmentID OR
 (e1.DepartmentID IS NULL AND e2.DepartmentID IS NULL)
 ) t1
 ORDER BY LastName
 FOR XML PATH('')
 )
 ,1,1, ''
 ) AS LastNames
FROM employee e1
GROUP BY DepartmentID
```

2017 이후 버전에서는 STRING_AGG() 함수를 사용하면 된다.

``` sql numberLines
SELECT  DepartmentID
    ,   STRING_AGG(LastName, ',') WITHIN GROUP (ORDER BY LastName ASC) AS LastNames
FROM    employee
GROUP BY
        DepartmentID
;
```



## 대체

외부 조인의 결과는 또한 INNER JOIN과 조인 조건을 수행하지 않은 주요 테이블 내의 열들의 SELECT 사이에 UNION ALL을 사용함으로써 동일한 결과를 얻을 수 있다. 예제는 다음과 같다.

``` sql
SELECT employee.LastName, employee.DepartmentID, department.DepartmentName
FROM employee
LEFT OUTER JOIN department ON employee.DepartmentID = department.DepartmentID;
```

이것은 다음과 같이 쓸 수도 있다.

``` sql
SELECT employee.LastName, employee.DepartmentID, department.DepartmentName
FROM employee
INNER JOIN department ON employee.DepartmentID = department.DepartmentID

UNION ALL

SELECT employee.LastName, employee.DepartmentID, cast(NULL as varchar(20))
FROM employee
WHERE NOT EXISTS (
    SELECT * FROM department
             WHERE employee.DepartmentID = department.DepartmentID)
```

## 각주

## 외부 링크

  - 특정 제품에 따른
      - [Sybase ASE 15 Joins](http://infocenter.sybase.com/help/index.jsp?topic=/com.sybase.help.ase_15.0.sqlug/html/sqlug/sqlug138.htm)
      - [MySQL 5.5 Joins](http://dev.mysql.com/doc/refman/5.5/en/join.html)
      - [PostgreSQL Join with Query Explain](https://web.archive.org/web/20090928025753/http://www.postgresqlguide.com/retrieving-data-from-multiple-tables-by-using-sql-join.aspx)
      - [PostgreSQL 8.3 Joins](http://www.postgresql.org/docs/8.3/static/tutorial-join.html)
      - [Joins in Microsoft SQL Server](https://web.archive.org/web/20081010173643/http://msdn2.microsoft.com/en-us/library/ms191517.aspx)
      - [Joins in MaxDB 7.6](http://maxdb.sap.com/currentdoc/45/f31c38e95511d5995d00508b5d5211/content.htm)
      - [Joins in Oracle 11g](http://download.oracle.com/docs/cd/B28359_01/server.111/b28286/queries006.htm)
  - 일반
      - [A Visual Explanation of SQL Joins](http://www.codinghorror.com/blog/archives/000976.html)
      - [Another visual explanation of SQL joins, along with some set theory](http://www.halfgaar.net/sql-joins-are-easy)
      - [SQL join types classified with examples](http://www.gplivna.eu/papers/sql_join_types.htm)
      - [An alternative strategy to using FULL OUTER JOIN](http://weblogs.sqlteam.com/jeffs/archive/2007/04/19/Full-Outer-Joins.aspx)
      - [Latest article explaining Join in simple diagrams and relevant code](http://blog.sqlauthority.com/2009/04/13/sql-server-introduction-to-joins-basic-of-joins/)
      - [Visual representation of 7 possible SQL joins between two sets](http://www.flickr.com/photos/mattimattila/8190148857/)

[분류:SQL 키워드](https://ko.wikipedia.org/wiki/분류:SQL_키워드 "wikilink")

1.  [SQL CROSS JOIN](http://www.sqlguides.com/sql_cross_join.php)
2.  [Simplifying Joins with the USING Keyword](http://www.java2s.com/Tutorial/Oracle/0140__Table-Joins/SimplifyingJoinswiththeUSINGKeyword.htm)
3.  \[<http://asktom.oracle.com/pls/asktom/f?p=100:11:0>::::P11_QUESTION_ID:13430766143199 Ask Tom "Oracle support of ANSI joins."\] [Back to basics: inner joins » Eddie Awad's Blog](http://awads.net/wp/2006/03/20/back-to-basics-inner-joins/#comment-2837)
4.
5.
6.  Adapted from