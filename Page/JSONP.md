> This article is converted from Wikipedia: [JSONP](https://ko.wikipedia.org/wiki/JSONP).


[thumb](https://ko.wikipedia.org/wiki/파일:JSONP_logo.png "wikilink") **JSONP**(**[JSON](../Page/JSON.md "wikilink") with Padding** 또는 JSON-P\[1\])는 클라이언트가 아닌, 각기 다른 도메인에 상주하는 서버로부터 데이터를 요청하기 위해 사용된다. 2005년에 Bob Ippolito가 제안하였다.\[2\] JSONP는 [동일-출처 정책을](../Page/동일-출처_정책.md "wikilink") 우회하는 데이터의 공유를 가능하게 한다. 이 정책은 페이지의 출처 밖에서 가져온 미디어 [DOM](../Page/문서_객체_모델.md "wikilink") 요소나 [XHR](../Page/XMLHttpRequest.md "wikilink") 데이터를 읽기 위해 [자바스크립트](../Page/자바스크립트.md "wikilink")를 실행하는 것을 허용하지 않는다. 사이트의 스킴, 포트 번호, 호스트 이름의 집합은 출처로 식별된다. 상속 비보안 문제로 인해 JSONP는 [CORS로](https://ko.wikipedia.org/wiki/크로스_오리진_리소스_셰어링 "wikilink") 대체되고 있다.

## JSONP의 동작 원리

웹 브라우저에서 실행되는 JavaScript는 동일 출처 정책에 따라 XMLHttpRequest 등의 직접적인 HTTP 통신을 이용해 외부 출처에서 데이터를 받아오는 것이 불가능하지만, HTML <code>

<script>

</code> 요소는 외부 출처로부터 조회된 내용을 실행하는 것이 허용되어 있다. 예를 들어 외부 서비스 `http://server.example.com/Users/1234`에서 사람 Foo의 기록을 JSON 포맷으로 반환한다 하자. 다음과 같은 JSON 포맷을 볼 수 있을 것이다.

``` json numberLines
{
    "Name": "Foo",
    "Id": 1234,
    "Rank": 7
}
```

이 데이터를 불러오기 위해 다음과 같이 JavaScript의 직접적인 HTTP 통신을 하면 오류가 발생한다.

``` javascript numberLines
var xmlhttp = new XMLHttpRequest();
xmlhttp.open('GET', 'http://server.example.com/Users/1234', true);
xmlhttp.onload = function () {
  console.log('Retrieved Data: ' + xmlhttp.responseText);
};
xmlhttp.send(); // -> 교차 출처 요청 차단
```

반면 다음과 같이 script 태그에 JSON 데이터를 직접적으로 삽입하면 JSON 데이터를 교차 출처 정책에 관계 없이 불러올 수 있지만 JavaScript 문법 오류가 발생한다.

``` html numberLines
<script type="application/javascript"
        src="http://server.example.com/Users/1234">
</script>
```

이는 웹 브라우저의 JavaScript 엔진이 변수, 상수 정의 등의 특정한 상황 없이 나오는 중괄호 문법을 block으로 해석하기 때문이다.

JSONP는 이러한 웹 브라우저의 특성을 이용해, JSON 데이터를 클라이언트가 지정한 콜백 함수를 호출하는 유효한 JavaScript 문법으로 감싸 클라이언트에 전송한다.

클라이언트가 'parseResponse'라는 함수를 JSONP 요청의 콜백 함수로 지정하였다고 하면, 다음과 같은 HTML 태그가 문서에 삽입된다.

``` html numberLines
<script type="application/javascript"
        src="http://server.example.com/Users/1234?callback=parseResponse">
</script>
```

외부 서비스 server.example.com은 다음과 같이 JSON 데이터를 패딩하여 클라이언트에 보낸다.

``` json numberLines
parseResponse({"Name": "Foo", "Id": 1234, "Rank": 7});
```

웹 브라우저는 이 데이터를 유효한 JavaScript 프로그램으로 받아들여 실행하고, 콜백 함수인 parseResponse가 실행되며 받아온 데이터를 처리할 수 있게 된다.

## 각주

## 외부 링크

  - [server side filter wraps any response into a jsonp callback](https://code.google.com/p/jsonp-java/)done with jsonp-java source code
  - [Potential security issues related to JSON](http://quaxio.com/jsonp_handcrafted_flash_files/)
  - [JSONP data source for remote domains](https://datatables.net/examples/server_side/jsonp.html)

[분류:Ajax](https://ko.wikipedia.org/wiki/분류:Ajax "wikilink") [분류:JSON](https://ko.wikipedia.org/wiki/분류:JSON "wikilink")

1.
2.