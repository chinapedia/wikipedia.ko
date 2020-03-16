> This article is converted from Wikipedia: [LLVM](https://ko.wikipedia.org/wiki/LLVM).


**LLVM**(이전 이름: Low Level Virtual Machine)은 [컴파일러](../Page/컴파일러.md "wikilink")의 기반구조이다. 프로그램을 컴파일 타임, 링크 타임, [런타임](../Page/런타임.md "wikilink") 상황에서 프로그램의 작성 언어에 상관없이 최적화를 쉽게 구현할 수 있도록 구성되어 있다.\[1\]

LLVM은 원래는 저급 [가상 기계](https://ko.wikipedia.org/wiki/가상_기계 "wikilink")(low-level virtual machine)의 약자를 가리켰지만, LLVM이 성장하고 다양한 목적을 가지게 되면서 현재는 그 이름을 약자로서 사용하는 것이 아니라 그냥 프로젝트의 이름으로서 사용하고 있다.\[2\]

LLVM의 핵심 코드는 'LLVM 라이선스'로 배포되며, 이것은 [BSD 라이선스와](https://ko.wikipedia.org/wiki/BSD_라이선스 "wikilink") 비슷한 속성을 가진다.\[3\] 즉, LLVM을 사용한 프로그램을 배포하였을 때 해당 소스 코드를 공개/배포해야 하는 의무가 없다. 단 LLVM의 프론트엔드를 [GNU 컴파일러 모음](../Page/GNU_컴파일러_모음.md "wikilink")(GCC) 기반으로 사용할 경우 프론트엔드는 [GPL로](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 배포한다. LLVM 프로젝트에서는 LLVM 라이선스를 가지는 프론트엔드를 위해, [Clang](https://ko.wikipedia.org/wiki/Clang "wikilink")이라는 프로젝트를 진행하고 있다.

## 역사

LLVM 프로젝트는 2000년에 [일리노이 대학교 어배너-섐페인에서](../Page/일리노이_대학교_어배너-섐페인.md "wikilink") [Vikram Adve와](https://ko.wikipedia.org/wiki/Vikram_Adve "wikilink") [크리스 라트너의](../Page/크리스_라트너.md "wikilink") 감독 아래에 시작되었다.

## 개요

LLVM으로 언어에 가상 기계를 생성, 가상 기계가 언어에 독립적인 최적화를 실행한다. LLVM은 언어와 구조로부터 독립적이며, 언어 모듈과 시스템을 위한 코드 생성 부의 사이에 위치한다. LLVM은 컴파일 과정 동안 최적화와 함께 [JIT을](../Page/JIT_컴파일.md "wikilink") 정적 컴파일러로 사용, 개발의 각종 단계에서 사용할 수 있는 많은 부분을 가지고 있다.\[4\] LLVM은 전통적인 GCC 시스템에서 그랬듯이 코드를 정적으로 컴파일할 수도 있고, [Java처럼](../Page/자바_\(프로그래밍_언어\).md "wikilink") [JIT를](../Page/JIT_컴파일.md "wikilink") 이용하여 [기계어](../Page/기계어.md "wikilink")(machine code)로 한 번 더 컴파일되는 중간 형식으로 코드를 컴파일할 수도 있다. 이말은 자바처럼 플랫폼에 독립적이란 뜻은 아니다.

JIT 컴파일러의 경우 런타임에 불필요한 정적 분기를 최적화하는 기능이 있는데, 이 기능은 다양한 런타임 옵션을 제공하면서 특정 환경에서는 사용되지 않는 옵션을 쉽게 식별할 수 있는 프로그램의 경우에 부분 평가([partial evaluation](https://ko.wikipedia.org/wiki/partial_evaluation "wikilink"))를 하는데 유용하다. [Mac OS X v10.5에서는](https://ko.wikipedia.org/wiki/맥_오에스_텐_v10.5 "wikilink") 이를 사용하여 하드웨어에서 지원하지 않는 [OpenGL](../Page/OpenGL.md "wikilink") 파이프라인을 제공하고 있다.\[5\]

현재 [GNU 컴파일러 모음](../Page/GNU_컴파일러_모음.md "wikilink")(GCC) 3.4와 4.0.1에서 빼낸 프런트 엔드를 사용하는 C 언어와 C++ 컴파일러를 지원하고 있다.

## 코드 표현

LLVM은 언어에서 독립적인 명령어 집합과 형식 시스템을 갖추고 있다. 명령의 대부분은 [3-어드레스 코드](../Page/3-어드레스_코드.md "wikilink") 형식과 유사하다. 각 명령은 또한 [정적 단일 대입 형식이며](https://ko.wikipedia.org/wiki/정적_단일_대입_형식 "wikilink"), 변수(로 입력된 레지스터)는 한 번 지정되면 그 다음은 변경되지 않는다. 따라서 변수간의 의존관계의 분석을 단순하게 할 수 있다.

변환은 어떤 형식이라도 명시적으로 형변환 명령을 통해 실행된다. LLVM의 기본 형식은 다수의 고정 길이의 정수이고, 파생 형식으로 포인터, 배열, 벡터, 구조체, 함수의 5가지가 존재한다. 구체적인 언어에서의 형식은 LLVM에서 지원하는 형식들을 결합하여 표현한다. 예를 들면, C++의 클래스는 구조체와 함수와 함수에 대한 포인터의 배열을 함께 사용하여 표현된다.

## 구성 요소

LLVM은 여러 구성 요소를 포함하는 산하 프로젝트가 되었다.

### 프론트엔드: 프로그래밍 언어 지원

LLVM은 원래 GCC 스택의 기존 [코드 발생기를](https://ko.wikipedia.org/wiki/코드_발생 "wikilink") 대체할 목적으로 작성되었으며\[6\], GCC 프론트엔드 중 다수가 이것과 함께 동작하도록 수정되어왔다. LLVM은 현재 다양한 [프론트엔드](https://ko.wikipedia.org/wiki/프론트엔드 "wikilink")를 사용하여 [에이다](https://ko.wikipedia.org/wiki/에이다 "wikilink"), [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [D](../Page/D_\(프로그래밍_언어\).md "wikilink"), [델파이](../Page/델파이.md "wikilink"), [포트란](../Page/포트란.md "wikilink"), [하스켈](../Page/하스켈.md "wikilink"), [오브젝티브-C](../Page/오브젝티브-C.md "wikilink"), [스위프트](https://ko.wikipedia.org/wiki/스위프트 "wikilink")의 컴파일을 지원하고 있으며, 일부는 [GNU 컴파일러 모음](../Page/GNU_컴파일러_모음.md "wikilink")(GCC)의 4.0.1 및 4.2에서 가져온 것이다.

#### 표준 라이브러리 지원

LLVM은 자신만의 표준 라이브러리를 지원하지만, [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink") [musl](https://ko.wikipedia.org/wiki/musl "wikilink")(ARM을 초기에 지원하는 3.9 기준)의 대안이기도 하다.\[7\]

### LLVM 중간 표현

LLVM의 핵심은 [중간 표현](https://ko.wikipedia.org/wiki/중간_표현 "wikilink")(IR)으로, 어셈블리어와 비슷한 저급 프로그래밍 언어이다.

``` llvm
@.str = internal constant [14 x i8] c"hello, world\0A\00"

declare i32 @printf(i8*, ...)

define i32 @main(i32 %argc, i8** %argv) nounwind {
entry:
    %tmp1 = getelementptr [14 x i8]* @.str, i32 0, i32 0
    %tmp2 = call i32 (i8*, ...)* @printf( i8* %tmp1 ) nounwind
    ret i32 0
}
```

\[8\]

### 백엔드: 명령어 집합 및 마이크로아키텍처 지원

버전 3.4를 기준으로, LLVM은 [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink"), [퀄컴 헥사곤](https://ko.wikipedia.org/wiki/퀄컴_헥사곤 "wikilink"), [MIPS](https://ko.wikipedia.org/wiki/MIPS "wikilink"), [엔비디아](../Page/엔비디아.md "wikilink") [병렬 스레드 실행](https://ko.wikipedia.org/wiki/병렬_스레드_실행 "wikilink")(PTX), [파워PC](../Page/파워PC.md "wikilink"), [AMD 테라스케일](https://ko.wikipedia.org/wiki/AMD_테라스케일 "wikilink")\[9\], AMD [그래픽스 코어 넥스트](../Page/그래픽스_코어_넥스트.md "wikilink")(GCN), [SPARC](../Page/SPARC.md "wikilink"), [z/아키텍처](https://ko.wikipedia.org/wiki/z/아키텍처 "wikilink"), [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")/[x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink"), [XCore](https://ko.wikipedia.org/wiki/XCore "wikilink")를 포함하여 수많은 [명령어 집합을](../Page/명령어_집합.md "wikilink") 지원한다. 일부 기능들은 일부 플랫폼에서 사용하지 못한다. 대부분의 기능들이 x86/x86-64, z/아키텍처, ARM, 파워PC에 존재한다.\[10\]

## 버전 역사

버전 역사는 다음과 같다.\[11\]

| 버전    | 출시일        |
| ----- | ---------- |
| 9.0.0 | 2019-09-19 |
| 8.0.0 | 2019-03-20 |
| 7.0.0 | 2018-09-19 |
| 6.0.1 | 2018-07-05 |
| 5.0.2 | 2018-05-16 |
| 6.0.0 | 2018-03-08 |
| 5.0.1 | 2017-12-21 |
| 5.0.0 | 2017-09-07 |
| 4.0.1 | 2017-07-04 |
| 4.0.0 | 2017-03-13 |
| 3.9.1 | 2016-12-23 |
| 3.9.0 | 2016-09-02 |
| 3.8.1 | 2016-07-11 |
| 3.8.0 | 2016-03-08 |
| 3.7.1 | 2016-01-05 |
| 3.7.0 | 2015-09-01 |
| 3.6.2 | 2015-07-16 |
| 3.6.1 | 2015-05-26 |
| 3.6.0 | 2015-02-27 |
| 3.5.2 | 2015-04-02 |
| 3.5.1 | 2015-01-20 |
| 3.5.0 | 2014-09-03 |
| 3.4.2 | 2014-06-19 |
| 3.4.1 | 2014-05-07 |
| 3.4.0 | 2014-01-02 |
| 3.3   | 2013-06-17 |
| 3.2   | 2012-12-20 |
| 3.1   | 2012-05-22 |
| 3.0   | 2011-12-01 |
| 2.9   | 2011-04-06 |
| 2.8   | 2010-10-05 |
| 2.7   | 2010-04-27 |
| 2.6   | 2009-10-23 |
| 2.5   | 2009-03-02 |
| 2.4   | 2008-11-09 |
| 2.3   | 2008-06-09 |
| 2.2   | 2008-02-11 |
| 2.1   | 2007-09-26 |
| 2.0   | 2007-05-23 |
| 1.9   | 2006-11-19 |
| 1.8   | 2006-08-09 |
| 1.7   | 2006-04-20 |
| 1.6   | 2005-11-08 |
| 1.5   | 2005-05-18 |
| 1.4   | 2004-12-09 |
| 1.3   | 2004-08-13 |
| 1.2   | 2004-03-19 |
| 1.1   | 2003-12-17 |
| 1.0   | 2003-10-24 |

버전 역사

## 각주

<references />

## 외부 링크

  -

  - [LLVM 프로젝트 블로그](http://blog.llvm.org/)

[분류:컴파일러](https://ko.wikipedia.org/wiki/분류:컴파일러 "wikilink") [분류:C++](https://ko.wikipedia.org/wiki/분류:C++ "wikilink") [분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:가상 머신](https://ko.wikipedia.org/wiki/분류:가상_머신 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.
2.
3.
4.  Java 바이트 코드와 MSIL 프런트 엔드, CPython 프런트 엔드, 그래프 컬러링 레지스터 할당 모듈 등에 이용할 수 있다.
5.
6.
7.  <http://llvm.org/releases/3.9.0/docs/ReleaseNotes.html>
8.  For the full documentation, refer to .
9.
10. [Target-specific Implementation Notes: Target Feature Matrix](http://llvm.org/docs/CodeGenerator.html#target-feature-matrix) // The LLVM Target-Independent Code Generator, LLVM site.
11. <http://llvm.org/releases/>