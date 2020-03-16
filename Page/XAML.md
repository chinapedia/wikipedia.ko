> This article is converted from Wikipedia: [XAML](https://ko.wikipedia.org/wiki/XAML).


[섬네일](https://ko.wikipedia.org/wiki/파일:Wpfapp.PNG "wikilink") **확장 응용 프로그램 마크업 언어**(Extensible Application Markup Language), 곧 **XAML**(\[zæ:mɛl\])로 발음)은 [마이크로소프트](../Page/마이크로소프트.md "wikilink")사가 구조값과 객체를 초기화하는 데 사용하려고 만든 선언형 [XML](../Page/XML.md "wikilink") 기반 언어이다. 마이크로소프트사의 [Open Specification Promise를](https://ko.wikipedia.org/wiki/Open_Specification_Promise "wikilink") 통해 사용할 수 있다.\[1\] XAML은 원래 [윈도 프레젠테이션 파운데이션의](https://ko.wikipedia.org/wiki/윈도_프레젠테이션_파운데이션 "wikilink") 코드 이름이기도 했던 Avalon에서 따와서 "eXtension Avalon Markup Language"를 대표하는 말이었다.\[2\]

## 개요

XAML은 [닷넷 프레임워크 3.0](../Page/닷넷_프레임워크.md "wikilink") 기술에, 특히 [윈도 프레젠테이션 파운데이션](https://ko.wikipedia.org/wiki/윈도_프레젠테이션_파운데이션 "wikilink")(WPF), [윈도 워크플로 파운데이션](https://ko.wikipedia.org/wiki/윈도_워크플로_파운데이션 "wikilink")(WF)에 널리 쓰인다. WPF에서 XAML은 [사용자 인터페이스 마크업 언어로](https://ko.wikipedia.org/wiki/사용자_인터페이스_마크업_언어 "wikilink") 쓰이면서 사용자 인터페이스의 요소, 데이터 바인딩, 이벤트 등의 기능을 정의한다. 윈도 워크플로 파운데이션에서 [워크플로](https://ko.wikipedia.org/wiki/워크플로 "wikilink")는 XAML을 사용하여 정의할 수 있다.

XAML 요소는 [공통 언어 런타임](../Page/공통_언어_런타임.md "wikilink") 객체 인터페이스에 직접 매핑할 수 있지만 XAML은 공통 언어 런타임 속성과 이벤트를 해당 객체로 매핑하는 데 사용한다. XAML 파일은 [마이크로소프트 익스프레션 블렌드](https://ko.wikipedia.org/wiki/마이크로소프트_익스프레션_블렌드 "wikilink"), [마이크로소프트 비주얼 스튜디오](../Page/마이크로소프트_비주얼_스튜디오.md "wikilink"), 호스팅 가능한 [윈도 워크플로 파운데이션](https://ko.wikipedia.org/wiki/윈도_워크플로_파운데이션 "wikilink") 비주얼 디자이너와 같은 시각 디자인 도구로 만들고 편집할 수 있다. 표준 [문서 편집기](../Page/문서_편집기.md "wikilink"), [XAMLPad](https://ko.wikipedia.org/wiki/XAMLPad "wikilink")와 같은 코드 편집기, [Vectropy](https://ko.wikipedia.org/wiki/Vectropy "wikilink")와 같은 그래픽 편집기로 만들어 편집할 수도 있다.

XAML을 추가하거나 그것으로 만든 어떠한 것이든 [C\#](../Page/C_샤프.md "wikilink"), [비주얼 베이직 닷넷과](../Page/비주얼_베이직_닷넷.md "wikilink") 같은 기존에 쓰여왔던 닷넷 언어를 사용하여 표현할 수 있다. 그러나 이 기술의 주된 측면은 [XML](../Page/XML.md "wikilink") 기반이기에 XAML을 처리하는 도구에 필요한 복잡성을 줄이는 것이다.\[3\] 그 결과 다양한 제품이 XAML 기반의 응용 프로그램을 만들 수 있는(특히 [윈도 프레젠테이션 파운데이션](https://ko.wikipedia.org/wiki/윈도_프레젠테이션_파운데이션 "wikilink")) 공간에서 등장하고 있다. XAML은 단순히 XML 기반이므로 개발자들과 디자이너들은 컴파일을 하지 않아도 그들 사이에서 콘텐츠를 자유로이 공유하고 편집할 수 있다.

## 예

이 윈도우 프레젠테이션 파운데이션의 예는 캔버스(Canvas)라 불리는 최상위 XAML 컨테이너에 "Hello, world\!"를 표시한다.

``` XML
<Canvas ns="http://schemas.microsoft.com/client/2007"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
  <TextBlock>Hello, world!</TextBlock>
</Canvas>
```

스키마(ns="<https://web.archive.org/web/20170705010515/http://schemas.microsoft.com/>..." 부분)는 컴퓨터에서 동작할 수 있게 변경할 필요가 있다. 마이크로소프트가 권장하는 스키마를 사용한 예시는 다음과 같을 수도 있다.\[4\]

``` XML
<Canvas ns="http://schemas.microsoft.com/winfx/2006/xaml/presentation">
  <TextBlock>Hello, world!</TextBlock>
</Canvas>
```

이것은 브라우저 내에 호스팅되는 샌드박스 환경에서 실행되는 컴파일된 응용 프로그램인 [XBAP](https://ko.wikipedia.org/wiki/XBAP "wikilink")를 사용하여 WPF를 설치하는 경우 [웹 페이지로](../Page/웹_페이지.md "wikilink") 통합할 수 있다. 다른 방법으로는 [실버라이트 플러그인을](https://ko.wikipedia.org/wiki/마이크로소프트_실버라이트 "wikilink") 사용하는 것이다. 닷넷 3.0 이후가 설치되어 있다면 느슨한(loose) XAML 파일도 실버라이트 플러그인 없이 닷넷 프레임워크 3.0과 결합하여 호환 [웹 브라우저](../Page/웹_브라우저.md "wikilink")([인터넷 익스플로러와](../Page/인터넷_익스플로러.md "wikilink") [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 포함) 직접 확인이 가능하다.\[5\] 코드는 [HTML](../Page/HTML.md "wikilink") 페이지에 직접 추가할 수 없다. 대신 [자바스크립트](../Page/자바스크립트.md "wikilink")를 통해 페이지로 로드되어야 한다. 느슨한 XAML 파일들은 렌더링할 시각적인 내용을 정의하는 것으로 제한되는 마크업 전용 파일이다. 이들은 응용 프로그램과 컴파일되지 않는다.

``` xml
<html ns="http://www.w3.org/1999/xhtml">
  <head>
    <title>XAML Example</title>
    <script type="text/javascript" src="MySilverlight.js" />
    <script type="text/javascript" src="Silver.js" />
  </head>
  <body>
    <div id="MySilverlight" >
    </div>
    <script type="text/javascript">
      createMySilverlight();
    </script>
  </body>
</html>
```

*MySilverlight.js* 파일은 *MySilverlight* 요소 밑에 상기의 XAML 코드(XML 파일로)를 로드하는 코드를 포함해야 한다.

## 같이 보기

  - [레이아웃 매니저](https://ko.wikipedia.org/wiki/레이아웃_매니저 "wikilink")
  - [ZUML](https://ko.wikipedia.org/wiki/ZK_프레임워크 "wikilink")
  - [NextStep/Cocoa 인터페이스 빌더](../Page/인터페이스_빌더.md "wikilink")

## 각주

## 외부 링크

  - [마이크로소프트 XAML 개요](https://web.archive.org/web/20060717193028/http://windowssdk.msdn.microsoft.com/en-us/library/ms752059.aspx)

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:선언형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:선언형_프로그래밍_언어 "wikilink") [분류:닷넷 프레임워크](https://ko.wikipedia.org/wiki/분류:닷넷_프레임워크 "wikilink") [분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink")

1.
2.
3.  [XAML Syntax Terminology](http://msdn2.microsoft.com/en-us/library/ms788723.aspx)
4.  Microsoft XAML Overview page at [XAML Overview (Root element and xmlns)](https://msdn.microsoft.com/en-us/library/ms752059.aspx#xaml_files)
5.  [Windows Presentation Foundation on the Web: Web Browser Applications - MSDN](https://msdn.microsoft.com/en-us/library/aa480223.aspx#wpfandwbas_topic6)