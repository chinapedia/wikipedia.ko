> This article is converted from Wikipedia: [NVLink](https://ko.wikipedia.org/wiki/NVLink).


**NVLink**(NV링크)는 [엔비디아](https://ko.wikipedia.org/wiki/엔비디아 "wikilink")가 개발한 와이어 기반 [통신 프로토콜](https://ko.wikipedia.org/wiki/통신_프로토콜 "wikilink") 시리얼 멀티 레인 근범위 통신 링크이다. [PCI 익스프레스와](https://ko.wikipedia.org/wiki/PCI_익스프레스 "wikilink") 달리 장치는 여러 개의 NVLink로 구성할 수 있으며 장치는 중앙 [허브](https://ko.wikipedia.org/wiki/허브 "wikilink") 대신 [메시 네트워크를](../Page/메시_네트워크.md "wikilink") 사용하여 통신할 수 있다.

## 성능

<table>
<thead>
<tr class="header">
<th><p>반도체</p></th>
<th><p>인터커넥트</p></th>
<th><p>전송 기술<br />
속도 (레인 당)</p></th>
<th><p>서브 링크 당 레인<br />
(out + in)</p></th>
<th><p>서브 링크 데이터 속도<br />
(데이터 방향별)</p></th>
<th><p>서브 링크<br />
카운트</p></th>
<th><p>전체 데이터 속도<br />
(out + in)</p></th>
<th><p>전체<br />
레인<br />
(out + in)</p></th>
<th><p>전체<br />
데이터 속도<br />
(out + in)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nvidia P100[1]</p></td>
<td><p>PCIe 3.0</p></td>
<td><p>8 <a href="https://ko.wikipedia.org/wiki/전송_(컴퓨팅)" title="wikilink">GT/s</a></p></td>
<td><p>16 + 16 <strong>Ⓑ</strong></p></td>
<td><p>128 Gbit/s = 16 GByte/s</p></td>
<td><p>1</p></td>
<td><p>16 + 16 GByte/s[2]</p></td>
<td><p>32 <strong>Ⓒ</strong></p></td>
<td><p>32 GByte/s</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/POWER9#I.2FO" title="wikilink">IBM Power9</a>[3]</p></td>
<td><p>PCIe 4.0</p></td>
<td><p>16 GT/s</p></td>
<td><p>16 + 16 <strong>Ⓑ</strong></p></td>
<td><p>256 Gbit/s = 32 GByte/s</p></td>
<td><p>3</p></td>
<td><p>96 + 96 GByte/s</p></td>
<td><p>48</p></td>
<td><p>192 GByte/s</p></td>
</tr>
<tr class="odd">
<td><p>Nvidia P100</p></td>
<td><p>NVLink 1.0</p></td>
<td><p>20 GT/s</p></td>
<td><p>8 + 8 <strong>Ⓐ</strong></p></td>
<td><p>160 Gbit/s = 20 GByte/s</p></td>
<td><p>4</p></td>
<td><p>80 + 80 GByte/s</p></td>
<td><p>64</p></td>
<td><p>160 GByte/s</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/POWER8#POWER8_with_NVLink" title="wikilink">IBM Power8+</a></p></td>
<td><p>NVLink 1.0</p></td>
<td><p>20 GT/s</p></td>
<td><p>8 + 8 <strong>Ⓐ</strong></p></td>
<td><p>160 Gbit/s = 20 GByte/s</p></td>
<td><p>4</p></td>
<td><p>80 + 80 GByte/s</p></td>
<td><p>64</p></td>
<td><p>160 GByte/s</p></td>
</tr>
<tr class="odd">
<td><p>Nvidia V100</p></td>
<td><p>NVLink 2.0</p></td>
<td><p>25 GT/s</p></td>
<td><p>8 + 8 <strong>Ⓐ</strong></p></td>
<td><p>200 Gbit/s = 25 GByte/s</p></td>
<td><p>6[4]</p></td>
<td><p>150 + 150 GByte/s</p></td>
<td><p>96</p></td>
<td><p>300 GByte/s</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/POWER9#I.2FO" title="wikilink">IBM Power9</a>[5]</p></td>
<td><p>NVLink 2.0<br />
(블루링크 포트)</p></td>
<td><p>25 GT/s</p></td>
<td><p>8 + 8 <strong>Ⓐ</strong></p></td>
<td><p>200 Gbit/s = 25 GByte/s</p></td>
<td><p>6</p></td>
<td><p>150 + 150 GByte/s</p></td>
<td><p>96</p></td>
<td><p>300 GByte/s</p></td>
</tr>
</tbody>
</table>

**참고**: 데이터 속도 열은 전송 속도에 따라 대략적으로 반올림되었다.
:**Ⓐ**: 샘플값. NVLink 서브 링크 번들링이 가능하다
:**Ⓑ**: 샘플값. PCIe 레인 사용 시 다른 분기가 가능하다
:**Ⓒ**: 단일(no\! 16) PCIe 레인은 각기 다른 쌍으로 데이터를 전송한다

## 각주

[분류:엔비디아](https://ko.wikipedia.org/wiki/분류:엔비디아 "wikilink") [분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink") [분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink")

1.  [All aboard the PCIe bus for Nvidia's Tesla P100 supercomputer grunt](https://www.theregister.co.uk/2016/06/20/nvidia_tesla_p100_pcie_card/) by Chris Williams at theregister.co.uk on June 20, 2016
2.  [NVLink Takes GPU Acceleration To The Next Level](https://www.nextplatform.com/2016/05/04/nvlink-takes-gpu-acceleration-next-level/) by Timothy Prickett Morgan at nextplatform.com on May 4, 2016
3.  [POWER9 Webinar presentation by IBM for Power Systems VUG](https://www.ibm.com/developerworks/community/wikis/form/anonymous/api/wiki/61ad9cf2-c6a3-4d2c-b779-61ff0266d32a/page/1cb956e8-4160-4bea-a956-e51490c2b920/attachment/56cea2a9-a574-4fbb-8b2c-675432367250/media/POWER9-VUG.pdf) by Jeff Stuecheli on January 26, 2017
4.  [GV100 Blockdiagramm](https://www.hardwareluxx.de/index.php/galerie/komponenten/grafikkarten/gtc17-keynote-volta.html) in "GTC17: NVIDIA präsentiert die nächste GPU-Architektur Volta - Tesla V100 mit 5.120 Shadereinheiten und 16 GB HBM2" by Andreas Schilling on hardwareluxx.de on May 10, 2017
5.  [NVIDIA Volta GV100 GPU Chip For Summit Supercomputer Twice as Fast as Pascal P100 – Speculated To Hit 9.5 TFLOPs FP64 Compute](http://wccftech.com/nvidia-volta-gv100-gpu-fast-pascal-gp100/) by Hassan Mujtaba at wccftech.com on December 20, 2016