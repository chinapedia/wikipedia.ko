> This article is converted from Wikipedia: [New와 delete \(C++\)](https://ko.wikipedia.org/wiki/New와_delete_\(C++\)).


[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서, **new**와 **delete**는 [동적 메모리 할당](../Page/동적_메모리_할당.md "wikilink"), [객체 생성](https://ko.wikipedia.org/wiki/생성자 "wikilink") 그리고 객체 소멸을 수행하는 한 쌍의 언어 구조들이다.\[1\]

## 개요

"Placement new"라고 불리는 형태를 제외하고, new 연산자는 프로세스의 힙에 메모리 할당을 요청한다. 만약 충분한 메모리가 사용 가능하다면 new는 메모리를 초기화하고, 필요한 경우에 객체 생성자를 호출하며, 새로 할당되고 초기화된 메모리의 주소를 반환한다.\[2\]\[3\] new 요청은 다음과 같은 간단한 형태이다:

``` cpp
p = new T;
```

p는 type T의 포인터로 이미 선언되어 있다. T를 위한 [기본 생성자는](../Page/기본_생성자.md "wikilink") 할당된 메모리 버퍼에서 T 인스턴스를 생성하기 위해 호출된다.

만약 type T의 객체를 위한 공간이 메모리에서 충분하지 않다면, new 요청은 타입 std::bad_alloc의 예외를 던지면서 실패한다. 이것은 명시적으로 할당의 결과를 검사할 필요를 없애준다.

new와 대응하는 할당 해제는 delete이며, 소멸자를 호출하고 new에 의해 할당된 메모리를 자유 공간에 반환한다. 모든 new의 호출은 delete와 매치되어야 한다; 이것이 실패하면 [메모리 누수를](../Page/메모리_누수.md "wikilink") 유발한다.\[4\]

new 문법은 메모리 할당과 객체 생성에 대한 제어를 위해 여러 종류를 갖는다. 함수 호출 같은 문법은 기본 생성자가 아닌 다른 생성자(argument로 전달되는)를 호출하기 위해 사용된다.

``` cpp
p = new T(argument);
```

새로 할당된 버퍼를 초기화할 때, 기본 생성자 대신 단일 인자를 갖는 T 생성자를 호출한다.

다른 종류로서 단일 객체들이 아닌 객체들의 배열을 할당할 수도 있다.

``` cpp
p = new T [N];
```

이것은 자유 공간에서 type T의 N개의 객체들의 배열들을 위한 메모리 버퍼를 요청하며, 배열의 각 요소에 기본 생성자를 호출한다.

new\[\]를 사용한 메모리 할당은 반드시 delete\[\] 연산자를 사용해서 할당 해제되어야 한다. 부적절한 형태를 사용하는 것은 정의되지 않은 행동을 하는 결과를 초래할 수 있다. C++ 컴파일러들은 잘못된 형태를 사용하는 것을 위한 진단 메시지를 만들어야 할 필요는 없다.

[C++11](../Page/C++11.md "wikilink") 표준은 추가적인 문법을 명시하였다

``` cpp
p = new T[N] {initializer1, ..., initializerN};
```

이것은 각 p\[*i*\]를 initializer*i*로 초기화한다.

### 오류 처리

만약 new가 요청한 할당을 위한 충분한 메모리를 찾지 못한다면 3가지 방식으로 오류를 리포트할 수 있다. 첫번째로, ISO C++ 표준은 프로그램이 C++ 런타임과 함께 호출되는 new_handler로 불리는 커스텀 함수를 등록할 수 있게 한다. 이럴 경우 이 함수는 new가 오류를 마주칠 때마다 호출된다. new_handler는 더 많은 메모리를 사용 가능하게 시도하거나 할 수 없는 경우에 프로그램을 종료시킬 것이다.

만약 new_handler가 설치되지 않았다면, new는 대신 std::bad_alloc 타입의 예외를 던진다. 그래서 프로그램은 반환된 포인터의 값을 검사할 필요가 없다. 만약 오류가 던져지지 않았다면 할당은 성공한 것이다.

오류 처리의 세번째 방식은 다른 형태 new(std::nothrow)를 통해서 제공되는데, 이것은 예외가 던져지지 않았다는 것을 명시한다. 대신 할당 오류를 나태내기 위한 [널 포인터가](../Page/널_포인터.md "wikilink") 반환된다.

### 오버로딩

new 연산자는 [오버로드될](../Page/연산자_오버로딩.md "wikilink") 수 있으며, 특정한 타입들(클래스)은 자신의 인스턴스들을 위한 커스텀 메모리 할당 알고리즘을 사용할 수 있다. 예를 들면 다음에 나오는 코드는 [싱글턴 패턴의](https://ko.wikipedia.org/wiki/싱글턴_패턴 "wikilink") 변종으로서, 첫번째 new Singleton 호출은 인스턴스를 할당하고, 모든 나머지들은 이 같은 인스턴스의 반환을 호출한다:\[5\]

``` cpp
class Singleton {
    static Singleton *instance;
    static std::size_t refcount;

  public:
    static void *operator new(std::size_t nbytes) throw (std::bad_alloc) {
        if (instance == nullptr)
            instance = ::new Singleton; // Use the default allocator
        refcount++;
        return instance;
    }

    static void operator delete(void *p) {
        if (--refcount == 0) {
            ::delete instance;
            instance = nullptr;
        }
    }
};

Singleton *Singleton::instance = nullptr;
std::size_t Singleton::refcount = 0;
```

비록 특정한 오버로딩 메커니즘은 변경되었지만, 이 특징은 C++의 예전 역사에서부터 가능했었다. 이것은 객체 지향 C++ 프로그램들이 new(내부적으로 C 할당자를 사용하는: [§ Relation to malloc and free](https://ko.wikipedia.org/wiki/:en:New_and_delete_\(C++\)#Relation_to_malloc_and_free "wikilink"))로 많은 작은 객체들을 할당하는 경향이 있었기 때문에 언어에 추가되었다. 그러나 이것은 일반적인 C 프로그램들에 의해 수행되는 더 적고 큰 할당들을 위해 최적화되었다. [비야네 스트롭스트룹은](../Page/비야네_스트롭스트룹.md "wikilink") 초기의 애플리케이션들에서 C 함수 malloc가, 프로그램들이 이 함수에만 자신의 50%의 시간을 소비하는 "실제 시스템들에서 가장 흔한 성능 병목지역"이라고 언급하였다.

### void\* operator new(size_t size)

C++은  `void* operator new(size_t size)`.라고 불리는 단지 메모리를 할당하는 것을 구성한다. 할당 국면에서 new가 사용되며, 이것은 특정한 메모리 할당자를 정의하기 위해 클래스 별로 또는 전역적으로 오버라이딩될 수 있다.

## malloc과 free와의 관계

표준 C++이 [C 표준 라이브러리를](../Page/C_표준_라이브러리.md "wikilink") 포함하기 때문에, C 동적 메모리 할당 루틴들인 malloc, realloc 그리고 free도 C++ 프로그래머에게 사용될 수 있다. 이것들은 객체 초기화와 소멸을 수행하지 않기 때문에 이러한 루틴들의 사용은 대부분의 경우에 추천되지 않는다.\[6\] 사실 new와 delete는 객체 초기화를 직접 수행하는 것을 피하기 위해 C++의 첫 번째 버전에서 도입되었다.\[7\]

realloc으로 할당된 배열을 키우거나 줄이는 C 루틴들과 대조적으로, new\[\]에 의해 할당된 메모리 버퍼의 크기를 변경하는 것은 불가능하다. [C++ 표준 라이브러리는](../Page/C++_표준_라이브러리.md "wikilink") 대신 자신의 std::vector 템플릿 클래스에서 확장되거나 줄여질 수 있는 [동적 배열을](https://ko.wikipedia.org/wiki/동적_배열 "wikilink") 제공한다.

C++ 표준은 new/delete와 C 메모리 할당 루틴들 사이에서 특정한 관계를 명시하지 않지만, new와 delete는 일반적으로 malloc과 free의 래퍼로서 구현된다.\[8\] 두 집단의 연산자들을 혼합하는 것은 정의되지 않은 행동을 유발하며 실제로 락의 릴리즈의 실패로 인한 [데드락](https://ko.wikipedia.org/wiki/데드락 "wikilink") 같은 비극적인 결과를 초래한다.\[9\]

## 같이 보기

  - [할당자](../Page/할당자.md "wikilink")
  - [예외 처리](../Page/예외_처리.md "wikilink")
  - [메모리 풀](../Page/메모리_풀.md "wikilink")
  - [포인터 (프로그래밍)](../Page/포인터_\(프로그래밍\).md "wikilink")
  - [Resource Acquisition Is Initialization (RAII)](https://ko.wikipedia.org/wiki/Resource_Acquisition_Is_Initialization_\(RAII\) "wikilink")
  - [스마트 포인터](https://ko.wikipedia.org/wiki/스마트_포인터 "wikilink")

## 각주

[분류:C++](https://ko.wikipedia.org/wiki/분류:C++ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.   Section 4.4, Common C++ Memory Management Errors.