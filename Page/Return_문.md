> This article is converted from Wikipedia: [Return ](https://ko.wikipedia.org/wiki/Return_).


[컴퓨터 프로그래밍에서](../Page/컴퓨터_프로그래밍.md "wikilink") **return 문**은 현재의 [함수에서](../Page/함수_\(프로그래밍\).md "wikilink") 값이나 주소를 반환할 때 사용한다.

## 문법

<table>
<thead>
<tr class="header">
<th><p>언어</p></th>
<th><p>Return 문</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/에이다" title="wikilink">에이다</a>, <a href="../Page/배시_(유닉스_셸).md" title="wikilink">Bash</a>,[1] <a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C</a>, <a href="https://ko.wikipedia.org/wiki/C++" title="wikilink">C++</a>, <a href="../Page/자바_(프로그래밍_언어).md" title="wikilink">자바</a>, <a href="../Page/PHP.md" title="wikilink">PHP</a>, <a href="../Page/C_샤프.md" title="wikilink">C#</a>, <a href="../Page/자바스크립트.md" title="wikilink">자바스크립트</a>, <a href="../Page/D_(프로그래밍_언어).md" title="wikilink">D</a></p></td>
<td><div class="sourceCode" id="cb1"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb1-1"><a href="#cb1-1"></a><span class="cf">return</span> value;</span></code></pre></div></td>
</tr>
<tr class="even">
<td><p><a href="../Page/베이직.md" title="wikilink">베이직</a></p></td>
<td><pre class="qbasic"><code>RETURN</code></pre></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/리스프.md" title="wikilink">리스프</a></p></td>
<td><div class="sourceCode" id="cb3"><pre class="sourceCode lisp"><code class="sourceCode commonlisp"><span id="cb3-1"><a href="#cb3-1"></a>(<span class="kw">return</span> value)</span></code></pre></div></td>
</tr>
<tr class="even">
<td><p><a href="../Page/펄.md" title="wikilink">펄</a>, <a href="../Page/루비_(프로그래밍_언어).md" title="wikilink">루비</a></p></td>
<td><div class="sourceCode" id="cb4"><pre class="sourceCode perl"><code class="sourceCode perl"><span id="cb4-1"><a href="#cb4-1"></a><span class="kw">return</span> <span class="dt">@values</span>;</span>
<span id="cb4-2"><a href="#cb4-2"></a><span class="kw">return</span> <span class="dt">$value</span>;</span>
<span id="cb4-3"><a href="#cb4-3"></a><span class="kw">return</span>;</span></code></pre></div>
<p>또는 컨텍스트 반환 시퀀스</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/파이썬.md" title="wikilink">파이썬</a></p></td>
<td><div class="sourceCode" id="cb5"><pre class="sourceCode python"><code class="sourceCode python"><span id="cb5-1"><a href="#cb5-1"></a><span class="cf">return</span> value</span></code></pre></div></td>
</tr>
<tr class="even">
<td><p><a href="../Page/스몰토크.md" title="wikilink">스몰토크</a></p></td>
<td><pre class="smalltalk"><code>^ value</code></pre></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/비주얼_베이직_닷넷.md" title="wikilink">비주얼 베이직 닷넷</a></p></td>
<td><pre class="vbnet"><code>Return value</code></pre></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도우_파워셸" title="wikilink">윈도우 파워셸</a></p></td>
<td><div class="sourceCode" id="cb8"><pre class="sourceCode c"><code class="sourceCode c"><span id="cb8-1"><a href="#cb8-1"></a><span class="cf">return</span> value;</span></code></pre></div></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/x86_어셈블리" title="wikilink">x86 어셈블리</a></p></td>
<td><div class="sourceCode" id="cb9"><pre class="sourceCode asm"><code class="sourceCode fasm"><span id="cb9-1"><a href="#cb9-1"></a><span class="bu">ret</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [종료 상태](../Page/종료_상태.md "wikilink")

## 각주

[분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink")

1.  in Bash, only integers in the range 0-255 may be returned: <http://tldp.org/LDP/abs/html/complexfunct.html#RETURNREF>