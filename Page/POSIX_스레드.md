> This article is converted from Wikipedia: [POSIX ](https://ko.wikipedia.org/wiki/POSIX_).


**POSIX 스레드**(POSIX Threads, 약어: **PThread**)는 병렬적으로 작동하는 소프트웨어의 작성을 위해서 제공되는 표준 API다.

Pthread는 모든 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") POSIX 시스템에서, 일반적으로 이용되는 라이브러리이다. 유닉스 계열 운영 체제라 하면 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 등이 포함된다. Unix 시스템과는 다른 길을 걷고 있는 Windows 역시 여러가지 이유로 Pthread를 지원한다. 예를 들어 pthread-w32 를 이용하면 윈도 상에서도 Pthread API의 subset 함수를 이용할 수 있다. pthread-w32 는 [redhat.com](http://sources.redhat.com/pthreads-win32/) 에서 얻을 수 있다. (Pthread 에서 P는 항상 대문자로 쓰도록 약속되어 있다.)

## 설명

Pthread는 C 프로그래밍 언어에서 사용할 수 있는 함수들의 모음으로 제공된다. Pthread 라이브러리에서 제공하는 함수는 **pthread.h**를 포함하여 호출할 수 있다.

자료형

  - pthread_ t : 스레드 핸들러
  - pthread_attr_t : 스레드 성질

Pthread는 스레드 제어를 위한 다양한 함수를 제공한다. 제공되는 함수의 목록은 [Pthread API Reference](http://www.joinc.co.kr/modules/moniwiki/wiki.php/Site/Thread/Beginning/PthreadApiReference)에서 확인할 수 있다.

## 외부 링크

  - [Joinc Pthread API Reference](http://www.joinc.co.kr/modules/moniwiki/wiki.php/Site/Thread/Beginning/PthreadApiReference)
  - [Thread에 대해서](http://www.joinc.co.kr/modules/moniwiki/wiki.php/Site/Thread/Beginning/WhatThread)
  - [스레드 설명 사이트](http://www.joinc.co.kr/modules/moniwiki/wiki.php/Site/Thread)

[분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink") [분류:스레드](https://ko.wikipedia.org/wiki/분류:스레드 "wikilink")