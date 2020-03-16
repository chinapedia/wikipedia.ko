> This article is converted from Wikipedia: [DHTML](https://ko.wikipedia.org/wiki/DHTML).


**DHTML**(Dynamic HTML; 동적 HTML)은 정적 [마크업 언어인](../Page/마크업_언어.md "wikilink") [HTML](../Page/HTML.md "wikilink")과 클라이언트 기반 스크립트 언어([자바스크립트](../Page/자바스크립트.md "wikilink") 같은) 그리고 스타일 정의 언어인 [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink")를 조합하여 대화형 [웹 사이트를](https://ko.wikipedia.org/wiki/웹_사이트 "wikilink") 제작하는 기법을 의미한다.

DHTML은 [웹 브라우저](../Page/웹_브라우저.md "wikilink") 상에서 동작하는 응용 프로그램을 제작하는 데에도 쓰인다. 예를 들어 간편한 내비게이션을 위해 대화형 [폼](https://ko.wikipedia.org/wiki/폼_\(문서\) "wikilink")(form)을 제작하거나, [전자 학습에](../Page/전자_학습.md "wikilink") 사용되는 대화형 실습장을 만드는 데 이용될 수 있다. 완전히 브라우저에 포함되어, 데이터베이스와 같은 서버측 지원이 없이 동작하는 DHTML 응용 프로그램을 때로 [SPA](https://ko.wikipedia.org/wiki/SPA "wikilink")(Single Page Applications; 단일 페이지 응용 프로그램)라 부른다.

경쟁 기술로는 애니메이션을 위한 [어도비 플래시나](../Page/어도비_플래시.md "wikilink") [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [AJAX](https://ko.wikipedia.org/wiki/AJAX "wikilink"), [애플릿](../Page/자바_애플릿.md "wikilink"), [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink") 등이 있다(SVG는 아직까지 주요 웹 브라우저에서 잘 지원되지 않는다).

DHTML의 단점으로는 브라우저마다 기술 지원에 대한 편차가 있기 때문에 개발과 [디버그](../Page/디버그.md "wikilink") 작업이 힘들다는 것과, 화면 크기가 다양하기 때문에 제한된 브라우저와 화면 크기 조합에만 최적화가 가능하다는 점이다. 최신 브라우저([인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") 5.0+, [넷스케이프](../Page/넷스케이프_\(웹_브라우저\).md "wikilink") 6.0+, [오페라](../Page/오페라_\(웹_브라우저\).md "wikilink") 7.0+)에서의 개발은 공통된 [DOM](https://ko.wikipedia.org/wiki/DOM "wikilink") 덕분에 이전보다 간편해졌다.

## 예

### 일반적인 DHTML의 예

``` html5
<!doctype html>
<html lang="en">
     <head>
          <meta charset="utf-8">
          <title>DHTML example</title>
     </head>
     <body>
          <div id="navigation"></div>

          <script>
               var init = function () {
                    myObj = document.getElementById("navigation");
                    // ... manipulate myObj
               };
               window.onload = init;
          </script>

          <!--
          Often the code is stored in an external file; this is done
          by linking the file that contains the JavaScript.
          This is helpful when several pages use the same script:
          -->
          <script src="myjavascript.js"></script>
     </body>
</html>
```

### 텍스트 추가 블록 표시

``` html5
<!doctype html>
<html lang="en">
     <head>
          <meta charset="utf-8">
          <title>Using a DOM function</title>
          <style>
               a {background-color:#eee;}
               a:hover {background:#ff0;}
               #toggleMe {background:#cfc; display:none; margin:30px 0; padding:1em;}
          </style>
     </head>
     <body>
          <h1>Using a DOM function</h1>

          <h2><a id="showhide" href="#">Show paragraph</a></h2>

          <p id="toggleMe">This is the paragraph that is only displayed on request.</p>

          <p>The general flow of the document continues.</p>

          <script>
               changeDisplayState = function (id) {
                    var d = document.getElementById('showhide'),
                         e = document.getElementById(id);
                    if (e.style.display === 'none' || e.style.display === '') {
                         e.style.display = 'block';
                         d.innerHTML = 'Hide paragraph';
                    }
                    else {
                         e.style.display = 'none';
                         d.innerHTML = 'Show paragraph';
                    }
               };
               document.getElementById('showhide').onclick = function () {
                    changeDisplayState('toggleMe');
                    return false;
               };
          </script>
     </body>
</html>
```

## 외부 링크

  - [QuirksMode](http://www.quirksmode.org/) - 여러 운영체제에서 동작하는 DHTML 코드 작성에 대한 예제와 설명 등을 포괄한 사이트
  - [DHTML 데모](https://web.archive.org/web/20050713024411/http://www.dhteumeuleu.com/)

[분류:HTML](https://ko.wikipedia.org/wiki/분류:HTML "wikilink")