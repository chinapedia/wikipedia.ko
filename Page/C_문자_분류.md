> This article is converted from Wikipedia: [C 문자 분류](https://ko.wikipedia.org/wiki/C_문자_분류).


**C 문자 분류**는 [C 프로그래밍 언어에서](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink") [ANSI C 표준 라이브러리의](../Page/C_표준_라이브러리.md "wikilink") 함수에 의해 제공되는 명령의 하나이다.

**ctype.h**는 [C 언어의](https://ko.wikipedia.org/wiki/C_언어 "wikilink") [표준 라이브러리로](../Page/C_표준_라이브러리.md "wikilink"), 문자들을 조건에 맞는지 검사하고 변환하는 함수들을 포함하고 있다.

## 함수

| 함수                             | 설명                                                         |
| ------------------------------ | ---------------------------------------------------------- |
| 문자 검사                          |                                                            |
| int **isalnum** ( int c );     | c가 *알파벳 또는 숫자*이면 0이 아닌 값을 반환한다.                            |
| int **isalpha** ( int c );     | c가 *알파벳*이면 0이 아닌 값을 반환한다.                                  |
| int **iscntrl** ( int c );     | c가 *[제어 문자](../Page/제어_문자.md "wikilink")*이면 0이 아닌 값을 반환한다. |
| int **isdigit** ( int c );     | c가 *숫자*이면 0이 아닌 값을 반환한다.                                   |
| int **isgraph** ( int c );     | c가 *그래픽 문자*이면 0이 아닌 값을 반환한다.                               |
| int **islower** ( int c );     | c가 *소문자*이면 0이 아닌 값을 반환한다.                                  |
| int **isprint** ( int c );     | c가 *출력할 수 있는 문자*이면 0이 아닌 값을 반환한다.                          |
| int **ispunct** ( int c );     | c가 *구두점 문자*이면 0이 아닌 값을 반환한다.                               |
| int **isspace** ( int c );     | c가 *공백 문자*이면 0이 아닌 값을 반환한다.                                |
| int **isupper** ( int c );     | c가 *대문자*이면 0이 아닌 값을 반환한다.                                  |
| int **isxdigit** ( int c );    | c가 *16진 숫자*이면 0이 아닌 값을 반환한다.                               |
| 문자 변환                          |                                                            |
| int **tolower** ( int c );     | c를 소문자로 변환한다.                                              |
| int **toupper** ( int c );     | c를 대문자로 변환한다.                                              |
| int **__toascii** ( int c ); | c를 아스키 코드로 변환한다.                                           |
|                                |                                                            |

## 함수 대조

X로 표시된 부분은 해당 함수가 0 아닌 값을 반환한다.

| 범위          | 문자                                     | iscntrl | isspace | isupper | islower | isalpha | isdigit | isxdigit | isalnum | ispunct | isgraph | isprint |
| ----------- | -------------------------------------- | ------- | ------- | ------- | ------- | ------- | ------- | -------- | ------- | ------- | ------- | ------- |
| 0x00 - 0x08 | [제어 문자](../Page/제어_문자.md "wikilink")   | X       |         |         |         |         |         |          |         |         |         |         |
| 0x09 - 0x0D | 공백 제어 문자 '\\t','\\f','\\v','\\n','\\r' | X       | X       |         |         |         |         |          |         |         |         |         |
| 0x0E - 0x1F | 제어 문자                                  | X       |         |         |         |         |         |          |         |         |         |         |
| 0x20        | 공백 ' '                                 |         | X       |         |         |         |         |          |         |         |         | X       |
| 0x21 - 0x2F | \!"\#$%&'()\*+,-./                     |         |         |         |         |         |         |          |         | X       | X       | X       |
| 0x30 - 0x39 | `0123456789`                           |         |         |         |         |         | X       | X        | X       |         | X       | X       |
| 0x3A - 0x40 | :;\<=\>?@                              |         |         |         |         |         |         |          |         | X       | X       | X       |
| 0x41 - 0x46 | `ABCDEF`                               |         |         | X       |         | X       |         | X        | X       |         | X       | X       |
| 0x47 - 0x5A | `GHIJKLMNOPQRSTUVWXYZ`                 |         |         | X       |         | X       |         |          | X       |         | X       | X       |
| 0x5B - 0x60 | \[\\\]^_\`                            |         |         |         |         |         |         |          |         | X       | X       | X       |
| 0x61 - 0x66 | `abcdef`                               |         |         |         | X       | X       |         | X        | X       |         | X       | X       |
| 0x67 - 0x7A | `ghijklmnopqrstuvwxyz`                 |         |         |         | X       | X       |         |          | X       |         | X       | X       |
| 0x7B - 0x7E | {|}\~                                  |         |         |         |         |         |         |          |         | X       | X       | X       |
| 0x7F        | 제어 문자 (DEL)                            | X       |         |         |         |         |         |          |         |         |         |         |
|             |                                        |         |         |         |         |         |         |          |         |         |         |         |

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")