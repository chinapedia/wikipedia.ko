> This article is converted from Wikipedia: [ML \( \)](https://ko.wikipedia.org/wiki/ML_\(_\)).


**ML**은 범용 [프로그래밍 언어의](../Page/프로그래밍_언어.md "wikilink") 일종이다. 프로그래밍 언어 분야의 핵심 연구 성과들을 잘 반영하면서도 실용적인 언어로 알려져 있다. 특히, 안전한 [타입 시스템을](https://ko.wikipedia.org/wiki/타입_시스템 "wikilink") 갖추고 있어 프로그램을 실행하는 중에 나올 수 있는 타입 에러를 실행하기 전에 미리 모두 찾아준다. 힌들리-밀너(Hindley-Milner) 타입 추론 시스템을 구현하여 [자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") 같은 길고 불편한 [자료형](../Page/자료형.md "wikilink")(타입) 표기 없이도 변수들의 자료형을 추론할 수 있다.

ML은 [하스켈](../Page/하스켈.md "wikilink")과 같은 순수한 함수형 언어와 같이 함수가 자유롭게 사용될 수 있으면서도, 메모리 상태를 변화시키는 함수를 허용하는 [함수형 프로그래밍 언어의](../Page/함수형_프로그래밍.md "wikilink") 모습도 갖추고 있다. 이 때문에 함수형 언어이면서 순수하지 않은 함수형 언어로 분류한다.

그밖에 ML에는 이런 특징이 있다.

  - [메모리 재활용](https://ko.wikipedia.org/wiki/메모리_재활용 "wikilink")(garbage collection)을 통해서 자동으로 메모리를 관리한다.
  - 함수의 [다형성](https://ko.wikipedia.org/wiki/다형성 "wikilink")(polymorphic functions)을 지원하여 타입과 상관 없이 실행할 수 있는 함수를 정의할 수 있다.
  - [대수적 자료형](https://ko.wikipedia.org/wiki/대수적_자료형 "wikilink")(algebraic data type)을 지원하여 상위에서 자료구조를 표현할 수 있다.
  - 값들의 패턴 매칭을 통해 간편하게 조건문을 만들 수 있다.
  - 간단하고 강력한 예외 시스템으로 프로그램의 실행흐름을 편리하게 기획할 수 있다.

ML 프로그래밍 시스템은 다양한 종류가 있다. [SML](https://ko.wikipedia.org/wiki/SML_프로그래밍_언어 "wikilink")(Standard ML)과 [Caml이](https://ko.wikipedia.org/wiki/Caml_프로그래밍_언어 "wikilink") 가장 널리 알려진 것이며, [F\#](../Page/F_샤프.md "wikilink") 등 다른 언어들도 존재한다. [한국](../Page/한국.md "wikilink")에서 개발된 ML 프로그래밍 시스템으로는 [KAIST에서](../Page/한국과학기술원.md "wikilink") 개발하였고 현재는 [서울대에서](https://ko.wikipedia.org/wiki/서울대학교 "wikilink") 확장·관리하고 있는 [nML](https://ko.wikipedia.org/wiki/nML "wikilink")이 있다.

ML의 기본 아이디어는 [C\#](../Page/C_샤프.md "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [하스켈](../Page/하스켈.md "wikilink"), [사이클론](https://ko.wikipedia.org/wiki/사이클론_프로그래밍_언어 "wikilink"), [네멜레](https://ko.wikipedia.org/wiki/네멜레_프로그래밍_언어 "wikilink") 등 많은 언어에 영향을 미쳤다.

ML은 주로 프로그래밍 언어의 실행기(interpreter)나 번역기(compiler), 프로그램 분석기 등을 개발하고 다루는 데 사용하지만, ML은 본래 범용 프로그래밍 언어이므로 [생물정보학](../Page/생물정보학.md "wikilink"), 금융 전산망, P2P 클라이언트/서버 프로그램 등의 개발에도 사용한다.

## 예제

### ML 함수의 형태

함수형 프로그래밍의 [Hello world라고](https://ko.wikipedia.org/wiki/Hello_world_프로그램 "wikilink") 할 만한 것은 [팩토리얼을](../Page/계승.md "wikilink") 계산하는 코드이다. 순수 ML로는 다음과 같이 표현할 수 있다.

`fun fac : (fn: int -> int) 0 = 1`
` | fac n = n * fac (n-1);`

이 코드는 팩토리얼을 기본적인 경우(base case)가 하나 있는 [재귀 함수로](https://ko.wikipedia.org/wiki/재귀_함수 "wikilink") 정의한 것이다. 수학 교과서에서 볼 수 있는 팩토리얼의 정의와 비슷하다. ML 코드는 문법과 계산방식의 측면에서 수학적 언어와 닮았다.

팩토리얼 함수의 첫 번째 줄은 이 함수의 [자료형](../Page/자료형.md "wikilink")을 표시하는 부분이다. ML은 코드로부터 자동으로 변수와 함수의 자료형을 추론하므로 이 부분은 없어도 무방하다. 첫 번째 줄은 "*함수 fac* (fac)*의 자료형은* (:) *정수에서 정수로 가는* (fn: int -\> int) *함수이다.*" 와 같이 해석할 수 있다. 따라서 이 함수는 정수를 인자로 받아 또 다른 정수를 반환하는 함수이다.

자료형을 명시하는 부분을 제거하면 코드는 다음과 같이 간단해진다.

`fun fac 0 = 1`
` |  fac n = n * fac(n-1);`

함수의 인자가 괄호로 둘러싸여 있지 않고 공백으로 구분되어 있음을 주목하라. 두 번째 줄은 ML의 또다른 중요한 특성인 패턴 매칭으로 이루어져 있다. 함수 fac은 인자가 0이면 1을 반환한다. 나머지 모든 경우에 대해서는 두 번째 줄을 실행하여 0에 도달할 때까지 fac을 재귀적으로 계속 호출한다.

## 외부 링크

  - [여러 언어들 사이의 속도 비교](https://web.archive.org/web/20121231010227/http://benchmarksgame.alioth.debian.org/)
  - [Standard ML의 유명한 버전인 Moscow ML](https://web.archive.org/web/20120225230022/http://www.dina.kvl.dk/~sestoft/mosml.html)
  - [마이크로소프트의 .NET 프레임워크를 이용한 ML언어인 F\#](http://research.microsoft.com/projects/ilx/fsharp.aspx)

[분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink") [분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:1973년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1973년_개발된_프로그래밍_언어 "wikilink") [분류:ML 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:ML_프로그래밍_언어_계열 "wikilink")