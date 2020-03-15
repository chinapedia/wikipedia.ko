> This article is converted from Wikipedia: [C   ](https://ko.wikipedia.org/wiki/C___).


[C](../Page/C_언어의_문법.md "wikilink")/[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서 실수형은 실수를 처리하기 위해 사용한다. 실수를 2진수를 표현할 때 [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink")(Float-Point) 방식과 [고정 소수점](https://ko.wikipedia.org/wiki/고정_소수점 "wikilink") 방식이 있는데, C/C++에서는 부동소수점 방식을 사용한다. 이것은 국제표준 [IEEE 754](https://ko.wikipedia.org/wiki/IEEE_754 "wikilink") 규격에 따른다. [float](https://ko.wikipedia.org/wiki/float "wikilink")와 [double](https://ko.wikipedia.org/wiki/double "wikilink")을 사용하여 변수 선언을 한다. 이것은 CPU의 구조와 상관이 없이 국제 표준에 의한 규정에 따른 변수이므로 int처럼 변수 길이(비트 수)가 변하지 않는다.

보통 [마이크로프로세서](https://ko.wikipedia.org/wiki/마이크로프로세서 "wikilink")(CPU)는 정수형 ALU을 사용한다. 그러나 실수형 처리를 위한 [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink") 처리 모듈은 많은 CPU에 존재하지 않는다. 이렇게 실수형 ALU가 없다면 실수형 처리 함수를 사용한다. 정수형과 실수형 연산 모듈이 같은 CPU 안에 따로 존재하기도 한다. 이렇게 따로 존재한다면 각각의 기계어 코드를 나누어, C/C++가 각각의 기계어를 사용하도록 컴파일한다. 고성능의 CPU 경우 별도의 FPU 연산 모듈로 구성하는 것이 일반적이다. 인텔의 x86 계열은 80386의 경우 80387이라는 칩이 별도로 구성하였다. 다른 칩이므로 컴퓨터 설계과정에서 [PCB](https://ko.wikipedia.org/wiki/PCB "wikilink") 상에서 결합되어 있었다. 80486에서 이 두 칩이 하나의 칩으로 합쳐졌다. 결국 80486은 정수형 ALU와 [FPU](https://ko.wikipedia.org/wiki/FPU "wikilink")(Floating-point unit)가 한 칩 내에 만들어져 있다. 실수형 변수는 FPU을 이용하여 연산할 수 있다.

프로그램 개발도구에 따라 FPU가 존재하는 CPU라도 FPU을 사용하지 않고 정수형 계산 함수를 사용할 수 있도록 컴파일 옵션을 설정할 수 있다. FPU가 없는 CPU라면 함수로 실수 계산을 할 수밖에 없다. 정수형 ALU을 사용하여 계산하는 것이기 때문에 속도에 부담이 될 수도 있다. 실수형의 각 부분을 나누어 복잡한 정수계산을 통해 실행되도록 함수를 구성한다. 보통 8비트 CPU는 거의 FPU가 없기 때문에 대부분 함수를 사용한 실수 연산을 한다. 동시에 컴파일러가 어디까지 실수형을 지원하는지 확인해야 한다. 보통 float만을 지원하는 컴파일러가 많다.

## float와 double의 규정

C 언어에서 실수를 처리하기 위해 [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink")(Float-Point) 방식을 사용한다. 이것은 국제표준 [IEEE 754](https://ko.wikipedia.org/wiki/IEEE_754 "wikilink") 규격에 따른다.

  - float : 단정밀도(single precision) 32비트
  - double : 배정밀도(double precision) 64비트

기타 부동소수점은 고정밀도의 표현도 있지만 C언어에서는 위의 2가지 변수형을 사용한다.

### 숫자 표현

실수형은 숫자와 점 그리고 지수로 표현한다.

  - 3.141592, 3.141592f
    3.1E-3

float 형은 숫자 끝에 f을 붙여 32비트 단정밀도에 따른 숫자임을 나타낸다. 통상 f 없이 사용하면 double형 숫자이다.

## 실수형 변수의 유효자릿수

``` c
float frnum = 3.141593f;
double drnum = 3.141592653589793;
```

여기서 유효 자리 개수를 생각할 때, float는 7자리의 유횻값을 갖는다. double은 16개의 자리의 숫자를 저장할 수 있다.

``` c
float frnum = 3.141592653589793f;
```

이렇게 프로그램을 하면 컴파일러는 7개의 숫자를 처리하고 나머지는 버린다. 이때 컴파일러는 경고(warning)로 알려 준다. 단정밀도의 가수부 23비트가 가질 수 있는 범위가 제한되기 때문이다. 큰 수는 지수부를 이용하여 값을 지정한다.

## 같이 보기

  - [float](https://ko.wikipedia.org/wiki/float "wikilink")
  - [double](https://ko.wikipedia.org/wiki/double "wikilink")
  - [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink")([FPU](https://ko.wikipedia.org/wiki/FPU "wikilink"))

## 외부 링크

  - [Richard M. Stallman](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink"): *[Using and Porting the GNU Compiler Collection](http://gcc.gnu.org/onlinedocs/gcc-2.95.3/gcc.html)*, [Free Software Foundation](https://ko.wikipedia.org/wiki/자유_소프트웨어_재단 "wikilink"),

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink")