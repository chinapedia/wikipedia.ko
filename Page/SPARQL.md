> This article is converted from Wikipedia: [SPARQL](https://ko.wikipedia.org/wiki/SPARQL).


**SPARQL** ("[sparkle](https://ko.wikipedia.org/wiki/:wikt:sparkle "wikilink")", 스파클, SPARQL Protocol and RDF Query Language의 [재귀 약자](../Page/재귀_약자.md "wikilink")\[1\])은 [RDF 질의어](https://ko.wikipedia.org/wiki/RDF_질의어 "wikilink"), 즉 [데이터베이스](../Page/데이터베이스.md "wikilink")를 위한 [시맨틱](https://ko.wikipedia.org/wiki/시맨틱_쿼리 "wikilink") [질의어](https://ko.wikipedia.org/wiki/질의어 "wikilink")로서 [자원 기술 프레임워크](../Page/자원_기술_프레임워크.md "wikilink")(RDF) 형식으로 저장된 데이터를 검색, 조작할 수 있다.\[2\]\[3\] [월드 와이드 웹 컨소시엄의](https://ko.wikipedia.org/wiki/월드_와이드_웹_컨소시엄 "wikilink") RDF DAWG(Data Access Working Group)에 의해 표준화되었으며 [시맨틱 웹의](../Page/시맨틱_웹.md "wikilink") 주요 기술 가운데 하나로 지목된다. 2008년 1월 15일, SPARQL 1.0은 공식 W3C 권고안이 되었으며,\[4\]\[5\] 2013년 3월 SPARQL 1.1이 그 다음 권고안으로 되었다.\[6\]

SPARQL은 쿼리가 [트리플 패턴](../Page/트리플스토어.md "wikilink"), [논리곱](https://ko.wikipedia.org/wiki/논리곱 "wikilink"), [논리합](https://ko.wikipedia.org/wiki/논리합 "wikilink"), 선택적 [패턴](https://ko.wikipedia.org/wiki/패턴 "wikilink")을 구성할 수 있게 한다.\[7\]

여러 [프로그래밍 언어를](../Page/프로그래밍_언어.md "wikilink") 위한 구현체들이 존재한다.\[8\] 이를테면 ViziQuer처럼 SPARQL 엔드포인트를 위한 SPARQL 쿼리를 연결, 반자동 구성할 수 있게 하는 도구들이 존재한다.\[9\] 이뿐 아니라 SPARQL 쿼리를 다른 질의어, 이를테면 [SQL](../Page/SQL.md "wikilink")\[10\]과 [XQuery](../Page/XQuery.md "wikilink")로 변환하는 도구들도 존재한다.\[11\]

## 예

"아프리카의 모든 국가 수도는?"이라는 질문의 SPARQL 쿼리 예제이다:

``` sparql
PREFIX ex: <http://example.com/exampleOntology#>
SELECT ?capital
       ?country
WHERE
  {
    ?x  ex:cityname       ?capital   ;
        ex:isCapitalOf    ?y         .
    ?y  ex:countryname    ?country   ;
        ex:isInContinent  ex:Africa  .
  }
```

변수는 "`?`" 또는 "`$`" 두문자로 구분한다. `?capital`과 `?country`의 바인딩을 반환한다.

## 같이 보기

  - [사이퍼 질의어](../Page/사이퍼_질의어.md "wikilink")

## 각주

## 외부 링크

  - [W3C SPARQL Working Group](http://www.w3.org/2001/sw/DataAccess/), was RDF Data Access Working Group
  - [SPARQL 1.1 Recommendation](http://www.w3.org/TR/sparql11-overview/)
  - [SPARQL 1.0 Query language](http://www.w3.org/TR/rdf-sparql-query/) (legacy)
  - [SPARQL 1.0 Protocol](http://www.w3.org/TR/rdf-sparql-protocol/) (legacy)
  - [SPARQL 1.0 Query XML Results Format](http://www.w3.org/TR/2008/REC-rdf-sparql-XMLres-20080115/) (legacy)
  - [SPARQL2XQuery](http://www.dblab.ntua.gr/~bikakis/SPARQL2XQuery.html) Mappings between OWL-RDF/S & XML Schemas, and XML Schema to OWL Transformation.

SPARQL Syntax Expressions (alternatively, *SPARQL S-Expressions*) is the [RDF](../Page/자원_기술_프레임워크.md "wikilink")–centric syntax.

  - [SPARQL Syntax Expressions specification](https://web.archive.org/web/20160630002046/http://openjena.org/wiki/SSE)
  - [SPARQL Syntax Expressions in the ARQ query engine](http://jena.sourceforge.net/ARQ/algebra.html)
  - [SPARQL Syntax Expressions translations of the DAWG test suite](http://blog.dydra.com/2011/09/08/dawg-tests)

Open SPARQL web services

  - [Wikidata](https://query.wikidata.org)
  - [DBpedia](http://dbpedia.org/isparql/)

[SPARQL](https://ko.wikipedia.org/wiki/분류:SPARQL "wikilink") [분류:선언형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:선언형_프로그래밍_언어 "wikilink") [분류:질의어](https://ko.wikipedia.org/wiki/분류:질의어 "wikilink") [분류:웹 서비스](https://ko.wikipedia.org/wiki/분류:웹_서비스 "wikilink") [분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:데이터 모델링 언어](https://ko.wikipedia.org/wiki/분류:데이터_모델링_언어 "wikilink")

1.
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