> This article is converted from Wikipedia: [PCI ](https://ko.wikipedia.org/wiki/PCI_).


[섬네일](https://ko.wikipedia.org/wiki/파일:PCI-Express-Bus-1-lane.jpg "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:PCI-Express-Bus.jpg "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:Gigabyte_GV-NX62TC256D8_Rev_1.0.jpg "wikilink")

**PCI 익스프레스**()는 2002년 [PCI SIG가](https://ko.wikipedia.org/wiki/PCI_SIG "wikilink") 책정한 입출력을 위한 직렬 구조의 [인터페이스이며](https://ko.wikipedia.org/wiki/물리_인터페이스 "wikilink") [인텔](../Page/인텔.md "wikilink") 주도하에 만들어졌다. 공식적인 약어로 **PCIe**로 표기한다. 옛 [PCI](https://ko.wikipedia.org/wiki/PCI "wikilink"), [PCI-X](../Page/PCI-X.md "wikilink")와 [AGP](../Page/가속_그래픽_포트.md "wikilink") [버스](../Page/버스.md "wikilink")를 대체하기 위하여 개발 되었다. PCIe는 앞서 언급한 버스 표준들과 비교하여 높은 시스템 버스 대역폭, 적은 I/O 핀 수, 적은 물리적 면적, 버스 장치들에게 더 뛰어난 성능 확장성, 상세한 오류 검출 및 보고 구조(Advanced Error Reporting (AER)\[1\]), 네이티브 [핫-플러그](https://ko.wikipedia.org/wiki/핫_스와핑 "wikilink") 기능등 여러 장점을 가지고 있다. 최근에는 하드웨어 I/O 가상화도 지원한다.

PCIe 3.0이 현재 생산되는 확장 카드를 위한 최신 버전이며 주류 개인용 컴퓨터에 사용되고 있다.\[2\]\[3\]

## 역사

개발 기간 동안에 PCIe는 HSI (High Speed Interconnect)로 불렸으며 [PCI-SIG](https://ko.wikipedia.org/wiki/PCI-SIG "wikilink")가 이름을 PCI 익스프레스로 최종 결정하기 전까지 3GIO (3세대 입출력)라는 이름을 가지기도 했다. 인텔 설계팀으로만 구성된 아라파호 워크 그룹(Arapaho Work Group)이라는 기술 그룹이 처음 기본 틀을 설계하였다.

PCIe는 꾸준한 개발과 개선을 거쳐온 기술이다. 현재의 PCI 익스프레스는 버전 3.0이며 버전 4.0이 곧 나오게 될 상황이다.

### PCI 익스프레스 1.0

2004년에 [인텔](../Page/인텔.md "wikilink")이 초당 250MB의 데이터 속도와 초당 2.5 [GT의](https://ko.wikipedia.org/wiki/전송_\(컴퓨팅\) "wikilink") [전송 속도를](https://ko.wikipedia.org/wiki/전송_\(컴퓨팅\) "wikilink") 지닌 PCIe 1.0을 도입하였다.

### PCI 익스프레스 2.0

[PCI-SIG](https://ko.wikipedia.org/wiki/PCI-SIG "wikilink")는 2007년 1월 15일에 2.0 규격을 이용할 수 있다고 발표하였다.\[4\] 이 리비전은 PCIe 1.0 표준의 초당 250MB 속도를 500MB로 두 배 늘린 것이다. 32 레인(lane) PCI 단자 (x32)가 초당 16 GB의 출력을 지원한다는 뜻이다. 초기 버전은 2.5 GT로 동작하였으나 PCIe 2.0은 5.0GT의 기본 클럭 속도로 동작한다.

### PCI 익스프레스 2.1

PCI 익스프레스 3.0에 완전히 추가할 계획이었던 관리, 지원, 문제 해결 시스템의 상당 부분을 지원한다. 그러나 속도는 이전의 PCI 익스프레스 2.0과 같다. 대부분의 메인보드가 PCI 익스프레스 2.0 단자를 달고 판매되고 있다.

### PCI 익스프레스 3.0

PCI 익스프레스 3.0 기본 규격 리비전 3.0은 여러 번 연기되다가 2010년 11월에 발표 되었다. 2007년 8월에 PCI-SIG는 PCI 익스프레스 3.0이 초당 8 [GT의](https://ko.wikipedia.org/wiki/전송_\(컴퓨팅\) "wikilink") 비트레이트를 지원할 것이라고 발표하였다. 기존의 PCIe와 하위 호환된다.\[5\]

PCI Express 3.0은 인코딩 방식을 이전 [8b/10b 인코딩에서](https://ko.wikipedia.org/wiki/8b/10b_인코딩 "wikilink") 128b/130b으로 개선하였다. 이것으로 대역폭의 오버헤드를 PCI Express 2.0의 20%에서 약 1.54% (= 2/130)로 줄였다. PCI Express 3.0의 8 GT/s 비트율은 이전 세대인 PCI Express 2.0보다 2배 빠른 레인(lane)당 985 MB/s의 대역폭을 제공한다.\[6\]

2010년 11월 18일에 PCI-SIG는 공식적으로 PCI Express 3.0 최종 규격을 PCI-SIG 구성원들에게 발표하여 이 새로운 규격에 맞춰 장치들을 개발할 수 있도록 하였다.\[7\]

### PCI 익스프레스 4.0

2011년 11월 29일에 PCI-SIG는 구리 기술 기반의 16 GT/s를 지원하는 PCI Express 4.0 규격을 발표하였다. 동적 및 유휴 전력 최적화 방법들이 추가되었으며 최종 사양은 2017년에 발표될 것으로 예상한다.\[8\]

2017년 10월 인텔은 4.0규격을 정식 발표했다.[PCIe 4.0 Blog](https://pcisig.com/sites/default/files/newsroom_attachments/PCIe%204.0%20Blog.pdf) 해당 내용 관련하여 한글 벤치마크 사이트에서 소개. 출처: 보드나라. [PCIe 4.0 수명은 2년? PCIe 5.0 규격 2019년 목표로 개발 중](https://www.bodnara.co.kr/bbs/article.html?num=142240)

### PCI 익스프레스 5.0

상기 4.0의 규격 발표와 동시에 5.0은 2019년 2분기(2Q) 목표로 하고 있음을 게시함. (4.0의 링크 참조) 2019년 1월 버전 0.9를 발표. (영문 사이트 원본은 아니고, 한글 벤치마크 사이트에서 링크. 출처: 보드나라. [PCIe 4.0보다 두 배 빠른 PCIe 5.0 0.9규격 공식 발표](https://www.bodnara.co.kr/bbs/article.html?num=152194)

## 물리 규격

| 선로  | 총 핀 수 | 주요 절반 구분핀 수 | 길이    | 주요 절반 구분핀 길이 |
| --- | ----- | ----------- | ----- | ------------ |
| x1  | 36    | 14          | 25 mm | 7.65 mm      |
| x4  | 64    | 42          | 39 mm | 21.65 mm     |
| x8  | 98    | 76          | 56 mm | 38.65 mm     |
| x16 | 164   | 142         | 89 mm | 71.65 mm     |

## 폼 팩터

### PCI 익스프레스 (표준)

#### 핀 배치

| 핀               | 사이드 B     | 사이드 A    | 설명                                                                                              |
| --------------- | --------- | -------- | ----------------------------------------------------------------------------------------------- |
| 1               | \+12V     | PRSNT1\# | 카드 장착 여부를 확인                                                                                    |
| 2               | \+12V     | \+12V    |                                                                                                 |
| 3               | Reserved  | \+12V    |                                                                                                 |
| 4               | Ground    | Ground   |                                                                                                 |
| 5               | SMCLK     | TCK      | [SM버스](https://ko.wikipedia.org/wiki/SM버스 "wikilink") 및 [JTAG](../Page/JTAG.md "wikilink") 포트 핀 |
| 6               | SMDAT     | TDI      |                                                                                                 |
| 7               | Ground    | TDO      |                                                                                                 |
| 8               | \+3.3V    | TMS      |                                                                                                 |
| 9               | TRST\#    | \+3.3V   |                                                                                                 |
| 10              | \+3.3Vaux | \+3.3V   | [대기 전력](https://ko.wikipedia.org/wiki/대기_전력 "wikilink")                                         |
| 11              | WAKE\#    | PWRGD    | 연결을 다시 활성화 (대기 모드에서 깨어남).                                                                       |
| 키 노치(Key notch) |           |          |                                                                                                 |
| 12              | Reserved  | Ground   |                                                                                                 |
| 13              | Ground    | REFCLK+  | 참조 클럭차 동작                                                                                       |
| 14              | HSOp(0)   | REFCLK-  | 레인(Lane) 0 송신 데이터, + 와 −                                                                        |
| 15              | HSOn(0)   | Ground   |                                                                                                 |
| 16              | Ground    | HSIp(0)  | 레인(Lane) 0 수신 데이터, + 와 −                                                                        |
| 17              | PRSNT2\#  | HSIn(0)  |                                                                                                 |
| 18              | Ground    | Ground   |                                                                                                 |
|                 |           |          |                                                                                                 |
| 19              | HSOp(1)   | Reserved | 레인(Lane) 1 송신 데이터, + 와 −                                                                        |
| 20              | HSOn(1)   | Ground   |                                                                                                 |
| 21              | Ground    | HSIp(1)  | 레인(Lane) 1 수신 데이터, + 와 −                                                                        |
| 22              | Ground    | HSIn(1)  |                                                                                                 |
| 23              | HSOp(2)   | Ground   | 레인(Lane) 2 송신 데이터, + 와 −                                                                        |
| 24              | HSOn(2)   | Ground   |                                                                                                 |
| 25              | Ground    | HSIp(2)  | 레인(Lane) 2 수신 데이터, + 와 −                                                                        |
| 26              | Ground    | HSIn(2)  |                                                                                                 |
| 27              | HSOp(3)   | Ground   | 레인(Lane) 3 송신 데이터, + 와 −                                                                        |
| 28              | HSOn(3)   | Ground   |                                                                                                 |
| 29              | Ground    | HSIp(3)  | 레인(Lane) 3 수신 데이터, + 와 −                                                                        |
| 30              | Ground    | HSIn(3)  |                                                                                                 |
| 31              | PRSNT2\#  | Ground   |                                                                                                 |
| 32              | Ground    | Reserved |                                                                                                 |

PCI 익스프레스 4배속 단자 핀 출력

1배속 슬롯은 이것보다 더 짧고 핀 18 직후에서 끝난다. 8배속과 16배속 슬롯은 이 패턴을 확장한다.

| Ground 핀                                                  | 0 볼트 참조                          |
| --------------------------------------------------------- | -------------------------------- |
| 전력 핀                                                      | 전력을 PCIe 카드에 공급                  |
| 출력 핀                                                      | 신호를 카드에서 메인보드로 보냄                |
| 입력 핀                                                      | 신호를 메인보드에서 카드로 보냄                |
| [오픈 드레인](https://ko.wikipedia.org/wiki/오픈_컬렉터 "wikilink") | 여러 개의 카드가 장착되었는지, 또 낮게 장착되었는지 확인 |
| 감지 핀                                                      | 카드가 잘 장착되었는지 확인                  |
| Reserved                                                  | 현재 쓰이지 않음. 연결하지 말 것.             |

범례

### PCI 익스프레스 미니 카드

PCI 익스프레스 미니 카드 (미니 PCI 익스프레스, 미니 PCIe, 미니 PCI-E로도 불림)는 [미니 PCI](../Page/PCI_버스.md "wikilink") 폼 팩터를 대체한다. 이것은 [PCI-SIG](https://ko.wikipedia.org/wiki/PCI-SIG "wikilink")가 개발한 것이다. 호스트 장치는 PCI 익스프레스와 [USB](../Page/USB.md "wikilink") 2.0 연결을 둘 다 지원한다. 2005년 뒤에 제조된 대부분의 노트북 컴퓨터는 PCI 익스프레스에 기반을 두며 미니 카드 슬롯도 몇 개 포함되어 있다.

##### 크기

PCI 익스프레스 미니 카드의 크기는 30x50.95 밀리미터이다. 두께는 1.0 mm (외부 부품 크기는 제외)이다.

##### 전기적 구성

PCI 익스프레스 미니 카드 모서리 단자는 여러 개의 연결과 버스를 제공한다:

  - PCIex1
  - [USB](../Page/USB.md "wikilink") 2.0
  - [SM버스](https://ko.wikipedia.org/wiki/SM버스 "wikilink")
  - [GPS](../Page/GPS.md "wikilink")
  - [와이파이](../Page/와이파이.md "wikilink")와 같은 무선 네트워크의 진단 LED 상태 선
  - [GSM](../Page/GSM.md "wikilink"), [WCDMA](https://ko.wikipedia.org/wiki/WCDMA "wikilink"), [LTE](https://ko.wikipedia.org/wiki/LTE "wikilink")를 위한 [SIM 카드](../Page/SIM_카드.md "wikilink")
  - 다른 PCIe를 장착할 수 있는 확장(예 : [솔리드 스테이트 드라이브](../Page/솔리드_스테이트_드라이브.md "wikilink"))
  - 1.5 및 3.3 볼트 전력

### 파생된 용어

  - 높이가 낮은 카드.
  - [미니 카드](https://ko.wikipedia.org/wiki/PCI_익스프레스_미니_카드 "wikilink"): [미니 PCI](https://ko.wikipedia.org/wiki/미니_PCI "wikilink") 폼 팩터를 대체.
  - [익스프레스카드](../Page/익스프레스카드.md "wikilink"): [PC 카드](../Page/PC_카드.md "wikilink") 폼 팩터의 뒤를 이음.
  - PCI 익스프레스 익스프레스모듈: 핫 플러깅을 지원하는 모듈러 폼 팩터로 서버와 워크스테이션에서 쓰임.
  - XMC: CMC/[PMC](https://ko.wikipedia.org/wiki/PCI_Mezzanine_Card "wikilink") 폼 팩터와 비슷함. (x4 PCIe 또는 Serial RapidI/O 포함)
  - [AdvancedTCA](https://ko.wikipedia.org/wiki/Advanced_Telecommunications_Computing_Architecture "wikilink"): [콤팩트PCI](https://ko.wikipedia.org/wiki/콤팩트PCI "wikilink")를 보완.
  - [AMC](https://ko.wikipedia.org/wiki/Advanced_Mezzanine_Card "wikilink"): [AdvancedTCA](https://ko.wikipedia.org/wiki/Advanced_Telecommunications_Computing_Architecture "wikilink") 규격을 보완.
  - PCI 익스프레스 외부 케이블링\[9\]
  - [모바일 PCI 익스프레스 모듈](../Page/모바일_PCI_익스프레스_모듈.md "wikilink") (MXM): [엔비디아](../Page/엔비디아.md "wikilink")사가 만든 노트북용 그래픽스 모듈 규격
  - Advanced eXpress I/O Module (AXIOM) 그래픽스 모듈 디자인은 [ATI 테크놀로지스사가](../Page/ATI_테크놀로지스.md "wikilink") 승인함.

## 같이 보기

  - [PCI 버스](../Page/PCI_버스.md "wikilink")
  - [ISA 버스](../Page/ISA_버스.md "wikilink")
  - [EISA](../Page/EISA.md "wikilink")
  - [MCA](https://ko.wikipedia.org/wiki/:en:Micro_Channel_Architecture "wikilink")
  - [AGP](../Page/가속_그래픽_포트.md "wikilink")
  - [VLB](../Page/VESA_로컬_버스.md "wikilink")
  - [PCI-X](../Page/PCI-X.md "wikilink")

## 각주

<references />

## 외부 링크

  - [PCI-SIG: | PCI-Express Specification Info](http://www.pcisig.com/specifications/pciexpress/)

  - [Introduction to PCI Protocol](http://electrofriends.com/articles/computer-science/protocol/introduction-to-pci-protocol/)

  -

  - [영문 위키 PCI Express](https://en.wikipedia.org/wiki/PCI_Express)

[분류:2004년 도입](https://ko.wikipedia.org/wiki/분류:2004년_도입 "wikilink") [분류:메인보드 확장 슬롯](https://ko.wikipedia.org/wiki/분류:메인보드_확장_슬롯 "wikilink") [분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:표준화 기구](https://ko.wikipedia.org/wiki/분류:표준화_기구 "wikilink")

1.
2.
3.
4.
5.  [PCI Express 3.0 Spec Pushed Out to 2010 | News & Opinion | PCMag.com](http://www.pcmag.com/article2/0,2817,2351266,00.asp)
6.
7.
8.
9.  [PCI-SIG - PCI Express External Cable 1.0 Specification](http://www.pcisig.com/specifications/pciexpress/pcie_cabling1.0/)