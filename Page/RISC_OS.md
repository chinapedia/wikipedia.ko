> This article is converted from Wikipedia: [RISC OS](https://ko.wikipedia.org/wiki/RISC_OS).


**RISC OS**(리스크 오에스 \[1\])는 [ARM 아키텍처용으로](https://ko.wikipedia.org/wiki/ARM_아키텍처 "wikilink") 설계된 [그래픽 사용자 인터페이스](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 기반 컴퓨터 [운영 체제](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 시리즈이다. 이를 지원하는 [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") 아키텍처에서 이름을 땄다. 이 운영 체제는 원래 [아콘 컴퓨터가](../Page/아콘_컴퓨터.md "wikilink") [아콘 RISC 머신](https://ko.wikipedia.org/wiki/ARM_아키텍처 "wikilink") 프로세서를 사용하는 1987년의 [아콘 아르키메데스](https://ko.wikipedia.org/wiki/아콘_아르키메데스 "wikilink") 개인용 컴퓨터 세대에 채용할 목적으로 개발되었다. [윈도 시스템을](https://ko.wikipedia.org/wiki/윈도_시스템 "wikilink") 갖춘 [데스크톱 환경과](../Page/데스크톱_환경.md "wikilink") [명령 줄 인터페이스로](../Page/명령_줄_인터페이스.md "wikilink") 이루어져 있다.

1988년부터 1998년까지 이 운영 체제는 아르키메데스 제품군, [RiscPC](https://ko.wikipedia.org/wiki/RiscPC "wikilink"), 뉴스패드, [A7000을](https://ko.wikipedia.org/wiki/아콘_A7000 "wikilink") 포함한 거의 모든 ARM 기반 아콘 컴퓨터 모델에 기본 포함되었다. 이 운영 체제의 버전 ([NCOS](https://ko.wikipedia.org/wiki/NCOS "wikilink"))은 [오라클의](../Page/오라클_\(기업\).md "wikilink") [네트워크 컴퓨터](https://ko.wikipedia.org/wiki/네트워크_컴퓨터 "wikilink") 및 호환 기종에 사용되었다. 1998년 아콘이 해체된 뒤 이 운영 체제의 개발은 분리되면서 [RISCOS](https://ko.wikipedia.org/wiki/RISCOS "wikilink"), [페이스 마이크로 테크놀로지](https://ko.wikipedia.org/wiki/페이스_plc "wikilink"), [캐슬 테크놀로지를](https://ko.wikipedia.org/wiki/캐슬_테크놀로지 "wikilink") 포함한 여러 기업에서 별도로 개발을 지속하고 있다. 1998년 이후 [Iyonix](https://ko.wikipedia.org/wiki/Iyonix_PC "wikilink")\[2\], [A9홈](https://ko.wikipedia.org/wiki/A9홈 "wikilink")과 같은 수많은 ARM 기반 데스크톱 컴퓨터에 기본 포함되고 있다. 2012년 기준으로 이 운영 체제는 분기화되어 독립적으로 RISCOS사와 [RISC OS 오픈](https://ko.wikipedia.org/wiki/RISC_OS_오픈 "wikilink") 커뮤니티가 개발을 맡고 있다.

가장 최근의 안정판은 ARMv3/ARMv4 [RiscPC](https://ko.wikipedia.org/wiki/RiscPC "wikilink")\[3\] ([버추얼아콘](https://ko.wikipedia.org/wiki/버추얼아콘 "wikilink")이나 [RPCEmu](https://ko.wikipedia.org/wiki/RPCEmu "wikilink")와 같은 에뮬레이션을 통해), ARMv5 [Iyonix](https://ko.wikipedia.org/wiki/Iyonix_PC "wikilink")\[4\], ARMv7 [Cortex-A8](https://ko.wikipedia.org/wiki/ARM_Cortex-A8 "wikilink") 프로세서\[5\]\[6\]([비글보드](https://ko.wikipedia.org/wiki/비글보드 "wikilink"), [터치 북에서](https://ko.wikipedia.org/wiki/터치_북 "wikilink") 사용됨)에서 구동된다. 2011년에는 [Cortex-A9](https://ko.wikipedia.org/wiki/ARM_Cortex-A9_MPCore "wikilink") [판다보드](https://ko.wikipedia.org/wiki/판다보드 "wikilink")용 포팅이 발표되었으며\[7\] [라즈베리 파이용](../Page/라즈베리_파이.md "wikilink") 개발 버전이 대중에 공개되었다.\[8\]\[9\]\[10\]

## 역사

## 지원 하드웨어

RISC OS 버전들은 다음의 하드웨어에서 동작한다.

<table>
<caption>RISC OS 호환 하드웨어</caption>
<thead>
<tr class="header">
<th><p>기기</p></th>
<th><p>도입연도</p></th>
<th><p>버전</p></th>
<th><p>ROOL<br />
개발 ROM[11]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>최초</p></td>
<td><p>최종</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong><a href="https://ko.wikipedia.org/wiki/26비트" title="wikilink">26비트</a> 프로그램 카운터를 갖춘 ARM</strong></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/아콘_아르키메데스" title="wikilink">아콘 아르키메데스</a></p></td>
<td><p>1987 ­ 1992</p></td>
<td><p>0.30 ­ 3.1x</p></td>
<td><p>3.1x</p></td>
</tr>
<tr class="even">
<td><p><strong>26- &amp; 32비트 프로그램 카운터를 갖춘 ARM</strong></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Risc_PC" title="wikilink">아콘 Risc PC</a></p></td>
<td><p>1994[12]</p></td>
<td><p>3.50[13]</p></td>
<td><p>6.20[14]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/아콘_A7000" title="wikilink">아콘 A7000 및 A7000+</a></p></td>
<td><p>1995[15] ­ 1997[16]</p></td>
<td><p>3.60[17] ­ 3.71[18]</p></td>
<td><p>6.20[19]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/아콘_Phoebe" title="wikilink">아콘 Phoebe</a></p></td>
<td><p>1998 (취소)</p></td>
<td><p>3.80 (Ursula)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>마이크로디지털 메디[20]</p></td>
<td><p>1998[21]</p></td>
<td><p>3.71[22]</p></td>
<td><p>6.20</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/마이크로디지털_마이크로" title="wikilink">마이크로디지털 마이크로</a></p></td>
<td><p>1999[23]</p></td>
<td><p>4.03[24]</p></td>
<td><p>4.39[25]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/RiscStation_R7500" title="wikilink">RiscStation R7500</a></p></td>
<td><p>1999[26]</p></td>
<td><p>4.03[27]</p></td>
<td><p>4.39[28]</p></td>
</tr>
<tr class="odd">
<td><p>캐슬 키네틱 RiscPC</p></td>
<td><p>2000[29]</p></td>
<td><p>4.03</p></td>
<td><p>6.20</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/마이크로디지털_오메가" title="wikilink">마이크로디지털 오메가</a></p></td>
<td><p>2003[30]</p></td>
<td><p>4.03[31]</p></td>
<td><p>4.39[32]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/어드밴티지_식스_A75" title="wikilink">어드밴티지 식스 A75</a></p></td>
<td><p>2004[33]</p></td>
<td><p>4.39[34]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>32비트 프로그램 카운터를 갖춘 ARM</strong></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Iyonix_PC" title="wikilink">Iyonix Ltd Iyonix PC</a></p></td>
<td><p>2002</p></td>
<td><p>5.01</p></td>
<td><p>5.18[35]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/A9Home" title="wikilink">어드밴티지 식스 A9</a>(Home/RM/Loc)</p></td>
<td><p>2005</p></td>
<td><p>4.42[36]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/비글보드" title="wikilink">비글보드</a>[37]</p></td>
<td><p>2008</p></td>
<td><p>5.15</p></td>
<td><p>5.18[38]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/터치_북" title="wikilink">얼웨이즈 이노베이팅 터치 북</a></p></td>
<td><p>2009</p></td>
<td><p>5.15</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/판다보드" title="wikilink">판다보드</a>[39]</p></td>
<td><p>2011</p></td>
<td><p>5.17</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/오픈판도라" title="wikilink">오픈판도라</a> <a href="https://ko.wikipedia.org/wiki/판도라_(콘솔)" title="wikilink">판도라</a></p></td>
<td><p>2009</p></td>
<td><p>5.17</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/라즈베리_파이.md" title="wikilink">라즈베리 파이</a>[40][41]</p></td>
<td><p>2012</p></td>
<td><p>5.19</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><small><strong>미결정</strong> = 공식적으로 이용이 불가능함</small></p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

이와 더불어, [마이크로디지털](https://ko.wikipedia.org/wiki/마이크로디지털 "wikilink"), [어드밴티지 식스](https://ko.wikipedia.org/wiki/어드밴티지_식스 "wikilink"), [R-Comp](https://ko.wikipedia.org/wiki/R-Comp "wikilink")의 상용 에뮬레이터를 마이크로소프트 윈도 PC의 독립 제품으로 [버추얼아콘](https://ko.wikipedia.org/wiki/버추얼아콘 "wikilink")을 통해 사용이 가능하다. 이 에뮬레이터에는 구매한 버추얼 아콘 버전에 따라 RiscOS - 4.02 또는 4.39의 완전한 라이선스 사본이 동봉된다.\[42\]

RISC OS는 아콘과 [페이스 마이크로 테크놀로지의](https://ko.wikipedia.org/wiki/페이스_마이크로_테크놀로지 "wikilink") 다양한 TV 연결 [셋톱 박스에도](https://ko.wikipedia.org/wiki/셋톱_박스 "wikilink") 사용되고 있다.

## 각주

<references />

## 외부 링크

  - [What is RISC OS?](https://archive.is/20070219161339/http://productsdb.riscos.com/admin/riscos.htm)

[분류:아콘 컴퓨터](https://ko.wikipedia.org/wiki/분류:아콘_컴퓨터 "wikilink") [분류:데스크톱 환경](https://ko.wikipedia.org/wiki/분류:데스크톱_환경 "wikilink") [분류:ARM 운영 체제](https://ko.wikipedia.org/wiki/분류:ARM_운영_체제 "wikilink") [분류:자유 소프트웨어 운영 체제](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_운영_체제 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11. [RISC OS Open: ROM image releases](https://www.riscosopen.org/content/downloads/other-zipfiles)
12. [Chris's Acorns – Risc PC](http://acorn.chriswhy.co.uk/Computers/RiscPCComputers.html)
13.
14.
15. [Chris's Acorns – A7000](http://acorn.chriswhy.co.uk/Computers/A7000.html)
16. [Chris's Acorns – A7000+](http://acorn.chriswhy.co.uk/Computers/A7000+.html)
17.
18.
19.
20. repackaged A7000+
21. [Chris's Acorns – Microdigital Medi](http://acorn.chriswhy.co.uk/AfterAcorn/Microdigital.html#Medi)
22.
23. [Chris's Acorns – Microdigital Mico](http://acorn.chriswhy.co.uk/AfterAcorn/Microdigital_Mico.html)
24.
25.
26. [Chris's Acorns – RiscStation R7500](http://acorn.chriswhy.co.uk/AfterAcorn/Riscstation.html)
27.
28.
29. [Castle reveal Kinetic to the press](http://www.iconbar.com/forums/viewthread.php?newsid=918)
30. [Drobe – Omega production saga continues](http://www.drobe.co.uk/article.php?id=973)
31. [– Microdigital Omega](http://acorn.chriswhy.co.uk/AfterAcorn/Microdigital.html#Omega)
32.
33. [Drobe – A75 is ARM7500FE ruggable](http://www.drobe.co.uk/article.php?id=1047)
34. [Advantage6: Thea75](http://www.advantagesix.com/Thea75.html)
35.
36.
37.
38.
39.
40.
41.
42. [Virtual Acorn versions](http://www.virtualacorn.co.uk/product.htm)