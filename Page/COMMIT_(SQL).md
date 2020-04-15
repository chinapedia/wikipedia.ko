> This article is converted from Wikipedia: [COMMIT \(SQL\)](https://ko.wikipedia.org/wiki/COMMIT_\(SQL\)).


**`COMMIT`** 문은 [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)에서 트랜잭션을 종료하고 다른 사용자에게 변경된 모든 사항을 보이도록 만드는 문이다.\[1\]\[2\] 일반적으로 트랜잭션 종료시 해당 업데이트를 확정한다는 의미에서 "커밋"이라고 사용한다. 반대로 업데이트를 취소 처리를 [롤백 (ROLLBACK)이라고](../Page/롤백_\(데이터_관리\).md "wikilink") 하며, 이러한 제어를 약속 제어라고 부른다. SQL에서는 ROLLBACK 문이 그 처리를 한다.

## SQL

SQL에서 COMMIT은 [RDBMS](https://ko.wikipedia.org/wiki/RDBMS "wikilink") 내에 있는 [데이터베이스 트랜잭션을](../Page/데이터베이스_트랜잭션.md "wikilink") 종결시키고, 모든 변화를 다른 사용자들이 볼 수 있게 만들어 준다. 일반적인 포맷은 BEGIN WORK 구문으로 시작하여, COMMIT 구문이 나온다. 다른 방법으로 ROLLBACK 구문으로 시작될 수 있으며, 이것은 BEGIN WORK로 시작된 모든 작업을 그 이전으로 되돌린다. COMMIT 구문은 또한 현존하는 [SAVEPOINT](../Page/SAVEPOINT.md "wikilink")가 사용될 수 있을 것이다.

트랜잭션의 측면에서 커밋의 반대는 트랜잭션의 임시적인 변화를 포기하는 것(롤백)이다.

## 같이 보기

  - [자동 커밋](https://ko.wikipedia.org/wiki/자동_커밋 "wikilink")

## 각주

[분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:데이터 관리](https://ko.wikipedia.org/wiki/분류:데이터_관리 "wikilink") [분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink") [분류:트랜잭션 처리](https://ko.wikipedia.org/wiki/분류:트랜잭션_처리 "wikilink")

1.
2.