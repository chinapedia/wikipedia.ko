> This article is converted from Wikipedia: [C  ](https://ko.wikipedia.org/wiki/C__).


**C 프로그램 언어의 문법**은 소프트웨어 측면에서 다양하게 사용된다. C언어가 [유닉스](../Page/유닉스.md "wikilink")를 만들 때부터 사용하여 발전해 왔다. 그 동안 많은 발전을 거쳐 다양한 분야에서 사용한다.

전자공학에서 전자장치는 기본적으로 [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")를 사용하는데, 거의 모든 소프트웨어는 C 언어를 사용한다. 기계어를 일부 사용하지만 아주 일부분만을 코딩하여 C언어와 결합 한다. 임베디드 분야에서 역시 중요하다. 리눅스 커널이 C언어로 작성되어 있으므로 이것의 포팅에서 필수 요소이다.

#### [전처리기 매크로](../Page/매크로_\(컴퓨터_과학\).md "wikilink")

  - \#include

      -
        다른 프로그램 코드 파일을 선언 위치에 붙여 연결한다.

<!-- end list -->

  - \#define

      -
        특정 코드 영역을 재 정의 한다. 상수, 함수, 프로그램 블 등 다양한 정의를 할 수 있으나 주로 상수를 많이 사용한다.

<!-- end list -->

  - \#undef

      -
        정의 된 코드 영역을 해제 한다. 주로 정의된 상수를 많이 사용한다.

<!-- end list -->

  - \#if, \#elseif, \#else, \#endif

      -
        특정 코드 영역을 컴파일에 포함시킬 것인가를 조건 조사해서 결정한다.

<!-- end list -->

  - \#pragma

      -
        컴파일러에게 다양한 옵션을 지정하거나 설정 한다.

#### [자료형](../Page/자료형.md "wikilink") 관련

C/C++에서 취급하는 자료의 종류는 크게 정수형, 실수형으로 나누어 생각할 수 있다.

  - 정수형: 정수(char,int), 논리형 (bool), 문자형(char, wchar_t)

<!-- end list -->

  -

      -
        논리형은 bool이 추가 되었지만 C/C++ 에서 참과 거짓의 기준은 해당 연산결과가 0이냐 0이 아니냐로 구별 해 왔다. 그러나 프로그램에서 확실히 눈에 보이는 형태를 지원하기 bool이 추가 되었고, 상태는 true와 false 키워드가 추가 되었다. 문자 취급을 위해서는 기존의 [아스키](https://ko.wikipedia.org/wiki/아스키 "wikilink") 코드 만으로 충분했으므로 char만으로 충분 했지만 국제화 되면서 16비트를 많이 사용하므로 wchar_t가 추가 되었다.

<!-- end list -->

  - 실수형: 부동소수점 처리 방식으로 실수를 다룬다. float(32비트), double(64비트), long double(128비트)등이 있다.

<!-- end list -->

  -

      -
        실제로 CPU와 시스템에 따라 부동소수점을 지원하기 위한 하드웨어 연산 모듈이 없는 경우가 있다. 이렇게 되면 실수계산을 위한 함수를 사용하는 경우가 많다. 따라서 CPU와 컴파일러를 확인하고 경우에 따라 설정 해야 한다. 예를 들어 개인용 컴퓨터는 x86계열을 사용하기 때문에 [FPU](https://ko.wikipedia.org/wiki/FPU "wikilink")을 사용하면 된다. 그러나 ARM 등의 경우 FPU가 없는 것이 많다.

<!-- end list -->

  - [char](https://ko.wikipedia.org/wiki/char "wikilink"), [int](https://ko.wikipedia.org/wiki/int_\(C_프로그래밍_언어\) "wikilink")

      -
        정수형 변수를 선언 한다.

<!-- end list -->

  - [short](https://ko.wikipedia.org/wiki/short "wikilink"), [long](https://ko.wikipedia.org/wiki/long "wikilink")

      -
        정수형 변수의 데이터 저장 길이를 조절 한다.

<!-- end list -->

  - [unsigned](https://ko.wikipedia.org/wiki/unsigned "wikilink"), [signed](https://ko.wikipedia.org/wiki/signed "wikilink")

      -
        정수형 부호를 결정 한다.

<!-- end list -->

  - [float](https://ko.wikipedia.org/wiki/float "wikilink"){{·}}[double](https://ko.wikipedia.org/wiki/double "wikilink"){{·}}[long double](https://ko.wikipedia.org/wiki/long_double "wikilink")

      -
        실수형 변수를 선언 한다.

<!-- end list -->

  - [auto](https://ko.wikipedia.org/wiki/auto "wikilink")

      -
        변수의 초기값등을 고려하여 자료형을 자동 선언 한다.

<!-- end list -->

  - [struct](https://ko.wikipedia.org/wiki/struct "wikilink"){{·}}[union](https://ko.wikipedia.org/wiki/struct "wikilink"){{·}}[default](https://ko.wikipedia.org/wiki/struct "wikilink")

      -
        구조체 변수를 선언 한다.

<!-- end list -->

  - [bool](https://ko.wikipedia.org/wiki/bool "wikilink")

      -
        논리형 변수를 선언 한다. C99에서 추가 되었다.

<!-- end list -->

  - [wchar t](https://ko.wikipedia.org/wiki/wchar_t "wikilink")

      -
        [유니코드](../Page/유니코드.md "wikilink") 등의 변수를 선언 한다.

#### 함수 관련

  - [inline](https://ko.wikipedia.org/wiki/inline "wikilink"): 코딩은 함수 처럼 표현하지만 호출 부분에 코드가 추가된다. 일종의 블록 선언이다. 함수가 코드가 한번 존재하지만 이것은 호출 한 부분에 기계어 코드가 계속 복사된다.

<!-- end list -->

  - [return](https://ko.wikipedia.org/wiki/return "wikilink"): 함수를 빠져 나온다.

<!-- end list -->

  - [stdcall](https://ko.wikipedia.org/wiki/stdcall "wikilink"),[cdecl](https://ko.wikipedia.org/wiki/cdecl "wikilink"): 함수의 호출 방식을 지정 한다. 표준함수는 아니고 [마이크로소프트](../Page/마이크로소프트.md "wikilink")에서 지원한다.

#### 제어 분기 관련

  - [if](../Page/조건문.md "wikilink"), else: 조건에 따라 정해진 영역의 프로그램을 실행 한다.

<!-- end list -->

  - [goto](https://ko.wikipedia.org/wiki/GOTO_문 "wikilink"), *label*: 특정 프로그램 코드 위치로 무조건 점프 한다.

<!-- end list -->

  - [switch](../Page/Switch_문.md "wikilink"), [case](../Page/Switch_문.md "wikilink"): 특정 값에 따라 브랜치 점프 실행 한다.

#### [반복문](https://ko.wikipedia.org/wiki/반복문 "wikilink") 관련

  - [for](https://ko.wikipedia.org/wiki/for_루프 "wikilink"): 특정 조건이 완료 될 때까지 특정 영역을 반복 실행 한다.

<!-- end list -->

  - [while](https://ko.wikipedia.org/wiki/while_루프 "wikilink"): 특정 조건이 만족할 동안 특정 영역을 반복 실행 한다.

<!-- end list -->

  - [do\~while](https://ko.wikipedia.org/wiki/do-while_루프 "wikilink"): 먼저 특정 영역을 실행하고 조건이 맞으면 이를 반복 한다.

<!-- end list -->

  - [break](https://ko.wikipedia.org/wiki/break "wikilink"): 현재 실행하고 있는 블록을 종료하기 위해 블록을 빠져 나온다.

<!-- end list -->

  - [continue](https://ko.wikipedia.org/wiki/continue "wikilink"): 반복 실행문에서 현재부터 다음 블록을 실행하지 않고 블록의 초기로 이동 한다.

### 연산자

#### 종류와 기능

##### 산술 연산자

**`-`**     빼기

**`+`**     더하기

**`*`**     곱하기

**`/`**     나누기

**`%`**     나머지

**`--`**    1 감소

**`++`**    1 증가

**`-=x`**  x만큼 감소.

**`+=x`**  x만큼 증가.

**`*=x`**  x만큼 곱해짐.

**`/=x`**  x만큼 나뉨.

**`&=x`**  x와 비트곱.

**`^=x`**  x와 Exclusive OR 연산.

\++와 -- 연산자를 사용할 때, 언제 연산이 되는지 혼돈이 일어날 수 있다.

``` c
   char num;
   char rnum;

   num = 3;
   rnum = num++ + num + 5;
   printf("num=%d, rnum=%d\n", num, rnum);

   rnum = num + 5 + --num;
   printf("num=%d, rnum=%d\n", num, rnum);

   if (num++)
      rnum = num + 5;
   printf("num=%d, rnum=%d\n", num, rnum);
```

실행결과:

`num=4, rnum=11: 3+3+5=11   이후 num++=> 4`
`num=3, rnum=11: --num => 3 이후  3+5+2=10`
`num=4, rnum=9 : if 조건 처리후, num++=>4 이후  4+5=9`

##### 관계 연산자

**`>`**   보다 큼

**`>=`** 보다 크거나 같음

**`<`**  보다 작음

**`<=`** 보다 작거나 같음

**`!=`** 다름

**`==`** 같음

#### 우선순위

| 순위 | 연산자                            |
| -- | ------------------------------ |
| 1  | ( ) \[ \] −\> .                |
| 2  | \! \~ ++ –– (type) \* & sizeof |
| 3  | \* / %                         |
| 4  | \+ −                           |
| 5  | \<\< \>\>                      |
| 6  | \< \<= \> \>=                  |
| 7  | \== \!=                        |
| 8  | &                              |
| 9  | ^                              |
| 10 | |                              |
| 11 | &&                             |
| 12 | <nowiki>                       |
| 13 | ?:                             |
| 14 | \= += −=\*= /=                 |
| 15 | ,                              |

우선 순위는 이미 위와 같이 [C99](../Page/C99.md "wikilink") 국제표준으로 정해져 있다. 그러나 개발자가 암기하는 것은 불편하다. 너무 복잡하기 때문이다. 이를 해결하는 방법은 우선 순위가 높은 (,), \[, \]을 이용하여 지정하는 것이다.

``` c
   char chr;
   char idx = 0x5A;

   chr = 0x55;
   chr &= idx | char & 0xF1 | 0x33;
```

이렇게 코딩을 하면 &와 | 가 혼재 되어 의도한 데로 실행되지 않는 논리적 오류를 범할 수 있다.

``` c
   char chr;
   char idx = 0x5A;

   chr = 0x55;
   chr &= [idx | (char & 0xF1)] | 0x33;
```

우선 순위를 지정하면 개발자가 비교적 정확하게 표현할 수 있다.

### 전처리기 매크로

[매크로는](../Page/매크로_\(컴퓨터_과학\).md "wikilink") 컴퍼일러에게 코드의 특성을 알려주는 [키워드](https://ko.wikipedia.org/wiki/키워드 "wikilink")이다. 따라서 기계어로 컴파일 과정에서 필요한 요소이고, 매크로 자체가 기계어 코드로 생성 되지는 않지만 특정 코드를 제어하는데 사용한다.

## 자료형 (변수형)

### 정수형

#### char

#### int

### 실수형

실수를 처리하기 위해 float와 double을 사용한다. 실수를 2진수를 표현할 때는 [부동소수점](../Page/부동소수점.md "wikilink")(Float-Point) 방식을 사용한다. 이것은 국제표준 [IEEE 754](../Page/IEEE_754.md "wikilink") 규격에 따른다.

### struct

### [const](https://ko.wikipedia.org/wiki/const "wikilink")

``` c
#define I_PI 3
#define DPI 3.14159265

const int iPI = 3;
const double dPI = 3.14159265;

const int num; // error C2734: 'num': const 개체는 extern이 아닌 경우 초기화될 수 있습니다.
const int count = 100;
int const sz = 10;
int main(int argc, char **argv)
{
   while (sz)
      sz--;      // error C2105: '--'에 l-value가 필요합니다. - const 변수는 변경이 불가능
   while (count)
      count--;   // error C2105: '--'에 l-value가 필요합니다. - const 변수는 변경이 불가능
   return 0;
}
```

## [enum](https://ko.wikipedia.org/wiki/enum "wikilink")과 \#define

``` c
#define ST_NULL 0
#define ST_IN 1
#define ST_OUT 2

#define ERR_NULL ST_NULL
#define ERR_READ -1
#define ERR_WRITE -2
```

특정 의미가 있는 숫자나 문자를 개발자가 이해가 쉬운 형태로 바꾸는 것이 **define** 이다. 그러나 개발 단계에서 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink")([debug](https://ko.wikipedia.org/wiki/debug "wikilink")) 과정에서 위의 정의 된 문자는 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink") 테이블에서 제거되어 디버깅 단계에서 값이 어떤 값인지 알수가 없다. 정의 된 내용이 코드에 나오면, 바로 앞의 내용을 뒤에 정의 된 내용으로 바꾸어 치기 때문이다. 결국 컴파일 과정에서 기계어 코드에 이진수값을 넣는 방법으로 단순 대체 하는 것이다.

``` c
enum {
   ST_NULL = 0,
   ST_IN,
   ST_OUT,

   ERR_NULL = ST_NULL,
   ERR_READ = -1,
   ERR_WRITE = -2
};
```

**enum**은 define과 기능적으로 비슷 하지만 디버깅 단계에서 값을 확인 할 수 있다. 예를 들어 ERR_READ가 어떤 숫자 인지를 알 수 있다. 이것을 개발툴이 지원하려면 각 코드의 내용 중, 디버깅에 필요한 테이블에 등록하여 값 들을 저장하고 표시하는 것이다.

## 포인터

## 조건 판단

프로그램에서 조건은 여러가지 곳에서 사용한다. 조건문, 루프 등에서 조건을 판단한다. 조건은 최종적으로 참(true)과 거짓(false)로 결정한다.

조건의 사용 예 :

``` cpp
  int val;
  //...

  if (val)
    // ...
  if (val && val >= 100)
    // ...
  while (val)
    // ...
```

그런데 조건은 참과 거짓 등으로 하나의 비트만 있으면 구별해서 표현할 수 있다. 그러나 C언어는 정수형에서 여러비트의 숫자가 존재하고 이것의 조건 판단도 가능하다.

조건 판단 기준 :

  - 참: 조건 값이 0이 아닐 때
  - 거짓: 조건이 0일 때

로 정의 한다.

``` cpp
  int val = 10;
  if (val)  // val가 10 이므로 참
     val++;
  if (val && val >= 100) // val값이 11이므로 val는 참, 11 >= 100이므로 거짓. 참 && 거짓 하면 거짓
     val = 1;
  while (-1)   // -1이 참이므로 무한 루프
  {
     if (val < 0)
        break;
     // ...
  }
```


\== 블록 == 블록은 프로그램 코드 중, 특정 영역을 지정하는데 사용한다.

  - 함수는 기본적으로 블록을 포함 한다.
  - 조건문에서 조건에 따라 코드가 여러 ';'가 존재할 때 만든다.
  - 임의의 블록을 만든다.

### 함수에서 블록

함수는 블록에 의해 함수의 코드 시작과 끝이 결정 된다. 따라서 함수의 시작을 위한 블록 '{'으로 시작하면, '}'으로 닫아야 한다.

블록의 예 :

``` cpp
#include <stdlib.h>
#include <stdio.h>

int gResNum;

int add(int a, int b)
{
   return a+b;
}

int main(int argc, char *argv[], char**env)
{ // 함수의 코드를 시작 한다.
   int sum; // 이 지역 변수는 함수 블록이 끝나면 없어진다.
   int num;

   if (argc < 2)
   { // 조건문에서 다음 개의 함수를 실행 한다. 2개의 함수 이므로 블록이 필요하다.
      printf("숫자 입력 : "); scanf("%d", &num);
   }
   else
      num = atoi(argv[1]);

   {   // 임의로 블록을 만든다.
      int sum = 0;  // 블록 내에서 선언 된 변수는 지역변수(자동변수)로 이 블록이 끝나면 없어진다.
      for (int cnt = 0;cnt < num;cnt++)
      {
           sum += cnt;
      }
      printf("1 ~ %d 합 = %d\n", num, sum);
      gResNum = sum;
   }  // 임의의 블록 끝.
   sum = add(num, 100);
   printf("%d에 100을 더하면 %d.\n", num, sum);
   return 0;
}
```

## 흐름 제어

프로그램 코드의 실행은 나열된 순서로 진행 한다. 조건에 따라 실행 위치를 결정하기 조건적 실행 코드를 만들 수 있다.

### 조건 실행: if \~ else

``` cpp
 if (조건)
   // 조건이 참일 때 실행
 else
    // 조건이 거짓일 때 실행
```

### void 변수

### 포인터 함수

## 정적 변수와 동적 변수 할당

### 동적 변수 할당

## 함수

### 함수의 호출 방식

#### __stdcall __cdecl

### inline

### static 함수

### 루프 실행

#### for

#### while

#### do \~ while

#### switch

## 외부 링크

  - Ritchie, Dennis M. [The Development of the C Language](http://plan9.bell-labs.com/who/dmr/chist.html). History of Programming Languages-II. Second History of Programming Languages conference, Cambridge, Massachusetts, April, 1993. .

  - [Richard M. Stallman](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink"): *[Using and Porting the GNU Compiler Collection](http://gcc.gnu.org/onlinedocs/gcc-2.95.3/gcc.html)*, [Free Software Foundation](../Page/자유_소프트웨어_재단.md "wikilink"),

  - Richard M. Stallman: *[Using Gcc: The Gnu Compiler Collection Reference](http://gcc.gnu.org/onlinedocs/gcc-3.3.1/gcc/)*, Free Software Foundation,

  - [Brian J. Gough](https://ko.wikipedia.org/wiki/Brian_J._Gough "wikilink"): *[An Introduction to GCC](https://archive.is/20121205072412/http://www.network-theory.co.uk/gcc/intro/)*, Network Theory Ltd.,

[분류:소스 코드](https://ko.wikipedia.org/wiki/분류:소스_코드 "wikilink") [분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink")