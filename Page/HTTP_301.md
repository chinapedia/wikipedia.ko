> This article is converted from Wikipedia: [HTTP 301](https://ko.wikipedia.org/wiki/HTTP_301).


[HTTP](../Page/HTTP.md "wikilink") 응답 [상태 코드](../Page/HTTP_상태_코드.md "wikilink") **301 Moved Permanently**는 영구적인 [URL 리다이렉션을](../Page/URL_리다이렉션.md "wikilink") 위해 사용되며, 즉 응답을 수신하는 [URL](../Page/URL.md "wikilink")을 사용하는 현재의 링크나 레코드가 업데이트되어야 함을 의미한다. 이 새 URL은 응답에 포함된 [위치 필드에](https://ko.wikipedia.org/wiki/HTTP_위치 "wikilink") 지정되어야 한다. 301 리다이렉트는 사용자가 HTTP를 HTTPS로 업그레이드하게 만드는 최상의 방법으로 간주된다.\[1\]

RFC 2616은 다음과 같이 언급한다:\[2\]

  - 클라이언트가 링크 편집 기능이 있으면 요청 URL에 대한 모든 참조를 업데이트해야 한다.
  - 특별한 표시가 없으면 응답은 캐시가 가능할 것.
  - 요청 메소드가 HEAD가 아닌 경우 엔티티는 새로운 URL로 향하는 하이퍼링크와 함께 크기가 작은 하이퍼텍스트 참고사항을 포함해야 한다.
  - GET이나 HEAD 외의 요청에 대해 301 상태 코드를 수신할 경우 클라이언트는 리다이렉트 전에 사용자에게 물어보아야 한다.

## 예시

클라이언트 요청:

    GET /index.php HTTP/1.1
    Host: www.example.org

서버 응답:

    HTTP/1.1 301 Moved Permanently
    Location: http://www.example.org/index.asp

다음은 [.htaccess](https://ko.wikipedia.org/wiki/.htaccess "wikilink") 파일을 사용하여, 안전하지 않은 URL을 안전한 주소로 www 없이 리다이렉트 처리하는 예이다.

    RewriteEngine On
    RewriteCond %{HTTPS} off
    RewriteCond %{HTTP_HOST} ^www\.(.*)$ [NC]
    RewriteRule ^(.*)$ http://%1/$1 [R=301,L]

    RewriteCond %{HTTPS} on
    RewriteCond %{HTTP_HOST} ^www\.(.*)$ [NC]
    RewriteRule ^(.*)$ https://%1/$1 [R=301,L]

    RewriteEngine On
    RewriteCond %{SERVER_PORT} 80
    RewriteRule ^(.*)$ https://example.com/$1 [R,L]

다음은 [펄](../Page/펄.md "wikilink") [펄](../Page/펄.md "wikilink") [CGI.pm](https://ko.wikipedia.org/wiki/CGI.pm "wikilink")을 사용한 예이다:

``` perl numberLines
print redirect("https://example.com/newpage.html");
```

다음은 [PHP](../Page/PHP.md "wikilink") 리다이렉트를 사용한 예이다:

``` php numberLines
<?php
header("Location: https://example.com/newpage.html", true, 301);
exit;
```

[Nginx](../Page/Nginx.md "wikilink") 구성의 예이다:

    location /old/url/ {
        return 301 /new/url/;
    }

다음은 [Express.js](../Page/Express.js.md "wikilink")를 사용한 리다이렉트의 예이다:

    app.all("/old/url", (req, res) => {
        res.redirect(301, "/new/url");
    });

## 같이 보기

  - [HTTP](../Page/HTTP.md "wikilink")
  - [HTTP 상태 코드](../Page/HTTP_상태_코드.md "wikilink")
  - [URL 리다이렉션](../Page/URL_리다이렉션.md "wikilink")

## 각주

[분류:HTTP 상태 코드](https://ko.wikipedia.org/wiki/분류:HTTP_상태_코드 "wikilink")

1.
2.  Fielding, *et al* (1999-06). "10.3.2 301 Moved Permanently". RFC 2616, p 61. IETF, June 1999. Retrieved from <https://tools.ietf.org/html/rfc2616#section-10.3.2>.