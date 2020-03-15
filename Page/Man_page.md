> This article is converted from Wikipedia: [Man page](https://ko.wikipedia.org/wiki/Man_page).


[섬네일](https://ko.wikipedia.org/wiki/파일:Unix_manual.png "wikilink")

**man 페이지**(<small>←매뉴얼 페이지(Manual pages)의 줄임말</small>)는 거의 모든 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 및 [유닉스 계열의](../Page/유닉스_계열.md "wikilink") [운영 체제에](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 기본으로 설치되는 광범위의 문서들이다. `man`라는 유닉스 명령어를 이용하면 이 문서들을 볼 수 있다. 각 페이지는 개별 문서로 이루어져 있다.

## 역사

[유닉스의 역사](https://ko.wikipedia.org/wiki/유닉스의_역사 "wikilink") 처음 2년 동안은 문서화란 존재하지 않았다.\[1\] [유닉스 프로그래머의 매뉴얼](http://man.cat-v.org/unix-1st/)이 1971년 11월 3일 처음 출판되었다.

실제 최초의 man page는 1971년 [더글러스 매클로이의](https://ko.wikipedia.org/wiki/더글러스_매클로이 "wikilink") 주장으로 [데니스 리치와](https://ko.wikipedia.org/wiki/데니스_리치 "wikilink") [켄 톰프슨이](https://ko.wikipedia.org/wiki/켄_톰프슨 "wikilink") 작성하였다. man page 외에 "프로그래머의 매뉴얼" 또한 짧은 문서들을 모아두었고, 그 중 일부는 [강좌](https://ko.wikipedia.org/wiki/강좌 "wikilink")였고 그 외에는 운영 체제 기능에 대한 더 자세한 설명이었다.

Man page는 일반적으로 영어로 작성되어 있지만, 시스템에서 다른 언어로의 번역 또한 가능하다.

## 사용

[셸](https://ko.wikipedia.org/wiki/셸 "wikilink") 프롬프트에서 다음과 같은 식을 이용하면 유닉스 명령어에 대한 매뉴얼 페이지를 볼 수 있다.

``` bash
 man <명령어_이름>
```

예를 들면, "`man ftp`"과 같이 입력할 수 있다. 일반적으로 man의 기본 페이저는 초기값이 [less](https://ko.wikipedia.org/wiki/less "wikilink")이다.\[2\]\[3\] 즉, man 페이지를 보여줄 때 less를 사용한다. 그렇기 때문에 페이지를 탐색할 때 less의 명령어를 사용한다. (ex. : 다음 페이지로 이동. q: 종료.)

페이저는 환경변수

``` bash
 MANPAGER
```

또는

``` bash
 PAGER
```

를 덮어씌워서 자신이 원하는 프로그램(ex. [Vim](../Page/Vim.md "wikilink")) 으로 설정할 수 있다.

설명 페이지들은 전통적으로 "이름(단락)" 기호를 이용하여 나타낸다. 예를 들면, 라고 입력한다. 하나의 명령어에 대한 매뉴얼 페이지가 여러 단락에서 나타나기도 한다.

예를 들면, 리눅스와 BSD 계열의 의 설명을 보기 위한 명령어는 다음과 같다.

``` bash
 man 3 printf
```

## 매뉴얼 단락

매뉴얼은 일반적으로 여덟 개의 단락으로 나뉘어 있는데, ([BSD](https://ko.wikipedia.org/wiki/BSD "wikilink"), [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 등에서의) 단락은 다음과 같이 구성된다.

| 단락 | 설명                                                                                                         |
| -- | ---------------------------------------------------------------------------------------------------------- |
| 1  | 일반 [명령어](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink")                                             |
| 2  | [시스템 호출](../Page/시스템_호출.md "wikilink")                                                                     |
| 3  | [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink") 함수들                                                         |
| 4  | [특수 파일](../Page/장치_파일.md "wikilink") (보통 /dev 에서 발견되는 장치 파일)과 [드라이버](../Page/장치_드라이버.md "wikilink")        |
| 5  | [파일 형식과](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") convensions                                       |
| 6  | [게임과](../Page/PC_게임.md "wikilink") [화면 보호기](../Page/화면_보호기.md "wikilink")                                  |
| 7  | 기타                                                                                                         |
| 8  | 시스템 관리 [명령어와](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink") [데몬](../Page/데몬_\(컴퓨팅\).md "wikilink") |

[유닉스 시스템 V에서는](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") 비슷한 방식을 사용하지만, 순서가 다르다.

| 단락 | 설명                                                                                                         |
| -- | ---------------------------------------------------------------------------------------------------------- |
| 1  | 일반 [명령어](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink")                                             |
| 1M | 시스템 관리 [명령어와](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink") [데몬](../Page/데몬_\(컴퓨팅\).md "wikilink") |
| 2  | [시스템 호출](../Page/시스템_호출.md "wikilink")                                                                     |
| 3  | [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink") 함수들                                                         |
| 4  | [파일 형식과](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") convensions                                       |
| 5  | Miscellanea                                                                                                |
| 6  | [게임과](../Page/PC_게임.md "wikilink") [화면 보호기](../Page/화면_보호기.md "wikilink")                                  |
| 7  | [특수 파일](../Page/장치_파일.md "wikilink") (보통 /dev 에서 발견되는 장치 파일)과 [드라이버](../Page/장치_드라이버.md "wikilink")        |
|    |                                                                                                            |

어떤 시스템에서는 다음 단락이 나타난다.

| 단락 | 설명                                                                                      |
| -- | --------------------------------------------------------------------------------------- |
| 0  | [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink") [헤더 파일들](../Page/헤더_파일.md "wikilink")    |
| 9  | [커널](https://ko.wikipedia.org/wiki/커널_\(컴퓨팅\) "wikilink") 루틴들                           |
| n  | [Tcl](../Page/Tcl.md "wikilink")/[Tk](https://ko.wikipedia.org/wiki/Tk "wikilink") 키워드들 |
| x  | [X 윈도 시스템](../Page/X_윈도_시스템.md "wikilink")                                              |

단락들은 숫자 다음에 나타나는 문자들에 더 나뉜다. 예를 들면, 3C는 C 라이브러리 호출, 3M 은 수학 라이브러리 등등.

`man`명령어에 사용할 수 있는 옵션을 보려면 터미널에서 `man man`을 입력한다.

## 레이아웃

모든 man page들은 잠재적으로는 어떠한 글꼴 제어 강조 부분 없이 단순 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 텍스트 디스플레이에 출력하기에 최적화된 공통 레이아웃을 따른다. 단락은 다음을 포함할 수 있다:

  - NAME: 명령이나 함수의 이름으로, 한 줄의 설명이 뒤따른다.
    SYNOPSIS: 명령의 경우, 실행 방법 및 명령 줄 옵션이 어떠한지를 설명한다. 프로그램 함수의 경우 함수가 취하는 매개변수의 목록과 어느 파일 헤더가 이에 대한 정의를 포함하는지 설명한다.
    DESCRIPTION: 명령이나 함수의 기능에 대한 텍스트 설명이다.
    EXAMPLES: 일반적인 사용법의 몇 가지 예시이다.
    SEE ALSO: 관련 명령이나 함수의 목록이다.

그 밖의 단락들도 존재할 수 있지만, man page 간에 제대로 표준화된 것들은 아니다. 일반적인 예로는 다음을 포함한다: OPTIONS, EXIT STATUS, ENVIRONMENT, BUGS, FILES, AUTHOR, REPORTING BUGS, HISTORY, COPYRIGHT.

## 각주

## 외부 링크

  - [*Unix Programmer's Manual*](http://man.cat-v.org/unix-1st/) 1971년 11월 3일, ([스캔된 원본 PS 와 PDF](https://web.archive.org/web/20080518013206/http://cm.bell-labs.com/cm/cs/who/dmr/1stEdman.html) 참고).

  - [man](https://web.archive.org/web/20120502051559/http://primates.ximian.com/~flucifredi/man/): 오픈소스 버전의 매뉴얼, Red Hat, Mac OS X 등에 사용됨.

  - [man-db](http://man-db.nongnu.org/): 다른 버전의 매뉴얼, 데비안/우분투, SUSE 등에서 사용됨.

  - [UNIX 매뉴얼 페이지](http://manpages.bsd.lv): 유닉스 매뉴얼 페이지 언어 *mdoc*의 리소스.

  -
[분류:기술 소통](https://ko.wikipedia.org/wiki/분류:기술_소통 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:온라인 도움말](https://ko.wikipedia.org/wiki/분류:온라인_도움말 "wikilink")

1.
2.
3.