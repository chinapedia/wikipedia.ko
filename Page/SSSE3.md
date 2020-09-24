> This article is converted from Wikipedia: [SSSE3](https://ko.wikipedia.org/wiki/SSSE3).


**스트리밍 SIMD 확장 3 추가판**()는 인텔의 4번째 SSE 명령어 집합이다. 이전 버전은 SSE3였고 인텔은 버전 번호를 증가시키기보다는 *S*를 붙였다. 왜냐하면 단지 SSE3의 개정판으로 생각 했기 때문이다. 인텔이 공식적으로 이름을 붙이기 전에는 **[SSE4](../Page/SSE4.md "wikilink")**로 잘못 언급되기도 하였다. 또한 이것을 지원하고자 하는 첫 프로세서 코드 이름으로서 **[테자스](https://ko.wikipedia.org/wiki/테자스 "wikilink") 신규 명령어(TNI)** 또는 **[메롬](https://ko.wikipedia.org/wiki/인텔_코어_2#메롬 "wikilink") 신규 명령어(MNI)**로 언급되기도 했다. 인텔의 [코어 마이크로아키텍처에서](https://ko.wikipedia.org/wiki/코어_마이크로아키텍처 "wikilink") 소개된 SSSE3는 서버와 워크스테이션용 [제온](../Page/제온.md "wikilink") 5100 계열 및 [인텔 코어 2](../Page/인텔_코어_2.md "wikilink") 노트북 및 데스크톱 프로세서에서 지원된다.

SSSE3는 SSE3와 비교하여 16개의 새 개별 명령어를 포함한다. 각각은 64비트 MMX 또는 128비트 XMM레지스터들위에서 동작을 한다. 따라서 인텔의 자료에서는 신규 명령어가 32개라고 한다. [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")플랫폼에서의 이전 [SIMD](../Page/SIMD.md "wikilink") 명령어 집합은 시간순으로 [MMX](../Page/MMX.md "wikilink"), [3DNow\!](https://ko.wikipedia.org/wiki/3DNow! "wikilink") (AMD에 의해 개발), [SSE](../Page/스트리밍_SIMD_확장.md "wikilink"), [SSE2](../Page/SSE2.md "wikilink") 그리고 [SSE3](../Page/SSE3.md "wikilink")이다.

## SSSE3를 지원하는 CPU

  - [인텔](../Page/인텔.md "wikilink"):
      - [제온](../Page/제온.md "wikilink") 5100 계열
      - [제온](../Page/제온.md "wikilink") 5300 계열
      - [제온](../Page/제온.md "wikilink") 3000 계열
      - [코어 2](https://ko.wikipedia.org/wiki/코어_2 "wikilink") 듀오
      - [코어 2](https://ko.wikipedia.org/wiki/코어_2 "wikilink") 익스트림
      - [코어 2](https://ko.wikipedia.org/wiki/코어_2 "wikilink") 쿼드
      - [펜티엄 듀얼 코어](../Page/펜티엄_듀얼_코어.md "wikilink")
      - [셀러론 4xx 계열 콘로-L](https://ko.wikipedia.org/wiki/셀러론#셀러론_\(코어\) "wikilink")
      - [셀러론 듀얼 코어 E1200](https://ko.wikipedia.org/wiki/셀러론_M#셀러론_듀얼_코어_\(코어\) "wikilink")
      - [셀러론 M 500 계열](https://ko.wikipedia.org/wiki/셀러론_M#메롬-1024 "wikilink")
      - [아톰](../Page/인텔_아톰.md "wikilink")
  - [VIA](https://ko.wikipedia.org/wiki/VIA "wikilink"):
      - [나노](../Page/비아_나노.md "wikilink")

## 같이 보기

<table>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="../Page/스트리밍_SIMD_확장.md" title="wikilink">스트리밍 SIMD 확장</a> (SSE)</li>
<li><a href="../Page/SSE2.md" title="wikilink">SSE2</a></li>
<li><a href="../Page/SSE3.md" title="wikilink">SSE3</a></li>
<li><a href="../Page/SSE4.md" title="wikilink">SSE4</a></li>
<li><a href="https://ko.wikipedia.org/wiki/SSE5" title="wikilink">SSE5</a></li>
<li><a href="../Page/SIMD.md" title="wikilink">SIMD</a></li>
</ul></td>
<td><ul>
<li><a href="https://ko.wikipedia.org/wiki/넷버스트_마이크로아키텍처" title="wikilink">넷버스트 마이크로아키텍처</a></li>
<li><a href="https://ko.wikipedia.org/wiki/네할렘_마이크로아키텍처" title="wikilink">네할렘 마이크로아키텍처</a></li>
<li><a href="../Page/마이크로아키텍처.md" title="wikilink">마이크로아키텍처</a></li>
<li><a href="https://ko.wikipedia.org/wiki/콘로" title="wikilink">콘로</a></li>
<li><a href="../Page/제온.md" title="wikilink">제온</a></li>
<li><a href="https://ko.wikipedia.org/wiki/코어_마이크로아키텍처" title="wikilink">코어 마이크로아키텍처</a></li>
</ul></td>
</tr>
</tbody>
</table>

## 외부 링크

  - [코어 2 모바일 규격](https://web.archive.org/web/20061104143303/http://download.intel.com/design/mobile/datashts/31407801.pdf)
  - [Intel white-paper admitting the existence of SSSE3 and describing SSE4](https://web.archive.org/web/20111124230720/http://download.intel.com/technology/architecture/new-instructions-paper.pdf)
  - [Instruction set documentation listing the functions of the SSSE3 instructions](http://www.intel.com/design/processor/manuals/253667.pdf)

[분류:X86 아키텍처](https://ko.wikipedia.org/wiki/분류:X86_아키텍처 "wikilink") [분류:인텔](https://ko.wikipedia.org/wiki/분류:인텔 "wikilink") [분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink") [분류:SIMD 컴퓨팅](https://ko.wikipedia.org/wiki/분류:SIMD_컴퓨팅 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink")