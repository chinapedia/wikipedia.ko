> This article is converted from Wikipedia: [Nginx](https://ko.wikipedia.org/wiki/Nginx).


**Nginx**(엔진 x라 읽는다)는 [웹 서버 소프트웨어로](https://ko.wikipedia.org/wiki/웹_서버_소프트웨어 "wikilink"), 가벼움과 높은 성능을 목표로 한다. [웹 서버](../Page/웹_서버.md "wikilink"), [리버스 프록시](https://ko.wikipedia.org/wiki/리버스_프록시 "wikilink") 및 메일 프록시 기능을 가진다.

2017년 10월 기준으로 실질적으로 작동하는 웹 사이트(active site)들에서 쓰이는 [웹 서버 소프트웨어](https://ko.wikipedia.org/wiki/웹_서버_소프트웨어 "wikilink") 순위는 [아파치](https://ko.wikipedia.org/wiki/아파치 "wikilink")(44.89%), [엔진엑스](https://ko.wikipedia.org/wiki/엔진엑스 "wikilink")(20.65%), [구글 웹 서버](../Page/구글_웹_서버.md "wikilink")(7.86%), 마이크로소프트 [IIS](https://ko.wikipedia.org/wiki/IIS "wikilink")(7.32%)순이다.\[1\] 이 조사에서 생성은 되어있으나 정상적으로 작동하지 않는 웹 사이트들은 배제되었으며\[2\] 특히 MS의 [인터넷 정보 서비스](../Page/인터넷_정보_서비스.md "wikilink")([IIS](https://ko.wikipedia.org/wiki/IIS "wikilink"))를 설치한 웹 사이트들의 상당수가 비활성 사이트였다. 그런 사이트들도 포함하면 MS IIS가 1위이다. 2017년 6월 현재 Nginx는 한국 전체 등록 도메인 중 24.73%가 사용하고 있다.\[3\]

Nginx는 요청에 응답하기 위해 비동기 [이벤트 기반](../Page/이벤트_\(컴퓨팅\).md "wikilink") 구조를 가진다. 이것은 [아파치 HTTP 서버의](../Page/아파치_HTTP_서버.md "wikilink") 스레드/프로세스 기반 구조를 가지는 것과는 대조적이다. 이러한 구조는 서버에 많은 부하가 생길 경우의 성능을 예측하기 쉽게 해준다.

## 설명

[위키백과](../Page/위키백과.md "wikilink")에서는 nginx를 [SSL 터미네이션 프록시로](https://ko.wikipedia.org/wiki/SSL_터미네이션_프록시 "wikilink") 사용한다.\[4\]

### HTTP 프록시와 웹 서버 기능

  - 정적 파일과 인덱스 파일 표현, 자동 인덱싱 기능.
  - 캐싱을 통한 리버스 프록시
  - 로드 밸런싱
  - 고장 진단
  - SSL 지원
  - 캐싱을 통한 FastCGI 지원
  - Name-, IP-기반 가상서버
  - FLV 스트리밍
  - MP4 스트리밍 모듈을 이용한 MP4 스트리밍
  - 웹페이지 접근 인증
  - gzip 압축
  - 10000개의 동시 접속을 처리할 수 있는 능력
  - URL 다시쓰기 (URL rewriting)
  - 맞춤 로깅
  - 서버 사이드 기능 포함
  - WebDAV

### 메일 프록시 기능

  - SMTP, POP3, IMAP 프록시
  - STARTTLS 지원
  - SSL 지원

## 각주

<references/>

## 외부 링크

  - [nginx 공식 웹사이트](http://www.nginx.org/)
  - [nginx 설치예시(리눅스 우분투)](https://swiftcoding.org/lemp-on-lightsail)

[분류:자유 웹 서버 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_웹_서버_소프트웨어 "wikilink") [분류:2002년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2002년_소프트웨어 "wikilink") [분류:2011년 설립된 기업](https://ko.wikipedia.org/wiki/분류:2011년_설립된_기업 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink")

1.  <https://news.netcraft.com/archives/2017/10/26/october-2017-web-server-survey-13.html>
2.  <https://www.netcraft.com/active-sites/>
3.
4.