> This article is converted from Wikipedia: [XML](https://ko.wikipedia.org/wiki/XML).


[섬네일](https://ko.wikipedia.org/wiki/파일:RecipeBook_XML_Example.svg "wikilink") **XML**(Extensible Markup Language)은 [W3C](../Page/W3C.md "wikilink")에서 개발된, 다른 특수한 목적을 갖는 [마크업 언어를](https://ko.wikipedia.org/wiki/마크업_언어 "wikilink") 만드는데 사용하도록 권장하는 다목적 [마크업 언어이다](https://ko.wikipedia.org/wiki/마크업_언어 "wikilink"). XML은 [SGML](https://ko.wikipedia.org/wiki/SGML "wikilink")의 단순화된 부분집합으로, 다른 많은 종류의 데이터를 기술하는 데 사용할 수 있다. XML은 주로 다른 종류의 시스템, 특히 [인터넷](../Page/인터넷.md "wikilink")에 연결된 시스템끼리 데이터를 쉽게 주고 받을 수 있게 하여 [HTML](../Page/HTML.md "wikilink")의 한계를 극복할 목적으로 만들어졌다.

기계는 인간의 언어를 읽거나 이해할 수 없는 계산기에 불과하므로 XML과 같은 구조화된 마크업 언어들은 인간의 읽고 분석하여 이해하는 능력과 컴퓨터의 단순한 계산적인 판독 능력 사이에 타협점을 만들어 줄 수 있다. [W3C](../Page/W3C.md "wikilink")가 만든 XML 1.0 Specification\[1\]과 몇몇 다른 관련 명세들\[2\]과 모든 자유 [개방형 표준](../Page/개방형_표준.md "wikilink")\[3\]에서 정의되었다.

W3C는 XML 설계 목표에서 단순성과 일반성, 그리고 [인터넷](../Page/인터넷.md "wikilink")을 통한 사용 가능성을 강조했다.\[4\] XML은 텍스트 데이터 형식으로 [유니코드](../Page/유니코드.md "wikilink")를 사용해 전 세계 언어를 지원한다. XML을 설계할 때는 주로 문서를 표현하는데 집중했지만, 지금은 임의의 자료구조를 나타내는 데 널리 쓰인다. 대표적인 예가 [웹 서비스이다](https://ko.wikipedia.org/wiki/웹_서비스 "wikilink").

많은 [API](../Page/API.md "wikilink")가 개발되어 XML 데이터를 처리하고자 하는 소프트웨어 개발자들이 활용하고 있다. 또한, 여러 가지 [스키마 시스템이](../Page/XML_스키마.md "wikilink") 있어서 XML 기반 언어의 정의를 보다 쉽게 할 수 있도록 도와준다.

## 역사

XML은 [SGML](https://ko.wikipedia.org/wiki/SGML "wikilink")의 애플리케이션 프로파일이다.\[5\]

동적 정보 표시를 위한 [SGML](https://ko.wikipedia.org/wiki/SGML "wikilink")의 다재다능함은 인터넷의 성장 이전인 1980년대 말에 초기 디지털 미디어 출판사들에 의해 인지되었다.\[6\]\[7\] 1990년대 중순, 일부 SGML 실천자들은 당시 새로운 [월드 와이드 웹을](../Page/월드_와이드_웹.md "wikilink") 경험하였고 웹이 성장할수록 마주칠 가능성이 있던 문제들 중 일부를 SGML이 해결해줄 것이라 믿었다. 댄 커널리는 1995년 당시 직원으로 있었을 때 SGML을 W3C의 활동 목록에 추가하였다. 작업은 1996년 중순 [썬 마이크로시스템즈의](../Page/썬_마이크로시스템즈.md "wikilink") 엔지니어 [존 보삭이](https://ko.wikipedia.org/wiki/존_보삭 "wikilink") 선언문을 만들고 협업자들을 모집하였을 때 시작되었다. 보삭은 SGML과 웹에 모두 경험이 있는 사람들의 작은 공동체와 잘 어울렸다.\[8\]

주요 디자인 결정은 1996년 7월과 11월 사이 도달했으며,\[9\] 당시 XML 사양의 최초 워킹 드래프트가 출판되었다.\[10\] 추가 디자인 작업이 1997년에 계속되었으며 XML 1.0은 1998년 2월 10일 [W3C](../Page/W3C.md "wikilink") 권고안이 되었다.

## 기본 개념

XML에서의 기본 개념에는 10가지가 있다.

  - XML은 구조적인 데이터를 위한 것이다.
  - XML은 다소 [HTML](../Page/HTML.md "wikilink") 같이 보인다.
  - XML은 텍스트이며, 읽히는 것만을 뜻하지 않는다.
  - XML은 크기가 커진다.
  - XML은 기술의 [집합](https://ko.wikipedia.org/wiki/집합 "wikilink")이다.
  - XML은 새로운 기술이 아니라 발전한 기술이다.
  - XML은 [HTML](../Page/HTML.md "wikilink")에서 [XHTML](https://ko.wikipedia.org/wiki/XHTML "wikilink")로 이끌었다.
  - XML은 모듈식이다.
  - XML은 [RDF](https://ko.wikipedia.org/wiki/RDF "wikilink")와 [시맨틱 웹의](https://ko.wikipedia.org/wiki/시맨틱_웹 "wikilink") 토대이다.
  - XML은 [라이선스](https://ko.wikipedia.org/wiki/라이선스 "wikilink") 제약이 없으며, [플랫폼](https://ko.wikipedia.org/wiki/플랫폼 "wikilink")이 독립적이고, 많은 지원이 있다.

### XML 기반 언어

XML 기반 언어는 다음과 같다.

  - [RDF](https://ko.wikipedia.org/wiki/RDF "wikilink")
  - [RSS](../Page/RSS.md "wikilink")
  - [Atom](https://ko.wikipedia.org/wiki/Atom "wikilink")
  - [MathML](../Page/MathML.md "wikilink")
  - [XHTML](https://ko.wikipedia.org/wiki/XHTML "wikilink")
  - [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink")

이들 언어들은 단일하게 규정된 방식으로 정의되었기 때문에, 사전 정보가 없어도 이들 언어로 작성된 문서에 대해 수정이나 유효성 검사를 하는 프로그램도 제작할 수 있다.

## 중요 용어

이 절의 내용은 XML 명세에 기반한다. XML에 나타나는 모든 요소의 목록이 아니다. 가장 많이 쓰이는 핵심 요소만을 소개한다.

  - (유니코드) 문자: 정의 상, XML 문서는 문자로 이루어진 문자열이다. 거의 모든 올바른 [유니코드](../Page/유니코드.md "wikilink") 문자는 XML 문서에 나타날 수 있다.

<!-- end list -->

  - 프로세서(processor)와 애플리케이션(application): *프로세서*는 마크업을 분석하고 구조화된 정보를 *애플리케이션*에 넘긴다. 이 명세는 XML 프로세서가 무엇을 해야하고 하지 말아야 하는지 제시하지만, 애플리케이션에 대해서는 다루지 않는다. 이 프로세서(명세가 부르기를)는 흔히 *XML parser*라 불린다.

<!-- end list -->

  - 마크업(markup)과 내용(content): XML 문서를 구성하는 문자들은 *마크업*과 *내용*으로 나뉘는데, 그 구분은 간단한 문법 규칙으로 이루어진다. 일반적으로 마크업을 구성하는 문자열은 문자 `<`로 시작하여 문자 `>`로 끝나거나, 문자 `&`로 시작하여 문자 `;`로 끝나며, 마크업이 아닌 문자열은 내용이다. 그러나, [CDATA](https://ko.wikipedia.org/wiki/CDATA "wikilink") 절에서, 구분자 와 `]]>`는 마크업으로 분류되고, 그들 사이의 텍스트는 내용으로 구분된다. 추가로, 가장 바깥 엘리먼트의 앞과 뒤의 공백(whitespace)은 마크업으로 분류된다.

<!-- end list -->

  - 태그(tag)
    `<`로 시작하여 `>`로 끝나는 마크업 구조. 태그는 세 가지 종류가 있다:
      - *시작 태그(start-tag)*; 예: <code>
        <section>
        </code>
      - *끝 태그(end-tag)*; 예: <code>
        </section>
        </code>
      - *빈 엘리먼트(empty-element) 태그*; 예: `<line-break />`

<!-- end list -->

  - 엘리먼트(element): 문서의 논리 요소로서, 시작 태그로 시작하여 짝이 되는 끝 태그로 끝나거나, 빈 엘리먼트 태그만으로 이루어진다. 시작 태그와 끝 태그 사이의 문자들은(있다면) 엘리먼트의 *내용*이고, 마크업을 포함할 수 있다. 이 마크업은 *자식 엘리먼트(child elements)*라 부르는 다른 엘리먼트들을 포함할 수도 있다. 엘리먼트의 예는 <Greeting>`Hello, world.`</Greeting> (see [hello world](https://ko.wikipedia.org/wiki/Hello_world_program "wikilink")). 다른 예는 `<line-break />`.

<!-- end list -->

  - 애트리뷰트(Attribute): 이름/값 짝으로 이루어진 마크업 구조로 시작 태그 또는 빈 엘리먼트 태그 속에 위치한다. 다음 예에서 엘리먼트 *img*는 *src*와 *alt*의 두 애트리뷰트를 갖는다:

    ``` xml
    <img src="madonna.jpg" alt='Foligno Madonna, by Raphael'/>
    ```

    다른 예로

    ``` xml
    <step number="3">Connect A to B.</step>
    ```

    에서 애트리뷰트 이름은 "number"이고 값은 "3"이다.

<!-- end list -->

  - **XML** 선언: XML 문서는 다음과 같이 자신에 대한 정보 일부를 선언하는 것으로 시작할 수 있다:

    ``` xml
    <?xml version="1.0" encoding="UTF-8" ?>
    ```

## 문자와 이스케이프

XML 문서는 완전히 [유니코드](../Page/유니코드.md "wikilink") 문자로만 이루어진다. 소수의 일부 특별히 제외된 [제어 문자](../Page/제어_문자.md "wikilink")([control characters](https://ko.wikipedia.org/wiki/control_characters "wikilink"))를 제외하면, 유니코드에 정의된 어떤 문자든 XML 문서 내용에 나타날 수 있다.

XML은 문서를 구성하는 유니코드 문자들의 *인코딩*을 인식하고 맞게 출력하는 기능을 포함한다.

### 인코딩 감지

유니코드 문자 집합은 저장 또는 전송을 위해 여러 방법으로 부호화될 수 있다("인코딩"). Unicode itself defines encodings that cover the entire repertoire; 잘 알려진 것으로 [UTF-8](https://ko.wikipedia.org/wiki/UTF-8 "wikilink")과 [UTF-16](https://ko.wikipedia.org/wiki/UTF-16 "wikilink")이 있다.\[11\] 유니코드 이전에 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")나 [ISO/IEC 8859](https://ko.wikipedia.org/wiki/ISO/IEC_8859 "wikilink") 같은, 많은 텍스트 인코딩 방식이 있었다. 이들의 문자 집합은 대개 유니코드 문자 집합의 부분집합이다.

XML은 유니코드가 정의한 어떤 인코딩이든 사용하는 것을 허용하며, 문자들이 유니코드에 나타나는 다른 인코딩도 사용할 수 있다. XML은 또한 XML 프로세서가 안정적으로, 사전지식 없이, 어느 인코딩이 사용되고 있는지 결정하는 메커니즘을 제공한다.\[12\] UTF-8 또는 UTF-16이 아닌 인코딩은 XML 파서에 인식되지 못할 가능성이 있다.

### 주석 사용

주석은 다른 마크업의 밖이라면 어디서나 나타날 수 있다. XML 선언 전에는 올 수 없다. ""로 끝난다. 문자열 "`--`" (하이픈 두 개)는 주석 안에서는 허용되지 않는다; 즉 주석은 겹쳐질(nested) 수 없다. 주석 내에서는 앰퍼샌드(ampersand, &)가 특별한 의미를 갖지 않는다. 따라서 엔티티나 문자 참조에 이를 쓸 수 없고, 문서 인코딩에 쓰인 문자 집합 이외의 문자를 주석 내에서는 표현할 방법이 없게 된다.

유효한 주석의 예: ""

### 국제어 사용

XML 1.0 (Fifth Edition)과 XML 1.1은 거의 모든 [유니코드](../Page/유니코드.md "wikilink") 문자의 이름, 애트리뷰트, 주석, 문자 데이터, 처리 명령어에 대한 직접 사용을 지원한다.(XML 자체에 대한 특별한 기호적 의미가 있는, 예를 들어 "\<" 같은 문자는 제외). 아래는 잘 구성된(well-formed) XML 문서로 [한자](../Page/한자.md "wikilink")와 [키릴 문자를](https://ko.wikipedia.org/wiki/키릴_문자 "wikilink") 포함하고 있다:

``` xml
<?xml version="1.0" encoding="UTF-8" ?>
<俄语>данные</俄语>
```

## 웰 폼(Well-formed) 문서와 유효 XML 문서

XML 문서에는 두 가지 수준의 수정 절차가 있다:

  - **웰 폼**(Well-formed) : 웰 폼 문서는 모든 XML의 구문을 허용한다. 예를 들어, 한 요소가 닫기 태그와 자체 닫기 없이 열기 태그를 가지고 있으면, 웰 폼이라고 부르지 않는다. 웰 폼이 아닌 문서는 XML이 된다고 말하지 않는다. *순응 파서*\[13\]는 이를 처리하도록 허용하지 않는다.
  - **유효** : 유효 문서는 추가적으로 몇 가지 의미적 규칙을 허용한다. 이러한 규칙들은 사용자 정의로 되어 있거나, [XML 계획](https://ko.wikipedia.org/wiki/XML_Schema "wikilink") 또는 [DTD로](https://ko.wikipedia.org/wiki/문서_형식_정의 "wikilink") 포함된다. 예를 들어, 어느 문서가 정의되지 않은 태그를 포함하고 있으면, *유효*한 것이 아니다. *유효화 파서*는 이를 처리하도록 허용하지 않는다.

## 잘 구성됨(Well-formedness)과 오류 처리(error-handling)

XML 명세는 XML 문서를 [well-formed](https://ko.wikipedia.org/wiki/Well-formed_element "wikilink") 텍스트로 정의한다. 이는 명세에 제공된 문법 규칙들을 만족한다는 뜻이다. 긴 목록 중 핵심을 짚어 보면,

  - 문서는 적절히 인코딩된 올바른(legal) 유니코드 문자만을 포함한다.
  - `<`나 `&` 같은 특수 문법 문자 중 어떤 것도, 원래의 마크업 경계 식별 목적 이외의 목적으로 나타나지 않는다.
  - 엘리먼트의 한계를 정하는 시작 태그, 끝 태그, 빈 엘리먼트 태그들은 모두 올바르게, 빠지거나 중복됨이 없이, 겹쳐진다(nested).
  - 엘리먼트의 태그는 대소문자를 구분한다; the beginning and end tags must match exactly. 태그 이름은 다음 문자를 포함할 수 없다 ``!"#$%&'()*+,/;<=>?@[\]^`{|}~``. 또 공백 문자도 포함할 수 없으며, `-`, `.`, 또는 숫자로 시작할 수 없다.
  - 하나의 "루트root" 엘리먼트가 다른 모든 엘리먼트를 포함한다.

## 스키마(Schema)와 유효화(Validation)

잘 구성됨에 더하여, XML 문서에는 유효성(*validity*)이라는 것이 있다. 이는 문서가 [Document Type Definition](https://ko.wikipedia.org/wiki/문서_형식_정의 "wikilink") (DTD)에 대한 참조를 포함하고, 문서의 엘리먼트들과 애트리뷰트들이 그 DTD에 선언되어 있으며 DTD가 명시하는 문법 규칙을 따른다는 것을 의미한다.

XML 프로세서는 *유효화하는validating* 또는 *유효화하지 않는non-validating*으로, 유효성 검증 여부에 따라 분류한다. 유효성 오류를 조사하는 프로세서는 그것을 보고할 수 있어야 하지만, 정상 처리를 계속할 수도 있다.

DTD는 *[schema](https://ko.wikipedia.org/wiki/XML_schema "wikilink")* 또는 *문법*의 예이다. XML 1.0의 초판 발표 이래로, XML을 위한 스키마 언어 분야의 연구가 많이 이루어졌다. 그런 스키마 언어들은 전형적으로 어떤 문서에서 사용되어도 좋은 엘리먼트의 종류, 그 엘리먼트들에 적용되어도 좋은 애트리뷰트의 종류, 나타나는 순서, 허용 가능한 부모-자식 관계 등을 제한한다.

### Document Type Definition

XML을 위한 가장 오래된 스키마 언어는 [SGML](https://ko.wikipedia.org/wiki/SGML "wikilink")에서 유래한 [Document Type Definition](https://ko.wikipedia.org/wiki/문서_형식_정의 "wikilink")(DTD)이다.

DTD의 장점:

  - DTD는 XML 1.0 표준에 포함됐기 때문에 어디서나 지원된다.
  - DTD는 엘리먼트 기반 스키마 언어들에 비해 매우 간결하므로, 한 화면에 더 많은 정보를 표현할 수 있다.
  - DTD는 네임스페이스에서 쓰인 타입들이 아닌, *문서 형식*을 정의함으로써, 문서에 대한 모든 제약을 하나의 컬렉션에 모은다.

DTD의 제한점:

  - XML의 새로운 [기능들에](https://ko.wikipedia.org/wiki/:en:feature_\(software_design\) "wikilink") 대한 직접적인 지원이 없다. 가장 중요하게는 [XML Namespace](https://ko.wikipedia.org/wiki/XML_Namespace "wikilink").
  - 표현성이 떨어진다. XML DTD는 SGML DTD보다 간단해서 정규 문법으로는 표현하지 못하는 구조가 있다. DTD는 rudimentary datatype만을 지원한다.
  - 가독성이 떨어진다. DTD 설계자는 전형적으로 파라미터 엔티티를 많이 사용한다(텍스트 [매크로](https://ko.wikipedia.org/wiki/매크로 "wikilink")처럼 동작하는). 이로써 복잡한 문법을 정의하기는 쉬워지지만 명료성이 떨어진다.

### XML 스키마

DTD의 후계자로서 W3C에 의해 기술된 새로운 스키마 언어가 [XML Schema이다](https://ko.wikipedia.org/wiki/XML_Schema_\(W3C\) "wikilink"). XSD는 DTD보다 XML 언어 기술에 훨씬 강력하다. 더 풍부한 [datatyping](https://ko.wikipedia.org/wiki/Data_type "wikilink") 시스템을 사용하며 XML 문서 논리 구조에 더 세세한 제약을 가할 수 있다. XSD도 XML-기반 형식을 사용하므로, 일반적인 XML 도구로 처리할 수 있다.

## 같이 보기

  - XML 처리 API: [DOM](https://ko.wikipedia.org/wiki/DOM "wikilink"), [SAX](https://ko.wikipedia.org/wiki/SAX "wikilink"), [E4X](https://ko.wikipedia.org/wiki/E4X "wikilink")
  - [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink"), [XSL](https://ko.wikipedia.org/wiki/XSL "wikilink")
  - [DTD](https://ko.wikipedia.org/wiki/문서_형식_정의 "wikilink"), [XML Schema](https://ko.wikipedia.org/wiki/XML_Schema "wikilink")
  - [AST](https://ko.wikipedia.org/wiki/AST "wikilink")
  - [XRI](https://ko.wikipedia.org/wiki/XRI "wikilink"), [XDI](https://ko.wikipedia.org/wiki/XDI "wikilink")
  - [ASN.1](https://ko.wikipedia.org/wiki/ASN.1 "wikilink")
  - [WBXML](https://ko.wikipedia.org/wiki/WBXML "wikilink")
  - [XLink](../Page/XLink.md "wikilink")
  - [XHTML](https://ko.wikipedia.org/wiki/XHTML "wikilink")

## 각주

## 외부 링크

  - [W3C XML 홈페이지](http://www.w3.org/XML/)
  - [XML 1.0 기술 규격](http://www.w3.org/TR/REC-xml)
  - [XML 1.1 기술 규격](http://www.w3.org/TR/xml11)
  - [주석이 있는 XML 기술 규격](http://www.xml.com/axml/testaxml.htm)
  - [XML 보급/확장을 위한 XML 인터넷 데이터 센터](http://www.xmlidc.com)
  - [EasyXML](http://coderschool.dothome.co.kr)
  - [XeML.net](https://web.archive.org/web/20180316073129/http://xeml.net/)
  - [XML Java](https://web.archive.org/web/20140407072920/http://talkera.org.cp-in-1.webhostbox.net/wp/?p=79)
  - [XML Viewer](https://codebeautify.org/xmlviewer) XML 뷰어
  - [XML Formatter](https://www.mydigitaltoolbox.pro/tools/xml-formatter/) XML 포매터

[XML](https://ko.wikipedia.org/wiki/분류:XML "wikilink") [분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink") [분류:표현 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:표현_계층_프로토콜 "wikilink") [분류:데이터 직렬화 포맷](https://ko.wikipedia.org/wiki/분류:데이터_직렬화_포맷 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink") [분류:데이터 모델링 언어](https://ko.wikipedia.org/wiki/분류:데이터_모델링_언어 "wikilink")

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
12.
13. 파서: 컴퓨터에 입력된 정보를 번역, 처리하는 프로그램