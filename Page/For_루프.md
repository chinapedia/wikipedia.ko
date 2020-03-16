> This article is converted from Wikipedia: [For ](https://ko.wikipedia.org/wiki/For_).


[섬네일](https://ko.wikipedia.org/wiki/파일:For-loop-diagram.png "wikilink") [컴퓨터 프로그래밍에서](../Page/컴퓨터_프로그래밍.md "wikilink") **for 루프**는 [반복문](https://ko.wikipedia.org/wiki/반복문 "wikilink")의 일종으로, 특정한 부분의 코드가 반복적으로 수행될 수 있도록 한다. for 루프는 [while 루프와](https://ko.wikipedia.org/wiki/while_루프 "wikilink") 같은 다른 반복문과는 달리 일반적으로 해당 루프에 연계된 [루프 변수가](https://ko.wikipedia.org/wiki/루프_변수 "wikilink") 존재하며, 그 변수의 비교 및 증감을 위해서 별도의 문법을 할애한 점이 구분된다.

for 루프의 이름은 영어 표현 “”(…동안 …를 하라)에서 유래하였다. [포트란](../Page/포트란.md "wikilink")과 같은 언어에서는 for 대신 do [예약어](https://ko.wikipedia.org/wiki/예약어 "wikilink")를 사용하며 그 문법의 이름도 **do 루프**이지만, 이를 제외하고는 for 루프와 큰 차이가 없다.

## 종류

for 루프는 대부분의 [명령형 프로그래밍 언어에서](https://ko.wikipedia.org/wiki/명령형_프로그래밍_언어 "wikilink") 기본적으로 지원된다. 그러나 각 언어 별로 지원하는 for 문의 종류는 반복문인 것을 제외하고는 다음의 여러 가지로 나뉜다.

### 숫자 범위

이 종류의 for 루프는 특정한 루프 변수에 주어진 숫자 범위, 좀 더 정확하게는 [등차수열](../Page/등차수열.md "wikilink") 안의 숫자들을 대입하여 안쪽 코드를 실행하는 형식으로 이루어져 있다. 숫자 범위는 시작점과 끝점으로 대표되며, 보통은 시작점부터 1씩 커져 끝점보다 작지 않을 때까지 루프가 수행되지만 1 대신 증감될 값을 직접 선택해서 루프를 반대로 수행하거나 하는 것이 가능한 경우도 있다.

많은 [베이직](../Page/베이직.md "wikilink") 계열 언어들과 [포트란](../Page/포트란.md "wikilink") 등이 이 형태의 for 문을 지원한다. 예를 들어 다음 베이직 코드는 1부터 시작해서 10으로 끝나고, 3씩 차이 나는 숫자들(즉 1, 4, 7, 10)을 출력한다.

**`FOR`**` `*`I`*` = 1 `**`TO`**` 10 `**`STEP`**` 3`
`    `**`PRINT`**` `*`I`*
**`NEXT`**` `*`I`*

### 임의의 집합

이 종류의 for 루프는 흔히 foreach 루프라고 불리며, 숫자 범위 뿐만 아니라 특정한 집합 또는 목록 안에 있는 원소들을 순서대로 루프 변수에 대입하여 안쪽 코드를 실행하는 형식으로 이루어져 있다.

[파이썬](../Page/파이썬.md "wikilink")은 이 형태의 for 루프 이외에 다른 형태의 문법을 가지고 있지 않은 것으로 잘 알려져 있다. 파이썬에서 숫자 범위를 사용해서 for 루프를 흉내내려면 배열을 반환하는 `range` 함수(또는 [반복자](../Page/반복자.md "wikilink")만을 구현하는 `xrange` 자료형)를 사용하여 다음과 같이 쓸 수 있다.

``` python
for i in range(1, 11, 3):
    print i
```

반면 많은 다른 언어들은 숫자 범위를 사용하는 형태와 집합을 사용하는 형태 두 가지 모두 지원하며, 전자를 for, 후자를 foreach라는 예약어로 구분하곤 한다. [PHP](../Page/PHP.md "wikilink")나 [C\#가](../Page/C_샤프.md "wikilink") 대표적이다.

### 조건절의 추가

일부 언어들은 보통의 for 루프에 while 루프와 같은 조건절을 추가하기도 한다. 이런 형태의 문법은 [ALGOL 68에서](https://ko.wikipedia.org/wiki/ALGOL_68 "wikilink") 처음 소개되고 [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink")에서도 사용되었다. 다음의 ALGOL 68 코드는 1부터 42까지 3씩 증가하며 반복하되, i가 10보다 크면 반복을 중단한다. (따라서 앞의 코드들과 같이 1, 4, 7, 10만을 출력한다.)

``` algol68
for i from 1 by 3 to 42 while i≤10
do
  print((i,newline));
od
```

### 초기화-조건식-증감문 형식

[섬네일](https://ko.wikipedia.org/wiki/파일:For-loop-diagram.png "wikilink")

이 종류의 for 루프는 [C로부터](../Page/C_\(프로그래밍_언어\).md "wikilink") 유래한 문법을 사용하는 대부분의 언어들이 지원하며, 세 개의 식 내지는 문장으로 루프를 정의한다.

  - 초기화: 루프 안에서 사용할 변수를 초기화한다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")의 경우 `int i = 0`과 같이 지역 변수를 선언하면서 초기화하는 것도 가능하다.
  - 조건식: 루프 안쪽 코드가 실행되기 전에 참인지의 여부가 검사되며, 참이 아니면 루프를 종료한다. 이 식은 초기화 직후에도 평가될 수 있다.
  - 증감문: 루프 안쪽 코드가 실행된 후에 실행되는 문장이다. 보통 루프 변수를 증감시키는 용도로 쓰인다.

다음의 C++ 코드는 초기화, 조건식, 증감문을 모두 사용하는 예제이다.

``` cpp
for (int i = 1; i <= 10; i += 3)
    printf("%d\n", i);

/* C의 경우 다음 코드가 필요하다. */
int i;
for (i = 1; i <= 10; i += 3)
    printf("%d\n", i);
```

각 식은 아무것도 없이 [세미콜론](https://ko.wikipedia.org/wiki/세미콜론 "wikilink") 구분자만을 둬서 생략할 수 있다. 만약 조건식이 생략되면, 조건식은 항상 참으로 평가되며 이는 [무한 루프를](https://ko.wikipedia.org/wiki/무한_루프 "wikilink") 구현하는 데 사용된다. 다음은 세 식을 모두 생략하여 같은 의미를 구현한 것이다.

``` cpp numberLines
int i = 1;
for (;;) {
    printf("%d\n", i);
    i += 3;
    if (i > 10) break;
}
```

## 문법과 의미론

for 루프는 루프 변수의 초기화나 증감 과정을 안쪽 코드에 명시적으로 집어 넣고 조건문만을 남겨서 [while 루프로](https://ko.wikipedia.org/wiki/while_루프 "wikilink") 변환할 수 있다. 다만 일부 경우, 변수를 접근할 수 있는 코드 영역이 변환 도중 바뀔 수 있기 때문에 주의를 요한다.

C 계열의 언어들이 제공하는 [break 문이나](https://ko.wikipedia.org/wiki/break_문 "wikilink") [continue 문과](https://ko.wikipedia.org/wiki/continue_문 "wikilink") 같이, 일부 언어는 루프를 도중에 중단하거나 뒤에 실행될 코드를 뛰어 넘고 증감문 또는 조건 검사로 바로 넘어 가는 명령을 지원하기도 한다.

[파이썬](../Page/파이썬.md "wikilink")과 같은 언어는 for 루프가 break 문과 같은 다른 명령에 의하여 갑작스럽게 종료되지 않고, 조건문이 실패하여 ‘평범하게’ 종료되는 경우에 한해 실행되는 코드를 지정해 줄 수 있다.

## 예제

### [C 언어](https://ko.wikipedia.org/wiki/C_언어 "wikilink")

``` c numberLines
#include <stdio.h>

int main(void){
    int i = 5;                //i는 5이다.
    int n = 5;                //n는 5이다.

    for(i=1; i <= n; i++) {   // i는 1부터 시작해서 n까지 1씩 증가한다.
        printf("Hello!\n");   // hello 를 출력한다
    }                         // 이 for문이 끝나면 콘솔 창에는 hello 가 5번 출력된다.
    return 0;
}
```

#### 응용

``` c numberLines
#include <stdio.h>

int main(void){
    int i = 5;
    int n = 5;

    for(;n;){ // n이 0 이외의 경우 계속 돌아감. 0이 입력될 때까지 프로그램은 종료되지 않음
        printf("아무 수나 입력하세요 : ");
        scanf("%d", &n);
    }
    return 0;
}
```

### [비주얼 베이직](../Page/비주얼_베이직.md "wikilink")

``` vb numberLines
Sub Main()
    Dim I,N As Integer
    N = 5 'N을 5로 바꿈
    For I = 1 To N Step 1 'I는 1부터 시작해서 N까지 1씩 증가한다.
        Debug.Print("hello")
    Next I
End Sub
```

## 같이 보기

  - [while 루프](https://ko.wikipedia.org/wiki/while_루프 "wikilink")
  - [do-while 루프](https://ko.wikipedia.org/wiki/do-while_루프 "wikilink")
  - [foreach 루프](https://ko.wikipedia.org/wiki/foreach_루프 "wikilink")

[분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink")