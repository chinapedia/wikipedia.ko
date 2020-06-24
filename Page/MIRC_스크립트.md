> This article is converted from Wikipedia: [MIRC 스크립트](https://ko.wikipedia.org/wiki/MIRC_스크립트).


**mIRC 스크립트**()는 [윈도용](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [IRC](https://ko.wikipedia.org/wiki/IRC "wikilink") 클라이언트인 [mIRC](https://ko.wikipedia.org/wiki/mIRC "wikilink")에서 지원하는 [스크립트 언어이다](../Page/스크립트_언어.md "wikilink").

mIRC 스크립트는 적게는 사용자의 편의를 위한 줄임글 명령 정의로부터, 자동 채널 관리, 게임, 재미를 위한 기능을 비롯해 크게는 거대한 응용 프로그램을 만드는 데까지 여러 용도로 사용된다. mIRC 사용자들 사이에서 관련된 포럼이 몇몇 형성되어 있다.

## 구성

mIRC 스크립트는 일반적인 텍스트 파일로, .mrc [확장자를](../Page/파일_확장자.md "wikilink") 쓰거나 [INI 파일로](../Page/INI_파일.md "wikilink") 저장된다. mIRC 내에서도 스크립트 편집기([Alt](https://ko.wikipedia.org/wiki/Alt_글쇠 "wikilink")-A,R,P)를 통해 스크립트를 편집할 수 있다.

mIRC 스크립트는 [사건 기반 프로그래밍 언어에](https://ko.wikipedia.org/wiki/사건_기반_프로그래밍 "wikilink") 속한다. mIRC 스크립트는 호출되는 시점에 따라서 줄임글(alias, 사용자가 특정한 명령을 입력했을 때), 자동 반응(remote, IRC 서버에서 특정한 명령이 날아 왔을 때), 그리고 팝업 메뉴(popup menu, 메뉴를 클릭했을 때)로 나눌 수 있다.

언어 자체는 단어 단위로 [해석되며](https://ko.wikipedia.org/wiki/구문_해석 "wikilink"), [명령들의](../Page/명령형_프로그래밍.md "wikilink") 집합으로 구성된다. 명령 중에 스크립트에서 정의한 것은 줄임글(alias)이라 불린다. 명령의 인자에 $, &, %로 시작하는 단어가 있으면 그 단어는 특수하게 해석되는데, $는 값을 반환하는 [함수로](https://ko.wikipedia.org/wiki/서브루틴 "wikilink") 식별자(identifier)라 불리며, &는 이진 변수, %는 일반 변수를 나타낸다. 명령 자체에는 아무 기호도 붙지 않지만 사용자가 채팅 창에서 직접 입력해야 할 경우 /, //, /. 등의 접두사를 붙여야 한다. 명령 중에는 [while과](https://ko.wikipedia.org/wiki/while문 "wikilink") 같이 명령 블록을 필요로 하는 것도 있는데, 이런 경우 {와 }로 감싸서 명령 블록을 표시한다.

변수는 [옥텟](../Page/옥텟_\(컴퓨팅\).md "wikilink") 문자열을 담는 이진 변수와 [자료형](../Page/자료형.md "wikilink")이 바뀔 수 있는 임의의 값을 담는 일반 변수로 나뉜다. 이진 변수는 [어디서나 접근할](../Page/전역_변수.md "wikilink") 수 있으며, 일반 변수는 서브루틴에서 [지역 변수로](../Page/지역_변수.md "wikilink") 선언되지 않으면 전역 변수로 인식한다. mIRC 스크립트는 [약형](https://ko.wikipedia.org/wiki/약형 "wikilink") 언어로, 서로 다른 변수 사이에 연산이 일어나면 자동으로 형 변환이 일어난다.

mIRC 스크립트에서 기본으로 지원하는 명령 및 식별자는 IRC 제어로부터 계산, [GUI까지](../Page/그래픽_사용자_인터페이스.md "wikilink") 다양하다. 스크립트만으로 처리하기 힘들거나 느린 경우에는 외부의 [DLL 파일이나](../Page/동적_링크_라이브러리.md "wikilink") [COM 객체를](../Page/컴포넌트_오브젝트_모델.md "wikilink") 사용할 수 있다.

## 예제

다음은 [Hello World 프로그램이다](https://ko.wikipedia.org/wiki/Hello_World_프로그램 "wikilink"). 사용자가 /hello를 입력하면 채팅 창에 문자열이 출력된다.

    alias hello {
      echo -a Hello World!
    }

다음은 /ten을 입력하면 1부터 10까지를 채팅창에 출력하는 프로그램으로, 반복문과 지역 변수의 예를 보여 준다.

    alias ten {
      var %i = 1
      while (%i <= 10) {
        echo -a %i
        inc %i
      }
    }

다음은 자동 반응 스크립트의 예이다. \#IRChelp라는 채널에 입장(JOIN 명령)하면 입장한 사람에게 인사를 한다. 단어 단위로 해석되므로 ‘$nick님’이라고 쓸 수 없음을 주목하라.

    on *:JOIN:#IRChelp:{
      msg $chan $nick $+ 님 안녕하세요~
    }

다음은 그림 [창을](../Page/창_\(컴퓨팅\).md "wikilink") 띄우는 프로그램이다.

    alias cir {
      var %x = 0
      window -ek0p @cir
      while (%x < 360) {
        inc %x
        drawdot @cir 4 2 $calc(($cos(%x)*50)+200) $calc(($sin(%x)*50)+200)
      }
    }

## 외부 링크

  - [공식 mIRC 홈페이지](http://www.mirc.com/)

  -
  - [mIRC 온라인 매뉴얼](https://web.archive.org/web/20130618184758/http://wi-fizzle.com/mircdocs/) — 단일 문서 HTML 포맷에 관한 설명

[분류:전문 영역 언어](https://ko.wikipedia.org/wiki/분류:전문_영역_언어 "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink")