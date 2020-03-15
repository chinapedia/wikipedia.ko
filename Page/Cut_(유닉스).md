> This article is converted from Wikipedia: [Cut \(\)](https://ko.wikipedia.org/wiki/Cut_\(\)).


**cut**은 [유닉스 계열에](../Page/유닉스_계열.md "wikilink") 있는 프로그램으로, [텍스트 파일의](../Page/텍스트_파일.md "wikilink") 각 줄에서 특정 부분을 자르는 데에 사용한다.

## 예제

다음과 같은 텍스트 파일이 있을 때:

`foo`<u>**`:bar:ba`**</u>`z:qux:quux`
`one`<u>**`:two:th`**</u>`ree:four:five:six:seven`
`alp`<u>**`ha:beta`**</u>`:gamma:delta:epsilon:zeta:eta:teta:iota:kappa:lambda:mu`

각 문장의 4번째부터 10번째 글자만 얻고 싶다면 다음과 같이 실행하면 된다.

``` bash
 $ cut -c 4-10 file
```

이때 출력은 다음과 같다.

`:bar:ba`
`:two:th`
`ha:beta`

문장 일부분의 발췌는 일반적으로 구획문자(`-d` — 디폴트에 의한 [탭 문자](https://ko.wikipedia.org/wiki/탭_문자 "wikilink"))에 의해서 구분된 [바이트](https://ko.wikipedia.org/wiki/바이트 "wikilink")들 (`-b`), [단어](https://ko.wikipedia.org/wiki/단어 "wikilink")들(`-c`)이나 파일들(`-f`)로 된다. 범위는 `N`, `N-M,` `N-` (`N`에서 문장 끝까지)나 `-M` (문장 시작에서 `M`까지) 중 하나로 구성된 각각의 경우에 따라서 정해진다.

필드 구획문자로서 [콜론 문자를](https://ko.wikipedia.org/wiki/콜론_문자 "wikilink") 사용하면서 5번째 필드부터 각 문장의 마지막까지 출력하기 위해서는:

``` bash
 $ cut -d ":" -f 5- file
```

이는 다음과 같이 출력된다:

`quux`
`five:six:seven`
`epsilon:zeta:eta:teta:iota:kappa:lambda:mu`

## 구문

` cut [-b] [-c] [-f list] [-n] [-d delim] [-s] [file]`

사용될지도 모르는 플래그들은 다음과 같다

  - \-b : Bytes; -b를 따르는 리스트는 리턴될 [바이트](https://ko.wikipedia.org/wiki/바이트 "wikilink")들에 의한 범위를 지정한다. 예를 들어 cut -b1-66은 문장의 최초 66 바이트들을 리턴한다. 만약 -n과 함께 사용될 경우, 어떠한 [멀티-바이트](https://ko.wikipedia.org/wiki/멀티-바이트 "wikilink") 문자들도 쪼개질 수 없음을 주의하라. -bsms 1023 바이트보다 더 적은 입력어에서만 사용 가능하다는 것도 주의하라.
    \-c : Characters; -c를 따르는 리스트는 리턴될 문자들의 범위를 지정한다. 예를 들어서 cut -c1-66은 문장의 최초 66 문자들의 리턴한다.
    \-f : [구획 문자에](https://ko.wikipedia.org/wiki/구획_문자 "wikilink") 의해 구분된 필드 리스트를 지정한다.
    list : 정수로 표시된 필드들의 콤마로 구분된 혹은 공백으로 구분된 리스트, 점진적으로 명령된다. - 표시는 필드들의 범위 포괄을 허용하기 위한 약기로서 제공된다. 예를 들어서 *4-6*은 범위 4-6를, *5-*는 필드 5부터 끝까지를 나타내기 위한 약기로 사용된다.
    \-n : [멀티-바이트 문자들의](https://ko.wikipedia.org/wiki/멀티-바이트_문자 "wikilink") 구분을 진압하기 위해서 -b와 함께 사용된다.
    \-d : Delimiter; -d 옵션을 즉시 따르는 문자는 -f 옵션과 함께 사용되기 위한 필드 구획문자이다; 그 디폴트 구획문자는 *탭*이다. 사용되고 있는 스페이스와 [셸](https://ko.wikipedia.org/wiki/셸 "wikilink")의 문맥 안에서 특별한 의미들을 지닌 다른 문자들은 반드시 인용부호를 달거나 필요에 따라 에스케이프 되어야 한다.
    \-s : -f가 지정되었을 때 어떠한 필드 구획 문자도 포함하지 않은 문장들은 명시되어 있지 않는한 우회한다.
    file : 파일을 (그리고 필요하다면 동반되는 경로) 입력어로서 처리한다. 만약 어떠한 파일도 지정되지 않았다면 [표준 입력어가](https://ko.wikipedia.org/wiki/표준_입력어 "wikilink") 사용된다.

## 함께 보기

  - [grep](https://ko.wikipedia.org/wiki/grep "wikilink")
  - [paste](https://ko.wikipedia.org/wiki/paste_\(유닉스\) "wikilink")
  - [awk](https://ko.wikipedia.org/wiki/awk "wikilink")

## 외부 링크

  - [*cut* manual page: 파일들의 각 문장으로부터 부분을 제거한다](http://linux.die.net/man/1/cut).

[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")