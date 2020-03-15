> This article is converted from Wikipedia: [JTAG](https://ko.wikipedia.org/wiki/JTAG).


**JTAG**(Joint Test Action Group)은 [디지털 회로에서](../Page/디지털_회로.md "wikilink") 특정 [노드](https://ko.wikipedia.org/wiki/노드 "wikilink")의 디지털 입출력을 위해 [직렬 통신](../Page/직렬_통신.md "wikilink") 방식으로 출력 데이터를 전송하거나 입력데이터를 수신하는 방식을 말한다. JTAG('제이택'으로 발음)은 [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") 1149.1에 표준으로 정해져 있다.\[1\] 보통 디지털 회로의 칩 외부와 연결되는 핀의 입출력회로에 적용하여 활용한다. 회로 설계에 따라 [디지털 회로의](../Page/디지털_회로.md "wikilink") 내부로 전송하거나 핀의 외부로 데이터를 출력할 수도 있고 상태를 읽을 수도 있다. JTAG을 통해 데이터를 동기식 [직렬 통신](../Page/직렬_통신.md "wikilink") 전송하는 방식은 boundary scan을 통해 구현한다.

[임베디드 시스템](../Page/임베디드_시스템.md "wikilink") 개발 시에 사용하는 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink") 장비가 대표적인 활용 예이다. [임베디드 시스템을](../Page/임베디드_시스템.md "wikilink") 개발하기 위해 통합한 회로로 사용되며, CPU의 기계어 코드를 실행하지 않고 MCU 내부의 [플래시 메모리나](../Page/플래시_메모리.md "wikilink") 임베디드 장치에서 CPU의 외부 플래시 메모리에 코드를 쓰거나 읽을 수 있다.

또한 디버거가 CPU 동작과 연동하여 특정 기계어 코드 위치에서 멈추고 상태를 읽어 내부의 상태를 알 수 있다.

## 개념

다층기판 보드가 등장하면서 기존의 보드 테스트 방식은 안정성과 비용에 문제를 일으키게 되었고, 이러한 문제점을 해결하기 위해 80년대 중반에 Joint European Test Access Group이란 단체가 결성되어 a serial shift register around the boundary of the device라는 개념을 발전시켜 탄생하게 되었다. 일반적으로 JTAG이란 말보다는 Boundary-Scan이란 말을 더 많이 사용한다.

JTAG의 작동 방식은 칩 내부에 Boundary Cell을 만들어 이것이 외부의 핀과 일대 일로 연결되어, 프로세서가 할 수 있는 동작을 중간의 Cell을 통해 인위적으로 수행할 수 있도록 하는 것이다. 이런 방식으로 JTAG은 다양한 하드웨어의 테스트나 연결 상태등을 체크할 수 있다.

## 구성

JTAG 인터페이스는 다음과 같은 핀으로 칩 안에 구성된다.

1.  TDI (데이터 입력) : Test하기 위한 데이터 신호. TMS에 의해 전이된 TAP state에 따라, TDI가 command/data 가 결정됨
2.  TDO (데이터 출력) : Test한 결과를 외부에서 모니터링 하기 위한 pin, 이 역시 TAP state에 따라 address/data가 될 수 있음.
3.  TCK ([클럭](https://ko.wikipedia.org/wiki/클럭 "wikilink")) : Test clock
4.  TMS (모드) : Test Mode로 전환하기 위한 제어 신호
5.  TRST (리셋)

더 자세한 것은 아래의 그림을 참고하라. (테스트 리셋 신호를 표시하지 않았음) [center](https://ko.wikipedia.org/wiki/파일:Jtag_chain.svg "wikilink")

또, JTAG 라인(엄밀하게 이야기 하면 boundary scan cell)을 통해 칩 내부를 조사(Capture 기능) 및 제어(INTEST 기능)를 할 수 있다.

데이터 라인은 한개만이 유효하기 때문에, 프로토콜은 시리얼 방식을 사용한다. 클럭 입력은 TCK 핀으로 , 설정은 TMS 핀을 사용하며, 동작 주파수는 10-100MHz (10-100ns/bit)가 일반적으로 사용된다.

그 밖에도 EXTEST 기능을 이용하여 임베디드 시스템의 다른 칩을 제어 할 수도있다. 예로는 임베디드 시스템의 ROM(NOR Flash일 경우 등), NAND Flash 등의 내용을 기록하거나 읽어 낼 수 있다. [리눅스](../Page/리눅스.md "wikilink")의 부트로더등을 다운로드하여 아무런 코드도 없는 임베디드 시스템을 부팅하게 만들 수 있다.

## 기능

프로세서(CPU)의 상태와는 상관 없이 디바이스의 모든 외부 핀을 구동시키거나 값을 읽어 들일 수 있는 기능을 제공한다.

JTAG은 디바이스 내에서 모든 외부와의 연결점, 즉 각각의 핀들을 Boundary Cell과 일대일로 연결하고, 각각의 Cell은 boundary scan register를 형성하기 위해 서로 연결한다. 전체적인 인터페이스는 5개의 핀(TDI, TMS, TCK, nTRST, TDO)을 통해 제어한다. 이렇게 준비한 상태에서 디바이스 간의 연결 상태를 테스트하거나, 플래시 메모리에 퓨징(fusing)하는 기능을 한다.

## 같이 보기

  - ICE(in-circuit emulation)
  - [소자 프로그래머](../Page/소자_프로그래머.md "wikilink")

## 각주

<references />

[분류:IEEE 표준](https://ko.wikipedia.org/wiki/분류:IEEE_표준 "wikilink") [분류:임베디드 시스템](https://ko.wikipedia.org/wiki/분류:임베디드_시스템 "wikilink") [분류:전자공학 제조](https://ko.wikipedia.org/wiki/분류:전자공학_제조 "wikilink") [분류:디지털 회로](https://ko.wikipedia.org/wiki/분류:디지털_회로 "wikilink") [분류:전자공학](https://ko.wikipedia.org/wiki/분류:전자공학 "wikilink")

1.  [IEEE 1149.1-2001](http://standards.ieee.org/reading/ieee/std_public/description/testtech/1149.1-2001_desc.html)