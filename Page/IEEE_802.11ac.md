> This article is converted from Wikipedia: [IEEE 802.11ac](https://ko.wikipedia.org/wiki/IEEE_802.11ac).


**IEEE 802.11ac**는 높은 속도의 [근거리 통신망](../Page/근거리_통신망.md "wikilink")(LAN)을 제공하기 위하여 개정된 80[2.11](https://ko.wikipedia.org/wiki/802.11 "wikilink") 무선 [컴퓨터 네트워킹](https://ko.wikipedia.org/wiki/컴퓨터_네트워킹 "wikilink") 표준 중의 하나이다.\[1\] 5GHz 주파수에서 높은 대역폭(80MHz\~160MHz)을 지원하고, 동일한 5GHz에서 802.11n과의 호환성을 위해 40MHz까지 대역폭을 지원한다. 2011년 1월 20일, IEEE 802.11 TGac (ac를 위한 Task Group)\[2\]에 의해 초기 기술 사양 초안 0.1\[3\]이 확정되었다. 표준의 마무리는 2012년 후기에, 최종 802.11 위원회의 승인은 2014년 1월에 완료되었다.\[4\] 연구 자료에 따르면, 802.11ac 사양의 장치들은 2015년에 일반화되어 전 세계에 10억 개 이상 퍼져 나갈 것으로 기대된다.\[5\]

이론적으로, 이 규격에 따르면 다중 단말의 무선랜 속도는 최소 1 Gbit/s, 최대 단일 링크 속도는 최소 500 Mbit/s 까지 가능하게 된다. 이는 더 넓은 무선 주파수 대역폭(최대 160 MHz), 더 많은 [MIMO](../Page/MIMO.md "wikilink") 공간적 스트림(최대 8 개), [다중 사용자 MIMO](https://ko.wikipedia.org/wiki/다중_사용자_MIMO "wikilink"), 그리고 높은 밀도의 변조(최대 256 [QAM](https://ko.wikipedia.org/wiki/QAM "wikilink")) 등 [802.11n](https://ko.wikipedia.org/wiki/802.11n "wikilink") 에서 받아들인 무선 인터페이스 개념을 확장하여 이루어진다.

## 새 기술

  - 더 넓은 채널 대역폭
      - 80 MHz 와 160 MHz 채널 대역폭 ([802.11n의](https://ko.wikipedia.org/wiki/IEEE_802.11n-2009 "wikilink") 최대 40 MHz 와 비교)
          - 의무적 80 MHz, 선택적 160 MHz
  - 더 많은 [MIMO](../Page/MIMO.md "wikilink") 공간적 스트림
      - 8개의 공간적 스트림까지 지원([802.11n의](https://ko.wikipedia.org/wiki/IEEE_802.11n-2009 "wikilink") 4개와 비교)
  - [다중 사용자 MIMO](https://ko.wikipedia.org/wiki/다중_사용자_MIMO "wikilink") (MU-MIMO)
      - 각각 한개 또는 그 이상의 안테나를 가지고 있는 다중 단말이 동시에 독립적인 데이터 스트림을 송수신
          - “공간 분할 다중 접속” (SDMA): 스트림이 주파수에 의하여 구분되지 않고, 11n 형식의 MIMO와 유사하게 공간적으로 분석됨
      - 선택적 모드로서 하향 MU-MIMO(하나의 송신 장치, 다수의 수신 장치) 포함
  - 변조
      - 256-[QAM](https://ko.wikipedia.org/wiki/QAM "wikilink"), 변조율 3/4 과 5/6이 선택적 동작 모드로 포함됨 ([802.11n의](https://ko.wikipedia.org/wiki/IEEE_802.11n-2009 "wikilink") 최대 64-[QAM](https://ko.wikipedia.org/wiki/QAM "wikilink"), 변조율 5/6 과 비교)
  - 그밖의 요소 및 기능
      - [빔포밍](../Page/빔포밍.md "wikilink")을 위한 단일 측량 및 되먹임 형식 ([802.11n의](https://ko.wikipedia.org/wiki/IEEE_802.11n-2009 "wikilink") 다중 방식과 비교)
      - (위의 변화를 지원하기 위한) 매체 접근 제어(MAC) 계층 수정
      - 20/40/80/160 MHz 채널들, 11ac 과11a/n 장치들과의 공존을 위한 구조

## 새 시나리오와 설정

802.11ac에서 지원되는 단일-연결 과 다중-단말 기능의 향상은 몇가지 새로운 무선랜 사용 시나리오를 가능하게 하였다. 예를 들어 가정 내에서의 HD급 영상을 여러 사용자들에게 동시에 전송하거나, 대용량 데이터 파일의 빠른 동기화 및 백업, 무선 디스플레이, 대규모 캠퍼스/강당에서의 배치, 현장 시스템 자동화 등이 있다.\[6\]

### 설정 예제

모든 속도는 256-QAM, 변조율 5/6를 가정함:

<table>
<thead>
<tr class="header">
<th><p>시나리오</p></th>
<th><p>일반적 사용자 형태</p></th>
<th><p>PHY 연결 속도</p></th>
<th><p>총 용량</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1-안테나 <a href="https://ko.wikipedia.org/wiki/액세스_포인트" title="wikilink">AP</a>, 1-안테나 단말, 80MHz</p></td>
<td><p>핸드헬드</p></td>
<td><p>433 Mbit/s</p></td>
<td><p>433 Mbit/s</p></td>
</tr>
<tr class="even">
<td><p>2-안테나 <a href="https://ko.wikipedia.org/wiki/액세스_포인트" title="wikilink">AP</a>, 2-안테나 단말, 80MHz</p></td>
<td><p>태블릿, 랩탑</p></td>
<td><p>867 Mbit/s</p></td>
<td><p>867 Mbit/s</p></td>
</tr>
<tr class="odd">
<td><p>1-안테나 <a href="https://ko.wikipedia.org/wiki/액세스_포인트" title="wikilink">AP</a>, 1-안테나 단말, 160MHz</p></td>
<td><p>핸드헬드</p></td>
<td><p>867 Mbit/s</p></td>
<td><p>867 Mbit/s</p></td>
</tr>
<tr class="even">
<td><p>2-안테나 <a href="https://ko.wikipedia.org/wiki/액세스_포인트" title="wikilink">AP</a>, 2-안테나 단말, 160MHz</p></td>
<td><p>태블릿, 랩탑</p></td>
<td><p>1.73 Gbit/s</p></td>
<td><p>1.73 Gbit/s</p></td>
</tr>
<tr class="odd">
<td><p>4-안테나 <a href="https://ko.wikipedia.org/wiki/액세스_포인트" title="wikilink">AP</a>, 1-안테나 단말 4개, 160MHz<br />
(<a href="https://ko.wikipedia.org/wiki/Multi-user_MIMO" title="wikilink">MU-MIMO</a>)</p></td>
<td><p>핸드헬드</p></td>
<td><p>각 단말 당 867 Mbit/s</p></td>
<td><p>3.47 Gbit/s</p></td>
</tr>
<tr class="even">
<td><p>8-안테나 <a href="https://ko.wikipedia.org/wiki/액세스_포인트" title="wikilink">AP</a>, 160MHz (<a href="https://ko.wikipedia.org/wiki/Multi-user_MIMO" title="wikilink">MU-MIMO</a>)<br />
-- 4-안테나 단말 1개<br />
-- 2-안테나 단말 1개<br />
-- 1-안테나 단말 2개</p></td>
<td><p>디지털 TV, 셋탑박스,<br />
태블릿, 랩탑, PC, 핸드헬드</p></td>
<td><p>4-안테나 단말 3.47 Gbit/s<br />
2-안테나 단말 1.73 Gbit/s<br />
각 1-안테나 단말 당 867 Mbit/s</p></td>
<td><p>6.93 Gbit/s</p></td>
</tr>
<tr class="odd">
<td><p>8-안테나 <a href="https://ko.wikipedia.org/wiki/액세스_포인트" title="wikilink">AP</a>, 2-안테나 단말 4개, 160MHz<br />
(<a href="https://ko.wikipedia.org/wiki/Multi-user_MIMO" title="wikilink">MU-MIMO</a>)</p></td>
<td><p>디지털 TV, 태블릿, 랩탑, PC</p></td>
<td><p>각 단말 당 1.73 Gbit/s</p></td>
<td><p>6.93 Gbit/s</p></td>
</tr>
</tbody>
</table>

## 데이터 속도

<table>
<thead>
<tr class="header">
<th><p>단일 공간 스트림에 대한 이론적인 속도 [Mb/s]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>MCS<br />
인덱스</p></td>
</tr>
<tr class="even">
<td><p>800 ns<br />
보호구역</p></td>
</tr>
<tr class="odd">
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p>6</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p>9</p></td>
</tr>
</tbody>
</table>

주: 2번째 스트림은 이론적으로 데이터 속도가 2배, 3번째는 3배로 늘어난다.

## 제품

Quantenna사는 2011년 11월 15일 세계 최초로 소매용 Wi-Fi 라우터와 가전 제품을 위한 802.11ac 칩셋을 발표\[7\]하였다. Redpine Signals사는 2011년 12월 14일 최초로 스마트폰 애플리케이션 프로세서를 위한 저전력 802.11ac 기술을 발표\[8\]하였다. 2012년 1월 5일, Broadcom사는 그들 최초의 802.11ac Wi-Fi 칩과 협력사를 발표\[9\]하였다.

## 참조

<references />

[분류:IEEE 802.11](https://ko.wikipedia.org/wiki/분류:IEEE_802.11 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.