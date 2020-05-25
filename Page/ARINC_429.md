> This article is converted from Wikipedia: [ARINC 429](https://ko.wikipedia.org/wiki/ARINC_429).


**[ARINC](../Page/ARINC.md "wikilink") 429**\[1\]는 항공전자 시스템을 위한 데이터 포맷이다. 제공되는 것은 기본적인 기능을 기술하고, 항공기 디지털 정보 시스템을 위한 인터페이스가 있다. ARINC 429는 오늘날 가장 사용량이 많은 [데이터 버스이다](https://ko.wikipedia.org/wiki/데이터_버스 "wikilink").

## 기술적인 기술

ARINC 429는 두 개의 와이어로 구성된 데이터 버스가 있는데 상용기, 수송기에 적용되고 있다. 연결하는 와이어는 트위스트 페어(twisted pairs)로 되어 있다. 워드(Word)는 32 비트의 길이이고, 대부분의 메시지는 한 개의 데이터 워드로 구성된다. 규격에는 전기적 데이터 특성 및 프로토콜을 정의하였다. ARINC 429는 단방향 데이터 버스 규격(Tx와 Rx 각각 분리)을 사용하는데 Mark 33 Digital Information Transfer System (DITS)으로 알려져 있다. 메시지가 전달되는데 12.5 또는 100 kbit/s 속도가 된다. 전달기(transmitter)는 항상 32-bit data words 또는 NULL 상태로 보낸다. 한개의 버스 상에 20개 이상의 수신기(receiver)가 붙지 않는다.

## ARINC 429 워드 포맷

각 ARINC 워드는 5개의 영역으로 구성된 32 비트 값을 갖는다. :

  - 비트 32는 패리티 비트이고 워드 데이터 정상여부를 확인하기 위해 사용된다.
  - 비트 30 \~ 31는 Sign/Status Matrix 또는 SSM으로 가끔 워드 데이터 정상 여부를 나타낸다.
      - OP (operational) - 워드 내의 데이터가 정상임을 지시한다.
      - TEST - 테스트 소스에 의해 데이터가 제공되고 있음을 지시한다.
      - FAIL - 데이터가 분실되어 일어나는 하드웨어 고장을 지시한다.
      - NCD (No Computed Data) - 하드웨어 고장이 아닌 다른 이유로 데이터가 분실 또는 부정확함을 지시한다. 예를 들어 자동 조정 장치가 켜지지 않은 상태에서 자동 조정 명령이 나타나는 경우이다.
          - SSM은 방위와 같은 데이터 또는 정보의 부호를 지시할 수 있다.

<!-- end list -->

  - 비트 11 \~ 29는 데이터를 포함한다. Bit-field, [Binary Coded Decimal](https://ko.wikipedia.org/wiki/Binary_Coded_Decimal "wikilink") (BCD), binary encoding (BNR)가 ARINC 429 공통 데이터 포맷이다. 데이터 포맷을 혼합할 수 있다.

<!-- end list -->

  - 비트 9 \~ 10은 Source/Destination Identifiers (SDI)와 어떤 수신기로부터 데이터가 왔는지를 지시한다.

<!-- end list -->

  - 비트 1 \~ 8은 라벨을 포함한다. 표현은 8진수로 되어 있다.

## 라벨

라벨 가이드라인은 ARINC 429 규격의 일부로 다양한 장비 타입을 위해 제공된다. 각 항공기에는 수많은 다른 시스템을 포함하고 있는데 Flight Management Computers, Inertial Reference Systems, Air Data Computers, Radio Altimeters, Radios, GPS Sensors 등이다. 예를 들어 Air Data Computer는 바로메트릭 고도를 라벨 204로 제공함으로 대부분의 컴퓨터가 이것을 적용하도록 유도한다.

## 관련 항목

  - ARINC 429는 [ARINC 708](https://ko.wikipedia.org/wiki/ARINC_708 "wikilink") [기후 레이다](https://ko.wikipedia.org/wiki/기후_레이다 "wikilink") 시스템에 사용된다.

## 각주

## 외부 링크

규격서

  - <http://www.arinc.com/>

제작업체

  - [ARINC 429 Interface Products (Excalibur Systems, Inc.)](http://www.mil-1553.com/Templates/showpage.asp?DBID=1&TMID=86&FID=210)
  - [ARINC 429 Interface and Analyser Products (Ballard Technology, Inc.)](http://www.ballardtech.com/products.aspx/dir/protocol/ARINC_429/?link=Wikipedia)
  - [ARINC 429 Interface Products (Condor Engineering, Inc. Now Part of GE Fanuc Embedded Systems)](https://web.archive.org/web/20081119231425/http://www.gefanucembedded.com/products/family/16/AFC-WIK)
  - [ARINC 429 Interface Products (MAX Technologies, Inc.)](https://web.archive.org/web/20061018162904/http://www.maxt.com/Product_IPM_ARINC_429_overview.asp)
  - [ARINC-429 Interface Products (Data Device Corporation)](https://web.archive.org/web/20081121085844/http://www.ddc-web.com/products/cards/arinc.asp)

교육자료

  - [ARINC 429 Tutorial](https://web.archive.org/web/20081120000832/http://www.gefanucembedded.com/news-events/whitepapers/1956/AFC-WIK) by Condor Engineering, Now part of GE Fanuc Embedded Systems (registration required)

[분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:ARINC](https://ko.wikipedia.org/wiki/분류:ARINC "wikilink") [분류:표준](https://ko.wikipedia.org/wiki/분류:표준 "wikilink")

1.