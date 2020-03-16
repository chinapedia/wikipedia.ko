> This article is converted from Wikipedia: [PC](https://ko.wikipedia.org/wiki/PC).


[섬네일](https://ko.wikipedia.org/wiki/파일:IBM_PowerPC601_PPC601FD-080-2_top.jpg "wikilink")

**파워PC**(Power PC, Performance Optimization With Enhanced RISC – Performance Computing의 약어, 간단히 **PPC**)는 [1991년](../Page/1991년.md "wikilink") [애플](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink"), [IBM](../Page/IBM.md "wikilink"), [모토로라](../Page/모토로라.md "wikilink") 등이 제휴한 [AIM 연합에서](https://ko.wikipedia.org/wiki/AIM_연합 "wikilink") 발표한 [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") 방식의 명령 집합 아키텍처(Instruction Set Architecture)를 말한다. PowerPC 명령 집합은 지속적으로 진화하고 있으며, [2006년](../Page/2006년.md "wikilink")에 Power ISA로 이름을 바꾸었으나, 그 이후에도 파워PC는 [파워 아키텍처](https://ko.wikipedia.org/wiki/파워_아키텍처 "wikilink") 기반의 몇몇 프로세서를 통칭하는 명칭으로 사용되고 있다.

파워PC 아키텍처 자체는 동작의 기본이 되는 [명령 집합이나](https://ko.wikipedia.org/wiki/명령_집합 "wikilink") [레지스터](https://ko.wikipedia.org/wiki/레지스터 "wikilink") 집합, [메모리 어드레싱](https://ko.wikipedia.org/wiki/메모리_어드레싱 "wikilink"), [캐시](../Page/캐시.md "wikilink") 모델 등을 규정하고 있지만 이들의 [구현](../Page/구현.md "wikilink") 방법에 대한 규정은 없다. 그러므로 극단적으로 파워 피씨 아키텍처에서 내부적으로 [CISC](https://ko.wikipedia.org/wiki/CISC "wikilink") 또는 [소프트웨어](../Page/소프트웨어.md "wikilink")를 구현해도 파워 피씨 프로세서라고 부를 수 있다. 이러한 특징으로 실제로 제조되는 모델은 고속화를 위해서 아키텍처 수준에서는 규정되어 있지 않은 부품(2차, 3차 캐시나 관련 레지스터 등)을 갖추고 있는 것이 보통이다.

원래는 AIM(애플, IBM, 모토로라) 플랫폼의 CPU가 이런 의미로 개발된 것이지만, CPU 말고는 개발된 것이 없으므로 오늘날까지 남아 있는 파워피씨 계열 프로젝트의 유일한 성과물이기도 하다. 파워피씨는 [애플 컴퓨터사의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [파워맥](https://ko.wikipedia.org/wiki/파워맥 "wikilink")에 사용되었다. 그 밖에는 [IBM](../Page/IBM.md "wikilink")의 일부 [워크스테이션](../Page/워크스테이션.md "wikilink"), [서버](../Page/서버.md "wikilink")나 [BlueGene/L](https://ko.wikipedia.org/wiki/BlueGene/L "wikilink")뿐만 아니라 [슈퍼 컴퓨터에도](https://ko.wikipedia.org/wiki/슈퍼_컴퓨터 "wikilink") 사용된다.

또한 기판 크기가 작고 소비 전력이 낮으며 [자일링스](../Page/자일링스.md "wikilink") [FPGA](../Page/FPGA.md "wikilink")용 [IP 코어도](https://ko.wikipedia.org/wiki/IP_코어 "wikilink") 제공한다. 현재는 [모토로라](../Page/모토로라.md "wikilink")에서 분리된 [프리스케일 세미컨덕터와](../Page/프리스케일_세미컨덕터.md "wikilink") [IBM](../Page/IBM.md "wikilink")에서 개발하여 제조하고 있다.

## 특징

파워 피씨는 [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") 개념으로 만들어져 있으며 [슈퍼 스칼라](https://ko.wikipedia.org/wiki/슈퍼_스칼라 "wikilink") 방식으로 명령을 실행한다.

기본적인 파워의 특징에 몇 가지 수정 사항이 추가되었다.

  - [빅 엔디언](https://ko.wikipedia.org/wiki/빅_엔디언 "wikilink") 및 [리틀 엔디언](https://ko.wikipedia.org/wiki/리틀_엔디언 "wikilink") 지원 (G5 제외)
  - 단정도 [부동 소수점](https://ko.wikipedia.org/wiki/부동_소수점 "wikilink") 연산에 배정밀도 부동 소수점 연산 추가
  - 32[비트](../Page/비트_\(단위\).md "wikilink") 명령과 64 비트 명령 집합이 완전하게 [하위 호환](../Page/하위_호환성.md "wikilink")
  - 32개의 [GPR](https://ko.wikipedia.org/wiki/GPR "wikilink") (범용 레지스터)과 32 개의 [FPR](https://ko.wikipedia.org/wiki/FPR "wikilink")(부동 소수점 레지스터)
  - 파워 아키텍처 가운데 복잡한 것을 생략한 [명령 집합](https://ko.wikipedia.org/wiki/명령_집합 "wikilink")
  - 명령은 기본적으로 [하드 와이어](https://ko.wikipedia.org/wiki/하드_와이어 "wikilink") (Hard-Wired) 논리로 구현(일부는 마이크로 코드로 구현)
  - G4(제4 세대) 시리즈에서는128 비트 단위로 [벡터 연산을](https://ko.wikipedia.org/wiki/벡터_연산 "wikilink") 실시하는 [AltiVec](https://ko.wikipedia.org/wiki/AltiVec "wikilink")( [애플 컴퓨터는](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 벨로시티 엔진(Velocity Engine)이라고 부른다)를 적용
  - G5의 벡터 연산 장치는 슈퍼 스칼라나 슈퍼 [파이프 라인으로](https://ko.wikipedia.org/wiki/파이프_라인 "wikilink") 200개의 명령을 동시에 처리할 수 있도록 향상됨

## 역사

[1970년대](https://ko.wikipedia.org/wiki/1970년대 "wikilink") 후반, [존 콕의](https://ko.wikipedia.org/wiki/존_콕 "wikilink") [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") 아이디어를 착안한 미 [IBM](../Page/IBM.md "wikilink")사의 801 [프로토타입](../Page/프로토타입.md "wikilink") 칩으로 시작되었다. 801을 기본으로 한 코어는 수많은 IBM 제품에 채용되어 최종적으로는 16개의 [레지스터를](../Page/프로세서_레지스터.md "wikilink") 가진 [ROMP](https://ko.wikipedia.org/wiki/ROMP "wikilink") 프로세서인 [IBM RT까지](https://ko.wikipedia.org/wiki/IBM_RT "wikilink") 발전했다. 그러나 RT 프로세서의 성능은 충분하다고 말할 수 없었기 때문에 IBM은 [미국 프로젝트라고](https://ko.wikipedia.org/wiki/미국_프로젝트 "wikilink") 불리는 시장에서 가장 고속의 프로세서를 개발할 프로젝트를 시작했다. 이렇게 하여 개발된 것이 POWER 아키텍처이며, [1990](https://ko.wikipedia.org/wiki/1990 "wikilink")년 초에 [RISC System/6000과](https://ko.wikipedia.org/wiki/RISC_System/6000 "wikilink") 함께 발표되었다.

본래 POWER 마이크로프로세서는 [슈퍼 스칼라를](https://ko.wikipedia.org/wiki/슈퍼_스칼라 "wikilink") 실현한 최초의 프로세서의 하나이며, 높은 성능으로 [멀티 프로세서에](https://ko.wikipedia.org/wiki/멀티_프로세서 "wikilink") 대응하고 있었다. 하지만 IBM의 RS/6000의 제품군을 저성능 제품에서 부터 고성능 제품으로 확대할 즈음 POWER 프로세서로부터 몇 개의 구성 요소를 없애 싱글 칩 프로세서로 할 필요가 생겼기 때문에 IBM는 [RSC](https://ko.wikipedia.org/wiki/RSC "wikilink")(RISC 싱글 칩)의 개발에 착수했다. RSC는 개발의 초기 단계에서는 개인부터 공업용으로까지 폭넓게 사용할 수 있을 가능성을 가진 고기능의 프로세서가 될 것이라고 여겨졌다.

[1991년](../Page/1991년.md "wikilink") IBM은 애플 컴퓨터에 POWER 아키텍처를 기반으로 한 싱글 칩 마이크로프로세서 개발을 공동협력 하자고 제안한다. 애플컴퓨터는 그 당시 사무용 컴퓨터용 프로세서의 최대 공급 업체인 모토로라에 이 사실을 제안한다. 이 이유는 모토로라가 IBM보다 마이크로프로세서의 대량생산 경험이 풍부하고 마이크로프로세서에 대한 2차 공급자가 필요했기 때문이다. 이로써 IBM, 애플 컴퓨터, 모토로라라는 [AIM 연합이](https://ko.wikipedia.org/wiki/AIM_연합 "wikilink") 탄생한다.

[1991년](../Page/1991년.md "wikilink") PowerPC는 AIM 연합에게 가장 큰 요소의 하나가 되었다. 당시 [개인용 컴퓨터](../Page/개인용_컴퓨터.md "wikilink") 시장에서는 [마이크로소프트](../Page/마이크로소프트.md "wikilink") [윈도를](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 개발하고 있었으며, [인텔](../Page/인텔.md "wikilink") 프로세서가 시장을 지배하고 있었다. 또한 [CISC](https://ko.wikipedia.org/wiki/CISC "wikilink") 아키텍처의 인텔 [80386](https://ko.wikipedia.org/wiki/80386 "wikilink") 및 [80486](https://ko.wikipedia.org/wiki/80486 "wikilink")이 대부분의 컴퓨터에 채용되고 있어 다음의 [펜티엄](../Page/펜티엄.md "wikilink") 프로세서의 개발도 순조롭게 진행되고 있었다. PowerPC 프로세서는 모험적인 요소를 포함하고 있었지만, 확대되고 있는 마이크로소프트와 인텔에게 지배 당하지 않으려고 개발을 계속 진행하였다.

POWER 계열 프로세서의 개발에 참가하는 일은 모토로라에게는 다시 없을 기회였다. 이 시점에서 모토로라는 이미 자사 제품의 RISC 프로세서 [MC88000](https://ko.wikipedia.org/wiki/MC88000 "wikilink")을 시장에 투입하고 있었다. 그러나 이 프로세서는 빈약한 설계 수법과 제조상의 문제로 인해 시장에서는 낮은 평가를 받았고, 판매는 침체하고 있었다. 이 때문에 모토로라는 [MIPS나](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink") [SPARC](../Page/SPARC.md "wikilink") 경합 제품에 의해 시장을 잃고 있었다. 그러나 신형 POWER 계열 프로세서의 개발에 참가하면 [캐시](../Page/캐시.md "wikilink") 부분을 설계하기만 해도 잘 테스트된 고성능 RISC 프로세서를 판매할 수 있게 되므로 RISC 프로세서 시장에서의 반격이 기대되었다. 또한 중요한 고객인 애플 컴퓨터와의 관계의 개선이나 IBM에 제한 버전을 공급할 수 있을 가능성도 있었다.

한편 평가를 낮게 받았던 MC88000 프로세서는 이미 생산되고 있었고 애플사는 이미 이 프로세서를 이용한 프로토타입의 컴퓨터를 사용하고 있었다. 이 때문에 개발 중인 POWER 아키텍처 단일 칩 버스에 하드웨어의 단계에서 MC88000의 버스와의 호환성을 갖게 하면 [논리 기판을](https://ko.wikipedia.org/wiki/논리_기판 "wikilink") 다시 설계하는 것보다 더 빠르게 신형 프로세서를 시장에 투입할 수 있었다. 최종적으로 신형 프로세서 PowerPC에 대한 요구를 설계에 포함시키게 되었다.

그러나 PowerPC가 시장에 투입되기 직전 큰 움직임이 있었다. 애플 컴퓨터에 가세한 IBM과 모토로라의 양 회사는 PowerPC 프로세서에 적용한 시스템을 제안했다. 마이크로소프트는 모토로라의 PowerPC 서버 전용의 [윈도 NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") 3.51을 발표하고 [선마이크로시스템](https://ko.wikipedia.org/wiki/선마이크로시스템 "wikilink")도 [솔라리스 OS의](https://ko.wikipedia.org/wiki/솔라리스_OS "wikilink") PowerPC 판을 발표했다. 또한 IBM은 자사 제품의 [AIX 유닉스를](https://ko.wikipedia.org/wiki/AIX_유닉스 "wikilink") 이식하고, [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")의 이식도 계획하고 있었다. 또한 90년대 중순 PowerPC 프로세서는 벤치마크에 최고 속도의 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 계열 프로세서와 맞먹거나 능가하는 성능을 발휘했다. 그러나 이러한 움직임은 얼마 안 되는 기간에 끝나고 결국 PowerPC 신형 아키텍처에 기대되고 있던 이상이 실현되는 일은 없었다. 윈도, OS/2, 그리고 썬의 고객은 PowerPC 용 소프트웨어의 부족을 이유로 PowerPC 프로세서는 거의 돌아보지 않았다. 이러한 운영 체제의 후계가 시장에 투입되는 일은 없고, PowerPC로부터 완전하게 떨어져 갔다. 최종적으로는 애플의 Mac OS 그리고 상용이 아닌 [PPC 리눅스](https://ko.wikipedia.org/wiki/PPC_리눅스 "wikilink") 만이 남았다.

[2005년](../Page/2005년.md "wikilink") PowerPC 계열 CPU에 큰 변화가 찾아왔다. 우선 [2005년](../Page/2005년.md "wikilink")의 [E3에](../Page/일렉트로닉_엔터테인먼트_엑스포.md "wikilink") 전시된 차세대 게임기(레볼루션(코드네임, 현재의[Wii](../Page/Wii.md "wikilink")), [플레이 스테이션3](https://ko.wikipedia.org/wiki/플레이_스테이션3 "wikilink"), [엑스박스 360](../Page/엑스박스_360.md "wikilink"))의 CPU가 모두 PowerPC 계열 아키텍처가 탑재된 것이다. 한편 지금까지 PowerPC를 채용하고 있었던 [애플 컴퓨터](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 회사의 [매킨토시](../Page/매킨토시.md "wikilink")가 [2006](https://ko.wikipedia.org/wiki/2006 "wikilink")년부터 [인텔](../Page/인텔.md "wikilink")사의 CPU로 전면적으로 바꾸어 가는 것이 발표되었다. 현재 애플은 인텔 아키텍처를 완전하게 받아들이는 작업이 끝났으므로 PowerPC의 PC를 위한 프로세서로서의 역사는 끝났다.

현재는 게임기, 서버나 슈퍼 컴퓨터 그리고 군사용 장비에 채용되고 있다.

## PowerPC의 프로세서

### G1

PowerPC 계열은 IBM의 기존의 POWER 프로세서를 기반으로 설계되었다. 그러므로 정식으로는 PowerPC의 세대에 대한 숫자가 없다.

  - [PowerPC 601](https://ko.wikipedia.org/wiki/PowerPC_601 "wikilink") - 50,66,80,90MHz, POWER 명령도 구현
  - PowerPC 601+ - 외부 [버스](../Page/버스.md "wikilink") 의 3배 [클럭](https://ko.wikipedia.org/wiki/클럭 "wikilink") 그리고 동작, 저전원 전압화(+2.5V) 100, 110, 120MHz
  - PowerPC 602 - 저가격판 [3DO의](https://ko.wikipedia.org/wiki/3DO_인터렉티브_멀티플레이어 "wikilink") 후계 [M2에](https://ko.wikipedia.org/wiki/파나소닉_M2 "wikilink") 채용될 예정이었다. M2를 기반으로 했다. [코나미](../Page/코나미.md "wikilink")의 [업무용 게임기에](https://ko.wikipedia.org/wiki/업무용_게임기 "wikilink") 사용되었다.

### G2

알루미늄 배선 603, 604 G2가 1세대이고, 2세대의 경우 IBM이 문서에서 603e와 604e 모두 같은 배선을 적용하였다고 하였으나 250MHz 이상에 대한 문서가 흩어져 있어서 확실한 정보는 없다. 다만 어느 쪽이나 서로 버스가 완전하게 호환되었기 때문에 굳이 구별하는 것은 중요하지 않았다.

  - [PowerPC 603](https://ko.wikipedia.org/wiki/PowerPC_603 "wikilink") - 소비 전력이 낮음
      - PowerPC 603e - 소비 전력이 낮고 속도가 개선됨
      - PowerPC 603ev - PowerPC 603e보다 속도가 개선됨

<!-- end list -->

  - [PowerPC 604](https://ko.wikipedia.org/wiki/PowerPC_604 "wikilink") - [SMP](https://ko.wikipedia.org/wiki/대칭형_다중_처리 "wikilink") 호환, 인라인 L2 캐시, 고속의 부동 소수점 연산
      - PowerPC 604e - 604 의 낮은 소비 전력, 작아지고 속도가 개선됨
      - PowerPC 604ev - 604e 의 낮은 소비 전력, 작아지고 속도가 개선됨

<!-- end list -->

  - PowerPC 615 - [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")과 PowerPC 명령의 양립을 목표로 한 프로세서. [펜티엄](../Page/펜티엄.md "wikilink") 호환 소켓에 장착 가능. x86 프로세서로서는 당시의 펜티엄 등에 대항할 수 있는 성능을 유지할 것으로 전망되었지만 명령의 변환할 때 성능이 떨어진다. 다이 크기가 330 제곱 밀리미터와 파워피씨 계열으로서는 마이크로소프트 등이 지원하지 않을 가능성이 커서 개발이 중지되었다.

<!-- end list -->

  - PowerPC 620 - 64 비트판. 그 설계는 POWER3에 인계된다

<!-- end list -->

  - x0704 - 에크스포넨샤르사에 의한 호환 칩. BiCMOS가 제조한 것. 클럭 수는 당시의 PowerPC를 웃돌고 있었다.(433/500/533MHz)

### G3

[섬네일](https://ko.wikipedia.org/wiki/파일:Motorola_XPC7400RX400TK_top.jpg "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:XPC7455_01.jpg "wikilink") G3(제3 세대) 이후는 일반적으로 PowerPC를 채용한 대표적인 제품이 있다. [파워 매킨토시](https://ko.wikipedia.org/wiki/파워_매킨토시 "wikilink") 시리즈로 애플 표기에 함께 사용함으로써 구분이 일반적으로 명확하게 되었다. 성능에 비해 소비 전력이 낮은 것이 특징으로 현재는 주로 [임베디드 시스템에](../Page/임베디드_시스템.md "wikilink") 이용된다.

  - PowerPC 75x,74x - [PowerPC G3 시리즈로](https://ko.wikipedia.org/wiki/PowerPC_G3_시리즈 "wikilink") 불린다. 603e의 계열이며, PowerPC 75x 에는 백 사이드 캐시를 채용하였다. 정수 연산 장치를 2개가 기본이다.
      - PowerPC 750L -750 라인
      - PowerPC 750CX/CXe -256KB L2 캐시를 내장
      - PowerPC 750FX/FL -130나노미터 [SOI](https://ko.wikipedia.org/wiki/SOI "wikilink") L2 캐시 512KB
      - PowerPC 750GX -90나노미터 SOI, 200MHz FSB 대응, L2 캐시 1메가바이트, 1.1GHz 까지
      - PowerPC 750CL -L2 캐시 256KB, 400MHz \~1GHz, PowerPC 750GX의 약 50% 절전
  - Gekko - 닌텐도 게임 큐브용으로 개발된 것(PowerPC 750CXe를 기반으로 배정도 부동 소수점수(실수) 연산 대응, SIMD를 추가한 설계)
  - Broadway - 90나노미터 SOI, [닌텐도](../Page/닌텐도.md "wikilink")의 [Wii](../Page/Wii.md "wikilink") 용으로 개발(게코와 호환되며 PowerPC 750CL 기반이라고 여겨지지만 자세한 것은 공개되어 있지 않음)

### G4

G3을 기반으로 부동 소수점 연산 기능을 강화, [SIMD](https://ko.wikipedia.org/wiki/SIMD "wikilink")와 [대칭형 멀티 프로세서](https://ko.wikipedia.org/wiki/대칭형_멀티_프로세서 "wikilink")(SMP) 기능을 추가. 기존의 60x 버스보다 높은 수준의 제어 기능을 가졌다. [MPX 버스와도](https://ko.wikipedia.org/wiki/MPX_버스 "wikilink") 호환된다.

  - MPC 74xx - [G4 시리즈로](https://ko.wikipedia.org/wiki/G4_시리즈 "wikilink") 불린다. [모토로라](../Page/모토로라.md "wikilink") 및 [프리스케일 세미컨덕터에서](../Page/프리스케일_세미컨덕터.md "wikilink") 개발.
      - AltiVec ( Velocity Engine ) 탑재
      - CPU 버스에 MPX 버스 ( MaxBus ) 채용
      - SMP 호환
  - MPC 7400
      - MPC 7410 - 저전력판. 180 나노미터 공정으로 제조.
  - MPC 7450 - L2 캐시 256 킬로바이트 내장, L3 캐시 대응, 정수 연산 장치를 4개 기본으로 [파이프 라인의](https://ko.wikipedia.org/wiki/파이프_라인 "wikilink") 단계를 높여 속도를 빠르게 함.
      - MPC 7451 - 저전력판
      - MPC 7445 - 7455 의 L3 캐시 인터페이스 제거 제품.
      - MPC 7455 - 180 나노미터 공정,SOI를 채용. 클록은1GHz 에 다다름.
      - MPC 7457 - 130 나노미터 공정,L2 캐시를512KB 에
      - MPC 7447 - 7457의 L3 캐시 인터페이스 생략 타입. 전력 절약.
      - MPC 7448 - 90나노미터 공정으로 제조,1메가바이트의 L2 캐시, e600 코어를 채용.
      - MPC 8641 - e600 코어를 채용. 메모리 컨트롤러, [PCI 익스프레스](../Page/PCI_익스프레스.md "wikilink") 컨트롤러를 내장.
      - MPC 8641D - MPC 8641 의 듀얼 코어판.

### G5

PowerPC 970 - POWER4 기반으로 설계. G5로 불린다.

  - 64 비트
  - 파이프라인이 많아지고 더 높은 클럭으로 동작한다.
  - FSB 고속화(1GHz 초)
  - 고속의 부동 소수점 연산
  - AltiVec 호환의 VMX를 탑재
  - 리틀 엔디언(little endian)과 호환되지 않는다.

PowerPC 970은 다음과 같이 나뉜다.

  - PowerPC 970FX - 90 나노미터 공정으로 속도가 빨라졌다. 전력 절약 기능 파워 튠(PowerTune) 포함.
  - PowerPC 970MP - 듀얼 코어, 각 코어에 L2 캐시 1메가바이트 내장
  - PowerPC 970GX - PowerPC 970MP 의 싱글 코어·저전력판, L2 캐시 1메가바이트 내장

PWRficient PA6T는 P.A. 반도체로 설계한 64비트 호환 G5 제품이다.

  - 절전 (2GHz , 듀얼 코어로 평균 소비 전력 13와트 소비)
  - [멀티 코어](../Page/멀티_코어.md "wikilink") CONEXIUM 버스를 채용하였다.
  - 엔디언(endian)에 대응

## 관련 항목

  - [IBM 파워](https://ko.wikipedia.org/wiki/IBM_파워 "wikilink") - [IBM](../Page/IBM.md "wikilink")의 [유닉스](../Page/유닉스.md "wikilink")[서버](../Page/서버.md "wikilink") 및 [워크스테이션](../Page/워크스테이션.md "wikilink")용의 [CPU](../Page/중앙_처리_장치.md "wikilink")
  - [매킨토시](../Page/매킨토시.md "wikilink") - [애플 컴퓨터의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [개인용 컴퓨터](../Page/개인용_컴퓨터.md "wikilink")
  - [셀](https://ko.wikipedia.org/wiki/셀_\(마이크로프로세서\) "wikilink") -[소니 컴퓨터 엔터테인먼트](https://ko.wikipedia.org/wiki/소니_컴퓨터_엔터테인먼트 "wikilink"), [도시바](../Page/도시바.md "wikilink")와 공동으로 개발한 PowerPC계열 프로세서로 [플레이스테이션 3](../Page/플레이스테이션_3.md "wikilink") 등의 CPU.
  - [제논](../Page/제논_\(프로세서\).md "wikilink") - [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 [게임기](https://ko.wikipedia.org/wiki/게임기 "wikilink")인 [Xbox 360의](https://ko.wikipedia.org/wiki/Xbox_360 "wikilink") CPU, PowerPC계열 트리플 코어 프로세서.
  - [게임 큐브](https://ko.wikipedia.org/wiki/게임_큐브 "wikilink"), [Wii](../Page/Wii.md "wikilink") - [닌텐도](../Page/닌텐도.md "wikilink")의 [게임기](https://ko.wikipedia.org/wiki/게임기 "wikilink"). CPU에 PowerPC 계열 프로세서 Gekko, Broadway를 사용.

## 외부 링크

  - [IBM PowerPC 기능](http://www.ibm.com/chips/power/powerpc/)

  - [프리스케일 PowerPC 프로세서](http://www.freescale.com/webapp/sps/site/homepage.jsp?nodeId=0162468rH3bTdG)

  - [32비트 PowerPC 아키텍처(PDF)](https://web.archive.org/web/20070928191724/http://www.freescale.co.jp/pdf/MPCFPE32BJ_R1a.pdf)

  - [애플 PowerPC G5](https://www.apple.com/jp/g5processor/)

[분류:IBM](https://ko.wikipedia.org/wiki/분류:IBM "wikilink") [분류:파워 아키텍처](https://ko.wikipedia.org/wiki/분류:파워_아키텍처 "wikilink") [분류:파워PC 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:파워PC_마이크로프로세서 "wikilink")