> This article is converted from Wikipedia: [While 루프](https://ko.wikipedia.org/wiki/While_루프).


[섬네일](https://ko.wikipedia.org/wiki/파일:While-loop-diagram.svg "wikilink") 대부분의 컴퓨터 [프로그래밍](https://ko.wikipedia.org/wiki/프로그래밍 "wikilink") 언어에서 **while 루프**는 [반복문](https://ko.wikipedia.org/wiki/반복문 "wikilink")의 일종으로, 주어진 [불린 자료형](https://ko.wikipedia.org/wiki/불린_자료형 "wikilink") 조건을 기반으로 코드가 반복적으로 수행할 수 있게 도와준다. 이 while 루프는 [if 문의](../Page/조건문.md "wikilink") 반복으로 생각할 수도 있다.

while은 코드와 조건의 블록을 이루고 있다. 조건이 [true라면](https://ko.wikipedia.org/wiki/진리값 "wikilink") 블록 안의 코드는 실행한다. 조건이 false가 될 때까지 이 작업을 반복한다. 블록을 실행하기 전에 while 루프를 검사하므로 제어 구조는 **사전 시험 루프**(pre-test loop)로 불리기도 한다. 루프를 실행한 뒤에 조건을 시험하는 [do while 루프와](https://ko.wikipedia.org/wiki/do_while_루프 "wikilink") 비교된다.

이를테면, [C 프로그래밍 언어에서](../Page/C_\(프로그래밍_언어\).md "wikilink") (같은 구문을 사용하는 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에도 해당), 다음과 같은 코드의 파편은

``` c
x = 0;
while (x < 3) {
   x++;
}
```

먼저 x가 3보다 작은지를 검사하고 작을 경우 1씩 숫자를 더한다. 조건을 다시 검사하고 다시 실행하여 [변수](https://ko.wikipedia.org/wiki/변수 "wikilink") x가 값 3을 가질 때까지 이 과정을 반복한다.

물론 언제나 "true"라는 조건을 성립하게 만들 수도 있으며, 이때 [무한 반복을](https://ko.wikipedia.org/wiki/무한_루프 "wikilink") 만들어 낸다. 고의로 이러한 루프를 만들 경우, [break문과](../Page/제어_흐름.md "wikilink") 같은 다른 제어 구조를 사용하여 루프를 끝낼 수 있다.

## 같은 구조

``` c
while (condition) {
   statements;
}
```

는

``` c
while (true) {
   if (!condition) break;
   statements;
}
```

또는

``` c
   goto TEST;
LOOPSTART:
   statements;
TEST:
   if (condition) goto LOOPSTART;
```

와 같다.

또한 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 계열 언어에서 while 루프는 초기화나 셈식(counting expression)이 없는 [for 루프이다](https://ko.wikipedia.org/wiki/for_루프 "wikilink"). 이를테면 다음과 같다.

``` c
for ( ; condition; ) {
   statements;
}
```

## 같이 보기

  - [do while 루프](https://ko.wikipedia.org/wiki/do_while_루프 "wikilink")
  - [for 루프](https://ko.wikipedia.org/wiki/for_루프 "wikilink")
  - [foreach 문](https://ko.wikipedia.org/wiki/foreach_문 "wikilink")

[분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink")