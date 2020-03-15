> This article is converted from Wikipedia: [JSON-LD](https://ko.wikipedia.org/wiki/JSON-LD).


**JSON-LD**(JavaScript Object Notation for Linked Data)는 [JSON](https://ko.wikipedia.org/wiki/JSON "wikilink")을 사용하여 [링크드 데이터를](https://ko.wikipedia.org/wiki/링크드_데이터 "wikilink") 인코딩하는 방식이다. 목적은 개발자들이 기존의 JSON을 JSON-LD로 변환하는데 들어가는 노력을 가능한 최소화시키는 것이었다.\[1\] 이로써 데이터가 전통적인 JSON과 유사한 방식으로 직렬화할 수 있게 된다.\[2\] [월드 와이드 웹 컨소시엄 권고안의](https://ko.wikipedia.org/wiki/월드_와이드_웹_컨소시엄 "wikilink") 하나이다. 검토, 개선, 표준화를 위해\[3\] RDF 워킹 그룹으로 이전되기 전까지는 처음에 [JSON 포 링킹 데이터 커뮤니티 그룹](http://json-ld.org/)(JSON for Linking Data Community Group)에 의해 개발되었다.\[4\]

## 디자인

JSON-LD는 JSON→[RDF](https://ko.wikipedia.org/wiki/자원_기술_프레임워크 "wikilink") 모델의 추가적인 매핑을 제공하기 위한 컨텍스트의 개념으로 설계되어 있다. 이 컨텍스트는 JSON 문서 내의 객체 속성을 [온톨로지](https://ko.wikipedia.org/wiki/온톨로지 "wikilink")의 개념에 연결시킨다. JSON-LD 문법을 RDF에 매핑시키기 위해 JSON-LD는 값들을 특정한 유형에 강제시키거나 특정 언어에 태그할 수 있게 허용한다. 컨텍스트는 JSON-LD 문서에 직접 추가하거나 별도 파일에 넣거나 다른 문서들로부터(HTTP 링크 헤더를 통해 전통적인 JSON 문서로부터) 참조할 수 있다.

## 예시

``` json-ld
{
  "@context": {
    "name": "http://xmlns.com/foaf/0.1/name",
    "homepage": {
      "@id": "http://xmlns.com/foaf/0.1/workplaceHomepage",
      "@type": "@id"
    },
    "Person": "http://xmlns.com/foaf/0.1/Person"
  },
  "@id": "https://me.example.com",
  "@type": "Person",
  "name": "John Smith",
  "homepage": "https://www.example.com/"
}
```

## 각주

<references />

## 외부 링크

  - [JSON-LD.org](http://json-ld.org/)

[분류:자원 기술 프레임워크](https://ko.wikipedia.org/wiki/분류:자원_기술_프레임워크 "wikilink") [분류:데이터 직렬화 포맷](https://ko.wikipedia.org/wiki/분류:데이터_직렬화_포맷 "wikilink") [분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink") [분류:JSON](https://ko.wikipedia.org/wiki/분류:JSON "wikilink")

1.
2.  , M. Lanthaler and C. Gütl in Proceedings of the 3rd International Workshop on RESTful Design (WS-REST 2012) at WWW2012.
3.
4.  [RDF Working Group](http://www.w3.org/2011/rdf-wg/wiki/Main_Page) This Working Group ended its activities on 1 July 2014 and is now closed.