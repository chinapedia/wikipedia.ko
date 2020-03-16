> This article is converted from Wikipedia: [GNU readline](https://ko.wikipedia.org/wiki/GNU_readline).


**GNU readline**은 [명령 줄 인터페이스에서](../Page/명령_줄_인터페이스.md "wikilink") 줄 편집 및 입력 기록 저장 등의 역할을 하는 [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")이다. [GNU 프로젝트에](../Page/GNU_프로젝트.md "wikilink") 속해 있다.

GNU readline은 입력 자동 완성, 커서 이동, [잘라내기, 복사, 붙여넣기](../Page/잘라내기,_복사,_붙여넣기.md "wikilink") 등의 기능을 지원하며, [Bash](https://ko.wikipedia.org/wiki/Bash "wikilink") 등의 명령 줄 기반 인터랙티브 소프트웨어에서 사용된다.

## 샘플 코드

다음의 코드는 [C로](../Page/C_\(프로그래밍_언어\).md "wikilink") 작성되어 있으며 `-lreadline` 컴파일러 플래그를 사용하여 컴파일해야 한다:

``` cpp
#include <stdlib.h>
#include <stdio.h>
#include <unistd.h>
#include <readline/readline.h>
#include <readline/history.h>

int main()
{
    char* input, shell_prompt[100];

    // Configure readline to auto-complete paths when the tab key is hit.
    rl_bind_key('\t', rl_complete);

    for(;;) {
        // Create prompt string from user name and current working directory.
        snprintf(shell_prompt, sizeof(shell_prompt), "%s:%s $ ", getenv("USER"), getcwd(NULL, 1024));

        // Display prompt and read input (n.b. input must be freed after use)...
        input = readline(shell_prompt);

        // Check for EOF.
        if (!input)
            break;

        // Add input to history.
        add_history(input);

        // Do stuff...

        // Free input.
        free(input);
    }
}
```

## 외부 링크

  - [GNU readline 홈페이지](https://web.archive.org/web/20111024235829/http://cnswww.cns.cwru.edu/php/chet/readline/rltop.html)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:텍스트 사용자 인터페이스 라이브러리](https://ko.wikipedia.org/wiki/분류:텍스트_사용자_인터페이스_라이브러리 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")