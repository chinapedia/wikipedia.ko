> This article is converted from Wikipedia: [RSS](https://ko.wikipedia.org/wiki/RSS).


**RSS**()는 뉴스나 [블로그](../Page/블로그.md "wikilink") 사이트에서 주로 사용하는 콘텐츠 표현 방식이다. 웹 사이트 관리자는 RSS 형식으로 웹 사이트 내용을 보여 준다. 이 정보를 받는 사람은 다른 형식으로 이용할 수 있다.RSS 리더에는 웹기반형과 설치형이 있다. 웹기반형 리더는 간단한 계정등록으로 어디에서든 이용할 수 있다는 장점을 가지고 있다.

RSS가 등장하기 전에는 원하는 정보를 얻기 위해 해당 사이트를 직접 방문하여야 했으나, RSS 관련 프로그램(혹은 서비스)을 이용하여 자동 수집이 가능해졌기 때문에 사용자는 각각의 사이트 방문 없이 최신 정보들만 골라 한 자리에서 볼 수 있다.

또한 RSS는 [팟캐스팅](https://ko.wikipedia.org/wiki/팟캐스팅 "wikilink")과 같은 미디어 배포의 용도로도 사용된다. RSS 2.0 의 〈enclosure〉태그 내에 [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink") 나 [MOV](../Page/퀵타임.md "wikilink") 등의 미디어 파일을 첨부하여 배포하면, 팟캐스팅 클라이언트를 이용해 파일을 내려 받아 감상할 수 있다.

RSS 2.0은 공식적으로 완료된 것으로 선언되었으며, [하버드 대학교가](https://ko.wikipedia.org/wiki/하버드_대학교 "wikilink") 저작권을 보유하고 있다.

## 여러 표준

RSS는 [XML](https://ko.wikipedia.org/wiki/XML "wikilink") 기반의 표준이며, 여러 표준들이 존재한다. 표준들은 크게 [RDF](https://ko.wikipedia.org/wiki/RDF "wikilink") (또는 RSS 1.\*)과 RSS 2.\* 로 나뉜다.

  - RDF (RSS 1.\*)
      - RSS 0.90
      - RSS 1.0
      - RSS 1.1
  - RSS 2.0
      - RSS 0.91
      - RSS 0.92
      - RSS 2.01

## Rss 2.0에서의 활용 예

``` xml
<?xml version="1.0" encoding="UTF-8"?>
 <rss version="2.0">
  <channel>
    <title>제목</title>
    <link>주소/</link>
    <description>설명 (짤막하게)</description>

    <item>
      <title>제목</title>
      <link>주소/글 주소</link>

      <description>글 내용 전체(또는 일부)</description>
      <pubDate>시간</pubDate>
      <guid>주소/글 주소</guid>
    </item>

    <item>
      <title>제목</title>
      <link>주소/글 주소</link>
      <description>글 내용</description>
      <pubDate>시간과 날짜</pubDate>
      <guid>주소/글 주소</guid>
    </item>
  </channel>
</rss>
```

## 아톰과의 비교

RSS와 [아톰](https://ko.wikipedia.org/wiki/Atom "wikilink") 모두 모든 주요 피드리더들에게 널리 지원된다. 아톰보다 더 일찍 피드리더 기능이 도입되면서 RSS가 널리 이용되어 인기를 끌게 되었다. 그러나 아톰은 라이선스가 덜 제한적이고 [IANA](https://ko.wikipedia.org/wiki/IANA "wikilink") 등록 [MIME 타입](https://ko.wikipedia.org/wiki/인터넷_미디어_타입 "wikilink"), [XML 이름공간](https://ko.wikipedia.org/wiki/XML_이름공간 "wikilink"), 상대 [URI](https://ko.wikipedia.org/wiki/통합_자원_식별자 "wikilink") 지원, [RELAX NG](https://ko.wikipedia.org/wiki/RELAX_NG "wikilink") 지원과 같이 RSS에 비해 몇 가지 이점이 있다.\[1\] 기술적으로 아톰은 이 둘 사이에서 더 진보화된 신디케이션으로 간주된다.\[2\]

아래의 표는 아톰과 동일한 RSS 요소를 요약해 놓은 것이다.

| RSS 2.0                                                   | 아톰 1.0                      |
| --------------------------------------------------------- | --------------------------- |
| `author`                                                  | `author`                    |
| `category`                                                | `category`                  |
| `channel`                                                 | `feed`                      |
| `copyright`                                               | `rights`                    |
| `description`                                             | `subtitle`                  |
| `description`                                             | `summary` 또는 `content`      |
| `generator`                                               | `generator`                 |
| `guid`                                                    | `id`                        |
| `image`                                                   | `logo`                      |
| `item`                                                    | `entry`                     |
| `lastBuildDate` (`channel`에서)                             | `updated`                   |
| `link`                                                    | `link`                      |
| `managingEditor`                                          | `author` 또는 `contributor`   |
| `pubDate`                                                 | `published` (`entry`의 하부요소) |
| `title`                                                   | `title`                     |
| [`ttl`](https://ko.wikipedia.org/wiki/타임_투_리브 "wikilink") | `-`                         |

## 각주

<references />

## 외부 링크

  - 규격
      - [RSS 0.91 규격, 3판](http://my.netscape.com/publish/formats/rss-spec-0.91.html)

      - [RSS 1.0 규격](https://web.archive.org/web/20081022105748/http://web.resource.org/rss/1.0/)

      - [RSS 1.1 규격](http://inamidst.com/rss1.1/)

      - [RSS 2.0 규격](http://www.rssboard.org/rss-specification) [모듈](http://blogs.law.harvard.edu/tech/directory/5/specifications/rss20ModulesNamespaces)

      - [(제안) RSS를 위한 Simple Sharing Extensions](https://web.archive.org/web/20061112100137/http://msdn.microsoft.com/xml/rss/sse/) ([마이크로소프트](../Page/마이크로소프트.md "wikilink"))

      - [rss-extensions.org 마이크로소프트, 애플 등 기업들이 제출한 RSS 확장 제안 목록](http://rss-extensions.org)

      - [RSS 2.0 규격 번역문](http://naearu.tistory.com/2982748)
  - 유효성 검사기
      - [W3C Feed Validation Service, for Atom and RSS](http://validator.w3.org/feed/)

      - [Feed Validator for Atom and RSS](https://web.archive.org/web/20080227162320/http://www.feedvalidator.org/)
  - 디렉토리
      - [Blauer Bote Korea Newsfeeds](http://blauerbote.com/index.php?k=Newsfeeds&s=kr&c=1)
  - Article
      - [RSS 2.0 피드(Feed) 작성 방법, 문법 기초](http://mwultong.blogspot.com/2007/02/rss-20-feed-utf-8.html)

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [RSS](https://ko.wikipedia.org/wiki/분류:RSS "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.
2.