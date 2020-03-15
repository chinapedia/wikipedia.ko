> This article is converted from Wikipedia: [Direct2D](https://ko.wikipedia.org/wiki/Direct2D).


**Direct2D**는 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사가 차기 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [운영 체제를](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 위해 고안한 새로운 [2차원](https://ko.wikipedia.org/wiki/2차원_컴퓨터_그래픽스 "wikilink") 그래픽 [API](../Page/API.md "wikilink")이며 [DirectX](https://ko.wikipedia.org/wiki/DirectX "wikilink") 11의 한 부분이다. 현재 [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") SP2 이상, [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") 이상 운영 체제에서 지원되며, DirectX 10.1 이상을 지원하는 그래픽 하드웨어에서 완벽 지원한다.\[1\]

Direct2D는 [GDI](../Page/그래픽_장치_인터페이스.md "wikilink"), [GDI+를](../Page/그래픽_장치_인터페이스.md "wikilink") 대체하여 작동한다. GDI계열 API에서 CPU에 의존하던 처리를 GPU에 분산하여 빠르게 동작하면서도 높은 화질의 2차원 그래픽을 제공하도록 설계되어 있다.\[2\] 다만 Direct2D는 COM 런타임을 사용하지 않는다.\[3\]

Direct2D는 GDI, GDI+, Direct3D과의 상호 운용성을 가지며 [DirectWrite](https://ko.wikipedia.org/wiki/DirectWrite "wikilink"), [윈도 이미징 컴퍼넌트와](https://ko.wikipedia.org/wiki/윈도_이미징_컴퍼넌트 "wikilink") 같은 다른 순수 윈도 기술과 함께 동작한다.

## 요구 사항

다이렉트엑스 10.1 표준의 요구 사항에 따라 [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") SP2 이상 또는 [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") 이상의 운영 체제가 필요하다. (서버 기반 운영체제 포함) 하드웨어적으로는 다이렉트 엑스 9 이상을 지원하는 [GPU가](https://ko.wikipedia.org/wiki/그래픽_처리_장치 "wikilink") 필요하다.

## 응용 프로그램

  - [게코](../Page/게코_\(레이아웃_엔진\).md "wikilink") 1.9.3 alpha 3\[4\]\[5\]
  - [인터넷 익스플로러 9](https://ko.wikipedia.org/wiki/인터넷_익스플로러_9 "wikilink")

## 같이 보기

  - [DirectDraw](https://ko.wikipedia.org/wiki/DirectDraw "wikilink")
  - [Direct3D](../Page/Direct3D.md "wikilink")
  - [DirectWrite](https://ko.wikipedia.org/wiki/DirectWrite "wikilink")
  - [클리어타입](https://ko.wikipedia.org/wiki/클리어타입 "wikilink")
  - [오픈타입](../Page/오픈타입.md "wikilink")

## 참조

<references />

## 외부 링크

  - [Direct2D 개발자 토머스 올슨의 블로그](https://web.archive.org/web/20090216192618/http://blogs.technet.com/thomasolsen/default.aspx)
  - [Direct2D 백서](http://code.msdn.microsoft.com/PDC08WhitePapers)
  - [윈도 7: Direct2D 및 DirectWrite 소개](http://channel9.msdn.com/pdc2008/PC18/) - PDC 2008 영상

[2D](https://ko.wikipedia.org/wiki/분류:DirectX "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink")

1.  \[<http://msdn.microsoft.com/en-us/library/dd370990(VS.85>).aspx Direct2D (Windows) \]
2.  \[<http://msdn.microsoft.com/en-us/library/dd370990(VS.85>).aspx Direct2D (Windows) \]
3.
4.  [Release Notes: Mozilla Developer Preview](http://www.mozilla.org/projects/devpreview/releasenotes/)
5.  2010년 4월 현재, 파이어폭스 3.7 nightly 빌드에서 사용 가능하지만 기본값은 '사용안함'이다. 사용하기 위해서는 [여기](http://www.basschouten.com/blog1.php/2010/03/02/presenting-direct2d-hardware-acceleratio)를 참조하라.