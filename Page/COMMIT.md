> This article is converted from Wikipedia: [COMMIT](https://ko.wikipedia.org/wiki/COMMIT).


**커밋**(commit)은 [데이터베이스 트랜잭션의](../Page/데이터베이스_트랜잭션.md "wikilink") 내용 업데이트를 영구적으로 확정하는 것을 말한다. 일반적으로 트랜잭션 종료시 해당 업데이트를 확정한다는 의미에서 "커밋"이라고 사용한다. [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)의 SQL COMMIT 문은 트랜잭션이 완료될 때 사용되는 트랜잭션의 업데이트가 다른 사용자에서도 보이게 한다. 반대로 업데이트를 취소 처리를 [롤백 (ROLLBACK)이라고](../Page/롤백_\(데이터_관리\).md "wikilink") 하며, 이러한 제어를 약속 제어라고 부른다. SQL에서는 ROLLBACK 문이 그 처리를 한다.

[버전 관리 시스템도](../Page/버전_관리.md "wikilink") 데이터베이스의 일종이며, 다른 사람으로부터 자신의 업데이트를 볼 수 있도록 한다는 의미에서 "커밋"이라는 용어를 사용하고 있다.

## SQL

SQL에서 COMMIT은 [RDBMS](https://ko.wikipedia.org/wiki/RDBMS "wikilink") 내에 있는 [데이터베이스 트랜잭션을](../Page/데이터베이스_트랜잭션.md "wikilink") 종결시키고, 모든 변화를 다른 사용자들이 볼 수 있게 만들어 준다. 일반적인 포맷은 BEGIN WORK 구문으로 시작하여, COMMIT 구문이 나온다. 다른 방법으로 ROLLBACK 구문으로 시작될 수 있으며, 이것은 BEGIN WORK로 시작된 모든 작업을 그 이전으로 되돌린다. COMMIT 구문은 또한 현존하는 [SAVEPOINT](../Page/SAVEPOINT.md "wikilink")가 사용될 수 있을 것이다.

트랜잭션의 측면에서 커밋의 반대는 트랜잭션의 임시적인 변화를 포기하는 것(롤백)이다.

## 버전 관리 시스템의 커밋

[CVS](../Page/CVS.md "wikilink")나 [서브버전](../Page/서브버전.md "wikilink")(SVN) 같은 [버전 관리 시스템에서](https://ko.wikipedia.org/wiki/버전_관리_시스템 "wikilink") 사용되는 커밋은 자신이 작업한 파일의 업데이트를 저장소에 반영시키는 것을 말한다. Visual SourceSafe는 ‘체크인’라고 부른다. 저장소에 커밋하여 저장소에 이미 있는 정보와 업데이트된 파일과의 차이를 취하고 저장소에 업데이트 델타만 업로드 된다. 일반적으로 CVS와 Subversion에서는 다른 사용자가 커밋하여 만일 자신이 업데이트한 곳과 동일한 곳에서 충돌이 일어나 다른 사람이 고생하여 업데이트한 정보를 덮어 쓰는 것을 피하기 위해 커밋하기 전에 업데이트(Visual SourceSafe에서 새로 고침라고 부른다)를 실행하여 자신의 작업 영역을 최신 상태로 유지할 수 있다.

## 같이 보기

  - 자동 커밋

[분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:데이터 관리](https://ko.wikipedia.org/wiki/분류:데이터_관리 "wikilink") [분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink") [분류:트랜잭션 처리](https://ko.wikipedia.org/wiki/분류:트랜잭션_처리 "wikilink")