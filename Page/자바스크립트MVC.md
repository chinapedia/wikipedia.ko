> This article is converted from Wikipedia: [MVC](https://ko.wikipedia.org/wiki/MVC).


**자바스크립트MVC**(JavaScriptMVC)는 [제이쿼리](https://ko.wikipedia.org/wiki/제이쿼리 "wikilink")와 [OpenAjax](https://ko.wikipedia.org/wiki/OpenAjac_Alliance "wikilink") 기반의 오픈 소스 [리치 인터넷 애플리케이션](../Page/리치_인터넷_애플리케이션.md "wikilink") 프레임워크이다. [모델-뷰-컨트롤러](../Page/모델-뷰-컨트롤러.md "wikilink") 구조를 지원하는 라이브러리와 테스트, 배치를 위한 도구들이 있다. 서버 컴포넌트에 의존하지 않기 때문에 [ASP.NET](../Page/ASP.NET.md "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [펄](../Page/펄.md "wikilink"), [PHP](../Page/PHP.md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"), [루비와](../Page/루비_\(프로그래밍_언어\).md "wikilink") 같은 웹 서비스 인터페이스 및 서버 사이드 언어와 결합할 수 있다.

## 역사

자바스크립트MVC의 최초 릴리스는 2008년 5월에 게시되었다. 자바스크립트MVC 2.0은 2009년 6월에 안정판이 되었으며 주로 코드 크기를 작은 상태로 유지하고 고유한 기능에 집중할 수 있게 하기 위해 jQuery에 직접 기반을 두고 있다. 버전 3.0은 2010년 12월에 출시되었다. 자바스크립트MVC에서 추출되는 MVC 파트인 [CanJS](https://ko.wikipedia.org/wiki/CanJS "wikilink")는 2012년 4월에 출시되었다. 2015년 5월, 자바스크립트MVC는 확장된 기능 집합과 스코프와 더불어 DoneJS로 리브랜딩되었다.

## 컨트롤러

컨트롤러는 적절한 이벤트가 발생할 때 호출되는 함수의 목록이다. 함수 이름은 함수가 호출될 때의 설명을 제공한다. 올바른 방법으로 함수들의 이름을 지정해 줌으로써 컨트롤러는 이들을 Actions로 인지하여 이들을 올바르게 후킹하는데, 이를테면 다음과 같다:

``` javascript
 $.Controller('TodosController',{
   ".todo mouseover": function(el, ev){
     el.css("backgroundColor","red")
   },
   ".todo mouseout": function(el, ev){
     el.css("backgroundColor","")
   },
   "#create_todo click" : function(){
     this.find("ol").append("New Todo");
   }
 });
```

컨트롤러는 [OpenAjax](https://ko.wikipedia.org/wiki/OpenAjax_Alliance "wikilink") 이벤트도 관리할 수 있는데, 이를테면 다음과 같다:

``` javascript
 $.Controller('TodosController',{
   "main.test subscribe": function(ev, publisherData){
     // TODO: do something
   },
   "other.event subscribe": function(ev, publisherData){
     // TODO: do something
   }
 });
```

## 뷰

자바스크립트MVC는 EJS 템플릿을 사용하여 컨트롤러 내에서 HTML 데이터를 렌더링하고 [DOM에](../Page/문서_객체_모델.md "wikilink") 주입시킨다. 문법은 [ERuby](https://ko.wikipedia.org/wiki/ERuby "wikilink")의 영향을 받았으며 PHP나 그 밖의 서버 사이드 템플릿 엔진과 유사하다.

이를테면 파일 "test.ejs" ( data = \[ "Hello", "World" \] )는:

``` html4strict
<ul>
<% for( var i=0, len = data.length; i < len; i++ ) { %>
 <li><%= data[i] %></li>
<% } %>
</ul>
```

다음의 출력을 만들어낸다:

``` html4strict
<ul>
 <li>Hello</li>
 <li>World</li>
</ul>
```

## 모델

모델 클래스는 애플리케이션의 데이터 계층을 조직하기 위한 기초적인 기능을 제공한다.

``` javascript
 $.Model('Todo',{
  findAll: '/todos',
  findOne: '/todos/{id}',
  create: '/todos',
  update: '/todos/{id}',
  destroy : '/todos/{id}'
 },{});
```

## 테스트

자바스크립트MVC는 기능 테스트 외에도 모델을 위한 고전적인 단위 테스트를 지원하는 포괄적인 테스트 플러그인이 포함되어 있으며 이벤트 구동 아키텍처를 다루는데 필수적이다. 테스트는 셀레늄을 사용하여 Rhino를 가지고 명령 줄에서 수행하거나 통합 테스트 콘솔 팝업 창을 가지고 개발 중에 수행할 수 있다.

## 각주

## 외부 링크

  -
  - [GitHub Repo](https://github.com/bitovi/javascriptmvc)

  - [Old Project page on Google Code](http://code.google.com/p/javascriptmvc/)

[분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:Ajax](https://ko.wikipedia.org/wiki/분류:Ajax "wikilink")