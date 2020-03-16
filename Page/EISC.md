> This article is converted from Wikipedia: [EISC](https://ko.wikipedia.org/wiki/EISC).


**EISC**()는 에이디칩스\[1\] 에서 개발한 임베디드 프로세서용 RISC 기반 [명령어 집합이다](../Page/명령어_집합.md "wikilink"). [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink")에 기반했지만 [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink")의 간결성과 [CISC](https://ko.wikipedia.org/wiki/CISC "wikilink")의 확장성을 동시에 지녔다.

## EISC 코어 개요

EISC는 에이디칩스에서 개발한 임베디드 프로세서용 Instruction Set Architecture로서 확장 레지스터(Extension Register)와 확장 플래그(Extension Flag)라는 새로운 개념을 도입하여, operand길이를 필요한 만큼 임의로 확장이 가능하고, 길이가 16bit로 고정된 명령어(16bit fixed length instruction)구조를 갖는다.

RISC 기반의 명령어 집합에 확장이라는 부분이 추가되어, RISC의 간결성과 CISC의 확장성을 동시에 지니고 있고, EISC(Extendable Instruction Set Computer)라는 이름을 갖게 되었다.

[AE32000_ISA_Reference.pdf](http://www.adc.co.kr/technology/eisc/eisc.php)

### Extension(확장 레지스터(ER), 확장 플래그(E))

  -
    EISC는 가변길이 operand를 표현하기 위해 확장 레지스터(ER)와 확장 플래그(E)를 사용한다.
      -
        확장 레지스터(ER) : 확장 operand가 저장되는 레지스터
        확장 플래그 : 확장 레지스터에 operand가 저장 되어 있는지를 나타내는 플래그

<!-- end list -->

  -
    확장 레지스터에 확장 operand를 load하는 명령어로 LERI를 사용하는데, LERI명령과 immediate값을 load하는 LDI명령이 같이 사용될 때 어떻게 동작하는지 아래 그림에서 나타낸다.

<!-- end list -->

  -

      -
        **16bit EISC Processor**

[섬네일](https://ko.wikipedia.org/wiki/파일:16bit_EISC_Processor.GIF "wikilink")

{{-}}

  -

      -
        **32bit EISC Processor**

[섬네일](https://ko.wikipedia.org/wiki/파일:32bit.GIF "wikilink") {{-}}

  -

      -
        위의 그림은 16bit EISC Processor와 32BIt EISC Processor 에서 LERI와 LDI의 동작을 표한한 그림으로, 그림에서 확인할 수 있듯이 16bit EISC processor에서는 12bit 단위로 확장 레지스터(ER)를 확장하고, 32bit EISC processor에서는 14bit 단위로 확장 레지스터(ER)를 확장하는 것을 알 수 있다

## EISC core Features

EISC의 특징은 크게 다음 그림과 같이 5개로 표현 할 수 있다.

[섬네일](https://ko.wikipedia.org/wiki/파일:EISC_5_step.GIF "wikilink")

**Small**(Small lcode size, High cocde density) EISC는 출현 빈도가 높은 short length operadn를 가지는 16bit fixed length instruction으로 구성되어 있으며, 필요한 operand length만큼 LERI instruction을 사용하여 operand를 확장하는 방식을 사용하므로 program size가 작아진다. 즉, code density가 높은 장점을 가지고 있다.

**Simple**(Simple instruction set, Simple hardware) ESIC는 16bit fixed length instruction set을 가지며, 한가지 Op-Code에 한 개의 instruction만을 가지고 있어서 instruction의 수가 적다. 즉, operand length에 따른 여러 개의 instruction을 만들 필요가 없으므로 instruction수가 기존 microprocessor보다 적고 간단하여 hardware도 간단해 진다.

**Speed**(High speed) EISC는 simple instruction set을 가짐으로써 hardware가 단단해지고, operation frequency가 높아지므로 performance 또한 높아진다.

**Scalable**(Scalable 16/32bit microprocessor architecture) EISC는 16/32bit microprocessor의 특징을 반영하여 operand를 필요한 길이만큼 확장하는 구조로 16/32bit microprocessor 모두에서 효울적이다. 또한 EISC architecture는 16/32bit microprocessor에 따른 instruction set의 변화가 크지 않아, 하나의 micropricessor만 개발하면 다른 word length micropricessor도 손쉽게 개발할 수 있는 장점을 지니고 있다.

**Saving**(Power saving-low power) 전력소모를 낮추기 위해서는 첫째로 전력을 소모하는 logic gate count를 줄여야 하는데 이를 위해서는 hardware가 단단한 구조가 되어야 한다. 둘째로는 logic gate 입출력의 상태가 자주 변하지 않아야 하는데, 이를 위해서는 data bus traffic을 낮추어야 한다. 따라서 program size가 작은 architecture즉 high code density architecture가 요구된다. EISC는 기존 microprocessor에 비하여 hardware가 단단하고, code density가 높아야 위의 두 조건을 만족하므로 전력 소모가 적은 architecture이다.

## EISC core Architecture

  -

      -
        **SE1608**
          -
            Gate count가 작고 속도가 빠르면서 C-언어와 같은 high level language에 적합한 16bit EISC microprocessor인 SE1608을 개발하였다.
            SE1608은 7개의 general purpose register, 6개의 special purpose register를 가지고 있으며 16bit fixed length instruction set을 사용한다. 또한 16bit barrel shift와 16bitx16bit 1cycle multiplier를 갖추고 있다. SE1608은 약 7K gate이며, 0.18um 공정에서 50Mhz 속도로 동작한다.
            [SE1608 Processor 바로가기](http://www.adc.co.kr/technology/eisc/archltecture.php)

<!-- end list -->

  -

      -
        **SE3208**
          -
            Embedded microprocessor 시장에서 30MIPS 이하의 성능을 가진 microprocessor의 점유율이 높은 것으로 조사되고 있어, 이 시장에서 적합한 low end 32bit microprocessor인 SE3208을 개발하였다.
            SE3208은 8개의 general purpose register, 6개의 special purpose register를 가지고 있으며, 16bit fixed length instruction set을 사용한다. 또한 32bit barrel shift와 32bitx32bit의 1-cycle multiplier를 갖추고 있다. SE3208은 약 15K gate이며, 0.18um 공정에서 50MHz 속도로 동작한다.
            [SE3208 Processor 바로가기](http://www.adc.co.kr/technology/eisc/archltecture.php)

<!-- end list -->

  -

      -
        **AE32000**
          -
            AE32000은 high code density, high performance 32bit embedded microprocessor로 16개의 general purpose register, 7개의 special purpose register를 가지고 있으며, 16bit fixed length instruction set을 사용한다. 또한 32x32 = 64 signed/unsigned multiplier와 32x32 = 64 multiply and accumulate(MAC) 및 32bit barrel shift를 갖추고 있으며, DSP instruction과 DSP X/Y memory를 option으로 갖추고 있다.
            AE32000은 기존 RISC/CISC microprocessor와 비교하여 code density가 높고, hardware가 단단하며, preformance가 높으면서, 전력 소모가 적다.
            [AE32000 Processor 바로가기](http://www.adc.co.kr/technology/eisc/archltecture.php)

## EISC core Software Tool

  -

      -
        EISSC Studio
        EISC processor를 위한 통합 개발환경(Integrated Development Environmnet)
        EISC Studio는 EISC Processor를 이용한 application program을 개발할 때 Program Source 편집, Compile, Debug 환경을 제공하여 개발에 편의성을 제공한다. 또한 high-level programming language의 다양한 이미지, 그리고 source level에서 실행 코드를 디버그 할 수 있는 환경을 제공해 준다.

:::**Integrated Development Environment**

::\* Works in Windows 2000 / XP / VISTA / 7

::\* Friendly User Interface like Microsoft Visual-Studio

::\* Source Edit / Compile

::\* Automatic Windows Docking

::\* Project file Tree view

::\* Class / Function / Global variable Tree view

::\* Auto Generate Make file

::\* Graphicla Symbol Brower

::\* Support All EISC compilers

:::**Convenient Embedded Editor**

::\* Syntax highlighting

::\* Column Editor

::\* Code Completion

::\* Smart Auto-indent

::\* Find and replace facilities

::\* Bookmark

::\* Move Up / Down Current Line

::\* Support for collapsible nodes (outlining)

::\* Support various fonts and styles

## 프로세서 종류

EISC 프로세서의 종류는 [ISA](https://ko.wikipedia.org/wiki/ISA "wikilink")의 구성에 따라 SE (Simple EISC)군과 AE (Advanced EISC)군으로 나뉜다.

| 프로세서 군           | 코어                 | 프로세서               | Clock Freq.    | Average IPC    | Peak MIPS        | Gate Counts      | Power Consumption(@0.18μm) | Pipelines | SIMD-DSP |
| ---------------- | ------------------ | ------------------ | -------------- | -------------- | ---------------- | ---------------- | -------------------------- | --------- | -------- |
| SE               | SE1608             | 16bit CPU          | 70MHz@0.18μm   |                |                  |                  |                            |           |          |
|                  |                    |                    |                |                |                  |                  |                            |           |          |
| 8K               |                    |                    |                |                |                  |                  |                            |           |          |
| 3stages          |                    |                    |                |                |                  |                  |                            |           |          |
|                  |                    |                    |                |                |                  |                  |                            |           |          |
| SE3208           | 32bit CPU          | 70MHz@0.18μm       |                |                |                  |                  |                            |           |          |
|                  |                    |                    |                |                |                  |                  |                            |           |          |
| 13K              |                    |                    |                |                |                  |                  |                            |           |          |
| 3stages          |                    |                    |                |                |                  |                  |                            |           |          |
|                  |                    |                    |                |                |                  |                  |                            |           |          |
| AE               | AE32000C-Tiny      | upto 100MHz@0.18μm | over 0.8       | 110MIPS@100MHz | 26\~30K          | under 0.15mW/MHz | 3stages                    |           |          |
|                  |                    |                    |                |                |                  |                  |                            |           |          |
| AE32000C-Lucida  | upto 150MHz@0.18μm | over 0.87          | 145MIPS@130MHz | 50\~88K        | under 0.30mW/MHz | 5stages          | SIMD-DSP                   |           |          |
| AE32000C-Empress | upto 300MHz@0.13μm | over 0.78          |                |                |                  |                  |                            |           |          |
| 120K             | under 0.38mW/MHz   | 9stages            | SIMD-DSP       |                |                  |                  |                            |           |          |

## 개발 환경

[마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink") 운영 체제에 한해 EISC-Studio라는 [오픈 소스](../Page/오픈_소스.md "wikilink") 기반 [통합 개발 환경을](../Page/통합_개발_환경.md "wikilink") 지원한다. [리눅스](../Page/리눅스.md "wikilink")나 [유닉스](../Page/유닉스.md "wikilink")는 [KDE](../Page/KDE.md "wikilink")나 [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")를 이용할 수 있다.

## 관련 문헌

  - [A DSP-enhanced 32-bit embedded microprocessor](http://www.springerlink.com/content/u205vlq218515275/?p=c7f819d59b3c42d6b24080f59e59fdc0&pi=1)
  - ["An automated, reconfigurable, low-power RFID tag"](http://portal.acm.org/citation.cfm?id=1146948&coll=GUIDE&dl=ACM&CFID=2777145&CFTOKEN=88500148) compares the EISC architecture with other architectures
  - [Supports for Processing Media Data in Embedded Processors](http://www.hipc.org/hipc2004/posters/park.doc)

## 각주

[분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink")

1.  [에이디칩스](http://www.adc.co.kr/index.php)