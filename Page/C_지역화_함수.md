> This article is converted from Wikipedia: [C 지역화 함수](https://ko.wikipedia.org/wiki/C_지역화_함수).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서, **C 지역화 함수**는 기본적인 지역화 루틴을 구현한 [C 프로그래밍 언어내](../Page/C_\(프로그래밍_언어\).md "wikilink") 함수 모음이다.\[1\]\[2\] 이 기능은 다국어 프로그램에서 사용되어 특정 로케일에 조정된다. 특히, 숫자나 통화를 표시하는 방법을 수정하는 데 쓰인다. 이 설정은 C 표준 라이브러리 내 [입출력 함수의](../Page/C_파일_입출력.md "wikilink") 동작에 영향을 준다.

## 예시

``` c
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

int main(void)
{
    /* Locale is set to "C" before this. This call sets it
       to the "current locale" by reading environment variables: */
    setlocale(LC_ALL, "");

    const struct lconv * const currentlocale = localeconv();

    printf("In the current locale, the default currency symbol is: %s\n",
        currentlocale->currency_symbol);

    return EXIT_SUCCESS;
}
```

## 같이 보기

  - [로케일](../Page/로케일.md "wikilink")

## 참조

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.
2.