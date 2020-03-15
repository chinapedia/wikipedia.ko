> This article is converted from Wikipedia: [Acid3](https://ko.wikipedia.org/wiki/Acid3).


**Acid3**는 [웹 브라우저가](https://ko.wikipedia.org/wiki/웹_브라우저 "wikilink") (특히 [DOM](https://ko.wikipedia.org/wiki/DOM "wikilink")과 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink")와 관련하여) 얼마나 잘 [웹 표준을](https://ko.wikipedia.org/wiki/웹_표준 "wikilink") 준수하고 있는지를 검사하는 [웹 표준 프로젝트의](https://ko.wikipedia.org/wiki/웹_표준_프로젝트 "wikilink") 테스트 페이지이다.

성공할 경우 Acid3 테스트는 흰 배경에 색이 들어간 여러 개의 [직사각형](https://ko.wikipedia.org/wiki/직사각형 "wikilink")을 표현하면서 점차 증가하는 백분율 수치를 보여 준다. 표시되는 백분율 수치는 통과된 서브 테스트의 수에 기반을 둔다(하지만 통과한 서브 테스트의 개수와 백분율이 항상 같다고 볼 수 없다). 또한 브라우저는 같은 브라우저에 표시되는 참고 페이지와 정확히 같은 페이지를 [렌더해야](https://ko.wikipedia.org/wiki/렌더링 "wikilink") 한다. 비트맵 결과만 나오는 [Acid2](https://ko.wikipedia.org/wiki/Acid2 "wikilink") 테스트와 달리 Acid3 테스트의 참고 렌더링의 글자는 비트맵이 아니기 때문에 글꼴 표시의 차이점도 구별할 수 있다.

2007년 4월에 개발되었으며\[1\] [2008년](https://ko.wikipedia.org/wiki/2008년 "wikilink") [3월 3일에](https://ko.wikipedia.org/wiki/3월_3일 "wikilink") 공개되었다.\[2\] 주 개발자는 [이언 힉슨](https://ko.wikipedia.org/wiki/이언_힉슨 "wikilink")(Ian Hickson)으로 그는 [Acid2](https://ko.wikipedia.org/wiki/Acid2 "wikilink") 테스트도 작성하였다. Acid2는 주로 [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink")에 초점을 두고 있지만, 세 번째 Acid 테스트는 역시 현대에 쓰이며 매우 상호성이 높은 기술인 [웹 2.0](https://ko.wikipedia.org/wiki/웹_2.0 "wikilink")([ECMAScript](https://ko.wikipedia.org/wiki/ECMAScript "wikilink"), [DOM Level 2와](https://ko.wikipedia.org/wiki/DOM#DOM_.EB.8B.A8.EA.B3.84 "wikilink") 같은)의 웹사이트 특성에 초점을 둔다. 일부 서브 테스트는 [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink"), [XML](https://ko.wikipedia.org/wiki/XML "wikilink"), [data: URIs와](https://ko.wikipedia.org/wiki/data:_URI_scheme "wikilink") 관련되어 있다. 논란이 되는 것은, 이 테스트는 [CSS2](https://ko.wikipedia.org/wiki/CSS2 "wikilink") 권고안의 내용 중, CSS2.1에서 삭제되었다가 아직 권고 예정안으로 정해지지 않은 W3C [CSS3](https://ko.wikipedia.org/wiki/CSS3 "wikilink") 개발에 다시 도입된 요소를 일부 포함하고 있다는 점이다.

## 테스트 내용

Acid3 의 주요 부분은 [ECMA스크립트](https://ko.wikipedia.org/wiki/ECMA스크립트 "wikilink") ([자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink"))로 쓰여져있고, 네 개의 특별한 서브 테스트(0, 97, 98, 99번)를 포함한 100개의 서브 테스트들이 6개의 '버킷(Bucket)'으로 불리는 묶음으로 나뉘어 있다.\[3\]

  - 버킷 1: DOM 순회(DOM Traversal), DOM 범위(Range), [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")
  - 버킷 2: DOM2 코어(Core), DOM2 이벤트(Events)
  - 버킷 3: DOM2 뷰(Views), DOM2 스타일(Style, CSS 3 선택자(Selectors), [미디어 쿼리](http://www.w3.org/TR/css3-mediaqueries/)
  - 버킷 4: 스크립트와 DOM2 HTML에 의한 [HTML](https://ko.wikipedia.org/wiki/HTML "wikilink") 테이블/형식의 가동
  - 버킷 5: Acid3 경쟁에서 나온 테스트들 (SVG\[4\], HTML, SMIL, 유니코드, ...)
  - 버킷 6: ECMA스크립트

이 테스트의 표준 규정은 각 브라우저가 기본 설정으로 테스트를 진행하기를 요구한다. 최종 결과는 100/100 의 점수와 함께, [참고 페이지](http://acid3.acidtests.org/reference.html)와 픽셀 하나도 다르지 않은 결과가 나와야 한다. 개인용 컴퓨터를 위해 개발된 브라우저의 경우, 화면의 변화가 부드러워야([애플 랩톱에](https://ko.wikipedia.org/wiki/맥북_프로 "wikilink") 준하는 성능의 환경에서 각 서브 테스트를 33 [ms](https://ko.wikipedia.org/wiki/1_E-3_s "wikilink") 안에 통과)\[5\] 하지만, 보다 뒤떨어진 환경에서의 느린 결과가 불합격을 뜻하진 않는다.\[6\]

테스트를 통과하기 위해서는 또한, 브라우저의 툴바에 특정한 [파비콘](../Page/파비콘.md "wikilink")을 표시해야한다. 하지만 이것은 Acid3 웹 서버에 있는 파비콘 그림이 아닌데, 만일 Acid3 서버에 `favicon.ico` 파일을 요청하면 [404](https://ko.wikipedia.org/wiki/HTTP_404 "wikilink") 응답을 하며 화면엔 그림의 데이터만 표시하기 때문이다. 이 테스트는 브라우저가 파비콘을 불러올 때 404 에러 코드를 정확하게 처리하면, 에러를 제대로 인식하여 특정 파비콘을 나타내게 된다.\[7\]

[섬네일](https://ko.wikipedia.org/wiki/파일:Fennec_acid3-89.png "wikilink") 1.0 알파로 테스트한 Acid3 결과. 1. 버킷 2, 4와 6은 16 개의 서브테스트를 모두 통과했고, 버킷 1과 3 은 10개 이상의 서브 테스트를, 버킷 5 는 5개 이상의 서브 테스트를 통과했음을 알 수 있다.\]\] 테스트가 실행되면서 그림에 사각형들이 추가되는데, 각 사각형의 색깔은 한 버킷 당 통과한 서브 테스트의 개수로부터 결정된다. 만일 특정 버킷에 포함된 모든 서브 테스트에 불합격했다면, 그 버킷에 해당되는 사각형은 화면에 나타나지 않을 것이다. 하나 이상의 서브 테스트에 통과하면, 사각형의 색깔은 네 단계로 변화하게 된다.

  - 1 \~ 5 개의 서브 테스트 통과: [검정](https://ko.wikipedia.org/wiki/검정 "wikilink") 사각형
  - 6 \~ 10 개의 서브 테스트 통과: [회색](https://ko.wikipedia.org/wiki/회색 "wikilink") 사각형
  - 11 \~ 15 개의 서브 테스트 통과: [은색](https://ko.wikipedia.org/wiki/은색 "wikilink") 사각형
  - 16개 서브 테스트 모두 통과: [유채색](https://ko.wikipedia.org/wiki/유채색 "wikilink") 사각형 (각각 [빨강](../Page/빨강.md "wikilink"), [주황](../Page/주황.md "wikilink"), [노랑](../Page/노랑.md "wikilink"), [연두](https://ko.wikipedia.org/wiki/연두 "wikilink"), [파랑](../Page/파랑.md "wikilink"), [보라](../Page/보라.md "wikilink") 색의 사각형)

Acid3 테스트 페이지 표시가 완료되면, 대문자 A 는 클릭이 가능한 상태가 되며, 클릭할 경우(새 창에서 보려면 Shift + 클릭) 어떤 서브 테스트가 실패했는지, 그리고 어떤 에러가 발생했는지 설명하는 경고를 볼 수 있다.

이 테스트를 정확히 수행하려면, 프로그램은 [W3C](https://ko.wikipedia.org/wiki/W3C "wikilink")에서 현재 표준으로 지정할 것으로 고려중인 [CSS 3 Text Shadows](http://www.w3.org/TR/css3-text/#text-shadow) 와 [CSS 2.x Downloadable Fonts](http://www.w3.org/TR/css3-webfonts/#font-descriptions) 지시 사항을 만족해야한다. 이것은 테스트에서 20x20 픽셀 크기의 붉은 사각형을 가려주는, "AcidAhemTest"라고 하는 자체 [트루타입](https://ko.wikipedia.org/wiki/트루타입 "wikilink") [폰트](https://ko.wikipedia.org/wiki/폰트 "wikilink")의 사용에 필요하다. 내려받아진 폰트가 표시되면 이 [글자 모양은](https://ko.wikipedia.org/wiki/자형 "wikilink"), CSS 에 의해 하얀 네모로만 표시되어, 결국 보이지 않게 된다.\[8\]

추가로, 이 테스트는 또한 [베이스64](https://ko.wikipedia.org/wiki/베이스64 "wikilink") 코드로 만들어진 그림과, 몇 가지의 더 발달된 선택자, CSS 3 색상 값([HSLA](http://www.w3.org/TR/2003/CR-css3-color-20030514/#hsla-color)), 그리고 무시되어야 할 가짜 선택자와 값들도 사용한다.

## 정식 통과한 브라우저

이미 배포된 정식판, 혹은 안정판의 테스트 결과만을 인정한다.

### 데스크톱 브라우저

<table>
<thead>
<tr class="header">
<th><p>레이아웃 엔진</p></th>
<th><p>브라우저</p></th>
<th><p>발매 일자</p></th>
<th><p>최신 버전 및 출시일</p></th>
<th><p>렌더링</p></th>
<th><p>수행능력</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/게코_(레이아웃_엔진).md" title="wikilink">게코</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/모질라_파이어폭스" title="wikilink">모질라 파이어폭스</a> 4.0[9][10]</p></td>
<td></td>
<td></td>
<td></td>
<td><p>{{?}}</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/웹키트" title="wikilink">웹키트</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/구글_크롬" title="wikilink">구글 크롬</a> 4.0.249.78[11]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/웹키트" title="wikilink">웹키트</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/사파리_(웹_브라우저)" title="wikilink">사파리</a> 4.0[12][13]</p></td>
<td></td>
<td></td>
<td></td>
<td><p>[14]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/프레스토_(레이아웃_엔진)" title="wikilink">프레스토</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/오페라_(웹_브라우저)" title="wikilink">오페라</a> 10[15]</p></td>
<td></td>
<td></td>
<td></td>
<td><p>{{?}}</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/웹키트" title="wikilink">웹키트</a></p></td>
<td><p><a href="../Page/웹_(웹_브라우저).md" title="wikilink">웹</a> 2.28.0[16]</p></td>
<td></td>
<td></td>
<td><p>{{?}}</p></td>
<td><p>{{?}}</p></td>
</tr>
</tbody>
</table>

### 모바일 브라우저

모바일 브라우저는 기준이 되는 하드웨어를 정할 수 없기 때문에 기능 수행 능력을 '평가'할 수 없다.

<table>
<thead>
<tr class="header">
<th><p>레이아웃 엔진</p></th>
<th><p>브라우저</p></th>
<th><p>발매 일자</p></th>
<th><p>렌더링</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/웹키트" title="wikilink">웹키트</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/아이리스_브라우저" title="wikilink">아이리스 브라우저</a> 1.1.4[17]</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/웹키트" title="wikilink">웹키트</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/볼트_브라우저" title="wikilink">볼트 브라우저</a> 1.6[18]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/프레스토_(레이아웃_엔진)" title="wikilink">프레스토</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/오페라_모바일" title="wikilink">오페라 모바일</a> 9.7[19]</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 통과하지 못한 브라우저

Acid3 는 처음 공개 당시 모든 웹 브라우저가 통과하지 못했기 때문에, 이에 대해 언급하는 것에 신중했다. 많은 수의 브라우저 개발 팀은 테스트 결과를 향상시키기 위해 열의를 다해 일하고 있다.

### 데스크톱 브라우저

<table>
<caption><strong>데스크톱 레이아웃 엔진의 Acid3 테스트 결과 추이</strong></caption>
<thead>
<tr class="header">
<th><p>레이아웃 엔진</p></th>
<th><p>주요 브라우저</p></th>
<th><p>Acid3 공개 당시 최신버전의 스크린샷{{-}}</p></th>
<th><p>현재 배포판의 스크린샷</p></th>
<th><p>알려진 개발 버전의 스크린샷</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/KHTML" title="wikilink">KHTML</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/캉커러" title="wikilink">캉커러</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Acid3_Konqueror_402.NEW.jpg" title="wikilink">150px</a> {{-}} 61/100 {{-}} 캉커러 4.0.2</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Konqueror_4.3b1_Acid3.png" title="wikilink">150px</a> {{-}} 89/100 {{-}} 캉커러 4.3.0</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Konqueror_4.3b1_Acid3.png" title="wikilink">150px</a> {{-}} 89/100 {{-}} 캉커러 <ref>{{웹 인용</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/트라이던트_(레이아웃_엔진).md" title="wikilink">트라이던트</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/인터넷_익스플로러" title="wikilink">인터넷 익스플로러</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Acid3_ie7.png" title="wikilink">150px</a> {{-}} 14/100 {{-}} 인터넷 익스플로러 7.0</p></td>
<td><p>{{-}} 100/100<br />
(만점이지만 부정확한 렌더링 있음) {{-}} 인터넷 익스플로러 9.0</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 모바일 브라우저

<table>
<caption><strong>Acid3 테스트의 모바일 레이아웃 엔진 진행 상황</strong></caption>
<thead>
<tr class="header">
<th><p>레이아웃 엔진</p></th>
<th><p>주요 브라우저</p></th>
<th><p>현재 배포판의 스크린샷</p></th>
<th><p>알려진 개발 버전의 스크린샷</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/웹키트" title="wikilink">웹키트</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/사파리_(웹_브라우저)" title="wikilink">모바일 사파리</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:MobileSafari_4_3_3.png" title="wikilink">150px</a> {{-}} 100/100<br />
(만점이지만 부정확한 렌더링 있음) {{-}} iOS 4.3.3</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/안드로이드_(운영_체제)" title="wikilink">안드로이드</a> 브라우저</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Android_acid3_render.png" title="wikilink">150px</a> {{-}} 93/100 {{-}} 안드로이드 2.3 {{-}} <a href="https://ko.wikipedia.org/wiki/파일:Android3_Acid3.png" title="wikilink">150px</a> {{-}} 100/100<br />
(만점이지만 부정확한 렌더링 있음) {{-}} 안드로이드 3.1</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/블랙베리_(스마트폰)" title="wikilink">블랙베리</a> 브라우저</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:BlackBerry6_ACID3.jpg" title="wikilink">150px</a> {{-}} 100/100<br />
(만점이지만 부정확한 렌더링 있음) {{-}} 블랙베리 OS 6</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/바다_(운영_체제)" title="wikilink">바다</a> 브라우저</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Acid3test_on_bada_webkit_dolphin.jpg" title="wikilink">150px</a> {{-}} 98/100 {{-}} 바다 OS 1.0.2</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/S60용_웹_브라우저" title="wikilink">노키아 미니 맵 브라우저</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Acid3_S60_5th_Edition.png" title="wikilink">150px</a> {{-}} 47/100 {{-}} S60 5번째 판</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/스카이파이어_(웹_브라우저)" title="wikilink">스카이파이어</a></p></td>
<td><p>{{-}} 100/100<br />
(만점이지만 부정확한 렌더링 있음) {{-}} 스카이파이어 2.0</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/webOS#웹_브라우저" title="wikilink">웹OS 브라우저</a></p></td>
<td><p>{{-}} 92/100 {{-}} webOS 1.4</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/아이리스_브라우저" title="wikilink">아이리스 브라우저</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Iris-wm-acid3-100.png" title="wikilink">150px</a> {{-}} 100/100<br />
(만점이지만 부정확한 렌더링 있음) {{-}} 아이리스 브라우저 1.1.4</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/프레스토_(레이아웃_엔진)" title="wikilink">프레스토</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/오페라_미니" title="wikilink">오페라 미니</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Opera_Mini_5_beta_2_Acid_3_test.png" title="wikilink">150px</a> {{-}} 98/100 {{-}} 오페라 미니 5</p></td>
<td><p>없음</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/게코_(레이아웃_엔진).md" title="wikilink">게코</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파이어폭스_모바일" title="wikilink">모질라 파이어폭스 모바일</a></p></td>
<td><p>97/100 {{-}} 모질라 파이어폭스 모바일 4</p></td>
<td><p>없음</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/마이크로B" title="wikilink">마이크로B</a></p></td>
<td><p>94/100</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/트라이던트_(레이아웃_엔진).md" title="wikilink">트라이던트</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/인터넷_익스플로러_모바일" title="wikilink">인터넷 익스플로러 모바일</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Internet_Explorer_Mobile_9_Acid3.png" title="wikilink">150px</a> {{-}} 95/100 {{-}} 인터넷 익스플로러 모바일 9</p></td>
<td><p>없음</p></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [Acid1](https://ko.wikipedia.org/wiki/Acid1 "wikilink")
  - [Acid2](https://ko.wikipedia.org/wiki/Acid2 "wikilink")
  - [레이아웃 엔진](https://ko.wikipedia.org/wiki/레이아웃_엔진 "wikilink")

## 각주

## 외부 링크

  - [Acid3 테스트](http://acid3.acidtests.org/)
  - [Acid3 테스트 (참고 페이지)](http://acid3.acidtests.org/reference.html)
  - [웹 표준 프로젝트의 Acid3 테스트](http://www.webstandards.org/action/acid3/)
  - [Acid3 테스트 이후 출시 버전](http://ln.hixie.ch/?start=1206565203&count=1)

[분류:Acid 테스트](https://ko.wikipedia.org/wiki/분류:Acid_테스트 "wikilink") [분류:웹 디자인](https://ko.wikipedia.org/wiki/분류:웹_디자인 "wikilink")

1.
2.
3.
4.
5.
6.  [Acid3 Browser Test - The Web Standards Project(Acid3 브라우저 테스트 - 웹 표준 프로젝트)](http://www.webstandards.org/action/acid3/). 확인일자 2009-09-03.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.