> This article is converted from Wikipedia: [Du \(유닉스\)](https://ko.wikipedia.org/wiki/Du_\(유닉스\)).


**`du`**(디스크 사용률을 의미하는 ***d**isk **u**sage*의 준말)는 [파일 시스템](../Page/파일_시스템.md "wikilink") 상의 특정 [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")나 [파일](../Page/컴퓨터_파일.md "wikilink") 하에 사용되는 파일 공간 사용률을 측정하기 위해 사용되는 표준 [유닉스](../Page/유닉스.md "wikilink") [프로그램이다](../Page/컴퓨터_프로그램.md "wikilink").

## 역사

`du` 유틸리티는 [AT\&T 유닉스](https://ko.wikipedia.org/wiki/유닉스의_역사 "wikilink") 버전 1에 처음 등장하였다. [GNU](../Page/GNU.md "wikilink") [coreutils에](../Page/GNU_코어_유틸리티.md "wikilink") 기본 포함된 `du`는 Torbjorn Granlund, David MacKenzie, Paul Eggert, Jim Meyering에 의해 처음 개발되었다.\[1\]

## 사양

기본적으로 [단일 유닉스 규격](../Page/단일_유닉스_규격.md "wikilink")(SUS)은 `du`가 현재 디렉터리에 포함된 각 파일과 디렉터리에 할당된 파일 공간을 표시할 것을 규정하고 있다. 링크는 링크 파일의 크기로 표시되며 어디에 연결되는지를 표시하지는 않는다. 디렉터리의 내용물의 크기는 예측한대로 표시된다.

`du`는 할당 공간을 보고하며 절대 파일 공간을 보고하지는 않는다. `du`를 통해 표시되는 파일 시스템의 공간의 양은 파일들이 [삭제되었으나](https://ko.wikipedia.org/wiki/rm_\(유닉스\) "wikilink") 파일 블록이 아직 해제(free)되지 않은 경우 [`df`](https://ko.wikipedia.org/wiki/df_\(Unix\) "wikilink")에 의해 표시되는 바와 차이를 보일 수 있다. 또, 파일시스템의 데이터블록을 할당하는 minfree 설정과 슈퍼 사용자 프로세스들은 전체 블록과 사용 중인/사용 가능한 블록의 합 사이의 차이를 보일 수 있다. minfree 설정은 보통 전체 파일 시스템 크기의 약 5%로 설정된다. 더 자세한 정보의 경우 [core utils faq](https://www.gnu.org/software/coreutils/faq/coreutils-faq.html#df-Size-and-Used-and-Available-do-not-add-up)를 참고할 것.

## 사용법

`du`는 하나의 인수를 받으며 `du`가 동작하기 위한 경로명을 지정한다. 이를 지정하지 않으면 현재의 디렉터리가 사용된다. SUS는 `du`에 다음의 옵션을 규정한다:

  -
    `-a`: 기본 출력 외에 디렉터리가 아닌 개별 항목의 정보를 포함한다
    `-c`: 다른 인수에 의해 발견된 디스크 사용률의 총합을 표시한다
    `-d #`: 총합 발생 심도(depth). -d 0은 현재 레벨의 총합, -d 1은 하위 디렉터리의 합계, -d 2는 하위 디렉터리들의 합계 등을 의미한다
    `-H`: 명령 줄에 지정된 링크 참조에 대한 디스크 사용률을 계산한다
    `-k`: 512바이트가 아닌 1024[바이트](../Page/바이트.md "wikilink") 단위로 크기를 표시한다
    `-L`: 모든 곳의 링크 참조에 대한 디스크 사용률을 계산한다
    `-s`: 포함된 각 디렉터리가 아닌, 현재 디렉터리의 사용률 총합만 보고한다
    `-x`: 경로명 인수가 지정된 장치의 파일과 디렉터리만 탐색한다

다른 유닉스, 유닉스 계열 운영 체제는 추가 옵션이 있을 수 있다. 이를테면, BSD와 GNU `du`는 사용자가 디스크 사용률을 읽기 더 쉬운 포맷을 표시하는 `-h` 옵션을 제공한다.

## 예시

[킬로바이트](../Page/킬로바이트.md "wikilink")(-k) 단위로 디렉터리의 총합을 구한다(-s):

``` console
$ du -sk *
152304  directoryOne
1856548 directoryTwo
```

인간이 읽을 수 있는 포맷(-h : 바이트, 킬로바이트, 메가바이트, 기가바이트, 테라바이트, 페타바이트)으로 디렉터리의 총합(-s)을 구한다:

``` console
$ du -sh *
149M directoryOne
1.8G directoryTwo
```

현재 디렉터리 안의 숨김 파일을 포함하여 모든 하위 디렉터리와 파일의 디스크 사용률을 구한다 (파일 크기순 정렬):

``` bash
 $ du -sk .[!.]* *| sort -n
```

현재 디렉터리 안의 숨김 파일을 포함하여 모든 하위 디렉터리와 파일의 디스크 사용률을 구한다 (파일 크기 역순 정렬):

``` bash
 $ du -sk .[!.]* *| sort -nr
```

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 각주

## 외부 링크

  -
### 매뉴얼 페이지

  -
  -
  -
  -
  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink")

1.  <https://linux.die.net/man/1/du>