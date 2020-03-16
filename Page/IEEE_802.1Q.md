> This article is converted from Wikipedia: [IEEE 802.1Q](https://ko.wikipedia.org/wiki/IEEE_802.1Q).


**IEEE 802.1Q**는 하나의 [이더넷](../Page/이더넷.md "wikilink") 네트워크에서 [가상 랜](../Page/가상_랜.md "wikilink")(VLAN)을 지원하는 [네트워크](../Page/컴퓨터_네트워크.md "wikilink") 표준이다. 이 표준은 [이더넷 프레임을](https://ko.wikipedia.org/wiki/이더넷_프레임 "wikilink") 위한 VLAN 태그 추가 시스템과 더불어, 이러한 프레임을 관리하는데 동반되는 [브리지와](../Page/네트워크_브리지.md "wikilink") [스위치에](https://ko.wikipedia.org/wiki/네트워크_스위치 "wikilink") 쓰이는 절차들을 정의한다. 또, 이 표준은 [IEEE 802.1p라는](https://ko.wikipedia.org/wiki/IEEE_802.1p "wikilink") [QoS](../Page/QoS.md "wikilink") 우선 순위 스키마를 위한 예비를 포함하고 있으며 [GARP를](https://ko.wikipedia.org/wiki/MRP "wikilink") 정의한다.

이 표준은 [IEEE 802](../Page/IEEE_802.md "wikilink") 표준 위원회의 [워킹 그룹인](https://ko.wikipedia.org/wiki/워킹_그룹 "wikilink") [IEEE 802.1이](https://ko.wikipedia.org/wiki/IEEE_802.1 "wikilink") 개발한 것으로, 그 뒤로 [IEEE 802.1ak](https://ko.wikipedia.org/wiki/IEEE_802.1ak "wikilink"), [IEEE 802.1Qat](https://ko.wikipedia.org/wiki/IEEE_802.1Qat "wikilink"), [IEEE 802.1Qay를](https://ko.wikipedia.org/wiki/IEEE_802.1Qay "wikilink") 포함한 개정판들을 활발하게 개발하고 있다.

## 프레임 포맷

[center](https://ko.wikipedia.org/wiki/파일:Ethernet_802.1Q_Insert.svg "wikilink") 802.1Q는 원래 프레임을 실제로 캡슐화(encapsulate)하지 않는다. 그 대신 [이더넷 프레임에](https://ko.wikipedia.org/wiki/이더넷_프레임 "wikilink") 대하여 출발지 [MAC 주소와](../Page/MAC_주소.md "wikilink") 원래 프레임의 [이더타입](https://ko.wikipedia.org/wiki/이더타입 "wikilink")/길이 필드들 사이에 32비트 필드를 추가하여 최소 및 최대 프레임 크기를 64 및 1,518 바이트 (옥텟)에서 64 및 1,522 바이트 (802.1Q가 존재하면 42 옥텟을 최소로 적용, 802.1Q가 없으면 46 옥텟을 최소로 적용. IEEE 802.3-2005 Clause 3.5 참조.)로 확장한다. TPID (태그 프로토콜 식별자, tag protocol identifier)를 위해 두 개의 바이트가 사용되며 다른 2바이트는 TCI(태그 제어 정보, tag control information)를 위해 쓰인다. TCI 필드는 더 나아가 PCP, DEI, VID로 분리된다.\[1\]

| 16 비트 | 3 비트 | 1 비트 | 12 비트 |
| ----- | ---- | ---- | ----- |
| TPID  | TCI  |      |       |
| PCP   | DEI  | VID  |       |

  - TPID: IEEE 802.1Q 태그 프레임으로서 프레임을 식별하기 위해 0x8100의 값으로 설정된 16비트 필드. 이 필드는 태그되지 않은 프레임에서 [이더타입](https://ko.wikipedia.org/wiki/이더타입 "wikilink")/길이 필드와 동일한 위치에 있으므로, 태그되지 않은 프레임과 일반 프레임을 구별하는데 사용할 수 있다.
  - TCI
      - PCP(Priority Code Point): [IEEE 802.1p](https://ko.wikipedia.org/wiki/IEEE_802.1p "wikilink") 우선 순위를 가리키는 3비트 필드. 프레임의 우선 순위를 가리킨다. 값은 0(최고 작용)부터 7(가장 높음)까지이다. 1은 가장 낮은 우선 순위를 가리킨다.
      - DEI(Drop Eligible Indicator): 1비트 필드.(이전에는 CFI\[2\]\[3\]) PCP와는 별도로, 또는 결합해서 쓰이며 트래픽이 혼잡해질 때 제거되기 적합한 프레임들을 가리키는데 사용된다.\[4\]
      - VID(VLAN Identifier): VLAN이 어느 프레임에 속하는지를 결정하는 12비트 필드. 0x000, 0xFFF의 값이 예비로 보존된다. 다른 모든 값들은 VLAN 식별자들로 사용될 수 있으며 최대 4,094개의 VLAN까지 허용한다. 예비값 0x000은 프레임이 어떠한 VLAN에도 속하지 않음을 나타낸다. 이 경우 802.1Q는 우선 순위만 지정하고 이를 우선 순위 태그(*priority tag*)로 참조한다. 브리지에서는 VLAN 1 (기본 VLAN ID)이 관리 VLAN을 위해 예비로 자주 보존되며, 이는 업체에 따라 다르다.

### 이중 태그 추가

IEEE 표준 [802.1ad](https://ko.wikipedia.org/wiki/802.1ad "wikilink")와 더불어 이중 태그 추가는 인터넷 서비스 제공업자들에게 유용할 수 있는데, VLAN 태그가 이미 있는 클라이언트들로부터 트래픽을 혼합하는 동안 인터넷 서비스 제공업자들이 내부적으로 VLAN을 사용할 수 있게 한다. 외부(출발지 MAC 다음으로, ISP VLAN을 대표) S-TAG (서비스 태그)가 먼저 오고, 그 뒤 내부 C-TAG (고객 태그)가 그 뒤를 따른다. 이러한 경우 [802.1ad](https://ko.wikipedia.org/wiki/802.1ad "wikilink")는 서비스 제공자 외부 S-TAG를 위해 0x88a8를 규정한다. [center](https://ko.wikipedia.org/wiki/파일:TCPIP_802.1ad_DoubleTag.svg "wikilink") 비표준 삼중 태그 추가도 가능하다.

| 16 비트 | 3 비트           | 1 비트 | 12 비트 |
| ----- | -------------- | ---- | ----- |
| TPID0 | PCP            | DEI  | VID0  |
| TPID1 | CONTENT RATING | DEI  | VID1  |
| TPID2 | HOP            | DEI  | VID2  |

TPID0+TPID1+TPID2의 내용은 출발지 장비의 48비트 MAC 주소를 포함하고 있다.

## 관련 프로토콜

  - [MVRP](https://ko.wikipedia.org/wiki/MVRP "wikilink") (IEEE 802.1Q의 정의)
  - [GVRP](https://ko.wikipedia.org/wiki/GVRP "wikilink") (IEEE 802.1ak-2007 추가)
  - [MSTP](https://ko.wikipedia.org/wiki/MSTP "wikilink") (본래 [IEEE 802.1s에](https://ko.wikipedia.org/wiki/IEEE_802.1s "wikilink") 정의됨)

## 같이 보기

  - [VLAN 트렁킹 프로토콜](https://ko.wikipedia.org/wiki/VLAN_트렁킹_프로토콜 "wikilink")

## 각주

## 참조

<references />

## 외부 링크

  -
  -
  - [ISL & 802.1q Frame Formats](http://www.cisco.com/en/US/tech/tk389/tk689/technologies_tech_note09186a0080094665.shtml)

[분류:IEEE 802](https://ko.wikipedia.org/wiki/분류:IEEE_802 "wikilink") [분류:이더넷 표준](https://ko.wikipedia.org/wiki/분류:이더넷_표준 "wikilink")

1.  IEEE 802.1Q-2011 clause 9.6
2.  This field was formerly designated *Canonical Format Indicator (CFI)* with a value of 0 indicating a MAC address in [canonical format](https://ko.wikipedia.org/wiki/MAC_address#Bit-reversed_notation "wikilink"). It is always set to zero for Ethernet. CFI was used for compatibility between Ethernet and [Token Ring](https://ko.wikipedia.org/wiki/Token_Ring "wikilink") networks. If a frame received at an Ethernet port had a CFI set to 1, then that frame would not be bridged to an untagged port.
3.  IEEE 802.1Q-2005 clause 9.6
4.  IEEE 802.1Q-2011 clause 6.9.3