> This article is converted from Wikipedia: [JQuery UI](https://ko.wikipedia.org/wiki/JQuery_UI).


**jQuery UI**(제이쿼리 UI)는 [jQuery](https://ko.wikipedia.org/wiki/jQuery "wikilink")([자바스크립트](../Page/자바스크립트.md "wikilink") [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")), [종속형 시트](../Page/종속형_시트.md "wikilink")(CSS), [HTML](../Page/HTML.md "wikilink")로 구현된 [GUI 위젯](../Page/GUI_위젯.md "wikilink"), 애니메이션 시각 효과, [테마](https://ko.wikipedia.org/wiki/테마 "wikilink")의 묶음이다.\[1\] 자바스크립트 애널리틱스 서비스 [Libscore](https://ko.wikipedia.org/wiki/Libscore "wikilink")에 따르면 jQuery UI는 상위 100만 개의 웹사이트 중 197,000곳 이상에서 이용되며 2번째로 유명한 자바스크립트 라이브러리로 분석되었다.\[2\] 저명한 사용처는 [핀터레스트](../Page/핀터레스트.md "wikilink"), [페이팔](../Page/페이팔.md "wikilink"), [IMDb](../Page/인터넷_영화_데이터베이스.md "wikilink"), [허핑턴 포스트](https://ko.wikipedia.org/wiki/허핑턴_포스트 "wikilink"), [넷플릭스](../Page/넷플릭스.md "wikilink")가 포함된다.\[3\]

jQuery와 jQuery UI 둘 다 [MIT 허가서를](../Page/MIT_허가서.md "wikilink") 통해 jQuery 재단에 의해 배급되는 [자유-오픈 소스 소프트웨어이다](../Page/자유-오픈_소스_소프트웨어.md "wikilink"). jQuery UI는 2007년 9월 처음 게시되었다.\[4\]\[5\]

## 기능

1.11.4 릴리스 기준:\[6\]

### 상호작용

Draggable, Droppable, Resizable, Selectable, Sortable

### 위젯

jQuery UI의 위젯들 모두 테마 매커니즘을 사용하여 테마를 입힐 수 있다.\[7\]

  - **Accordion** – Accordion 컨테이너
  - **Autocomplete** – 사용자가 입력한 것에 기반한 자동 완성 상자
  - **Button** – 강화된 버튼 모습, 라디오 버튼과 체크상자를 푸시 버튼으로 변환
  - **Datepicker** – 고급 날짜 선택기
  - **Dialog** – 쉽게 견고하게 다른 콘텐츠 최상위에 대화 상자 표시
  - **Menu** – 메뉴 표시
  - **Progressbar** – 상태 표시줄 (애니메이션 있음/없음 모두)
  - **Selectmenu** – 네이티브 컨트롤의 제한을 극복하기 위한, 네이티브 HTML 셀렉트 요소의 복제 및 확장
  - **Slider** – 완전한 맞춤식 슬라이더
  - **Spinner** – 넘퍼 스피너 표시
  - **Tabs** – 탭 사용자 인터페이스 관리 (인라인 / 요청 시 로드 콘텐츠 포함)
  - **Tooltip** – 툴팁 표시

### 효과

  - **Color Animation** – 한 색에서 다른 색으로 전환하는 애니메이션
  - **Toggle Class**, **Add Class**, **Remove Class**, **Switch Class** – 한 스타일에서 다른 스타일로 전환하는 애니메이션
  - **Effect** – 다양한 효과 (appear, slide-down, explode, fade-in, 등)
  - **Toggle** – 효과를 켜거나 끄는 것을 토글 처리
  - **Hide**, **Show** - 상기 효과를 사용하여 숨기거나 표시

### 유틸리티

  - **Position** – 다른 요소의 위치에 상대적으로 요소의 위치 설정 (정렬)
  - **Widget Factory** – 모든 jQuery UI 위젯과 동일한 추상화를 사용하여, 상태를 저장하는(stateful) jQuery 플러그인 생성

## 예제

``` javascript
// Make the element with id "draggable" draggable
$(function () {
    $("#draggable").draggable();
});
```

``` html5
<div id="draggable">
    <p>Drag me around</p>
</div>
```

이를 통해 ID "draggable"의 div가 사용자의 마우스에 의해 드래그가 가능해지게 된다.

## 출시 역사

jQuery UI는 2007년 9월 17일에 시작되었다.\[8\]

| 출시일\[9\]      | 버전 번호                | [JQuery](../Page/JQuery.md "wikilink") 의존성 | 참고                         |
| ------------- | -------------------- | ------------------------------------------ | -------------------------- |
| 2007년 9월 17일  |                      | 1.2.1+                                     | 초기 릴리스\[10\]               |
| 2008년 6월 8일   | 1.5                  |                                            |                            |
| 2009년 4월 16일  | 1.6                  | 1.2.6+                                     | jQuery 1.2.6의 호환 릴리스.      |
| 2009년 3월 3일   | 1.7                  | 1.3.2+                                     |                            |
| 2010년 3월 18일  | 1.8                  | 1.3.2+                                     |                            |
| 2011년 1월 19일  | 1.8.9                | 1.3.2+                                     |                            |
| 2011년 2월 22일  | 1.8.10               | 1.3.2+                                     |                            |
| 2011년 3월 15일  | 1.8.11               | 1.3.2+                                     |                            |
| 2011년 4월 13일  | 1.8.12               | 1.3.2+                                     |                            |
| 2011년 5월 12일  | 1.8.13               | 1.3.2+                                     |                            |
| 2011년 6월 17일  | 1.8.14               | 1.3.2+                                     |                            |
| 2011년 8월 1일   | 1.8.15               | 1.3.2+                                     |                            |
| 2011년 8월 15일  | 1.8.16               | 1.3.2+                                     |                            |
| 2012년 1월 10일  | 1.8.17               | 1.3.2+                                     |                            |
| 2012년 2월 20일  | 1.8.18               | 1.3.2+                                     |                            |
| 2012년 4월 16일  | 1.8.19               | 1.3.2+                                     |                            |
| 2012년 4월 30일  | 1.8.20               | 1.3.2+                                     |                            |
| 2012년 6월 5일   | 1.8.21               | 1.3.2+                                     |                            |
| 2012년 7월 24일  | 1.8.22               | 1.3.2+                                     |                            |
| 2012년 8월 15일  | 1.8.23               | 1.3.2+                                     |                            |
| 2012년 9월 28일  | 1.8.24               | 1.3.2+                                     |                            |
| 2012년 10월 8일  | 1.9.0                | 1.6+                                       |                            |
| 2012년 10월 25일 | 1.9.1                | 1.6+                                       |                            |
| 2012년 11월 23일 | 1.9.2                | 1.6+                                       |                            |
| 2013년 1월 17일  | 1.10.0               | 1.6+                                       | IE6 지원 중단\[11\]            |
| 2013년 2월 15일  | 1.10.1               | 1.6+                                       |                            |
| 2013년 3월 14일  | 1.10.2               | 1.6+                                       |                            |
| 2013년 5월 3일   | 1.10.3               | 1.6+                                       |                            |
| 2014년 1월 17일  | 1.10.4               | 1.6+                                       |                            |
| 2014년 4월 25일  | 1.11.0-beta.1        | 1.6+                                       | IE7 지원 중단\[12\]            |
| 2014년 5월 23일  | 1.11.0-beta.2        | 1.6+                                       |                            |
| 2014년 6월 26일  | 1.11.0               | 1.6+                                       |                            |
| 2014년 8월 13일  | 1.11.1               | 1.6+                                       |                            |
| 2014년 10월 16일 | 1.11.2               | 1.6+                                       |                            |
| 2015년 2월 12일  | 1.11.3               | 1.6+                                       |                            |
| 2015년 3월 11일  | 1.11.4               | 1.6+                                       |                            |
| 2016년 1월 26일  | 1.12.0-beta.1        | 1.7+                                       | IE8, IE9, IE10 지원 중단\[13\] |
| 2016년 3월 17일  | 1.12.0-rc.1          | 1.7+                                       |                            |
| 2016년 4월 21일  | 1.12.0-rc.2          | 1.7+                                       |                            |
| 2016년 7월 8일   | 1.12.0 (unannounced) | 1.7+                                       |                            |
| 2016년 9월 14일  | 1.12.1               | 1.7+                                       |                            |

## 각주

## 참고 자료

  -
  -
  -
## 외부 링크

  -
[분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:2006년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2006년_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:CSS 프레임워크](https://ko.wikipedia.org/wiki/분류:CSS_프레임워크 "wikilink")

1.
2.  <http://libscore.com/#libs>
3.  <http://libscore.com/#$.ui>
4.
5.
6.
7.
8.
9.
10.
11. [jQuery UI 1.10.0](http://blog.jqueryui.com/2013/01/jquery-ui-1-10-0/), retrieved on 2013년 2월 15일
12. [jQuery UI 1.11.0-beta.1](http://blog.jqueryui.com/2014/04/jquery-ui-1-11-0-beta-1/), retrieved on 2014년 5월 1일
13. [jQuery UI 1.12.0-beta.1](http://blog.jqueryui.com/2016/01/jquery-ui-1-12-0-beta-1/), retrieved on 2016년 2월 5일