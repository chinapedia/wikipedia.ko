> This article is converted from Wikipedia: [Basename](https://ko.wikipedia.org/wiki/Basename).


**basename**(베이스네임)은 표준 [유닉스](../Page/유닉스.md "wikilink") [컴퓨터 프로그램이다](../Page/컴퓨터_프로그램.md "wikilink"). basename에 [경로 이름을](../Page/경로.md "wikilink") 지정하면 마지막 슬래시(`'/'`) 전까지의 앞 글자들을 지우고 결과를 반환한다. basename은 [SUS에](../Page/단일_유닉스_규격.md "wikilink") 기술되어 있으며 주로 [셸 스크립트에](../Page/셸_스크립트.md "wikilink") 쓰인다.

## 사용법

basename에 대한 [SUS의](../Page/단일_유닉스_규격.md "wikilink") 용법은 다음과 같다.

    basename 문자열 [접미사]

  -
    `문자열`
      -
        경로 이름
    `접미사`
      -
        접미사를 지정하면 `basename`는 접미사 부분도 삭제한다.

## 예

basename은 경로 이름에서 마지막 이름만을 반환한다.

``` console
$ basename /home/jsmith/base.wiki
base.wiki

$ basename /home/jsmith/
jsmith

$ basename /
/
```

또, basename은 기초 이름의 끝 부분을 제거하는데 사용할 수도 있다.

``` console
$ basename /home/jsmith/base.wiki .wiki
base

$ basename /home/jsmith/base.wiki ki
base.wi

$ basename /home/jsmith/base.wiki base.wiki
base.wiki
```

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [dirname](https://ko.wikipedia.org/wiki/dirname "wikilink")
  - [경로](../Page/경로.md "wikilink")

## 외부 링크

  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")