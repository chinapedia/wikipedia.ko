> This article is converted from Wikipedia: [Twm](https://ko.wikipedia.org/wiki/Twm).


**twm**(Tom's Window Manager → Tab Window Manager → Timeless Windows Manager)은 [X 윈도 시스템의](../Page/X_윈도_시스템.md "wikilink") 초창기 [창관리자](https://ko.wikipedia.org/wiki/창관리자 "wikilink") 가운데 하나다. Tom LaStrange가 만들었다. 사용자 입맛대로 고칠 수 있는 부분이 많으며 처음 나왔을 때는 혁신적인 [창관리자](https://ko.wikipedia.org/wiki/창관리자 "wikilink")로 평가되기도 했으며 [X윈도](https://ko.wikipedia.org/wiki/X윈도 "wikilink")의 개발에 큰 영향을 주었다. [C](../Page/C.md "wikilink")로 만들어졌으며 [GTK+](../Page/GTK+.md "wikilink"), [Qt같은](https://ko.wikipedia.org/wiki/Qt_\(툴킷\) "wikilink") 별도의 툴킷을 쓰지 않고 [xlib](https://ko.wikipedia.org/wiki/xlib "wikilink")을 직접 썼다. [크노픽스](../Page/크노픽스.md "wikilink")가 twm을 기본으로 탑재하고 있다.

[MIT 라이선스를](https://ko.wikipedia.org/wiki/MIT_라이선스 "wikilink") 따르며 2009년 1월 29일 기준 최신판은 **1.0.4**다.

## 걸어온 길

twm은 1987년 Evans and Sutherland에서 일하던 Tom LaStrange가 [UWM](https://ko.wikipedia.org/wiki/UWM "wikilink")에 불만을 느껴 만들었고 1988년 6월 13일 X11R1용 twm이 [유즈넷](../Page/유즈넷.md "wikilink")의 comp.unix.sources를 통해 나왔다.

9달 뒤 MIT X Consortium의 Jim Fulton이 Tom LaStrange를 만났고 Tom LaStrange는 X Consortium으로 하여금 twm을 관리하게 했다. Jim Fulton은 twm을 Inter-Client Communication Conventions Manual에 맞게 바꿨으며 Keith Packard가 제목 틀(타이틀바)을 덧붙였다. 그 뒤 twm은 X11R4의 기본 GUI가 되었다.

twm은 처음에는 Tom's Window Manager의 줄임말이었고 X Consortium에서 twm을 관리하게 된 뒤 몇몇 사람들의 의견으로 Tab Window Manager의 줄임말이 되었다. vtwm.gamma 파일에는 "Tom LaStrange가 twm 관리를 그만둔 뒤 twm에 일어난 심한 변화들 때문에 Tom LaStrange가 여론의 뭇매를 맞게 하지 않기 위해 twm을 Tab Window Manager라는 뜻으로 바꾸었다."라고 쓰여 있다. Jim Fulton은 Tab이라는 단어를 쓴 이유로 T로 시작한다는 것과 제목 틀이 폴더(컴퓨터 폴더를 가리키는 것이 아님. 회사에서 쓰는, 보고서 따위의 문서를 끼워넣는 폴더)의 탭같이 생겼다는 것을 들었다.

그 뒤 한동안 관리가 없다가 오늘날 Eeri Kask가 관리를 맡게 되면서 twm의 뜻은 Timeless Windows Manager로 바뀌었다.

## 쓰는 법

  - twm 안에서 뜨는 창들은 제목 틀(타이틀바)에 두 개의 단추(버튼)를 가지고 있다.

<!-- end list -->

  -   - 최소화(왼쪽 끝의 동그라미): 창을 최소화한다. 최소화한 창은 이름이 적혀 있는 아이콘의 형태를 갖는다.
      - 크기 바꾸기(오른쪽 끝의 3겹 네모): 이 단추를 누른 채로 마우스를 끌어 창의 크기를 바꾼다.

<!-- end list -->

  - twm 안에서 뜨는 창들은 기본적으로 끝내기 단추가 없다. 다만 주 메뉴에 Kill(강제로 끝내기) 항목이 있다.
  - 주 메뉴는 바탕화면에서 마우스 왼쪽 단추를 누르면 나온다. 단추를 놓자마자 메뉴가 바로 사라지기 때문에 항목을 고를 때 단추를 누르고 있어야 된다.
  - 마우스 가운데 단추는 창 옮기기 기능을 하며 마우스 오른쪽 단추는 해당 창을 여러 개의 창 가운데 맨 뒤로 가리는 기능을 한다.
  - 커서를 창에 대기만 해도 그 창이 활성화된다.
  - 새 창이 만들어질 때 가로 3칸 × 세로 3칸인 격자가 나타난다. 이때 커서를 원하는 곳으로 끌고 가서 마우스 왼쪽 단추를 누르면 그 자리에 새 창이 나타난다. 마우스 가운데 단추로 격자의 크기를 바꿀 수 있으며 마우스 오른쪽 단추를 누르면 새 창이 세로로 양 끝까지 늘어난 채로 나타난다.

위의 내용들은 사용자의 설정에 따라 달라질 수 있다.

## 외부 링크

  - [freedesktop.org twm Git 사이트](http://cgit.freedesktop.org/xorg/app/twm/)

[분류:그래픽 사용자 인터페이스](https://ko.wikipedia.org/wiki/분류:그래픽_사용자_인터페이스 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:X 윈도 시스템](https://ko.wikipedia.org/wiki/분류:X_윈도_시스템 "wikilink") [분류:1987년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1987년_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")