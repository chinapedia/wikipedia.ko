> This article is converted from Wikipedia: [콘셉트 \(C++\)](https://ko.wikipedia.org/wiki/콘셉트_\(C++\)).


**콘셉트**()는 ISO Technical Specification ISO/IEC TS 19217:2015으로 제출된 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") [템플릿의](../Page/템플릿_\(C++\).md "wikilink") 확장 기능이다.\[1\] 콘셉트는 이름이 붙은 불린 술어이며, 컴파일 시간에 평가된다. 콘셉트는 템플릿(클래스 템플릿, 함수 템플릿, 클래스의 멤버 함수 템플릿)과 함께 사용되어 사용자에게 제한을 거는데, 템플릿 파라미터로 받을 수 있는 인수에 조건을 건다.

다음 코드는 콘셉트를 사용 가능한 C++ 표준 라이브러리(또 다른 C++ ISO 기술 명세서이다. ISO/IEC DTS 21425)를 이용해 "EqualityComparable"라는 이름의 콘셉트를 정의한다. a==b와 a\!=b가 컴파일이 되고, "Boolean" 콘셉트를 만족하는 타입의 리턴값을 내놓는다면 모든 타입 T는 이 콘셉트를 만족시킨다.

``` Cpp
template <class T>
concept bool EqualityComparable() {
    return requires(T a, T b) {
        {a == b} -> Boolean; // Boolean은 불린 컨텍스트에서 사용될 수 있는 타입을 정의하는 콘셉트임
        {a != b} -> Boolean;
    };
}
```

이 콘셉트로 인해 제약이 걸린 함수 템플릿을 다음과 같이 선언될 수 있다.

``` Cpp
void f(const EqualityComparable&); // 제약이 걸린 함수 템플릿 선언
```

그리고 평범하게 호출할 수 있다.

``` Cpp
f(42); // 가능. int는 EqualityComparable을 만족함
```

콘셉트의 주요 용도는 다음과 같다.

  - 템플릿 프로그래밍에 타입 검사를 적용
  - 템플릿 인스턴스 생성 실패를 컴파일러가 단순하게 진단
  - 타입 프로퍼티에 따라 함수 템플릿 오버로드 혹은 클래스 템플릿 특수화를 선택
  - 자동 타입 추론에 제한을 걺

## 컴파일러 진단

만약 프로그래머가 템플릿의 요구사항을 만족시키지 않는 템플릿 인자를 사용하려 하면 컴파일러는 에러를 발생시킨다. 콘셉트가 없는 경우, 컴파일러 에러는 사람이 이해하기 어렵다. 왜냐하면 에러는 호출된 장소에서 일어나는 것이 아니라, 컴파일러 깊숙히 파묻혀 있는 내부 구현 안에서 발생하기 때문이다.

예를 들어, 는 처음 두 인자가 랜덤 접근 반복자이기를 요구한다. 만약 인자가 반복자가 아니거나 다른 종류의 반복자인 경우 std::sort가 인자를 양방향 반복자로써 사용하려 할 때 에러가 발생한다.

``` Cpp
std::list<int> l = {2, 1, 3};
std::sort(l.begin(), l.end());
```

콘셉트가 없는 일반적인 컴파일러 진단은 50줄이 넘어간다. 두 반복자의 뺄셈 표현식의 컴파일을 실패했다는 메시지부터 시작한다.

`인스턴스화 과정에서 '``':`
`에러: 찾을 수 없음 'operator-' (피연산자 타입은 '``' and '``')`
`,`

콘셉트가 사용된 경우, 에러는 호출 시점에 감지되어 보고될 수 있다.

``` cpp
error: cannot call function 'void std::sort(_RAIter, _RAIter) [with _RAIter = std::_List_iterator<int>]'
note:   concept 'RandomAccessIterator()' was not satisfied
```

## 함수 오버로드 선택

콘셉트는 템플릿 인자의 속성을 기반으로 하여 템플릿 함수 오버로드나 클래스 템플릿 특수화를 선택하는 데 [SFINAE](https://ko.wikipedia.org/wiki/SFINAE "wikilink")와 [tag dispatching](https://ko.wikipedia.org/wiki/tag_dispatching "wikilink") 대신 사용될 수 있다. 만약 인자가 둘 이상의 콘셉트를 만족시키는 경우, 좀 더 제약이 많은 콘셉트와 연관된 오버로드가 선택된다

## 타입 추론

변수 선언과 함수 반환 타입을 정할 때, 콘셉트가 사용되어 무제한의 타입 추론을 하는 를 대체할 수 있다.

``` Cpp
auto x1 = f(y); //x1의 타입은 f의 리턴값에 의해 추론됨
Sortable x2 = f(y); // x2의 타입도 추론되나, Sortable을 만족하는 경우에만 컴파일됨
```

## 구현 여부

콘셉트는 [GCC 6에서](../Page/GNU_컴파일러_모음.md "wikilink")  ISO/IEC TS 19217:2015에 명시된 대로 구현되었다.\[2\]

2016년 3월에 열린 C++ 표준 위원회 회의에서 evolution working group은 콘셉트를 [C++17](../Page/C++17.md "wikilink")에 포함시키려했지만, full committee에서 실패했다.\[3\]

콘셉트 v1은 [C++20](../Page/C++20.md "wikilink") 초안에 포함되었다.\[4\]

## 역사

콘셉트의 다른 형태인 "C++0x 콘셉트"가 [C++11](../Page/C++11.md "wikilink")에 잠깐 승인됐었으나 2009년에 삭제되었다.\[5\] "C++0x 콘셉트"는 추가적으로 콘셉트 맵(예를 들어 "Stack" 콘셉트가 'push()'라는 연산을 요구할 때, std::vector의 push_back()과 같은 연산을 'push()'와 매핑시킬 수 있음)과 *axiom*(연관성, 교환 가능성과 같은 의미론적 속성을 명기하여 컴파일러가 이용할 수 있게 함)이 포함돼 있었다.

이 버려진 신청과 대비하여, [C++20](../Page/C++20.md "wikilink")의 콘셉트는 "콘셉트 라이트"(Concepts Lite)\[6\]라고 불리기도 한다.

## 같이 보기

  - [콘셉트 (제네릭 프로그래밍)](../Page/콘셉트_\(제네릭_프로그래밍\).md "wikilink")
  - [타입 클래스](https://ko.wikipedia.org/wiki/타입_클래스 "wikilink")

## 내용주

<references />

## 참조

  -
  -
  -
## 외부 링크

  - [cppreference.com](http://en.cppreference.com/w/cpp/language/constraints) Constraints and Concepts

  -
[분류:C++](https://ko.wikipedia.org/wiki/분류:C++ "wikilink")

1.
2.
3.
4.
5.
6.