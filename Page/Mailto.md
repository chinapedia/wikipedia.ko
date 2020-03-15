> This article is converted from Wikipedia: [Mailto](https://ko.wikipedia.org/wiki/Mailto).


**mailto**는 [이메일 주소를](../Page/전자_우편_주소.md "wikilink") 위한 [통합 자원 식별자(URI)](https://ko.wikipedia.org/wiki/통합_자원_식별자 "wikilink") 스킴이다. [이메일 클라이언트로의](https://ko.wikipedia.org/wiki/이메일_클라이언트 "wikilink") 복사 및 입력 과정 없이 사용자들이 특정한 주소로 [전자 우편을](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 보낼 수 있도록 [웹사이트](https://ko.wikipedia.org/wiki/웹사이트 "wikilink")의 [하이퍼링크](https://ko.wikipedia.org/wiki/하이퍼링크 "wikilink")를 만들기 위해 사용된다. [RFC](https://ko.wikipedia.org/wiki/RFC "wikilink") 2368에 처음 정의되어 1998년 7월에 출판되었고,\[1\] RFC 6068에 사소한 개선이 추가되어 2010년 10월 출판되었다.\[2\]

## 예

[HTML](https://ko.wikipedia.org/wiki/HTML "wikilink") 문서에 "mailto"을 사용하면 이메일을 보내기 위한 링크를 생성한다:

``` html4strict
<a href="mailto:someone@example.com">Send email</a>
```

헤더의 초기값(예: 제목, 참조 등)과 메시지 본문을 URL에 지정할 수도 있다. 빈 값, 캐리지 리턴, 라인피드는 넣을 수 없으므로 [퍼센트 인코딩처리되어야](https://ko.wikipedia.org/wiki/퍼센트_인코딩 "wikilink") 한다.

``` html4strict
<a href="mailto:someone@example.com?subject=This%20is%20the%20subject&cc=someone_else@example.com&body=This%20is%20the%20body">Send email</a>
```

여러 개의 주소를 지정할 수도 있다:\[3\]

``` html4strict
<a href="mailto:someone@example.com,someoneelse@example.com">Send email</a>
```

주소를 생략할 수도 있다:

``` html4strict
<a href="mailto:?to=&subject=mailto%20with%20examples&body=https://en.wikipedia.org/wiki/Mailto">Share this knowledge...</a>
```

## 각주

[분류:전자 우편](https://ko.wikipedia.org/wiki/분류:전자_우편 "wikilink") [분류:URI 스킴](https://ko.wikipedia.org/wiki/분류:URI_스킴 "wikilink") [분류:웹 1.0](https://ko.wikipedia.org/wiki/분류:웹_1.0 "wikilink")

1.
2.
3.