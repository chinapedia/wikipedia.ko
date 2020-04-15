> This article is converted from Wikipedia: [Processing.js](https://ko.wikipedia.org/wiki/Processing.js).


**Processing.js**는 시각화, 이미지 및 대화 형 결과를 만들도록 설계된 프로그래밍 언어인 [프로세싱](../Page/프로세싱_\(프로그래밍_언어\).md "wikilink")(Processing)이 JavaScript로 [포팅된](../Page/이식_\(컴퓨팅\).md "wikilink") 버전이다. 웹 브라우저는 이것를 통해서 [Java 애플릿이나](../Page/자바_애플릿.md "wikilink") [Flash](../Page/어도비_플래시.md "wikilink") [플러그인](../Page/플러그인.md "wikilink")을 사용하지 않고도 애니메이션, 비주얼 애플리케이션, 게임 및 기타 그래픽등 풍부한 컨텐츠를 표시 할 수 있다.\[1\]\[2\]

Processing.js는 원래 Processing 개발자와 기존 코드가 웹에서 수정되지 않은 상태로 작동 할 수 있도록하기 위해 만들어졌다.

Processing.js는 [JavaScript](https://ko.wikipedia.org/wiki/JavaScript "wikilink")를 사용하여 [HTML](../Page/HTML.md "wikilink") 캔버스 요소에서 2D 및 3D 콘텐츠를 렌더링하며 이 요소를 구현한 브라우저 ([파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink"), [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink"), [사파리](../Page/사파리_\(웹_브라우저\).md "wikilink"),[오페라](../Page/오페라_\(웹_브라우저\).md "wikilink"), 등)에서 지원된다.

Processing.js의 개발은 [존 레식](../Page/존_레식.md "wikilink")(John Resig)에 의해 시작되어 2008 년 첫 번째 릴리스 이후 [세네카 컬리지의](https://ko.wikipedia.org/wiki/세네카_컬리지 "wikilink") 학생들에 의해 진행되었다. 한 팀의 팀이 Processing.js 포팅(porting)를 완성하고 900 개 이상의 버그를 수정하고 12 개의 릴리스를 출시했으며 그 과정에서 활발한 커뮤니티가 만들어졌다. 이 프로젝트는 David Humphrey, Al MacDonald 및 Corban Brook이 이끄는 [모질라재단](https://ko.wikipedia.org/wiki/모질라재단 "wikilink")(Mozilla Foundation)과 [세네카 컬리지](https://ko.wikipedia.org/wiki/세네카_컬리지 "wikilink")(Seneca College) 간의 파트너십을 통해 수행되었다.

## 수학 프로그래밍에서의 활용

[300px](https://ko.wikipedia.org/wiki/파일:LogisticMap_processing_js001.png "wikilink")

[파이겐바움 상수가](../Page/파이겐바움_상수.md "wikilink") 얻어지는 대표적인 [비선형](../Page/비선형.md "wikilink")(Non-linear) \(f(x)=a-x^2\)의 processing.js를 사용한 [로지스틱 맵](../Page/로지스틱_사상.md "wikilink") 표현

## 소스 코드

\(f(x)=a-x^2\) [로지스틱 맵](../Page/로지스틱_사상.md "wikilink") 의 processing.js를 사용한 [자바스크립트](../Page/자바스크립트.md "wikilink") 소스 코드

``` javascript
var canvas = document.getElementById("canvas");

var sketchProc=function(processingInstance){ with (processingInstance){

size(400, 400);
frameRate(30);


background(200,100,100);
fill(255,255,255);



for(var a=0;a<10;a+=0.001){

var x=0.1;

for(var n=0;n<1000;n++){

x=a-(x*x);

if(n>900){

point(a*200,200-x*100);

}

}

}



}};

var processingInstance = new Processing(canvas, sketchProc);
```

## 함께보기

  - [프로세싱](../Page/프로세싱_\(프로그래밍_언어\).md "wikilink")
  - [JQuery](../Page/JQuery.md "wikilink")

## 참고

  - [공식processing.js 버전 다운로드](http://processingjs.org/download/archived.html)
  - [로지스틱 맵](https://web.archive.org/web/20170914125200/https://www.khanacademy.org/computer-programming/logistic-map/1060730277)

## 각주

## 외부 링크

  -
[분류:프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:프로그래밍_언어 "wikilink") [분류:자바스크립트로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바스크립트로_작성된_자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.  [칸 아카데미](https://ko.wikipedia.org/wiki/칸_아카데미 "wikilink")-[Finn the Baby Raccoon](https://www.khanacademy.org/computer-programming/finn-the-baby-raccoon/5268411358838784)
2.  [테트리스 버전](https://www.khanacademy.org/computer-programming/highly-addictive-tetris/6749811916341248) (회전 ↑방향키)