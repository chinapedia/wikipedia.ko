> This article is converted from Wikipedia: [Printf](https://ko.wikipedia.org/wiki/Printf).


[350px](https://ko.wikipedia.org/wiki/파일:Printf.svg "wikilink") **printf** 함수는 일반적으로 몇 가지 프로그래밍 언어와 연결된 [함수의](../Page/함수_\(프로그래밍\).md "wikilink") 일종이다. 다양한 자료형 변수를 문자열로 변환하는 방식을 지정해주는 형식 문자열(format string)인 문자열 변수를 받아들인다. 이 문자열은 기본적으로 [표준 출력](https://ko.wikipedia.org/wiki/표준_스트림#.ED.91.9C.EC.A4.80_.EC.B6.9C.EB.A0.A5_.28stdout.29 "wikilink") 시스템에 인쇄된다.

이에 대한 변종으로 fprintf, sprintf에서부터 vprintf, vfprintf, vsprintf, vsnprintf, vasprintf 등이 있다.

## 일반적인 예

일반적인 프로그래밍 언어에서는 다음과 같은 형식으로 printf를 이용한다.

``` c
int printf(const char *format, ...)
```

## 프로그래밍 언어에서의 사용

### C 언어

``` c
printf("문자열 %s, 정수 %d, 16진수 %#x, 소숫점 %3.2, 자른 문자열 %.*s \n", "test", 20, 0xf747, 3.1415f, 3, "toast");

```

이 코드는 다음과 같이 출력한다

`문자열 test, 정수 20, 16진수 0xf747, 소숫점 3.14, 자른 문자열 toa`

## 일반적인 변종 함수

### fprintf

``` c
char fprintf(FILE *stream, const char *format, ...)
```

### sprintf

``` c
int sprintf(char *str, const char *format, ...)
```

sprintf()는 스트림(char 변수이름\[\])에 기존에 있던 내용을 지우고 그 곳에다가 'const char \*format'부분에다 쓴 내용을 넣는다.

``` c++ numberLines
#include<stdio.h>

int main(void)
{
    char text[11];

    sprintf(text,"ABCDEFGHIJ");
    printf("%s",text);

    return 0;
}
```

출력:

``` c
ABCDEFGHIJ
```

### vprintf, vfprintf, vsprintf, vsnprintf, and vasprintf

``` c
#include <stdio.h>
/* va_list versions of above */
int vprintf(const char *format, va_list ap);
int vfprintf(FILE *stream, const char *format, va_list ap);
int vsprintf(char *str, const char *format, va_list ap);
int vsnprintf(char *str, size_t size, const char *format, va_list ap);
int vasprintf(char **ret, const char *format, va_list ap);
```

이 함수들은 일부 printf가 구현되어 있지 않은 임베디드 시스템에서 직접적인 구현을 위해 사용된다.

## printf를 이용하는 프로그래밍 언어

  - [AMPL](https://ko.wikipedia.org/wiki/AMPL "wikilink")
  - [awk](https://ko.wikipedia.org/wiki/aWK "wikilink")
  - [본 셸](https://ko.wikipedia.org/wiki/본_셸 "wikilink") (sh) 및 파생물([콘 셸](../Page/콘_셸.md "wikilink") (ksh), [bash](https://ko.wikipedia.org/wiki/bash "wikilink"), [Z 셸](../Page/Z_셸.md "wikilink") (zsh)
  - [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink")
      - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")
      - [오브젝티브-C](https://ko.wikipedia.org/wiki/오브젝티브-C "wikilink")
  - [클로저](https://ko.wikipedia.org/wiki/클로저 "wikilink")
  - [D](https://ko.wikipedia.org/wiki/D_\(프로그래밍_언어\) "wikilink")
  - [F\#](https://ko.wikipedia.org/wiki/F_샤프_\(프로그래밍_언어\) "wikilink")
  - [GNU MathProg](https://ko.wikipedia.org/wiki/GNU_리니어_프로그래밍_키트 "wikilink")
  - [GNU 옥타브](../Page/GNU_옥타브.md "wikilink")
  - [Go](https://ko.wikipedia.org/wiki/Go_\(프로그래밍_언어\) "wikilink")
  - [하스켈](https://ko.wikipedia.org/wiki/하스켈 "wikilink")
  - [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") (1.5 버전 이후)
  - [메이플](https://ko.wikipedia.org/wiki/메이플_\(소프트웨어\) "wikilink")
  - [Mathematica](https://ko.wikipedia.org/wiki/매스매티카 "wikilink")
  - [MATLAB](../Page/MATLAB.md "wikilink")
  - [Mythryl](https://ko.wikipedia.org/wiki/Mythryl "wikilink")
  - [Objective Caml](https://ko.wikipedia.org/wiki/Objective_Caml "wikilink")
  - [PHP](https://ko.wikipedia.org/wiki/PHP "wikilink")
  - [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") (% 연산자 사용)
  - [펄](https://ko.wikipedia.org/wiki/펄 "wikilink")
  - [R](../Page/R_\(프로그래밍_언어\).md "wikilink")
  - [루비](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink")
  - [Vala](https://ko.wikipedia.org/wiki/Vala_\(프로그래밍_언어\) "wikilink") (`print()` 및 `FileStream.printf()`을 통해)

## 같이 보기

  - [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink")
  - [형식 문자열 공격](https://ko.wikipedia.org/wiki/형식_문자열_공격 "wikilink")
  - [`iostream`](https://ko.wikipedia.org/wiki/iostream "wikilink")
  - [`scanf`](https://ko.wikipedia.org/wiki/scanf "wikilink")

## 외부 링크

  -
  -
[분류:Stdio.h](https://ko.wikipedia.org/wiki/분류:Stdio.h "wikilink") [분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink")