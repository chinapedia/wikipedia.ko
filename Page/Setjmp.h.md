> This article is converted from Wikipedia: [Setjmp.h](https://ko.wikipedia.org/wiki/Setjmp.h).


**setjmp.h**는 비로컬 점프를 제공하기 위한 [C 표준 라이브러리에](../Page/C_표준_라이브러리.md "wikilink") 정의된 [헤더 파일로](../Page/헤더_파일.md "wikilink") 일반적인 [서브루틴](https://ko.wikipedia.org/wiki/서브루틴 "wikilink") 콜에서 벗어나고 시퀀스를 반환하는 [제어 흐름이다](../Page/제어_흐름.md "wikilink"). 상호보완적인 함수 **`setjmp`**와 **`longjmp`**가 이러한 기능을 제공한다.

`setjmp`/`longjmp`의 일반적인 사용법은 여러 단계의 함수 호출에서도 프로그램 또는 스레드 상태를 재설정하는 데 `longjmp` 기능을 활용하는 [예외 매커니즘의](https://ko.wikipedia.org/wiki/예외_매커니즘 "wikilink") 구현에 있다. 그 외의 `setjmp` 용도로는 [코루틴](../Page/코루틴.md "wikilink")과 비슷한 구문을 만들기 위해 사용된다.

## 간단한 예

setjmp의 기초적인 예시를 보여준다. 여기서 `main()`은 `second()`를 호출하는 `first()`를 호출한다. 다음, `second()`은 `main()`로 점프하면서 `first()`의 `printf()`의 호출을 생략한다.

``` c
#include <stdio.h>
#include <setjmp.h>

static jmp_buf buf;

void second(void) {
    printf("second\n");         // 출력
    longjmp(buf,1);             // setjmp가 불려진 곳으로 점프하면서 setjmp가 1을 반환
}

void first(void) {
    second();
    printf("first\n");          // 출력되지 않음
}

int main() {
    if (!setjmp(buf))
        first();                // 실행되면 setjmp가 0을 반환
    else                        // longjmp 점프가 되돌아가면 setjmp가 1을 반환
        printf("main\n");       // 출력

    return 0;
}
```

실행하면 다음과 같이 출력한다.

``` text
second
main
```

`first()` 서브루틴이 호출되어도 "`first`"이 출력되지 않는 것을 확인할 수 있다. 조건문 `if (!setjmp(buf))`이 두 번 실행함으로서 "`main`"에서 출력 코드가 실행된다.

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink") [분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink")