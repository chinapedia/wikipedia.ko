> This article is converted from Wikipedia: [CUPS](https://ko.wikipedia.org/wiki/CUPS).


**CUPS**(, 공식 명칭으로 CUPS가 더 자주 쓰임)는 컴퓨터를 인쇄 서버로 기능하도록 해주는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제를 위한 모듈 방식의 프린팅 시스템이다. CUPS는 [유닉스](../Page/유닉스.md "wikilink") 계열의 운영 체제에서 프린터 형식과 형태마다 독자적으로 써야 했던 장치 드라이버의 작성을 용이하게 해 주었는데, 과거 유닉스 계열 운영 체제가 지원하던 특수 라인 프린터와 포스트 스크립트 프린터 뿐만 아니라, [매킨토시](../Page/매킨토시.md "wikilink"), [윈도용으로](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 시판되는 프린터의 대부분을 유닉스 계열 운영 체제에서 사용할 수 있게 하였다.

CUPS를 사용하는 컴퓨터는 클라이언트 컴퓨터에서 인쇄 작업을 수신하는 서버가 되어, 해당 작업을 처리하고 적절한 프린터로 자료를 보낸다. 또한 그 때에는 HTTP의 Basic 인증 및 Digest 인증, 로컬 인증, 128비트 TLS/SSL 암호화 등을 이용할 수도 있다.

CUPS는 유닉스 인쇄 스풀러와 스케줄러 필터 시스템 및 백엔드 시스템으로 구성된다. 이 중 필터 시스템은 인쇄 데이터를 프린터가 인식할 수 있는 형식으로 변환하고, 백엔드 시스템이 이 데이터를 프린터로 보내는 역할을 수행한다. CUPS는 인쇄 작업과 대기열을 취급하는 기반으로 IPP (Internet Printing Protocol)을 이용하고 있다. 또한, CUPS는 유닉스에서 기존에 지원하던 System V 형식과 BSD 형식의 커멘드라인 인터페이스도 지원하고 SMB 프로토콜도 부분적으로 지원한다. CUPS가 제공하는 장치 드라이버는 [어도비](https://ko.wikipedia.org/wiki/어도비 "wikilink")의 PPD (PostScript Printer Description) 형식의 텍스트 파일을 이용하여 설정이 가능하다. CUPS를 설정하는 CUPS 스스로는 웹(HTTP)을 이용한 임베디드 인터페이스를 지원하고 있다.

## 히스토리

컵스(CUPS)는 [애플](../Page/애플.md "wikilink")에서 개발한 오픈소스형태의 프린터관련 소프트웨어이다.\[1\]

## 관련 자료

  - Sweet, Michael (July 10, 2000). [CUPS overview](https://web.archive.org/web/20041225054134/http://www.cups.org/overview.html). *Easy Software Products*.
  - [CUPS software administration manual : Managing printers from the web](https://web.archive.org/web/20041225043927/http://www.cups.org/sam.html#4_4) (version 1.1.21, 2004). *Easy Software Products*. Retrieved January 5, 2005.
  - <https://web.archive.org/web/20060613001400/http://www.cups.org/articles.php> How-to articles and FAQs about using CUPS
  - [Design of CUPS Filtering System — including the context for Mac OS X ("Jaguar")](http://www.linuxprinting.org/CUPS-Filter-Chart.html). *LinuxPrinting.org*. Retrieved January 5, 2005.
  - [KDE](../Page/KDE.md "wikilink"). *[KDEPrint information](https://web.archive.org/web/20050207054956/http://printing.kde.org/info/)*. KDE-printing website. Retrieved January 14, 2005.

## 참조

<references />

## 외부 링크

  - [공식 웹사이트](http://www.cups.org/)
  - [오픈프린팅](http://www.linux-foundation.org/en/OpenPrinting)
  - [유니버셜 플러그 앤 플레이 – 프린터 디바이스 V 1.0와 프린터 베이직 서비스 V 1.0](https://web.archive.org/web/20081017120654/http://upnp.org/standardizeddcps/printer.asp)

[분류:장치 드라이버](https://ko.wikipedia.org/wiki/분류:장치_드라이버 "wikilink") [분류:애플 인수 기업](https://ko.wikipedia.org/wiki/분류:애플_인수_기업 "wikilink") [분류:1999년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1999년_소프트웨어 "wikilink") [분류:애플의 소프트웨어](https://ko.wikipedia.org/wiki/분류:애플의_소프트웨어 "wikilink")

1.  (CUPS 2.2.7- CUPS is the standards-based, open source printing system developed by Apple Inc. for macOS® and other UNIX®-like operating systems.)https://www.cups.org/