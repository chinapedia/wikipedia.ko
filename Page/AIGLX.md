> This article is converted from Wikipedia: [AIGLX](https://ko.wikipedia.org/wiki/AIGLX).


[thumb](https://ko.wikipedia.org/wiki/파일:Linux_graphics_drivers_DRI_current.svg "wikilink") and **AIGLX** versus [direct rendering](https://ko.wikipedia.org/wiki/Direct_Rendering_Infrastructure "wikilink").\]\] **AIGLX**()는 [X.Org](https://ko.wikipedia.org/wiki/X.Org "wikilink")와 [DRI](https://ko.wikipedia.org/wiki/DRI "wikilink") 드라이버가 간접 [GLX](https://ko.wikipedia.org/wiki/GLX "wikilink") 렌더링이 가능하도록 [래드햇](https://ko.wikipedia.org/wiki/래드햇 "wikilink")과 [페도라 커뮤니티에서](https://ko.wikipedia.org/wiki/페도라_프로젝트 "wikilink") 개발한 [오픈 소스](../Page/오픈_소스.md "wikilink") [프로젝트](https://ko.wikipedia.org/wiki/프로젝트 "wikilink")이다. AIGLX는 원격 X 클라이언트가 GLX 프로토콜로 완전히 하드웨어 가속된 렌더링이 가능하게 한다. 동시에 하드웨어 가속을 사용하는 ([컴피즈](../Page/컴피즈.md "wikilink")같은) [OpenGL](../Page/OpenGL.md "wikilink") [컴포지트 창 관리자는](https://ko.wikipedia.org/wiki/컴포지트_창_관리자 "wikilink") AIGLX의 개발이 요구되었다. [페도라](https://ko.wikipedia.org/wiki/페도라 "wikilink")에 기본적으로 포함되어 있다.

## AIGLX를 지원하는 그래픽 드라이버

### ATI

오래된 그래픽 카드는 X.Org의 공식 [레이디언](https://ko.wikipedia.org/wiki/레이디언 "wikilink") 드라이버로 오랫동안 지원하고 있다. [ATI](https://ko.wikipedia.org/wiki/ATI "wikilink")의 독점 드라이버는 [fglrx](https://ko.wikipedia.org/wiki/fglrx "wikilink") 8.42 버전부터 AIGLX를 지원한다. 최신 컴피즈와 X.Org를 사용하는 사용자는 불안정과 문제점이 제기하지만, 드라이버와 관련된 문제인지, 컴피즈나 X.Org 문제인지는 명확하지 않다. 만약 컴피즈 + ATI 독점 드라이버를 사용한 시스템이 불안정하다면, 다음 버전을 발표할 때까지 기다려야 한다.\[1\]

### 엔비디아

엔비디아는 자체적인 GL, GLX 아키텍처를 통해 AIGLX를 오랫동안 지원하였으며 표준 [다이렉트 렌더링 인프라](https://ko.wikipedia.org/wiki/다이렉트_렌더링_인프라 "wikilink") 구조를 이용하지 않는다.\[2\]

### 인텔

인텔은 추가를 용이하게 하는 오픈 소스 드라이버를 제공함으로써 AIGLX는 오랫동안 [X.Org](https://ko.wikipedia.org/wiki/X.Org "wikilink")의 공식 인텔 드라이버의 일부로 지원되어 왔다.

## 같이 보기

  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [XGL](https://ko.wikipedia.org/wiki/XGL "wikilink")
  - [X 윈도 시스템](../Page/X_윈도_시스템.md "wikilink")
  - [컴피즈](../Page/컴피즈.md "wikilink")

## 각주

## 외부 링크

  - [페도라 프로젝트 - 렌더링 프로젝트/AIGLX](http://fedoraproject.org/wiki/RenderingProject/aiglx)

[분류:자유 소프트웨어 프로젝트](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_프로젝트 "wikilink")

1.  [\[Phoronix](http://www.phoronix.com/scan.php?page=article&item=887&num=1) AMD 8.42 Driver Brings Fixes, AIGLX\! \]
2.  [Gentoo Linux Documentation - Gentoo Linux nVidia Guide](http://www.gentoo.org/doc/en/nvidia-guide.xml)