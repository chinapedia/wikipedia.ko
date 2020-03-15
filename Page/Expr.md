> This article is converted from Wikipedia: [Expr](https://ko.wikipedia.org/wiki/Expr).


**expr**은 [명령 줄](https://ko.wikipedia.org/wiki/명령_줄_인터페이스 "wikilink") [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 유틸리티의 하나로, [식을](https://ko.wikipedia.org/wiki/수식 "wikilink") 평가하고 일치하는 값을 출력한다. [유닉스 v7에](https://ko.wikipedia.org/wiki/버전_7_유닉스 "wikilink") 처음 등장하였다.

문법: `expr (식)`

expr은 패턴 일치 [정규 표현식을](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 포함하여 [정수](https://ko.wikipedia.org/wiki/정수 "wikilink")나 [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink") 식을 평가한다.

사용 가능한 연산자는 다음과 같다.

  - 정수의 경우: 더하기, 빼기, 곱하기, 나누기, 계수(modulus)
  - 문자열의 경우: 정규 표현식 찾기, 문자열 내의 문자들의 집합을 찾기. 일부 버전에서는: 부스트링 찾기, 문자열의 길이
  - 둘 중 하나에 대해: 비교 (동등, 동등하지 않음, 보다 작음 등)

다음은 [불리언 식을](https://ko.wikipedia.org/wiki/불리언_식 "wikilink") 수반하는 예이다:

`expr length  "abcdef"  "<"  5  "|"  15  -  4  ">"  8`

이 예의 출력값은 "1"이다. 길이 "abcdef"가 6인데, 이는 5 보다 작지 않기 때문에 발생한다. (그러므로 |의 좌측은 0을 반환) 그러나 15 빼기 4는 11이며 이는 8보다 크므로 우측은 참이 되며 "or"를 참으로 만들면서 결과값이 1로 된다. 프로그램 [종료 상태는](../Page/종료_상태.md "wikilink") 이 예에서 0으로 된다.

순수 산술에서 [bc를](https://ko.wikipedia.org/wiki/Bc_프로그래밍_언어 "wikilink") 사용하는 것이 더 편리한 경우도 있다. 이를테면 다음과 같다:

`echo "3*4+14/2" | bc`

식을 하나의 문으로 받아들인다.

## 외부 링크

  -
  - [expr invocation in GNU coreutils manual](https://www.gnu.org/software/coreutils/manual/html_node/expr-invocation.html#expr-invocation)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")