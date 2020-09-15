> This article is converted from Wikipedia: [SFINAE](https://ko.wikipedia.org/wiki/SFINAE).


**SFINAE**(대체 실패는 오류가 아님, Substitution failure is not an error)는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서 [템플릿](../Page/템플릿_\(C++\).md "wikilink") 매개변수에 자료형이나 값을 넣을 수 없어도 오류가 발생하지 않는 상황을 말한다. 이를 이용한 프로그래밍 테크닉을 설명하기 위해 SFINAE라는 줄임말을 최초로 사용한 사람은 David Vandevoorde이다.\[1\]

더 자세히 설명하자면, [함수 오버로드](../Page/함수_오버로드.md "wikilink") 후보 집합을 만들 때 그 중에는 템플릿 매개 변수에 자료형이나 값이 대입된 경우가 있을 수 있다. 이 대체 과정에서 발생한 오류가 C++ 표준이 허용하는 것이라면, 컴파일러는 컴파일 오류를 보고하지 않고, 후보 집합에서 그 후보를 제외한다.\[2\] 만약 하나 이상의 후보가 남고 오버로드 결정(Overload Resolution)에 성공한다면, 호출이 정상적으로 이루어진다.

## 예시

다음은 SFINAE의 기본 예시이다.

``` cpp
struct Test {
  typedef int foo;
};

template <typename T>
void f(typename T::foo) {}  // 정의 1

template <typename T>
void f(T) {}  // 정의 2

int main() {
  f<Test>(10);  // 정의 1을 호출한다.
  f<int>(10);   // SFINAE 덕분에
                // int::foo가 없으므로 오류 없이 정의 2를 호출한다.
}
```

위 예제에서, `f`<int> 를 사용했을 때 `int` 내부에 `foo` 가 정의되어 있지 않기 때문에 `T::foo` 에서 대체 오류가 발생하지만, 유효한 함수가 후보 집합에 남아있기 때문에 이 프로그램은 잘 작동한다.

이 개념은 잘못된 템플릿 선언이 사용되는 것을 막기 위해(헤더 파일이 포함되었을 때 등) 도입되었지만, 많은 개발자들이 이러한 점을 이용해서 컴파일 시에 활용할 수 있는 검사 기법을 만들어냈다. 특히 SFINAE는 템플릿을 인스턴스화할 때 템플릿 전달인자의 속성들을 정할 수 있도록 해준다.

예를 들어, SFINAE를 사용하면 주어진 자료형에 특정 typedef가 포함되어있는지 확인할 수 있다.

``` cpp
#include <iostream>

template <typename T>
struct has_typedef_foobar {
  // 자료형 "yes"와 "no"는 다른 크기를 가지도록 보장되어있다.
  // 여기서 sizeof(yes) == 1 이고 sizeof(no) == 2이다.
  typedef char yes[1];
  typedef char no[2];

  template <typename C>
  static yes& test(typename C::foobar*);

  template <typename>
  static no& test(...);

  // 만약 test<T>(nullptr)를 호출한 결과의 sizeof가 sizeof(yes)와 같다면,
  // 첫번째 오버로드가 호출된 것이고 주어진 자료형 T는 foobar라는 내부 타입을
  // 가지고 있다.
  static const bool value = sizeof(test<T>(nullptr)) == sizeof(yes);
};

struct foo {
  typedef float foobar;
};

int main() {
  std::cout << std::boolalpha;
  std::cout << has_typedef_foobar<int>::value << std::endl;  // false를 출력
  std::cout << has_typedef_foobar<foo>::value << std::endl;  // true를 출력
}
```

`T` 내부에 자료형 `foobar`가 정의되어 있으면 첫번째 `test`가 후보로 선택되고 널포인터 상수가 성공적으로 전달된다. (이 때 호출 결과의 자료형은 `yes`이다. ) 반대의 경우, 사용할 수 있는 유일한 함수는 두번째 `test`이고 결과의 자료형은 `no`이다. 여기서 생략 부호는 아무 자료형이나 받을 수 있으면서, 변환 순위가 가장 낮기 때문에 가능한 경우 첫번째 함수가 호출되도록 만든다. 이를 통해 모호성을 없앨 수 있다.

## C++11에서 더 단순하게 사용하기

[C++11](../Page/C++11.md "wikilink") 에서는 위 코드를 다음과 같이 더 단순하게 사용할 수 있다.

``` cpp
#include <iostream>
#include <type_traits>

template <typename... Ts>
using void_t = void;

template <typename T, typename = void>
struct has_typedef_foobar : std::false_type {};

template <typename T>
struct has_typedef_foobar<T, void_t<typename T::foobar>> : std::true_type {};

struct foo {
  using foobar = float;
};

int main() {
  std::cout << std::boolalpha;
  std::cout << has_typedef_foobar<int>::value << std::endl;
  std::cout << has_typedef_foobar<foo>::value << std::endl;
}
```

[Library fundamental v2 (n4562)](http://en.cppreference.com/w/cpp/experimental/lib_extensions_2)에서 제안된 탐지 패턴 표준을 이용하면, 위 코드를 다음과 같이 쓸 수 있다.

``` cpp
#include <iostream>
#include <type_traits>

template <typename T>
using has_typedef_foobar_t = typename T::foobar;

struct foo {
  using foobar = float;
};

int main() {
  std::cout << std::boolalpha;
  std::cout << std::is_detected<has_typedef_foobar_t, int>::value << std::endl;
  std::cout << std::is_detected<has_typedef_foobar_t, foo>::value << std::endl;
}
```

[Boost](../Page/Boost.md "wikilink")의 개발진은 boost::enable_if\[3\]과 같은 방법으로 SFINAE를 사용하였다.

## 참고 문헌

[분류:소프트웨어 디자인 패턴](https://ko.wikipedia.org/wiki/분류:소프트웨어_디자인_패턴 "wikilink") [분류:C++](https://ko.wikipedia.org/wiki/분류:C++ "wikilink")

1.
2.  International Organization for Standardization. "ISO/IEC 14882:2003, Programming languages — C++", § 14.8.2.
3.  [Boost Enable If](http://www.boost.org/doc/libs/release/libs/utility/enable_if.html)