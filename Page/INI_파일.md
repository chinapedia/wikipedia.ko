> This article is converted from Wikipedia: [INI ](https://ko.wikipedia.org/wiki/INI_).


**INI(Initialization) 파일** [포맷은](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") [설정 파일에](https://ko.wikipedia.org/wiki/설정_파일 "wikilink") 대한 [de facto](https://ko.wikipedia.org/wiki/de_facto "wikilink") 표준이다. INI 파일은 단순 구조의 [텍스트 파일로](../Page/텍스트_파일.md "wikilink") 이루어져 있다. 보통 [마이크로소프트 윈도와](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 연결되어 있지만 다른 [운영 체제에서도](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 사용할 수 있다. "INI 파일"이라는 이름은 ".INI"라는 [파일 확장자가](../Page/파일_확장자.md "wikilink") 따라오지만, ".CFG", ".conf"\[1\]\[2\], ".TXT"\[3\] 등의 다른 확장자를 사용하기도 한다.

## 형식

  - 매개 변수

INI 파일에 포함된 기본 요소는 매개 변수이다. 각 변수는 이름과 값을 가지고 있으며 [등호](https://ko.wikipedia.org/wiki/등호 "wikilink")로 이를 구분한다. "이름"은 등호 왼쪽에 적는다.

``` ini
이름 = 값
```

  - 섹션

매개 변수는 임의의 이름으로 지정된 여러 개의 섹션으로 구분할 수 있다. 이 섹션 이름은 [괄호](https://ko.wikipedia.org/wiki/괄호 "wikilink") (\[, \])로 구분한다.

``` ini
[섹션]
```

  - 주석

[세미콜론](https://ko.wikipedia.org/wiki/세미콜론 "wikilink") (;)은 [주석의](../Page/주석_\(프로그래밍\).md "wikilink") 시작을 가리킨다. 줄이 끝날 때까지 주석을 계속 적을 수 있다. 세미콜론 사이의 모든 항목과 줄의 끝 부분까지의 내용은 프로그램의 설정값에서 무시한다.

``` ini
; 주석
```

## 예

가상의 프로그램(실제로 존재하지는 않음)을 위한 INI 파일의 예는 다음과 같다. 두 개의 섹션을 가지고 있으며, 그 가운데 한 섹션은 소프트웨어의 소유자에 대한 것이며, 나머지 하나는 종업원 명부 데이터베이스 연결에 대한 것이다. 또, 파일을 마지막으로 수정한 날짜, [도메인 이름](https://ko.wikipedia.org/wiki/도메인_이름_시스템 "wikilink") 대신 [IP 주소가](https://ko.wikipedia.org/wiki/IP_주소 "wikilink") 쓰인 까닭에 대해 주석을 적고 있다.

``` ini
; 홍길동이 2001년 4월 1일에 마지막으로 수정하였음
[owner]
name=홍길동
organization=최고의 제품

[database]
server=192.0.2.62     ; 네트워크 이름 변환이 동작하지 않는 경우 IP 주소를 사용한다
port=143
file="payroll.dat"
```

## 같이 보기

  - [MSConfig](https://ko.wikipedia.org/wiki/MSConfig "wikilink")
  - [윈도 레지스트리](https://ko.wikipedia.org/wiki/윈도_레지스트리 "wikilink")

## 참조

<references />

## 외부 링크

  - [비공식 규격](http://www.cloanto.com/specs/ini/)
  - [INI C++ 툴킷](https://github.com/feff/ini)

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:설정 파일](https://ko.wikipedia.org/wiki/분류:설정_파일 "wikilink")

1.  [.conf initialization files](http://www.fileinfo.com/extension/conf)
2.  [Other .conf initialization files](https://www.google.com/search?q=.conf+file+format&ie=utf-8&oe=utf-8&aq=t&rls=org.mozilla:en-US:official&client=firefox-a)
3.  See [Trainz](https://ko.wikipedia.org/wiki/b:Trainz/Config.txt_Files "wikilink") which uses config.txt for virtually all data base assets. (Trainsoptions.txt is that app's version of a .ini file)