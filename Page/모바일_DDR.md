> This article is converted from Wikipedia: [모바일 DDR](https://ko.wikipedia.org/wiki/모바일_DDR).


**모바일 DDR** (**mDDR**, **Low Power DDR**, 간단히 **LPDDR**)은 [이동식 컴퓨터를](https://ko.wikipedia.org/wiki/이동식_컴퓨터 "wikilink") 위해 개발된 저전력의 [DDR](https://ko.wikipedia.org/wiki/더블_데이터_레이트 "wikilink") [SDRAM](../Page/SDRAM.md "wikilink") 인터페이스이다.

|                                                                      | LPDDR1     | LPDDR1E      | LPDDR2       | LPDDR2E      | LPDDR3    | LPDDR3E      | LPDDR4    | *LPDDR4E*    |
| -------------------------------------------------------------------- | ---------- | ------------ | ------------ | ------------ | --------- | ------------ | --------- | ------------ |
| 메모리 배열 클럭 (내부 접근 속도)                                                 | 200 MHz    | 266.67 MHz   | 200 MHz      | 266.67 MHz   | 200 MHz   | 266.67 MHz   | 200 MHz   | 266.67 MHz   |
| 프리페치 크기                                                              | 2*n*       | 4*n*         | 8*n*         | 16*n*        |           |              |           |              |
| [I/O](../Page/입출력.md "wikilink") 버스 클럭 주파수                           | 200 MHz    | 266.67 MHz   | 400 MHz      | 533.33 MHz   | 800 MHz   | 1066.67 MHz  | 1600 MHz  | 2133.33 MHz  |
| 데이터 전송률 ([DDR](https://ko.wikipedia.org/wiki/더블_데이터_레이트 "wikilink")) | 400 MT/s   | 533.33 MT/s  | 800 MT/s     | 1066.67 MT/s | 1600 MT/s | 2133.33 MT/s | 3200 MT/s | 4266.67 MT/s |
| 공급 전압                                                                | 1.8 V      | 1.2 V, 1.8 V | 1.2 V, 1.8 V | 1.1 V, 1.8 V |           |              |           |              |
| 명령어 / 주소 버스                                                          | 19 비트, SDR | 10 비트, DDR   | 10 비트, DDR   | 6 비트, SDR    |           |              |           |              |

LPDDR 세대

## LPDDR

LPDDR (LPDDR2와 구별하기 위해 때때로 **LPDDR1**로도 불림)은 원래 [DDR SDRAM에](../Page/DDR_SDRAM.md "wikilink") 총 전력 소모량 절감을 위한 여러 변형을 가한 것이다.

SDRAM에 비해 가장 극명한 변화는 공급 전압이 2.5V에서 1.8V로 낮아진 점이다. 메모리 재충전(DRAM refresh)이 낮은 온도에서 덜 필요한 점을 이용하여 재충전 회수를 온도에 적응시키며, 메모리의 모든 내용을 지우고 "깊은 절전 모드"에 빠질 수 있게 해서 추가적인 전력 소모 절감을 얻는다. 또한 메모리 칩은 작아지고 기판 면적 점유가 줄어든다. [삼성전자](https://ko.wikipedia.org/wiki/삼성전자 "wikilink")와 [마이크론은](../Page/마이크론_테크놀로지.md "wikilink") 이 기술의 두 최대 공급자로 [애플의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [아이패드](../Page/아이패드.md "wikilink"), [삼성전자](https://ko.wikipedia.org/wiki/삼성전자 "wikilink")의 [갤럭시탭](https://ko.wikipedia.org/wiki/갤럭시탭 "wikilink")과 [모토로라](../Page/모토로라.md "wikilink")의 [드로이드 X](https://ko.wikipedia.org/wiki/드로이드_X "wikilink")\[1\] 등과 같은 다양한 태블릿 기기에 공급하고 있다.

## LPDDR2

새로운 [JEDEC](https://ko.wikipedia.org/wiki/JEDEC "wikilink") 표준 [JESD209-2E](http://www.jedec.org/user/register?destination=node/16037) 은 저전력 DDR 인터페이스에 더 큰 변화를 정의했다. 이것은 DDR1이나 DDR2와는 호환되지 않는 규격이지만 아래와 같은 메모리와 호환된다.:

  - LPDDR2-S2: 2n prefetch 메모리 (DDR1과 같은 종류),
  - LPDDR2-S4: 4n prefetch 메모리 (DDR2와 같은 종류), 또는
  - LPDDR2-N: 비휘발성 ([NAND 플래시](https://ko.wikipedia.org/wiki/NAND_플래시 "wikilink")) 메모리.

저전력 상태는 기본적인 LPDDR와 비슷하며, 일부 메모리 열만 재충전할 수 있는 약간의 기능 추가가 이루어졌다.

타이밍 변수는 LPDDR-200 에서 LPDDR-1066 까지 정의된다. (즉 동작 클럭은 100 에서 533 MHz에 이른다.)

1.2V에서 동작하며 LPDDR2는 동작 배선과 주소 배선을 10비트 [더블 데이터 레이트](https://ko.wikipedia.org/wiki/더블_데이터_레이트 "wikilink") CA 버스에 통합한다. 명령어는 예비충전과 최대속도전송(Burst) 정지 코드의 재배열을 제외하고 [일반적인 SDRAM 명령어와](https://ko.wikipedia.org/wiki/SDRAM#SDRAM_control_signals "wikilink") 유사하다.

<table>
<caption>LPDDR2 명령어 인코딩[2]</caption>
<thead>
<tr class="header">
<th><p>CK</p></th>
<th><p>CA0<br />
()</p></th>
<th><p>CA1<br />
()</p></th>
<th><p>CA2<br />
()</p></th>
<th><p>CA3</p></th>
<th><p>CA4</p></th>
<th><p>CA5</p></th>
<th><p>CA6</p></th>
<th><p>CA7</p></th>
<th><p>CA8</p></th>
<th><p>CA9</p></th>
<th><p>동작</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p>—</p></td>
<td><p>NOP</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>—</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p>—</p></td>
<td><p>모든 뱅크 사전충전</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>—</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p>—</p></td>
<td><p>BA2</p></td>
<td><p>BA1</p></td>
<td><p>BA0</p></td>
<td><p>한 뱅크 사전충전</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>—</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p>A30</p></td>
<td><p>A31</p></td>
<td><p>A32</p></td>
<td><p>BA2</p></td>
<td><p>BA1</p></td>
<td><p>BA0</p></td>
<td><p>사전활성화<br />
(LPDDR2-N only)</p></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>A20</p></td>
<td><p>A21</p></td>
<td><p>A22</p></td>
<td><p>A23</p></td>
<td><p>A24</p></td>
<td><p>A25</p></td>
<td><p>A26</p></td>
<td><p>A27</p></td>
<td><p>A28</p></td>
<td><p>A29</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p>—</p></td>
<td><p>최고속도전송 종료</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>—</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><em>예약됨</em></p></td>
<td><p>C1</p></td>
<td><p>C2</p></td>
<td><p>BA2</p></td>
<td><p>BA1</p></td>
<td><p>BA0</p></td>
<td><p>읽기<br />
(AP=자동 사전충전)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>AP</p></td>
<td><p>C3</p></td>
<td><p>C4</p></td>
<td><p>C5</p></td>
<td><p>C6</p></td>
<td><p>C7</p></td>
<td><p>C8</p></td>
<td><p>C9</p></td>
<td><p>C10</p></td>
<td><p>C11</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><em>예약됨</em></p></td>
<td><p>C1</p></td>
<td><p>C2</p></td>
<td><p>BA2</p></td>
<td><p>BA1</p></td>
<td><p>BA0</p></td>
<td><p>쓰기<br />
(AP=자동 사전충전)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>AP</p></td>
<td><p>C3</p></td>
<td><p>C4</p></td>
<td><p>C5</p></td>
<td><p>C6</p></td>
<td><p>C7</p></td>
<td><p>C8</p></td>
<td><p>C9</p></td>
<td><p>C10</p></td>
<td><p>C11</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p>R8</p></td>
<td><p>R9</p></td>
<td><p>R10</p></td>
<td><p>R11</p></td>
<td><p>R12</p></td>
<td><p>BA2</p></td>
<td><p>BA1</p></td>
<td><p>BA0</p></td>
<td><p>활성<br />
(R0–14=행 주소)</p></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>R0</p></td>
<td><p>R1</p></td>
<td><p>R2</p></td>
<td><p>R3</p></td>
<td><p>R4</p></td>
<td><p>R5</p></td>
<td><p>R6</p></td>
<td><p>R7</p></td>
<td><p>R13</p></td>
<td><p>R14</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p>A15</p></td>
<td><p>A16</p></td>
<td><p>A17</p></td>
<td><p>A18</p></td>
<td><p>A19</p></td>
<td><p>BA2</p></td>
<td><p>BA1</p></td>
<td><p>BA0</p></td>
<td><p>활성화<br />
(LPDDR2-N only)</p></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>A5</p></td>
<td><p>A6</p></td>
<td><p>A7</p></td>
<td><p>A8</p></td>
<td><p>A9</p></td>
<td><p>A10</p></td>
<td><p>A11</p></td>
<td><p>A12</p></td>
<td><p>A13</p></td>
<td><p>A14</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p>—</p></td>
<td><p>모든 뱅크 재충전<br />
(LPDDR2-Sx only)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>—</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p>—</p></td>
<td><p>한 뱅크 재충전<br />
(Round-robin addressing)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>—</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>H</strong></p></td>
<td><p>MA0</p></td>
<td><p>MA1</p></td>
<td><p>MA2</p></td>
<td><p>MA3</p></td>
<td><p>MA4</p></td>
<td><p>MA5</p></td>
<td><p>Mode register read<br />
(MA0–7=Address)</p></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>MA6</p></td>
<td><p>MA7</p></td>
<td><p>—</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p><strong>L</strong></p></td>
<td><p>MA0</p></td>
<td><p>MA1</p></td>
<td><p>MA2</p></td>
<td><p>MA3</p></td>
<td><p>MA4</p></td>
<td><p>MA5</p></td>
<td><p>Mode register write<br />
(OP0–7=Data)</p></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>MA6</p></td>
<td><p>MA7</p></td>
<td><p>OP0</p></td>
<td><p>OP1</p></td>
<td><p>OP2</p></td>
<td><p>OP3</p></td>
<td><p>OP4</p></td>
<td><p>OP5</p></td>
<td><p>OP6</p></td>
<td><p>OP7</p></td>
<td></td>
</tr>
</tbody>
</table>

행 주소 비트 C0는 절대 전송되지 않으며 0으로 취급된다. 최고 속도 전송 (Burst transfer)은 항상 짝수 주소에서 시작한다.

상태 레지스터들은 옛날의 SDRAM과 비교해서 크게 확장되어 8비트 주소 공간을 가지며 이전의 주소를 읽어낼 수 있는 능력을 가진다. 이 레지스터들은 [SPD](https://ko.wikipedia.org/wiki/:en:serial_presence_detect "wikilink") EEPROM보다 작으면서도 그것이 불필요할 만큼 충분한 정보를 포함한다.

S2 장치들은 4기가비트보다 작고 S4 장치들은 1기가비트보다 작은 단 4개의 [뱅크](https://ko.wikipedia.org/wiki/뱅크 "wikilink")를 가진다. 이것들은 BA2 신호를 무시하며 뱅크 개별의 재충전을 지원하지 않는다.

비휘발성 메모리 장치는 재충전 명령이 필요하지 않으므로 사용하지 않으며, 사전충전 명령을 A20이상의 주소 비트를 전송하는 데 이용한다. 낮은 순위 비트(A19이하)들은 뒤이은 활성 명령에 의해서 전송된다. 이 경우 메모리 배열에서 선택된 행은 그것들이 읽기 명령에 의해 읽을 수 있는 4 또는 8 행 데이터 버퍼(BA비트로 선택된)로 전송한다. DRAM과는 달리 뱅크 주소 비트는 메모리 주소의 일부가 아니며 어떤 주소든 모든 행 데이터 버퍼로 전송가능하다. 행 데이터 버퍼는 메모리 종류에 따라 32에서 4096바이트의 길이를 가진다. 32바이트보다 큰 행은 활성화 명령시 몇몇 낮은 순위의 주소비트를 무시한다. 4096바이트보다 작은 행은 읽기 명령시 몇몇 높은 순위의 데이터 비트를 무시한다.

비휘발성 메모리는 열 데이터 버퍼의 쓰기 명령어를 지원하지 않는다. 대신 특수 주소 구역의 순차적인 제어 레지스터가 읽기/쓰기 명령어를 지원하며 이것으로 메모리 열의 삭제와 프로그램이 가능하다.

## LPDDR3

2012년 5월에, [JEDEC](https://ko.wikipedia.org/wiki/JEDEC "wikilink")은 JESD209-3 저전력 메모리 장치 표준을 공개했다. LPDDR2와 비교하여 LPDDR3는 더 높은 데이터 속도, 확장된 대역폭, 향상된 전력 효율과 기억 장치 밀도를 제공한다. 확장된 대역폭은 채널당 6.4GBps, [듀얼 채널](https://ko.wikipedia.org/wiki/듀얼_채널 "wikilink") 구성으로 최대 12.8GBps 에 달한다. LPDDR3는 POP또는 개별 패키징 형식을 지원하여 다양한 활용이 가능하다. LPDDR3는 LPDDR2의 전력효율적 특징과 신호 인터페이스를 여전히 포함하면서 빠른 클럭의 시작/종료와 저전력 자가 재충전, 지능적 배열 관리, 무중단 신호 배선들을 지원한다. LPDDR3는 개발중인 [스마트폰](../Page/스마트폰.md "wikilink")과 태블릿 기기에 요구되는 높은 대역폭을 만족하기 위해 개발 되었다.현재 [삼성 갤럭시 노트 3](../Page/삼성_갤럭시_노트_3.md "wikilink"),[삼성 갤럭시 S5](../Page/삼성_갤럭시_S5.md "wikilink"),[LG G3](../Page/LG_G3.md "wikilink"),[아이폰6](https://ko.wikipedia.org/wiki/아이폰6 "wikilink"),[아이폰6+](https://ko.wikipedia.org/wiki/아이폰6+ "wikilink")등에 장착되었다.

## LPDDR4

2012년 3월 14일, JEDEC은 미래의 모바일 기기의 요구 사항이 LPDDR4와 같은 새로운 표준을 어떻게 이끌어 낼지 탐구하기위한 회의를 주최했다. 이후 삼성전자는 2013년 12월 30일 핀 당 3,200 Mbit/s의 속도로 데이터를 전송할 수있는 최초의 20nm급 8기비비트 (1 GiB) LPDDR4를 개발하여 가장 빠른 LPDDR3보다 50% 더 높은 성능을 제공하며 1.1**V**에서 40 %나 적은 에너지 소모를 구현했다.

2014년 8월 25일, JEDEC는 JESD209-4 LPDDR4 저전력 메모리 표준을 발표했다.

LPDDR3에서의 변경 사항은 다음과 같다.

  - I/O 표준을 저전압 스윙 터미네이션 로직(LVSTL)으로 변경하는 것을 포함하여 인터페이스 속도와 수많은 전기적 변화를 두 배로 늘림
  - 내부 프리 페치 크기와 최소 전송 크기를 배로 늘림
  - 10비트 DDR 명령/주소 버스에서 6비트 SDR 버스로 변경
  - 싱글 32비트 폭의 버스에서 두 개의 독립적 인 16비트 폭 버스로 변경
  - 셀프 리프레시는 CKE 라인에 의해 제어되는 것이 아니라 전용 명령에 의해 가능

이 표준은 두 개의 독립적 인 16비트 액세스 채널을 포함하는 SDRAM 패키지를 정의한다. 각 채널은 패키지 당 최대 2개의 다이에 연결된다. 각 채널의 데이터 폭은 16비트이며 자체 제어/주소 핀을 가지고 있으며 DRAM의 8개 뱅크에 대한 액세스를 허용한다. 따라서 패키지는 세 가지 방법으로 연결될 수 있다.

  - 데이터 라인 및 컨트롤은 16 비트 데이터 버스에 병렬로 연결되며 칩 선택 만 채널별로 독립적으로 연결된다.
  - 칩 선택을 포함하여 32 비트 폭의 데이터 버스와 제어 라인을 병렬로 연결합니다.
  - 두 개의 독립적인 16비트 폭의 데이터 버스

각 다이는 각 채널에 따라서 4, 6, 8, 12 또는 16 기가비트의 메모리를 제공한다. 따라서 각 뱅크의 크기는 디바이스의 16분의 1이다. 이것은 16384비트 (2048 바이트) 행 중에서 적절한 수 (16 Ki \~ 64 Ki)으로 구성된다. 24 및 32 기가비트 확장이 계획되어 있지만 행 수, 너비 또는 뱅크 수를 늘려야할지 여부는 아직 결정되지 않았다. 이중 너비 (4 개 채널)와 채널당 최대 4개의 다이 (패키지 당 총 8개)를 제공하는 더 큰 패키지도 정의된다. 데이터는 16 또는 32 전송 (256 또는 512 비트, 32 또는 64 바이트, 8 또는 16 사이클 DDR)의 버스트로 액세스된다. 버스트는 64비트의 경계선에서 시작되어야 한다. 클럭 주파수가 높고 이전 버스트 표준보다 긴 버스트 길이가 길기 때문에 명령/주소 버스가 병목 현상을 일으키지 않고 제어 신호를 더 다중화 할 수 있다. LPDDR4는 제어 및 주소 라인을 6 비트 단일 데이터 속도 CA 버스로 멀티플렉싱한다. 명령은 2 클럭 사이클을 필요로하며, 주소를 인코딩하는 동작 (예: 활성화, 읽기 또는 쓰기)에는 두 개의 명령이 필요하다. 예를 들어, 대기상태의 칩에서 읽기를 요청하려면 8개의 클럭 사이클 (활성 - 1, 활성화 - 2, 읽기, CAS-2)을 취하는 4개의 명령이 필요하다. 칩 선택 라인 (CS)은 액티브 하이이다. 첫 번째 명령 사이클은 칩 선택이 높게 설정되며, 두 번째 사이클은 낮게 설정된다.

| 첫 사이클 (CS=H) |       | 두번째 사이클 (CS=L) | 작업    |
| ------------ | ----- | -------------- | ----- |
| CA5          | CA4   | CA3            | CA2   |
| **L**        | **L** | **L**          | **L** |
| **H**        | **L** | **L**          | **L** |
| AB           | **H** | **L**          | **L** |
| AB           | **L** | **H**          | **L** |
| —            | **H** | **H**          | **L** |
| BL           | **L** | **L**          | **H** |
| —            | **H** | **L**          | **H** |
| 0            | **L** | **H**          | **H** |
| —            | **H** | **H**          | **H** |
| BL           | **L** | **L**          | **L** |
| C8           | **H** | **L**          | **L** |
| —            | **H** | **L**          | **H** |
| OP7          | **L** | **L**          | **H** |
| OP6          | **H** | **L**          | **H** |
| —            | **L** | **H**          | **H** |
| —            | **H** | **H**          | **H** |
| R15          | R14   | R13            | R12   |
| R9           | R8    | R7             | R6    |

LPDDR4 명령어 인코딩\[3\]

## LPDDR4X

[삼성전자](https://ko.wikipedia.org/wiki/삼성전자 "wikilink")는 [2016년](../Page/2016년.md "wikilink"), LPDDR4X라 불리는 모바일 기기용으로 개량된 LPDDR4를 제안했다. 기존의 LPDDR4와는 동일하지만, [I/O](https://ko.wikipedia.org/wiki/I/O "wikilink")전압 (Vddq)을 1.1**V**가 아닌 0.6**V**으로 줄임으로써 전력소모를 기본의 LPDDR4보다 줄이는데 성공했다. 2017년 1월 9일에는 [SK하이닉스](../Page/SK하이닉스.md "wikilink")가 8과 6GiB LPDDR4X 패키지를 발표했다. JEDEC는 2017년 3월 8일 LPDDR4X 표준을 발표했다. 저전력 메모리 디바이스 표준을 업데이트한 JEDEC은 저전압을 제외하고도 더 작은 크기의 디바이스에 맞게, 싱글 채널 다이 옵션을 포함하고있다. 새로운 기능으로 MCP, PoP 및 IoT 패키지에서 최고 4266Mbps 속도에 대한 추가 정의 및 타이밍 개선을 제공한다.

## 미래 규격

JEDEC 소위원회 JC-42.6은 LPDDR2의 후계자를 개발하고 있다. JC-42.6에서는 다음과 같은 두 규격을 다루고 있다.\[4\]

<references />

### WideIO

WideIO 또한 현재 JC-42.6에서 개발되고 있다. 시스템의 집적도를 높이고자 하는 산업계의 요구를 충족하기 위한 돌파구가 될 기술으로 스마트폰, 태블릿, 휴대용 게임 콘솔과 같은 고성능 모바일 기기의 성능, 대역폭, 지연시간, 전력과 부피에 엄청난 향상을 가능하게 한다. WideIO 모바일 DRAM 메모리는 칩 수준의 3차원 집적 기술인 [TSV](https://ko.wikipedia.org/wiki/TSV "wikilink") 내부연결을 사용하여 메모리칩을 직접 SoC에 연결한다. 3차원 집적 기술은 회로 면적에 제한받는 고전적인 연결방식에 비해 엄청나게 많은 IO핀을 제공하며 이를 활용하여 성능을 높이는 기술이다. WideIO는 3D게이밍, HD비디오와 같은 12.8GBps(LPDDR3 듀얼채널 구성)을 넘어서는 메모리 대역폭을 요구하는 응용 프로그램에 적합한 기술이다.

## 활용

[삼성전자](https://ko.wikipedia.org/wiki/삼성전자 "wikilink")는 WideIO의 핵심 기술인 [TSV](https://ko.wikipedia.org/wiki/TSV "wikilink")의 선두주자 중 하나이며 이를 바탕으로 WideIO 모바일 DRAM의 개발을 이미 완료하였다.\[5\]

## 참조

## 외부 링크

  - [Samsung](http://www.samsung.com/global/business/semiconductor/products/dram/Products_MobileSDRAM.html)

  - [Micron](https://web.archive.org/web/20080520121425/http://www.micron.com/products/dram/mobiledram)

  - [Elpida](https://web.archive.org/web/20110829044651/http://www.elpida.com/en/products/mobile.html)

[분류:기억 장치](https://ko.wikipedia.org/wiki/분류:기억_장치 "wikilink") [분류:컴퓨터 메모리](https://ko.wikipedia.org/wiki/분류:컴퓨터_메모리 "wikilink")

1.  [Anandtech Samsung Galaxy Tab - The AnandTech Review](http://www.anandtech.com/show/4062/samsung-galaxy-tab-the-anandtech-review), December 23, 2010
2.
3.   Username and password "cypherpunks" will allow download.
4.  [JEDEC - Mobile Memory: LPDDR2, LPDDR3, WideIO, Memory MCP](http://www.jedec.org/standards-documents/technology-focus-areas/mobile-memory-lpddr2-lpddr3-wideio-memory-mcp)  2011년 8월 31일 확인.
5.