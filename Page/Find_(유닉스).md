> This article is converted from Wikipedia: [Find \(유닉스\)](https://ko.wikipedia.org/wiki/Find_\(유닉스\)).


[유닉스 계열과](../Page/유닉스_계열.md "wikilink") 일부 기타 [운영 체제에서](../Page/운영_체제.md "wikilink") **`find`**는 일부 [사용자](../Page/사용자_\(컴퓨팅\).md "wikilink") 지정 기준에 따라 [파일을](../Page/컴퓨터_파일.md "wikilink") 찾고 사용자 정의 행위를 각 매칭되는 파일에 적용하여 [파일 시스템의](../Page/파일_시스템.md "wikilink") 하나 이상의 [디렉터리 트리를](https://ko.wikipedia.org/wiki/디렉터리 "wikilink") 검색하는 [명령 줄 유틸리티이다](https://ko.wikipedia.org/wiki/명령_줄_유틸리티 "wikilink"). 사용 가능한 검색 기준에는 [패턴을](https://ko.wikipedia.org/wiki/패턴_매칭 "wikilink") 포함시켜 [파일 이름](../Page/파일_이름.md "wikilink") 또는 파일의 수정일/접근일의 시간 범위를 매칭시키는 것이 포함된다. 기본적으로 `find`는 현재의 [작업 디렉터리](https://ko.wikipedia.org/wiki/작업_디렉터리 "wikilink") 아래의 파일 목록을 반환한다.

관련 [`locate`](../Page/Locate.md "wikilink") 프로그램들은 `find`를 통해 수집된 인덱싱된 파일의 데이터베이스를 사용하여([`Cron`](../Page/Cron.md "wikilink") 잡을 통해 정기적인 주기로 업데이트됨) 전체 파일 시스템에서 이름순으로 파일을 검색하는 빠른 방식을 제공한다.

## 역사

`find`는 [프로그래머의 워크벤치](https://ko.wikipedia.org/wiki/PWB/UNIX "wikilink") 프로젝트의 일부로서 [버전 5 유닉스에](https://ko.wikipedia.org/wiki/버전_5_유닉스 "wikilink") 등장했으며 cpio와 더불어 Dick Haight에 의해 작성되었다.\[1\] (cpio와 함께 사용하도록 설계되었음)\[2\]

## Find 문법

``` console
$ find [-H] [-L] [-P] 경로... [식]
```

3개의 옵션들은 어떻게 `find` 명령이 심볼릭 링크를 처리하는지를 통제한다. 기본 동작은 심볼릭 링크를 따라가지 않는다. -P 플래그를 사용하여 명시적인 지정이 가능하다. -L 플래그는 `find` 명령어가 심볼릭 링크를 따라갈 수 있게 한다. -H 플래그는 명령 줄 변수를 처리하는 동안에만 심볼릭 링크를 따라가게 한다. 이 플래그들은 일부 오래된 버전의 `find`에서는 사용이 불가능하다.

적어도 하나의 경로는 식이 우선해야 한다. `find`는 내부적으로 [와일드카드를](https://ko.wikipedia.org/wiki/와일드카드_문자 "wikilink") 해석할 수 있으며 명령어들은 [셸 글로빙을](../Page/글로브_\(프로그래밍\).md "wikilink") 통제하기 위해 조심스럽게 구성되어야 한다.

식 요소들은 공백으로 구분되며 왼쪽에서 오른쪽으로 평가한다. 이들은 AND(‑and 또는 ‑a) 또는 OROR (‑or ‑o) 등의 논리 요소들을 포함할 수 있다.

[GNU](../Page/GNU_패키지_목록.md "wikilink") `find`에는 POSIX에서 규정되지 않은 수많은 추가 기능들이 포함되어 있다.

## 관련 유틸리티

  - [`locate`](../Page/Locate.md "wikilink")
  - [`Grep`](../Page/Grep.md "wikilink")
  - [`tree`](https://ko.wikipedia.org/wiki/tree "wikilink")
  - [GNU Find 유틸리티](../Page/GNU_패키지_목록.md "wikilink")(findutils)
  - [비지박스](../Page/비지박스.md "wikilink")
  - [`dir`](https://ko.wikipedia.org/wiki/dir "wikilink")

## 같이 보기

  - [스포트라이트 (소프트웨어)](https://ko.wikipedia.org/wiki/스포트라이트_\(소프트웨어\) "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [도스 명령어 목록](../Page/도스_명령어_목록.md "wikilink")
  - [Grep](../Page/Grep.md "wikilink")

## 각주

## 외부 링크

  -
  - [Official webpage for GNU find](https://www.gnu.org/software/findutils/manual/html_mono/find.html)

  - [Command find – 25 practical examples](http://www.librebyte.net/en/gnulinux/command-find-25-practical-examples/)

[분류:정보 검색 시스템](https://ko.wikipedia.org/wiki/분류:정보_검색_시스템 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.
2.