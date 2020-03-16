> This article is converted from Wikipedia: [X  ](https://ko.wikipedia.org/wiki/X__).


[섬네일](https://ko.wikipedia.org/wiki/파일:X-Window-System.png "wikilink")[창 관리자가](https://ko.wikipedia.org/wiki/창_관리자 "wikilink") 실행되어 있는 X 서버의 모습\]\] [섬네일](https://ko.wikipedia.org/wiki/파일:Screenshot_of_KDE..png "wikilink") 창 관리자를 이용한 현대적인 그래픽 [유저 인터페이스](https://ko.wikipedia.org/wiki/유저_인터페이스 "wikilink")([GUI](https://ko.wikipedia.org/wiki/GUI "wikilink"))의 예시.\]\]

**X 윈도 시스템** (X Window System, 흔히 X11, X라고 알려져 있음. )은 주로 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영체제](https://ko.wikipedia.org/wiki/운영체제 "wikilink")에서 사용되는 [윈도 시스템이다](https://ko.wikipedia.org/wiki/윈도_시스템 "wikilink").

X 윈도 시스템은 [디스플레이 장치에](https://ko.wikipedia.org/wiki/디스플레이_장치 "wikilink") [창을](../Page/창_\(컴퓨팅\).md "wikilink") 표시하며 [마우스](../Page/마우스.md "wikilink")와 [키보드](https://ko.wikipedia.org/wiki/키보드 "wikilink") 등의 [입력 장치의](../Page/컴퓨터_입력_장치.md "wikilink") 상호작용 등을 관리해 [GUI](https://ko.wikipedia.org/wiki/GUI "wikilink") 환경의 구현을 위한 기본적인 [프레임워크를](../Page/소프트웨어_프레임워크.md "wikilink") 제공한다.

X 윈도 시스템은 [MIT](https://ko.wikipedia.org/wiki/MIT "wikilink")에서 1984년에 처음 개발되었다. X 윈도 시스템 프로토콜의 가장 최근 버전은 1987년 9월에 나온 X11이다. 지금은 X.Org 재단이 X 윈도 시스템의 개발을 주도하고 있다. X.Org 재단은 X 윈도 시스템의 [참조 구현인](https://ko.wikipedia.org/wiki/참조_구현 "wikilink") X.Org Server를 개발해서 [MIT 허가서와](../Page/MIT_허가서.md "wikilink") 같은 [오픈 소스 라이선스로](../Page/오픈_소스_소프트웨어.md "wikilink") 배포한다.\[1\]

## 역사

X 윈도는 원래 플랫폼과 독립적으로 작동하는 윈도 시스템 개발을 위해 IBM과 MIT, DEC 공동의 아데나 프로젝트를 통해서 Bob Scheifler와 Jim Gettys가 1984년에 처음 개발하였다. 그 뒤로 지속적인 개발을 통해 1987년에 X11 버전이 개발되었다.

1986년에는 Bob Scheifler이 누구나 자유롭게 X를 사용하고 배포할 수 있는 오픈 소스 프로젝트 디자인을 만들었고 1987년에 이러한 오픈 소스 프로젝트 하에 X11이 발표된다.

1988년에는 수많은 컴퓨터 제조업체로 이루어진 X컨소시엄이 조직되고, X컨소시엄에 의해서 X11버전이 처음으로 개정되어 X11R2가 발표되었으며 1996년에는 최종 개정판인 X11R6 버전을 내놓으면서 X11R6.3 버전을 끝으로 X컨소시엄은 해체되었다.

같은 해에 오픈 소프트웨어 재단과 X/Open으로 형성된 오픈 그룹이 X11R6.4 버전을 발표하였지만, 오픈 그룹은 기존 공개 배포 라이선스 정책을 무시한 채, XFree86와 같은 수많은 프로젝트와 일부 상용 제조업체들의 참여를 가로막는 새로운 라이선스로 인한 잡음으로 결국에는 그 해 가을 기존 배포 라이선스 정책에 따라 X11R6.4 버전을 다시 배포하였다. 1999년 오픈 그룹은 X.org를 만들고, X.org에 의해서 X11R6.5.1이 나오게 되었다.

2004년에는 X.org 재단이 만들어졌으며, XFree86 4.4RC2와 X11R6.6을 기반으로 한 X11R6.7 버전이 개발되었다.

2004년 9월에는 X11R6.8 버전을 발표하였으며, 이 버전은 투명 창 지원, 체계적인 시각 효과 및 해상도 변경 기능, 3차원 가상 현실 디스플레이 장치 도구 지원, 섬네일 기능 등 다양한 시각적인 기능과 효과를 지원한다.

가장 최근 버전은 2012년 6월에 개발된 X11R7.7이다.

## 목적과 기능

X 윈도 시스템은 그래픽 사용자 인터페이스(GUI) 환경으로, 기존의 디스플레이 시스템과 다른 점은 [네트워크 프로토콜](../Page/통신_프로토콜.md "wikilink")(X 프로토콜)을 기반한 [클라이언트와 서버 모델의](https://ko.wikipedia.org/wiki/클라이언트_서버_시스템 "wikilink") 네트워크 지향 윈도 시스템이다. 서로 네트워크로 연결되어 있는 [단말기](../Page/단말기.md "wikilink")에 접속한 모든 사람은 입력 장치를 통해 컴퓨터를 이용할 수 있다.

X [응용 프로그램은](https://ko.wikipedia.org/wiki/응용_프로그램 "wikilink") 자신이 [클라이언트](https://ko.wikipedia.org/wiki/클라이언트 "wikilink")로서, 네트워크로 X [서버](../Page/서버.md "wikilink")에 접속하여 X 서버에게 명령 서비스(예를 들면, '굴림 글꼴을 출력'해 달라는 요청하든지 또는 '마우스 포인터를 여기로 옮겨라' 등등)를 요청하면, X 서버는 이러한 명령 요청을 받아 글꼴 서버를 통해서 굴림 글꼴을 보여 주거나, 응용 프로그램에서 마우스 포인터의 위치를 이동시켜 준다. 이와 같이 X 클라이언트는 X 서버에서 동작하면서 서버에게 명령을 전달하고, X 서버는 클라이언트에게 명령 요청의 결과를 디스플레이 장치에 출력해 주거나 키보드, 마우스, 터치스크린과 같은 사용자 입력을 클라이언트에게 제공해 주는 역할을 한다.

X의 클라이언트/서버의 네트워크 지향 시스템 구조는 로컬 상의 X 서버로부터 다른 시스템의 X 클라이언트의 요청을 받아들일 수 있는 또 다른 특징을 제공해 준다.

이것은 다른 시스템에 있는 응용 프로그램을 로컬 상의 X에서 실행시킬 수 있음을 의미하는 것으로써 예를 들어, 로컬상의 X 시스템에서는 파이어폭스가 설치되어 있지 않더라도 다른 원격 시스템에 파이어폭스가 설치되어 있다면 원격 시스템에 텔넷이나 SSH로 접속하여 로그인한 후 파이어폭스를 실행하면 로컬 X 서버에서 제공하는 화면 출력을 이용하여 원격 시스템에서 파이어폭스를 사용할 수 있다는 말이다. 이때 X 응용 프로그램의 디스플레이는 로컬 X 서버에서 처리되기 때문에, 원격 시스템에서는 X서버가 없어도 상관이 없다.

X 윈도 시스템은 단순하지만 표준 [위젯 툴킷과](https://ko.wikipedia.org/wiki/위젯_툴킷 "wikilink") 프로토콜 스택을 제공해 대부분의 Unix 기반 운영 체제 및 [OpenVMS](../Page/OpenVMS.md "wikilink")에서 [인터페이스](https://ko.wikipedia.org/wiki/인터페이스 "wikilink") 개발에 사용될 수 있다. 또한, X 윈도 시스템은 여러가지 운영 체제로 [이식되었다](../Page/이식_\(컴퓨팅\).md "wikilink").

X 윈도 시스템은 [사용자 인터페이스의](../Page/사용자_인터페이스.md "wikilink") 모습에 관여하지 않는다. 그래서 X 윈도를 이용한 사용자 환경의 모습은 매우 다양할 수 있다. 예를 들어, [KDE](../Page/KDE.md "wikilink"), [그놈](../Page/그놈.md "wikilink"), [Xfce](../Page/Xfce.md "wikilink") 등 대부분의 [데스크톱 환경은](../Page/데스크톱_환경.md "wikilink") X윈도를 기반으로 하지만, 유저 인터페이스의 모양은 매우 다르다.

파일:GNOME Shell.png|[그놈](../Page/그놈.md "wikilink") 데스크톱 환경 파일:KDE 4.png|[KDE](../Page/KDE.md "wikilink") 데스크톱 환경 파일:Xfce-4.4.png|[Xfce](../Page/Xfce.md "wikilink") 데스크톱 환경

## X 윈도 시스템의 구현 및 이식

X.Org 재단이 개발한 X.Org 서버가 X 윈도 시스템의 대표적인 구현이다. 2004년까지는 [XFree86](../Page/XFree86.md "wikilink")가 Unix 계열 운영 체제에서 가장 많이 쓰였던 X 윈도의 구현이였다. XFree86은 X를 [인텔 80386](../Page/인텔_80386.md "wikilink")-호환 컴퓨터로 [이식하기](../Page/이식_\(컴퓨팅\).md "wikilink") 위해 처음 개발되었다. 1990년대에는 XFree86이 X 윈도 시스템의 발전에 가장 큰 기여를 했으며 X 개발의 대표자가 되었다. 그러나 2004년부터는 XFree86의 [포크인](../Page/포크_\(소프트웨어_개발\).md "wikilink") X.Org 서버가 우세해졌다. 주로 Unix 계열 운영체제가 X 윈도 시스템을 사용하지만 다른 그래픽 환경을 위한 X 서버의 구현도 존재한다. 예를 들어, [휴렛 팩커드가](../Page/휴렛_팩커드.md "wikilink") 개발한 운영체제 [OpenVMS](../Page/OpenVMS.md "wikilink")도 X 윈도 시스템의 구현인 [공통 데스크톱 환경을](../Page/공통_데스크톱_환경.md "wikilink") 포함한다. 애플의 Mac OS X도 XQuartz라는 X 윈도 시스템의 구현을 포함하며, [마이크로소프트 윈도는](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") X 윈도를 공식으로 지원하지는 않지만 [시그윈](../Page/시그윈.md "wikilink") X 등 서드 파티 소프트웨어를 통해 구현할 수 있다. 이 외에도 [자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") [안드로이드를](../Page/안드로이드_\(운영_체제\).md "wikilink") 대상으로 한 구현이 존재한다.

## 경쟁 소프트웨어

[썬 마이크로시스템즈와](../Page/썬_마이크로시스템즈.md "wikilink") [NeXT](../Page/NeXT.md "wikilink") 등 여러 회사와 사람은 X 윈도 시스템과 비슷한 기능을 갖고 있는 소프트웨어 프레임워크를 개발하려고 했다. 다음은 현재 X 윈도 시스템과 비슷한 기능을 제공하는 경쟁 소프트웨어의 목록이다.

  - [OS X과](https://ko.wikipedia.org/wiki/OS_X "wikilink") [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")는 유닉스 계열 운영 체제 중에서 X 윈도를 쓰지 않는 가장 대표적인 운영 체제이다. OS X이 사용하는 윈도 시스템 쿼츠(Quartz)의 개발자 Mike Paquette는 만약 [애플이](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") X 윈도를 사용해서 운영 체제를 개발했다면 다른 X11 사용 서버와 호환성이 떨어졌을 것이라고 설명했다.\[2\]
  - [안드로이드는](../Page/안드로이드_\(운영_체제\).md "wikilink") 리눅스 기반 커널을 사용하지만, X 윈도 서비스 대신 SurfaceFlinger라는 디스플레이 서비스를 사용한다.
  - [Wayland는](../Page/웨이랜드.md "wikilink") X.Org 재단 개발자 몇 명이 만든 X 윈도 서비스를 대체하기 위한 디스플레이 서버로, [그래픽 카드](../Page/그래픽_카드.md "wikilink") 하드웨어를 응용 프로그램이 직접 제어할 수 있게 하는 것이 특징이다.

## 같이 보기

  - [창 관리자](https://ko.wikipedia.org/wiki/창_관리자 "wikilink")
  - [XFree86](../Page/XFree86.md "wikilink")
  - [Xgl](../Page/Xgl.md "wikilink")
  - [X11 색 이름](../Page/X11_색_이름.md "wikilink")

## 참조

  - Linda Mui and Eric Pearce, *X Window System Volume 8: X Window System Administrator's Guide for X11 Release 4 and Release 5, 3rd edition* (O'Reilly and Associates, July 1993; softcover )
  - Robert W. Scheifler and James Gettys: *X Window System: Core and extension protocols: X version 11, releases 6 and 6.1*, Digital Press 1996,
  - [The Evolution of the X Server Architecture](http://keithp.com/~keithp/talks/Xarchitecture/Talk.htm) (Keith Packard, 1999)
  - [The means to an X for Linux: an interview with David Dawes from XFree86.org](https://web.archive.org/web/20060916213448/http://www.cat.org.au/maffew/cat/xfree-dawes.html) (Matthew Arnison, CAT TV, June 1999)
  - [Lessons Learned about Open Source](http://www.usenix.org/publications/library/proceedings/usenix2000/invitedtalks/gettys_html/Talk.htm) (Jim Gettys, USENIX 2000 talk on the history of X)
  - [Open Source Desktop Technology Road Map](https://web.archive.org/web/20080413140042/http://people.freedesktop.org/~jg/roadmap.html) (Jim Gettys, 9 December 2003)
  - [X Marks the Spot: Looking back at X11 Developments of Past Year](http://www.osnews.com/story.php?news_id=6157) (Oscar Boykin, *OSNews*, 25 February 2004)
  - [Getting X Off The Hardware](http://keithp.com/~keithp/talks/xserver_ols2004/) (Keith Packard, July 2004 Ottawa Linux Symposium talk)
  - [Why Apple didn't use X for the window system](http://developers.slashdot.org/comments.pl?sid=75257&cid=6734612) (Mike Paquette, Apple Computer)

## 외부 링크

  - [X.Org 재단](http://www.x.org/) 공식 웹사이트

[X_윈도_시스템](https://ko.wikipedia.org/wiki/분류:X_윈도_시스템 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink")

1.
2.  [Why Apple didn't use X for the window system](http://developers.slashdot.org/comments.pl?sid=75257&cid=6734612) 19 August 2007