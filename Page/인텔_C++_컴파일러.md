> This article is converted from Wikipedia: [ C++ ](https://ko.wikipedia.org/wiki/_C++_).


**인텔 C++ 컴파일러**(Intel C++ Compiler, 간단히 icc 또는 icl)는 [인텔](../Page/인텔.md "wikilink")이 [GNU/리눅스](../Page/리눅스.md "wikilink"), [맥 OS X](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink"), [마이크로소프트 윈도를](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 대상으로 제공하는 [C와](../Page/C_\(프로그래밍_언어\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") [컴파일러](../Page/컴파일러.md "wikilink")의 모음이다.

인텔은 [IA-32](../Page/IA-32.md "wikilink"), [인텔 64](https://ko.wikipedia.org/wiki/x86-64#인텔_64 "wikilink") 프로세서, 그리고 AMD 프로세서와 같은 특정 비 인텔 호환 프로세서의 컴파일을 지원한다. 개발자들은 시스템 요구 사항을 확인할 필요가 있다. IA-32 및 인텔 64용 인텔 C++ 컴파일러는 [SSE](../Page/스트리밍_SIMD_확장.md "wikilink"), [SSE2](../Page/SSE2.md "wikilink"), [SSE3](../Page/SSE3.md "wikilink"), [SSSE3](../Page/SSSE3.md "wikilink"), [SSE4](../Page/SSE4.md "wikilink"), [AVX](../Page/고급_벡터_확장.md "wikilink") [SIMD](https://ko.wikipedia.org/wiki/SIMD "wikilink") 명령어([인텔 MMX 및 MMX2의](../Page/MMX.md "wikilink") [임베디드](../Page/임베디드_시스템.md "wikilink") 변종)를 만들어내는 자동 벡터라이저의 기능을 갖추고 있다.\[1\]

나아가, 인텔 C++ 컴파일러는 [대칭형 다중 처리에](https://ko.wikipedia.org/wiki/대칭형_다중_처리 "wikilink") 대한 [오픈MP](https://ko.wikipedia.org/wiki/오픈MP "wikilink") 3.1과 [자동 병렬화를](https://ko.wikipedia.org/wiki/자동_병렬화 "wikilink") 지원한다. [클러스터 오픈MP](http://software.intel.com/en-us/whatif/)의 추가 기능과 더불어 이 컴파일러는 오픈MP 지향 [분산 메모리](https://ko.wikipedia.org/wiki/분산_메모리 "wikilink") [다중 처리용](https://ko.wikipedia.org/wiki/다중_처리 "wikilink") [메시지 전달 인터페이스](https://ko.wikipedia.org/wiki/메시지_전달_인터페이스 "wikilink") 호출을 자동으로 만들어낼 수 있다.

인텔 C++ 컴파일러는 [에디슨 디자인 그룹](https://ko.wikipedia.org/wiki/에디슨_디자인_그룹 "wikilink") 프론트엔드([SGI](../Page/실리콘_그래픽스.md "wikilink") [MIPSpro](https://ko.wikipedia.org/wiki/오픈64 "wikilink"), [코모 C++](https://ko.wikipedia.org/wiki/코모_C++ "wikilink"), [더 포틀랜드 그룹](https://ko.wikipedia.org/wiki/더_포틀랜드_그룹 "wikilink") 따위)를 포함한 컴파일러 계열에 속한다. 이 컴파일러는 또한 [IA-32](../Page/IA-32.md "wikilink"), [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink"), [아이테니엄 2](../Page/아이테니엄.md "wikilink") 아키텍처의 [SPEC CPU](https://ko.wikipedia.org/wiki/퍼포먼스_이벨루에이션_코퍼레이션 "wikilink") 벤치마크에 널리 쓰이는 것으로도 알려져 있다.

인텔 C++ 컴파일러는 [인텔 패러럴 스튜디오](https://ko.wikipedia.org/wiki/인텔_패러럴_스튜디오 "wikilink"), 인텔 페러럴 스튜디오 XE, 인텔 C++ 컴포저 패키지, 인텔 C++ 컴포저 XE 패키지, 인텔 컴포저 XE 패키지, 인텔 클러스터 스튜디오를 포함한 인텔의 다양한 패키지를 통해 이용할 수 있다. [인텔 소프트웨어 제품](http://www.intel.com/software/products) 사이트에서 더 많은 정보가 제공된다.

## 언어

인텔 컴파일러 제품군에는 [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [포트란](../Page/포트란.md "wikilink")을 위한 프론트엔드가 제공된다.

[GCC](../Page/GNU_컴파일러_모음.md "wikilink") 3.x 이전에 나온 초기 버전의 리눅스용 ICC는 GCC 2.x보다 C++ 표준을 더 잘 준수할 목적으로 [Dinkumware](https://ko.wikipedia.org/wiki/Dinkumware "wikilink") [네임 맹글링을](https://ko.wikipedia.org/wiki/네임_맹글링 "wikilink") 이용한다. 이로 말미암아 [ABI가](../Page/응용_프로그램_이진_인터페이스.md "wikilink") 두 GCC 버전 모두와 호환되지 않게 되었다. 인텔은 2007년 6월 10.0판에서 Dinkumware 라이브러리를 제거하였다. 그 뒤로 이 컴파일러는 GCC 3.2 이후와 호환성을 유지하고 있다.

## 아키텍처

  - [IA-32](../Page/IA-32.md "wikilink")
  - [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") ([인텔 64](https://ko.wikipedia.org/wiki/인텔_64 "wikilink") 및 [AMD64](https://ko.wikipedia.org/wiki/AMD64 "wikilink"))

## 버전

  - 인텔 C++ 컴포저 XE 2013 (컴파일러 13) - 2012년 9월 5일
  - 인텔 C++ 컴포저 XE 2011 업데이트 6 이상 (컴파일러 12.1) - 2011년 9월 8일 출시
  - 인텔 C++ 컴포저 XE 2011 최대 업데이트 5까지 (컴파일러 12.0) - 2010년 11월 7일 출시
  - 인텔 C++ 컴파일러 11.1 - 2009년 6월 23일 출시
  - 인텔 C++ 컴파일러 11.0 - 2008년 11월 출시
  - 인텔 C++ 컴파일러 10.1 - 2007년 11월 7일 출시
  - 인텔 C++ 컴파일러 10.0 - 2007년 6월 5일 출시
  - 인텔 C++ 컴파일러 9.0 - 2005년 6월 14일 출시
  - 인텔 C++ 컴파일러 8.1 - 2004년 9월 출시
  - 인텔 C++ 컴파일러 8.0 - 2003년 12월 15일 출시
  - 인텔 C++ 컴파일러 7.1 - 2003년 3월 출시
  - 인텔 C++ 컴파일러 7.0 - 2002년 11월 25일 출시
  - 인텔 C++ 컴파일러 6.0 - 2002년 4월 24일 출시

## 실험 / 프로토타입 버전

  - [Intel STM Compiler Prototype Edition](http://software.intel.com/en-us/whatif/) - 2007년 9월 17일 출시\[2\]
  - [Intel Concurrent Collections for C/C++ 0.3](http://software.intel.com/en-us/articles/intel-concurrent-collections-for-cc/) - 2008년 9월 출시

## 플래그

최적화 플래그는 다음과 같다. ([인텔 소프트웨어 기술 문서 사이트](http://software.intel.com/en-us/articles/intel-software-technical-documentation/))

| 윈도           | 리눅스 및 맥 OS X | 설명                                                                                                                                                                                              |
| ------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `/Od`        | `-O0`        | 최적화 안 함                                                                                                                                                                                         |
| `/O1`        | `-O1`        | 크기 최적화                                                                                                                                                                                          |
| `/O2`        | `-O2`        | 속도 최적화 및 일부 최적화 사용                                                                                                                                                                              |
| `/O3`        | `-O3`        | O2의 최적화 모든 사용, 철저한 루프 최적화                                                                                                                                                                       |
| `/QxO`       | `-xO`        | 비 인텔 CPU를 위한 SSE3, SSE2, SSE 명령어 집합 최적화 사용.\[3\]                                                                                                                                                |
| `/fast`      | `-fast`      | 빠른 사용. [윈도의](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 경우 "`/O3 /Qipo /QxHost /no-prec-div`"와 동일. [리눅스](../Page/리눅스.md "wikilink")의 경우 "`-O3 -ipo -static -xHOST -no-prec-div`"와 동일. |
| `/Qprof-gen` | `-prof_gen`  | 프로파일 생성하여 프로그램 컴파일.                                                                                                                                                                             |
| `/Qprof-use` | `-prof_use`  | `prof_gen`를 사용하여 컴파일한 프로그램을 실행한 뒤에만 사용할 수 있음. 컴파일 각 단계 동안 프로파일 정보 사용.                                                                                                                           |

## 각주

<references />

## 외부 링크

  - [인텔 컴파일러](http://www.intel.com/cd/software/products/asmo-na/eng/compilers/284132.htm)

  - [비상업 목적의 인텔 컴파일러 무료 다운로드](http://software.intel.com/en-us/articles/non-commercial-software-download/)

[분류:C++ 컴파일러](https://ko.wikipedia.org/wiki/분류:C++_컴파일러 "wikilink") [분류:C 컴파일러](https://ko.wikipedia.org/wiki/분류:C_컴파일러 "wikilink") [분류:인텔 제품](https://ko.wikipedia.org/wiki/분류:인텔_제품 "wikilink") [분류:인텔 소프트웨어](https://ko.wikipedia.org/wiki/분류:인텔_소프트웨어 "wikilink")

1.  A. J. C. Bik, *The Software Vectorization Handbook* (Intel Press, Hillsboro, OR, 2004), .
2.  [PRESS KIT - Intel Developer Forum](http://www.intel.com/pressroom/kits/events/idffall%5F2007)
3.  <http://www.intel.com/software/products/compilers/docs/cwin/release_notes.htm>