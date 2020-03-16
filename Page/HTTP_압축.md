> This article is converted from Wikipedia: [HTTP ](https://ko.wikipedia.org/wiki/HTTP_).


**HTTP 압축**(HTTP compression)은 전송 속도와 대역폭 이용을 개선하기 위해 [웹 서버와](../Page/웹_서버.md "wikilink") [웹 브라우저에](../Page/웹_브라우저.md "wikilink") 빌드되는 기능이다.\[1\]

[HTTP](../Page/HTTP.md "wikilink") 데이터는 서버로부터 전송되기 전에 [압축된다](../Page/데이터_압축.md "wikilink"). 호환 브라우저들은 유효한 포맷을 다운로드하기 전에 어느 메소드가 지원되는지 서버에 알린다. 호환 압축 메소드를 지원하지 않는 브라우저들은 압축되지 않은 데이터를 다운로드한다. 가장 흔한 압축 스킴으로는 [Gzip](../Page/Gzip.md "wikilink")와 [DEFLATE](https://ko.wikipedia.org/wiki/DEFLATE "wikilink")가 있다. 그러나 사용 가능한 전체 스킴 목록은 [IANA](https://ko.wikipedia.org/wiki/IANA "wikilink")에 의해 관리되고 있다.\[2\] 게다가 서드파티들은 새 메소드들을 개발하며 이것들을 자사의 제품에 포함시키는데, 이를테면 [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink") 브라우저에 구현된 스킴이자 구글 서버에 사용되는 구글 [Shared Dictionary Compression for HTTP](https://ko.wikipedia.org/wiki/Shared_Dictionary_Compression_for_HTTP "wikilink")(SDCH)을 들 수 있다.

HTTP에서 수행할 수 있는 2가지 다른 방식의 압축이 있다. 더 낮은 단계에서 전송 인코딩 헤더 필드는 HTTP의 페이로드가 압축되었음을 지시할 수 있다. 더 높은 단계에서 콘텐츠 인코딩 헤더 필드는 전송, 캐시, 기타 참조되는 리소스가 압축됨을 지시할 수 있다. 콘텐츠 인코딩을 사용하는 압축은 전송 인코딩보다 더 널리 지원되며 일부 브라우저는 서버 내 버그를 일으키는 것을 예방하기 위해 전송 인코딩 압축 지원을 광고하지 않는다.\[3\]

## 압축 스킴 협상

대부분의 경우 SDCH를 제외했을 때 협상은 RFC 2616에 기술된 바대로 2단계로 끝난다:

1\. [웹 브라우저는](../Page/웹_브라우저.md "wikilink") [HTTP 요청에](../Page/HTTP.md "wikilink") 토큰 목록을 포함시킴으로써 지원되는 압축 스킴을 알린다. *Content-Encoding*의 경우 필드 내 목록은 *Accept-Encoding*으로 호칭되며 *Transfer-Encoding*의 경우 필드 이름은 *TE*로 호칭된다.

``` http
GET /encrypted-area HTTP/1.1
Host: www.example.com
Accept-Encoding: gzip, deflate
```

2\. 서버가 하나 이상의 압축 스킴을 지원하는 경우 나가는 데이터는 양측에서 모두 지원되는 하나 이상의 메소드에 의해 압축된다. 이 경우라면, 서버는 HTTP 응답 안에 사용되는 스킴과 함께 *Content-Encoding* 또는 *Transfer-Encoding*를 추가하게 되며 쉼표로 구분한다.

``` http
HTTP/1.1 200 OK
Date: mon, 26 June 2016 22:38:34 GMT
Server: Apache/1.3.3.7 (Unix)  (Red-Hat/Linux)
Last-Modified: Wed, 08 Jan 2003 23:11:55 GMT
Accept-Ranges: bytes
Content-Length: 438
Connection: close
Content-Type: text/html; charset=UTF-8
Content-Encoding: gzip
```

## HTTP 압축 지원 서버

  - [SAP NetWeaver](https://ko.wikipedia.org/wiki/SAP_NetWeaver "wikilink")
  - [마이크로소프트 IIS](../Page/인터넷_정보_서비스.md "wikilink")
  - [아파치 HTTP 서버](../Page/아파치_HTTP_서버.md "wikilink")(**[mod_deflate](http://httpd.apache.org/docs/current/mod/mod_deflate.html)**를 통해. 이름에도 불구하고 gzip만 지원\[4\])
  - [Hiawatha HTTP server](https://ko.wikipedia.org/wiki/Hiawatha "wikilink"): 미리 압축된 파일을 서비스함\[5\]
  - [제우스 웹 서버](https://ko.wikipedia.org/wiki/제우스_웹_서버 "wikilink")
  - [Lighttpd](../Page/Lighttpd.md "wikilink") (**mod_compress** 및 더 새로운 **mod_deflate** (1.4.42+)를 통해)
  - [Nginx](../Page/Nginx.md "wikilink") – 내장
  - [제티 서버](../Page/제티_\(웹_서버\).md "wikilink")
  - [GeoServer](../Page/GeoServer.md "wikilink")
  - [아파치 톰캣](../Page/아파치_톰캣.md "wikilink")
  - [IBM 웹스피어](../Page/IBM_웹스피어.md "wikilink")
  - [AOLserver](https://ko.wikipedia.org/wiki/AOLserver "wikilink")
  - [HAProxy](https://ko.wikipedia.org/wiki/HAProxy "wikilink")
  - [바니시](../Page/바니시_\(소프트웨어\).md "wikilink")

## 각주

## 외부 링크

  - RFC 2616: Hypertext Transfer Protocol – HTTP/1.1

  - [HTTP Content-Coding Values](http://www.iana.org/assignments/http-parameters) by Internet Assigned Numbers Authority

  - [Compression with lighttpd](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:Modcompress)

  - [Coding Horror: HTTP Compression on IIS 6.0](http://www.codinghorror.com/blog/2004/08/http-compression-and-iis-6-0.html)

  -
  - [HTTP Compression](http://www.http-compression.com/): resource page by the founder of VIGOS AG, Constantin Rack

  - [Using HTTP Compression](http://www.serverwatch.com/tutorials/article.php/3514866) by Martin Brown of Server Watch

  - [Using HTTP Compression in PHP](http://www.devshed.com/c/a/PHP/Using-HTTP-Compression-in-PHP-Make-Your-Web-Pages-Load-Faster/)

  - [Dynamic and static HTTP compression with Apache httpd](https://web.archive.org/web/20120430023716/https://banu.com/blog/38/dynamic-and-static-http-compression-with-apache-httpd/)

[분류:웹 개발](https://ko.wikipedia.org/wiki/분류:웹_개발 "wikilink") [분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink") [분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink")

1.
2.  RFC 2616, Section 3.5: "The Internet Assigned Numbers Authority (IANA) acts as a registry for content-coding value tokens."
3.  ['RFC2616 "Transfer-Encoding: gzip, chunked" not handled properly'](https://code.google.com/p/chromium/issues/detail?id=94730), [Chromium](../Page/크로미엄_\(웹_브라우저\).md "wikilink") Issue 94730
4.
5.