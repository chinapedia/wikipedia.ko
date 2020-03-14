> This article is converted from Wikipedia: [Wget](https://ko.wikipedia.org/wiki/Wget).


**GNU Wget**(간단히 Wget, 이전 이름: Geturl)는 [웹 서버로부터](https://ko.wikipedia.org/wiki/웹_서버 "wikilink") 콘텐츠를 가져오는 [컴퓨터 프로그램으로](https://ko.wikipedia.org/wiki/컴퓨터_프로그램 "wikilink"), [GNU 프로젝트의](https://ko.wikipedia.org/wiki/GNU_프로젝트 "wikilink") 일부이다. 이 프로그램의 이름은 [월드 와이드 웹과](https://ko.wikipedia.org/wiki/월드_와이드_웹 "wikilink") [get에서](https://ko.wikipedia.org/wiki/HTTP_GET "wikilink") 가져온 것이다. [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink"), [HTTPS](https://ko.wikipedia.org/wiki/HTTPS "wikilink"), [FTP](https://ko.wikipedia.org/wiki/파일_전송_프로토콜 "wikilink") 프로토콜을 통해 내려받기를 지원한다.

## Wget 사용법

### 기본 사용 예

GNU Wget의 일반적인 사용법으로는 명령 줄을 이용하여 실행하는 것으로, 하나 이상의 URL을 변수로 제공한다.

``` bash
# example.com의 "index.html" 제목 페이지를
# 파일로 내려받기
wget http://www.example.com/
```

``` bash
# GNU FTP 사이트로부터 Wget의 소스 코드 내려받기.
wget ftp://ftp.gnu.org/pub/gnu/wget/wget-latest.tar.gz
```

더 복잡한 예로는 여러 URL을 하나의 디렉터리 계층으로 자동 다운로드하는 방법이 있다.

``` bash
# Download *.gif from a website
# (globbing, like "wget http://www.server.com/dir/*.gif", only works with ftp)
wget -e robots=off -r -l1 --no-parent -A.gif ftp://www.example.com/dir/
```

``` bash
# Download the title page of example.com, along with
# the images and style sheets needed to display the page, and convert the
# URLs inside it to refer to locally available content.
wget -p -k http://www.example.com/
```

``` bash
# Download the entire contents of example.com
wget -r -l 0 http://www.example.com/
```

### 고급 사용 예

``` bash
wget -t 7 -w 5 --waitretry=14 --random-wait -m -k -K -e robots=off
        http://www.oreilly.com/catalog/upt3/errata/ -o ./myLog.log
```

``` bash
wget -t 22 --waitretry=48 --wait=33 --random-wait --referer="" --user-agent=""
     --limit-rate=512k -e robots=off -o ./my_movies.log -P./movies -i ./my_movies.txt
```

## 같이 보기

  - [웹 크롤러](https://ko.wikipedia.org/wiki/웹_크롤러 "wikilink")

## 각주

## 외부 링크

  -
[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:FTP 클라이언트](https://ko.wikipedia.org/wiki/분류:FTP_클라이언트 "wikilink") [분류:다운로드 관리자](https://ko.wikipedia.org/wiki/분류:다운로드_관리자 "wikilink") [분류:1996년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1996년_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:웹 크롤러](https://ko.wikipedia.org/wiki/분류:웹_크롤러 "wikilink")