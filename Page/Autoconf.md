> This article is converted from Wikipedia: [Autoconf](https://ko.wikipedia.org/wiki/Autoconf).


[오른쪽의](https://ko.wikipedia.org/wiki/파일:Autoconf-automake-process.svg "wikilink") 순서도\]\] **Autoconf**는 [셸 스크립트를](../Page/셸_스크립트.md "wikilink") 만드는 도구이다. 이 도구를 사용하여 자동으로 소프트웨어 [소스 코드](../Page/소스_코드.md "wikilink") 꾸러미를 구성하여 여러 종류의 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 시스템에 적용할 수 있다.

Autoconf가 만든 구성 스크립트는 스크립트가 실행될 때 독립적으로 동작한다.

또한 Autoconf는 [Automake](../Page/Automake.md "wikilink"), [Libtool](https://ko.wikipedia.org/wiki/Libtool "wikilink")과 함께 [GNU 빌드 시스템을](../Page/GNU_빌드_시스템.md "wikilink") 만든다.

Autoconf는 사용자가 작성한 configure.ac 파일을 configure 셸 스크립트로 바꾸는 데 [GNU m4를](https://ko.wikipedia.org/wiki/GNU_m4 "wikilink") 이용한다. 이 configure 스크립트는 사용자와 대화하면서 실행되지 않으며 미리 작성된 양식으로부터 미리 정해 둔 헤더와 [makefile](https://ko.wikipedia.org/wiki/makefile "wikilink")을 만들어 낸다.

Autoconf는 'configure.ac' 안에서 [M4](https://ko.wikipedia.org/wiki/m4_\(언어\) "wikilink") 프로그램을 셸 스크립트로 [컴파일한다고](../Page/컴파일러.md "wikilink") 할 수 있다.

## 역사

Autoconf는 1991년 여름에 데이비드 맥켄지(David Mackenzie)가 [자유 소프트웨어 재단의](../Page/자유_소프트웨어_재단.md "wikilink") 작업을 지원하기 위해 시작하였다. 그 뒤 여러 해 동안 다양한 제작자로부터 기능 개선을 제공 받아 성장하였으며 자유, 오픈 소스 소프트웨어에서 가장 널리 쓰이는 빌드 구성 시스템이 되었다.

## 접근

Autoconf는 [펄](../Page/펄.md "wikilink")이 사용하는 [Metaconfig](https://ko.wikipedia.org/wiki/Metaconfig "wikilink") 꾸러미와 비슷하다. [X 윈도 시스템에서](../Page/X_윈도_시스템.md "wikilink") 사용된 [imake](https://ko.wikipedia.org/wiki/imake "wikilink") 시스템은 이와 밀접한 관계가 있지만 시스템에 대한 관점은 다르다.

[포팅](https://ko.wikipedia.org/wiki/포팅 "wikilink")이 대한 Autoconf의 접근은 [기능](https://ko.wikipedia.org/wiki/기능 "wikilink")을 테스트하기 위함이지, 버전을 테스트하기 위한 것은 아니다. 이를테면, 썬OS 4 위의 네이티브 C 컴파일러는 [ISO C를](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink") 지원하지 않았다. 그러나 사용자나 관리자가 ISO C 호환 컴파일러를 설치할 수 있다. 순수한 버전을 기반으로 접근하면 ISO C 컴파일러의 존재를 파악하지 못하지만 접근을 테스트하는 기능은 사용자가 설치했던 ISO C 컴파일러를 발견할 수 있다.

이 접근은 다음의 장점을 얻기 위해 원칙을 세우고 있다:

  - configure 스크립트는 새로운 시스템이나 알지 못하는 시스템 위에서 제대로 된 결과를 얻을 수 있다.
  - [관리자가](https://ko.wikipedia.org/wiki/시스템_관리자 "wikilink") 저만의 컴퓨터의 환경을 설정하고 configure 스크립트가 그 설정의 장점을 활용할 수 있게 도와 준다.
  - 어떠한 특정한 기능의 지원 여부를 알아 내기 위해 버전, 패치 번호 등의 자세한 정보의 흔적을 굳이 유지하지 않아도 된다.

## 같이 보기

  - [GNU 빌드 시스템](../Page/GNU_빌드_시스템.md "wikilink")
  - [Sane 빌드 환경](https://ko.wikipedia.org/wiki/Sane_빌드_환경 "wikilink")
  - [pkg-config](https://ko.wikipedia.org/wiki/pkg-config "wikilink") 패키지 의존 감지
  - [CMake](../Page/CMake.md "wikilink") 대체 빌드 시스템

## 외부 링크

  - [GNU Autoconf 홈페이지](http://www.gnu.org/software/autoconf/)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:컴파일러](https://ko.wikipedia.org/wiki/분류:컴파일러 "wikilink") [분류:유닉스](https://ko.wikipedia.org/wiki/분류:유닉스 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")