> This article is converted from Wikipedia: [HTTP](https://ko.wikipedia.org/wiki/HTTP).


**[HTTP](../Page/HTTP.md "wikilink")**(**H**yper**T**ext **T**ransfer **P**rotocol, )는 [WWW](https://ko.wikipedia.org/wiki/WWW "wikilink") 상에서 정보를 주고받을 수 있는 [프로토콜이다](../Page/통신_프로토콜.md "wikilink"). 주로 [HTML](../Page/HTML.md "wikilink") 문서를 주고받는 데에 쓰인다. [TCP와](../Page/전송_제어_프로토콜.md "wikilink") [UDP를](../Page/사용자_데이터그램_프로토콜.md "wikilink") 사용하며, 80번 포트를 사용한다. [1996년](../Page/1996년.md "wikilink") 버전 1.0, 그리고 [1999년](../Page/1999년.md "wikilink") 1.1이 각각 발표되었다.

HTTP는 [클라이언트](https://ko.wikipedia.org/wiki/클라이언트 "wikilink")와 [서버](../Page/서버.md "wikilink") 사이에 이루어지는 요청/응답(request/response) 프로토콜이다. 예를 들면, 클라이언트인 [웹 브라우저가](../Page/웹_브라우저.md "wikilink") HTTP를 통하여 서버로부터 웹페이지나 그림 정보를 요청하면, 서버는 이 요청에 응답하여 필요한 정보를 해당 사용자에게 전달하게 된다. 이 정보가 모니터와 같은 출력 장치를 통해 사용자에게 나타나는 것이다.

HTTP를 통해 전달되는 자료는 <http:로> 시작하는 [URL](../Page/URL.md "wikilink")(인터넷 주소)로 조회할 수 있다.

## 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:Tim_Berners-Lee_CP_2.jpg "wikilink").\]\]

[하이퍼텍스트](../Page/하이퍼텍스트.md "wikilink")라는 용어는 1965년 [제너두 프로젝트에서](https://ko.wikipedia.org/wiki/제너두_프로젝트 "wikilink") [테드 넬슨이](../Page/테드_넬슨.md "wikilink") 만들었으며, 제너두 프로젝트는 《[As We May Think](https://ko.wikipedia.org/wiki/As_We_May_Think "wikilink")》(1945년)라는 수필에서 마이크로필름 기반 정보 수신 및 관리 "[메멕스](https://ko.wikipedia.org/wiki/메멕스 "wikilink")" 시스템을 기술한 [버니바 부시의](../Page/버니바_부시.md "wikilink") 비전(1930년대)에 의해 영감을 받았다. [팀 버너스 리와](https://ko.wikipedia.org/wiki/팀_버너스_리 "wikilink") 그의 팀은 [CERN](https://ko.wikipedia.org/wiki/CERN "wikilink")에서 HTML뿐 아니라 웹 브라우저 및 텍스트 기반 웹 브라우저 관련 기술과 더불어 오리지널 HTTP을 발명하였다. 버너스 리는 최초로 "월드와이드웹" 프로젝트를 1989년에 제안하였으며, 이것이 현재의 [월드 와이드 웹이다](../Page/월드_와이드_웹.md "wikilink"). 이 프로토콜의 최초 버전은 서버로부터 페이지를 요청하는 GET이라는 이름의 하나의 메소드만 있었다.\[1\] 서버로부터의 응답은 무조건 HTML 문서였다.\[2\]

문서화된 최초의 HTTP 버전은 **[HTTP V0.9](http://www.w3.org/pub/WWW/Protocols/HTTP/AsImplemented.html)**(1991년)이다. [데이브 레겟은](https://ko.wikipedia.org/wiki/데이브_레겟 "wikilink") 1995년 HTTP 워킹 그룹(HTTP WG)을 이끌었으며 확장된 조작, 확장된 협상, 더 보강된 메타 정보, 또 추가 메소드와 헤더 필드를 통한 더 효율적인 보안 프로토콜을 갖춘 프로토콜을 확장하기를 바랐다.\[3\]\[4\] RFC 1945는 공식적으로 1996년 HTTP v1.0을 도입하였다.

HTTP WG는 1995년 12월 새로운 표준을 출간하기로 계획하였으며\[5\] 당시 개발 중인 RFC 2068(이른바 HTTP-NG)에 기반한 이전 표준 HTTP/1.1에 대한 지원이 1996년 초에 주요 브라우저 개발자들에 의해 빠르게 채택되었다. 1996년 3월, 이전 표준 HTTP/1.1을 지원한 웹 브라우저로 [아레나](https://ko.wikipedia.org/wiki/아레나_\(웹_브라우저\) "wikilink"),\[6\] [넷스케이프 2.0](../Page/넷스케이프_내비게이터.md "wikilink"),\[7\] 넷스케이프 내비게이터 골드 2.01,\[8\] [모자이크 2.7](../Page/모자이크_\(웹_브라우저\).md "wikilink"), [링크스 2.5](../Page/링크스_\(웹_브라우저\).md "wikilink"), [인터넷 익스플로러 2.0이](../Page/인터넷_익스플로러_2.md "wikilink") 있다. 새로운 브라우저의 최종 사용자 채택 속도를 빨랐다. 1996년 3월, 한 웹 호스팅 회사의 보고에 따르면 인터넷 상에서 사용 중인 브라우저 중 40% 이상이 HTTP 1.1과 호환되었다. 같은 웹 호스팅 회사는 1996년 6월 기준으로 서버에 접근하는 모든 브라우저들 가운데 65%가 HTTP/1.1 호환이라고 보고하였다.\[9\] RFC 2068에 정의된 HTTP/1.1 표준은 공식적으로 1997년 1월에 출시되었다. HTTP/1.1 표준에 대한 개선과 업데이트는 1999년 6월 RFC 2616으로 출시되었다.

2007년에 부분적으로 HTTP/1.1 사양을 개정하고 분명히 하기 위해 **[HTTPbis 워킹 그룹](http://trac.tools.ietf.org/wg/httpbis/trac/wiki)**이 창설되었다. 2014년 6월, WG는 RFC 2616를 obsolete 처리하는, 업데이트된 6 파트 사양을 출시하였다:

  - RFC 7230, *HTTP/1.1: Message Syntax and Routing*
  - RFC 7231, *HTTP/1.1: Semantics and Content*
  - RFC 7232, *HTTP/1.1: Conditional Requests*
  - RFC 7233, *HTTP/1.1: Range Requests*
  - RFC 7234, *HTTP/1.1: Caching*
  - RFC 7235, *HTTP/1.1: Authentication*

[HTTP/2](https://ko.wikipedia.org/wiki/HTTP/2 "wikilink")는 2015년 5월 RFC 7540로 출판되었다.

## 메시지 포맷

클라이언트와 서버 사이의 소통은 평문([ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")) 메시지로 이루어진다. 클라이언트는 서버로 요청메시지를 전달하며 서버는 응답메시지를 보낸다.

### 요청 메시지

클라이언트가 서버에게 보내는 요청 메시지는 다음과 같다.

  - 요청 내용

<!-- end list -->

  -
    보기) GET /images/logo.gif HTTP/1.1

<!-- end list -->

  - 헤더

<!-- end list -->

  -
    보기) Accept-Language: en

<!-- end list -->

  - 빈 줄 (empty line)
  - 기타 메시지를 포함하여 표시된다.

요청 내용과 헤더 필드는 <CR><LF>로 끝나야 한다. 즉, 캐리지 리턴([Carriage Return](https://ko.wikipedia.org/wiki/Carriage_Return "wikilink")) 다음에 라인 피드([Line Feed](https://ko.wikipedia.org/wiki/Line_Feed "wikilink"))가 와야 한다. 빈 줄(empty line)은 <CR><LF>로 구성되며 그 외 다른 [화이트스페이스](https://ko.wikipedia.org/wiki/화이트스페이스 "wikilink")(whitespace)가 있어서는 안된다.

#### 요약표

<table>
<thead>
<tr class="header">
<th><p>HTTP 메소드</p></th>
<th><p>RFC</p></th>
<th><p>요청에 Body가 있음</p></th>
<th><p>응답에 Body가 있음</p></th>
<th><p>안전</p></th>
<th><p>멱등(Idempotent)</p></th>
<th><p>캐시 가능</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GET</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>HEAD</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>POST</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PUT</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>DELETE</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>CONNECT</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>OPTIONS</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>TRACE</p></td>
<td><p>RFC 7231</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PATCH</p></td>
<td><p>RFC 5789</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 응답 메시지

응답 메시지는 다음으로 구성된다.

  - 상태표시 행(status line): [상태코드](https://ko.wikipedia.org/wiki/상태코드 "wikilink")(status code)와 reason message를 포함한다. (예. *HTTP/1.1 200 OK*. 클라이언트의 요청이 성공적으로 전달되었음을 표시)
  - 응답 헤더필드 (예.*Content-Type: text/html*)
  - 빈 줄 (empty line)
  - 기타 메시지

### 예제 세션

아래는 포트 80의 [www.example.com에서](https://ko.wikipedia.org/wiki/example.com "wikilink") 실행 중인 HTTP 클라이언트와 HTTP 서버 간의 샘플 변환이다. 모든 데이터는 줄 끝마다 [2바이트 CR LF](https://ko.wikipedia.org/wiki/새줄 "wikilink") ('\\r\\n')를 사용하여 플레인 텍스트([ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")) 인코딩을 통해 송신된다.

#### 클라이언트 요청

``` http
GET /restapi/v1.0 HTTP/1.1
Accept: application/json
Authorization: Bearer UExBMDFUMDRQV1MwMnzpdvtYYNWMSJ7CL8h0zM6q6a9ntw
```

#### 서버 응답

``` http
HTTP/1.1 200 OK
Date: Mon, 23 May 2005 22:38:34 GMT
Content-Type: text/html; charset=UTF-8
Content-Encoding: UTF-8
Content-Length: 138
Last-Modified: Wed, 08 Jan 2003 23:11:55 GMT
Server: Apache/1.3.3.7 (Unix) (Red-Hat/Linux)
ETag: "3f80f-1b6-3e1cb03b"
Accept-Ranges: bytes
Connection: close

<html>
<head>
  <title>An Example Page</title>
</head>
<body>
  Hello World, this is a very simple HTML document.
</body>
</html>
```

## 응답 코드

클라이언트가 서버에 접속하여 어떠한 요청을 하면, 서버는 세 자리 수로 된 응답 코드와 함께 응답한다. HTTP의 응답 코드는 다음과 같다.

| 코드     | 메시지                                                   | 설명                                                                                                           |
| ------ | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| 1XX    | Informational(정보)                                     | 정보 교환.                                                                                                       |
| 100    | Continue                                              | 클라이언트로부터 일부 요청을 받았으니 나머지 요청 정보를 계속 보내주길 바람. (HTTP 1.1에서 처음 등장)                                               |
| 101    | Switching Protocols                                   | 서버는 클라이언트의 요청대로 Upgrade 헤더를 따라 다른 프로토콜로 바꿀 것임. (HTTP 1.1에서 처음 등장)                                            |
| 2XX    | Success(성공)                                           | 데이터 전송이 성공적으로 이루어졌거나, 이해되었거나, 수락되었음.                                                                         |
| 200    | OK                                                    | 오류 없이 전송 성공.                                                                                                 |
| 202    | Accepted                                              | 서버가 클라이언트의 요청을 수락함.                                                                                          |
| 203    | Non-authoritavive Information                         | 서버가 클라이언트 요구중 일부만 전송.                                                                                        |
| 204    | Non Content                                           | 클라이언트의 요구를 처리했으나 전송할 데이터가 없음.                                                                                |
| 205    | Reset Content                                         | 새 문서 없음. 하지만 브라우저는 문서 창을 리셋해야 함. (브라우저가 CGI 폼 필드를 전부 지우도록 할 때 사용됨.) (HTTP 1.1에서 처음 등장)                       |
| 206    | Partial Content                                       | 클라이언트가 Range 헤더와 함께 요청의 일부분을 보냈고 서버는 이를 수행했음. (HTTP 1.1에서 처음 등장)                                             |
| 3XX    | Redirection(방향 바꿈)                                    | 자료의 위치가 바뀌었음.                                                                                                |
| 300    | Multiple Choices                                      | 최근에 옮겨진 데이터를 요청.                                                                                             |
| 301    | Moved Permanently                                     | 요구한 데이터를 변경된 URL에서 찾았음.                                                                                      |
| 302    | Moved Permanently                                     | 요구한 데이터가 변경된 URL에 있음을 명시. 301과 비슷하지만 새 URL은 임시 저장 장소로 해석됨. \[10\]                                            |
| 303    | See Other                                             | 요구한 데이터를 변경하지 않았기 때문에 문제가 있음.                                                                                |
| 304    | Not modified                                          | 클라이언트의 캐시에 이 문서가 저장되었고 선택적인 요청에 의해 수행됨 (보통 지정된 날짜보다 더 나중의 문서만을 보여주도록 하는 If-Modified-Since 헤더의 경우).\[11\]     |
| 305    | Use Proxy                                             | 요청된 문서는 Location 헤더에 나열된 [프록시](https://ko.wikipedia.org/wiki/프록시 "wikilink")를 통해 추출되어야 함. (HTTP 1.1에서 처음 등장) |
| 307    | Temporary Redirect                                    | 자료가 임시적으로 옮겨짐.                                                                                               |
| 4XX    | Client Error(클라이언트 오류)                                | 클라이언트 측의 오류. 주소를 잘못 입력하였거나 요청이 잘못 되었음.                                                                       |
| 400    | Bad Request                                           | 요청 실패. 문법상 오류가 있어서 서버가 요청사항을 이해하지 못함,\[12\]                                                                  |
| 401.1  | Unauthorized                                          | 권한 없음 (접속실패). 서버에 로그온 하려는 요청사항이 서버에 들어있는 권한과 비교했을 때 맞지 않음.\[13\]                                             |
| 401.2  | Unauthorized                                          | 권한 없음 (서버설정으로 인한 접속 실패). 서버에 로그온 하려는 요청사항이 서버에 들어있는 권한과 비교했을 때 맞지않음.\[14\]                                   |
| 401.3  | Unauthorized                                          | 권한 없음 (자원에 대한 ACL에 기인한 권한 없음). 클라이언트가 특정 자료에 접근할 수 없음.\[15\]                                                 |
| 401.4  | Unauthorized                                          | 권한 없음 (필터에 의한 권한 부여 실패). 서버에 접속하는 사용자들을 확인하기 위해 설치한 필터 프로그램이 있음.\[16\]                                       |
| 401.5  | Unauthorized                                          | 권한 없음 (ISA PI/CGI 애플리케이션에 의한 권한부여 실패). 이용하려는 서버의 주소에 ISA PI나 CGI프로그램이 설치되어 있고, 권한을 부여할 수 없음.\[17\]           |
| 402    | Payment Required                                      | 예약됨.                                                                                                         |
| 403.1  | Forbidden                                             | 금지 (수행접근 금지). 수행시키지 못하도록 되어있는 디렉터리 내의 실행 파일을 수행하려고 하였음.                                                      |
| 403.2  | Forbidden                                             | 금지 (읽기 접근 금지). 접근한 디렉터리에 가용한 기본 페이지가 없음.\[18\]                                                               |
| 403.4  | Forbidden                                             | 금지 ([SSL](https://ko.wikipedia.org/wiki/SSL "wikilink") 필요함). 접근하려는 페이지가 SSL로 보안유지 되고 있음.\[19\]              |
| 403.5  | Forbidden                                             | 금지 ([SSL](https://ko.wikipedia.org/wiki/SSL "wikilink") 128필요함). 페이지가 128비트의 SSL로 보안유지 되고 있음.\[20\]          |
| 403.6  | Forbidden                                             | 금지 (IP 주소 거부됨). 사용자가 허용되지 않은 IP로부터 접근함.                                                                      |
| 403.7  | Forbidden                                             | 금지 (클라이언트 확인 필요). 클라이언트가 자료에 접근할 수 있는지 확인 요함.\[21\]                                                          |
| 403.8  | Forbidden                                             | 금지 (사이트 접근 거부됨). 서버가 요청사항을 수행하고 있지 않거나, 해당 사이트에 접근하는 것이 허락되지 않음.                                             |
| 403.9  | Forbidden                                             | 접근금지 (연결된 사용자수 과다). 서버가 BUSY 상태에 있어서 요청을 수행할 수 없음.                                                           |
| 403.10 | Forbidden                                             | 접근금지 (설정이 확실 하지 않음).                                                                                         |
| 403.11 | Forbidden                                             | 접근금지 (패스워드 변경됨). 잘못된 암호를 입력했음.                                                                               |
| 403.12 | Forbidden                                             | 접근금지(Mapper 접근 금지됨). 클라이언트 인증용 맵이 해당 웹 사이트에 접근하는 것이 거부됨.                                                     |
| 404    | Not Found                                             | 문서를 찾을 수 없음. 서버가 요청한 파일이나 스크립트를 찾지 못함.                                                                       |
| 405    | Method not allowed                                    | 메서드 허용 안됨. 요청 내용에 명시된 메서드를 수행하기 위해 해당 자원의 이용이 허용되지 않음.\[22\]                                                 |
| 406    | Not Acceptable                                        | 받아들일 수 없음.\[23\]                                                                                             |
| 407    | Proxy Authentication Required                         | 프록시 서버의 인증이 필요함.\[24\]                                                                                       |
| 408    | Request timeout                                       | 요청 시간이 지남.                                                                                                   |
| 409    | Conflict                                              | 요청을 처리하는 데 문제가 있음. 보통 PUT 요청과 관계가 있다. 보통 다른 버전의 파일을 업로드할 경우 발생함. (HTTP 1.1에서 새로 등장)                          |
| 410    | [Gone](https://ko.wikipedia.org/wiki/Gone "wikilink") | 영구적으로 사용할 수 없음.                                                                                              |
| 411    | Length Required                                       | 클라이언트가 헤더에 Content-Length를 포함하지 않으면 서버가 처리할 수 없음.(HTTP 1.1에서 새로 등장)                                          |
| 412    | Precondition Failed                                   | 선결조건 실패. 헤더에 하나 이상의 선결조건을 서버에서 충족시킬 수 없음.\[25\]                                                              |
| 413    | Request entity too large                              | 요청된 문서가 현재 서버가 다룰 수 있는 크기보다 큼.\[26\] (HTTP 1.1에서 새로 등장)                                                      |
| 414    | Request-URI too long                                  | 요청한 URI가 너무 김.\[27\]                                                                                         |
| 415    | Unsupported media type                                | 요청이 알려지지 않은 형태임. (HTTP 1.1에서 새로 등장)                                                                          |
| 5XX    | Server Error(서버 오류)                                   | 서버 측의 오류로 올바른 요청을 처리할 수 없음.                                                                                  |
| 500    | Internal Server Error                                 | 서버 내부 오류.\[28\]                                                                                              |
| 501    | Not Implemented                                       | 필요한 기능이 서버에 설치되지 않았음.\[29\]                                                                                  |
| 502    | Bad gateway                                           | 게이트웨이 상태 나쁨.\[30\]                                                                                           |
| 503    | Service Unavailable                                   | 외부 서비스가 죽었거나 현재 멈춘 상태 또는 이용할 수 없는 서비스.\[31\]                                                                 |
| 504    | Gateway timeout                                       | 프록시나 게이트웨이의 역할을 하는 서버에서 볼 수 있음. 초기 서버가 원격 서버로부터 응답을 받을 수 없음. (HTTP 1.1에서 새로 등장)                              |
| 505    | HTTP Version Not Supported                            | 해당 HTTP 버전을 지원하지 않음.                                                                                         |

## 같이 보기

  - [HTTPS](../Page/HTTPS.md "wikilink")
  - [HTML](../Page/HTML.md "wikilink")
  - [월드 와이드 웹](../Page/월드_와이드_웹.md "wikilink")

## 각주

## 외부 링크

  - [IETF의 HTTP/1.0 기술 명세서 (1996년 5월)](https://ko.wikipedia.org/wiki/rfc:1945 "wikilink")

  - [IETF의 HTTP/1.1 기술 명세서 (1999년 6월)](https://ko.wikipedia.org/wiki/rfc:2616 "wikilink")

  - [Bulkcheck HTTP-Headers from different URLs simultaneously](https://web.archive.org/web/20100216153716/http://pc-intern.com/http-header-bulkcheck.html)

  - [Watch HTTP Client/Server Request/Responses](http://www.tcpcatcher.org)

  - [HTTP header bookmarklet](http://www.webconfs.com/http-header-check.php)

  - [Eclipse HTTP Client - HTTP4E](https://web.archive.org/web/20090826024803/http://http4e.roussev.org/): a commercial Eclipse IDE plugin to execute/test/debug HTTP calls.

  - [스토리나인](http://m.storynine.co.kr/)

[분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:인터넷 표준](https://ko.wikipedia.org/wiki/분류:인터넷_표준 "wikilink") [분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:파일 전송 프로토콜](https://ko.wikipedia.org/wiki/분류:파일_전송_프로토콜 "wikilink") [HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. 이 메시지는 HTTP 1.0에서는‘Moved Temporarily’였다. 그리고 HttpServletResponse의 상수는 SC_FOUND가 아니라 C_MOVED_TEMPORARILY다. 이것은 매우 유용한 헤더인데 이 헤더를 통해 브라우저가 자동적으로 새 URL의 링크를 따라가기 때문이다. 이 상태 코드는 아주 유용하기 때문에 이 상태 코드를 위해 sendRedirect 라는 특별한 메서드가 있다. response.sendRedirect(url)을 사용하는 것은 response.setStatus(response.SC_MOVED_TEMPORARILY)과 response.setHeader("Location", url)를 쓰는 것에 비해 몇 가지 장점이 있다. 첫째, 더 쉽게 사용할 수 있다. 둘째, sendRedirect을 써서 서블릿이 그 링크를 포함한 페이지를 자동으로 만들어 준다(자동으로 redirect를 따라갈 수 없는 오래 된 브라우저에서도 볼 수 있게 해 준다). 마지막으로, sendRedirect에서는 상대 URL이 절대 URL로 해석되기 때문에 상대 URL도 다룰 수 있다. 이 상태 코드는 종종 301번과 혼용된다. 예를 들어 \<<http://host/~user>\> (마지막에 '/'가 빠짐)과 같이 오류가 있는 요청에 대해 어떤 서버는 301을 어떤 서버는 302를 보낸다. 기술적으로 브라우저는 원 요청이 GET이었다면 자동적으로 리다이렉션을 따라 가도록 되어 있다. 더 자세한 사항은 307 헤더를 보라.
11. 서버는 클라이언트에게 캐시에 저장된 이전 문서를 계속 사용해야 한다고 말할 것이다.
12. 클라이언트는 수정없이 요청 사항을 반복하지 않기 바람.
13. 이 경우, 여러분이 요청한 자원에 접근할 수 있는 권한을 부여받기 위해 서버 운영자에게 요청해야 할 것이다.
14. 이것은 일반적을 으로 적절한 www-authenticate head field를 전송하지 않아서 발생한다.
15. 이 자원은 페이지가 될 수도 있고, 클라이언트의 주소 입력란에 명기된 파일일 수도 있다. 아니면 클라이언트가 행당 주소로 들어갈 때 이용되는 또 다른 파일일 수도 있다. 여러분이 접근할 전체 주소를 다시 확인해 보고 웹 서버 운영자에게 여러분이 자원에 접근할 권한이 있는지를 확인해 본다.
16. 서버에 접속하는 데 이용되는 인증 과정이 이런 필터 프로그램에 의해 거부되었다.
17. 서버에 접속하는 데 이용되는 인증 과정이 이 프로그램에 의해 거부되었다.
18. 아니면 Eecute나 Script로 분한이 부여된 디렉터리에 들어있는 HTML페이지를 보려했을 때 발생한다.
19. 이것을 보기 위해서 여러분은 주소를 입력하기 전에 먼저 SSL을 이용할 수 있어야 한다.
20. 이 자원을 보기 위해서는 여러분의 브라우저가 SSL의 행당 레벌을 지원해야 한다. 여러분의 브라우저가 128비트의 SSL을 지원하는지를 확인해 본다.
21. 여러분이 접근하려는 자료가 서버가 인식하기 위해 여러분의 브라우저에게 클라이언트 SSL을 요청하는 경우 발생한다. 이것은 여러분이 자원을 이용할 수 있는 상용자임을 입증하는 데 사용된다.
22. 여러분이 요청한 자원에 적절한 MIME 타입을 갖고 있는지 확인해 본다.
23. 요청 사항에 필요한 자원은 요청 사항으로 전달된 Acceptheader에 따라 "Not Acceptable"인 내용을 가진 Response 개체만을 만들 수 있다.
24. 해당 요청이 수행되도록 프록시 서버에게 인증을 받아야 한다. 프록시 서버로 로그온 한 후에 다시 시도해 본다.
25. 현재 자원의 메타-정보가 하나 이상의 자원에 적용되는 것을 막기 위한 클라이언트 선결조건이 의도되었다.
26. 만약 서버에서 나중에 다룰 수 있다고 생각되면 Retry-After 헤더를 포함시켜야 한다.
27. 요청한 URI가 너무 길어서 서버가 요청 사항의 이행을 거부했다. 이렇게 희귀한 상황은 아래와 같은 경우에만 발생한다. 클라이언트가 긴 탐색용 정보를 가지고 POST 요청을 GET으로 부적절하게 전환했다. 클라이언트가 Redirection 문제를 접하게 되었다. 서버가, 몇몇 서버가 사용하고 있는 요청한 URI 를 읽고 처리하는 고정된 길이의 메모리 버퍼를 이용해 보안체계에 들어가려는, 클라이언트에 의한 공격을 받고 있다.
28. 서버가 요청사항을 수행할 수 없다. 다시 한 번 요청해 본다.
29. 서버가 요청사항을 수행하는 데 필요한 기능을 지원하지 않는다. 오류가 발생한 URL을 확인한 후에, 문제가 지속될 경우에는 웹 서버 운영자에게 연락한다.
30. 서버의 과부하 상태Gateway나 proxy로 활동하고 있는 서버가 요구 사항을 접수한 upstream 서버로부터 불명확한 답변을 접수 했을 때 발생한다. 만약 문제가 지속된다면 웹 서버 운영자와 상의해 본다.
31. 서버는 현재 일시적인 과부하 또는 관리(유지,보수) 때문에 요청을 처리할 수 없다. 이것은 약간의 지연 후 덜게 될 일시적인 상태를 말한다. Retry-After 헤더에 지연의 길이가 표시될 수도 있다. 만약 Retry-After를 받지 못했다면 클라이언트는 500 응답을 위해 하고자 했는 것처럼 응답을 처리해야 한다. 상태코드의 존재는 서버가 과부하가 걸릴때 그것을 사용해야한다는 것을 말하는 것이 아니다. 몇몇 서버는 접속을 거부하는 것을 바랄지도 모른다.