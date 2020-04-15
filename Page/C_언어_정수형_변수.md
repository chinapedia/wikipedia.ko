> This article is converted from Wikipedia: [C 언어 정수형 변수](https://ko.wikipedia.org/wiki/C_언어_정수형_변수).


[C/C++에서](https://ko.wikipedia.org/wiki/C와_C++에서의_연산자 "wikilink") **정수형 변수**는 [정수](../Page/정수.md "wikilink")를 처리하기 위한 변수이다. 정수형 변수를 [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")가 처리할 때, 부호와 숫자범위를 결정해야 한다. C/C++로 작성 된 코드는 결국 해당 마이크로프로세서의 기계어 코드로 변환하는데, 마이크로프로세서의 숫자체계(ALU 등 이용)를 사용하기 때문이다.

숫자 범위는 2진수의 몇비트로 처리할 것인가를 결정 해야 한다. 이것은 곧 정수 처리 범위를 결정된다. 마이크로프로세서 내에서 레지스터와 ALU의 비트수가 결정 되었기 때문이다. 숫자 범위는 char, int, short, long을 사용해 변수선언을 하면 된다. 부호는 unsigned을 이용한다. 음수와 양수를 표현하기 위해서는 signed과 unsigned를 사용한다. 음수를 사용할 경우 보통 signed를 생략 한다. int나 char 만을 선언하면 양수와 음수를 같이 사용한다. 양수 만을 사용하려면 unsigned 붙이면 된다.

CPU에서 음수는 2진수 체계중에 논리 공학의 *2의보수*를 사용한다. unsigned를 사용할 경우는 정해진 비트 수 내에서 이진수와 같다. 그러나 음수를 사용할 경우, 양수와 음수는 2의 보수 체계를 사용하여 숫자를 배치 한다. 이것은 연산자로 코딩 될 때 수월하게 숫자를 표현하거나 계산할 수 있기 때문이다.

정수 연산은 CPU 내의 ALU에서 처리 한다. 4칙연산, 논리연산, 비트 쉬프트 등의 연산이 가능하다. 많은 CPU의 경우 [부동소수점](../Page/부동소수점.md "wikilink") 연산(FPU) 모듈이 없지만, 정수형 연산은 모든 CPU가 가능하다. 정수는 정수형 ALU을 사용하여 연산한다. 경우에 따라 저속의 8비트 CPU는 나누기 기계어 코드가 없지만, 현재의 CPU 들은 거의 모두 4칙연산을 할 수 있다. 보통의 CPU ALU는 정수형의 나누기의 연산 시, 나누기 기계어 코드가 실행되고 몫과 나머지로 분리하여 레지스터에 저장함으로써 결과를 얻는다.

## 정수형 변수의 종류와 숫자 처리 능력

### 비트별 종류

  - char : 8비트(1바이트)의 정수형 선언 한다.
  - int : 16/32/64비트로 정수형 선언

int의 경우, 대부분의 8비트 CPU는 16비트를 사용한다. 32비트의 CPU의 경우 32비트를 그리고 64비트의 경우 64비트를 사용한다. 따라서 이것은 어떤 [OS](https://ko.wikipedia.org/wiki/OS "wikilink")냐와 컴파일러가 어떤 비트까지 가능한 가에 따라 결정된다. 따라서 이 int 형의 경우 길이를 측정할 때는 sizeof 연산자를 사용하는 것이 좋다.

``` c
  int val;
   printf("val 길이는 %d\n", sizeof(val) );

  int data[] = { 23,32,3,4,3,43 };
  #define SZ_DATA sizeof(data)/sizeof(data[0])
  for (int cnt = 0;cnt < SZ_DATA;cnt++)
  // ...
```

**int와 결합한 비트 결정**

  - short : int 정수형에서 더 적은 비트수를 선언 한다.
  - long : int 정수형에서 더 많은 비트수를 선언 한다.

### 부호 종류

  - [signed](https://ko.wikipedia.org/wiki/signed와_unsigned "wikilink") : 양수와 음수를 사용한다. 보통 생략한다.
  - [unsigned](https://ko.wikipedia.org/wiki/signed와_unsigned "wikilink") : 양수 만을 사용한다.

unsigned와 signed가 모두다 없으면 signed로 결정된다. 따라서 부호없이 선언하려면 unsigned를 사용해야 한다.

## char

**8비트** 단위로 처리는 되는 정수형 변수이다. int가 CPU 마다 비트수가 다른데 비해, 이 변수는 8비트로 규정 되어 있다. 부호는 unsigned을 이용하여 부호가 없는 변수임을 지정 한다. 부호가 있는 변수는 signed을 사용할 수도 있지만 이것은 생략도 가능하다. 따라서 보통 습관적으로 signed을 사용하지 않는다. char 처리는 ALU을 이용하여 8비트 연산을 한다. 부호에 따라 정수 연산 기계어 코드가 달라지고, 이 기계어 코드가 실행될 때 ALU에 부호 지정과 연산 단위 비트수를 지정하면 연산이 진행된다.

## int

char가 8비트 처리 단위라면 [int](https://ko.wikipedia.org/wiki/int "wikilink")은 CPU마다 처리 단위가 다르다. 보통 8비트 CPU([Z-80](https://ko.wikipedia.org/wiki/Z-80 "wikilink"), [8051](https://ko.wikipedia.org/wiki/8051 "wikilink"),[AVR](https://ko.wikipedia.org/wiki/AVR "wikilink")) 등은 16비트가 지정된다. 따라서 컴파일러 사용 시, int 변수값의 범위가 어떻게 되는지 확인 해야 오류를 줄일 수 있다. 32비트 CPU(x86, 68000계열, ARM) 등은 32비트로 지정된다.

컴퓨터 운용시스템과 개발도구인 컴파일러에 따라 int가 32비트인지 64비트인지를 다를 수 있으므로 확인해야 하는 경우도 있다.

다른 비트수로 변경하려면 short와 long을 사용하여 변경할 수 있다.

  - 8비트 CPU의 일반적 형태

<!-- end list -->

``` c
char val8;     // 8비트 정수형
int ival;      // 16비트 일반적
long int ival; // 32비트 변수
```

대부분의 8비트 CPU의 컴파일러는 int가 16비트이므로 short가 필요없는 경우가 많다.

  - 32비트 CPU의 일반적 형태

<!-- end list -->

``` c
short int sval;    // 16비트 변수
int   ival;        // 32비트 변수
long  int  lval;   // 일반적으로 32비트 변수
                   // 보통 32비트로 int와 같은 경우가 많으므로 컴파일러마다 32비트 인지 확인이 필요하다.
long long int llval;// 64비트 변수
                   // 64비트는 컴파일러에 따라 제공하지 않는 경우가 있으므로 주의가 필요하다.
                   // 비주얼 스튜디오 6.0버전은 인식이 되지 않는다.
```

보통 short이나 long을 쓸 경우 int 생략이 가능하다.

## 같이 보기

  - [char](https://ko.wikipedia.org/wiki/char "wikilink")
  - [long](https://ko.wikipedia.org/wiki/long "wikilink")
  - [unsigned](https://ko.wikipedia.org/wiki/unsigned "wikilink")
  - [const](https://ko.wikipedia.org/wiki/const "wikilink")

## 외부 링크

  - [Richard M. Stallman](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink"): *[Using and Porting the GNU Compiler Collection](http://gcc.gnu.org/onlinedocs/gcc-2.95.3/gcc.html)*, [Free Software Foundation](../Page/자유_소프트웨어_재단.md "wikilink"),

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink")