> This article is converted from Wikipedia: [Volatile ](https://ko.wikipedia.org/wiki/Volatile_).


C/C++ 프로그래밍 언어에서 이 키워드는 최적화 등 컴파일러의 재량을 제한하는 역할을 한다. 개발자가 설정한 개념을 구현하기 위해 코딩된 프로그램을 온전히 컴파일되도록 한다. 주로 최적화와 관련하여 **volatile**가 선언된 변수는 최적화에서 제외된다. OS와 연관되어 장치제어를 위한 주소체계에서 지정한 주소를 직접 액세스하는 방식을 지정할 수도 있다. 리눅스 커널 등의 OS에서 메모리 주소는 MMU와 연관 된 주소체계로 논리주소와 물리주소 간의 변환이 이루어진다. 경우에 따라 이런 변환을 제거하는 역할을 한다. 또한 원거리 메모리 점프 기계어 코드 등의 제한을 푼다.

## C언어 MMIO에서 적용

주로 [메모리 맵 입출력](../Page/메모리_맵_입출력.md "wikilink")(MMIO)을 제어할 때, volatile을 선언한 변수를 사용하여 컴파일러의 최적화를 못하게 하는 역할을 한다.

``` c
static int foo;

void bar(void)
{
    foo = 0;

    while (foo != 255);
}
```

foo의 값의 초기값이 0 이후, [while 루프](https://ko.wikipedia.org/wiki/while_루프 "wikilink") 안에서 foo의 값이 변하지 않기 때문에 while의 조건은 항상 [true](https://ko.wikipedia.org/wiki/true "wikilink")가 나온다. 따라서 컴파일러는 다음과 같이 최적화한다.

``` c
void bar_optimized(void)
{
    foo = 0;

    while (true);
}
```

이렇게 되면 while의 무한 루프에 빠지게 된다. 이런 최적화를 방지하기 위해 다음과 같이 **volatile**을 사용한다.

``` c
static volatile int foo;

void bar (void)
{
    foo = 0;

    while (foo != 255);
}
```

이렇게 되면 개발자가 의도한 대로, 그리고 눈에 보이는 대로 기계어 코드가 생성된다. 이 프로그램만으로는 무한루프라고 생각할 수 있지만, 만약 foo가 하드웨어 장치의 레지스터라면 하드웨어에 의해 값이 변할 수 있다. 따라서 하드웨어 값을 [폴링](https://ko.wikipedia.org/wiki/폴링 "wikilink")(poll)할 때 사용할 수 있다.

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:변수 (컴퓨터 과학)](https://ko.wikipedia.org/wiki/분류:변수_\(컴퓨터_과학\) "wikilink") [분류:동시성 제어](https://ko.wikipedia.org/wiki/분류:동시성_제어 "wikilink")