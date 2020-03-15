> This article is converted from Wikipedia: [PuTTY](https://ko.wikipedia.org/wiki/PuTTY).


**PuTTY**(**퍼티**, {{\#tag:ref|영단어 [putty의](https://ko.wikipedia.org/wiki/wikt:en:putty "wikilink") 발음과 동일하다.\[1\]}})는 [SSH](https://ko.wikipedia.org/wiki/시큐어_셸 "wikilink"), [텔넷](../Page/텔넷.md "wikilink"), [rlogin](https://ko.wikipedia.org/wiki/rlogin "wikilink"), [raw TCP를](https://ko.wikipedia.org/wiki/전송_제어_프로토콜 "wikilink") 위한 [클라이언트](https://ko.wikipedia.org/wiki/클라이언트 "wikilink")로 동작하는 [자유 및 오픈 소스](https://ko.wikipedia.org/wiki/자유_및_오픈_소스_소프트웨어 "wikilink") [단말 에뮬레이터](../Page/단말_에뮬레이터.md "wikilink") 응용 프로그램이다. PuTTY라는 이름에는 특별한 뜻이 없으나\[2\] tty는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 전통의 터미널의 이름을 가리키며 [teletype를](https://ko.wikipedia.org/wiki/인쇄_전신기 "wikilink") 짧게 줄인 것이다.

PuTTY는 본래 [마이크로소프트 윈도용으로](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 작성되었으나 다른 다양한 [운영 체제에도](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") [포팅](https://ko.wikipedia.org/wiki/포팅 "wikilink")되었다. 공식 포팅은 일부 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 플랫폼에서 사용할 수 있으며 클래식 [맥 OS와](https://ko.wikipedia.org/wiki/맥_OS "wikilink") [맥 OS X으로의](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink") 포팅을 추진하고 있다. [심비안](https://ko.wikipedia.org/wiki/심비안 "wikilink")\[3\]\[4\], [윈도 모바일과](https://ko.wikipedia.org/wiki/윈도_모바일 "wikilink") 같은 운영 체제에 대한 비공식 포팅도 존재한다.

PuTTY는 [사이먼 테이썸이](https://ko.wikipedia.org/wiki/:en:Simon_Tatham "wikilink") 관리하고 있으며 현재는 [베타 소프트웨어이다](https://ko.wikipedia.org/wiki/베타_소프트웨어 "wikilink").

## 역사

PuTTY의 개발은 1998년 말로 거슬러 올라가며,\[5\] 2000년 10월부터 SSH-2 클라이언트가 되고 있다.\[6\]\[7\]

## 구성 요소

PuTTY는 여러 구성 요소로 이루어져 있다:

  - `PuTTY`: [텔넷](../Page/텔넷.md "wikilink"), [rlogin](https://ko.wikipedia.org/wiki/rlogin "wikilink"), [SSH](https://ko.wikipedia.org/wiki/시큐어_셸 "wikilink") 클라이언트 자체. [직렬 포트로](https://ko.wikipedia.org/wiki/직렬_포트 "wikilink") 연결할 수도 있다.
  - `PSCP`: [SCP](https://ko.wikipedia.org/wiki/시큐어_카피 "wikilink") 클라이언트. (예: 명령 줄 보안 파일 복사)
  - `PSFTP`: [SFTP](https://ko.wikipedia.org/wiki/SFTP "wikilink") 클라이언트. (예: [FTP와](https://ko.wikipedia.org/wiki/파일_전송_프로토콜 "wikilink") 비슷한 일반적인 파일 전송 세션)
  - `PuTTYtel`: 텔넷 전용 클라이언트
  - `Plink`: Putty 백엔드에 대한 명령 줄 인터페이스
  - `Pageant`: PuTTY, PSCP, Plink용 SSH 인증 에이전트
  - `PuTTYgen`: [RSA](https://ko.wikipedia.org/wiki/RSA "wikilink") 및 [DSA](https://ko.wikipedia.org/wiki/DSA "wikilink") 키 생성 유틸리티
  - `pterm`: 단독 터미널 에뮬레이터

## 각주

## 외부 링크

  - [프로젝트 홈페이지](http://www.chiark.greenend.org.uk/~sgtatham/putty/)
  -
  - PuTTY 개발 라이브러리
      - [W-PuTTY-CD, PuTTY Communications in a Microsoft Windows DLL](https://web.archive.org/web/20190819190155/http://winputty.com/)

[분류:통신 소프트웨어](https://ko.wikipedia.org/wiki/분류:통신_소프트웨어 "wikilink") [분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 터미널 에뮬레이터](https://ko.wikipedia.org/wiki/분류:자유_터미널_에뮬레이터 "wikilink")

1.  <http://www.chiark.greenend.org.uk/~sgtatham/putty/faq.html#faq-pronounce>
2.  <http://www.chiark.greenend.org.uk/~sgtatham/putty/faq.html#faq-meaning>
3.  <http://s2putty.sourceforge.net/>
4.
5.
6.  [PuTTY FAQ: Does PuTTY support SSH-2?](http://www.chiark.greenend.org.uk/~sgtatham/putty/faq.html#faq-ssh2)
7.  [PuTTY Change Log](http://www.chiark.greenend.org.uk/~sgtatham/putty/changes.html)