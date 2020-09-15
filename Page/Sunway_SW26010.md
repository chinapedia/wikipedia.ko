> This article is converted from Wikipedia: [Sunway SW26010](https://ko.wikipedia.org/wiki/Sunway_SW26010).


**[Sunway](../Page/Sunway.md "wikilink") SW26010**은 상하이의 National High Performance Integrated Circuit Design Center에서 설계한 260 코어의 멀티 코어 프로세서이다.\[1\] 이 제품은 중국에서 설계된 [64 비트](https://ko.wikipedia.org/wiki/64bit "wikilink") [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") (Reduced Instruction Set Computing) [아키텍처](https://ko.wikipedia.org/wiki/아키텍처 "wikilink")인 Sunway 아키텍처를 구현했다. SW26010에는 8x8 어레이로 배열 된 64 개의 Compute Processing Elements (CPE) 클러스터가 4 개 있다. 이러한 CPE는 [SIMD](https://ko.wikipedia.org/wiki/SIMD "wikilink") 명령어를 지원하며 사이클 당 8배의 정밀도에서 [부동소수점](../Page/부동소수점.md "wikilink") 연산을 수행 할 수 있다. 각 클러스터에는 관리 기능을 제공하는 MPE (Management Processing Element)라고하는보다 일반적인 범용 코어가 있다. 각 클러스터는 고유한 [DDR3](https://ko.wikipedia.org/wiki/DDR3 "wikilink") [SDRAM](../Page/SDRAM.md "wikilink") 컨트롤러와 자체 주소 공간이있는 메모리 뱅크를 가지고 있다.\[2\]\[3\] 프로세서는 1.45GHz의 클럭 속도로 작동한다.\[4\]\[5\]

CPE 코어는 기존 캐시 계층 구조 대신 64KB의 스크래치 패드 메모리와 16KB의 명령어를 제공하며 칩을 통해 네트워크를 통해 통신한다. MPE는 32KB L1 명령어 및 데이터 캐시와 256KB L2 캐시를 사용하는보다 전통적인 설정이다. 마지막으로 온칩 네트워크는 칩을 외부 인터페이스에 연결하는 단일 시스템 상호 연결 인터페이스에 연결된다.\[6\]

SW26010은 [썬웨이 타이후 라이트](https://ko.wikipedia.org/wiki/썬웨이_타이후_라이트 "wikilink")(Sunway TaihuLight) 슈퍼 컴퓨터에 사용되며, 2016년 11월 현재 [TOP500](../Page/TOP500.md "wikilink") 프로젝트에서 세계에서 가장 빠른 슈퍼 컴퓨터이다. 이 시스템은 40,960 개의 SW26010을 사용하여 [LINPACK](../Page/LINPACK.md "wikilink") 벤치 마크에서 93.01 PFlop/s를 얻었다.\[7\]

## 같이 보기

  - [베오울프 클러스터](../Page/베오울프_클러스터.md "wikilink")
  - [스팍프로세서](../Page/SPARC.md "wikilink")
  - [알파 프로세서](https://ko.wikipedia.org/wiki/알파_프로세서 "wikilink")

## 참고

  - [National Supercomputing Center in Wuxi](https://web.archive.org/web/20170925141254/http://nsccwx.cn/) (NRCPC)
  - (NUDT)National Super Computer Center in Guangzhou

## 각주

[분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink")

1.  Dongarra, Jack (June 20, 2016). "Report on the Sunway TaihuLight System" (PDF). www.netlib.org. Retrieved June 20, 2016.
2.  Fu, Haohuan; Liao, Junfeng; Yang, Jinzhe; et al. (2016). "The Sunway TaihuLight Supercomputer: System and Applications". Sci. China Inf. Sci. <doi:10.1007/s11432-016-5588-7>. Retrieved 2016-06-22.
3.  Trader, Tiffany (June 19, 2016). "China Debuts 93-Petaflops ‘Sunway’ with Homegrown Processors". HPC Wire. Retrieved 21 June 2016. Each core of the CPE has a single floating point pipeline that can perform 8 flops per cycle per core (64-bit floating point arithmetic) and the MPE has a dual pipeline each of which can perform 8 flops per cycle per pipeline (64-bit floating point arithmetic). Jump up ^
4.  Hemsoth, Nicole (2016-06-20). "A Look Inside China's Chart-Topping New Supercomputer". The Next Platform. Retrieved 2016-06-20.
5.  Dongarra, Jack (June 20, 2016). "Report on the Sunway TaihuLight System" (PDF). www.netlib.org. Retrieved June 20, 2016.
6.  Lendino, Jamie (20 June 2016). "Meet the new world’s fastest supercomputer: China’s TaihuLight". Extremetech. Retrieved 21 June 2016. The TOP500 report said that the chip also lacks any traditional L1-L2-L3 cache, and instead has 12KB of instruction cache and 64KB “local scratchpad” that works sort of like an L1 cache.
7.  "Top 500 The List: November 2016". TOP 500. 14 November 2016. Retrieved 26 November 2016.