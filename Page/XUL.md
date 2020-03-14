> This article is converted from Wikipedia: [XUL](https://ko.wikipedia.org/wiki/XUL).


**XUL**(XML User Interface Language, '줄'로 발음)은 [모질라](https://ko.wikipedia.org/wiki/모질라 "wikilink")가 개발한 사용자 인터페이스 마크업 언어이다. XUL은 [XML](https://ko.wikipedia.org/wiki/XML "wikilink") 파생 언어로 구현되어 있으며 [그래픽 사용자 인터페이스를](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 제공함으로써 [웹 페이지와](https://ko.wikipedia.org/wiki/웹_페이지 "wikilink") 비슷한 방식으로 작성할 수 있다.

XUL은 [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink")와 같은 크로스 플랫폼 응용 프로그램들을 작성하는데 사용할 수 있으며, 여기서 [게코로](https://ko.wikipedia.org/wiki/게코_\(레이아웃_엔진\) "wikilink") 알려진 [레이아웃 엔진이](https://ko.wikipedia.org/wiki/레이아웃_엔진 "wikilink") 이를 해석하여 파이어폭스 사용자 인터페이스와 웹 페이지 화면을 렌더링한다.\[1\]

## 예

아래의 예는 수직 상자 컨테이너 안에 위치한 3개의 버튼을 보여 준다.:\[2\] [right](https://ko.wikipedia.org/wiki/파일:Boxes-ex1.png "wikilink")

``` xml
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
ns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <vbox>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </vbox>
</window>
```

## 같이 보기

  - [XBL](https://ko.wikipedia.org/wiki/XBL "wikilink")
  - [ZK 프레임워크](https://ko.wikipedia.org/wiki/ZK_프레임워크 "wikilink")

## 참조

<references />

## 외부 링크

  - [XUL documentation](https://web.archive.org/web/20081113171050/https://developer.mozilla.org/en/XUL) - developer.mozilla.org

  - [XUL Periodic Table](http://www.hevanet.com/acorbin/xul/top.xul) — Visual demonstration of XUL capabilities (requires a [Gecko](https://ko.wikipedia.org/wiki/게코_\(레이아웃_엔진\) "wikilink")-based (XUL-enabled) browser such as [Mozilla Firefox](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink"))

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:모질라](https://ko.wikipedia.org/wiki/분류:모질라 "wikilink")

1.
2.  <https://developer.mozilla.org/en/XUL_Tutorial/The_Box_Model>