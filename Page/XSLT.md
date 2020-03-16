> This article is converted from Wikipedia: [XSLT](https://ko.wikipedia.org/wiki/XSLT).


**XSLT**()는 [XML](../Page/XML.md "wikilink") 문서를 다른 XML 문서로 변환하는데 사용하는 XML 기반 언어이다. [W3C](../Page/W3C.md "wikilink")에서 제정한 표준으로 [XML 변환 언어를](https://ko.wikipedia.org/wiki/XML_변환_언어 "wikilink") 사용하여 XML 문서로 바꿔주며, 탐색하기 위해 [XPath](../Page/XPath.md "wikilink")를 사용한다.

원본 문서는 변경되지 않으며, 원본 문서를 기반으로 새로운 문서가 생성된다.\[1\] 새 문서는 표준 XML 문법 또는 [HTML](../Page/HTML.md "wikilink"), 일반 텍스트 형식으로 출력된다.\[2\] XSLT는 XML 데이터를 웹 페이지로 표시하기 위해 HTML 또는 XHTML 문서로 변환할 때 자주 사용된다. 변환은 클라이언트나 서버에서 동적으로 수행되거나, 퍼블리싱 단계에서 수행되기도 한다. XML을 [PDF](../Page/PDF.md "wikilink"), [PostScript](https://ko.wikipedia.org/wiki/PostScript "wikilink"), [AWT](https://ko.wikipedia.org/wiki/AWT "wikilink"), [PNG](../Page/PNG.md "wikilink")와 같은 다양한 형태로 바꿀 수 있는 [XML-FO](https://ko.wikipedia.org/wiki/XML-FO "wikilink")로 변환할 때도 사용한다. XSLT는 일반적으로 서로 다른 [XML 스키마를](../Page/XML_스키마.md "wikilink") 사용하는 XML 메시지를 변환하거나, 하나의 [스키마](https://ko.wikipedia.org/wiki/스키마 "wikilink") 안에서 문서를 변경하기 위해 사용한다(예: 메시지에서 불필요한 부분 삭제).

## 개요

XSLT 처리의 구성 요소는 다음과 같다.

  - 하나 이상의 XML 원본 문서
  - 하나 이상의 XSLT 스타일시트 모듈
  - XSLT 템플릿 처리 엔진(프로세서)
  - 하나 이상의 결과 문서

XSLT는 일반적으로 XML 원본 문서와 XSLT 스타일시트를 입력으로 받아 문서를 출력한다. XSLT 스타일시트는 *템플릿 룰:명령어(template rules: instructions)*와 프로세서가 출력 문서를 제작하는 데 필요한 지침을 담고 있다.

### 템플릿 룰 처리

XSLT은 선언적인 언어이다. 템플릿 룰은 조건에 따라 어떤 동작을 수행하는지 나열하는 대신, 지정한 XPath 형태의 패턴과 일치하는 노드를 어떻게 처리할지를 정의한다. 템플릿은 프로세서가 패턴을 *결과 트리* 형태로 나타낼 수 있는 표현식을 담고 있다.

프로세서는 고정된 알고리즘을 따른다. 스타일시트는 이미 읽어와서 준비되어 있고, 프로세서는 입력 XML 문서에서 원본 트리를 만든다. 원본 트리의 루트 노드부터 스타일시트에서 가장 잘 맞는 템플릿을 찾아 변환한다. 각 템플릿의 명령어는 결과 트리의 노드를 생성하거나, 원본 트리의 다음 노드를 처리하도록 지시한다.

### 프로세서 구현

XSLT 프로세서 구현은 크게 서버 측과 클라이언트 측으로 나뉜다. 클라이언트 XSLT 프로세싱은 Microsoft [Internet Explorer에서](https://ko.wikipedia.org/wiki/Internet_Explorer "wikilink") 1999년부터 가능하지만, XSLT를 지원하지 않는 이전 브라우저와 다른 브라우저가 널리 퍼져 있어 도입 속도가 느리다. 비슷한 이유로 XSLT 2.0의 도입도 제한되어 있다.

XSLT 프로세서는 단일 제품으로 제작되거나, 웹 브라우저, 애플리케이션 서버, Java나 .NET 등 프레임워크 또는 운영체제의 컴포넌트로 제작된다.

### XSLT와 XPath

XSLT는 원본 문서 트리의 부분을 식별하고 연산을 수행하기 위해 XPath 언어를 사용한다. XSLT 1.0은 XPath 1.0을 사용하며, XSLT 2.0은 XPath 2.0을 사용한다. 두 가지 스펙은 모두 같은 날 출판되었다.

### XSLT와 XQuery 비교

XSLT의 기능은 다량의 XML 문서의 쿼리 언어로 사용되는 XQuery와 겹친다.

XSLT 2.0과 XQuery 1.0 표준은 W3C의 별도 작업 그룹이 개발하였으며, 접근 방식을 통일하기 위해 협업하였다. 데이터 모델과, 타입 시스템, 함수 라이브러리를 공유하며, 둘 다 XPath 2.0을 보조 언어로 사용한다.

두 언어는 서로 다른 환경의 요구를 반영한다. XSLT의 주요 목적은 XML을 처리하여 사람이 화면, 웹, 인쇄물로 읽을 수 있게 하는 것이다. XQuery의 주로 전통적인 SQL로 데이터베이스의 쿼리 언어로 여긴다.

## XSLT 예제

다음은 입력 XML 문서의 예시이다.

``` xml
<?xml version="1.0" ?>
<persons>
  <person username="JS1">
    <name>John</name>
    <family-name>Smith</family-name>
  </person>
  <person username="MI1">
    <name>Morka</name>
    <family-name>Ismincius</family-name>
  </person>
</persons>
```

다음은 XSLT 스타일시트의 예시이다.

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
  <xsl:output method="xml" indent="yes"/>

  <xsl:template match="/persons">
    <root>
      <xsl:apply-templates select="person"/>
    </root>
  </xsl:template>

  <xsl:template match="person">
    <name username="{@username}">
      <xsl:value-of select="name" />
    </name>
  </xsl:template>

</xsl:stylesheet>
```

다음은 결과 XML 문서의 예시이다.

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<root>
  <name username="JS1">John</name>
  <name username="MI1">Morka</name>
</root>
```

## 각주

<references/>

## 외부 링크

  - [XSLT 강좌](http://www.data2type.de/xml-xslt-xslfo/xslt)

  - [XSLT 2.0 참조](http://www.data2type.de/xml-xslt-xslfo/xslt/xslt-referenz)

  - [XSLT와 XPath에 대한 참조](https://web.archive.org/web/20100602185558/http://www.data2type.de/xml-xslt-xslfo/xslt/xsltundxpathreferenz)

[분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:XML](https://ko.wikipedia.org/wiki/분류:XML "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink") [분류:선언형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:선언형_프로그래밍_언어 "wikilink") [분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink")

1.  [XSL Transformations (XSLT)](http://www.w3.org/TR/xslt#section-Introduction)
2.  See e. g., <http://www.w3.org/TR/xslt#output>, specifying alternate output methods.