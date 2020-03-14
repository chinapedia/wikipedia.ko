> This article is converted from Wikipedia: [Assert.h](https://ko.wikipedia.org/wiki/Assert.h).


**assert.h**는 [C 표준 라이브러리](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") 중 하나다. [C 언어 전처리기](https://ko.wikipedia.org/wiki/C_언어_전처리기 "wikilink") [매크로](https://ko.wikipedia.org/wiki/매크로 "wikilink") 중 하나인 `assert()`\[1\]\[2\] 이 매크로는 [표명](../Page/표명.md "wikilink")을 구현하여 프로그램이 추정한 것을 확인하며 거짓인 경우 진단 메시지를 출력한다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서는 **cassert** 헤더 파일을 통해 사용할 수 있다.

프로그램이 실행될 때, `assert()` 는 조건에 오류가 있을 경우 표준오류 (`stderr`) 를 통해 실패한 호출의 정보를 출력하고, `abort()`를 호출한다. 표준오류 (`stderr`)에 포함된 정보는 아래와 같다.

  - 소스 파일명 (미리정의된 매크로 `__FILE__`)
  - 소스 라인 넘버 (미리정의된 매크로 `__LINE__`)
  - 소스 함수 (미리정의된 식별자 `__func__`)(**C99**에서 추가 됨)
  - 0으로 추정된 텍스트 표현\[3\]

리눅스에서 컴파일된 오류의 예

``program: program.c:5: main: Assertion `a != 1' failed.``
`Abort (core dumped)`

## 예제

``` c
#include <stdio.h>
#include <assert.h>

int test_assert ( int x )
{
   assert( x <= 4 );
   return x;
}

int main ( void )
{
  int i;

    for (i=0; i<=9; i++)
    {
        test_assert( i );
        printf("i = %d\n", i);
    }

  return 0;
}
```

`i = 0`
`i = 1`
`i = 2`
`i = 3`
`i = 4`
``assert: assert.c:6: test_assert: Assertion `x <= 4' failed.``
`Aborted`

## 같이 보기

  - [표명](../Page/표명.md "wikilink")

## 각주

[분류:C 표준 라이브러리 헤더](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리_헤더 "wikilink")

1.  International Standard for Programming Language C (C99), ISO/IEC 9899:1999, p. 169
2.
3.  International Standard for Programming Language C (C99), ISO/IEC 9899:1999, p. 169