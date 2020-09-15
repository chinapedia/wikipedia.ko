> This article is converted from Wikipedia: [LaTeX](https://ko.wikipedia.org/wiki/LaTeX).


\\\!\\\!\\\!\\\!\\\!\\;\\; T\\\!_{\\displaystyle E} \\\! X} \\, 2_{\\displaystyle \\varepsilon}</math> |최근 버전 출시일 = |미리보기 버전 = |미리보기 버전 출시일 = |운영체제 = | 플랫폼 = |종류 = |라이선스 = |웹사이트 = [LaTeX Project](http://www.latex-project.org/) }}

**LaTeX**( <small>또는</small> )은 문서 조판에 사용되는 프로그램이다. [도널드 커누스가](https://ko.wikipedia.org/wiki/도널드_커누스 "wikilink") 만든 [TeX](../Page/TeX.md "wikilink")을 쉽게 사용하기 위하여 [1984년](../Page/1984년.md "wikilink")에 [레슬리 램포트가](../Page/레슬리_램포트.md "wikilink") 만든 매크로이다. TeX을 직접 사용하기는 어렵기 때문에, 오늘날에는 LaTeX을 이용하여 문서를 만드는 경우가 많다.

[섬네일](https://ko.wikipedia.org/wiki/파일:LaTeX_diagram.svg "wikilink")

## 버전

LaTeX 소프트웨어는 LaTeX Project Public License(LPPL)로 제공되는 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink"). 현재, [OS X과](https://ko.wikipedia.org/wiki/OS_X "wikilink") [솔라리스](../Page/솔라리스_\(운영_체제\).md "wikilink") 등의 [유닉스](../Page/유닉스.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink")와 [BSD](../Page/BSD.md "wikilink") 계열 OS 등의 UNIX 호환 OS, [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink") 등 다양한 OS에서 사용할 수 있다. 현재 최신 버전은 1993년 발표된 LaTeX2e이다. 구버전인 LaTeX 2.09을 사용하는 경우에는 LaTeX2e로 업데이트하는 것이 좋다.

## 로고

LaTeX2e 공식 로고는  \(2_{\displaystyle \varepsilon}\)와 같이 표기하고, 이 같은 표기가 불가능한 [텍스트](https://ko.wikipedia.org/wiki/텍스트 "wikilink") 또는 [전자 우편의](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 경우에는 "LaTeX2e" 또는 "LaTeX 2e"로 표기하도록 되어 있다.

## 입출력 예시

아래는 LaTeX 입력의 예이다. 이 입력은 오른쪽 그림처럼 출력된다.

<table>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode latex"><code class="sourceCode latex"><span id="cb1-1"><a href="#cb1-1"></a><span class="bu">\documentclass</span>[12pt]{<span class="ex">article</span>}</span>
<span id="cb1-2"><a href="#cb1-2"></a><span class="bu">\usepackage</span>{<span class="ex">amsmath</span>}</span>
<span id="cb1-3"><a href="#cb1-3"></a><span class="fu">\title</span>{<span class="fu">\LaTeX</span>}</span>
<span id="cb1-4"><a href="#cb1-4"></a><span class="fu">\date</span>{}</span>
<span id="cb1-5"><a href="#cb1-5"></a><span class="kw">\begin</span>{<span class="ex">document</span>}</span>
<span id="cb1-6"><a href="#cb1-6"></a>  <span class="fu">\maketitle</span></span>
<span id="cb1-7"><a href="#cb1-7"></a>  <span class="fu">\LaTeX</span>{} is a document preparation system for the <span class="fu">\TeX</span>{}</span>
<span id="cb1-8"><a href="#cb1-8"></a>  typesetting program. It offers programmable desktop publishing</span>
<span id="cb1-9"><a href="#cb1-9"></a>  features and extensive facilities for automating most aspects of</span>
<span id="cb1-10"><a href="#cb1-10"></a>  typesetting and desktop publishing, including numbering and</span>
<span id="cb1-11"><a href="#cb1-11"></a>  cross-referencing, tables and figures, page layout, bibliographies,</span>
<span id="cb1-12"><a href="#cb1-12"></a>  and much more. <span class="fu">\LaTeX</span>{} was originally written in 1984 by Leslie</span>
<span id="cb1-13"><a href="#cb1-13"></a>  Lamport and has become the dominant method for using <span class="fu">\TeX</span>; few</span>
<span id="cb1-14"><a href="#cb1-14"></a>  people write in plain <span class="fu">\TeX</span>{} anymore. The current version is</span>
<span id="cb1-15"><a href="#cb1-15"></a>  <span class="fu">\LaTeX</span>2e.</span>
<span id="cb1-16"><a href="#cb1-16"></a></span>
<span id="cb1-17"><a href="#cb1-17"></a>  <span class="co">% This is a comment; it will not be shown in the final output.</span></span>
<span id="cb1-18"><a href="#cb1-18"></a>  <span class="co">% The following shows a little of the typesetting power of LaTeX:</span></span>
<span id="cb1-19"><a href="#cb1-19"></a>  <span class="kw">\begin</span>{<span class="ex">align</span>}</span>
<span id="cb1-20"><a href="#cb1-20"></a><span class="ss">    E &amp;= mc^2                              </span><span class="sc">\\</span></span>
<span id="cb1-21"><a href="#cb1-21"></a><span class="ss">    m &amp;= </span><span class="sc">\frac</span><span class="ss">{m_0}{</span><span class="sc">\sqrt</span><span class="ss">{1-</span><span class="sc">\frac</span><span class="ss">{v^2}{c^2}}}</span></span>
<span id="cb1-22"><a href="#cb1-22"></a><span class="ss">  </span><span class="kw">\end</span>{<span class="ex">align</span>}</span>
<span id="cb1-23"><a href="#cb1-23"></a><span class="kw">\end</span>{<span class="ex">document</span>}</span></code></pre></div></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:LaTeX_Output.svg" title="wikilink">425px</a></p></td>
</tr>
</tbody>
</table>

## 한글 조판

``` latex numberLines
\usepackage[T1]{fontenc}
\usepackage{CJKutf8}
\usepackage[english]{babel}

\begin{document}
\begin{CJK}{UTF8}{mj}
안녕하세요?
\end{CJK}
\end{document}
```

위의 코드로도 한글을 조판할 수 있으며 이보다 더 다양한 방법들은 [KTUG Wiki](https://web.archive.org/web/20191227101734/http://wiki.ktug.org/wiki/wiki.php/%ED%95%9C%EA%B8%80LaTeX%ED%8C%A8%ED%82%A4%EC%A7%80)에서 확인할 수 있다.

## 같이 보기

  - [닥북](https://ko.wikipedia.org/wiki/닥북 "wikilink")(DocBook)
  - [BibTeX](http://www.bibtex.org/)
  - [TeX](../Page/TeX.md "wikilink")
  - [MikTeX](https://ko.wikipedia.org/wiki/MikTeX "wikilink")
  - [Lyx](http://www.lyx.org/)
  - [수식 편집기](../Page/수식_편집기.md "wikilink")
  - [ShareLaTex](https://web.archive.org/web/20200619001932/https://www.sharelatex.com/)

## 외부 링크

  - [한글 TeX 사용자 모임](https://web.archive.org/web/20130604184548/http://ktug.org/) 한글 LaTeX 설치에서 활용에 관한 자세한 설명을 볼 수 있으며, 한글 TeX 환경 개발은 물론, 문답 게시판 및 개발[위키](../Page/위키.md "wikilink")를 통해 활발하게 운영되고 있다.
  - [LaTeX 프로젝트 홈페이지](http://www.latex-project.org/)
  - [BibTeX](http://www.bibtex.org/)

[분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:페이지 기술 언어](https://ko.wikipedia.org/wiki/분류:페이지_기술_언어 "wikilink") [분류:TeX](https://ko.wikipedia.org/wiki/분류:TeX "wikilink") [분류:1984년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1984년_소프트웨어 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink") [분류:자유 문서 편집기](https://ko.wikipedia.org/wiki/분류:자유_문서_편집기 "wikilink")