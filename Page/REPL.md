> This article is converted from Wikipedia: [REPL](https://ko.wikipedia.org/wiki/REPL).


**REPL**(read-eval-print loop) 또는 **인터랙티브 톱레벨**(interactive toplevel), **랭기지 셸**(language shell)은 단일 사용자의 입력(예: 단일 [식](https://ko.wikipedia.org/wiki/식_\(프로그래밍\) "wikilink"))을 취하고 이를 평가(실행)하고 결과를 사용자에게 반환시키는 단순한 상호작용 [컴퓨터 프로그래밍](../Page/컴퓨터_프로그래밍.md "wikilink") 환경이다. REPL 환경으로 작성된 프로그램은 구간마다 실행된다. 이 용어는 보통 클래식 [리스프 머신](https://ko.wikipedia.org/wiki/리스프_머신 "wikilink") 상호작용 환경과 유사한 프로그래밍 인터페이스를 의미하기도 한다. 일반적인 예로는 [프로그래밍 언어를](../Page/프로그래밍_언어.md "wikilink") 위한 [명령 줄](../Page/명령_줄_인터페이스.md "wikilink") [셸](../Page/셸.md "wikilink") 및 유사 환경을 들 수 있으며 기법은 [스크립트 언어의](../Page/스크립트_언어.md "wikilink") 특징과 매우 닮아있다.\[1\]

## 개요

REPL에서 사용자는 (전체 컴파일 단위가 아닌) 하나 이상의 식을 입력하면 REPL은 이들을 평가하고 결과를 표시한다.

## 용도

[셸](../Page/셸.md "wikilink")로서 REPL 환경을 통해 사용자가 운영 체제의 관련 기능에 접근할 수 있고 프로그래밍 기능에도 접근이 가능하다.

운영 체제 셸 밖에서 REPL의 가장 일반적인 용도는 즉각적인 프로토타이핑이다. 그 밖의 용도로는 수식 계산, 과학 분석(예: [IPython](https://ko.wikipedia.org/wiki/IPython "wikilink"))을 연동하는 문서 만들기, 상호 작용적인 소프트웨어 유지보수, [벤치마킹](../Page/벤치마킹.md "wikilink"), 알고리즘 탐색이 있다.

REPL은 새로운 언어를 학습하는데 필수적인 부분으로 되고 있는데, 초보자에게 빠른 피드백을 제공하기 때문이다.

## 리스프 특화

### 구현체

최소한의 정의:

``` Scheme
(define (REPL env)
  (print (eval env (read)))
  (REPL env) )
```

여기서 `env`는 초기 `eval`-uation(평가) 환경을 대표한다. 또, `env`가 `eval`에 의해 파괴적으로 업데이트될 수 있다.

## 같이 보기

  - [인터프리터](../Page/인터프리터.md "wikilink")

## 각주

## 외부 링크

  - [Paul Graham](https://ko.wikipedia.org/wiki/폴_그레이엄 "wikilink") has written a [description of a REPL implementation](http://www.paulgraham.com/rootsoflisp.html) in Common Lisp.
  - [:en:Repl.it](https://ko.wikipedia.org/wiki/:en:Repl.it "wikilink") [Online REPL for various programming languages](https://web.archive.org/web/20190108043127/https://repl.it/languages)
  - Joël Franusic [Online-REPs-and-REPLs list](http://joel.franusic.com/Online-REPs-and-REPLs)

[분류:셸](https://ko.wikipedia.org/wiki/분류:셸 "wikilink") [분류:리스프](https://ko.wikipedia.org/wiki/분류:리스프 "wikilink") [분류:인터프리터](https://ko.wikipedia.org/wiki/분류:인터프리터 "wikilink")

1.