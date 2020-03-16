> This article is converted from Wikipedia: [HQ9+](https://ko.wikipedia.org/wiki/HQ9+).


**HQ9+**는 몇몇 종류의 [컴퓨터 프로그램을](../Page/컴퓨터_프로그램.md "wikilink") 만드는 데 매우 효과적인, 간단하고 세련된 [난해한 프로그래밍 언어이다](../Page/난해한_프로그래밍_언어.md "wikilink"). 클리프 비플(Cliff L. Biffle)가 [2000년](../Page/2000년.md "wikilink")경에 만들었다. 언어의 이름에서 알 수 있듯이, 이 언어는 네 개의 한 글자 명령어, 즉 H, Q, 9, +를 가지고 있다.

  - H 명령은 ‘[Hello, world\!](https://ko.wikipedia.org/wiki/Hello_world_프로그램 "wikilink")’를 출력한다.
  - Q 명령은 프로그램의 [소스 코드를](../Page/소스_코드.md "wikilink") 출력한다. ([콰인 (전산학)의](https://ko.wikipedia.org/wiki/콰인 "wikilink") 역할을 한다)
  - 9 명령은 [99병의 맥주](../Page/99병의_맥주.md "wikilink")(99 Bottles of Beer on the Wall) 노래의 가사를 출력한다.
  - \+ 명령은 [가산기](../Page/가산기.md "wikilink")를 증가시킨다. 그러나 가산기의 값에 접근할 방법이 없어 입출력 관점으로는 [NOP](../Page/NOP.md "wikilink") 명령과 동일하며, 그 다음에 나올 언어 HQ9++의 '++' 명령도 마찬가지다.

예를 들어서 `HHQ+HQ++`라는 코드는 올바른 HQ9+ 프로그램이다. 이 프로그램은

    Hello, world! Hello, world! HHQ+HQ++ Hello, world! HHQ+HQ++

를 출력하면서 가산기를 세 번 증가시킬 것이다.

실제로 HQ9+로 유용한 프로그램을 만들 수는 없으며, [난해한 프로그래밍 언어로](../Page/난해한_프로그래밍_언어.md "wikilink") 분류된다. 각각의 명령들은 새로운 [프로그래밍 언어를](../Page/프로그래밍_언어.md "wikilink") 배우는 초보자들이 하는 공통적인 과제를 표시한다. 예를 들어서, ‘[Hello, world\!](https://ko.wikipedia.org/wiki/Hello_world_프로그램 "wikilink")’라는 문장을 만드는 프로그램은 언어를 처음 배울 때 하는 과제인데, 몇몇 [프로그래밍 언어는](../Page/프로그래밍_언어.md "wikilink") 이런 일을 하기가 상당히 어렵지만 HQ9+에서는 H 명령으로 해결할 수 있는 매우 기초적인 과제이다. 많은 프로그래밍 언어에서 가장 어려운 과제는 [콰인 (전산학)](https://ko.wikipedia.org/wiki/콰인 "wikilink"), 즉 자기 자신의 소스 코드를 출력하는 프로그램을 만드는 것이지만 HQ9+에서는 이 또한 자명하다.

HQ9+ [인터프리터](../Page/인터프리터.md "wikilink")는 만들기 매우 쉬우며, 여러 언어로 많이 만들어져 있다. 하지만 HQ9+ 프로그램은 입력을 받을 수 없기 때문에 HQ9+로 HQ9+ 인터프리터나 컴파일러를 만드는 것은 불가능하다.

## HQ9++

**HQ9++**는 데이비드 모르간-마르(Davia Morgan-mar)에 의해 만들어진 HQ9+의 확장이다. 이 언어는 HQ9+와 하위 호환성을 유지하는 [객체 지향적인](../Page/객체_지향_프로그래밍.md "wikilink") 언어이다. 여기에는 [가산기](../Page/가산기.md "wikilink")를 두 번 증가시키면서 객체의 새 인스턴스를 만드는 새로운 명령 `++`이 추가되었으며, [정보 은닉의](https://ko.wikipedia.org/wiki/정보_은닉 "wikilink") 원리에 따라서 이 객체에 접근하는 것은 불가능하다.

## HQ9+-

**HQ9+-**는 이반 멜리캠프(Ivan Meilkamp)에 의해 만들어진 HQ9++의 확장이다. HQ9+ 및 HQ9++와 하위 호환성을 유지한다. HQ9++의 다섯 명령을 모두 가지고 있으며, 여기에 오류를 일으키는 새로운 명령어 `-`가 추가되었다. 이것의 기능은 선행하는 연산자에 따라 달라진다.

  - 프로그램의 처음에 올 경우, 그것은 [구문 오류이다](https://ko.wikipedia.org/wiki/구문_오류 "wikilink").
  - H 명령어의 다음에 올 경우, 입출력 오류를 일으킨다.
  - Q 명령어의 다음에 올 경우, [무한 피드백에](https://ko.wikipedia.org/wiki/무한_피드백 "wikilink") 빠진다.
  - 9 명령어의 다음에 올 경우, [무한 루프에](https://ko.wikipedia.org/wiki/무한_루프 "wikilink") 빠진다.
  - \+ 명령어의 다음에 올 경우, 1을 0으로 나눈다.
  - \++ 명령어의 다음에 올 경우, 객체가 상위 클래스를 하위 클래스로 가지게 된다. 정보 은닉의 원리에 따라 이것을 막는 것은 불가능하다.

## 외부 링크

  - [HQ9+](https://web.archive.org/web/20041214033417/http://www.cliff.biffle.org/esoterica/hq9plus.html)

  - [HQ9++](http://www.dangermouse.net/esoteric/hq9plusplus.html)

  - [DM's Esoteric Programming Languages](http://www.dangermouse.net/esoteric/)

  - [HQ9+-](http://melikamp.com/features/hq9pm.shtml)

[분류:난해한 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:난해한_프로그래밍_언어 "wikilink")