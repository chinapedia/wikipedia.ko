> This article is converted from Wikipedia: [Curses](https://ko.wikipedia.org/wiki/Curses).


**curses**는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제를 위한 [터미널](https://ko.wikipedia.org/wiki/컴퓨터_디스플레이 "wikilink") 제어 [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")의 하나로, [텍스트 사용자 인터페이스](../Page/텍스트_사용자_인터페이스.md "wikilink")(TUI) 응용 프로그램들의 구성을 가능케 한다.

이 이름은 "[커서](../Page/커서_\(사용자_인터페이스\).md "wikilink") 최적화"(cusor optimization)에서 따온 것이다. 문자 셀 터미널([VT100](https://ko.wikipedia.org/wiki/VT100 "wikilink") 따위) 상에서 응용 프로그램의 디스플레이를 관리하는 명령들이 모인 라이브러리이다.\[1\]

## 개요

curses API는 일부 장소에서 기술된다.\[2\] 대부분의 curses 구현물들은 수천 개의 다른 터미널의 기능을 기술할 수 있는 데이터베이스를 이용한다. PDCurses와 같은 일부 구현물들은 터미널 데이터베이스가 아닌 특별한 장치 드라이버를 사용한다. 대부분의 구현물들은 [terminfo](https://ko.wikipedia.org/wiki/terminfo "wikilink")을 이용하며 일부는 [termcap](https://ko.wikipedia.org/wiki/termcap "wikilink")을 이용한다. curses는 모든 셀 터미널과의 하위 호환성과 단순성의 이점이 있다. 비트맵 그래픽이나 여러 개의 글꼴이 필요 없는 응용 프로그램의 경우 curses를 이용하는 인터페이스 구현물은 X 툴킷을 이용하는 것보다 일반적으로 훨씬 더 단순하고 더 빠르다.

프로그래머들은 curses을 이용하여 특정 터미널 형태만을 위해 기록하지 않고도 텍스트 기반 응용 프로그램들을 기록할 수 있다. 시스템을 실행하는 curses 라이브러리는 터미널 형태를 기반으로 한 유효 [제어 문자를](../Page/제어_문자.md "wikilink") 전송한다.

## 예

  - [PDCurses](../Page/PDCurses.md "wikilink")
  - [ncurses](https://ko.wikipedia.org/wiki/ncurses "wikilink")

## 스크린샷

아래는 curses의 일반적인 예들을 나열한 것이다. (색을 지원하는 터미널 창) 뉴스리더 tin과 CD 처리 제품에 쓰인다.

파일:Tin_console.png|컬러 뉴스리더 인터페이스 파일:Jack-curses-screen.gif|Jack the Ripper에 쓰이는 curses

## 각주

<references />

## 외부 링크

  - [NCURSES - Manual Pages](http://invisible-island.net/ncurses/man/)
  - [Curses tutorial](http://heather.cs.ucdavis.edu/~matloff/UnixAndC/CLanguage/Curses.pdf) ([PDF](https://ko.wikipedia.org/wiki/Portable_Document_Format "wikilink") format)
  - [Public Domain Curses](http://pdcurses.sourceforge.net/)
  - [Interface for Rexx programmers](http://rexxcurses.sourceforge.net/)
  - [Tcl Toolkit](http://www.ch-werner.de/ck/)
  - [X/Open Curses](http://www.opengroup.org/onlinepubs/007908799/cursesix.html)
  - [Curses for Python](http://docs.python.org/library/curses.html)
  - [NetBSD Curses main manual page](http://netbsd.gw.com/cgi-bin/man-cgi?curses+3+NetBSD-current)

[분류:텍스트 사용자 인터페이스 라이브러리](https://ko.wikipedia.org/wiki/분류:텍스트_사용자_인터페이스_라이브러리 "wikilink") [분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink")

1.
2.  John Strang, *Programming with curses*, O'Reilly,