> This article is converted from Wikipedia: [Stdarg.h](https://ko.wikipedia.org/wiki/Stdarg.h).


**`stdarg.h`**는 [C의](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") [C 표준 라이브러리의](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") 헤더로 인자 수를 [제한 없이 할 수 있도록](https://ko.wikipedia.org/wiki/가변_함수 "wikilink") 하는 함수를 허용할 수 있도록 한다.\[1\] 이 헤더는 알려지지 않는 숫자나 타입의 함수 인자 목록을 통한 절차를 위한 기능을 제공한다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서는 이 기능을 `cstdarg`에서 제공한다.

`stdarg.h`의 내용은 가변 함수라 불리는 다른 함수 (예 - [vprintf](https://ko.wikipedia.org/wiki/vprintf "wikilink"))에 쓰이나 일반적으로 [가변 함수에](https://ko.wikipedia.org/wiki/가변_함수 "wikilink") 쓰인다.

## 가변 함수 선언

[가변 함수는](https://ko.wikipedia.org/wiki/가변_함수 "wikilink") 임의 개수의 인자가 쓰이고 마지막 인자 대신 줄임표에 의해 선언되는 함수이다. 이를 이용한 함수의 예시로 [`printf`](https://ko.wikipedia.org/wiki/printf "wikilink")가 있다. 일반적으로 다음과 같이 선언할 수 있다.

``` c
int check(int a, double b, ...);
```

가변 함수는 최소 하나의 인자는 가져야 한다. 따라서 다음 예시는

``` c
char *wrong(...);
```

는 C에서 허용되지 않는다. (C++에선 가능) C에서, 콤마는 줄임표 앞에 있어야 하나 C++에선 그렇지 않아도 된다.

## 예시

``` c
#include <stdio.h>
#include <stdarg.h>

/* print all args one at a time until a negative argument is seen;
   all args are assumed to be of int type */
void printargs(int arg1, ...)
{
  va_list ap;
  int i;

  va_start(ap, arg1);
  for (i = arg1; i >= 0; i = va_arg(ap, int))
    printf("%d ", i);
  va_end(ap);
  putchar('\n');
}

int main(void)
{
   printargs(5, 2, 14, 84, 97, 15, -1, 48, -1);
   printargs(84, 51, -1);
   printargs(-1);
   printargs(1, -1);
   return 0;
}
```

이 프로그램은 다음과 같이 출력한다.

    5 2 14 84 97 15
    84 51

    1

함수에서 부터 다른 var 인자 함수를 부르기 위해 (예 - sprintf) 해당 함수의 var 인자 함수를 사용할 필요가 있다. (vsprintf가 이 예시에 있음)

``` c
void MyPrintf(const char *format, ...)
{
  va_list args;
  char buffer[BUFSIZ];

  va_start(args, format);
  vsnprintf(buffer, sizeof buffer, format, args);
  va_end(args);
  FlushFunnyStream(buffer);
}
```

## 각주

<references />

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.