> This article is converted from Wikipedia: [OpenGL  ](https://ko.wikipedia.org/wiki/OpenGL__).


**OpenGL 유틸리티 툴킷**(OpenGL Utility Toolkit, GLUT)은 호스트 운영체제와 시스템 수준의 입출력을 가능하게 만드는 [OpenGL](../Page/OpenGL.md "wikilink") 프로그램용 유틸리티 라이브러리이다. 주요한 기능으로 창의 크기와 형태를 정의하고 제어하며, 키보드와 마우스 입력을 감지하는 기능이 있다. 뿐만 아니라 [정육각형](https://ko.wikipedia.org/wiki/정육각형 "wikilink"), [구](https://ko.wikipedia.org/wiki/구_\(기하학\) "wikilink"), [유타 찻잔과](https://ko.wikipedia.org/wiki/유타_찻잔 "wikilink") 같은 컴퓨터 그래픽스에서 요긴한 몇가지 기하학적인 기본객체(geometric primitives)를 그려주는 루틴도 가지고 있으며, 팝업 메뉴를 생성하는 기능도 제공한다.

OpenGL 유틸리티 툴킷은 [실리콘 그래픽스사에서](../Page/실리콘_그래픽스.md "wikilink") 근무하고 *OpenGL Programming for the X Window System*와 *The Cg Tutorial: The Definitive Guide to Programmable Real-Time Graphics*라는 책을 저술한 마크 킬가드(Mark Kilgard)가 개발하였다.

OpenGL 유틸리티 툴킷의 두가지 중요한 목적은 운영체제사이의 이식성이 좋은 코드를 구현하자는 것과 OpenGL을 쉽게 익히도록하는 것이다. 실제로 [OpenGL](../Page/OpenGL.md "wikilink") [프로그래밍](https://ko.wikipedia.org/wiki/프로그래밍 "wikilink")을 OpenGL 유틸리티 툴킷을 사용하게되면 매우 적은 라인과 운영체제에 대한 깊이 있는 지식이 없더라도 쉽게 프로그램을 작성할 수 있다. 모든 OpenGL 유틸리티 툴킷 함수는 `glutPostRedisplay`, `glutCreateWindow`와 같이`glut`라는 접두사로 시작한다.

## 구현

원래 OpenGL 유틸리티 툴킷 라이브러리는 X 윈도 시스템을 지원하기 위하여 마크 킬가드가 개발하였으며 이후에 네이트 로빈스에 의하여 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사의 WiggleWin32로 포팅되었다. 또한 현재는 [애플사의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [매킨토시](https://ko.wikipedia.org/wiki/매킨토시 "wikilink") 운영 체제에서도 사용되고 있다.

## 같이 보기

  - [OpenGL 유틸리티 라이브러리](https://ko.wikipedia.org/wiki/OpenGL_유틸리티_라이브러리 "wikilink") (GLU)
  - [OpenGL 사용자 인터페이스 라이브러리](../Page/OpenGL_사용자_인터페이스_라이브러리.md "wikilink") (GLUI)
  - [freeglut](https://ko.wikipedia.org/wiki/freeglut "wikilink")
  - [심플 다이렉트미디어 레이어](../Page/심플_다이렉트미디어_레이어.md "wikilink")(SDL)

[분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:3차원 컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/분류:3차원_컴퓨터_그래픽스 "wikilink")