> This article is converted from Wikipedia: [CMOS](https://ko.wikipedia.org/wiki/CMOS).


[섬네일](https://ko.wikipedia.org/wiki/파일:CMOS_Inverter.svg "wikilink") **CMOS**(Complementary metal–oxide–semiconductor, 시모스)는 [집적 회로의](../Page/집적_회로.md "wikilink") 한 종류로, [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")나 [SRAM](https://ko.wikipedia.org/wiki/에스램 "wikilink") 등의 [디지털 회로를](../Page/디지털_회로.md "wikilink") 구성하는 데에 이용된다. **상보성 금속 산화막 반도체**(相補性 金屬 酸化膜 半導體)라는 용어도 통용된다.

## 개요

P 채널과 N 채널의 [MOSFET를](https://ko.wikipedia.org/wiki/전계효과_트랜지스터 "wikilink") 전원 전압 간에 직렬로 구성하고 입력은 두가지 MOSFET의 게이트에 같이 연결하고 출력은 두가지 MOSFET 드레인 사이에 연결한 [집적 회로의](../Page/집적_회로.md "wikilink") 구조이다. 이 경우 각 MOSFET는 스위치로 간주될 수 있으며 같은 입력신호에 대하여 P 채널과 N 채널이 서로 반대로 동작하므로 전원전압과 접지사이에 기본적으로 흐르는 [bleeding current가](https://ko.wikipedia.org/wiki/블리딩_전류 "wikilink") 거의 없어지므로 [TTL 논리 소자에](../Page/트랜지스터-트랜지스터_논리.md "wikilink") 비해 소비 전력이 적은 [논리 회로를](../Page/논리_회로.md "wikilink") 구현할 수 있고, 부하를 면적을 많이 차지하는 저항이 아닌 MOSFET를 사용하므로 집적도를 향상시킬 수 있다.

MOSFET의 동작 영역에서 직류 전달 특성은 선형 영역에서 출력 전압이 입력 전압과 거의 같고, 포화 영역에서 출력 전압은 게이트 전압에서 「문턱 전압」을 뺀 값이 된다. P-MOSFET가 포화 영역일 때 N-MOSFET는 선형 영역이고, N-MOSFET가 포화 영역일 때 P-MOSFET는 선형 영역이다. 시모스의 동작 영역의 대부분은 선형 영역이다. 엄밀하게 양자의 「문턱 전압」이 겹치는 영역이 존재하므로, 사용하지 않는 입력 단자는 문턱 전압 영역에 들어가지 않도록 풀업 또는 풀다운에 연결해 주는 것이 좋다.

시모스 구조에서 게이트 전압에 입력되는 제어 펄스를 "1"에서 "0"으로 변경했을 경우에 노이즈 없이 이전의 출력을 할 수 있고, "0"에서 "1"로 변경했을 경우 역시 노이즈 없이 입력 신호를 출력할 수 있다.

시모스 구조의 논리 회로는 전원 전압을 낮게 하면 소비 전력이 적은 반면, 전달 지연 시간이 커지는 특성을 가지고 있다. 제조 프로세서가 개선되어 낮은 전압의 동작과 고속 동작을 할 수 있게 되었다.

1990년대가 되면서 [반도체 메모리나](../Page/반도체.md "wikilink") [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")의 논리 [IC는](../Page/집적_회로.md "wikilink") 대부분 시모스 구조가 되었으며 , 작은 규모의 [전원 회로](https://ko.wikipedia.org/wiki/전원_회로 "wikilink"), [아날로그-디지털 변환회로](../Page/아날로그-디지털_변환회로.md "wikilink"), [디지털-아날로그 변환회로](../Page/디지털-아날로그_변환회로.md "wikilink") 등이 포함되어 제작하기 시작하였다.

## 시모스 [논리 표준 IC](https://ko.wikipedia.org/wiki/논리_표준_IC "wikilink")

단일 전원으로 시모스 수준의 입출력 인터페이스로 통일된 집적회로이다. (74HCT나 74ACT처럼 입력 논리 수준을 [TTL에](../Page/트랜지스터-트랜지스터_논리.md "wikilink") 맞춘 형태도 있음.)

<table>
<thead>
<tr class="header">
<th><p>형태 이름</p></th>
<th><p>전원 전압 범위<br />
(V)</p></th>
<th><p>지연<br />
(ns)</p></th>
<th><p>정지시 전류<br />
(μA/Gate)</p></th>
<th><p>특징</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>4000</p>
</td></td>
<td><p>3 - 15</p>
</td></td>
<td><p>30</p></td>
<td><p>200</p></td>
<td><p>초기의 표준 제품</p></td>
</tr>
<tr class="even">
<td><p>74HC</p></td>
<td><p>2 - 6</p></td>
<td><p>10</p></td>
<td><p>23</p></td>
<td><p>74시리즈와 핀 배치 호환</p></td>
</tr>
<tr class="odd">
<td><p>74AC</p></td>
<td><p>2 - 5.5</p></td>
<td><p>8.5</p></td>
<td><p>40</p></td>
<td><p>HC를 고속으로 동작하게 함</p></td>
</tr>
<tr class="even">
<td><p>74LVX</p></td>
<td><p>2 - 3.6</p></td>
<td><p>12</p></td>
<td><p>20</p></td>
<td><p>3.3V전용</p></td>
</tr>
<tr class="odd">
<td><p>74LCX</p></td>
<td><p>2 - 3.6</p></td>
<td><p>6.5</p></td>
<td><p>10</p></td>
<td><p>3.3V전용 고속 제품</p></td>
</tr>
<tr class="even">
<td><p>74VCX</p></td>
<td><p>1.8 - 3.6</p></td>
<td><p>2.5</p></td>
<td><p>20</p></td>
<td><p>2.0V대응</p></td>
</tr>
</tbody>
</table>

### 시모스 입출력 전압 (V)

  - Hi 레벨 입력 전압 : 0.7×Vcc
  - Low 레벨 입력 전압 : 0.2×Vcc
  - Hi 레벨 출력 전압 : Vcc-0.8
  - Low 레벨 출력 전압 : 0.4

Vcc : 전원 전압

## 그 밖의 예

  - 이미지 장치 분야에서는 [시모스 이미지 센서를](https://ko.wikipedia.org/wiki/시모스_이미지_센서 "wikilink") 줄여서 시모스라고 하는 경우가 있다. 기존에 대중화된 CCD를 대체하게 되었다.
  - [개인용 컴퓨터나](../Page/개인용_컴퓨터.md "wikilink") [워크스테이션](../Page/워크스테이션.md "wikilink")과 같은 작은 규모의 컴퓨터 세계에서 현재 시간이나 하드웨어 정보([BIOS](https://ko.wikipedia.org/wiki/BIOS "wikilink")라고 함)를 보관하고 유지하기 위해 쓰이는 비휘발성 메모리를 시모스 롬, 또는 단순히 시모스라고 하는 경우도 있고 보관되어 있는 데이터 자체를 시모스라고 하기도 한다. 예를 들어 「메인보드가 동작하지 않을 때 CMOS를 초기화한다」라는 표현이 사용된다.

## 같이 보기

  - [시모스 이미지 센서](https://ko.wikipedia.org/wiki/시모스_이미지_센서 "wikilink")

[분류:트랜지스터](https://ko.wikipedia.org/wiki/분류:트랜지스터 "wikilink") [분류:반도체](https://ko.wikipedia.org/wiki/분류:반도체 "wikilink")