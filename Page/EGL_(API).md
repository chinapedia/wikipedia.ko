> This article is converted from Wikipedia: [EGL \(API\)](https://ko.wikipedia.org/wiki/EGL_\(API\)).


**EGL**은 ([OpenGL](../Page/OpenGL.md "wikilink"), [OpenGL ES](../Page/OpenGL_ES.md "wikilink") 또는 [OpenVG](https://ko.wikipedia.org/wiki/OpenVG "wikilink")와 같은) [크로노스](../Page/크로노스_그룹.md "wikilink") [렌더링 API와](https://ko.wikipedia.org/wiki/렌더링_API "wikilink") 기본 네이티브 플랫폼 [윈도우 시스템](https://ko.wikipedia.org/wiki/윈도우_시스템 "wikilink") 간의 [인터페이스이다](../Page/인터페이스_\(컴퓨팅\).md "wikilink"). EGL은 그래픽 [컨텍스트 관리](https://ko.wikipedia.org/wiki/컨텍스트_관리 "wikilink"), [서피스](https://ko.wikipedia.org/wiki/서피스 "wikilink")/[버퍼](https://ko.wikipedia.org/wiki/Data_buffer "wikilink") 바인딩, [렌더링](../Page/렌더링.md "wikilink") 동기화를 처리하고 "다른 크로노스 API를 사용하여 고성능, 가속화된, 혼합모드 [2D](https://ko.wikipedia.org/wiki/2차원_컴퓨터_그래픽스 "wikilink") 및 [3D](../Page/3차원_컴퓨터_그래픽스.md "wikilink") 렌더링"을 가능하게 한다.\[1\] EGL [비영리](../Page/비영리_단체.md "wikilink") 기술 컨소시엄 [크로노스 그룹에](../Page/크로노스_그룹.md "wikilink") 의해 관리되고 있다.

약어 *EGL*은 *Khronos Native Platform Graphics Interface*에 언급되어 EGL 버전 1.2부터 시작된 [initialism](https://ko.wikipedia.org/wiki/initialism "wikilink")이다.\[2\] 버전 1.2이전에는 EGL 스펙의 이름이 *OpenGL ES Native Platform Graphics Interface*였다.\[3\] [X.Org](https://ko.wikipedia.org/wiki/X.Org_재단 "wikilink") 개발 문서 용어집에서는 EGL을 "Embedded-System Graphics Library"로 정의한다.\[4\]

## 채택

  - [BlackBerry 10](https://ko.wikipedia.org/wiki/BlackBerry_10 "wikilink") 와 [BlackBerry Tablet OS](https://ko.wikipedia.org/wiki/BlackBerry_Tablet_OS "wikilink") 모바일 장치의 운영체제는 3D 그래픽 렌더링을 위해 EGL을 사용한다. Both support EGL version 1.4.\[5\]

  - [안드로이드](../Page/안드로이드_\(운영_체제\).md "wikilink") 모바일 장치 운영 체제는 3D 그래픽 렌더링을 위해 EGL을 사용한다.\[6\]

  - [Wayland](https://ko.wikipedia.org/wiki/Wayland "wikilink") 디스플레이 서버 프로토콜은 EGL을 사용한다.\[7\] Wayland 클라이언트가 EGL을 사용하여 프레임버퍼에 직접 그려주는 방식으로 구현되었다.

  - [메사 3D는](https://ko.wikipedia.org/wiki/메사_3D "wikilink") 이전에 이글(Eagle)로 알려진 EGL을 구현했다.\[8\]

  - [캐노니컬](../Page/캐노니컬.md "wikilink")에 의한 [Mir](https://ko.wikipedia.org/wiki/Mir "wikilink") 디스플레이 서버 프로토콜은 EGL을 사용한다.\[9\]

  - [SDL](../Page/심플_다이렉트미디어_레이어.md "wikilink")(Simple DirectMedia Layer) 툴킷은 EGL을 사용하기 위해 포팅되었다. [프레임버퍼](https://ko.wikipedia.org/wiki/프레임버퍼 "wikilink")에 직접 쓰기위해 [Xlib](../Page/Xlib.md "wikilink")을 사용하거나 EGL을 사용할 수 있다.

  - [Raspberry Pi](https://ko.wikipedia.org/wiki/Raspberry_Pi "wikilink") 싱글 보드 컴퓨터는 하드웨어 가속 3D 그래픽 랜더링에 EGL 인터페이스를 가지고 있다.\[10\]

  - 부터 독점적인 [엔비디아](../Page/엔비디아.md "wikilink") 드라이버 331.13 BETA 는 EGL API를 지원한다.\[11\]

  - [타이젠](../Page/타이젠.md "wikilink")(Tizen) OS는 3D 그래픽 렌더링을 위해 OpenGL ES 1.1 또는 OpenGL ES 2.0과 함께 EGL을 사용한다\[12\]

## 구현

  - [메사](https://ko.wikipedia.org/wiki/메사 "wikilink")는 많은 그래픽 렌더링 API들의 [자유-오픈 소스 소프트웨어](../Page/자유-오픈_소스_소프트웨어.md "wikilink") 구현이다. EGL도 그중 하나이다.
  - [일반 버퍼 관리](https://ko.wikipedia.org/wiki/일반_버퍼_관리 "wikilink")(Generic Buffer Management)는 버퍼를 관리하는 API이다.

## 같이 보기

  - [WGL](https://ko.wikipedia.org/wiki/WGL_\(API\) "wikilink") – OpenGL에 상응하는 [Windows](https://ko.wikipedia.org/wiki/Windows "wikilink") 인터페이스
  - [CGL](https://ko.wikipedia.org/wiki/Core_OpenGL "wikilink") – OpenGL에 상응하는 [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") 인터페이스
  - [GLX](https://ko.wikipedia.org/wiki/GLX "wikilink") – OpenGL에 상응하는 [X11](https://ko.wikipedia.org/wiki/X11 "wikilink") 인터페이스
      - [AIGLX](../Page/AIGLX.md "wikilink") – GLX를 가속화 하기 위한 시도
  - [WSI](https://ko.wikipedia.org/wiki/벌칸_\(API\) "wikilink") – Vulkan 윈도우 시스템 인터페이스 (WSI)는 OpenGL ES을 위해 EGL이 수행하는 작업을 Vulkan을 위해 수행.

## 참조

## 외부 링크

  -
[분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:자유 그래픽 스포트웨어](https://ko.wikipedia.org/wiki/분류:자유_그래픽_스포트웨어 "wikilink")

1.  [EGL Overview](http://www.khronos.org/egl/)
2.  [EGL 1.2 Specification](http://www.khronos.org/registry/egl/specs/eglspec.1.2.pdf)
3.  [EGL 1.0 Specification](http://www.khronos.org/registry/egl/specs/eglspec.1.0.pdf)
4.  [EGL in X.Org development documentation glossary](http://www.x.org/wiki/Development/Documentation/Glossary#EGL)
5.
6.  <http://developer.android.com/about/versions/android-2.3-highlights.html>
7.  <http://ppaalanen.blogspot.com/2012/03/what-does-egl-do-in-wayland-stack.html>
8.  [Mesa EGL](http://www.mesa3d.org/egl.html)
9.
10. <http://elinux.org/RPi_VideoCore_APIs>
11.
12. <https://wiki.tizen.org/wiki/Porting_Guide/Graphics_and_UI>