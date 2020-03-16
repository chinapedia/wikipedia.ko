> This article is converted from Wikipedia: [XML  \(W3C\)](https://ko.wikipedia.org/wiki/XML__\(W3C\)).


**XML 스키마**는 2001년 5월에 [W3C 표준으로](https://ko.wikipedia.org/wiki/W3C#W3C_표준 "wikilink") 발표된\[1\] 여러 [XML 스키마 언어](../Page/XML_스키마.md "wikilink") 중 하나이다. 이는 W3C 권고를 만족하는 첫 번째 [XML](../Page/XML.md "wikilink") 스키마 전용 언어이다. XML 스키마와 W3C에서 구체적으로 지정한 것과 명칭이 같아 혼동이 되기 때문에, 사용자 커뮤니티 일부에서는 이 언어를 **WXS**라 칭하는데, 이는 W3C XML Schema의 앞 글자를 딴 것이다. 다른 이들은 XML Schema Definition의 약자인 **XSD**를 쓰기도 한다.\[2\]\[3\] 버전 1.1에서 W3C는 XSD를 선호하는 이름으로 정했으며, 이 문서에서도 XSD라 부른다.

다른 모든 XML 스키마 언어처럼, XSD는 XML 문서가 그 스키마에 대하여 '유효'한 것으로 여겨지기 위해 반드시 지켜야 하는 규칙들의 집합을 표현하는 데 쓰인다. 그러나 다른 대부분의 스키마 언어들과 달리, XSD는 문서의 유효성 검증을 통해 특정 [자료형](../Page/자료형.md "wikilink")들에 종속적인 정보들의 묶음을 만들어 내자는 의도로 설계되었다.

## 스키마들과 스키마 문서

스키마 문서는 네임스페이스(namespace)로 조직화된다: 모든 이름이 달린 스키마 구성 요소는 대상 네임스페이스에 속하며, 그 대상 네임스페이스는 스키마 문서 전체의 속성 중 하나이다. 스키마 문서는 네임스페이스가 같은 다른 스키마 문서를 포함할 수 있다. 또한 다른 네임스페이스의 스키마 문서를 불러 올 수 있다.

어떤 인스턴스 문서를 어떤 스키마에 대하여 유효성 검증할 때(*assessment*라 한다), 유효성 검증에 사용될 스키마는 유효성 검증 엔진에게 인자로 주어질 수도 있고, 인스턴스 문서 자체에서 직접 참조될 수도 있다. 인스턴스 문서가 참조할 때는 두 가지 특별한 애트리뷰트를 사용하는데, `xsi:schemaLocation`과 `xsi:noNamespaceSchemaLocation`이 그것이다. 관습적으로 "xsi"는 "[http://www.w3.org/2001/XMLSchema-instance"를](http://www.w3.org/2001/XMLSchema-instance%22를) 가리키는 접두어로 쓰인다.)

XML 스키마 문서는 대개 확장자로 ".xsd"를 갖는다. XSD에 대한 고유의 [MIME 타입은](https://ko.wikipedia.org/wiki/Internet_Media_Type "wikilink") 아직 등록되지 않았다. 따라서 RFC 3023에 따라 "application/xml" 혹은 "text/xml"을 사용해야 한다.

## 스키마 요소들

스키마의 주된 요소들은 다음과 같다:

  - **요소 선언(Element declarations)**, 요소의 속성(properties)을 정의한다. 요소 이름과 대상 네임스페이스를 포함한다. 요소의 종류(type)가 중요한 속성으로, 요소가 어떤 속성과 자식(children)을 가질 수 있는 지를 제한한다. XSD 1.1에서, 요소 종류는 그 특성 값에 따라 달라질 수 있다. 요소는 대체 그룹(substitution group)에 속할 수 있다; 만약 요소 E가 요소 H의 대체 그룹에 속하면, 스키마가 H를 허용하는 곳 어디에나 E가 나타날 수 있다. 요소는 무결성 조건(integrity constraints)을 가질 수 있다. 요소 선언은 전역(global)이거나 지역(local)일 수 있다. 따라서 인스턴스 문서(instance document)의 서로 다른 부분에서, 서로 관련이 없는 요소들을 가리키는 데 같은 이름을 쓸 수 있다.

<!-- end list -->

  - **속성 선언(Attribute declarations)**, 속성의 속성을 정의한다. 여기서도 속성 이름과 대상 네임스페이스를 포함한다. 속성의 타입은 속성이 가질 수 있는 값을 제한한다. 속성 선언에 기본값을 지정하거나, 값을 고정할 수 있다.

<!-- end list -->

  - **간단한 타입과 복잡한 타입**. 다음 절에서 다룬다.

<!-- end list -->

  - **모델 그룹**과 **속성 그룹** 정의. 요소와 속성들의 이름 있는 매크로 다양한 형 선언에서 재사용될 수 있는 필수적인 매크로이다.

다른 더 특수화된 구성요소들로 주석(annotations), [표명](../Page/표명.md "wikilink")(assertions), 표기법(notations), 스키마 전체에 대한 정보를 포함하는 **스키마 구성요소(schema component)**가 있다.

## 종류

복잡한 타입은 요소에 허용된 내용(content)을 기술하며, 거기에는 그것의 요소와 특성들과 텍스트 자식들을 포함한다. 복잡한 타입의 정의는 속성들의 집합과 내용 모형(content model)으로 이루어진다. 내용 모형에는 여러 가지가 있다. 요소-전용 내용은, 텍스트(공백이나, 자식 요소로 감싸진 텍스트는 제외)가 나타나지 않는 것이다; 간단한 내용은, 텍스트가 허용되지만 자식 엘리먼트는 허용되지 않는다; 빈 내용은, 텍스트와 자식 엘리먼트 모두 허용되지 않는다; 섞여진 내용은, 요소와 텍스트가 다 나타날 수 있다. 복잡한 타입은 다른 복잡한 타입을 제한(restriction, 기반 형식이 허용하는 일부 요소/속성/값을 금지)하거나 확장(속성이나 요소의 등장을 추가로 허용)하여 유도될 수 있다.

간단한 타입(데이터 타입 또는 자료형이라고도 한다)은 요소나 속성에 나타날 수 있는 텍스트 값을 제한한다. 이것이 XML 스키마가 [DTD](https://ko.wikipedia.org/wiki/DTD "wikilink")와의 차이 중 중요한 것이다. 예를 들어 속성은 유효한 날짜나 십진수만을 가지도록 제한될 수 있다.

XSD는 19가지 기본 자료형[primitive data type을](https://ko.wikipedia.org/wiki/primitive_data_type "wikilink") 제공한다: (`anyURI`, `base64Binary`, `boolean`, `date`, `dateTime`, `decimal`, `double`, `duration`, `float`, `hexBinary`, `gDay`, `gMonth`, `gMonthDay`, `gYear`, `gYearMonth`, `NOTATION`, `QName`, `string`, `time`). 이들 기본자료형으로부터 다음 세 가지 방법으로 새로운 자료형을 만들 수 있다:

  - restriction (허용되는 값의 집합을 줄임)
  - list (값들의 연속을 허용)
  - union (여러 타입들 중에서 값을 선택함을 허용).

명세 자체에 25가지 유도된 자료형이 정의돼 있다. 사용자는 추가로 유도된 자료형을 정의할 수 있다.

자료형을 제한하는 방법으로 최솟값과 최댓값을 지정하거나, 정규식(regular expressions)을 사용하거나, 문자열의 길이를 제한하거나, 숫자의 자릿수를 제한할 수 있다. XSD 1.1에서는 assertion이 추가되어, [XPath 2.0](https://ko.wikipedia.org/wiki/XPath_2.0 "wikilink") 식을 사용하여 임의의 제한을 규정할 수 있다.

## PSVI(Post-Schema-Validation Infoset)

XML 스키마 기반 검증(XML Schema-based validation)에 따라서, XML 문서의 구조(structure)와 내용(content)을 검증(validation) 동안 함축된 [데이터 모델로](../Page/데이터_모델.md "wikilink") 표현할 수 있게 되었다. XML 스키마 데이터 모델은 다음을 포함한다:

  - 요소와 속성의 이름들 (The vocabulary)
  - 관계와 구조 (The content model)
  - 자료형

이러한 자료의 집합을 PSVI(Post-Schema-Validation Infoset 라고 한다. PSVI는 XML 문서의 "타입"을 명확히 하고, [객체지향 프로그래밍(OOP)](https://ko.wikipedia.org/wiki/객체지향 "wikilink") 패러타임을 통해 문서가 객체로 취급될 수 있도록 도와준다.

## 예제

간단한 스키마 문서로 주소를 기술하는 예.

``` xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema elementFormDefault="qualified" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="Address">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="Recipient" type="xs:string" />
        <xs:element name="House" type="xs:string" />
        <xs:element name="Street" type="xs:string" />
        <xs:element name="Town" type="xs:string" />
        <xs:element name="County" type="xs:string" minOccurs="0" />
        <xs:element name="PostCode" type="xs:string" />
        <xs:element name="Country" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="IN" />
              <xs:enumeration value="DE" />
              <xs:enumeration value="ES" />
              <xs:enumeration value="UK" />
              <xs:enumeration value="US" />
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

스키마의 도식화 표현을 만들어 주는 개발 도구들이 있다. 대개 아래와 같은 다이어그램을 생성한다:

[파일:SimpleAddress.png](https://ko.wikipedia.org/wiki/파일:SimpleAddress.png "wikilink")

이 스키마를 따르는 XML 문서의 예

``` xml
<?xml version="1.0" encoding="utf-8"?>
<Address xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:noNamespaceSchemaLocation="SimpleAddress.xsd">
  <Recipient>Mr. Walter C. Brown</Recipient>
  <House>49</House>
  <Street>Featherstone Street</Street>
  <Town>LONDON</Town>
  <PostCode>EC1Y 8SY</PostCode>
  <Country>UK</Country>
</Address>
```

## XML 스키마의 다른 용도

XML 스키마를 정의하는 주된 이유는 명확하게 XML 문서를 설명하기 위함이다. 그러나 단순한 XML 스키마 확인을 넘어서 다른 많은 용도로 사용된다.

### 코드 생성

스키마는 코드 생성에 쓰일 수 있으며, 이를 [XML 데이터 바인딩이라](https://ko.wikipedia.org/wiki/XML_데이터_바인딩 "wikilink") 한다. 이 코드는 XML 문서의 내용을 프로그래밍 환경의 객체처럼 취급할 수 있게 한다.

### XML 파일 구조 문서 생성

XML 파일 구조에 대한, 사람이 읽을 수 있는 문서를 만드는 데 쓰일 수 있다. 이는 특히 저자가 주석 요소를 사용했을 때 유용하다. 문서 생성에 규격화된 표준은 존재하지 않는다. 하지만 몇 가지 툴이 나와 있다. [Xs3p](https://ko.wikipedia.org/wiki/Xs3p "wikilink") 스타일시트가 그것으로, 고품질의 읽을 수 있는 HTML과 인쇄물을 생성한다.

## 버전 1.1

XSD 1.1이 [2012 4월](http://www.w3.org/News/2012#entry-9412) 에 [W3C](https://ko.wikipedia.org/wiki/World_Wide_Web_Consortium#W3C_Recommendation_.28REC.29 "wikilink") 권고안이 되었다. 이는 승인된 W3C 표준이 되었음을 의미한다.

## 참고 자료

  - *Definitive XML Schema*, Priscilla Walmsley, Prentice-Hall, 2001,
  - *XML Schema*, Eric van der Vlist, O'Reilly, 2001,
  - *The XML Schema Companion*, Neil Bradley, Addison-Wesley, 2003,
  - *Professional XML Schemas*, Jon Ducket et al., Wrox Press, 2001,
  - *XML Schemas*, Lucinda Dykes et al., Sybex,

## 각주

## 외부 링크

**W3C XML Schema 1.0 Specification**

  - [XSD 1.0 Primer](http://www.w3.org/TR/xmlschema-0/)
  - [XSD 1.0 Structures](http://www.w3.org/TR/xmlschema-1/)
  - [XSD 1.0 Datatypes](http://www.w3.org/TR/xmlschema-2/)
  - [Tools](http://www.w3.org/XML/Schema#Tools)

**W3C XML Schema 1.1 Specification**

  - [XSD 1.1 Structures](http://www.w3.org/TR/xmlschema11-1/)
  - [XSD 1.1 Datatypes](http://www.w3.org/TR/xmlschema11-2/)

**Other**

  -
  -
  - [SPARQL2XQuery](http://www.dblab.ntua.gr/~bikakis/SPARQL2XQuery.html) Tranform XML Schema to OWL. Map XML Schemas and OWL-RDF/S ontologies.

[분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink")

1.
2.  [Schema - W3C](http://www.w3.org/standards/xml/schema)
3.  [W3C XML Schema Definition Language (XSD) 1.1 Part 1: Structures](http://www.w3.org/TR/xmlschema11-1/)