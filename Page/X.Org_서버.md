> This article is converted from Wikipedia: [X.Org 서버](https://ko.wikipedia.org/wiki/X.Org_서버).


**X.Org 서버**(X.Org Server)는 [X.Org 재단에](https://ko.wikipedia.org/wiki/X.Org_재단 "wikilink") 의해 구성된 [X 윈도 시스템용](../Page/X_윈도_시스템.md "wikilink") [디스플레이 서버](https://ko.wikipedia.org/wiki/디스플레이_서버 "wikilink") 구현체인 [자유-오픈 소스](../Page/자유-오픈_소스_소프트웨어.md "wikilink") 구현체이다. 이 프로토콜의 클라이언트 사이드 구현체로는 [Xlib](../Page/Xlib.md "wikilink")와 [XCB](../Page/XCB.md "wikilink") 등으로 이용이 가능하다.

## 소프트웨어 구조

X.Org 서버는 서버 사이드의 [X 윈도우 시스템 코어 프로토콜](https://ko.wikipedia.org/wiki/X_윈도우_시스템_코어_프로토콜 "wikilink") 버전 11(X11)과 이 버전의 확장(예: RandR)을 구현한다.\[1\]

버전 1.16.0은 [systemd](https://ko.wikipedia.org/wiki/systemd "wikilink") 기반의 런칭 및 관리를 지원함으로써 부팅 성능과 신뢰성을 높였다.\[2\]

###  DIX(Device Independent X)

DIX(Device Independent X)는 클라이언트와 통신하고 소프트웨어 렌더링을 구현하는 X.Org 서버의 일부이다. 메인 루프와 이벤트 전달은 DIX의 일부분이다.\[3\]

###  DDX(Device Dependent X)

DDX(Device Dependent X)는 하드웨어와 통신하는 x-server의 일부이다.

####  2D 그래픽스 드라이버

역사적인 이유로 X.Org 서버는 일부 형태의 2D 렌더링 가속을 지원하는 그래픽스 장치 드라이버를 포함하고 있다.

##### 가속 아키텍처

(적어도) XAA(XFree86 Acceleration Architecture),\[4\] [EXA](https://ko.wikipedia.org/wiki/EXA "wikilink"), [UXA](https://ko.wikipedia.org/wiki/UMA_가속_아키텍처 "wikilink"), [SNA가](https://ko.wikipedia.org/wiki/SNA_\(컴퓨터_그래픽스\) "wikilink") 있다.

#####  글래머

글래머(Glamor)는 X 렌더 프리미티브를 [OpenGL](../Page/OpenGL.md "wikilink") 명령으로 변환하는 X 서버용, 하드웨어 독립적인 2D 가속 드라이버이며 기존 3D OpenGL 드라이버의 장점을 취한다.\[5\] 이러하 방식으로, 기능은 쿼츠 익스트림과 쿼츠GL(2D 성능 가속)→(애플 [쿼츠 컴포지터용](https://ko.wikipedia.org/wiki/쿼츠_컴포지터 "wikilink"))과 비슷하다.

글래머의 궁극적인 목적은 모든 DDX 2D 그래픽스 장치 드라이버와 가속 아키텍처를 대체시킴으로써 지원하는 모든 그래픽 칩셋을 위해 X 2D 특화 드라이버들의 작성 필요성을 없애는 것이다.\[6\]\[7\]\[8\] 글래머는 [셰이더](../Page/셰이더.md "wikilink") 지원을 위해 3D 드라이버가 필요하다.\[9\]

#####  가상화

[가상화 환경](../Page/가상화.md "wikilink") 내부의 시스템에서 동작하는 X.Org 서버 인스턴스를 위한 별개의 특수한 DDX가 존재한다: xf86-video-qxl는 "QXL 비디오 장치"용 드라이버이다. [SPICE](https://ko.wikipedia.org/wiki/SPICE "wikilink")는 이 드라이버를 활용하지만 이 드라이버 없이도 동작한다.

데비안 저장소에서는 다음으로 호칭한다: xserver-xorg-video-qxl, cf. <https://packages.debian.org/buster/xserver-xorg-video-qxl>

####  입력 스택

데비안에서 입력과 관련한 드라이버들은 `/usr/lib/xorg/modules/input/`에서 볼 수 있다. 이러한 드라이버의 이름은 이를테면 다음과 같다: `evdev_drv.so`, `mouse_drv.so`, `synaptics_drv.so`, `wacom_drv.so`.

#### 기타 DDX 구성 요소

  - XWayland

  - XQuartz

  - Xspice

  - Xephyr

  - RandR

## 채택

  - 유닉스, 리눅스
  - 마이크로소프트 윈도우
  - OS X

## 역사

### 릴리스

<table>
<thead>
<tr class="header">
<th><p>버전</p></th>
<th><p>날짜</p></th>
<th><p>X11 릴리스</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>[10]</p></td>
<td><p>X11R7.0 (1.0.1)</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>[11]</p></td>
<td><p>X11R7.1 (1.1.0)</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[12]</p></td>
<td><p>X11R7.2 (1.2.0)</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>[13]</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[14]</p></td>
<td><p>X11R7.3 (1.4.0)</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>[15]</p></td>
<td><p>X11R7.4 (1.5.1)</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[16]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>[17]</p></td>
<td><p>X11R7.5 (1.7.1)</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[18]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>[19]</p></td>
<td><p>X11R7.6 (1.9.3)</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[20]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>[21]</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[22]</p></td>
<td><p>X11R7.7 (1.12.2)</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>[23]</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[24]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>[25]</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[26]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>[27]</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[28]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>[29]</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>[30]</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [참조 구현](https://ko.wikipedia.org/wiki/참조_구현 "wikilink")

## 각주

## 외부 링크

  - [X.Org home page](http://www.x.org/)
  - [X.Org git source code repository](http://cgit.freedesktop.org/xorg/)

[분류:X 서버](https://ko.wikipedia.org/wiki/분류:X_서버 "wikilink") [분류:Freedesktop.org](https://ko.wikipedia.org/wiki/분류:Freedesktop.org "wikilink") [분류:소프트웨어 포크](https://ko.wikipedia.org/wiki/분류:소프트웨어_포크 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.