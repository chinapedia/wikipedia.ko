> This article is converted from Wikipedia: [IEEE 802.11n-2009](https://ko.wikipedia.org/wiki/IEEE_802.11n-2009).


**IEEE 802.11n-2009** 또는 **IEEE 802.11n**은 기존 표준인 [IEEE 802.11a와](https://ko.wikipedia.org/wiki/IEEE_802.11a "wikilink") [IEEE 802.11g의](https://ko.wikipedia.org/wiki/IEEE_802.11g "wikilink") 대역폭을 향상시키기 위한 [IEEE 802.11](https://ko.wikipedia.org/wiki/IEEE_802.11 "wikilink") 무선 네트워킹 표준의 개정판이다. IEEE 802.11n는 40MHz의 채널 대역을 사용함으로써 최대 데이터 전송률을 54Mbps에서 600Mbps로 상당히 향상시켰다. 와이파이 연합(Wi-Fi Alliance)은 2007년부터 IEEE 802.11n의 물리적 규격에 대한 드래프트(draft, 초안) 2.0을 기반으로 드래프트-N 제품들과의 상호 연동성에 대한 인증 업무를 수행하고 있다. 연합은 드래프트 2.0 이후에 추가된 성능 향상에 대한 호환성 테스트를 업그레이드하고 있다. 또한 모든 드래프트-N을 바탕으로 인증을 거친 제품들이 최종 표준을 마친 제품들과도 여전히 호환 가능하다고 발표하였다. 2009년 9년 16일, [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink")는 IEEE 802.11n 표준을 최종적으로 비준하였으며, 드래프트 2.0을 대부분 수용하였다.\[1\]

## 개요

IEEE 802.11n은 IEEE 802.11의 개정판이다. IEEE 802.11n은 기존 802.11 표준 위에 [MIMO](../Page/MIMO.md "wikilink")(multiple-input multiple-output)와 40 MHz 채널 대역폭을 가진 물리 계층(physical layer), 맥 계층(MAC layer)의 프레임 집적(frame aggregation) 기술을 추가하여 만들어졌다.

[MIMO](../Page/MIMO.md "wikilink")는 하나의 안테나를 사용하는 것보다 더 많은 정보를 송수신 할 수 있도록 여러 개의 안테나를 사용하는 기술이다. 이렇게 하기 위한 한 가지 방법이 바로 공간 분할 다중화(Spatial Division Multiplexing) 기술이다. SDM은 여러 개의 독립적인 데이터 스트림을 다중화한다. [MIMO](../Page/MIMO.md "wikilink") SDM은 데이터 스트림이 증가하는 것에 따라 데이터 전송률을 상당히 향상시킨다. 각각의 스트림에는 각각의 안테나가 필요하다. 또한 [MIMO](../Page/MIMO.md "wikilink") 기술은 각각의 [MIMO](../Page/MIMO.md "wikilink") 안테나를 위해 분리된 라디오 주파수 체인과 아날로그 디지털 컨버터를 요구한다. 따라서 [MIMO](../Page/MIMO.md "wikilink") 기술을 사용하지 않는 시스템에 비해 더 많은 구현 비용이 필요하다.

40MHz채널 대역폭은 802.11n에 포함된 또다른 특성이다. 이것은 기존의 802.11 PHY가 데이터를 전송하는 데 사용하던 20 MHz 채널 대역을 두 배로 넓힌 것이다. 이것은 하나의 20 MHz 채널을 사용하는 것에 비해 물리 계층에서의 데이터 전송률을 두 배로 높여 준다. 이것은 5 GHz 모드에서 사용할 수 있다. 같은 채널을 사용하는 다른 802.11 시스템이나 블루투스와 같은 802.11이 아닌 시스템을 방해하지 않는 방법을 알고 있는 경우 2.4GHz에서도 사용할 수 있다.\[2\]

MIMO와 넓은 채널 대역폭을 이용해서 물리 계층의 전송 속도를 802.11a (5 GHz)나 802.11g (2 GHz)에 비해 향상시킬 수 있다.\[3\]

### 데이터 인코딩

[MIMO](../Page/MIMO.md "wikilink") 연결을 활용하기 위해서 송신부와 수신부는 각각 프리코딩(precoding)과 애프터코딩(aftercoding) 기술을 사용한다. 프리코딩(precoding)은 [빔포밍](../Page/빔포밍.md "wikilink")과 spatial coding을 포함한다. [빔포밍](../Page/빔포밍.md "wikilink")은 디코딩 단계에서 수신한 신호 품질을 향상시켜준다. Spatial coding은 데이터 전송률(throughput)을 향상시켜준다.

#### 안테나 개수

데이터 스트림의 수는 링크 양쪽에서 사용하는 안테나 개수 이하로 제한된다. 라디오에 따라 때로는 그보다 더 작은 숫자의 스트림으로 제한하기도 한다. 특정한 라디오의 능력치를 표현하기 위해서 \(a \times b \colon c\) 와 같은 표현식을 자주 사용한다. a는 최대 송신부의 안테나 혹은 라디오에서 사용하고 있는 RF chain의 개수를 나타낸다. b는 수신부의 안테나 혹은 라디오에서 사용하고있는 RF chain의 개수를 나타낸다. c는 라디오에서 사용 가능한 최대 스트림의 개수를 의미한다. 예를 들어 2개의 송신 안테나와 3개의 수신안테나를 가지고 있고 2개의 데이터 스트림을 송수신할 수 있는 라디오 장치는 \(2 \times 3 \colon 2\) 와 같이 표시할 수 있다. 802.11n draft는 최대 \(4 \times 4 \colon 4\) 를 허용한다. 일반적인 11n 장비의 경우 \(2 \times 2 \colon 2\), \(2 \times 3 \colon 2\)혹은 \(3 \times 3 \colon 2\)를 사용한다. 이 세가지 설정 모두 같은 최대 데이터 전송률을 가지고 있다.

### 데이터 전송률

초당 최대 600Mbit의 데이터 전송률은 40 MHz 폭의 채널에서 4개의 최대 스트림을 사용한 경우에만 가능하다. 여러 가지 설계와 그에 따른 전송 속도가 표준에 따라 MCS(Modulation and Coding Scheme)에 정의되어 있다. 각 모드별 최대 전송 속도는 다음 표와 같다.

<table>
<thead>
<tr class="header">
<th><p>MCS<br />
Index</p></th>
<th><p>Spatial<br />
Streams</p></th>
<th><p>Modulation<br />
Type</p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/Code_rate" title="wikilink">Coding<br />
Rate</a></p></th>
<th><p>Data Rate Mb/s</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>20 MHz 채널</p></td>
<td><p>40 MHz 채널</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>800ns <a href="https://ko.wikipedia.org/wiki/보호_구간" title="wikilink">GI</a></p></td>
<td><p>400ns <a href="https://ko.wikipedia.org/wiki/보호_구간" title="wikilink">GI</a></p></td>
<td><p>800ns <a href="https://ko.wikipedia.org/wiki/보호_구간" title="wikilink">GI</a></p></td>
<td><p>400ns <a href="https://ko.wikipedia.org/wiki/보호_구간" title="wikilink">GI</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>0</p></td>
<td><p>1</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/BPSK" title="wikilink">BPSK</a></p></td>
<td><p>1/2</p></td>
<td><p>6.50</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>1</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/QPSK" title="wikilink">QPSK</a></p></td>
<td><p>1/2</p></td>
<td><p>13.00</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>1</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/QPSK" title="wikilink">QPSK</a></p></td>
<td><p>3/4</p></td>
<td><p>19.50</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p>1</p></td>
<td><p>16-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>1/2</p></td>
<td><p>26.00</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>1</p></td>
<td><p>16-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>3/4</p></td>
<td><p>39.00</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>1</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>2/3</p></td>
<td><p>52.00</p></td>
</tr>
<tr class="odd">
<td><p>6</p></td>
<td><p>1</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>3/4</p></td>
<td><p>58.50</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>1</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>5/6</p></td>
<td><p>65.00</p></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td><p>2</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/BPSK" title="wikilink">BPSK</a></p></td>
<td><p>1/2</p></td>
<td><p>13.00</p></td>
</tr>
<tr class="even">
<td><p>9</p></td>
<td><p>2</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/QPSK" title="wikilink">QPSK</a></p></td>
<td><p>1/2</p></td>
<td><p>26.00</p></td>
</tr>
<tr class="odd">
<td><p>10</p></td>
<td><p>2</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/QPSK" title="wikilink">QPSK</a></p></td>
<td><p>3/4</p></td>
<td><p>39.00</p></td>
</tr>
<tr class="even">
<td><p>11</p></td>
<td><p>2</p></td>
<td><p>16-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>1/2</p></td>
<td><p>52.00</p></td>
</tr>
<tr class="odd">
<td><p>12</p></td>
<td><p>2</p></td>
<td><p>16-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>3/4</p></td>
<td><p>78.00</p></td>
</tr>
<tr class="even">
<td><p>13</p></td>
<td><p>2</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>2/3</p></td>
<td><p>104.00</p></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p>2</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>3/4</p></td>
<td><p>117.00</p></td>
</tr>
<tr class="even">
<td><p>15</p></td>
<td><p>2</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>5/6</p></td>
<td><p>130.00</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>3</p></td>
<td><p>...</p></td>
<td><p>...</p></td>
<td><p>...</p></td>
</tr>
<tr class="even">
<td><p>23</p></td>
<td><p>3</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>5/6</p></td>
<td><p>195.00</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>4</p></td>
<td><p>...</p></td>
<td><p>...</p></td>
<td><p>...</p></td>
</tr>
<tr class="even">
<td><p>31</p></td>
<td><p>4</p></td>
<td><p>64-<a href="https://ko.wikipedia.org/wiki/QAM" title="wikilink">QAM</a></p></td>
<td><p>5/6</p></td>
<td><p>260.00</p></td>
</tr>
</tbody>
</table>

### 물리계층(PHY) 동작 모드

1.  Non-HT 모드: 기존에 있던 11a, 11b, 11g과의 통신을 지원
2.  Mixed 모드: 기존의 통신과 11n에서 새로 채택한 HT(High Throughput) 모드를 모두 지원
3.  Green Field 모드: HT 모드만을 지원

### 맥 계층(Mac layer) 프레임 집적(frame aggregation)

물리 계층에서의 전송률 향상은 contention process, interframe spacing, PHY level headers (Preamble + PLCP), acknowledgment frames 과 같은 802.11 프로토콜의 오버 헤드 때문에 사용자 수준에서의 전송률을 어느 정도 이상 향상시켜 주지 못한다. 맥 계층(MAC layer)에서 성능 향상을 위해 제공하는 가장 주된 방법은 프레임 집적(frame aggregation)이다. 두 가지 종류의 집적이 정의되어 있다.

1.  층 서비스 데이터 유닛의 집적 (MSDU 집적 또는 A-MSDU 라고 불림)
2.  MAC 프로토콜 데이터 유닛의 집적 (MPDU 집적 또는 A-MPDU 라고 불림)

프레임 집적은 여러 개의 [MSDU](https://ko.wikipedia.org/wiki/MSDU "wikilink")나 [MPDU](https://ko.wikipedia.org/wiki/MPDU "wikilink") 패킷을 하나로 묶어 여러 개의 패킷을 각각 따로 전송하는 데 드는 오버헤드를 줄임으로써 사용자 수준의 전송률을 향상시키는 것이다. A-MPDU 집적은 802.11e에서 도입되고 802.11n에서 최적화된 집단 ACK(Blocking Acknowledgement)을 요구한다.

#### A-MSDU

우선 순위가 같고 동일한 목적지로 향하는 다수의 MSDU를 모아 하나의 A-MSDU 패킷으로 전송하는 방법. A-MSDU 내의 각 MSDU는 sub-frame 헤더에 의해 구분된다. A-MSDU는 일반 MSDU 패킷과 동일하게 취급된다.

## 사용 전략

가장 빠른 전송률을 얻기 위해서는 802.11n 5 GHz 네트워크를 사용하는 것이 좋다. 5 GHz 대역은 2.4 GHz 대역에 비해 적은 무선 간섭과 적은 채널 중복 때문에 상대적으로 더 나은 능력을 가지고 있다.\[4\] 현재까지 대부분의 컴퓨터에서 802.11b/g 모드를 사용하고 있기 때문에 802.11n 만을 허용하는 네트워크(802.11n-only)는 비효율적이다. 오래된 컴퓨터에서 802.11n 만을 허용하는 네트워크를 사용하기 위해서는 호환되지 않는 기존의 WIFI 카드를 교체하거나 혹은 컴퓨터 전체를 교체해야 한다. 따라서 단기적으로는 802.11n 하드웨어가 널리 쓰일 때 까지 802.11b/g/n 이 혼합된 네트워크를 사용하는 것이 효율적이다. 802.11b/g/n이 혼합된 모드를 사용하는 경우 두 개의 라디오를 사용할 수 있는 AP를 이용하여 802.11b/g 트래픽은 2.4 GHz 대역으로 802.11n 트래픽은 5 GHz 대역으로 분리하여 사용하는 것이 일반적으로 가장 좋다.\[5\]

### 11n 칩셋

현재 출시된 11n 라우터 혹은 공유기의 경우 대부분 RealTek 사의 칩셋, Atheros(Qualcomm), MediaTek(Ralink) 사의 칩셋을 사용하고 있다. 이 외에도 Broadcom, Marvell, Intel 등의 회사가 칩셋을 개발하여 출시하고 있다. 11n 표준이 확정된지 얼마 되지 않았기 때문에 칩셋에 따라 적용된 11n 표준이 다른 경우가 있으므로 같은 칩셋으로 되어있는 장비를 짝지어 사용하는 것이 좋다.

## 제약

11N 표준은 보안상 허점이 발견된 WEP와 TKIP은 11N의 HT(High Throughput)모드에서 사용하지 않도록 정하고 있다. 11N에서 WEP나 WPA TKIP으로 접속하려는 경우 54Mbps의 속도로 낮아진 상태에서 동작하게 된다. 즉 11g 모드에서 동작하는 것과 마찬가지가 된다.

## 각주

## 외부 링크

  - [IEEE 802.11n 드래프트 2.0 - Wi-Fi Alliance](https://web.archive.org/web/20111027065400/http://www.wi-fi.org/files/kc/WFA_802_11n_Industry_June07.pdf)

[분류:IEEE 802.11](https://ko.wikipedia.org/wiki/분류:IEEE_802.11 "wikilink") [분류:무선 네트워크](https://ko.wikipedia.org/wiki/분류:무선_네트워크 "wikilink") [분류:홈 네트워킹](https://ko.wikipedia.org/wiki/분류:홈_네트워킹 "wikilink") [분류:통신공학](https://ko.wikipedia.org/wiki/분류:통신공학 "wikilink") [분류:통신](https://ko.wikipedia.org/wiki/분류:통신 "wikilink")

1.
2.  <https://mentor.ieee.org/802.11/dcn/09/11-09-0576-03-000n-sp2-40mhz-coexistence-cids-presentation.ppt>
3.
4.
5.