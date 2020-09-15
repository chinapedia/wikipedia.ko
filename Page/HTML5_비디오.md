> This article is converted from Wikipedia: [HTML5 비디오](https://ko.wikipedia.org/wiki/HTML5_비디오).


**HTML5 비디오**(HTML5 video) 태그는 [HTML5](../Page/HTML5.md "wikilink") 초안 규격에서 소개된 마크업 언어 태그로 HTML 페이지의 동영상을 임베드(embed)하는 것을 지원해 준다. [2010년](../Page/2010년.md "wikilink") 4월, [어도비 플래시 플레이어는](../Page/어도비_플래시_플레이어.md "wikilink") [유튜브](../Page/유튜브.md "wikilink")와 같은 웹사이트에서 동영상을 포함하는데 널리 사용된다. 이것은 애플의 [아이폰](../Page/아이폰.md "wikilink")이나 [아이패드](../Page/아이패드.md "wikilink")와 같은 특정 브라우저를 제외하고는 대다수의 웹 브라우저에 [어도비 플래시 플레이어가](../Page/어도비_플래시_플레이어.md "wikilink") 설치되어 있기 때문이다. HTML5 동영상은 동영상 온라인을 보여주기 위한 새로운 표준 방식이 될 예정이었지만, 어떤 동영상 포맷이 동영상 태그에서 지원될 것인지 하는 것에 대한 합의 부족으로 방해를 받아왔다.

## 예제

아래의 HTML5 코드는 [WebM](../Page/WebM.md "wikilink") 비디오를 웹 페이지에 포함한다.

``` html5
<video src="movie.webm" controls>
브라우저가 비디오 태그를 지원하지 않으면 이 문자열이 나타납니다.
</video>
```

### 복수 소스

``` html5
<video poster="movie.jpg" controls>
    <syntaxhighlight src="movie.webm" type='video/webm; codecs="vp8.0, vorbis"' />
    <syntaxhighlight src="movie.ogv" type='video/ogg; codecs="theora, vorbis"' />
    <syntaxhighlight src="movie.mp4" type='video/mp4; codecs="avc1.4D401E, mp4a.40.2"' />
    <p>브라우저가 비디오 태그를 지원하지 않으면 이 문자열이 나타납니다.</p>
</video>
```

## 지원 브라우저

현재의 HTML5 초안 규격에는 동영상 태그에서 어떤 동영상 포맷을 브라우저가 지원해야 할 것인지를 명시해 두지 않았다. 따라서 브라우저는 그들이 적합하다고 생각되는 동영상 포맷을 마음대로 지원할 수 있다.

### 기본 동영상 포맷 논쟁

브라우저가 지원할 동영상 포맷을 적어도 하나는 명시하는 것이 바람직하다. 이러한 이상적인 동영상 포맷은 다음을 만족하여야 한다.

  - 고효율의 압축률과 고화질을 가지고 있고, 낮은 디코드 과정을 사용할 것.
  - 로열티가 없을 것.
  - 그 포맷을 지원하는 소프트웨어 디코더, 하드웨어 동영상 디코더가 존재할 것.

처음에는 Ogg Theora가 HTML5에서 추천하는 표준 동영상 포맷이었다. 특허에 영향을 받지 않았기 때문이었다. 그러나 [2007년](../Page/2007년.md "wikilink") [12월 10일](../Page/12월_10일.md "wikilink") HTML5 규격이 업데이트되었을 때, 포맷을 구체화하기 위해 참고사항이 갱신되었다.

<table>
<thead>
<tr class="header">
<th><p>브라우저</p></th>
<th><p>최신 안정판 (공개일)</p></th>
<th><p>동영상 포맷</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Ogg.md" title="wikilink">Ogg</a> <a href="../Page/테오라.md" title="wikilink">Theora</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/H.264/AVC" title="wikilink">H.264/MPEG-4 AVC</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/VP8" title="wikilink">VP8</a> (<a href="../Page/WebM.md" title="wikilink">WebM</a>)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/인터넷_익스플로러.md" title="wikilink">인터넷 익스플로러</a></p></td>
<td></td>
<td><p>수동 설치</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/파이어폭스" title="wikilink">파이어폭스</a></p></td>
<td></td>
<td><p>[1]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/구글_크롬" title="wikilink">구글 크롬</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/사파리_(웹_브라우저).md" title="wikilink">사파리</a></p></td>
<td></td>
<td><p>수동 설치</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/오페라_(웹_브라우저).md" title="wikilink">오페라</a></p></td>
<td></td>
<td><p>[2]</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/캉커러.md" title="wikilink">캉커러</a></p></td>
<td></td>
<td><p>[3]</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/웹_(웹_브라우저).md" title="wikilink">웹</a></p></td>
<td></td>
<td><p><ref name="epiphany">{{웹 인용</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/오리진_웹_브라우저" title="wikilink">오리진</a></p></td>
<td><p><a href="../Page/모르프OS.md" title="wikilink">모르프OS</a>용 1.9<br />
()</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [HTML5](../Page/HTML5.md "wikilink")

## 각주

## 외부 링크

  - [동영상 요소](https://html.spec.whatwg.org/multipage/media.html)
  - [HTML5 동영상 소개](http://dev.opera.com/articles/view/introduction-html5-video/)
  - [HTML5 동영상과 음성에 대해 알아야 할 모든 것](https://web.archive.org/web/20100307033247/http://my.opera.com/core/blog/2010/03/03/everything-you-need-to-know-about-html5-video-and-audio-2)
  - [자바스크립트 HTML5 동영상 Wrapper (GPL)](http://www.projekktor.com)
  - [jQuery HTML5 동영상 플레이어 (GPL)](http://www.mediafront.org/project/osmplayer)

[분류:HTML](https://ko.wikipedia.org/wiki/분류:HTML "wikilink") [분류:HTML5](https://ko.wikipedia.org/wiki/분류:HTML5 "wikilink")

1.  [Mozilla Firefox 3.5 Release Notes](http://www.mozilla.com/en-US/firefox/3.5/releasenotes/)
2.
3.