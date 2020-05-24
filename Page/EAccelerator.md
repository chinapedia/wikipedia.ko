> This article is converted from Wikipedia: [EAccelerator](https://ko.wikipedia.org/wiki/EAccelerator).


**eAccelerator**는 [PHP](../Page/PHP.md "wikilink") [프로그래밍 언어에](../Page/프로그래밍_언어.md "wikilink") 대한 [MMCache](https://ko.wikipedia.org/wiki/MMCache "wikilink") [확장](https://ko.wikipedia.org/wiki/확장 "wikilink")에서 [포크된](../Page/포크_\(소프트웨어_개발\).md "wikilink") [PHP 엑셀레이터이다](https://ko.wikipedia.org/wiki/PHP_엑셀레이터 "wikilink") .eAccelerator 는 [바이트코드](../Page/바이트코드.md "wikilink") [캐시](../Page/캐시.md "wikilink")를 제공한다. eAccelerator 는 [오픈 소스](../Page/오픈_소스.md "wikilink") 사용 및 배포하여 무료다. 오래되고 전혀 관리가되지 않고있는 버전도 인코더를 제공했다.

PHP 스크립트 에 액세스 할 때마다, PHP 는 일반적으로 구문 분석하고 바이트 코드로 스크립트를 컴파일한다. 일단 설치하면 eAccelerator는 컴파일 된 바이트 코드 를 최적화하고 공유 메모리 나 디스크 또는 둘 모두를 캐시한다. 그 대신 스크립트가 컴파일되는 것이 가능한 경우 스크립트에 대한 후속 접근시, eAccelerator는 캐시 된 바이트 코드에 액세스한다. 이것은 반복 구문 분석 및 컴파일의 성능 오버 헤드를 방지한다.

이전 eAccelerator 의 버전도 [공유 메모리접근](../Page/공유_메모리.md "wikilink"), 자동 [캐싱](../Page/웹_캐시.md "wikilink") 및 기타 관련 작업 을 가능하게 하는 PHP 스크립트에서 사용하는 기능\[1\]을 제공한다. 이 버전 0.9.6rc1 같이 제거했다.

이전 eAccelerator 버전은 몇 가지 코드 보호를 제공하고, 쉽게 정상 PHP 스크립트로 읽을 수 없는 파일을 생성하는 인코더 구성 요소를 가졌다. eLoader라는 전용의 확장은 eAccelerator 확장을 원하지 않을 경우 이러한 인코딩된 스크립트를 처리하는 데 사용할 수 있다. 이 기능은 현재 개발자버전에서 제거되었고 다음 버전에서 포함되지 않을 것이다.

EAccelerator는 [GNU GPL](https://ko.wikipedia.org/wiki/GNU_GPL "wikilink") 2.0로 배포되는 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink").

## 참조

## 같이 보기

  - [Zend Performance Suite](https://ko.wikipedia.org/wiki/Zend_Performance_Suite "wikilink")
  - [Alternative PHP Cache](https://ko.wikipedia.org/wiki/Alternative_PHP_Cache "wikilink")

## 외부 링크

  - [eAccelerator Web Site](http://eaccelerator.net/)
  - [eAccelerator Windows Downloads](http://www.sitebuddy.com/PHP/Accelerators/eAccelerator_windows_binaries_builds)
  - [doc eAccelerator](https://github.com/eaccelerator/eaccelerator/wiki)
  - [PHPCoder: web based front-end](http://phpcoder.sourceforge.net/)
  - [various versions of eAccelerator Windows binaries (VC6/VC9, TS/NTS)](https://web.archive.org/web/20140515082133/http://dev.freshsite.pl/php-accelerators/eaccelerator.html)

[분류:PHP](https://ko.wikipedia.org/wiki/분류:PHP "wikilink") [분류:프록시 서버](https://ko.wikipedia.org/wiki/분류:프록시_서버 "wikilink")

1.