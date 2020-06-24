> This article is converted from Wikipedia: [F 샤프](https://ko.wikipedia.org/wiki/F_샤프).


**F\#**(에프 샤프)는 강타입 함수형 우선 다중패러다임 언어이다. 주로 [공통 언어 기반](../Page/공통_언어_기반.md "wikilink") 크로스 플랫폼으로 사용되며, [자바스크립트](../Page/자바스크립트.md "wikilink")\[1\]나 GPU 코드\[2\] 생성에도 사용할 수 있다.

F\# 소프트웨어 재단\[3\]이나 [마이크로소프트](../Page/마이크로소프트.md "wikilink"), 오픈소스 기여자에 의해 개발된다. F\# 소프트웨어 재단에서 만든 오픈소스 크로스 플랫폼 컴파일러가 있다.\[4\] [비주얼 스튜디오](../Page/마이크로소프트_비주얼_스튜디오.md "wikilink")\[5\]나 [자마린](../Page/자마린.md "wikilink") 스튜디오\[6\]에서도 지원한다. 다른 프로그램으로는 [Mono](https://ko.wikipedia.org/wiki/모노 "wikilink"), [MonoDevelop](../Page/MonoDevelop.md "wikilink"), SharpDevelop, MBrace, WebShaper 등이 있다. 테스트 에디터에서도 플러그인 형식으로 지원하며, 특히 Atom, VSCode, Vim, Emacs, Rider 등에서 지원한다.

F\#은 ML 계열의 언어이며, [닷넷 프레임워크의](../Page/닷넷_프레임워크.md "wikilink") [OCaml](../Page/OCaml.md "wikilink") 구현체로 시작했고,\[7\]\[8\] [C\#](../Page/C_샤프.md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"), [하스켈](../Page/하스켈.md "wikilink"), [스칼라](../Page/스칼라_\(프로그래밍_언어\).md "wikilink"), [얼랭](../Page/얼랭.md "wikilink")에서 영향을 받았다.

## 문법

### F\# 함수의 형태

함수형 프로그래밍의 "Hello World"라고 할 만한 것은 [팩토리얼을](../Page/계승.md "wikilink") 계산하는 코드이다. F\# 으로는 다음과 같이 표현할 수 있다.

``` fsharp
let rec fact n =
    match n with
    | 0 -> 1
    | _ -> n * fact (n-1);;
```

이 코드는 팩토리얼을 재귀 함수로 정의한 것이다. 일반적으로 함수를 정의할 때는 let ... 와 같이 쓰고, 재귀함수를 정의할 때는 let rec ... 와 같이 명시한다. 함수의 마지막에는 두 개의 세미콜론으로 끝마침을 해 준다.

위 함수 정의는 수학 교과서에서 볼 수 있는 팩토리얼의 정의와 비슷하다. F\# 코드는 문법과 계산방식의 측면에서 수학적 언어와 닮았다.

F\# 은 자동으로 타입을 유추한다. 위의 fact 함수는 (int -\> int) 타입 즉, 정수를 인자로 받아 또 다른 정수를 반환하는 함수이다.

두 번째 줄에서 F\#의 또 다른 중요한 특성인 패턴 매칭을 볼 수 있다. 패턴 매칭은 match ... with ... 와 같이 표현한다. 함수 fact 는 인자가 0 이면 1 을 반환하고, 아니면 두 번째 케이스를 실행하여 0에 도달할 때까지 fact 을 재귀적으로 계속 호출한다. 패턴 매칭에서 underbar('_')는 디폴트 케이스를 의미한다.

계산과정을 살펴보면 위 함수가 어떻게 수행이 되고, [팩토리얼이](../Page/계승.md "wikilink") 계산되는지 알 수 있다.

`fact 4`
` => 4 * fact 3`
` => 4 * (3 * fact 2)`
` => 4 * (3 * (2 * fact 1))`
` => 4 * (3 * (2 * (1 * fact 0)))`
` => 4 * (3 * (2 * (1 * 1)))`
` ...`
` => 24`

F\# 은 [OCaml](../Page/OCaml.md "wikilink") 을 계승한 언어여서, 위에서 설명한 부분은 [OCaml](../Page/OCaml.md "wikilink") 언어에도 그대로 적용된다.

### 개선된 팩토리얼 함수

팩토리얼 함수는 지수함수 보다도 훨씬 빨리 커지기 때문에 큰 정수의 계산도 가능해야 하고, 재귀호출 함수의 성능도 고려해야 한다. 큰 정수의 곱셈 계산을 위해 팩토리얼 값은 bigint 타입을 이용하고 그 대신 factiorial 함수의 인자는 int 타입으로 하여 재작성해 보았다. bigint 타입을 표현하는 리터럴은 int 타입을 표현하는 리터럴의 끝에 문자 I만 붙이면 된다. 즉 4는 int 타입이지만 4I는 bigint 타입이다. 또 int 타입을 bigint 타입으로의 타입변환은 정수값이 되는 표현식의 좌측에 bigint 만 붙이면 된다. 즉, bigint expression1 하면 expression1 의 값을 bigint 타입으로 변환하는 식이다. 아래의 소스에서는 함수의 인자(매개변수)로 전달된 int 타입의 값 x를 bigint 타입으로 변환하기 위해 bigint x 라는 타입 변환식을 사용하였다. 아래의 factorial 함수는 (int -\> bigint) 타입의 함수이다.

``` fsharp
 #light

 let factorial n =
     let rec fac a x =
         match x with
         | k when k < 1 -> 1I
         | k when k = 1 -> a
         | v -> fac (a*(bigint x)) (x-1)
     fac 1I n

 let b = 50
 let z = factorial b
 printfn "%O! = %O" b z
```

C 언어, Java 언어에서는 함수 안에서 함수를 또 정의하지 못하지만 F\# 언어는 Python 언어, Lua 언어 처럼 함수 안에서 함수를 또 정의할 수 있다. 위의 소스는 factorial 함수 안에서 재귀호출 함수 fac 을 정의하는 중첩 구조(nested structure)로 되어 있다.

위의 소스 코드의 실행 결과는

`50! = 30414093201713378043612608166064768844377641568960512000000000000`

이다.

저 소스에서 재귀호출 함수 fac에 전달되는 첫번 째 인자 a는 상태로 이해하면 된다. 여기서 상태는 재귀 호출 과정에서 계산된 전 단계의 팩토리얼 값으로 이용되고 있다. 4\! 을 계산하는 저 소스의 계산과정을 추적하면

` fac 1I 4`
` => fac (4I) 3`
` => fac (12I) 2`
` => fac (24I) 1`
` => 24I`

이다.

저 소스는 5000\! 을 계산할 때도 stack overflow 를 걱정하지 않아도 된다. 이것이 F\# 언어의 한 특징이다. 보통의 명령형 언어(Python 언어)와 달리 패턴 매칭(match)에 의한 재귀호출은 상태에 의한 호출이기 때문이다. 저 소스에서 쓰인 재귀호출을 보통은 꼬리재귀호출이라고 한다.

## 같이 보기

  - [피보나치 수 프로그램](https://ko.wikipedia.org/wiki/피보나치_수_프로그램 "wikilink")

## 각주

## 외부 링크

  - F\# 소프트웨어 재단

  - [마이크로소프트 리서치의 F\# 사이트](http://research.microsoft.com/en-us/um/cambridge/projects/fsharp/default.aspx)

      - \[<http://msdn.microsoft.com/library/dd233154(VS.100>).aspx F\# 매뉴얼\]

  - [F Sharp & F\# .Net](http://www.fsharp.net)

[분류:닷넷 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:닷넷_프로그래밍_언어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink") [분류:2002년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:2002년_개발된_프로그래밍_언어 "wikilink") [분류:마이크로소프트 리서치](https://ko.wikipedia.org/wiki/분류:마이크로소프트_리서치 "wikilink") [분류:ML 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:ML_프로그래밍_언어_계열 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.