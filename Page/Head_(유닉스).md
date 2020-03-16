> This article is converted from Wikipedia: [Head \(\)](https://ko.wikipedia.org/wiki/Head_\(\)).


**head**는 유닉스 및 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제 하에서 사용되는 컴퓨터 프로그램으로 파일이나 데이터의 처음 몇 줄을 보여 주는 명령어이다. 기본적인 용례는 아래와 같다:

`head [options] `<file_name>

head 명령어는 아무 옵션 없이 사용될 경우, 입력된 데이터의 처음 10개 행만을 출력할 것이다. 출력되는 행의 개수는 명령행 옵션으로 변경될 수 있다. 아래에 따르는 예가 *filename*의 처음 20개 행을 출력하여 보여줄 것이다. :

`head -n 20 `*`filename`*

아래와 같은 명령은 *foo*로 시작하는 모든 파일의 처음 5 행을 출력하여 보여 준다. :

`head -n 5 `*`foo*`*

몇몇 버전에서는 n을 생략하고 -5와 같이 숫자만 입력해도 같은 기능을 수행하게 되어 있다.

## Flags

`-c `<x number of bytes>` 첫 x만큼의 바이트를 복사하시오`

## 기타

유닉스의 많은 초기 버전들은 이 명령어를 가지고 있지 않았기 때문에, [sed](https://ko.wikipedia.org/wiki/sed "wikilink")로 이와 같은 일을 하였다. :

`sed 5q `*`foo`*

이것은 *foo*라는 파일의 5줄을 출력하고, 끝내라(q)는 뜻이다.

## 같이 보기

  - [tail](https://ko.wikipedia.org/wiki/tail_\(유닉스\) "wikilink")

## 외부 링크

  - [head](http://www.gnu.org/software/coreutils/manual/html_node/head-invocation.html) manual page from [GNU](../Page/GNU.md "wikilink") [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink").
  - [FreeBSD documentation for head](http://www.freebsd.org/cgi/man.cgi?query=head&apropos=0&sektion=0&manpath=FreeBSD+5.3-RELEASE+and+Ports&format=html)

[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")