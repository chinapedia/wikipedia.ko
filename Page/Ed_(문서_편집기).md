> This article is converted from Wikipedia: [Ed \( \)](https://ko.wikipedia.org/wiki/Ed_\(_\)).


**ed**는 [유닉스](../Page/유닉스.md "wikilink") 운영 체제용 [라인 에디터이다](https://ko.wikipedia.org/wiki/라인_에디터 "wikilink"). 1969년 8월 개발된 유닉스 운영 체제의 첫 부분들 가운데 하나이다.\[1\] [vi](https://ko.wikipedia.org/wiki/vi "wikilink")와 같은 더 복잡한 전체 화면 편집기와 나란히, 유닉스 기반 운영 체제를 위한 [POSIX](../Page/POSIX.md "wikilink")와 [오픈 그룹](../Page/오픈_그룹.md "wikilink") 표준의 일부로 남아있다.\[2\]

## 기능

  - 실직적인 모든 유닉스 시스템에서 이용 가능
  - 명령 모드, 텍스트 모드, 뷰잉 모드를 지원하는 모달 편집기
  - [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 지원
  - 강력한 자동화를 통해 [표준 입력으로부터](https://ko.wikipedia.org/wiki/표준_입력 "wikilink") 명령을 피드(feed)할 수 있음

## 예

ed 세션의 예제이다. 사용자가 입력한 명령어와 텍스트는 보통의 글씨체로 되어있고, ed의 출력물은 **강조** 표시로 되어있다.

`a`
`ed is the standard Unix text editor.`
`This is line number two.`
`.`
`2i`
`  `
`.`
`,l`
**`ed``   ``is``   ``the``   ``standard``   ``Unix``   ``text``   ``editor.$`**
**`$`**
**`This``   ``is``   ``line``   ``number``   ``two.$`**
`3s/two/three/`
`,l`
**`ed``   ``is``   ``the``   ``standard``   ``Unix``   ``text``   ``editor.$`**
**`$`**
**`This``   ``is``   ``line``   ``number``   ``three.$`**
`w text`
**`65`**
`q`

최종 결과는 다음의 문자를 포함하는 단순 텍스트 파일이다:

`ed is the standard Unix text editor.`
`  `
`This is line number three.`

## 같이 보기

  - [vi](https://ko.wikipedia.org/wiki/vi "wikilink"): ex 기반의 시각 전체 화면 편집기

## 각주

## 외부 링크

  - [GNU ed homepage](https://www.gnu.org/software/ed/ed.html)

  -
  -
  - , a direct descendant of the original ed.

[분류:유닉스 문서 편집기](https://ko.wikipedia.org/wiki/분류:유닉스_문서_편집기 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.
2.