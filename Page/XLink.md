> This article is converted from Wikipedia: [XLink](https://ko.wikipedia.org/wiki/XLink).


**XLink**(XML Linking Language, XML 링크 언어)는 [XML](../Page/XML.md "wikilink") 문서에서 사용되는 [하이퍼링크](../Page/하이퍼링크.md "wikilink")를 만들기 위한 XML [마크업 언어이다](../Page/마크업_언어.md "wikilink"). XLink 는 [XML](../Page/XML.md "wikilink") 문서에 속한 내부 혹은 외부 자원간의 링크를 표현하기 위해 [W3C](../Page/W3C.md "wikilink")를 따른다.

## XLink의 사용 의의

XLink는 [하이퍼링크](../Page/하이퍼링크.md "wikilink")를 제공함에 있어 기존의 [HTML](../Page/HTML.md "wikilink") 링크와 유사성을 가지나 다음과 같은 차이점을 가진다.

  - 기존 [HTML](../Page/HTML.md "wikilink")링크에서 지원하지 않았던 양방향 링크를 제공한다.
  - 문자 단위의 문서 세부 위치 지정 링크가 가능하다.
  - 링크 정보만 따로 문서화 하여 관리할 수 있다.
  - 링크에 의미 부여가 가능하다
  - [XML](../Page/XML.md "wikilink") 문서 중 일부분만 링크되도록 할 수 있다.

## XLink의 네임스페이스

XLink의 [네임스페이스](https://ko.wikipedia.org/wiki/네임스페이스 "wikilink")는 다음과 같다.

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<elementmame xmlns:xlink="http://www.w3.org/1999/xlink"/>
```

## Xlink의 기타 선택 속성

### xlink:show

링크된 리소스가 표현되는 방식을 기술한다.

  - new

새창으로 보여주기.

  - replace

현재 화면을 해당 리소스로 갱신됨.

  - embed

해당 리소스의 부분이 링크가 걸린 엘리먼트의 자리에 삽입되어 표시됨.

  - undefined

응용 프로그램이 알아서 처리하게 한다.

### xlink:actuate

리소스를 가져 올 시점을 기술한다.

  - onload

XML 문서가 전부 로딩 된 후 로딩한다.

  - onRequest

사용자가 선택하면 가져온다.

  - undefined

응용 프로그램이 알아서 처리하게 한다.

### xlink:arcrole

컴퓨터가 이해할 수 있는 arc 이름을 기술한다. 반드시 QName(접두사:이름) 형태로 기술한다.

### xlink:title

풍선 도움말에 해당하는 내용을 기술한다.

## 단순 링크

  - XLink의 단순 링크를 사용하기 위해서는 xlink:type 속성을 simple 으로 선언해야 한다.
  - 이동할 XML문서의 URI는 xlink:href 항목에 기술한다.
  - 단순 링크에 기타 선택 속성을 추가 할 수 있다.

### 단순 링크의 사용 예

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<XLinksample xmlns:xlink="http://www.w3.org/1999/xlink"
xlink:type="simple"
xlink:href="somexml.xml">someXML</XLinksample>
```

## 확장 링크

확장 링크는 여러개의 자원을 링크 할 수 있다. 리소스가 로컬에 있거나 원격지에 있어도 여러개의 arc들로 연결 할 수 있다. label을 사용하여 자원들을 체계화 하고 하나 또는 더 많은 arc들을 이용한다면 확장링크는 자원간 연결된 자유로운 링크를 만들 수 있다.

예를 들어, 확장 링크 된 모든 자원들의 label이 A라고 해보자, 이때 arc 속성이 A 에서 A 로의 링크를 정의 한다면 라벨이 A인 모든 자원이 연결 된 것이다. 이 정의에서 어떤 자료에서 다른 자료로 옮겨가는 링크는 자유롭다.

확장 링크는 자신이 링크하려는 자원의 전체를 링크 할 필요가 없다. 사용자는 필요에 따라 [메타데이터](../Page/메타데이터.md "wikilink")나 다른 추가적 데이터들을 편집하지 않고서도 필요한 부분만 링크하여 쓸 수 있을 것이다.

XLink는 또한 다양한 타입의 연결 형식과 자원들의 역할을 정의 할 수 있다.

### 확장 링크의 요소들

XLink의 확장 링크 형식에서는 다음과 같은 요소들이 필요하다.

  - Locator 요소

확장 링크가 가리키는 자원에 대한 [URI](https://ko.wikipedia.org/wiki/URI "wikilink") 를 기술하는 요소, 원격 리소스를 지정한다.

  - Resource 요소

링크를 사용하기 위해서 사용하는 요소, 로컬 리소스를 지정한다.

  - Arc 요소

링크의 연결 방향을 지정하고 링크가 진행되는 방향을 지정하는 요소. arc 요소는 한 방향의 링크 방향을 나타낼 수 있는 단방향적 요소이다.

### 확장 링크의 사용 예

  - main.xml

<!-- end list -->

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<books xmlns:xlink="http://www.w3.org/1999/xlink" xlink:type="extended">

<author xlink:type="locator"
xlink:label="author"
 xlink:title="author"
xlink:href="author.xml"/>

<list xlink:type="resource" xlink:label="list">view list</list>

<viewauthor xlink:type="arc"
xlink:from="list"
xlink:to="author"
xlink:title="author"
xlink:actuate="onRequest"
xlink:show="new"/>

</books>
```

  - author.xml

<!-- end list -->

``` xml
<?xml version="1.0" encoding="UTF-8"?>
   <author>
      <name>DRG</name>
      <country>KOR</country>
   </author>
```

## 외부 링크

  - [W3C Recommendation](http://www.w3.org/TR/xlink11/)

  - [W3C Recommendation (version 1.0)](http://www.w3.org/TR/xlink/)

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink") [분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink")