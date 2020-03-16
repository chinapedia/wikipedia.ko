> This article is converted from Wikipedia: [WxPython](https://ko.wikipedia.org/wiki/WxPython).


**wxPython**은 [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") [GUI](../Page/그래픽_사용자_인터페이스.md "wikilink") [API](../Page/API.md "wikilink")(흔히 [툴킷](https://ko.wikipedia.org/wiki/툴킷 "wikilink")으로 부름)인 [wxWidgets](https://ko.wikipedia.org/wiki/wxWidgets "wikilink")([C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 작성)를 [파이썬 프로그래밍 언어](../Page/파이썬.md "wikilink") 환경에서 이용하기 위한 래퍼(wrapper)이다. 파이썬과 묶여 있는 [트킨터](https://ko.wikipedia.org/wiki/트킨터 "wikilink")를 대체하는 것들 가운데 하나이기도 하다. 파이썬 [확장 모듈](https://ko.wikipedia.org/wiki/확장_모듈 "wikilink") ([네이티브 코드](https://ko.wikipedia.org/wiki/네이티브_코드 "wikilink"))로 추가되었다. 이 밖의 다른 대체물로는 [PyGTK](https://ko.wikipedia.org/wiki/PyGTK "wikilink"), [PyQt](https://ko.wikipedia.org/wiki/PyQt "wikilink")가 있다. wxWidgets과 같이 wxPython은 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink").

## 라이선스

래퍼로서 wxPython은 [wxWidgets](https://ko.wikipedia.org/wiki/wxWidgets "wikilink")에 쓰이는 동일한 [자유 소프트웨어 라이선스를](https://ko.wikipedia.org/wiki/자유_소프트웨어_라이선스 "wikilink") 이용한다.\[1\] 이 라이선스는 [자유 소프트웨어 재단과](../Page/자유_소프트웨어_재단.md "wikilink") [오픈 소스 이니셔티브에](https://ko.wikipedia.org/wiki/오픈_소스_이니셔티브 "wikilink") 승인되어 있다.

## 예

[Hello world](https://ko.wikipedia.org/wiki/Hello_world "wikilink") 모듈의 간단한 예로, wxPython에 두 개의 주요 오브젝트(주가 되는 창 객체와 응용 프로그램 객체)를 만드는 것을 기술하고 있다. `MainLoop()`를 호출하여 프로그램의 사용자 상호 작용 부분을 관리하는 이벤트 시스템에 제어권을 넘긴다.

``` python
#!/usr/bin/env python

import wx

class TestFrame(wx.Frame):
    def __init__(self, parent, title):
        wx.Frame.__init__(self, parent, title=title)
        text = wx.StaticText(self, label="Hello, World!")

app = wx.App(redirect=False)
frame = TestFrame(None, "Hello, world!")
frame.Show()
app.MainLoop()
```

## wxPython으로 개발된 응용 프로그램

  - [비트토렌트](https://ko.wikipedia.org/wiki/비트토렌트 "wikilink")
  - [챈들러](https://ko.wikipedia.org/wiki/챈들러_\(소프트웨어\) "wikilink")
  - [드롭박스](../Page/드롭박스.md "wikilink")
  - [Phatch](https://ko.wikipedia.org/wiki/Phatch "wikilink")
  - [TaskCoach](http://www.taskcoach.org/)
  - [Editra](http://editra.org/)
  - [Ulipad](http://code.google.com/p/ulipad/)
  - [Whyteboard](http://code.google.com/p/whyteboard)
  - [Wrye Bash](http://wryebash.netai.net/)

## 같이 보기

  - [wxGlade](https://ko.wikipedia.org/wiki/wxGlade "wikilink"): 파이썬 코드를 만드는 wxWidgets용 GUI 디자이너

## 각주

<references />

  -
## 외부 링크

  - [wxPython 공식 웹사이트](http://wxpython.org/)
  - [wxWidgets 공식 웹사이트](http://wxwidgets.org/)

[분류:파이썬 라이브러리](https://ko.wikipedia.org/wiki/분류:파이썬_라이브러리 "wikilink") [분류:위젯](https://ko.wikipedia.org/wiki/분류:위젯 "wikilink") [분류:프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:프로그래밍_도구 "wikilink") [분류:1998년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1998년_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.