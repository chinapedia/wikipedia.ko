> This article is converted from Wikipedia: [AHAH](https://ko.wikipedia.org/wiki/AHAH).


**AHAH**(Asynchronous HTML and HTTP, 비동기식 HTML과 HTTP)는 [자바스크립트](../Page/자바스크립트.md "wikilink")를 이용하여 동적으로 [웹 페이지를](../Page/웹_페이지.md "wikilink") 갱신하는 방법이라는 점에서 [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink")와 유사하지만, [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink")와는 달리 클라이언트측에서 요청에 대한 응답을 파싱하지 않고 직접적으로 사용된다는 점이 다르다. 이는 서버의 응답이 텍스트이거나 유효한 [XHTML](../Page/XHTML.md "wikilink")/[HTML](../Page/HTML.md "wikilink")구조를 포함하고 있어야 한다는 것을 의미한다.

## 개요

Ajax와 같이 XML-HTTP기능이 요청을 초기화하기 위해 사용되지만, 응답을 받았을 때 요청의 상태변화는 함수에 의해 통제되며 그 함수는 응답을 [도큐먼트 오브젝트 모델을](https://ko.wikipedia.org/wiki/도큐먼트_오브젝트_모델 "wikilink") 이용한 [XML](../Page/XML.md "wikilink")로 파싱하지 않는 대신 비 표준인 innerHTML 속성을 이용하여 문서의 대상 엘리먼트에 응답 내용을 직접적으로 삽입한다. innerHTML은 주요 [웹 브라우저](../Page/웹_브라우저.md "wikilink") (또는 사용자 에이전트)에 의해 지원되는 읽기/쓰기가 가능한 속성이며 [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 [인터넷 익스플로러에서](../Page/인터넷_익스플로러.md "wikilink") 처음 소개되었다.

## 고려사항

AHAH를 사용하기 위한 가장 실용적인 연습은 XML-HTTP 응답의 본문 구조를 수정하지 않으려고 하는 것이며, 사용하기 쉽고 덜 복잡하며 향상된 속도와 향상된 코드 가독성을 제공하기 때문에 자주 추천되는 방법이다. 또한, 비록 [W3C](../Page/W3C.md "wikilink")의 DOM 추천사항에 포함되어 있지 않더라도 innerHTML 속성 또한 광범위하게 지원되고 있다. 하지만 응답 XHTML 구조를 단순한 문자열 조작 이상의 변화를 필요로 할 경우에는 DOM을 기반으로 한 [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink")를 이용하는 것이 대상 엘리먼트에 추가된 응답 콘텐츠를 기반으로 한 엘리먼트에 대한 참조문서가 이미 생성되어 있으므로 재 사용이 가능하기 때문에 더 낫다. 하지만 구조의 복잡도와 변경 빈도는 성능변화에 영향을 끼치기 때문에 이러한 고려사항은 경우에 따라 다양해지게 된다. [오페라](../Page/오페라_\(웹_브라우저\).md "wikilink") 8.54와 [인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") 6이 현재 어떠한 문자열이든 허용하는 반면 [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 1.5는 *innerHTML*로서만 놓이게 되는 유효한 엘리먼트 구조만을 허용할 것이다. 또한 DOM을 다루기 위해 *innerHTML*을 사용하면서 속도는 매우 향상되었고 몇몇 광범위한 벤치마크가 이를 증명하기 위해 수행되었다. 이는 일부 케이스에서 Ajax를 사용하는 데 AHAH를 이용하는 것을 보장할 수도 있을지도 모른다. 하지만 불운하게도, 일반적으로 대부분의 주요 웹 브라우저는 심지어 문서 형태가 우선적으로 유효한 XML을 요구하는 [XHTML 1.0 표준을 엄격히 준수하는](https://ko.wikipedia.org/wiki/XHTML_1.0_표준을_엄격히_준수하는 "wikilink") 셋이라 하더라도 *innerHTML*로부터 유효한 [XML](../Page/XML.md "wikilink")을 반환하지 않는다. 이것은 *innerHTML*의 엉망인 [문자열 표기를](https://ko.wikipedia.org/wiki/문자열_표기 "wikilink") 분석하여 유효한 XML로 바꾸기 위해 상당한 가공이 필요하다는 것을 의미한다. 현재 대부분의 주요 웹 브라우저는 *innerHTML*을 사용할 때 원본 문서의 서로 다른 변형물을 반환한다. [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 1.5는 *img*, *br*, *input*등과 같은 단독 엘리먼트를 종결짓지 못하며 [오페라](../Page/오페라_\(웹_브라우저\).md "wikilink") 9는 엘리먼트 이름을 대문자로 변화시켜 반환한다. 게다가 [인터넷 익스플로러는](../Page/인터넷_익스플로러.md "wikilink") 앞의 두 가지 예에 대해 모두 실패할 뿐만 아니라 표준 요구사항인 속성값 주변의 *인용 부호*마저 제거해 버린다. 오페라와 파이어폭스의 경우 각각 단지 한 개씩만을 생략할 뿐이고 바라건대 그것은 곧 고쳐질 것이다. 그 사이 개발자는 무엇보다도 innerHTML의 결과물을 수정해야 한다. 오페라의 경우 제공되는 문서 형태가 커스텀 타입의 *text/html*형식 뿐만 아니라 *application/XHTML+XML*이나 *application/XML*, 또는 *text/xml*인 경우에도 소문자 형태의 엘리먼트 이름을 반환해야 한다.

innerHTML의 다른 사용례는 주 문서에 있는 [액션스크립트](../Page/액션스크립트.md "wikilink")와 [자바스크립트](../Page/자바스크립트.md "wikilink") 함수라 불리는 *ExternalInterface*를 통해 [Flash](https://ko.wikipedia.org/wiki/Flash "wikilink")로 중계하는 것이다. 이것은 파싱을 위해 유효한 XML을 필요로 하며 Flash를 통해 외부 콘텐트를 로딩하는 것을 피하는 데 사용될 수 있지만 오히려 대체나 Flash 표현을 위해 주 문서 구조에 포함된다. 이것은 [검색 엔진 최적화](../Page/검색_엔진_최적화.md "wikilink")(SEO) 노력에 도움을 준다.

## 표준화

AHAH는 [REST](../Page/REST.md "wikilink")가 가능한 XHTML(REX) 마이크로포맷의 일부분으로 채택되었다. AHAH를 구현하기 위한 방법 또한 Javascript 라이브러리에서 사용 가능하도록 만들어졌고 코드 크기를 줄여준다는 이점이 있다.

[분류:XML](https://ko.wikipedia.org/wiki/분류:XML "wikilink")