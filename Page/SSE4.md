> This article is converted from Wikipedia: [SSE4](https://ko.wikipedia.org/wiki/SSE4).


**SSE4**(Streaming SIMD Extensions 4)는 [인텔 코어 마이크로아키텍처와](https://ko.wikipedia.org/wiki/인텔_코어_마이크로아키텍처 "wikilink") [AMD K10](../Page/AMD_K10.md "wikilink")(K8L)에서 지원되는 [명령어 집합이다](../Page/명령어_집합.md "wikilink"). [2006년](../Page/2006년.md "wikilink") 9월 27일에 2006 추계 [인텔 개발자 포럼에서](../Page/인텔_개발자_포럼.md "wikilink") 약간 모호한 백서와 함께 발표되었다.\[1\] 이후 2007년 봄 북경에서 개최된 인텔 개발자 포럼에서 47개의 자세한 명령어가 소개되었다.\[2\] SSE4 프로그래밍 참조서가 [1](https://web.archive.org/web/20081031084014/http://softwarecommunity.intel.com/isn/Downloads/Intel%20SSE4%20Programming%20Reference.pdf) 인텔로부터 제공된다.

## SSE4 부분집합

인텔 SSE4는 총 54개 명령어로 이루어졌다. 첫 47개의 명령어 집합은 인텔자료에서 **SSE4.1**로 불리며, 이것은 [펜린에서부터](https://ko.wikipedia.org/wiki/코어_2#펜린 "wikilink") 사용 가능하다. 이후 인텔은 추가적으로 7개의 명령어 **SSE4.2**를 [인텔 코어 i7](../Page/인텔_코어_i7.md "wikilink")([네할렘](https://ko.wikipedia.org/wiki/네할렘 "wikilink") 아키텍처)에서부터 지원한다. 인텔은 일반적으로 명령어 집합을 개발하는 데 있어서 개발자들의 의견을 중시하여 반영한다고 알려져 있다.

[AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")는 SSE4 명령어 집합 중 **SSE4A**라고 불리는 4개의 명령어. 나중에 2개의 SSE 명령어를 추가하였다. 이 명령어는 인텔의 프로세서에서는 지원되지 않고있다.

## 이름의 혼동

[인텔 코어 2](../Page/인텔_코어_2.md "wikilink") 제품 계열에서 발표된 [SSSE3](../Page/SSSE3.md "wikilink")(Supplemental Streaming SIMD Extension 3)는 개발기간 동안에 미디어에 의해 SSE4로 잘못 언급되었었다.

## 신규 명령어

이전 모든 SSE와는 다르게 SSE4는 멀티미디어 애플리케이션과 관련이 없는 명령어들이 포함되었다. 상수항과 함축적인 3번째 피연산자로서 XMM0를 사용하는 명령어에 의해 그 동작이 결정되는 명령어 집합이다.

이러한 여러 명령어들은 [펜린에서부터](https://ko.wikipedia.org/wiki/코어_2#펜린 "wikilink") 한 싸이클 셔플 엔진(shuffle engine)에 의해 구현된다.( 셔플은 비트들을 재배치 시키는 것에 관련된 동작이다.)

### SSE4.1

이 명령어들은 코어 마이크로아키텍처의 더 미세화된 공정 45 nm를 사용하는 펜린 마이크로아키텍처에서 적용되었다.

### SSE4.2

이 명령어들은 [네할렘 마이크로아키텍처](https://ko.wikipedia.org/wiki/네할렘_마이크로아키텍처 "wikilink") 기반 제품부터 적용되었다. SSE4 명령어 집합을 완결한다.

### SSE4a

이 그룹은 AMD의 바르셀로나 마이크로아키텍처에서 소개되었다. POPCNT명령어외엔 인텔 프로세서에서 지원되지 않는다.

## 지원 CPU

  - [인텔](../Page/인텔.md "wikilink")
      - Intel 펜린 프로세서 (SSE4.1 지원)
      - Intel [네할렘](https://ko.wikipedia.org/wiki/네할렘_마이크로아키텍처 "wikilink") 프로세서 (SSE4.1, SSE4.2 ,POPCNT 명령어 지원)
      - Intel [실버몬트](https://ko.wikipedia.org/wiki/실버몬트_마이크로아키텍처 "wikilink") 프로세서 (SSE4.1, SSE4.2, POPCNT 명령어 지원)
      - Intel [하스웰](https://ko.wikipedia.org/wiki/해스웰_\(마이크로아키텍처\) "wikilink") 프로세서 (SSE4.1, SSE4.2, POPCNT ,LZCNT 명령어 지원)
  - [AMD](../Page/어드밴스트_마이크로_디바이시스.md "wikilink")
      - AMD [바르셀로나](../Page/AMD_K10.md "wikilink")-기반 프로세서 (SSE4a, POPCNT ,LZCNT 명령어 지원)
      - AMD [불도저](../Page/불도저_\(마이크로아키텍처\).md "wikilink") 기반 프로세서 (SSE4a, SSE4.1, SSE4.2, POPCNT ,LZCNT 명령어 지원)
      - AMD [밥캣](../Page/밥캣_\(마이크로아키텍처\).md "wikilink") 기반 프로세서 (SSE4a, POPCNT ,LZCNT 명령어 지원)
      - AMD [재규어기반](../Page/재규어_\(마이크로아키텍처\).md "wikilink") 프로세서 (SSE4a, SSE4.1, SSE4.2, POPCNT ,LZCNT 명령어 지원)

<!-- end list -->

  - [VIA](../Page/비아_테크놀로지스.md "wikilink")
      - VIA [Nano](https://ko.wikipedia.org/wiki/VIA_Nano "wikilink") 프로세서 (SSE4.1 명령어 지원)

## 같이 보기

<table>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="../Page/스트리밍_SIMD_확장.md" title="wikilink">스트리밍 SIMD 확장</a> (SSE)</li>
<li><a href="../Page/SSE2.md" title="wikilink">SSE2</a></li>
<li><a href="../Page/SSE3.md" title="wikilink">SSE3</a></li>
<li><a href="../Page/SSSE3.md" title="wikilink">SSSE3</a></li>
<li><a href="../Page/SIMD.md" title="wikilink">SIMD</a></li>
<li><a href="../Page/고급_벡터_확장.md" title="wikilink">AVX</a></li>
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

## 각주

[분류:SIMD 컴퓨팅](https://ko.wikipedia.org/wiki/분류:SIMD_컴퓨팅 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink")

1.  [Intel Streaming SIMD Extensions 4 (SSE4) Instruction Set Innovation](http://www.intel.com/technology/architecture-silicon/sse4-instructions/index.htm), Intel.
2.  [Tuning for Intel SSE4 for the 45nm Next Generation Intel Core Microarchitecture](https://intel.wingateweb.com/published/BMAS005/BMAS005_100Eng.pdf), Intel.