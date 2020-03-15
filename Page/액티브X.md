> This article is converted from Wikipedia: [X](https://ko.wikipedia.org/wiki/X).


**액티브X**()는 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사가 개발한 재사용 가능한 [객체지향적인](https://ko.wikipedia.org/wiki/객체_지향_프로그래밍 "wikilink") [소프트웨어](https://ko.wikipedia.org/wiki/소프트웨어 "wikilink") 구성 요소 개발에 사용되는 기술이다. 액티브X는 [컴포넌트 오브젝트 모델과](https://ko.wikipedia.org/wiki/컴포넌트_오브젝트_모델 "wikilink") [객체 연결 삽입 (OLE)을](https://ko.wikipedia.org/wiki/객체_연결_삽입 "wikilink") 적용해 [WWW](https://ko.wikipedia.org/wiki/WWW "wikilink")으로부터 다운로드받은 컨텐츠들을 이용하는 데 이용된다. 액티브X는 전반적인 기술 혹은 기술을 구현하는데 필요한 구성요소를 가리키며, 액티브X컨트롤은 액티브X를 이용해 만든 작은 프로그램을 말한다. 대부분 액티브X는 [인터넷 익스플로러의](https://ko.wikipedia.org/wiki/인터넷_익스플로러 "wikilink") [플러그인](https://ko.wikipedia.org/wiki/플러그인 "wikilink")을 만드는 데 사용된다.\[1\]

## 액티브X 컨트롤

액티브X 컨트롤은 액티브X를 이용해 만든 응용 프로그램을 말한다. 각각의 액티브X 컨트롤은 독립된 사용자 인터페이스를 가지는 [COM](https://ko.wikipedia.org/wiki/컴포넌트_오브젝트_모델 "wikilink") 서버로서 동작하며 주로 [인터넷](../Page/인터넷.md "wikilink")으로 배포되어 웹 브라우저를 통해 실행된다. 이를테면 애니메이션을 보여주고 특정한 종류의 파일을 보여 주고 데이터를 수집하는 맞춤식의 응용 프로그램들이 이에 속한다.

어떠한 면에서 액티브X 컨트롤은 [자바 애플릿과](https://ko.wikipedia.org/wiki/자바_애플릿 "wikilink") 비슷하다. 프로그래머들은 액티브X 컨트롤이나 자바 애플릿을 사용하여 웹 브라우저가 해당 프로그램을 다운로드하여 실행게 한다. 자바 애플릿과 액티브X 컨트롤의 차이점은 다음과 같다.

  - 자바 애플릿은 거의 모든 플랫폼에서 실행할 수 있지만 액티브X 구성 요소는 공식적으로 마이크로소프트의 [인터넷 익스플로러](https://ko.wikipedia.org/wiki/인터넷_익스플로러 "wikilink") [웹 브라우저와](https://ko.wikipedia.org/wiki/웹_브라우저 "wikilink") [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [운영 체제에서만](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 동작하고,\[2\] 바이너리 형태로 배포되기 때문에 인텔 x86 CPU가 필요한 경우가 많다.\[3\] [컴퓨터 바이러스와](https://ko.wikipedia.org/wiki/컴퓨터_바이러스 "wikilink") [스파이웨어](https://ko.wikipedia.org/wiki/스파이웨어 "wikilink")와 같은 [악성 코드는](https://ko.wikipedia.org/wiki/악성_코드 "wikilink") 액티브X 컨트롤을 이용하면 악성 사이트로부터 뜻하지 않게 설치될 수 있다. (이를 [드라이브 바이 다운로드라](../Page/드라이브_바이_다운로드.md "wikilink") 부른다)
  - 액티브X 컨트롤은 자바 애플릿과는 다르게 코드 실행에 대한 제약이 적기 때문에, 보안이 취약해 소프트웨어와 데이터를 손상시킬 수 있는 위험성이 있다. 이를 위해 마이크로소프트는 등록 시스템을 개발하여, 브라우저가 액티브X 컨트롤을 다운로드하기 전에 해당 컨트롤의 디지털 서명과 인증서를 확인하고, 적절한 프로그램인지 인증할 수 있게 하였다.

프로그래머들은 액티브X 컨트롤을 다음의 언어/환경을 포함하여, COM 구성 요소 개발을 지원하는 어떠한 언어로도 기록할 수 있다.

  - [ATL](https://ko.wikipedia.org/wiki/액티브_탬플릿_라이브러리 "wikilink") 또는 [MFC와](../Page/마이크로소프트_파운데이션_클래스_라이브러리.md "wikilink") 같은 라이브러리의 도움을 받거나 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")를 직접 이용하여 사용할 수 있다.\[4\]
  - [볼랜드 델파이](https://ko.wikipedia.org/wiki/볼랜드_델파이 "wikilink")
  - [비주얼 베이직](https://ko.wikipedia.org/wiki/비주얼_베이직 "wikilink")

## 역사

[OLE 2.0이](https://ko.wikipedia.org/wiki/객체_연결_삽입 "wikilink") 복잡하고 [MFC에서](../Page/마이크로소프트_파운데이션_클래스_라이브러리.md "wikilink") COM을 거의 지원하지 않는 문제가 일자 마이크로소프트는 이들을 더 단순하게 만들기 위한 규격을 세워서 1996년에 액티브X라는 이름으로 기술을 다시 상품화하였다.\[5\]\[6\] 이렇게 단순화한 뒤에도 사용자들은 컨트롤에 여섯 가지 핵심 인터페이스를 추가할 것을 요구 받았다. 이에 대응하여 마이크로소프트는 [마법사](https://ko.wikipedia.org/wiki/마법사_\(소프트웨어\) "wikilink"), [ATL](https://ko.wikipedia.org/wiki/액티브_탬플릿_라이브러리 "wikilink") 기반 클래스, [매크로](https://ko.wikipedia.org/wiki/매크로_\(컴퓨터_과학\) "wikilink"), C++ 언어 확장을 만들면서 컨트롤을 더 간단히 기록할 수 있게 만들어 놓았다.

인터넷 익스플로러 3.0 (1996년)을 기점으로 마이크로소프트는 HTML 콘텐츠 안에 액티브X 컨트롤을 관리할 수 있는 지원을 추가하였다. 브라우저가 OBJECT [태그를](https://ko.wikipedia.org/wiki/HTML_요소 "wikilink") 통하여 액티브X 컨트롤을 지정한 페이지를 발견하면 사용자의 간섭 없이 컨트롤을 자동으로 내려받아 설치하였다. 이로써 웹을 더 풍성히 만드는 데 기여하긴 하였으나 윈도에서만 실행한다는 호환성 문제와 더불어 보안 문제까지 나타나게 되었다. 마침내 마이크로소프트는 액티브X를 포함한 브라우징을 더 안전하게 만들기 위하여 보안 기준을 도입하였다.\[7\]

  - 설치 패키지 ([CAB](https://ko.wikipedia.org/wiki/CAB "wikilink") 파일과 실행 파일)의 [디지털 서명이](https://ko.wikipedia.org/wiki/디지털_서명 "wikilink") 필요하다.
  - 컨트롤은 스크립팅을 위하여 이들이 안전하다는 것을 분명하게 선언하여야 한다.
  - 기본 보안 설정을 크게 높였다.
  - 인터넷 익스플로러는 악성 컨트롤의 차단 목록을 관리한다.

액티브X는 마이크로소프트가 자체적으로 호환성에서 기술적으로 자사의 웹표준을 지향하는 엣지 브라우저에서 이에 관한 기능을 지원하지 않는다.\[8\]

## IE가 아닌 응용 프로그램에서의 액티브X

굳이 인터넷 익스플로러를 사용하지 않고서라도 액티브X 콘텐츠를 실행할 수 있다. (이를테면 [와인을](https://ko.wikipedia.org/wiki/와인_\(소프트웨어\) "wikilink") 설치하는 등) 그 밖의 다른 방법은 다음과 같다:

  - [FX ActiveX 호스트](http://code.google.com/p/ff-activex-host/) 는 윈도용 [모질라 파이어폭스에서](https://ko.wikipedia.org/wiki/모질라_파이어폭스 "wikilink") 액티브X 컨트롤을 실행할 수 있다.
  - [모질라 ActiveX 컨트롤](http://www.iol.ie/~locka/mozilla/mozilla.htm) 은 2005년 말에 최신으로 업데이트되었으며 파이어폭스 1.5에서 실행한다.

## 다른 액티브X 기술

마이크로소프트는 액티브X 객체를 사용하여 많은 제품과 소프트웨어 플랫폼을 개발하였으며, 지금도 여전히 많이 사용되고 있다.

  - [액티브엑스 데이터 오브젝트](https://ko.wikipedia.org/wiki/액티브엑스_데이터_오브젝트 "wikilink")(ADO)
  - [ASP](https://ko.wikipedia.org/wiki/액티브_서버_페이지 "wikilink")
  - [DirectShow](https://ko.wikipedia.org/wiki/DirectShow "wikilink")
  - [컬래버레이션 데이터 오브젝트](https://ko.wikipedia.org/wiki/컬래버레이션_데이터_오브젝트 "wikilink")(CDO)
  - [액티브 스크립팅](https://ko.wikipedia.org/wiki/액티브_스크립팅 "wikilink")
  - [고급 시스템 포맷](https://ko.wikipedia.org/wiki/능동_스트리밍_포맷 "wikilink")(ASF)

## 개선 노력

  - [2010년](https://ko.wikipedia.org/wiki/2010년 "wikilink") [2월](https://ko.wikipedia.org/wiki/2월 "wikilink") [모질라 재단은](https://ko.wikipedia.org/wiki/모질라_재단 "wikilink") 대한민국의 인터넷 사용자들에게 액티브X의 퇴치 운동을 권유하였다.\[9\]
  - [2010년](https://ko.wikipedia.org/wiki/2010년 "wikilink") [3월 7일](https://ko.wikipedia.org/wiki/3월_7일 "wikilink") 행정안전부는 금융거래시 공인인증서만 보안 프로그램으로 인정하고 있는 규제를 폐지하기로 하였다. 이로 인해 액티브X가 실행되지 않는 스마트폰에서도 인터넷 뱅킹이 가능하게 되었다.\[10\] 그러나, 금융위원회는 전자금융거래법 시행령 개정을 검토한 바 없다고 밝혔다.\[11\]
  - [2010년](https://ko.wikipedia.org/wiki/2010년 "wikilink") [4월 20일](https://ko.wikipedia.org/wiki/4월_20일 "wikilink")
  - [2010년](https://ko.wikipedia.org/wiki/2010년 "wikilink") [4월 21일](https://ko.wikipedia.org/wiki/4월_21일 "wikilink")
  - [2010년](https://ko.wikipedia.org/wiki/2010년 "wikilink") [7월 9일](https://ko.wikipedia.org/wiki/7월_9일 "wikilink") [우리은행](https://ko.wikipedia.org/wiki/우리은행 "wikilink")은 대한민국 최초로 액티브X 없이 인터넷 뱅킹(우리오픈뱅킹(다른 운영체제, 다른 웹 브라우저 사용가능))을 사용할 수 있다.\[12\]\[13\]\[14\]
  - [2011년](https://ko.wikipedia.org/wiki/2011년 "wikilink") [3월 30일](https://ko.wikipedia.org/wiki/3월_30일 "wikilink") [방송통신위원회](https://ko.wikipedia.org/wiki/방송통신위원회 "wikilink")는 액티브X 대체기술 적용 확산, 웹 브라우저 이용 다양화 및 웹환경 고도화 등을 골자로 하는 「인터넷 이용 환경 개선 추진계획」을 발표했다.\[15\]
  - [2012년](https://ko.wikipedia.org/wiki/2012년 "wikilink") [1월 17일](https://ko.wikipedia.org/wiki/1월_17일 "wikilink") [방송통신위원회](https://ko.wikipedia.org/wiki/방송통신위원회 "wikilink")는 주요 100대 웹사이트의 액티브X 사용실태를 분기별로 조사·발표(1차 발표 3월말 예정)하고, 웹사이트 개선시 활용할 수 있는 ‘웹사이트 진단 시스템’을 구축해 웹 개발자나 웹서비스 제공자에게 개방할 계획이라고 발표했다.\[16\]
  - [2012년](https://ko.wikipedia.org/wiki/2012년 "wikilink") [4월 2일](https://ko.wikipedia.org/wiki/4월_2일 "wikilink") [행정안전부](https://ko.wikipedia.org/wiki/행정안전부 "wikilink")와 [방송통신위원회](https://ko.wikipedia.org/wiki/방송통신위원회 "wikilink")는 인터넷 이용편의증진 및 웹서비스 경쟁력 강화를 위해 민간 및 행정기관의 주요 웹 사이트 각각 100개를 대상으로 액티브X 사용현황을 조사했다. 대한민국의 민·관 주요 200대 사이트 중 84%인 168개 사이트에서 웹브라우저 호환성과 보안문제를 야기하는 액티브X 기술을 사용하고 있는 것으로 나타났다. 민간영역은 결제·인증(41.1%), 행정기관은 보안(40%)에서 액티브X를 가장 많이 사용하는 것으로 나타났다.\[17\]
  - [2012년](https://ko.wikipedia.org/wiki/2012년 "wikilink") [7월 12일](https://ko.wikipedia.org/wiki/7월_12일 "wikilink") [행정안전부](https://ko.wikipedia.org/wiki/행정안전부 "wikilink")와 [방송통신위원회](https://ko.wikipedia.org/wiki/방송통신위원회 "wikilink")는 1/4분기에 이어 2/4분기에도 주요 웹사이트 200개(민간 100, 행정기관 100)를 대상으로 액티브X 사용현황을 조사했다. 이번 조사에서는 IE(인터넷 익스플로러)에서만 액티브X를 사용하고 다른 웹브라우저에서는 대체기술을 제공하여 3종 이상의 웹브라우저(멀티브라우저)를 지원하는 웹사이트 현황도 함께 조사되었다. 그 결과 정부 행정기관의 100대 웹사이트 중 73%는 액티브X가 없거나 대체기술을 제공하여 3종 이상 웹브라우저에서 사용 가능한 것으로 나타났다.\[18\]
  - [2012년](https://ko.wikipedia.org/wiki/2012년 "wikilink") [7월 12일](https://ko.wikipedia.org/wiki/7월_12일 "wikilink") [방송통신위원회](https://ko.wikipedia.org/wiki/방송통신위원회 "wikilink")는 대한민국의 웹 환경 개선과 인터넷 글로벌 경쟁력 강화를 위해 “차세대 웹 표준 HTML5 확산 추진계획”을 발표했다.\[19\]
  - [2013년](https://ko.wikipedia.org/wiki/2013년 "wikilink") [4월 9일](https://ko.wikipedia.org/wiki/4월_9일 "wikilink") [슬로우뉴스](../Page/슬로우뉴스.md "wikilink")의 일부 기자와 [오픈넷](https://ko.wikipedia.org/wiki/오픈넷 "wikilink")의 일부 사람들, [최재천의원이](https://ko.wikipedia.org/wiki/최재천_\(1963년\) "wikilink") 액티브엑스 폐지 서명사이트 노액티브엑스를 제안하였다. [2014년](https://ko.wikipedia.org/wiki/2014년 "wikilink") [8월 25일](https://ko.wikipedia.org/wiki/8월_25일 "wikilink") 기준 서명인 수는 약 만 명이다.\[20\]
  - [2015년](https://ko.wikipedia.org/wiki/2015년 "wikilink") [6월 9일](https://ko.wikipedia.org/wiki/6월_9일 "wikilink") [한국인터넷진흥원](https://ko.wikipedia.org/wiki/한국인터넷진흥원 "wikilink")와 [미래창조과학부](https://ko.wikipedia.org/wiki/미래창조과학부 "wikilink")는 국내 웹사이트 운영업체 및 솔루션 업체를 대상으로 웹 표준 전환, 비표준 웹 기술 (액티브X, NPAPI) 관련정보 제공 및 개선기술 도입, 개발 지원을 추진한다고 밝혔다.\[21\]
  - [2017년](https://ko.wikipedia.org/wiki/2017년 "wikilink") [12월](https://ko.wikipedia.org/wiki/12월 "wikilink") [대한민국정부](https://ko.wikipedia.org/wiki/대한민국정부 "wikilink")는 2018년 연말정산에서 액티브X 설치 없이도 이용이 가능하도록 연말정산 간소화 서비스를 진행하였다.

## 같이 보기

### 액티브 기술

1990년대 말에 마이크로소프트사는 "액티브"(Active)라는 용어를 수많은 자사 기술 속에 다시 사용하기 시작했다. 다음의 기술은 액티브엑스 자체와 관계는 없지만 비슷한 이름을 가진다:

  - [액티브 채널](https://ko.wikipedia.org/wiki/액티브_채널 "wikilink")
  - [액티브 데스크톱](https://ko.wikipedia.org/wiki/액티브_데스크톱 "wikilink")
  - [액티브 디렉터리](https://ko.wikipedia.org/wiki/액티브_디렉터리 "wikilink")

### 기타

  - [대한민국의 웹 호환성 문제](../Page/대한민국의_웹_호환성_문제.md "wikilink")
  - [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink")
  - [오픈웹](../Page/오픈웹.md "wikilink")
  - [김기창](https://ko.wikipedia.org/wiki/김기창_\(법학자\) "wikilink")
  - [공인인증서](../Page/공인인증서.md "wikilink")
  - [NPAPI](../Page/NPAPI.md "wikilink")

## 각주

## 외부 링크

  - [Activating ActiveX Controls](https://web.archive.org/web/20130508092550/http://capitalhead.com/articles/click-to-activate-and-use-this-control---kb912812.aspx)

[분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:인터넷 익스플로러](https://ko.wikipedia.org/wiki/분류:인터넷_익스플로러 "wikilink")

1.
2.
3.
4.
5.
6.
7.  [Activating ActiveX Controls | Capitalhead.com](http://capitalhead.com/articles/activating-activex-controls.aspx)
8.  [IT동아](http://it.donga.com/26401/)
9.
10.
11. [한국경제 「모든 스마트폰서 인터넷뱅킹 된다」 제하의 기사 관련](http://www.korea.kr/policy/pressReleaseView.do?newsId=155439221)
12.
13.
14.
15. [2011년 제21차 위원회 결과](http://www.korea.kr/policy/pressReleaseView.do?newsId=155733596)
16. [방통위, 비표준 기술 액티브X 사용하는 사이트 정기적으로 조사·발표한다](http://www.korea.kr/policy/pressReleaseView.do?newsId=155807537)
17. [액티브X, 민간·정부 200대 사이트 중 168곳(84%)에서 사용](http://www.korea.kr/policy/pressReleaseView.do?newsId=155820220)
18. [민·관 주요 웹사이트 액티브X 2/4분기 현황조사 결과 발표](http://www.korea.kr/policy/pressReleaseView.do?newsId=155839186)
19. [방통위, 차세대 웹 표준 HTML5로 웹 환경 개선·인터넷 산업 경쟁력 모두 잡는다](http://www.korea.kr/policy/pressReleaseView.do?newsId=155839243)
20.
21.