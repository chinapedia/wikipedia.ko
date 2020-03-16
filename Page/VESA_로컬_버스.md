> This article is converted from Wikipedia: [VESA  ](https://ko.wikipedia.org/wiki/VESA__).


[섬네일](https://ko.wikipedia.org/wiki/파일:Vlb_svga.jpg "wikilink") VLB 카드\]\] [섬네일](https://ko.wikipedia.org/wiki/파일:Vlb.jpg "wikilink") 위의 VLB 및 [ISA](../Page/ISA_버스.md "wikilink") 슬롯\]\] **VESA 로컬 버스**(**VLB**, **VL버스**)는 1992년 8월 [비디오 일렉트로닉스 표준 협회](../Page/비디오_전자공학_표준위원회.md "wikilink")(VESA)에서 책정한 로컬 버스 규격이다.

VESA 로컬 버스는 [ISA 버스](../Page/ISA_버스.md "wikilink") 밑에 [MCA](https://ko.wikipedia.org/wiki/MCA "wikilink") 단자를 추가하고 거기에 [i486의](../Page/인텔_80486.md "wikilink") 메모리 버스를 바로 연결하는 구조로 ISA 버스가 포트 맵 입출력(port-mapped I/O)과 [인터럽트](../Page/인터럽트.md "wikilink")를 MCA 단자 부분이 메모리 맵 입출력(memory-mapped I/O)과 [DMA를](../Page/직접_메모리_접근.md "wikilink") 담당한다.

VLB 슬롯은 ISA 슬롯의 확장으로 VLB 카드와 ISA 카드 둘 다 장착하여 사용할 수 있으며 [그래픽 카드](../Page/그래픽_카드.md "wikilink"), [SCSI](../Page/SCSI.md "wikilink") 카드, 다중 입출력 카드([IDE](https://ko.wikipedia.org/wiki/고급_기술_결합 "wikilink") 컨트롤러) 등이 출시되었다.

VESA 로컬 버스는 ISA 버스의 제한된 속도를 보완하고자 임시 방편으로 설계된 것으로 몇 가지 문제점이 있었다.

  - **[i486](../Page/인텔_80486.md "wikilink") 의존적이다.**: VESA 로컬 버스는 i486의 메모리 버스를 그대로 이용하고 있기 때문에 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 밖의 다른 아키텍처에 구현하는 것은 거의 불가능했다. 몇몇의 [펜티엄](../Page/펜티엄.md "wikilink") 기판에도 탑재되어 있지만 버스 변환 브릿지를 거치기 때문에 본래의 성능은 발휘할 수 없었다.
  - **사용할 수 있는 슬롯 수가 적다.**: i486 메모리 버스에 바로 연결되어 있어 배선을 많이 늘릴 수 없고 [FSB에도](../Page/프론트_사이드_버스.md "wikilink") 영향을 받아 25MHz에서는 3개, 33MHz 2개, 50MHz는 1개의 슬롯만을 사용할 수 있었다.
  - **신뢰성이 낮다.**: 단거리로 신뢰성이 높은 메모리 버스를 그대로 끌어 낸 구조이기 때문에 오류 검출/정정 기능, 재송신 기능 등이 존재하지 않는다. 그렇기 때문에 노이즈 대책 등이 부족한 저가형 기판의 VLB에 하드 디스크 컨트롤러같은 기기를 사용할 경우 데이터 오류가 일어날 가능성이 있다.
  - **설치성이 나쁘다.**: ISA 버스에 MCA 단자를 추가한 구조이므로 VLB 카드의 길이가 매우 길고 슬롯과의 접촉면이 넓어 장착, 탈착이 나빠 메인보드나 카드가 손상되는 경우도 있었다.

VESA 로컬 버스는 i486 보드에서 흔히 사용되었으나 나중에 [PCI 버스로](../Page/PCI_버스.md "wikilink") 교체되었다.

## 기술 자료

|                                                     |
| :-------------------------------------------------: |
|                     VESA 로컬 버스                      |
|                        버스 폭                         |
|                         핀 수                         |
| [Vcc](https://ko.wikipedia.org/wiki/Vcc "wikilink") |
|                         클럭                          |

## 같이 보기

  - [ISA 버스](../Page/ISA_버스.md "wikilink")
  - [마이크로채널 아키텍처](https://ko.wikipedia.org/wiki/:en:Micro_Channel_Architecture "wikilink")
  - [확장 ISA 버스](../Page/EISA.md "wikilink")
  - [PCI 버스](../Page/PCI_버스.md "wikilink")
  - [가속 그래픽 포트](../Page/가속_그래픽_포트.md "wikilink") (AGP)
  - [PCI 익스프레스](../Page/PCI_익스프레스.md "wikilink") (PCIe)

## 외부 링크

  - [비디오 일렉트로닉스 표준 협회](http://www.vesa.org/)

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink") [분류:컴퓨터 하드웨어](https://ko.wikipedia.org/wiki/분류:컴퓨터_하드웨어 "wikilink") [분류:VESA](https://ko.wikipedia.org/wiki/분류:VESA "wikilink")