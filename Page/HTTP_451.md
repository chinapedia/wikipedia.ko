> This article is converted from Wikipedia: [HTTP 451](https://ko.wikipedia.org/wiki/HTTP_451).


**HTTP 451** 혹은 **법적인 이유로 사용할 수 없습니다**(Unavailable For Legal Reasons)는 [오류 메시지는](../Page/오류_메시지.md "wikilink") 법적인 이유, 예를 들어 정부기관의 검열 등으로 인해 사용자가 요구한 리소스를 가져올 수 없다는 의미이다. 451이란 수는 [레이 브래드버리의](../Page/레이_브래드버리.md "wikilink") [디스토피아](https://ko.wikipedia.org/wiki/디스토피아 "wikilink") 소설이자 검열을 다룬 [화씨 451에서](../Page/화씨_451.md "wikilink") 이름을 따왔다.\[1\] HTTP 451은 2016년 2월 RFC 7725에 의해 표준화되었다.

HTTP 451이 표기될 수 있는 상황은 국가 안보에 중대한 위협을 주는 페이지이거나, 저작권 위반, 프라이버시 침해, 법률 모독 혹은 법정이나 법률에 의한 위반 등이 있을 수 있다. RFC 명세상 HTTP 451은 자원이 존재하지만, 차단된 경우에 사용하지 않으며, 만약 그 자원이 법적 이유로 제거되어 더 이상 존재하지 않거나 자원이 존재하지 않았지만 해당 주제에 대한 논의가 합법적으로 금지된 경우 사용할 수 있다. 몇몇 사이트의 경우 법적으로 자원이 제거된 경우 기존의 [HTTP 404를](../Page/HTTP_404.md "wikilink") 반환하거나 혹은 유사한 코드를 반환한다.

## 예시

``` http
HTTP/1.1 451 Unavailable For Legal Reasons
Link: <https://spqr.example.org/legislatione>; rel="blocked-by"
Content-Type: text/html

<html>
 <head><title>Unavailable For Legal Reasons</title></head>
 <body>
  <h1>Unavailable For Legal Reasons</h1>
  <p>This request may not be serviced in the Roman Province
  of Judea due to the Lex Julia Majestatis, which disallows
  access to resources hosted on servers deemed to be
  operated by the People's Front of Judea.</p>
 </body>
</html>
```

## 참고 문헌

## 외부 링크

  - [RFC 7725 - An HTTP Status Code to Report Legal Obstacles](https://tools.ietf.org/html/rfc7725)

[분류:HTTP 상태 코드](https://ko.wikipedia.org/wiki/분류:HTTP_상태_코드 "wikilink") [분류:인터넷 검열](https://ko.wikipedia.org/wiki/분류:인터넷_검열 "wikilink")

1.