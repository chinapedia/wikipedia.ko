> This article is converted from Wikipedia: [More \(명령어\)](https://ko.wikipedia.org/wiki/More_\(명령어\)).


[명령 프롬프트에서](https://ko.wikipedia.org/wiki/명령_프롬프트 "wikilink") **`more`**는 [텍스트 파일의](../Page/텍스트_파일.md "wikilink") 내용을 한 번에 한 화면씩 보여주기 위한 [명령어이다](https://ko.wikipedia.org/wiki/명령어\(전산\) "wikilink").([터미널 페이저](https://ko.wikipedia.org/wiki/터미널_페이저 "wikilink")). 이 명령어는 [유닉스](../Page/유닉스.md "wikilink")와 [유닉스 계통](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") 시스템, [도스](../Page/도스.md "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), 그리고 [윈도에서](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 사용된다. 이러한 종류의 프로그램은 [페이저](https://ko.wikipedia.org/wiki/터미널_페이저 "wikilink")\[1\]라고 불린다. `more`는 매우 기본적인 페이저로서, 원래는 파일의 앞방향으로 밖에 움직일 수 없지만, 새로운 구현체는 뒷방향으로 움직이는 기능을 제한적으로 제공하고 있다.

## 역사

`more` 명령어는 원래 [캘리포니아 대학교 버클리](../Page/캘리포니아_대학교_버클리.md "wikilink") 졸업생인 다니엘 할버트(Daniel Halbert)가 1978년에 작성한 것이다. 이것은 3.0 [BSD](../Page/BSD.md "wikilink")에 최초로 포함된 이래로 모든 유닉스 시스템에서 표준 프로그램으로 사용되고 있다. 이와 비슷한 명령어인 [`less`](https://ko.wikipedia.org/wiki/less "wikilink")는 파일의 앞 방향만이 아닌 앞뒤 방향 모두로 움직일 수 있는 확장된 기능을 제공하는데 1983-85년에 마크(Mark Nudelman)가 작성한 것으로, 현재는 거의 모든 유닉스, 유닉스 계통 시스템에 포함되어 있다.

## 사용법

### 유닉스

[명령문](https://ko.wikipedia.org/wiki/명령문 "wikilink")은 다음과 같다:

`more [옵션] [파일 이름]`

만약 파일 이름이 주어지지 않는다면 `more`는 [`표준``   ``입력`](https://ko.wikipedia.org/wiki/표준_입력 "wikilink")으로부터 입력값을 찾는다.

`more`이 일단 입력값을 얻게 되면, 현재 화면에 맞는 한 최대한의 정보를 보여주고 이어지는 사용자의 입력을 기다린다. 단 예외적으로 폼 피드(form feed ; `^L`)가 있는 경우에는 화면에 얼마의 텍스트가 나타났는지와 무관하게 폼피드 명령이 있는 행에서 진행이 멈추게 된다. 화면 좌측 아래에 "`--More--`"라는 텍스트와 `more`가 진행시킨 파일의 백분율이 나타난다. (이 백분율 값은 현재 화면에 나타나 있는 문자를 포함한 것이다.) `more`가 파일을 끝(100%)까지 진행시키면 프로그램은 종료된다. 파일을 진행시키는 가장 일반적인 방법들로는 출력물을 한 줄씩 진행시키는 와, 한 페이지씩 진행시키는 가 있다.

다른 명령어들도 문서를 진행시키는 데에 사용될 수 있다. 더 자세한 사항은 `more`의 [매뉴얼 페이지를](https://ko.wikipedia.org/wiki/매뉴얼_페이지 "wikilink") 참고하라.\[2\]

#### 옵션

옵션들은 일반적으로 파일 이름 앞에 들어가는데, `$MORE`와 같이 [환경 변수안에](../Page/환경_변수.md "wikilink") 들어갈 수도 있다. 실제 명령행 내에 쓰인 옵션은 `$MORE` 환경 변수 안에 들어간 옵션들보다 우위를 지닌다. 옵션들은 유닉스 시스템에 따라 달라질 수 있지만 일반적인 옵션들은 다음과 같다:

  - **`-num`**: 이 옵션은 화면에 나타나는 줄 수를 지정한다.
  - **`-d`**: `more` 는 글자를 입력받아야 할 때 "\[계속하려면 스페이스바를 누르고, 나가려면 'q'를 누르시오.\]"라는 메시지를 사용자에게 보여주고 잘못된 키를 눌렀을 때에는 소리를 내는 대신 "\[도움말을 보려면 'h'를 누르시오.\]"라는 메시지를 보여준다.
  - **`-l`**: `more`는 일반적으로 `^L`(폼 피드)를 특수 문자로 받아들이기 때문에 폼 피드를 포함하고 있는 행 다음에서는 정지하게 된다. `-l` 옵션은 이러한 상황을 방지한다.
  - **`-f`**: `more`가 논리적으로 화면을 구성하도록 한다. (예를 들어 긴 문장이 끊이지 않게 한다.)
  - **`-p`**: 스크롤을 하지 않게 한다. 대신 전체 화면을 지우고 텍스트를 보이게 한다.
  - **`-c`**: 스크롤을 하지 않게 한다. 대신 화면에 보이는 대로 각 행의 남아있는 것을 지우고 화면의 위에서부터 채운다.
  - **`-s`**: 여러 행의 빈 줄을 하나로 통합한다.
  - **`-u`**: 밑줄 문자열을 무시하고 보여준다.
  - **`+/`**: **`+/`** 옵션은 파일이 표시되기 전에 찾을 문자열을 지정한다. (예시: `more +/Preamble gpl.txt`)
  - **`+num`**: `num`행 번호로부터 시작한다.

### 마이크로소프트 윈도

명령문은 다음과 같다\[3\]:

*`command`*` | `**`more`**` [/c] [/p] [/s] [/tn] [+n]`
**`more`**` [[More_(명령어)/c]_[/p]_[/s]_[/tn]_[+n|More_(명령어)//c] [/p] [/s] [/tn] [+n]] < [드라이브:] [경로] 파일 이름`
**`more`**` [/c] [/p] [/s] [/tn] [+n] [파일]`

#### 예시

화면에 letter.txt라는 이름으로 저장된 파일을 나타내기 위해서 사용자는 아래에 나오는 두 명령 중 하나를 사용할 수 있다:

**`more`**` < letter.txt`
[`type`](../Page/TYPE_\(도스_명령어\).md "wikilink")` letter.txt | `**`more`**

이 명령은 letter.txt의 첫 화면부터 보여주는데, 다음과 같은 프롬프트가 나타난다:

`-- More --`

를 누르면 다음 화면이 나타난다. 파일을 열기 전에 화면을 지우거나 모든 여백 행을 지우는 것이 가능하다.

**`more`**` /c /s < letter.txt`
[`type`](../Page/TYPE_\(도스_명령어\).md "wikilink")` letter.txt | `**`more`**` /c /s`

### OS/2

명령문은 다음과 같다:

`MORE < [드라이브:][경로]파일 이름`
`command | more`

  - **`드라이브:\경로\파일``   ``이름`** – 한 번에 한 화면씩 나타낼 파일의 장소를 지정한다.
  - **`command``   ``|`** – 그 결과가 출력될 명령어를 지정한다.

#### 예시

[`dir`](https://ko.wikipedia.org/wiki/dir_\(명령\) "wikilink") 명령을 사용하여 OS/2의 [시스템 디렉터리의](https://ko.wikipedia.org/wiki/디렉터리_\(파일_시스템\) "wikilink") 내용으로 돌아가 `more` 명령을 사용하여 그 내용을 한 화면에 보여주기:

``` dos
[C:\]dir C:\OS2 | more
```

## 함께 보기

  - [pg (유닉스)](https://ko.wikipedia.org/wiki/pg_\(유닉스\) "wikilink")
  - [less](https://ko.wikipedia.org/wiki/less "wikilink")

## 참고

## 외부 링크

  - ["FOLDOC entry for pager"](http://foldoc.org/?pager); 정의 \#2 참고.
  - [more의 manpage](http://www.linuxmanpages.com/man1/more.1.php)
  - [more 명령어의 초기 역사](https://web.archive.org/web/20090413025409/http://halwitz.org/halbert/more.html)

[분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:터미널 페이저](https://ko.wikipedia.org/wiki/분류:터미널_페이저 "wikilink") [분류:외부 도스 명령어](https://ko.wikipedia.org/wiki/분류:외부_도스_명령어 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")

1.  [foldoc.org/?pager](http://foldoc.org/?pager)
2.  [`more`](http://www.opengroup.org/onlinepubs/009695399/utilities/more.html): 파일을 한 페이지씩 보여주는 명령어 – Commands & Utilities Reference, The Single UNIX® Specification, Issue 6 from The Open Group
3.  [Microsoft TechNet More article](http://technet.microsoft.com/en-us/library/bb490933.aspx)