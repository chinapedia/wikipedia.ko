> This article is converted from Wikipedia: [Int \(C 프로그래밍 언어\)](https://ko.wikipedia.org/wiki/Int_\(C_프로그래밍_언어\)).


정수형을 처리하기 위한 변수로, [정수형](../Page/정수형.md "wikilink")(integer)의 약자이다. [char](https://ko.wikipedia.org/wiki/char "wikilink")와 같은 구조와 특성을 가지며 char가 8비트 인데 비해, 16, 32, 64비트의 처리 단위로 CPU 마다 다르다는 차이가 있다. 변수 사용 시, [unsigned](https://ko.wikipedia.org/wiki/unsigned "wikilink")을 이용하면 부호없는 정수를 처리 할 수 있다. char는 모든 CPU에서 무조건 8비트인데 비해, int의 처리 단위 비트는 CPU마다 차이가 있다. 보통 8비트 CPU는 16비트의 처리 단위를 가지며, 32비트 CPU 이면 32비트의 처리 단위를 갖는 것이 일반적인 정수형 처리이다. 숫자를 표시하는 방식은 [signed](https://ko.wikipedia.org/wiki/signed "wikilink") 일 경우의 [2의 보수](../Page/2의_보수.md "wikilink") 체계를 사용한다. char와 마찬가지 CPU의 ALU을 사용하여 연산 처리 한다. 8비트 CPU는 16비트 처리 단위인 int의 16비트를 처리하기 위해 여러개의 [기계어](../Page/기계어.md "wikilink") 코드를 사용한다. 따라서 8비트 CPU는 32비트 CPU에 비해 처리 시간이 더 걸린다.

## 정수체계

[C](../Page/C_\(프로그래밍_언어\).md "wikilink")/[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")는 다른 고급언어에 비해 CPU의 특성을 최대한 이용한 언어이다. CPU는 보통 정수형 ALU을 갖는데, 이것을 최대한 활용한 변수체계를 사용한다. 모든 CPU는 8비트 처리는 기본적으로 제공한다. 현재에는 4비트 CPU는 거의 사용하지 않으므로 전자공학관련 개발자라도 8비트 이상의 CPU을 사용할 것이다. 8비트 이상의 CPU을 생각하면 모든 정수형의 비트 처리는 기본이 8비트이다. 8비트 이상에서의 정수형은 CPU마다 다르므로 개발전에 미리 컴파일러의 특성을 이해해야 한다. 그럼 왜 이렇게 int가 16 또는 32비트를 사용하는 것인가는 바로 지금 까지 설명한 CPU의 특성을 최대한 활용하도록 컴파일러를 구성 했기 때문이다.

### 정수형의 처리와 비트수

8비트는 무조건 8비트 이므로 어떤 CPU 이든 상관 없다. int는 short과 long을 이용하여 비트 수를 변경할 수 있다.

  - 8비트 CPU의 일반적인 처리 비트수

<!-- end list -->

  - char: 8비트 정수형
  - int: 16비트 정수형
  - long int: 32비트 정수형

<!-- end list -->

  - 32비트 CPU의 일반적인 처리 비트수

<!-- end list -->

  - char: 8비트 정수형
  - short: 16비트 정수형
  - int: 32비트 정수형
  - long long: 64비트 정수형

여기서 short이나 long을 사용할 대는 기본적으로 int을 생략 할 수도 있다. 8비트 CPU에서는 무조건 char이므로 여기에 short나 long을 붙일 필요가 없기 때문이다.

### 정수형 부호지정

  - \[signed\] char|int: 부호를 갖는 정수형으로 [2의 보수체계를](../Page/2의_보수.md "wikilink") 사용한다.
  - unsigned char|int: 부호가 없는 정수형으로 [이진법](../Page/이진법.md "wikilink")과 같은 수의 배치를 갖는다.

## 선언 및 초기화

int 는 선언이며 int=(숫자)의 값까지 붙이면 초기화라고 간단히 설명할 수 있다.

## 정수형 변수의 [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")에서의 처리 방식

CPU는 성능에 따라 최대 처리 단위 비트가 결정되어 있고, 보통 ALU와 레지스터가 연결되어 데이터가 처리된다. 정수형 처리는 기본적으로 모든 CPU에서 제공하면, 정수형 처리가 가능한 기계어 코드에 의해 ALU에서 계산된다. 전역변수의 경우 메모리에 변수가 설정 되지만, 지역변수는 스택이나 레지스터를 이용하여 숫자를 처리된다. 지역변수를 스택에 할당 할 것인가 레지스터에 할당할 것인가를 컴파일러의 옵션과 연관되어 컴파일된다. 즉, 속도를 최적화하도록 옵션 설정하면 레지스터에 할당 될 가능성이 높아 진다. 더불어 함수 내에서 얼마나 많은 변수를 선언 할 것인가 와도 상관이 있다. 연산을 할 때, 메모리에 할당될 경우 변수의 정수 값은 CPU의 레지스터 내로 옮겨오고, ALU가 필요한 경우 ALU을 통해 연산 하고 다시 결과는 레지스터에 저장된다. 이 레지스터 값은 다음에 어떤 코드가 있는냐에 따라 메모리에 저장할 것인가 부분적으로 버릴 것인가가 결정된다. 정수를 연산할 때, ALU는 몇 비트 계산을 할것인가와 부호(sign 또는 unsign)연산을 할것인가를 결정 해야 한다. 그리고 이것은 기계어 코드에 의해 지정된다. 예를 들어 32비트 CPU는 ALU가 8,16,32 비트 단위로 한번의 기계어 코드에 의해 계산된다. 만약 32비트라고 해서 8비트 처리를 제공하지 않고 32비트 단위로 만 처리한다면 심각한 자원(메모리, 속도 등) 낭비가 초래된다. 이런 CPU 특성을 이용하여 선언된 변수는 컴파일러가 어떤 기계어 코드를 사용 할것인가를 결정하고 실행 처리가 이루어진다.

## 배열

정수형 배열은 여러개의 정수를 저장하기 위해 사용한다. \[ \]을 사용한다.

``` c
int a[10];
int *pa[10];
```

[전역 변수의](../Page/전역_변수.md "wikilink") 초기화는 다음과 같이 할 수 있다.

``` c
int a[4][3] = {
    { 10, -2, 1 },
    { 20, 54, 2 },
    { 30 },
    { 0 }
};

int *pat1[2] = { a[0], a[1] };
int *pat2[2] = { &a[0][0], &a[1][0] };
```

전역변수의 초기화는 main 함수가 실행되기 전에 CONST 메모리 영역에서 초기값을 갖는 변수 영역으로 복사된다. 프로그램이 처음 실행 될때 일관적으로 복사 되는 것이다. 따라서 데이터를 초기화 하기나 값을 설정하는 기계어 코드는 없다.

[지역 변수의](../Page/지역_변수.md "wikilink") 초기화는 다음과 같이 할 수 있다.

``` c
int main(int argc, char **argv)
{
    int aa[2][3] = { { 10, -2, 1 }, { 20, 54 } };
    // ...
    printf("%d\n", aa[1][2]);

    return 0;
}
```

이와 같이 함수 내에 초기화 되는 경우는 함수가 실행 될 때 초기화 하는 코드가 컴파일러에 의해 넣어 진다. 전역변수와는 초기화 동작 방식이 다르다.

## 같이 보기

  - [char](https://ko.wikipedia.org/wiki/char "wikilink")
  - [long](https://ko.wikipedia.org/wiki/long "wikilink")
  - [unsigned](https://ko.wikipedia.org/wiki/unsigned "wikilink")
  - [const](https://ko.wikipedia.org/wiki/const "wikilink")
  - [float](https://ko.wikipedia.org/wiki/float "wikilink")

## 외부 링크

  - [ISO C Working Group official website](http://www.open-std.org/jtc1/sc22/wg14/)

  - [ISO/IEC 9899](http://www.open-std.org/JTC1/SC22/WG14/www/standards). Official C99 documents.

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:자료형](https://ko.wikipedia.org/wiki/분류:자료형 "wikilink")