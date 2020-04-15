> This article is converted from Wikipedia: [웹 기반 SSH](https://ko.wikipedia.org/wiki/웹_기반_SSH).


**웹 기반 [시큐어 셸](../Page/시큐어_셸.md "wikilink")**(Web-based SSH)은 표준 [웹 브라우저를](../Page/웹_브라우저.md "wikilink") 통해 [시큐어 셸](../Page/시큐어_셸.md "wikilink") (SSH) 서버 접속을 가능하게 하는 셸이다.

자바스크립트와 AJAX 가능한 모든 브라우저에서 실행되며 언제 컴퓨터나 아이폰이나 스마트폰에서 사용할 수 있다. 서버는 파이썬으로 작성되며 리눅스,맥 OS X, BSD와, 솔라리스 등 파이썬 2.3이 실행되는데에 설치하는 것은 매우 쉽다. 이 셸은 Ajaxterm을 기반으로 한다.

## 기술

웹 기반 SSH 클라이언트는 기본적으로 다음 부분으로 구성된다:

  - 클라이언트 사이드. 일반적으로 [자바스크립트](../Page/자바스크립트.md "wikilink")와 동적 [HTML](../Page/HTML.md "wikilink") 페이지를 사용하여 키눌림을 포착하고 메시지를 서버로 전송하며 사용자의 [웹 브라우저에](../Page/웹_브라우저.md "wikilink") 결과를 표출한다.
  - 서버 사이드/웹 애플리케이션. 들어오는 요청은 [웹 애플리케이션 서버에서](../Page/웹_애플리케이션_서버.md "wikilink") 처리된다. 키보드 이벤트는 연결된 SSH 서버와 통신하는 시큐어 셸 클라이언트로 포워드된다. 터미널 출력은 [자바스크립트](../Page/자바스크립트.md "wikilink")를 통해 HTML로 변환되도록 클라이언트에 전달되거나, 서버에서 [HTML](../Page/HTML.md "wikilink")로 변환한 다음 클라이언트로 전송된다.

### 클라이언트 사이드 터미널 에뮬레이션

클라이언트 사이드 터미널 에뮬레이션을 이용하는 웹 기반 SSH 서버는 일반적으로 SSH 서버로부터 직접 순수 터미널 출력을 클라이언트로 전달한다.

클라이언트 사이드 터미널 에뮬레이션의 예: vt1000.js\[1\]

### 서버 사이드 터미널 에뮬레이션

서버 사이드 터미널 에뮬레이션을 사용하는 웹 기반 SSH 서버는 일반적으로 터미널 화면과 메모리 내 상태를 추적한 다음 화면 업데이트 발생 시 또는 클라이언트가 업데이트를 요청 시 이를 HTML로 변환한다.

서버 사이드 터미널 에뮬레이션의 예: terminal.py\[2\]

## 같이 보기

  - [시큐어 셸](../Page/시큐어_셸.md "wikilink")

## 각주

[분류:암호 프로토콜](https://ko.wikipedia.org/wiki/분류:암호_프로토콜 "wikilink") [분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink")

1.  <http://code.google.com/p/shellinabox/source/browse/demo/vt100.js>
2.  <https://liftoff.github.io/GateOne/Developer/terminal.html>