> This article is converted from Wikipedia: [Mod perl](https://ko.wikipedia.org/wiki/Mod_perl).


**mod_perl**은 [아파치 HTTP 서버용](https://ko.wikipedia.org/wiki/아파치_HTTP_서버 "wikilink") 선택적 모듈이다. [펄](https://ko.wikipedia.org/wiki/펄 "wikilink") [인터프리터](https://ko.wikipedia.org/wiki/인터프리터 "wikilink")를 아파치 서버 안으로 임베드한다. 아파치 모듈을 펄 프로그래밍 언어로 작성할 수 있게 허용할 뿐 아니라 아파치 웹 서버가 동적으로 펄 프로그램에 의해 구성될 수 있게 한다. 그러나 가장 일반적인 용도는 각 요청마다 펄 인터프리터를 다시 실행하는 상당한 부하 없이 펄 [스크립트가](https://ko.wikipedia.org/wiki/스크립트_언어 "wikilink") 만든 동적 콘텐츠를 들어오는 요청에 대응하여 서비스할 수 있게 하는 것이다.

웹 사이트 [슬래시닷](https://ko.wikipedia.org/wiki/슬래시닷 "wikilink")을 운영하는 [슬래시는](https://ko.wikipedia.org/wiki/슬래시_\(CMS\) "wikilink") mod_perl을 사용하여 작성되어 있다.\[1\] 초기 버전의 [PHP](https://ko.wikipedia.org/wiki/PHP "wikilink")는 mod_perl을 사용하여 펄로 구현되었다.\[2\]

## CGI와의 비교

mod_perl은 [공용 게이트웨이 인터페이스](https://ko.wikipedia.org/wiki/공용_게이트웨이_인터페이스 "wikilink")(CGI) 환경을 에뮬레이트할 수 있으므로 기존의 펄 CGI 스크립트들은 재작성할 필요 없이 성능 향상의 이점을 취할 수 있다.

CGI 및 기타 대부분의 웹 애플리케이션 환경과 달리 mod_perl은 아파치 [API](https://ko.wikipedia.org/wiki/API "wikilink")에 대한 완전한 접근을 제공하므로 [프로그래머](https://ko.wikipedia.org/wiki/프로그래머 "wikilink")들이 아파치 요청 사이클 내의 모든 구간에 대한 핸들러를 작성할 수 있으며 아파치의 내부 테이블과 상태 매커니즘을 조작하고 아파치 [프로세스](https://ko.wikipedia.org/wiki/프로세스 "wikilink")나 [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink") 간 데이터를 공유하며 아파치 [구성 파일](https://ko.wikipedia.org/wiki/구성_파일 "wikilink") [파서를](https://ko.wikipedia.org/wiki/파싱 "wikilink") 변경, 확장하고 펄 코드를 구성 파일 자체에 추가하는 등의 일을 허용한다.

## 같이 보기

  - [CGI.pm](https://ko.wikipedia.org/wiki/CGI.pm "wikilink")
  - [FastCGI](https://ko.wikipedia.org/wiki/FastCGI "wikilink")

## 각주

## 외부 링크

  - \[//perl.apache.org/ 주 웹사이트\]
  - [Why mod_perl?](http://www.perl.com/pub/a/2002/02/26/whatismodperl.html)
  - [The magic of mod_perl](http://www.revsys.com/writings/modperl.html)
  - [Writing Apache Modules with Perl and C](https://web.archive.org/web/20080511203607/http://www.modperl.com/)
  - [The mod_perl Developer's Cookbook](http://www.modperlcookbook.org/)
  - [mod_perl2 User's Guide](http://modperl2book.org/)
  - [An easy step-by-step installation guide for mod_perl2 on Unix/Linux and Windows/ReactOS](http://www.modperl.pl/how-to/)

[펄](https://ko.wikipedia.org/wiki/분류:아파치_httpd_모듈 "wikilink") [분류:펄](https://ko.wikipedia.org/wiki/분류:펄 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink")

1.
2.