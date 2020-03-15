> This article is converted from Wikipedia: [FastCGI](https://ko.wikipedia.org/wiki/FastCGI).


**FastCGI**는 상호 작용 프로그램을 [웹 서버와](https://ko.wikipedia.org/wiki/웹_서버 "wikilink") 통신하기 위한 [바이너리 프로토콜이다](https://ko.wikipedia.org/wiki/바이너리_프로토콜 "wikilink"). FastCGI는 초기 [공용 게이트웨이 인터페이스](https://ko.wikipedia.org/wiki/공용_게이트웨이_인터페이스 "wikilink")(CGI)의 변형이다. FastCGI의 주 목적은 웹 서버와 [CGI](https://ko.wikipedia.org/wiki/공용_게이트웨이_인터페이스 "wikilink") 프로그램 간 통신 시 발생되는 부하를 줄임으로써 서버가 한 번에 더 많은 웹 페이지 요청을 관리할 수 있게 하는 것이다.

## FastCGI를 구현하는 웹 서버

  - [아파치 HTTP 서버](https://ko.wikipedia.org/wiki/아파치_HTTP_서버 "wikilink") (부분적)
  - 캐디(Caddy)\[1\]
  - [Cherokee](https://ko.wikipedia.org/wiki/Cherokee "wikilink")\[2\]
  - [Hiawatha](https://ko.wikipedia.org/wiki/Hiawatha "wikilink")\[3\]
  - [제티](../Page/제티_\(웹_서버\).md "wikilink")\[4\]
  - [Kerio WebSTAR](https://ko.wikipedia.org/wiki/Kerio_WebSTAR "wikilink")
  - [Lighttpd](https://ko.wikipedia.org/wiki/Lighttpd "wikilink")\[5\]
  - [라이트스피드 웹 서버](https://ko.wikipedia.org/wiki/라이트스피드_웹_서버 "wikilink")
  - [인터넷 정보 서비스](https://ko.wikipedia.org/wiki/인터넷_정보_서비스 "wikilink")\[6\]
  - [Nginx](https://ko.wikipedia.org/wiki/Nginx "wikilink")
  - [내비서버](https://ko.wikipedia.org/wiki/내비서버 "wikilink")(NaviServer)
  - [Oracle iPlanet Web Server](https://ko.wikipedia.org/wiki/Oracle_iPlanet_Web_Server "wikilink")
  - [OpenBSD](https://ko.wikipedia.org/wiki/OpenBSD "wikilink")의 [`httpd(8)`](http://man.openbsd.org/OpenBSD-current/man8/httpd.8)\[7\]
  - [오픈 마켓 웹 서버](https://ko.wikipedia.org/wiki/오픈_마켓 "wikilink")
  - [Resin Application Server](https://ko.wikipedia.org/wiki/Resin_Server "wikilink")
  - [Roxen Web Server](https://ko.wikipedia.org/wiki/Roxen "wikilink")
  - [ShimmerCat web server](https://ko.wikipedia.org/wiki/ShimmerCat "wikilink").\[8\]
  - [제우스 웹 서버](https://ko.wikipedia.org/wiki/제우스_웹_서버 "wikilink")

## FastCGI API 바인딩 언어

FastCGI은 [네트워크 소켓을](https://ko.wikipedia.org/wiki/네트워크_소켓 "wikilink") 지원하는 언어로 구현이 가능하다. (FastCGI는 프로토콜이지, 구현체는 아니므로 언어에 큰 제한을 받지는 않는다.) 다음을 위한 [API](https://ko.wikipedia.org/wiki/API "wikilink")가 존재한다\[9\]:

  - [에이다](https://ko.wikipedia.org/wiki/에이다 "wikilink")\[10\]
  - [델파이](https://ko.wikipedia.org/wiki/델파이 "wikilink")/[라자루스](https://ko.wikipedia.org/wiki/라자루스_\(IDE\) "wikilink") [프리 파스칼](https://ko.wikipedia.org/wiki/프리_파스칼 "wikilink")\[11\]
  - [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") / [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")
  - [치킨 스킴](https://ko.wikipedia.org/wiki/치킨_스킴 "wikilink")
  - [커먼 리스프](https://ko.wikipedia.org/wiki/커먼_리스프 "wikilink")\[12\]
  - [D 프로그래밍 언어](https://ko.wikipedia.org/wiki/D_\(프로그래밍_언어\) "wikilink")
  - [Eiffel](https://ko.wikipedia.org/wiki/에펠_\(프로그래밍_언어\) "wikilink")\[13\]
  - [얼랭](https://ko.wikipedia.org/wiki/얼랭 "wikilink")
  - [Go](https://ko.wikipedia.org/wiki/Go_\(프로그래밍_언어\) "wikilink")
  - [Guile Scheme](https://ko.wikipedia.org/wiki/Guile_Scheme "wikilink")
  - [하스켈](https://ko.wikipedia.org/wiki/하스켈 "wikilink")
  - [HP BASIC for OpenVMS](https://ko.wikipedia.org/wiki/HP_BASIC_for_OpenVMS "wikilink")
  - [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink")\[14\]\[15\]
  - [루아](https://ko.wikipedia.org/wiki/루아_\(프로그래밍_언어\) "wikilink")
  - [Node.js](https://ko.wikipedia.org/wiki/Node.js "wikilink")\[16\]
  - [OCaml](https://ko.wikipedia.org/wiki/OCaml "wikilink")
  - [펄](https://ko.wikipedia.org/wiki/펄 "wikilink")<ref>

There are a number of FastCGI modules for Perl: [FCGI](http://metacpan.org/module/FCGI) (a compiled module written in C), \[<http://metacpan.org/module/FCGI>::Async FCGI::Async\] (for asynchronous FastCGI applications), \[<http://metacpan.org/module/AnyEvent>::FCGI AnyEvent::FCGI\] (for [AnyEvent](http://metacpan.org/module/AnyEvent)-based applications), \[<http://metacpan.org/module/FCGI>::EV FCGI::EV\] (for [EV](http://metacpan.org/module/EV)-based applications), \[<http://metacpan.org/module/CGI>::Fast CGI::Fast\] (Perl [CGI](http://metacpan.org/module/CGI)-like interface for FastCGI), \[<http://metacpan.org/module/FCGI>::Client FCGI::Client\] (a FastCGI client library), and \[<http://metacpan.org/module/Net>::FastCGI Net::FastCGI\] (constants and functions to build and parse FastCGI messages). </ref>

  - [PHP](https://ko.wikipedia.org/wiki/PHP "wikilink") (php-fpm 또는 [HipHop for PHP을](https://ko.wikipedia.org/wiki/HipHop_for_PHP "wikilink") 통해\[17\])
  - [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")
  - [REALbasic (REAL Studio)](https://ko.wikipedia.org/wiki/소조_\(소프트웨어\) "wikilink")\[18\]
  - [루비](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink")
  - [러스트](../Page/러스트_\(프로그래밍_언어\).md "wikilink")\[19\]
  - [SmallEiffel](https://ko.wikipedia.org/wiki/SmallEiffel "wikilink")
  - [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink"): [FasTalk](https://ko.wikipedia.org/wiki/FasTalk "wikilink"), [돌핀 스몰토크](https://ko.wikipedia.org/wiki/돌핀_스몰토크 "wikilink")
  - [Tcl](https://ko.wikipedia.org/wiki/Tcl "wikilink")
  - [WebDNA](https://ko.wikipedia.org/wiki/WebDNA "wikilink")
  - [발라](../Page/발라_\(프로그래밍_언어\).md "wikilink") (C 바인딩을 통해)

[루비 온 레일즈](https://ko.wikipedia.org/wiki/루비_온_레일즈 "wikilink"), [카탈리스트](../Page/카탈리스트_\(소프트웨어\).md "wikilink"), [장고](https://ko.wikipedia.org/wiki/장고 "wikilink"), [케플러](https://ko.wikipedia.org/wiki/케플러_\(소프트웨어\) "wikilink"), [Plack](https://ko.wikipedia.org/wiki/Plack "wikilink") 등의 최근의 프레임워크들은 임베디드된 인터프리터 ([mod ruby](https://ko.wikipedia.org/wiki/mod_ruby "wikilink") , [mod perl](https://ko.wikipedia.org/wiki/mod_perl "wikilink"), [mod python](https://ko.wikipedia.org/wiki/mod_python "wikilink"), [mod_lua](https://ko.wikipedia.org/wiki/케플러_\(소프트웨어\) "wikilink") 등), 또는 FastCGI와 함께 사용이 가능하다.

## 각주

## 외부 링크

  - [FastCGI specification](https://fastcgi-archives.github.io/FastCGI_Specification.html) (site backup)
      - [Secondary backup](http://www.mit.edu/~yandros/doc/specs/fcgi-spec.html)
  - [FastCGI Web Site fork](https://fastcgi-archives.github.io/)
  - [mod_fastcgi - FastCGI module fork for Apache 1.x and 2.x supporting external applications](https://fastcgi-archives.github.io/mod_fastcgi/)
  - [mod_fcgid - a FastCGI module for Apache 2.x](http://httpd.apache.org/mod_fcgid/)
  - [Microsoft FastCGI](http://www.iis.net/default.aspx?tabid=1000051)
  - [Apache v2.x mod_proxy FastCGI Module](https://zenprojects.github.io/Apache-Proxy-FastCGI-Module/)

[분류:웹 기술](https://ko.wikipedia.org/wiki/분류:웹_기술 "wikilink") [분류:월드 와이드 웹](https://ko.wikipedia.org/wiki/분류:월드_와이드_웹 "wikilink")

1.  [Caddy User Guide - FastCGI](https://caddyserver.com/docs/fastcgi)
2.  [FastCGI for Cherokee](http://www.cherokee-project.com/doc/modules_handlers_fcgi.html)
3.  [FastCGI HOWTO for Hiawatha](http://www.hiawatha-webserver.org/howto/cgi_and_fastcgi)
4.  [FastCGI Support in Jetty](http://www.eclipse.org/jetty/documentation/current/fastcgi.html)
5.  [FastCGI for Lighttpd](http://trac.lighttpd.net/trac/wiki/Docs:ModFastCGI)
6.
7.  [OpenBSD's httpd(8) initial commit](http://marc.info/?l=openbsd-cvs&m=140520832128782&w=2)
8.
9.  [Application Libraries / Development Kits](https://fastcgi-archives.github.io)
10. [Matreshka](http://forge.ada-ru.org/matreshka)
11. [ExtPascal](https://github.com/farshadmohajeri/extpascal)
12. [How to use FastCGI from Common Lisp](http://cliki.net/fastcgi)
13. [Goanna Eiffel](https://svn.eiffel.com/goanna/trunk/goanna/)
14. [jFastCGI, a Java Servlet implementing FastCGI protocol](http://jfastcgi.org/)
15.
16. [node-fastcgi npm package](https://www.npmjs.org/package/node-fastcgi)
17. [FasterCGI with HHVM](http://www.hhvm.com/blog/1817/fastercgi-with-hhvm)
18. [REAL Studio Web Edition, builds web apps called via FastCGI](http://www.realsoftware.com/web/)
19. \[//github.com/danielksb/rust-fcgi\]