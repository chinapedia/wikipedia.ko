> This article is converted from Wikipedia: [DDR4 SDRAM](https://ko.wikipedia.org/wiki/DDR4_SDRAM).


[컴퓨팅](../Page/컴퓨팅.md "wikilink") 분야에서 **DDR4 SDRAM**은 2배속 [SDRAM](../Page/SDRAM.md "wikilink")의 일종으로, 2014년에 출시되었다.\[1\]\[2\]\[3\] 'DDR4 SDRAM'은 'double data rate 4th generation synchronous dynamic random-access memory'(4세대 2배속 동기 동적 랜덤 접근 기억장치)를 줄인 말이다.

1970년대 초 이후로 사용되어 온 DRAM들 중 가장 최근의 변종이 되며,\[4\] [DDR2 SDRAM과](../Page/DDR2_SDRAM.md "wikilink") [DDR3 SDRAM](../Page/DDR3_SDRAM.md "wikilink") 기술의 뒤를 이었다. DDR4 SDRAM은 서로 다른 신호 전압, 물리적 인터페이스, 기타 요인으로 인해 이전 세대의 RAM과는 호환되지 않는다.

DDR4 SDRAM은 2015년 2/4분기에 [ECC 메모리에](../Page/ECC_메모리.md "wikilink") 주력하여 시장에 공개되었고,\[5\] 비 ECC 메모리 모듈은 DDR4 메모리를 사용하는 [하스웰-E의](../Page/하스웰_\(마이크로아키텍처\).md "wikilink") 출시와 함께 2014년 3/4분기에 출시되었다.\[6\]

## 특징

이전 기종인 DDR3에 비해 DDR4가 좋은 점으로는 모듈 밀도가 높고, 높은 [비트 전송률과](../Page/비트레이트.md "wikilink") 함께 필요한 전압이 낮음을 들 수 있다. DDR4의 기준은 이론적으로 DIMM이 용량 512[GiB까지](https://ko.wikipedia.org/wiki/기비바이트 "wikilink") 가능한데, DDR3의 경우 이론적으로 DIMM당 128GiB이 최고였다.\[7\] DDR4는 1.2 V에 800에서 1600 MHz의 주파수로 운용되는데, DDR3는 1.5 V 또는 1.65 V에서 400에서 1067 MHz로 기동한다.\[8\]\[9\]\[10\] 2014년 8월 저전력 기준이 확정되지는 않았지만, 저전력 DDR4는 DDR3의 저전력 기준인 1.35V의 운용 전압보다 낮은 1.05V로 구동이 된다.\[11\]

### DIMM 차이

DDR4는 240핀 DDR-2/DDR-3 DIMM과 비슷한 284핀 DIMM으로 출시된다.\[12\] DDR4 SO-DIMM은 256핀을 지니며 0.5mm 더 공간이 좁아졌고 1.0 mm 더 넓어졌으나 기존과 동일한 30 mm 높이를 유지한다.\[13\] 최소 메모리용량은 4GB이며 32비트는없다.

### 최종 규격

2012년 9월 25일, 메모리 표준 규격을 정하는 JEDEC (Joint Electron Device Engineering Council ) 은 차기 메모리인 DDR4 의 최종 규격을 발표했다. 이에 의하면 핀당 전송 속도는 최소 1.6 GT/s (Gigatransfer per second) 에서 최대 3.2 GT/s 가 기본이지만 이전 DDR3 이하 메모리에서 그랬듯이 이보다 더 빠른 규격이 등장할 수도 있을 것으로 예상되었다. 또한 DDR4 메모리는 기본이 1.2 V 로 작동해 1.5 V 로 작동하는 DDR3 메모리보다 전력 소모가 줄어들고 속도는 빨라졌기 때문에 도입되면 큰 이점이 있을 것으로 기대되었다.\[14\]

## 모듈

### JEDEC 표준 DDR4 모듈

JEDEC 표준 DDR4 모듈은 다음과 같다.\[15\]\[16\]

<table>
<thead>
<tr class="header">
<th><p>표준<br />
이름</p></th>
<th><p>메모리<br />
클럭 <small>(MHz)</small></p></th>
<th><p>입출력 버스<br />
클럭 <small>(MHz)</small></p></th>
<th><p>데이터<br />
속도 <small>(<a href="https://ko.wikipedia.org/wiki/전송" title="wikilink">MT/s</a>)</small></p></th>
<th><p>모듈<br />
이름</p></th>
<th><p>최고 전송<br />
속도 <small>(MB/s)</small></p></th>
<th><p>타이밍,<br />
<small>CL-tRCD-tRP</small></p></th>
<th><p>CAS 레이턴시<br />
<small>(ns)</small></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DDR4-1600J*<br />
DDR4-1600K<br />
DDR4-1600L</p></td>
<td><p>200</p></td>
<td><p>800</p></td>
<td><p>1600</p></td>
<td><p>PC4-12800</p></td>
<td><p>12800</p></td>
<td><p>10-10-10<br />
11-11-11<br />
12-12-12</p></td>
<td><p>12.5<br />
13.75<br />
15</p></td>
</tr>
<tr class="even">
<td><p>DDR4-1866L*<br />
DDR4-1866M<br />
DDR4-1866N</p></td>
<td><p>233.33</p></td>
<td><p>933.33</p></td>
<td><p>1866.67</p></td>
<td><p>PC4-14900</p></td>
<td><p>14933.33</p></td>
<td><p>12-12-12<br />
13-13-13<br />
14-14-14</p></td>
<td><p>12.857<br />
13.929<br />
15</p></td>
</tr>
<tr class="odd">
<td><p>DDR4-2133N*<br />
DDR4-2133P<br />
DDR4-2133R</p></td>
<td><p>266.67</p></td>
<td><p>1066.67</p></td>
<td><p>2133.33</p></td>
<td><p>PC4-17000</p></td>
<td><p>17066.67</p></td>
<td><p>14-14-14<br />
15-15-15<br />
16-16-16</p></td>
<td><p>13.125<br />
14.063<br />
15</p></td>
</tr>
<tr class="even">
<td><p>DDR4-2400P*<br />
DDR4-2400R<br />
DDR4-2400T<br />
DDR4-2400U</p></td>
<td><p>300</p></td>
<td><p>1200</p></td>
<td><p>2400</p></td>
<td><p>PC4-19200</p></td>
<td><p>19200</p></td>
<td><p>15-15-15<br />
16-16-16<br />
17-17-17<br />
18-18-18</p></td>
<td><p>12.5<br />
13.32<br />
14.16<br />
15</p></td>
</tr>
<tr class="odd">
<td><p>DDR4-2666T<br />
DDR4-2666U<br />
DDR4-2666V<br />
DDR4-2666W</p></td>
<td><p>333.33</p></td>
<td><p>1333.33</p></td>
<td><p>2666.67</p></td>
<td><p>PC4-21333</p></td>
<td><p>21333.33</p></td>
<td><p>17-17-17<br />
18-18-18<br />
19-19-19<br />
20-20-20</p></td>
<td><p>12.75<br />
13.50<br />
14.25<br />
15</p></td>
</tr>
<tr class="even">
<td><p>DDR4-2933V<br />
DDR4-2933W<br />
DDR4-2933Y<br />
DDR4-2933AA</p></td>
<td><p>366.67</p></td>
<td><p>1466.67</p></td>
<td><p>2933.33</p></td>
<td><p>PC4-23466</p></td>
<td><p>23466.67</p></td>
<td><p>19-19-19<br />
20-20-20<br />
21-21-21<br />
22-22-22</p></td>
<td><p>12.96<br />
13.64<br />
14.32<br />
15</p></td>
</tr>
<tr class="odd">
<td><p>DDR4-3200W<br />
DDR4-3200AA<br />
DDR4-3200AC</p></td>
<td><p>400</p></td>
<td><p>1600</p></td>
<td><p>3200</p></td>
<td><p>PC4-25600</p></td>
<td><p>25600</p></td>
<td><p>20-20-20<br />
22-22-22<br />
24-24-24</p></td>
<td><p>12.50<br />
13.75<br />
15</p></td>
</tr>
</tbody>
</table>

\* 선택 사항

## 각주

### 보충 설명

<references group="주해" />

[분류:SDRAM](https://ko.wikipedia.org/wiki/분류:SDRAM "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  일부 DDR3 제품은 원래보다 높은 1600 MHz까지의 속도로 작동되기도 한다.
10.
11. .
12.
13.
14.
15.
16.