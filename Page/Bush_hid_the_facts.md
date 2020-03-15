> This article is converted from Wikipedia: [Bush hid the facts](https://ko.wikipedia.org/wiki/Bush_hid_the_facts).


****(“[부시가](https://ko.wikipedia.org/wiki/조지_W._부시 "wikilink") 사실을 숨겼다”)는 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), 특히 [윈도 2000](https://ko.wikipedia.org/wiki/윈도_2000 "wikilink") 이후에 포함된 [메모장의](https://ko.wikipedia.org/wiki/메모장_\(소프트웨어\) "wikilink") 오류를 흔히 부르는 이름이다. 이 오류는 다음과 같은 방법으로 재현할 수 있다.\[1\]

1.  메모장에 라고 치고 ANSI 인코딩으로 저장한다.

2.  메모장을 닫고, 그 파일을 다시 열어 본다.

3.  대신 알아 볼 수 없는 한자들(이 경우 )로 바뀌어 있을 것이다. (올바른 언어팩이 설치되어 있지 않은 경우 사각형 모양의 도형이 대신 나타난다.)

혹자는 이 오류를 [음모론](https://ko.wikipedia.org/wiki/음모론 "wikilink")으로 보기도 했지만,  말고도 다양한 문자열(예를 들어 )이 이 오류를 일으키기 때문에 설득력이 떨어진다. KBS에서 방영하는 [스펀지에서는](https://ko.wikipedia.org/wiki/스펀지_\(텔레비전\) "wikilink") 방송에서 이 오류를 다루면서, 위 과정에서 나타나는 한자가 ‘사실은 자기가 숨겨도 언젠가는 밝혀진다’라는 의미라고 해석하기도 하였다.

## 오류의 원인

이 오류는 메모장이 내부적으로 사용하는 [윈도 API](https://ko.wikipedia.org/wiki/윈도_API "wikilink") 함수 `IsTextUnicode`가 짧은 문자열에 대해 잘못된 [문자 인코딩을](https://ko.wikipedia.org/wiki/문자_인코딩 "wikilink") 반환해서 생기는 문제이다. 예를 들어서 는 사실 ANSI 인코딩으로 표현된 원래 문자열을 [엔디언](https://ko.wikipedia.org/wiki/리틀_엔디언 "wikilink") 형식으로 저장된 [UTF-16](https://ko.wikipedia.org/wiki/UTF-16 "wikilink") 문자열로 해석해서 나온 문자열이다.

구체적으로 ‘Xxxx xxx xxx xxxxx’ 형식으로 쓰인 여러 영어 문자열이 이 버그에 영향을 받을 수 있다. (하지만 와 같이 이 버그에 영향을 받지 않는 문자열도 있다.) 이 문자열들은 UTF-16으로 해석했을 때 보통 U+6100부터 U+7AFF에 이르는 영역의 문자로 해석되며, 이 문자들은 모두 [한자](https://ko.wikipedia.org/wiki/한자 "wikilink")에 속하기 때문에 알아 볼 수 없는 한자로 보이는 것이다.

[레이먼드 첸은](https://ko.wikipedia.org/wiki/레이먼드_첸 "wikilink") 이 문제에 대해 자신의 블로그에서 [바이트 순서 표식](../Page/바이트_순서_표식.md "wikilink")(BOM)이 없는 경우 UTF-16을 자동으로 선택하지 말 것을 제안했다.\[2\]

### 자세히

메모장이 파일을 ANSI 인코딩으로 제대로 인식하지 못하고 UTF-16 리틀 엔디언으로 인식해서 열었기 때문이다. 이제 Bush hid the facts 글자 각각의 ANSI 값을 알아보자.

  - [공백](https://ko.wikipedia.org/wiki/공백 "wikilink"): 0x20
  - B: 0x42
  - a: 0x61
  - c: 0x63
  - d: 0x64
  - e: 0x65
  - f: 0x66
  - h: 0x68
  - i: 0x69
  - s: 0x73
  - t: 0x74
  - u: 0x75

ANSI 인코딩에선 이 글자들이

  -
    `42 75 73 68 20 68 69 64 20 74 68 65 20 66 61 63 74 73`

으로 저장된다. 그러나 이 글자들은 UTF-16 리틀 엔디언으로

  -
    `75 42 68 73 68 20 64 69 74 20 65 68 66 20 63 61 73 74`

로 바뀐다. 이는

  -
    `75-42 68-73 68-20 64-69 74-20 65-68 66-20 63-61 73-74`

로 두 글자 단위로 묶이며, 결과로

  -
    `U+7542 U+6873 U+6820 U+6469 U+7420 U+6568 U+6620 U+6361 U+7374`를 출력하게 한다. 따라서 출력 결과는 이다. (대문자 B(0x42) 대신 소문자 b(0x62)로 했다면, U+7542  대신 U+7562 가 출력된다.)

## 참고사항

대신 나타난 문자열()을 해석해 보면 다음과 같다.

<table>
<thead>
<tr class="header">
<th></th>
<th><p>땅 갈아 일어난 흙</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>수레 덮개</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>나무가 연하다</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>문지르다</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>귀막이</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>펴다</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>비치다</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>단속하다</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>몽계</p></td>
</tr>
</tbody>
</table>

## 참조

## 외부 링크

  - [Hoax Slayer의 설명](http://www.hoax-slayer.com/bush-hid-the-facts-notepad.html)

[분류:소프트웨어 버그](https://ko.wikipedia.org/wiki/분류:소프트웨어_버그 "wikilink") [분류:문자 인코딩](https://ko.wikipedia.org/wiki/분류:문자_인코딩 "wikilink") [분류:영어 어구](https://ko.wikipedia.org/wiki/분류:영어_어구 "wikilink")

1.  [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") 이후 버전에는 이 버그가 고쳐졌기 때문에 이 버그가 작동하지 않는다.
2.  [The Old New Thing - 메모장 파일 인코딩 문제, redux](http://blogs.msdn.com/oldnewthing/archive/2007/04/17/2158334.aspx)