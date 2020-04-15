> This article is converted from Wikipedia: [C 날짜와 시간 함수](https://ko.wikipedia.org/wiki/C_날짜와_시간_함수).


**C 날짜와 시간 함수**는 날짜와 시간 조작 명령을 구현하는 [C 프로그래밍 언어의](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink") [표준 라이브러리의](../Page/표준_라이브러리.md "wikilink") 함수들의 모임이다.\[1\]

## 함수 개요

**time.h**는 [C 언어의](https://ko.wikipedia.org/wiki/C_언어 "wikilink") [표준 라이브러리로](../Page/C_표준_라이브러리.md "wikilink"), 시간과 날짜를 얻거나 조작하는 함수들을 포함하고 있다.

| 함수                                                                                                                                                            | 설명                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| 시간 조작                                                                                                                                                         |                                                  |
| clock_t **clock** ( void );                                                                                                                                  | 프로그램이 시작될 때부터 지난 시간(단위ms)을 반환한다.                 |
| double **difftime** ( time_t time2, time_t time1 );                                                                                                         | time2와 time1의 차이를 반환한다.                          |
| time_t **time** ( time_t \* timer );                                                                                                                        | timer가 NULL이 아니면 timer가 가리키는 변수에 현재 시간을 채운다.     |
| 변환                                                                                                                                                            |                                                  |
| char \* **asctime** ( const struct tm \* timeptr );                                                                                                           | timeptr이 가리키는 구조체를 문자열로 변환한다.                    |
| char \* **[ctime](https://ko.wikipedia.org/wiki/ctime "wikilink")** ( const time_t \* timer );                                                               | timer가 가리키는 변수를 문자열로 변환한다.                       |
| time_t **mktime** ( struct tm \* timeptr );                                                                                                                  | timeptr이 가리키는 구조체를 time_t 형식으로 변환한다.            |
| struct tm \* **gmtime** ( const time_t \* timer );                                                                                                           | timer가 가리키는 변수를 UTC 시간 기준으로 구조체로 변환해 그 주소를 반환한다. |
| struct tm \* **localtime** ( const time_t \* timer );                                                                                                        | timer가 가리키는 변수를 지역 시간 기준으로 구조체로 변환해 그 주소를 반환한다.  |
| size_t **[strftime](https://ko.wikipedia.org/wiki/strftime "wikilink")** ( char \* ptr, size_t maxsize, const char \* format, const struct tm \* timeptr ); | 시간을 문자열로 서식화한다.                                  |
|                                                                                                                                                               |                                                  |

## 변수 · 상수 · 형식

| 이름                                                         | 설명                                                                                       |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| 상수                                                         |                                                                                          |
| NULL                                                       | [널 포인터의](../Page/널_포인터.md "wikilink") 약어인 상수. 이 상수는 메모리의 어떤 유효한 위치의 개체도 가리키지 않는 포인터 값이다. |
| CLOCKS_PER_SEC                                           | 초당 ms 수(=1000)이다.                                                                        |
| 형식 정의                                                      |                                                                                          |
| size_t                                                    | sizeof 연산자의 결과값을 나타내는 정수이다.                                                              |
| clock_t                                                   | 틱 수를 저장하는 형식이다.                                                                          |
| [time_t](https://ko.wikipedia.org/wiki/time_t "wikilink") | UTC 1970년 1월 1일 0시 0분 0초를 기준으로 하는 초 단위의 시간을 저장하는 형식이다.                                   |
|                                                            |                                                                                          |

## 구조체 · 공용체 · 열거 형식

  - struct **tm** - 날짜와 시간을 나타내는 구조체이다.
      - int **tm_sec** - 초(0\~59)
      - int **tm_min** - 분(0\~59)
      - int **tm_hour** - 시(0\~23)
      - int **tm_mday** - 일(1\~31)
      - int **tm_mon** - 월(0\~11)
      - int **tm_year** - 년(1900년 기준)
      - int **tm_wday** - 요일(일요일부터 시작, 0\~6)
      - int **tm_yday** - 연중 일자(0\~365)
      - int **tm_isdst** - 서머타임 설정 여부

## 각주

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink") [분류:시간](https://ko.wikipedia.org/wiki/분류:시간 "wikilink")

1.