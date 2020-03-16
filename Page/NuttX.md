> This article is converted from Wikipedia: [NuttX](https://ko.wikipedia.org/wiki/NuttX).


**NuttX**는 [임베디드 시스템의](../Page/임베디드_시스템.md "wikilink") 플랫폼으로 [ARM](../Page/ARM_아키텍처.md "wikilink"), [AVR](../Page/아트멜_AVR.md "wikilink"), AVR32, HCS12, LM32, [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink"), RISC-V, SuperH, Xtensa XL6, Z80등에 사용가능한 [운영 체제이다](../Page/운영_체제.md "wikilink"). 커널 유형은 [마이크로커널](../Page/마이크로커널.md "wikilink")(Microkernel)이다.

NuttX는 표준 준수 및 초소형 풋 프린트 설계보드에 중점을 둔 실시간 운영 시스템 ([RTOS](https://ko.wikipedia.org/wiki/RTOS "wikilink"))으로 개발되었다. 8비트에서32 비트 [마이크로 컨트롤러](https://ko.wikipedia.org/wiki/마이크로_컨트롤러 "wikilink") 환경까지 확장 가능한 NuttX의 주요 관리 표준은 [POSIX](../Page/POSIX.md "wikilink") 및 [ANSI](https://ko.wikipedia.org/wiki/ANSI "wikilink") 표준을 준수한다는 점에서 유연성을 보장한다. [유닉스](../Page/유닉스.md "wikilink") 및 기타 일반적인 표준 RTOS에대한 추가 API를 갖는 다른 마이크로커널이 이러한 표준에서 사용할 수없는 기능이나 임베디드 환경에서 적합하지 않을수있는 기능을 갖는다는 점에서 NuttX는 보다 더 강력하다고 할수있다.

NuttX는 허용된 [BSD 라이센스하에](https://ko.wikipedia.org/wiki/BSD_라이센스 "wikilink") 2007년 그레고리 너트(Gregory Nutt)에 의해 처음 배포되었다.

오픈소스를 지향하므로 따라서 커스터마이징이 가능하며 표준 C 라이브러리 OS에 완벽하게 통합되어있다.

## 핵심기술

  - 표준을 준수하는 [C로](../Page/C_\(프로그래밍_언어\).md "wikilink") 쓰여진 [커널](../Page/커널_\(컴퓨팅\).md "wikilink") ([GNU/Linux](https://ko.wikipedia.org/wiki/GNU/Linux "wikilink") 빌드방식)
  - 모듈형 설계
  - BSD 소켓 인터페이스
  - 대칭 멀티 프로세싱 (Symmetric Multi-Processing ,SMP)
  - 쓰레드 로컬 저장소 (TLS,Thread Local Storage)
  - [네트워크 파일 시스템](../Page/네트워크_파일_시스템.md "wikilink")(NFS)
  - [유닉스](../Page/유닉스.md "wikilink")및 다양한 표준 네트워크 프로토콜 지원

<!-- end list -->

  -
    IPv4, IPv6, TCP/IP, UDP, ARP, ICMP, ICMPv6, IGMPv2 and MLDv1/v2 (클라이언트 측)

<!-- end list -->

  - [Nutt Shell](https://ko.wikipedia.org/wiki/Nutt_Shell "wikilink") 제공

## 저수준 저전력 장치 운영체제

NuttX는 오픈소프트웨어 및 오픈하드웨어로 유명한 드론 업체 3DR의 [픽스호크 프로젝트](https://ko.wikipedia.org/wiki/픽스호크 "wikilink")(Pixhawk project,PX4)및 플라이트 컨트롤러(flight controller,FC)에 사용되는 운영체제이다. 픽스호크 플라이트 컨트롤러는 32비트 ARM 아키텍처인 Cortex M4를 장착했다. [리눅스재단](https://ko.wikipedia.org/wiki/리눅스재단 "wikilink")의 [드론 코드](https://ko.wikipedia.org/wiki/드론_코드 "wikilink") 프로젝트는 PX4를 채택하고 있다.\[1\]\[2\]\[3\]

이처럼 NuttX는 리소스를 최소한으로 구성하여 최적의 성능을 얻기위한 저수준에서 매우 효율적이며 또한 [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink") 플레이어등 여러 소형 장치의 운영체제로 사용되고 있다.\[4\]

## 함께보기

  - [VxWorks](../Page/VxWorks.md "wikilink")
  - [아두파일럿](../Page/아두파일럿.md "wikilink")

## 각주

## 참고

  - (NuttX Operating System - User's Manual by Gregory Nutt - Last Updated: July 15, 2018)https://web.archive.org/web/20190202042646/http://nuttx.org/doku.php?id=documentation:userguide
  - (공식 웹 사이트) www.nuttx.org
  - (What is Pixhawk)https://pixhawk.org/ 또는 <http://px4.io>
  - (드론코드 프로젝트)https://www.dronecode.org/about/

[분류:운영 체제](https://ko.wikipedia.org/wiki/분류:운영_체제 "wikilink")

1.  (PX4) <https://docs.px4.io/en/flight_controller/pixhawk.html>
2.  (PX4 Build) <http://dev.px4.io/kr/setup/dev_env_linux.html>
3.  (PX4 firmware) <https://github.com/PX4/Firmware>
4.