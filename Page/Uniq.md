> This article is converted from Wikipedia: [Uniq](https://ko.wikipedia.org/wiki/Uniq).


**`uniq`**(유니크)는 텍스트 파일 내에 중복된 내용의 행이 연속으로 있으면 중복 없이 하나의 행으로 만들어 주는 [유닉스](../Page/유닉스.md "wikilink") 유틸리티이다. **`uniq`**는 일종의 [필터 프로그램](https://ko.wikipedia.org/wiki/필터_프로그램 "wikilink")(filter program)으로 보통 [`sort`](https://ko.wikipedia.org/wiki/sort "wikilink")뒤에 덧붙여 사용된다. 또한 `-d`옵션을 적용하여 중복되는 행만을 볼 수 있거나, `-c`옵션을 적용하여 중복행의 중복횟수를 출력할 수 있다.

## 예시

한 예로 어떤 파일에 중복되는 내용의 행을 정렬하고 중복횟수를 세어 오름차순 정리한다면,

`$ sort file | `**`uniq`**` -c | sort -n`

위와 같이 적용하면 된다. [셸 스크립트에서](../Page/셸_스크립트.md "wikilink") [파이프라인을](https://ko.wikipedia.org/wiki/파이프라인_\(소프트웨어\) "wikilink") 삽입하여 **`uniq`**를 [`sort`](https://ko.wikipedia.org/wiki/sort "wikilink")와 함께 실행하는 것이다. 여기서 주의해야 할 점은 **`uniq`**는 파일 내용이 미리 정렬되어 있는 상태에서 실행할 수 있다.

`$ `[`cat`](https://ko.wikipedia.org/wiki/cat_\(유닉스\) "wikilink")` fruits.txt`
`orange`
`apple`
`apple`
`orange`
`orange`
`apple`

`$ `**`uniq`**` -c fruits.txt`
`1 orange`
`2 apple`
`2 orange`
`1 apple`

정렬이 이루어지지 않은 상태에서 **`uniq`**를 적용하였기에 위와 같은 결과를 얻을 수 있다.

`$ sort -u fruits.txt`
`apple`
`orange`

이것은 파일내용을 정렬시켜 중복되는 것을 하나로 표현하는 것이다. 결론적으로 **`uniq`**는 파일에 전체적으로 분산된 중복을 한번에 잡아내지 못한다. 따라서 정렬하여 순차적으로 만든 뒤에 적용한다.

## 옵션

<table>
<tbody>
<tr class="odd">
<td><p><code>$ </code><strong><code>uniq</code></strong><code> -u fruits.txt</code><br />
<code>orange</code><br />
<code>apple</code></p></td>
</tr>
</tbody>
</table>

  - \-u: 원래 파일에서 연속으로 중복되지 않는 행만을 출력한다.
    \-d: 원래 파일에서 연속으로 중복되는 행들을 출력한다. 즉, -u 옵션과는 반대로 연속으로 중복된 내용을 지닌 줄만을 한 번씩 보여준다.
    \-c: 중복발생횟수를 연속 중복 행과 함께 보여준다. -c 옵션이 적용되면 앞에 -u나 -d 옵션이 적용되었더라도 그들은 무시된다.
    \-i: 행들을 비교할때 대소문자 구별을 하지 않는다.
    \-s수: 한행에서 지정된 수만큼의 문자를 비교대상에서 제외한다.
    \-f수: 맨 앞에서부터 지정된 수 만큼의 필드를 비교대상에서 제외한다.
    \-w수: 비교대상 문자 수를 지정한다.
    \--help: 각종 옵션에 대한 설명과 도움말을 볼 수 있다.
    \--version: uniq의 버전 번호를 보여준다.

## 함께 보기

  - [유닉스 프로그램 목록](https://ko.wikipedia.org/wiki/유닉스_프로그램_목록 "wikilink")

## 외부 링크

  - [uniq's](http://www.linuxmanpages.com/man1/uniq.1.php) [리눅스](../Page/리눅스.md "wikilink") [맨페이지](https://ko.wikipedia.org/wiki/man_page "wikilink")(man page)
  - [SourceForge UnxUtils – Port of the most important GNU utilities to Windows](http://sourceforge.net/projects/unxutils/)

[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")