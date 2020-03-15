> This article is converted from Wikipedia: [Split \(\)](https://ko.wikipedia.org/wiki/Split_\(\)).


**`split`**(스플릿)은 하나의 파일을 두 개 이상의 작은 파일들로 분할하는데 주로 사용되는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 유틸리티이다.

## 사용

명령형식은 다음과 같다.

`split 옵션 입력파일명 출력파일명`

`split`은 1000줄까지의 출력파일들을 만들 수 있게 초기 설정되어 있다. 그 파일들은 사용자가 설정한 출력파일명 뒤에 aa,ab,ac 등으로 덧붙여져 이름이 지어진다. 만약 출력파일명이 주어지지 않는다면 초기파일명은 x를 사용하여 xaa,xab 등으로 설정된다. 입력파일명 대신에 하이픈(*-*)이 사용되거나 입력파일명이 없으면, 데이터는 [표준 입력](https://ko.wikipedia.org/wiki/표준_입력 "wikilink")(standard input)에서 얻어진다.

## 옵션

  - `-a수`: 분할되어 저장될 출력파일명의 뒤에 붙을 aa,ab,...,혹은 aaa,aab,... 등의 자릿수를 지정한다. 예컨대 `split -a4 fruits.txt fruits-split.txt`라 하면 fruits-split.txtaaaa로 저장된다.
    `-b수`: 출력파일당 바이트 크기가 지정된다. 여기서 지정되는 바이트 크기에 따라 aa부터 ab,ac,...,순으로 파일을 만들어간다. 512바이트는 b로, 1킬로바이트는 k로, 1메가바이트는 m으로 설정된다.
    `-C수`: 출력파일당 줄들의 바이트 크기를 지정한다. 소문자가 아닌 대문자 C임에 유의하라.
    `-l수`: 출력파일당 줄 수를 지정한다. 다시 말해, 원래의 파일을 여러 줄씩 끊어 저장할 것인지 지정하는 것이다.
    `--help`: 도움말을 보여준다.
    `--version`: 버전 정보를 보여준다.

## 같이 보기

  - [`cat`](../Page/Cat_\(유닉스\).md "wikilink")

## 외부 링크

  -

  -

[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")