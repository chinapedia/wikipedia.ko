> This article is converted from Wikipedia: [CRUD](https://ko.wikipedia.org/wiki/CRUD).


**CRUD**는 대부분의 [컴퓨터](../Page/컴퓨터.md "wikilink") [소프트웨어](../Page/소프트웨어.md "wikilink")가 가지는 기본적인 데이터 처리 기능인 Create(생성), Read(읽기), Update(갱신), Delete(삭제)를 묶어서 일컫는 말이다. 사용자 인터페이스가 갖추어야 할 기능(정보의 참조/검색/갱신)을 가리키는 용어로서도 사용된다.

CRUD 대신에 다음과 같은 유사용어가 사용되기도 한다.

  - ABCD: add(추가), browse(보기), change(변경), delete(삭제)
  - ACID: add(추가), change(변경), inquire(질의), delete(삭제)\[1\]
  - BREAD: browse(보기), read(읽기), edit(편집), add(추가), delete(삭제)
  - VADE(R): view(참조), add(추가), delete(삭제), edit(편집), 트랜잭션 처리에서는 restore(복원) 추가

각 문자는 다음과 같이 표준 SQL문으로 대응 가능하다.

| 이름                 | 조작        | SQL    |
| ------------------ | --------- | ------ |
| Create             | 생성        | INSERT |
| Read(또는 Retrieve)  | 읽기(또는 인출) | SELECT |
| Update             | 갱신        | UPDATE |
| Delete(또는 Destroy) | 삭제(또는 파괴) | DELETE |

CRUD 용어를 최초로 사용한 논문으로는 Kilov, H(1990)의 논문이며, 그 개념은 Kilov(1998)에도 자세히 서술되어 있다.

유저 인터페이스 CRUD는, 여러 [응용 프로그램의](https://ko.wikipedia.org/wiki/응용_프로그램 "wikilink") 사용자 인터페이스에도 들어맞는다. 예를 들어, 주소록나 전화번호부 소프트웨어를 생각해볼 수 있다. 여기서 기본적인 기록 단위는 각 개인의 연락처이다. 다음과 같은 기능들은 가장 간단한 것이면서도 필수적이다.

  - 새로운 연락처 정보를 추가할 수 있다.
  - 기존의 연락처 정보를 검색할 수 있다.
  - 기존의 연락처 정보를 편집할 수 있다.
  - 기존의 연락처 정보를 삭제할 수 있다.

이러한 4개의 조작을 모두 할 수 없다면 그 [소프트웨어](../Page/소프트웨어.md "wikilink")는 완전하다고 할 수 없다. 이들 기능은 매우 기본적이기 때문에, 한 묶음으로 설명되는 경우가 많다.

## 각주

[분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink")

1.  트랜잭션(transaction) 분야에서 사용되는 ACID와는 다른 것이다. 혼동하기 쉬우므로 주의가 필요하다.