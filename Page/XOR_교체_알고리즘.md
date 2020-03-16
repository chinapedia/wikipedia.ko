> This article is converted from Wikipedia: [XOR  ](https://ko.wikipedia.org/wiki/XOR__).


**XOR 교체 알고리즘**은 임시 [변수](https://ko.wikipedia.org/wiki/변수 "wikilink")를 두지 않고, 두 개의 변수를 [배타적 논리합](../Page/배타적_논리합.md "wikilink")(XOR) [비트 연산을](https://ko.wikipedia.org/wiki/비트_연산 "wikilink") 이용하여 [교체하는](../Page/교체_연산.md "wikilink") 알고리즘이다. 이 알고리즘은 [컴퓨터 프로그래밍](../Page/컴퓨터_프로그래밍.md "wikilink") 분야에서 [프로세서의](../Page/중앙_처리_장치.md "wikilink") 최적화 능력이 부족했을 때 대안으로 자주 사용되었다.

## 개요

XOR 교체 알고리즘은 세 개의 XOR 연산을 사용하여 임시 변수 없이 두 변수를 교환한다. [의사코드](../Page/의사코드.md "wikilink")로는 다음과 같이 표현할 수 있다.

`X ← X XOR Y`
`Y ← X XOR Y`
`X ← X XOR Y`

보통 위의 세 줄은 각각 하나씩 세 개의 [기계어](../Page/기계어.md "wikilink") 명령에 대응될 수 있다. 예를 들어 [IBM System/370에서](https://ko.wikipedia.org/wiki/IBM_System/370 "wikilink") 위 코드는 다음과 같은 어셈블리 코드로 변환된다:

`XR    R1,R2`
`XR    R2,R1`
`XR    R1,R2`

여기서 R1과 R2는 [레지스터이고](../Page/프로세서_레지스터.md "wikilink") XR은 첫째 레지스터와 둘째 레지스터의 값을 XOR해서 그 결과값을 첫째 레지스터에 저장하는 명령이다.

하지만 이 알고리즘은 *X*와 *Y*가 같은 기억 장소를 가리킬 경우 제대로 동작하지 않는다. 예상했던 대로라면 두 값이 같으므로 아무 일도 일어 나지 않아야 하지만, 위 알고리즘은 첫 문장에서 *X*와 *Y*를 모두 0으로 초기화해 버리기 때문에 기억 장소에는 0이 저장된다. 만약 위의 알고리즘을 임의의 경우에도 쓸 수 있게 하려면 다음과 같은 수정이 필요하다.

`만약 X ≠ Y이면,`
`    X ← X XOR Y`
`    Y ← X XOR Y`
`    X ← X XOR Y`

## 증명

비트 문자열에 대한 XOR [이항 연산은](https://ko.wikipedia.org/wiki/이항_연산 "wikilink") 다음과 같은 성질을 갖는다. 여기서 \(\otimes\)는 XOR 연산자를 뜻한다.

  - **L1.** [교환법칙](../Page/교환법칙.md "wikilink"): \(A \otimes B = B \otimes A\)
  - **L2.** [결합법칙](../Page/결합법칙.md "wikilink"): \((A \otimes B) \otimes C = A \otimes (B \otimes C)\)
  - **L3.** [항등원](../Page/항등원.md "wikilink")의 존재: 어떤 \(A\)에 대하여서도, \(A \otimes Z = A\)가 되는 값 \(Z = 0\)이 존재한다.
  - **L4.** 각 원소에 대해 유일한 [역원](https://ko.wikipedia.org/wiki/역원 "wikilink")의 존재: 각 \(A\)에 대하여, \(A \otimes A^{-\!1} = Z\)가 되는 \(A^{-\!1}\)가 존재한다.
      - **L4a.** 각 원소의 역원은 사실 자기 자신임: \(A \otimes A = 0\)

**L1**부터 **L4**까지의 성질은 [아벨 군](../Page/아벨_군.md "wikilink")(ablian group)의 정의이다. **L4a**는 XOR 연산의 구조적 성질에 해당하는 것이며, 아벨 군이나 다른 군에 꼭 있는 성질은 아니다.

`R1`과 `R2`의 두 레지스터에 값 *A*와 *B*가 저장되어 있을 때, XOR 교체 알고리즘을 수행할 때 각각의 결과는 다음과 같다.

| 과정 | 수행된 명령           | `R1`의 값                                     | `R2`의 값                                     | 사용된 성질         |
| -- | ---------------- | ------------------------------------------- | ------------------------------------------- | -------------- |
| 1  | (초기 상태)          | *A*                                         | *B*                                         | \--            |
| 2  | `R1 ← R1 XOR R2` | *A*^*B*                                     | *B*                                         | \--            |
| 3  | `R2 ← R1 XOR R2` | *A*^*B* = *B*^*A*                           | (*A*^*B*)^*B* = *A*^(*B*^*B*) = *A*^0 = *A* | L1, L2, L4, L3 |
| 4  | `R1 ← R1 XOR R2` | (*B*^*A*)^*A* = *B*^(*A*^*A*) = *B*^0 = *B* | *A*                                         | L2, L3, L4     |

## 코드 예제

다음은 XOR 교체 알고리즘을 구현한 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 코드이다.

``` c
void swap(int *x, int *y)
{
    if (x != y) {
        *x ^= *y;
        *y ^= *x;
        *x ^= *y;
    }
}
```

이 코드는 두 포인터가 서로 다른 메모리 공간을 가리킬 때에만 교체 연산을 수행해서 문제를 제거한다.

이 코드는 종종 다음과 같은 형태로 쓰이기도 한다.

``` c
if (x != y) *x ^= *y ^= *x ^= *y;
```

하지만 이 코드는 [시퀀스 포인트의](https://ko.wikipedia.org/wiki/시퀀스_포인트 "wikilink") 부재 때문에 올바른 C 코드가 아니며, 이 코드의 수행 결과는 컴파일러에 따라 다를 수 있다.

## 실제 사용에서의 장단점

XOR 교체 알고리즘은 대부분의 현대적인 프로세서에서는 임시 변수를 사용하는 방법보다 더 느린데, 그 이유 중 하나로는 임시 변수를 사용하는 방법은 여러 명령어를 동시에 실행할 수 있도록 (명령어 수준 병렬성) 최적화하기가 더 쉽기 때문이다. XOR 교체 알고리즘은 3 연산 모두 데이터 의존성 (Read-After-Write)을 만들기에 반드시 순서대로만 실행해야한다. 따라서 현대 비순차 프로세서나 VLIW 컴파일러가 XOR 교체 알고리즘을 최적화할 수 있는 방법은 거의 없다.

반면, XOR 교체 알고리즘은 속도가 그리 빠르지 않아도 되고 메모리 (혹은 캐시) 사용을 최소화해야 하는 환경에서는 유용하게 사용될 수 있다. 따라서 이 방식은 임베디드 개발 환경에서 많이 이용된다.

## 같이 보기

  - [교체 연산](../Page/교체_연산.md "wikilink")

## 외부 링크

  - [두 변수 값 바꾸기에 대한 고찰](http://minjang.egloos.com/1241820)
  - [swap](https://web.archive.org/web/20140330155228/http://talkera.org.cp-in-1.webhostbox.net/wp/?p=60)

[분류:컴퓨터 프로그래밍](https://ko.wikipedia.org/wiki/분류:컴퓨터_프로그래밍 "wikilink")

[pl:Zamiana wartości zmiennych](https://ko.wikipedia.org/wiki/pl:Zamiana_wartości_zmiennych "wikilink")