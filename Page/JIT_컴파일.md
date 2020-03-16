> This article is converted from Wikipedia: [JIT ](https://ko.wikipedia.org/wiki/JIT_).


**JIT 컴파일**() 또는 **동적 번역**()은 프로그램을 실제 실행하는 시점에 [기계어](../Page/기계어.md "wikilink")로 번역하는 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink") 기법이다. 이 기법은 프로그램의 실행 속도를 빠르게 하기 위해 사용된다.

전통적인 입장에서 컴퓨터 프로그램을 만드는 방법은 두 가지가 있는데, 인터프리트 방식과 정적 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink") 방식으로 나눌 수 있다. 이 중 인터프리트 방식은 실행 중 프로그래밍 언어를 읽어가면서 해당 기능에 대응하는 기계어 코드를 실행하며, 반면 정적 컴파일은 실행하기 전에 프로그램 코드를 기계어로 번역한다.

JIT 컴파일러는 두 가지의 방식을 혼합한 방식으로 생각할 수 있는데, 실행 시점에서 인터프리트 방식으로 기계어 코드를 생성하면서 그 코드를 캐싱하여, 같은 함수가 여러 번 불릴 때 매번 기계어 코드를 생성하는 것을 방지한다.

최근의 [자바 가상 머신과](../Page/자바_가상_머신.md "wikilink") .NET, [V8](../Page/크롬_V8.md "wikilink")(node.js)에서는 JIT 컴파일을 지원한다. 즉, 자바 컴파일러가 [자바 프로그램 코드를](https://ko.wikipedia.org/wiki/자바_프로그래밍_언어 "wikilink") [바이트코드](../Page/바이트코드.md "wikilink")로 변환한 다음, 실제 바이트코드를 실행하는 시점에서 자바 가상 머신이 바이트코드를 JIT 컴파일을 통해 기계어로 변환한다.

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