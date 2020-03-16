> This article is converted from Wikipedia: [Getty \(\)](https://ko.wikipedia.org/wiki/Getty_\(\)).


**`getty`**("get tty"의 준말)는 물리적 [터미널이나](../Page/단말기.md "wikilink") 가상 터미널(TTYs)을 관리하는 [호스트 컴퓨터에서](../Page/호스트_\(네트워크\).md "wikilink") 실행되는 [유닉스](../Page/유닉스.md "wikilink") 프로그램이다. 연결을 감지하면 사용자 인증을 위해 사용자 이름을 물어본 다음 '[login](../Page/로그인.md "wikilink")' 프로그램을 실행한다.

원래 전통적인 유닉스 시스템에서 getty는 호스트 컴퓨터에 연결된 일련의 터미널([텔레타이프](https://ko.wikipedia.org/wiki/텔레타이프 "wikilink") 머신)로의 연결을 관리하였다. *tty*라는 이름은 부분적으로 텔레타이프(teletype)를 의미하지만 어떠한 종류의 [터미널을](../Page/단말기.md "wikilink") 의미할 수도 있다. *getty* 프로세스는 하나의 터미널에 대해 서비스를 제공한다. 일부 시스템에서, 예를 들어 [솔라리스에서](../Page/솔라리스_\(운영_체제\).md "wikilink") *getty*는 [ttymon](https://ko.wikipedia.org/wiki/ttymon "wikilink")으로 대체되었다.

[유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제를](../Page/운영_체제.md "wikilink") 구동하는 [개인용 컴퓨터에서](../Page/개인용_컴퓨터.md "wikilink") 원격 로그인 서비스를 제공하지 않는다고 하더라도 로컬 [가상 콘솔에](https://ko.wikipedia.org/wiki/가상_콘솔 "wikilink") 로그인하는 수단으로 *getty*를 사용할 수 있다.

여러 ttys를 사이클링하는 일은 키 조합  \~ 을 통해 수행이 가능하다.\[1\]  키 조합은 tty를 종료하는데 사용하기도 한다.\[2\]

명령 줄 스타일 tty에서 X를 시작하는 일은 "startx" 명령어를 통해 수행할 수 있다.

*login* 프로그램 대신 *getty*는 그 밖의 모든 프로그램을 실행하기 위해 [시스템 관리자에](https://ko.wikipedia.org/wiki/시스템_관리자 "wikilink") 의해 설정이 가능한데, 이를테면 전화 접속 인터넷 연결을 제공하기 위한 pppd([점대점 프로토콜](../Page/점대점_프로토콜.md "wikilink") [데몬](../Page/데몬_\(컴퓨팅\).md "wikilink"))을 들 수 있다.

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [비지박스](../Page/비지박스.md "wikilink"): getty를 제공
  - [GNU 코어 유틸리티](../Page/GNU_코어_유틸리티.md "wikilink") (stty를 구현)
  - [util-linux](https://ko.wikipedia.org/wiki/util-linux "wikilink"): getty를 제공

## 각주

## 외부 링크

  -
  - [TTY](http://www.tldp.org/HOWTO/Text-Terminal-HOWTO-15.html)

[분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink")

1.
2.  [Ctrl+D](http://www.psych.upenn.edu/~saul/parasite/man/man4/tty.4.html)