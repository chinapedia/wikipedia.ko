> This article is converted from Wikipedia: [JIT 컴파일](https://ko.wikipedia.org/wiki/JIT_컴파일).


**JIT 컴파일**() 또는 **동적 번역**()은 프로그램을 실제 실행하는 시점에 [기계어](../Page/기계어.md "wikilink")로 번역하는 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink") 기법이다.

전통적인 입장에서 컴퓨터 프로그램을 만드는 방법은 두 가지가 있는데, 인터프리트 방식과 정적 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink") 방식으로 나눌 수 있다. 이 중 인터프리트 방식은 실행 중 프로그래밍 언어를 읽어가면서 해당 기능에 대응하는 기계어 코드를 실행하며, 반면 정적 컴파일은 실행하기 전에 프로그램 코드를 기계어로 번역한다.

JIT 컴파일러는 두 가지의 방식을 혼합한 방식으로 생각할 수 있는데, 실행 시점에서 인터프리트 방식으로 기계어 코드를 생성하면서 그 코드를 캐싱하여, 같은 함수가 여러 번 불릴 때 매번 기계어 코드를 생성하는 것을 방지한다.

최근의 [자바 가상 머신과](../Page/자바_가상_머신.md "wikilink") .NET, [V8](../Page/크롬_V8.md "wikilink")(node.js)에서는 JIT 컴파일을 지원한다. 즉, 자바 컴파일러가 [자바 프로그램 코드를](https://ko.wikipedia.org/wiki/자바_프로그래밍_언어 "wikilink") [바이트코드](../Page/바이트코드.md "wikilink")로 변환한 다음, 실제 바이트코드를 실행하는 시점에서 자바 가상 머신이 바이트코드를 JIT 컴파일을 통해 기계어로 변환한다.

## 개요

바이트코드 컴파일러는 소스 코드를 중간언어인 바이트코드로 변환한다. 바이트코드는 기계어는 아니지만 가상 머신에 의해 기계어로 손쉽게 변환할 수 있는 코드이다. JIT 컴파일러는 바이트코드를 읽어 빠른 속도로 기계어를 생성할 수 있다. 이런 기계어 변환은 코드가 실행되기 과정에 실시간으로 일어나며(그래서 Just-In-Time이다), 전체 코드의 필요한 부분만 변환한다. 기계어로 변환된 코드는 캐시에 저장되기 때문에 재사용시 컴파일을 다시 할 필요가 없다.

일반적인 인터프러터 언어(예시: cpython)는 바이트코드나 소스코드를 최적화 과정이 없기 번역하기 때문에 성능이 낮다. 반면 정적으로 컴파일하는 언어(예시: c 언어)는 실행 전에 무조건 컴파일을 해야하기 때문에 다양한 플랫폼에 맞게 컴파일을 하려면 시간이 오래 걸린다. *동적 컴파일 환경*은 실행 과정에서 컴파일을 할 수 있기 위해 만들어졌다. JIT는 정적 컴파일러 만큼 빠르면서 인터프러터 언어의 빠른 응답속도를 추구하기 위해 사용한다. 바이트코드 컴파일러가 시간이 많이 소요되는 최적화를 미리 해주기 때문에 바이트코드에서 기계어 번역은 훨씬 빠르게 진행될 수 있다. 또한 바이트코드는 이식성이 뛰어나 가상 머신이 설치되어 있으면 빠르게 실행할 수 있다. 플랫폼 별로 가상 머신을 개발하는 과정은 컴파일러를 만드는 간단한데, 그 이유는

1.  복잡한 최적화 과정은 바이트코드 컴파일러가 대신 해주므로 고려하지 않아도 된다.
2.  바이트코드는 빠른 기계어 변환을 목적으로 설계되었기 때문에 일반적인 컴파일러보다 제작 과정이 수월하다.

JIT 코드는 일반적인 인터프러터 언어에 비해 훨씬 좋은 성능을 낸다. 심지어 경우에 따라 정적 컴파일러 언어보다 좋은 성능을 내곤 하는데, 이는 실행 과정에 컴파일을 할 수 있기 때문에 가지는 장점이라고 할 수 있다:

1.  컴파일이 cpu나 운영체제에 따라 다르게 진행될 수 있다. 예를 들어 cpu가 SSE2 vector instruction을 지원한다면 cpu는 이를 활용하는 방법으로 최적화를 진행한다.
2.  정적 컴파일러 언어로 Garbage Collection을 지원하게 만들 수 있지만, JIT 시스템을 이용하면 더 쉽게 GC를 사용할 수 있다.

## 역사

최초로 공개된 JIT 컴파일러는 일반적으로 1960년 [존 매카시의](https://ko.wikipedia.org/wiki/존_매카시 "wikilink") [리스프](../Page/리스프.md "wikilink")에 공이 주어진다.

## 참고 자료

  - L. Peter Deutsch and Allan M. Schiffman, ["Efficient Implementation of the Smalltalk-80 System"](https://web.archive.org/web/20040618105930/http://webpages.charter.net/allanms/popl84.pdf), 11th Annual Symposium on Principles of Programming Languages, Jan 1984, pp. 297-302
  - [Free Online Dictionary of Computing entry](https://web.archive.org/web/20020905042721/http://foldoc.doc.ic.ac.uk/foldoc/foldoc.cgi?just-in-time)
  - John Aycock, ["A brief history of just-in-time"](http://doi.acm.org/10.1145/857076.857077), ACM Computing Surveys, 35,2, 2003, pp. 97-113
  - Matthew Arnold, Stephen Fink, David Grove, Michael Hind, and Peter F. Sweeney, ["A Survey of Adaptive Optimization in Virtual Machines"](http://www.research.ibm.com/people/h/hind/papers.html#survey05), Proceedings of the IEEE, 92(2), February 2005, Pages 449-466.

## 같이 보기

  - [LLVM](../Page/LLVM.md "wikilink")
  - [이진 변환](https://ko.wikipedia.org/wiki/이진_변환 "wikilink")
  - [자체 수정 코드](../Page/자체_수정_코드.md "wikilink")

## 각주

## 외부 링크

  - [Real-time Java, Part 2: 컴파일 기술 비교](http://www.ibm.com/developerworks/kr/library/j-rtj2/index.html) - [자바 프로그래밍 언어에서의](https://ko.wikipedia.org/wiki/자바_프로그래밍_언어 "wikilink") JIT 컴파일의 장점과 단점을 설명하고 있다.
  - [GNU *lightning*](http://www.gnu.org/software/lightning/) — 동적 시간에 어셈블리 언어를 생성하는 라이브러리

[분류:컴파일러 구성](https://ko.wikipedia.org/wiki/분류:컴파일러_구성 "wikilink") [분류:에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:에뮬레이션_소프트웨어 "wikilink") [분류:가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:가상화_소프트웨어 "wikilink")