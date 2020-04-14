> This article is converted from Wikipedia: [IDA 프로](https://ko.wikipedia.org/wiki/IDA_프로).


**IDA**(Interactive DisAssembler)는 컴퓨터 소프트웨어 용 [디스어셈블러](https://ko.wikipedia.org/wiki/디스어셈블러 "wikilink")이다. 디스어셈블러는 기계어 코드로부터 [어셈블리어](../Page/어셈블리어.md "wikilink") [소스 코드를](../Page/소스_코드.md "wikilink") 생성한다. 이것은 다양한 [실행 파일과](../Page/실행_파일.md "wikilink") [중앙 처리 장치](../Page/중앙_처리_장치.md "wikilink") 그리고 [운영 체제를](../Page/운영_체제.md "wikilink") 지원한다. 또한 Windows PE, [Mac OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") Mach-O, 그리고 [리눅스](../Page/리눅스.md "wikilink") ELF 실행 파일에 대해서는 [디버거](../Page/디버거.md "wikilink")로 사용할 수 있다. [C](../Page/C_\(프로그래밍_언어\).md "wikilink")/<span class="nowrap">[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")</span><span class="nowrap"></span> [컴파일러](../Page/컴파일러.md "wikilink")로 컴파일된 프로그램은 [디컴파일러](https://ko.wikipedia.org/wiki/디컴파일러 "wikilink") 플러그인은 추가 요금을 통해 사용할 수 있다. 최신 버전의 IDA Pro는 상업용이지만, 기능이 조금 부족한 옛날 버전은 무료로 다운로드할 수 있다(2015년 12월의 경우 버전 5.0).

<div>

\[1\]

</div>

IDA는 코드 섹션들 사이의 상호 참조와 API 호출 시의 파라미터, 그리고 다른 정보를 통해 자동 코드 분석을 수행한다. 디스어셈블의 특성상 정확한 분석이 어렵고, 사람의 많은 도움을 필요로 하지만 IDA는 디스어셈블을 향상시키기 위한 대화형 기능을 가지고 있다. 보편적인 IDA 사용자는 자동으로 생성된 디스어셈블 목록과 함께 시작하게 되며 코드에서 데이터로 또는 데이터에서 코드로 섹션을 바꾸고, 리네이밍, 주석 달기, 정보 추가 등을 할 수 있다.

Ilfak Guilfanov에 의해 [셰어웨어](../Page/셰어웨어.md "wikilink")로 개발된 IDA는 나중에 벨기에 회사인 DataRescue에 의해 상용 제품으로 팔리게 된다. 이 회사는 제품을 개선시키고 IDA Pro라는 이름으로 판매한다. 2005년에는 Guilfanov가 Hex-Rays 디컴파일러 IDA extention을 위해 Hex-Rays를 만들고, 2008년 1월에는 Hex-Rays가 DataRescue의 IDA Pro에 대한 개발과 지원을 맡게 된다.\[2\]

## 스크립팅

"IDC 스크립트"는 디스어셈블러의 기능을 확장할 수 있게 만들어 준다. 유저의 스크립트 작성을 위한 기준으로 몇몇 도움이 되는 스크립트들이 제공된다. 대부분의 빈번한 스크립트들은 생성된 코드의 추가적인 변경을 위해 사용된다. 예를 들면 외부 기호 테이블(external symbol table)들은 원본 소스 코드의 함수 이름을 사용함으로써 로드될 수 있다. IDA 스크립트와 발생한 문제들에 대한 지원을 위한 웹사이트가 있다.

사용자들은 IDC에 추가하거나 대신할 수 있는 용도로 사용되는 다른 스크립트 언어들을 통해 플러그인들을 개발하였다. [IdaRUB](https://github.com/spoonm/idarub) 는 [루비를](../Page/루비_\(프로그래밍_언어\).md "wikilink"), [IDAPython](https://web.archive.org/web/20150506023607/http://d-dome.net/idapython)은 [파이썬](../Page/파이썬.md "wikilink")을 지원한다.

## 지원되는 시스템/프로세서/컴파일러

  - 시스템 호스트
    \* [윈도우](../Page/마이크로소프트_윈도우.md "wikilink") x86와 ARM
      - 리눅스 x86

      - x86
  - 인식되는 실행 파일 포맷
      - COFF와 여기서 파생된 Win32/64/generic [PE 포맷](../Page/PE_포맷.md "wikilink")
      - ELF와 여기서 파생된 것들
      - Mach-O ([Mach](../Page/Mach_\(커널\).md "wikilink"))
      - NLM ([넷웨어](../Page/넷웨어.md "wikilink"))
      - [LC/LE/LX](../Page/EXE.md "wikilink") (OS/2 3.x와 다양한 도스 익스텐더들)
      - NE (OS/2 2.x, Win16와 다양한 도스 익스텐더들)
      - [MZ](../Page/MZ_실행_파일.md "wikilink") ([MS-DOS](../Page/MS-DOS.md "wikilink"))
      - OMF와 여기서 파생된 것들
      - AIM (포괄적으로)
      - ROM 이미지나 [COM 파일](../Page/COM_파일.md "wikilink") 같은 바이너리
  - 명령어 집합
    \* [인텔](../Page/인텔.md "wikilink") 80x86 Family
      - [ARM 아키텍처](../Page/ARM_아키텍처.md "wikilink")
      - Motorola 68k와 H8
      - [자일로그 Z80](../Page/자일로그_Z80.md "wikilink")
      - [MOS 6502](../Page/MOS_6502.md "wikilink")
      - [인텔 i860](../Page/인텔_i860.md "wikilink")
      - [DEC Alpha (알파 프로세서)](https://ko.wikipedia.org/wiki/알파_프로세서 "wikilink")
      - [아날로그 디바이스](../Page/아날로그_디바이스.md "wikilink") ADSP218x
      - Angstrem KR1878
      - Atmel AVR 시리즈
      - DEC 시리즈 PDP11
      - 후지쯔 F2MC16L/F2MC16LX
      - 후지쯔 FR 32-bit Family
      - 히타치 SH3/SH3B/SH4/SH4B
      - 히타치 H8: h8300/h8300a/h8s300/h8500
      - 인텔 196 시리즈: 80196/80196NP
      - 인텔 51 시리즈: 8051/80251b/80251s/80930b/80930s
      - 인텔 i960 시리즈
      - 인텔 Itanium (ia64) 시리즈
      - 자바 가상 머신
      - MIPS: mipsb/mipsl/mipsr/mipsrl/r5900b/r5900l
      - 마이크로칩 PIC: PIC12Cxx/PIC16Cxx/PIC18Cxx
      - [MSIL (공통 중간 언어)](../Page/공통_중간_언어.md "wikilink")
      - 미쓰비시 7700 Family: m7700/m7750
      - 미쓰비시 m32/m32rx
      - 미쓰비시 m740
      - 미쓰비시 m7900
      - 모토롤라 DSP 5600x Family: dsp561xx/dsp5663xx/dsp566xx/dsp56k
      - 모토롤라 ColdFire
      - 모토롤라 HCS12
      - NEC 78K0/78K0S
      - PA-RISC
      - 파워PC
      - 제논 파워PC Family
      - SGS-Thomson ST20/ST20c4/ST7
      - [SPARC](../Page/SPARC.md "wikilink") Family
      - 삼성 SAM8
      - 지멘스 C166 시리즈
      - TMS320Cxxx 시리즈
  - 컴파일러/라이브러리 (자동으로 라이브러리 함수를 인식하기 위해)\[3\]
      - 도스/윈도우용 볼랜드 C++ 5.x
      - 볼랜드 C++ 3.1
      - 도스/윈도우용 볼랜드 C 빌더 v4
      - Cygwin용 GNU C++
      - [비주얼 C++](https://ko.wikipedia.org/wiki/비주얼_C++ "wikilink")
      - 마이크로소프트 QuickC
      - 마이크로소프트 Visual C++
      - 도스/OS2용 Watcom C++ (16/32 bit)
      - ARM C v1.2
      - 유닉스용 GNU C++

## 디버깅

IDA Pro는 아래를 포함한 다양한 디버거들을 지원한다.\[4\]

  - 원격으로 윈도우, 리눅스 그리고 맥 응용 프로그램들을 자신의 원래 환경에서 디버깅 할 수 있게 한다. (주로 악성코드 디버깅을 위해 사용한다.)
  - [GNU 디버거](../Page/GNU_디버거.md "wikilink") (gdb)는 네이티브 윈도우 디버거처럼 리눅스와 OS X를 지원한다.
  - [Bochs](../Page/Bochs.md "wikilink") 플러그인은 간단한 응용 프로그램 디버깅을 위해 제공된다. (즉, 손상된 [UPX](../Page/UPX.md "wikilink") 또는 mpress로 압축된 실행파일들)
  - 인텔 PIN 디버거
  - 기록 다시보기

## 각주

## 외부 링크

  -

  -

[분류:디버거](https://ko.wikipedia.org/wiki/분류:디버거 "wikilink") [분류:역어셈블러](https://ko.wikipedia.org/wiki/분류:역어셈블러 "wikilink")

1.  [IDA Pro 5.0 Freeware version download](http://www.hex-rays.com/idapro/idadownfreeware.htm)
2.
3.
4.