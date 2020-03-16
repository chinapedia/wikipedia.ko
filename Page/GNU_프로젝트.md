> This article is converted from Wikipedia: [GNU ](https://ko.wikipedia.org/wiki/GNU_).


[오른쪽](https://ko.wikipedia.org/wiki/파일:Heckert_GNU_white.svg "wikilink") **GNU 프로젝트**(GNU project)는 [1983년](../Page/1983년.md "wikilink") [9월 27일](../Page/9월_27일.md "wikilink") [유즈넷](../Page/유즈넷.md "wikilink") net.unix-wizard 그룹을 통해 일반에 알려졌다. 스톨만은 첫 선언문에 이은 "GNU 선언문"을 비롯한 여러 글들을 통해서, "초기 전산 공동체에 지배적이었던, 협동 정신을 되돌리자"라고 주장했다. GNU 프로젝트는 누구나 자유롭게 "실행, 복사, 수정, 배포"할 수 있고, 누구도 그런 권리를 제한하면 안 된다는 사용 허가권(License) 아래 [소프트웨어](../Page/소프트웨어.md "wikilink")를 배포한다. [카피레프트](../Page/카피레프트.md "wikilink")로 불리는 이런 생각은 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")(GNU 일반 공중 사용 허가서)에 나타나 있다.\[1\]

GNU는 "GNU는 유닉스가 아니다."란 의미를 갖는 영어 문장 "GNU's Not UNIX"의 약자로, 원래의 문장 안에 자신이 이미 들어 있는 [재귀 약자이다](../Page/재귀_약자.md "wikilink"). 스톨만은 GNU를 *그누*로 읽자고 제안한다. [유닉스](../Page/유닉스.md "wikilink")는 이미 널리 쓰이던 [독점 소프트웨어](https://ko.wikipedia.org/wiki/독점_소프트웨어 "wikilink") 운영 체제로, 유닉스의 아키텍처는 기술적으로 믿을만 한 것으로 증명되어 있어, GNU 시스템은 유닉스와 호환될 수 있도록 만들어졌다. 유닉스 아키텍처는 개별적인 요소들이 따로 따로 작성되는 것을 허용한다. 또, 이미 공개되어 있던 조판 소프트웨어 [TeX](../Page/TeX.md "wikilink")나 [X 윈도도](https://ko.wikipedia.org/wiki/X_윈도 "wikilink") 쓸 수 있는 장점이 있었다.

[1985년](../Page/1985년.md "wikilink")에 스톨만은 GNU 프로젝트를 철학적, 법률적, 금융적으로 지원하기 위해 [자선단체](https://ko.wikipedia.org/wiki/자선단체 "wikilink")인 [자유 소프트웨어 재단](../Page/자유_소프트웨어_재단.md "wikilink")(FSF, Free Software Foundation)을 세웠다. 이 재단은 GNU를 개발할 프로그래머들도 고용했다. 그러나, 프로젝트의 대부분은 자원 봉사자들이 개발했으며, 앞으로도 그럴 것이다. GNU가 눈길을 끎에 따라, 이를 주목한 회사들은 GNU 소프트웨어의 개발이나 판매 및 기술 지원을 돕기 시작했다. 이 가운데 가장 두드러지고 성공적인 것은 (현재는 [레드햇](../Page/레드햇.md "wikilink")의 일부인) Cygnus Solutions이다.\[2\]

[1990년](../Page/1990년.md "wikilink")까지 GNU 시스템엔 확장 가능한 [문서 편집기](../Page/문서_편집기.md "wikilink")([이맥스](../Page/이맥스.md "wikilink")), 뛰어난 최적화 [컴파일러](../Page/컴파일러.md "wikilink")([GCC](../Page/GNU_컴파일러_모음.md "wikilink")), 그리고 표준 유닉스 배포판의 핵심 [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")와 [유틸리티가](https://ko.wikipedia.org/wiki/유틸리티_소프트웨어 "wikilink") 있었다. 하지만, 여기엔 주요 구성요소인 [커널이](../Page/커널_\(컴퓨팅\).md "wikilink") 빠져 있었다.

[GNU 선언문에서](../Page/GNU_선언문.md "wikilink"), 스톨만은 "기본적인 커널은 있지만 유닉스를 흉내내려면 아직 더 많은 기능이 필요하다"라고 했다. 여기서 그가 지칭한 것은 MIT에서 개발하여 자유롭게 배포했고, 유닉스 7번째 판과 호환되는 트릭스(TRIX)라는 [원격 프로시저 호출](../Page/원격_프로시저_호출.md "wikilink") 커널이었다. [1986년](../Page/1986년.md "wikilink") 12월, 이 커널을 고치는 작업이 시작됐다. 하지만, 개발자들은 결국 트릭스(TRIX)를 기반으로 새 커널을 만드는 것은 어렵다는 결론을 내렸다. 주된 이유는 트릭스(TRIX)는 "애매하고(잘 안 쓰이고?) 비싼 68000 box"에서만 동작했고, 따라서 그 상자에서 쓰이기 전에 다른 구조로 [포팅해야](../Page/이식_\(컴퓨팅\).md "wikilink") 했기 때문이다. [1988년](../Page/1988년.md "wikilink") 즈음에, [카네기멜론 대학교에서](https://ko.wikipedia.org/wiki/카네기멜론_대학교 "wikilink") 개발되던 마하 통신-전송 커널(Mach message-passing kernel)을 그 대체품으로 고려했지만, 이것은 처음에 이것을 개발한 사람들이 AT\&T 소유의 코드를 지우면서 지연되었다. 처음엔, 이 커널은 앨릭스(Alix)라고 불렸지만, 나중에 개발자 마이클 부시넬(Michael Bushnell)는 [HURD라는](../Page/GNU_허드.md "wikilink") 이름을 선호하여, 앨릭스(Alix)란 이름은 하부 구조로 옮겨지고 마침내 완전히 떨어졌다. 결국은, [HURD의](../Page/GNU_허드.md "wikilink") 개발은 기술적이고 개인적인 충돌로 지지부진해지고 말았다.

[1991년](../Page/1991년.md "wikilink")에 [리누스 토르발스는](../Page/리누스_토르발스.md "wikilink") 유닉스 호환의 [리눅스](../Page/리눅스.md "wikilink") 커널을 작성하여 GPL 라이선스 아래에 배포했다. 다른 여러 프로그래머들은 인터넷을 통해 리눅스를 더욱 발전시켰다. [1992년](../Page/1992년.md "wikilink") 리눅스는 GNU 시스템과 통합되었고, 이로써 완전한 공개 운영 체제가 탄생되었다. GNU 시스템들 가운데 가장 흔한 것이, "[GNU/리눅스](https://ko.wikipedia.org/wiki/GNU/리눅스 "wikilink")" 또는 "[리눅스 배포판](../Page/리눅스_배포판.md "wikilink")"이라고 불리는 바로 이 시스템이다. ([2016년](../Page/2016년.md "wikilink") 기준으로, 허드(HURD)는 여전히 개발 중이며, 리눅스를 대신하여 허드를 사용한 GNU 시스템을 비공식 실험판으로 사용할 수 있다.\[3\])

또한, 비공개 유닉스 시스템에도 GNU의 구성 요소들이 본래의 유닉스 프로그램을 대신하여 들어 있는 경우도 많다. 이는 GNU 프로젝트를 통해 쓰여진 프로그램들이 질적으로 우수하다는 사실을 증명한다. 종종, 이런 구성 요소들은 "GNU 툴"로 불리기도 한다. 다수의 GNU 프로그램은 [마이크로소프트 윈도나](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [맥 OS X](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink") 등으로 포팅되기도 했다.

## GNU 소프트웨어

다음은 GNU 프로젝트를 통해 개발한 소프트웨어들이다.

  - [Bison](../Page/GNU_bison.md "wikilink"), [yacc](https://ko.wikipedia.org/wiki/yacc "wikilink")을 대체하려고 만든 [파서 발생기](https://ko.wikipedia.org/wiki/컴파일러-컴파일러 "wikilink")
  - [Bash](https://ko.wikipedia.org/wiki/Bash "wikilink"), 셸.
  - [Binutils](https://ko.wikipedia.org/wiki/GNU_Bytinutils "wikilink"), [어셈블러](https://ko.wikipedia.org/wiki/어셈블러 "wikilink")와 [링커](https://ko.wikipedia.org/wiki/링커 "wikilink")를 포함.
  - [이맥스](../Page/이맥스.md "wikilink") (Emacs), 다양한 기능의 문서 편집기.
  - [GCC](../Page/GNU_컴파일러_모음.md "wikilink"), C를 비롯한 다양한 프로그래밍 언어를 위한 컴파일러
  - [GDB](https://ko.wikipedia.org/wiki/GDB "wikilink"), 디버깅 프로그램.
  - [김프](../Page/김프.md "wikilink"), 그림 편집기.
  - [glibc](https://ko.wikipedia.org/wiki/glibc "wikilink"), C 라이브러리.
  - [GMP](../Page/GMP_\(라이브러리\).md "wikilink"), 수치 계산 라이브러리.
  - [그놈](../Page/그놈.md "wikilink"), 그래픽 데스크톱 환경.
  - [GNU 빌드 시스템](../Page/GNU_빌드_시스템.md "wikilink") - [Autoconf](../Page/Autoconf.md "wikilink"), [Automake](../Page/Automake.md "wikilink"), [Libtool](https://ko.wikipedia.org/wiki/Libtool "wikilink")
  - [GNUStep](https://ko.wikipedia.org/wiki/GNUStep "wikilink") - [오픈스텝](../Page/오픈스텝.md "wikilink") 표준의 추가 (그래픽 응용 소프트웨어를 위한 라이브러리 및 개발 도구 집합)
  - GSL, GNU 과학 라이브러리.
  - [GZip](https://ko.wikipedia.org/wiki/GZip "wikilink"), [데이터 압축을](../Page/데이터_압축.md "wikilink") 위한 라이브러리와 프로그램
  - [HURD](https://ko.wikipedia.org/wiki/HURD "wikilink"), 유닉스 커널과 같은 기능을 수행하는 [마이크로커널](../Page/마이크로커널.md "wikilink")과 서버들의 모임
  - [Maxima](https://ko.wikipedia.org/wiki/Maxima "wikilink"), [컴퓨터 대수학 체계](https://ko.wikipedia.org/wiki/컴퓨터_대수학_체계 "wikilink").
  - [Octave](../Page/GNU_옥타브.md "wikilink"), [MATLAB](../Page/MATLAB.md "wikilink")과 비슷한 수치 계산기.
  - [GNU MDK](https://ko.wikipedia.org/wiki/GNU_MDK "wikilink"), [MIX](https://ko.wikipedia.org/wiki/MIX "wikilink") 안에서 프로그램을 짜기 위한 개발 키트.
  - [GNU 라디오](../Page/GNU_라디오.md "wikilink"), 범용 하드웨어를 이용한 소프트웨어 무선 통신 신호 처리 패키지
  - [오픈오피스 (Open Office)](../Page/오픈오피스.md "wikilink"), GNU 오피스

GNU 프로젝트는 다른 곳에서 개발된 패키지로 배포하고 도와 주기도 한다.

## 함께 보기

  - [GNU](../Page/GNU.md "wikilink")
  - [GNU 선언문](../Page/GNU_선언문.md "wikilink")
  - [오픈 소스](../Page/오픈_소스.md "wikilink")
  - [자유소프트웨어](https://ko.wikipedia.org/wiki/자유소프트웨어 "wikilink")

## 각주

## 외부 링크

  -
  - [GNU 자유 소프트웨어 디렉터리](http://directory.fsf.org/wiki/GNU)

[GNU_프로젝트](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트 "wikilink") [분류:자유 소프트웨어 재단](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_재단 "wikilink")

1.  <http://www.gnu.org/gnu/manifesto.ko.html>
2.  <https://www.gnu.org/home.ko.html>
3.