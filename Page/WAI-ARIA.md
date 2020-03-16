> This article is converted from Wikipedia: [WAI-ARIA](https://ko.wikipedia.org/wiki/WAI-ARIA).


**WAI-ARIA**(Web Accessibility Initiative – Accessible Rich Internet Applications)는 웹 페이지, 특히 [동적 콘텐츠](https://ko.wikipedia.org/wiki/동적_콘텐츠 "wikilink"), 그리고 [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink"), [HTML](../Page/HTML.md "wikilink"), [자바스크립트](../Page/자바스크립트.md "wikilink") 및 관련 기술로 개발된 사용자 인터페이스 구성 요소의 [접근성](../Page/접근성.md "wikilink")을 증가시키는 방법에 대해 규정한 [W3C](../Page/W3C.md "wikilink")가 출판한 기술 사양이다.\[1\]

## 역사

2008년 9월 15일 작업 초안으로 SVG 1.2 Tiny가 WA-ARIA 지원을 추가했다.\[2\] 2014년 3월 20일, WAI-ARIA 1.0은 완전한 W3C 권고안이 되었다.\[3\]

## 범위

웹 개발자들은 점차 [클라이언트 사이드](../Page/클라이언트_사이드.md "wikilink") 스크립트를 사용하여, HTML만으로 만들 수 없는 사용자 인터페이스 컨트롤을 만든다. 클라이언트 사이드 스크립트를 사용하여 [웹 서버로부터](../Page/웹_서버.md "wikilink") 새 페이지를 완전히 요청하지 않고도 페이지의 일부를 업데이트할 수도 있다. 웹사이트 상의 이러한 기술들은 [리치 인터넷 애플리케이션이라고](../Page/리치_인터넷_애플리케이션.md "wikilink") 부른다. 이 사용자 인터페이스 컨트롤과 콘텐츠 업데이트들은 [장애가](../Page/장애인.md "wikilink") 있는 사용자들, 특히 [스크린 리더](https://ko.wikipedia.org/wiki/스크린_리더 "wikilink") 사용자, 또 [마우스](../Page/마우스.md "wikilink")나 기타 [포인팅 장치를](https://ko.wikipedia.org/wiki/포인팅_장치 "wikilink") 사용할 수 없는 사용자에게는 접근이 되지 않을 수도 있다. WAI-ARIA는 역할, 속성, 상태 정보를 동적 웹 애플리케이션에 추가함으로써 [웹 페이지](../Page/웹_페이지.md "wikilink")(페이지의 일부)가 스스로를 [정적 문서보다는](../Page/정적_웹_페이지.md "wikilink") [애플리케이션으로](../Page/응용_소프트웨어.md "wikilink") 선언할 수 있게 한다. ARIA는 [웹 애플리케이션](../Page/웹_애플리케이션.md "wikilink"), [웹 브라우저](../Page/웹_브라우저.md "wikilink"), [보조 기술](../Page/보조과학기술.md "wikilink"), 접근성 평가 도구의 개발자들이 사용하도록 고안되었다.\[4\]

WAI-ARIA는 사용자 인터페이스 컨트롤과 동적인 콘텐츠를 더 잘 접근할 수 있도록 만들기 위해 시맨틱과 기타 [메타데이터](../Page/메타데이터.md "wikilink")를 HTML 콘텐츠에 추가하는 방식을 기술한다. 이를테면 WAI-ARIA를 통해 내비게이션 [메뉴로서](https://ko.wikipedia.org/wiki/메뉴_\(컴퓨팅\) "wikilink") [링크](../Page/하이퍼링크.md "wikilink") 목록을 식별할 수 있으며, 펼치기/접기 여부의 상태를 지시할 수 있다. 원래 HTML의 접근성 문제를 해결하기 위해 개발되었으나 WAI-ARIA는 HTML에만 국한되어 사용되지 않는다. SVG 등 다른 [마크업 언어에도](../Page/마크업_언어.md "wikilink") 사용할 수 있다.\[5\]

## 같이 보기

  - [접근성](../Page/접근성.md "wikilink")
  - [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink")
  - [리치 인터넷 애플리케이션](../Page/리치_인터넷_애플리케이션.md "wikilink")
  - [유니버설 디자인](../Page/유니버설_디자인.md "wikilink")

## 각주

## 외부 링크

  - [Introduction to WAI ARIA by Gez Lemon](http://dev.opera.com/articles/view/introduction-to-wai-aria/)
  - [ARIA developer portal](https://developer.mozilla.org/en/aria) documentation, videos, and articles relating to ARIA (materials under Creative Commons Attribution-Share Alike license)
  - [Henny Swan (Opera): Setting up a screen reader test environment for WAI-ARIA](https://web.archive.org/web/20171028073530/http://www.iheni.com/screen-reader-testing/)

[분류:Ajax](https://ko.wikipedia.org/wiki/분류:Ajax "wikilink") [분류:웹 2.0](https://ko.wikipedia.org/wiki/분류:웹_2.0 "wikilink")

1.
2.  See [SVG 1.2 Tiny: role attribute](http://www.w3.org/TR/2008/WD-SVGMobile12-20080915/struct.html#RoleAttribute) and [SVG 1.2 Tiny: Extensible metadata attributes](http://www.w3.org/TR/2008/WD-SVGMobile12-20080915/metadata.html#MetadataAttributes).
3.
4.
5.