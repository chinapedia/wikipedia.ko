> This article is converted from Wikipedia: [DBASE](https://ko.wikipedia.org/wiki/DBASE).


[섬네일](https://ko.wikipedia.org/wiki/파일:DBaseLogo_BlackWithRed_glass_300.png "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:Screenshot_of_Dbase_III_Plus.png "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:DBASE_timeline.png "wikilink") **dBASE**는 [마이크로컴퓨터](https://ko.wikipedia.org/wiki/마이크로컴퓨터 "wikilink")용의 최초의 [데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/데이터베이스_관리_시스템 "wikilink") 가운데 하나였으며, 당시 가장 성공한 데이터베이스 관리 시스템이었다.\[1\] [미국](https://ko.wikipedia.org/wiki/미국 "wikilink") 애시턴(Ashton)이 개발하였으며, 1979년에 처음 등장하였다. 초기에는 [CP/M](https://ko.wikipedia.org/wiki/CP/M "wikilink")과 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink")용으로 개발되었고, 명령어 사용과 메뉴 사용이 모두 가능하였다. 한국에서는 1990년대에 도스용 [로터스 1-2-3](https://ko.wikipedia.org/wiki/로터스_1-2-3 "wikilink") 등과 더불어 사무용 소프트웨어로 사용되었으며, [완성형](https://ko.wikipedia.org/wiki/완성형 "wikilink") 한글로 한글화되었다.

## 프로그래밍 예

아래의 예는 empl이라는 이름의 직원 테이블을 열어서 하나 이상의 직원을 관리하는 모든 관리자에게 10% 인상을 제공한 다음 이름과 봉급을 출력한다.

``` xbase
 USE empl
 REPLACE ALL salary WITH salary * 1.1 FOR supervisors > 0
 LIST ALL fname, lname, salary TO PRINT
 * (comment: reserved words shown in CAPITALS for illustration purposes)
```

또, dBase는 [문자열 평가를](../Page/Eval.md "wikilink") 구현한 최초의 비즈니스 지향 언어들 가운데 하나이다.

``` xbase
 i = 2
 myMacro = "i + 10"
 i = &myMacro
 * comment: i now has the value 12
```

## 각주

## 외부 링크

  - [현재의 dBASE 제품](http://www.dbase.com/)

  - [dBase 7 파일 포맷](http://www.dbase.com/KnowledgeBase/int/db7_file_fmt.htm)

[분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:1979년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1979년_소프트웨어 "wikilink") [분류:볼랜드 소프트웨어](https://ko.wikipedia.org/wiki/분류:볼랜드_소프트웨어 "wikilink")

1.