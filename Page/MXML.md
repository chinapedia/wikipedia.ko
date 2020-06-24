> This article is converted from Wikipedia: [MXML](https://ko.wikipedia.org/wiki/MXML).


**MXML**은 2004년 3월 매크로미디어사가 도입한 [XML](../Page/XML.md "wikilink") 기반의 사용자 인터페이스 생성 언어이다. 어도비(2005년 12월에 매크로미디어를 인수하였음.)에서는 MXML이 어떤 뜻의 줄임말이라고 공식적으로 언급된 바가 없다. 하지만 어떠한 개발자들은 'Magic eXtensible Markup Language'라는 표현을 표준으로 하자고 제안하고 있다. 또한 이것은 2002년과 2004년 사이에 출시된 매크로미디어의 제품군의 접미사(Macromedia eXtensible Markup Language)로서 'MX'에서 유래되었다고 보기도 한다. [웹 애플리케이션](../Page/웹_애플리케이션.md "wikilink") 개발자들은 [액션스크립트](../Page/액션스크립트.md "wikilink")와 같이 MXML을 사용하여 리치 인터넷 애플리케이션을 개발한다.

MXML은 주로 애플리케이션의 화면 레이아웃을 선언하는 데 사용된다. 그리고 복잡한 업무로직이나 리치 인터넷 애플리케이션 작업에 사용할 수 있다. 중괄호(**{**)를 사용하게 되면 컴퓨터로 하여금 해당 부분을 변수로 인식하게 하는 것이나 점 표기법(dot notation)을 통해 객체의 다양한 변수와 메서드에 접근하는 것과 같은 일반적인 문법을 따라간다.

**MXML**은 1.5버전까지 그리고 FDS(Flex Data Services) 또는 LCDS(LiveCycle Data Services)에서는 서버단에서 런타임시 표준 바이너리 SWF 파일로 변환하는 데에 쓰인다. 그러나 어도비의 플렉스 빌더 IDE나 공개된 플렉스 SDK에서 MXML로부터 SWF 파일을 만들어낼 수 있다.

MXML은 어도비의 기술과 단단히 통합되어 있기 때문에 독점적인 표준이라고 여겨진다. 이런 면에서 XAML과 비슷한 면이 있다. MXML 문서와 UIML, XUL, XAML 또는 [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink")와 같은 다른 [사용자 인터페이스](../Page/사용자_인터페이스.md "wikilink") 언어와의 변환을 위한 공식적인 문서는 없다.

## 보기

``` mxml
<?xml version="1.0" encoding="utf-8"?>
<mx:Application xmlns:mx="http://www.adobe.com/2006/mxml">
    <mx:Array id="sampleArray">
        <mx:String>예제 문서제목 1</mx:String>
        <mx:String>예제 문서제목 2</mx:String>
    </mx:Array>
    <mx:Panel title="패널 예제">
        <mx:ComboBox dataProvider="{sampleArray}"></mx:ComboBox>
    </mx:Panel>
</mx:Application>
```

## 같이 보기

  - [어도비 플렉스](https://ko.wikipedia.org/wiki/어도비_플렉스 "wikilink")
  - [XML](../Page/XML.md "wikilink")
  - [어도비 플래시](../Page/어도비_플래시.md "wikilink")

## 외부 링크

  - [Flex 빠른 시작 가이드: 시작하기](https://web.archive.org/web/20070923072513/http://www.adobe.com/kr/devnet/flex/quickstart/coding_with_mxml_and_actionscript/): 어도비 개발자 센터
  - <https://web.archive.org/web/20090525075722/http://try.flex.org/> : 위의 예제가 실제 플래시 응용으로 어떻게 컴파일되는지 확인하려면 소스를 복사하여 이 사이트의 문서 편집 창에 붙여 넣으면 된다.

[분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:웹 개발 소프트웨어](https://ko.wikipedia.org/wiki/분류:웹_개발_소프트웨어 "wikilink") [분류:선언형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:선언형_프로그래밍_언어 "wikilink")