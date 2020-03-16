> This article is converted from Wikipedia: [Ember.js](https://ko.wikipedia.org/wiki/Ember.js).


**Ember.js**는 [모델-뷰-뷰모델](https://ko.wikipedia.org/wiki/모델-뷰-뷰모델 "wikilink")(MVV) 패턴에 기반을 둔 [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") [자바스크립트](../Page/자바스크립트.md "wikilink") [웹 프레임워크이다](../Page/웹_프레임워크.md "wikilink"). 공통 이디엄(idiom)과 최상의 프랙티스(practice)를 프레임워크에 도입함으로써 개발자들이 스케일링이 가능한 [싱글 페이지 웹 애플리케이션을](../Page/싱글_페이지_애플리케이션.md "wikilink") 개발할 수 있게 한다.\[1\]

Ember는 수많은 유명 웹사이트에 사용되는데, 여기에는 [디스코스](https://ko.wikipedia.org/wiki/디스코스 "wikilink"),\[2\] [그루폰](https://ko.wikipedia.org/wiki/그루폰 "wikilink"),\[3\] [링크드인](../Page/링크드인.md "wikilink"), [Vine](https://ko.wikipedia.org/wiki/Vine "wikilink"), [Live Nation](https://ko.wikipedia.org/wiki/Live_Nation "wikilink"), [노드스트롬](../Page/노드스트롬.md "wikilink"), [트위치](../Page/트위치.md "wikilink"), [치폴레가](https://ko.wikipedia.org/wiki/치폴레_멕시칸_그릴 "wikilink") 포함된다.\[4\] 주로 웹 프레임워크로 간주되지만 Ember로 데스크톱과 모바일 애플리케이션도 만들 수 있다.\[5\]\[6\]\[7\] Ember 데스크톱의 가장 저명한 예로 [애플 뮤직](../Page/애플_뮤직.md "wikilink"),\[8\]([아이튠즈](../Page/아이튠즈.md "wikilink") 데스크톱 애플리케이션의 한 기능)이 있다. Ember의 상표는 Tilde사가 소유하고 있다.\[9\]

## 기본 개념

Ember는 5가지 주요 개념을 구성한다:\[10\]

  - 루트(Routes)
    Ember에서 애플리케이션의 상태는 URL로 표현한다. 각 URL은 사용자에게 보이는 것을 제어하는, 상응하는 루트가 있다.

<!-- end list -->

  - 모델(Models)
    모든 루트는 이와 연결되는 모델이 있으며, 애플리케이션의 현재 상태에 관한 데이터를 담고 있다.\[11\] 서버의 [JSON](../Page/JSON.md "wikilink") 객체를 불러들여 해당 객체들을 모델로 사용하기 위해 [jQuery](https://ko.wikipedia.org/wiki/jQuery "wikilink")를 사용할 수 있지만, 대부분의 애플리케이션들은 Ember 데이터 등의 모델 라이브러리를 사용하여 이를 관리한다.

<!-- end list -->

  - 템플릿(Templates)
    애플리케이션의 HTML을 빌드하기 위해 템플릿을 사용할 수 있으며 [HTMLBars](https://ko.wikipedia.org/wiki/HTMLBars "wikilink") 템플릿 언어로 작성한다. (HTMLBars는 문자열이 아닌 DOM 요소를 만드는 핸들바이다.)\[12\]

<!-- end list -->

  - 컴포넌트(Components)
    컴포넌트는 사용자 지정 HTML 태그이다. 자바스크립트를 사용하여 동작을 구현하며 보이는 형태는 HTMLBars 템플릿을 사용하여 정의한다. 컴포넌트는 자신의 데이터를 "소유"한다. 네스트(nest) 처리할 수 있으며 액션(이벤트)를 통해 부모 컴포넌트와 통신할 수 있다. [Polymer](https://web.archive.org/web/20150814004009/https://www.polymer-project.org/1.0/) 등 다른 컴포넌트 라이브러리들을 Ember에 사용할 수도 있다.\[13\]

<!-- end list -->

  - 서비스(Services)
    서비스는 사용자 세션 등 장기간 데이터를 보유하기 위한 싱글톤(singleton) 객체이다.\[14\]

## Ember 2.0

Ember 2.0은 2015년 8월 31일 출시되었다.\[15\]

## Ember 소프트웨어 스택

Ember.js는 Ember 코어 팀이 개발하고 지원하는 완전한 프론트엔드 스택의 한 구성 요소이다.

## 각주

## 추가 문헌

  - Regularly updated.

  - Regularly updated.

  -
## 외부 링크

  -
  -
  -
  - The official guide to learn Ember.

  -
  -
  -
  -
  - Collection of links to Ember resources.

  - Weekly newsletter on Ember.

  - Short screencasts covering various Ember features.

  - Bi-weekly podcast.

  - Weekly podcast.

[분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:Ajax](https://ko.wikipedia.org/wiki/분류:Ajax "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:웹 프레임워크](https://ko.wikipedia.org/wiki/분류:웹_프레임워크 "wikilink")

1.
2.
3.
4.  <http://libscore.com/?#Ember>
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.