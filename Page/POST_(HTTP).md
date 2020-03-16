> This article is converted from Wikipedia: [POST \(HTTP\)](https://ko.wikipedia.org/wiki/POST_\(HTTP\)).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **POST**(포스트)는 [월드 와이드 웹에](../Page/월드_와이드_웹.md "wikilink") 사용되는, [HTTP](../Page/HTTP.md "wikilink")가 지원하는 [요청 방식이다](../Page/HTTP.md "wikilink"). 설계상 POST 요청 방식은 [웹 서버가](../Page/웹_서버.md "wikilink") 요청 메시지의 본문에 감싸있는 데이터를 받아들일 것을 요청하며 이러한 정보를 저장할 가능성이 높다.\[1\] 파일을 업로드할 때나 완성된 [웹 폼을](../Page/폼_\(HTML\).md "wikilink") 제출할 때 종종 사용된다.

이와 대조적으로 HTTP [GET](../Page/HTTP.md "wikilink") 요청 방식은 서버로부터 정보를 검색한다. GET 요청의 일부로서 일부 데이터는 URL의 [쿼리 스트링을](https://ko.wikipedia.org/wiki/쿼리_스트링 "wikilink") 통해 전달되며 (이를테면) 검색 용어, 날짜 범위, 또 쿼리를 정의하는 기타 정보를 지정한다.

POST 요청의 일부로서, 요청 메시지의 본문에다 임의의 유형의 임의의 양의 데이터를 담아 서버로 전송할 수 있다. POST 요청의 [헤더 필드는](https://ko.wikipedia.org/wiki/HTTP_헤더_필드_목록 "wikilink") 보통 메시지 본문의 [인터넷 미디어 타입을](../Page/미디어_타입.md "wikilink") 지시한다.

## 웹 폼 제출

웹 브라우저가 [웹 폼](../Page/폼_\(HTML\).md "wikilink") 요소로부터 POST 요청을 보낼 때 기본 [인터넷 미디어 타입은](../Page/미디어_타입.md "wikilink") [application/x-www-form-urlencoded이다](https://ko.wikipedia.org/wiki/퍼센트_인코딩 "wikilink").\[2\] 이것은 잠재적으로 중복 키가 포함된 [키-값 쌍을](https://ko.wikipedia.org/wiki/연관_배열 "wikilink") 인코딩하기 위한 포맷이다. 각각의 키-값 쌍은 '&' 문자로 구분되며 각 키는 '=' 문자의 값과 구분된다. 키와 값들은 둘 다 공백을 '+' 문자로 대체하며 [영숫자](https://ko.wikipedia.org/wiki/영숫자 "wikilink")가 아닌 그 밖의 모든 문자는 [퍼센트 인코딩](https://ko.wikipedia.org/wiki/퍼센트_인코딩 "wikilink") 처리한다.\[3\]

이를테면 다음의 키-값 쌍은

    Name: Gareth Wylie
    Age: 24
    Formula: a + b == 13%!

다음으로 인코딩된다.

    Name=Gareth+Wylie&Age=24&Formula=a+%2B+b+%3D%3D+13%25%21

HTML 4.0을 기점으로 폼은 [multipart/form-data로](../Page/MIME.md "wikilink") 데이터를 제출할 수도 있으며 이는 RFC 2388에 정의되어 있다. (HTML 3.2에 언급된, HTML 2.0의 확장으로 정의된 초기 실험 버전의 경우 RFC 1867 문헌을 참고할 것)

폼이 속한 동일한 문서에 POST하는 특수한 케이스는 [포스트백](https://ko.wikipedia.org/wiki/포스트백 "wikilink")이라고 한다.

## 같이 보기

  - [포스트백](https://ko.wikipedia.org/wiki/포스트백 "wikilink")

## 각주

## 외부 링크

  - [Straightforward definition of POST](http://www.jmarshall.com/easy/http/#postmethod)
  - [POST verb in HTTP specification](http://tools.ietf.org/html/rfc7231#section-4.3.3)
  - [URIs, Addressability, and the use of HTTP GET and POST](http://www.w3.org/2001/tag/doc/whenToUseGet.html)

[분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink")

1.
2.
3.