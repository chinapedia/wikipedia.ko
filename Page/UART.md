> This article is converted from Wikipedia: [UART](https://ko.wikipedia.org/wiki/UART).


**UART**(범용 비동기화 송수신기: Universal asynchronous receiver/transmitter)는 병렬 데이터의 형태를 직렬 방식으로 전환하여 데이터를 전송하는 [컴퓨터 하드웨어의](../Page/컴퓨터_하드웨어.md "wikilink") 일종이다. UART는 일반적으로 [EIA](https://ko.wikipedia.org/wiki/미국_전자_산업_협회 "wikilink") [RS-232](../Page/RS-232.md "wikilink"), [RS-422](../Page/RS-422.md "wikilink"), [RS-485](https://ko.wikipedia.org/wiki/RS-485 "wikilink")와 같은 통신 표준과 함께 사용한다. UART의 U는 범용을 가리키는데 이는 자료 형태나 전송 속도를 직접 구성할 수 있고 실제 전기 신호 수준과 방식(이를테면 [차분 신호](https://ko.wikipedia.org/wiki/차분_신호 "wikilink"))이 일반적으로 UART 바깥의 특정한 드라이버 회로를 통해 관리를 받는다는 뜻이다.

통신 데이터는 메모리 또는 레지스터에 들어 있어 이것을 차례대로 읽어 직렬화 하여 통신한다. 최대 8비트가 기본 단위이다.

UART는 일반적으로 컴퓨터나 주변 기기의 일종으로 병렬 데이터를 직렬화 하여 통신하는 개별 [집적 회로이다](../Page/집적_회로.md "wikilink"). 비동기 통신이므로 동기 신호가 전달되지 않는다. 따라서 수신 쪽에서 동기신호를 찾아내어 데이터의 시작과 끝을 시간적으로 알아 처리할 수 있도록 약속되어 있다. 디지털 회로는 자체의 [클럭 신호를](../Page/클럭_신호.md "wikilink") 추가로 사용하여 정해진 속도로 수신 데이터로 부터 비트 구간을 구분하고 그 비트의 논리 상태를 결정하여 데이터 통신을 하는 USRT(범용 동기화 송수신기: Universal synchronous receiver/transmitter)도 사용한다.

UART는 보통 마이크로컨트롤러에도 포함되어 있다. 듀얼 UART, 곧 **DUART**는 두 개의 UART를 하나의 칩에 합친 것이다. 수많은 현대의 집적 회로(IC)는 동기화 통신인 USRT도 함께 지원한다. 이러한 장치들은 'USARTs'(범용 동기화/비동기화 송수신기: universal synchronous/asynchronous receiver/transmitter) 또는 'USART/UART'로도 부른다.

## 데이터 송 수신 형태

<table>
<thead>
<tr class="header">
<th><p>비트 수</p></th>
<th><p>1</p></th>
<th><p>2</p></th>
<th><p>3</p></th>
<th><p>4</p></th>
<th><p>5</p></th>
<th><p>6</p></th>
<th><p>7</p></th>
<th><p>8</p></th>
<th><p>9</p></th>
<th><p>10</p></th>
<th><p>11</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>시작 비트<br />
(Start bit)</p></td>
<td><p>5–8 데이터 비트</p></td>
<td><p>패리티 비트<br />
(parity bit)</p></td>
<td><p>종료 비트<br />
(Stop bit(s))</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>Start</p></td>
<td><p>Data 0</p></td>
<td><p>Data 1</p></td>
<td><p>Data 2</p></td>
<td><p>Data 3</p></td>
<td><p>Data 4</p></td>
<td><p>Data 5</p></td>
<td><p>Data 6</p></td>
<td><p>Data 7</p></td>
<td><p>Parity</p></td>
<td><p>Stop</p></td>
</tr>
</tbody>
</table>

가장 일반적으로 각 데이터 비트의 시간에 대해 16/64 배 빠른 [클럭 신호를](../Page/클럭_신호.md "wikilink") 이용하여 시작 비트로 부터 세어 각 비트의 경계를 찾아낸다. 이 클럭 신호는 자체적인 내부 클럭 디지털 회로에 의해 발생한다. 보드 설정에 따라 주 클럭으로 부터 타이머등을 써서 설정한 속도의 클럭 신호를 만든다. 이것은 프로그래밍에 의한 레지스터 설정에 따라 클럭 신호의 주파수가 바뀐다. 통신 양쪽에서 설정을 미리 약속하고 클럭 신호 발생부의 레지스터를 같은 속도로 설정해야 통신이 원활하게 이루어진다.

  - 시작 비트 : 통신의 시작을 의미하며 한 비트 시간 길이 만큼 유지한다. 지금 부터 정해진 약속에 따라 통신을 시작한다.
  - 데이터 비트 : 5\~8비트의 데이터 전송을 한다. 몇 비트를 사용할 것인지는 해당 레지스터 설정에 따라 결정된다.
  - 패리티 비트 : 오류 검증을 하기 위한 패리티 값을 생성하여 송신하고 수신쪽에 오류 판단한다. 사용안함, 짝수, 홀수 패리티 등의 세가지 옵션으로 해당 레지스터 설정에 따라 선택할 수 있다. '사용안함'을 선택하면 이 비트가 제거된다.
  - 끝 비트 : 통신 종료를 알린다. 세가지의 정해진 비트 만큼 유지해야 한다. 1, 1.5, 2비트로 해당 레지스터 설정에 따라 결정된다.

## UART 모델

<table>
<thead>
<tr class="header">
<th><p>모델</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>EXAR XR21V1410</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>인터실 6402</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>자일로그 Z8440</p></td>
<td><p>2000 kbit/초. Async, <a href="https://ko.wikipedia.org/wiki/이진_동기화_통신" title="wikilink">Bisync</a>, <a href="https://ko.wikipedia.org/wiki/SDLC" title="wikilink">SDLC</a>, <a href="https://ko.wikipedia.org/wiki/HDLC" title="wikilink">HDLC</a>, <a href="../Page/X.25.md" title="wikilink">X.25</a>. <a href="https://ko.wikipedia.org/wiki/순환_중복_검사" title="wikilink">CRC</a>. 4바이트 RX 버퍼. 2바이트 TX 버퍼. <a href="../Page/직접_메모리_접근.md" title="wikilink">DMA</a>.[1]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/8250_UART" title="wikilink">8250</a></p></td>
<td><p>1바이트 버퍼와 더불어 사용하지 않음</p></td>
</tr>
<tr class="even">
<td><p>모토로라 6850</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/MOS_테크놀로지_6522" title="wikilink">6522</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/MOS_테크놀로지_6551" title="wikilink">6551</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>록웰 65C52</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>16450</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/16550_UART" title="wikilink">16550</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/16550_UART" title="wikilink">16550A</a></p></td>
<td><p>16바이트 버퍼, TL=1,4,8,14; 115.2 kbit/초 표준, 다수가 230.4 및 460.8 kbit/초 지원. DMA 방식.[2]</p></td>
</tr>
<tr class="odd">
<td><p>16C552</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>16650</p></td>
<td><p>32바이트 버퍼. 460.8 kbit/초</p></td>
</tr>
<tr class="odd">
<td><p>16750</p></td>
<td><p>64바이트 버퍼 (송신), 56바이트 (수신). 921.6 kbit/초</p></td>
</tr>
<tr class="even">
<td><p>16850</p></td>
<td><p>128바이트 버퍼. 460.8 kbit/초, 즉 1500 kbit/초</p></td>
</tr>
<tr class="odd">
<td><p>16C850</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>16950</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>1 kByte 버퍼</p></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [직렬 통신](../Page/직렬_통신.md "wikilink")
  - [I2C](https://ko.wikipedia.org/wiki/I2C "wikilink")
  - [SPI 버스](../Page/직렬_주변기기_인터페이스_버스.md "wikilink")

## 각주

<references />

[분류:데이터 전송](https://ko.wikipedia.org/wiki/분류:데이터_전송 "wikilink") [분류:마이크로컨트롤러](https://ko.wikipedia.org/wiki/분류:마이크로컨트롤러 "wikilink") [분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:아두이노](https://ko.wikipedia.org/wiki/분류:아두이노 "wikilink")

1.   090529 zilog.com
2.   090529 cs.utk.edu