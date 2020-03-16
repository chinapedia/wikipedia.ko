> This article is converted from Wikipedia: [Char](https://ko.wikipedia.org/wiki/Char).


[C](https://ko.wikipedia.org/wiki/C_언어 "wikilink") 및 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 프로그래밍 언어에서의 **char**는 8비트 정수형 처리 변수로 **character**(문자)의 약자이다. C언어 정수형의 처리에서 부호가 있는 sign형과 부호가 없는 unsigned형으로 선언하여 사용할 수 있다. 부호가 있는 변수는 char 만으로 선언된 변수이고, 부호가 없는 경우는 unsigned과 결합하여 선언 한다. 부호가 있는 정수형은 2의 보수 체계를 사용하여 +와 -로 나누어 숫자를 표현할 수 있다. char는 8비트 변수 이므로 부호형 변수는 -128\~127까지의 숫자를 취급할 수 있다. [CPU가](../Page/중앙_처리_장치.md "wikilink") 해당변수를 처리할 때는 해당 변수의 메모리 위치의 숫자를 CPU의 레지스터로 가져와 [ALU를](../Page/산술_논리_장치.md "wikilink") 통해 계산할 수도 있다. 계산 결과는 레지스터로 저장되고 다음 프로그램 코드에 따라 사용 된다. 모든 CPU는 8비트 단위의 처리가 가능하므로 CPU의 레지스터 및 ALU을 통해 한번의 계산에 의해 이루어진다. 계산의 종류는 4칙연산 뿐아니라 [논리연산](https://ko.wikipedia.org/wiki/논리연산 "wikilink"), 비트 쉬프트 등 다양한 연산을 ALU을 통해 이루어진다. 원래 char는 문자형 값을 처리하기 위한 변수 인데, character의 약자이다. 글자에서의 의미로 보면 [아스키](https://ko.wikipedia.org/wiki/아스키 "wikilink")([ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink"))의 문자형을 취급하여 계산하거나 처리 한다. 아스키 코드 값은 기본적으로 8비트 이므로 이것은 8비트 정수형의 부분집합일 뿐이다. 따라서 문자 만이 아니라 8비트 정수형 연산도 가능하다. 예를 들어 'A'를 'a'로 바꾸려면 정수형 연산으로 가능하다. 이때 역시 ALU을 통한 정수형 연산이 기계어 코드에 의해 계산 된다. 그러나 한글의 경우 보통 16비트([KS X 1001](../Page/KS_X_1001.md "wikilink") 또는 [유니코드](../Page/유니코드.md "wikilink")) 이므로 char의 배열형이 필요하다. 따라서 한글은 char 변수만으로는 불가능하고 char 배열형으로 선언해야 한다. 또한 char 변수는 문자 뿐만 아니라 8비트의 정수형 변수의 연산이 가능하므로 문자 뿐만 아니라 일반적인 데이터를 처리 할 수 있다. 예를 들어 온도를 저장하기 위한 변수를 생각할 때, -128도 부터 127도 까지 처리 한다면 char 변수를 사용할 수 있다.

## 선언

문자를 취급할 때 ASCII 코드는 8비트이므로 char 변수에 의해 저장할 수 있다. 문자열이 모인 [스트링](https://ko.wikipedia.org/wiki/스트링 "wikilink")(string)은 char의 배열형을 사용하면 된다.

``` c
   char chr;
   chr = '2';

   char ch = 'A';
```

한글의 처리에서 [KS X 1001](../Page/KS_X_1001.md "wikilink")(구 [KS C 5601](https://ko.wikipedia.org/wiki/KS_C_5601 "wikilink"))와 [유니코드](../Page/유니코드.md "wikilink") 등의 코드는 16비트 이므로 char 변수에는 값을 치환할 수 없다.

``` c
   char name = '홍'; // compile error
```

이와 같은 경우 컴파일러에 의해 오류(error)를 발생하여 실행 파일을 만들 수 없다. 이런 경우 한글 한글자라도 다음과 같은 배열형을 사용해야 한다.

``` c
   char chan[] = "홍";
```

이렇게 되면 한글 한글자 '홍'이 2바이트이고 스트링의 마지막을 알리는 0을 넣어 3바이트 이상의 배열이 필요 하다.

정수형 처리를 할 때는 숫자를 치환하거나 계산을 할 수 있다. 또한 정수형은 부호가 있는 경우와 없는 경우가 있으므로 unsigned와 결합하여 사용하면 된다.

``` c
   char cnum;
   cnum = 10;

   unsigned char unum = 255;
   unum -= 3;
```

### 예

  - 영문자의 대문자를 소문자로 변환 하는 함수의 예.

<!-- end list -->

``` c
#include <stdio.h>
#include <string.h>

// 영문자 중에 대문자를 소문자로 바꾼다.
char convLowerAplha(char ech)
{
    if (ech >= 'A' && ech <= 'Z') {
       ech -= 'A';
       ech += 'a';
    }
    return ech;
}

 char gStr[256];

int main(int argc, char**argv)
{
   char *pstr;

    pstr = gStr;
    strcpy(pstr, "Hello");

    while (*pstr) {
      *pstr = convLowerAplha(*pstr);
      pstr++;
    }

    printf("%s\n", gStr);

    return 0;
}
```

  - 정수형 숫자를 취급하는 경우

<!-- end list -->

``` c
#include <stdio.h>

int main(int argc, char**argv)
{
   char temp = -3;

   if (temp < 0)
      printf("지금 온도는 영하 %d도 입니다.\n", temp);
   else
      printf("지금 온도는 영상 %d도 입니다.\n", temp);

   return 0;
}
```

  - 부호없는 숫자 취급 예

<!-- end list -->

``` c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define SZ_RANDNUM 100

unsigned char gRandNum[SZ_RANDNUM];

int main(int argc, char**argv)
{
   int cnt;
   int sum;

    srand( (unsigned int) time(NULL));

    for (cnt = 0;cnt < SZ_RANDNUM;cnt++)
        gRandNum[cnt] = (unsigned char) (rand() % 100);

    for (cnt = 0, sum = 0;cnt < SZ_RANDNUM;cnt++)
        sum += (int) gRandNum[cnt];

    printf("랜덤의 평균값은 %d 입니다.\n", sum / SZ_RANDNUM);

    return 0;
}
```

## 숫자 범위

char 변수는 정수형인데 8비트의 숫자 범위에서 처리 된다.

### sign형 변수

``` c
  char cnum;
```

와 같이 선언된 변수는 +와 -을 처리하기 위한 8비트 [2의 보수](../Page/2의_보수.md "wikilink") 체계를 사용한다. 따라서 다음과 같이 [이진수](https://ko.wikipedia.org/wiki/이진수 "wikilink")로 나타낼 수 있다.

| [10진수](https://ko.wikipedia.org/wiki/10진수 "wikilink") | [2진수](https://ko.wikipedia.org/wiki/2진수 "wikilink") |
| ----------------------------------------------------- | --------------------------------------------------- |
| 127                                                   | 0111 1111                                           |
| 126                                                   | 0111 1110                                           |
| 125                                                   | 0111 1101                                           |
| ...                                                   | ...                                                 |
| 1                                                     | 0000 0001                                           |
| 0                                                     | 0000 0000                                           |
| \-1                                                   | 1111 1111                                           |
| ...                                                   | ...                                                 |
| \-127                                                 | 1000 0001                                           |
| \-128                                                 | 1000 0000                                           |

\+127의 2의보수는 -127이 된다. 반대로 -127의 2의 보수는 +127이 된다. 그러나 -128의 2의 보수는 +128이 되어야 하는데 char 변수의 범위를 벗어나므로 취급할 수 없다.

### unsign형 변수

음수가 필요 없을 경우 다음과 같이 [unsigned](https://ko.wikipedia.org/wiki/unsigned "wikilink")을 사용한다.

``` c
 unsigned char cnum;
```

위와 같이 선언된 변수는 8비트 [2진수](https://ko.wikipedia.org/wiki/2진수 "wikilink") 체계를 사용한다. 따라서 다음과 같이 2진수로 나타낼 수 있다.

| [10진수](https://ko.wikipedia.org/wiki/10진수 "wikilink") | [2진수](https://ko.wikipedia.org/wiki/2진수 "wikilink") |
| ----------------------------------------------------- | --------------------------------------------------- |
| 255                                                   | 1111 1111                                           |
| 254                                                   | 1111 1110                                           |
| 253                                                   | 1111 1101                                           |
| ...                                                   | ...                                                 |
| 1                                                     | 0000 0001                                           |
| 0                                                     | 0000 0000                                           |

## 쉬프트 연산자

``` cpp
  char c = -128;
  printf("c = %d [0x%02x]\n", c, c&0xFF );
  c >>= 1;
  printf("c >>= 1: %d [0x%02x]\n",  c, c&0xFF  );

  c = -128;
  c <<= 1;
  printf("-128 <<= 1: %d [0x%02x]\n", c, c&0xFF );

  c = 32;
  c <<= 2;
  printf("32 <<= 2: %d [0x%02x]\n", c, c&0xFF );

  unsigned char d = -128;  // unsigned는 음수를 취급하지 않으므로 음수값은 이진화 한것 자체.
  unsigned char e = d << 1;
  printf("unsigned [%d, 0x%x] <<= 1 ==> %d [0x%02x]\n", d, d, e, e );

  e = d >> 1;
  printf("unsigned [%d, 0x%x] >>= 1 ==> %d [0x%02x]\n", d, d, e, e );
```

실행결과 :

`c = -128 [0x80]`
`c >>= 1: -64 [0xc0]`
`-128 <<= 1: 0 [0x00]`
`32 <<= 2: -128 [0x80]`
`unsigned [128, 0x80] <<= 1 ==> 0 [0x00]    ---> -128은 unsigned에서 128로 저장된다.`
`unsigned [128, 0x80] >>= 1 ==> 64 [0x40]`

왼쪽으로 쉬프트할 때, char는 부호를 고려하지 않는다. 정해진 비트만쪽 LSB에 0을 채워 넣는다. 따라서 양수가 음수가 될 수도 있다.

오른쪽으로 쉬프트 할 때는

  - signed char: 부호 비트가 유지 된다. 따라서 부호 비트인 MSB가 그대로 유지된다.
  - unsigned char: MSB에 0을 무조건 채워넣는다.

## char 배열

배열은 메모리에 차례대로 나열된 구조이므로 char 문자열도 마찬가지로 8비트단위로 차례로 나열된다.

8비트 정수형 배열의 예:

``` c
  char temp[100];
  char cnt;
  for (cnt = 0; cnt < 100; cnt++)
      temp[cnt] = cnt+1;
```

### 초기치

배열의 초기치는 일반적인 배열의 규칙에 따른다.

``` c
  char temp[100] = { -10, 2, 'k', 20, 0 }; // 배열의 크기와 초기치의 크기가 다른 경우
  char temp[] = { 'k', 'i', 'm', 0 };  // 배열의 크기를 초기치로 부터 규정하는 경우
  char temp[] = "kim";

  char temp[] = { "홍", 'k',0 };  // 이런경우 배열이 1차원이기 때문에 불가능

  char temp[][10] = { "홍", { 'k',0 }, { 'h',0 }, {'p', 0 }  };
```

### [문자열](https://ko.wikipedia.org/wiki/C_문자열 "wikilink")(String)

문자열 중에서 문자를 표기하는 ASCII코드 같은 문자 코드로 구성된 경우를 문자열이라고 한다. 그러나 문자나 기타 [바이너리](https://ko.wikipedia.org/wiki/바이너리 "wikilink") 숫자 모두 정수형으로 취급 한다. 따라서 문자열이라고 특별할것은 없지만 문자만을 위한 규정이 있다. "kim"이라고 규정한다면 ASCII 3개문자와 4번째 끝을 알리는 0이 결합된 4바이트 이다. 따라서 배열에 넣으려면 4바이트 공간 이상이 있어야 한다.

만약 배열의 정해진 공간이상을 [액세스](https://ko.wikipedia.org/wiki/액세스 "wikilink")하면 액세스 자체는 가능하지만, 변수 배치상 다른 변수에 액세스하는 효과가 있으므로 개발자가 범위를 넘지 않도록 프로그램하는 수 밖에 없다.

## [struct](https://ko.wikipedia.org/wiki/struct "wikilink")에서의 사용

## [포인터](https://ko.wikipedia.org/wiki/포인터 "wikilink")

## 같이 보기

  - [C 문자열](https://ko.wikipedia.org/wiki/C_문자열 "wikilink")
  - [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")
  - [int (C 프로그래밍 언어)](https://ko.wikipedia.org/wiki/int_\(C_프로그래밍_언어\) "wikilink")
  - [wchar t](https://ko.wikipedia.org/wiki/wchar_t "wikilink")

## 외부 링크

  - [ISO C 워킹그룹 공식 웹사이트](http://www.open-std.org/jtc1/sc22/wg14/)

  - [ISO/IEC 9899](http://www.open-std.org/JTC1/SC22/WG14/www/standards). 공식 C99 문서.

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:자료형](https://ko.wikipedia.org/wiki/분류:자료형 "wikilink")