> This article is converted from Wikipedia: [UnixODBC](https://ko.wikipedia.org/wiki/UnixODBC).


**unixODBC**는 [ODBC](../Page/ODBC.md "wikilink") [API](../Page/API.md "wikilink")를 구현하는 [오픈 소스](../Page/오픈_소스.md "wikilink") 프로젝트이다. 코드는 [GNU 일반 공중 사용 허가서](../Page/GNU_일반_공중_사용_허가서.md "wikilink")/[LGPL](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink") 하에 제공되며 [유닉스](../Page/유닉스.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), IBM [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), 마이크로소프트 [Interix](https://ko.wikipedia.org/wiki/Interix "wikilink") 등 각기 다른 여러 운영 체제에서 빌드하여 사용할 수 있다.

프로젝트의 목표는 다음과 같다:

  - 최소한의 코드 변경으로 [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink") ODBC 애플리케이션을 다른 플랫폼으로 포팅할 수 있는 도구를 개발자들에게 제공한다.
  - 프로젝트를 벤더 중립적인 인터페이스 데이터베이스 [SDK로](../Page/소프트웨어_개발_키트.md "wikilink") 유지보수한다.
  - ODBC 드라이버를 개발하는 사람들에게 드라이버를 윈도우가 아닌 플랫폼으로 포팅하는 도구를 제공한다.
  - 데이터베이스 접근 관리를 위한 GUI 및 명령 줄 도구 집합을 사용자에게 제공한다.
  - 상호 운용성을 보증하기 위해 [자유 소프트웨어 커뮤니티와](https://ko.wikipedia.org/wiki/자유_소프트웨어_운동 "wikilink") 상용 데이터베이스 벤더들의 연결고리를 관리한다.

## 역사

unixODBC 프로젝트는 1999년 초 Peter Harvey에 의해 처음 언급되었으며 당시 [iODBC](https://ko.wikipedia.org/wiki/iODBC "wikilink")(또다른 오픈 소스 [ODBC](../Page/ODBC.md "wikilink")) 개발자들이 코드의 LGPL화에 대한 의지가 없었고 현재의 ODBC 3 API 사양을 포함하도록 API를 확장하면서도 GUI 기반 구성 도구의 추가를 고려하지 않던 찰라에 만들어졌다. 지금은 [iODBC](https://ko.wikipedia.org/wiki/iODBC "wikilink")가 이 부분들을 추가하고 있으며, ODBC 인터페이스를 사용하는 애플리케이션들은 대부분의 경우 큰 변경 없이 iODBC와 unixODBC를 둘 다 사용할 수 있으며 이는 두 프로젝트들이 하나의 ODBC 사양을 고수했기 때문에 가능하였다.

## 외부 링크

  - [unixODBC homepage](http://www.unixODBC.org/)
  - [UnixODBC & MySQL Sample Program](http://compscinotes.wordpress.com/2010/04/18/unixodbc-mysql-sample-program/)

[분류:데이터베이스 API](https://ko.wikipedia.org/wiki/분류:데이터베이스_API "wikilink")