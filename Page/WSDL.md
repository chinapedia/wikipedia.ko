> This article is converted from Wikipedia: [WSDL](https://ko.wikipedia.org/wiki/WSDL).


**WSDL**(Web Services Description Language의 약자)은 [웹 서비스](../Page/웹_서비스.md "wikilink") 기술언어 또는 기술된 정의 파일의 총칭으로 XML로 기술된다. 웹 서비스의 구체적 내용이 기술되어 있어 서비스 제공 장소, 서비스 메시지 포맷, 프로토콜 등이 기술된다.

## 개요

[섬네일](https://ko.wikipedia.org/wiki/파일:WSDL_11vs20.png "wikilink") WSDL은 네트워크의 엔드포인트나 포트의 총집합으로서의 서비스를 기술한다. WSDL의 사양은 [XML](../Page/XML.md "wikilink") [형식을](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 제공한다.

WSDL은 자주 [SOAP](../Page/SOAP.md "wikilink")와 [XML 스키마와](../Page/XML_스키마_\(W3C\).md "wikilink") 결합하여 [인터넷](../Page/인터넷.md "wikilink") 상에 웹 서비스를 제공하기 위해 사용되기도 한다. 웹 서비스에 연결되는 클라이언트 프로그램은 WSDL 파일을 읽어들여 서버에 어떠한 조작이 가능한지를 결정할 수 있다.

현재의 WSDL 버전은 2.0이다. 버전 1.1은 [W3C](../Page/W3C.md "wikilink")에 의해 서명되지 않았으나 버전 2.0은 W3C 권고안이다.\[1\] 1.1버전까지는 WSDL의 D는 Definition을 뜻하였다. WSDL 1.2가 WSDL 2.0으로 바뀐 이유는 WSDL 1.1과의 근본적인 차이 때문이다. 모든 [HTTP 요청 메소드에](../Page/HTTP.md "wikilink") 바인드하는 것을 허용함으로써(버전 1.1에서처럼 GET, POST뿐 아니라) WSDL 2.0 사양은 [RESTful](https://ko.wikipedia.org/wiki/RESTful "wikilink") [웹 서비스에](../Page/웹_서비스.md "wikilink") 대한 더 나은 지원을 제공하며 구현하기가 훨씬 더 쉬워졌다.\[2\]\[3\]

{{-}}

| WSDL 1.1 용어 | WSDL 2.0 용어 | 설명                                                                                                                                                         |
| ----------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Service     | Service     | 웹 기반 프로토콜에 노출되는 시스템 함수의 집합을 포함한다.                                                                                                                          |
| Port        | Endpoint    | 웹 서비스로의 주소 또는 연결 지점을 정의한다. 단순 HTTP URL 문자열로 표현하는 것이 보통이다.                                                                                                  |
| Binding     | Binding     | 인터페이스를 규정하고 [SOAP](../Page/SOAP.md "wikilink") 바인딩 스타일(RPC/Document)과 트랜스포트([SOAP](../Page/SOAP.md "wikilink") 프로토콜)을 정의한다. binding 섹션 또한 operation을 정의한다. |
| PortType    | Interface   | 웹 서비스를 정의한다.                                                                                                                                               |
| Operation   | Operation   | SOAP의 동작 및 메시지 인코딩 방식을 정의한다.                                                                                                                               |
| Message     | 없음          | 보통 message는 operation에 상응한다.                                                                                                                               |
| Types       | Types       | 데이터를 기술한다.                                                                                                                                                 |

## 예제

WSDL 2.0 문서의 구조:

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<description ns="http://www.w3.org/ns/wsdl"
             xmlns:tns="http://www.example.com/wsdl20sample"
             xmlns:whttp="http://www.w3.org/ns/wsdl/http"
             xmlns:wsoap="http://www.w3.org/ns/wsdl/soap"
             targetNamespace="http://www.example.com/wsdl20sample">


<!-- Abstract types -->
   <types>
      <xs:schema ns="http://www.example.com/wsdl20sample"
                 xmlns:xs="http://www.w3.org/2001/XMLSchema"
                 targetNamespace="http://www.example.com/wsdl20sample">

         <xs:element name="request">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="header" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:simpleContent>
                           <xs:extension base="xs:string">
                              <xs:attribute name="name" type="xs:string" use="required"/>
                           </xs:extension>
                        </xs:simpleContent>
                     </xs:complexType>
                  </xs:element>
                  <xs:element name="body" type="xs:anyType" minOccurs="0"/>
               </xs:sequence>
               <xs:attribute name="method" type="xs:string" use="required"/>
               <xs:attribute name="uri" type="xs:anyURI" use="required"/>
            </xs:complexType>
         </xs:element>

         <xs:element name="response">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="header" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:simpleContent>
                           <xs:extension base="xs:string">
                              <xs:attribute name="name" type="xs:string" use="required"/>
                           </xs:extension>
                        </xs:simpleContent>
                     </xs:complexType>
                  </xs:element>
                  <xs:element name="body" type="xs:anyType" minOccurs="0"/>
               </xs:sequence>
               <xs:attribute name="status-code" type="xs:anySimpleType" use="required"/>
               <xs:attribute name="response-phrase" use="required"/>
            </xs:complexType>
         </xs:element>
      </xs:schema>
   </types>


<!-- Abstract interfaces -->
   <interface name="RESTfulInterface">
      <fault name="ClientError" element="tns:response"/>
      <fault name="ServerError" element="tns:response"/>
      <fault name="Redirection" element="tns:response"/>
      <operation name="Get" pattern="http://www.w3.org/ns/wsdl/in-out">
         <input messageLabel="GetMsg" element="tns:request"/>
         <output messageLabel="SuccessfulMsg" element="tns:response"/>
      </operation>
      <operation name="Post" pattern="http://www.w3.org/ns/wsdl/in-out">
         <input messageLabel="PostMsg" element="tns:request"/>
         <output messageLabel="SuccessfulMsg" element="tns:response"/>
      </operation>
      <operation name="Put" pattern="http://www.w3.org/ns/wsdl/in-out">
         <input messageLabel="PutMsg" element="tns:request"/>
         <output messageLabel="SuccessfulMsg" element="tns:response"/>
      </operation>
      <operation name="Delete" pattern="http://www.w3.org/ns/wsdl/in-out">
         <input messageLabel="DeleteMsg" element="tns:request"/>
         <output messageLabel="SuccessfulMsg" element="tns:response"/>
      </operation>
   </interface>



<!-- Concrete Binding Over HTTP -->
   <binding name="RESTfulInterfaceHttpBinding" interface="tns:RESTfulInterface"
            type="http://www.w3.org/ns/wsdl/http">
      <operation ref="tns:Get" whttp:method="GET"/>
      <operation ref="tns:Post" whttp:method="POST"
                 whttp:inputSerialization="application/x-www-form-urlencoded"/>
      <operation ref="tns:Put" whttp:method="PUT"
                 whttp:inputSerialization="application/x-www-form-urlencoded"/>
      <operation ref="tns:Delete" whttp:method="DELETE"/>
   </binding>

<!-- Concrete Binding with SOAP-->
   <binding name="RESTfulInterfaceSoapBinding" interface="tns:RESTfulInterface"
            type="http://www.w3.org/ns/wsdl/soap"
            wsoap:protocol="http://www.w3.org/2003/05/soap/bindings/HTTP/"
            wsoap:mepDefault="http://www.w3.org/2003/05/soap/mep/request-response">
      <operation ref="tns:Get" />
      <operation ref="tns:Post" />
      <operation ref="tns:Put" />
      <operation ref="tns:Delete" />
   </binding>


<!-- Web Service offering endpoints for both the bindings-->
   <service name="RESTfulService" interface="tns:RESTfulInterface">
      <endpoint name="RESTfulServiceRestEndpoint"
                binding="tns:RESTfulInterfaceHttpBinding"
                address="http://www.example.com/rest/"/>
      <endpoint name="RESTfulServiceSoapEndpoint"
                binding="tns:RESTfulInterfaceSoapBinding"
                address="http://www.example.com/soap/"/>
   </service>
</description>
```

## 역사

WSDL 1.0(2000년 9월)은 SOAP 툴킷에 웹 서비스를 기술하기 위해 [IBM](../Page/IBM.md "wikilink"), [마이크로소프트](../Page/마이크로소프트.md "wikilink"), [Ariba에](https://ko.wikipedia.org/wiki/SAP_Ariba "wikilink") 의해 개발되었다. 2개의 서비스 기술 언어를 병합함으로써 만들어졌다: IBM의 NASSL(Network Application Service Specification Language)과 마이크로소프트의 SDL(Service Description Language).

2001년 3월에 출판된 WSDL은 WSDL 1.0의 형식을 갖춘 판이다. 1.0과 1.1 간에 도입된 주요 변경사항은 없다.

WSDL 1.2(2013년 6월)은 W3C에서 작업 중인 초안이었으나 WSDL 2.0이 되었다.

## 각주

## 외부 링크

  - [WSDL 1.0 Specification](http://xml.coverpages.org/wsdl20000929.html)

  - [WSDL 1.1 Specification](http://www.w3.org/TR/wsdl)

  - [WSDL 2.0 Specification Part 0: Primer (Latest Version)](http://www.w3.org/TR/wsdl20-primer/)

  - [WSDL 2.0 Specification Part 1: Core (Latest Version)](http://www.w3.org/TR/wsdl20/)

  - [WSDL 2.0 Specification Part 2: Adjuncts (Latest Version)](http://www.w3.org/TR/wsdl20-adjuncts/)

  - [Web Services Description Working Group](http://www.w3.org/2002/ws/desc/)

  - [XML protocol activity](http://www.w3.org/2000/xp/)

[분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink")

1.
2.
3.