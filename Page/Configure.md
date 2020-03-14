> This article is converted from Wikipedia: [Configure](https://ko.wikipedia.org/wiki/Configure).


[thumb와](https://ko.wikipedia.org/wiki/파일:Autoconf-automake-process.svg "wikilink") [automake](https://ko.wikipedia.org/wiki/automake "wikilink")를 포함한 흐름도. 이 도구들은 GNU 빌드 시스템에 위치해 있다.\]\] **configure** 스크립트는 개발 중인 프로그램을 각기 다른 수많은 컴퓨터들에서 실행할 수 있도록 도와주도록 설계된 실행 스크립트이다. [소스 코드로부터](https://ko.wikipedia.org/wiki/소스_코드 "wikilink") [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")하기 직전에 사용자 컴퓨터의 [라이브러리의](https://ko.wikipedia.org/wiki/라이브러리_\(컴퓨팅\) "wikilink") 존재 여부를 확인하고 연결시킨다.

일반적으로 모든 configure 스크립트는 "configure"라는 이름으로 되어 있다. 또, configure 스크립트는 [bash](https://ko.wikipedia.org/wiki/bash "wikilink") 문법으로 작성되지만, 원하는 셸에 맞추어 실행 스크립트를 작성할 수 있다.

## 이용

소프트웨어를 소스 코드로부터 직접 가져오는 일은 일반적으로 다음 단계들을 수반한다: [makefile](https://ko.wikipedia.org/wiki/makefile "wikilink") 구성, 소스 컴파일, 적절한 곳에 실행 파일 최종 설치. configure 스크립트는 이러한 단계들 가운데 첫 단계를 완수한다. configure 스크립트를 사용하는 일은 컴파일 이전에 makefile을 생성하는 자동화된 방식으로, 소프트웨어가 실행 파일이 컴파일되고 실행될 수 있도록 시스템에 길들이게 한다. 최종 실행 소프트웨어는 소스 코드를 포함한 현재 디렉터리를 가리키는 셸에서 다음의 명령을 실행하여 얻을 수 있다.

    ./configure
    make
    make install

단순히 `configure` 대신 `./configure`를 사용해야 스크립트가 현재 디렉터리에 있음을 셸에게 지시할 수 있다. 기본적으로 보안을 이유로 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 계열 운영 체제들은 실행 파일에 대해 현재 디렉터리를 검색하지 않으므로 완전한 경로를 명시해 주어야 오류를 피할 수 있다.\[1\]

일을 마치면 `configure`는 `config.log`에 보고서를 출력한다. `./configure --help`를 실행하면 명령 줄 매개변수를 보여주며 다음과 같은 부가 기능을 켜고 끌 수 있다:

    ./configure --libs="-lmpfr -lgmp"
    ./configure --prefix=/home/myname/apps

첫 줄은 `mpfr`과 `gmp` 라이브러리를 포함한다. 두 번째 줄은 [make에](https://ko.wikipedia.org/wiki/Make_\(소프트웨어\) "wikilink") 마지막 버전을 `/home/myname/apps`에 설치할 것을 지시한다. 매개변수 안에 공백 문자가 있으면 인용 부호로 감싸 주어야 한다.

## configure 생성

소프트웨어 개발자들은 GNU의 [Autotools를](https://ko.wikipedia.org/wiki/GNU_빌드_시스템 "wikilink") 이용함으로써 [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") 소프트웨어 개발을 단순화한다. 이 스크립트들은 환경 설정, 플랫폼 아키텍처, 필요한 빌드 및 런타임 의존성의 존재 및 위치에 대한 정보를 조회한다. 수집된 정보는 설치 단계 가운데 `configure.ac` 또는 (현재는 사용이 권장되지 않는) `configure.in`에 저장한다.\[2\]

## 의존성 검사

신규 개발에서 라이브러리 의존성 검사는 대개 [m4](https://ko.wikipedia.org/wiki/m4_\(프로그래밍_언어\) "wikilink") 매크로 PKG_CHECK_MODULES를 통해 [pkg-config](https://ko.wikipedia.org/wiki/pkg-config "wikilink")를 사용한다. pkg-config가 인기를 끌기 전에는 별개의 m4 매크로를 만들어서 의존하는 라이브러리 배포판에 포함할 파일을 위치시켜야 했다.

## 같이 보기

  - [Autoconf](https://ko.wikipedia.org/wiki/Autoconf "wikilink")
  - [소프트웨어 빌드](https://ko.wikipedia.org/wiki/소프트웨어_빌드 "wikilink")
  - [GNU 빌드 시스템](https://ko.wikipedia.org/wiki/GNU_빌드_시스템 "wikilink")

## 참고문헌

  - A succinct introduction\[3\]
  - A verbose introduction\[4\]

## 참조

<references />

[분류:컴파일 도구](https://ko.wikipedia.org/wiki/분류:컴파일_도구 "wikilink") [분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink")

1.
2.
3.
4.