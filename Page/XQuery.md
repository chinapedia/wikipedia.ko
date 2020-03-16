> This article is converted from Wikipedia: [XQuery](https://ko.wikipedia.org/wiki/XQuery).


**XQuery**(**XML Query**, XML 쿼리)는 일반적으로 [XML](../Page/XML.md "wikilink"), 텍스트, 벤더 특정 확장 데이터 포맷(JSON, 바이너리 등)으로 되어 있는, 정형, 비정형 데이터를 질의하고 변환하는 [질의](https://ko.wikipedia.org/wiki/질의어 "wikilink"), [함수형 프로그래밍](../Page/함수형_프로그래밍.md "wikilink") 언어이다. 이 언어는 [W3C](../Page/W3C.md "wikilink")의 XML 쿼리 [워킹 그룹에](https://ko.wikipedia.org/wiki/워킹_그룹 "wikilink") 의해 개발되었다. 작업은 XSL 워킹 그룹의 [XSLT](../Page/XSLT.md "wikilink")의 개발과 긴밀히 조율되었다. 이 두 단체는 XQuery의 하위 집합인 [XPath](../Page/XPath.md "wikilink")을 함께 책임지고 있다.

**XQuery 1.0**은 2007년 1월 23일, [W3C 권고안이](../Page/W3C.md "wikilink") 되었다.\[1\]

**XQuery 3.0**은 2014년 4월 8일 [W3C 권고안이](../Page/W3C.md "wikilink") 되었다.\[2\]

**XQuery 3.1**은 2017년 3월 21일 [W3C 궈고안이](../Page/W3C.md "wikilink") 되었다.\[3\]

## 예시

아래의 샘플 XQuery 코드는 셰익스피어의 연극 햄릿마다 고유한 화자를 나열하며 [hamlet.xml](http://www.ibiblio.org/xml/examples/shakespeare/hamlet.xml)에 인코딩되어 있다.

``` xquery
 <html><body>
 {
   for $act in doc("hamlet.xml")//ACT
   let $speakers := distinct-values($act//SPEAKER)
   return
     <div>
       <h1>{ string($act/TITLE) }</h1>
       <ul>
       {
         for $speaker in $speakers
         return <li>{ $speaker }</li>
       }
       </ul>
     </div>
 }
 </body></html>
```

## 각주

## 외부 링크

  - [W3C XML Query (XQuery)](http://www.w3.org/XML/Query)
  - [XQuery tutorial](https://www.w3schools.com/xml/xquery_intro.asp)
  - [XQuery API for Java](https://ko.wikipedia.org/wiki/XQuery_API_for_Java "wikilink") (XQJ) [자바 커뮤니티 프로세스](../Page/자바_커뮤니티_프로세스.md "wikilink")
  - [hamlet.xml](http://www.ibiblio.org/xml/examples/shakespeare/hamlet.xml) Hamlet in XML Format
  - [XQuery](http://www.cafeconleche.org/slides/xmlsig/xquery/index.html) (presentation - as HTML slides)
  - [List of open-source XQuery implementations](http://www.martinbroadhurst.com/open-source-xquery-implementations.html)

[분류:4GL](https://ko.wikipedia.org/wiki/분류:4GL "wikilink") [분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink") [분류:질의어](https://ko.wikipedia.org/wiki/분류:질의어 "wikilink") [분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink")

1.
2.
3.