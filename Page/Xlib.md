> This article is converted from Wikipedia: [Xlib](https://ko.wikipedia.org/wiki/Xlib).


**Xlib**는 [C 프로그래밍 언어로](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 작성된 [X 윈도 시스템](https://ko.wikipedia.org/wiki/X_윈도_시스템 "wikilink") 프로토콜 클라이언트 [라이브러리이다](https://ko.wikipedia.org/wiki/라이브러리_\(컴퓨팅\) "wikilink"). X [서버](https://ko.wikipedia.org/wiki/서버 "wikilink")와 상호 작용하는 [함수](https://ko.wikipedia.org/wiki/함수 "wikilink")들을 포함하고 있다. 이 함수들은 프로그래머들이 [통신 프로토콜을](https://ko.wikipedia.org/wiki/통신_프로토콜 "wikilink") 자세히 모르더라도 프로그램을 작성할 수 있게 도와 준다. Xlib을 직접 사용하는 응용 프로그램들은 드문 편이지만, 대개 [위젯 툴킷을](https://ko.wikipedia.org/wiki/위젯_툴킷 "wikilink") 제공하기 위해 Xlib 함수들을 사용하는 다른 라이브러리들을 이용하는 편이다:

[frame](https://ko.wikipedia.org/wiki/파일:Xlib_and_XCB_in_the_X_Window_System_graphics_stack.svg "wikilink"), 그리고 이들을 사용하는 라이브러리들\]\]

  - [인트린식스](https://ko.wikipedia.org/wiki/X_툴킷_인트린식스 "wikilink") (Xt)
  - [아테나 위젯 집합](https://ko.wikipedia.org/wiki/X_아테나_위젯 "wikilink") (Xaw)
  - [모티프](https://ko.wikipedia.org/wiki/모티프_\(위젯_툴킷\) "wikilink")
  - [FLTK](https://ko.wikipedia.org/wiki/FLTK "wikilink")
  - [GTK+](https://ko.wikipedia.org/wiki/GTK+ "wikilink")
  - [Qt](https://ko.wikipedia.org/wiki/Qt_\(툴킷\) "wikilink") (X11 버전)
  - [Tk](https://ko.wikipedia.org/wiki/Tk_\(프레임워크\) "wikilink")

Xlib은 1985년 즈음에 출현했으며 현재 수많은 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") [운영 체제의](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") [GUI에](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 사용된다. [XCB](https://ko.wikipedia.org/wiki/XCB "wikilink") 라이브러리는 Xlib을 대체할 목적으로 만들어진 라이브러리이다. 아직까지 Xlib이 널리 쓰이고 있으나, 오늘날 Xlib에서 구현하는 것들은 낮은 수준의 전송 계층으로서 XCB를 대신 이용할 수 있다.

## 자료형

Xlib의 주가 되는 자료형은 `Display` 구조\[1\]와 그 식별자의 자료형들이다.

## 예

다음의 프로그램은 내부에 조그마한 검은 사각형이 포함된 창을 하나 만들어낸다:

``` C
 /*
  * 창 안에 상자를 그려내는 단순 Xlib 응용 프로그램입니다.
  * gcc input.c -o output -lX11
  */

#include <X11/Xlib.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    Display *display;
    Window window;
    XEvent event;
    char *msg = "Hello, World!";
    int s;

    /* 서버 연결 개시 */
    display = XOpenDisplay(NULL);
    if (display == NULL) {
        fprintf(stderr, "display를 열 수 없습니다\n");
        exit(1);
    }

    s = DefaultScreen(display);

    /* 창 만들기 */
    window = XCreateSimpleWindow(display, RootWindow(display, s), 10, 10, 200, 200, 1,
                           BlackPixel(display, s), WhitePixel(display, s));

    /* 이용하려는 이벤트 종류 선택 */
    XSelectInput(display, window, ExposureMask | KeyPressMask);

    /* 창 보이기 */
    XMapWindow(display, window);

    /* 이벤트 루프 */
    while (1) {
        XNextEvent(display, &event);

        /* 창을 (다시) 그리기 */
        if (event.type == Expose) {
            XFillRectangle(display, window, DefaultGC(display, s), 20, 20, 10, 10);
            XDrawString(display, window, DefaultGC(display, s), 50, 50, msg, strlen(msg));
        }
        /* 키 눌림이 있으면 끝내기 */
        if (event.type == KeyPress)
            break;
    }

    /* 서버 연결 닫기 */
    XCloseDisplay(display);

    return 0;
 }
```

클라이언트는 `XOpenDisplay`를 호출함으로써 서버 연결을 만든다. 그 뒤 `XCreateSimpleWindow`로 창 만들기를 요청한다. `XMapWindow`로의 별도 호출은 창을 매핑(보여주기)하는데 필수적이다.

`XFillRectangle`을 호출함으로써 사각형을 그려낸다. 이 동작은 창이 만들어진 뒤에만 수행할 수 있다. 그러나 한 차례만 수행하는 것은 충분하지 않을 수도 있다. 사실 창의 내용은 언제나 보존될 것임을 보증하지는 않는다. 이를테면 창이 다른 무언가에 의해 가려졌다가 다시 보이게 되면 내용물은 다시 그리기가 필요할 수 있다. 이 프로그램은 창이나 창의 일부가 `Expose` 이벤트를 도입함으로써 그리기가 필요할 수 있다.

## 참조

<references />

## 같이 보기

  - [X 윈도 시스템](https://ko.wikipedia.org/wiki/X_윈도_시스템 "wikilink")
  - [X 윈도 시스템 프로토콜 및 아키텍처](https://ko.wikipedia.org/wiki/X_윈도_시스템_프로토콜_및_아키텍처 "wikilink")

## 외부 링크

  - [Xlib의 짧은 강좌](http://tronche.com/gui/x/xlib-tutorial/)

  - [Xlib 함수 매뉴얼 문서](http://tronche.com/gui/x/xlib/function-index.html)

  - [Xlib - C 언어 X 인터페이스](http://www.x.org/docs/X11/xlib.pdf)

  - [X 윈도 및 모티프에 대한 켄튼 리의 문서](http://www.rahul.net/kenton/bib.html)

  - [Xlib의 긴 강좌](https://web.archive.org/web/20071018025425/http://users.actcom.co.il/~choo/lupg/tutorials/xlib-programming/xlib-programming.html#create_window)

  - [Xlib을 이용하여 화면 보호기 모듈 만들기](http://www.dis.uniroma1.it/%7eliberato/screensaver)

[분류:C 라이브러리](https://ko.wikipedia.org/wiki/분류:C_라이브러리 "wikilink") [분류:X 라이브러리](https://ko.wikipedia.org/wiki/분류:X_라이브러리 "wikilink")

1.