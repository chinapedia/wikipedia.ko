> This article is converted from Wikipedia: [OMAP](https://ko.wikipedia.org/wiki/OMAP).


[300px](https://ko.wikipedia.org/wiki/파일:PandaBoard_described.png "wikilink")

**OMAP** (Open Multimedia Applications Platform)은 [TI에서](../Page/텍사스_인스트루먼트.md "wikilink") 개발한 SoC이며, 주요 적용 대상은 휴대용 멀티미디어 장치이다. OMAP CPU는 [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink") 아키텍처 기반 CPU 및 하나 이상의 보조 프로세서를 내장하고 있다. 초기 OMAP CPU는 TI TMS320 계열 디지털 시그널 프로세서(DSP)를 장착하였다.

2012년 9월 26일 TI는 스마트폰과 태블릿을 대상으로 하는 OMAP 칩셋의 사업을 축소하고 임베디드 플랫폼에 초점을 맞추기로 발표하였다.\[1\] 2012년 11월 14일 프로세서 사업 변경으로 인하여 1700명을 감원하였다.\[2\]

## 개요

OMAP 계열 제품은 성능과 주 사용 용도로 구분된 세 가지 계열로 분류된다.

  - 고성능 애플리케이션 프로세서
  - 기본 멀티미디어 애플리케이션 프로세서
  - 모뎀 및 애플리케이션 통합 프로세서

두 가지의 유통 채널을 통해서 판매되며, 유통 채널별로 판매되는 칩셋의 종류에 차이가 있다. OMAP 제품군의 휴대 전화 제조사와의 협력에서 시작되었으며 주 유통 채널은 휴대 전화 제조사에 직접 판매하는 것이다. 휴대 전화 이외의 다른 기능을 지원할 수 있는 고성능의 유연한 마이크로프로세서는 카탈로그 채널로 판매되며, OMAP 1 제품군의 일부 및 다수의 OMAP 3 제품군이 별개의 판매 및 지원 모델을 사용하는 카탈로그 채널을 통해 발매되었다. OMAP35x 및 OMAP-L13x 제품군이 카탈로그 채널로 판매되기 시작하면서 고성능 및 고전력효율 마이크로프로세서로 마케팅되었다.

## 애플리케이션 프로세서

스마트폰과 같은 장치의 애플리케이션 프로세서로 사용되며, 이들 프로세서는 [리눅스](../Page/리눅스.md "wikilink"), [안드로이드](../Page/안드로이드_\(운영_체제\).md "wikilink"), [심비안](https://ko.wikipedia.org/wiki/심비안 "wikilink")과 같은 모바일 운영 체제를 실행시키고 다양한 멀티미디어를 구현할 수 있다.

### OMAP 1

OMAP 1 계열 프로세서는 TI에서 추가적으로 기능을 개선한 ARM 코어를 기반으로 하였으나, 이후 표준 ARM926 코어로 변경하였다. 각각의 프로세서는 제조 공정(OMAP171x 계열을 제외하면 130nm), CPU, 명령어 집합, 유통 채널로 구분된다. OMAP 1 프로세서를 사용한 제품으로는 여러 휴대폰 및 [노키아 770이](https://ko.wikipedia.org/wiki/노키아_770 "wikilink") 있다.

  - OMAP171x - 220MHz ARM926EJ-S + [C55x](https://ko.wikipedia.org/wiki/TI_TMS320 "wikilink") DSP, 저전압 90nm 공정
  - OMAP162x - 204MHz ARM926EJ-S + C55x DSP + 2MB 내장 SRAM, 130nm 공정
  - OMAP5912 - OMAP1621의 카탈로그 유통 파생형 (구 버전의 경우 OMAP1611b)
  - OMAP161x - 204MHz ARM926EJ-S + C55x DSP, 130nm 공정
  - OMAP1510 - 168MHz ARM925T (TI 개선형) + C55x DSP
  - OMAP5910 - OMAP1510의 카탈로그 유통 파생형

### OMAP 2

OMAP 2 프로세서는 휴대 전화 제조사에게만 판매되었다.

  - OMAP2431 - 330MHz ARM1136 + 220MHz C64x DSP
  - OMAP2430 - 330MHz ARM1136 + 220MHz C64x DSP + [PowerVR](https://ko.wikipedia.org/wiki/PowerVR "wikilink") MBX 라이트 GPU
  - OMAP2420 - 330MHz ARM1136 + 220MHz C55x DSP + PowerVR MBX GPU

### OMAP 3

3세대 OMAP, OMAP 3 프로세서\[3\]는 OMAP34x, OMAP35x, 그리고 OMAP36x의 3가지 계열로 나뉜다. OMAP34x 및 OMAP36x 계열은 휴대 전화 제조회사의 프로세서용으로 납품되었다. OMAP35x 계열은 OMAP34x 계열의 파생형으로 카탈로그 채널을 통하여 유통되었다. OMAP36x 계열은 OMAP34x 계열의 65nm 공정을 45nm 공정으로 개선하고 클럭 속도를 향상시킨 제품군이다.\[4\]

비디오 재생 기술은 OMAP의 전 세대 제품들처럼 TI 다빈치에서 유래하였으며, TI C64x+ DSP 및 이미지 프로세서를 기반으로 한다.\[5\] 멀티미디어 프로세싱을 담당하는 IVA2(이미지, 오디오, 비디오) 가속기가 포함되어 있어서(프로세서별 처리 능력은 다름) 최대 1200만 화소, 일부 3\~500만 화소까지의 카메라를 제어할 수 있으며, 일부 제품은 HD 촬영을 지원한다.

| 모델명                | 제조 공정 | CPU 아키텍처 | CPU                                                                            | GPU                                                                |
| ------------------ | ----- | -------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------ |
| OMAP3410           | 65nm  | ARMv7    | 600MHz [ARM Cortex-A8](https://ko.wikipedia.org/wiki/ARM_Cortex-A8 "wikilink") | [PowerVR](https://ko.wikipedia.org/wiki/PowerVR "wikilink") SGX530 |
| OMAP3420           | 65nm  | ARMv7    | 600MHz ARM Cortex-A8                                                           | PowerVR SGX530                                                     |
| OMAP3430           | 65nm  | ARMv7    | 600MHz ARM Cortex-A8                                                           | PowerVR SGX530                                                     |
| OMAP3440           | 65nm  | ARMv7    | 800MHz ARM Cortex-A8                                                           | PowerVR SGX530                                                     |
| OMAP3503           | 65nm  | ARMv7    | 600MHz ARM Cortex-A8                                                           | 없음                                                                 |
| OMAP3515           | 65nm  | ARMv7    | 600MHz ARM Cortex-A8                                                           | PowerVR SGX530                                                     |
| OMAP3525           | 65nm  | ARMv7    | 600MHz ARM Cortex-A8                                                           | 없음                                                                 |
| OMAP3530           | 65nm  | ARMv7    | 720MHz ARM Cortex-A8                                                           | PowerVR SGX530                                                     |
| OMAP3611           | 45nm  | ARMv7    | 800MHz ARM Cortex-A8                                                           | PowerVR SGX530                                                     |
| OMAP3621; OMAP3622 | 45nm  | ARMv7    | 3621: 800MHz, 3622: 1GHz; ARM Cortex-A8                                        | PowerVR SGX530                                                     |
| OMAP3630           | 45nm  | ARMv7    | 600MHz\~1.2GHz ARM Cortex-A8                                                   | PowerVR SGX530                                                     |
|                    |       |          |                                                                                |                                                                    |
| OMAP3640           | 45nm  | ARMv7    | 1.2GHz ARM Cortex-A8                                                           | PowerVR SGX530                                                     |
|                    |       |          |                                                                                |                                                                    |

### OMAP 4

[섬네일](https://ko.wikipedia.org/wiki/파일:Texas_Instruments_Ducati.svg "wikilink") OMAP 4세대 제품군 OMAP4430, 4460 (이전에는 OMAP 4440),\[6\] 및 OMAP 4470은 모두 ARM Cortex-A9 기반 듀얼 코어 SoC이다. OMAP4470은 대기 상태에서 전력 효율 향상을 위해 266MHz ARM Cortex-M3 기반의 보조 코어를 포함한다.\[7\] OMAP4430과 4460 제품은 [PowerVR](https://ko.wikipedia.org/wiki/PowerVR "wikilink") GPU SGX540을 탑재하고 있으며, 각각 304MHz와 384MHz로 작동한다.\[8\] OMAP4470은 PowerVR SGX544 GPU를 갖고 있고, DirectX 9를 지원해서 [윈도 8을](https://ko.wikipedia.org/wiki/윈도_8 "wikilink") 작동시킬 수 있으며, 별도의 2D 그래픽 가속기를 장착하여 전력 효율을 최대 50-90%까지 증가시켰다.\[9\] 모든 OMAP 4 프로세서는 IVA3 멀티미디어 가속기 및 1080p 풀 HD 동영상 인코더/디코더 기능을 지원하는 DSP 코어를 장착하였다.\[10\]\[11\]\[12\]\[13\]\[14\] OMAP 4는 ARM Cortex-A9 코어 및 SIMD 엔진인 NEON을 장착하였으며,\[15\] 듀얼 채널 LPDDR2 메모리 컨트롤러를 장착하였다.

| 모델명      | 제조 공정 | CPU 아키텍처 | CPU                                                                                | GPU                                                                         | 메모리 컨트롤러                 | 출시 시기     |
| -------- | ----- | -------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------------------------ | --------- |
| OMAP4430 | 45nm  | ARMv7    | 1-1.2GHz 듀얼 코어 ARM [Cortex-A9](https://ko.wikipedia.org/wiki/Cortex-A9 "wikilink") | [PowerVR](https://ko.wikipedia.org/wiki/PowerVR "wikilink") SGX540 @ 304MHz | 32비트 듀얼 채널 LPDDR2        | 2011년 1분기 |
| OMAP4460 | 45nm  | ARMv7    | 1.2-1.5GHz 듀얼 코어 ARM Cortex-A9                                                     | PowerVR SGX540 @ 384MHz                                                     | 32비트 듀얼 채널 LPDDR2        | 2011년 4분기 |
| OMAP4470 | 45 nm | ARMv7    | 1.5-1.8GHz 듀얼 코어 ARM Cortex-A9\[16\]                                               | PowerVR SGX544 @ 384MHz + Vivante GC320 2D 전용 그래픽 코어\[17\]                  | 32비트 듀얼 채널 466MHz LPDDR2 | 2012년 2분기 |
|          |       |          |                                                                                    |                                                                             |                          |           |

### OMAP 5 제품군

5세대 OMAP OMAP 5 프로세서는 듀얼 코어 ARM Cortext-A15 프로세서 및 2개의 추가적인 Cortex-M4 코어를 장착하여 사용량이 많지 않을 때 작업을 분산시켜서 전력 효율을 향상시켰다. 두 개의 PowerVR SGX544MP 그래픽 코어를 장착하였고 TI 2D BitBlt 그래픽 가속기, 다중 파이프 디스플레이 서브시스템 및 시그널 프로세서를 장착하였다.\[18\] 최대 2400만 및 2000만 화소까지의 전면 및 후면 카메라를 지원하며 3D HD 영상 녹화에 사용할 수 있다. 총 8GB의 듀얼 채널 LPDDR2/LPDDR3 메모리를 지원하며, 4개의 3D HD 디스플레이 출력, 3D HDMI 1.4 비디오 출력을 지원한다. 이 외에 USB 2.0 포트 3개, USB 3.0 OTG 포트 1개, SATA 2.0 컨트롤러를 장착하였다.

| 모델명      | 제조 공정                                                 | CPU 아키텍처                                                | CPU                                                                                                                                                               | GPU                                                                                                                                            | 메모리 공정                                                                                                                                                                                  | 출시 시기          |
| -------- | ----------------------------------------------------- | ------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| OMAP5430 | 28[nm](https://ko.wikipedia.org/wiki/나노미터 "wikilink") | [ARMv7](https://ko.wikipedia.org/wiki/ARMv7 "wikilink") | 2[GHz](https://ko.wikipedia.org/wiki/GHz "wikilink") 듀얼 코어 [ARM](../Page/ARM_홀딩스.md "wikilink") [Cortex-A15](https://ko.wikipedia.org/wiki/Cortex-A15 "wikilink") | [PowerVR](https://ko.wikipedia.org/wiki/PowerVR "wikilink") SGX544MP2 @ 532[MHz](https://ko.wikipedia.org/wiki/MHz "wikilink") + 2D/3D 그래픽 가속기 | 32비트 듀얼 채널 532[MHz](https://ko.wikipedia.org/wiki/MHz "wikilink") [LPDDR2](https://ko.wikipedia.org/wiki/LPDDR2 "wikilink") (8.5[GB](https://ko.wikipedia.org/wiki/기가바이트 "wikilink")/s) | 2013년 2분기 (예정) |
| OMAP5432 | 28nm                                                  | ARMv7                                                   | 2GHz 듀얼 코어 ARM Cortex-A15                                                                                                                                         | PowerVR SGX544MP2 @ 532MHz + 2D/3D 그래픽 가속기                                                                                                     | 32비트 듀얼 채널 532MHz [DDR3](../Page/DDR3_SDRAM.md "wikilink") (8.5GB/s)                                                                                                                    | 2013년 2분기 (예정) |
|          |                                                       |                                                         |                                                                                                                                                                   |                                                                                                                                                |                                                                                                                                                                                         |                |

## 기본 멀티미디어 애플리케이션 프로세서

휴대 전화 제조사를 대상으로 판매되며, 다기능이 통합된 저가형 제품을 대상으로 한다. OMAP-DM 계열 프로세서는 고화소 디지털 카메라를 장착한 모바일 장치의 디지털 미디어 보조 프로세서로 개발되었다. 이미지 시그널 프로세서(ISP)를 통하여 카메라 영상 처리를 가속한다.

  - OMAP331 - ARM9
  - OMAP310 - ARM9
  - OMAP-DM270 - ARM7 + [C54x](https://ko.wikipedia.org/wiki/TI_TMS320 "wikilink") DSP
  - OMAP-DM299 - ARM7 + ISP + 적층 mDDR SDRAM
  - OMAP-DM500 - ARM7 + ISP + 적층 mDDR SDRAM
  - OMAP-DM510 - ARM926 + ISP + 128MB 적층 mDDR SDRAM
  - OMAP-DM515 - ARM926 + ISP + 256MB 적층 mDDR SDRAM
  - OMAP-DM525 - ARM926 + ISP + 256MB 적층 mDDR SDRAM

## 모뎀 및 애플리케이션 통합 프로세서

휴대 전화 제조사를 대상으로 판매되며, 저가형 휴대폰에 장착하였다. TI가 모뎀 칩셋 시장에서 철수하면서 단종되었다.

  - OMAPV1035 - 단일 칩 EDGE (2009년 단종)
  - OMAPV1030 - EDGE 디지털 베이스밴드
  - OMAP850 - 200MHz ARM926EJ-S + [GSM](../Page/GSM.md "wikilink")/[GPRS](https://ko.wikipedia.org/wiki/GPRS "wikilink") 디지털 베이스밴드 + 적층 [EDGE](https://ko.wikipedia.org/wiki/EDGE "wikilink") 보조 프로세서
  - OMAP750 - 200MHz ARM926EJ-S + GSM/GPRS 디지털 베이스밴드 + DDR 메모리 지원
  - OMAP733 - 200MHz ARM926EJ-S + GSM/GPRS 디지털 베이스밴드 + 적층 SDRAM
  - OMAP730 - 200MHz ARM926EJ-S + GSM/GPRS 디지털 베이스밴드 + SDRAM 메모리 지원
  - OMAP710 - 133MHz ARM925 + GSM/GPRS 디지털 베이스밴드

## OMAP L-1x

OMAP L-1x 계열은 카탈로그 채널을 통해서 유통되며, 다른 OMAP 제품군과는 다르게 비디오 지향 TI 다빈치 제품에서 발전하였다. 다빈치 프로세서에서 비디오 가속 관련 기능을 삭제하고, 다른 주변 장치를 개선한 형태이다. 고정 소수점 대신 부동 소수점 DSP를 장착하였다.

  - OMAP-L137 - 300MHz ARM926EJ-S + C674x 부동 소수점 DSP
  - OMAP-L138 - 300MHz ARM926EJ-S + C674x 부동 소수점 DSP

## OMAP 탑재 제품

여러 제조사의 휴대 전화, 태블릿, 통합형 디스플레이, 개발 보드가 OMAP 칩을 탑재하였다.

## 비슷한 플랫폼

  - [퀄컴 스냅드래곤](../Page/스냅드래곤.md "wikilink")
  - [삼성 엑시노스](../Page/삼성_엑시노스.md "wikilink")
  - [화웨이](../Page/화웨이.md "wikilink")의 [하이 실리콘](https://ko.wikipedia.org/wiki/하이_실리콘 "wikilink")
  - [프리스케일 세미컨덕터의](../Page/프리스케일_세미컨덕터.md "wikilink") [i.MX](https://ko.wikipedia.org/wiki/i.MX "wikilink")
  - [엔비디아 테그라](../Page/엔비디아_테그라.md "wikilink")
  - [애플 A4](../Page/애플_A4.md "wikilink"), [애플 A5](../Page/애플_A5.md "wikilink")

## 각주

<references />

## 관련 항목

  - [텍사스 인스트루먼트](../Page/텍사스_인스트루먼트.md "wikilink")

## 외부 링크

  - [OMAP 애플리케이션 프로세서](http://www.ti.com/omap)
  - [OMAPWorld](https://web.archive.org/web/20100908234614/http://www.omapworld.org/)
  - [OMAPpedia](http://www.omappedia.org/wiki/Main_Page)

[분류:ARM 아키텍처](https://ko.wikipedia.org/wiki/분류:ARM_아키텍처 "wikilink") [분류:디지털 신호 처리 장치](https://ko.wikipedia.org/wiki/분류:디지털_신호_처리_장치 "wikilink") [분류:임베디드 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:임베디드_마이크로프로세서 "wikilink") [분류:단일 칩 체제](https://ko.wikipedia.org/wiki/분류:단일_칩_체제 "wikilink")

1.
2.
3.  [OMAP34xx series in TI Web site](http://focus.ti.com/general/docs/wtbu/wtbuproductcontent.tsp?templateId=6123&navigationId=11989&contentId=4682)
4.
5.
6.  <https://archive.is/20120903184239/http://www.linuxfordevices.com/c/a/News/Variscite-VARSOMOM44/> Computer module taps 1.5GHz, dual-core OMAP4460 SoC
7.  [Texas Instruments announces multi-core, 1.8GHz OMAP4470 ARM processor for Windows 8 - Engadget](http://www.engadget.com/2011/06/02/texas-instruments-announces-multi-core-1-8ghz-omap4470-arm-proc/)
8.  [AnandTech - TI Announces OMAP4470 and Specs: PowerVR SGX544, 1.8 GHz Dual Core Cortex-A9](http://www.anandtech.com/show/4413/ti-announces-omap-4470-and-specs-powervr-sgx544-18-ghz-dual-core-cortexa9)
9.
10.
11.
12.
13.
14.
15.
16. <http://www.ti.com/general/docs/wtbu/wtbuproductcontent.tsp?templateId=6123&navigationId=12869&contentId=123362>
17.
18.