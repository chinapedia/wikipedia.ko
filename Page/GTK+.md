> This article is converted from Wikipedia: [GTK+](https://ko.wikipedia.org/wiki/GTK+).


**GTK+**는 **김프 툴킷**(GIMP Toolkit)의 준말로, 초기에 [김프](../Page/김프.md "wikilink")를 위해서 만든 툴킷이었으며 [X 윈도 시스템을](../Page/X_윈도_시스템.md "wikilink") 위한 위젯 툴킷 가운데 하나이다. GTK+와 [Qt는](../Page/Qt_\(프레임워크\).md "wikilink") [모티프에](https://ko.wikipedia.org/wiki/모티프_\(위젯_툴킷\) "wikilink") 대한 좋은 대안이 되어 주었다. GTK+는 1997년 [스펜서 킴볼](https://ko.wikipedia.org/wiki/스펜서_킴볼 "wikilink")(Spencer Kimball), [피터 마티스](https://ko.wikipedia.org/wiki/피터_마티스 "wikilink")(Peter Mattis), [조시 맥도널드](https://ko.wikipedia.org/wiki/조시_맥도널드 "wikilink")(Josh MacDonald)가 함께 만든 것이다. 그들은 모두 [UC 버클리에](https://ko.wikipedia.org/wiki/UC_버클리 "wikilink") 있는 [eXperimental Computing Facility](https://ko.wikipedia.org/wiki/eXperimental_Computing_Facility "wikilink") (XCF) 소속이었다. [LGPL로](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink") 라이선스되었기 때문에, GTK+는 자유 소프트웨어이자 오픈 소스 소프트웨어이고, GNU 프로젝트의 일부분이다.

## 설계

GTK+는 [C언어로](../Page/C_\(프로그래밍_언어\).md "wikilink") 작성된 객체지향 위젯 툴킷이다. X11 디스플레이 서버 상에서, GTK+는 위젯들을 그리는데 Xlib를 사용한다. Xlib는 유연하고 X 윈도 시스템이 작동하지 않는 플랫폼에서도 GTK+가 사용될 수 있도록 한다.

GTK+는 Qt와 마찬가지로 (다른 많은 위젯 툴킷들과 달리) [Xt에](https://ko.wikipedia.org/wiki/Intrinsics "wikilink") 기반을 두지 않는다. 그래서 GTK+를 많은 다른 환경으로 이식할 수 있었다. 하지만 전통적인 X11 응용 프로그램의 사용자 설정 방식인 X 리소스 데이터베이스에 접근할 수 없다는 단점이 있다.

## 언어 바인딩

[C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [펄](../Page/펄.md "wikilink"), [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [파이썬](../Page/파이썬.md "wikilink") 등으로의 바인딩을 제공한다. 많은 사람들이 [에이다](https://ko.wikipedia.org/wiki/에이다_프로그래밍_언어 "wikilink"), [D](../Page/D_\(프로그래밍_언어\).md "wikilink"), [하스켈](../Page/하스켈.md "wikilink"), [파스칼](../Page/파스칼_\(프로그래밍_언어\).md "wikilink"), [PHP](../Page/PHP.md "wikilink"), [닷넷 프레임워크로의](../Page/닷넷_프레임워크.md "wikilink") 바인딩을 작성하였다.

### [Hello World 프로그램](https://ko.wikipedia.org/wiki/Hello_World_프로그램 "wikilink")

#### [C](../Page/C_\(프로그래밍_언어\).md "wikilink")

  - 소스 코드

<!-- end list -->

``` c
#include <gtk/gtk.h>

int main (int argc, char *argv[])
{
    GtkWidget *window;
    GtkWidget *label;

    gtk_init(&argc, &argv);

    /* Create the main, top level window */
    window = gtk_window_new(GTK_WINDOW_TOPLEVEL);

    /* Give it the title */
    gtk_window_set_title(GTK_WINDOW(window), "Hello, world!");

    /*
    ** Map the destroy signal of the window to gtk_main_quit;
    ** When the window is about to be destroyed, we get a notification and
    ** stop the main GTK+ loop by returning 0
    */
    g_signal_connect(window, "destroy", G_CALLBACK(gtk_main_quit), NULL);

    /*
    ** Assign the variable "label" to a new GTK label,
    ** with the text "Hello, world!"
    */
    label = gtk_label_new("Hello, world!");

    /* Plot the label onto the main window */
    gtk_container_add(GTK_CONTAINER(window), label);

    /* Make sure that everything, window and label, are visible */
    gtk_widget_show_all(window);

    /*
    ** Start the main loop, and do nothing (block) until
    ** the application is closed
    */
    gtk_main();

    return 0;
}
```

  - 빌드 명령

<!-- end list -->

``` bash
$ gcc -Wall helloworld.c -o helloworld $(pkg-config --cflags --libs gtk+-3.0)
```

#### [Vala](../Page/발라_\(프로그래밍_언어\).md "wikilink")

  - 소스 코드

<!-- end list -->

``` vala
using Gtk;

int main (string[] args) {
    Gtk.init (ref args);

    /* Create the main, top level window */
    var window = new Window();

    /* Give it the title, border, position, and size */
    window.title = "Hello, World!";
    window.border_width = 10;
    window.window_position = WindowPosition.CENTER;
    window.set_default_size(350, 70);

    /*
    ** Map the destroy signal of the window to gtk_main_quit;
    ** When the window is about to be destroyed, we get a notification and
    ** stop the main GTK+ loop by returning 0
    */
    window.destroy.connect(Gtk.main_quit);

    /*
    ** Assign the variable "label" to a new GTK label,
    ** with the text "Hello, world!"
    */
    var label = new Label("Hello, World!");

    /* Add the label onto the main window */
    window.add(label);

    /* Make sure that everything, window and label, are visible */
    window.show_all();

    /*
    ** Start the main loop, and do nothing (block) until
    ** the application is closed
    */
    Gtk.main();
    return 0;
}
```

  - 빌드 명령

<!-- end list -->

``` bash
$ valac --pkg gtk+-3.0 HelloWorldGtk.vala
```

## 모양

사용자는 디스플레이 엔진으로 툴킷의 모양을 설정할 수 있다. 엔진들은 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [모티프](https://ko.wikipedia.org/wiki/모티프_\(위젯_툴킷\) "wikilink"), [Qt](../Page/Qt_\(프레임워크\).md "wikilink"), [넥스트스텝](https://ko.wikipedia.org/wiki/넥스트스텝 "wikilink")등의 모양으로 그려줄 수 있다.

## GTK+를 사용하는 환경

[오른쪽](https://ko.wikipedia.org/wiki/파일:gimp2-2.png "wikilink") 2.0 on [Xfce](../Page/Xfce.md "wikilink")4\]\]

  - [그놈](../Page/그놈.md "wikilink") 환경은 GTK+를 기반으로 사용한다.
  - [Xfce](../Page/Xfce.md "wikilink") 환경도 GTK+를 기반으로 사용한다. 하지만 Xfce용 프로그램은 많은 것에 의존하지 않는다. (이것은 그놈 프로그램과 GTK+ 프로그램을 구분한다)
  - [GPE](https://ko.wikipedia.org/wiki/GPE "wikilink"), [Maemo](https://ko.wikipedia.org/wiki/Maemo "wikilink") (노키아의 인터넷 태블릿 프레임워크), [액세스 리눅스 플랫폼](https://ko.wikipedia.org/wiki/액세스_리눅스_플랫폼 "wikilink") (새로운 팜 OS 호환 PDA 플랫폼) 도 GTK+를 기반으로 한다.

GTK+ 프로그램은 [KDE](../Page/KDE.md "wikilink") 같은 다른 데스크톱 환경에서 돌아간다. GTK+는 [마이크로소프트 윈도에서도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 돌아간다. [DirectFB](https://ko.wikipedia.org/wiki/DirectFB "wikilink")와 [ncurses](https://ko.wikipedia.org/wiki/ncurses "wikilink") 기반 포팅도 있다.

### 창 관리자

  - [메타시티](https://ko.wikipedia.org/wiki/메타시티 "wikilink")는 GTK+ 2를 사용한다.
  - [Xfwm](https://ko.wikipedia.org/wiki/Xfwm "wikilink")은 GTK+ 2를 사용한다.

## 그래픽과 관련되지 않은 코드

GTK+는 초기에 그래픽과 관련되지 않은 코드를 포함했다. 이들은 링크드 리스트 및 바이너리 트리를 제공했다. [GObject](../Page/GObject.md "wikilink")와 함께 오는 이러한 유틸리티 시스템은 [Glib](https://ko.wikipedia.org/wiki/Glib "wikilink")라는 별도의 라이브러리로 쪼개졌고, 이는 그래픽 인터페이스가 필요 없는 프로그래머에게 도움을 준다.

## GTK+ 2

GTK+ 2는 GTK+를 계승하였다. 이것의 새로운 기능은 [Pango](https://ko.wikipedia.org/wiki/Pango "wikilink")를 사용하는 새로운 텍스트 렌더링 엔진, 새로운 테마 엔진, 향상된 접근성, [유니코드](../Page/유니코드.md "wikilink")로의 완전한 전환이 있다. 하지만 GTK+ 2는 GTK+ 1과 호환성이 없으므로 프로그래머들이 소스를 새로 짜야 한다. 몇몇 프로그램들은 GTK+ 1을 그대로 사용한다. GTK+ 1은 GTK+ 2보다 빠르고 덜 복잡하고 임베디드 환경에 더 적합하다.

GTK+ 2.8부터는 [카이로](https://ko.wikipedia.org/wiki/카이로_\(그래픽\) "wikilink") 엔진을 사용해서 벡터 그래픽을 처리한다.

## MS 윈도우에서의 환경설정

공식웹사이트\[1\] 에서 최신버전을 다운로드받아 압축을 원하는 폴더에 풀어준다.

  -
    압축을 푼 다음, ------\\gtk------\\bin 경로를 시스템 환경 설정(환경변수)에서 PATH 경로 추가
    설치가 잘 되었는지 확인을 위해 명령행에서 "gtk-demo"를 실행\[2\]

## 차후 개발

  - [Project Ridley](https://web.archive.org/web/20110301113158/http://live.gnome.org/ProjectRidley)는 GTK+가 현재 포함하지 않는 각종의 라이브러리를 포함하려고 하는 시도이다. 이들은 libgnome, libgnomeui, libgnomeprint22, libgnomeprintui22, libglade, libgnomecanvas, libegg, libeel ,gtkglext를 포함한다.

## 같이 보기

  - [Gtk\#](https://ko.wikipedia.org/wiki/Gtk_샤프 "wikilink") - [닷넷 프레임워크](../Page/닷넷_프레임워크.md "wikilink") API를 GTK+로
  - [PyGTK](https://ko.wikipedia.org/wiki/PyGTK "wikilink"), [파이썬](../Page/파이썬.md "wikilink") API를 GTK+로
  - [PHP-GTK](https://ko.wikipedia.org/wiki/PHP-GTK "wikilink"), [PHP](../Page/PHP.md "wikilink") 확장
  - [루비 그놈](https://ko.wikipedia.org/wiki/루비_그놈 "wikilink")

## 각주

## 외부 링크

  -
  - [GTK+ Reference Manual](http://library.gnome.org/devel/gtk3/stable/)

  - [List of GTK+ applications](https://web.archive.org/web/20160624083231/http://gtk-apps.org/)

  - [Another list of GTK+ applications](https://web.archive.org/web/20130317070842/http://gtkfiles.org/)

  - [GTK+2&3 binaries for Windows](https://sourceforge.net/projects/gtk-mingw/)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:그놈](https://ko.wikipedia.org/wiki/분류:그놈 "wikilink") [분류:위젯 툴킷](https://ko.wikipedia.org/wiki/분류:위젯_툴킷 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:LGPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:LGPL_라이선스_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.  <http://www.gtk.org>
2.  <http://www.sysnet.pe.kr/Default.aspx?mode=2&sub=0&detail=1&pageno=0&wid=1366&rssMode=1&wtype=0>