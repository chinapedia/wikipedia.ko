> This article is converted from Wikipedia: [ \(macOS\)](https://ko.wikipedia.org/wiki/_\(macOS\)).


[NeXTSTEP](https://ko.wikipedia.org/wiki/NeXTSTEP "wikilink"), [OPENSTEP](https://ko.wikipedia.org/wiki/OPENSTEP "wikilink"), [GNUstep](https://ko.wikipedia.org/wiki/GNUstep "wikilink"), 그리고 이것들의 후손작이라 할 수 있는 [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")와 [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink"), [tvOS](https://ko.wikipedia.org/wiki/tvOS "wikilink"), [watchOS](https://ko.wikipedia.org/wiki/watchOS "wikilink")에서의 **번들**(bundle)은 정의된 정와 파일 확장자를 갖는 [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")로, 개념상 관련된 파일들을 모두 하나로 묶어주는 역할을 한다.

보통 이런 번들은 [애플리케이션](https://ko.wikipedia.org/wiki/애플리케이션 "wikilink"), 프레임워크나 플러그인의 실행 파일을 포함하고 있다. 이런 번들들은 실행 코드란 걸 알려주는 파일이 있으며, 그리고 인터페이스 빌더나 스트링 같은 같은 리소스 파일, 틀, 사진, 음악 등등을 모두 다 집어넣고 있다. 다른 OS, 예를 들어 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 같은 경우, 이런 리소스들은 컴파일시 실행파일 안으로 들어간다. 구 [Mac OS에서도](https://ko.wikipedia.org/wiki/Mac_OS "wikilink") 비슷한 개념을 다뤘는데, 이는 파일의 리소스 포크에다가 추가적인 [메타데이터](https://ko.wikipedia.org/wiki/메타데이터 "wikilink")를 다는 것이었다.

프로그램적으로 번들은 [코코아](https://ko.wikipedia.org/wiki/코코아_\(API\) "wikilink") 클래스 중 `NSBundle`을 쓰거나, NeXTSTEP과 GNUStep의 파운데이션 프레임워크, 그리고 [코어 파운데이션의](https://ko.wikipedia.org/wiki/코어_파운데이션 "wikilink") `CFBundle`으로 접근할수 있다. 이런 번들의 UTI는 `com.apple.bundle`를 사용한다.\[1\] 기본적으로 이들 번들파일은 [파인더에서](https://ko.wikipedia.org/wiki/파인더_\(소프트웨어\) "wikilink") 하나의 파일로 보이며, 패키지 열기로 내용물을 보거나 수정할수 있다.

## 애플리케이션 번들

애플리케이션 번들은 디렉터리 계층을 가지는데, 맨 윗 디렉터리의 끝은 `.app` 확장자로 끝난다. 애플리케이션 번들의 경우 그 아래에 `Contents` 디렉터리가 자리하며, 이 `Contents` 디렉터리 안에 보통 다른 디렉터리가 들어간다. 이 `Contents` 중 맥의 경우 `MacOS`, [GNUStep](https://ko.wikipedia.org/wiki/GNUStep "wikilink") 같은 경우엔 애플리케이션의 이름 파일이 존재하고, 여기에 애플리케이션의 실행파일이 담긴다. 그리고 `Contents` 안에 리소스 폴더가 자리하고 있으며, 여기에 애플리케이션의 인터페이스 빌더 파일, nib 파일이 자리한다. 그리고 `Contents` 디렉터리 아래엔 없을수도 있지만 `Plugins`, `Frameworks`, 그리고 `Shared Frameworks`가 있어서 애플리케이션의 실행을 돕는다. 그리고 애플의 코드 서명을 받았을경우 `_CodeSignature`가 추가된다.

## 프레임워크 번들

macOS의 프레임 워크도 마찬가지로 번들로 저장되며, 맨 윗 디렉터리의 끝은 `.framework` 확장자로 끝난다. 그 아래 대렉터리엔 `Versions` 디렉터리가 자리하는데, 이 디렉터리엔 프레임워크의 한 버전 혹은 여러 버전이 있으며, 각각의 디렉터리 안에는 프레임워크의 다이내막 라이브러리 코드를 포함하고 있다. `Versions` 디렉터리는 또한 현재 버전의 `Current` 디렉터리로의 심볼릭 링크가 포함되어 있다.\[2\]

## 적재가능한 번들

적재가능한 번들에는 런타임에서 불러올수 있는 코드를 저장한다.\[3\] 이런 적재가능한 번들은 `.bundle`로 끝나며, 종종 플러그인에 사용되는데, 제일 대표적인 번들은 [메일 (애플)에서](https://ko.wikipedia.org/wiki/메일_\(애플\) "wikilink") 볼 수 있다.\[4\]\[5\]

## 기타 번들들

여러 macOS 소프트웨어들은 이 번들 포맷을 활용한다. 대표적인 예를 보자면 [스크리브너](../Page/스크리브너.md "wikilink") 같은 경우엔 `.scriv`로 끝난다. 그러나, 윈도에서는 이런 번들 개념이 없는터라 디렉터리 상태로 저장한다.

## .lproj

애플리케이션 번들에 포함된 **.lproj** 폴더는 [소프트웨어](https://ko.wikipedia.org/wiki/소프트웨어 "wikilink")의 [국제화와 지역화](https://ko.wikipedia.org/wiki/국제화와_지역화 "wikilink") 파일을 담고 있다. .lproj 폴더는 macOS 의 언어 선택에 따라 그 앞의 문자에 따라 선택된다. 예를 들어 `ko.lproj` 같은 경우, 한국어로 설정된 macOS에서 한글로 프로그램을 띄어준다. 보통 이들 폴더에는 [.nib](https://ko.wikipedia.org/wiki/.nib "wikilink") 파일이나 필요한 스트링 파일이나 이미지를 넣을수 있다.

## 참고 문헌

## 외부 링크

  - [Bundle Programming Guide](https://developer.apple.com/library/content/documentation/CoreFoundation/Conceptual/CFBundles/Introduction/Introduction.html) at Apple Developer Connection
  - [NSBundle documentation](http://www.gnustep.org/resources/documentation/Developer/Base/Reference/NSBundle.html) from the GNUstep project
  - [Platypus](http://www.sveinbjorn.org/platypus) — a tool to create application bundles around scripts
  - [File extension details](http://filext.com/file-extension/lproj)

[분류:MacOS](https://ko.wikipedia.org/wiki/분류:MacOS "wikilink") [분류:NeXT](https://ko.wikipedia.org/wiki/분류:NeXT "wikilink")

1.
2.
3.
4.  [Apple Mail plug-ins and tools](http://www.tikouka.net/mailapp/)
5.