> This article is converted from Wikipedia: [API](https://ko.wikipedia.org/wiki/API).


**API**(, 응용 프로그램 프로그래밍 인터페이스)는 [응용 프로그램에서](https://ko.wikipedia.org/wiki/응용_프로그램 "wikilink") 사용할 수 있도록, [운영 체제나](../Page/운영_체제.md "wikilink") [프로그래밍 언어가](../Page/프로그래밍_언어.md "wikilink") 제공하는 기능을 제어할 수 있게 만든 [인터페이스를](../Page/인터페이스_\(컴퓨팅\).md "wikilink") 뜻한다. 주로 파일 제어, 창 제어, 화상 처리, 문자 제어 등을 위한 인터페이스를 제공한다.

## 이용

API는 [응용 프로그램 이진 인터페이스](../Page/응용_프로그램_이진_인터페이스.md "wikilink")(ABI)와는 구별한다. API는 소스 코드 기반인 반면 ABI는 이진 인터페이스이다. 이를테면 POSIX는 API인 반면, [리눅스 기본 규격은](../Page/리눅스_기본_규격.md "wikilink") ABI를 제공한다.\[1\]\[2\]

### 절차적 언어에서의 API

대부분의 절차적 언어에서 API는 특정한 작업을 수행할 [함수](../Page/함수.md "wikilink")들의 집합을 규정하며, 특정 소프트웨어 구성 요소와 상호 작용할 수 있게 한다.

유닉스 명령어 `man 3 sqrt`는 `sqrt` 함수의 [시그너처를](https://ko.wikipedia.org/wiki/타입_시그너처 "wikilink") 대표한다:

``` C
SYNOPSIS
            #include <math.h>
            double sqrt(double X);
            float  sqrtf(float X);
DESCRIPTION
       sqrt computes the positive square root of the argument. ...
RETURNS
       On success, the square root is returned. If X is real and positive...
```

이와 비슷하게, 다른 언어들은 절차적 라이브러리를 갖고 있다. 이를테면 [펄](../Page/펄.md "wikilink")에는 내부 문서화 기능을 이용할 수 있는 동일한 수식 작업을 위한 전용 API들이 있으며, [perldoc](https://ko.wikipedia.org/wiki/perldoc "wikilink") 유틸리티를 이용하여 접근할 수 있다:

``` perl
$ perldoc -f sqrt
       sqrt EXPR
       sqrt    #Return the square root of EXPR.  If EXPR is omitted, returns
               #square root of $_.  Only works on non-negative operands, unless
               #you've loaded the standard Math::Complex module.
```

## API의 예

  - [윈도 API](https://ko.wikipedia.org/wiki/윈도_API "wikilink")
  - [마이크로소프트 윈도의](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [다이렉트엑스](https://ko.wikipedia.org/wiki/다이렉트엑스 "wikilink")
  - [단일 유닉스 규격](../Page/단일_유닉스_규격.md "wikilink")
  - [자바 API](https://ko.wikipedia.org/wiki/자바_API "wikilink")
  - [스칼라 API](../Page/스칼라_\(프로그래밍_언어\).md "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [OpenAL](../Page/OpenAL.md "wikilink")
  - [OpenCL](../Page/OpenCL.md "wikilink")

## 웹 API

웹 API는 웹 애플리케이션 개발에서 다른 서비스에 요청을 보내고 응답을 받기 위해 정의된 명세를 일컫는다. 예를 들어 블로그 API를 이용하면 [블로그](../Page/블로그.md "wikilink")에 접속하지 않고도 다른 방법으로 글을 올릴 수 있다. 그 외에 우체국의 우편번호 API, 구글과 네이버의 지도 API등 유용한 API들이 많으므로, 요즘은 홈페이지 구축이나 추가개편 시 따로 추가로 개발하지 않고 이런 오픈 API를 가져와 사용하는 추세다.

## 같이 보기

  - [플러그인](../Page/플러그인.md "wikilink")
  - [소프트웨어 개발 키트](../Page/소프트웨어_개발_키트.md "wikilink")
  - [웹 서비스](../Page/웹_서비스.md "wikilink")
  - [매시업](https://ko.wikipedia.org/wiki/매시업 "wikilink")

## 각주

[API](https://ko.wikipedia.org/wiki/분류:API "wikilink")

1.
2.