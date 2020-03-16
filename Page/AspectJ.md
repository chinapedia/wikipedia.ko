> This article is converted from Wikipedia: [AspectJ](https://ko.wikipedia.org/wiki/AspectJ).


**AspectJ**는 [PARC](https://ko.wikipedia.org/wiki/PARC "wikilink")에서 개발한 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 프로그래밍 언어용 [관점 지향 프로그래밍](../Page/관점_지향_프로그래밍.md "wikilink") (AOP) 확장 기능이다. [이클립스 재단](../Page/이클립스_재단.md "wikilink") 오픈 소스 프로젝트에서 독립형 또는 [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")로 통합하여 이용 가능하다. AspectJ는 최종 사용자를 위한 단순함과 이용성을 강조함으로써 폭넓게 사용되는 AOP에 대한 데 팍토 표준이 되었다. 자바 계열 문법을 사용하며 2001년 초기 출시 이후 [횡단 구조를](../Page/횡단_관심사.md "wikilink") 표시하기 위한 IDE 연동을 포함하였다.

## 단순 언어 설명

유효한 모든 자바 프로그램들은 유효한 AspectJ 프로그램들이기도 하지만 AspectJ는 프로그래머들이 [관점](https://ko.wikipedia.org/wiki/관점_지향_소프트웨어_개발 "wikilink")(aspect)이라 불리는 특수한 생성자를 정의한다. 관점들은 표준 클래스들에 이용할 수 없는 여러 엔티티를 포함할 수 있다. 이들은 다음과 같다:

  - [확장 메소드](https://ko.wikipedia.org/wiki/확장_메소드 "wikilink")(extension method): 프로그래머가 메소드, 필드, 인터페이스를 aspect 내의 기존 클래스들에 추가할 수 있게 한다. 이 예는 `acceptVisitor` ([비지터 패턴](../Page/비지터_패턴.md "wikilink") 참고) 메소드를 `Point` 클래스에 추가한다:

:

``` aspectj
aspect VisitAspect {
  void Point.acceptVisitor(Visitor v) {
    v.visit(this);
  }
}
```

  - [포인트컷](https://ko.wikipedia.org/wiki/포인트컷 "wikilink")(Pointcut): 프로그래머가 [조인 포인트를](https://ko.wikipedia.org/wiki/조인_포인트 "wikilink") 지정할 수 있게 한다. 모든 포인트컷은 주어진 조인 포인트와 일치하는지를 결정하는 식이다. 이를테면, 포인트컷은 이름이 `set`으로 시작하는 `Point`형의 오브젝트의 임의의 인스턴스 메소드의 실행과 일치한다:

:

``` aspectj
pointcut set() : execution(* set*(..) ) && this(Point);
```

  - [어드바이스](https://ko.wikipedia.org/wiki/어드바이스 "wikilink")(Advice): 프로그래머가 [포인트컷](https://ko.wikipedia.org/wiki/포인트컷 "wikilink")에 의해 일치되는 조인 포인트에서 실행할 코드를 지정할 수 있게 한다. 이 동작은 지정된 조인 포인트의 앞("before"), 뒤("after"), 주변("around")에서 수행할 수 있다. 여기에서 어드바이스는 위에 선언된 포인트컷을 사용하여 `Point` 상의 무언가가 설정될 때마다 화면을 새로 고친다:

:

``` aspectj
after () : set() {
  Display.update();
}
```

또, AspectJ는 제한된 형태의 포인트컷 기반 정적 검사와 aspect 재사용(상속을 통해)을 지원한다. 언어의 더 자세한 설명에 대해서는 [AspectJ 프로그래밍 가이드](http://www.eclipse.org/aspectj/doc/released/progguide/index.html) 참고.

## 역사 및 기여자

[Gregor Kiczales는](https://ko.wikipedia.org/wiki/Gregor_Kiczales "wikilink") [PARC](../Page/팰로앨토_연구소.md "wikilink") 팀을 시작, 주도하면서 최종적으로 AspectJ를 개발하였다. 그는 크로스커팅(crosscutting), 즉 "횡단"이라는 용어를 만들어냈다. 크리스 마에다(Crhis Maeda)는 관점 지향 프로그래밍(aspect-oriented programming)이라는 용어를 만들어냈다.

### AspectWerkz

AspectWerkz는 [자바용의](../Page/자바_\(프로그래밍_언어\).md "wikilink") 가벼운 동적 고성능 [AOP/AOSD](../Page/객체_지향_프로그래밍.md "wikilink") 프레임워크이다. AspectJ 프로젝트와 병합되었으며 AspectJ 5 이후로 AspectWerkz 기능을 지원한다.

## 같이 보기

  - [관점 지향 프로그래밍](../Page/관점_지향_프로그래밍.md "wikilink")
  - [스프링 AOP](../Page/스프링_프레임워크.md "wikilink") ([스프링 프레임워크의](../Page/스프링_프레임워크.md "wikilink") 일부)
  - [관점 지향 소프트웨어 개발](https://ko.wikipedia.org/wiki/관점_지향_소프트웨어_개발 "wikilink")

## 참고문헌

  -
  -
  -
  -
## 외부 링크

  - [AJDT](https://web.archive.org/web/20170811190325/http://www.eclipse.org/ajdt/)
  - Aspect bench : <https://web.archive.org/web/20170816093700/http://www.sable.mcgill.ca/abc/>
  - [AspectJ Home Page](https://web.archive.org/web/20170805180224/http://www.eclipse.org/aspectj/)
  - [AspectWerkz Project homepage](https://web.archive.org/web/20060706114810/http://aspectwerkz.codehaus.org/)
  - [Improve modularity with aspect-oriented programming](http://www.ibm.com/developerworks/java/library/j-aspectj)
  - [Spring AOP and AspectJ Introduction](http://java2novice.com/spring/aop-and-aspectj-introduction/)
  - [The AspectJ<sup>TM</sup> Programming Guide](http://www.eclipse.org/aspectj/doc/released/progguide/index.html)
  - Xerox has  for AOP/AspectJ, but published AspectJ source code under the [Common Public License](https://web.archive.org/web/20170811230223/http://www.eclipse.org/legal/cpl-v10.html), which grants some patent rights.

[분류:관점 지향 프로그래밍](https://ko.wikipedia.org/wiki/분류:관점_지향_프로그래밍 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:소프트웨어 배포](https://ko.wikipedia.org/wiki/분류:소프트웨어_배포 "wikilink") [분류:자바 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:자바_프로그래밍_언어_계열 "wikilink") [분류:이클립스 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:이클립스_라이선스_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink")