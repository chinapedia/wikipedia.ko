> This article is converted from Wikipedia: [ RSS ](https://ko.wikipedia.org/wiki/_RSS_).


**윈도우 RSS 플랫폼**()은 [인터넷 익스플로러 7](../Page/인터넷_익스플로러_7.md "wikilink") 및 [윈도우 비스타에](../Page/윈도우_비스타.md "wikilink") 내장된 플랫폼으로서, 윈도우 응용 프로그램에게 피드(feed) 처리 및 관리 기능을 제공해주는 플랫폼이다. [인터넷 익스플로러 7의](../Page/인터넷_익스플로러_7.md "wikilink") [RSS](https://ko.wikipedia.org/wiki/RSS "wikilink") 지원 기능이 이 플랫폼에 기반한다.

## 개요

윈도우 RSS 플랫폼은 다음 세 가지의 콤포넌트로 구성된다:

  - **공통 RSS 데이터 스토어**(**Common RSS Data Store**) - RSS 플랫폼이 관리하는 모든 피드에 대한 데이터 스토어(The data store). RSS 플랫폼 API는 피드를 가공하여 – 스크립트를 제거하고, 임베디드(embedded) 오브젝트를 제거하고, 잠재적으로 보안을 위협하는 것들을 제거 한 후 – 피드를 제공한다. 포맷 안 된 XML로의 접근도 허용된다.

<!-- end list -->

  - **공통 RSS 싱크 엔진**(**Common RSS sync engine**) - 주기적으로 콘텐트를 다운로드해야 할 책임을 갖고 있는 다운로드 엔진이다. 기본적으로, 피드에 붙은 오브젝트인 피드 인클로저는 다운로드하지 않는다. 하지만 이 기능의 동작 여부는 사용자가 설정 가능하다.

<!-- end list -->

  - **공통 RSS 피드 목록**(**Common RSS Feed List**) - RSS 플랫폼 API가 노출해주는 가입한 피드들의 목록. [인터넷 익스플로러 7이나](../Page/인터넷_익스플로러_7.md "wikilink") [마이크로소프트 아웃룩](https://ko.wikipedia.org/wiki/마이크로소프트_아웃룩 "wikilink") 같은 모든 RSS 클라이언트들은 이 목록을 공유한다. 목록의 변경이 있었다면, 모든 RSS 리더들 사이에 그 변경이 공유되고 반영된다.

## 같이 보기

  - [인터넷 익스플로러](https://ko.wikipedia.org/wiki/인터넷_익스플로러 "wikilink") [7](../Page/인터넷_익스플로러_7.md "wikilink")
  - [마이크로소프트 아웃룩](https://ko.wikipedia.org/wiki/마이크로소프트_아웃룩 "wikilink") [2007](https://ko.wikipedia.org/wiki/마이크로소프트_오피스_2007#마이크로소프트_오피스_아웃룩 "wikilink")

## 외부 링크

  - [Microsoft Team RSS blog](http://blogs.msdn.com/rssteam/archive/2006/02/02/522642.aspx)

  - [윈도우 RSS 플랫폼](http://www.niallkennedy.com/blog/archives/2006/03/windows-rss-platform.html)

  - [롱혼(Longhorn)에서의 RSS 지원](http://msdn2.microsoft.com/en-us/library/aa480204.aspx)

[분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink") [분류:인터넷 익스플로러](https://ko.wikipedia.org/wiki/분류:인터넷_익스플로러 "wikilink") [분류:RSS](https://ko.wikipedia.org/wiki/분류:RSS "wikilink")