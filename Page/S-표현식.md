> This article is converted from Wikipedia: [S-](https://ko.wikipedia.org/wiki/S-).


**S-표현식**, **S-expression** 또는 **sexp**라는 용어는 (S는 Symbolic을 의미) 구조적인 데이터를 사람이 읽을 수 있는 텍스트 형태로 나타내는 방법을 가리킨다. S-표현식은 대체로 [리스프](../Page/리스프.md "wikilink") 어족의 프로그래밍 언어에서 사용되는 것으로 잘 알려져 있다. 또한 리스프에서 파생된 언어인 [DSSSL](https://ko.wikipedia.org/wiki/Document_Style_Semantics_and_Specification_Language "wikilink"), [IMAP](https://ko.wikipedia.org/wiki/IMAP "wikilink")와 같은 통신 프로토콜에서의 마크업, 그리고 [존 매카시의](../Page/존_매카시_\(컴퓨터_과학자\).md "wikilink") [CBCL에서도](https://ko.wikipedia.org/wiki/Common_Business_Communication_Language "wikilink") S-표현식이 사용되고 있다. 상세한 문법과 제공되는 자료형은 언어들에 따라서 다르지만 가장 일반적인 특징은 괄호로 둘러싸인 prefix 표기법이다 ([폴란드 표기법이라고도](../Page/폴란드_표기법.md "wikilink") 부름).

S-표현식은 리스프에서 코드와 데이터 모두를 표현하는 데 사용된다([리스프](../Page/리스프.md "wikilink") 참조). S-표현식은 [M-표현식](https://ko.wikipedia.org/wiki/M-표현식 "wikilink")으로 다루어지던 데이터를 위한 것이었지만 최초의 리스프 구현은 S-표현식으로 인코딩된 M-표현식의 [인터프리터](../Page/인터프리터.md "wikilink")였고 리스프 프로그래머들은 곧 코드와 데이터 양쪽에서 S-표현식을 사용하는 것에 익숙해졌다.

S-표현식은 수, 또는 특별한 아톰 `nil`와 `t`를 포함하는 [리스프 아톰](https://ko.wikipedia.org/wiki/리스프_아톰 "wikilink"), 또는 (x . y)로 쓰는 [cons 쌍과](https://ko.wikipedia.org/wiki/cons_쌍 "wikilink") 같은 단일 객체가 될 수 있다. 더 긴 리스트는 중첩된 cons 쌍으로 만들어진다. 예를 들어 `(1 . (2 . (3 . nil)))`는 `(1 2 3)`로 편리하게 표시한다.

프로그램 코드는 prefix 표기법을 이용해서 S-표현식으로 나타낼 수 있다. 리스프 프로그램을 작성하기 위해 흔히 사용하는 syntactic sugar로 `(quote x)`를 `'x`로 축약해 나타내는 것이 있다.

## 예제

다음은 [계승](../Page/계승.md "wikilink")(factorial)을 구하는 코드이다.

### [커먼 리스프](../Page/커먼_리스프.md "wikilink")

``` lisp
 (defun factorial (x)
    (if (zerop x) 1
        (* x (factorial (- x 1)))))
```

### [스킴](../Page/스킴_\(프로그래밍_언어\).md "wikilink")

``` scheme
 (define (factorial x)
     (if (zero? x) 1
         (* x (factorial (- x 1)))))
```

## 표준화

[1997년](../Page/1997년.md "wikilink") 5월, Ron Rivest는 [RFC](../Page/RFC.md "wikilink")로 출판하기 위해 인터넷-드래프트\[1\]를 제출하였다. 그 드래프트 문서는 리스프 S-표현식에 기초해서 문법을 정의하긴 했지만 특정 프로그래밍을 위해서가 아닌 일반적인 목적의 데이터 저장과 교환을 위한 의도\[2\]로 작성되었다. 그 문서는 RFC로 인정받지는 못했지만 다른 RFC 문서들\[3\]과 몇몇 다른 문서들이 참조하거나 인용하였다.\[4\]

Rivest의 형식은 S-표현식을 octet-문자열 ([바이트](../Page/바이트.md "wikilink")의 나열) 또는 다른 S-표현식의 유한한 리스트로 정의한다. 이 구조를 표현하는 세 가지 교환 형식은 다음과 같다. 첫 번째는 "향상된 전달(advanced transport)"로 형식이 매우 유연하며 리스프에서의 표현식과 문법적으로 유사하지만 완전히 동일하지는 않다. 예를 들어, "향상된 전달"에서는 octet-문자열을 verbatim (문자열의 길이 뒤에 콜론이 나오고 그 뒤에 원래의 문자열 전체가 나오는 형식의 문자열), escape 문자들을 허용하는 따옴표로 둘러싸인 형식, [십육진법](../Page/십육진법.md "wikilink"), 또는 [베이스64](https://ko.wikipedia.org/wiki/베이스64 "wikilink")로 나타내거나 특정한 조건을 만족하는 "토큰"으로 바로 나타낼 수 있다. (Rivest의 토큰은 편리성을 위해 만들어졌고 다른 문자열들과 정확히 같게 취급되지만 리스프의 토큰은 명확한 문법적인 의미를 가지고 있다는 점에서 다르다.) 두 번째 교환형식 "정규 표현(canonical representation)"은 더 간결하고 분석하기 쉬우며 모든 추상 S-표현식에 대해서 유일하게 표현할 의도로 만들어졌다. 이 형식은 오직 verbatim 문자열만을 허용하고 문자열 바깥에서 whitespace를 사용하는 것을 금지한다. 마지막으로 "기본 전달 표현(basic transport representation)"은 정규 표현이거나 정규 표현을 베이스64로 인코딩하고 [대괄호](https://ko.wikipedia.org/wiki/대괄호 "wikilink")로 둘러싼 것이다. 후자는 정규적으로 인코딩된 S-표현식을 문자열 간격을 바꾸는 시스템 (예를 들어, 이메일 시스템은 80 글자를 넘는 줄은 줄바꿈을 한다)에서 안전하게 전달하기 위한 것이다.

이 형식은 SPKI 이외에는 널리 받아들여지지 못했다. Rivest의 [S-expressions 웹페이지](http://theory.lcs.mit.edu/~rivest/sexp.html)에서 [C로](../Page/C_\(프로그래밍_언어\).md "wikilink") 짜여진 파서와 생성기 소스 코드를 제공한다. 이 파서와 생성기는 비록 [저작권](../Page/저작권.md "wikilink")이 불분명하지만 이론적으로 다른 시스템에 적용될 수 있다. 하지만 이 형식을 독립적으로 구현하는 데는 제약이 없다.

## 함께 보기

  - [리스프](../Page/리스프.md "wikilink")(LISP)
  - [M-expression](https://ko.wikipedia.org/wiki/M-expression "wikilink")
  - [car and cdr](https://ko.wikipedia.org/wiki/car_and_cdr "wikilink")
  - [cons](https://ko.wikipedia.org/wiki/cons "wikilink")

## 각주

<references/>

[분류:리스프](https://ko.wikipedia.org/wiki/분류:리스프 "wikilink") [분류:데이터 직렬화 포맷](https://ko.wikipedia.org/wiki/분류:데이터_직렬화_포맷 "wikilink")

1.  <http://people.csail.mit.edu/rivest/Sexp.txt>
2.  [XML](../Page/XML.md "wikilink")과 비슷하다.
3.  예: RFC 2693
4.  <http://scholar.google.com/scholar?hl=en&lr=&safe=off&q=rivest+sexp&btnG=Search>