> This article is converted from Wikipedia: [Echo \(\)](https://ko.wikipedia.org/wiki/Echo_\(\)).


**`echo`**는 [도스](../Page/도스.md "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [유닉스](../Page/유닉스.md "wikilink") 및 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제에서 문자열을 [컴퓨터 터미널에](https://ko.wikipedia.org/wiki/컴퓨터_터미널 "wikilink") 출력하는 [명령어](https://ko.wikipedia.org/wiki/명령어 "wikilink")이다. 일반적으로 [셸 스크립트와](../Page/셸_스크립트.md "wikilink") [배치 파일에서](../Page/배치_파일.md "wikilink") 화면이나 파일로 상황을 알리는 문자열을 출력할 때에 사용된다.

## 사용 예시

``` bash
$ echo This is a test.
This is a test.
$ echo "This is a test." > ./test.txt
$ cat ./test.txt
This is a test.
```

유닉스의 프로그램은 `-n`이나 `-e` 등의 옵션을 지원한다. 이러한 옵션은 보통 [BSD](../Page/BSD.md "wikilink")와 [시스템 V](https://ko.wikipedia.org/wiki/시스템_V "wikilink") 간의 비호환성 때문에 표준\[1\] 으로 인정받지는 못하고 있다. 이러한 문제가 발생할 때에는 [`printf`](https://ko.wikipedia.org/wiki/printf "wikilink") 명령어를 사용하여 해결할 수 있다.

## 구현 예시

`echo` 명령어는 [C 언어로도](https://ko.wikipedia.org/wiki/C_언어 "wikilink") 단지 몇 줄의 [코드](https://ko.wikipedia.org/wiki/코드 "wikilink")로 구현이 가능하다.

``` c
/* echo command-line arguments */

#include <stdio.h>

int main(int argc, char *argv[]) {
  int i;
  for (i = 1; i < argc; i++)
    printf("%s%s", argv[i], (i < argc-1) ? " " : "");
  printf("\n");
  return 0;
}
```

[스크립트 언어로는](../Page/스크립트_언어.md "wikilink") 한 줄로도 만들 수 있다.

``` bash
$ perl -e 'print join " ", @ARGV; print "\n"' This is a test.
This is a test.
$ python -c "import sys; print ' '.join(sys.argv[1:])" This is a test.
This is a test.
```

## 참고 자료

<references/>

## 외부 링크

  - [Microsoft TechNet Echo article](http://technet.microsoft.com/en-us/library/bb490897.aspx)
  - [Writing programs with Echo (DOS)](https://web.archive.org/web/20081227071839/http://www.halcode.com/archives/2008/05/04/writing-programs-with-echo-dos/)

[분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:내부 도스 명령어](https://ko.wikipedia.org/wiki/분류:내부_도스_명령어 "wikilink") [분류:OS/2](https://ko.wikipedia.org/wiki/분류:OS/2 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:컴퓨팅 명령어](https://ko.wikipedia.org/wiki/분류:컴퓨팅_명령어 "wikilink")

1.  [IEEE Std 1003.1, 2004, documentation for echo](http://www.opengroup.org/onlinepubs/009695399/utilities/echo.html)