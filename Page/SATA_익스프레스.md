> This article is converted from Wikipedia: [SATA ](https://ko.wikipedia.org/wiki/SATA_).


**SATA 익스프레스**(SATA Express, Serial ATA Express의 준말, 가끔 비공식적으로 SATAe로 줄여서 언급)는 [시리얼 ATA](https://ko.wikipedia.org/wiki/SATA "wikilink")(SATA)와 [PCI 익스프레스](https://ko.wikipedia.org/wiki/PCI_익스프레스 "wikilink")(PCIe) 기억 장치들을 둘 다 지원하는 [컴퓨터 버스](https://ko.wikipedia.org/wiki/컴퓨터_버스 "wikilink") 인터페이스로서, 처음에 [SATA 3.2](https://ko.wikipedia.org/wiki/SATA "wikilink") 사양으로 표준화되었다.\[1\] 호스트 측의 SATA 익스프레스의 단자는 표준 [3.5인치 SATA 데이터 단자와](https://ko.wikipedia.org/wiki/3.5인치_SATA_데이터_단자 "wikilink") [하위 호환되며](https://ko.wikipedia.org/wiki/하위_호환성 "wikilink"),\[2\] 기억 장치에 대한 순수 PCI 익스프레스 연결로서 두 개의 [PCI 익스프레스 레인도](https://ko.wikipedia.org/wiki/PCI_익스프레스_레인 "wikilink") 제공한다.\[3\]

각 주요 버전을 통해 SATA 인터페이스의 네티이브 속도를 두 배로 만들지 않는 대신, SATA 3.2 사양은 PCI 익스프레스 [버스를](https://ko.wikipedia.org/wiki/컴퓨터_버스 "wikilink") 포함하여 [SATA 3.0](https://ko.wikipedia.org/wiki/SATA_3.0 "wikilink") 속도 제한인 6 [Gbit/초](https://ko.wikipedia.org/wiki/Gbit/초 "wikilink") 보다 더 높은 데이터 전송 속도를 달성한다. SATA 인터페이스의 설계자는 네이티브 SATA 속도를 두 배로 만드는 것은 [솔리드 스테이트 드라이브](https://ko.wikipedia.org/wiki/솔리드_스테이트_드라이브 "wikilink")(SSD) 기술의 진보를 따라잡는데 너무 많은 시간이 걸리고,\[4\] SATA 표준에 너무 많은 변경이 필요하며 기존 PCI 익스프레스 버스에 비해 전력 소비량이 훨씬 더 커질 것이라고 결론내렸다.\[5\]\[6\] 널리 채택된 컴퓨터 버스인 PCI 익스프레스는 충분한 대역을 제공하면서도 더 빠른 추가 [레인을](https://ko.wikipedia.org/wiki/PCI_익스프레스_레인 "wikilink") 사용하여 쉬운 확장을 허용한다.\[7\]

논리 인터페이스 수준의 레거시 [AHCI](https://ko.wikipedia.org/wiki/AHCI "wikilink")를 지원할 뿐 아니라 SATA 익스프레스는 또한 PCI 익스프레스 부착 기억 장치에 대해 [NVM 익스프레스](../Page/NVM_익스프레스.md "wikilink")(NVMe)를 논리 장치 인터페이스로 지원한다. AHCI에 대한 지원이 레거시 SATA 장치와 레거시 [운영 체제와의](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 소프트웨어 수준의 하위 호환성을 보장하지만, NVM 익스프레스는 [병렬로](https://ko.wikipedia.org/wiki/병렬화 "wikilink") 운영되는 수많은 [입출력](https://ko.wikipedia.org/wiki/입출력 "wikilink") 기능을 수행함으로써 고속의 PCI 익스프레스 기억 장치를 완전히 이용하도록 설계되어 있다.\[8\]

## 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:SATA_Express_connectors_on_a_computer_motherboard.jpg "wikilink") 시리얼 ATA (SATA) 인터페이스는 본래는 주로 하드 디스크 드라이브(HDD)와 통신하기 위해 설계되었으며, 각 주요 버전별로 네이티브 속도가 두 배가 되었다. 최대 SATA 전송 속도는 SATA 1.0 (2003년 표준화)에서 1.5 Gbit/초, SATA 2.0 (2004년 표준화)에서 3 Gbit/초, SATA 3.0 (2009년 표준화)에서 6 Gbit/초로 발전하였다.\[9\] SATA는 점차 솔리드 스테이트 드라이브(SSD)로까지 채택되었으나 SSD와 하이브리드 드라이브의 속도가 시간이 지남에 따라 증가함에 따라 더 빠른 인터페이스에 대한 필요성이 대두되었다. 예를 들어, 2009년 초에 출시된 일부 SSD들은 이미 SATA 1.0의 능력을 뛰어넘었으며 SATA 2.0 최대 전송 속도에 근접하였던 반면\[10\], 2013년 하반기 고성능 컨슈머 SSD는 이미 SATA 3.0 속도 제한을 넘어섰고 훨씬 더 빠른 인터페이스가 필요하게 되었다.\[11\]\[12\]

필요한 속도 증가에 대한 각기 다른 접근을 평가할 때, SATA 인터페이스의 설계자들은 SATA 인터페이스를 확장하여 네이티브 속도를 초당 12Gbit로 확대하는 데 2년 이상 필요할 것이며 이러한 접근은 SSD 기술의 발전을 따라잡는데 부적절하다고 결론내렸다.\[13\] 동시에 네이티브 SATA 속도를 12 Gbit/초로 증가시키면 SATA 표준에 너무 많은 변화가 필요하여 이미 널리 채택된 PCI 익스프레스 버스와 비교하면 더 많은 비용과 더 낮은 전력 효율성을 보이게 된다. 그러므로 PCI 익스프레스가 SATA 인터페이스의 설계자들에 의해 [SATA 3.2](https://ko.wikipedia.org/wiki/SATA_3.2 "wikilink") 리비전의 일부로 채택되었다. (2013년 표준화됨) 이는 SATA 사양을 확장함과 동시에 동일한 하위 호환 단자의 PCI 익스프레스 인터페이스를 제공하여 기존의 기술을 재이용함으로써 훨씬 더 빠른 속도를 낼 수 있게 하였다.\[14\]\[15\]

또, 일부 업체들은 자신들만의 사유 논리 인터페이스를 그들의 [기업형](https://ko.wikipedia.org/wiki/엔터프라이즈_스토리지 "wikilink") 플래시 기반 스토리지 제품에 사용하여 PCI 익스프레스 버스를 통해 연결하게 한다. 이러한 스토리지 제품들은 여러 PCI 익스프레스 레인을 한데 묶지만 [사유](https://ko.wikipedia.org/wiki/사유_소프트웨어 "wikilink") 드라이버와 호스트 인터페이스를 통해 운영 체제와 통신한다.\[16\]\[17\] 게다가, 2014년 6월 기준으로 사유 논리 인터페이스로서 NVM 익스프레스를 이용한 유사 기업형 스토리지 제품들이 있으며 이 또한 여러 개의 PCI 익스프레스 레인들을 한데 묶는다.\[18\]

## 기능

[섬네일](https://ko.wikipedia.org/wiki/파일:SATA_Express_interface.svg "wikilink") SATA 익스프레스 인터페이스는 동일한 호스트 측 SATA 익스프레스 단자를 통해 두 개의 PCI 익스프레스 2.0 또는 3.0 레인과 두 개의 SATA 3.0 (6 Gbit/초) 포트를 노출시킴으로써 PCI 익스프레스와 SATA 기억 장치를 둘 다 지원한다. 노출된 PCI 익스프레스 레인은 추가적인 버스 추상화 계층 없이 호스트와 기억 장치 간의 순수 PCI 익스프레스 연결을 제공한다.\[19\]\[20\] 2013년 8월 기준으로 골드 리비전에 있는 [SATA 리비전 3.2](https://ko.wikipedia.org/wiki/SATA_3.2 "wikilink") 사양은 SATA 익스프레스를 표준화하며 하드웨어 레이아웃과 전기적 매개변수를 규정한다.\[21\]\[22\]

PCI 익스프레스를 선택하면 또한 여러 레인과 각기 다른 버전의 PCI 익스프레스를 사용하여 SATA 익스프레스 인터페이스의 성능을 확장할 수 있다. 더 자세히 설명하면, 두 개의 PCI 익스프레스 2.0 레인을 사용하면 총 1 [GB](https://ko.wikipedia.org/wiki/기가바이트 "wikilink")/초의 대역을 제공하며, 이론상 2 × 5 [GT](https://ko.wikipedia.org/wiki/기가트랜스퍼 "wikilink")/초의 순수 데이터 속도, 효율이 좋을 때의 실질적으로는 1000 [MB](https://ko.wikipedia.org/wiki/메가바이트 "wikilink")/초의 [8b/10b 인코딩과](https://ko.wikipedia.org/wiki/8b/10b_인코딩 "wikilink") 맞먹는 반면 두 개의 [PCI 익스프레스 3.0를](https://ko.wikipedia.org/wiki/PCI_익스프레스_3.0 "wikilink") 사용하면 2 GB/초에 가까운 성능을 제공하며 이론적으로 2 × 8 GT/초의 순수 데이터 속도를, 효율이 좋을 때의 실질적으로는 1969 MB/초와 맞먹는다.\[23\]\[24\]

논리 장치 인터페이스의 경우 3가지 옵션이 지원되며 그 외에 SATA 익스프레스 컨트롤러에 연결되는 기억 장치와의 통신을 위한 명령 집합도 제공된다:\[25\]\[26\]

  - 레거시 SATA
    레거시 SATA 장치와의 [하위 호환성을](https://ko.wikipedia.org/wiki/하위_호환성 "wikilink") 위해 사용되며 AHCI 드라이버 및 SATA 익스프레스 컨트롤러가 제공하는 레거시 SATA 3.0 (6 Gbit/초) 포트를 통해 통신한다.

<!-- end list -->

  - AHCI를 사용하는 PCI 익스프레스
    PCI 익스프레스 SSD를 위해 사용되며 [AHCI](https://ko.wikipedia.org/wiki/AHCI "wikilink") 드라이버 및 제공되는 PCI 익스프레스 레인을 통해 통신하며, PCI 익스프레스 SSD 접근을 위하 AHCI를 사용하므로 최적의 성능을 전달하지는 않지만 운영 체제의 폭넓은 SATA 지원을 통한 하위 호환성을 제공한다. AHCI는 시스템의 [호스트 버스 어댑터](https://ko.wikipedia.org/wiki/호스트_버스_어댑터 "wikilink")(HBA)의 목적이 CPU/메모리 하위 시스템을 훨씬 더 느린, 회전하는 [자기 매체](https://ko.wikipedia.org/wiki/자기_디스크 "wikilink") 기반의 스토리지 하위 시스템과 연결할 목적이었던 당시에 개발되었다. 그러므로 AHCI는 회전하는 매체가 아닌 [DRAM](https://ko.wikipedia.org/wiki/DRAM "wikilink")과 같이 동작하는 SSD 장치에 적용할 때 [비효율성을](https://ko.wikipedia.org/wiki/NVMe_vs_AHCI "wikilink") 갖고 있다.

<!-- end list -->

  - NVMe를 사용하는 PCI 익스프레스
    PCI 익스프레스 SSD에 사용되며 [NVMe](https://ko.wikipedia.org/wiki/NVMe "wikilink") 드라이버 및 제공되는 PCI 익스프레스 레인을 통해 통신한다. 특별히 PCI 익스프레스 SSD와 통신하기 위해 설계되고 최적화된 고성능의 확장 가능한 호스트 컨트롤러 인터페이스이다.

## 단자

[섬네일|upright=1.7|right|SATA 익스프레스 호스트 측 단자는 이전에 "호스트 플러그"라고 불렸으며 공식적으로는 "호스트 플러그"라고 부른다. 이는 SATA 익스프레스와 레거시 3.5인치 SATA 데이터 케이블을 모두 허용한다.\[27\]\[28\]](https://ko.wikipedia.org/wiki/파일:SATA_Express_motherboard_connection.svg "wikilink") SATA 익스프레스에 쓰이는 단자는 가능하면 레거시 SATA 장치와 하위 호환성을 보장하기 위해 선택되었으므로 추가 어댑터나 변환기가 필요 없다.\[29\] 연결되는 기억 장치의 종류에 따라 PCI 익스프레스 레인이나 SATA 3.0 포트를 제공함으로써 호스트 측 단자는 하나의 PCI 익스프레스 SSD 또는 최대 두 개의 레거시 SATA 장치를 허용한다.\[30\]

SATA 익스프레스 단자에는 5종이 있으며, 위치와 목적에 따라 다르다:\[31\]

  - 호스트 플러그: 메인보드의 및 애드온 컨트롤러에 사용된다. 이 단자는 레거시 3.5인치 SATA 데이터 케이블을 허용함으로써 하위 호환되는데, 즉 최대 2개의 SATA 장치르를 위한 연결을 제공한다.
  - 호스트 케이블 리셉터클: SATA 익스프레스 케이블의 호스트 측 단자이다. 이 단자는 하위 호환이 되지 않는다.
  - 장치 케이블 리셉터클: SATA 익스프레스 케이블의 장치 측 단자로서, 하나의 SATA 장치를 허용함으로써 하위 호환된다.
  - 장치 플러그: SATA 익스프레스 장치에 사용된다. SATA 익스프레스 장치를 U.2 [백플레인](https://ko.wikipedia.org/wiki/백플레인 "wikilink")\[32\]이나 [멀티링크 SAS](https://ko.wikipedia.org/wiki/SAS "wikilink") 리셉터클로 연결할 수 있게 함으로써 이 단자는 부분적으로 하위 호환된다. 그러나 이렇게 연결된 SATA 익스프레스 장치는 호스트가 PCI 익스프레스 장치를 지원하는 경우에만 기능한다.
  - 호스트 리셉터클: SATA 익스프레스 장치와의 직접 연결을 위한 백플레인에 사용되며, 즉 케이블 없는 연결이 된다. 이 단자는 하나의 SATA 장치를 허용함으로써 하위 호환된다.

위에 나열된 SATA 익스프레스 단자들은 오직 2개의 PCI 익스프레스 레인만 제공하는데 이는 낮은 비용의 빠른 플랫폼 전환에 초점을 둔 전반적인 설계 때문이다. 이러한 선택은 더 값싼 비차폐 케이블을 사용할 수 있게 함과 더불어 레거시 SATA 장치와의 더 용이한 하위 호환성을 허용하였다. 2.5인치 드라이브 형태의 2015년 3월 기준으로 일부 NVM 익스프레스 장치들은 *U.2* 단자 (원래 이름은 *SFF-8639*이지만 2015년 6월 이름이 변경됨)\[33\]\[34\]\[35\]를 사용한다. U.2 단자는 기계적으로 SATA 익스프레스 장치 플러그와 동일하지만, 각기 다른 이용 가능한 핀을 통해 4개의 PCI 익스프레스 레인을 제공한다.\[36\]\[37\]\[38\]\[39\]

아래의 표는 동반되는 단자의 호환성에 대해 요약한 것이다.

<table>
<caption>단자 결합 호환표[40]</caption>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p>SATA 익스프레스<br />
호스트 케이블<br />
리셉터클</p></th>
<th><p>SATA 익스프레스<br />
장치 케이블<br />
리셉터클</p></th>
<th><p>SATA 익스프레스<br />
호스트 리셉터클</p></th>
<th><p>SATA 케이블<br />
리셉터클</p></th>
<th><p>U.2 백플레인<br />
리셉터클</p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/SAS_멀티링크" title="wikilink">SAS 멀티링크</a><br />
리셉터클</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SATA 익스프레스<br />
호스트 플러그</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>SATA 익스프레스<br />
장치 플러그</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>SATA<br />
장치 플러그</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 각주

  - 내용주

<references group="lower-alpha" />

## 외부 링크

  - Official  (SATA-IO) website

  - US patent 20130294023, November 7, 2013, assigned to Raphael Gay

[SATA_익스프레스](https://ko.wikipedia.org/wiki/분류:SATA_익스프레스 "wikilink") [분류:2013년 출시](https://ko.wikipedia.org/wiki/분류:2013년_출시 "wikilink") [분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink") [분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:컴퓨터 단자](https://ko.wikipedia.org/wiki/분류:컴퓨터_단자 "wikilink") [분류:메인보드 확장 슬롯](https://ko.wikipedia.org/wiki/분류:메인보드_확장_슬롯 "wikilink")

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
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.