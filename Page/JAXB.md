> This article is converted from Wikipedia: [JAXB](https://ko.wikipedia.org/wiki/JAXB).


**JAXB**(Java Architecture for XML Binding)는 자바 클래스를 XML로 표현하는 [자바 API이다](https://ko.wikipedia.org/wiki/자바_API "wikilink"). JAXB는 주로 2가지 기능이 있다. 자바 객체를 XML로 직렬화하는 것이고 반대로 XML에서 자바 객체로 역직렬화하는 것이다. 즉, JAXB는 메모리의 데이터를 XML 형식으로 변환하여 저장할 수 있고, 이 과정을 위해 프로그램의 각 클래스에서 XML을 읽고 저장하는 일을 구현해야 한다.

## 기본 자료형 바인딩

다음 표는 [XML 스키마](../Page/XML_스키마_\(W3C\).md "wikilink")(XSD) 자료형을 JAXB의 자바 자료형과 매핑한 것을 나열한 것이다.\[1\]

| XML 스키마 타입               | 자바 자료형                                    |
| ------------------------ | ----------------------------------------- |
| `xsd:string`             | `java.lang.String`                        |
| `xsd:integer`            | `java.math.BigInteger`                    |
| `xsd:positiveInteger`    | `java.math.BigInteger`                    |
| `xsd:int`                | **`int`**                                 |
| `xsd:long`               | **`long`**                                |
| `xsd:short`              | **`short`**                               |
| `xsd:decimal`            | `java.math.BigDecimal`                    |
| `xsd:float`              | **`float`**                               |
| `xsd:double`             | **`double`**                              |
| `xsd:boolean`            | **`boolean`**                             |
| `xsd:byte`               | **`byte`**                                |
| `xsd:QName`              | `javax.xml.namespace.QName`               |
| `xsd:dateTime`           | `javax.xml.datatype.XMLGregorianCalendar` |
| `xsd:base64Binary`       | **`byte[]`**                              |
| `xsd:hexBinary`          | **`byte[]`**                              |
| `xsd:unsignedInt`        | **`long`**                                |
| `xsd:unsignedShort`      | **`int`**                                 |
| `xsd:unsignedByte`       | **`short`**                               |
| `xsd:unsignedLong`       | `java.math.BigDecimal`                    |
| `xsd:time`               | `javax.xml.datatype.XMLGregorianCalendar` |
| `xsd:date`               | `javax.xml.datatype.XMLGregorianCalendar` |
| `xsd:g`                  | `javax.xml.datatype.XMLGregorianCalendar` |
| `xsd:anySimpleType`\[2\] | `java.lang.Object`                        |
| `xsd:anySimpleType`\[3\] | `java.lang.String`                        |
| `xsd:duration`           | `javax.xml.datatype.Duration`             |
| `xsd:NOTATION`           | `javax.xml.namespace.QName`               |
|                          |                                           |

## 버전 역사

| JAXB version | 발표 | 자바 플랫폼    | 중요한 변화                                                  |
| ------------ | -- | --------- | ------------------------------------------------------- |
| JAXB 2.0     |    | Java EE 5 | [JSR](https://ko.wikipedia.org/wiki/JSR "wikilink") 222 |
| JAXB 1.0     |    |           | [JSR](https://ko.wikipedia.org/wiki/JSR "wikilink") 31  |

JAXB API 역사

## 각주

## 외부 링크

  - [JAXB home page](http://jaxb.java.net/) Reference Implementation on Project [GlassFish](https://ko.wikipedia.org/wiki/GlassFish "wikilink")
  - [previous JAXB home page](http://java.sun.com/xml/jaxb/index.jsp)

[분류:자바 플랫폼, 엔터프라이즈 에디션](https://ko.wikipedia.org/wiki/분류:자바_플랫폼,_엔터프라이즈_에디션 "wikilink")

1.
2.  for `xsd:element` of this type
3.  for `xsd:attribute` of this type