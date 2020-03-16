> This article is converted from Wikipedia: [BBCode](https://ko.wikipedia.org/wiki/BBCode).


**BBCode** 또는 **불리틴 보드 코드**(Bulletin Board Code, [전자 게시판](../Page/전자_게시판.md "wikilink") 부호)는 [전자 게시판에](../Page/전자_게시판.md "wikilink") 글을 작성하는데 쓰이는 [가벼운 마크업 언어이다](https://ko.wikipedia.org/wiki/가벼운_마크업_언어 "wikilink"). BBCode는 [HTML](../Page/HTML.md "wikilink")과 거의 같은 역할을 하며 이들의 문법도 유사하다. 다만, BBCode는 [대괄호](https://ko.wikipedia.org/wiki/대괄호 "wikilink")를 사용하여 태그를 나타낸다.

## 역사

BBCode는 1998년 Ultimate Bulletin Board(UBB)라는 [전자 게시판](../Page/전자_게시판.md "wikilink") 프로그램에 처음 도입되었다. 그래서 BBCode를 UBBCode라고 부르기도 한다.

## 목적

많은 [전자 게시판](../Page/전자_게시판.md "wikilink") 프로그램이 사용자에게 [HTML](../Page/HTML.md "wikilink")로 글을 작성하게 하고 있다. 이는 [HTML](../Page/HTML.md "wikilink")의 특성상의 한계로 인해 [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink") 등의 보안 문제가 생기게 한다. 또 [HTML](../Page/HTML.md "wikilink")의 문법이 난해하기 때문에 [HTML](../Page/HTML.md "wikilink")을 처리하는 프로그램을 만들기 쉽지 않다. 이에 [HTML](../Page/HTML.md "wikilink")과 유사하지만 [HTML](../Page/HTML.md "wikilink")의 단점을 해결한 BBCode를 도입하여 [HTML](../Page/HTML.md "wikilink")을 대체함으로써 이 문제를 해결하였다.

## BBCode 태그

다음은 기본적으로 사용되는 BBCode 태그들의 목록이다. 이 태그들은 [전자 게시판마다](../Page/전자_게시판.md "wikilink") 조금씩 다를 수 있다.

<table>
<tbody>
<tr class="odd">
<td><p><strong>BBCode</strong></p></td>
<td><p><strong>HTML</strong></p></td>
<td><p><strong>효과</strong></p></td>
</tr>
<tr class="even">
<td><p><code>[b]굵은 글씨[/b]</code></p></td>
<td><p><code>&lt;b&gt;굵은 글씨&lt;/b&gt;</code></p></td>
<td><p><strong>굵은 글씨</strong></p></td>
</tr>
<tr class="odd">
<td><p><code>[i]기울임 글씨[/i]</code></p></td>
<td><p><code>&lt;i&gt;기울임 글씨&lt;/i&gt;</code></p></td>
<td><p><em>기울임 글씨</em></p></td>
</tr>
<tr class="even">
<td><p><code>[u]밑줄 글씨[/u]</code></p></td>
<td><p><code>&lt;u&gt;밑줄 글씨&lt;/u&gt;</code></p></td>
<td><p><span style="text-decoration:underline;">밑줄 글씨</span></p></td>
</tr>
<tr class="odd">
<td><p><code>[s]가로줄 글씨[/s]</code></p></td>
<td><p><code>&lt;s&gt;가로줄 글씨&lt;/s&gt;</code></p></td>
<td><p><s>가로줄 글씨</s></p></td>
</tr>
<tr class="even">
<td><p><code>[url]https://ko.wikipedia.org[/url]</code></p></td>
<td><p><code>&lt;a href="https://ko.wikipedia.org"&gt;https://ko.wikipedia.org&lt;/a&gt;</code></p></td>
<td><p><span class="plainlinks"><a href="https://ko.wikipedia.org"><a href="https://ko.wikipedia.org">https://ko.wikipedia.org</a></a></span></p></td>
</tr>
<tr class="odd">
<td><p><code>[url=https://ko.wikipedia.org]위키백과[/url]</code></p></td>
<td><p><code>&lt;a href="https://ko.wikipedia.org"&gt;위키백과&lt;/a&gt;</code></p></td>
<td><p><span class="plainlinks"><a href="https://ko.wikipedia.org">위키백과</a></span></p></td>
</tr>
<tr class="even">
<td><p><code>[img]http://exmple.com/Go-home.svg.png[/img]</code></p></td>
<td><p><code>&lt;img src="http://exmple.com/Go-home.svg.png" alt="" /&gt;</code></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Go-home.svg" title="wikilink">파일:Go-home.svg</a></p></td>
</tr>
<tr class="odd">
<td><p><code>[quote]인용 텍스트[/quote]</code></p></td>
<td><p><code>&lt;blockquote&gt;&lt;p&gt;인용 텍스트&lt;/p&gt;&lt;/blockquote&gt;</code><br />
</p></td>
<td><p>To quote:</p>
<blockquote>
<p>인용 텍스트</p>
</blockquote>
<p>[1]</p></td>
</tr>
<tr class="even">
<td><p><code>[code]코드 텍스트[/code]</code></p></td>
<td><p><code>&lt;pre&gt;코드 텍스트&lt;/pre&gt;</code></p></td>
<td><p><code>코드 텍스트</code></p></td>
</tr>
<tr class="odd">
<td><p><code>[size=15]큰 글씨[/size]</code>[2]</p></td>
<td><p><code>&lt;span style="font-size:15px"&gt;큰 글씨&lt;/span&gt;</code></p></td>
<td><p><span style="font-size:xx-large;">큰 글씨</span></p></td>
</tr>
<tr class="even">
<td><p><code>[color=red]붉은 글씨[/color]</code><br />
<small>또는</small><br />
<code>[color=#FF0000]붉은 글씨[/color]</code><br />
<small>또는</small><br />
<code>[color=FF0000]붉은 글씨[/color]</code><br />
[3]</p></td>
<td><p><code>&lt;span style="color:#FF0000;"&gt;붉은 글씨&lt;/span&gt;</code></p></td>
<td><p><span style="color:#FF0000;">붉은 글씨</span></p></td>
</tr>
<tr class="odd">
<td><p><code>[list]</code> <code>[*]목록 1</code> <code>[*]목록 2</code> <code>[/list]</code></p></td>
<td><p><code>&lt;ul&gt;&lt;li&gt;목록 1&lt;/li&gt;&lt;li&gt;목록 2&lt;/li&gt;&lt;/ul&gt;</code></p></td>
<td><ul>
<li>목록 1</li>
<li>목록 2</li>
</ul></td>
</tr>
<tr class="even">
<td><p><code>[table]</code> <code>[tr]</code> <code>[td]테이블 데이터[/td]</code> <code>[/tr]</code> <code>[/table]</code>[4]</p></td>
<td><p><code>&lt;table&gt;&lt;tr&gt;&lt;td&gt;테이블 데이터&lt;/td&gt;&lt;/tr&gt;&lt;/table&gt;</code></p></td>
<td><table>
<tbody>
<tr class="odd">
<td><p>| 테이블 데이터</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

어떤 [전자 게시판은](../Page/전자_게시판.md "wikilink") 추가적인 태그들을 지원하기도 한다.

대부분의 [전자 게시판은](../Page/전자_게시판.md "wikilink") BBCode 사용법에 관한 도움말을 사용자에게 보여준다. 또한 BBCode 태그를 직접 만들어 사용할 수 있는 기능을 제공하기도 한다.

## 같이 보기

  - [전자 게시판](../Page/전자_게시판.md "wikilink")
  - [마크업 언어](../Page/마크업_언어.md "wikilink")
  - [가벼운 마크업 언어](https://ko.wikipedia.org/wiki/가벼운_마크업_언어 "wikilink")
  - [HTML](../Page/HTML.md "wikilink")
  - [Markdown](https://ko.wikipedia.org/wiki/Markdown "wikilink")
  - [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink")
  - [CSRF](https://ko.wikipedia.org/wiki/CSRF "wikilink")
  - [phpBB](https://ko.wikipedia.org/wiki/phpBB "wikilink")

## 각주

## 외부 링크

  - [BBCode.org](http://www.bbcode.org/)

[분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink")

1.  일반적으로 이것보다 더욱 좋게 보인다.
2.  size의 단위는 전자 게시판 프로그램마다 다를 수 있다.
3.  일반적으로 HTML 색상명과 \#AABBCC 꼴이 모두 지원된다.
4.  거의 사용되지 않음