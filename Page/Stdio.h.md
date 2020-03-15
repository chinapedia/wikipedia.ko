> This article is converted from Wikipedia: [Stdio.h](https://ko.wikipedia.org/wiki/Stdio.h).


**stdio.h**은 Standard Input/Output library (표준입출력 라이브러리)의 약어로써, [C 언어의](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") [표준 라이브러리](https://ko.wikipedia.org/wiki/C_언어_표준_라이브러리 "wikilink") 함수의 [매크로](https://ko.wikipedia.org/wiki/매크로_\(컴퓨터_과학\) "wikilink") 정의, 상수, 여러 형의 입출력 함수가 포함된 헤더 파일이다. 1970년대, 벨 연구소의 [마크 레스크가](https://ko.wikipedia.org/wiki/마크_레스크 "wikilink") 쓴 "portable I/O package"\[1\]로부터 내려저 왔다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서는 호환성을 이유로 `stdio.h` 헤더 파일이 포함되어 있는 것과 마찬가지로 **cstdio**도 [std](../Page/C++_표준_라이브러리.md "wikilink") [이름공간](../Page/이름공간.md "wikilink")에서 `stdio.h`의 함수와 형식이 선언되어 있다.

## 예제

라이브러리 함수 (및 변종들)는 [헤더 파일에](../Page/헤더_파일.md "wikilink") 정의되어 있다. 그러므로, 프로그래머는 헤더 파일에 정의된 함수를 사용하기 위해 반드시 `stdio.h` 헤더 파일을 소스 코드에 포함해야 한다.

``` c
#include <stdio.h>

int main()
{
    int ch;

    while ((ch = getchar()) != EOF)
        putchar(ch);

    putchar('\n');

    return 0;
}
```

위의 [프로그램은](https://ko.wikipedia.org/wiki/컴퓨터_프로그램 "wikilink") 바이트에 의해 바이트로 표준 입력으로 입력하고, 표준 출력으로 출력한다. 그리고 출력의 끝에 [개행 문자를](https://ko.wikipedia.org/wiki/개행_문자 "wikilink") 추가한다.

## 멤버 함수

`stdio.h`에 선언되어 있는 함수는 일반적으로 파일 조작 함수와 콘솔 입출력 함수 둘로 구분된다.

| 이름                                                                                                             | 해설                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| 파일 조작 함수                                                                                                       |                                                                                                                                         |
| [`fopen``   ``freopen`](https://ko.wikipedia.org/wiki/fopen "wikilink"),                                       | 파일을 읽거나 쓴다.                                                                                                                             |
| [`fclose`](https://ko.wikipedia.org/wiki/fclose "wikilink")                                                    | 파일을 닫는다.                                                                                                                                |
| [`remove`](https://ko.wikipedia.org/wiki/remove "wikilink")                                                    | 파일을 삭제한다.                                                                                                                               |
| [`rename`](https://ko.wikipedia.org/wiki/rename "wikilink")                                                    | 파일 이름을 바꿉니다.                                                                                                                            |
| [`rewind`](https://ko.wikipedia.org/wiki/rewind_\(C\) "wikilink")                                              | 파일 위치를 초기화한다.\[2\]                                                                                                                      |
| [`tmpfile`](https://ko.wikipedia.org/wiki/tmpfile "wikilink")                                                  | 임시 파일을 만들고 연다. [fclose](https://ko.wikipedia.org/wiki/fclose "wikilink")()로 닫으면 임시 파일이 삭제된다.                                            |
| 콘솔 입출력 함수                                                                                                      |                                                                                                                                         |
| [`clearerr`](https://ko.wikipedia.org/wiki/clearerr "wikilink")                                                | [end-of-file](https://ko.wikipedia.org/wiki/end-of-file "wikilink")와 주어진 스트림에 대한 오류 지시자를 지운다.                                           |
| [`feof`](https://ko.wikipedia.org/wiki/feof "wikilink")                                                        | [end-of-file](https://ko.wikipedia.org/wiki/end-of-file "wikilink") 지시자가 주어진 스트림으로 설정되어 있는지 검사한다.                                       |
| [`ferror`](https://ko.wikipedia.org/wiki/ferror "wikilink")                                                    | 오류 지시자가 주어진 스트림으로 설정되어 있는지 검사한다.                                                                                                        |
| [`fflush`](https://ko.wikipedia.org/wiki/fflush "wikilink")                                                    | 보류 중인 버퍼된 **출력**을 주어진 스트림의 파일에 강제로 쓴다.                                                                                                  |
| [`fgetpos`](https://ko.wikipedia.org/wiki/fgetpos "wikilink")                                                  | 첫 번째 변수 (FILE \*) 부터 두 번째 변수 (fpos_t \*)의 파일 위치 지시자를 저장한다.                                                                             |
| [`fgetc`](https://ko.wikipedia.org/wiki/fgetc "wikilink")                                                      | 파일로부터 한 개의 문자를 리턴한다.                                                                                                                    |
| [`fgets`](https://ko.wikipedia.org/wiki/fgets "wikilink")                                                      | 파일로부터 문자열을 읽는다. (파일의 끝이거나 개행 문자의 끝)                                                                                                     |
| [`fputc`](https://ko.wikipedia.org/wiki/fputc "wikilink")                                                      | 한 문자를 파일에 입력한다.                                                                                                                         |
|                                                                                                                |                                                                                                                                         |
| [`fseek`](https://ko.wikipedia.org/wiki/fseek "wikilink")                                                      | 파일을 찾는다.                                                                                                                                |
| [`fsetpos`](https://ko.wikipedia.org/wiki/fsetpos "wikilink")                                                  | 기억된 첫 번째 인수(FILE \*) 두 번째 인수(fpos_t \*) 까지의 파일 위치 지시자를 설정한다.                                                                           |
| [`fread`](https://ko.wikipedia.org/wiki/fread "wikilink")                                                      | 파일로부터 데이터를 읽어들입니다.                                                                                                                      |
| [`fwrite`](https://ko.wikipedia.org/wiki/fwrite "wikilink")                                                    | 파일로부터 데이터를 쓴다.                                                                                                                          |
| [`getc`](https://ko.wikipedia.org/wiki/getc "wikilink")                                                        | 주어진 스트림으로부터 문자를 읽고 리턴한다. 강화된 파일 지시자로서, 주어진 스트림을 한 번 이상으로 평가하는 [fgetc](https://ko.wikipedia.org/wiki/fgetc "wikilink")와 같은 효과를 내는 매크로이다. |
| [`getchar`](https://ko.wikipedia.org/wiki/getchar "wikilink")                                                  | [getc](https://ko.wikipedia.org/wiki/getc "wikilink")([stdin](https://ko.wikipedia.org/wiki/stdin "wikilink"))와 같은 효과를 냅니다.             |
| [`gets`](https://ko.wikipedia.org/wiki/gets "wikilink")                                                        | stdin이 개행문자를 발생시키고 인수에 저장할 때까지 문자를 읽는다.                                                                                                 |
| [`printf``   ``vprintf`](https://ko.wikipedia.org/wiki/printf "wikilink"),                                     | 표준 출력 스트림에 출력한다.                                                                                                                        |
| [`fprintf``   ``vfprintf`](https://ko.wikipedia.org/wiki/fprintf "wikilink"),                                  | 파일로 출력한다.                                                                                                                               |
| [`sprintf``   ``snprintf,``   ``vsprintf,``   ``vsnprintf`](https://ko.wikipedia.org/wiki/sprintf "wikilink"), | 문자 배열로 출력한다. ([C 문자열](https://ko.wikipedia.org/wiki/C_문자열 "wikilink"))                                                                  |
| [`perror`](https://ko.wikipedia.org/wiki/perror "wikilink")                                                    | [stderr](https://ko.wikipedia.org/wiki/stderr "wikilink")에 오류 메시지를 쓴다.                                                                  |
| [`putc`](https://ko.wikipedia.org/wiki/putc "wikilink")                                                        | 스트림에 문자를 쓴다.                                                                                                                            |
| [`putchar``   ``fputchar`](https://ko.wikipedia.org/wiki/putchar "wikilink"),                                  | [putc](https://ko.wikipedia.org/wiki/putc "wikilink")(stdout)와 같은 효과를 낸다.                                                               |
| [`scanf``   ``vscanf`](https://ko.wikipedia.org/wiki/scanf "wikilink"),                                        | 표준 입력 스트림으로 입력한다.                                                                                                                       |
| [`fscanf``   ``vfscanf`](https://ko.wikipedia.org/wiki/fscanf "wikilink"),                                     | 파일로 입력한다.                                                                                                                               |
| [`sscanf``   ``vsscanf`](https://ko.wikipedia.org/wiki/sscanf "wikilink"),                                     | 문자 배열로부터 입력한다. (예: [C 문자열](https://ko.wikipedia.org/wiki/C_문자열 "wikilink"))                                                             |
| [`setbuf``   ``setvbuf`](https://ko.wikipedia.org/wiki/setbuf "wikilink"),                                     | 주어진 스트림에 버퍼링 모드로 전환한다.                                                                                                                  |
| [`tmpnam`](https://ko.wikipedia.org/wiki/tmpnam "wikilink")                                                    | 임시 파일을 만듭니다.                                                                                                                            |
| [`ungetc`](https://ko.wikipedia.org/wiki/ungetc "wikilink")                                                    | 문자를 스트림의 역순으로 읽는다                                                                                                                       |
| [`puts`](https://ko.wikipedia.org/wiki/puts_\(C\) "wikilink")                                                  | `stdout`에 문자, 문자열을 출력한다.                                                                                                                |

## 멤버 상수

| 이름                                                            | 해설                                                                                             |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| [`EOF`](https://ko.wikipedia.org/wiki/End-of-file "wikilink") | end-of-file 절을 가리키는 용도로 사용되는 `int`형의 음의 정수.                                                    |
| `BUFSIZ`                                                      | `setbuf()` 함수에 의해 버퍼 크기를 나타내는 정수.                                                              |
| `FILENAME_MAX`                                                | 충분히 열 수 있는 저장 가능한 파일 이름의 `char`형의 배열 크기.                                                       |
| `FOPEN_MAX`                                                   | 동시에 열 수 있는 파일의 개수; 최소 8                                                                        |
| `_IOFBF`                                                      | "input/output fully buffered"의 약어. 이 정수값은 `setvbuf()` 함수에 넘겨서 버퍼화된 블록의 스트림을 열기 위해 입출력에 요구한다.   |
| `_IOLBF`                                                      | "input/output line buffered"의 약어. 이 정수값은 `setvbuf()` 함수에 넘겨서 버퍼화된 라인의 스트림을 열기 위해 입출력에 요구한다.    |
| `_IONBF`                                                      | "input/output not buffered"의 약어. 이 정수값은 `setvbuf()` 함수에 넘겨서 버퍼화 되지 않은 것을 스트림을 열기 위해 입출력에 요구한다. |
| `L_tmpnam`                                                    | `char` 배열이 `tmpnam()` 함수를 발생시킬 정도의 충분한 크기                                                      |
| `NULL`                                                        | [널 포인터의](../Page/널_포인터.md "wikilink") 약어인 매크로 상수. 이 상수는 메모리의 어떤 유효한 위치의 개체도 가리키지 않는 포인터 값이다.   |
| `SEEK_CUR`                                                    | `fseek()` 함수의 요구한 현재 파일 위치의 상대 위치를 나타내는 정수.                                                    |
| `SEEK_END`                                                    | `fseek()` 함수의 요구한 end of file의 상대 위치를 나타내는 정수.                                                 |
| `SEEK_SET`                                                    | `fseek()` 함수의 요구한 파일의 시작점의 상대 위치를 나타내는 정수.                                                     |
| `TMP_MAX`                                                     | `tmpnam()` 함수가 생성가능한 최대 파일명 길이 (최소 25자)                                                        |

## 멤버 변수

| 이름                                                                           | 해설                                               |
| ---------------------------------------------------------------------------- | ------------------------------------------------ |
| [`stdin`](https://ko.wikipedia.org/wiki/표준_스트림#표준_입력_\(stdin\) "wikilink")   | 표준 입력 스트림(일반적으로 키보드)를 참조하는 `FILE`에 대한 포인터.       |
| [`stdout`](https://ko.wikipedia.org/wiki/표준_스트림#표준_출력_\(stdout\) "wikilink") | 표준 출력 스트림(일반적으로 디스플레이 터미널)을 참조하는 `FILE`에 대한 포인터. |
| [`stderr`](https://ko.wikipedia.org/wiki/표준_스트림#표준_오류_\(stderr\) "wikilink") | 표준 오류 스트림(항상 디스플레이 터미널)을 참조하는 `FILE`에 대한 포인터.    |

## 멤버 형식

`stdio.h` 헤더에 정의된 데이터 형식이 포함되어 있다:

  - `FILE` - 입출력 작동에 필요한 파일/텍스트 스트림에 대한 정보를 포함하는 구조다.
      - [파일 서술자](https://ko.wikipedia.org/wiki/파일_서술자 "wikilink")
      - 현재 스트림 위치.
      - end-of-file 지시자
      - 오류 지시자
      - 적용 가능할 경우, 스트림의 버퍼에 대한 포인터.
  - `fpos_t` - 유일하게 파일의 바이트 위치를 식별할 수 있는 비 배열 형식.
  - `size_t` - [`sizeof`](https://ko.wikipedia.org/wiki/sizeof "wikilink") 연산자의 결과값을 나타내는 형식의 양의 [정수](https://ko.wikipedia.org/wiki/정수 "wikilink")형.

## 참고

<references/>

[\*](https://ko.wikipedia.org/wiki/분류:Stdio.h "wikilink") [분류:C 표준 라이브러리 헤더](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리_헤더 "wikilink")

1.
2.