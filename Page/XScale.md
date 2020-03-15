> This article is converted from Wikipedia: [XScale](https://ko.wikipedia.org/wiki/XScale).


[인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink")의 **XScale**(엑스스케일) [프로세서는](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink")v5 아키텍처를 기반으로 설계된 [인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink")의 모바일 프로세서 아키텍처로 핸드헬드 PC나 PDA에 폭넓게 사용되고 있는 모바일 프로세서 아키텍처이다. StrongARM CPU는 [DEC](https://ko.wikipedia.org/wiki/DEC "wikilink")사에서 개발되었고 인텔이 인수하면서 인텔의 상표를 달고 출고되었다. XScale은 이 StrongARM 프로세서의 후속작이다.

2006년 인텔이 XScale 관련 라이선스를 [마벨사에](https://ko.wikipedia.org/wiki/마벨_테크놀로지_그룹 "wikilink") 매각함에 따라 현재 XScale 기반 프로세서는 [마벨](https://ko.wikipedia.org/wiki/마벨 "wikilink")(Marvell)사에서 제조되고 있다.

## XScale 기반 프로세서 나열

### PXA21x/25x 계열

[섬네일](https://ko.wikipedia.org/wiki/파일:Typhoon_MyGuide_3500_mobile_-_controller_-_Intel_PXA255A0C300-1180.jpg "wikilink") 2002년 2월 출시 제품이고, PXA21x는 저전압, 중전압 두 가지 동작 전압 모드를 지원하며 25x의 경우 고전압 모드를 추가로 지원한다.

#### 저전압 모드(0.85V)

  - 일반모드 100MHz, 터보모드 132MHz
  - 50 \~ 99.5MHz PXBus Clock Speed
  - 50 \~ 99.5MHz [SDRAM](https://ko.wikipedia.org/wiki/SDRAM "wikilink") Controller Clock Speed (99.5MHz)
  - 0.765 \~ 0.935V 동작

#### 중전압 모드(1.00V)

  - 일반모드 100MHz, 터보모드 200MHz
  - 50 \~ 99.5MHz PXBus Clock Speed
  - 50 \~ 99.5MHz SDRAM Controller Clock Speed (99.5MHz)
  - 0.90 \~ 1.10V 동작

#### 고전압 모드(1.10V)

  - 일반모드 200MHz, 터보모드 300MHz
  - 50 \~ 99.5MHz PXBus Clock Speed
  - 50 \~ 99.5MHz SDRAM Memory Clock Speed (99.5MHz)
  - 0.99 \~ 1.21V 동작
  - 특이사항 : PXA25x 에서만 지원하며 **PXA255는 터보모드 동작 속도가 400MHz**.

#### 공통/특이 사항

  - 32KB [I-Cache](https://ko.wikipedia.org/wiki/I-Cache "wikilink"), 32KB [D-Cache](https://ko.wikipedia.org/wiki/D-Cache "wikilink"), 2KB Mini D-Cache
  - [AC97](https://ko.wikipedia.org/wiki/AC97 "wikilink")/[I2S](https://ko.wikipedia.org/wiki/I2S "wikilink") 오디오 지원
  - [USB](https://ko.wikipedia.org/wiki/USB "wikilink")-Client 지원
  - 고속 [UART](../Page/UART.md "wikilink") 포트
  - 흐름제어 가능 2번 UART 포트
  - FIR, SIR 적외선 포트

### PXA26x 시리즈

2003년 3월 출시했고, 재원은 PXA255과 같다,

#### 공통/특이 사항

  - Intel(R) [StrataFlash](https://ko.wikipedia.org/wiki/StrataFlash "wikilink") 기술 지원

### PXA27x 시리즈

2004년 4월 출시했고, 개발 코드명 Bulverde. 이 시점부터 PXA 프로세서의 멀티미디어 관련 성능이 대폭 향상됐으며 향상된 전력 관리 기술을 지원하기 시작한다.

#### 지원 동작 속도

  - 절전모드 208MHz, 일반모드 520MHz (일반적으로 사용되는 모드)
  - 최저 104MHz \~ 최고 624MHz까지 동작 가능
  - 104MHz PXBus Clock Speed
  - 104MHz SDRAM Memory Clock Speed
  - 2.25 \~ 3.75V 동작

#### 공통/특이 사항

  - 32KB I-Cache, 32KB D-Cache, 2KB Mini D-Cache
  - Intel(R) Wireless [MMX](../Page/MMX.md "wikilink") Technology
  - Wireless Intel [SpeedStep](https://ko.wikipedia.org/wiki/SpeedStep "wikilink") Technology (소소한 결함이 있는 관계로 잘 사용되지 않음)
  - AC97/I2S 오디오 지원
  - USB-Client/Host 지원
  - USB On-the-go(OTG) 지원
  - 고속 3채널 UART 포트(두 개 포트는 하드웨어 흐름 제어 지원)
  - FIR, SIR 적외선 포트
  - [메모리 스틱](../Page/메모리_스틱.md "wikilink") 카드 인터페이스 지원

### PXA3xx 시리즈

2005년 8월에 출시되었다. 개발 코드명은 Monahans이다. PXA270의 성공을 바탕으로 제작된 프로세서로 XScale 기반 프로세서중 처음으로 1GHz 이상의 설계 클럭을 가진다.

이 제품은 인텔이 XScale 코어 라이선스를 Marvell사에 매각함에 따라 마벨이 생산하기 시작한다.

#### 지원 동작 속도

  - 걸리는 부하에 따라 208 \~ 624MHz 사이의 가변 클럭 (일반적으로 사용되는 모드)
  - 최저 104MHz \~ 최고 806MHz까지 동작 가능
  - 설계 가능한 최고 클럭은 1.25GHz
  - 208MHz Bus Clock Speed

#### 공통/특이 사항

  - 32KB I-Cache, 32KB D-Cache, 2KB Mini D-Cache
  - 256KB 캐시용 SRAM 내장
  - x16 DDR SDRAM 지원
  - Intel(R) Wireless [MMX](../Page/MMX.md "wikilink")2 [Co-Processor](https://ko.wikipedia.org/wiki/Co-Processor "wikilink")
  - Wireless Intel [SpeedStep](https://ko.wikipedia.org/wiki/SpeedStep "wikilink") Technology
  - 하드웨어 수준의 멀티미디어 영상(JPEG)/비디오 가속 지원
  - Intel(R) [QuickCapture](https://ko.wikipedia.org/wiki/QuickCapture "wikilink") 카메라 가속 인터페이스 지원
  - USB 2.0 Client 지원
  - 2채널 USB Full-Speed(12MBps) Host 지원
  - 4채널 SSP 인터페이스 지원
  - [OpenGL ES](../Page/OpenGL_ES.md "wikilink") 1.1 3D 가속 지원
  - Monahans 프로세서의 최고 실현가능 클럭은 1.25GHz이나 806MHz 이상부터는 전력 소비 효율이 급격히 저하되므로 잘 사용되지 않는다. (624MHz@800[MIPS](https://ko.wikipedia.org/wiki/MIPS "wikilink"), 1.25GHz@1000MIPS)

## 외부 링크

  - [인텔 홈페이지](http://www.intel.com/)

[분류:인텔의 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:인텔의_마이크로프로세서 "wikilink") [분류:ARM 아키텍처](https://ko.wikipedia.org/wiki/분류:ARM_아키텍처 "wikilink") [분류:블랙베리](https://ko.wikipedia.org/wiki/분류:블랙베리 "wikilink")