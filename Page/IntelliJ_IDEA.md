> This article is converted from Wikipedia: [IntelliJ IDEA](https://ko.wikipedia.org/wiki/IntelliJ_IDEA).


**IntelliJ IDEA**는 [JetBrains](https://ko.wikipedia.org/wiki/JetBrains "wikilink")사에서 제작한 상용 [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") [통합 개발 환경이다](https://ko.wikipedia.org/wiki/통합_개발_환경 "wikilink"). 줄여서 **IntelliJ** 혹은 **IDEA**로도 불린다.

[이클립스 재단](../Page/이클립스_재단.md "wikilink") 의 [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")와 [썬 마이크로시스템즈의](../Page/썬_마이크로시스템즈.md "wikilink") [넷빈즈](../Page/넷빈즈.md "wikilink")로 대표되는 무료 자바 통합개발환경에서 [볼랜드](../Page/볼랜드.md "wikilink")(/[코드기어](../Page/코드기어.md "wikilink"))의 [제이빌더](https://ko.wikipedia.org/wiki/제이빌더 "wikilink")()와 함께 얼마 안 되는 상용 개발 도구 가운데 하나이다.

## 시스템 요구사항

시스템 요구사항은 다음과 같다.\[1\]

|            | 윈도우                                     | OS X                                | 리눅스               |
| ---------- | --------------------------------------- | ----------------------------------- | ----------------- |
| **OS 버전**  | 윈도우 10/8/7 x64                          | OS X 10.5 이상, 최대 10.11 (El Capitan) | GNOME 또는 KDE 데스크톱 |
| **RAM**    | 1 GB 최소, 4 GB 이상 권장 (안드로이드 개발 및 상업용 생산) |                                     |                   |
| **디스크 공간** | 300 MB 하드 디스크 공간 + 최소 1 GB (캐시용)        |                                     |                   |
| **JDK 버전** | JDK 1.8 (2016.1 이후)\[2\]                |                                     |                   |
| **화면 해상도** | 1024×768 최소 화면 해상도                      |                                     |                   |

## 지원 언어

커뮤니티 에디션과 얼티밋 에디션은 아래의 표에 보이듯이 다양한 프로그래밍 언어를 지원 시 차이가 있다.\[3\]

| 언어                                                                                                                                                                | IntelliJ IDEA 커뮤니티 에디션                | IntelliJ IDEA 얼티밋 에디션       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | --------------------------- |
| [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink")                                                                                                    | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [클로저](https://ko.wikipedia.org/wiki/클로저 "wikilink") (별도 플러그인을 통해)                                                                                                 | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [다트](https://ko.wikipedia.org/wiki/다트_\(프로그래밍_언어\) "wikilink") (별도 플러그인을 통해)                                                                                      | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [얼랑](https://ko.wikipedia.org/wiki/얼랑 "wikilink") (별도 플러그인을 통해)                                                                                                   | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [Go](../Page/Go_\(프로그래밍_언어\).md "wikilink") (별도 플러그인을 통해)                                                                                                         | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [그루비](https://ko.wikipedia.org/wiki/그루비 "wikilink")                                                                                                               | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [Haxe](https://ko.wikipedia.org/wiki/Haxe "wikilink") (별도 플러그인을 통해)                                                                                               | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [펄](https://ko.wikipedia.org/wiki/펄 "wikilink") ([별도 플러그인](https://plugins.jetbrains.com/plugin/7796)을 통해)                                                        | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [스칼라](https://ko.wikipedia.org/wiki/스칼라_\(프로그래밍_언어\) "wikilink") (별도 플러그인을 통해)                                                                                    | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [XML](https://ko.wikipedia.org/wiki/XML "wikilink")/[XSL](https://ko.wikipedia.org/wiki/XSL "wikilink")                                                           | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [코틀린](https://ko.wikipedia.org/wiki/코틀린 "wikilink")                                                                                                               | style="background: \#9F9 |예           | style="background: \#9F9 |예 |
| [액션스크립트](https://ko.wikipedia.org/wiki/액션스크립트 "wikilink")/[MXML](../Page/MXML.md "wikilink")                                                                      | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |
| [커피스크립트](../Page/커피스크립트.md "wikilink")                                                                                                                            | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |
| [하스켈](https://ko.wikipedia.org/wiki/하스켈 "wikilink") (별도 플러그인을 통해)                                                                                                 | style="background: \#9F9 |예\[4\]      | style="background: \#9F9 |예 |
| [HTML](https://ko.wikipedia.org/wiki/HTML "wikilink")/[XHTML](https://ko.wikipedia.org/wiki/XHTML "wikilink")/[CSS](https://ko.wikipedia.org/wiki/CSS "wikilink") | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |
| [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink")                                                                                                         | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |
| [루아](https://ko.wikipedia.org/wiki/루아 "wikilink") (별도 플러그인을 통해)                                                                                                   | style="background: \#9F9 |예\[5\]      | style="background: \#9F9 |예 |
| [PHP](https://ko.wikipedia.org/wiki/PHP "wikilink") (별도 플러그인을 통해)                                                                                                 | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |
| [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") (별도 플러그인을 통해)                                                                                                 | style="background: \#9F9 |예\[6\]\[7\] | style="background: \#9F9 |예 |
| [루비](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink")/[JRuby](https://ko.wikipedia.org/wiki/JRuby "wikilink")                                            | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |
| [SQL](../Page/SQL.md "wikilink")                                                                                                                                  | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |
| [타입스크립트](../Page/타입스크립트.md "wikilink") (별도 플러그인을 통해)                                                                                                              | style="background: \#F99 |아니오         | style="background: \#9F9 |예 |

## 상용 및 무료 버전

IntelliJ IDEA는 **Ultimate Edition**으로 불리는 상용버전과 **Community Edition**으로 불리는 무료 버전이 존재하며 상용버전은 30일간 무료로 사용해 보고 계속 사용할지 여부를 결정할 수 있다.

무료 버전은 [아파치 라이선스](../Page/아파치_라이선스.md "wikilink") 2.0으로 제공되고 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink")()이며 상용버전에 비하여 일부 기능이 제약된다.\[8\]

## 같이 보기

  - [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")
  - [넷빈즈](../Page/넷빈즈.md "wikilink")
  - [제이빌더](https://ko.wikipedia.org/wiki/제이빌더 "wikilink")
  - [통합 개발 환경](https://ko.wikipedia.org/wiki/통합_개발_환경 "wikilink")

## 참고 자료

## 외부 링크

  - [IntelliJ IDEA 홈페이지](http://www.jetbrains.com/idea)

  - [IntelliJ IDEA Community 버전 홈페이지](http://www.jetbrains.org/display/IJOS)

[분류:통합 개발 환경](https://ko.wikipedia.org/wiki/분류:통합_개발_환경 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink") [분류:자유 통합 개발 환경](https://ko.wikipedia.org/wiki/분류:자유_통합_개발_환경 "wikilink")

1.
2.  [IntelliJ IDEA 2016.1 is Here](https://blog.jetbrains.com/idea/2016/03/intellij-idea-2016-1-is-here/)
3.
4.  [Haskell language support](https://plugins.jetbrains.com/plugin/7453?pr=idea_ce)
5.  [Lua For IDEA](https://bitbucket.org/sylvanaar2/lua-for-idea/wiki/Home)
6.  [Python Community Edition](https://plugins.jetbrains.com/plugin/7322?pr=)
7.  [JetBrains Delights the Python Community with a Free Edition of its Famous IDE, PyCharm 3.0](https://blog.jetbrains.com/pycharm/2013/09/jetbrains-delights-the-python-community-with-a-free-edition-of-its-famous-ide-pycharm-3-0/)
8.  [상용버전 및 무료버전의 기능 차이](http://www.jetbrains.com/idea/features/editions_comparison_matrix.html)