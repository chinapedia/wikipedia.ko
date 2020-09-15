> This article is converted from Wikipedia: [Nu \(프로그래밍 언어\)](https://ko.wikipedia.org/wiki/Nu_\(프로그래밍_언어\)).


**Nu**는 [리스프](../Page/리스프.md "wikilink") 계열 문법을 사용하는 인터프리터 방식의 [객체 지향 프로그래밍](../Page/객체_지향_프로그래밍.md "wikilink") 언어이며, 개발자는 팀 벅스이다. [코코아](../Page/코코아_\(API\).md "wikilink") [API](../Page/API.md "wikilink")를 통해 [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")를 프로그래밍하는 스크립트 언어의 다른 대안이다. [아이폰](../Page/아이폰.md "wikilink")과 [리눅스](../Page/리눅스.md "wikilink")용 구현체도 존재한다.

이 언어는 2007년 8월 인디 맥 개발자들을 위한 콘퍼런스인 [C4에서](https://ko.wikipedia.org/wiki/C4_\(콘퍼런스\) "wikilink") 처음 발표되다.\[1\]

## 예시 코드

이 Nu 코드는 단순 복소수 클래스를 정의한다.

``` lisp
(class Complex is NSObject
  (ivar (double) real
        (double) imaginary)

  (- initWithReal:(double) x imaginary:(double) y is
    (super init)
    (set @real x)
    (set @imaginary y)
    self))
```

아래 예시는 복소수의 기본 정의이다: 인스턴스 변수를 정의하고 객체를 초기화하기 위한 메소드를 정의한다. Nu의 코드와 [오브젝티브-C](../Page/오브젝티브-C.md "wikilink")의 동일 코드 간 유사성을 보여주고 있다. 또, [루비와도](../Page/루비_\(프로그래밍_언어\).md "wikilink") 유사성을 보여준다.

``` lisp
(unless @prefix
        (set @prefix
             "#{((((NSProcessInfo processInfo) arguments) 0) dirName)}.."))

(unless @icon_files
        (set @icon_files
             (array "#{@prefix}/share/nu/resources/nu.icns")))
```

이 샘플은 Nu에 번들링된 "nuke" 도구로부터 비롯된 것으로 언어 설계에 [오브젝티브-C](../Page/오브젝티브-C.md "wikilink"), [리스프](../Page/리스프.md "wikilink"), [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink") 언어가 영향을 미친 것을 보여준다.

## 같이 보기

  - [맥루비](https://ko.wikipedia.org/wiki/맥루비 "wikilink")
  - [루비코코아](https://ko.wikipedia.org/wiki/루비코코아 "wikilink")

## 각주

## 외부 링크

  -
  -
[분류:리스프 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:리스프_프로그래밍_언어_계열 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink") [분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:객체 지향 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍_언어 "wikilink") [분류:2007년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:2007년_개발된_프로그래밍_언어 "wikilink")

1.