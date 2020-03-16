> This article is converted from Wikipedia: [RAPIEnet](https://ko.wikipedia.org/wiki/RAPIEnet).


|                               RAPIEnet                               |
| :------------------------------------------------------------------: |
| [400px](https://ko.wikipedia.org/wiki/파일:RAPIEnet_로고.png "wikilink") |
|       [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink") 정보       |
|                           Type of Network                            |
|                            Physical Layer                            |
|                           Network Topology                           |
|                          Device Addressing                           |
|                        Network Configuration                         |
|                                                                      |

**RAPIEnet**(Real-time Automation Protocols for Industrial Ethernet)은 실시간 데이터 전송을 위한 [대한민국](../Page/대한민국.md "wikilink") 최초의 산업용 [이더넷](../Page/이더넷.md "wikilink") 국제표준규격이다.

  - 이더넷 기반의 실시간성을 보장하는 산업용 네트워크.\[1\][LS산전](../Page/LS산전.md "wikilink")에서 독자 개발한 통신방식으로, 대한민국 최초로 산업용 통신망이 국제표준으로 등록되어 있다.\[2\] (IEC 61158-3-21: 2010, IEC 61158-4-21: 2010, IEC 61158-5-21: 2010, IEC 61158-6-21: 2010, IEC 61784-2: 2010)

<!-- end list -->

  - 두개의 포트의 이더넷 스위치를 기기에 내장하여 별도의 외장 스위치 없이 데이지 체인 방식으로 네트워크 확장을 이루고, 유연한 설치가 용이하며 배선 절감 효과를 가지고 있다.\[3\]

<!-- end list -->

  - 100Mbps/1Gbps 전송속도 및 전기/광 미디어를 혼용하여 사용할 수 있다.\[4\]\[5\]

<!-- end list -->

  - 전송방법으로는 Unicast, Multicast, Broadcast기능을 지원한다.\[6\]

<!-- end list -->

  - "Store & Forward”와 “Cut Through”기능을 지원한다.\[7\]

## 취득 규격(국내/외)

### 국제 취득 규격

  - IEC 61158-3-21: 2010, Industrial communication networks - Fieldbus specifications - Part 3-21: Data-link layer service definition - Type 21 elements.\[8\] </br>
  - IEC 61158-4-21: 2010, Industrial communication networks - Fieldbus specifications - Part 4-21: Data-link layer protocol specification - Type 21 elements.\[9\] </br>
  - IEC 61158-5-21: 2010, Industrial communication networks - Fieldbus specifications - Part 5-21: Application layer service definition - Type 21 elements.\[10\] </br>
  - IEC 61158-6-21: 2010, Industrial communication networks - Fieldbus specifications - Part 6-21: Application layer protocol specification - Type 21 elements.\[11\] </br>
  - IEC 61784-2: 2010, Industrial communication networks - Profiles - Part 2: Additional fieldbus profiles for real-time networks based on ISO/IEC 8802-3.\[12\] </br>
  - IEC 62439-7, Industrial communication networks - High availability automation networks - Part 7: Ring-based Redundancy Protocol (RRP)\[13\]</br>

### 국내 취득 규격

  - KSCIEC 61158-3-21 : 계측제어를 위한 디지털 데이터 통신-산업제어시스템에서 사용되는 필드버스-제3부:데이터링크 서비스 정의</br>
  - KSCIEC 61158-4-21 : 계측제어를 위한 디지털 데이터 통신-산업제어시스템에서 사용되는 필드버스-제4부:데이터링크 프로토콜 규격</br>
  - KSCIEC 61158-5-21 : 계측제어를 위한 디지털 데이터 통신-산업제어시스템에서 사용되는 필드버스-제5부:응용계층 서비스 정의</br>
  - KSCIEC 61158-6-21 : 계측제어를 위한 디지털 데이터 통신-산업제어시스템에서 사용되는 필드버스-제6부:응용계층 프로토콜 규격

<small>출처 = KATS(지식경제부 기술표준원)</small>\[14\]

## RAPIEnet 기술

### 프로토콜 스택 구조

[섬네일](https://ko.wikipedia.org/wiki/파일:RAPIEnet_프로토콜_구조.png "wikilink") {{-}}

### 내장 듀얼 포트 스위치 동작

[섬네일](https://ko.wikipedia.org/wiki/파일:내장_듀얼_포트_스위치_동작.png "wikilink") {{-}}

  - 실시간 데이터 전송을 위해 하드웨어 기반으로 처리되는 내장스위치를 채택하였다.
  - 전이중 통신을 지원하여 링형 토폴로지로 연결된 경우 각 노드가 이중화된 연결경로를 갖고 있다.

{{-}}

### 프레임 포맷

[섬네일](https://ko.wikipedia.org/wiki/파일:RAPIEnet_프레임_포맷.png "wikilink") {{-}}

  - RAPIEnet Ether type: 0x88FE\[15\]

### 토폴로지

[섬네일](https://ko.wikipedia.org/wiki/파일:선형_토폴로지.png "wikilink") {{-}}

[섬네일](https://ko.wikipedia.org/wiki/파일:링형_토폴로지.png "wikilink") {{-}}

### 복구 시스템

  - 내장스위치와 전이중 통신방식으로 인해 이중화 연결경로를 가지며, 통신장애에 대한 내성을 갖고 있다, 이를통해 빠른 장애복구 능력을 가진다.

<!-- end list -->

  -
    \- 복구 시간 \< 10 ms\[16\]

{{-}} [섬네일](https://ko.wikipedia.org/wiki/파일:링형에서의_복구.png "wikilink") {{-}}

1.  디바이스1에서 디바이스3으로 신호를 전달한다.
2.  디바이스2와 디바이스3 사이에 fault발생.
3.  디바이스2에서 디바이스1로 문제가 발생했음을 전달한다.
4.  디바이스1에서 반대방향으로 디바이스3에게 신호를 전달한다.

### Flexible Hybrid Structure

[섬네일](https://ko.wikipedia.org/wiki/파일:구리선과_광선혼합1.png "wikilink") {{-}}

  - Fiber Optics/Copper Media

<!-- end list -->

  -
    \- Copper: 낮은 설치 비용이 들지만 노이즈가 상대적으로 크다 .
    \- Optics: 높은 설치 비용이 들지만 노이즈가 적으며 상대적으로 배선거리가 길다.

<!-- end list -->

  - 각각의 장단점을 가진 두 가지의 회선을 복합적으로 사용하여 간편하고 효율적인 배선을 할 수 있다.

{{-}}

## RAPIEnet을 이용한 시스템 구성도

[섬네일](https://ko.wikipedia.org/wiki/파일:RAPIEnet을_이용한_시스템구성도.png "wikilink") {{-}}

## 기타

### 추가 진행 중인 국제표준

  - IEC 61784-5-17, Industrial communication networks - Profiles - Part 5-17: Installation of fieldbuses - Installation profiles for CPF 17 (2012년 IEC 국제표준 등록 예정)\[17\]</br>

## 각주

<references />

[분류:이더넷](https://ko.wikipedia.org/wiki/분류:이더넷 "wikilink") [분류:컴퓨터 네트워크](https://ko.wikipedia.org/wiki/분류:컴퓨터_네트워크 "wikilink")

1.
2.  [RAPIEnet관련 보도자료](http://www.upkorea.net/news/articleView.html?idxno=19909)
3.
4.
5.  [ISO/IEC 8802-3: 2000](http://webstore.iec.ch/preview/info_isoiec8802-3%7Bed6.0%7Den.pdf)
6.
7.
8.  [IEC 61158-3-21: 2010](http://webstore.iec.ch/preview/info_iec61158-3-21%7Bed1.0%7Den.pdf)
9.  [IEC 61158-4-21: 2010](http://webstore.iec.ch/preview/info_iec61158-4-21%7Bed1.0%7Den.pdf)
10. [IEC 61158-5-21: 2010](http://webstore.iec.ch/preview/info_iec61158-5-21%7Bed1.0%7Den.pdf)
11. [IEC 61158-6-21: 2010](http://webstore.iec.ch/preview/info_iec61158-6-21%7Bed1.0%7Den.pdf)
12. [IEC 61784-2: 2010](http://webstore.iec.ch/preview/info_iec61784-2%7Bed2.0%7Den.pdf)
13. [IEC 62439-7](http://www.iec.ch/cgi-bin/restricted/getfile.pl/65C_656e_RVC.pdf?dir=65C&format=pdf&type=_RVC&file=656e.pdf)
14. [KATS(지식경제부 기술표준원)](http://www.kats.go.kr/)
15. [IEEE - Ether type](http://standards.ieee.org/develop/regauth/ethertype/eth.txt)
16.
17. [IEC 61784-5-17](http://www.iec.ch/cgi-bin/restricted/getfile.pl/65C_641ea_CD.pdf?dir=65C&format=pdf&type=_CD&file=641ea.pdf)