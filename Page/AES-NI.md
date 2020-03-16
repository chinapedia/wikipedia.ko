> This article is converted from Wikipedia: [AES-NI](https://ko.wikipedia.org/wiki/AES-NI).


**AES-NI** ()는 인텔이 2008년 3월에 제안한 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 명령어 집합의 확장으로서 [AES를](https://ko.wikipedia.org/wiki/고급_암호_표준 "wikilink") 사용하는 암호화와 복호화의 수행 성능을 향상시키기 위한 명령어 집합이다\[1\]. [인텔](../Page/인텔.md "wikilink") [웨스트미어](https://ko.wikipedia.org/wiki/웨스트미어 "wikilink") 프로세서부터 처음으로 지원하기 시작했으며 7개의 명령어로 이루어져 있다.

## 새 명령어

| 명령어             | 설명                           |
| --------------- | ---------------------------- |
| AESENC          | AES 암호화 라운드 수행               |
| AESENCLAST      | AES 암호화의 마지막 라운드 수행          |
| AESDEC          | AES 복호화 라운드 수행               |
| AESDECLAST      | AES 복호화의 마지막 라운드 수행          |
| AESKEYGENASSIST | AES 라운드 키 생성                 |
| AESIMC          | AES Inverse Mix Column 연산 수행 |
| PCLMULQDQ       | 캐리 없는 곱셈(CLMUL)\[2\]         |

## AES-NI를 지원하는 CPU

  - [인텔](../Page/인텔.md "wikilink")\[3\]
      - 인텔 [웨스트미어](https://ko.wikipedia.org/wiki/네할렘_\(마이크로아키텍처\)#웨스트미어 "wikilink") 기반 프로세서 중 일부
          - 웨스트미어-EP(제온 5600 시리즈)
          - 클락데일(코어 i3, 펜티엄, 셀러론 제외)
          - 애런데일(코어 i5-4xxM, 코어 i3, 펜티엄, 셀러론 제외)
      - 인텔 [샌디브리지](https://ko.wikipedia.org/wiki/샌디_브리지_마이크로아키텍처 "wikilink") 기반 프로세서
          - 데스크톱: 코어 i5, 코어 i7, 제온\[4\]\[5\]
          - 모바일: 코어 i5, 코어 i7. 일부 노트북 제조사들은 바이오스 설정에서 AES-NI를 비활성화시켜 두었고 이후 업데이트로 활성화시켰다.\[6\]\[7\]
      - 인텔 [아이비브리지](../Page/아이비브리지_\(마이크로아키텍처\).md "wikilink") 기반 프로세서
          - 모든 코어 i5, 코어 i7, 제온, i3-2115C\[8\]
      - 인텔 [하스웰](../Page/하스웰_\(마이크로아키텍처\).md "wikilink") 기반 프로세서
          - 코어 i3-4000M, 펜티엄, 셀러론 제외 모든 프로세서\[9\]
      - 인텔 [브로드웰](../Page/브로드웰_\(마이크로아키텍처\).md "wikilink") 기반 프로세서
          - 펜티엄 3xxxU, 셀러론 3xxxU 제외 모든 프로세서
      - 인텔 [스카이레이크](../Page/스카이레이크_\(마이크로아키텍처\).md "wikilink") 기반 프로세서
          - 펜티엄 3xxxU, 셀러론 3xxxU 제외 모든 프로세서
  - [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")
      - AMD 불도저 기반 프로세서\[10\]
      - AMD 파일드라이버 기반 프로세서
      - AMD 스팀롤러 기반 프로세서
      - AMD 재규어 기반 프로세서
      - AMD 퓨마 기반 프로세서

## 성능

*AES-NI Performance Analyzed*에서, Patrick Schmid 와 Achim Roos 는 "... 인텔의 AES-NI를 이용하여 최적화한 몇개의 애플리케이션에서 놀랄만한 결과를 얻었다”라고 한다.\[11\]

## 지원 소프트웨어

AES-NI 발표 이후 출시된 컴파일러 및 소프트웨어에서 해당 명령어를 지원하며, 다음 주요 구성 요소에서도 지원한다.

  - 마이크로소프트 Cryptography API: Next Generation (CNG)\[12\]
  - [리눅스 커널 암호화 API](../Page/크립토_API_\(리눅스\).md "wikilink")
  - [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 7 HotSpot
  - NSS 3.13 이상(파이어폭스와 크롬에서 사용함)\[13\]
  - 솔라리스 10 이상의 암호화 프레임워크\[14\]
  - [FreeBSD](../Page/FreeBSD.md "wikilink") OpenCrypto API(aesni(4) 드라이버)\[15\]
  - [OpenSSL](../Page/OpenSSL.md "wikilink") 1.0.1 이상\[16\]

## 같이 보기

  - [고급 암호 표준](https://ko.wikipedia.org/wiki/고급_암호_표준 "wikilink")
  - [SSE](https://ko.wikipedia.org/wiki/SSE "wikilink")
  - [SSE2](../Page/SSE2.md "wikilink")
  - [SSE3](../Page/SSE3.md "wikilink")
  - [SSE4](../Page/SSE4.md "wikilink")
  - [AVX](../Page/고급_벡터_확장.md "wikilink")
  - [X86](../Page/X86.md "wikilink")

## 각주

  - AES-NI 백서 <http://software.intel.com/file/20457> 4.4 Mbyte, pdf

[분류:X86 아키텍처](https://ko.wikipedia.org/wiki/분류:X86_아키텍처 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink") [분류:고급 암호화 표준](https://ko.wikipedia.org/wiki/분류:고급_암호화_표준 "wikilink")

1.
2.  [Intel website - Carry-Less Multiplication](http://software.intel.com/en-us/articles/intel-carry-less-multiplication-instruction-and-its-usage-for-computing-the-gcm-mode/)
3.  [ARK: Advanced Search](http://ark.intel.com/search/advanced/?AESTech=true)
4.  [AnandTech - The Sandy Bridge Review: Intel Core i7-2600K, i5-2500K and Core i3-2100 Tested](http://www.anandtech.com/show/4083/the-sandy-bridge-review-intel-core-i5-2600k-i5-2500k-and-core-i3-2100-tested/2)
5.  [Compare Intel® Products](http://ark.intel.com/compare/53415,63913,58667,53480,53481,53482,53483,53484,53485,53490,53491,53492,53416,53414)
6.  [AES-NI support in TrueCrypt (Sandy Bridge problem)](http://forum.notebookreview.com/windows-os-software/582628-aes-ni-support-truecrypt-sandy-bridge-problem.html)
7.
8.  \[<http://ark.intel.com/products/68332/Intel-Core-i3-2115C-Processor-(3MB-Cache-2_00-GHz)> \]
9.  <http://ark.intel.com/products/75104/Intel-Core-i3-4000M-Processor-3M-Cache-2_40-GHz>
10.
11.
12.
13.
14.
15.
16.