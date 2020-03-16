> This article is converted from Wikipedia: [Memcached](https://ko.wikipedia.org/wiki/Memcached).


**Memcached** (멤캐시디, 멤캐시트)는 범용 분산 [캐시](../Page/캐시.md "wikilink") 시스템이다. 외부 데이터 소스(예: 데이터베이스나 API)의 읽기 횟수를 줄이기 위해 데이터와 [객체들을](https://ko.wikipedia.org/wiki/객체_\(컴퓨터_과학\) "wikilink") [RAM에](../Page/랜덤_액세스_메모리.md "wikilink") 캐시 처리함으로써 동적 [데이터베이스](../Page/데이터베이스.md "wikilink") 드리븐 웹사이트의 속도를 높이기 위해 종종 사용된다. Memcached는 [BSD 허가서로](../Page/BSD_허가서.md "wikilink") 라이선스되는 [자유-오픈 소스 소프트웨어이다](../Page/자유-오픈_소스_소프트웨어.md "wikilink").\[1\] Memcached는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제(적어도 [리눅스](../Page/리눅스.md "wikilink")와 [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")), [마이크로소프트 윈도우에서](../Page/마이크로소프트_윈도우.md "wikilink") 실행된다. [libevent](https://ko.wikipedia.org/wiki/libevent "wikilink") 라이브러리에 의존한다.

## 역사

Memcached는 2003년 5월 22일 [Brad Fitzpatrick가](https://ko.wikipedia.org/wiki/Brad_Fitzpatrick "wikilink") 자신의 웹사이트 [라이브저널](../Page/라이브저널.md "wikilink")을 위해 처음 개발한 것이다.\[2\]\[3\] 처음에 [펄](../Page/펄.md "wikilink")로 작성되었다가 나중에 [Anatoly Vorobey에](https://ko.wikipedia.org/wiki/Anatoly_Vorobey "wikilink") 의해 [C로](../Page/C_\(프로그래밍_언어\).md "wikilink") 재개발되었고, 이후 라이브저널에 채용되었다.\[4\] Memcached는 현재 수많은 시스템에 사용되고 있는데, 여기에는 [유튜브](../Page/유튜브.md "wikilink"),\[5\] [레딧](../Page/레딧.md "wikilink"),\[6\] [페이스북](../Page/페이스북.md "wikilink"),\[7\]\[8\] [핀터레스트](../Page/핀터레스트.md "wikilink"),\[9\]\[10\] [트위터](../Page/트위터.md "wikilink"),\[11\], [위키백과](../Page/위키백과.md "wikilink")가 포함된다.\[12\] [구글 앱 엔진](../Page/구글_앱_엔진.md "wikilink"), [마이크로소프트 애저](../Page/마이크로소프트_애저.md "wikilink"), [블루믹스](../Page/블루믹스.md "wikilink"), [아마존 웹 서비스](../Page/아마존_웹_서비스.md "wikilink") 또한 API를 통해 Memcached 서비스를 제공한다.\[13\]\[14\]\[15\]\[16\]

## 이용

  - [MySQL](../Page/MySQL.md "wikilink") - 버전 5.6 기준으로 Memcached API를 직접 지원.\[17\]
  - [오라클 코히어런스](https://ko.wikipedia.org/wiki/오라클_코히어런스 "wikilink") - 버전 12.1.3 기준으로 Memcached API를 직접 지원.\[18\]
  - [GigaSpaces XAP](https://ko.wikipedia.org/wiki/GigaSpaces_XAP "wikilink") - 고가용성, 트랜잭션 지원과 함께 Memcached 지원\[19\]

## 같이 보기

  - [카우치베이스 서버](../Page/카우치베이스_서버.md "wikilink")
  - [레디스](../Page/레디스.md "wikilink")
  - [카산드라](../Page/아파치_카산드라.md "wikilink")

## 각주

## 외부 링크

  -
[분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:2003년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2003년_소프트웨어 "wikilink")

1.
2.  [1](http://community.livejournal.com/changelog/637455.html). Community.livejournal.com (2003-05-22). Retrieved on 2013-09-18.
3.  [2](http://community.livejournal.com/lj_dev/539656.html). Community.livejournal.com (2003-05-27). Retrieved on 2013-09-18.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.