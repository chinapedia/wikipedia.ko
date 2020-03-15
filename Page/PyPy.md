> This article is converted from Wikipedia: [PyPy](https://ko.wikipedia.org/wiki/PyPy).


**PyPy**는 유연함과 쉬운 실험을 위해 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 프로그래밍 언어 자체로 작성된 파이썬 구현체이다. 이 프로젝트의 목적 중 하나는 최적화된 PyPy의 파이썬 구현이 현재의 [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 구현보다 빠르도록 하는 것이다. PyPy 자체는 파이썬 언어의 부분집합인 [RPython](https://ko.wikipedia.org/wiki/RPython "wikilink")으로 구현되어 있다.

PyPy는 파이썬 코드를 [기계어](https://ko.wikipedia.org/wiki/기계어 "wikilink")나 다른 [저급 언어로](https://ko.wikipedia.org/wiki/저급_언어 "wikilink") 자동 번역하는 [저스트 인 타임 컴파일러](https://ko.wikipedia.org/wiki/저스트_인_타임_컴파일러 "wikilink") 기능을 포함하고 있는데, 특이한 점은 JIT 컴파일러 자체가 JIT 컴파일러 생성기로부터 — PyPy RPython 코드를 분석하여 — 자동생성된다는 점이다.

벤치마크 대상에 따라 다르긴 하지만 PyPy 1.4 버전부터 CPython보다 나은 성능을 보인다.\[1\]

예를 들어, PyPy 1.4는 PyPy 자체를 컴파일 하는 코드가 CPython보다 PyPy에서 더 빠르게 돌아가는 첫 번째 버전이다.

## 각주

<references/>

## 외부 링크

  -
  - [공식 블로그](http://morepypy.blogspot.com/)

[분류:파이썬 구현](https://ko.wikipedia.org/wiki/분류:파이썬_구현 "wikilink") [분류:파이썬 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬_소프트웨어 "wikilink") [분류:2007년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2007년_소프트웨어 "wikilink") [분류:파이썬으로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬으로_작성된_자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink")

1.  [CPython 2.6.2의 성능을 기준으로 비교한 PyPy 1.4 벤치마크](http://speed.pypy.org/comparison/?exe=2%2B35,1%2B172&ben=1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20&env=1&hor=false&bas=2%2B35&chart=normal+bars) - 그래프 막대가 낮을수록 빠름.