> This article is converted from Wikipedia: [Strings \(유닉스\)](https://ko.wikipedia.org/wiki/Strings_\(유닉스\)).


**strings**는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제에서](../Page/운영_체제.md "wikilink") 실행 파일 같은 [바이너리 파일에](https://ko.wikipedia.org/wiki/바이너리_파일 "wikilink") 삽입된 텍스트 [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")들을 찾고 보여주는 프로그램이다. 이것은 [목적 파일과](../Page/목적_파일.md "wikilink") [코어 덤프에서도](../Page/코어_덤프.md "wikilink") 사용될 수 있다.

문자열들은 출력 가능하고 NULL 문자로 끝나는 최소 4(기본적으로)개의 문자열들을 찾음으로써 인식된다. 몇몇 구현들은 출력 문자로서 무엇을 인식할지를 결정하는 옵션을 제공하는데 이것은 비 ASCII 그리고 확장 문자 텍스트를 찾는데 유용하다.

일반적인 사용은 이것의 출력을 [`grep`](https://ko.wikipedia.org/wiki/grep "wikilink")에`  파이핑하고  `출력을 파일로 보내는 것이다.\[1\]

이것은 [GNU 바이너리 유틸리티](../Page/GNU_바이너리_유틸리티.md "wikilink") (binutils)의 한 부분으로서 [마이크로소프트 윈도우를](../Page/마이크로소프트_윈도우.md "wikilink") 포함한 다른 운영 체제들에 포트되었다.\[2\]

## 예시

*strings*를 최소 8 문자 길이의 문자열을 프린트하는데 사용한다(이 명령어는 시스템의 [BIOS](../Page/바이오스.md "wikilink") 정보를 출력하므로 root로 실행되어야 한다):

``` bash
dd if=/dev/mem bs=1k skip=768 count=256 2>/dev/null | strings -n 8 | less
```

## 같이 보기

  - [`cat`](../Page/Cat_\(유닉스\).md "wikilink")
  - [GNU 디버거](../Page/GNU_디버거.md "wikilink")
  - [`strip`](https://ko.wikipedia.org/wiki/strip "wikilink")

## 각주

## 외부 링크

  -
[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:문자열](https://ko.wikipedia.org/wiki/분류:문자열 "wikilink")

1.
2.  [시그윈](../Page/시그윈.md "wikilink")