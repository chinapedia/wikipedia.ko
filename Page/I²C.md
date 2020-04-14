> This article is converted from Wikipedia: [I²C](https://ko.wikipedia.org/wiki/I²C).


**I²C**(아이스퀘어드시, Inter-Integrated Circuit)는 [필립스](../Page/필립스.md "wikilink")에서 개발한 [직렬](../Page/직렬_통신.md "wikilink") [버스이다](../Page/버스_\(컴퓨팅\).md "wikilink"). [마더보드](https://ko.wikipedia.org/wiki/마더보드 "wikilink"), [임베디드 시스템](../Page/임베디드_시스템.md "wikilink"), [휴대 전화](../Page/휴대_전화.md "wikilink") 등에 저속의 주변 기기를 연결하기 위해 사용된다.

## 설계

I²C 는 [풀업 저항이](https://ko.wikipedia.org/wiki/풀업_저항 "wikilink") 연결된 직렬 데이터(SDA)와 직렬 클럭(SCL)이라는 두 개의 양 방향 [오픈 컬렉터](https://ko.wikipedia.org/wiki/오픈_컬렉터 "wikilink") 라인을 사용한다. 최대 전압은 +5 V 이며, 일반적으로 +3.3 V 시스템이 사용되지만 다른 전압도 가능하다.

I²C [레퍼런스 디자인은](https://ko.wikipedia.org/wiki/레퍼런스_디자인 "wikilink") 7 비트의 [주소 공간을](../Page/주소_공간.md "wikilink") 가지며, 이 중 16개는 예약되어 있으므로, 동일한 버스에 최대 112개의 노드를 연결할 수 있다. 가장 일반적으로 사용되는 I²C 버스의 모드는 ‘표준 모드’인 100 [kbit/s](https://ko.wikipedia.org/wiki/kbit/s "wikilink")와, ‘저속 모드’인 10 kbit/s 가 사용된다. 최신 리비전의 I²C 는 보다 빠르게 동작하며, ‘패스트(fast) 모드’인 400 kbit/s와 ‘고속(high-speed) 모드’인 3.4 [Mbit/s](https://ko.wikipedia.org/wiki/Mbit/s "wikilink")를 지원한다. 최대 1008 노드까지 연결 가능한 10 비트 [주소 지정](../Page/주소_공간.md "wikilink") 등의 확장된 기능들을 지원한다.

## 리비전

원래 I²C 시스템은 [1980년대](../Page/1980년대.md "wikilink") 초반에 개발되었으며, 여러 필립스 칩들을 이용하여 전자 제품을 구성하기 위한 간단한 내부 버스 시스템으로 사용되었다.

  - [1992년](../Page/1992년.md "wikilink")에 ‘패스트 모드’ 10 비트 주소 지정 기능이 추가된 최초 표준 버전이 발표되었으며,
  - [1998년](../Page/1998년.md "wikilink")에 낮은 전압에서 동작하는 ‘고속 모드’와 전원 관리 요구 사항이 추가된 버전 2.0이 발표되었다.
  - [2001년](../Page/2001년.md "wikilink")에 발표된 버전 2.1은 버전 2.0에서 약간의 수정이 가해진 것으로 현재 최신 버전에 해당한다.

## 응용

I²C 는 빠른 속도를 요구하지 않는 간단한 저비용 주변 장치들에 적합하다. I²C 버스가 사용되는 주된 응용 영역은 다음과 같다.

  - 사용자 설정값을 저장하기 위해 [NVRAM](https://ko.wikipedia.org/wiki/NVRAM "wikilink")에 접근하는 경우
  - 저속의 [디지털-아날로그 변환회로에](../Page/디지털-아날로그_변환회로.md "wikilink") 접근하는 경우
  - 저속의 [아날로그-디지털 변환회로에](../Page/아날로그-디지털_변환회로.md "wikilink") 접근하는 경우
  - [모니터의](https://ko.wikipedia.org/wiki/컴퓨터_디스플레이 "wikilink") 명암, 대비, 색상 등을 변경하는 경우
  - 지능형 [스피커](../Page/스피커.md "wikilink")의 볼륨값을 변경하는 경우
  - [휴대전화](https://ko.wikipedia.org/wiki/휴대전화 "wikilink")같은 장치에 포함된 [발광 다이오드를](../Page/발광_다이오드.md "wikilink") 제어하는 경우
  - [중앙 처리 장치](../Page/중앙_처리_장치.md "wikilink") 온도나 팬 속도와 같은 하드웨어 모니터링 정보나 진단 센서 정보를 읽는 경우
  - [실시간 클럭](https://ko.wikipedia.org/wiki/실시간_클럭 "wikilink") 값을 읽는 경우
  - 시스템 요소의 전원을 제어하는 경우

I²C 의 장점은 특히 [마이크로컨트롤러](../Page/마이크로컨트롤러.md "wikilink")에서 단지 2개의 [일반 목적 입출력](https://ko.wikipedia.org/wiki/일반_목적_입출력 "wikilink") 핀과 [소프트웨어](../Page/소프트웨어.md "wikilink")만을 이용하여 여러 장치들을 제어할 수 있다는 점이다.

주변 장치들은 시스템이 동작 중일때도 I²C 버스에 추가/제거될 수 있으며, 이것은 [핫 스왑이](https://ko.wikipedia.org/wiki/핫_스왑 "wikilink") 필요한 요소들을 이용하는 응용에 적합하다.

I²C 와 같은 버스들은 컴퓨터 엔지니어들이 칩의 패키지 크기와 핀 수가 생산 비용과 IC 설계에 영향을 준다는 것을 인식한 후부터 널리 사용되었다. 또한 작은 패키지는 일반적으로 더 적은 전력을 소모하므로, [휴대전화](https://ko.wikipedia.org/wiki/휴대전화 "wikilink")나 이동형 장치들에서 사용하기에 편리하다.

## 운영 체제 지원

[리눅스](../Page/리눅스.md "wikilink")에서는, I²C 는 특정 장치에 대한 [커널 모듈로](https://ko.wikipedia.org/wiki/모듈_\(리눅스\) "wikilink") 처리된다. I²C 클라이언트를 작성하는 법은 커널 관련 문서와 /usr/include/linux/i2c.h [헤더 파일에서](../Page/헤더_파일.md "wikilink") 찾아볼 수 있다.

[OpenBSD](../Page/OpenBSD.md "wikilink")는 최근 I²C 프레임워크에 대한 지원을 추가하였으며, 몇 가지 일반적인 마스터 컨트롤러들과 센서들을 지원한다.

[Sinclair QDOS와](https://ko.wikipedia.org/wiki/Sinclair_QDOS "wikilink") [Minerva (QDOS reimplementation)](https://ko.wikipedia.org/wiki/Minerva "wikilink"), [QL](https://ko.wikipedia.org/wiki/Sinclair_QL "wikilink") [운영체제](https://ko.wikipedia.org/wiki/운영체제 "wikilink")에서는 [TF 서비스에서](https://ko.wikipedia.org/wiki/TF_서비스 "wikilink") 제공하는 확장 기능을 통해 I²C 를 지원한다.

[AmigaOS](https://ko.wikipedia.org/wiki/AmigaOS "wikilink")는 Wilhelm Noeker의 *i2c.library* 공유 라이브러리를 통해 I²C 를 지원한다.

[eCos](https://ko.wikipedia.org/wiki/eCos "wikilink")는 여러 하드웨어 아키텍처에 대해 I²C 를 지원한다.

[EPIA](https://ko.wikipedia.org/wiki/EPIA "wikilink")-M 마더보드는 [Mini-ITX](https://ko.wikipedia.org/wiki/Mini-ITX "wikilink") 범위에서 I²C 를 지원한다.

## 파생 기술

I²C 는 [액세스.버스](https://ko.wikipedia.org/wiki/액세스.버스 "wikilink"), [VESA](https://ko.wikipedia.org/wiki/VESA "wikilink") [디스플레이 데이터 채널](https://ko.wikipedia.org/wiki/디스플레이_데이터_채널 "wikilink")(DDC) 인터페이스, [시스템 관리 버스](https://ko.wikipedia.org/wiki/시스템_관리_버스 "wikilink")(SMBus), [지능형 플랫폼 관리 인터페이스](https://ko.wikipedia.org/wiki/지능형_플랫폼_관리_인터페이스 "wikilink")(IPMI) 프로토콜 중의 하나인 지능형 플랫폼 관리 버스(IPMB)의 기본 기술이다. 이러한 것들은 전압과 클럭 주파수 범위에서 차이가 있으며, [인터럽트](../Page/인터럽트.md "wikilink") 라인을 가질 수 있다.

## 함께 보기

  - [I²S](../Page/I²S.md "wikilink")
  - [1-Wire](https://ko.wikipedia.org/wiki/1-Wire "wikilink") 버스
  - [직렬 주변기기 인터페이스 버스](../Page/직렬_주변기기_인터페이스_버스.md "wikilink")(SPI 버스)
  - [시스템 관리 버스](https://ko.wikipedia.org/wiki/시스템_관리_버스 "wikilink")
  - [CAN 버스](../Page/CAN_버스.md "wikilink")

## 외부 링크

  - [필립스 I2C 명세](http://www.nxp.com/acrobat_download/literature/9398/39340011.pdf)
  - [자세한 소개, 입문서](http://www.i2c-bus.org/)
  - [I2C 소개](https://web.archive.org/web/20070926222250/http://embedded.com/story/OEG20010718S0073)
  - [I<sup>2</sup>C Bus / Access Bus](http://www.interfacebus.com/Design_Connector_I2C.html)
  - [리눅스에서 I2C 버스 사용하기](http://www.linuxjournal.com/article/1342)
  - [OpenBSD iic(4) 매뉴얼 페이지](http://www.openbsd.org/cgi-bin/man.cgi?query=iic&sektion=4)
  - 리눅스 패키지 [lm-sensors](http://secure.netroedge.com/~lm78/) - I2C 및 다른 버스 지원.
  - [massmind i2c page](http://techref.massmind.org/i2cs.htm) PC, PIC, SX 마이크로 컨트롤러에서 i2c 를 사용하기 위한 소스 코드 및 기술 정보
  - [I<sup>2</sup>C bus](https://web.archive.org/web/20061230193623/http://tmd.havit.cz/Papers/I2C.pdf)
  - [직렬 버스 정보](http://www.epanorama.net/links/serialbus.html)
  - [I2C 버스의 기술적인 개요 및 FAQ](http://www.esacademy.com/faq/i2c/)
  - [I2C FAQ 버전 2.0](https://web.archive.org/web/20070102155852/http://www.kar.elf.stuba.sk/predmety/mmp/i2c/i2cindex.htm)
  - [I2C, SMBus, PMBus, IPMB & IPMI 와 같은 2 라인 버스 정보](https://web.archive.org/web/20161013012648/http://www.bus-buffer.com/)

[분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")