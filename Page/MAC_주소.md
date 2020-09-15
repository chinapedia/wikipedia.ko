> This article is converted from Wikipedia: [MAC 주소](https://ko.wikipedia.org/wiki/MAC_주소).


[섬네일](https://ko.wikipedia.org/wiki/파일:UMTS_Router_Surf@home_II,_o2-0017.jpg "wikilink") **MAC 주소**(Media Access Control Address)는 네트워크 세그먼트의 [데이터 링크 계층에서](https://ko.wikipedia.org/wiki/데이터_링크_계층 "wikilink") 통신을 위한 네트워크 인터페이스에 할당된 고유 식별자이다.

MAC 주소는 [이더넷](../Page/이더넷.md "wikilink")과 [와이파이](../Page/와이파이.md "wikilink")를 포함한 대부분의 [IEEE 802](../Page/IEEE_802.md "wikilink") 네트워크 기술에 [네트워크 주소로](https://ko.wikipedia.org/wiki/휴대폰_네트워크_주소 "wikilink") 사용된다. 논리적으로 MAC 주소는 [매체 접근 제어](https://ko.wikipedia.org/wiki/매체_접근_제어 "wikilink") 프로토콜이라는 [OSI 모델의](https://ko.wikipedia.org/wiki/OSI_모델 "wikilink") 하위 계층에서 사용된다.

MAC 주소는 대체적으로 [네트워크 인터페이스 컨트롤러](../Page/네트워크_인터페이스_컨트롤러.md "wikilink")(NIC)의 제조업체가 할당하며 하드웨어에 저장되는데, 이는 마치 카드의 [읽기 전용 메모리나](https://ko.wikipedia.org/wiki/읽기_전용_메모리 "wikilink") 일부 다른 펌웨어 구조와 같다. 제조업체에 의해 할당되면 MAC 주소는 일반적으로 제조업체의 등록된 식별 번호로 인코딩되며 이를 **BIA**(burned-in address)로 부를 수 있다. 또, **이더넷 하드웨어 주소**(Ethernet hardware address, EHA), **하드웨어 주소**, **물리 주소**(메모리 [물리 주소와](https://ko.wikipedia.org/wiki/물리_주소 "wikilink") 다름)로 부르기도 한다. 이는 호스트 장치가 NIC에 명령을 할당하여 임의의 주소를 사용하는 프로그래밍된 주소와는 다른 것이다.

하나의 네트워크 노드는 여러 개의 NIC를 가질 수 있으며, 각 NIC는 고유한 MAC 주소를 가진다. [멀티레이어 스위치](https://ko.wikipedia.org/wiki/멀티레이어_스위치 "wikilink"), 라우터와 같은 복잡한 [네트워크 장비는](https://ko.wikipedia.org/wiki/네트워크_장비 "wikilink") 하나 이상의 영구적으로 할당된 MAC 주소가 필요할 수 있다.

MAC 주소는 [전기 전자 기술자 협회](../Page/전기_전자_기술자_협회.md "wikilink")(IEEE)에 관리되는 세 개의 이름공간들 중 하나의 규칙들을 따라 만든다: MAC-48, EUI-48, EUI-64. IEEE는 EUI-48\[1\]과 EUI-64\[2\]라는 이름에 대한 [상표](../Page/상표.md "wikilink")를 보유하고 있으며, 여기에서 EUI는 확장 고유 식별자(Extended Unique Identifier)의 준말이다.

  - 지역적으로 관리되는 mac 주소를 제외하고, 일반적인 MAC 주소는 각각의 장비 벤더별로 고유한 번호를 갖고 있어서 본 정보를 통해서 해당 하드웨어의 제조사를 알수 있는 정보로도 사용 가능하다.
  - 국제 IEEE가 규정을 따르는 표준 MAC 주소는 총 48비트로 구성되어 있다. 이 중 첫 24비트는 OUI(Organizational Unique Identifier) 제조업체의 식별코드이며, NIC 제조업체의 정보를 파악할수 있고, 24비트는 해당 업체의 랜 카드의 정보를 담고 있다.
  - MAC 주소(어드레스) 6바이트(48비트)중 앞 3바이트(24비트)는 각각의 벤더별로 할당되어 있는 고유의 코드로 MAC만으로 어느벤더인지 확인이 가능하며, IEEE 해당 MAC 주소 관리 페이지 싸이트를 통해서 상위 3바이트(24비트)를 입력후 Search 클릭하여 검색 가능하다.\[3\]

## 주소의 상세 설명

[right](https://ko.wikipedia.org/wiki/파일:MAC-48_Address.svg "wikilink") 원래의 [IEEE 802](../Page/IEEE_802.md "wikilink") MAC 주소는 오리지널 [제록스](https://ko.wikipedia.org/wiki/제록스_네트워크_시스템 "wikilink") 이더넷 어드레싱 스킴에서 비롯된다.\[4\] 48비트 주소 공간은 잠재적으로 2<sup>48</sup>, 즉 281,474,976,710,656개의 사용 가능한 MAC 주소를 포함한다.

### 전역 관리와 지역 관리

주소는 전역적으로 관리되는 주소(UAA, Universally Administered Address)이거나 지역적으로 관리되는 주소(LAA, Locally Administered Address) 중 하나가 될 수 있다. 전역적으로 관리되는 주소는 제조업체에 의해 고유하게 할당된다. 처음 3개의 [옥텟](../Page/옥텟_\(컴퓨팅\).md "wikilink")(전송 순서대로)은 [조직 고유 식별자](https://ko.wikipedia.org/wiki/조직_고유_식별자 "wikilink")(OUI)이며, 식별자를 발행한 조직을 식별한다.\[5\] 그 다음의 3개(MAC-48 또는 EUI-48) 또는 5개(EUI-64)의 옥텟은 조직이 원하는 거의 모든 방식대로 조직에 의해 할당되며 이는 고유성의 제한에 종속된다. IEEE는 MAC-48 공간 사용 시 수명을 100년으로 두고 있지만, 대신 EUI-64의 채택을 장려한다.\[6\] 지역적으로 관리되는 주소는 네트워크 관리자에 의해 장치에 할당되며 기록된 주소를 무효화할 수 있다. 지역적으로 관리되는 주소는 OUI가 포함되어 있지 않다.

전역적으로 관리되는 주소와 지역적으로 관리되는 주소는 주소의 첫 옥텟의 두 번째로 [작은 비트로](../Page/최하위_비트.md "wikilink") 설정함으로써 구별할 수 있다. 이 비트는 U/L 비트(Universal/Local의 준말)로도 부르며, 주소가 어떻게 관리될지를 식별한다. 비트가 0이면 주소는 전역적으로 관리되며, 1이면 지역적으로 관리된다. 주소 06-00-00-00-00-00의 예에서 첫 옥텟은 06(16진)이며, 이것의 이진 형태는 00000110인데 여기에서 두 번째로 작은 비트가 1이다. 그러므로 이것은 지역적으로 관리되는 주소이다.\[7\] 즉, 이 비트는 모든 OUI에서 0이 된다.

### 유니캐스트와 멀티캐스트

주소의 첫 옥텟의 최하위 비트를 0으로 설정하면, 프레임은 하나의 수신 중인 [NIC에만](../Page/네트워크_인터페이스_컨트롤러.md "wikilink") 도달하는 것을 의미한다.\[8\] 이러한 종류의 전송을 [유니캐스트](../Page/유니캐스트.md "wikilink")라 부른다. 유니캐스트 프레임은 [충돌 도메인](https://ko.wikipedia.org/wiki/충돌_도메인 "wikilink") 안의 모든 노드에 전송되어, 일반적으로 가장 가까운 [네트워크 스위치나](../Page/네트워크_스위치.md "wikilink") 라우터에 이르게 된다. 스위치는 어느 포트가 해당 MAC 주소에 도달하는지 알 수 없는 상황이라면 유니캐스트 프레임을 모든 포트에 걸쳐 포워드하고, 도달 여부를 알 수 있다면 적절한 포트로 전송한다. (프레임을 시작한 포트는 제외)\[9\]\[10\] 일치하는 하드웨어 MAC 주소가 있는 노드만 프레임을 받아들이며, 일치하지 않은 MAC 주소의 네트워크 프레임은 장치가 [무차별 모드에서](https://ko.wikipedia.org/wiki/무차별_모드 "wikilink") 동작하지 않으면 무시된다.

첫 옥텟의 최하위 비트를 1로 설정하면, 프레임은 한 번만 전송된다. 그러나 NIC는 MAC 주소 일치 외에 다른 기준에 기반하여 이를 받아들일지 선택한다: 예를 들어, 수락되는 멀티캐스트 MAC 주소의 구성 가능한 목록에 따라 결정될 수 있다. 이는 [멀티캐스트](../Page/멀티캐스트.md "wikilink") 어드레싱으로 부른다.

## 응용

다음의 기술들이 MAC-48 식별자 형식을 사용한다:

  - [이더넷](../Page/이더넷.md "wikilink")
  - [802.11](../Page/IEEE_802.11.md "wikilink") 무선 네트워크
  - [블루투스](../Page/블루투스.md "wikilink")
  - IEEE 802.5 [토큰링](../Page/토큰링.md "wikilink")
  - 다른 대부분의 IEEE 802 네트워크
  - [FDDI](https://ko.wikipedia.org/wiki/광섬유_분산_데이터_인터페이스 "wikilink") (광섬유 분산 데이터 인터페이스)
  - [ATM](../Page/비동기_전송_방식.md "wikilink") ([NSAP 주소의](https://ko.wikipedia.org/wiki/NSAP_주소 "wikilink") 일부로서, 교환 가상 연결 전용)
  - [파이버 채널](../Page/파이버_채널.md "wikilink"), [직렬 SCSI](https://ko.wikipedia.org/wiki/직렬_SCSI "wikilink") ([월드 와이드 네임의](https://ko.wikipedia.org/wiki/월드_와이드_네임 "wikilink") 일부)
  - [ITU-T](../Page/ITU-T.md "wikilink") [G.hn](https://ko.wikipedia.org/wiki/G.hn "wikilink") 표준 (전력선을 이용하여 최대 초속 1기가비트의 LAN 구성 방식을 제공.)

이더넷과 와이파이와 같은 IEEE 802 네트워크에 연결하는 모든 장치는 MAC-48 주소가 있다. MAC-48을 사용하는 일반적은 컨슈머 장치에는 모든 PC, 스마트폰, 태블릿 컴퓨터가 포함된다.

EUI-64 식별자는 다음에 쓰인다:

  - [파이어와이어](https://ko.wikipedia.org/wiki/파이어와이어 "wikilink")
  - [IPv6](../Page/IPv6.md "wikilink")
  - [직비](../Page/직비.md "wikilink") / [802.15.4](https://ko.wikipedia.org/wiki/IEEE_802.15 "wikilink") / [6LoWPAN](../Page/6LoWPAN.md "wikilink")

## hosts에서의 이용

이더넷과 같은 브로드캐스트 네트워크에서 MAC 주소는 해당 세그먼트의 각 노드를 고유하게 식별하며 프레임들을 특정 호스트를 위해 구별할 수 있게 도와준다.

영구적이고 전역적인 고유 식별을 위해 고안되었지만 현대의 대부분의 하드웨어의 MAC 주소를 변경할 수 있다. MAC 주소를 변경하는 일은 [네트워크 가상화에서](https://ko.wikipedia.org/wiki/네트워크_가상화 "wikilink") 필수적이다. 보안 취약점을 활용하는 과정에도 사용할 수 있는데, 이를 [MAC 스푸핑](https://ko.wikipedia.org/wiki/MAC_스푸핑 "wikilink")(MAC spoofing)이라고 한다.

## 같이 보기

  - [NSAP 주소](https://ko.wikipedia.org/wiki/NSAP_주소 "wikilink")

## 각주

## 외부 링크

  -
  - [IEEE Registration Authority Tutorials](http://standards.ieee.org/develop/regauth/tut/index.html)

  - [IEEE Public OUI and Company_id Assignment lookup](http://standards.ieee.org/develop/regauth/oui/public.html)

  - [IEEE Public IAB list](http://standards.ieee.org/develop/regauth/iab/iab.txt)

  - [IEEE Public OUI list](http://standards.ieee.org/develop/regauth/oui/oui.txt)

  - [IANA Considerations and IETF Protocol Usage for IEEE 802 Parameters](http://tools.ietf.org/html/rfc5342)

  - [IANA list of Ethernet Numbers](https://web.archive.org/web/20120615170357/http://www.iana.org/assignments/ethernet-numbers)

  - [Wireshark](../Page/와이어샤크.md "wikilink")'s [MAC address list](http://anonsvn.wireshark.org/wireshark/trunk/manuf)

[분류:네트워크 주소](https://ko.wikipedia.org/wiki/분류:네트워크_주소 "wikilink") [분류:매체 접근 제어](https://ko.wikipedia.org/wiki/분류:매체_접근_제어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.   Getting Started with LANs {{\!}} Cisco Support Community {{\!}} 5896 {{\!}} 68421|website=supportforums.cisco.com|access-date=2016-05-17}}
10. [MAC 테이블](https://ko.wikipedia.org/wiki/MAC_테이블 "wikilink")