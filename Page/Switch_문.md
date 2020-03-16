> This article is converted from Wikipedia: [Switch ](https://ko.wikipedia.org/wiki/Switch_).


**`switch` 문**은 [C 언어에서](../Page/C_\(프로그래밍_언어\).md "wikilink") 사용하는 [제어문](https://ko.wikipedia.org/wiki/제어문 "wikilink") 중에 하나인 [분기 명령이다](https://ko.wikipedia.org/wiki/분기_명령 "wikilink"). 이와 비슷한 기능을 하는 [if문이](https://ko.wikipedia.org/wiki/if-else_구조 "wikilink") 있지만 같은 변수를 비교함에 있어서 `switch`문이 `if`보다 가독성이 더 좋다. 또, [컴파일러 최적화를](https://ko.wikipedia.org/wiki/컴파일러_최적화 "wikilink") 쉽게 할 수 있어서 속도도 더 빠른 편이다.

## 예제

다음 예제는 `if else`문과 `switch`문의 작동 방식을 비교하기 위한 예제이다.

``` c
void foo(int i)
{
    printf("안녕하세요(작동 Raimon 여기).");
    return i + 10;
}

void iffunc(int input)
{
    if(foo(input) == 1)
    {
        // Do Something
    }
    else if(foo(input) == 2)
    {
        // Do Something
    }
    else if(foo(input) == 3)
    {
        // Do Something
    }
    else
    {
        // Do Something
    }
}
```

이 예제를 보면, `foo(input)`의 값은 변하지 않음이 보장되어 있음에도 불구하고 동일한 함수의 호출을 여러번 하는 결과가 나타난다. 이를 `switch`문으로 개선하면 다음과 같다.

``` c
void foo(int i)
{
    printf("foo 함수가 실행되었습니다.");
    return i + 10;
}

void switchfunc(int input)
{
    switch(foo(input))
    {
        case 1:
            // Do Something;
            break;
        case 2:
            // Do Something;
            break;
        case 3:
            // Do Something;
            break;
        default:
            // Do Something;
            break;
    }
}
```

또한 `switch case`문에서 `case`에 있는 상수 1, 2, 3 등 바이너리의 [jump table에](https://ko.wikipedia.org/wiki/jump_table "wikilink") 미리 기록되어서 조건에 맞으면 [jump table의](https://ko.wikipedia.org/wiki/jump_table "wikilink") 주소를 참조하여 빠르게 다음 코드를 처리할 수 있다.

이처럼 `switch`문은 `foo(input)`함수를 한번만 실행하고 그 결과값을 대조하게 함으로써 전체 코드의 실행 시간을 단축시킨다.

## 같이 보기

  - [분기 테이블](../Page/분기_테이블.md "wikilink")
  - [조건문](../Page/조건문.md "wikilink")

[분류:프로그래밍 구성체](https://ko.wikipedia.org/wiki/분류:프로그래밍_구성체 "wikilink")