> This article is converted from Wikipedia: [MinGW](https://ko.wikipedia.org/wiki/MinGW).


**MinGW**(과거 이름: **mingw32**)는 [마이크로소프트 윈도로](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 포팅한 GNU 소프트웨어 도구 모음이다.

MinGW는 [윈도 API를](https://ko.wikipedia.org/wiki/윈도_API "wikilink") 구현할 수 있는 헤더 파일들을 가지고 있으며 이로써 개발자들이 "자유롭게 쓸 수 있는" 컴파일러인 [GCC를](https://ko.wikipedia.org/wiki/GNU_컴파일러_모음 "wikilink") 사용할 수 있다. [시그윈](../Page/시그윈.md "wikilink") 포팅을 사용할 경우 컴파일한 프로그램 결과물이 [유닉스 계통의](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") 기능을 가상으로 구현하는 [런타임](https://ko.wikipedia.org/wiki/런타임 "wikilink")에 의존하는 반면, MinGW의 경우 이러한 기능에 의존하지 않고 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 기반 프로그램들을 만들 수 있다.

이 MinGW 프로젝트는 두 개의 기본 꾸러미를 관리하고 배포한다. 첫째로는 포팅된 GCC 컴파일러들은 [윈도 명령 줄에서](https://ko.wikipedia.org/wiki/Cmd.exe "wikilink"), 아니면 IDE에 통합된 채로 쓸 수 있다. 아니면 둘째로는 MSYS(minimal system의 약자)를 쓸 수도 있는데, 이것은 가벼운 유닉스 계통의 [셸](https://ko.wikipedia.org/wiki/셸 "wikilink") 환경을 제공한다. 이러한 환경은 [rxvt](https://ko.wikipedia.org/wiki/rxvt "wikilink")와 [autoconf](https://ko.wikipedia.org/wiki/autoconf "wikilink") 스크립트들을 실행하는 데에 충분한 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 도구들이 집약되어 있다.

두 개의 꾸러미들은 원래 [시그윈](../Page/시그윈.md "wikilink") 일부의 [forks였으며](https://ko.wikipedia.org/wiki/forks_\(프로그램_개발\) "wikilink") forks는 네이티브 윈도 기능 덕에 더 포괄적인 유닉스 계통의 지원을 제공한다. 두 개의 꾸러미들은 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink"). Win32 헤더 파일들은 [공용 도메인에](https://ko.wikipedia.org/wiki/퍼블릭_도메인 "wikilink") 공개된다. 반면 GNU에서 포팅되는 프로그램들은 [GNU 일반 공중 사용 허가서](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 하에서 사용할 수 있다. 완전한 MSYS 꾸러미와 개별 MinGW GNU 유틸리티들의 바이너리 파일들은 MinGW 사이트에서 내려 받을 수 있다.

## 역사

MinGW의 원래 이름은 mingw32 (Minimalist GNU for W32)이다.\[1\]\[2\] [32비트 바이너리를](https://ko.wikipedia.org/wiki/32비트 "wikilink") 만드는 것으로 제한되는 것으로 생각될 수 있었기에 이를 피하고자 숫자 32는 제거되었다. 콜린 피터스는 1998년 초판을 만들었고, 당시 [GCC의](https://ko.wikipedia.org/wiki/GNU_컴파일러_모음 "wikilink") [시그윈](../Page/시그윈.md "wikilink") 포팅만으로 이루어져 있었다.\[3\]\[4\] Jan-Jaap van der Heijden는 GCC의 윈도우 네이티브 이식판을 만들었고 [Binutils](https://ko.wikipedia.org/wiki/Binutils "wikilink")과 [Make를](https://ko.wikipedia.org/wiki/Make_\(소프트웨어\) "wikilink") 추가하였다. Mumit Khan은 나중에 Anders Norlander의 윈도우 시스템 헤더들을 포함하여, 윈도우 특화 기능들을 패키지에 더 추가하였다. 2000년에 이 프로젝트는 [소스포지](https://ko.wikipedia.org/wiki/소스포지 "wikilink")로 이동되어 커뮤니티의 도움을 받아 개발에 집중하고 있다.\[5\]\[6\]

MinGW는 2005년 9월 [소스포지](https://ko.wikipedia.org/wiki/소스포지 "wikilink")의 "이 달의 프로젝트"에 선정되었다.\[7\]

2013년 마지막 분기에, 새로운 프로젝트가 시작되었는데,\[8\] 그 이름은 MSYS2로, 32비트와 64비트 MinGW 패키지가 함께 포함되었다.

## 이름 붙이기

MinGW라는 이름은 Minimalist GNU for Windows의 줄임말이다. MinGW는 Mingw32라고 말할 수도 있는데 Win32 API용 헤더를 제공하기 때문이다.

MinGW를 발음하는 데에 정해진 기준은 없다. 흔히 "밍 위", "민기 더블유", "밍 더블유", 아니면 "민 그누"라고 발음한다. 간혹 발음 상의 편의성을 위해 "민지"로 발음하는 부류도 있다.

## 기능

MinGW와 MSYS의 결합은 작고 알찬 환경을 제공한다. 이로써 컴퓨터의 레지스트리나 파일의 항목을 남겨두지 않은 채 이동식 미디어로 불러들일 수 있다. 시그윈은 설치와 관리 면에서 더욱 복잡하다.

MinGW에서 응용 프로그램들을 크로스 컴파일할 수 있다. 시그윈 없이 윈도에서 돌아갈 소프트웨어를 컴파일하기 위해 개발자들이 MSYS의 윈도 설치판을 필요로 하지 않는다는 것을 말해 준다. 현재는 한때 지원하지 못하였던 [윈도 비스타와](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") [윈도 7과](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") 완전히 호환된다.

## 시그윈과의 비교

MinGW는 1.3.3의 시그윈에서 분리된 버전이다. 시그윈과 MinGW 둘 다 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 소프트웨어에서 [마이크로소프트 윈도로](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 포팅되긴 했으나 그 둘의 목표는 다르다.

시그윈은 완전한 POSIX 레이어를 윈도 상에서 제공하는 데 초점을 두고 호환성이 필요한 곳에는 성능을 포기한다. 반면 MinGW는 자유 컴파일러와 도구 모음을 제공하는 데 힘을 쏟지만 성능을 우선한다.

시그윈과 달리, MinGW는 호환성 레이어 DLL을 요구하지 않으며, 그에 따른 런타임은 허가 라이선스 하에서 주어진다. MinGW가 POSIX API를 제공하지 않기 때문에, 시그윈으로 컴파일할 수 있는 유닉스 응용 프로그램들을 컴파일할 수 없다. 구체적으로 말해, 특정한 POSIX 기능을 요구하는 응용 프로그램들과 POSIX 환경에서 실행될 것으로 예정된 프로그램들을 말한다. [SDL](https://ko.wikipedia.org/wiki/심플_다이렉트미디어_레이어 "wikilink"), [wxWidgets](https://ko.wikipedia.org/wiki/wxWidgets "wikilink"), [Qt](https://ko.wikipedia.org/wiki/Qt_\(프레임워크\) "wikilink"), 또는 [GTK+](https://ko.wikipedia.org/wiki/GTK+ "wikilink")와 같은, 여러 플랫폼을 지원하는 라이브러리들을 사용하여 짜여진 응용 프로그램들은 보통 시그윈에서 하던 것처럼 MinGW 안에서 쉽게 컴파일할 수 있다.

## 같이 보기

  - [시그윈](../Page/시그윈.md "wikilink")
  - [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink")

## 참조

<references />

## 외부 링크

  -
  -
[분류:마이크로소프트 윈도우](https://ko.wikipedia.org/wiki/분류:마이크로소프트_윈도우 "wikilink") [분류:퍼블릭 도메인 소프트웨어](https://ko.wikipedia.org/wiki/분류:퍼블릭_도메인_소프트웨어 "wikilink") [분류:에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:에뮬레이션_소프트웨어 "wikilink") [분류:유닉스](https://ko.wikipedia.org/wiki/분류:유닉스 "wikilink") [분류:리눅스](https://ko.wikipedia.org/wiki/분류:리눅스 "wikilink") [분류:1998년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1998년_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.