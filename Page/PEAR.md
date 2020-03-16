> This article is converted from Wikipedia: [PEAR](https://ko.wikipedia.org/wiki/PEAR).


**PEAR**(피어, )는 [PHP](../Page/PHP.md "wikilink") 소프트웨어 코드의 저장소이다. PEAR 프로젝트는 동일 함수들을 수행하는 코드의 [재사용을](../Page/코드_재사용.md "wikilink") 장려할 목적으로 [스티그 S. 바켄에](https://ko.wikipedia.org/wiki/스티그_S._바켄 "wikilink") 의해 1999년에 개설되었다. 이 프로젝트는 구조화된 코드 [라이브러리를](../Page/라이브러리_\(컴퓨팅\).md "wikilink") 제공하고 코드 배포 시스템을 유지 보수하며 코드 패키지를 관리, 표준 코딩 스타일을 제고하고자 한다. 커뮤니티가 운영하지만 PEAR 프로젝트는 이사회 역할을 하고 행정 업무를 관할하는 PEAR 그룹을 보유한다. 각각의 PEAR 코드 패키지는 PEAR 산하에 독립적인 프로젝트를 이루고 있다. 또, 자체적인 개발 팀과 버전 관리, 문서를 보유하고 있다.

## PEAR 패키지

**PEAR 패키지**(PEAR package)는 [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink")으로 압축된 [tar](https://ko.wikipedia.org/wiki/tar_\(파일_포맷\) "wikilink") 파일로 배포된다. 각 압축 파일은 [PHP](../Page/PHP.md "wikilink")로 작성된 소스 코드를 이루고 있으며 보통 [객체 지향](https://ko.wikipedia.org/wiki/객체_지향 "wikilink") 스타일로 되어 있다. 수많은 PEAR 패키지들은 PHP 내의 단순한 include 문을 통해 일상적인 타사 코드로 사용할 수 있어서 개발자들이 이용하기 쉽다. 즉, PHP와 함께 포함된 PEAR 패키지 매니저는 패키지가 제공하는 특별한 기능이 PHP 설치의 일부로 표시하기 위해 기본적으로 PEAR 패키지를 설치하는데 쓰이기도 한다.

## PEAR 패키지 관리자

PEAR 패키지 관리자는 새로운 PEAR 패키지나 PECL 확장을 설치, 제거, 업그레이드하는 표준화된 방법을 제공한다. 패키지를 설치하기 앞서 패키지 의존성을 고려하는 것을 지시 받을 수 있으므로 필요한 추가 패키지들도 모두 설치할 수 있다.

PEAR 패키지 관리자는 명령 줄에 `pear` 명령을 이용하여 실행한다.

## PECL

**PECL**()은 PEAR와 개념적으로는 매우 비슷하며 실제로 PECL 모듈들은 PEAR 패키지 관리자와 함께 설치된다. PECL은 PHP로 컴파일하기 위한 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 확장을 포함하고 있다. C 프로그램인 PECL 확장은 PEAR 패키지 보다 더 효율적으로 동작한다. PECL에는 XML 파싱, 추가 데이터베이스로의 접근, 메일 파싱, [펄](../Page/펄.md "wikilink")이나 [파이썬](../Page/파이썬.md "wikilink")을 PHP 스크립트로의 임베디드, PHP 스크립트 컴파일을 위한 모듈들을 포함하고 있다. PECL은 2003년 10월 PEAR 프로젝트로부터 파생되었다. 원래의 이름은 PEAR 확장 코드 라이브러리(PEAR Extension Code Library)였으나 현재는 PEAR와 독립적으로 운영된다.

PECL 확장은 PHP 매뉴얼 내의 표준 확장과 나란히 문서화되어 있으므로 PECL 확장에 대한 특별한 매뉴얼은 존재하지 않는다.

## 외부 링크

  - [The PEAR Project](http://pear.php.net)

  - [The PECL Project](http://pecl.php.net)

[분류:PHP](https://ko.wikipedia.org/wiki/분류:PHP "wikilink") [분류:웹 프레임워크](https://ko.wikipedia.org/wiki/분류:웹_프레임워크 "wikilink") [분류:자유 패키지 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_패키지_관리_시스템 "wikilink")