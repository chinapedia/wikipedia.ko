> This article is converted from Wikipedia: [CAN 버스](https://ko.wikipedia.org/wiki/CAN_버스).


**CAN 통신**(**Controller Area Network**)은 차량 내에서 호스트 컴퓨터 없이 마이크로 콘트롤러나 장치들이 서로 통신하기 위해 설계된 표준 통신 규격이다. CAN 통신은 메시지 기반 프로토콜이며 최근에는 차량 뿐만 아니라 산업용 자동화기기나 의료용 장비에서도 종종 사용되고 있다. **Controller Area Network** (CAN)은 각 제어기들 간의 통신을 위해 주로 사용되는 non-host 버스 방식의 메시지 기반 네트워크 프로토콜이다.

1983년 최초로 Bosch社에 의해 개발되었고, 1986년 공식적으로 소개된 이래, 현재 생산되는 대부분의 자동차에서 사용되고 있으며, 기타 다양한 분야에서도 적용이 되고 있다.

CAN 통신은 [로버트 보쉬사에서](https://ko.wikipedia.org/wiki/보쉬 "wikilink") 1983년부터 개발에 착수해\[1\] 1986년 미국 미시간주 [디트로이트](../Page/디트로이트.md "wikilink")에서 열린 [SAE(Society of Automotive Engineers)](http://www.sae.org/)에서 공식적으로 발표되었다. 최초의 CAN 콘트롤러 칩은 인텔과 필립스에 의해 생산되었으며 1987년 시장에 출시되었다. 1991년 보쉬는 CAN 2.0 스펙을 발표하였다.

CAN 통신은 OBD-II라고 불리는 차량 진단용 통신 표준의 5대 프로토콜 중 하나로 포함되어 있다. OBD-II 표준은 1996년 이후로 미국에서 판매되는 모든 승용차와 소형 트럭에 필수사항으로 적용되었으며 EU에서는 2001년 이후 판매되는 가솔린 차량에 대해, 2004년 이후 판매되는 모든 디젤차량에 대해 EOBD 표준을 적용하여야 한다.\[2\]

## 역사\[3\]

|      |                                                                    |
| ---- | ------------------------------------------------------------------ |
| 1983 | Bosch社에서 차량용 네트워크 프로토콜 개발 프로젝트 착수                                  |
| 1986 | CAN 프로토콜이 Society of Automotive Engineers (SAE)에 공식적으로 소개됨         |
| 1987 | Intel社와 Philips社에 의해 첫 번째 CAN 칩이 생산됨                               |
| 1991 | Bosch, CAN 2.0 사양 발표                                               |
| 1992 | Mercedes-Benz社에서 최초로 CAN 적용 차량 생산                                  |
| 1993 | ISO 11898 (data link and high-speed physical layer) 사양 제정          |
| 1994 | SAE J1939 사양 제정                                                    |
| 1995 | ISO 11898 사양 개정 (extended frame format)                            |
| 2003 | Data link 계층과 high-speed physical 계층 사양 분리 (ISO 11898-1 / -2)      |
| 2006 | ISO 11898-3 (low-power, low-speed physical layer) 사양 제정            |
| 2007 | ISO 11898-5 (low-power, high-speed physical layer) 사양 제정           |
| 2011 | CAN FD 프로토콜 개발 착수                                                  |
| 2013 | ISO 11898-6 (physical layer with selective wake-up function) 사양 제정 |
| 2015 | ISO 11898-1 (Classical CAN and CAN FD) 사양 발표                       |

## 데이터 전송

CAN 네트워크에서 데이터를 전송하는 둘 이상의 노드가 있을 경우 충돌이 발생할 수 있다. CAN 명세서에서는 우성(dominant) 비트와 열성(recessive) 비트라는 용어를 사용한다. 우성 비트는 논리적인 비트값 0을 가지며, 예를 들어 전기적으로 신호값을 강제로 low로 내린다. 열성 비트는 논리적인 비트값 1을 가지며, 예를 들어 전기적으로 high 상태에 머물러 있는다. 결론적으로 두 노드가 서로 동시에 0을 보내면 네트워크상에서 0이 지나가며, 둘 다 1이면 1이 지나간다. 그러나, 하나는 0이고 다른 하나는 1이라면 네트워크 상에는 0이 지나가게 된다. 우성 비트가 경쟁에서 이긴다는 뜻이다. 즉 CAN 네트워크는 낮은 CAN ID를 갖는 프레임에게 오류나 지연없이 데이터를 전송할 수 있는 기법을 제공한다. 경쟁에서 진 높은 CAN ID를 갖는 프레임은 우성 메시지의 전송이 끝난 후 6 비트를 전송할 수 있는 시간을 추가로 기다린 후 재전송을 자동으로 시작한다. 이러한 충돌 해결 방식 때문에, 자동화 시스템에서 CAN 버스는 실시간 우선순위 기반 통신 시스템으로 사랑받고 있다.

예를 들어, 11 비트 ID CAN 네트워크에 노드 ID 15(00000001111b)와 16(00000010000)이 동작하고 있다고 하자. 두 노드가 동시에 메시지를 전송한다고 할 때, 각각은 먼저 시작 비트를 전송한 후, 노드 ID의 첫 번째 0 여섯 개를 충돌없이 전송한다.

<table>
<thead>
<tr class="header">
<th></th>
<th><p>Start<br />
Bit</p></th>
<th><p>ID Bits</p></th>
<th><p>The Rest of the Frame</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10</p></td>
<td><p>9</p></td>
<td><p>8</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>Node 15</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>Node 16</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>CAN Data</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
</tr>
</tbody>
</table>

7번째 비트를 전송할 때, 노드 16은 열성 비트 1을 전송하고 노드 15는 우성 비트 0을 전송한다. 이 때 노드 16은 자신이 1을 전송한 것을 알고 있으나, 자신이 CAN 네트워크에서 읽은 값은 0이 된다. 그러므로 충돌을 감지하고 노드 16은 나머지 메시지들을 더 이상 전송하지 않는다. 반면 노드 15는 아무런 문제없이 다음 비트들을 전송할 수 있다.

CAN 버스는 40m 이하의 네트워크 길이에서 1Mbps까지 전송할 수 있다. 거리가 멀어지면 전송률은 낮아져서, 500m에서는 125kbps로 전송할 수 있다. 향상된 CAN FD 표준에서는 충돌 해결 이후 즉 노드 ID를 전송한 이후에 데이터 부분은 노드 ID 전송 속도의 10배정도까지 빠르게 전송할 수 있다.

## 프레임

### 베이스 프레임 형식

CANH, CANL 신호는 차동 방식이므로 dominant 상태에서는 CANH-CANL 전압차가 0.9V 이상 발생한다. 따라서 그림과 CANL 신호가 dominant 상태에서는 0V로 본다. Recessive state는 CANH-CANL \<0.5V 이고 VCC/2 상태로 CANL가 중간 전압으로 뜬다.

Dominant 상태에서는 CANH 전압이 5V였다가 Recessive state에서는 CANL와 마찬가지로 VCC/2 즉 2.5V가 된다.

일반적으로 CANL의 전압을 기준으로 0V를 LOGIC 0, 2.5V를 LOGIC 1로 표시한다. 신호는 Start-of-frame에서 시작해서 End-Of-Frame으로 끝나게 되다 [섬네일](https://ko.wikipedia.org/wiki/파일:CAN-Bus-frame_in_base_format_without_stuffbits.svg "wikilink")

## 같이 보기

  - [FlexRay](https://ko.wikipedia.org/wiki/FlexRay "wikilink")
  - [Time-Triggered Protocol](https://ko.wikipedia.org/wiki/Time-Triggered_Protocol "wikilink")
  - [SPI](../Page/직렬_주변기기_인터페이스_버스.md "wikilink")
  - [I2C](https://ko.wikipedia.org/wiki/I2C "wikilink")


\== 외부 링크 ==

  - [CAN in Automation](http://www.can-cia.org/can-knowledge/)


\== 각주 ==

<references/>

[분류:통신 표준](https://ko.wikipedia.org/wiki/분류:통신_표준 "wikilink") [분류:컴퓨터 네트워크](https://ko.wikipedia.org/wiki/분류:컴퓨터_네트워크 "wikilink") [분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:자동화](https://ko.wikipedia.org/wiki/분류:자동화 "wikilink") [분류:산업 자동화](https://ko.wikipedia.org/wiki/분류:산업_자동화 "wikilink") [분류:산업 컴퓨팅](https://ko.wikipedia.org/wiki/분류:산업_컴퓨팅 "wikilink")

1.  [CAN in Automation.](http://www.can-cia.org)
2.  [*Building Adapter for Vehicle On-board Diagnostic*](http://www.obddiag.net/adapter.html), obddiag.net, accessed 2009-09-09
3.