> This article is converted from Wikipedia: [USB](https://ko.wikipedia.org/wiki/USB).


**범용 직렬 버스**(, )는 컴퓨터와 주변 기기를 연결하는 데 쓰이는 입출력 표준 [프로토콜의](../Page/통신_프로토콜.md "wikilink") 하나이다.

## 배경

[직렬 포트](../Page/직렬_포트.md "wikilink"), [병렬 포트](../Page/병렬_포트.md "wikilink") 등 다양한 기존의 연결 방식을 대체하기 위하여 만들어졌다. [키보드](../Page/컴퓨터_자판.md "wikilink"), [마우스](../Page/마우스.md "wikilink"), [게임패드](../Page/게임패드.md "wikilink"), [조이스틱](../Page/조이스틱.md "wikilink"), [스캐너](../Page/이미지_스캐너.md "wikilink"), [디지털 카메라](../Page/디지털_카메라.md "wikilink"), [프린터](../Page/프린터.md "wikilink"), [PDA](https://ko.wikipedia.org/wiki/PDA "wikilink"), [저장장치](https://ko.wikipedia.org/wiki/저장장치 "wikilink")와 같은 다양한 기기를 연결하는 데 사용되며, 이러한 기기 연결의 대부분은 표준 연결 방식을 이용하여 이루어진다. USB는 [PC를](../Page/개인용_컴퓨터.md "wikilink") 위하여 개발되었지만, 지금은 [PDA](https://ko.wikipedia.org/wiki/PDA "wikilink")나 [비디오 게임 콘솔](../Page/비디오_게임_콘솔.md "wikilink") 등에도 채택되어 사용되며, USB의 전원 공급 기능을 이용한 충전 용도로도 많이 사용된다. 2008년에는 전 세계적으로 약 20억 개의 USB 장치가 있었다.

표준은 USB 임플리멘터스 포럼(USB Implementers Forum; USB-IF)에서 결정하며, 2010년 3월 기준으로 포럼 의장은 인텔사의 제프(Jeff Ravencraft)이다. 컴퓨터 메인보드 시장에서 인텔의 I/O칩 점유율이 압도적\[1\]\[2\](메릴린치의 2004년 3사분기 보고서에 따르면 62.1%)이기 때문에 소비자 시장에서의 가장 큰 수요를 쥐고 포럼 내의 영향력도 가장 큰 [인텔](../Page/인텔.md "wikilink")사에서 주도하여 만들어진다.

경쟁 규격으로 언급되는 [IEEE 1394가](../Page/IEEE_1394.md "wikilink") 주로 캠코더에 탑재되어 [DV규격으로](../Page/디브이.md "wikilink") 주로 사용되는 반면에 USB는 다수의 저가격 기기에 채택되어 있다.

## 구성

USB의 가장 윗 부분에는 주 컨트롤러(host controller)가 있고, 이는 루트 허브를 통해 두 개의 USB 단자를 제공한다. 보통 이 단자에 주변 기기를 연결해 사용하며, 포트가 부족하면 허브를 연결하여 더 많은 포트를 마련할 수 있다. 하나의 주 컨트롤러에는 주변 기기를 나뭇가지 모양으로 127개까지 연결할 수 있다. USB 방식으로 연결된 주변 기기는 대부분 [핫 스와핑을](https://ko.wikipedia.org/wiki/핫_스와핑 "wikilink") 지원하며, USB 방식으로 연결된 주변 기기에는 약간의 전력이 함께 공급된다. 따라서 보통은 외부 전원을 이용하지 않고도 주변 기기를 쉽게 사용할 수 있다. USB 2.0의 정격 전류용량은 5 V 500 mA이며, USB 3.0의 정격 전류용량은 5 V·12 V 900 mA이다.\[3\]

### 연결시에 전기 충격의 감소

연결 단자 속에 4핀 중에서 데이터 전송에 사용되는 2개의 핀은 짧고 전원을 공급해주는 2개의 핀은 길게 되어 있다. 이런 구조적 이점 때문에 연결할 때는 언제나 전원 공급용 핀 2개가 먼저 연결되고 데이터 전송용 핀 2개가 그 후에 연결이 되며, 연결이 해제될 때는 언제나 반대의 순서로 데이터 전송 핀들이 끊어지고 그 후에 전원 공급 핀들이 끊어진다.

이런 이유로 전원 공급과 관련한 2개 핀 중에서 하나는 0이라는 신호에 기준이 되는 접지(ground) 핀인데 접지가 먼저 연결되고 데이터 전송이 시작되거나 끝이 나므로, 연결이 시작되거나 끝나는 시점에 전압과 관련한 [노이즈가](../Page/잡음.md "wikilink") 기계적으로 최소화된다. USB가 출시되기 전에 [시리얼 케이블](https://ko.wikipedia.org/wiki/:en:Serial_cable "wikilink"), 병렬 케이블 기반 [프린터 포트보다](https://ko.wikipedia.org/wiki/:en:Parallel_port "wikilink") 전자적으로 안정화된 구조이다.

## 속도

USB 표준의 이론상 최고 전송 속도는 다음과 같다. [직렬 통신보다](../Page/직렬_통신.md "wikilink") 압도적인 빠른 전송에 비결은 하드웨어 기반의 압축 전송 기술이다.

  - USB 1.0 Low speed(초당 1.5 메가비트)
  - USB 1.1 Full speed(초당 12 메가비트)
  - USB 2.0 High-speed(초당 480 메가비트)
  - USB 3.0 SuperSpeed(초당 5 기가비트)
  - USB 3.1 SuperSpeedPlus(초당 10 기가비트)

USB 초기에는 Low speed로 연결되는 키보드, 마우스 같은 제품들이 있었지만 이제는 거의 쓰이지 않는다. Full speed의 USB 1.0도 1.1 규격으로 업데이트된 다음 USB 2.0으로 전환되었다. 2010년 초 USB 3.0을 적용한 제품들이 나오기 전에는 대부분 USB 2.0을 사용했다. 그러나 USB의 속도에는 치명적인 제약이 있는데 주 컨트롤러(host controller)에 연결된 기기들 간에는 대역폭을 나누어 쓰게 되므로 장치가 늘어날수록 속도는 현저히 떨어진다.

## 역사

1994년 [컴팩](../Page/컴팩.md "wikilink"), [DEC](https://ko.wikipedia.org/wiki/DEC "wikilink"), [IBM](../Page/IBM.md "wikilink"), [인텔](../Page/인텔.md "wikilink"), [마이크로소프트](../Page/마이크로소프트.md "wikilink"), [NEC](https://ko.wikipedia.org/wiki/NEC "wikilink"), [노텔](https://ko.wikipedia.org/wiki/노던_텔레콤 "wikilink") 등 7개사로 이루어진 그룹에서 USB의 개발을 시작하였다\[4\]. 목적은 PC의 뒤에 여러 단자들을 제거함으로써 외부 장치들을 PC로 연결하기 쉽게 만드는 것으로, 기존 인터페이스의 이용성 문제를 해결하고 USB에 장착된 모든 장치들의 소프트웨어 구성을 단순케 하며 외부 장치를 위한 데이터 속도를 증가시킬 수 있게 한다.

### 버전 역사

#### 1.0 이전

  - USB 0.7: 1994년
  - USB 0.8: 1994년 12월 출시
  - USB 0.9: 1995년 4월 출시
  - USB 0.99: 1995년 8월 출시
  - USB 1.0 후보 버전: 1995년 11월 출시

#### USB 1.0

1.5 Mbit/s (Low speed), 12 Mbit/s (Full speed)가 제공된다.

  - USB 1.0: 1996년 1월 출시
  - USB 1.1: 1998년 9월 출시

#### USB 2.0

  - USB 2.0: 2000년 4월

최대 전송속도는 480 Mbit/s (초당속도 60 MByte/s)

#### USB 3.0

[섬네일](https://ko.wikipedia.org/wiki/파일:SuperSpeed_USB.svg "wikilink")

  - SS(Super Speed)라는 명칭으로 사용되며 마이크로소프트와 인텔 등의 회사에서 개발을 마쳤다.
  - [2008년](../Page/2008년.md "wikilink") [11월 17일에](../Page/11월_17일.md "wikilink") SIG(Special Interest Group)에서 USB 3.0 스펙에 대한 표준안 작업이 완료되어 USB 3.0 규격(Rev. 1.0)이 발표되었고, 2010년에 출시되었다.

#### USB 3.1 Gen1

  - 최대 속도는 5 Gbit/s(625 MByte/s)이다. 이전 버전과는 [하위 호환성이](../Page/하위_호환성.md "wikilink") 있으며, USB 2.0 장치를 USB 3.0 포트에 연결하거나 USB 3.0 장치를 USB 2.0 포트에 연결하는 경우 모두 USB 2.0 하위호환 모드로 동작한다. 케이블은 2.0 이전의 4선에서 9선으로 증가하였기 때문에, 3.0 모드로 동작하기 위해서는 3.0 케이블이 필요하다.
  - 전원용으로 공급되는 전압은 이전 버전과 마찬가지로 5 V이나, 최대 전류는 2.0의 500 mA에서 900 mA로 증가하였다.

#### USB 3.1 Gen2

USB 3.1 (Super Speed Plus)은 10 Gbit/s(초당속도 1.25GByte/s)의 전송속도를 내며\[5\], USB 2.0, USB 3.1 Gen 1과 하위 호환성이 있다. [2013년](../Page/2013년.md "wikilink") [7월 26일에](../Page/7월_26일.md "wikilink") 발표되었다.

[섬네일](https://ko.wikipedia.org/wiki/파일:USB_&_Thunderbolt_Speed_Comparison.svg "wikilink") 참고로 이름이 USB 3.2로 변경되었다.

## USB 연결 단자 형태

파일:USB 2.0 connectors.svg|USB 형태에 대한 도식도(2.0 및 이전) 파일:USB 3.0 Micro-B plug.png|마이크로USB 3.0 타입B에 대한 도식도 파일:USB Type-C icon.svg|USB 3.1 규격의 [USB-C](../Page/USB-C.md "wikilink") 단자에 대한 도식도 파일:Usb connectors.JPG|왼쪽부터 마이크로USB 타입B 수, 미니USB(8핀) 타입A 수, 미니USB(5핀) 타입B 수, USB 타입A 암, USB 타입A 수, USB 타입B 수 파일:Mini usb AB.jpg|미니USB 타입A(왼쪽)와 타입B(오른쪽)

## 같이 보기

  - [무선 USB](../Page/무선_USB.md "wikilink")
  - [USB-C](../Page/USB-C.md "wikilink")
  - [IEEE 1394](../Page/IEEE_1394.md "wikilink")

## 각주

<references />

## 외부 링크

  - [www.usb.org](http://www.usb.org)

  - [USB - 네이버 캐스트](http://navercast.naver.com/contents.nhn?contents_id=5125)

[USB](https://ko.wikipedia.org/wiki/분류:USB "wikilink") [분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")

1.
2.  <http://www.channelregister.co.uk/2004/11/01/chipset_market_q3_04/>
3.
4.
5.