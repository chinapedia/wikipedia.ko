> This article is converted from Wikipedia: [XNU](https://ko.wikipedia.org/wiki/XNU).


**XNU**는 [맥 OS X](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink") [운영 체제에](../Page/운영_체제.md "wikilink") 사용할 목적으로 [애플이](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 인수하고 개발한 컴퓨터 [운영 체제](../Page/운영_체제.md "wikilink") [커널이다](../Page/커널_\(컴퓨팅\).md "wikilink"). [다윈](../Page/다윈_\(운영_체제\).md "wikilink") 운영 체제의 일부로서 [자유 및 오픈 소스 소프트웨어로](https://ko.wikipedia.org/wiki/자유_및_오픈_소스_소프트웨어 "wikilink") 공개되었다. XNU는 *X is Not [Unix](../Page/유닉스.md "wikilink")*(X는 유닉스가 아니다)를 가리킨다.\[1\]

원래 [NeXT](../Page/NeXT.md "wikilink")가 [NeXTSTEP](../Page/NeXTSTEP.md "wikilink") 운영 체제에 사용할 목적으로 개발된 XNU는 [카네기 멜론 대학교가](https://ko.wikipedia.org/wiki/카네기_멜론_대학교 "wikilink") [4.3BSD의](../Page/BSD.md "wikilink") 구성요소를 포함하여 개발한 [마하 커널의](https://ko.wikipedia.org/wiki/마하_\(커널\) "wikilink") 버전 2.5와, 드라이버 키트(Driver Kit)라는 이름의 객체 지향 API를 합친 [하이브리드 커널이다](../Page/하이브리드_커널.md "wikilink").

애플이 NeXT를 인수한 뒤 마하 구성 요소는 3.0으로 업그레이드되었으며 BSD 구성 요소들은 [FreeBSD](../Page/FreeBSD.md "wikilink") 프로젝트의 코드 업그레이드와 더불어 업그레이드되었고 드라이버 키트는 [입출력 키트로](https://ko.wikipedia.org/wiki/입출력_키트 "wikilink") 불리는 드라이버를 기록하기 위해 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") API로 대체되었다.

## 커널 디자인

[섬네일](https://ko.wikipedia.org/wiki/파일:XNU_v2.svg "wikilink") XNU는 [하이브리드 커널로](../Page/하이브리드_커널.md "wikilink"), [모놀리식 커널과](../Page/모놀리식_커널.md "wikilink") [마이크로 커널의](https://ko.wikipedia.org/wiki/마이크로_커널 "wikilink") 특징을 모두 갖고 있다.

### Mach

XNU 커널의 기본인 [Mach는](../Page/Mach_\(커널\).md "wikilink") 간단한 마이크로 커널이다. 그렇기 때문에 OS의 코어 부분을 분리된 프로세스에서 실행할 수 있고, 높은 유연성을 보인다(Mach 코어 상에서 여러 OS를 병렬로 실행할 수 있다). 그러나 커널 모드와 유저모드의 전환과 마이크로커널과 서비스 데몬의 주소 공간 사이의 맵핑과 복사때문에 오버헤드가 발생해, 퍼포먼스가 저하될 수 있다. macOS의 디자이너들은 속도를 올리기 위해 [BSD](../Page/BSD.md "wikilink")의 기능을 마하 커널에 집어넣었다. 그 결과 마하 커널과 클래식 BSD 커널의 몇몇 장단점을 모두 가지게 되었다.

### BSD

커널의 [BSD](../Page/BSD.md "wikilink") 부분은 [POSIX](../Page/POSIX.md "wikilink") [API](../Page/API.md "wikilink")과 마하 커널 위에서의 [유닉스](../Page/유닉스.md "wikilink") 프로세스 모델, 보안 규칙, 사용자와 그룹id, 권한, [네트워크 프로토콜](https://ko.wikipedia.org/wiki/네트워크_프로토콜 "wikilink"), [가상 파일 시스템](https://ko.wikipedia.org/wiki/가상_파일_시스템 "wikilink")(저널링 단에 독립적인 파일시스템도 포함), [HFS](https://ko.wikipedia.org/wiki/HFS "wikilink")/[HFS+](../Page/HFS_플러스.md "wikilink"), [네트워크 파일 시스템](../Page/네트워크_파일_시스템.md "wikilink") 클라이언트와 서버, 암호 프레임워크, [유닉스 시스템 V](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink")(IPC), 유닉스 audit 시스템, 필수 접근 관리 등을 제공한다.\[2\] XNU의 BSD 코드는 [FreeBSD](../Page/FreeBSD.md "wikilink") 커널에서 가져왔다. 많은 부분이 상당히 바뀌었지만 애플과 FreeBSD 프로젝트 사이에서의 코드 공유는 계속 일어나고 있다.\[3\]

### K32/K64

[맥 OS X 10.6 스노 레퍼드](https://ko.wikipedia.org/wiki/맥_OS_X_10.6 "wikilink")([다윈](../Page/다윈_\(운영_체제\).md "wikilink") 버전 10) 이후 버전에 들어간 XNU의 경우 [32비트](../Page/32비트.md "wikilink")의 K32와 [64비트](../Page/64비트.md "wikilink")의 K64로 나뉜다.\[4\] K32는 64비트 애플리케이션을 [사용자 공간에서](../Page/사용자_공간.md "wikilink") 구동할 수 있다. 맥 OS X 10.6에서 추가된 것은 XNU를 64비트 [커널 공간에서](../Page/사용자_공간.md "wikilink") 구동할 수 있게 된 것이다. K64는 K32와 비교해서 많은 장점을 갖는다.\[5\]

  - 32GB 이상의 램을 관리할 수 있다.
  - 캐시 버퍼 사이즈가 32비트 커널이 허용하는 것보다 큰 사이즈를 가질 수 있어 I/O 성능을 향상시킬 수 있다.
  - 높은 성능의 네트워크 기기나 여러 [GPU](https://ko.wikipedia.org/wiki/GPU "wikilink")를 사용할 때의 성능이 증가한다. 이는 주변기기들이 아주 큰 [직접 메모리 접근](../Page/직접_메모리_접근.md "wikilink") 버퍼를 가진다 해도 커널이 모두 64비트 공간에 할당할 수 있기 때문이다.

## 각주

<references />

## 외부 링크

  - [XNU: 커널](http://osxbook.com/book/bonus/ancient/whatismacosx/arch_xnu.html) - XNU 구성요소 개요

[분류:모놀리식 커널](https://ko.wikipedia.org/wiki/분류:모놀리식_커널 "wikilink") [분류:MacOS](https://ko.wikipedia.org/wiki/분류:MacOS "wikilink")

1.
2.
3.
4.  [Mac OS X 10.6 Snow Leopard: the Ars Technica review, page 5](http://arstechnica.com/apple/reviews/2009/08/mac-os-x-10-6.ars/5)
5.  [What's New in Mac OS X: Mac OS X v10.6](http://developer.apple.com/mac/library/releasenotes/MacOSX/WhatsNewInOSX/Articles/MacOSX10_6.html)