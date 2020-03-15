> This article is converted from Wikipedia: [GMP \(\)](https://ko.wikipedia.org/wiki/GMP_\(\)).


**GMP**(GNU Multiple-Precision Library)는 임의의 크기를 가진 수치를 계산하기 위한 [자유 소프트웨어](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink") [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")이다. GMP가 설치된 컴퓨터의 저장 장치가 가용한 한 이론상 무한한 정도의 계산이 가능하다. GMP 라이브러리는 풍부한 함수와 정규 인터페이스를 제공하고 있다. 기본 인터페이스는 C 프로그래밍 언어를 위하여 제공하며, 기타 다른 언어에 대해서는 래퍼(wrapper)를 통한 인터페이스를 제공한다. 인터페이스를 지원하는 언어로는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [OCaml](https://ko.wikipedia.org/wiki/OCaml "wikilink"), [Perl](https://ko.wikipedia.org/wiki/Perl "wikilink"), 그리고 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 등이 있다. GMP는 암호화 애플리케이션, 인터넷 보안 애플리케이션 및 대수학 등에 사용하는 것이 주요 목적이다.

GMP는 그 어떤 큰 수 라이브러리보다 더 빠르게 만드려는 목표를 가지고 있다. 이 목표를 달성하기 위하여 다음과 같은 중요한 성공 요소를 고려하고 있다.

  - 기본 숫자 형 데이터는 풀 워드를 사용
  - 서로 다른 [피 연산자의](https://ko.wikipedia.org/wiki/피_연산자 "wikilink") 크기에 따른 다른 알고리즘 채택 – 큰 수 처리 알고리즘이 작은 수 계산에 동시에 빠른 성능을 내는 경우가 거의 없기 때문이다.
  - 서로 다른 [CPU에](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") 따른 고도의 최적화 구현

최초의 GMP는 1991년에 발표되었다. 지속적인 개발과 유지보수 활동을 통해서, 거의 매년 새로운 버전을 발표하고 있다. 현재 발표된 최신 버전은 5.0.3이다.

GMP는 GNU 프로젝트의 일환으로 유지되고 있으며, GNU LPGL 라이선스 정책에 따라 배포되고 있다.

[매스매티카](https://ko.wikipedia.org/wiki/매스매티카 "wikilink")\[1\] 와 같은 대표적인 컴퓨터 대수 시스템 소프트웨어의 정수 계산을 위한 부분에 사용되고 있기도 하다.

## 같이 보기

  - [MPSolve](https://ko.wikipedia.org/wiki/:en:MPSolve "wikilink")

## 각주

입니다

## 외부 링크

  - [GMP 공식 웹사이트](http://gmplib.org/)

[분류:수치 해석 소프트웨어](https://ko.wikipedia.org/wiki/분류:수치_해석_소프트웨어 "wikilink") [GMP 라이브러리](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:C 라이브러리](https://ko.wikipedia.org/wiki/분류:C_라이브러리 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:LGPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:LGPL_라이선스_소프트웨어 "wikilink")

1.  [Numerical computation features for Mathematica 5.0](http://library.wolfram.com/infocenter/Demos/4946/) Rob Knapp