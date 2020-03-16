> This article is converted from Wikipedia: [Pkg-config](https://ko.wikipedia.org/wiki/Pkg-config).


**pkg-config**는 [소스 코드로부터](../Page/소스_코드.md "wikilink") 소프트웨어를 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")할 목적으로 설치된 [라이브러리를](../Page/라이브러리_\(컴퓨팅\).md "wikilink") 조회하기 위해 통일된 인터페이스를 제공하는 컴퓨터 [소프트웨어](../Page/소프트웨어.md "wikilink")이다. pkg-config는 원래 [리눅스](../Page/리눅스.md "wikilink")용으로 설계되었으나 현재는 다양한 계열의 [BSD](../Page/BSD.md "wikilink"), [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [솔라리스에서도](../Page/솔라리스_\(운영_체제\).md "wikilink") 이용할 수 있다.

설치된 라이브러리에 대해 다양한 정보를 출력한다. 이 정보는 다음을 포함한다:

  - [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") [컴파일러](../Page/컴파일러.md "wikilink")를 위한 매개변수
  - [링커를](../Page/링커_\(컴퓨팅\).md "wikilink") 위한 매개변수
  - 패키지 버전

최초의 구현은 셸로 작성되었으며, 나중에 [GLib](../Page/GLib.md "wikilink") 라이브러리를 이용하여 C로 재작성되었다.

## 개요

라이브러리가 설치될 때(RPM, deb 등을 통한 자동 설치 또는 소스로부터 직접 컴파일) .pc 파일이 포함되어 있어야 한다.

[libpng](https://ko.wikipedia.org/wiki/libpng "wikilink")에 대한 .pc 파일의 예는 다음과 같다:

``` pkgconfig
prefix=/usr/local
exec_prefix=${prefix}
libdir=${exec_prefix}/lib
includedir=${exec_prefix}/include

Name: libpng
Description: Loads and saves PNG files
Version: 1.2.8
Libs: -L${libdir} -lpng12 -lz
Cflags: -I${includedir}/libpng12
```

컴파일을 하는 동안 pkg-config의 사용 예는 다음과 같다.

``` console
$ gcc -o test test.c $(pkg-config --libs --cflags libpng)
```

## 외부 링크

  - [pkg-config home at freedesktop.org](http://pkg-config.freedesktop.org/)

  - [pkg-config manual page](http://www.die.net/doc/linux/man/man1/pkg-config.1.html)

[분류:라이브러리](https://ko.wikipedia.org/wiki/분류:라이브러리 "wikilink")