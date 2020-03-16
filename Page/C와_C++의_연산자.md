> This article is converted from Wikipedia: [C C++ ](https://ko.wikipedia.org/wiki/C_C++_).


이것은 [C와](../Page/C_\(프로그래밍_언어\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") [프로그래밍 언어의](../Page/프로그래밍_언어.md "wikilink") [연산자의](https://ko.wikipedia.org/wiki/연산자_\(프로그래밍\) "wikilink") 목록이다. 나열된 모든 연산자는 C++에 존재한다. 네번째 열("C에 포함됨")은 해당 연산자가 C에 존재하는지를 표시한다. C는 연산자 오버로딩을 지원하지 않는다.

연산자가 오버로드되지 않았다면, `&&`, `||`, `,`([쉼표 연산자](https://ko.wikipedia.org/wiki/쉼표_연산자 "wikilink")) 연산자는 첫 번째 피연산자(operand)가 평가된 시점이 [시퀀스 포인트이다](https://ko.wikipedia.org/wiki/시퀀스_포인트 "wikilink").

C++는 [형 변환](https://ko.wikipedia.org/wiki/형_변환 "wikilink") 연산자인 `const_cast`, `static_cast`, `dynamic_cast`, `reinterpret_cast`를 포함한다. 이들 연산자의 서식은 우선순위 단계가 중요하지 않다는 것을 의미한다.

C와 C++에서 사용 가능한 연산자 중 대부분은 [C\#](../Page/C_샤프.md "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [펄](../Page/펄.md "wikilink"), 그리고 [PHP](../Page/PHP.md "wikilink")와 같은 다른 언어에서도 동일한 우선순위, 결합법칙, 의미론으로 사용가능하다.

## 연산자 표

이 표에서 `a`, `b`, `c`는 경우에 따라 유효한 값(리터럴, 변수 값, 반환 값), 개체 이름, 왼쪽 값(lvalue)을 나타낸다. `R`, `S`, `T`는 자료형을 나타내고 `K`는 클래스나 열거형을 나타낸다.

### 산술 연산자

<table>
<thead>
<tr class="header">
<th><p>연산자 이름</p></th>
<th><p>구문</p></th>
<th><p>오버로드 <wbr/>가능<wbr/>[1]</p></th>
<th><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C에</a> 포함됨[2]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T의 멤버로서</p></td>
<td><p>외부 클래스 정의들</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/C++의_할당_연산자" title="wikilink">기본 할당</a></p></td>
<td><p><code>a </code><strong><code>=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/덧셈" title="wikilink">덧셈</a></p></td>
<td><p><code>a </code><strong><code>+</code></strong><code> b</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/뺄셈.md" title="wikilink">뺄셈</a></p></td>
<td><p><code>a </code><strong><code>-</code></strong><code> b</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/단항_연산" title="wikilink">단항</a> 덧셈<br />
(<a href="https://ko.wikipedia.org/wiki/형_변환" title="wikilink">정수 승급</a>)</p></td>
<td><p><strong><code>+</code></strong><code>a</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>단항 뺄셈<br />
(<a href="https://ko.wikipedia.org/wiki/반수_(수학)" title="wikilink">반수</a>)</p></td>
<td><p><strong><code>-</code></strong><code>a</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/곱셈.md" title="wikilink">곱셈</a></p></td>
<td><p><code>a </code><strong><code>*</code></strong><code> b</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/나눗셈.md" title="wikilink">나눗셈</a></p></td>
<td><p><code>a </code><strong><code>/</code></strong><code> b</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/모듈러_연산" title="wikilink">모듈러</a> (나머지)</p></td>
<td><p><code>a </code><strong><code>%</code></strong><code> b</code></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/증감_연산자.md" title="wikilink">증가</a></p></td>
<td><p>전위</p></td>
<td><p><strong><code>++</code></strong><code>a</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>후위</p></td>
<td><p><code>a</code><strong><code>++</code></strong></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/증감_연산자.md" title="wikilink">감소</a></p></td>
<td><p>전위</p></td>
<td><p><strong><code>--</code></strong><code>a</code></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>후위</p></td>
<td><p><code>a</code><strong><code>--</code></strong></p></td>
<td><p>rowspan="2" </p></td>
<td><p>rowspan="2" </p></td>
</tr>
</tbody>
</table>

### 비교 연산자/관계 연산자

<table>
<thead>
<tr class="header">
<th><p>연산자 </p></th>
<th><p>구문</p></th>
<th><p>오버로드<br />
가능[3]</p></th>
<th><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C에서</a><br />
포함됨[4]</p></th>
<th><p>프로토타입 예제[5]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T의 멤버로서</p></td>
<td><p>외부 클래스 정의들</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>같음</p></td>
<td><p><code>a </code><strong><code>==</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>같지 </p></td>
<td><p><code>a </code><strong><code>!=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>큼</p></td>
<td><p><code>a </code><strong><code>&gt;</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>작음</p></td>
<td><p><code>a </code><strong><code>&lt;</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>크거나<br />
같음</p></td>
<td><p><code>a </code><strong><code>&gt;=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>작거나<br />
같음</p></td>
<td><p><code>a </code><strong><code>&lt;=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>삼단 비교</p></td>
<td><p><code>a </code><strong><code>&lt;=&gt;</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 논리 연산자

<table>
<thead>
<tr class="header">
<th><p>연산자<br />
이름</p></th>
<th><p>구문</p></th>
<th><p>오버로드<br />
가능[6]</p></th>
<th><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C에서</a><br />
포함됨[7]</p></th>
<th><p>프로토타입 예제[8]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T의 멤버로서</p></td>
<td><p>외부 클래스 정의들</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/부정" title="wikilink">논리적<br />
부정 (NOT)</a></p></td>
<td><p><strong><code>!</code></strong><code>a</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/논리곱" title="wikilink">논리적<br />
AND</a></p></td>
<td><p><code>a </code><strong><code>&amp;&amp;</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/논리합" title="wikilink">논리적<br />
OR</a></p></td>
<td><p><code>a '''<nowiki></p></td>
<td><p></nowiki>''' b</code></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

연산자 && 와 || 그리고 , 는 오버로딩하지 말아야 한다.\[9\] 논리 연산이 필요하다면 대신 operator bool () 을 쓰도록 하자.

### 비트 연산자

<table>
<thead>
<tr class="header">
<th><p>연산자<br />
이름</p></th>
<th><p>구문</p></th>
<th><p>오버로드 <wbr/>가능<wbr/>[10]</p></th>
<th><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C에서</a> 포함됨[11]</p></th>
<th><p>프로토타입 예제[12]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T의 멤버로서</p></td>
<td><p>외부 클래스 정의들</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/비트_연산#NOT" title="wikilink">비트 NOT</a></p></td>
<td><p><strong><code>~</code></strong><code>a</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/비트_연산#AND" title="wikilink">비트<br />
AND</a></p></td>
<td><p><code>a </code><strong><code>&amp;</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/비트_연산#OR" title="wikilink">비트<br />
OR</a></p></td>
<td><p><code>a </code><strong><code>|</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td><p>(const T&amp; b) const;|lang=cpp}}</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/비트_연산#XOR" title="wikilink">비트<br />
XOR</a></p></td>
<td><p><code>a </code><strong><code>^</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>비트<br />
왼쪽<br />
시프트[13]</p></td>
<td><p><code>a </code><strong><code>&lt;&lt;</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>비트<br />
오른쪽<br />
시프트[14]</p></td>
<td><p><code>a </code><strong><code>&gt;&gt;</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 복합 할당 연산자

<table>
<thead>
<tr class="header">
<th><p>연산자 이름</p></th>
<th><p>구문</p></th>
<th><p>오버로드 <wbr/>가능<wbr/>[15]</p></th>
<th><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C에서</a> 포함됨[16]</p></th>
<th><p>프로토타입 예제[17]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T의 멤버로서</p></td>
<td><p>외부 클래스 정의들</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>덧셈 할당</p></td>
<td><p><code>a </code><strong><code>+=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>뺄셈 할당</p></td>
<td><p><code>a </code><strong><code>-=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>곱셈 할당</p></td>
<td><p><code>a </code><strong><code>*=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>나눗셈 할당</p></td>
<td><p><code>a </code><strong><code>/=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>모듈러 할당</p></td>
<td><p><code>a </code><strong><code>%=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>비트 AND 할당</p></td>
<td><p><code>a </code><strong><code>&amp;=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>비트 OR 할당</p></td>
<td><p><code>a </code><strong><code>|=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td><p>=(const T&amp; b);|lang=cpp}}</p></td>
</tr>
<tr class="odd">
<td><p>비트 XOR 할당</p></td>
<td><p><code>a </code><strong><code>^=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>비트 왼쪽 시프트 할당</p></td>
<td><p><code>a </code><strong><code>&lt;&lt;=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>비트 오른쪽 시프트 할당</p></td>
<td><p><code>a </code><strong><code>&gt;&gt;=</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 멤버와 포인터 연산자

<table>
<thead>
<tr class="header">
<th><p>연산자 이름</p></th>
<th><p>구문</p></th>
<th><p>오버로드 <wbr/>가능<wbr/>[18]</p></th>
<th><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C에서</a> 포함됨[19]</p></th>
<th><p>프로토타입 예제[20]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T의 멤버로서</p></td>
<td><p>외부 클래스 정의들</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>포인터 <a href="../Page/배열.md" title="wikilink">배열</a></p></td>
<td><p><code>a</code><strong><code>[</code></strong><code>b</code><strong><code>]</code></strong></p></td>
<td></td>
<td></td>
<td><p><br />
</p></td>
</tr>
<tr class="odd">
<td><p>포인터[21]</p></td>
<td><p><strong><code>*</code></strong><code>a</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>참조[22]</p></td>
<td><p><strong><code>&amp;</code></strong><code>a</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>포인터 <code>a</code>에 할당된 객체의 멤버 <code>b</code></p></td>
<td><p><code>a</code><strong><code>-&gt;</code></strong><code>b</code></p></td>
<td></td>
<td></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p>객체 <code>a</code>의 멤버 <code>b</code></p></td>
<td><p><code>a</code><strong><code>.</code></strong><code>b</code></p></td>
<td></td>
<td></td>
<td><p>colspan="2" </p></td>
</tr>
<tr class="odd">
<td><p>포인터 <code>a</code>에 할당된 객체의 멤버<br />
<code>b</code>에 할당된 멤버[23]</p></td>
<td><p><code>a</code><strong><code>-&gt;*</code></strong><code>b</code></p></td>
<td></td>
<td></td>
<td><p>[24]</p></td>
</tr>
<tr class="even">
<td><p>객체 <code>a</code>의 <code>b</code>에 할당된 멤버</p></td>
<td><p><code>a</code><strong><code>.*</code></strong><code>b</code></p></td>
<td></td>
<td></td>
<td><p>colspan="2" </p></td>
</tr>
</tbody>
</table>

### 기타 연산자

<table>
<thead>
<tr class="header">
<th><p>연산자<br />
이름</p></th>
<th><p>구문</p></th>
<th><p>오버로드<br />
가능[25]</p></th>
<th><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C에서</a><br />
포함됨[26]</p></th>
<th><p>프로토타입 예제[27]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T의 멤버로서</p></td>
<td><p>외부 클래스 정의들</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/함수_(프로그래밍).md" title="wikilink">함수</a> 호출<br />
[28]</p></td>
<td><p><code>a</code><strong><code>(</code></strong><code>a1, a2</code><strong><code>)</code></strong></p></td>
<td></td>
<td></td>
<td><p>[29]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/쉼표_연산자" title="wikilink">쉼표</a></p></td>
<td><p><code>a</code><strong><code>,</code></strong><code> b</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/?:.md" title="wikilink">삼항<br />
연산자</a></p></td>
<td><p><code>a </code><strong><code>?</code></strong><code> b </code><strong><code>:</code></strong><code> c</code></p></td>
<td></td>
<td></td>
<td><p>colspan="2" </p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/범위_확인_연산자#C++" title="wikilink">범위 확인</a></p></td>
<td><p><code>a</code><strong><code>::</code></strong><code>b</code></p></td>
<td></td>
<td></td>
<td><p>colspan="2" </p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/sizeof" title="wikilink">Size-of</a></p></td>
<td><p><strong><code>sizeof</code></strong><code>(a)</code>[30]<br />
<strong><code>sizeof</code></strong><code>(</code><em><code>자료형</code></em><code>)</code></p></td>
<td></td>
<td></td>
<td><p>colspan="2" </p></td>
</tr>
<tr class="odd">
<td><p>자료형<br />
식별</p></td>
<td><p><strong><code>typeid</code></strong><code>(a)</code><br />
<strong><code>typeid</code></strong><code>(</code><em><code>자료형</code></em><code>)</code></p></td>
<td></td>
<td></td>
<td><p>colspan="2" </p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/형변환" title="wikilink">캐스트</a></p></td>
<td><p><code>(</code><em><code>자료형</code></em><code>) a</code></p></td>
<td></td>
<td></td>
<td><p>[31]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/new_(c++)" title="wikilink">저장소<br />
할당</a></p></td>
<td><p><strong><code>new</code></strong><code> </code><em><code>자료형</code></em></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>저장소<br />
할당<br />
(배열)</p></td>
<td><p><strong><code>new</code></strong><code> </code><em><code>자료형</code></em><strong><code>[</code></strong><code>n</code><strong><code>]</code></strong></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/연산자_삭제" title="wikilink">저장소<br />
할당<br />
취소</a></p></td>
<td><p><strong><code>delete</code></strong><code> a</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>저장소<br />
할당<br />
취소<br />
(배열)</p></td>
<td><p><strong><code>delete[]</code></strong><code> a</code></p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 연산자 우선순위

다음은 [C와](../Page/C_\(프로그래밍_언어\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 언어에서 모든 연산자의 [우선순위와](../Page/연산의_우선순위.md "wikilink") [결합법칙을](https://ko.wikipedia.org/wiki/연산자_결합법칙 "wikilink") 나열하는 표이다\[32\]. 연산자는 내림차순 우선순위에서, 위에서 아래로 나열된다. 우선순위 내림차순은 연산자와 피연산자를 묶는 행위의 우선순서를 나타낸다. 표현식을 고려해서, 어떤 행 위에 나열된 연산자는 그것의 더 아래쪽 행 위에 나열된 모든 연산자의 이전에 피연산자와 묶인다. 같은 셀에 있는 연산자\[33\]는 주어진 결합법칙의 방향대로 피연산자와 묶인다. 연산자의 우선순위는 오버로딩에 의해 영향받지않는다. 연산자의 피연산자들이 모두 평가된 후에 그 연산자로 결과값이 계산되는 순서로 평가된다.

C와 C++에서 표현식의 구문은 [문맥 자유 문법에](https://ko.wikipedia.org/wiki/문맥_자유_문법 "wikilink") 의해 지정된다. 여기에 주어진 표는 문법으로부터 추론되었다. ISO C 1999년 표준에 대해, 항목 6.5.6 주 71은 C 연산자의 우선순위를 정의하는 사양에 의해 제공되는 C 문법을 정하고, 또한 사양의 항목 순서를 밀접하게 따라가는 문법으로 인한 연산자 우선순위를 정한다:

우선순위 표는, 대부분 적절하지만, 몇 가지 세부 정보를 해결할 수 없다. 특히, [3항 연산자는](https://ko.wikipedia.org/wiki/3항_연산자 "wikilink") 그것의 중간 피연산자로서 어떤 임의의 표현식을 허용함에도 불구하고, 할당 및 쉼표 연산자보다 높은 우선순위가 있는 것으로서 나열된다는 것을 참고한다. 그러므로 `a ? b , c : d`는 `a ? (b, c) : d`로서 해석되고, `(a ? b), (c : d)`로서 무의미하지 않다. 또한, 즉시, C 캐스트 표현식의 괄호묶지않은 결과는 `sizeof`의 피연산자가 될 수 없다는 것을 참고한다. 따라서, `sizeof (int) * x`는 `(sizeof(int)) * x`으로 해석되고 `sizeof ((int) *x)`가 아니다.

| 우선순위                 | 연산자                                                                                                                                   | 설명                                                                                                  | 결합법칙     |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | -------- |
| 1                    | `::`                                                                                                                                  | 범위 확인 (C++만)                                                                                        | 왼쪽에서 오른쪽 |
| 2                    | `++`                                                                                                                                  | 후위 증가                                                                                               |          |
| `--`                 | 후위 감소                                                                                                                                 |                                                                                                     |          |
| `()`                 | 함수 호출                                                                                                                                 |                                                                                                     |          |
| `[]`                 | 배열 첨자                                                                                                                                 |                                                                                                     |          |
| `.`                  | 참조에 의한 요소 선택                                                                                                                          |                                                                                                     |          |
| `->`                 | 포인터를 통해 요소 선택                                                                                                                         |                                                                                                     |          |
| `typeid()`           | [런타임 형식 정보](https://ko.wikipedia.org/wiki/런타임_형식_정보 "wikilink") (C++만) ([typeid](https://ko.wikipedia.org/wiki/typeid "wikilink") 참조) |                                                                                                     |          |
| `const_cast`         | 자료형 캐스트 (C++만) ([const cast](https://ko.wikipedia.org/wiki/const_cast "wikilink") 참조)                                                 |                                                                                                     |          |
| `dynamic_cast`       | 자료형 캐스트 (C++만) ([dynamic cast](https://ko.wikipedia.org/wiki/dynamic_cast "wikilink") 참조)                                             |                                                                                                     |          |
| `reinterpret_cast`   | 자료형 캐스트 (C++만) ([reinterpret cast](https://ko.wikipedia.org/wiki/reinterpret_cast "wikilink") 참조)                                     |                                                                                                     |          |
| `static_cast`        | 자료형 캐스트 (C++만) ([static cast](https://ko.wikipedia.org/wiki/static_cast "wikilink") 참고)                                               |                                                                                                     |          |
| 3                    | `++`                                                                                                                                  | 전위 증가                                                                                               | 오른쪽에서 왼쪽 |
| `--`                 | 전위 감소                                                                                                                                 |                                                                                                     |          |
| `+`                  | 단항 덧셈                                                                                                                                 |                                                                                                     |          |
| `-`                  | 단항 뺄셈                                                                                                                                 |                                                                                                     |          |
| `!`                  | 논리적 NOT                                                                                                                               |                                                                                                     |          |
| `~`                  | 비트 NOT                                                                                                                                |                                                                                                     |          |
| `(`*`자료형`*`)`        | 자료형 캐스트                                                                                                                               |                                                                                                     |          |
| `*`                  | 우회 (역참조)                                                                                                                              |                                                                                                     |          |
| `&`                  | 의-주소                                                                                                                                  |                                                                                                     |          |
| `sizeof`             | [의-크기](https://ko.wikipedia.org/wiki/sizeof "wikilink")                                                                               |                                                                                                     |          |
| `new`, `new[]`       | 동적 메모리 할당 (C++만)                                                                                                                      |                                                                                                     |          |
| `delete`, `delete[]` | 동적 메모리 할당해제 (C++만)                                                                                                                    |                                                                                                     |          |
| 4                    | style="border-bottom-style: none | `.*`                                                                                               | style="border-bottom-style: none | 멤버접근 포인터 (C++만)                                                  | 왼쪽에서 오른쪽 |
| `->*`                | 멤버접근 포인터 (C++만)                                                                                                                       |                                                                                                     |          |
| 5                    | style="border-bottom-style: none | `*`                                                                                                | style="border-bottom-style: none | 곱셈                                                               |          |
| `/`                  | 나눗셈                                                                                                                                   |                                                                                                     |          |
| `%`                  | [계수](https://ko.wikipedia.org/wiki/모듈러_연산 "wikilink") (나머지)                                                                           |                                                                                                     |          |
| 6                    | style="border-bottom-style: none | `+`                                                                                                | style="border-bottom-style: none | 덧셈                                                               |          |
| `-`                  | 뺄셈                                                                                                                                    |                                                                                                     |          |
| 7                    | style="border-bottom-style: none | `<<`                                                                                               | style="border-bottom-style: none | [비트](https://ko.wikipedia.org/wiki/비트_연산 "wikilink") 왼쪽 시프트      |          |
| `>>`                 | [비트](https://ko.wikipedia.org/wiki/비트_연산 "wikilink") 오른쪽 시프트                                                                          |                                                                                                     |          |
| 8                    | `<=>`                                                                                                                                 | 삼단 비교                                                                                               |          |
| 9                    | `<`                                                                                                                                   | [관계적 연산자들에](https://ko.wikipedia.org/wiki/관계형_연산자 "wikilink") 대해 \< 각각의                             |          |
| `<=`                 | 관계적 연산자들에 대해 ≤ 각각의                                                                                                                    |                                                                                                     |          |
| `>`                  | 관계적 연산자들에 대해 \> 각각의                                                                                                                   |                                                                                                     |          |
| `>=`                 | 관계적 연산자들에 대해 ≥ 각각의                                                                                                                    |                                                                                                     |          |
| 10                   | style="border-bottom-style: none | `==`                                                                                               | style="border-bottom-style: none | [관계적 =](https://ko.wikipedia.org/wiki/관계형_연산자#대등 "wikilink") 각각의 |          |
| `!=`                 | 관계적 ≠ 각각의                                                                                                                             |                                                                                                     |          |
| 11                   | `&`                                                                                                                                   | 비트 AND                                                                                              |          |
| 12                   | `^`                                                                                                                                   | 비트 XOR (배타적 or)                                                                                     |          |
| 13                   | `\|`                                                                                                                                  | 비트 OR (포함적 or)                                                                                      |          |
| 14                   | `&&`                                                                                                                                  | 논리 AND                                                                                              |          |
| 15                   | <code><nowiki>                                                                                                                        | </nowiki></code>                                                                                    | 논리 OR    |
| 16                   | `?:`                                                                                                                                  | [3항 연산자](https://ko.wikipedia.org/wiki/3항_연산자 "wikilink") 조건부 ([?:](../Page/?:.md "wikilink") 참조)   | 오른쪽에서 왼쪽 |
| 17                   | `=`                                                                                                                                   | 직접 할당 [(C++ 클래스를 위해 기본적으로 제공됨)](https://ko.wikipedia.org/wiki/C++에서_할당_연산자 "wikilink")              |          |
| `+=`                 | 덧셈에 의한 할당                                                                                                                             |                                                                                                     |          |
| `-=`                 | 뺄셈에 의한 할당                                                                                                                             |                                                                                                     |          |
| `*=`                 | 곱셈에 의한 할당                                                                                                                             |                                                                                                     |          |
| `/=`                 | 나눗셈에 의한 할당                                                                                                                            |                                                                                                     |          |
| `%=`                 | 나머지에 의한 할당                                                                                                                            |                                                                                                     |          |
| `<<=`                | 비트 왼쪽 시프트에 의한 할당                                                                                                                      |                                                                                                     |          |
| `>>=`                | 비트 오른쪽 시프트에 의한 할당                                                                                                                     |                                                                                                     |          |
| `&=`                 | 비트 AND에 의한 할당                                                                                                                         |                                                                                                     |          |
| `^=`                 | 비트 XOR에 의한 할당                                                                                                                         |                                                                                                     |          |
| `\|=`                | 비트 OR에 의한 할당                                                                                                                          |                                                                                                     |          |
| 18                   | `throw`                                                                                                                               | 던지기 연산자 (던지기 예외, C++만)                                                                              |          |
| 19                   | `,`                                                                                                                                   | [쉼표](https://ko.wikipedia.org/wiki/쉼표_연산자 "wikilink")                                               | 왼쪽에서 오른쪽 |

### 참고 사항

우선순위 표는 명시적으로 괄호에 의해 지정되지 않을 때, 체인화된 표현식들에서 바인딩의 순서를 결정한다.

  - 예를 들어, `++x*3`은 얼핏 보면 모호해 보이지만, 우선순위 표에 따르면 `x`는 `*`연산자보다 전위 `++`연산자를 더 우선시하고, 따라서 `++x` 연산을 수행한 후에 `x*3` 연산을 수행하게 된다.
  - `3*x++`도 마찬가지로, 후위 `++`연산자가 가장 나중에 실행될 것처럼 보이지만, 우선순위에 따라 `x++` 연산을 먼저 수행하게 된다. 그러나 `x++` 연산은 후위 연산자라서 변수의 값을 사용 후에 증가시키므로, 결국 출력값은 `x*3`으로 출력이 된 후에, x값이 증가한다.

[right](https://ko.wikipedia.org/wiki/파일:Precedence_2.png "wikilink")

  - 우선순위 또는 바인딩의 문제를 추상화한, 오른쪽 그림을 보자. 컴파일러의 직업은 여러 `y`에게 바인딩으로 경쟁하는 단항 연산자들\[34\]중 하나인, 표현식으로 도표를 해결하는 것이다. 우선순위 표의 순서는 각 행동에 대한 최종 하위-표현식들로 해결된다: `( . )[ i ]`은 오직 `y`에 대해 작동하고, `( . )++`은 오직 `y[i]`에 대해 작동하고, `2*( . )`은 오직 `y[i]++`에 대해 작동하고 `3+( . )`은 '오직' `2*((y[i])++)`에 대해 작동한다. 어떤 하위 표현식이 우선순위 표에서 명확한 각 연산자에 의해서 작동되지만 각 연산자의 행위가 우선순위 표에 의해결되지 않을 때를 참고하는 것은 중요하다; 이 예제에서, `( . )++` 연산자는 오직 우선순위 규칙에 의해 `y[i]`에서 작동하지만 단독 바인딩 수준들은 후위 연산자 ++의 타이밍을 표시하지 않는다\[35\].

다중-문자 순서들을 포함하고 있는 연산자의 대부분은 각 문자의 연산자 이름에서 내장된 "이름"이 주어진다. 예를 들어, `+=` 및 `-=`은 더 자세한 "덧셈에 의한 할당" 및 "뺄셈에 의한 할당" 대신에, '덧셈 등호(들)' 및 '뺄셈 등호(들)'이라고 자주 부른다.

C와 C++에서 연산자의 바인딩은 (해당 규칙에서)오히려 우선순위 표보다, 인수분해된 언어 문법에 의해 지정된다. 이것은 몇 가지 미묘한 갈등을 만든다. 예를 들어, C에서, 조건부 표현식에 대한 구문은:

`논리적 OR 표현식 ? `[`표현식`](https://ko.wikipedia.org/wiki/표현식 "wikilink")` : 조건부-표현`

하지만 C++에서 그것은:

`논리적 OR 표현식 ? `[`표현식`](https://ko.wikipedia.org/wiki/표현식 "wikilink")` : 할당-표현`

따라서 표현식:

``` text
e = a < d ? a++ : a = d
```

은 두 언어에서 다르게 분석되었다. C에서, 이 표현은 구문 오류이지만, 많은 컴파일러는 그것을 이와 같이 분석한다:  lvalue가 아닌 조건 표현식(`a++`일 수 있다)의 결과 때문에, 이것은 의미론적 오류이다. C++에서, 그것은 이와 같이 분석한다:  그리고 그것은 올바른 표현식이다.

비트 논리 연산자의 우선순위는 비판받고 있다.\[36\] 개념적으로, `&`와 `|`은 `+`와 `*`같이 산술 연산자이다.

표현식 `a & b == 7`은 `a & (b == 7)`로 분석했던 반면 표현식 `a + b == 7`은 구문적으로 `(a + b) == 7`로 분석했다. 이것은 그들이 다른방법으로 했던 것보다 더 자주 사용되는 괄호가 필요하다.

### C++ 연산자 동의어

C++는 연산자들의 숫자에 대한 별명으로서 작동하는 키워드를 정의한다:\[37\] `and (&&), bitand (&), and_eq (&=), or (||), bitor (|), or_eq (|=), xor (^), xor_eq (^=), not (!), not_eq (!=), compl (~)`. 그것들은 그들이 각 연산자의 *이름* (문자 열)에 대한 간단한 텍스트 별명을 제외한, 다른 이름 아래에서 연산자가 같지 않음으로 그들이 대체하는 상징으로서 같은 방법을 정확하게 사용될 수 있다. 예를 들어, `bitand`는 비트 연산자뿐만 아니라 address-of 연산자를 대체하는 데 사용될 수 있고, 그것이 심지어 참조 자료형들을 지정하는 데 사용될 수 있다.

ANSI C 사양은 헤더 파일 [`iso646.h`](https://ko.wikipedia.org/wiki/iso646.h "wikilink")에서 전처리 매크로로 이러한 키워드에 대한 허용을 만든다. C와의 호환성을 위해, C++는 헤더 [`ciso646`](https://ko.wikipedia.org/wiki/ciso646 "wikilink")을 제공하고, 또한\#include\<ciso646.h\>는 효과가 없다.

## 참고 문헌 및 각주

  -
## 주해

## 외부 링크

  - [C++ 연산자](http://cppreference.com/wiki/language/operators)
  - \[<http://msdn.microsoft.com/en-us/library/e1e3921c(VS.80>).aspx C와 C++에서 전위 연산자 대 후위 연산자\]
  - [C 프로그래밍에서 연산자](https://web.archive.org/web/20110924093643/http://www.allcompiler.com/2011/07/operators-in-c.html)

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:C++](https://ko.wikipedia.org/wiki/분류:C++ "wikilink") [분류:연산자 (프로그래밍)](https://ko.wikipedia.org/wiki/분류:연산자_\(프로그래밍\) "wikilink")

1.  연산자가 C++에서 오버로드 가능한(*overloadable*) 것을 의미한다.
2.  C에서 연산자가 있고 의미론적 의미를 가지는 것을 의미한다.(C는 [연산자 오버로딩을](../Page/연산자_오버로딩.md "wikilink") 지원하지 않는다.)
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20. T, T2 및 R은 모든 자료형이다.
21. 주소 `a`에 할당된 객체
22. `a`객체의 원본
23.
24.
25.
26.
27. T, R, Arg1 및 Arg2는 모든 자료형이다.
28. [함수 개체를](https://ko.wikipedia.org/wiki/함수_개체 "wikilink") 살펴본다.
29. Overload may accept zero or more arguments.
30.
31. 사용자 정의 변환에 대해, 반환 자료형은 절대적 및 필연적으로 연산자 이름과 일치한다.
32. 연산자는 또한 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [펄](../Page/펄.md "wikilink"), [PHP](../Page/PHP.md "wikilink") 및 많은 다른 최근 언어가 존재할 때, 우선순위는 그 주어진 것과 동일하다.
33. 여기는 셀에 나열된 연산자의 여러 행이 될 수 있다
34. 이것들을 `3+( . ), 2*( . ), ( . )++, ( . )[ i ]`이라고 부른다.
35. ( . )++ 연산자는 오직 `y[i]`이 표현식에서 평가된 후에 영향을 끼친다.
36. <http://cm.bell-labs.com/cm/cs/who/dmr/chist.html>
37.