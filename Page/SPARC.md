> This article is converted from Wikipedia: [SPARC](https://ko.wikipedia.org/wiki/SPARC).


[섬네일](https://ko.wikipedia.org/wiki/파일:Sparc-logo.svg "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:Sun_UltraSPARCII.jpg "wikilink") **SPARC** (스팍, Scalable Processor ARChitecture - 확장형 프로세서 아키텍처)는 [1985년](../Page/1985년.md "wikilink") [빌 조이가](../Page/빌_조이.md "wikilink") 몸담고있던 [썬 마이크로시스템즈가](../Page/썬_마이크로시스템즈.md "wikilink") 개발한 [빅 엔디안](../Page/엔디언.md "wikilink") [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")이다. SPARC 은 [1989년](../Page/1989년.md "wikilink") 썬 마이크로시스템즈가 스팍의 확산을 위해 설립한 SPARC International, Inc.의 등록 상표이기도 하다. SPARC International은 스팍 아키텍처를 공개하였으며, [텍사스 인스트루먼츠](https://ko.wikipedia.org/wiki/텍사스_인스트루먼츠 "wikilink")(TI), [사이프레스 세미컨덕터](https://ko.wikipedia.org/wiki/사이프레스_세미컨덕터 "wikilink"), [후지쯔](../Page/후지쯔.md "wikilink") 등 많은 칩 제조사에게 라이선스를 주기도 했다. 즉 SPARC에 기반한 마이크로프로세서는 더이상 썬 마이크로시스템즈만 제조할 수 있는 것이 아니다. 스팍 아키텍처는 SPARC International이 [VHDL](../Page/VHDL.md "wikilink")로 작성한 LEON라는 소스를 공개하였으며, 누구도 소유하지 않는 완전 공개된 아키텍처가 되었다. 이 소스는 [LGPL](https://ko.wikipedia.org/wiki/LGPL "wikilink")을 따른다.

스팍 아키텍처의 구현은 초기에는 썬이나 후지쯔의 대형 SMP서버나 [워크스테이션](../Page/워크스테이션.md "wikilink")을 위해 개발되었다. SPARC 머신은 일반적으로 썬이 SPARC를 위해 개발한 [운영 체제인](../Page/운영_체제.md "wikilink") [솔라리스와](../Page/솔라리스_\(운영_체제\).md "wikilink") 비슷하게 취급된다. 현재 [NeXTSTEP](../Page/NeXTSTEP.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink"), [OpenBSD](../Page/OpenBSD.md "wikilink"), [NetBSD](../Page/NetBSD.md "wikilink") 등이 스팍 프로세서에서 작동한다.

다양한 버전의 스팍 아키텍처가 있으며 스팍 버전 9는 64비트를 구현하였다. [2005년](../Page/2005년.md "wikilink") 12월에 썬은 자사의 새로운 스팍 아키텍처 울트라스팍 2005를 구현한 UltraSPARC T1을 개발하였다. 썬은 UltraSPARC T1의 디자인을 공개하였다.

## SPARC 마이크로프로세서 규격

<table>
<thead>
<tr class="header">
<th><p>이름<br />
(코드이름)</p></th>
<th><p>모델</p></th>
<th><p>주파수<br />
[MHz]</p></th>
<th><p>아키텍처<br />
버전</p></th>
<th><p>출시연도</p></th>
<th><p>스레드<br />
코어 당 × 코어<br />
= Total 스레드</p></th>
<th><p>공정<br />
[µm]</p></th>
<th><p>트랜지스터<br />
[100만]</p></th>
<th><p>다이 크기<br />
[mm²]</p></th>
<th><p>IO 핀</p></th>
<th><p>전력<br />
[W]</p></th>
<th><p>전압<br />
[V]</p></th>
<th><p>1차 데이터 D캐시<br />
[k]</p></th>
<th><p>1차 명령어 캐시<br />
[k]</p></th>
<th><p>2차 캐시<br />
[k]</p></th>
<th><p>3차 캐시<br />
[k]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SPARC</p></td>
<td><p>(다양함)[1]</p></td>
<td><p>14.28–40</p></td>
<td><p>V7</p></td>
<td><p>1987-1992</p></td>
<td><p>1×1=1</p></td>
<td><p>0.8–1.3</p></td>
<td><p>~0.1–1.8</p></td>
<td><p>--</p></td>
<td><p>160–256</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>0–128 (unified)</p></td>
<td><p>없음</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>microSPARC I (Tsunami)</p></td>
<td><p>TI TMS390S10</p></td>
<td><p>40–50</p></td>
<td><p>V8</p></td>
<td><p>1992</p></td>
<td><p>1×1=1</p></td>
<td><p>0.8</p></td>
<td><p>0.8</p></td>
<td><p>225?</p></td>
<td><p>288</p></td>
<td><p>2.5</p></td>
<td><p>5</p></td>
<td><p>2</p></td>
<td><p>4</p></td>
<td><p>없음</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>SuperSPARC I (Viking)</p></td>
<td><p>TI TMX390Z50 / Sun STP1020</p></td>
<td><p>33–60</p></td>
<td><p>V8</p></td>
<td><p>1992</p></td>
<td><p>1×1=1</p></td>
<td><p>0.8</p></td>
<td><p>3.1</p></td>
<td><p>--</p></td>
<td><p>293</p></td>
<td><p>14.3</p></td>
<td><p>5</p></td>
<td><p>16</p></td>
<td><p>20</p></td>
<td><p>0-2048</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>SPARClite</p></td>
<td><p>Fujitsu MB8683x</p></td>
<td><p>66–108</p></td>
<td><p>V8E</p></td>
<td><p>1992</p></td>
<td><p>1×1=1</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>144–176</p></td>
<td><p>--</p></td>
<td><p>2.5/3.3V</p></td>
<td><p>1–16</p></td>
<td><p>1–16</p></td>
<td><p>없음</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>hyperSPARC (Colorado 1)</p></td>
<td><p>Ross RT620A</p></td>
<td><p>40–90</p></td>
<td><p>V8</p></td>
<td><p>1993</p></td>
<td><p>1×1=1</p></td>
<td><p>0.5</p></td>
<td><p>1.5</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>5?</p></td>
<td><p>0</p></td>
<td><p>8</p></td>
<td><p>128-256</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>microSPARC II (Swift)</p></td>
<td><p>Fujitsu MB86904 / Sun STP1012</p></td>
<td><p>60–125</p></td>
<td><p>V8</p></td>
<td><p>1994</p></td>
<td><p>1×1=1</p></td>
<td><p>0.5</p></td>
<td><p>2.3</p></td>
<td><p>233</p></td>
<td><p>321</p></td>
<td><p>5</p></td>
<td><p>3.3</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>없음</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>hyperSPARC (Colorado 2)</p></td>
<td><p>Ross RT620B</p></td>
<td><p>90–125</p></td>
<td><p>V8</p></td>
<td><p>1994</p></td>
<td><p>1×1=1</p></td>
<td><p>0.4</p></td>
<td><p>1.5</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>3.3</p></td>
<td><p>0</p></td>
<td><p>8</p></td>
<td><p>128-256</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>SuperSPARC II (Voyager)</p></td>
<td><p>Sun STP1021</p></td>
<td><p>75–90</p></td>
<td><p>V8</p></td>
<td><p>1994</p></td>
<td><p>1×1=1</p></td>
<td><p>0.8</p></td>
<td><p>3.1</p></td>
<td><p>299</p></td>
<td><p>--</p></td>
<td><p>16</p></td>
<td><p>--</p></td>
<td><p>16</p></td>
<td><p>20</p></td>
<td><p>1024-2048</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>hyperSPARC (Colorado 3)</p></td>
<td><p>Ross RT620C</p></td>
<td><p>125–166</p></td>
<td><p>V8</p></td>
<td><p>1995</p></td>
<td><p>1×1=1</p></td>
<td><p>0.35</p></td>
<td><p>1.5</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>3.3</p></td>
<td><p>0</p></td>
<td><p>8</p></td>
<td><p>512-1024</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>TurboSPARC</p></td>
<td><p>Fujitsu MB86907</p></td>
<td><p>160–180</p></td>
<td><p>V8</p></td>
<td><p>1995</p></td>
<td><p>1×1=1</p></td>
<td><p>0.35</p></td>
<td><p>3.0</p></td>
<td><p>132</p></td>
<td><p>416</p></td>
<td><p>7</p></td>
<td><p>3.5</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>512</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>UltraSPARC I (Spitfire)</p></td>
<td><p>Sun STP1030</p></td>
<td><p>143–167</p></td>
<td><p>V9</p></td>
<td><p>1995</p></td>
<td><p>1×1=1</p></td>
<td><p>0.47</p></td>
<td><p>5.2</p></td>
<td><p>315</p></td>
<td><p>521</p></td>
<td><p>30 @167 MHz</p></td>
<td><p>3.3</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>512-1024</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC I (Hornet)</p></td>
<td><p>Sun STP1030</p></td>
<td><p>200</p></td>
<td><p>V9</p></td>
<td><p>1998</p></td>
<td><p>1×1=1</p></td>
<td><p>0.42</p></td>
<td><p>5.2</p></td>
<td><p>265</p></td>
<td><p>521</p></td>
<td><p>--</p></td>
<td><p>3.3</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>512-1024</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>hyperSPARC (Colorado 4)</p></td>
<td><p>Ross RT620D</p></td>
<td><p>180–200</p></td>
<td><p>V8</p></td>
<td><p>1996</p></td>
<td><p>1×1=1</p></td>
<td><p>0.35</p></td>
<td><p>1.7</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>3.3</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>512</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>SPARC64</p></td>
<td><p>Fujitsu (HAL)</p></td>
<td><p>101–118</p></td>
<td><p>V9</p></td>
<td><p>1995</p></td>
<td><p>1×1=1</p></td>
<td><p>0.4</p></td>
<td><p>--</p></td>
<td><p>297+163+142</p></td>
<td><p>286</p></td>
<td><p>50</p></td>
<td><p>3.8</p></td>
<td><p>128</p></td>
<td><p>128</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p>SPARC64 II</p></td>
<td><p>Fujitsu (HAL)</p></td>
<td><p>141–161</p></td>
<td><p>V9</p></td>
<td><p>1996</p></td>
<td><p>1×1=1</p></td>
<td><p>0.35</p></td>
<td><p>--</p></td>
<td><p>202+103+84</p></td>
<td><p>286</p></td>
<td><p>64</p></td>
<td><p>3.3</p></td>
<td><p>128</p></td>
<td><p>128</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p>SPARC64 III</p></td>
<td><p>Fujitsu (HAL) MBCS70301</p></td>
<td><p>250–330</p></td>
<td><p>V9</p></td>
<td><p>1998</p></td>
<td><p>1×1=1</p></td>
<td><p>0.24</p></td>
<td><p>17.6</p></td>
<td><p>240</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>2.5</p></td>
<td><p>64</p></td>
<td><p>64</p></td>
<td><p>8192</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p>UltraSPARC IIs (Blackbird)</p></td>
<td><p>Sun STP1031</p></td>
<td><p>250–400</p></td>
<td><p>V9</p></td>
<td><p>1997</p></td>
<td><p>1×1=1</p></td>
<td><p>0.35</p></td>
<td><p>5.4</p></td>
<td><p>149</p></td>
<td><p>521</p></td>
<td><p>25 @250 MHz</p></td>
<td><p>2.5</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>1024 or 4096</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC IIs (Sapphire-Black)</p></td>
<td><p>Sun STP1032 / STP1034</p></td>
<td><p>360–480</p></td>
<td><p>V9</p></td>
<td><p>1999</p></td>
<td><p>1×1=1</p></td>
<td><p>0.25</p></td>
<td><p>5.4</p></td>
<td><p>126</p></td>
<td><p>521</p></td>
<td><p>21 @400 MHz</p></td>
<td><p>1.9</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>1024–8192</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>UltraSPARC IIi (Sabre)</p></td>
<td><p>Sun SME1040</p></td>
<td><p>270–360</p></td>
<td><p>V9</p></td>
<td><p>1997</p></td>
<td><p>1×1=1</p></td>
<td><p>0.35</p></td>
<td><p>5.4</p></td>
<td><p>156</p></td>
<td><p>587</p></td>
<td><p>21</p></td>
<td><p>1.9</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>256–2048</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC IIi (Sapphire-Red)</p></td>
<td><p>Sun SME1430</p></td>
<td><p>333–480</p></td>
<td><p>V9</p></td>
<td><p>1998</p></td>
<td><p>1×1=1</p></td>
<td><p>0.25</p></td>
<td><p>5.4</p></td>
<td><p>--</p></td>
<td><p>587</p></td>
<td><p>21 @440 MHz</p></td>
<td><p>1.9</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>2048</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>UltraSPARC IIe (Hummingbird)</p></td>
<td><p>Sun SME1701</p></td>
<td><p>400–500</p></td>
<td><p>V9</p></td>
<td><p>2000</p></td>
<td><p>1×1=1</p></td>
<td><p>0.18 Al</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>370</p></td>
<td><p>13 max @500 MHz</p></td>
<td><p>1.5-1.7</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>256</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC IIi (IIe+) (Phantom)</p></td>
<td><p>--</p></td>
<td><p>550–650</p></td>
<td><p>V9</p></td>
<td><p>2002</p></td>
<td><p>1×1=1</p></td>
<td><p>0.18 Cu</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>370</p></td>
<td><p>17.6</p></td>
<td><p>1.7</p></td>
<td><p>16</p></td>
<td><p>16</p></td>
<td><p>512</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>SPARC64 GP</p></td>
<td><p>Fujitsu SFCB81147</p></td>
<td><p>400–810</p></td>
<td><p>V9</p></td>
<td><p>2000</p></td>
<td><p>1×1=1</p></td>
<td><p>0.18</p></td>
<td><p>30.2</p></td>
<td><p>217</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>1.8</p></td>
<td><p>128</p></td>
<td><p>128</p></td>
<td><p>8192</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p>SPARC64 IV</p></td>
<td><p>Fujitsu MBCS80523</p></td>
<td><p>450–810</p></td>
<td><p>V9</p></td>
<td><p>2000</p></td>
<td><p>1×1=1</p></td>
<td><p>0.13</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>--</p></td>
<td><p>128</p></td>
<td><p>128</p></td>
<td><p>2048</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p>UltraSPARC III (Cheetah)</p></td>
<td><p>Sun SME1050</p></td>
<td><p>600</p></td>
<td><p>V9</p></td>
<td><p>2001</p></td>
<td><p>1×1=1</p></td>
<td><p>0.18 Al</p></td>
<td><p>29</p></td>
<td><p>330</p></td>
<td><p>1368</p></td>
<td><p>53</p></td>
<td><p>1.6</p></td>
<td><p>64</p></td>
<td><p>32</p></td>
<td><p>8192</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC III (Cheetah)</p></td>
<td><p>Sun SME1052</p></td>
<td><p>750–900</p></td>
<td><p>V9</p></td>
<td><p>2001</p></td>
<td><p>1×1=1</p></td>
<td><p>0.13 Al</p></td>
<td><p>29</p></td>
<td><p>--</p></td>
<td><p>1368</p></td>
<td><p>--</p></td>
<td><p>1.6</p></td>
<td><p>64</p></td>
<td><p>32</p></td>
<td><p>8192</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>UltraSPARC III Cu (Cheetah+)</p></td>
<td><p>Sun SME1056</p></td>
<td><p>1002–1200</p></td>
<td><p>V9</p></td>
<td><p>2001</p></td>
<td><p>1×1=1</p></td>
<td><p>0.13 Cu</p></td>
<td><p>29</p></td>
<td><p>232</p></td>
<td><p>1368</p></td>
<td><p>80 @900 MHz</p></td>
<td><p>1.6</p></td>
<td><p>64</p></td>
<td><p>32</p></td>
<td><p>8192</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC IIIi (Jalapeno)</p></td>
<td><p>Sun SME1603</p></td>
<td><p>1064–1593</p></td>
<td><p>V9</p></td>
<td><p>2003</p></td>
<td><p>1×1=1</p></td>
<td><p>0.13</p></td>
<td><p>87.5</p></td>
<td><p>206</p></td>
<td><p>959</p></td>
<td><p>52</p></td>
<td><p>1.3</p></td>
<td><p>64</p></td>
<td><p>32</p></td>
<td><p>1024</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>SPARC64 V (Zeus)</p></td>
<td><p>Fujitsu</p></td>
<td><p>1100–1350</p></td>
<td><p>V9/JPS1</p></td>
<td><p>2003</p></td>
<td><p>1×1=1</p></td>
<td><p>0.13</p></td>
<td><p>190</p></td>
<td><p>289</p></td>
<td><p>269</p></td>
<td><p>40</p></td>
<td><p>1.2</p></td>
<td><p>128</p></td>
<td><p>128</p></td>
<td><p>2048</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p>SPARC64 V+ (Olympus-B)</p></td>
<td><p>Fujitsu</p></td>
<td><p>1650–2160</p></td>
<td><p>V9/JPS1</p></td>
<td><p>2004</p></td>
<td><p>1×1=1</p></td>
<td><p>0.09</p></td>
<td><p>400</p></td>
<td><p>297</p></td>
<td><p>279</p></td>
<td><p>65</p></td>
<td><p>1</p></td>
<td><p>128</p></td>
<td><p>128</p></td>
<td><p>4096</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p>UltraSPARC IV (Jaguar)</p></td>
<td><p>Sun SME1167</p></td>
<td><p>1050–1350</p></td>
<td><p>V9</p></td>
<td><p>2004</p></td>
<td><p>1×2=2</p></td>
<td><p>0.13</p></td>
<td><p>66</p></td>
<td><p>356</p></td>
<td><p>1368</p></td>
<td><p>108</p></td>
<td><p>1.35</p></td>
<td><p>64</p></td>
<td><p>32</p></td>
<td><p>16384</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/UltraSPARC_IV+" title="wikilink">UltraSPARC IV+</a> (Panther)</p></td>
<td><p>Sun SME1167A</p></td>
<td><p>1500–2100</p></td>
<td><p>V9</p></td>
<td><p>2005</p></td>
<td><p>1×2=2</p></td>
<td><p>0.09</p></td>
<td><p>295</p></td>
<td><p>336</p></td>
<td><p>1368</p></td>
<td><p>90</p></td>
<td><p>1.1</p></td>
<td><p>64</p></td>
<td><p>64</p></td>
<td><p>2048</p></td>
<td><p>32768</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/UltraSPARC_T1" title="wikilink">UltraSPARC T1</a> (Niagara)</p></td>
<td><p>Sun SME1905</p></td>
<td><p>1000–1400</p></td>
<td><p>V9 / UA 2005</p></td>
<td><p>2005</p></td>
<td><p>4×8=32</p></td>
<td><p>0.09</p></td>
<td><p>300</p></td>
<td><p>340</p></td>
<td><p>1933</p></td>
<td><p>72</p></td>
<td><p>1.3</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>3072</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>SPARC64 VI (Olympus-C)</p></td>
<td><p>Fujitsu</p></td>
<td><p>2150–2400</p></td>
<td><p>V9/JPS2</p></td>
<td><p>2007</p></td>
<td><p>2×2=4</p></td>
<td><p>0.09</p></td>
<td><p>540</p></td>
<td><p>422</p></td>
<td><p>--</p></td>
<td><p>120</p></td>
<td><p>--</p></td>
<td><p>128</p></td>
<td><p>128</p></td>
<td><p>5120</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/UltraSPARC_T2" title="wikilink">UltraSPARC T2</a> (Niagara 2)</p></td>
<td><p>Sun SME1908A</p></td>
<td><p>1000–1400</p></td>
<td><p>V9 / UA 2007</p></td>
<td><p>2007</p></td>
<td><p>8×8=64</p></td>
<td><p>0.065</p></td>
<td><p>503</p></td>
<td><p>342</p></td>
<td><p>1831</p></td>
<td><p>95</p></td>
<td><p>1.1–1.5</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>4096</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC T2 Plus (Victoria Falls)</p></td>
<td><p>Sun SME1910A</p></td>
<td><p>1200–1400</p></td>
<td><p>V9 / UA 2007</p></td>
<td><p>2008</p></td>
<td><p>8×8=64</p></td>
<td><p>0.065</p></td>
<td><p>503</p></td>
<td><p>342</p></td>
<td><p>1831</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>4096</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p>SPARC64 VII (Jupiter)[2]</p></td>
<td><p>Fujitsu</p></td>
<td><p>2400–2520</p></td>
<td><p>V9/JPS2(?)</p></td>
<td><p>2008</p></td>
<td><p>2×4=8</p></td>
<td><p>0.065</p></td>
<td><p>600</p></td>
<td><p>?</p></td>
<td><p>--</p></td>
<td><p>?</p></td>
<td><p>--</p></td>
<td><p>64</p></td>
<td><p>64</p></td>
<td><p>6144</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p>UltraSPARC RK (<a href="https://ko.wikipedia.org/wiki/Rock_processor" title="wikilink">Rock</a>)[3]</p></td>
<td><p>Sun SME1832</p></td>
<td><p>2300</p></td>
<td><p>V9 / UA__?__</p></td>
<td><p>2009</p></td>
<td><p>2×16=32</p></td>
<td><p>0.065</p></td>
<td><p>?</p></td>
<td><p>396</p></td>
<td><p>2326</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>32</p></td>
<td><p>32 + 8 predecoded bits</p></td>
<td><p>2048</p></td>
<td><p>?</p></td>
</tr>
<tr class="odd">
<td><p>이름</p></td>
<td><p>모델</p></td>
<td><p>주파수<br />
[MHz]</p></td>
<td><p>아키텍처<br />
버전</p></td>
<td><p>출시연도</p></td>
<td><p>스레드<br />
코어 당 × 코어<br />
= Total 스레드</p></td>
<td><p>공정<br />
[µm]</p></td>
<td><p>트랜지스터<br />
[100만]</p></td>
<td><p>다이 크기<br />
[mm²]</p></td>
<td><p>IO 핀</p></td>
<td><p>전력<br />
[W]</p></td>
<td><p>전압<br />
[V]</p></td>
<td><p>1차 데이터 D캐시<br />
[k]</p></td>
<td><p>1차 명령어 캐시<br />
[k]</p></td>
<td><p>2차 캐시<br />
[k]</p></td>
<td><p>3차 캐시<br />
[k]</p></td>
</tr>
</tbody>
</table>

## 함께보기

  - [빌 조이](../Page/빌_조이.md "wikilink")

## 각주

<references />

## 외부 링크

  - [SPARC 인터내셔널](http://www.sparc.org/)

[분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink") [분류:오라클 코퍼레이션](https://ko.wikipedia.org/wiki/분류:오라클_코퍼레이션 "wikilink") [분류:후지쯔](https://ko.wikipedia.org/wiki/분류:후지쯔 "wikilink") [분류:64비트 컴퓨터](https://ko.wikipedia.org/wiki/분류:64비트_컴퓨터 "wikilink") [분류:32비트 컴퓨터](https://ko.wikipedia.org/wiki/분류:32비트_컴퓨터 "wikilink")

1.  Various SPARC V7 implementations were produced by Fujitsu, [LSI Logic](https://ko.wikipedia.org/wiki/LSI_Logic "wikilink"), Weitek, Texas Instruments and Cypress. A SPARC V7 processor generally consisted of several discrete chips, usually comprising an Integer Unit (IU), a [Floating-Point Unit](https://ko.wikipedia.org/wiki/Floating-Point_Unit "wikilink") (FPU), a [Memory Management Unit](https://ko.wikipedia.org/wiki/Memory_Management_Unit "wikilink") (MMU) and 캐시 memory.
2.
3.