> This article is converted from Wikipedia: [GNU  ](https://ko.wikipedia.org/wiki/GNU__).


**GNU 바이너리 유틸리티**(GNU Binary Utilities) 또는 **GNU Binutils**는 여러 종류의 오브젝트 파일 형식들을 조작하기 위한 프로그래밍 도구 모음이다. 현재 버전은 [시그너스 솔루션즈의](https://ko.wikipedia.org/wiki/시그너스_솔루션즈 "wikilink") 프로그래머들이 [BFD](https://ko.wikipedia.org/wiki/BFD "wikilink") 라이브러리를 이용해 처음부터 만든 것이다. 이는 일반적으로 [GCC](../Page/GNU_컴파일러_모음.md "wikilink"), [make](https://ko.wikipedia.org/wiki/make "wikilink"), [GDB](https://ko.wikipedia.org/wiki/GDB "wikilink")와 함께 사용된다.

GNU 바이너리 유틸리티는 다음 명령을 포함한다.

  - [`as`](https://ko.wikipedia.org/wiki/as_\(유닉스\) "wikilink") - [어셈블러](https://ko.wikipedia.org/wiki/어셈블러 "wikilink")
  - [`ld`](https://ko.wikipedia.org/wiki/ld_\(유닉스\) "wikilink") - [링커](../Page/링커_\(컴퓨팅\).md "wikilink")
  - `addr2line` - 주소를 파일과 줄로 바꾼다.
  - [`ar`](https://ko.wikipedia.org/wiki/ar_\(유닉스\) "wikilink") - 아카이브(압축) 파일을 만들고, 수정하고, 해제한다.
  - `c++filt` - 맹글링된 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 심볼들을 원래대로 되돌린다.
  - [`nm`](https://ko.wikipedia.org/wiki/nm_\(유닉스\) "wikilink") - 오브젝트 파일의 심볼을 출력한다.
  - `objcopy` - 오브젝트 파일을 복사한다.
  - [`objdump`](https://ko.wikipedia.org/wiki/objdump "wikilink") - 오브젝트 파일에 대한 정보를 출력한다.
  - `ranlib` - 아카이브(압축)를 위한 색인을 만든다.
  - `readelf` - [ELF](https://ko.wikipedia.org/wiki/ELF "wikilink") 파일의 내용을 출력한다.
  - `size` - 전체와 부분의 크기를 출력한다.
  - `strings` - 표시할 수 있는 문자열을 출력한다.
  - [`strip`](https://ko.wikipedia.org/wiki/strip "wikilink") - 오브젝트 파일로부터 심볼을 제거한다.
  - `gprof` - [프로파일러](https://ko.wikipedia.org/wiki/프로파일러 "wikilink")

원래 이 꾸러미는 작은 유틸리티만으로 이뤄져 있었으나, 나중에 기능적으로 관련이 깊은 [GNU 어셈블러](../Page/GNU_어셈블러.md "wikilink") (GAS)와 [GNU 링커](../Page/GNU_링커.md "wikilink") (GLD)가 추가되었다.

GNU 바이너리 유틸리티에 들어있는 프로그램은 대부분 단순한 프로그램이다. 복잡한 구현은 이 프로그램들이 공유하고 있는 BFD, libopcodes 라이브러리에 들어있다.

초기 BFD 버전들은 [David Henkel-Wallace와](https://ko.wikipedia.org/wiki/David_Henkel-Wallace "wikilink") [Steve Chamberlain가](https://ko.wikipedia.org/wiki/Steve_Chamberlain "wikilink") 만들었다. [Ken Raeburn와](https://ko.wikipedia.org/wiki/Ken_Raeburn "wikilink") [Ian Lance Taylor이](https://ko.wikipedia.org/wiki/Ian_Lance_Taylor "wikilink") 최근까지 관리자를 맡아왔다. 2005년 현재 관리자는 [Nick Clifton이다](https://ko.wikipedia.org/wiki/Nick_Clifton "wikilink").

## 같이 보기

  - [GNU](../Page/GNU.md "wikilink")

## 외부 링크

  - [GNU 바이너리 유틸리티 공식 페이지](https://web.archive.org/web/20060622002253/http://www.gnu.org/software/binutils/manual/html_chapter/binutils.html)
  - [sourceware.org GNU 바이너리 유틸리티 페이지](http://sourceware.org/binutils/)
  - [GNU 바이너리 유틸리티 포럼](https://web.archive.org/web/20070312013735/http://www.nabble.com/Gnu---Binutils-f1499.html)

[분류:컴파일러](https://ko.wikipedia.org/wiki/분류:컴파일러 "wikilink") [분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")