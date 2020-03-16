> This article is converted from Wikipedia: [PhantomJS](https://ko.wikipedia.org/wiki/PhantomJS).


**PhantomJS**(팬텀JS)는 웹 페이지 상호작용을 자동화하기 위해 사용되는 [헤드리스 브라우저이다](https://ko.wikipedia.org/wiki/헤드리스_브라우저 "wikilink"). PhantomJS는 자동화된 탐색, 스크린샷, 사용자 동작, [어서션](https://ko.wikipedia.org/wiki/어서션 "wikilink")을 가능케 하므로 [지속적 통합](../Page/지속적_통합.md "wikilink") 환경과 같은 [헤드리스 시스템](https://ko.wikipedia.org/wiki/헤드리스_시스템 "wikilink") 내에서 브라우저 기반 유닛 테스트를 수행하기 위한 도구로 이용이 가능하다.

PhantomJS는 [사파리와](../Page/사파리_\(웹_브라우저\).md "wikilink") [구글 크롬과](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink") 유사한 브라우징 환경을 갖춘 [웹킷](../Page/웹킷.md "wikilink") 기반이다. [BSD 허가서로](../Page/BSD_허가서.md "wikilink") 출시된 [오픈 소스 소프트웨어이다](../Page/오픈_소스_소프트웨어.md "wikilink").\[1\]

## 역사

PhantomJS는 수년 간의 개발 끝에 Ariya Hidayat에 의해 2011년 1월 23일 출시되었다.\[2\]

공개 프로젝트의 첫 커밋은 2011년이었다.\[3\] 이 프로젝트는 2010년 12월 26일부터 현재까지 매주 어느 정도의 기여를 통해 유지되고 있다.\[4\] 2015년 2월 5일 기준으로 이 프로젝트의 오픈 소스 코드 저장소는 770명에 의해 주시되고 있으며 107명의 기여자에 의해 기여되었다. 또, 2015년 2월 5일 기준으로 1376개의 개방된 이슈와 1252개의 닫힌 이슈를 보유하고 있다.

## 사용법

PhantomJS 자바스크립트 API를 사용하여 웹 페이지를 열고 스크린샷을 찍고 사용자 동작을 실행하고 페이지 컨텍스트 내에서 자바스크립트를 삽입하여 실행할 수 있다. 이를테면 다음의 코드는 위키백과를 열고 로드할 때 파일로 스크린샷을 저장하고 끝낸다.

``` javascript
console.log('웹 페이지를 로드하는 중');
var page = require('webpage').create();
var url = 'https://ko.wikipedia.org/';
page.open(url, function (status) {
  console.log('페이지를 로드함');
  page.render('wikipedia.org.png');
  phantom.exit();
});
```

## 같이 보기

  - [모질라 파이어폭스](../Page/모질라_파이어폭스.md "wikilink")
  - [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink")
  - [SlimerJS](https://ko.wikipedia.org/wiki/SlimerJS "wikilink")
  - [TrifleJS](https://ko.wikipedia.org/wiki/TrifleJS "wikilink")
  - [WebKit](../Page/웹킷.md "wikilink")

## 각주

## 외부 링크

  -
[분류:C++ 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++_소프트웨어 "wikilink") [분류:웹 브라우저](https://ko.wikipedia.org/wiki/분류:웹_브라우저 "wikilink") [분류:크로스 플랫폼 웹 브라우저](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_웹_브라우저 "wikilink") [분류:포터블 소프트웨어](https://ko.wikipedia.org/wiki/분류:포터블_소프트웨어 "wikilink") [분류:웹키트 기반 소프트웨어](https://ko.wikipedia.org/wiki/분류:웹키트_기반_소프트웨어 "wikilink") [분류:2011년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2011년_소프트웨어 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")

1.
2.
3.
4.