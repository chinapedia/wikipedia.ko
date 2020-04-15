> This article is converted from Wikipedia: [C 수식 함수](https://ko.wikipedia.org/wiki/C_수식_함수).


**C 수식 함수**는 기초 수식 함수들을 구현하는 [C 프로그래밍 언어의](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink") [표준 라이브러리](../Page/표준_라이브러리.md "wikilink") 안의 함수들의 모임이다.\[1\]\[2\]

## 함수 개요

**math.h**는 여러 수학 함수들을 포함하는 [C 언어의](https://ko.wikipedia.org/wiki/C_언어 "wikilink") [표준 라이브러리이다](../Page/C_표준_라이브러리.md "wikilink"). 대부분의 함수들이 부동소수점을 다루며, 각도는 라디안을 사용한다.

| 함수                                                                        | 설명                                        |
| ------------------------------------------------------------------------- | ----------------------------------------- |
| 삼각 함수                                                                     |                                           |
| double **sin** ( double x );                                              | 사인 x를 구한다.                                |
| double **cos** ( double x );                                              | 코사인 x를 구한다.                               |
| double **tan** ( double x );                                              | 탄젠트 x를 구한다.                               |
| 역 삼각 함수                                                                   |                                           |
| double **asin** ( double x );                                             | 아크 사인 x를 구한다.                             |
| double **acos** ( double x );                                             | 아크 코사인 x를 구한다.                            |
| double **atan** ( double x );                                             | 아크 탄젠트 x를 구한다.                            |
| double **atan2** ( double y, double x );                                  | 아크 탄젠트 y/x를 구한다.                          |
| 쌍곡선 함수                                                                    |                                           |
| double **sinh** ( double x );                                             | 하이퍼볼릭 사인 x를 구한다.                          |
| double **cosh** ( double x );                                             | 하이퍼볼릭 코사인 x를 구한다.                         |
| double **tanh** ( double x );                                             | 하이퍼볼릭 탄젠트 x를 구한다.                         |
| 지수 · 대수 함수                                                                |                                           |
| double **exp** ( double x );                                              | e<sup>x</sup>를 구한다.                       |
| double **[frexp](../Page/부동소수점.md "wikilink")** ( double x, int \* exp ); | 지수를 exp가 가리키는 변수에 저장하고 가수를 반환한다.          |
| double **ldexp** ( double x, int exp );                                   | x \* 2<sup>exp</sup>를 반환한다.               |
| double **log** ( double x );                                              | log<sub>e</sub> x를 구한다.                   |
| double **log10** ( double x );                                            | log<sub>10</sub> x를 구한다.                  |
| double **modf** ( double x, double \* intpart );                          | 정수부를 intpart가 가리키는 변수에 저장하고 소수부를 반환한다.    |
| 거듭제곱 · 거듭제곱근 · 올림 · 내림 · 절댓값 · 나머지 함수                                     |                                           |
| double **pow** ( double x, double y );                                    | x<sup>y</sup>를 구한다.                       |
| double **sqrt** ( double x );                                             | \(\sqrt{x}\)를 구한다.                        |
| double **ceil** ( double x );                                             | x보다 작지 않은 가장 작은 정수를 구한다.                  |
| double **floor** ( double x );                                            | x보다 크지 않은 가장 큰 정수를 구한다.                   |
| double **abs** ( double x );                                              | x의 [절댓값](../Page/절댓값.md "wikilink")을 구한다. |
| double **fmod** ( double x, double y );                                   | x를 y로 나눈 나머지를 구한다.                        |
|                                                                           |                                           |

## XSI에서 추가된 것들

이 함수들은 ANSI나 표준 C에는 등록되지 않았다.

| 이름                               | 설명                               |
| -------------------------------- | -------------------------------- |
| double **j0**(double x)          | 밑이 0인 제 1종 베셀 함수                 |
| double **j1**(double x)          | 밑이 1인 제 1종 베셀 함수                 |
| double **jn**(int n,double x)    | 밑이 n인 제 1종 베셀 함수                 |
| double **scalb**(double x,int y) | *x* \* `FLT_RADIX`<sup>*y*</sup> |
| double **y0**(double x)          | 밑이 0인 제 2종 베셀 함수                 |
| double **y1**(double x)          | 밑이 1인 제 2종 베셀 함수                 |
| double **yn**(int n,double x)    | 밑이 n인 제 2종 베셀 함수                 |

The `double`-to-string conversion functions `ecvt`, `fcvt` and `gcvt` have been deprecated in favour of [`sprintf`](https://ko.wikipedia.org/wiki/sprintf "wikilink").

## 변수 · 상수 · 형식

| 이름           | 설명                                                  |
| ------------ | --------------------------------------------------- |
| 상수           |                                                     |
| HUGE_VAL    | 아주 큰 값을 나타낸다. 수학 계산에서 결과가 너무 커 오버플로우가 나면 이 값을 반환한다. |
| M_E         | 자연상수 e                                              |
| M_LOG2E     | log<sub>2</sub>e                                    |
| M_LOG10E    | log<sub>10</sub>e                                   |
| M_LN2       | log<sub>e</sub>2                                    |
| M_LN10      | log<sub>e</sub>10                                   |
| M_PI        | 원주율 π                                               |
| M_PI_2     | \({\pi \over 2}\)                                   |
| M_PI_4     | \({\pi \over 4}\)                                   |
| M_1_PI     | \({1 \over \pi}\)                                   |
| M_2_PI     | \({2 \over \pi}\)                                   |
| M_2_SQRTPI | \({2 \over \sqrt{\pi} }\)                           |
| M_SQRT2     | \(\sqrt{2}\)                                        |
| M_1_SQRT2  | \({1 \over \sqrt{2}}\)                              |
|              |                                                     |

## 예제

다음 예제는 부동소수점 수들의 거듭제곱을 출력한다. 컴파일시에 -lm 옵션을 추가해주어야 한다

``` c
int main (void)
{
  printf ("7 ^ 3 = %lf\n", pow (7.0,3));
  printf ("4.73 ^ 12 = %lf\n", pow (4.73,12));
  printf ("32.01 ^ 1.54 = %lf\n", pow (32.01,1.54));
  return 0;
}
```

**실행 결과**

    7 ^ 3 = 343.000000
    4.73 ^ 12 = 125410439.217423
    32.01 ^ 1.54 = 208.036691

## 각주

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.
2.