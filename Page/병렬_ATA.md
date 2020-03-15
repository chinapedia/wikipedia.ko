> This article is converted from Wikipedia: [ ATA](https://ko.wikipedia.org/wiki/_ATA).


[섬네일](https://ko.wikipedia.org/wiki/파일:ATA_cables.jpg "wikilink") **병렬 ATA**(Parallel ATA, , 이전 이름: 고급 기술 결합/Advanced Technology Attachment, ATA\[1\])은 [개인용 컴퓨터](https://ko.wikipedia.org/wiki/개인용_컴퓨터 "wikilink") 안에서 [하드 디스크](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink"), [CD-ROM](../Page/CD-ROM.md "wikilink") 드라이브와 같은 [기억 장치를](https://ko.wikipedia.org/wiki/기억_장치 "wikilink") 연결하는 [표준](https://ko.wikipedia.org/wiki/표준 "wikilink") [인터페이스이다](https://ko.wikipedia.org/wiki/물리_인터페이스 "wikilink").

병렬 ATA 케이블의 허용 가능한 최대 길이는 18 인치(457 밀리미터)이다.\[2\]\[3\] 이러한 제한으로 인해 이 기술은 일반적으로 내부 컴퓨터 스토리지 인터페이스로 등장한다. 수년 동안 ATA는 이러한 용도로 사용할 때 가장 일반적이면서 가장 값싼 인터페이스를 제공하였다. 더 새로운 시스템에서는 [직렬 ATA로](../Page/직렬_ATA.md "wikilink") 상당수 대체되고 있다.

## 역사

PATA 표준은 원래 "PC/AT Attachment"로 고안되었는데, 주 기능이 [IBM PC/AT와](https://ko.wikipedia.org/wiki/IBM_PC/AT "wikilink") 함께 도입된 16비트 [ISA 버스에](../Page/ISA_버스.md "wikilink") 직접 연결하는 것이었기 때문이다.\[4\] "IBM PC/AT"에서 "AT"는 "Advanced Technology"를 가리키지만 ATA 사양은 단순히 이름을 "AT Attachment"로 사용함으로써 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")과의 잠재적인 상표 문제를 회피한다.

## PATA 인터페이스

[center](https://ko.wikipedia.org/wiki/파일:nappe.svg "wikilink") [직렬 ATA(SATA)가](../Page/직렬_ATA.md "wikilink") 도입될 때까지는 40핀의 단자가 [리본 케이블로](https://ko.wikipedia.org/wiki/리본_케이블 "wikilink") 드라이브를 연결하였으며 이를 PATA(병렬 ATA) 인터페이스라고 한다. 각 케이블은 두 세 개의 단자를 갖추고 있었고, 그 가운데 하나는 컴퓨터 시스템의 남는 부분과 데이터를 주고 받는 어댑터와 장착된다. 나머지 한 두 개의 단자는 드라이브와 연결된다.

PATA 케이블은 16비트의 데이터를 한 번에 전송한다.

과거에는 PATA 리본 케이블로 40선 짜리를 이용했지만, UDMA/66 (UDMA4)이상에서는 80선짜리 케이블을 이용한다. 이 80선 중에 40선은 기존의 40선과 동일하며, 새로운 40선은 [그라운드](https://ko.wikipedia.org/wiki/그라운드 "wikilink")선으로, 이전의 40선과 번갈아가며 위치한다. 이 그라운드선은 신호선 끼리의 capacitive coupling을 줄여서 crosstalk 노이즈를 감소시키는 역할을 한다. Capacitive coupling은 전송 속도가 빨라질수록 문제가 되며, UDMA4 (66MB/s)이상으로 정상적으로 동작하려면 80선 리본케이블이 필요하다. 최근의 [HDD](https://ko.wikipedia.org/wiki/HDD "wikilink")등은 보통 UDMA6를 지원하므로, 80선 케이블을 이용한다.

80선 리본 케이블에서, 선은 80개로 증가했지만 연결 단자의 모양은 40선 리본 케이블과 동일하다. 신호선이 늘어난 것은 아니기 때문이다. 다만, 80선 케이블은 연결 단자에 파란색, 회색, 검은색으로 색이 입혀져있다. (40선 케이블에서 연결 단자는 모두 검은색이었다) 파란 커넥터는 호스트(컴퓨터)와 연결하며, 회색 커넥터는 슬레이브 장치, 검은 커넥터는 마스터 장치와 연결한다. 회색 커넥터의 경우 28번 핀이 연결돼 있지 않아서 호스트가 슬레이브라는 것을 인식할 수 있다.

SATA에서는 이러한 리본 케이블을 이용하지 않는다.

## ATA 표준 및 종류

<table>
<thead>
<tr class="header">
<th><p>표준</p></th>
<th><p>다른 이름</p></th>
<th><p>전송 방식 (MB/초)</p></th>
<th><p>최대 디스크 크기</p></th>
<th><p>새로운 기능</p></th>
<th><p>ANSI 참조</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>pre-ATA</p></td>
<td><p>IDE</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/프로그램_입출력" title="wikilink">PIO</a> 0</p></td>
<td><p>2.1 <a href="https://ko.wikipedia.org/wiki/기가바이트" title="wikilink">GB</a></p></td>
<td><p>22 비트 <a href="https://ko.wikipedia.org/wiki/LBA" title="wikilink">LBA</a></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>ATA-1</p></td>
<td><p>ATA, IDE</p></td>
<td><p>PIO 0, 1, 2 (3.3, 5.2, 8.3)<br />
<a href="https://ko.wikipedia.org/wiki/WDMA_(컴퓨터)" title="wikilink">Single-word DMA</a> 0, 1, 2 (2.1, 4.2, 8.3)<br />
Multi-word DMA 0 (4.2)</p></td>
<td><p>137 GB</p></td>
<td><p>28비트 LBA</p></td>
<td><p><a href="ftp://ftp.t10.org/t13/project/d0791r4c-ATA-1.pdf">X3.221-1994</a><br />
(1999년 이후로 쓰이지 않음)</p></td>
</tr>
<tr class="odd">
<td><p>ATA-2</p></td>
<td><p>EIDE, 고속 ATA,<br />
고속 IDE, 울트라 ATA</p></td>
<td><p>PIO 3, 4: (11.1, 16.6)<br />
Multi-word DMA 1, 2 (13.3, 16.6)</p></td>
<td></td>
<td></td>
<td><p><a href="https://web.archive.org/web/20071203002440/http://www.t10.org/t13/project/d0948r4c-ATA-2.pdf">X3.279-1996</a><br />
(2001년 이후로 쓰이지 않음)</p></td>
</tr>
<tr class="even">
<td><p>ATA-3</p></td>
<td><p>EIDE</p></td>
<td></td>
<td></td>
<td><p><br />
<a href="https://ko.wikipedia.org/wiki/S.M.A.R.T." title="wikilink">S.M.A.R.T.</a>, 보안</p></td>
<td><p><a href="https://web.archive.org/web/20080406222052/http://www.t10.org/t13/project/d2008r7b-ATA-3.pdf">X3.298-1997</a><br />
(2002년 이후로 쓰이지 않음)</p></td>
</tr>
<tr class="odd">
<td><p>ATA/ATAPI-4</p></td>
<td><p>ATA-4, 울트라 ATA/33</p></td>
<td><p>울트라 DMA 0, 1, 2 (16.7, 25.0, 33.3)<br />
aka UDMA/33</p></td>
<td></td>
<td><p>ATAPI (CD-ROM, 테이프 드라이브 등 지원)<br />
오버랩, 큐 명령 집합 기능 (선택 사항),<br />
호스트 보호 영역 (HPA)</p></td>
<td><p><a href="https://web.archive.org/web/20130513233657/http://www.t10.org/t13/project/d1153r18-ATA-ATAPI-4.pdf">NCITS 317-1998</a></p></td>
</tr>
<tr class="even">
<td><p>ATA/ATAPI-5</p></td>
<td><p>ATA-5, 울트라 ATA/66</p></td>
<td><p>울트라 DMA 3, 4 (44.4, 66.7)<br />
aka UDMA/66</p></td>
<td></td>
<td><p>80선 케이블</p></td>
<td><p><a href="https://web.archive.org/web/20110728081430/http://www.t10.org/t13/project/d1321r3-ATA-ATAPI-5.pdf">NCITS 340-2000</a></p></td>
</tr>
<tr class="odd">
<td><p>ATA/ATAPI-6</p></td>
<td><p>ATA-6, 울트라 ATA/100</p></td>
<td><p>UDMA 5 (100)<br />
aka UDMA/100</p></td>
<td><p>144 <a href="https://ko.wikipedia.org/wiki/페타바이트" title="wikilink">PB</a></p></td>
<td><p>48비트 LBA, <a href="https://ko.wikipedia.org/wiki/장치_구성_오버레이" title="wikilink">장치 구성 오버레이</a> (DCO),<br />
소음 자동 관리</p></td>
<td><p><a href="https://web.archive.org/web/20110728081452/http://www.t10.org/t13/project/d1410r3a-ATA-ATAPI-6.pdf">NCITS 361-2002</a></p></td>
</tr>
<tr class="even">
<td><p>ATA/ATAPI-7</p></td>
<td><p>ATA-7, 울트라 ATA/133</p></td>
<td><p>UDMA 6 (133)<br />
aka UDMA/133<br />
SATA/150</p></td>
<td></td>
<td><p><a href="https://ko.wikipedia.org/wiki/시리얼_ATA" title="wikilink">SATA</a> 1.0, 패킷이 아닌 장치의 스트리밍 기능, 긴 논리/물리 섹터 기능</p></td>
<td><p><a href="https://web.archive.org/web/20080406222032/http://www.t10.org/t13/project/d1532v1r4a-ATA-ATAPI-7.pdf">NCITS 397-2005 (1)</a> <a href="https://web.archive.org/web/20080406222054/http://www.t10.org/t13/project/d1532v2r4a-ATA-ATAPI-7.pdf">NCITS 397-2005 (2)</a> <a href="https://web.archive.org/web/20080406222040/http://www.t10.org/t13/project/d1532v3r4a-ATA-ATAPI-7.pdf">NCITS 397-2005 (3)</a></p></td>
</tr>
<tr class="odd">
<td><p>ATA/ATAPI-8</p></td>
<td><p>ATA-8</p></td>
<td><p>—</p></td>
<td></td>
<td><p><a href="../Page/하이브리드_드라이브.md" title="wikilink">하이브리드 드라이브</a>: 중요한 운영 체제 파일의 속도를 높이기 위해 비휘발성 캐시를 사용한다</p></td>
<td><p>진행 중</p></td>
</tr>
</tbody>
</table>

### 전송 방식별 속도

<table>
<caption>전송 방식</caption>
<thead>
<tr class="header">
<th><p>방식</p></th>
<th><p>#</p></th>
<th><p>최대 전송 속도<br />
(MB/초)</p></th>
<th><p>순환 시간</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/프로그램_입출력" title="wikilink">PIO</a></p></td>
<td><p>0</p></td>
<td><p>3.3</p></td>
<td><p>600 ns</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>5.2</p></td>
<td><p>383 ns</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>8.3</p></td>
<td><p>240 ns</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p>11.1</p></td>
<td><p>180 ns</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>16.7</p></td>
<td><p>120 ns</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/WDMA_(컴퓨터)" title="wikilink">싱글 워드 DMA</a></p></td>
<td><p>0</p></td>
<td><p>2.1</p></td>
<td><p>960 ns</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td><p>4.2</p></td>
<td><p>480 ns</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>8.3</p></td>
<td><p>240 ns</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/WDMA_(컴퓨터)" title="wikilink">멀티 워드 DMA</a></p></td>
<td><p>0</p></td>
<td><p>4.2</p></td>
<td><p>480 ns</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>13.3</p></td>
<td><p>150 ns</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>16.7</p></td>
<td><p>120 ns</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3[5]</p></td>
<td><p>20</p></td>
<td><p>100 ns</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4[6]</p></td>
<td><p>25</p></td>
<td><p>80 ns</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>울트라 DMA</p></td>
<td><p>0</p></td>
<td><p>16.7</p></td>
<td><p>240 ns ÷ 2</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td><p>25.0</p></td>
<td><p>160 ns ÷ 2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2 (울트라 ATA/33)</p></td>
<td><p>33.3</p></td>
<td><p>120 ns ÷ 2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>44.4</p></td>
<td><p>90 ns ÷ 2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4 (울트라 ATA/66)</p></td>
<td><p>66.7</p></td>
<td><p>60 ns ÷ 2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5 (울트라 ATA/100)</p></td>
<td><p>100</p></td>
<td><p>40 ns ÷ 2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6 (울트라 ATA/133)</p></td>
<td><p>133</p></td>
<td><p>30 ns ÷ 2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7 (울트라 ATA/167)[7]</p></td>
<td><p>167</p></td>
<td><p>24 ns ÷ 2</p></td>
<td></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [마스터 슬레이브](https://ko.wikipedia.org/wiki/마스터_슬레이브 "wikilink")
  - [AHCI](https://ko.wikipedia.org/wiki/AHCI "wikilink")

## 참조

## 외부 링크

  - [IDE/ATA 인터페이스 간단 보기 및 역사](http://www.pcguide.com/ref/hdd/if/ide/over-c.html)
  - [ATA/ATAPI 역사](https://web.archive.org/web/20080228090358/http://www.ata-atapi.com/hist.htm)

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")

1.  [Documentation](http://support.euro.dell.com/support/edocs/systems/opgx240/ko/ug/1glossry.htm)
2.
3.
4.
5.  [콤팩트플래시](https://ko.wikipedia.org/wiki/콤팩트플래시 "wikilink") 2.1
6.
7.