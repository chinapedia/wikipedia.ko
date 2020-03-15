> This article is converted from Wikipedia: [GYP \(\)](https://ko.wikipedia.org/wiki/GYP_\(\)).


**GYP**(Generate Your Projects)는 빌드 자동화 도구이며 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")으로 작성된 메타 빌드 시스템이다. GYP는 Google이 Chromium 웹 브라우저를 빌드 할 때 [OS](https://ko.wikipedia.org/wiki/OS "wikilink")에 의존하는 [IDE](https://ko.wikipedia.org/wiki/IDE "wikilink")들의 프로젝트 파일 (예 : [Visual Studio Code](https://ko.wikipedia.org/wiki/Visual_Studio_Code "wikilink") 및 [Xcode](https://ko.wikipedia.org/wiki/Xcode "wikilink") )을 생성하기 위해 만들어 졌으며 [BSD 소프트웨어 라이센스를](https://ko.wikipedia.org/wiki/BSD_허가서 "wikilink") 사용하여 [오픈 소스 소프트웨어로](https://ko.wikipedia.org/wiki/오픈_소스_소프트웨어 "wikilink") 라이센스가 부여되었다.

GYP의 기능은 [CMake](https://ko.wikipedia.org/wiki/CMake "wikilink") 빌드 도구와 비슷하다. GYP는 하나 이상의 대상 프로젝트 파일을 작성 및 생성하기 위해 [JSON](https://ko.wikipedia.org/wiki/JSON "wikilink") 사전\[1\] 을 포함하는 파일을 처리한다. 단일 소스 .GYP 파일은 일반 파일 또는 대상 파일이며 대상 파일은 각 대상 빌드 도구에만 적용된다.

GYP를 사용하여 구축되는 소프트웨어 프로젝트에는 [V8](https://ko.wikipedia.org/wiki/V8 "wikilink") Javascript 엔진, Google의 [Chromium](https://ko.wikipedia.org/wiki/Chromium "wikilink") 웹 브라우저, [다트](https://ko.wikipedia.org/wiki/다트_\(프로그래밍_언어\) "wikilink") , [Node.js](https://ko.wikipedia.org/wiki/Node.js "wikilink")\[2\], [WebRTC](../Page/WebRTC.md "wikilink")\[3\] , [Telegram](https://ko.wikipedia.org/wiki/Telegram "wikilink")\[4\] 및 [Electron이](../Page/일렉트론_\(소프트웨어_프레임워크\).md "wikilink") 있다.\[5\]

2016 년에 Chromium 프로젝트는 GYP를 GN으로 대체했다.

GYP는 대부분의 주요 [OS](https://ko.wikipedia.org/wiki/OS "wikilink")를 지원하는 [닌자](../Page/닌자_\(빌드_시스템\).md "wikilink") 파일이나 빌드 프로젝트 파일을 생성 할 수 있다.\[6\]

## 함께보기

  - [GN](../Page/GN_\(빌드_시스템\).md "wikilink")

## 참고

  - [GYP](https://gyp.gsrc.io/index.md)
  - [GYP, GYPvs. CMake](https://gyp.gsrc.io/docs/GypVsCMake.md)
  - [웹사이트](http://gyp.gsrc.io)

## 각주

[분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink") [분류:구글의 서비스](https://ko.wikipedia.org/wiki/분류:구글의_서비스 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")

1.  [Gyp Make file dictionary](https://gyp.gsrc.io/docs/UserDocumentation.md), GYP user documentation
2.  [Announcing Node 0.8](http://blog.nodejs.org/2012/06/25/node-v0-8-0/), the Node.js official blog, 25 Jun 2012
3.  [Development](http://www.webrtc.org/native-code/development)  WebRTC
4.
5.  [GitHub](https://github.com/atom/electron) Electron
6.  [닌자](https://ninja-build.org/manual.html#_using_ninja_for_your_project)