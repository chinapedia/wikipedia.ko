> This article is converted from Wikipedia: [PHP](https://ko.wikipedia.org/wiki/PHP).


**PHP**(\[1\])는 프로그래밍 언어의 일종이다. 원래는 동적 웹 페이지를 만들기 위해 설계되었으며 이를 구현하기 위해 PHP로 작성된 코드를 HTML 소스 문서 안에 넣으면 PHP 처리 기능이 있는 웹 서버에서 해당 코드를 인식하여 작성자가 원하는 웹 페이지를 생성한다. 근래에는 PHP 코드와 HTML을 별도 파일로 분리하여 작성하는 경우가 일반적이며, PHP 또한 웹서버가 아닌 php-fpm(PHP FastCGI Process Manager)을 통해 실행하는 경우가 늘어나고 있다.

또한 PHP는 명령 줄 인터페이스 방식의 자체 인터프리터를 제공하여 이를 통해 범용 프로그래밍 언어로도 사용할 수 있으며 그래픽 애플리케이션을 제작할 수도 있다.

많은 서버 측 [오픈 소스](../Page/오픈_소스.md "wikilink") 소프트웨어는 PHP로 구현되었다. PHP를 바탕으로 하는 프로그램 중 대표적인 예로 블로깅 도구 [워드프레스](https://ko.wikipedia.org/wiki/워드프레스 "wikilink")와 위키백과를 구동시키는 [미디어위키](../Page/미디어위키.md "wikilink")를 들 수 있다. [대한민국](../Page/대한민국.md "wikilink")의 PHP 기반 [BBS는](../Page/전자_게시판.md "wikilink") [제로보드](https://ko.wikipedia.org/wiki/제로보드 "wikilink"), [그누보드](../Page/그누보드.md "wikilink"), [XpressEngine](../Page/XpressEngine.md "wikilink") \[웹솔루션, 랭크업\]등이 있다.

PHP는 [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 [ASP.NET](../Page/ASP.NET.md "wikilink"), [비주얼 베이직](../Page/비주얼_베이직.md "wikilink"), [매크로미디어](../Page/매크로미디어.md "wikilink")의 [콜드퓨전](https://ko.wikipedia.org/wiki/매크로미디어_콜드퓨전 "wikilink"), [오라클의](../Page/오라클_\(기업\).md "wikilink") [자바나](../Page/자바_\(프로그래밍_언어\).md "wikilink") 오픈 소스 커뮤니티의 [파이썬](../Page/파이썬.md "wikilink"), [펄](https://ko.wikipedia.org/wiki/펄 "wikilink"), [루비에](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink") 대한 대안으로 생각될 수 있다.

PHP는 텍스트, 특히 [HTML](../Page/HTML.md "wikilink")의 처리에 강점을 가지고 있다. [URL](../Page/URL.md "wikilink")의 [파싱](https://ko.wikipedia.org/wiki/파싱 "wikilink")이나 폼 처리, [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 등이 그 한 예이다. 또한 다양한 데이터베이스를 지원하므로 데이터베이스와 사용자간의 다리 역할도 잘 수행한다.

PHP는 PHP 사용 허가서의 규정을 따라 릴리즈된 자유 소프트웨어이다. 그러나 PHP 사용 허가서는 PHP라는 단어의 사용에 제한을 두는 규정을 가지고 있기 때문에 GNU 일반 공중 사용 허가서와 호환되지 않는다.

## 역사

PHP는 1995년 [라스무스 러도프가](../Page/라스무스_러도프.md "wikilink") 처음 만든 것으로, 그 뒤로 개발이 계속되어 오늘날에까지 이르게 되었다.\[2\]

### PHP 1.0

1995년 6월 8일 발표 라스 매스·라드후가 개발. 초기는 펄로 작성된 스크립트였지만, 그 후 C 언어로 고쳐 작성된 PHP (Personal Home Page Tools)가 된다.

### PHP Version 2 (PHP/FI)

1996년 4월 16일 발표. FI(Form Interpreter, SQL이 만든 DBMS 도구)가 통합되어 1997년에 PHP/FI2.0 이 된다. 정식명칭은 "Personal Home Page Construction Kit/Form Interpreter"이다.

### PHP 3.0

1998년 6월 6일 발표. PHP/FI를 기반으로, 앤디·가트만즈와 제이브·스라스키에 의해 PHP3(PHP:Hypertext Preprocessor)로 업데이트되었다.

### PHP 4.0.0

2000년 5월 22일 발표. PHP3 를 큰 폭으로 기능을 확장하고. Zend 엔진을 도입하였다.

### PHP 4.1.0

2001년 12월 10일 발표. 슈퍼 전역 변수가 추가된다.

### PHP 4.2.0

2002년 4월 22일 발표. register_globals의 초기값이 Off로 변경된다.

### PHP 4.3.0

2002년 12월 27일 발표. [명령 줄 인터페이스가](../Page/명령_줄_인터페이스.md "wikilink") 추가된다.

### PHP 4.4.0

2005년 7월 11일 발표. 같은 날 PHP4의 지원을 2007년 12월 31일에 종료한다고 고지했다. 중대한 보안문제에 관한 수정만, 2008년 8월 8일까지 계속되어 그 후 모든 지원을 종료했다.

### PHP 5.0.0

2005년 7월 13일 발표. 의사적인 객체 지향이 한층 강화됨과 동시에 클래스 라이브러리로서 SPL가 지원되었다. 또, SQLite 가 표준으로 장착되게 되었다. Zend 엔진 2.0을 도입했다.

### PHP 5.1.0

2005년 11월 24일 발표. 실행 속도가 개선되고 PDO 확장 기능이 추가된다.

### PHP 5.2.0

2006년 11월 2일 발표. 확장 모듈에 필터(Filter)가 기본으로 추가된다.

### PHP 5.3.0

2009년 6월 30일 발표. 아래의 기능이 추가되었다.

  - 이름공간 (Namespace)
  - 지연 정적 바인딩(Late static bindings)
  - goto
  - 클로저(Native closures)
  - ?: 연산자
  - [가비지 컬렉션](https://ko.wikipedia.org/wiki/가비지_컬렉션 "wikilink")(garbage collection)

### PHP 5.4.0

2012년 3월 1일 발표. 단일 상속의 한계를 없앤 트레이트와 짧은 배열 구문이 추가되었다.

### PHP 5.5.0

2013년 6월 20일 발표. 아래의 기능들이 추가 또는 변경되었다.

  - 제너레이터(Generators)와 코루틴(coroutines)
  - finally 키워드
  - 강화된 패스워드 해슁 함수
  - 배열과 문자열의 디레퍼런싱
  - 상수 클래스명 ::class
  - empty() 함수가 수식을 지원
  - foreach 내 이터레이터(Interator)로 논스칼라(non-scalar) 사용
  - foreach 구문에 list() 사용
  - op코드 캐시를 위한 Zend OPcache

### PHP 5.6.0

2014년 8월 28일 발표. 아래의 기능들이 추가되었다.

  - 선언에 상수 표현식 지원
  - 가변길이 인수에 대한 문법 (...$args)
  - 매개변수 해체(argument unpacking)
  - 거듭제곱 연산자 (\*\*)
  - 추가적인 use 문 (use function, use const)
  - SAPI 모듈을 위한 새로운 phpdbg 디버거

### PHP 7.0.0

2015년 12월 3일 공개되었다. 특징은 다음과 같다.

  - 성능 향상 - PHP 5.6 보다 두배 이상 빠른 속도
  - 메모리 사용률이 현저히 감소
  - 추상 구문 트리(Abstract Syntax Tree)
  - 일관된 64비트 지원(Consistent 64-bit support)
  - 향상된 예외 상속(Improved Exception hierarchy)
  - 많은 치명적 에러들이 예외로 전환 됨
  - 보안 난수 발생기(Secure random number generator)
  - 오래 됐거나 지원하지 않는 SAPI와 확장 지원 중단
  - Null 병법 연산자(The null coalescing operator (??))
  - 리턴 값, 스칼라 타입 정의
  - 익명 클래스(Anonymous Classes)
  - Zero cost asserts

## 예제

다음은 예전에 코미디 프로그램에서 유행했던, 빛나리의 타잔 노래 가사를 출력해주는 코드이다. 이와 같이 PHP 구문은 일반적인 [HTML](../Page/HTML.md "wikilink") 문서에 삽입되어 동작하게 되어 있으며, 여기서는 \<?php \~ ?\> 사이의 내용이 PHP 코드로 해석된다.\[3\]

``` html+php numberLines
<html>
    <head>
        <title>php example </title>
    </head>
    <body>
        <h1>빛나리의 타잔 주제가</h1>
        <p>
            <?php
                $price = 10;
                $limit = 10000;

                while($price < $limit) {
                    echo '타잔이 '.$price.'원짜리 팬티를 입고,<br />'."\r\n";
                    $price=$price+10;
                    echo $price.'원짜리 칼을 차고 노래를 한다. 아~~!<br />'."\r\n";
                }
            ?>
        </p>
    </body>
</html>
```

또한, 간단한 템플릿 기능도 지원한다. 다만 이는 언어의 기능이라기보다는 하나의 트릭에 가까우며, 로직과 디자인이 완전히 분리되지 않는 문제점이 있다. 따라서 본격적인 템플릿 기능에는 [Smarty](https://ko.wikipedia.org/wiki/Smarty "wikilink") 등의 전문 [템플릿 엔진이](https://ko.wikipedia.org/wiki/템플릿_엔진 "wikilink") 많이 사용된다. 다음은 템플릿을 써서 비슷한 결과를 출력하는 PHP 코드이다. ([HTML](../Page/HTML.md "wikilink") 생성물은 위와 다르지만 화면 출력되는 모습은 같다.)

``` html+php numberLines
<?php
    $price = 10;
    $limit = 10000;
?>
<html>
    <head>
        <title>빛나리의 타잔 주제가</title>
    </head>
    <body>
        <h1>빛나리의 타잔 주제가</h1>
        <p>
            <?php
                while($price < $limit):
            ?>
            타잔이 <?= $price ?>원짜리 팬티를 입고,<br />
            <?PHP $price += 10; ?>
            <?= $price + 10 ?>원짜리 칼을 차고 노래를 한다. 아~~!<br />
            <?php
                endwhile;
            ?>
        </p>
    </body>
</html>
```

## 문법

근본적으로, PHP의 문법은 C스타일을 따른다.

### C언어와 다른 점

  - 변수는 $기호가 앞에 붙은 단어로 나타내며 함수는 *함수 이름(매개변수)*의 형식으로 나타낸다.
  - 함수를 선언할 때에는 `function`이라는 키워드를 앞에 붙여야 한다.
  - .(Dot) 연산자는 *문자열 결합 연산자*이며, 구조체 참조 연산자는 `->`로 통일된다.
  - 포인터를 제공하지 않으며 기본 매개변수 값은 값에 의한 전달(Call by value)이다.
  - 그 외 class 관련 문법이 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")과 다르다.

PHP4와 PHP5는 객체 문법에 차이를 보이고 있으므로 주의할 필요가 있다.

## 장점

PHP의 장점은 기존까지 존재해 왔던 언어에 비해 \`직관적\` 이라는 것이었다. 현재는 이런 인기 후, 유사하거나 더욱 개성이 강한 스크립트 언어들이 '웹 개발'을 위해 태어나게 된다.\[4\]

## 특징

자바나 C 언어에서 접근하려면 여러 Include 등을 통해야 했던 작업들이 '그냥 존재' 한다. 그래서 '그냥 적어 놓기만' 하면 작동을 한다. 즉 작성 코드의 양이 현저히 적다는 것이다. 그래서 직관적인 코드작성을 가능하게 하고 이것은 소스코드를 '절차적 프로그램 코드'에 가깝도록 만든다. 현재의 PHP는 절차적인 형태에서 '구조적 (클래스- Class)' 프로그램 작성이 가능한 상태로 진화된 상황이고 이런 진화하에서 Drupal, PHPbb, Wordpress 등의 거대한 프로그램들이 연이어 출시할 수 있게 되었다.

## 비판

PHP의 소스가 점점 방대해지고 구조적이 되면서 기존의 PHP가 추구했던 '간결함의 추구'라는 사상은 어떻게 되버리는 것인가라는 비판도 있었다. 그러나 웹의 역사를 보면 알 수 있듯이 웹문서가 초창기 보다 '다채롭고' , '복잡하며', '보다 많은 내용을 담으려 하고', 마우스나 키보드를 사용하여 보다 다양한 입력과, 움직임\[5\]을 첨가했기 때문에 이 PHP의 활용은 사용자의 기호에 달렸다고 볼 수 있다.

## PHP로 작성되어 출시된 프로그램들

PHP는 기존에, 사람들이 생각해오지 않았던 방향으로도 발전해가고 있었다. 웹으로 구현되리라 생각해오지 않았던 ERP, CRM 등의 경영에 관련한 프로그램이 개발하고 있다.\[6\] PHP로 작성되어 출시된 프로그램은 [워드프레스](https://ko.wikipedia.org/wiki/워드프레스 "wikilink"), [XpressEngine](../Page/XpressEngine.md "wikilink"), [태터툴즈](https://ko.wikipedia.org/wiki/태터툴즈 "wikilink"), [PHPbb](https://ko.wikipedia.org/wiki/PHPbb "wikilink"), [드루팔](https://ko.wikipedia.org/wiki/드루팔 "wikilink"), [제로보드](https://ko.wikipedia.org/wiki/제로보드 "wikilink"), [그누보드](../Page/그누보드.md "wikilink"), [테크노트](https://ko.wikipedia.org/wiki/테크노트 "wikilink"), [ExpressionEngine](https://ko.wikipedia.org/wiki/ExpressionEngine "wikilink"), webmaker3.0 등이 있다. 이 프로그램들은 소스가 오픈된 채 출시된 프로그램이 많다. 그리고 이 프로그램들은 개인 서버에 설치하여도 활용이 가능한 경우가 있으며, 개인/기관의 차원을 넘어, 그 활용의 형태로는 커뮤니티 사이트, 블로그 등을 들 수 있다. 상용 프로그램들은 CRM, ERP 등, 즉, 기업 경영에 활용하기 좋은 형태로, 수많은 프로그램들이 출시되어 실용화된다. 이것은 기존의 C언어와 같은 언어에서처럼 모듈로 존재하기도 한다.

## 같이 보기

  - [LAMP (소프트웨어 번들)](https://ko.wikipedia.org/wiki/LAMP_\(소프트웨어_번들\) "wikilink")
  - [코드이그나이터](../Page/코드이그나이터.md "wikilink")
  - [라라벨](../Page/라라벨.md "wikilink")

## 각주

## 외부 링크

  - [PHP 공식 사이트](http://www.php.net)

  - [아파치 프로젝트 공식 사이트](http://www.apache.org)

  - [PHP 한국어 매뉴얼](https://web.archive.org/web/20061214053634/http://php.morva.net/manual/kr/index.php)

  - [Drupal](http://www.drupal.org)

  - [PHPSCHOOL](http://phpschool.com)

  - [PHPKorea](https://web.archive.org/web/20091202163720/http://www.phpkorea.org/)

  - [PHPoC (PHP On Chip - embedded IoT Platform)](http://www.phpoc.com)

  - [PHP 7 가이드](https://www.toptal.com/php/php-7-performance-features)

[PHP](https://ko.wikipedia.org/wiki/분류:PHP "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:1995년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1995년_개발된_프로그래밍_언어 "wikilink") [분류:PHP 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:PHP_라이선스_소프트웨어 "wikilink") [분류:동적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:동적_프로그래밍_언어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.  [재귀 약자를](https://ko.wikipedia.org/wiki/재귀_약자 "wikilink") 사용하고 있다.
2.  <http://www.php.net/manual/en/history.php.php>
3.
4.  [루비온레일즈](https://ko.wikipedia.org/wiki/루비온레일즈 "wikilink")
5.
6.  JSP, ASP, Java