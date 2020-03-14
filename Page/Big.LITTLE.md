> This article is converted from Wikipedia: [Big.LITTLE](https://ko.wikipedia.org/wiki/Big.LITTLE).


**ARM big.LITTLE**(빅리틀)은 [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink")에서 개발된 이기종 컴퓨팅 아키텍처로 상대적으로 전력 소모가 적은 저성능 코어(LITTLE)들과 전력 소모가 많은 고성능 프로세서 코어(big)들을 함께 탑재하는 구조를 말한다. 일반적으로 두 종류의 코어들 중 한 쪽만이 활성화되어 작동하며, 코어들이 동일한 메모리 영역을 사용하므로 상황에 따라 작업이 big 코어와 LITTLE 코어 사이에서 동적으로 할당된다.\[1\] 이러한 구조의 목적은 멀티코어 환경에서 그때 그때 필요한 계산량에 따라 동적으로 코어를 할당함으로써 단순히 클럭을 조절하는 것보다 더 높은 수준의 전력소모 절감을 달성하는 것이다. [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink")의 마케팅 자료에 의하면 특정 상황에서 최대 75%까지 전력소모 절감이 가능하다.\[2\]

빅리틀 구조가 적용된 최초의 프로세서는 2011년 10월 발표된 Cortex-A7이었으며, 이 프로세서는 Cortex-A15와 구조적인 호환성을 갖도록 설계되었다.\[3\] 2012년 10월에 ARM은 Cortex-A53와 Cortex-A57(ARMv8) 코어들을 발표했다, 이 프로세서들 또한 서로 호환되어 빅리틀 칩 안에서 함께 사용하는 것이 가능하다.\[4\] 이후 2013년에는 Cortex-A12, 2014년 2월에는 Cortex-A17이 발표되었으며, 두 코어는 Cortex-A7과 함께 모두 한 칩 내에서 빅리틀 구조로 사용이 가능하다.\[5\]\[6\]

## 클러스터 마이그레이션

big.LITTLE에는 다른 성능의 프로세서 코어들을 이어주기 위한 리눅스 커널에 포함되어 스케줄러의 종속되어있는 3가지 방법이 있다. 클러스터화 모델 접근법은 첫 그리고 가장 단순한 적용이다. 이 접근법일 때 OS 스케줄러는 두 프로세서 클러스터들 중 하나만 볼 수 있다. CPU의 부하가 특정 포인트에 다가갔을 때 시스템은 다른 클러스터로 전이된다. 모든 관련 데이터는 L2 캐시를 통하여 바로 이동 된다. 첫 번째 코어 클러스터는 꺼지고 다른 하나의 클러스터는 활성화 된다. 캐시 일관성 인터커넥트(Cache Coherent Interconnect, CCI)가 사용된다. 이 모델은 삼성 Exynos 5 (5410)에 구현되었다.

## 인-커널 스위처(CPU 마이그레이션)

인커널 스위처(In Kernel Switcher, IKS)를 통해 이루어지는 CPU 마이그레이션은 'Big' 코어와 'LITTLE' 코어의 쌍으로 이루어져 있는데, 한 칩 안에 가능한 많은 동일한 칩들로 구성되어 있다. 각 쌍들은 가상의 하나의 코어처럼 작동하고, 한 시점에 반드시 둘 중 하나의 코어만 작동한다. 'Big' 코어는 높은 요구 상황에서 작동하고, 'LITTLE' 코어는 낮은 요구 상황에서 작동한다.

가상 코어의 변화(High와 low의 사이 변화)가 요구될 때, 새로 사용되는 코어는 전력이 인가되고, 실행 상태(Running state)가 전이되며, 사용이 중지된 코어는 꺼진다. 그리고 새로운 코어 상에서 프로세싱이 지속된다. 스위칭은 cpufreq 프레임워크에 의해서 완료된다. 완벽한 big.LITTLE IKS의 구현은 리눅스 3.11이나 3.12쯤이 예상된다. big.LITTLE IKS는 클러스터 마이그레이션의 발전된 형태이고, 제일 큰 다른 점은 각 쌍들이 스케줄러에게 가시적이라는 점이다. 'big'과 'LITTLE'코어들의 비대칭(non-symmetric) 그룹화에는 더 많은 합의점들이 포함된다. 하나의 칩이 한 두개의 'big' 코어와 보다 많은 'LITTLE' 코어들을 가질 수 있다, 혹은 반대의 경우도 있다. 엔비디아가 Tegra 3 SoC에 저전력의 컴패니언 코어('companion core')라는 이것과 비슷한 것을 만들었다.

## 이기종 간 다중 처리 (전역 태스크 스케줄링)

big.LITTLE의 ﻿ 가장 강력한 사용 모델은 모든 코어들을 동시에 사용 가능한 이기종 간 다중 처리(heterogeneous multi-processing)이다. 이 모델에서는 높은 우선순위거나 높은 계산능력을 요하는 스레드들이 백그라운드 태스크(task)들 처럼 낮은 우선 순위나 낮은 계산 능력을 요하는 스레드들과 동시에 같은 빅 코어를 할당 받을 수 있고, 'LITTLE' 코어들을 통해서도 수행할 수 있다. 수 분기 내에 리눅스 커널에서 big.LITTLE의 상위 GTS 패치들에 완전 포함할 예정이다. 이 모델은 삼성 Exynos 5 Octa(5420)에 포함되었다.

## 스케줄링

쌍으로 된 처리 방식은 운영 체제가 이미 존재하는 DVFS(동적 전압 및 주파수 교환: dynamic voltage and frequency switching) 기능을 완전하게 지원하기위해 스위칭을 하는 것을 허용한다.

커널 안에 이미 존재하는 DVFS 지﻿원(ex. 리눅스의 cpufreq)은 간단하게 주파수/전압(frequencies/voltages) 목록을 보거나 그 둘 사이가 보기 좋도록 교환(switch)될 것이다, 마치 이것이 존재하는 하드웨어에서 작동하는 듯이 말이다.

로엔드(low-end) 슬롯들은 'LITTLE' 코어에서 동작하고 하이엔드(high-end) 슬롯들은 'big' 코어에서 동작하게 된다. 그렇지 않으면, 아마도 모든 코어들은 각 프로세스/스레드가 실행되는 곳이 어딘지 결정할 수 있는 ﻿커널의 스케줄러에 노출될 것이다.

이것은 기본적으로 넌페어(non-paired) 방식이 요구되지만, 페어(paired) 코어들에서도 가능하다. 이것은 ﻿몇 가지 커널 스케줄러에 특별한 문제들을 야기한다. 적어도 현대의 상용화된 하드웨어들에는 SMP 시스템을 사용한 모든 코어들이 같은 문제를 가지고 있다고 추정할 수 있다.

## 글로벌 태스크 스케줄링의 이점

  - 코어 간 마이그레이션의 작업 부하를 유연하게 제어할 수 있다. 스케줄러가 태스크들을 코어들 사이에 직접적으로 이주(migrating)시킴으로써 커널의 부하를 줄이고 전력을 절약할 수 있다.
  - 스케줄러 내 구현 및 교환 결정이 IKS에 구현된 cpufreq 프레임워크에 구현된 것보다 빠르다.
  - 비대칭 SoCs(e.g. 2 Cortex-A15 코어들과 4 Cortex-A7 코어들)﻿을 쉽게 지원하기 위한 능력을 제공한다.
  - 모든 코어들을 동시에 사용하기 위해 Soc는 IKS와 비교하여 향상된 최고의 성능을 제공한다.

## 구현 상황

| SoC                                                                               | 제조 공정 | 빅 코어들                                                                                                                                             | 리틀 코어들                                                                                   | GPU               | 메모리 인터페이스                                | 무선 네트워크 기술 | 사용 가능 일자 | 활용 디바이스                                                                                                               |
| --------------------------------------------------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ----------------- | ---------------------------------------- | ---------- | -------- | --------------------------------------------------------------------------------------------------------------------- |
| [HiSilicon K3V3](https://ko.wikipedia.org/wiki/:en:HiSilicon#K3V3 "wikilink")     | 28 nm | 1.8 GHz [듀얼 코어](https://ko.wikipedia.org/wiki/멀티_코어_프로세서 "wikilink") [Cortex-A15](https://ko.wikipedia.org/wiki/ARM_Cortex-A15_MPCore "wikilink") | 1.2 GHz 듀얼 코어 [Cortex-A7](https://ko.wikipedia.org/wiki/ARM_Cortex-A7_MPCore "wikilink") | Mali-T658         |                                          |            | H2 2013  |                                                                                                                       |
| 삼성 [엑시노스](https://ko.wikipedia.org/wiki/엑시노스 "wikilink") 5 옥타 (5410 모델)\[7\]\[8\] | 28 nm | 1.6-1.8 GHz [쿼드 코어](https://ko.wikipedia.org/wiki/멀티_코어_프로세서 "wikilink") Cortex-A15                                                               | 1.2 GHz 쿼드 코어 Cortex-A7                                                                  | PowerVR SGX544MP3 | 32비트 듀얼 채널 800 MHz LPDDR3 (12.8 GB/sec)  |            | Q2 2013  | [삼성 갤럭시 S4](../Page/삼성_갤럭시_S4.md "wikilink") (GT-I9500 / SHV-E300 / SCH-I959 / GT-I9502모델에 한함. 이외의 모델은 퀄컴사의 AP를 사용함.) |
| 삼성 [엑시노스](https://ko.wikipedia.org/wiki/엑시노스 "wikilink") 5 옥타 (5420 모델)\[9\]      | 28 nm | 1.8-2.0 GHz 쿼드 코어 Cortex-A15                                                                                                                      | 1.3 GHz 쿼드 코어 Cortex-A7                                                                  | Mali-T628MP6      | 32비트 듀얼 채널 933 MHz LPDDR3e (14.9 GB/sec) |            | Q4 2013  | [삼성 갤럭시 노트 3](https://ko.wikipedia.org/wiki/삼성_갤럭시_노트_3 "wikilink")\[10\]                                             |
| 삼성 [엑시노스](https://ko.wikipedia.org/wiki/엑시노스 "wikilink") 5 옥타 (5422 모델)           |       | 2.1 GHz 쿼드 코어 Cortex-A15                                                                                                                          | 1.5 GHz 쿼드 코어 Cortex-A7                                                                  | Mali-T628MP6      |                                          |            |          | [삼성 갤럭시 S5](https://ko.wikipedia.org/wiki/삼성_갤럭시_S5 "wikilink")                                                       |
| Renesas Mobile MP6530\[11\]                                                       | 28 nm | 2 GHz 듀얼 코어 Cortex-A15                                                                                                                            | 1 GHz 듀얼 코어 Cortex-A7                                                                    | PowerVR SGX544    | 듀얼 채널 LPDDR3                             | LTE CAT4   |          |                                                                                                                       |

## 참조

  -
  -
  -
  -
  -
## 외부 링크

  - [big.LITTLE Processing](https://web.archive.org/web/20121022055646/http://www.arm.com/products/processors/technologies/bigLITTLEprocessing.php)

  - [big.LITTLE Processing with ARM CortexTM-A15 & Cortex-A7](https://web.archive.org/web/20131017064722/http://www.arm.com/files/downloads/big_LITTLE_Final_Final.pdf) (PDF) (full technical explanation)

[분류:ARM 아키텍처](https://ko.wikipedia.org/wiki/분류:ARM_아키텍처 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.