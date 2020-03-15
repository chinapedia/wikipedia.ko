> This article is converted from Wikipedia: [C ](https://ko.wikipedia.org/wiki/C_).


[매크로는](https://ko.wikipedia.org/wiki/매크로_\(컴퓨터_과학\) "wikilink") 컴퍼일러에게 코드의 특성을 알려주는 [키워드](https://ko.wikipedia.org/wiki/키워드 "wikilink")이다. 따라서 기계어로 컴파일 과정에서 필요한 요소이고, 매크로 자체가 기계어 코드로 생성되지는 않지만 특정 코드를 제어하는데 사용한다.

## 파일 포함하기

### \#include

특정 프로그램 파일을 현재 위치에 첨부하여 하나의 파일처럼 컴파일한다. 보통 [IDE](https://ko.wikipedia.org/wiki/IDE "wikilink") 개발툴들은 보통 프로젝트(Project)라는 개념이 도입되어 있다. 한개의 프로젝트를 수행하기 위한 프로그램 파일 및 설정 등을 관리하고, 컴파일하여 실행 파일을 만들고 디버깅을 제공한다. 여러개의 파일을 프로젝트에 등록만 하면 서로 설정된 함수나 변수를 사용할 수 있다. 프로그램 파일이 개별적으로 저장되고 개별적으로 컴파일되어 오브젝트 파일을 생성한다. 서로 다른 함수의 함수나 기타를 활용하기 위해 함수형이나 변수형이나 선언 내용을 다른 파일 끼리 연결하는 방식이 필요하다. 이때 **\#include**을 사용한다.

``` cpp
#include <stdio.h>

int main(void)
{
    printf("Hello, world!\n");
    return 0;
}
```

printf함수가 stdio.h 파일에 정의되어 있다. 따라서 printf함수의 모양을 알 수 있다. 만약 함수의 모양을 모른다면 호출이 불가능해진다.

## 조건부 컴파일하기

매크로 \#if, \#ifdef, \#ifndef, \#else, \#elif, \#endif는 조건부 컴파일하도록 정의한다. 따라서 조건이 맞지 않으면 컴파일에서 제거 된다. 즉, 조건이 맞지 않으면 소스 자체가 없는 것과 같은 효과가 있다.

### \#if \~ \[\#elseif\] \~ \[\#else\] \~ \#endif

``` cpp
#if VERBOSE >= 2
  print("trace message");
#endif
```

VERBOSE가 정의 된 값에 따라 print 함수를 제거할 수 있다. 조건 판단은 C언어 조건과 같이 예에서 VERBOSE가 2보다 크거나 같으면 컴파일한다. 이 경우 VERBOSE 값이 미리 정의되어 있어야 조건에서 참이 가능하다.

프로그램 코드 작성 시, 임의 영역을 다양한 상황에 맞게 컴파일에서 제거할 수 있다.

### 복합 정의와 조건부

``` cpp
#ifdef __unix__ /* __unix__ is usually defined by compilers targeting Unix systems */
# include <unistd.h>
#elif defined _WIN32 /* _Win32 is usually defined by compilers targeting 32 or 64 bit Windows systems */
# include <windows.h>
#endif
```

이 경우 OS가 [UNIX](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 또는 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 환경에 따라 다른 파일을 포함 시킬 수 있다. __unix__가 정의되어 있다면, unistd.h 파일을 첨부하고 그렇지 않고 _WIN32가 정의되어 있다면 windows.h 파일을 첨부한다. __unix__나 _WIN32의 정의는 다양한 방식으로 정의 할 수 있다.

매크로 `#if`와 `defined`와 연결하면 다음과 같이 복잡한 조건부 컴파일이 가능하다.

``` cpp
#if !(defined __LP64__ || defined __LLP64__) || defined _WIN32 && !defined _WIN64
    // we are compiling for a 32-bit system
#else
    // we are compiling for a 64-bit system
#endif
```

`#error`을 다음과 사용하여 컴파일 실패하게 만들 수 있다.

``` cpp
#if RUBY_VERSION == 190
# error 1.9.0 not supported
#endif
```

## 매크로 정의와 확장

### \#define \#undef 형식

**\#define**은 특정 숫자, 함수, 프로그램 블록을 다른 형태로 변환 지정한다. 다양한 선언이 가능하다. 조건은 선언 된 그 줄에 만 적용된다. 다음 줄로 연결하려면 '\\'을 사용하여 한 줄 처럼 코딩하면 된다.

프로그램 파일 내에서 **\#define**을 사용하는 것이 일반적이지만 makefile이나 기타 IDE 툴의 설정을 통해서도 정의 할 수 있다. 따라서 컴파일되는 파일에 없다고 무조건 선언이 되지 않았다는 보장이 없다. 남의 프로그램을 사용할 때는 주의가 필요하다.

이렇게 정의 내용을 해제하려면 **\#undef**을 사용하면 정의 된것이 없었던 것이 된다. 만약 어떤식으로든 이미 특정 정의가 선언되어 있다면 다시 설정할 때, **\#undef**을 이용해 제거하고 다시 설정하면 된다.

매크로 선언은 *대상변환형(Object-like macros)*\[1\] 과 *유사함수변환형(function-like macros)*\[2\] 가 있다.

대상변환형은 인수가 없고, 유사함수변환형은 함수와 유사하게 정의 :

``` cpp
#define <identifier> <replacement token list>                    // object-like macro
#define <identifier>(<parameter list>) <replacement token list>  // function-like macro, note parameters
```

정의 된 매크로는 "\#undef"을 사용하여 무효화 :

``` cpp
#undef <identifier>                                              // delete the macro
```

### 사용 예

대상변환형 :

``` cpp
#define PI 3.14159
```

코딩 중 PI 토큰이 나오면 바로 3.14159로 바꾸어 컴파일한다. 단순한 문자 교환이 이루어지는 것이다. 이렇게 하면 장점은 특정 숫자의 의미가 정확히 와닿지 않는 것을 방지할 수 있다.

``` cpp
     #define BUFFER_SIZE 1024

     foo = (char *) malloc (BUFFER_SIZE);
     for (int count = 0;count < BUFFER_SIZE;count++)
        // ...
```

코드 내에 정의 된 BUFFER_SIZE는 1024 바꾸어 컴파일한다. 이것은 다음과 같이 코딩한 것과 같다 :

``` cpp
     foo = (char *) malloc (1024);
     for (int count = 0;count < 1024;count++)
        // ...
```

코딩이 많아 질 수록 1024가 갖는 의미가 혼돈 스러울 수가 있다.

``` cpp
     #define NUMBERS 1, \
                     2, \
                     3
     int x[] = { NUMBERS }; // ==> int x[] = { 1, 2, 3 }; 와 같다.
```

`#define` 한 줄에 정의된 것만 취급한다. 다음 줄에 계속 연결할 때는 위와 같이 \\ 을 사용한다.

``` cpp
     foo = X;
     #define X 4
     bar = X;
```

매크로 정의는 정의된 이후 부터 적용 된다. 따라서 위 코드는 :

``` cpp
     foo = X;
     bar = 4;
```

토큰 교환이 bar 변수에만 적용 된다.

유사함수변환형:

``` cpp
#define RADTODEG(x) ((x) * 57.29578)
```

## 특별한 매크로와 지시문

### \#\# 토큰 연결 연산자

토큰 연결 연산자는 두개의 토큰을 하나의 토큰으로 연결한다. 예를 들어:

``` cpp
#define DECLARE_STRUCT_TYPE(name) typedef struct name##_s name##_t

DECLARE_STRUCT_TYPE(g_object); // 출력 결과는 typedef struct g_object_s g_object_t;
```

## 기타

### \#pragma

컴파일러에게 특성 옵션이나 라이브러리 형태등을 지정할 수 있다. 다양하므로 한마디로 정의 할 수 없다. 여러가지 환경에 적응할 수 있도록 컴파일러 마다 그리고 CPU 및 시스템 특성에 맞는 것들이 추가되거나 삭제된다.

## 같이 보기

  - [C 언어의 문법](../Page/C_언어의_문법.md "wikilink")

## 각주

## 외부 링크

  - [Macros](http://gcc.gnu.org/onlinedocs/cpp/Macros.html#Macros)

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:매크로 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:매크로_프로그래밍_언어 "wikilink")

1.
2.