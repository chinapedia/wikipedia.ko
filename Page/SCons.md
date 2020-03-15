> This article is converted from Wikipedia: [SCons](https://ko.wikipedia.org/wiki/SCons).


**SCons**는 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") 소프트웨어 빌드 도구이다. SCons는 [autoconf](https://ko.wikipedia.org/wiki/autoconf "wikilink")/[automake](https://ko.wikipedia.org/wiki/automake "wikilink")의 기능과 [ccache](https://ko.wikipedia.org/wiki/ccache "wikilink")와 같은 컴파일러 캐시를 통합한, 고전적인 [Make](https://ko.wikipedia.org/wiki/make_\(소프트웨어\) "wikilink") 유틸리티의 대체품이다. 이전의 도구들과 비교하여, SCons는 더 쓰기 쉽고, 더 신뢰할 수 있고, 더 빠른 것을 목표로 한다.

## 주요 기능

  - 설정 파일이 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 스크립트이다: 사용자가 작성한 빌드 스크립트에 완전한 범용 프로그래밍 언어의 기능을 사용할 수 있다.
  - [C](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")과 [포트란](https://ko.wikipedia.org/wiki/포트란 "wikilink")에 대해, 자동 [종속성](https://ko.wikipedia.org/wiki/종속성_\(컴퓨터_과학\) "wikilink") 분석(Automatic dependency analysis)이 내장되어 있다.
      - make와 달리, 종속성을 획득하기 위한 "`make depend`"나 "`make clean`"\[1\]과 같은 별도의 명령어는 필요하지 않다. 종속성 분석(Dependency analysis)은 다른 언어나 파일 종류를 위한 사용자 정의 종속성 스캐너를 통해 쉽게 확장할 수 있다.
      - [autotools와](../Page/GNU_빌드_시스템.md "wikilink") 달리, [gcc의](https://ko.wikipedia.org/wiki/GNU_컴파일러_모음 "wikilink") 내장 종속성 분석을 사용하지 않는다. 그 대신, "`#include`"에 대한 [regexp](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 스캔을 모든 C/C++ 소스 파일에 행한다. gcc 기반 빌드에서는, 종속성 생성이 더 느려질 수 있고(추가적인 스캔이 언제나 필요하므로). 신뢰성이 더 낮아질 수 있다(`-DSOMETHING`와 같은 전처리기 플래그 같은 것이 무시된다는 의미에서). 그러나 이것은 비-gcc 컴파일러에 호환성이 더 좋은 방식이다.
  - [C](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [D](https://ko.wikipedia.org/wiki/D_프로그래밍_언어 "wikilink"), [Java](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink"), [Fortran](https://ko.wikipedia.org/wiki/포트란 "wikilink"), [Objective-C](https://ko.wikipedia.org/wiki/Objective-C "wikilink"), [Yacc](https://ko.wikipedia.org/wiki/Yacc "wikilink"), [Lex](https://ko.wikipedia.org/wiki/Lex_프로그래밍_언어 "wikilink"), [Qt과](https://ko.wikipedia.org/wiki/Qt_\(툴킷\) "wikilink") [SWIG](../Page/SWIG.md "wikilink")와 [TeX](https://ko.wikipedia.org/wiki/TeX "wikilink") 및 [LaTeX](https://ko.wikipedia.org/wiki/LaTeX "wikilink") 문서 빌드를 기본 지원한다. 다른 언어나 파일 종류는 사용자 정의 빌더(Builder)를 통해 지원할 수 있다.
  - 소스 코드 및 빌드 전 대상(pre-built targets)에 대한 중심 저장소(central repositories)에서의 빌드를 지원한다.
  - [SCCS](https://ko.wikipedia.org/wiki/SCCS "wikilink"), [RCS](https://ko.wikipedia.org/wiki/RCS "wikilink")(Revision Control System), [CVS](https://ko.wikipedia.org/wiki/CVS "wikilink")(Concurrent Versions System), [서브버전](https://ko.wikipedia.org/wiki/서브버전 "wikilink"), [비트키퍼](https://ko.wikipedia.org/wiki/비트키퍼 "wikilink")와 [퍼포스](https://ko.wikipedia.org/wiki/퍼포스 "wikilink")(Perforce)에서 소스를 가져오는 것을 기본 지원한다.
  - .dsp, .dsw, .sln와 .vcproj 파일의 생성을 포함한 [마이크로소프트 비주얼 스튜디오 .NET와](https://ko.wikipedia.org/wiki/마이크로소프트_비주얼_스튜디오 "wikilink") 이전의 비주얼 스튜디오 버전을 기본 지원한다.
  - 파일 내용 변화 감지에 [MD5](../Page/MD5.md "wikilink") 시그너처를 사용한다: 옵션 설정으로, 전통적인 타임스탬프(timestamps) 방식도 지원한다.
  - 디렉터리 체계와 관계없이 지정한 작업들(jobs)의 수를 유지하는 병렬 빌드를 지원한다.
  - `#include` 파일과 라이브러리, 함수와 `typedef`들을 탐색하는 통합된 [Autoconf](https://ko.wikipedia.org/wiki/Autoconf "wikilink")와 유사한 기능을 지원한다.
  - 모든 종속성을 전역적으로 조망한다: 복수의 빌드 패스나 타겟 순서 재지정이 필요하지 않다.
  - 다중 빌드를 가속하기 위한 캐시 파일을 공유하는 능력이 있다: [ccache](https://ko.wikipedia.org/wiki/ccache "wikilink")와 유사하지만 C/C++ 컴파일 뿐만 아니라, 다른 모든 파일 종류를 지원한다.
  - 크로스 플랫폼 빌드(cross-platform builds)를 위해 처음부터 차례로 끝까지 다시 설계했다: [Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), 다른 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 호환 운영 체제([AIX](https://ko.wikipedia.org/wiki/AIX_\(운영_체제\) "wikilink"), [\*BSD systems](https://ko.wikipedia.org/wiki/BSD/OS "wikilink"), [HP-UX](../Page/HP-UX.md "wikilink"), [IRIX](../Page/IRIX.md "wikilink") 와 [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink"), [Mac OS X](https://ko.wikipedia.org/wiki/Mac_OS_X "wikilink")), [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 와 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")를 지원한다.

## 가장 단순한 SConstruct 파일

``` python
 Program('main.c')
```

사용자가 '`scons`' 명령을 실행하면, scons는 'main' 실행 파일 ([Unix](https://ko.wikipedia.org/wiki/Unix "wikilink") 호환 OS에서) 또는 'main.exe' 실행 파일 ([윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 에서)을 빌드한다.

## 역사

SCons는 2000년 8월의 SC\[2\] Build competition에서의 최우수상을 받은 'ScCons'라는 빌드 도구 설계에서 시작했다. 이 설계는 [Cons](https://archive.is/20000815211359/http://www.dsmit.com/cons/) 라는 빌드 도구에 기반한 것이었다.

## 주요 응용 프로젝트 목록

  - [Aqsis (3D 그래픽스)](https://ko.wikipedia.org/wiki/:en:Aqsis "wikilink")
  - [Ardour (audio processor)](https://ko.wikipedia.org/wiki/:en:Ardour_\(audio_processor\) "wikilink")
  - [배틀필드 1942](https://ko.wikipedia.org/wiki/:en:Battlefield_1942 "wikilink")
  - [블렌더 (3D 그래픽스)](../Page/블렌더_\(소프트웨어\).md "wikilink")
  - [Delta3D (게임 엔진)](https://ko.wikipedia.org/wiki/:en:Delta3D "wikilink")
  - [id Software](https://ko.wikipedia.org/wiki/이드_소프트웨어 "wikilink")
  - [Nullsoft Scriptable Install System](https://ko.wikipedia.org/wiki/:en:Nullsoft_Scriptable_Install_System "wikilink")
  - [SuperCollider (Audio programming language and environment)](https://ko.wikipedia.org/wiki/:en:SuperCollider "wikilink")
  - [VMware](https://ko.wikipedia.org/wiki/VMware "wikilink")
  - [Csound5](https://ko.wikipedia.org/wiki/:en:Csound5 "wikilink")

## 각주

<references />

## 외부 링크

  - [SCons 홈페이지](http://www.scons.org/)
  - [Make Alternatives](https://web.archive.org/web/20080513113324/http://freshmeat.net/articles/view/1715/)
  - [Stop the autoconf insanity\! Why we need a new build system.](https://web.archive.org/web/20080511200201/http://freshmeat.net/articles/view/889/)

[분류:컴파일 도구](https://ko.wikipedia.org/wiki/분류:컴파일_도구 "wikilink") [분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink") [분류:파이썬 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬_소프트웨어 "wikilink") [분류:파이썬으로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬으로_작성된_자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink")

1.  대부분의 경우, "`depend`"와 "`clean`" 타겟은 사용자가 작성하거나 [autotools](https://ko.wikipedia.org/wiki/autotools "wikilink")에 의해 생성되어야 한다. Make는 단지 이 타겟들을 실행하는 도구일 뿐이다.
2.