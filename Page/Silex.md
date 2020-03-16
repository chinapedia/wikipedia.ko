> This article is converted from Wikipedia: [Silex](https://ko.wikipedia.org/wiki/Silex).


**Silex**는 [PHP](../Page/PHP.md "wikilink")로 개발된 마이크로 [웹 프레임워크이며](../Page/웹_프레임워크.md "wikilink") [심포니](../Page/심포니_\(웹_프레임워크\).md "wikilink"), [트위그](https://ko.wikipedia.org/wiki/트위그 "wikilink"), [독트린에](https://ko.wikipedia.org/wiki/독트린_\(PHP\) "wikilink") 기반을 둔다. [MIT 라이선스이다](../Page/MIT_허가서.md "wikilink").

Silex의 일반 목적은 가능한 가볍게 함으로써 Silex 기반을 확장하고 기능을 추가하는 일을 쉽게 하는 것이다.\[1\] Silex는 소형 웹 애플리케이션(예: [REST API](../Page/REST.md "wikilink"))의 제작을 위해 사용할 수 있는데, 이는 마이크로 프레임워크를 위한 주요 케이스이지만,\[2\] Silex는 풀 스택 [MVC](../Page/모델-뷰-컨트롤러.md "wikilink") 프레임워크로 확장이 가능하다.\[3\]

Silex는 2가지 버전으로 사용할 수 있다: 'fat', 'slim'.\[4\] 이 둘의 차이점은 fat 버전의 경우 기능이 완전하며 [데이터베이스 추상화](https://ko.wikipedia.org/wiki/데이터베이스_추상화_계층 "wikilink"), [탬플릿 엔진](https://ko.wikipedia.org/wiki/탬플릿_엔진 "wikilink"), 다양한 심포니 컴포넌트를 포함하고 있는 반면 slim 버전은 기초적인 라우팅 엔진 정도만 포함하고 있다.

Silex는 2018년 6월 EOL(end-of-life) 처리되어 사람들에게 심포니를 대신 사용할 것을 권고하고 있다.\[5\].

## 역사

Silex는 심포니 프레임워크의 개발자 Fabien Potencier, 그리고 Igor Wiedler에 의해 개발되었다.\[6\] '웹 프레임워크 PoC' 성격으로 2010년 9월 16일 처음 출시되었다.\[7\]

Silex는 현재 가장 잘 알려진 PHP 마이크로 프레임워크 가운데 하나로서\[8\] 대체적으로 마이크로 프레임워크 비교를 위한 벤치마크에서 가장 빠른 것들 가운데 하나로 속해있다.\[9\]\[10\]

## 예

다음의 코드는 [Hello World\!를](https://ko.wikipedia.org/wiki/Hello_World! "wikilink") 출력하는 단순한 웹 애플리케이션을 보여준다.

``` php
$app = new Silex\Application();

$app->get('/', function() use($app) {
    return 'Hello World!';
});

$app->run();
```

## 같이 보기

  - [심포니 (웹 프레임워크)](../Page/심포니_\(웹_프레임워크\).md "wikilink")

## 각주

## 외부 링크

  -
[분류:PHP로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:PHP로_작성된_자유_소프트웨어 "wikilink") [분류:PHP 프레임워크](https://ko.wikipedia.org/wiki/분류:PHP_프레임워크 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:웹 프레임워크](https://ko.wikipedia.org/wiki/분류:웹_프레임워크 "wikilink")

1.
2.
3.
4.  <https://silex.symfony.com/download>
5.  <https://github.com/silexphp/Silex>
6.
7.
8.
9.
10.