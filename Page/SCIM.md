> This article is converted from Wikipedia: [SCIM](https://ko.wikipedia.org/wiki/SCIM).


[섬네일](https://ko.wikipedia.org/wiki/파일:Scim_logo.jpg "wikilink") **SCIM**(Smart Common Input Method)은 30개 이상의 언어([CJK](../Page/CJK.md "wikilink")와 각종 [유럽어](https://ko.wikipedia.org/wiki/유럽어 "wikilink"))를 지원하는 [POSIX](../Page/POSIX.md "wikilink") 스타일 [운영 체제](../Page/운영_체제.md "wikilink")([리눅스](../Page/리눅스.md "wikilink")나 [BSD](../Page/BSD.md "wikilink")를 포함)를 위한 [입력기](../Page/입력기.md "wikilink") 플랫폼이다.

SCIM은 입력기(, 줄여서 IM) 개발을 쉽게 하는 개발 플랫폼이다. 구조가 매우 명확하다는 장점이 있고, 상당히 간결하고 강력한 프로그래밍 인터페이스를 제공한다.

SCIM은 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 작성한 공용 입력기 플랫폼이다. 입력기 인터페이스를 여러 [계층으로](https://ko.wikipedia.org/wiki/계층_\(컴퓨터_과학\) "wikilink") 추상화하고, 계층들을 가능한 한 단순하고 서로 종속되지 않도록 한다. 이런 단순한 인터페이스로 인해, 개발자는 자신의 입력기를 몇 줄의 코드로 쉽게 작성할 수 있다.

SCIM은 모듈화가 잘 되어 있다. 대부분의 컴포넌트는 동적으로 로드할 수 있는 모듈로 구현하였기 때문에, [실행 시간에도](https://ko.wikipedia.org/wiki/실행_시간_\(컴퓨터_프로그래밍\) "wikilink") 마음대로 로드할 수 있다. 예를 들어, SCIM용 입력기 중에는 입력기 엔진 모듈도 있는데, 사용자는 다른 환경에서 그 입력기 엔진 모듈을 다시 만들거나 다시 컴파일하지 않고도 다른 인터페이스 모듈(프런트엔드)와 결합하여 사용할 수 있다.

SCIM은 XIM이나 IIIMF보다 높은 계층에 있는 라이브러러지만, 인터페이스는 더 간단하다. 그리고 XIM이나 심지어 IIIMF하고도 같이 동작할 수 있다. SCIM은 [GTK+](../Page/GTK+.md "wikilink")2 immodule이나[Qt immodule](https://web.archive.org/web/20051122094536/http://immodule-qt.freedesktop.org/wiki/Software_2fimmodule_2dqt)처럼 특정 클라이언트에 특화한 입력기 인터페이스를 지원할 수 있다.

SCIM을 [KDE](../Page/KDE.md "wikilink")에 최적화하는 것을 목표로 개발되는 프로젝트인 **SKIM**도 있다.

## SCIM의 주요 특징

  - C++로 기록한 완전한 객체지향 구조.
  - 높은 모듈화.
  - 매우 유연한 구조, C/S 입력기 환경처럼 동적으로 로드하는 라이브러리를 사용할 수 있음.
  - 단순한 프로그래밍 인터페이스.
  - UCS-4/UTF-8인코딩으로 완전한 국제화 지원.
  - 다양하고 편리한 유틸리티 기능을 포함하여 개발이 빠름.
  - 수많은 기능을 포함한 [그래픽 사용자 인터페이스](../Page/그래픽_사용자_인터페이스.md "wikilink") 패널.
  - 통합된 환경 설정 프레임워크.
  - scim-hangul 0.3.0이상의 버전에서 일본어 방식의 한자입력을 지원한다.\[1\]
  - 특수 문자 입력 기능(0.3.0\~0.3.1까지는 이 기능이 제거되었으나 0.3.2 버전에서 다시 추가되었다. 자음 하나를 입력하고 F9키를 누르면 된다.)

## SCIM의 목적

  - 현재 가능한 입력기 라이브러리를 위한 통합된 프런트엔드로 동작. 현재 uim과 m17n 라이브러리와 연동할 수 있음.
  - IIIMF 입력기 프레임워크의 언어 엔진으로 동작.
  - 가능한 한 다양한 고유 입력기 엔진 제공.
  - 가능한 한 다양한 입력기 프로토콜/인터페이스 지원 가능.
  - 가능한 한 다양한 운영체제 지원.

## 같이 보기

  - [입력기](../Page/입력기.md "wikilink")
  - [유닉스 플랫폼 입력기 목록](../Page/유닉스_플랫폼_입력기_목록.md "wikilink")
  - [uim](https://en.wikipedia.org/wiki/Uim)

## 각주

## 외부 링크

  - [SCIM 홈페이지](http://www.scim-im.org)
  - [sourceforge.net의 SCIM 프로젝트](http://scim.sf.net/)

[분류:입력기](https://ko.wikipedia.org/wiki/분류:입력기 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink")

1.