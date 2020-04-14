> This article is converted from Wikipedia: [StAX](https://ko.wikipedia.org/wiki/StAX).


**StAX**(Streaming API for XML)는 XML 문서를 처리하는 [자바 API로서](https://ko.wikipedia.org/wiki/자바_API "wikilink"), 기존 [DOM](https://ko.wikipedia.org/wiki/DOM "wikilink") 및 [SAX](https://ko.wikipedia.org/wiki/SAX "wikilink")에 추가된 API이다.

기존 XML API는 2가지 방식이었다.

  - 트리 기반 : 문서 전체를 트리(Tree) 구조로 메모리로 읽어서 랜덤하게 접근이 가능하다.
  - 이벤트 기반 : 문서의 한 항목식 이벤트가 발생하여 응용 프로그램에서 처리한다.

2가지 방식은 각각 보완작용을 한다. 트리 기반([DOM](https://ko.wikipedia.org/wiki/DOM "wikilink"))은 문서의 구조 해석이 가능하고, 이벤트 기반([SAX](https://ko.wikipedia.org/wiki/SAX "wikilink"))은 메모리를 적게 사용하면서 신속한 작동이 가능하다.

StAX는 이러한 방식의 중간 방식으로 설계되었다. StAX 방식은 프로그램의 동작점, 즉 문서의 한지점을 가리키는 커서가 있는 방식이다. 이러한 이유로 응용 프로그램은 필요에 따라 정보를 추출할 수 있게 된다. (pull 형) 이것이 기존 [SAX](https://ko.wikipedia.org/wiki/SAX "wikilink")와 같은 이벤트 기반 API와 다른 점이다. SAX는 파서에서 응용 프로그램으로 데이터를 보내는 방식이다. (push형)

## 예시

JSR-173 사양 최종판, V1.0 (공정 이용으로 사용됨).

인용:

  -
    다음 자바 API는 커서 접근에서 XML을 읽기 위한 메인 메소드를 보여준다.

<!-- end list -->

``` java
public interface XMLStreamReader {
    public int next() throws XMLStreamException;
    public boolean hasNext() throws XMLStreamException;
    public String getText();
    public String getLocalName();
    public String getNamespaceURI();
    // ...other methods not shown
}
```

  -
    API의 기록 사이드에는 StartElement와 EndElement 이벤트 타입을 위한 읽기 사이드와 일치하는 메소드가 있다.

<!-- end list -->

``` java
public interface XMLStreamWriter {
    public void writeStartElement(String localName) throws XMLStreamException;
    public void writeEndElement() throws XMLStreamException;
    public void writeCharacters(String text) throws XMLStreamException;
    // ...other methods not shown
}
```

  -
    5.3.1 XMLStreamReader
    이 예제는 인풋 팩토리를 인스턴스화하고 리더를 만들고 XML 문서의 요소들을 반복시키는 방법을 기술한다.

<!-- end list -->

``` java
XMLInputFactory xmlInputFactory = XMLInputFactory.newInstance();
XMLStreamReader xmlStreamReader = xmlInputFactory.createXMLStreamReader(...);
while (xmlStreamReader.hasNext()) {
    xmlStreamReader.next();
}
```

## 외부 링크

  - [Introduction to StAX](http://www.xml.com/pub/a/2003/09/17/stax.html) XML.com, Harold, Elliotte Rusty
  - [Java Streaming API for XML (Stax) - Tutorial](https://web.archive.org/web/20071212145813/http://www.vogella.de/articles/JavaXML/article.html)
  - [XMLPull Patterns](https://web.archive.org/web/20120630184808/http://www.extreme.indiana.edu/~aslom/xmlpull/patterns.html) Article on XML Pull (and StAX) design patterns by Aleksander Slominski.
  - [StAX Parser - Cursor & Iterator APIs](https://howtodoinjava.com/xml/read-xml-stax-parser-cursor-iterator/) Article on Cursor & Iterator APIs by HowToDoInJava.

[분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:XML](https://ko.wikipedia.org/wiki/분류:XML "wikilink")