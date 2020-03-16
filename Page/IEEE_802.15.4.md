> This article is converted from Wikipedia: [IEEE 802.15.4](https://ko.wikipedia.org/wiki/IEEE_802.15.4).


**IEEE 802.15.4**는 [물리 계층](../Page/물리_계층.md "wikilink")(PHY)과 [미디어 액세스 콘트롤 계층](https://ko.wikipedia.org/wiki/미디어_액세스_콘트롤_계층 "wikilink")(MAC)을 정의하는 표준으로서, 저속도 무선 [개인 통신망](../Page/개인_통신망.md "wikilink")(Low Rate Wireless Personal Area Networks, LR-WPANs)를 위한 표준 가운데 하나이다. [IEEE 802.15](https://ko.wikipedia.org/wiki/IEEE_802.15 "wikilink") 워킹 그룹이 관리하고 있다. 대표적 이름은 지그비 [Zigbee](https://ko.wikipedia.org/wiki/Zigbee "wikilink")이다.

IEEE 802.15.4는 [직비](../Page/직비.md "wikilink"), [와이어리스하트](https://ko.wikipedia.org/wiki/와이어리스하트 "wikilink")(WirelessHART), [마이와이](https://ko.wikipedia.org/wiki/마이와이 "wikilink")(MiWi) 표준의 기저 계층이 되었다. 앞서 말한 표준 각각은 IEEE 802.15.4-2006표준이 커버하고 있지 않은 상위 [프로토콜 스택을](https://ko.wikipedia.org/wiki/프로토콜_스택 "wikilink") 정의함으로써 완전한 통신망 솔루션을 제공하고자 하고 있다. 한편 IEEE 802.15.4-2006을 가지고 [6LoWPAN](../Page/6LoWPAN.md "wikilink")(소위, 센서 네트워크와 IPv6 네트워크를 직접 연동하는 기술)과 표준 인터넷 프로토콜과 함께 써서, 이른바 와이어리스 임베디드 인터넷(Wireless Embedded Internet)을 만들 수 있기도 하다.

## 개관

IEEE 표준 802.15.4는 무선 개인 통신망(WPAN)의 기본적인 하위 네트워크 계층을 제공하기 위해 제정되었다. 특히, 장치간의 저가격, 저속도 유비퀴터스 통신을 지향하였다. (대조적으로, 최종 사용자를 염두에 둔 표준으로 [Wi-Fi](https://ko.wikipedia.org/wiki/Wi-Fi "wikilink")가 있다. ) 거의 갖추고 있는 인프라스트럭쳐 없이도, 서로 가까운 거리에 있는 장치끼리 저가격으로 통신을 할 수 있다는 점을 강조하였다. 게다가 저전력 소비까지도 염두에 두었다.

기본 프레임워크는 10 미터 거리 내, 대략 250 kbit/s 전송 속도를 전제조건으로 하였다. 한 종류만의 물리 계층(physical layer)만 아닌 여러 종류의 물리 계층을 정의해두었다. 더 적은 전력소모를 요구하는 [임베디드 시스템에](../Page/임베디드_시스템.md "wikilink") 대해 트레이드오프를 하고자 물리 계층을 여러 개 정의한 것이었다. 최초의 스펙에서는 트랜스퍼 레이트가 약 20, 40 kbit/s 인 저속 스펙이 포함되었다. 현재 버전에서는 트랜스퍼 레이트가 약 100 kbit/s인 스펙이 추가되었다.

저전력소모 스펙에서는 이것들보다 더 낮은 트랜스퍼 레이트도 고려될 수 있다. 한데, 앞서 말했듯이, WPAN 표준 중 802.15.4만이 가지고 있는 특징은 극도로 저렴한 제조 단가를 추구한다는 것이며, 기술적으로 단순함을 추구하는 것인데, 단, 이는 기술적 유연성과 일반성을 해치지 않는 범위 내에서 이루어져야 할 것이다.

IEEE 802.15.4에 들어간 중요한 특징들은, [리얼 타임](https://ko.wikipedia.org/wiki/리얼_타임_컴퓨팅 "wikilink") 응용에 적합하도록 타임 슬롯(guaranteed time slot)을 예약하는 기능, [CSMA/CA](../Page/반송파_감지_다중_접속_및_충돌_탐지.md "wikilink") 을 이용한 콜리전 어보이던스, 보안성 있는 통신 지원 등이 되겠다. 또한, 제조사는 디바이스에 링크 퀄리티나 에너지 디텍션 등과 같은 전력 관리 기능을 포함시킬 수 있다.

IEEE 802.15.4 디바이스는 세 가지 가능한 [무선 주파수](https://ko.wikipedia.org/wiki/무선_주파수 "wikilink") 대역 중 하나를 골라 작동한다. PHY는 2450MHz(2400-2483.5), 868MHz(868-868.6), 915MHz(902-928) 에서 동작한다.

## 프로토콜 구조

[섬네일](https://ko.wikipedia.org/wiki/파일:IEEE_802.15.4_protocol_stack.svg "wikilink") 각 장치들은 개념적으로는 단순한 [무선 네트워크](https://ko.wikipedia.org/wiki/무선_인터넷 "wikilink") 상에서 상호 통신한다. 네트워크 계층의 정의는 [OSI 모델에](https://ko.wikipedia.org/wiki/OSI_모델 "wikilink") 기반하고 있다. 비록 IEEE 802.15.4가 표준 문서에서는 하위 계층만을 정의하고 있으며, 상위 계층과의 상호 작용을 염두에 두고 그것을 정의하고 있으나, 프로토콜 사용자는 컨버전스 서브레이어를 통해 MAC에 접근하는 [IEEE 802.2](https://ko.wikipedia.org/wiki/IEEE_802.2 "wikilink") [로지컬 링크 콘트롤](https://ko.wikipedia.org/wiki/로지컬_링크_콘트롤 "wikilink") 서브레이어를 선택적으로 사용할 수 있다.

## 같이 보기

  - [IEEE 802.15](https://ko.wikipedia.org/wiki/IEEE_802.15 "wikilink")
  - [직비](../Page/직비.md "wikilink")
  - [블루투스](../Page/블루투스.md "wikilink")
  - [무선 개인 통신망](https://ko.wikipedia.org/wiki/무선_개인_통신망 "wikilink")
  - [센서 네트워크](https://ko.wikipedia.org/wiki/센서_네트워크 "wikilink")

## 외부 링크

  - [802.15.4 Task Group](http://www.ieee802.org/15/pub/TG4.html)

  - [Get IEEE 802.15](http://standards.ieee.org/getieee802/802.15.html)

  - [IEEE standard 802.15.4a-2007](http://standards.ieee.org/getieee802/download/802.15.4a-2007.pdf)

  - [IEEE standard 802.15.4-2006](http://standards.ieee.org/getieee802/download/802.15.4-2006.pdf)

  - [IEEE standard 802.15.4-2003](http://standards.ieee.org/getieee802/download/802.15.4-2003.pdf)

  - [802.15.4 Resources](https://web.archive.org/web/20100526152108/http://www.daintree.net/resources/index.php) including whitepapers and glossary

  - [Identiko - company working in the field of Zigbee and Rfid](http://identiko.net/zigbee.html)

[분류:IEEE 802](https://ko.wikipedia.org/wiki/분류:IEEE_802 "wikilink") [분류:무선 네트워크](https://ko.wikipedia.org/wiki/분류:무선_네트워크 "wikilink") [분류:IEEE 표준](https://ko.wikipedia.org/wiki/분류:IEEE_표준 "wikilink")