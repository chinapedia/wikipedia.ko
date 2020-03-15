> This article is converted from Wikipedia: [C  ](https://ko.wikipedia.org/wiki/C__).


[표준 라이브러리에서](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") **시그널 처리(signal processing)**는 프로그램이 실행 중에 다양한 시그널들을 어떻게 처리하는지를 정의한다. 시그널은 프로그램 내에서 몇몇 예외적인 행위([0으로 나누기](https://ko.wikipedia.org/wiki/0으로_나누기 "wikilink") 같은)를 보고하거나, 프로그램 외부의 비동기적 이벤트(키보드 키를 누르기 같은)를 보고할 수 있다.

## 표준 시그널

C 표준은 단지 6개의 시그널만을 정의한다. 이것들은 모두 `signal.h` 헤더에 정의되어 있다 (`csignal` - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서):\[1\]

  - `SIGABRT` - "abort", 비정상적 종료.
  - `SIGFPE` - **[부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink")**.
  - `SIGILL` - "illegal", 유효하지 않은 명령어.
  - `SIGINT` - "interrupt", 프로그램에 보내진 상호적인 요청.
  - `SIGSEGV` - "[세그멘테이션 오류](https://ko.wikipedia.org/wiki/세그멘테이션_오류 "wikilink")", 유효하지 않은 메모리 접근.
  - `SIGTERM` - "terminate", 프로그램에 보내진 종료 요청.

추가적인 시그널들도 구현에 따라서 `signal.h` 헤더에 정의되어 있을 수 있다. 예를들면 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 운영 체제는 15개 이상의 추가적인 [시그널들을](../Page/유닉스_신호.md "wikilink") 정의한다. .\[2\]

## 처리

시그널은 `raise()` 또는 `kill()` 시스템 호출을 호출함으로써 생성될 수 있다. `raise()` 는 현재 프로세스에 시그널을 보내며, `kill()` 은 특정한 프로세스에 시그널을 보낸다.

시그널 처리기(핸들러)는 두 개의 시그널([SIGKILL과](../Page/유닉스_신호.md "wikilink") SIGSTOP는 잡히거나 무시될 수 없다)을 제외하고는 모두 정의될 수 있다. 시그널 처리기는 상응하는 시그널이 발생되었을 때 대상 환경에 의해 호출되는 함수이다. 대상 환경은 프로그램의 실행을 시그널 처리기가 반환하거나 `longjmp()`를 호출할 때 까지 대기시킨다. 최대한의 호환성을 위해서 비동기적 신호 처리기는 오직 다음을 수행하여야 한다 :

  - `signal()` 함수에 대한 성공적인 호출을 만들어야 한다.
  - `sig_atomic_t` [volatile](https://ko.wikipedia.org/wiki/Volatile_변수 "wikilink") 변수 타입의 객체에 값들을 할당해야 한다.
  - 호출자에게 제어를 반환해야 한다

만약 시그널이 프로그램 내부에서의 에러를 보고한다면, 시그널 처리기는 `abort()`, `exit()`, `longjmp()`를 호출함으로써 종료될 수 있다.

## 함수들

<table>
<thead>
<tr class="header">
<th><p>함수</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/program/raise"><code>raise</code></a></p></td>
<td><p>시그널을 인위적으로 발생시킨다</p></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/program/signal"><code>signal</code></a></p></td>
<td><p>프로그램이 특정한 시그널을 받았을 때의 행위를 설정한다</p></td>
</tr>
</tbody>
</table>

## 사용 예시

``` c
#include <signal.h>
#include <stdio.h>
#include <stdlib.h>

static void catch_function(int signo) {
    puts("Interactive attention signal caught.");
}

int main(void) {
    if (signal(SIGINT, catch_function) == SIG_ERR) {
        fputs("An error occurred while setting a signal handler.\n", stderr);
        return EXIT_FAILURE;
    }
    puts("Raising the interactive attention signal.");
    if (raise(SIGINT) != 0) {
        fputs("Error raising the signal.\n", stderr);
        return EXIT_FAILURE;
    }
    puts("Exiting.");
    return EXIT_SUCCESS;
    // exiting after raising signal
}
```

## 같이 보기

  - [유닉스 신호](../Page/유닉스_신호.md "wikilink")

## 각주

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.
2.