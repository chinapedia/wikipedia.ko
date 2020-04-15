> This article is converted from Wikipedia: [ASA 캐리지 제어 문자](https://ko.wikipedia.org/wiki/ASA_캐리지_제어_문자).


**ASA 제어 문자**(ASA carriage control characters)는 [라인 프린터를](https://ko.wikipedia.org/wiki/라인_프린터 "wikilink") 통해 용지의 이동을 제어하기 위해 사용되는 단순 인쇄 명령 문자이다. 이 명령들은 출력할 각 문자 줄의 첫 열에 특수 문자로 표현하며, 줄이 인쇄되기 전에 용지가 어떻게 앞당겨지는지에 영향을 미친다.

"ASA"(아사)는 [미국 국립 표준 협회](https://ko.wikipedia.org/wiki/미국_국립_표준_협회 "wikilink")(ANSI)의 과거 명칭인 미국표준협회(American Standards Association)의 준말로, 이 단체는 이러한 제어 문자들을 *ANSI X3.78-1981(R1992) representation of vertical carriage positioning characters in information interchange*로 표준화해오고 있다. 이 문자는 포트란 제어 문자(FORTRAN control characters)라고 하는데, 그 이유는 1960년대 초에 [포트란 II](../Page/포트란.md "wikilink") 버전에 첫 등장하였기 때문이며\[1\] 그 뒤로 [코볼](../Page/코볼.md "wikilink")과 [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink")과 같은 다른 프로그래밍 언어에도 사용되고 있다.

## 동작

<table>
<thead>
<tr class="header">
<th><p>ASA 문자</p></th>
<th><p>동작</p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/ASCII" title="wikilink">ASCII</a>에서의 동일한 동작</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/공백_문자.md" title="wikilink">공백</a></p></td>
<td><p>1줄 앞당김 (싱글 스페이스)</p></td>
<td><p><code>CR </code><a href="https://ko.wikipedia.org/wiki/라인_피드" title="wikilink"><code>LF</code></a></p></td>
</tr>
<tr class="even">
<td><p><code>1</code></p></td>
<td><p>다음 줄로 앞담김 (<a href="https://ko.wikipedia.org/wiki/페이지_브레이크" title="wikilink">폼 피드</a>)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/캐리지_리턴" title="wikilink"><code>CR</code></a><code> </code><a href="https://ko.wikipedia.org/wiki/폼_피드" title="wikilink"><code>FF</code></a></p></td>
</tr>
<tr class="odd">
<td><p>2–9, A, B, C</p></td>
<td><p>다음 탭 스톱으로 앞당김</p></td>
<td><p><code>CR </code><a href="https://ko.wikipedia.org/wiki/Tab_키#탭_문자" title="wikilink"><code>VT</code></a> (대략적)</p></td>
</tr>
<tr class="even">
<td><p><code>0</code></p></td>
<td><p>2줄 앞당김 (더블 스페이스)</p></td>
<td><p><code>CR LF LF</code></p></td>
</tr>
<tr class="odd">
<td><p><code>-</code></p></td>
<td><p>3줄 앞당김 (트리플 스페이스)</p></td>
<td><p><code>CR LF LF LF</code></p></td>
</tr>
<tr class="even">
<td><p><code>+</code></p></td>
<td><p>인쇄하기 전에 어떠한 줄도 앞당기지 않으며,<br />
이전 줄을 현재 줄로 겹쳐찍는다(overstrike)</p></td>
<td><p><code>CR</code></p></td>
</tr>
</tbody>
</table>

ASA 캐리지 제어 문자를 포함한 출력의 예는 다음과 같다:

**`1`**`This is the first line on the page`
**`0`**`This is the third line on the page`
**`-`**`This is the 6th line on the page`
` This is the 7th line on the page`
**`+`**`____    the                      - Overstrike the 7th line`

인쇄된 출력의 예는 다음과 같다:

`This is the first line on the page`

`This is the third line on the page`

`This is the 6th line on the page`
<u>`This`</u>` is `**`the`**` 7th line on the page - Overstrike the 7th line`

## 각주

## 외부 링크

  - More elaborate description at [Felgall Mainframe](https://web.archive.org/web/20160318082528/http://www.felgall.com/asa.htm)

  -
  - First-character forms-control data definition [1](http://publib.boulder.ibm.com/infocenter/iseries/v7r1m0/index.jsp?topic=%2Frzalu%2Frzalufcfcd.htm)

[분류:프린터](https://ko.wikipedia.org/wiki/분류:프린터 "wikilink") [분류:제어 문자](https://ko.wikipedia.org/wiki/분류:제어_문자 "wikilink")

1.