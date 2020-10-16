> This article is converted from Wikipedia: [XCB](https://ko.wikipedia.org/wiki/XCB).


[섬네일](https://ko.wikipedia.org/wiki/파일:Xlib_and_XCB_in_the_X_Window_System_graphics_stack.svg "wikilink") **XCB**(X protocol C-language Binding)는 [컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 [X 윈도 시스템을](../Page/X_윈도_시스템.md "wikilink") 위한 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") [언어 결합이다](https://ko.wikipedia.org/wiki/언어_결합 "wikilink"). [자유 소프트웨어로](../Page/자유_소프트웨어.md "wikilink") 구현되어 있으며 [Xlib](../Page/Xlib.md "wikilink")을 대체하는 것을 목적으로 한다. 이 프로젝트는 2001년 Bart Massey가 시작하였다.

**Xlib/XCB**는 점진적인 이식 경로를 통해 Xlib와 XCB에 대한 [응용 프로그램 이진 인터페이스](../Page/응용_프로그램_이진_인터페이스.md "wikilink") 호환성을 제공한다. Xlib/XCB는 Xlib 프로토콜 계층을 사용하지만 Xlib 전송 계층을 XCB로 대체하며 XCB를 직접 이용할 수 있도록 기반 XCB 연결로의 접근을 제공한다. 대부분의 운영 체제는 X11 구현을 위해 Xlib/XCB를 사용하는데, 그 까닭은 여러 라이브러리들을 통해 응용 프로그램이 [X 서버로의](https://ko.wikipedia.org/wiki/X_서버 "wikilink") 연결을 개시하여 XCB와 Xlib를 둘 다 사용할 수 있기 때문이다.\[1\]\[2\]

## 목적

XCB의 주 목적은 다음과 같다:

  - 라이브러리 크기와 복잡성을 줄이기 위해
  - [X11 프로토콜로의](https://ko.wikipedia.org/wiki/X_윈도_코어_프로토콜 "wikilink") 직접 접근을 제공하기 위해

## 예

``` c
/* 창 안에 상자를 그려내는 단순 XCB 응용 프로그램입니다 */
/* 컴파일하려면 다음을 사용하세요:
 gcc -Wall x.c -lxcb
*/
#include <xcb/xcb.h>
#include <stdio.h>
#include <stdlib.h>

int main(void) {
  xcb_connection_t    *c;
  xcb_screen_t        *s;
  xcb_window_t         w;
  xcb_gcontext_t       g;
  xcb_generic_event_t *e;
  uint32_t             mask;
  uint32_t             values[2];
  int                  done = 0;
  xcb_rectangle_t      r = { 20, 20, 60, 60 };

                        /* 서버 연결 개시 */
  c = xcb_connect(NULL,NULL);
  if (xcb_connection_has_error(c)) {
    printf("display를 열 수 없습니다\n");
    exit(1);
  }
                        /* 최초의 화면 가져오기 */
  s = xcb_setup_roots_iterator( xcb_get_setup(c) ).data;

                       /* 검은 그래픽 환경 만들기 */
  g = xcb_generate_id(c);
  w = s->root;
  mask = XCB_GC_FOREGROUND | XCB_GC_GRAPHICS_EXPOSURES;
  values[0] = s->black_pixel;
  values[1] = 0;
  xcb_create_gc(c, g, w, mask, values);

                       /* 창 만들기 */
  w = xcb_generate_id(c);
  mask = XCB_CW_BACK_PIXEL | XCB_CW_EVENT_MASK;
  values[0] = s->white_pixel;
  values[1] = XCB_EVENT_MASK_EXPOSURE | XCB_EVENT_MASK_KEY_PRESS;
  xcb_create_window(c, s->root_depth, w, s->root,
                    10, 10, 100, 100, 1,
                    XCB_WINDOW_CLASS_INPUT_OUTPUT, s->root_visual,
                    mask, values);

                        /* 창 보이기 */
  xcb_map_window(c, w);

  xcb_flush(c);

                        /* 이벤트 루프 */
  while (!done && (e = xcb_wait_for_event(c))) {
    switch (e->response_type & ~0x80) {
    case XCB_EXPOSE:    /* 창을 (다시) 그리기 */
      xcb_poly_fill_rectangle(c, w, g,  1, &r);
      xcb_flush(c);
      break;
    case XCB_KEY_PRESS:  /* 키가 눌릴 때 끝내기 */
      done = 1;
      break;
    }
    free(e);
  }
                        /* 서버 연결 닫기 */
  xcb_disconnect(c);

  return 0;
}
```

이 예제에서 볼 수 있듯이 XCB는 [Xlib와](https://ko.wikipedia.org/wiki/Xlib#예 "wikilink") 동등하지만 그 보다 살짝 낮은 수준의 API를 가지고 있다.

## 프로토콜 정의

XCB 제작자들은 전문화된 [인터페이스 정의 언어를](../Page/인터페이스_정의_언어.md "wikilink") 만들어서 언어 중립적인 방식으로 X11 프로토콜을 모델링하고 다른 프로그래밍 언어들과의 바인딩을 쉽게 할 수 있게 하였다. libxcb 그 자체는 코드 발생기로서 구현되어 있다.

예:

``` xml
<xcb header="bigreq" extension-xname="BIG-REQUESTS"
    extension-name="BigRequests" extension-multiword="true"
    major-version="0" minor-version="0">

  <request name="Enable" opcode="0">
    <reply>
      <pad bytes="1" />
      <field type="CARD32" name="maximum_request_length" />
    </reply>
  </request>
</xcb>
```

## 로고

XCB 로고는 Neko the Kitty [웹툰](../Page/웹툰.md "wikilink") 작가 Gearóid Molloy가 만들어 프로젝트에 기부한 것이다.\[3\]

## 기타 언어 바인딩

  - [xpyb](http://xcb.freedesktop.org/XcbPythonBinding/) - XCB를 이용한 X 윈도 시스템으로의 [파이썬](../Page/파이썬.md "wikilink") 바인딩. 2013년 6월 기준으로 python3를 지원하지 않는다. [freedesktop.org](https://ko.wikipedia.org/wiki/freedesktop.org "wikilink") 제공.

## 참조

<references />

## 참고 문헌

  -
  -
  -
## 외부 링크

  - [XCB 위키](http://xcb.freedesktop.org/) ([freedesktop.org](https://ko.wikipedia.org/wiki/freedesktop.org "wikilink"))

  - [XCB API 참조](http://xcb.freedesktop.org/XcbApi/) - [강좌](http://xcb.freedesktop.org/tutorial/)

  - [libxcb 강좌](http://www.x.org/releases/current/doc/libxcb/tutorial/index.html)

  - [출판물](http://xcb.freedesktop.org/Publications)

[분류:X 라이브러리](https://ko.wikipedia.org/wiki/분류:X_라이브러리 "wikilink") [분류:X 윈도 시스템](https://ko.wikipedia.org/wiki/분류:X_윈도_시스템 "wikilink") [분류:Freedesktop.org](https://ko.wikipedia.org/wiki/분류:Freedesktop.org "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink")

1.
2.
3.  [KittyLogo](http://xcb.freedesktop.org/KittyLogo/) (xcb.freedesktop.org)