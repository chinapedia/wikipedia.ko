> This article is converted from Wikipedia: [아트멜 AVR](https://ko.wikipedia.org/wiki/아트멜_AVR).


[섬네일](https://ko.wikipedia.org/wiki/파일:ATmega8_01_Pengo.jpg "wikilink").\]\] **아트멜 AVR**(Atmel AVR)은 [1996년](../Page/1996년.md "wikilink") [아트멜](../Page/아트멜.md "wikilink") 사에서 개발된 [하버드 구조로](https://ko.wikipedia.org/wiki/하버드_구조 "wikilink") 수정한 8비트 [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") 단일칩 [마이크로컨트롤러](../Page/마이크로컨트롤러.md "wikilink")이다. 출시 당시 AVR은 [프로그램](https://ko.wikipedia.org/wiki/프로그램 "wikilink")을 저장하기 위해 이용한 [메모리](https://ko.wikipedia.org/wiki/메모리 "wikilink") 방식을 다른 [마이크로컨트롤러](../Page/마이크로컨트롤러.md "wikilink") 처럼 [ROM](https://ko.wikipedia.org/wiki/ROM "wikilink"), [EPROM](../Page/EPROM.md "wikilink") 또는 [EEPROM](../Page/EEPROM.md "wikilink") 을 사용하지 않고, 단일칩 [플래시메모리](https://ko.wikipedia.org/wiki/플래시메모리 "wikilink")를 사용한 최초의 [마이크로컨트롤러](../Page/마이크로컨트롤러.md "wikilink") 중 하나이다.

## AVR의 구성

AVR은 [중앙처리장치](https://ko.wikipedia.org/wiki/중앙처리장치 "wikilink")와 소용량 [플래시메모리](https://ko.wikipedia.org/wiki/플래시메모리 "wikilink")가 하나의 IC에 집적되어 있다.

AVR 하버드구조(Harvard architecture)의 변형 형태로 프로그램과 데이터 메모리가 분리된 형태이다. 특수 명령어로 프로그램 데이터를 데이터 영역으로 읽을 수 있다.

## AVR의 종류

아트멜 AVR은 AVR이 있으며 그 중, [ATmega128](https://ko.wikipedia.org/wiki/ATmega128 "wikilink")이 교육용으로 가장 흔하게 쓰인다.

### 기본적인 AVR 계열

AVR은 6개의 기본 모둠으로 되어있다:

  - **tinyAVR** - ATtiny 시리즈
      - 0.5–8 kB 프로그램 메모리
      - 6–32핀 패키지
      - 제한된 주변 장치(peripheral) 세트

<!-- end list -->

  - **megaAVR** - ATmega 시리즈
      - 8–256 kB 프로그램 메모리
      - 28–100핀 패키지
      - 확장된 [명령어 집합](../Page/명령어_집합.md "wikilink") (곱셈 명령어, 큰 프로그램 메모리를 처리를 위한 명령어)
      - 확장된 주변 장치(peripheral) 세트

<!-- end list -->

  - **XMEGA** - ATxmega 시리즈
      - 16–384 kB 프로그램 메모리
      - 44–64–100핀 패키지 (A4, A3, A1)
      - 확장된 성능 (DMA, "Event System", 암호와 지원)
      - 확장된 주변 장치(peripheral) 세트 (ADC)

<!-- end list -->

  - **Application-specific AVR**
      - megaAVR을 기반으로 다른 AVR 계열에서 찾을 수 없는 LCD 제어, USB 제어, 진화된 PWM, CAN, 등의 모듈 추가.

<!-- end list -->

  - **FPSLIC (AVR에 FPGA 추가)**
      - [FPGA](../Page/FPGA.md "wikilink") 5K \~ 40K 게이트
      - 다른 AVR과는 달리, AVR 프로그램 코드를 SRAM에
      - AVR 코어는 50 MHz 이상에서도 실행\[1\]

<!-- end list -->

  - **32-bit AVRs**

<!-- end list -->

  -
    2006년에 Atmel은 32비트를 기반으로 [AVR32](https://ko.wikipedia.org/wiki/AVR32 "wikilink") 구조를 만들었다. SIMD과 [DSP](https://ko.wikipedia.org/wiki/DSP "wikilink") 명령어를 추가하여 오디오와 비디오 처리를 할 수 있다. 32비트 계열은 [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink")과 경쟁관계에 있다. 명령어 집합은 다른 RISC와 비슷하지만 원래 AVR이나 다양한 ARM 코어와 호환되지 않는다.

## 프로그래밍 인터페이스

AVR 칩에 프로그램 코드는 여러가지 방법으로 전송할 수 있다.

### ISP

[섬네일](https://ko.wikipedia.org/wiki/파일:Isp_headers.svg "wikilink") ISP(in-system programming) 프로그램 전송 방식은 기능적으로 [SPI](https://ko.wikipedia.org/wiki/SPI "wikilink") 방법에 *Reset* 선을 추가한 것이다. [PCB](https://ko.wikipedia.org/wiki/PCB "wikilink")에 납땜 상태에서 프로그램 코드를 전송할 수 있다. AVR에서 가장 일반적인 방법이다.

*Atmel AVR ISP mkII* 장치는 USB에 연결하고 Atmel의 ISP 프로그램에 의해 동작한다.

AVRDUDE (AVR Downloader/UploaDEr)는 [Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink"), 윈도, [OS X에서](https://ko.wikipedia.org/wiki/OS_X "wikilink") 실행되며 다양한 하드웨어(Atmel AVR ISP mkII, Atmel JTAG ICE)로 프로그래밍을 할 수 있다.\[2\] AVR의 대표적 개발환경인 Atmel Studio는 현재 7.0 버전까지 나와있으며, Microsoft의 Visual Studio를 바탕으로 만들어져 UI가 매우 유사하다.

AVRISP MKII와 같은 툴 없이 아두이노를 ISP 툴로 만들어 사용할 수 있다.

## 각주

<references/>

## 같이 보기

  - [전자 부품](../Page/전자_부품.md "wikilink")

## 외부 링크

  - [AVR Solutions](http://www.atmel.com/products/avr/default.asp?family_id=607)

[분류:마이크로컨트롤러](https://ko.wikipedia.org/wiki/분류:마이크로컨트롤러 "wikilink") [분류:명령어 집합 구조](https://ko.wikipedia.org/wiki/분류:명령어_집합_구조 "wikilink")

1.
2.