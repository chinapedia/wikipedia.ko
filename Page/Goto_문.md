> This article is converted from Wikipedia: [Goto ](https://ko.wikipedia.org/wiki/Goto_).


**goto 문**은 여러 [프로그래밍 언어에](../Page/프로그래밍_언어.md "wikilink") 등장하는 프로그램의 어느 부분에서 [행번호](https://ko.wikipedia.org/wiki/행번호 "wikilink")나 [레이블이](https://ko.wikipedia.org/wiki/레이블_\(전산학\) "wikilink") 있는 다른 부분으로 건너뛸 때 사용하는 명령이다. 프로그램의 흐름을 바꾸는 기본적인 명령이며, 다른 흐름 제어문도 컴파일러가 goto 문과 비슷하게 바꾼다.

goto 문은 [포트란](../Page/포트란.md "wikilink"), [알골](https://ko.wikipedia.org/wiki/알골_프로그래밍_언어 "wikilink"), [코볼](../Page/코볼.md "wikilink"), [스노볼](https://ko.wikipedia.org/wiki/스노볼 "wikilink"), [베이직](../Page/베이직.md "wikilink"), [커먼 리스프](../Page/커먼_리스프.md "wikilink"), [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [D](../Page/D_\(프로그래밍_언어\).md "wikilink"), [파스칼](../Page/파스칼_\(프로그래밍_언어\).md "wikilink"), [펄](../Page/펄.md "wikilink"), [PHP](../Page/PHP.md "wikilink")7 등지에서 사용되며, 특히 [어셈블리에서](../Page/어셈블리어.md "wikilink") 많이 발견된다. 어셈블리어에서는 goto 대신에 BRA(branch에서 유래), [JMP](../Page/JMP_\(x86_명령어\).md "wikilink"), JUMP 등으로 쓰이기도 한다.

그러나 goto 문이 모든 [고급언어](https://ko.wikipedia.org/wiki/고급언어 "wikilink")에서 사용 가능한 것은 아니다. 예를 들어, [자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") 같은 언어에서 goto는 [예약어](https://ko.wikipedia.org/wiki/예약어 "wikilink")이긴 하지만 아무 기능을 하지 않는다.

## 비판

고급 언어에서 goto 문은 비판의 대상이 되어 왔는데, goto 문이 과도하게 사용되면 읽고 유지하기 힘든 [스파게티 코드가](https://ko.wikipedia.org/wiki/스파게티_코드 "wikilink") 나오기 쉽기 때문이다. [구조적 프로그래밍은](../Page/구조적_프로그래밍.md "wikilink") [1960년대](../Page/1960년대.md "wikilink")와 [1970년대](https://ko.wikipedia.org/wiki/1970년대 "wikilink")에 더 두드러졌는데, 많은 [컴퓨터 과학자들의](../Page/컴퓨터_과학자.md "wikilink") 결론은 프로그램이 항상 goto 문 대신 일명 ‘구조적’인 흐름 제어문([순환문](https://ko.wikipedia.org/wiki/순환문 "wikilink"), if-then-else문)을 사용해야 한다는 것이다.\[1\] 그러나 goto 문의 사용이 종종 나쁜 습관이긴 하지만, 많은 프로그래밍 언어에서 goto 문을 사용하지 않고는 간단히 되지 않는 경우(중첩 순환문을 빠져나갈 때나 [예외 처리할](../Page/예외_처리.md "wikilink") 때)가 있다고 주장하는 사람들이 있다.

goto 문에 대한 한 가지 유명한 비판은 [1968년](../Page/1968년.md "wikilink")에 [에츠허르 데이크스트라의](../Page/에츠허르_데이크스트라.md "wikilink") 'goto 문의 해로움'\[2\] 이라는 서신이다. 이 서신에서 데이크스트라는 더 높은 수준의 언어에서는 goto 문을 제한하지 않으면 안된다고 했는데, 이것은 프로그램의 정확성을 분석하고 증명하는 것을(특히 순환문을 포함해서) 어렵게 하기 때문이라고 했다. [도널드 커누스의](https://ko.wikipedia.org/wiki/도널드_커누스 "wikilink") 'goto 문을 사용한 구조적 프로그래밍'\[3\] 에서는 goto의 적절한 위치를 고찰한다. 일반적으로 이것들은 특정 프로그래밍 구조가 없기 때문이다. 이런 경우들에서 goto 문은 항상 원하는 구조를 에뮬레이트 할 수 있고, 따라서 이것이 프로그래밍의 기본적인 요소의 하나라는 것이다. 다른 해법은 [매크로를](../Page/매크로_\(컴퓨터_과학\).md "wikilink") 이용하여 원하는 제어 구조를 만드는 것이다.([리스프](../Page/리스프.md "wikilink")와 그 변종이나 [포스에서는](https://ko.wikipedia.org/wiki/포스_프로그래밍_언어 "wikilink") 이렇게 해서 대부분의 일을 할 수 있다.)

## 변형

  - 계산된 goto 문(Computed GOTO): 수식의 값에 따라 몇 군데의 레이블로 분기하거나, 변수에 저장되어 있는 레이블로 분기한다. 계산된 goto 문은 보통 goto 문보다 문제가 더 심각한데, 프로그래머가 어떤 구문을 본다고 해도 다음에 무엇이 수행될지 알 수 없기 때문이다.
      - [베이직](../Page/베이직.md "wikilink")의 ON goto 문은 전자의 계산된 goto 문을 지원하며, 각각의 사례별로 분기에 유용하다.
      - [C에서는](../Page/C_\(프로그래밍_언어\).md "wikilink") [Switch 문을](../Page/Switch_문.md "wikilink") 지원한다. 어떤 C 컴파일러들은 레이블 변수에 따라 분기하는 goto 문을 제공하기도 한다.

<!-- end list -->

  - [컨티뉴에이션](https://ko.wikipedia.org/wiki/컨티뉴에이션 "wikilink")(): 프로그램의 임의의 위치에서 기억했던 위치로 분기하는 점에서 계산된 goto 문과 비슷하다. 그러나 이어하기는 현재 함수를 벗어날 수 있지만 goto 문은 그렇지 않기 때문에 이어하기가 더 유연하다. 이어하기를 실행하면 보통 분기하는 것뿐만 아니라 보통 프로그램의 [호출 스택을](https://ko.wikipedia.org/wiki/호출_스택 "wikilink") 조절하는 것까지 한다.

<!-- end list -->

  - 베이직 언어를 [패러디](https://ko.wikipedia.org/wiki/패러디 "wikilink")한 [인터칼](https://ko.wikipedia.org/wiki/인터칼 "wikilink")과 같은 언어에서는 [COME FROM 문을](https://ko.wikipedia.org/wiki/COME_FROM_문 "wikilink") goto 문 대신에 쓰기도 한다.

<!-- end list -->

  - [펄](../Page/펄.md "wikilink")과 같은 언어에서는 @_variable에 있는 현재 인자를 사용하여 서브루틴을 호출하는 방법으로 goto 문을 사용한다.

## 읽을거리

  - [항해형 데이터베이스](https://ko.wikipedia.org/wiki/항해형_데이터베이스 "wikilink")

## 각주

## 외부 링크

  - [A Structured Discipline of Programming](https://web.archive.org/web/20090822145609/http://www.geek-central.gen.nz/peeves/programming_discipline.html)

[분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink") [분류:에츠허르 데이크스트라](https://ko.wikipedia.org/wiki/분류:에츠허르_데이크스트라 "wikilink")

1.
2.   [에츠허르 데이크스트라](../Page/에츠허르_데이크스트라.md "wikilink"): [Go To Statement Considered Harmful](http://www.acm.org/classics/oct95/) . *Communications of the ACM* **11**:3 (1968), 147–148.
3.   [도널드 커누스](https://ko.wikipedia.org/wiki/도널드_커누스 "wikilink"): [Structured Programming with Goto Statements](http://pplab.snu.ac.kr/courses/adv_pl04/papers/p261-knuth.pdf). *Computing Surveys* **6**:4 (1974), 261–301.