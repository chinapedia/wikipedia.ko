> This article is converted from Wikipedia: [STM32](https://ko.wikipedia.org/wiki/STM32).


**STM32**는 [ST마이크로일렉트로닉스](../Page/ST마이크로일렉트로닉스.md "wikilink")(STMicroelectronics 또는 ST)의 32 비트 [마이크로컨트롤러 유닛(MCU)](../Page/마이크로컨트롤러.md "wikilink") 제품군이다. STM32 칩은 Cortex-M7F, Cortex-M4F, Cortex-M3, Cortex-M0 + 또는 Cortex-M0와 같은 32 비트 [ARM 프로세서 코어를](../Page/ARM_아키텍처.md "wikilink") 기반으로하는 관련 시리즈로 분류된다. 내부적으로 각 마이크로 컨트롤러는 프로세서 코어, 정적 RAM, 플래시 메모리, 디버깅 인터페이스 및 다양한 주변 장치로 구성되어있다.\[1\]\[2\]\[3\]

## Cortex-M4

[코텍스 M4는](https://ko.wikipedia.org/wiki/코텍스_M4 "wikilink") Cortex-M 시리즈중 하나로 현존하는 칩보드는 STM32의 뉴클레오(NUCLEO)F303K8 초소형보드에 채용되어있는것이 대표적이다.\[4\]\[5\]

| 모델명(칩)                                                  | 성능                                                                             | 비고  |
| ------------------------------------------------------- | ------------------------------------------------------------------------------ | --- |
| [아두이노](../Page/아두이노.md "wikilink") 프로 마이크로(ATmega32U4칩) | 8비트연산, 8x2 MHz / 8 MHz (5 V / 3.3 V)의 동작클럭과 플래시 메모리32KB, EEPROM 1KB,SDRAM2.5KB | 26핀 |
| 뉴클레오F303K8 (Cortex-M4칩)                                 | 8x4비트연산, 8x9 MHz (3.3V,5V,7\~12V)의 동작클럭과 플래시 메모리32x2KB, SRAM16KB,RTC           | 32핀 |

특히 STM32의 뉴클레오(NUCLEO)F303K8은 [아두이노 보드중](../Page/아두이노_보드.md "wikilink") 나노(Nano)와 호환될수있게 설계되었다.\[6\]\[7\]

|                                                                            |
| -------------------------------------------------------------------------- |
| [400px](https://ko.wikipedia.org/wiki/파일:STM32nucleoF303KB.svg "wikilink") |

STM32 Nucleo F303KB 모델은 총32개 핀 중 14개의 I/O핀 ,8개의 아날로그 핀, 전원 출력 및 GND ,6개의 PWM 핀 ,1개의 서보 전원 입력 ,5개의 I2C 확장 핀 ,AREF 출력 ,3.3V 출력을 지원한다.

## Cortex-M3

Cortex-M3코어칩을 장착한 개발용 미니 보드로는 저렴한 STM32F103C8T6 초소형 보드가 있다.\[8\]\[9\]\[10\]

## IDE

STM32칩을 장착한 보드를 개발하기 위한 통합개발환경(IDE)은 Mbed.org의 온라인 IDE뿐만아니라 [아두이노 IDE에서](../Page/아두이노_IDE.md "wikilink") 확장보드 인스톨로 개발을 지원하고있다.\[11\]\[12\]\[13\]

그러나 [NuttX](../Page/NuttX.md "wikilink")같은 임베디드 운영체제의 커널 및 C나 C++을 [펌웨어](../Page/펌웨어.md "wikilink")로 올리기 위해서는 [이클립스나](../Page/이클립스_\(소프트웨어\).md "wikilink") 다른 빌드 방법을 사용할수있으며 ARM은 크로스 컴파일 도구를 공식 지원한다.\[14\]\[15\]

## 같이 보기

  - [아트멜 AVR](../Page/아트멜_AVR.md "wikilink")
  - [I2C](https://ko.wikipedia.org/wiki/I2C "wikilink")
  - [SPI](https://ko.wikipedia.org/wiki/SPI "wikilink")

## 참고

  - [st.com datasheet-stm32f303k8](https://www.st.com/resource/en/datasheet/stm32f303k8.pdf)
  - [st.com datasheet-stm32f103c8](https://www.st.com/resource/en/datasheet/stm32f103c8.pdf)

[분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink") [분류:중앙 처리 장치](https://ko.wikipedia.org/wiki/분류:중앙_처리_장치 "wikilink")

1.  [STM32 Website; STMicroelectronics.](http://www.st.com/web/en/catalog/mmc/FM141/SC1169)
2.  [Cortex-M7 Specification Summary; ARM Holdings.](http://arm.com/products/processors/cortex-m/cortex-m7-processor.php?tab=Specifications)
3.  [Cortex-M0 Specification Summary; ARM Holdings.](http://arm.com/products/processors/cortex-m/cortex-m0.php?tab=Specifications)
4.  [UM1956: STM32 Nucleo-32 boards (MB1180)User manual](https://www.st.com/content/ccc/resource/technical/document/user_manual/e3/0e/88/05/e8/74/43/a0/DM00231744.pdf/files/DM00231744.pdf/jcr:content/translations/en.DM00231744.pdf)
5.  [STM32F103x8 STM32F103xB Datasheet](https://www.st.com/resource/en/datasheet/stm32f103c8.pdf)
6.  [STM32 NUCLEO-F303K8 , Arduino-Nano-compatible headers](https://os.mbed.com/platforms/ST-Nucleo-F303K8/)
7.  [STM32 Nucleo-32 development board with STM32F303K8 MCU, supports Arduino connectivity](https://www.st.com/content/st_com/en/products/evaluation-tools/product-evaluation-tools/mcu-eval-tools/stm32-mcu-eval-tools/stm32-mcu-nucleo/nucleo-f303k8.html#samplebuy-scroll)
8.  [STM32F103C8T6 wikipage](https://os.mbed.com/users/hudakz/code/STM32F103C8T6_Hello/)
9.  [STM32F103C8T6 dev. board](https://os.mbed.com/forum/electronics/topic/26451/?page=1#comment-60986)
10. (aliexpress.com) STM32F103C8T6-ARM-STM32-Minimum-System-Development-Board-Module-For-Arduino
11. [Mbed.org](https://ide.mbed.com/compiler/)
12. [Arduino for STM32 Everything relating to using STM32 boards with the Arduino IDE](http://www.stm32duino.com/)
13. [Preferences-settings-AdditionalBoardsManager URLs](https://raw.githubusercontent.com/stm32duino/BoardManagerFiles/master/STM32/package_stm_index.json) (Tools-Board-Manager ,install-STM32 cores by STMicroelectronics)
14. (이클립스) c/c++릴리즈 IDE
15. ([ARM](https://ko.wikipedia.org/wiki/ARM "wikilink"))gcc arm eabi cross compiler