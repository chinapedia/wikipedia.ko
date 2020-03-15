> This article is converted from Wikipedia: [JQuery](https://ko.wikipedia.org/wiki/JQuery).


**jQuery**(제이쿼리)는 [HTML](https://ko.wikipedia.org/wiki/HTML "wikilink")의 [클라이언트 사이드](https://ko.wikipedia.org/wiki/클라이언트_사이드 "wikilink") 조작을 단순화 하도록 설계된 [크로스 플랫폼의](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink") [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")다. [존 레식이](https://ko.wikipedia.org/wiki/존_레식 "wikilink") [2006년](https://ko.wikipedia.org/wiki/2006년 "wikilink") 뉴욕 시 [바캠프](../Page/바캠프.md "wikilink")(Barcamp NYC)에서 공식적으로 소개하였다. jQuery는 오늘날 가장 인기있는 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink") [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink") 중 하나이다.

jQuery는 [MIT 라이선스와](https://ko.wikipedia.org/wiki/MIT_라이선스 "wikilink") [GNU 일반 공중 사용 허가서v](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink")2의 [듀얼 라이선스를](https://ko.wikipedia.org/wiki/듀얼_라이선스 "wikilink") 가진 [자유 오픈 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_오픈_소프트웨어 "wikilink"). jQuery의 문법은 코드 보기, [문서 객체 모델](https://ko.wikipedia.org/wiki/문서_객체_모델 "wikilink") 찾기, 애니메이션 만들기, 이벤트 제어, [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink") 개발을 쉽게 할 수 있도록 디자인되었다. 또한, jQuery는 개발자가 [플러그인](https://ko.wikipedia.org/wiki/플러그인 "wikilink")을 개발할 수 있는 기능을 제공한다.

[마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")와 [노키아](https://ko.wikipedia.org/wiki/노키아 "wikilink")는 자사 플랫폼에 jQuery를 포함하는 계획을 발표한 바 있다. [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")는 [비주얼스튜디오](https://ko.wikipedia.org/wiki/비주얼스튜디오 "wikilink")의 ASP.NET AJAX 프레임워크와 ASP.NET MVC 프레임워크에 적용했고, [노키아](https://ko.wikipedia.org/wiki/노키아 "wikilink")는 자사의 [런타임](https://ko.wikipedia.org/wiki/런타임 "wikilink") [웹](https://ko.wikipedia.org/wiki/웹 "wikilink") [위젯](https://ko.wikipedia.org/wiki/위젯 "wikilink") 개발 플랫폼에 통합하였다. 또한, jQuery는 [미디어위키](https://ko.wikipedia.org/wiki/미디어위키 "wikilink")에도 1.16 버전부터 사용되고 있다.

## 기능

  - [DOM](https://ko.wikipedia.org/wiki/문서_객체_모델 "wikilink") 요소 선택 기의 파생 프로젝트이다.\[1\]
  - DOM 탐색 및 수정 (CSS 1-3 지원)
  - [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink") 셀렉터에 기반한 DOM 조작. 노드 요소 및 노드 속성(아이디 및 클래스)을 셀렉터 생성을 위한 기준으로 사용.
  - 이벤트
  - 특수효과 및 애니메이션
  - [AJAX](https://ko.wikipedia.org/wiki/AJAX "wikilink")
  - [JSON](../Page/JSON.md "wikilink") 파싱
  - 플러그인을 통한 확장성
  - 유틸리티
  - 호환성 메소드 (`inArray()`, `each()` 함수 등)
  - 멀티브라우저 지원 (크로스브라우저와는 다름)

### 브라우저 지원

jQuery 1.x와 2.x는 모두 최신 안정화 버전 및 그 이후 버전의 [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink"), [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink"), [사파리](https://ko.wikipedia.org/wiki/사파리_\(웹_브라우저\) "wikilink"), 그리고 [오페라를](https://ko.wikipedia.org/wiki/오페라_\(웹_브라우저\) "wikilink") 지원한다. 1.x 버전은 [인터넷 익스플로러](https://ko.wikipedia.org/wiki/인터넷_익스플로러 "wikilink") 6 및 그 이후 버전을 지원한다. 그러나 2.x 버전에서는 인터넷 익스플로러 6-8 버전이 지원되지 않으며 인터넷 익스플로러 9 또는 그 이후 버전을 지원한다.\[2\]

## 사용법

jQuery는 한 개의 JavaScript 파일로 존재한다. 공통의 DOM, 이벤트, 특수 효과, Ajax 함수를 포함한다. 다음 코드를 쓰면, 웹 페이지로 포함시킬 수 있다:

``` html4strict
<script type="text/javascript" src="path/to/jQuery.js"></script>
```

jQuery는 두 가지의 상호 작용 스타일을 갖고 있다:

  - `$` 함수 이용. jQuery 오브젝트의 팩토리 메소드이다. 각각의 함수들은 jQuery 오브젝트를 반환하고 서로 연계할 수 있다.
  - `$.` -가 앞에 붙은 함수 이용. 이들 함수는 jQuery 오브젝트 그 자체와 연동되지는 않는다.

일반적으로 여러 개의 DOM 노드들을 조작하는 작업은 `$` 함수로 시작된다. CSS 셀렉터 스트링을 가지고 호출된다. 결과적으로 0개 혹은 그 이상의 HTML 페이지 내의 엘리먼트를 레퍼런스하는 jQuery 오브젝트가 반환된다. 이 노드 집합들은 jQuery 오브젝트에 대해 인스턴스 메소드들을 적용함으로써 조작될 수 있다. 혹은 노드들 그 자체가 조작될 수 있다. 예를 들면 다음과 같다:

``` javascript
$("div.test").add("p.quote").addClass("blue").slideDown("slow");
```

…클래스에 `test`를 포함하는 모든 `div` 엘리먼트를 찾는다. 클래스에 `quote`를 포함하는 `p` 엘리먼트를 찾는다. 찾아낸 각각의 엘리먼트에 대해 `blue` 클래스를 추가한다. 그 뒤 아래쪽으로 슬라이드되는 애니메이션 효과를 준다. `$` 및 `add` 함수는 찾아낸(matched) 집합(set)에 영향을 준다. `addClass` 및 `slideDown` 함수는 레퍼런스된 노드들에 영향을 준다.

`$.`가 앞에 붙은 함수들은, 글로벌 프로퍼티나 행동에 영향을 주는, 유틸리티 메소드들이다. 예를 들면 다음과 같다:

``` javascript
$.each([1,2,3], function() {
  document.write(this + 1);
});
```

… `234` 를 도큐먼트에 출력한다.

`$.ajax` 및 관련 메소드로 [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink")를 수행하여 원격 데이터를 로드하거나 조작할 수 있다.

``` javascript
$.ajax({
  type: "POST",
  url: "some.php",
  data: "name=John&location=Boston",
  success: function(msg){
    alert( "Data Saved: " + msg );
  }
});
```

… 파라미터 `name=John&location=Boston`을 주면서 some.php에 요청을 보낸다.요청이 성공적으로 수행되었으면, 그 응답이 `alert()`된다.

## 배포 내역

| 배포일자                                                                                                              | 버전      | 부가정보                                 |
| ----------------------------------------------------------------------------------------------------------------- | ------- | ------------------------------------ |
| [2016년 7월 7일](http://blog.jquery.com/2016/07/07/jquery-3-1-0-released-no-more-silent-errors/)                     | 3.1     | jQuery.readyException 추가             |
| [2016년 6월 9일](http://blog.jquery.com/2016/06/09/jquery-3-0-final-released/)                                       | 3.0     | Promises/A+ 와 HTML5 호환성 개선           |
| [2016년 4월 5일](http://blog.jquery.com/2016/04/05/jquery-1-12-3-and-2-2-3-released/)                                | 2.2.3   |                                      |
| [2014년 1월 24일](http://blog.jquery.com/2014/01/24/jquery-1-11-and-2-1-released/)                                   | 2.1     |                                      |
| [2013년 4월 18일](http://blog.jquery.com/2013/04/18/jquery-2-0-released/)                                            | 2.0     | 2.x 버전의 IE 6 \~ 8 버전 지원 중단 1.x는 계속지원 |
| [2014년 1월 24일](http://blog.jquery.com/2014/01/24/jquery-1-11-and-2-1-released/)                                   | 1.11    |                                      |
| [2013년 5월 24일](http://blog.jquery.com/2013/05/24/jquery-1-10-0-and-2-0-1-released/)                               | 1.10    |                                      |
| [2013년 1월 15일](http://blog.jquery.com/2013/01/15/jquery-1-9-final-jquery-2-0-beta-migrate-final-released/)        | 1.9     | 사문화된 인터페이스 삭제 및 코드 정리                |
| [2012년 8월 9일](http://blog.jquery.com/2012/08/09/jquery-1-8-released/)                                             | 1.8     |                                      |
| [2011년 11월 3일](http://blog.jquery.com/2011/11/03/jquery-1-7-released/)                                            | 1.7     |                                      |
| [2011년 6월 30일](http://blog.jquery.com/2011/06/30/jquery-162-released/)                                            | 1.6.2   |                                      |
| [2011년 5월 12일](http://blog.jquery.com/2011/05/12/jquery-1-6-1-released/)                                          | 1.6.1   |                                      |
| [2011년 5월 3일](http://blog.jquery.com/2011/05/03/jquery-16-released/)                                              | 1.6     | attr()와 val() 함수의 큰 성능향상             |
| [2011년 3월 31일](http://blog.jquery.com/2011/03/31/jquery-152-released/)                                            | 1.5.2   |                                      |
| [2011년 2월 24일](http://blog.jquery.com/2011/02/24/jquery-151-released/)                                            | 1.5.1   |                                      |
| [2011년 1월 31일](http://blog.jquery.com/2011/01/31/jquery-15-released/)                                             | 1.5     |                                      |
| [2010년 11월 11일](http://blog.jquery.com/2010/11/11/jquery-1-4-4-release-notes/)                                    | 1.4.4   |                                      |
| [2010년 10월 16일](http://blog.jquery.com/2010/10/16/jquery-143-released/)                                           | 1.4.3   |                                      |
| [2010년 2월 19일](http://blog.jquery.com/2010/02/19/jquery-142-released/)                                            | 1.4.2   | 성능향상에 초점을 둔 버전업                      |
| [2010년 1월 25일](http://jquery14.com/day-12/jquery-141-released/)                                                   | 1.4.1   | 1.4 첫 번째 버그 픽스                       |
| [2010년 1월 14일](http://jquery14.com/day-01/jquery-14/)                                                             | 1.4     | 메이저 업데이트입니다.                         |
| [2009년 2월 20일](https://web.archive.org/web/20090827103446/http://blog.jquery.com/2009/02/20/jquery-132-released/) | 1.3.2   |                                      |
| [2009년 1월 21일](http://blog.jquery.com/2009/01/21/jquery-131-released/)                                            | 1.3.1   |                                      |
| [2009년 1월 14일](http://blog.jquery.com/2009/01/14/jquery-13-and-the-jquery-foundation/)                            | 1.3     | Sizzle Selector엔진을 핵심부에 도입           |
| [2008년 5월 24일](http://docs.jquery.com/Release:jQuery_1.2.6)                                                       | 1.2.6   |                                      |
| [2008년 5월 21일](http://docs.jquery.com/Release:jQuery_1.2.5)                                                       | 1.2.5   | 1.2.4 오류 빌드 수정                       |
| [2008년 5월 19일](http://docs.jquery.com/Release:jQuery_1.2.4)                                                       | 1.2.4   |                                      |
| [2008년 2월 8일](http://jquery.com/blog/2008/02/08/jquery-123-air-namespacing-and-ui-alpha/)                         | 1.2.3   |                                      |
| [2008년 1월 15일](http://jquery.com/blog/2008/01/15/jquery-122-2nd-birthday-present/)                                | 1.2.2   |                                      |
| [2007년 9월 16일](http://jquery.com/blog/2007/09/16/jquery-121-quick-fixes-for-12/)                                  | 1.2.1   |                                      |
| [2007년 9월 10일](http://jquery.com/blog/2007/09/10/jquery-12-jqueryextendawesome/)                                  | 1.2     |                                      |
| [2007년 8월 24일](http://jquery.com/blog/2007/08/24/jquery-114-faster-more-tests-ready-for-12/)                      | 1.1.4   |                                      |
| [2007년 7월 5일](http://jquery.com/blog/2007/07/05/jquery-1131/)                                                     | 1.1.3.1 |                                      |
| [2007년 7월 1일](http://jquery.com/blog/2007/07/01/jquery-113-800-faster-still-20kb/)                                | 1.1.3   |                                      |
| [2007년 5월 20일](http://jquery.com/blog/2007/05/20/help-test-jquery-113/)                                           | 1.1.3a  | Alpha 배포                             |
| [2007년 2월 27일](http://jquery.com/blog/2007/02/27/jquery-112/)                                                     | 1.1.2   |                                      |
| [2007년 1월 22일](http://jquery.com/blog/2007/01/22/jquery-111/)                                                     | 1.1.1   |                                      |
| [2007년 1월 14일](http://jquery.com/blog/2007/01/14/jquery-birthday-11-new-site-new-docs/)                           | 1.1     |                                      |
| [2007년 1월 8일](http://jquery.com/blog/2007/01/08/jquery-11a/)                                                      | 1.1a    | Alpha 배포                             |
| [2006년 12월 12일](http://jquery.com/blog/2006/12/12/jquery-104/)                                                    | 1.0.4   | Last 1.0 bug fix                     |
| [2006년 10월 27일](http://jquery.com/blog/2006/10/27/jquery-103/)                                                    | 1.0.3   |                                      |
| [2006년 10월 9일](http://jquery.com/blog/2006/10/09/jquery-102/)                                                     | 1.0.2   |                                      |
| [2006년 8월 31일](http://jquery.com/blog/2006/08/31/jquery-101/)                                                     | 1.0.1   |                                      |
| [2006년 8월 26일](http://jquery.com/blog/2006/08/26/jquery-10/)                                                      | 1.0     | 첫 번째 안정화 배포                          |
| [2006년 6월 30일](http://blog.jquery.com/2006/06/30/jquery-10-alpha-release/)                                        | 1.0a    | Alpha 배포                             |

## 각주

  - [eWeek](http://www.eweek.com/article2/0,1895,2010602,00.asp)
  - [Infoworld](https://web.archive.org/web/20071110102930/http://www.infoworld.com/article/06/08/31/HNjscriptsandcastle_1.html), [(again)](https://web.archive.org/web/20071216105531/http://weblog.infoworld.com/techwatch/archives/007794.html)
  - [Advancing JavaScript with Libraries (Part 1) VIDEO](https://web.archive.org/web/20070831084203/http://video.yahoo.com/video/play?ei=UTF-8&gid=133414&vid=410472&b=1)
  - [Advancing JavaScript with Libraries (Part 2) VIDEO](https://web.archive.org/web/20070317005236/http://video.yahoo.com/video/play?ei=UTF-8)

## 더 읽어보기

  - Learning jQuery,
  - jQuery in Action,
  - Beginning JavaScript with DOM Scripting and Ajax,
  - Hacking del.icio.us,
  - Pro JavaScript Techniques,
  - AJAX and PHP: Building Responsive Web Applications,
  - Web Development Solutions,

## 참조

<references/>

## 외부 링크

  -
[분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:2006년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2006년_소프트웨어 "wikilink") [분류:Ajax](https://ko.wikipedia.org/wiki/분류:Ajax "wikilink") [분류:자바스크립트로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바스크립트로_작성된_자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:웹 프레임워크](https://ko.wikipedia.org/wiki/분류:웹_프레임워크 "wikilink")

1.
2.  [Browser Support | jQuery](http://jquery.com/browser-support/)