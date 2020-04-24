> This article is converted from Wikipedia: [ECC 메모리](https://ko.wikipedia.org/wiki/ECC_메모리).


[300px은](https://ko.wikipedia.org/wiki/파일:Micron_PC2700_DDR_ECC_REG.JPG "wikilink") 일반적으로 각 면에 9개의 메모리 칩이 있으며 보통 각 측면에 여덟 개의 메모리 칩이 있는 비 ECC DIMM보다 각 측면에 한 개 더 많은 메모리 칩이 있는 것이다.(일부 모듈은 5개 또는 18개가 있을 수 있다)\[1\]\]\]

**오류 정정 코드 메모리**(), 즉 **ECC 메모리**()는 가장 일반적인 종류의 내부 [데이터 손상을](https://ko.wikipedia.org/wiki/데이터_손상 "wikilink") 감지하고 수정하는 [기억 장치의](../Page/기억_장치.md "wikilink") 일종이다. ECC 메모리는 [계산과학](../Page/계산과학.md "wikilink"), 금융 컴퓨팅 등 모든 상황에서 데이터 손상에 대처해야 하는 대부분의 컴퓨터에 사용된다.

일반적으로 ECC 메모리는 싱글 비트 오류에 메모리 시스템이 면역되도록 관리한다. 각 [워드로부터](../Page/워드_\(컴퓨팅\).md "wikilink") 읽은 데이터는 무조건 기록되는 데이터와 동일해야 하는데, 이는 실제로 저장되는 하나 이상의 비트가 잘못된 상태로 플립(flip) 되더라도 마찬가지이다.\[2\] 대부분의 비 ECC 메모리는 오류를 감지할 수 없으며, 패리티(parity)를 지원하는 일부 비 ECC 메모리는 오류를 감지할 수는 있으나 정정 기능은 없다.

## 문제 배경

[DRAM의](../Page/동적_램.md "wikilink") 단일 비트가 컴퓨터 시스템 내부의 전기적 또는 자기적 간섭으로 인해 자연스럽게 반대 상태로 바뀔 수 있는데, 처음에는 주로 칩 포장재의 오염물질에 의해 방출되는 [알파 입자](../Page/알파_입자.md "wikilink") 때문이라고 생각되었으나, 연구를 통해 [DRAM](../Page/동적_램.md "wikilink") 칩의 일회성 소프트 에러의 대부분은 주로 2차 [우주선의](../Page/우주선_\(물리\).md "wikilink") [중성자](../Page/중성자.md "wikilink")에 의한 배경 방사능의 결과로 발생하며, 이는 하나 이상의 메모리 셀의 내용을 변경하거나 읽기 또는 쓰기에 사용되는 회로를 방해할 수 있다는 것을 밝혀냈다.\[3\] 이러한 이유로 오류율은 고도가 증가할수록 급격히 증가하는데, 예를 들어 해수면 대비 중성자 선속은 1.5 km에서 3.5배, 10–12 km (상용 항공기의 순항 고도)에서 300배 더 빠르다.\[4\] 결과적으로, 높은 고도에서 작동하는 시스템은 신뢰성을 위해 특별한 규정이 필요하다.

이러한 예로, 1997년 발사된 우주선 *[카시니-하위헌스](https://ko.wikipedia.org/wiki/카시니-하위헌스 "wikilink")*가 있다. *[카시니-하위헌스](https://ko.wikipedia.org/wiki/카시니-하위헌스 "wikilink")*는 두 개의 동일한 비행 기록기에 각각 상용 [DRAM](../Page/동적_램.md "wikilink") 칩 배열의 형태로 2.5 [Gbit의](../Page/기가비트.md "wikilink") 메모리를 탑재했으며, [EDAC가](../Page/오류_검출_정정.md "wikilink") 내장되어 있어, *[카시니-하위헌스](https://ko.wikipedia.org/wiki/카시니-하위헌스 "wikilink")*의 엔지니어링 텔레메트리(telemetry)는 싱글 비트 워드 오류 (수정 가능) 수와 듀얼 비트 워드 오류 (수정 불가능) 수를 보고했다. 처음 2년 6개월간 비행하는 동안, *[카시니-하위헌스](https://ko.wikipedia.org/wiki/카시니-하위헌스 "wikilink")*는 하루에 약 280개의 오류를 보고했으며, 거의 일정한 싱글 비트 오류율을 보였다. 그러나 1997년 11월 6일, 우주에서의 첫 달 동안, 오류의 수는 하루에 4배 이상 증가했는데, 증가의 원인은 인공위성 *GOES 9*에 의해 탐지된 태양 입자 방출 (solar particle event) 이었다.\[5\]

## 레지스터드 메모리

## 각주

## 외부 링크

  - [SoftECC: A System for Software Memory Integrity Checking](http://pdos.csail.mit.edu/papers/softecc:ddopson-meng/softecc_ddopson-meng.pdf)
  - [A Tunable, Software-based DRAM Error Detection and Correction Library for HPC](http://www.fiala.me/pubs/papers/libsdc11.pdf)
  - [Detection and Correction of Silent Data Corruption for Large-Scale High-Performance Computing](http://www.fiala.me/pubs/papers/sc12-redmpi.pdf)
  - [Single-Bit Errors: A Memory Module Supplier’s perspective on cause, impact and detection](http://www.smartm.com/files/salesLiterature/dram/smart_whitepaper_sbe.pdf)
  - [Intel Xeon Processor E3 - 1200 Product Family Memory Configuration Guide](https://web.archive.org/web/20131228061309/http://cache-www.intel.com/cd/00/00/46/78/467819_467819.pdf)

[분류:컴퓨터 메모리](https://ko.wikipedia.org/wiki/분류:컴퓨터_메모리 "wikilink")

1.
2.  "[A survey of techniques for improving error-resilience of DRAM](https://dx.doi.org/10.1016/j.sysarc.2018.09.004)", JSA, 2018
3.  [Single Event Upset at Ground Level, Eugene Normand, Member, IEEE, Boeing Defense & Space Group, Seattle, WA 98124-2499](https://web.archive.org/web/20131021190327/http://pdf.yuri.se/files/art/2.pdf)
4.  "[A Survey of Techniques for Modeling and Improving Reliability of Computing Systems](https://dx.doi.org/10.1109/TPDS.2015.2426179)", IEEE TPDS, 2015
5.  [Gary M. Swift and Steven M. Guertin. "In-Flight Observations of Multiple-Bit Upset in DRAMs". Jet Propulsion Laboratory](https://trs.jpl.nasa.gov/bitstream/handle/2014/15831/00-1594.pdf?sequence=1)