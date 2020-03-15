> This article is converted from Wikipedia: [ HTTP ](https://ko.wikipedia.org/wiki/_HTTP_).


**아파치 HTTP 서버**()는 [아파치 소프트웨어 재단에서](../Page/아파치_소프트웨어_재단.md "wikilink") 관리하는 HTTP [웹 서버이다](../Page/웹_서버.md "wikilink"). [BSD](../Page/BSD.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink") 등 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 뿐 아니라 [마이크로소프트 윈도우나](../Page/마이크로소프트_윈도우.md "wikilink") [노벨 넷웨어](https://ko.wikipedia.org/wiki/노벨_넷웨어 "wikilink") 같은 기종에서도 운용할 수 있다.

## 활용

  - [리눅스](../Page/리눅스.md "wikilink") 운영 체제, 아파치 웹 서버, [MySQL](../Page/MySQL.md "wikilink") [데이터베이스](../Page/데이터베이스.md "wikilink"), [PHP](../Page/PHP.md "wikilink")등으로 웹 서버를 운영하는 것을 각각의 머릿글자를 따서 [LAMP](https://ko.wikipedia.org/wiki/LAMP "wikilink")라고도 부르기도 한다.
  - 톰캣(Tomcat), Resin 등의 [웹 애플리케이션 서버와](../Page/웹_애플리케이션_서버.md "wikilink") 같이 사용할 수 있다.
  - Open-SSL, Mod-SSL 을 설치하여, 보안을 강화할 수 있다. (http → https)

## 점유율

아파치 웹 서버는 현재 세계에서 가장 인기있는 웹 서버이다. 2017년 10월 기준으로 실질적으로 작동하는 웹 사이트(active site)들에서 쓰이는 [웹 서버 소프트웨어](https://ko.wikipedia.org/wiki/웹_서버_소프트웨어 "wikilink") 순위는 [아파치](https://ko.wikipedia.org/wiki/아파치 "wikilink")(44.89%), [엔진엑스](https://ko.wikipedia.org/wiki/엔진엑스 "wikilink")(20.65%), [구글 웹 서버](../Page/구글_웹_서버.md "wikilink")(7.86%), 마이크로소프트 [IIS](https://ko.wikipedia.org/wiki/IIS "wikilink")(7.32%)순이다.\[1\] 이 조사에서 생성은 되어있으나 정상적으로 작동하지 않는 웹 사이트들은 배제되었으며\[2\] 특히 MS의 [인터넷 정보 서비스](../Page/인터넷_정보_서비스.md "wikilink")([IIS](https://ko.wikipedia.org/wiki/IIS "wikilink"))를 설치한 웹 사이트들의 상당수가 비활성 사이트였다. 그런 사이트들도 포함하면 MS IIS가 1위이다.

2017년 3월 현재 Apache는 한국 전체 등록 도메인 중 42.39%가 사용하고 있다.\[3\]

## 리눅스 버전 설치 예

  - [페도라에서](https://ko.wikipedia.org/wiki/페도라_\(운영_체제\) "wikilink") 아파치 설치 : [yum](https://ko.wikipedia.org/wiki/yum "wikilink") install httpd
  - [데비안](../Page/데비안.md "wikilink")계열 아파치 설치 : [apt-get](https://ko.wikipedia.org/wiki/어드밴스트_패키지_툴 "wikilink") install apache2

역사적으로 아파치 웹서버 설정파일은 단일파일로 크게 아래와 같이 3가지 섹션으로 나뉘어 있었다.\[4\]

  -
    섹션 1 : Global Environment
    섹션 2 : 'Main' server configuration
    섹션 3 : Virtual Hosts

아파치의 핵심 설정파일은 /etc/httpd/conf/httpd.conf 또는 /etc/apache2/apache2.conf이다. 아파치2에 와서는 여기에 딸려 있는 하위파일 및 디렉토리들로 나뉘어졌다. 이들 중에서 SeverName 항목은 /etc/apache2/sites-enabled/\*.conf에 있다. 아파치가 설치되면 로컬호스트(localhost)인 내부 IP환경에서 http : / / 127.0.0.1로 초기화면을 확인할 수 있다.\[5\]

|                                                                      |
| -------------------------------------------------------------------- |
| [200px](https://ko.wikipedia.org/wiki/파일:Apache2-dir.svg "wikilink") |
| 우분투 아파치 웹서버 설정파일 및 디렉토리                                              |

그러나 이러한 웹서버는 [방화벽과](../Page/방화벽_\(네트워킹\).md "wikilink") 별개로 작동되므로, 방화벽에서 웹서버의 기본 포트 80번 등을 열어주지 않는 이상 외부에서 접근할수는 없다.\[6\]

아파치2에 와서는 별다른 설정치에 대한 수정 없이 아파치 웹서버는 기본설정값인 디폴트 환경에서도 잘 작동한다. 그러나 한편 최적화를 위한 설정 항목들은 더욱 다양해졌다.\[7\]

## 함께 보기

  - [ufw](https://ko.wikipedia.org/wiki/ufw "wikilink")(uncomplicated firewall)

## 각주

<references />

  - ([fedora](https://ko.wikipedia.org/wiki/페도라_\(운영_체제\) "wikilink"))https://docs.fedoraproject.org/quick-docs/en-US/getting-started-with-apache-http-server.html

## 외부 링크

  -

  - [한국 아파치 사용자 커뮤니티](https://web.archive.org/web/20070626085729/http://www.apache-kr.org/)

[분류:자유 웹 서버 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_웹_서버_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [웹 서버](https://ko.wikipedia.org/wiki/분류:아파치_소프트웨어_재단_프로젝트 "wikilink") [분류:유닉스 네트워크 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_네트워크_관련_소프트웨어 "wikilink") [분류:1995년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1995년_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink")

1.  <https://news.netcraft.com/archives/2017/10/26/october-2017-web-server-survey-13.html>
2.  <https://www.netcraft.com/active-sites/>
3.
4.  (httpd-2.0.39,hredhat-config-httpd-1.0.1-17,httpd-manual-2.0.39)
5.  (Apache2 Ubuntu Default Page)https://help.ubuntu.com/lts/serverguide/httpd.html
6.  (How to Configure a Firewall with UFW Updated Monday, September 17, 2018 by Linode Written by Elle Krout)https://www.linode.com/docs/security/firewalls/configure-firewall-with-ufw/
7.  <http://httpd.apache.org/docs/trunk/new_features_2_4.html>