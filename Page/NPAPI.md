> This article is converted from Wikipedia: [NPAPI](https://ko.wikipedia.org/wiki/NPAPI).


**NPAPI**(Netscape Plugin Application Programming Interface)는 [웹 브라우저용으로](https://ko.wikipedia.org/wiki/웹_브라우저 "wikilink") [플러그인](https://ko.wikipedia.org/wiki/플러그인 "wikilink")을 개발할 수 있게 허용하는 [API](https://ko.wikipedia.org/wiki/API "wikilink")이다. 처음에는 1995년 [넷스케이프 내비게이터 2.0을](https://ko.wikipedia.org/wiki/넷스케이프_내비게이터_2.0 "wikilink") 시작으로 [넷스케이프](https://ko.wikipedia.org/wiki/넷스케이프 "wikilink") 브라우저용으로 개발되었으나 이어서 다른 브라우저들에도 채용되었다.

NPAPI 구조에서 플러그인은 audio/mp3와 같은 처리 가능한 [콘텐츠 타입을](https://ko.wikipedia.org/wiki/미디어_타입 "wikilink") 선언한다. 브라우저가 네이티브로 처리할 수 없는 콘텐츠 타입을 마주치면 적절한 플러그인을 로드하여 플러그인이 렌더링할 브라우저 콘텍스트 내에 공간을 비치시킨 다음 데이터를 그곳으로 흘려보낸다. 이러한 플러그인은 데이터를 렌더링하는 역할을 하게 된다. 이 플러그인은 페이지 안에 자리를 차지하며 동작하는데 이는 외부 애플리케이션을 실행시켜 알 수 없는 콘텐츠 타입을 처리했던 오래된 브라우저들과는 상반된다.

NPAPI의 요구사항은 각 플러그인이 플러그인 콘텐츠의 초기화, 작성, 삭제, 위치 지정을 위한 약 15개의 기능을 구현, 노출해야 한다는 것이다. NPAPI는 또한 스크립팅, 인쇄, 전체 화면 플러그인, 창없는 플러그인, 콘텐츠 스크리밍을 지원한다.

## 스크립트 지원

  - 라이브커넥트(LiveConnect): 자바와 자바스크립트 소프트웨어가 웹 페이지 안에서 상호 통신할 수 있게 해 주는 웹 브라우저의 기능이다.
  - 크로스 포인트 커넥트(XPConnect): [XPCOM](https://ko.wikipedia.org/wiki/XPCOM "wikilink")과 자바스크립트 간의 단순한 상호운용을 허용하는 기술이다.
  - NPRuntime

## 브라우저 지원

다음의 [웹 브라우저들이](https://ko.wikipedia.org/wiki/웹_브라우저 "wikilink") NPAPI 플러그인들을 지원한다.

  - [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") (모질라는 [플래시 플레이어를](https://ko.wikipedia.org/wiki/플래시_플레이어 "wikilink") 제외하고\[1\] 2017년 3월 NPAPI 지원을 제거할 것이다. 윈도우용 64비트 파이어폭스는 플래시와 실버라이트 플러그인용 NPAPI만을 지원한다.\[2\])
  - [페일 문](https://ko.wikipedia.org/wiki/페일_문 "wikilink")
  - Isis ([웹OS](https://ko.wikipedia.org/wiki/웹OS "wikilink"))
  - [캉커러](https://ko.wikipedia.org/wiki/캉커러 "wikilink")
  - [미도리](https://ko.wikipedia.org/wiki/미도리_\(웹_브라우저\) "wikilink")
  - [오디세이 웹 브라우저](https://ko.wikipedia.org/wiki/오디세이_웹_브라우저 "wikilink") ([MorphOS](https://ko.wikipedia.org/wiki/MorphOS "wikilink"))
  - [QupZilla](https://ko.wikipedia.org/wiki/QupZilla "wikilink")
  - [사파리](https://ko.wikipedia.org/wiki/사파리_\(웹_브라우저\) "wikilink")
  - [시몽키](https://ko.wikipedia.org/wiki/시몽키 "wikilink")
  - [웹](https://ko.wikipedia.org/wiki/웹_\(웹_브라우저\) "wikilink")
  - [유즈블](https://ko.wikipedia.org/wiki/유즈블 "wikilink")

다음의 웹 브라우저들은 NPAPI를 지원하지만 개발이 중단되었다:

  - [카미노](https://ko.wikipedia.org/wiki/카미노 "wikilink")
  - [모질라 애플리케이션 스위트](https://ko.wikipedia.org/wiki/모질라_애플리케이션_스위트 "wikilink")
  - [넷스케이프 내비게이터](https://ko.wikipedia.org/wiki/넷스케이프_내비게이터 "wikilink"), [넷스케이프 커뮤니케이터](https://ko.wikipedia.org/wiki/넷스케이프_커뮤니케이터 "wikilink")

## 스크립팅 지원

스크립팅은 웹 페이지에서 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink") 코드가 플러그인과 상호 작용할 수 있게 하는 기능이다. 다양한 버전의 넷스케이프, 그 뒤 [모질라](https://ko.wikipedia.org/wiki/모질라 "wikilink")는 라이브커넥트, XP커넥트, NP런타임을 포함하여 각기 다른 기술들을 사용하여 이 기능을 지원하였다.

  - 라이브커넥트
  - XP커넥트
  - NP런타임

## 플러그인

다음은 NPAPI 기반 플러그인 목록이다.

  - [어도비 어크로뱃](https://ko.wikipedia.org/wiki/어도비_어크로뱃 "wikilink") 뷰어
  - [어도비 플래시 플레이어](https://ko.wikipedia.org/wiki/어도비_플래시_플레이어 "wikilink")
  - [어도비 쇼크웨이브 플레이어](https://ko.wikipedia.org/wiki/어도비_쇼크웨이브_플레이어 "wikilink")
  - [DivX 웹 플레이어](https://ko.wikipedia.org/wiki/DivX "wikilink")
  - [자바 런타임 환경](https://ko.wikipedia.org/wiki/자바_런타임_환경 "wikilink")
  - [유니티](https://ko.wikipedia.org/wiki/유니티_\(게임_엔진\) "wikilink") 웹 플레이어
  - [윈도우 정품 혜택](https://ko.wikipedia.org/wiki/윈도우_정품_혜택 "wikilink") 플러그인 (파이어폭스용)

## 유사 기술

### 액티브X

### PPAPI

2009년 8월 12일, 구글 코드의 한 페이지\[3\]는 새로운 프로젝트 페퍼(Project Pepper)를 선보이면서 페퍼 플러그인 API(PPAPI)와 연계되었다.\[4\]

PPAPI는 NPAPI의 파생물로서, 플러그인의 포팅을 높이고 더 안전하게 만드는 데 초점을 둔다.\[5\]

PPAPI는 구글 크롬과 [크로미엄에만](https://ko.wikipedia.org/wiki/크로미엄_\(웹_브라우저\) "wikilink") 지원되었다. 나중에 [오페라와](https://ko.wikipedia.org/wiki/오페라_\(웹_브라우저\) "wikilink") [비발디](https://ko.wikipedia.org/wiki/비발디 "wikilink")와 같은 다른 크로미엄 브라우저들 또한 PPAPI 플러그인 지원을 추가하였다.

2012년 2월, [어도비 시스템즈는](https://ko.wikipedia.org/wiki/어도비_시스템즈 "wikilink") 차기 리눅스 버전의 어도비 플래시 플레이어는 PPAPI를 통해서만 제공될 것이라 발표하였다. NPAPI로 지원되는 이전 릴리스 플래시 플레이어 11.2는 5년 동안 보안 업데이트를 받게 된다.\[6\] 2016년 8월, 어도비는 이전 발언과는 달리 리눅스에서 NPAPI 플래시 플레이어를 다시 지원하고 새로운 버전을 계속 출시할 것이라고 발표하였다.\[7\]

## 같이 보기

  - [NSAPI](https://ko.wikipedia.org/wiki/NSAPI "wikilink")(Netscape Server Application Programming Interface)
  - [액티브X](https://ko.wikipedia.org/wiki/액티브X "wikilink")

## 각주

## 외부 링크

  - [플러그인 개발 문서](https://developer.mozilla.org/en/Plugins) - 모질라 개발자 센터 (NPAPI API 포함)

[분류:넷스케이프](https://ko.wikipedia.org/wiki/분류:넷스케이프 "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:웹 브라우저](https://ko.wikipedia.org/wiki/분류:웹_브라우저 "wikilink")

1.
2.
3.
4.
5.
6.
7.