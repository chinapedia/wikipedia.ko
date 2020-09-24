> This article is converted from Wikipedia: [RISC-V](https://ko.wikipedia.org/wiki/RISC-V).


[섬네일](https://ko.wikipedia.org/wiki/파일:Yunsup_Lee_holding_RISC_V_prototype_chip.jpg "wikilink")

**RISC-V**("리스크 파이브"로 발음)는 [축소 명령어 집합 컴퓨터](../Page/축소_명령어_집합_컴퓨터.md "wikilink")(RISC) 기반의 [개방형](../Page/개방형_표준.md "wikilink") [명령어 집합](../Page/명령어_집합.md "wikilink")(ISA)이다.

대부분의 ISA와 달리 RISC-V ISA는 어떠한 목적으로는 자유로이 사용할 수 있으며, 누구든지 RISC-V [칩과](../Page/집적_회로.md "wikilink") [소프트웨어](../Page/소프트웨어.md "wikilink")를 [설계](../Page/집적_회로_설계.md "wikilink"), 제조, 판매할 수 있게 허가되어 있다. 최초의 개방형 ISA는 아니지만 웨어하우스 규모의 [클라우드 컴퓨터](../Page/클라우드_컴퓨팅.md "wikilink"), 고성능 [휴대 전화](../Page/휴대_전화.md "wikilink"), 초소형 [임베디드 시스템에](../Page/임베디드_시스템.md "wikilink") 이르는 현대의 산술 장치에 유용하게 쓰일 수 있게 설계되어 있다. 이러한 이용에 근거하여 설계자들은 성능과 전력 효율성을 둘 다 고려하였다. 명령어 집합은 또한 지원 소프트웨어의 실질적인 부분을 포함하고 있어서 새로운 명령어 집합의 일반적인 약점을 보완한다.

이 프로젝트는 [캘리포니아 대학교 버클리에서](../Page/캘리포니아_대학교_버클리.md "wikilink") 2010년에 시작되었으나 수많은 기여자들은 자발적인 봉사자들이자 대학 밖의 산업 노동자들이다.\[1\]

RISC-V ISA는 실생활의 소형, 고속, 저전력 구현체를 염두에 두고 설계되었으나,\[2\]\[3\] 특정 [마이크로아키텍처](../Page/마이크로아키텍처.md "wikilink") 스타일을 따르지는 않았다.\[4\]\[5\]\[6\]\[7\]

2017년 5월 기준으로 버전 2.2의 유저스페이스 ISA가 픽스되어 있으며 privileged ISA는 초안판 1.10으로 이용이 가능하다.\[8\]

## 중요성

RISC-V의 개발자들은 [BSD 허가서](../Page/BSD_허가서.md "wikilink") 하에서 자유롭게 사용할 수 있는 여러 CPU 디자인을 제공하는 것을 목표로 하였다. 이러한 라이선스들은 RISC-V 칩 디자인과 같은 파생작들이 RISC-V 그 자체와 비슷하게 오픈·자유를 따르거나, 클로즈드·사유를 따를 수 있게 하고 있다.

이와 반대로, [ARM 홀딩스와](../Page/ARM_홀딩스.md "wikilink") [MIPS 테크놀로지스와](https://ko.wikipedia.org/wiki/MIPS_테크놀로지스 "wikilink") 같은 상업적인 칩 벤더들은 자신들의 [특허](../Page/특허.md "wikilink") 사용에 대한 상당한 라이선스 비용을 부과한다.\[9\] 이들은 또한 설계적 장점과 명령어 집합을 기술하는 문서를 출시하기 전에 비공개 계약(NDA)을 요구한다. 수많은 설계적 개선사항들이 완전히 사유이며, 심지어는 고객을 대상으로 설명하지 않는다. 이러한 기밀은 공공의 교육적인 이용, 보안 감사, 공공의 낮은 비용의 [자유-오픈 소스 소프트웨어](../Page/자유-오픈_소스_소프트웨어.md "wikilink") [컴파일러](../Page/컴파일러.md "wikilink"), [운영 체제의](../Page/운영_체제.md "wikilink") 개발을 막아버린다.

CPU를 개발하는 것은 여러 전문분야의 설계적 전문 지식이 필요하다: 전자 논리, 컴파일러, 운영 체제. 전문 엔지니어링 팀 밖에서는 이러한 정보를 찾기가 어렵다. 그 결과로 현대의 고품질의 범용 목적의 컴퓨터 명령어 집합들이 최근까지도 학술적 환경을 제외하고는 어디에서도 사용할 수도 없고 설명되지도 않았다. 이러한 이유로 수많은 RISC-V 기여자들은 이를 통합된 공동체의 노고로 간주한다. 수많은 기여자들의 이러한 요구는 RISC-V가 수많은 용도에 맞게 엔지니어링된 이유 중 하나이다.

RISC-V 개발자들은 또한 실리콘과 시뮬레이션의 설계를 검증하는 것에서 실질적인 연구 및 사용자 경험을 갖추고 있다. RISC-V ISA는 일련의 학술적 컴퓨터 설계 프로젝트의 직접적인 개발품이다. 부분적으로는 이러한 프로젝트들을 지원하기 위해 시작되었다.\[10\]\[11\]

## 역사

### 선구자

"RISC"라는 용어는 약 1980년으로 거슬러 올라간다.\[12\] 이 이전에 더 단순한 컴퓨터가 더 효율적이라는 이야기는 있었지만 설계적 원칙은 널리 설명되지 않은 상태였다. 단순한 효율적인 컴퓨터는 늘 학술적 관심의 대상이 되고 있다.

여러 학교들에서 1990년에 Computer Architecture: A Quantitative Approach의 제1판을 위해 RISC 명령어 집합 [DLX](https://ko.wikipedia.org/wiki/DLX "wikilink")를 개발하였다. [데이비드 패터슨이](../Page/데이비드_패터슨.md "wikilink") 저자였으며 나중에 RISC-V를 지원하였다. 그러나 DLX는 교육용이었다. 학교와 호비스트들은 [FPGA](../Page/FPGA.md "wikilink")를 사용하여 이를 구현하였으나 상업적인 성공을 이루지는 못했다.

버전 2 이하의 ARM CPU들은 퍼블릭 도메인의 명령어 집합을 갖추었으며 인기있는 자유 소프트웨어 컴파일러의 하나인 [GCC에](../Page/GNU_컴파일러_모음.md "wikilink") 의해 지금도 지원된다. 이로써 ARM 아키텍처의 수용을 가속화시켰다. 3개의 오픈 소스 코어가 이 ISA를 위해 존재하지만 제조된 적은 없다.\[13\]\[14\]

[OpenRISC](https://ko.wikipedia.org/wiki/OpenRISC "wikilink")는 DLX 기반의 오픈 소스 ISA이며, RISC 디자인을 따른다. GCC와 [리눅스](../Page/리눅스.md "wikilink") 구현체를 완전히 지원한다. 그러나 일부 상용 구현체가 존재한다.

### 재단

버클리의 캘리포니아 대학교 Krste Asanović는 오픈 소스 컴퓨터 시스템의 여러가지 이용을 발견하였다. 2010년에 그는 여름 동안 짧은 3개월 프로젝트에서 개발 및 출판을 결심하였다. 이러한 계획은 학술 부문과 산업 부문의사용자들을 둘 다 지원하기 위한 것이다.\[15\] 버클리의 [데이비드 패터슨은](../Page/데이비드_패터슨.md "wikilink") 또한 이 노고를 도왔다. 패터슨은 처음에 [버클리 RISC의](https://ko.wikipedia.org/wiki/버클리_RISC "wikilink") 속성들을 식별하였으며,\[16\] RISC-V는 기나긴 일련의 협업 RISC 연구 프로젝트들 가운데 하나이다. 초기 자금 제공은 [DARPA](https://ko.wikipedia.org/wiki/DARPA "wikilink")에 의해 이루어졌다.\[17\]

RISC-V 재단을 지원하는 단체들로는 이를테면 다음과 같다: [구글](../Page/구글.md "wikilink"), [마이크로소프트](../Page/마이크로소프트.md "wikilink"), [엔비디아](../Page/엔비디아.md "wikilink"), [오라클](../Page/오라클_\(기업\).md "wikilink"), [퀄컴](../Page/퀄컴.md "wikilink"), [IBM](../Page/IBM.md "wikilink"), [화웨이](../Page/화웨이.md "wikilink"), [휴렛 팩커드 엔터프라이즈](../Page/휴렛_팩커드_엔터프라이즈.md "wikilink") (HPE), [인도 공과대학교 마드라스](https://ko.wikipedia.org/wiki/인도_공과대학교_마드라스 "wikilink"), [어드밴스트 마이크로 디바이시스](../Page/어드밴스트_마이크로_디바이시스.md "wikilink"), [BAE 시스템스](https://ko.wikipedia.org/wiki/BAE_시스템스 "wikilink"), [Berkeley Architecture Research](http://bar.eecs.berkeley.edu/), [Bluespec, Inc.](https://ko.wikipedia.org/wiki/Bluespec,_Inc. "wikilink"), [Cortus](https://ko.wikipedia.org/wiki/Cortus "wikilink"), [Draper](https://ko.wikipedia.org/wiki/Charles_Stark_Draper_Laboratory "wikilink"), [ICT](https://ko.wikipedia.org/wiki/중국과학원 "wikilink"), [래티스 세미컨덕터](../Page/래티스_세미컨덕터.md "wikilink"), [Mellanox Technologies](https://ko.wikipedia.org/wiki/Mellanox_Technologies "wikilink"), [Microsemi](https://ko.wikipedia.org/wiki/Microsemi "wikilink"), [마이크론](../Page/마이크론_테크놀로지.md "wikilink"), [NXP반도체](../Page/NXP반도체.md "wikilink"), [Rambus Cryptography Research](https://ko.wikipedia.org/wiki/Cryptography_Research "wikilink"), [웨스턴 디지털](../Page/웨스턴_디지털.md "wikilink").\[18\]\[19\]

### 수상

  - 2017: [The Linley Group's Analyst's Choice Award for Best Technology](http://linleygroup.com/press_detail.php?The-Linley-Group-Announces-Winners-of-Annual-Analysts-Choice-Awards-85) (명령어 집합에 대해)

## 설계

### 명령어 하위 집합

RISC-V 명령어 중 최소한의 필수적인 집합은 정수 명령어 집합이다. (문자 "I"로 표시) 이 집합은 자체적으로 범용 컴파일러를 포함하여 완전한 소프트웨어 지원과 더불어 단순화된 범용 컴퓨터를 구현할 수 있다.\[20\]

컴퓨터 설계는 추가적인 하위 집합을 추가할 수 있다: 정수 곱하기 및 나누기 (집합 "M"), [실시간](https://ko.wikipedia.org/wiki/실시간_시스템 "wikilink") 동시성 처리를 위한 원자적 명령어 ( "A"), 배정밀도("D")와 4배 정밀도("Q") 옵션이 있는 IEEE [부동소수점](../Page/부동소수점.md "wikilink") ("F").\[21\] "privileged" 명령어 집합은 [유닉스](../Page/유닉스.md "wikilink") 계열 [운영 체제의](../Page/운영_체제.md "wikilink") 지원을 위한 명령어들을 정의한다. [가상화](../Page/가상화.md "wikilink") 지원을 위해 [하이퍼바이저](../Page/하이퍼바이저.md "wikilink")를 지원할 예정이다.\[22\] 이러한 명령어 집합 "RVIMAFD"을 갖춘 컴퓨터를 "범용"(general-purpose)이라 부르며 간단히 "G"로 축약한다.\[23\]

코드 크기(집합 "C")를 줄이는 선택적인 "compact" 하위 집합이 있다. 수많은 RISC-V 컴퓨터들은 이 ISA를 추가하여 전력, 코드 크기, 메모리를 줄일 수 있다.\[24\] 16개의 레지스터만 지원하여 가장 작은 CPU들에 대한 비용을 줄이는 32비트 임베디드 하위 집합("E")도 있다.\[25\]

이러한 집합들은 32비트, 64비트와 같은 레지스터의 크기에 따라 추가적으로 기술된다. 각기 다른 레지스터 크기에 대한 각각의 하위 집합의 차이는 크지 않다.

[임베디드 시스템용](../Page/임베디드_시스템.md "wikilink") 소형 32비트 컴퓨터는 "RV32EC"일 수 있다. 대형 64비트 컴퓨터는 "RV64G"일 수 있다.\[26\]

하위 집합은 128비트 컴퓨터, 비트 조작("B"), 10진 [부동소수점](../Page/부동소수점.md "wikilink")("L"), Packed [SIMD](../Page/SIMD.md "wikilink")(예: budget multimedia, "P"), 벡터 처리("V"), 트랜잭셔널 메모리("T")도 계획되어 있다.\[27\]

## 같이 보기

  - [OpenRISC](https://ko.wikipedia.org/wiki/OpenRISC "wikilink"): [GNU 일반 공중 사용 허가서로](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 라이선스됨.
  - [축소 명령어 집합 컴퓨터](../Page/축소_명령어_집합_컴퓨터.md "wikilink")
  - [오픈 소스 컴퓨팅 하드웨어](https://ko.wikipedia.org/wiki/오픈_소스_컴퓨팅_하드웨어 "wikilink")

## 각주

## 추가 문헌

  - [The RISC-V Instruction Set Manual](http://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-118.pdf)
  - [Instruction Sets Should Be Free: The Case For RISC-V](http://www.eecs.berkeley.edu/Pubs/TechRpts/2014/EECS-2014-146.html) Whitepaper by Krste Asanović and [David A. Patterson](https://ko.wikipedia.org/wiki/:en:David_Patterson_\(computer_scientist\) "wikilink")
  - [The RISC-V Instruction Set](http://www.hotchips.org/wp-content/uploads/hc_archives/hc25/HC25-posters/HC25.26.p70-RISC-V-Warterman-UCB.pdf) HotChips 25 (2013)
  - [The RISC-V Software Ecosystem](http://riscv.org/wp-content/uploads/2015/02/riscv-software-toolchain-tutorial-hpca2015.pdf) HPCA 2015, Tutorial
  - [Rocket Chip](http://riscv.org/wp-content/uploads/2015/02/riscv-rocket-chip-generator-tutorial-hpca2015.pdf) HPCA 2015, Tutorial
  - [The RISC-V Compressed Instruction Set Manual Version 1.9 (draft)](https://riscv.org/wp-content/uploads/2015/11/riscv-compressed-spec-v1.9.pdf)

## 외부 링크

  -
  -
  -
  - [Pulpino](https://web.archive.org/web/20170824094526/http://www.pulp-platform.org/): A developed, open-source system-on-chip based on RISC-V, 4 August 2016

  -
  -
  -
  -
[분류:2010년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2010년_소프트웨어 "wikilink") [분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink") [분류:명령어 집합 구조](https://ko.wikipedia.org/wiki/분류:명령어_집합_구조 "wikilink")

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
12.
13.
14.
15.
16.
17.
18.
19. <https://riscv.org/membership/1424/rambus-cryptography-research/>
20.
21.
22.
23.
24.
25.
26.
27.