> This article is converted from Wikipedia: [Stdlib.h](https://ko.wikipedia.org/wiki/Stdlib.h).


**stdlib.h**는 [C 언어의](https://ko.wikipedia.org/wiki/C_언어 "wikilink") [표준 라이브러리로](../Page/C_표준_라이브러리.md "wikilink"), 문자열 변환, [의사 난수](https://ko.wikipedia.org/wiki/의사_난수 "wikilink") 생성, 동적 메모리 관리 등의 함수들을 포함하고 있다.

## 함수

| 함수                                                                                                                                                                                                    | 설명                                                                                        |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 문자열 변환                                                                                                                                                                                                |                                                                                           |
| int **atoi** ( const char \* str );                                                                                                                                                                   | str을 int로 변환한다.                                                                           |
| long int **atol** ( const char \* str );                                                                                                                                                              | str을 long으로 변환한다.                                                                         |
| double **atof** ( const char \* str );                                                                                                                                                                | str을 **double**으로 변환한다.                                                                   |
| long int **strtol** ( const char \* str, char \*\* endptr, int base );                                                                                                                                | str을 base진법으로 long으로 변환한 뒤 endptr\!=NULL이면 숫자가 끝난 후 첫 문자의 위치를 endptr에 반환한다.               |
| unsigned long int **strtoul** ( const char \* str, char \*\* endptr, int base );                                                                                                                      | str을 base진법으로 unsigned long으로 변환한 뒤 endptr\!=NULL이면 숫자가 끝난 후 첫 문자의 위치를 endptr에 반환한다.      |
| double **strtod** ( const char \* str, char \*\* endptr );                                                                                                                                            | str을 base진법으로 double으로 변환한 뒤 endptr\!=NULL이면 숫자가 끝난 후 첫 문자의 위치를 endptr에 반환한다.             |
| 의사 난수 생성                                                                                                                                                                                              |                                                                                           |
| int **rand** ( void );                                                                                                                                                                                | 0부터 RAND_MAX 사이의 의사 난수를 반환한다.                                                            |
| void **srand** ( unsigned int seed );                                                                                                                                                                 | 의사 난수 발생기를 seed로 초기화한다. 보통 seed는 time(NULL)로 설정된다.                                        |
| 동적 메모리 관리                                                                                                                                                                                             |                                                                                           |
| void \* **malloc** ( size_t size );                                                                                                                                                                  | size 바이트의 메모리를 힙에서 할당하여 반환한다.                                                             |
| void \* **calloc** ( size_t num, size_t size );                                                                                                                                                     | (num \* size) 바이트의 메모리를 힙에서 할당하여 반환한다.                                                    |
| void \* **realloc** ( void \* ptr, size_t size );                                                                                                                                                    | ptr이 가리키는 메모리를 size 바이트만큼 힙에서 재할당하여 반환한다.                                                 |
| void **free** ( void \* ptr );                                                                                                                                                                        | ptr이 가리키는 메모리를 해제한다.(할당했으면 반드시 해제해야 한다.)                                                  |
| 프로세스 제어                                                                                                                                                                                               |                                                                                           |
| void **abort** ( void );                                                                                                                                                                              | 현재 프로세스를 비정상적으로 종료한다.                                                                     |
| int **atexit** ( void ( \* function ) (void) );                                                                                                                                                       | 프로세스가 정상적으로 종료되었을 때 실행할 함수를 지정한다.                                                         |
| void **exit** ( int status );                                                                                                                                                                         | 현재 프로세스를 정상적으로 종료한다. status는 부모 프로세스에게 전달된다.                                              |
| char \* **[getenv](https://ko.wikipedia.org/wiki/getenv "wikilink")** ( const char \* name );                                                                                                         | name에 해당하는 [환경 변수를](../Page/환경_변수.md "wikilink") 반환한다.                                    |
| int **system** ( const char \* command );                                                                                                                                                             | command의 시스템 명령을 실행한다.                                                                    |
| 검색/정렬                                                                                                                                                                                                 |                                                                                           |
| void \* **[bsearch](https://ko.wikipedia.org/wiki/bsearch "wikilink")** ( const void \* key, const void \* base, size_t num, size_t size, int ( \* comparator ) ( const void \*, const void \* ) ); | [이진 검색을](../Page/이진_검색_알고리즘.md "wikilink") 한다.                                            |
| void **[qsort](https://ko.wikipedia.org/wiki/qsort "wikilink")** ( void \* base, size_t num, size_t size, int ( \* comparator ) ( const void \*, const void \* ) );                                 | [퀵 정렬](https://ko.wikipedia.org/wiki/퀵_정렬 "wikilink") 알고리즘을 사용하여 정렬한다.                    |
| 정수 산술                                                                                                                                                                                                 |                                                                                           |
| int **abs** ( int n ); long int **labs** ( long int n );                                                                                                                                              | n의 절댓값을 반환한다.                                                                             |
| div_t **div** ( int numerator, int denominator ); ldiv_t **ldiv** ( long numerator, long denominator );                                                                                             | numerator를 denominator로 나누어 div_t 또는 ldiv_t 구조체에 quot 멤버에는 몫을, rem 멤버에는 나머지를 채운 뒤 반환한다. |
|                                                                                                                                                                                                       |                                                                                           |

## 변수{{·}} 상수{{·}} 형식

| 이름            | 설명                                                                                       |
| ------------- | ---------------------------------------------------------------------------------------- |
| 상수            |                                                                                          |
| NULL          | [널 포인터의](../Page/널_포인터.md "wikilink") 약어인 상수. 이 상수는 메모리의 어떤 유효한 위치의 개체도 가리키지 않는 포인터 값이다. |
| RAND_MAX     | rand 함수가 반환하는 가장 큰 값이다.                                                                  |
| EXIT_SUCCESS | exit 함수의 인자로 전달되는 프로그램의 성공적 종료를 의미하는 매크로 상수이다.                                           |
| EXIT_FAILURE | exit 함수의 인자로 전달되는 프로그램의 실패에 따른 종료를 의미하는 매크로 상수이다.                                        |
| 형식 정의         |                                                                                          |
| size_t       | sizeof 연산자의 결과값을 나타내는 정수(unsigned int)이다.                                                |
|               |                                                                                          |

## 구조체{{·}} 공용체{{·}} 열거 형식

  - struct **div_t** - div 함수가 반환하는 구조체이다.
      - int **quot** - div 함수에 의한 나눗셈에서의 몫이다.
      - int **rem** - div 함수에 의한 나눗셈에서의 나머지이다.
  - struct **ldiv_t** - ldiv 함수가 반환하는 구조체이다.
      - long **quot** - ldiv 함수에 의한 나눗셈에서의 몫이다.
      - long **rem** - ldiv 함수에 의한 나눗셈에서의 나머지이다.

[분류:C 표준 라이브러리 헤더](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리_헤더 "wikilink")