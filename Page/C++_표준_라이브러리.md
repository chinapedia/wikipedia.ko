> This article is converted from Wikipedia: [C++ 표준 라이브러리](https://ko.wikipedia.org/wiki/C++_표준_라이브러리).


[C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 프로그래밍 언어에서, **C++ 표준 라이브러리** (C++ Standard Library)는 C++과 C++ ISO 표준 자체로 쓰여진 [클래스들과](https://ko.wikipedia.org/wiki/클래스_\(컴퓨터_과학\) "wikilink") [함수들의](../Page/함수_\(프로그래밍\).md "wikilink") 집합이다.\[1\] C++ 표준 라이브러리는 여러 제네릭 컨테이너들, 그리고 이러한 컨테이너들과 함수 객체, 제네릭 문자열, 스트림(인터렉티브와 파일 입출력을 포함하는), 몇몇 언어 특징 그리고 숫자의 제곱근을 찾는 것 같은 작업을 위한 모든 함수들을 활용하기 위한 함수들을 제공한다. C++ 표준 라이브러리는 또한 ".h"로 끝나는 ISO C90 C 표준 라이브러리의 18 헤더들을 포함하지만 이것들의 사용은 추천되지 않는다.\[2\] ".h"로 끝나지 않는 헤더는 C++ 표준 라이브러리에는 존재하지 않는다. C++ 표준 라이브러리의 특징은 `std` [이름공간](../Page/이름공간.md "wikilink") 내에 선언된다는 것이다.

C++ 표준 라이브러리는 [표준 템플릿 라이브러리](../Page/표준_템플릿_라이브러리.md "wikilink")(STL : Standard Template Library)에 의해 도입된 관습에 기반하며, [제네릭 프로그래밍과](https://ko.wikipedia.org/wiki/제네릭_프로그래밍 "wikilink") STL의 개발자들의 연구에 영향을 받았다.\[3\]\[4\] 비록 C++ 표준 라이브러리와 STL이 많은 특징들을 공유하지만, 둘 중 어느것도 다른 하나의 상위 집합은 아니다.

C++ 표준 라이브러리의 주목할 만한 특징은 이것이 단지 제네릭 알고리즘의 구문과 의미를 명시하는 것이 아니라 이것들의 성능의 요구에 가치를 두었다는 것이다.\[5\] 이러한 성능 요구 사항들은 종종 잘 알려진 알고리즘과 상응하는데, 이것은 기대되지만 사용되기 위해 요구되지는 않는다. 대부분의 경우에 이것은 선형 시간 O(*n*) 또는 선형 로그형 시간 O(*n* log *n*)를 요구하지만, 어떤 경우에는 안정 정렬을 위해 준선형 시간 O(*n* log<sup>2</sup> *n*) 같은 높은 수준도 허용된다. 이전의 정렬은 실질적으로 빠른 퀵 정렬의 사용을 허락하며 단지 평균적으로 O(*n* log *n*)를 요구하였지만, 인트로 정렬이 빠른 평균 성능과 최악의 상황 복잡도 최적화 모두를 위해 도입되었으며, C++11에서는 정렬이 최악의 경우라도 선형 로그적으로 보장되었다. 다른 경우에 요구 사항들은 퀵 선택의 경웨 단지 평균적으로 선형 시간을 요구하는 선택 알고리즘 같이 느슨한 상태로 남아 있으며,\[6\] 인트로 선택의 경우 최악의 경우에도 선형임을 요구하지 않는다.

C++ 표준 라이브러리는 C++ ISO 표준화 노력의 일환으로 ISO 표준화를 지나왔으며, 확장된 기능의 표준화를 다루는 다른 작업을 진행하고 있다.\[7\]

## 표준 헤더

다음의 파일들은 C++ 표준 라이브러리의 선언들을 포함하고 있다.

### 컨테이너

  - <array>
    C++11과 TR1에서 새로 추가되었다. 고정 크기 배열을 위한 컨테이너인 `std::array` 컨테이너 클래스 템플릿을 제공한다.
  - <bitset>
    비트 배열인 특수화된 `std::bitset` 컨테이너 클래스를 제공한다.
  - <deque>
    [덱인](https://ko.wikipedia.org/wiki/덱_\(자료_구조\) "wikilink") `std::deque` 컨테이너 클래스 템플릿을 제공한다.
  - <forward_list>
    C++11과 TR1에서 새로 추가되었다. 단일 [연결 리스트인](../Page/연결_리스트.md "wikilink") `std::forward_list` 컨테이너 클래스 템플릿을 제공한다.
  - <list>
    이중 [연결 리스트인](../Page/연결_리스트.md "wikilink") `std::list` 컨테이너 클래스 템플릿을 제공한다.
  - <map>
    연관 배열과 멀티맵인 `std::map` 와 `std::multimap` 컨테이너 클래스 템플릿을 제공한다.
  - <queue>
    단일 큐인 `std::queue`, 그리고 우선순위 큐인 `std::priority_queue` 컨테이너 어댑터 클래스를 제공한다.
  - <set>
    정렬된 연관 컨테이너 또는 집합인 `std::set` 와 `std::multiset` 컨테이너 클래스 템플릿을 제공한다.
  - <stack>
    스택인 `std::stack` 컨테이너 어댑터 클래스를 제공한다.
  - <unordered_map>
    C++11과 TR1에서 새로 추가되었다. 해시 테이블인 `std::unordered_map`와 `std::unordered_multimap` 컨테이너 클래스 템플릿을 제공한다.
  - <unordered_set>
    C++11과 TR1에서 새로 추가되었다. `std::unordered_set` 와 `std::unordered_multiset` 컨테이너 클래스 템플릿을 제공한다.
  - <vector>
    동적 배열인 [`std::vector`](../Page/벡터_\(STL\).md "wikilink") 컨테이너 클래스 템플릿을 제공한다.

### 일반

  - <algorithm>
    많은 컨테이너 [알고리즘](../Page/알고리즘.md "wikilink")의 정의를 제공한다.

<!-- end list -->

  - <chrono>
     `std::chrono::duration`, `std::chrono::time_point` 그리고 시계 같은 시간 요소를 제공한다.

<!-- end list -->

  - <functional>
    표준 알고리즘들과 함께 사용되는 목적으로 설계된 여러 [함수 객체들을](https://ko.wikipedia.org/wiki/함수_객체 "wikilink") 제공한다.
  - <iterator>
    반복자(iterator)들과 함께 사용되는 클래스와 템플릿을 제공한다.

<!-- end list -->

  - <memory>
    C++에서 클래스 템플릿 `std::unique_ptr`를 포함한 [메모리 관리를](../Page/메모리_관리.md "wikilink") 위한 기능들을 제공한다.
  - <stdexcept>
    `std::logic_error` 와 `std::runtime_error` (둘 다 `std::exception`를 상속한다.) 같은 표준 예외 클래스들을 포함한다.
  - <tuple>
    C++11과 TR1에서 새로 추가되었다. [튜플](../Page/튜플.md "wikilink")인 클래스 템플릿 `std::tuple`를 제공한다.
  - <utility>
    객체 쌍들(2 멤버 [튜플](../Page/튜플.md "wikilink")들)과 함께 동작하기 위한 템플릿 클래스 `std::pair`, 간단한 연산자 오버로딩을 위한 이름공간 `std::rel_ops`를 제공한다.

### 지역화

  - <locale>
    [로케일](../Page/로케일.md "wikilink")에 따른 특유한 정보를 캡슐화하고 조작하는 클래스들을 정의하고 함수들을 선언한다.
  - <codecvt>
    다양한 문자 인코딩들을 위한 코드 전환 측면을 제공한다.

### 문자열

  - <string>
    C++ 표준 [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink") 클래스와 템플릿들을 제공한다.
  - <regex>
    C++11과 TR1에서 새로 추가되었다. [정규 표현식을](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 사용하여 문자열 패턴 매칭을 위한 유틸리티들을 제공한다.

### 스트림과 입출력

  - <fstream>
    파일 기반 입력과 출력을 위한 기능을 제공한다. [fstream](https://ko.wikipedia.org/wiki/fstream "wikilink")을 보자.
  - <iomanip>
    정수와 [부동 소수점](https://ko.wikipedia.org/wiki/부동_소수점 "wikilink") 값의 [유효숫자](../Page/유효숫자.md "wikilink")를 포맷팅할 때 사용되는 베이스 같은 출력 포맷 조작을 위한 기능을 제공한다.
  - <ios>
    iostream의 동작을 위한 여러 타입과 함수들의 기본을 제공한다.
  - <iosfwd>
    여러 입출력 관련 클래스 템플릿들의 [선행선언](https://ko.wikipedia.org/wiki/선행선언 "wikilink")을 제공한다.
  - <iostream>
    C++ 입출력 기본을 제공한다. [iostream](https://ko.wikipedia.org/wiki/iostream "wikilink")을 보자.
  - <istream>
    템플릿 클래스 `std::istream`와 다른 입력을 위한 지원 클래스들을 제공한다.
  - <ostream>
    템플릿 클래스 `std::ostream`와 다른 출력을 위한 지원 클래스들을 제공한다.
  - <sstream>
    템플릿 클래스 `std::stringstream`와 다른 문자열 조작을 위한 지원 클래스들을 제공한다.
  - <streambuf>
    외부 파일이나 문자열 같은 특정한 타입의 문자들로 또는 문자들로부터 읽고 쓰는 기능을 제공한다.

### 언어 지원

  - <exception>
    표준 라이브러리에 의해 던져진 모든 예외들의 기본 클래스인 `std::exception`를 포함한 [예외 처리와](../Page/예외_처리.md "wikilink") 관련된 여러 타입들과 함수들을 제공한다.
  - <limits>
    기본 수치 타입들의 속성들을 만드는데 사용되는 템플릿 클래스 `std::numeric_limits`를 제공한다
  - <new>
    연산자 `new`와 `delete` 그리고 C++ [메모리 관리의](../Page/메모리_관리.md "wikilink") 기본을 구성하는 다른 함수들과 타입들을 제공한다.
  - <typeinfo>
    C++ [런타임 타입 정보와](../Page/런타임_타입_정보.md "wikilink") 함께 동작하기 위한 기능들을 제공한다.

### 스레드 지원 라이브러리

  - <thread>
    C++11과 TR1에서 새로 추가되었다. 스레드와 동작하기 위한 클래스와 이름공간을 제공한다.
  - <mutex>
    C++11과 TR1에서 새로 추가되었다. 30.4-1 이 섹션은 상호 배제 메커니즘을 제공한다: 뮤텍스 락 등.
  - <condition_variable>
    C++11에서 새로 추가되었다. 30.5-1 상태 변수들은 다른 스레드에 의해 통지되기 전까지 스레드를 막기 위해 사용되는 동기화를 제공한다.
  - <future>
    C++11에서 새로 추가되었다. 30.6.1-1은 C++ 프로그램이 한 스레드의 함수에서의 결과를 검색하기 위해 사용될 수 있는 구성 요소들을 제공한다.

### 수치(Numerics) 라이브러리

C++ 프로그램들이 준-수치 연산들을 수행하기 위해 사용할 수 있는 구성 요소들.

  - <complex>
    헤더 <complex>는 클래스 템플릿과 복잡한 숫자들을 표현하고 다루기 위한 많은 함수들을 정의한다
  - <random>
    (슈도)랜덤 숫자들을 생성하기 위한 기능
  - <valarray>
    5개의 클래스 템플릿(valarray, slice_array, gslice_array, mask_array 그리고 indirect_array), 두 클래스(slice와 gslice), 그리고 값들의 배열들을 표현하고 조작하는데 사용되는 관련된 함수들을 정의한다.
  - <numeric>
    일반화된 수치 연산들.

### C 표준 라이브러리

C 표준 라이브러리의 각 헤더들은 C++ 표준 라이브러리에서 다른 이름으로, .h를 제거하고 처음에 'c'를 추가한 상태로 생성된 채 포함된다; 예를 들면 'time.h'는 'ctime'이 된다. 이러한 헤더들과 전통적인 C 표준 라이브러리 헤더들의 유일한 차이점은 std:: 이름 공간의 어디에 함수들이 위치할 수 있느냐이다. ISO C에서, 표준 라이브러리에 존재하는 함수들은 매크로에 의해 구현될 수 있지만 ISO C++에서는 허락되지 않는다.

## 같이 보기

  - [아파치 C++ 표준 라이브러리](https://ko.wikipedia.org/wiki/아파치_C++_표준_라이브러리 "wikilink")
  - [Boost](../Page/Boost.md "wikilink")
  - [C POSIX 라이브러리](../Page/C_POSIX_라이브러리.md "wikilink")
  - [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink")
  - [표준 라이브러리](../Page/표준_라이브러리.md "wikilink")
  - [C++ 기술 보고서 1](../Page/C++_기술_보고서_1.md "wikilink")

## 각주

  - [Bjarne Stroustrup](../Page/비야네_스트롭스트룹.md "wikilink"): *[The C++ Programming Language](../Page/C++_프로그래밍_언어_\(책\).md "wikilink")*, Addison-Wesley, [ISBN 0-201-70073-5](https://ko.wikipedia.org/wiki/:en:Special:BookSources/0201700735 "wikilink")

## 외부 링크

  - [Standard C++ Library reference](http://en.cppreference.com/w/cpp)
  - \[<http://msdn2.microsoft.com/en-us/library/cscc687y(VS.80>).aspx Microsoft MSDN Library - Standard C++ Library Reference\]
  - [SourcePro C++ Documentation](http://www.roguewave.com/support/product-documentation/sourcepro.aspx)
  - [STLport](http://www.stlport.org/)
  - [The GNU Standard C++ Library](https://web.archive.org/web/20070706223608/http://gcc.gnu.org/libstdc++/)
  - [LLVM/Clang C++ Standard Library](http://libcxx.llvm.org/)

[분류:C++ 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C++_표준_라이브러리 "wikilink")

1.  ISO/IEC 14882:2003(E) *Programming Languages — C++* §17-27
2.  ISO/IEC 14882:2003(E) *Programming Languages — C++* §D.5
3.
4.
5.  "[Generic Algorithms](http://www.cs.rpi.edu/~musser/gp/algorithms.html)", David Musser
6.  [nth_element](http://en.cppreference.com/w/cpp/algorithm/nth_element)
7.