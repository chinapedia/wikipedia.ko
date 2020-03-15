> This article is converted from Wikipedia: [CalDriCon](https://ko.wikipedia.org/wiki/CalDriCon).


**CalDriCon**는 고해상도의 액정디스플레이의 드라이버 인터페이스의 하나로 모바일 기기, LCD TV향으로 THine Electronics사에 의해 개발되었다.

## 개요

  - 클럭과 데이터 분리형 Point-to-Point 연결에 의한 데이터 전송.
  - 전송속도：～2.0Gbps/lane
  - Driver IC측에서 수신용 샘플링 최적 포인트를 판단하여, 송신측에서의 클럭과 데이터의 위상조정을 실시함으로써 클럭과 데이터의 Skew를 조정.
  - 송신측 Pre-emphasis에 의해 전송파형의 신호품질(Signal Integrity, SI)을 보상. 파형특성이 좋지 않은 저가의 케이블을 사용해도 안정적인 전송이 가능.
  - 송신측과 수신측 양쪽을 Termination하는 것으로 Multi drop시의 전송로 분기에 의한 반사 영향을 억제할 수 있음.
  - 스프레드 스펙트럼을 인가할 수 있어서, 전체적인 시스템에서 EMI(Electro-Magnetic Interference) Noise를 억제할 수 있음.
  - 고화질 화상 전송에서는 핀수, 케이블수를 mini-LVDS등의 타 Driver Interface보다 더 줄일수 있어, 전체적인 원가절감과 공간절약이 가능

## LCD 드라이버 인터페이스 고속화 경위

2000년경 액정디스플레이의 드라이버 인터페이스는 Texas Instruments사의 mini-LVDS와 National Semiconductor사의 RSDS등의 기술이 널리 사용되었다. 그러나 액정 드라이버의 용도 중에서도 TV에 대해서는 2005년에 Full HD TV가 등장 했고, 2007년에는 Full HD 120Hz TV가 등장하는 등 고해상도화가 진행되면서 드라이버 인터페이스 에서도 이에 대처 할 수 있는 기술이 필요하게 되었다. 이에 Advanced PPmL, CalDriCon등의 새로운 차세대 드라이버 인터페이스 기술이 제안되었다.

## LCD 드라이버 인터페이스 기술 비교

새로운 차세대드라이버 인터페이스 중에서 CalDriCon은 드라이버 IC의 사용환경을 고려하고 있다고 할 수있다. 2.0Gbps의 고속화, 클럭과 데이터의 Skew 조정, 전원과 GND노이즈에 대한 내성이 강한것으로 나타나 있다.

|                                          |
| :--------------------------------------: |
| <big>**액정 Driver Interface기술의 비교**</big> |
|                    명칭                    |
|              신호선1개당데이터전송속도               |
|                   연결방식                   |
|          Multi drop에 의한 파형품질 열화          |
|              클럭 데이터의 Skew조정              |
|              전원・GND의 노이즈 내성              |

드라이버IC는 통상, Chip On Film (COF)에 의해 필름 형태의 배선 기판상에 직접 실장되기 때문에, 전원과 GND가 흔들리면 쉽게 노이즈 영향을 받을수 있다. mini-LVDS와 RSDS등의 종래의 액정 드라이버 인터페이스는 차동신호전송기술을 바탕으로 하고 있어 이러한 노이즈에 대한 내성은 강하나 클럭과 데이터의 Skew 조정이 불가능 하기 때문에 1Gbps를 넘어선 고속화 실현에는 어려움이 동반되었다. 이에 대해 차세대 드라이버 인터페이스 대부분이 Clock Data Recovery (CDR) 기술을 이용함으로써 클럭과 데이터의 Skew조정은 불필요하게 되었고, 이로 인해 데이터 전송률이 1.6Gbps등, 1Gbps를 넘어서는 수준에서 고속화를 실현하는데 성공을 하였다. 그러나 CDR기술을 이용한 드라이버 인터페이스는 데이터를 수신하는 드라이버IC의 위상 동기회로 (Phase Locked Loop, PLL)가 필요하고, COF에 의한 필름형태의 배선기판위에 있기 때문에 일반적으로는 전원과 GND의 노이즈 영향을 받기 쉽다. CalDriCon은 클럭을 임베디드 하는 대신 드라이버 IC측에서의 수신용 샘플링 최적 포인트 를 판단하여 그 정보를 송신측의 클럭과 데이터의 위상조정을 실행, 반영하게 되므로 고속화를 실현하면서 Skew문제를 해결하고, 전원이나 GND가 흔들려도 내성이 강한 드라이버 인터페이스가 되어있다. 또한, mini-LVDS는 BUS연결을 기본으로 하고, 연결하는 드라이버 개수 증가와 더불어 전송로의 분기도 증가하고, 그 반사에 의한 파형이 열화하는 형태의 영향을 받는다. 이에 대해서 CalDriCon을 포함한 차세대 인터페이스의 대부분이 Point-to-Point연결로 전송로 분기의 영향을 받지 않으면서 전송로의 반사에 의한 파형열화 영향은 BUS연결 인터페이스에 비해 적다.

## 참고 문헌

  - 「액정드라이버의 고속화 물결 2 GBit/sec의 전송기술이 실용화」Nikkei Electronics 2010/11/01호（p12～p13）
  - [2Gbps传输走向实用化 液晶驱动器掀高速化浪潮(本文转自电子工程世界)](http://www.eeworld.com.cn/szds/2010/1124/article_2285.html)

## 같이 보기

  - [V-by-One HS](../Page/V-by-One_HS.md "wikilink")

## 외부 링크

  - [THine Electronics](https://web.archive.org/web/20120719050310/http://www.thine.co.jp/index_e.php)

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")