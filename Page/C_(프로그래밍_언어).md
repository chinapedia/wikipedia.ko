> This article is converted from Wikipedia: [C \(프로그래밍 언어\)](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\)).


**C**는 [1972년](../Page/1972년.md "wikilink") [켄 톰슨과](https://ko.wikipedia.org/wiki/켄_톰슨 "wikilink") [데니스 리치가](../Page/데니스_리치.md "wikilink") 벨 연구소에서 일할 당시 새로 개발된 [유닉스](../Page/유닉스.md "wikilink") [운영 체제에서](../Page/운영_체제.md "wikilink") 사용하기 위해 개발한 [프로그래밍 언어이다](../Page/프로그래밍_언어.md "wikilink"). 켄 톰슨은 BCPL언어를 필요에 맞추어 개조해서 "B"언어(언어를 개발한 벨 연구소의 B를 따서)라 명명했고, [데니스 리치가](../Page/데니스_리치.md "wikilink") 이것을 개선하여 C 언어가 탄생했다. 유닉스 시스템의 바탕 프로그램은 모두 C로 작성되었고, 수많은 운영 체제의 [커널](../Page/커널_\(컴퓨팅\).md "wikilink") 또한 C로 만들어졌다. 오늘날 많이 쓰이는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")는 C에서 객체 지향형 언어로 발전된 것이다. 또 다른 다양한 최신 언어들도 그 뿌리를 C에 두고 있다.

## 개요

C는 실질적으로 모든 컴퓨터 시스템에서 사용할 수 있도록 설계된 프로그래밍 언어이다. 예를 들어 BASIC 등과는 달리 다양한 [플랫폼에서](../Page/컴퓨팅_플랫폼.md "wikilink") [ANSI C의](../Page/ANSI_C.md "wikilink") 정의에 따르는 비교적 동일한 구현이 가능하다. 모든 C 시스템에는 정규화된 [표준 C 라이브러리가](https://ko.wikipedia.org/wiki/표준_C_라이브러리 "wikilink") 존재한다. 이런 이유와 생성된 프로그램의 높은 성능이 아직까지도 C 언어가 사랑받는 이유 중 하나이다.

이는 반면 오늘날의 널리 쓰이는 거의 모든 [운영 체제](../Page/운영_체제.md "wikilink") [커널이](../Page/커널_\(컴퓨팅\).md "wikilink") C를 이용해 구현된 이유이기도 하다. 이처럼 C는 [시스템 프로그램](https://ko.wikipedia.org/wiki/시스템_프로그램 "wikilink") 개발에 매우 적합하지만, 응용 프로그램 개발에도 많이 쓰이기도 한다.

## 역사

  - [1963년](../Page/1963년.md "wikilink") - [ALGOL 60에서](https://ko.wikipedia.org/wiki/ALGOL_60 "wikilink") [CPL이](../Page/CPL_\(프로그래밍_언어\).md "wikilink") 파생
  - [1969년](../Page/1969년.md "wikilink") - [BCPL](../Page/BCPL.md "wikilink") 개발
  - [1970년](../Page/1970년.md "wikilink") - [B 언어](../Page/B_\(프로그래밍_언어\).md "wikilink") 개발
  - [1972년](../Page/1972년.md "wikilink") - [벨 연구소](../Page/벨_연구소.md "wikilink") (Bell Laboratories) 에 있는 Dennis Ritchie가 B의 후속으로 C 개발
  - [1983년](../Page/1983년.md "wikilink") - [미국 국가 표준 협회](https://ko.wikipedia.org/wiki/미국_국가_표준_협회 "wikilink")(ANSI, American National Standards Institute) 에서 [짐 브로디](https://ko.wikipedia.org/wiki/짐_브로디 "wikilink")(Jim Brodie) 주축으로 [X3J11 위원회](https://ko.wikipedia.org/wiki/X3J11_위원회 "wikilink") 소집
  - [1983년](../Page/1983년.md "wikilink") [12월 14일](../Page/12월_14일.md "wikilink") - ANSI X3.159-1989 라는 공식명칭으로 C 언어 표준 지정
  - [1999년](../Page/1999년.md "wikilink") - [C99](../Page/C99.md "wikilink") 표준안이 ISO/IEC 9899:1999라는 명칭으로 출간됨
  - [2000년 5월](https://ko.wikipedia.org/wiki/2000년_5월 "wikilink") - ANSI의 표준으로 C99가 채택됨
  - [2011년](../Page/2011년.md "wikilink") - [12월 8일](../Page/12월_8일.md "wikilink") [C11](https://ko.wikipedia.org/wiki/C11 "wikilink") 표준안이 ISO/IEC 9899:2011라는 명칭으로 출간됨

### 초기 개발

[섬네일](https://ko.wikipedia.org/wiki/파일:Ken_Thompson_and_Dennis_Ritchie.jpg "wikilink") C 언어의 초기 개발은 1969년부터 1973년까지 4년에 걸쳐 [AT\&T 벨 연구소에서](https://ko.wikipedia.org/wiki/AT&T_벨_연구소 "wikilink") 이루어 졌으며,\[1\] [데니스 리치의](../Page/데니스_리치.md "wikilink") 말에 따르면, 가장 창의적인 작업이 이루어진 기간은 1972년이었다. 언어의 이름이 'C'인 이유는 그 특징이 'B' 언어에서 유래되었기 때문이며, [켄 톰슨에](https://ko.wikipedia.org/wiki/켄_톰슨 "wikilink") 의하면, B 언어는 BCPL 언어의 기본만 남긴 버전이다.

리치와 톰슨에 의해 초기에 [PDP-7](https://ko.wikipedia.org/wiki/PDP-7 "wikilink")의 어셈블리 언어로 구현되었던 [유닉스](../Page/유닉스.md "wikilink") 운영체제의 개발과 C 언어의 기원은 밀접하게 연관되어 있다. 결국 그들은 유닉스 운영체제를 [PDP-11](../Page/PDP-11.md "wikilink")로 포팅하기로 결정하였다. PDP-11의 기능의 일부, 특히 [바이트](../Page/바이트.md "wikilink") 접근기능을 활용하지 못하는 B 언어의 부족함이 C 언어의 초기 버전의 개발을 이끌었다.

유닉스의 초기 PDP-11 버전은 어셈블리로 개발되었다. 1973년에 `struct` 자료형의 추가로, C 언어는 유닉스의 대부분을 C로 쓸 수 있을 정도로 강력해 졌다. 유닉스는 어셈블리가 아닌 언어로 구현된 최초의 운영체제 커널 중의 하나였다.(더 빠른 사례는 [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink")로 쓰인 [Multics](https://ko.wikipedia.org/wiki/Multics "wikilink") 시스템, [ALGOL](https://ko.wikipedia.org/wiki/ALGOL "wikilink")로 쓰인 Burroughs B5000을 위한 MCP(Master Control Program)가 있다.) 1977년 경, 리치와 스티븐 C. 존슨이 유닉스 운영체제의 이식성을 향상시키기 위해, C 언어를 추가적으로 변경하였다. 존슨의 [Portable C Compiler는](https://ko.wikipedia.org/wiki/Portable_C_Compiler "wikilink") 새로운 플랫폼에서의 C의 구현의 기초가 되었다.\[2\]

### K\&R C

[섬네일](https://ko.wikipedia.org/wiki/파일:The_C_Programming_Language,_First_Edition_Cover_\(2\).svg "wikilink")

[1978년](../Page/1978년.md "wikilink")에 [브라이언 커니핸과](../Page/브라이언_커니핸.md "wikilink") [데니스 리치가](../Page/데니스_리치.md "wikilink") *The C Programming Language*라는 책의 초판을 출간했다. 커니핸과 리치의 앞 글자만 따서 C 프로그래머들에게는 "K\&R"로 불리는 이 책은, 비공식적이지만 오랫동안 C의 규격과 같은 역할을 했다. 그리하여, 이 책에서 서술하는 C의 판이 "K\&R C"란 명칭으로 불리게 되었고, 이 책의 2판에서는 후의 [ANSI C](../Page/ANSI_C.md "wikilink") 표준을 다루게 되었다.

K\&R에서 다음과 같은 기능이 등장한다.

  - 표준 입출력 라이브러리
  - `long int` 자료형
  - `unsigned int` 자료형
  - `=-`와 같은 형태의 복합 대입 연산자를 `-=` 형태로 변경
      - `i=-10`라는 코드가 원래 의도한 `i =- 10` (i의 값을 10 차감)이 아닌, `i = -10` (i의 값을 -10으로 설정)으로 해석될 수 있기 때문에 중의성을 없애기 위해서 형태를 변경했다.

### C99

C 언어 표준이 상대적으로 정적으로 남아 있었던 동안, [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")는 표준화를 위하여 계속 진화하고 있었다. 1995년에 1990년의 C 표준에 대한 규약 수정안 1이 출판되었는데, 이는 약간의 세부 사항을 교정하고 국제적 문자 세트에 대한 보다 확장된 지원을 위한 것이었다. C 표준은 1990년대 후반에 더 개정되어, 1999년 ISO/IEC 9899:1999가 출간되었고, 여기서 명시한 규범을 흔히 [C99](../Page/C99.md "wikilink")라 부른다. 이는 기술적 교정에 의하여 현재까지 3번의 수정이 있었다. 국제 C 표준은 실무 그룹 ISO/IEC JTC1/SC22/WG14에 의해 관리되고 있다.

### C11

2011년 ISO/IEC 9899:2011이 출간되었고, 간단하게 [C11](https://ko.wikipedia.org/wiki/C11 "wikilink")라고 부른다. [C11](https://ko.wikipedia.org/wiki/C11 "wikilink")이 나오기 전까지의 개발 버전을 [C1X](https://ko.wikipedia.org/wiki/C1X "wikilink")라고 부른다. 최종 개발 버전은 2011년도 4월 N1570이었다.

## 문법

C는 C 표준에 의해 규정되는 [형식 문법을](../Page/형식_문법.md "wikilink") 갖고 있다. [포트란 77과](https://ko.wikipedia.org/wiki/포트란_77 "wikilink") 같은 언어와 달리, C 소스코드는 free-form 언어로써 형식 코드에 공백을 마음대로 넣을 수 있다.

### 연산자

### 변수형

### 포인터

### 분기문

## 메모리 관리

OS에서 응용 프로그램을 실행하거나, CPU의 프로그램을 실행하기 위해 여러가지 영역으로 나누어 메모리를 할당하고 이를 메모리에 올려 실행 한다.

  - OS: 주로 [저장장치](https://ko.wikipedia.org/wiki/저장장치 "wikilink")에서 실행 파일을 메모리에 올려 실행 한다. 따라서 프로그램에 필요한 메모리는 거의 RAM에 할당하고 실행 한다.
  - CPU을 사용한 장치: OS가 없이 개발자가 설정한 메모리 배치에 따라 코드를 ROM/FLASH에 생산할 때 쓰고, 전원 공급시 실행 한다.

C 언어로 개발된 프로그램은 메모리 입장에서 다음과 같은 할당 영역으로 나누어 생각할 수 있다.

  - 정적 변수: static을 이용하여 정적 변수임을 명시하고, 단 한 번만 초기화되며 프로그램이 시작할 때 생성되어 종료될 때까지 유지된다.
  - 동적 변수: [힙](https://ko.wikipedia.org/wiki/힙 "wikilink")(HEAP)영역을 이용하여 할당 함수를 호출하여 변수 영역을 할당 받아 사용하고, 해제 함수에 의해 반납한다.
  - 자동변수: 함수나 블록({ } 이용) 안에서 선언하는 지역변수를 사용하면 [스택](../Page/스택.md "wikilink")(STACK) 영역에서 자동 할당을 받는다.

CPU을 사용하여 개발하여 장치에 넣어 코드를 실행할 때, 힙 영역을 많이 사용하지는 않는다. 따라서 필요 없다면 메모리 공간을 할당할 필요도 없고 힙관리 프로그램 코드(함수를 개발툴에서 라이브러리 형태로 제공)도 필요하지 않는다. 만약 [malloc](https://ko.wikipedia.org/wiki/malloc "wikilink") 등의 함수를 사용하면, 힙 영역을 사용하겠다는 의미 이기 때문에 힙 영역을 개발자가 선언하여 관리 해야 한다. 이 때 힙관리 프로그램 코드는 자동으로 링크 된다. 물론 저 사양의 CPU 경우, 이 함수를 제공하지 않을 수 있는 컴파일러도 있을 수 있다.

### 변수와 메모리 맵

C 언어 작성된 코드는 컴파일 과정과 링크 과정을 거치면 실행 파일이 만들어진다. 변수는 여러가지 특성이 있다.

  - 초기치를 갖는 변수
  - 초기치가 없는 변수
  - 상수 데이터

<!-- end list -->

``` c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <conio.h>

int count = 4;
char name[50] = "홍길동";
char tel[256];

///////////////////////////////////

int getTel(char *pstr)
{
  static char buff[1024];
   gets(buff);
   strcpy(pstr, buff);
   return strlen(pstr);
}

int main(int argc, char **argv)
{
  char *paddr;

   printf("이름= %s\n", name);
   getTel(tel);
   printf("전화 = %s\n", tel);
   paddr = (char*) malloc(1024);
   if (!paddr)
      return -1;
   {  // 블록 시작
       int scount;
       char *piaddr = paddr;
       for (scount = 1024;scount > count;scount--,piaddr++) {
         *piaddr = getch();  // getch 함수는 표준함수는 아니다.
         putchar(*piaddr);
         if (*piaddr == '\r')
            break;
       }
       *piaddr = 0;
       printf("주소 = %s\n", paddr);
   } // 블록 끝

   free(paddr);
   return 0;
}
```

이 프로그램 예에서 변수 별로 분리하면 다음과 같은 특성의 변수로 나눌 수 있다.

<table>
<thead>
<tr class="header">
<th><p>초기치 변수</p></th>
<th><p>int count = 4;<br />
char name[50] = "홍길동"[3];</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>초기치 없는 변수</p></td>
<td><p>char tel[256];<br />
static char buff[1024];</p></td>
</tr>
<tr class="even">
<td><p>상수</p></td>
<td><p>"이름 = %s\n"<br />
"전화 = %s\n"<br />
"주소 = %s\n"<br />
</p></td>
</tr>
<tr class="odd">
<td><p>스택<br />
(또는 레지스터[4])</p></td>
<td><p>char *paddr;<br />
char *pstr;<br />
int scount;<br />
char *piaddr;<br />
</p></td>
</tr>
<tr class="even">
<td><p>힙 (heap)</p></td>
<td><p>paddr(malloc()에서 할당된 공간)</p></td>
</tr>
</tbody>
</table>

Notes:

각 특성별로 나누어 그룹을 지어 메모리에 배치 하는데, 이것을 링커가 한다. 이렇게 그룹은 나누는 것을 세그먼트(SEGMENT) 또는 섹션(SECTION)이라는 단어를 사용한다.

위의 그룹은 가장 기본적인 내용만을 표시 한것이다. CPU와 컴파일 마다 다르다. 어떤 컴파일러는 더욱 세밀히 하기도 한다. 그리고 각 세그먼트 이름도 다르다.

Visual Studio의 맵 이름 예

| 변수형태      | SEGMENT |
| --------- | ------- |
| 초기치 변수    | DATA    |
| 초기치 없는 변수 | BSS     |
| 프로그램 코드   | TEXT    |
| 상수        | CONST   |
| 힙         | HEAP    |
| 스택        | STACK   |

컴파일마다 각 세그먼트 이름과 구조가 다르지만, 예를 들어 중요한 세그먼트 만 표시 하였다, TEXT와 CONST는 ROM/FLASH에 배치해도 되는 변하지 않는 세그먼트이므로 같은 부류이고, CPU를 설계하고 코드를 직접 쓰는 경우 ROM/FLASH을 이용한다.

거의 모든 툴에서 이 맵을 파일로 만들어 준다. 물론 옵션으로 설정을 해야하는 경우도 있지만 구조를 얻을 수 있다. 함수와 변수의 위치와 이름 등을 확인할 수 있고, 각각의 세그먼트 크기 등의 데이터를 알 수 있다. 실제 CPU을 다루는 C 언어에서 이런 정보는 중요하다. 내가 사용하는 MCU의 메모리는 얼마나 사용하는지 등을 확인할 필요가 있기 때문이다.

## [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")

C 언어 함수는 표준함수가 있고, 개발 툴에서 제공하는 함수가 있다. 여러가지 부류가 있고 특성 별로 나누어 lib 파일로 코드를 제공하고 헤더파일로 선언을 알 수 있다.

### C 표준 라이브러리

C 표준 라이브러리는 함수 형태와 기능이 정해져 있기 때문에 개발툴별 같다는 특징이 있다.

### [ISO C 라이브러리 헤더](../Page/C_표준_라이브러리.md "wikilink")

| 파일명                                                                   | 출처  | 설명                                                                                                                                                       |
| --------------------------------------------------------------------- | --- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`<assert.h>`](https://ko.wikipedia.org/wiki/assert.h "wikilink")     |     | [assert](https://ko.wikipedia.org/wiki/assertion_\(프로그래밍_언어\) "wikilink") 매크로, 논리오류 및 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink") 시 오류 형 등 지원한다. |
| [`<complex.h>`](https://ko.wikipedia.org/wiki/complex.h "wikilink")   | C99 | [복소수](../Page/복소수.md "wikilink") 처리용 세트.                                                                                                                 |
| [`<ctype.h>`](https://ko.wikipedia.org/wiki/ctype.h "wikilink")       |     | 초기의 대-소 문자 변환 함수 제공                                                                                                                                      |
| [`<errno.h>`](https://ko.wikipedia.org/wiki/errno.h "wikilink")       |     | 함수에서 발생하는 오류 형태 변환등의 오류처리.                                                                                                                               |
| [`<fenv.h>`](https://ko.wikipedia.org/wiki/fenv.h "wikilink")         | C99 | [부동소수점](../Page/부동소수점.md "wikilink") 환경 제어.                                                                                                              |
| [`<float.h>`](https://ko.wikipedia.org/wiki/float.h "wikilink")       |     | [부동소수점](../Page/부동소수점.md "wikilink") 특성 정의. 두 숫자 사이의 최소 차이(`_EPSILON`), 숫자의 최대 자리수(`_DIG`), 숫자의 범위의 표현(`_MIN`, `_MAX`).                                  |
| [`<inttypes.h>`](https://ko.wikipedia.org/wiki/inttypes.h "wikilink") | C99 | 정수형 변수의 정확한 변환.                                                                                                                                          |
| [`<iso646.h>`](https://ko.wikipedia.org/wiki/iso646.h "wikilink")     | NA1 | [ISO 646](https://ko.wikipedia.org/wiki/ISO_646 "wikilink") 문자열 처리.                                                                                      |
| [`<limits.h>`](https://ko.wikipedia.org/wiki/limits.h "wikilink")     |     | 정수형의 특성 정의, 정수 숫자 범위(`_MIN`, `_MAX`).                                                                                                                    |
| [`<locale.h>`](https://ko.wikipedia.org/wiki/locale.h "wikilink")     |     | [`로케일`](../Page/로케일.md "wikilink")`(` 관련 상수. 국제어 처리를 위한 적용.                                                                                              |
| [`<math.h>`](https://ko.wikipedia.org/wiki/math.h "wikilink")         |     | 수학 함수.                                                                                                                                                   |
| [`<setjmp.h>`](https://ko.wikipedia.org/wiki/setjmp.h "wikilink")     |     | `setjmp` 와 `longjmp` 매크로 선언.                                                                                                                             |
| [`<signal.h>`](https://ko.wikipedia.org/wiki/signal.h "wikilink")     |     | 다양한 예외 처리 제어.                                                                                                                                            |
| [`<stdarg.h>`](https://ko.wikipedia.org/wiki/stdarg.h "wikilink")     |     | 아규먼트 변수 처리. va_start, va_arg, va_end 함수 등.                                                                                                            |
| [`<stdbool.h>`](https://ko.wikipedia.org/wiki/stdbool.h "wikilink")   | C99 | 논리 변수.                                                                                                                                                   |
| [`<stdint.h>`](https://ko.wikipedia.org/wiki/stdint.h "wikilink")     | C99 | 정수형 변수의 각종 정의/선언.                                                                                                                                        |
| [`<stddef.h>`](https://ko.wikipedia.org/wiki/stddef.h "wikilink")     |     | 유용한 형과 매크로 정의/선언.                                                                                                                                        |
| [`<stdio.h>`](https://ko.wikipedia.org/wiki/stdio.h "wikilink")       |     | C 언어의 입출력 제공. [`printf`](https://ko.wikipedia.org/wiki/printf "wikilink") 등이 포함 되어 있다.                                                                   |
| [`<stdlib.h>`](https://ko.wikipedia.org/wiki/stdlib.h "wikilink")     |     |                                                                                                                                                          |
| [`<string.h>`](https://ko.wikipedia.org/wiki/string.h "wikilink")     |     | 문자열 조작.                                                                                                                                                  |
| [`<tgmath.h>`](https://ko.wikipedia.org/wiki/tgmath.h "wikilink")     | C99 | 수학 함수에서 일반 형 변환 관련.                                                                                                                                      |
| [`<time.h>`](https://ko.wikipedia.org/wiki/time.h "wikilink")         |     | 시간과 날짜 변환 함수.                                                                                                                                            |
| [`<wchar.h>`](https://ko.wikipedia.org/wiki/wchar.h "wikilink")       | NA1 | 국제어 등의 처리를 위한 [확장 문자](../Page/확장_문자.md "wikilink")(문자열 처리.                                                                                               |
| [`<wctype.h>`](https://ko.wikipedia.org/wiki/wctype.h "wikilink")     | NA1 | [확장 문자](../Page/확장_문자.md "wikilink") 처리.                                                                                                                 |

## 개발 도구

### [GCC](https://ko.wikipedia.org/wiki/GCC "wikilink")

[유닉스 계열](../Page/유닉스_계열.md "wikilink")(리눅스)의 시스템에서 주로 사용하는 C/C++ 언어 개발 도구이다. 리눅스의 OS을 제 컴파일하거나, 각종 응용 프로그램 개발에 사용한다. 또한 X-Windows의 개발 도구로도 사용할 수 있다.

전자 장치의 개발 시 임베디드 OS 포팅에서, 리눅스 커널이나 리눅스 커널 기반으로 하는 OS 커널 자체를 개발하는 도구로 사용한다. 리눅스 커널 기반 임베디드에서 실행되는 응용 프로그램 역시 [gcc](https://ko.wikipedia.org/wiki/gcc "wikilink")을 많이 사용한다.

#### [make](https://ko.wikipedia.org/wiki/make_\(소프트웨어\) "wikilink")

여러 파일들끼리의 의존성과 각 파일에 필요한 명령을 정의함으로써 프로그램을 컴파일할 수 있으며 최종 프로그램을 만들 수 있는 과정을 서술할 수 있는 표준적인 문법을 가지고 있고, 구조로 기술된 파일(주로 Makefile이라는 파일명)을 \[make\]가 해석하여 프로그램 빌드를 수행하게 된다.

#### Cygwin

[gcc](https://ko.wikipedia.org/wiki/gcc "wikilink")을 [윈도에서](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 실행 할 수 있도록 재 포팅한 것이다.

#### MinGW

Cygwin에서 분화 된 gcc 기반 개발 라이브러리 이다.

### [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")

이클립스는 다양한 언어와 다양한 [OS](https://ko.wikipedia.org/wiki/OS "wikilink")에서 실행되는 [IDE](https://ko.wikipedia.org/wiki/IDE "wikilink")이다. 따라서 여러가지 상황에서 다양하게 적용할 수 있다.

#### Eclipse IDE for C/C++ Developers

C/C++언어를 제공하는 [IDE으로](../Page/통합_개발_환경.md "wikilink") 리눅스의 경우 기존의 [gcc](https://ko.wikipedia.org/wiki/gcc "wikilink")을 사용할 수 있도록 연결 설정만 하면 된다.

  - [MinGW](http://www.mingw.org/)

[윈도에서](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [gcc](https://ko.wikipedia.org/wiki/gcc "wikilink")와 연결하여 C/C++ 언어를 사용하여 프로그램을 개발 할 수 있다. MinGW는 다양한 언어를 지원하므로 다른 언어로도 이클립스와 연결하여 개발 도구로 사용할 수 있다.

### [마이크로소프트 비주얼 스튜디오](../Page/마이크로소프트_비주얼_스튜디오.md "wikilink")

[마이크로소프트](../Page/마이크로소프트.md "wikilink")에서 개발, 판매하는 [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink") 환경에서 작동하는 개발도구이다. 현재는 C 뿐만 아니라 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [C\#](https://ko.wikipedia.org/wiki/C# "wikilink") 등 다양한 언어를 지원하고 있지만 초기의 마이크로소프트 개발 도구는 C 언어로 부터 출발 하였다. 비주얼 스튜디오로는 [윈도우 API를](../Page/윈도우_API.md "wikilink") 이용한 [GUI](../Page/그래픽_사용자_인터페이스.md "wikilink") 프로그램, [명령 줄 인터페이스](../Page/명령_줄_인터페이스.md "wikilink") 환경으로 실행되는 Windows Console Application, 윈도우 서비스, [동적 링크 라이브러리](../Page/동적_링크_라이브러리.md "wikilink") 등의 형태로 소프트웨어를 개발할 수 있고, 최근 버전에서는 [모바일 응용 소프트웨어](https://ko.wikipedia.org/wiki/모바일_응용_소프트웨어 "wikilink") 개발도 지원한다.

비주얼 스튜디오에서 사용 가능한 [소프트웨어 개발 키트와](../Page/소프트웨어_개발_키트.md "wikilink") 라이브러리는 다음과 같다.

#### [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink")

표준 C에서 정의하는 라이브러리 함수를 거의 대부분 그대로 사용할 수 있다.

#### Windows SDK

윈도우 운영체제의 API를 사용할 수 있게 해주는 툴킷이다. 응용프로그램에서 사용 가능한 윈도우 운영체제의 기능은 Windows SDK를 통해 제공된다. 초기에는 C가 기본 언어였으나, 최근에는 C\#, C++ 등의 언어 툴킷도 제공한다. 예전에는 Win32 SDK라고 불리었다.

#### [MFC](../Page/마이크로소프트_파운데이션_클래스_라이브러리.md "wikilink")

윈도우 개발에 필요한 Windows API를 클래스로 래핑한 C++ 라이브러리이다.

#### [DirectX](../Page/DirectX.md "wikilink")

윈도우에서 주로 게임 등을 개발할 때 사용하는 툴킷 이다. 고속의 화면 제어, 음성지원, 3D 등을 지원한다.

## 디버깅

보통 소프트웨어 개발에서 디버깅의 가장 일반적인 방법은 두가지 이다.

1.  IDE를 통해 소스 수준에서 디버깅 한다. 일명 'BREAK POINT'를 설정하면 그 위치에서 멈추고 해당 상황을 파악할 수 있다. 가장 중요한 파악 대상이 변수의 값으로 표시 화면에 해당 변수의 형과 맞게 변수의 값을 표시 한다. 또한 줄단위로 실행하기, 함수로 들어가기와 나오기 등 IDE에 따라 구성이 다양하다.
2.  내부 변수나 기타 상황을 printf 형태의 함수를 UART, 네트워크, USB 등과 연결하여 출력함으로써 프로그램 상황을 표시 할 수 있다. 보통 IDE 처럼 다양한 구성이 불가능 할 때 많이 사용한다.
    1.  리눅스 커널의 경우 printfk 함수로 출력하면 정해진 출력 메시지 파일태로 표시할 수 있다.
    2.  [MCU](https://ko.wikipedia.org/wiki/MCU "wikilink")와 같은 전자장치의 개발에서 개인용 컴퓨터 처럼 성능이 좋은 IDE을 만들기 쉽지 않다. 따라서 저 성능의 IDE을 사용하거나 UART등으로 상황을 출력해서 디버깅 하는 방법을 사용할 수 있다. 구성이 간단해서 개발 소스에 printf 형의 메시지 출력을 추가하면 된다. 개발자가 직접 해야하는 것이 번거롭다.

### [GDB](https://ko.wikipedia.org/wiki/GDB "wikilink")

[GCC](https://ko.wikipedia.org/wiki/GCC "wikilink")을 기반으로 하는 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink") 도구이다. 따라서 [유닉스](../Page/유닉스.md "wikilink") 계열에서 가장 일반적으로 실행된다.

#### 응용 프로그램 디버깅

GCC 옵션을 디버깅이 되도록 설정하면 디버깅 테이블을 만든다. gdb 실행 중에 이것을 사용한다. GDB을 실행하여 응용 프로그램을 실행하면서 break, 변수, 함수 등의 디버깅을 할 수 있다.

#### 원격 디버깅

GCC에서 [gdb](https://ko.wikipedia.org/wiki/gdb "wikilink")는 서버 구조를 사용할 수 있다. [gdb-server](https://ko.wikipedia.org/wiki/gdb-server "wikilink")을 설치하면 [네트워크](https://ko.wikipedia.org/wiki/네트워크 "wikilink")를 통해 디버깅 환경을 구성할 수 있다. 예를 들어 임베디드 개발 시 리눅스 커널을 포팅하고, 해당 리눅스 시스템에 gdb-server를 설치하면 다른 환경에서 이를 통해 응용 프로그램을 디버깅 할 수 있다. 임베디드의 많은 경우 자신의 시스템에서는 디버깅이 만만치 않다. 따라서 원격으로 gdb의 실행 결과를 전송 할 수 있고 이 정보를 바탕으로 이클립스와 같은 IDE와 연동할 수 있다. 보통 리눅스 기반의 임베디드 개발 환경은 이클립스 C++를 사용할 수 있는데, 이것과 결합할 수 있다.

#### 커널 디버깅

원격 디버깅 모드는 리눅스 커널에 사용되는 소스 수준의 디버거인 KGDB에서도 사용된다. KGDB를 사용하면 커널 개발자는 일반 응용 프로그램과 마찬가지로 커널을 디버깅할 수 있다.

### IDE 디버깅

[비주얼 스튜디오나](https://ko.wikipedia.org/wiki/비주얼_스튜디오 "wikilink") [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink") 등의 도구 들은 기본적으로 디버깅 방법을 제시 한다. 이클립스 디버깅은 [GDB](https://ko.wikipedia.org/wiki/GDB "wikilink")와 연동해서 구성할 수 있다.

## Hello world 출력 프로그램

``` c
#include <stdio.h> // C 표준 라이브러리 stdio.h 를 include 한다. 이것으로 printf 함수 등을 사용할 수 있다.

int main(void) // 프로그램 호출시 가장 먼저 실행되는 함수
{
    printf("Hello, world"); // 표준출력에 Hello, world라는 문자열을 출력한다.
    return 0;                 // 0을 반환하고 main 함수 종료.
}
```

이 프로그램은 표준출력(stdout)으로 `Hello, world`를 출력한다.

## 같이 보기

  - [B (프로그래밍 언어)](../Page/B_\(프로그래밍_언어\).md "wikilink")
  - [C99](../Page/C99.md "wikilink")
  - [C11](https://ko.wikipedia.org/wiki/C11 "wikilink")
  - [C 언어의 문법](../Page/C_언어의_문법.md "wikilink")
      - [C 언어 변수](../Page/C_언어_변수.md "wikilink")
      - [C 언어 포인터](https://ko.wikipedia.org/wiki/C_언어_포인터 "wikilink")
  - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")
  - [오브젝티브-C](../Page/오브젝티브-C.md "wikilink")

## 각주

## 외부 링크

  - [comp.lang.c FAQ 한국어 번역판](https://web.archive.org/web/20050822131654/http://www.cinsk.org/cfaqs/index-ko.html)

  - [joinC C 언어 소개](http://www.joinc.co.kr/modules/moniwiki/wiki.php/Site/C)

  - Ritchie, Dennis M. [The Development of the C Language](http://plan9.bell-labs.com/who/dmr/chist.html). History of Programming Languages-II. Second History of Programming Languages conference, Cambridge, Massachusetts, April, 1993. .

  - [Richard M. Stallman](https://ko.wikipedia.org/wiki/리처드_스톨만 "wikilink"): *[Using and Porting the GNU Compiler Collection](http://gcc.gnu.org/onlinedocs/gcc-2.95.3/gcc.html)*, [Free Software Foundation](../Page/자유_소프트웨어_재단.md "wikilink"),

  - Richard M. Stallman: *[Using Gcc: The Gnu Compiler Collection Reference](http://gcc.gnu.org/onlinedocs/gcc-3.3.1/gcc/)*, Free Software Foundation,

  - [Brian J. Gough](https://ko.wikipedia.org/wiki/Brian_J._Gough "wikilink"): *[An Introduction to GCC](https://archive.is/20121205072412/http://www.network-theory.co.uk/gcc/intro/)*, Network Theory Ltd.,

[C_프로그래밍_언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:ISO 표준](https://ko.wikipedia.org/wiki/분류:ISO_표준 "wikilink") [분류:미국의 발명품](https://ko.wikipedia.org/wiki/분류:미국의_발명품 "wikilink") [분류:1972년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1972년_개발된_프로그래밍_언어 "wikilink") [분류:C 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어_계열 "wikilink") [분류:시스템 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:시스템_프로그래밍_언어 "wikilink")

1.
2.
3.
4.