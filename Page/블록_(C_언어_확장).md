> This article is converted from Wikipedia: [블록 \(C 언어 확장\)](https://ko.wikipedia.org/wiki/블록_\(C_언어_확장\)).


**블록**은 [Clang](https://ko.wikipedia.org/wiki/Clang "wikilink") [C](../Page/C_\(프로그래밍_언어\).md "wikilink")/[C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [Objective-C](https://ko.wikipedia.org/wiki/Objective-C "wikilink") 컴파일러에서 지원하는 [람다 표현식과](../Page/람다_대수.md "wikilink") 유사한 형태의 언어 확장이다. 공식적으로는 Mac OS X 10.6 및 iOS 4.0 이후 버전에서만 지원되지만,\[1\] [서드 파티의](../Page/서드_파티_개발자.md "wikilink") 지원으로 하위 일부 버전(Mac OS X 10.5, iOS 2.2 이상)이나 비 Apple 시스템에서도 사용할 수 있다.\[2\]

블록은 당초 Apple 사에 의해 자사의 Grand Central Dispatch 아키텍처를 기반으로 한 프로그램 개발을 용이하게 하려는 목적으로 디자인되었지만,\[3\]\[4\] 해당 아키텍처가 아닌 컴퓨터에서도 여타 언어의 [클로저와](../Page/클로저_\(프로그래밍_언어\).md "wikilink") 비슷한 방식으로 활용될 수 있다. 블록은 Apple에 의해 자사 전용 [GNU 컴파일러 모음](../Page/GNU_컴파일러_모음.md "wikilink") 브랜치와\[5\] [Clang LLVM](../Page/LLVM.md "wikilink") 업스트림에 구현된 상태이며, 런타임 라이브러리 역시 [LLVM 프로젝트의](../Page/LLVM.md "wikilink") 일환으로 배포되고 있다. 한편, 블록의 *문법*은 Khronos 그룹에 의해 커널 안에 또다른 커널을 네스팅시키는 용도로 [OpenCL](../Page/OpenCL.md "wikilink") 2.0 버전부터 사용되고 있기도 하다.\[6\]

블록은 기본적으로 일반적인 함수와 정의 및 용도 면에서 매우 유사한데, 특수하게도 정의되는 시점의 컨텍스트에서 메모리 상태를 캡쳐해둘 수 있다는 점에서 일반적인 함수와 상이하다. 이를 구현하기 위해 블록은 정의 시점에 [함수 콜 스택에](../Page/콜_스택.md "wikilink") 존재하는 지역 변수들의 값을 캡쳐하여 보관해두는데, 이 캡쳐값은 후에 블록이 함수와 비슷한 방식으로 호출될 때에 참조된다.

블록은 변수에 대입되거나 함수 간에 인자로 전달될 수 있는데, 일반적인 C 언어의 함수는 함수 자체가 아니라 함수의 *포인터*를 이용해 간접적으로 다뤄진다는 점에서 차이가 있다. 단, 블록을 정의된 스코프 바깥에서 사용하기 위해서는 Block_copy라는 특수한 연산자로 표시해주어야 한다.

블록 호출은 함수 호출과 구문상으로 동일하다.

## 예시

주변 스코프의 가변 상태를 캡쳐하는 간단한 예제로 정수 범위 [반복자](../Page/반복자.md "wikilink")를 들 수 있다.\[7\]

  - blocks-test.c

<!-- end list -->

``` objc
#include <stdio.h>
#include <Block.h>
typedef int (^IntBlock)();

IntBlock MakeCounter(int start, int increment) {
    __block int i = start;

    return Block_copy( ^(void) {

        /* 이 정의에 제어 흐름이 닿는 시점에 상위 스코프의 지역 변수
         * i를 캡쳐하여 보관한다. 이후 블록이 호출될 때 아래 코드에서 읽는
         * 값은 이때 캡쳐된 값. 일종의 static 변수와 유사하게도, i에 쓰인 값은
         * 이 캡쳐된 값에 갱신되어 저장된다. */

        int ret = i;
        i += increment;
        return ret;
    });

}

int main(void) {
    IntBlock mycounter = MakeCounter(5, 2);
    printf("First call: %d\n", mycounter());
    printf("Second call: %d\n", mycounter());
    printf("Third call: %d\n", mycounter());

    /* 복사한 블록을 해제하기 */
    Block_release(mycounter);

    return 0;
}
```

### 컴파일 및 실행

``` console
$ clang -fblocks blocks-test.c   # Mac OS X
$ # clang -fblocks blocks-test.c -lBlocksRuntime   # Linux
$ ./a.out
First call: 5
Second call: 7
Third call: 9
```

## GCC 지역 함수와의 관계

블록은 GCC의 언어 확장인 *지역 함수*와 외형적인 유사성이 있지만,\[8\] 세부적인 디자인이나 구현에서 비롯된 차이점들이 다수 존재한다.

  - GCC의 지역 함수는 정의된 지점의 스코프 바깥에서 호출될 수 없지만, 블록은 정의된 스코프 바깥에서도 Block_copy를 통해 복사된 후에 호출될 수 있다.

<!-- end list -->

  - GCC의 지역 함수는 일반적인 함수 포인터를 통해 참조될 수 있지만, 블록은 표준에 정의되지 않은 완전히 새로운 *개념*의 포인터 사용하므로 함수 포인터를 이용해 참조될 수 없다. 이 점에선 블록을 일종의 *뚱뚱한* 함수 포인터(Fat function pointer)를 이용한 지역 함수 구현으로 볼 수도 있다.
  - GCC의 지역 함수는 본인을 주소로 참조하는 코드가 존재하는 경우에 한하여 실행 가능한 "[썽크](https://ko.wikipedia.org/wiki/:en:Thunk "wikilink")"를 [스택에](../Page/콜_스택.md "wikilink") 동적으로 생성시키는데, 이를 위해 일부 [콜 스택](../Page/콜_스택.md "wikilink") 메모리가 실행 권한을 부여받는다. [실행 가능한 스택은](https://ko.wikipedia.org/wiki/실행_가능한_스택 "wikilink") 일반적으로 잠재적인 [보안 취약점으로](../Page/보안_취약점.md "wikilink") 간주되는데, 반면 블록은 실행 가능한 썽크를 필요로하지 않으므로 해당 취약점을 발생시키지 않는다.

## 참조

  - [클로저 (컴퓨터 과학)](../Page/클로저_\(컴퓨터_프로그래밍\).md "wikilink")
  - [변수 영역](../Page/변수_영역.md "wikilink")
  - [람다 함수](https://ko.wikipedia.org/wiki/람다_함수 "wikilink")
  - 스파게티 스택
  - 썽크 (함수형 프로그래밍)
  - [XNU](../Page/XNU.md "wikilink")
  - [C++11](../Page/C++11.md "wikilink") ("람다 표현식" 포함)

## 참고 문헌

## 외부 링크

  -
  -
[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:함수 (프로그래밍)](https://ko.wikipedia.org/wiki/분류:함수_\(프로그래밍\) "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.