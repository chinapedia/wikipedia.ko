> This article is converted from Wikipedia: [XPointer](https://ko.wikipedia.org/wiki/XPointer).


**XPointer**(XML Pointer Language)는 웹 상에 존재하는 [XML](../Page/XML.md "wikilink") 문서의 일부분에 주소를 부여할 수 있는 방법을 제공하는 [W3C](../Page/W3C.md "wikilink") 표준 언어이다.

## XPointer의 사용 의의

  - XPointer는 XML 문서 내의 노드, 범위, 글자 단위로 주소를 부여할 수 있다.
  - XML 문서의 일부를 다른 XML 문서에서 링크하고자 할 때 유용하다.
  - 문서 내의 일부 정보를 검색할 때 유용하다.

## XPointer의 표현법

XML 문서의 위치를 나타내는 데에는 [URI](https://ko.wikipedia.org/wiki/URI "wikilink")가 쓰이고, 이후 XML 문서의 세부 내용을 표현하는 데에는 XPointer가 쓰인다.

  - 위치 지정 방식

href="URL\#절대위치경로.상대위치경로.문자위치경로"

  - [XPath](../Page/XPath.md "wikilink") 활용 방식

href="URL\#Xpointer(Xpath 표현식)"

## 위치 지정 요소 어드레싱

`element()` 스킴은 차일드 요소의 위치 지정 어드레싱을 도입한다. 단순한 XPath 주소와 비슷하지만 최종 단계는 트리의 브랜치에 상대적인 위치를 나타내는 숫자여야 한다.

이를테면 다음의 경우:

``` xml
<foobar id="foo">
  <bar/>
  <baz>
    <bom a="1"/>
  </baz>
  <bom a="2"/>
</foobar>
```

다음의 결과를 출력한다:

` xpointer(id("foo")) => foobar`
` xpointer(/foobar/1) => bar`
` xpointer(//bom) => bom (a=1), bom (a=2)`
` element(/1/2/1) => bom (a=1) (/1 descend into first element (foobar),`
`                               /2 descend into second child element (baz),`
`                               /1 select first child element (bom))`

## 외부 링크

  - [XPointer Framework](http://www.w3.org/TR/xptr-framework/)
  - [Positional element addressing](http://www.w3.org/TR/xptr-element/)
  - [Namespacing](http://www.w3.org/TR/xptr-xmlns/)
  - [Path based addressing](http://www.w3.org/TR/xptr-xpointer/)

[분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink")