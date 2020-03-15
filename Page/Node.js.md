> This article is converted from Wikipedia: [Node.js](https://ko.wikipedia.org/wiki/Node.js).


**Node.js**는 확장성 있는 네트워크 애플리케이션(특히 서버 사이드) 개발에 사용되는 소프트웨어 플랫폼이다. 작성 언어로 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink")를 활용하며 Non-blocking I/O와 단일 스레드 이벤트 루프를 통한 높은 처리 성능을 가지고 있다.

내장 HTTP 서버 라이브러리를 포함하고 있어 웹 서버에서 아파치 등의 별도의 소프트웨어 없이 동작하는 것이 가능하며 이를 통해 웹 서버의 동작에 있어 더 많은 통제를 가능케 한다.

## 개요

[V8 (자바스크립트 엔진)으로](https://ko.wikipedia.org/wiki/V8_\(자바스크립트_엔진\) "wikilink") 빌드 된 [이벤트](https://ko.wikipedia.org/wiki/이벤트_기반_설계 "wikilink") 기반 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink") [런타임](../Page/런타임.md "wikilink")이다. [웹 서버와](../Page/웹_서버.md "wikilink") 같이 확장성 있는 네트워크 프로그램 제작을 위해 고안되었다.

[파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")으로 만든 [트위스티드](../Page/트위스티드_\(소프트웨어\).md "wikilink"), [펄](https://ko.wikipedia.org/wiki/펄 "wikilink")로 만든 [펄 객체 환경](https://ko.wikipedia.org/wiki/:en:Perl_Object_Environment "wikilink"), [루비로](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink") 만든 [이벤트머신](https://ko.wikipedia.org/wiki/이벤트머신 "wikilink")과 그 용도가 비슷하다. 대부분의 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink")가 웹 브라우저에서 실행되는 것과는 달리, 서버 측에서 실행된다. 일부 [CommonJS](https://ko.wikipedia.org/wiki/CommonJS "wikilink") 명세\[1\]를 구현하고 있으며, 쌍방향 테스트를 위해 [REPL](https://ko.wikipedia.org/wiki/:en:Read-eval-print_loop "wikilink") 환경을 포함하고 있다.

## 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:Ryan_Dahl.jpg "wikilink") 2009년 Ryan Dahl은 [플리커](../Page/플리커.md "wikilink")의 파일 업로드 진행 표시줄을 보았을 때, 파일이 얼마나 업로드되었는지 알기 위해서는 서버에 쿼리를 전송해야 한다는 점을 보고 조금 더 쉬운 방법을 찾다가 고안해 내었으며,\[2\] 그가 일하던 [Joyent](https://ko.wikipedia.org/wiki/Joyent "wikilink")라는 회사에서 개발 및 운영을 담당하고 있다.\[3\]

최초 버전은 2009년 리눅스 기반으로 출시되었고, Inangural JSConf EU conference에서 Ryan Dahl의 발표\[4\] 직후 국제적인 관심을 끌기 시작했다.\[5\] 패키지 매니저인 [npm](https://ko.wikipedia.org/wiki/npm "wikilink")은 2011년에 처음 소개되었다.

2011년 6월 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")는 Joyent와 파트너십을 맺고\[6\] 같은 해 7월 [윈도용](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 최초 버전을 출시했다.

2014년 12월, Fedor Indutny는 Node.js의 포크인 io.js를 시작했다.

2015년 9월, Node.js v0.12와 io.js v3.3은 병합되어 Node v4.0으로 합쳐졌다.\[7\]

2019년 4월, Node.js v12 부터 [ECMA스크립트](https://ko.wikipedia.org/wiki/ECMA스크립트 "wikilink")의 공식 모듈 시스템 사용을 실험적으로 지원하기 시작했다. (그 이전까지는 서드파티인 [CommonJS](https://ko.wikipedia.org/wiki/CommonJS "wikilink") 모듈만을 사용해오고 있었다.)

## 출시

Node.js 의 버전별 출시 및 관리는 규칙적인 주기를 가지고 이루어지고 있으며, v4 이후로 약 6개월 주기로 새로운 버전을 출시하고 있다. 이 중 짝수버전의 경우 장기지원 버전(LTS) 이라고 하여 별도의 코드명을 부여받으며, 약 3년간 유지보수 대상이 된다.

Node.js를 운영하는 재단의 [한국어 웹페이지](https://nodejs.org/ko/about/releases/)에서는 버전별 출시 및 유지보수 일정을 명시해두고 있다.

| 릴리스   | 코드명           | 출시일        | LTS 상태 | 활동적인 LTS 시작일 | 유지보수 시작일   | 유지보수 종료일   |
| ----- | ------------- | ---------- | ------ | ------------ | ---------- | ---------- |
| v0.10 |               | 2013-03-11 | 수명 종료  | \-           | 2015-10-01 | 2016-10-31 |
| v0.12 |               | 2015-02-06 | 수명 종료  | \-           | 2016-04-01 | 2016-12-31 |
| v4    | Argon\[8\]    | 2015-09-08 | 수명 종료  | 2015-10-01   | 2017-04-01 | 2018-04-01 |
| v5    |               | 2015-10-29 | LTS 없음 | N/A          | 2016-06-30 |            |
| v6    | Boron\[9\]    | 2016-04-26 | 수명 종료  | 2016-10-18   | 2018-04-18 | 2019-04-18 |
| v7    |               | 2016-10-25 | LTS 없음 | N/A          | 2017-06-30 |            |
| v8    | Carbon\[10\]  | 2017-05-30 | 유지보수   | 2017-10-31   | 2019-04-01 | 2019-12-31 |
| v9    |               | 2017-10-01 | LTS 없음 | N/A          | 2018-06-30 |            |
| v10   | Dubnium\[11\] | 2018-04-24 | 활성     | 2018-10-30   | 2020-04-01 | 2021-04-30 |
| v11   |               | 2018-10-23 | LTS없음  | N/A          | 2019-06-01 |            |
| v12   | Erbium        | 2019-04-23 | 활성     | 2019-10-21   | 2020-10-21 | 2022-04-30 |
| v13   |               | 2019-10-22 | 현재     | N/A          |            |            |
| v14   | ?             | 2020-04-21 | 대기     | 2020-10-20   | 2021-10-20 | 2023-04-30 |

## 예제

[Hello world](https://ko.wikipedia.org/wiki/Hello_world "wikilink") [HTTP 서버](../Page/웹_서버.md "wikilink"):

``` javascript
var http = require('http');

http.createServer(function (request, response) {
    response.writeHead(200, {'Content-Type': 'text/plain'});
    response.end('Hello World\n');
}).listen(8000);

console.log('Server running at http://localhost:8000/');
```

다른 예제, 7000번 [포트를](https://ko.wikipedia.org/wiki/포트_번호 "wikilink") 여는 간단한 [TCP](https://ko.wikipedia.org/wiki/전송_제어_프로토콜 "wikilink") [Echo](https://ko.wikipedia.org/wiki/Echo "wikilink") [서버](https://ko.wikipedia.org/wiki/서버 "wikilink"):

``` javascript
var net = require('net');

net.createServer(function (stream) {
    stream.write('hello\r\n');

    stream.on('end', function () {
        stream.end('goodbye\r\n');
    });

    stream.pipe(stream);
}).listen(7000);
```

## 같이 보기

  - [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink")
  - [V8 (자바스크립트 엔진)](https://ko.wikipedia.org/wiki/V8_\(자바스크립트_엔진\) "wikilink")

## 각주

## 외부 링크

  -
  - [깃허브 저장소](https://github.com/nodejs/node)

  - [The Node Beginner Book](http://www.nodebeginner.org/index-kr.html)

[분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:자바스크립트로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바스크립트로_작성된_자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:리눅스 재단 프로젝트](https://ko.wikipedia.org/wiki/분류:리눅스_재단_프로젝트 "wikilink")

1.  <http://wiki.commonjs.org/wiki/Implementations/node.js>
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.