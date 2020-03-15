> This article is converted from Wikipedia: [Scanf](https://ko.wikipedia.org/wiki/Scanf).


**scanf**는 주어진 문자열 스트림 소스에서 지정된 형식으로 데이터를 읽어내는 기능으로 [C 프로그래밍 언어로부터](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 유래했으며 많은 프로그래밍 언어에 쓰이고 있다.

`scanf`의 기본 형태는 다음과 같다:
:

``` c
int scanf(const char *format, ...);
```

## 사용법

`scanf`는 [C에서](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 비롯했는데, 표준 입력(종종 명령 줄 인터페이스)으로부터 숫자나 다른 입력한 데이터타입을 입력 받아 읽어낸다.

아래는 C 언어에서 각 줄의으로부터 언포맷된 10진 정수값 가변 숫자를 읽는 코드이다:(쓸만함)

``` c
#include <stdio.h>
int
main(void)
{
    int n;
    while (scanf("%d", &n));
        printf("%d\n", n);
    return 0;
}
```

## 같이 보기

  - [`printf`](https://ko.wikipedia.org/wiki/printf "wikilink")
  - [C 프로그래밍 언어](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink")
  - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")
  - [PHP](https://ko.wikipedia.org/wiki/PHP "wikilink")
  - [형식 문자열 공격](https://ko.wikipedia.org/wiki/형식_문자열_공격 "wikilink")

## 외부 링크

  -
## 응용

scanf을 이용한 계산기이다

출저 : [hyhgo1님의 블로그](https://hyhgo1.blog.me/221194170230)

``` c
#include <stdio.h>

int calculator( num1 , num2 , symbol ){
    if(symbol  == 1 ) {
        printf("%d + %d = %d입니다\n", num1, num2, num1+num2);
    } else if( symbol == 2 ) {
        printf("%d - %d = %d입니다\n", num1, num2, num1-num2);
    } else if( symbol == 3 ) {
        printf("%d * %d = %d입니다\n", num1, num2, num1*num2);
    } else if( symbol == 4 ) {
        printf("%d / %d = %d입니다\n", num1, num2, num1/num2);
    } else if( symbol == 5 ) {
        printf("%d % %d = %d입니다\n1", num1, num2, num1%num2);
    } else {
        printf("잘못 입력하셨습니다.");
    }
    return 1;
}

int main() {
    int A;
    int N1;
    int N2;
    printf("계산할 기호는 \n1는 더하기\n2는 빼기\n3는 곱하기\n4는 나누기\n5는 나누기의 나머지\n");
    printf("계산할 기호를 입력하세요...\n");
    scanf("%d", &A);
    printf("첫번째 수를 입력하세요...\n");
    scanf("%d", &N1);
    printf("두번째 수를 입력하세요...\n");
    scanf("%d", &N2);
    calculator( N1 , N2 , A );
    printf("프로그램 종료");
    return 0;
}
```

[분류:Stdio.h](https://ko.wikipedia.org/wiki/분류:Stdio.h "wikilink")