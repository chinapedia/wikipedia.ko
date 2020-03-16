> This article is converted from Wikipedia: [SWIG](https://ko.wikipedia.org/wiki/SWIG).


**SWIG**(Simplified Wrapper and Interface Generator)는 [C나](../Page/C_\(프로그래밍_언어\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 작성된 [컴퓨터 프로그램이나](../Page/컴퓨터_프로그램.md "wikilink") 라이브러리들을 [루아](../Page/루아_\(프로그래밍_언어\).md "wikilink"), [펄](../Page/펄.md "wikilink"), [PHP](../Page/PHP.md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"), [R](../Page/R_\(프로그래밍_언어\).md "wikilink"), [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink"), [Tcl](../Page/Tcl.md "wikilink")과 같은 [스크립트 언어](../Page/스크립트_언어.md "wikilink") 및 [C 샤프](../Page/C_샤프.md "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [자바스크립트](../Page/자바스크립트.md "wikilink"), [Go](https://ko.wikipedia.org/wiki/Go "wikilink"), [모듈러-3](https://ko.wikipedia.org/wiki/모듈러-3 "wikilink"), [Ocaml](https://ko.wikipedia.org/wiki/Ocaml "wikilink"), [옥타브](../Page/GNU_옥타브.md "wikilink"), [Scilab](https://ko.wikipedia.org/wiki/Scilab "wikilink"), [스킴](../Page/스킴_\(프로그래밍_언어\).md "wikilink") 등의 다른 언어들과 연결하는데 사용하는 [오픈 소스 소프트웨어](../Page/오픈_소스_소프트웨어.md "wikilink") 도구이다.

## 역사

SWIG는 C와 C++로 작성되어 있으며, 1996년 2월 이후로 일반에 공개되었다. 초기 개발자이자 주요 개발자는 데이브 비즐리이며, [로스 앨러모스 국립 연구소](https://ko.wikipedia.org/wiki/로스_앨러모스_국립_연구소 "wikilink") 및 [유타 대학교에서](../Page/유타_대학교.md "wikilink") 학부생으로 일하는 동안, 또 [시카고 대학교에서](../Page/시카고_대학교.md "wikilink") 교수로 활동하는 동안 SWIG를 개발하였다. 개발은 현재 윌리엄 펄튼(William Fulton) 주도의 활발한 자발자들의 그룹에 의해 지원을 받고 있다. SWIG는 [GNU GPL에](https://ko.wikipedia.org/wiki/GNU_GPL "wikilink") 의거하여 출시되고 있다.

## 기능

다른 프로그래밍 언어가 C나 C++로 작성된 네이티브 함수의 호출을 허용하고, 복잡한 자료형을 해당 함수에 전달하고, 메모리를 부적절하게 해제하지 못하게 하며, 언어 간에 오브젝트 클래스를 상속할 수 있게 하는 것이 목적이다. 프로그래머는 C/C++ 함수의 목록이 포함된 인터페이스 파일을 작성하여 인터프리터에 보이게 한다. SWIG는 인터페이스를 컴파일한 다음 일반 C/C++ 및 대상 프로그래밍 언어를 발생시킨다. SWIG는 단순한 인수가 포함된 함수들을 위한 [변환 코드를](../Page/마샬링_\(컴퓨터_과학\).md "wikilink") 만든다. 즉, 복잡한 인수형의 변환 코드는 프로그래머에 의해 작성되어야 한다. SWIG 도구는 C/C++과 대상 언어 간의 접착제(glue)를 제공하는 [소스 코드를](../Page/소스_코드.md "wikilink") 만든다. 이 언어에 의존하여 이 접착제는 2가지 형태로 나타난다:

  - 현존하는 인터프리터가 특정한 형태의 확장 모듈로 링크할 수 있는 [공유 라이브러리](../Page/라이브러리_\(컴퓨팅\).md "wikilink")
  - 대상 언어로 컴파일된 다른 프로그램으로 링크할 수 있는 공유 라이브러리 (예를 들어 자바의 JNI, [자바 네이티브 인터페이스를](../Page/자바_네이티브_인터페이스.md "wikilink") 사용)

SWIG는 네이티브 코드에 의해 해석된 함수를 호출하기 위해 사용되지는 않는다. 즉, 프로그래머가 수동으로 완성해야 한다.

## 예

SWIG는 선언이 C 프로그램에서 사용되는 방식과 동일한 인터페이스를 작성함으로써 단순한 C 선언들을 래핑한다. 이를테면, 다음의 인터페이스 파일이 있다고 가정한다:\[1\]

``` swig
%module example

%inline %{
extern double sin(double x);
extern int strcmp(const char *, const char *);
extern int Foo;
%}
#define STATUS 50
#define VERSION "1.1"
```

이 파일에서  및 라는 두 개의 함수와 전역 변수 , 그리고 와 이라는 두 개의 상수가 있다. SWIG가 확장 모듈을 만들 때 이 선언들은 스크립트 언어 함수, 변수, 상수로 각각 접근이 가능하다. 파이썬에서는:

``` pycon
>>> example.sin(3)
0.141120008
>>> example.strcmp('Dave','Mike')
-1
>>> print example.cvar.Foo
42
>>> print example.STATUS
50
>>> print example.VERSION
1.1
```

## 목적

기존의 C/C++ 프로그램에서 [스크립트 엔진을](../Page/스크립트_언어.md "wikilink") 임베드하는 주된 이유는 2가지가 있다:

  - C/C++ 대신 스크립트 언어를 통해 프로그램을 훨씬 더 빠르게 개인화(customize)시킬 수 있다. 스크립트를 작성함으로써 공통 작업을 자동화될 수 있으므로 스크립트 엔진은 최종 사용자에게 노출될 수도 있다.
  - 최종 제품이 스크립트 엔진을 포함하지 않는다고 하더라도 테스트 스크립트 작성에 매우 유용할 수 있다.

현존하는 인터프리터에 로드할 수 있는 동적 라이브러리를 만드는 이유가 몇 가지 있는데 다음을 포함한다:

  - 스크립트 언어와 동등하지 않은 C/C++ [라이브러리로의](../Page/라이브러리_\(컴퓨팅\).md "wikilink") 접근을 제공한다.
  - 우선 스크립트 언어의 전반적인 프로그램을 작성하고 [프로파일링을](https://ko.wikipedia.org/wiki/프로파일링_\(컴퓨터_프로그래밍\) "wikilink") 거친 다음 성능에 많은 영향을 미치는 코드를 C나 C++로 재작성한다.

## SWIG를 이용한 프로젝트

  - [ZXID](https://ko.wikipedia.org/wiki/ZXID "wikilink")
  - Symlabs SFIS (상용)
  - [LLDB](../Page/LLDB.md "wikilink")
  - [GNU 라디오](../Page/GNU_라디오.md "wikilink")
  - [Xapian](https://ko.wikipedia.org/wiki/Xapian "wikilink")
  - Armory

## 같이 보기

  - [LLDB](../Page/LLDB.md "wikilink")

## 참고문헌

  - Article "[Expose Your C/C++ Program's Internal API with a Quick SWIG](http://codeguru.com/csharp/.net/net_asp/scripting/article.php/c11103/)" by Victor Volkman
  - Article "[Python Extensions In C++ Using SWIG](https://web.archive.org/web/20090129071001/http://geocities.com/foetsch/python/extending_python.htm)" by Michael Fötsch
  - Presentation "[Application overview for openSUSE](https://web.archive.org/web/20090425013344/http://blip.tv/file/1179673/)" by Klaus Kämpf

## 각주

## 외부 링크

  -
[분류:프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:프로그래밍_도구 "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink")

1.  <http://www.swig.org/Doc3.0/SWIG.html#SWIG_nn9>