> This article is converted from Wikipedia: [Ls \(\)](https://ko.wikipedia.org/wiki/Ls_\(\)).


**`ls`**는 [POSIX](../Page/POSIX.md "wikilink") 및 [단일 유닉스 규격에](../Page/단일_유닉스_규격.md "wikilink") 규정되어 있는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제의](../Page/운영_체제.md "wikilink") [명령어](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink") 가운데 하나로, ‘list segments’의 약자이며, [파일의](../Page/컴퓨터_파일.md "wikilink") 목록을 표시하는 기능을 수행하는 명령어이다. [도스](../Page/도스.md "wikilink")에서의 [`dir`](https://ko.wikipedia.org/wiki/dir "wikilink")과 유사한 명령어이다.

## 역사

`ls`는 [AT\&T](../Page/AT&T.md "wikilink")의 유닉스 초기 버전부터 존재하던 명령어였다. 이 명칭은 [멀틱스](../Page/멀틱스.md "wikilink")에 존재하고 있었던 비슷한 커맨드에서 계승되었다. 현재 사용되고 있는 `ls`는 [자유 소프트웨어 재단에서](../Page/자유_소프트웨어_재단.md "wikilink") 구현된 판과 [FreeBSD](../Page/FreeBSD.md "wikilink"), [OpenBSD](../Page/OpenBSD.md "wikilink"), [NetBSD](../Page/NetBSD.md "wikilink") 및 [다윈](../Page/다윈_\(운영_체제\).md "wikilink") 등의 [BSD](../Page/BSD.md "wikilink") 계열 유닉스 시스템에서 사용되고 있는 판 등이 있으며, 양쪽 다 [자유 소프트웨어이며](../Page/자유_소프트웨어.md "wikilink") [오픈 소스이기도](../Page/오픈_소스.md "wikilink") 하다.

## 작동 형태

[유닉스 계열의](../Page/유닉스_계열.md "wikilink") 운영 체제에서는 현재 사용자가 작업을 수행하고 있는 [파일 시스템상의](../Page/파일_시스템.md "wikilink") 위치를 나타내는 ‘[현재 디렉터리](https://ko.wikipedia.org/wiki/작업_디렉터리 "wikilink")’(current directory)라는 개념이 존재한다. (이 개념은 [도스](../Page/도스.md "wikilink") 등에서도 존재한다.) `ls`를 옵션 없이 기동시킬 경우, 현재 디렉터리에 있는 [파일의](../Page/컴퓨터_파일.md "wikilink") 목록이 표시되게 된다. 또한, [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink") 또는 파일의 목록을 매개 변수로 지정하였을 경우, 지정된 파일 또는 디렉터리 안에 소속되어 있는 파일의 목록이 표시된다.

이때, 명칭이 ‘.’로 시작되는 파일은 보통은 표시되지 않으며, 이런 종류의 파일 또한 표시하기 위해서는 `-a`를 옵션으로 지정해야 한다.

옵션을 지정하지 않고 `ls`를 실행시켰을 경우, 파일 이름만 표시되나, 이 경우 파일의 종류와 크기, [퍼미션](https://ko.wikipedia.org/wiki/퍼미션 "wikilink") 등의 부가 정보가 표시되지 않는다. `ls`에는 표시의 형식을 변경할 수 있는 옵션들이 많이 존재하고 있다.

파일 종류를 가리키는 색을 사용하는 옵션을 적용하면 다음과 같이 출력된다:

<span style="background:#000000; color:#c0c0c0">` brw-r--r--    1 unixguy staff 64,  64 Jan 27 05:52 `<span style="color:yellow     ">`block         `</span>
` crw-r--r--    1 unixguy staff 64, 255 Jan 26 13:57 `<span style="color:#ffff00    ">`character     `</span>
` -rw-r--r--    1 unixguy staff     290 Jan 26 14:08 `<span style="color:#ff00ff    ">`compressed.gz `</span>
` -rw-r--r--    1 unixguy staff  331836 Jan 26 14:06 `<span style="color:#ff00ff    ">`data.ppm      `</span>
` drwxrwx--x    2 unixguy staff      48 Jan 26 11:28 `<span style="color:#0000ff    ">`directory     `</span>
` -rwxrwx--x    1 unixguy staff      29 Jan 26 14:03 `<span style="color:#00ff00    ">`executable    `</span>
` prw-r--r--    1 unixguy staff       0 Jan 26 11:50 `<span style="color:#ffffaa    ">`fifo          `</span>
` lrwxrwxrwx    1 unixguy staff       3 Jan 26 11:44 `<span style="color:#00ffaa    ">`link`</span>` -> `<span style="color:blue">`dir   `</span>
` -rw-rw----    1 unixguy staff     217 Jan 26 14:08 regularfile   `</span>

## 옵션

명령어 `ls` 뒤에 한 칸을 띄우고 옵션을 입력하여 출력형태를 바꿀 수 있다. 모든 파일과 폴더를 출력하라는 `-a`, 목록의 각 항목에 대해 수정시간, 파일 용량 등의 세부적인 내용을 제시하라는 `-l`등의 옵션이 있다.

옵션 없이 `ls`를 사용하면 단순 형식으로 파일을 보여준다. 일반적인 옵션은 다음과 같다:

  - `-l` 롱 포맷.
  - `-f` 정렬 안 함. 많은 수의 파일을 포함하고 있는 디렉터리에 유용함.
  - `-F` 파일의 본질을 나타내는 문자 추가.
  - `-a` “.”으로 시작하는 이름을 포함, 관련 디렉터리의 모든 파일 나열.
  - `-R` 하부 디렉터리를 반복하여 나열. 그러므로 `ls -R /` 명령은 모든 파일을 나열.
  - `-d` 심볼 링크나 디렉터리에 대한 정보 표시.
  - `-t` 수정 시간에 따라 파일 목록을 나열,
  - `-h` 사람이 인지할 수 있는 형태로 크기를 출력. (예: 1K, 234M, 2G, 등)

## 사용의 예

다음의 예는, 두 개의 옵션 (`-l`, `-F`)를 파라미터로 지정하여 `ls`를 각각 실행시켰을 때의 다른 출력 결과이다.

``` console
$ pwd
/home/fred
$ ls -l
drwxr--r--   1 fred  editors   4096  drafts
-rw-r--r--   1 fred  editors  30405  edition-32
-r-xr-xr-x   1 fred  fred      8460  edit
$ ls -F
drafts/
edition-32
edit*
```

여기서, `fred` 사용자의 홈 디렉터리에는 `drafts`라고 하는 디렉터리와 `edition-32`라는 이름의 보통 [파일](../Page/컴퓨터_파일.md "wikilink"), 여기에 `edit`라는 이름의 실행 가능한 파일이 존재함을 확인할 수 있다. `ls`는 사용자(user), 사용자의 소속 그룹(group), 파일의 소유자 외의 다른 사용자들(other)이 파일에 대해 어떤 권한(퍼미션)을 가지고 있는가를 표시하기 위해 몇 가지 문자를 채용하고 있다.

퍼미션 부분의 최초의 문자는 파일의 종류를 가리킨다.

| 문자         | 의미              |
| ---------- | --------------- |
| `-`        | 보통 파일           |
| `b`        | 블록 장치           |
| `c`        | 문자열 장치          |
| `d`        | 디렉터리            |
| `l`        | 심볼릭 링크          |
| `p` 또는 `=` | named pipe/FIFO |
| `s`        | 소켓              |
|            |                 |

첫 번째 문자 이후의 9개의 문자열은 각각 3문자씩의 세 묶음으로 나뉘어 있으며, 3문자에는 `-` 또는 각각 `r`, `w`, `x`가 표시될 수 있어, 각각 읽기, 쓰기, 실행의 권한을 가지고 있음을(`-`의 경우 없음을) 나타낸다. 첫 번째 묶음은 파일의 소유자인 사용자, 두 번째 묶음은 사용자가 속한 그룹, 세 번째는 다른 사용자들을 의미한다. 위의 예에서, `fred` 사용자는 `edition-32`을 읽고 쓸 수는 있으나, 실행은 할 수 없음을 알 수 있다. `editors` 그룹의 소속 사용자는 그 밖의 다른 사용자와 마찬가지로, `edition-32`을 읽을 수 있으나, 파일을 쓰거나 실행시키는 작업은 할 수 없다.

## 외부 링크

  -

  -

  - [ls.c](http://minnie.tuhs.org/UnixTree/V5/usr/source/s1/ls.c.html) AT\&T Ver. 5 UNIX의 ls 소스 코드.

  - [GNU ls 소스 코드](http://ftp.gnu.org/pub/gnu/coreutils/)

[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")