> This article is converted from Wikipedia: [템플릿 \(C++\)](https://ko.wikipedia.org/wiki/템플릿_\(C++\)).


**템플릿**()은 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 프로그래밍 언어의 한 기능으로, 함수와 클래스가 [제네릭 형과](https://ko.wikipedia.org/wiki/제네릭_프로그래밍 "wikilink") 동작할 수 있게 도와 준다. 함수나 클래스가 개별적으로 다시 작성하지 않고도 각기 다른 수많은 [자료형](../Page/자료형.md "wikilink")에서 동작할 수 있게 한다. 이는 [튜링 완전](https://ko.wikipedia.org/wiki/튜링_완전 "wikilink") 언어로 볼 수 있다.

템플릿은 C++에서 프로그래머들에게 유용한데, 특히 [다중 상속과](https://ko.wikipedia.org/wiki/다중_상속 "wikilink") [연산자 오버로딩과](../Page/연산자_오버로딩.md "wikilink") 결합할 때 그러하다. [C++ 표준 라이브러리는](../Page/C++_표준_라이브러리.md "wikilink") 연결된 템플릿의 프레임워크 안에서 수많은 유용한 함수들을 제공한다.

C++ 템플릿은 [CLU](https://ko.wikipedia.org/wiki/CLU "wikilink")가 제공하는 매개변수 형태의 모듈과 [에이다](https://ko.wikipedia.org/wiki/에이다 "wikilink")가 제공하는 제네릭에 영향을 받았다.\[1\]

## 개괄

템플릿의 종류는 함수 템플릿과 클래스 템플릿의 두 가지가 있다. C++14부터는 세번째 템플릿으로 변수 템플릿이 있다.

### 함수 템플릿

여러 다른 자료형(int, long, float, double, class... )을 템플릿 인자 ('\<...\>' 안에 들어가는)로 받아, 함수 내부에서 활용할 수 있도록 한 것이다. 다시 말하면, 여러 다른 자료형에 대하여 같은 역할을 하는 하나의 함수 계열을 하나의 템플릿으로 표현할 수 있다는 점이다. 형태는 아래와 같다.

``` cpp
template <class identifier> function_declaration;
template <typename identifier> function_declaration;
```

두 표현 모두 같은 의미와 같은 행동을 하도록 되어있다. 다시 말해서 템플릿 안에 들어있는 *class* 키워드와 *typename* 키워드는 동일한 의미이다. *typename* 키워드는 클래스를 생성할 때 활용하는 *class* 키워드와 혼동되지 않도록 나중에 추가된 키워드이다.

예를 들면, C++ STL에 두 값 중에 더 큰 값을 구하는 `max(x,y)` 함수가 있다. `max(x,y)` 함수는 아래와 같이 정의될 수 있다.

``` cpp
template <typename Type>
Type max(Type a, Type b) {
    return a > b ? a : b;
}
```

위에 정의된 하나의 함수가, 여러가지 다른 형태의 자료형(int, double, float)에 대하여 동작을 하게 된다.

템플릿이 아니라 오버로딩으로 구현하고자 했다면 아래와 같이 각각의 변수형에 대해 각각의 함수를 정의해 주어야 한다.

``` cpp
int max(int a, int b) {
    return a > b ? a : b;
}

double max(double a, double b) {
    return a > b ? a : b;
}

float ...

long ....
```

컴파일 과정 중에 해당 함수가 어떤 자료형으로 호출이 될지 결정이 될 때 실제 함수가 생성이 되도록 되어 있다.

``` cpp
#include <iostream>

int main()
{
  // This will call max <int> (by argument deduction)
  std::cout << max(3, 7) << std::endl;
  // This will call max<double> (by argument deduction)
  std::cout << max(3.0, 7.0) << std::endl;
  // This type is ambiguous, so explicitly instantiate max<double>
  std::cout << max<double>(3, 7.0) << std::endl;
  return 0;
}
```

앞 두 형태의 경우, 컴파일러는 들어오는 자료 형태를 각각 `int`와 `double`로 추론한다. 세 번째 형태는, 컴파일러가 추론에 실패한다. 왜냐하면, 인자로 넘어오는 두가 자료형이 정확하게 같다고 정의되어 있기 때문이다. 이럴 경우, 해당 함수 template은 `(y < x)`를 만족하는, [카피 컨스트럭터](https://ko.wikipedia.org/wiki/copy_constructor "wikilink") 형태의 어떠한 형태로도 인스턴스화된다. 사용자 정의 타입의 경우에는, `<`연산자가 class의 [오버로드](https://ko.wikipedia.org/wiki/operator_overloading "wikilink") 적용을 받아, 적법할 때 인스턴스화된다.

### 클래스 템플릿

클래스 템플릿은 클래스를 템플릿 변수에따라 생성할 수 있게 하는 기능이다. 클래스 템플릿은 [컨테이너](../Page/컨테이너.md "wikilink")의 용도로 많이 쓰인다. [C++ 표준 라이브러리에는](../Page/C++_표준_라이브러리.md "wikilink") 다수의 템플릿들이 있는데, 벡터와 같은 컨테이너들은 [표준 템플릿 라이브러리로부터](../Page/표준_템플릿_라이브러리.md "wikilink") 유래했다.

이렇게 Type마다 하나의 함수를 추가하여야 했을 것이다.

## 각주

## 외부 링크

  - [Demonstration of the Turing-completeness of C++ templates](http://matt.might.net/articles/c++-template-meta-programming-with-lambda-calculus/) (Lambda calculus implementation)

[분류:제네릭 프로그래밍](https://ko.wikipedia.org/wiki/분류:제네릭_프로그래밍 "wikilink") [분류:메타프로그래밍](https://ko.wikipedia.org/wiki/분류:메타프로그래밍 "wikilink") [분류:C++](https://ko.wikipedia.org/wiki/분류:C++ "wikilink")

1.