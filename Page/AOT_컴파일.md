> This article is converted from Wikipedia: [AOT ](https://ko.wikipedia.org/wiki/AOT_).


**AOT 컴파일**(ahead-of-time compile)은 목표 시스템의 기계어와 무관하게 중간 언어 형태로 배포된 후 목표 시스템에서 [인터프리터](../Page/인터프리터.md "wikilink")나 [JIT 컴파일](../Page/JIT_컴파일.md "wikilink") 등 기계어 번역을 통해 실행되는 중간 언어를 미리 목표 시스템에 맞는 기계어로 번역하는 방식을 지칭한다. 이런 중간 언어로는 [자바 바이트코드](../Page/자바_바이트코드.md "wikilink"), [공통 중간 언어](../Page/공통_중간_언어.md "wikilink")(Common Intermediate Language), IBM System/38 혹은 IBM System i의 기술 독립적 머신 인터페이스(Technology Independent Machine Interface)가 있으며 학계에서도 마이클 프란즈(Michael Franz)\[1\]가 제안해 오베론 시스템의 일부 구현에서 사용된 슬림 바이너리(Slim Binaries)와 같은 제안이 있었다.

일반적으로 중간 언어를 사용하는 시스템은 실행 시간에 [JIT 컴파일과](../Page/JIT_컴파일.md "wikilink") 같은 기법을 통해 실행 시에만 얻을 수 있는 프로그램 분석 정보를 사용하여 높은 성능을 달성할 수 있다. 특히 [객체 지향](https://ko.wikipedia.org/wiki/객체_지향 "wikilink") 언어나 [스크립트 언어](../Page/스크립트_언어.md "wikilink") 같이 동적인 언어인 경우 효과적이다. 하지만 실행 시 프로그램 분석과 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")을 함께 수행하는데 추가 메모리 및 CPU 사이클이 필요한 단점이 있다. 따라서 AOT 컴파일은 이에 대한 보완책으로 사용되고 있다.

## 응용 범위

  - 메모리 및 CPU 제약이 있는 경우: [인터프리터](../Page/인터프리터.md "wikilink")는 너무 느리고 [JIT 컴파일은](../Page/JIT_컴파일.md "wikilink") 너무 부담이 큰 경우로 [임베디드 시스템인](../Page/임베디드_시스템.md "wikilink") 경우가 많다. 단 이 경우 목표 시스템에 내장 되는 프로그램에 한해서 AOT 컴파일을 하고 내려받는 프로그램은 인터프리터나 JIT 컴파일로 실행하는 경우가 보통이다.
  - 프로그램 특성 상 빠른 시작 시간과 일관된 성능이 중요한 경우: [데스크톱 환경에서](../Page/데스크톱_환경.md "wikilink") 그래픽 사용자 인터페이스 위주의 프로그램인 경우가 이에 해당 한다.
  - 전통적인 컴파일러 최적화가 효과적인 경우: 계산이 많은 프로그램처럼 일반 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")을 통한 최적화가 효과적인 경우에 사용할 수 있다. AOT 컴파일은 [소스 코드](../Page/소스_코드.md "wikilink") 대신 중간 언어를 받아 들인다는 점을 빼면 일반적인 정적 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")과 동일하기 때문에 실행 시간에 비해 충분한 프로그램 분석을 통해 최적화를 보여준다.

## 구현

### 자바

  - GNU 자바 컴파일러\[2\]: GNU 컴파일러에 자바 전단부(front-end)를 넣어서 자바 코드를 실행 코드로 컴파일한다.
  - Excelsior JET\[3\]: 자바를 위한 상용 AOT 컴파일러 제품

### .NET CLR

  - .NET NGen\[4\]: 마이크로소프트의 .NET CLR 구현에 포함된 AOT 컴파일러
  - Mono AOT 컴파일러\[5\]: Mono 프로젝트의 AOT 컴파일러 구현

## 각주

<references/>

[분류:컴파일러](https://ko.wikipedia.org/wiki/분류:컴파일러 "wikilink")

1.  [1](http://www.ics.uci.edu/~franz/) 마이클 프란즈의 UCI 홈페이지
2.  [2](http://gcc.gnu.org/java/)  GNU 자바 컴파일러 프로젝트 페이지
3.  [3](http://www.excelsior-usa.com/jet.html)  Excelsior JET 제품 페이지
4.  \[<http://msdn.microsoft.com/ko-kr/library/6t9t5wcf(VS.80>).aspx\] MSDN NGen.exe 설명 문서
5.  [4](http://www.mono-project.com/AOT) Mono AOT 페이지