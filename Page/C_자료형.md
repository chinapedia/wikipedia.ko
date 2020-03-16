> This article is converted from Wikipedia: [C ](https://ko.wikipedia.org/wiki/C_).


[C 프로그래밍 언어에서](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink") **자료형**은 데이터의 특징을 결정하는 [메모리 위치나](../Page/메모리_주소.md "wikilink") [변수](https://ko.wikipedia.org/wiki/변수 "wikilink")의 선언이다.

C 언어는 [정수](../Page/정수.md "wikilink")와 [실수](https://ko.wikipedia.org/wiki/실수 "wikilink")형과 같은 기초적인 산술형, 그리고 배열과 복합형을 만드는 문법을 제공한다.

## 기초 자료형

### 기초 자료형의 속성에 대한 인터페이스

**limits.h**는 [C 언어의](https://ko.wikipedia.org/wiki/C_언어 "wikilink") [표준 라이브러리로](../Page/C_표준_라이브러리.md "wikilink"), [정수형](../Page/정수형.md "wikilink")의 범위를 나타내는 상수들을 정의한다.

#### 상수

| 이름           | 설명                      | 최소 크기(더 클 수 있음)          |
| ------------ | ----------------------- | ------------------------ |
| CHAR_BIT    | char의 비트 수              | 8                        |
| SCHAR_MIN   | signed char의 최솟값        | \-127                    |
| SCHAR_MAX   | signed char의 최댓값        | 127                      |
| UCHAR_MAX   | unsigned char의 최댓값      | 255                      |
| CHAR_MIN    | char의 최솟값               | SCHAR_MIN 또는 0          |
| CHAR_MAX    | char의 최댓값               | SCHAR_MAX 또는 UCHAR_MAX |
| MB_LEN_MAX | 멀티바이트 문자의 최대 바이트 수      | 1                        |
| SHRT_MIN    | short int의 최솟값          | \-32767                  |
| SHRT_MAX    | short int의 최댓값          | 32767                    |
| USHRT_MAX   | unsigned short int의 최댓값 | 65535                    |
| INT_MIN     | int의 최솟값                | \-2147483647             |
| INT_MAX     | int의 최댓값                | 2147483647               |
| UINT_MAX    | unsigned int의 최댓값       | 4294967295               |
| LONG_MIN    | long int의 최솟값           | \-2147483647             |
| LONG_MAX    | long int의 최댓값           | 2147483647               |
| ULONG_MAX   | unsigned long int의 최댓값  | 4294967295               |
|              |                         |                          |

## 같이 보기

  - [C 언어의 문법](../Page/C_언어의_문법.md "wikilink")

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink") [분류:자료형](https://ko.wikipedia.org/wiki/분류:자료형 "wikilink")