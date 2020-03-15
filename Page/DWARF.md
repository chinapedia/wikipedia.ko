> This article is converted from Wikipedia: [DWARF](https://ko.wikipedia.org/wiki/DWARF).


**DWARF**는 널리 사용되는 표준화된 [디버깅 자료 형식이다](https://ko.wikipedia.org/wiki/디버깅_자료_형식 "wikilink"). DWARF는 원래 [ELF 파일 형식을](https://ko.wikipedia.org/wiki/ELF_파일_형식 "wikilink") 위해 만들어 졌지만, 이것은 목적 파일과 독립적이다.\[1\] 이름은 중세 판타지인 "ELF" 같은 것으로서 공식적인 뜻은 없지만 이후에 [배크로님](https://ko.wikipedia.org/wiki/배크로님 "wikilink")인 'Debugging With Attributed Record Formats'이 제안되었다.\[2\]

## 역사

DWARF의 첫 버전은 지나친 저장 공간을 사용하였지만 호환 불가능한 다음 버전인 DWARF-2는 자료 크기를 줄이기 위해 다양한 인코딩 기법들을 추가하였다. DWARF는 즉시 범용적으로 받아들여지지 않았다. 예를 들면 [썬 마이크로시스템즈가](https://ko.wikipedia.org/wiki/썬_마이크로시스템즈 "wikilink") ELF를 [솔라리스의](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 한 부분으로 채택하였을 때, 그들은 [stabs](https://ko.wikipedia.org/wiki/stabs "wikilink")를 계속 사용하기로 하였다. 이것은 "stabs-in-elf"로 삽입되었다. [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")도 따라함으로써 DWARF-2는 1990년대 후반까지도 일반적으로 채택되지 않았다.

[자유 표준 그룹](https://ko.wikipedia.org/wiki/자유_표준_그룹 "wikilink")(Free Standards Group)의 DWARF 워크그룹은 2006년 1월에 DWARF 버전 3을 릴리즈하였다.\[3\] 이것은 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 이름공간과 추가적인 [컴파일러 최적화](https://ko.wikipedia.org/wiki/컴파일러_최적화 "wikilink") 기법들의 지원을 추가하였다.

DWARF 위원회는 2010년 버전 4를 공개했는데 이것은 개선된 데이터 압축, 최적화된 코드에 대한 더 나은 명세 그리고 C++ 언어의 새로운 특징들에 대한 지원을 제공한다.\[4\]

## 구조

DWARF는 디버깅 정보 엔트리(DIE)라고 불리는 데이터 구조를 사용하는데 이것은 각각 변수, 타입, 프로시저 등을 나타낸다. DIE는 태그(예를 들면 `DW_TAG_variable`, `DW_TAG_pointer_type`, `DW_TAG_subprogram`)들과 속성(key-value pairs)들을 갖는다. DIE는 내부(자식) DIE들을 갖을 수 있는데 이것은 트리 구조를 형성한다. DIE 속성은 트리 안에서 다른 DIE를 가리킬 수 있다. 예를 들면 변수를 나타내는 DIE는 변수의 타입을 기술하는 DIE를 가리키는 `DW_AT_type` 엔트리를 가질 것이다.

공간을 절약하기 위해서, 심볼릭 디버거들에서 사용되는 두 큰 테이블들이 간단하고 특별한 목적의 [유한 상태 기계를](https://ko.wikipedia.org/wiki/유한_상태_기계 "wikilink") 위한 [바이트코드](https://ko.wikipedia.org/wiki/바이트코드 "wikilink") 명령어들로 나타내진다. 코드 위치와 소스 코드 위치를 매핑하는 줄 번호 테이블은 또한 어떤 명령어들이 함수 프롤로그와 에필로그의 부분인지를 명시한다. 콜 프레임 정보 테이블은 디버거들이 [콜 스택에서](https://ko.wikipedia.org/wiki/콜_스택 "wikilink") 위치를 찾을 수 있게 한다.

## 더 읽어보기

DWARF 표준 위원회의 의장인 마이클 이거는 디버깅 형식과 DWARF 3을 소개하는, *Introduction to the DWARF Debugging Format*라는 책을 썼다.\[5\]

## 같이 보기

  - stabs - 심볼 테이블 문자열 디버깅 형식

## 각주

## 외부 링크

  -
  - [Libdwarf](http://www.prevanders.net/dwarf.html), a C library intended to simplify reading (and writing) applications using DWARF2, DWARF3.

  - [How debuggers work](http://eli.thegreenplace.net/2011/02/07/how-debuggers-work-part-3-debugging-information/): Part 3 - Debugging information

  - [Debugging formats DWARF and STAB](http://www.ibm.com/developerworks/library/os-debugging/)

[분류:디버깅 자료 형식](https://ko.wikipedia.org/wiki/분류:디버깅_자료_형식 "wikilink")

1.
2.
3.
4.
5.