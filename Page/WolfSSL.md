> This article is converted from Wikipedia: [WolfSSL](https://ko.wikipedia.org/wiki/WolfSSL).


</ref> | 최근 버전= 3.15.3 | 최근 버전 출시일= 2018년 6월 22일\[1\] | 프로그래밍 언어= [C](../Page/C_\(프로그래밍_언어\).md "wikilink") | 종류= [보안 라이브러리](../Page/라이브러리_\(컴퓨팅\).md "wikilink") | 운영체제= 멀티 플랫폼 | 라이선스= [GNU GPLv2](https://ko.wikipedia.org/wiki/GNU_GPLv2 "wikilink") 또는 [상용 라이선스](https://ko.wikipedia.org/wiki/상용_라이선스 "wikilink")\[2\]\[3\] | 웹사이트=  }}

**wolfSSL** (이전 이름 **CyaSSL**)는 임베디드 시스템 개발자의 사용을 타겟으로 한 소형의 휴대성 좋은 내장 SSL / TLS 라이브러리이다. [C 언어](../Page/C_\(프로그래밍_언어\).md "wikilink") 로 작성된 TLS (SSL 3.0 TLS 1.0, 1.1, 1.2, 1.3, DTLS 1.0, 1.2)의 [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") 를 구현한다. SSL / TLS 클라이언트 라이브러리 및 서버 라이브러리를 포함, [SSL](../Page/전송_계층_보안.md "wikilink") 및 [TLS](../Page/전송_계층_보안.md "wikilink") 에서 정의 된 다양한 API 외에 지원한다. 또한 [OpenSSL](../Page/OpenSSL.md "wikilink") 에서 주로 사용되는 함수와 호환\[4\] 의 인터페이스를 제공하고있다.

wolfSSL / CyaSSL의 전신 인 **yaSSL**는 임베디드 환경과 자원의 한정된 리얼 타임 OS를 위한 [C ++](https://ko.wikipedia.org/wiki/C++ "wikilink") 로 작성된 SSL 라이브러리이다.

## 플랫폼

wolfSSL는 [Win32 / 64](../Page/윈도우_API.md "wikilink") , [Linux](../Page/리눅스.md "wikilink") , [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink") , [Solaris](https://ko.wikipedia.org/wiki/Solaris "wikilink") , ThreadX, [VxWorks](../Page/VxWorks.md "wikilink") , [FreeBSD](../Page/FreeBSD.md "wikilink") , [NetBSD](../Page/NetBSD.md "wikilink") , [OpenBSD](../Page/OpenBSD.md "wikilink") , [임베디드 Linux](../Page/임베디드_리눅스.md "wikilink") , [Haiku](https://ko.wikipedia.org/wiki/하이쿠_\(운영_체제\) "wikilink") , [OpenWrt](../Page/OpenWrt.md "wikilink") , [iPhone](https://ko.wikipedia.org/wiki/IOS "wikilink") , [Android](https://ko.wikipedia.org/wiki/Android "wikilink") , [Nintendo Wii](../Page/Wii.md "wikilink") 및 [Gamecube는](../Page/닌텐도_게임큐브.md "wikilink") DevKitPro 통하며 [QNX](../Page/QNX.md "wikilink") , [MontaVista](https://ko.wikipedia.org/wiki/:en:MontaVista "wikilink") , Tron variants, [NonStop](https://ko.wikipedia.org/wiki/:en:NonStop "wikilink") , [OpenCL](../Page/OpenCL.md "wikilink") , Micrium의 [MicroC / OS-II](https://ko.wikipedia.org/wiki/MicroC/OS-III "wikilink") , [FreeRTOS](../Page/FreeRTOS.md "wikilink"), [SafeRTOS](../Page/FreeRTOS.md "wikilink") , [프리 스케일 MQX](https://ko.wikipedia.org/wiki/:en:MQX "wikilink"), [Nucleus](../Page/Nucleus_RTOS.md "wikilink") , [TinyOS](../Page/TinyOS.md "wikilink"), [TI-RTOS](https://ko.wikipedia.org/wiki/:en:TI-RTOS "wikilink"), [HP-UX](../Page/HP-UX.md "wikilink") , uTasker 및 embOS 에서 이용 가능하다.

## 역사

yaSSL의 시작은 2004년으로 거슬러 올라간다. 2004년 당시 OpenSSL 가 가능했고, 그 라이센스는 *OpenSSL License* 및 *SSLeay license*의 듀얼 라이센스\[5\]라는 것이 독특한 것이었다. yaSSL은 상용 라이선스와 GPL로 듀얼 라이센스에서 사용할 수있는 OpenSSL의 대안으로 개발되었다\[6\] . yaSSL는 더 정교한 API 상용 개발의 지원, OpenSSL과의 완벽한 호환성을 제공했다\[7\]. wolfSSL/CyaSSL/yaSSL의 첫 시작은 [MySQL](../Page/MySQL.md "wikilink")\[8\]에서 이용되었다. 이 결과, yaSSL은 MySQL과의 번들링을 통해 수백만 단위의 매우 높은 보급을 실현했다.

## 프로토콜

자세한 내용은 [Transport Layer Security](../Page/전송_계층_보안.md "wikilink") 를 참조

wolfSSL는 다음의 다양한 프로토콜을 실현하고있다 :\[9\]

·        SSL 3.0, TLS 1.0, TLS 1.1, TLS 1.2, TLS 1.3

·        DTLS 1.0, DTLS 1.2

프로토콜 Notes:

·        SSL 2.0은 RFC 6176 에 의해 2011년 폐지되었다. WolfSSL은 이를 서포트하지 않는다.

·        SSL 3.0은 RFC 7568 에 의해 2015년 폐지되었다. [POODLE 공격에](https://ko.wikipedia.org/wiki/:en:POODLE_attack "wikilink") 대응하여, SSL 3.0은 wolfSSL 3.3.6 이후 기본적으로 비활성화 되었으나, 컴파일 시간 옵션으로 사용될 수 있다.\[10\]

## 알고리즘

wolfSSL는 다음의 암호화 라이브러리를 사용하고있다 :

### wolfCrypt

기본적으로 wolfSSL 표준에서는 wolfCrypt 에서 제공되는 암호화 서비스를 사용한다.\[11\] wolfCrypt은 [RSA](../Page/RSA_암호.md "wikilink") , [타원 곡선 암호](../Page/타원곡선_암호.md "wikilink") , [DSS](../Page/디지털_서명_알고리즘.md "wikilink") , [Diffie Hellman](../Page/디피-헬먼_키_교환.md "wikilink") , [EDH](https://ko.wikipedia.org/wiki/:en:Error_Detection_and_Handling "wikilink"), [NTRU](https://ko.wikipedia.org/wiki/:en:NTRU "wikilink") , [DES](../Page/데이터_암호화_표준.md "wikilink") , [Triple DES](../Page/트리플_DES.md "wikilink") , [AES](../Page/고급_암호화_표준.md "wikilink") ( CBC, CTR , CCM , GCM ) [Camellia](https://ko.wikipedia.org/wiki/:en:Camellia_\(cipher\) "wikilink") , [IDEA](https://ko.wikipedia.org/wiki/:en:International_Data_Encryption_Algorithm "wikilink"), [ARC4](https://ko.wikipedia.org/wiki/RC4 "wikilink") , [HC-128](https://ko.wikipedia.org/wiki/:en:HC-128 "wikilink") , [ChaCha20](https://ko.wikipedia.org/wiki/:en:ChaCha20 "wikilink") , [MD2](https://ko.wikipedia.org/wiki/:en:MD2_\(cryptography\) "wikilink") , [MD4](../Page/MD4.md "wikilink") , [MD5](../Page/MD5.md "wikilink") , [SHA](../Page/SHA.md "wikilink")-1 , [SHA-2](../Page/SHA-2.md "wikilink") , [BLAKE2](https://ko.wikipedia.org/wiki/:en:BLAKE_\(hash_function\) "wikilink") , [RIPEMD-160](https://ko.wikipedia.org/wiki/:en:RIPEMD-160 "wikilink"), [Poly1305](https://ko.wikipedia.org/wiki/:en:Poly1305 "wikilink") , 난수 생성 , 대규모 정수 연산베이스 16/64 인코딩 / 디코딩을 지원한다. 유럽의 eSTREAM 공용 도메인 스트림 암호 [Rabbit](https://ko.wikipedia.org/wiki/:en:Rabbit_\(cipher\) "wikilink") 도 포함되어있다. Rabbit은 고성능, 높은 부하 환경에서의 암호화 스트리밍 미디어에 잠재적으로 유용성이 있다. wolfCrypt는 SSL의 일종을 위해 필요한 기능에 특화하는 한편, 최대한의 이식성을 얻을 수 있도록 배려되어있다.

wolfCrypt는 또한 [Curve25519과](https://ko.wikipedia.org/wiki/:en:Curve25519 "wikilink") [Ed25519](https://ko.wikipedia.org/wiki/:en:EdDSA "wikilink") 을 지원한다.

wolfCrypt 는 MIT Kerberos\[12\](빌드 옵션 사용) 를 포함하여 몇 가지 소프트웨어 패키지와 라이브러리의 백엔드 암호화 구현으로 활약하고있다.

### NTRU

CyaSSL + 에는 NTRU\[13\] 공개 키 암호화가 포함되어 있다. CyaSSL +에의 NTRU의 추가는 yaSSL과 Security Innovation의 파트너십의 결과였다.\[14\] NTRU는 다른 공개 키 암호화와 같은 수준의 보안을 작은 비트 수로 제공하므로 모바일 및 임베디드 환경에서 잘 작동한다. 게다가 TRU 또는quantum attack에 대해서도 취약점이 알려져 있지 않다. TRU를 사용하하는 암호화 세트는 CyaSSL + 을 비롯하여 AES-256, RC4 또는 HC-128 등 에서 사용 가능하다.

## SGX

wolfSSL는 인텔 SGX (소프트웨어 보호 확장)\[15\]을 지원한다. 인텔 SGX는 공격 대상 영역을 줄이고 기존의 코드에서 눈에 띄는 성능 저하 없이 높은 수준의 안전성을 확보하고있다.

## 암호화 하드웨어 가속 지원

> <big>[Intel AES-NI](http://www.intel.com/content/www/us/en/architecture-and-technology/advanced-encryption-standard--aes-/data-protection-aes-general-technology.html) (Xeon 및 Core 프로세서 제품군)</big>

|                                                                                                                  |                   |
| ---------------------------------------------------------------------------------------------------------------- | ----------------- |
| [AES](../Page/고급_암호화_표준.md "wikilink") - [GCM](https://ko.wikipedia.org/wiki/:en:Galois/Counter_Mode "wikilink") | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CCM](https://ko.wikipedia.org/wiki/:en:CCM_mode "wikilink")             | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[ECB](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CTR](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
|                                                                                                                  |                   |

> <big>[AVX1 / AVX2](https://ko.wikipedia.org/wiki/:en:Advanced_Vector_Extensions "wikilink") (Intel 및 AMD x86)</big>

|                                        |
| -------------------------------------- |
| [SHA-2](../Page/SHA-2.md "wikilink")56 |
| [SHA-384](../Page/SHA-2.md "wikilink") |
| [SHA-512](../Page/SHA-2.md "wikilink") |
|                                        |

> <big>[RDRAND](https://software.intel.com/en-us/blogs/2012/11/17/the-difference-between-rdrand-and-rdseed) (Intel 64 IA-32 아키텍처)</big>

|                                        |
| -------------------------------------- |
| [SHA-2](../Page/SHA-2.md "wikilink")56 |
| [SHA-512](../Page/SHA-2.md "wikilink") |
|                                        |

> <big>[RDSEED](https://software.intel.com/en-us/blogs/2012/11/17/the-difference-between-rdrand-and-rdseed) (Intel Broadwell, AMD Zen)</big>

|                                        |
| -------------------------------------- |
| [SHA-2](../Page/SHA-2.md "wikilink")56 |
| [SHA-512](../Page/SHA-2.md "wikilink") |
|                                        |

> <big>[Freescale Coldfire SEC](http://www.nxp.com/assets/documents/data/en/application-notes/AN2788.pdf) (NXP MCF547X 및 MCF548X)</big>

|                                                                                   |                   |
| --------------------------------------------------------------------------------- | ----------------- |
| [DES](../Page/데이터_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink") | 64 bit            |
| [3DES](../Page/트리플_DES.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")   | 192 bit           |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")  | 128, 192, 256 bit |
|                                                                                   |                   |

> <big>[Freescale Kinetis MMCAU](http://www.nxp.com/assets/documents/data/en/application-notes/AN4307.pdf) K50, K60, K70 및 K80 (ARM Cortex-M4 core)</big>

|                                                                                                                  |                   |
| ---------------------------------------------------------------------------------------------------------------- | ----------------- |
| [MD5](../Page/MD5.md "wikilink")                                                                                 | 128 bit digest    |
| [SHA](../Page/SHA.md "wikilink")1                                                                                | 160 bit digest    |
| [SHA256](../Page/SHA-2.md "wikilink")                                                                            |                   |
| [DES](../Page/데이터_암호화_표준.md "wikilink")-[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 64 bit            |
| [3DES](../Page/트리플_DES.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                  | 192 bit           |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CCM](https://ko.wikipedia.org/wiki/:en:CCM_mode "wikilink")             | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") - [GCM](https://ko.wikipedia.org/wiki/:en:Galois/Counter_Mode "wikilink") | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[ECB](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
|                                                                                                                  |                   |

> <big>[ST 마이크로 일렉트로닉스 STM32](../Page/ST마이크로일렉트로닉스.md "wikilink") F1, F2, F4, L1, W 시리즈 (ARM Cortex - M3 / M4)</big>

|                                                                                   |                   |
| --------------------------------------------------------------------------------- | ----------------- |
| [RNG](https://ko.wikipedia.org/wiki/:en:Random_number_generation "wikilink")      |                   |
| [DES](../Page/데이터_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink") | 64 bit            |
| [DES](../Page/데이터_암호화_표준.md "wikilink") -[ECB](../Page/블록_암호_운용_방식.md "wikilink") | 64 bit Encrypt    |
| [3DES](../Page/트리플_DES.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")   | 192 bit           |
| [MD5](../Page/MD5.md "wikilink")                                                  | 128 bit           |
| [SHA](../Page/SHA.md "wikilink")1                                                 | 160 bit           |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")  | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CTR](../Page/블록_암호_운용_방식.md "wikilink")  | 128, 192, 256 bit |

<small>[CubeMX](http://www.st.com/en/development-tools/stm32cubemx.html) 및 [Std Per Lib](http://www.st.com/en/embedded-software/stm32-standard-peripheral-libraries.html?querycriteria=productId=LN1939)</small>

> <big>[Cavium NITROX](http://cavium.com/processor_security.html) (III / V PX 프로세서)</big>

|                                                                                             |                                       |
| ------------------------------------------------------------------------------------------- | ------------------------------------- |
| [RNG](https://ko.wikipedia.org/wiki/:en:Random_number_generation "wikilink")                |                                       |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")            | 128, 192, 256 bit                     |
| [3DES](../Page/트리플_DES.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")             | 192 bit                               |
| [RC4](https://ko.wikipedia.org/wiki/RC4 "wikilink")                                         | 2048 bit 최대                           |
| [HMAC](https://ko.wikipedia.org/wiki/:en:Hash-based_message_authentication_code "wikilink") | MD5 , SHA1 , SHA256 , SHA3            |
| [RSA](../Page/RSA_암호.md "wikilink")                                                         | 512 - 4096 bit                        |
| [ECC](../Page/타원곡선_암호.md "wikilink")                                                        | NIST Prime 192, 224, 256, 384 and 521 |
|                                                                                             |                                       |

> <big>[Microchip PIC32 MX / MZ](http://www.microchip.com/design-centers/32-bit) (Embedded Connectivity)</big>

|                                                                                                                  |                     |
| ---------------------------------------------------------------------------------------------------------------- | ------------------- |
| [MD5](../Page/MD5.md "wikilink")                                                                                 | 128 bit digest      |
| [SHA](../Page/SHA.md "wikilink")1                                                                                | 160 bit digest      |
| [SHA256](../Page/SHA-2.md "wikilink")                                                                            |                     |
| [HMAC](https://ko.wikipedia.org/wiki/:en:Hash-based_message_authentication_code "wikilink")                      | MD5 , SHA1 , SHA256 |
| [DES](../Page/데이터_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                | 64 bit              |
| [3DES](../Page/트리플_DES.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                  | 192 bit             |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit   |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CTR](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit   |
| [AES](../Page/고급_암호화_표준.md "wikilink") - [GCM](https://ko.wikipedia.org/wiki/:en:Galois/Counter_Mode "wikilink") | 128, 192, 256 bit   |
|                                                                                                                  |                     |

> <big>[Texas Instruments TM4C1294](http://www.ti.com/product/TM4C1294NCPDT) (ARM Cortex-M4F)</big>

|                                                                                                                  |                   |
| ---------------------------------------------------------------------------------------------------------------- | ----------------- |
| [DES](../Page/데이터_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                | 64 bit            |
| [3DES](../Page/트리플_DES.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                  | 192 bit           |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CCM](https://ko.wikipedia.org/wiki/:en:CCM_mode "wikilink")             | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") - [GCM](https://ko.wikipedia.org/wiki/:en:Galois/Counter_Mode "wikilink") | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[ECB](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CTR](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
|                                                                                                                  |                   |

> <big>[Nordic NRF51](https://web.archive.org/web/20180619035750/https://www.nordicsemi.com/Products/nRF51-Series-SoC) (Series SoC family 32-bit ARM Cortex M0 processor core)</big>

|                                                                                  |         |
| -------------------------------------------------------------------------------- | ------- |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[ECB](../Page/블록_암호_운용_방식.md "wikilink") | 128 bit |
| [RNG](https://ko.wikipedia.org/wiki/:en:Random_number_generation "wikilink")     |         |
|                                                                                  |         |

> <big>[Microchip](http://www.microchip.com/wwwproducts/en/ATECC508A) / [Atmel](http://www.atmel.com/Images/Atmel-8923S-CryptoAuth-ATECC508A-Datasheet-Summary.pdf) ATECC508A (MPU 또는 MCU 호환)</big>

|                                      |                     |
| ------------------------------------ | ------------------- |
| [ECC](../Page/타원곡선_암호.md "wikilink") | 256 bit (NIST-P256) |
|                                      |                     |

> <big>[ARMv8](https://www.arm.com/files/downloads/ARMv8_Architecture.pdf)</big>

|                                                                                                                  |                   |
| ---------------------------------------------------------------------------------------------------------------- | ----------------- |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CTR](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") - [GCM](https://ko.wikipedia.org/wiki/:en:Galois/Counter_Mode "wikilink") | 128, 192, 256 bit |
| [SHA256](../Page/SHA-2.md "wikilink")                                                                            |                   |
|                                                                                                                  |                   |

> <big>[Intel QuickAssist 기술](https://www.wolfssl.com/docs/intel-quickassist/)</big>

|                                                                                                                  |                           |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------- |
| [RSA](../Page/RSA_암호.md "wikilink")                                                                              | 512 - 4096 bit            |
| [SHA](../Page/SHA.md "wikilink")1                                                                                | 160 bit digest            |
| [SHA2](../Page/SHA-2.md "wikilink")                                                                              | 224, 256, 384 and 512 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit         |
| [AES](../Page/고급_암호화_표준.md "wikilink") - [GCM](https://ko.wikipedia.org/wiki/:en:Galois/Counter_Mode "wikilink") | 128, 192, 256 bit         |
| [ECC](../Page/타원곡선_암호.md "wikilink")                                                                             | Any curve or bit strength |
| [HMAC](https://ko.wikipedia.org/wiki/:en:Hash-based_message_authentication_code "wikilink")                      | SHA1 , SHA2               |
| [MD5](../Page/MD5.md "wikilink")                                                                                 |                           |
|                                                                                                                  |                           |

> <big>[Freescale NXP LTC](https://www.wolfssl.com/nxp-kinetis-k8x-ltc-support-for-pki-rsaecc-with-tls13/)</big>

|                                                                                                                  |                   |
| ---------------------------------------------------------------------------------------------------------------- | ----------------- |
| [Curve25519](https://ko.wikipedia.org/wiki/:en:Curve25519 "wikilink")                                            | 256 bit           |
| [Ed25519](https://ko.wikipedia.org/wiki/:en:EdDSA "wikilink")                                                    | 256 bit           |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CCM](https://ko.wikipedia.org/wiki/:en:CCM_mode "wikilink")             | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[ECB](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CBC](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") -[CTR](../Page/블록_암호_운용_방식.md "wikilink")                                 | 128, 192, 256 bit |
| [AES](../Page/고급_암호화_표준.md "wikilink") - [GCM](https://ko.wikipedia.org/wiki/:en:Galois/Counter_Mode "wikilink") | 128, 192, 256 bit |
| [SHA](../Page/SHA.md "wikilink")1                                                                                | 160 bit digest    |
| [SHA256](../Page/SHA-2.md "wikilink")                                                                            |                   |
| [ECC](../Page/타원곡선_암호.md "wikilink")                                                                             | 128, 256 bit      |
| [ECC](../Page/타원곡선_암호.md "wikilink")-[DHE](../Page/디피-헬먼_키_교환.md "wikilink")                                     | 128, 256 bit      |
| [RSA](../Page/RSA_암호.md "wikilink")                                                                              | 512 - 4096 bit    |
|                                                                                                                  |                   |

## 라이센스

wolfSSL는 오픈 소스로, GNU General Public License GPLv2\[16\]에 상용 라이센스를 받아 이용 가능하다.

## 각주

[분류:C 라이브러리](https://ko.wikipedia.org/wiki/분류:C_라이브러리 "wikilink") [분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:전송 계층 보안 구현](https://ko.wikipedia.org/wiki/분류:전송_계층_보안_구현 "wikilink")

1.   wolfSSL Embedded SSL/TLS Library Documentation|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-27}}
2.  <http://www.cryptlib.com/security-faq>
3.  <https://www.gnu.org/licenses/license-list.html#BerkeleyDB>
4.   wolfSSL SSL/TLS Library|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-27}}
5.
6.   wolfSSL Embedded SSL/TLS Library|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-27}}
7.
8.
9.   Chapter 4: Features {{\!}} Documentation|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-27}}
10.
11.  Chapter 10: wolfCrypt Usage Reference {{\!}} Docs|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-27}}
12.
13.
14.
15.
16.