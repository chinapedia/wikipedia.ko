> This article is converted from Wikipedia: [Cat \(\)](https://ko.wikipedia.org/wiki/Cat_\(\)).


**`cat`** 명령어는 파일들을 [연결하고](https://ko.wikipedia.org/wiki/연결어 "wikilink") 표시하기 위해 사용되는 표준 [유닉스](../Page/유닉스.md "wikilink") 프로그램이다. 이름은 concatenate(연결하다)의 동의어인 *[catenate](https://ko.wikipedia.org/wiki/:en:wikt:catenate "wikilink")*에서 유래하였다.

## 규격

[단일 유닉스 규격은](../Page/단일_유닉스_규격.md "wikilink") 인수들로서 일정한 순서로 주어지는 각각의 파일들이 그 내용을 각각의 바이트들이 그것들이 읽혀지는 그대로 출력되도록 동일한 순서로서 표준 출력어에 쓰도록 지정한다. 또한 단일 유닉스 규격은 `-u`라는 하나의 옵션을 명령한다.

만약 파일명이 `-`로 지정된다면, `cat`은 그 순서 안에 있는 바로 그 지점에서 표준 입력어를 읽는다. 만약 어떠한 파일들도 지정되지 않았다면, `cat`은 입력되는 표준 입력어를 읽는다.

## 예시

여러개의 파일들을 합치는 명령은 다음과 같다.

`cat xaa xab xac > 파일이름`

또는

`cat xa[a-c] > 파일이름`

### 확장

`cat`의 BSD 버전([OpenBSD](../Page/OpenBSD.md "wikilink") 메뉴페이지에 따라서)과 `cat`의 GNU [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink") 버전은 다음과 같은 옵션들을 지정한다:

  - `-b` (GNU only: `--number-nonblank`): 공백이 없는 출력어에 순서를 매긴다
  - `-n` (GNU only: `--number`): 모든 출력어에 순서를 매긴다
  - `-s` (GNU only: `--squeeze-blank`): 수많은 근접한 공백들을 밀착시킨다
  - `-v` (GNU only: `--show-nonprinting`): 출력되지 않은 글자들을 보이는 것처럼 표시한다. 단 텝과 마지막 문자열은 제외한다.
  - `-t` on BSD, `-T` on GNU: `-v`을 의미하나 `^I`로서 텝을 표시할 수도 있다.
  - `-e` on BSD, `-E` on GNU: `-v`을 의미하나 `$`로서 마지막 문자열을 표시할 수도 있다.

## 유닉스 문화

### Jargon File 정의

[Jargon File](https://ko.wikipedia.org/wiki/Jargon_File "wikilink") 버전 4.4.7은 `cat`의 정의로서 다음을 열거한다:

### cat의 쓸모없는 사용

UUOC\[1\]은 "Useless Use of cat(cat의 쓸모없는 사용)"을 의미한다. *comp.unix.shell*에서 얻어진 지혜를 준수하므로 "cat의 목적은 파일들을 연결(혹은'catenate')하는 것이다. 만약 오직 하나의 파일만이 있다면, 그 파일을 아무것과도 연결시키지 않는다면 이는 시간 낭비이고 프로세스를 낭비하는 일이다." 그럼에도 불구하고 아래 같은 일을 하는 사람들이 있다.

**`cat`**` `*`file`*` | `*`some_command``   ``and``   ``its``   ``args`*` .....`

동일하고 더 저렴한 것 대신에

`<`*`file`*` `*`some_command``   ``and``   ``its``   ``args`*` ...`

이나 (동일하고 보다 더 규범적으로)

*`some_command``   ``and``   ``its``   ``args`*` ... <`*`file`*

1995년 이래로 UUOC에 대한 정기적인 상이 수여되었고, 이는 일반적으로 [펄](../Page/펄.md "wikilink") 권위자인 [Randal L. Schwartz에](https://ko.wikipedia.org/wiki/Randal_L._Schwartz "wikilink") 의해서 주어진다. 이 상과 다른 비슷한 상들에 대한 웹 페이지가 있다. [영국인](../Page/영국인.md "wikilink") [해커](../Page/해커.md "wikilink")들 사이에서는 UUCO의 정형화된 예들의 활동이 때때로 *[demoggification](https://ko.wikipedia.org/wiki/moggy "wikilink")*으로 불린다.

가벼운 편집증 환자들은 많은 유명한 키보드 매핑들에서 \< 와 \> 키가 다른 키들 옆에 있도록 주어진 경우들에 대해서는 cat을 사용하는 것이 여전히 더 안전하다고 간주한다. 리스크가 낮다고 할지라도 \< 대신에 \> 을 사용하는 영향은 매우 크고 굉장히 비쌀 수 있다.

## zcat

`zcat`은 `cat`과 비슷한 [유닉스](../Page/유닉스.md "wikilink") 프로그램으로, 개별 파일들의 압축상태를 풀고 그것들을 표준 출력어에 [연결](https://ko.wikipedia.org/wiki/연결 "wikilink")시킨다. 일반적으로 `zcat`은 [`compress`](https://ko.wikipedia.org/wiki/compress "wikilink")로 압축된 파일들에서 작동되었으나, 오늘날에는 [`gzip`](https://ko.wikipedia.org/wiki/gzip "wikilink")이나 심지어는 [`bzip2`](https://ko.wikipedia.org/wiki/bzip2 "wikilink") 아카이브들에서도 작동될 수 있다. 이러한 시스템들에서는 `gunzip -c`과 동일하다.\[2\]

## 함께 보기

  - [Coreutils](https://ko.wikipedia.org/wiki/Coreutils "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [`split`](../Page/Split_\(유닉스\).md "wikilink"), 파일을 cat이 다시 연결할 수 있는 조각들로 분리시키는 명령어
  - [`tac`](https://ko.wikipedia.org/wiki/tac_\(유닉스\) "wikilink"), 파일들을 반대로 연결시킬 수 있는 비슷한 도구
  - [`type`](../Page/TYPE_\(도스_명령어\).md "wikilink"), a [DOS](https://ko.wikipedia.org/wiki/DOS "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink") 그리고 [Microsoft Windows](https://ko.wikipedia.org/wiki/Microsoft_Windows "wikilink") 명령어로 파일의 내용물을 표시한다.

## 각주

## 외부 링크

  -
### 매뉴얼 페이지

  -
  -
  -
  -
  -
### 기타

  - [UUOC awards](http://www.iki.fi/era/unix/award.html)

[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.  [유즈넷](../Page/유즈넷.md "wikilink")의 *comp.unix.shell*에서 나온 말
2.  \[[http://www.freebsd.org/cgi/man.cgi?query=zcat\&apropos=0\&sektion=1\&manpath=FreeBSD+7.0-RELEASE\&format=html\]zcat](http://www.freebsd.org/cgi/man.cgi?query=zcat&apropos=0&sektion=1&manpath=FreeBSD+7.0-RELEASE&format=html%5Dzcat) manual page in FreeBSD 7.0