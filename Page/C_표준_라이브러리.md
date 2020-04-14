> This article is converted from Wikipedia: [C 표준 라이브러리](https://ko.wikipedia.org/wiki/C_표준_라이브러리).


**C 표준 라이브러리**(C standard library)는 C 언어를 위한 [표준 라이브러리로서](../Page/표준_라이브러리.md "wikilink"), ANSI C 표준에 의해 명시되었다.\[1\] 이것은 상위 집합인 [C POSIX 라이브러리와](../Page/C_POSIX_라이브러리.md "wikilink") 동시에 개발되었다.\[2\]\[3\] ANSI C가 [국제 표준화 기구에](../Page/국제_표준화_기구.md "wikilink") 의해서 채택됨에 따라,\[4\] C 표준 라이브러리는 또한 **ISO C library**로도 불린다.

C 표준 라이브러리는 매크로, 타입 정의 그리고 문자열 처리나 수학적 연산, 입출력 프로세스, 메모리 할당과 다른 운영 체제 서비스 같은 작업을 위한 함수들을 제공한다.

## 애플리케이션 프로그래밍 인터페이스 (API)

### 헤더 파일들

C 표준 라이브러리의 [API](../Page/API.md "wikilink")는 많은 헤더 파일들에 정의되어 있다. 각 헤더 파일은 하나 이상의 함수 정의와 데이터 타입 정의 그리고 매크로들을 포함한다.

| 이름                                                                    | 표준  | 상세                                                                                                       |
| --------------------------------------------------------------------- | --- | -------------------------------------------------------------------------------------------------------- |
| [`<assert.h>`](../Page/Assert.h.md "wikilink")                        |     | [assert](../Page/표명.md "wikilink") 매크로를 포함하며, 이것은 프로그램의 디버깅 버전들에서 논리 오류들과 버그들의 다른 타입들을 탐지하는 것을 돕는데 사용된다. |
| [`<complex.h>`](https://ko.wikipedia.org/wiki/Math.h "wikilink")      | C99 | [복소수](../Page/복소수.md "wikilink")를 조작하는데 사용되는 함수들의 집합.                                                    |
| [`<ctype.h>`](https://ko.wikipedia.org/wiki/Ctype.h "wikilink")       |     | 그들의 타입에 따라 문자들을 분류하거나 대소문자를 전환하는데 사용되는 함수들의 집합을 정의한다.                                                    |
| [`<errno.h>`](https://ko.wikipedia.org/wiki/errno.h "wikilink")       |     | 라이브러리 함수들에 의해 리포트되는 오류 코드들을 테스팅할 때 사용된다.                                                                 |
| `<fenv.h>`                                                            | C99 | 부동소수점 환경을 제어하는데 사용되는 함수들의 집합을 정의한다.                                                                      |
| `<float.h>`                                                           |     | 부동소수점 라이브러리의 구현된 속성을 명시하는 매크로 상수를 정의한다.                                                                  |
| [`<inttypes.h>`](https://ko.wikipedia.org/wiki/Limits.h "wikilink")   | C99 | 정확한 정수형을 정의한다.                                                                                           |
| `<iso646.h>`                                                          | NA1 | 여러 표준 토큰들을 표현하기 위한 대체 방식들을 구현하는 여러 매크로들을 정의한다.                                                           |
| `<limits.h>`                                                          |     | 정수형 타입의 구현된 속성을 명시하는 매크로 상수를 정의한다.                                                                       |
| `<locale.h>`                                                          |     | 지역화 함수 정의                                                                                                |
| `<math.h>`                                                            |     | 일반적인 수학 함수 정의                                                                                            |
| `<setjmp.h>`                                                          |     | `setjmp` 와 `longjmp` 매크로를 선언한다.                                                                          |
| [`<signal.h>`](../Page/C_시그널_처리.md "wikilink")                        |     | 시그널 핸들링 함수를 정의한다.                                                                                        |
| `<stdalign.h>`                                                        | C11 | 객체들의 얼라인먼트를 질의하고 명시하기 위한.                                                                                |
| `<stdarg.h>`                                                          |     | 함수에 전달되는 인자들에 접근하기 위한.                                                                                   |
| `<stdatomic.h>`                                                       | C11 | 스레드 사이에서 공유되는 데이터의 원자적 동작을 위한.                                                                           |
| [`<stdbool.h>`](https://ko.wikipedia.org/wiki/stdbool.h "wikilink")   | C99 | 불린 데이터 형 정의                                                                                              |
| `<stddef.h>`                                                          |     | 여러 유용한 타입과 매크로 정의.                                                                                       |
| `<stdint.h>`                                                          | C99 | 정확한 정수형을 정의.                                                                                             |
| **`<stdio.h>`**                                                       |     | **핵심 입력과 출력 함수들을 정의한다.**                                                                                 |
| `<`[`stdlib.h`](https://ko.wikipedia.org/wiki/stdlib.h "wikilink")`>` |     | 숫자 변환 함수들, 슈도 랜덤 숫자 생성 함수들, 메모리 할당, [프로세스 제어](../Page/C_프로세스_제어.md "wikilink") 함수들을 정의한다.                |
| `<stdnoreturn.h>`                                                     | C11 | 반환하지 않는 함수들을 명시하기 위한                                                                                     |
| [`<string.h>`](https://ko.wikipedia.org/wiki/String.h "wikilink")     |     | 문자열 처리 함수들을 정의한다.                                                                                        |
| `<tgmath.h>`                                                          | C99 | 포괄형 수학 함수들을 정의한다.                                                                                        |
| `<threads.h>`                                                         | C11 | 다중 스레드들과 뮤텍스 그리고 제어 변수들을 관리하는 함수들을 정의한다.                                                                 |
| `<`[`time.h`](https://ko.wikipedia.org/wiki/time.h "wikilink")`>`     |     | 데이터와 시간 처리 함수들을 정의한다.                                                                                    |
| `<uchar.h>`                                                           | C11 | 유니코드 문자들과 이것을을 조작하는 함수들                                                                                  |
| `<wchar.h>`                                                           | NA1 | wide 문자열 처리 함수들을 정의한다.                                                                                   |
| `<wctype.h>`                                                          | NA1 | 그들의 형에 따라 wide 문자들을 분류하거나 대소문자를 전환하는데 사용되는 함수들의 집합.                                                      |

세 헤더 파일들의(`complex.h`, `stdatomic.h`, `threads.h`) 구현은 필수는 아니다.

[POSIX](../Page/POSIX.md "wikilink") 표준은 유닉스를 위한 기능을 위해 여러 표준이 아닌 C 헤더들을 추가하였다. 예를 들면 `unistd.h` 그리고 `signal.h`가 있다.

### 문서화

유닉스 계열 시스템들에서 실제 구현된 API의 권위 있는 문서화는 [man page의](https://ko.wikipedia.org/wiki/man_page "wikilink") 형태로 제공된다.

## 구현

유닉스 계열 시스템들은 일반적으로 공유 라이브러리 형태로 C 라이브러리를 가지지만, 헤더 파일들이 설치 시에 존재하지 않아서 C 개발이 불가능할 수도 있다. C 라이브러리는 유닉스 계열 운영 체제에서 한 부분으로 여겨진다. ISO C 표준을 포함한 C 함수들은 프로그램들에서 널리 사용되지만, 운영 체제 인터페이스의 한 부분이다. 유닉스 계열 시스템들은 일반적으로 C 라이브러리가 제거되면 동작할 수 없다.

마이크로소프트 윈도우에서, 핵심 시스템 [동적 라이브러리들은](../Page/동적_링크_라이브러리.md "wikilink") C 표준 라이브러리의 구현을 제공한다. C 로 쓰여진 컴파일된 애플리케이션들은 C 라이브러리와 정적으로 링크되거나 딸려온 라이브러리와 동적으로 링크된다. 컴파일러의 C 라이브러리에 존재하는 함수들은 마이크로소프트 윈도우와의 인터페이스로 여겨지지 않는다.

운영 체제와 C 컴파일러에서 제공되는 많은 구현들이 존재한다. 몇몇 유명한 구현들은 다음과 같다.

  - [BSD libc](../Page/C_표준_라이브러리.md "wikilink"), [BSD](../Page/BSD.md "wikilink") 운영 체제 하에 배포되는 구현.
  - [GNU C 라이브러리](../Page/GNU_C_라이브러리.md "wikilink") (glibc), [리눅스](../Page/리눅스.md "wikilink"), [GNU 허드](../Page/GNU_허드.md "wikilink") 그리고 GNU/kFreeBSD에서 사용된다.
  - [마이크로소프트 C 런타임 라이브러리](../Page/윈도우_라이브러리_파일.md "wikilink"), [비주얼 C++의](https://ko.wikipedia.org/wiki/비주얼_C++ "wikilink") 한 부분

### 컴파일러 빌트인 함수들

몇몇 컴파일러들은(예를 들면 [GCC](../Page/GNU_컴파일러_모음.md "wikilink")\[5\]) C 표준 라이브러리에서 많은 함수들의 빌트인 버전들을 제공한다; 즉, 함수들의 구현들은 컴파일된 [목적 파일로](../Page/목적_파일.md "wikilink") 쓰여지며 프로그램은 C 라이브러리 공유 목적 파일에 있는 함수들 대신 빌트인 버전들을 호출한다. 이것은 특히 만약 함수 호출들이 [인라인](https://ko.wikipedia.org/wiki/인라인_함수 "wikilink") 형태로 대체된다면 함수 호출 오버헤드를 감소시키며, [최적화의](https://ko.wikipedia.org/wiki/컴파일러_최적화 "wikilink") 다른 형태(컴파일러가 빌트인 형태의 [제어 흐름](../Page/제어_흐름.md "wikilink") 특징을 알 때)를 허용하지만 디버깅 시에 혼란을 야기할 수 있다. (예를 들면 빌트인 버전들은 인스트루멘트된 형태로 대체될 수 없다)

그러나 빌트인 함수들은 반드시 ISO C에 따라 기본 함수들처럼 행동해야 한다. 중요한 것은 프로그램이 반드시 이러한 함수들을 가리키는 포인터를 주소를 사용해서 생성할 수 있어야 하고, 이 포인터로 함수를 발생시킬 수 있어야 한다. 만약 같은 함수에 대한 두 포인터들이 프로그램에서 두 다른 변환 유닛으로 만들어진다면, 이러한 두 포인터들은 반드시 같아야 한다. 즉, 외부 링크를 갖는 함수의 이름을 리졸브해서 얻은 주소이다.

### 링킹, libm

리눅스 그리고 FreeBSD에서,\[6\] 수학 함수들( `math.h`에 정의된)은 수학 라이브러리 [libm에서](https://ko.wikipedia.org/wiki/Math.h "wikilink") 따로 묶어져야 한다. 만약 이것들 중 어느 것이 사용된다면, 링커는 반드시 지시자 `-lm`을 받아야 한다.

### 탐지

C 표준에 따르면, 만약 구현이 호스트된다면 매크로 `__STDC_HOSTED__` 는  **1** 로 정의될 것이다. 호스트된 구현은 C 표준에 명시된 모든 헤더들을 갖는다. 구현은 또한 *freestanding* 일 수 있는데 이것은 이러한 헤더들이 존재하지 않는다는 의미이다. 만약 구현이 *freestanding*이라면, 이것은 `__STDC_HOSTED__` 을 **0**으로 정의할 것이다.

## 개념, 문제 그리고 해결책

### 버퍼 오버플로우 취약점

C 표준 라이브러리에 있는 몇몇 함수들은 버퍼 오버플로우 취약점들과 채택 이후의 버그를 유발하는 프로그래밍을 조장하는 것으로 악명 높다.\[7\] 가장 비판받는 항목은:

  - 문자열 조작 루틴들 :  `strcpy()` 와 `strcat()`를 포함하며 경계 검사의 부족과 경계가 직접 검사되지 않았을 때의 버퍼 오버플로우 가능성이 있다;
  - 일반적인 문자열 루틴들 : [부작용으로](../Page/부작용_\(컴퓨터_과학\).md "wikilink") 인해서 무책임한 버퍼 사용을 부추기며, 항상 유효한 널 종료 출력과 선형 길이 계산을 보장하지는 않는다;\[8\]
  - [`printf`](https://ko.wikipedia.org/wiki/printf "wikilink")`()` 관련 루틴들 : 포맷 스트링이 주어진 인자와 맞지 않았을 때 [실행 스택을](../Page/콜_스택.md "wikilink") 망친다. 이러한 근본적인 결함은 많은 공격들을 만들어 낸다: [포맷 스트링 버그](../Page/포맷_스트링_버그.md "wikilink");
  - `gets()` 와 [`scanf`](https://ko.wikipedia.org/wiki/scanf "wikilink")`()` 같은 입출력 루틴들 : 입력 길이 검사가 부족하다.

`gets()`를 사용한 극단적인 경우를 제외하고, 모든 보안 취약점들은 보조 코드가 메모리 관리, 경계 검사, 입력 검사 등을 수행하게 함으로써 피할 수 있다. 이것은 종종 표준 라이브러리 함수들을 사용하기 쉽고 안전하게 만들어 주는 래퍼의 형태를 통해 가능해 진다.

함수들에 경계 검사와 자동 버퍼 할당을 채택하는 것을 제안하기 위해 ISO C 윈원회는 기술 보고서 TR 24731-1\[9\]를 발행하였고 TR 24731-2\[10\]를 작성중에 있다. 전자는 많은 비판을 받았지만,\[11\]\[12\] 후자는 비판과 칭찬을 모두 받았다. 그럼에도 불구하고 TR 24731-1 는 마이크로소프트의 C 표준 라이브러리에 구현되었으며, 이것의 컴파일러는 오래된 불안정한 함수들을 사용할 때 경고를 발생시킨다.

### 쓰레딩 문제, 경쟁 상태에 대한 취약점

`mktemp()` 과 [`strerror`](https://ko.wikipedia.org/wiki/String.h "wikilink")`()` 루틴들은 [스레드 안전와](../Page/스레드_안전.md "wikilink") [경쟁 상태에](https://ko.wikipedia.org/wiki/경쟁_상태 "wikilink") 대한 취약점 때문에 비판을 받았다.

### 오류 처리

C 표준 라이브러리에서 함수들의 오류 처리는 일관되지 않으며 가끔은 혼란스럽다. 이것은 리눅스 매뉴얼 페이지 `math_error` 에 잘 요약되어 있다:\[13\]

` `*`glibc``   ``하의``   ``현재(버전``   ``2.8)``   ``상황은``   ``엉망이다.``   ``대부분의(모두는``   ``아니지만)``   ``함수들은``   ``오류들에``   ``대해``   ``예외를``   ``일으킨다.``   ``몇몇은``   ``또한``   ``errno를``   ``설정한다.``   ``소수의``   ``함수들은``   ``errno를``   ``설정하지만,``   ``예외를``   ``일으키지는``   ``않는다.``   ``극히``   ``소수의``   ``함수들은``   ``둘``   ``모두``   ``하지``   ``않는다.`*

## 표준화

다른 언어들과 달리, 원본 C 언어는 입출력 동작 같은 빌트인 함수들을 제공하지 않았다. 시간이 지나면서 C의 사용자 커뮤니티들은 생각을 공유하고 현재 C 표준 라이브러리라고 불리는 것을 구현하였다. 이러한 아이디어들 중 많은 수가 결국 표준 C 언어의 정의에 포함되었다.

유닉스와 C는 모두 [벨 연구소에서](../Page/벨_연구소.md "wikilink") 1960년대에에서 1970년대에 만들어졌다. 1970년대 동안 C 언어는 점점 유명해 졌다. 많은 대학교들과 단체들이 자신의 프로젝트를 위해 이 언어를 자신만의 형태로 만들었다. 1980년대의 시작에 이것들 간에 호환 문제가 발생하였다. 1983년 [미국 국립 표준 협회](https://ko.wikipedia.org/wiki/미국_국립_표준_협회 "wikilink")(ANSI)는 위원회를 구성해서 C의 표준 명세를 확립하였고 이것은 ANSI C로 불린다. 이 작업은 1989년 C89라고 불리는 것이 만들어짐으로써 끝이나게 된다.

### POSIX 표준 라이브러리

[POSIX](../Page/POSIX.md "wikilink"), 또는 [SUS는](../Page/단일_유닉스_규격.md "wikilink") 기본 C 표준 라이브러리에서 사용 가능한 많은 수의 루틴들을 명시하였다. POSIX 명세는 멀티 스레드, 네트워킹 그리고 정규 표현식에 대한 헤더 파일들을 포함한다. 이러한 것들은 종종 C 표준 라이브러리 기능들과 동시에 구현되었다. 예를 들면 [glibc는](../Page/GNU_C_라이브러리.md "wikilink") `libc.so` 내의 fork 같은 함수들을 구현하였다. 종종 POSIX 명세의 기능은 라이브러리의 한 부분으로 여겨질 수 있다; 기본 C 라이브러리는 ANSI 또는 ISO C 라이브러리로 식별된다.

### BSD libc

**BSD libc**는 POSIX 표준 라이브러리의 상위 집합으로서 [FreeBSD](../Page/FreeBSD.md "wikilink"), [NetBSD](../Page/NetBSD.md "wikilink"), [OpenBSD](../Page/OpenBSD.md "wikilink") 그리고 [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") 같은 BSD 운영 체제에서 사용된다. 이것은 1994년 릴리즈된 [4.4BSD에서](../Page/BSD.md "wikilink") 처음 선보여졌다. BSD libc는 원본 표준에서 정의되지 않은 몇몇 확장들을 갖는다. BSD libc의 확장들 중 몇몇은 다음과 같다:

  - [`sys/tree.h`](http://bxr.su/o/sys/sys/tree.h)<span> </span>–.\[14\]
  - [`sys/queue.h`](http://bxr.su/o/sys/sys/queue.h)<span> </span>–.\[15\]
  - [`fgetln()`](http://bxr.su/o/lib/libc/stdio/fgetln.c#fgetln)<span> </span>– [`stdio.h`](http://bxr.su/o/include/stdio.h)에 정의되었다. 이것은 파일을 라인 단위로 읽을 때 사용된다.\[16\]
  - [`fts.h`](http://bxr.su/o/include/fts.h)<span> </span>– 파일 계층을 순회하기 위한 함수들을 포함한다.\[17\]
  - [`db.h`](http://bxr.su/o/include/db.h)<span> </span>– 버플리 DB에 연결하기 위한 함수들.\[18\]
  - [`strlcat()`](http://bxr.su/o/lib/libc/string/strlcat.c) 와 [`strlcpy()`](http://bxr.su/o/lib/libc/string/strlcpy.c)<span> </span>– [`strncat()`](http://bxr.su/o/lib/libc/string/strncat.c) 와 [`strncpy()`](http://bxr.su/o/lib/libc/string/strncpy.c)의 안전한 대체\[19\]
  - [`err.h`](http://bxr.su/o/include/err.h)<span> </span>– 정형화된 오류 메시지들을 출력하는 함수들을 포함한다.\[20\]
  - [`vis.h`](http://bxr.su/o/include/vis.h)<span> </span>– [`vis()`](http://bxr.su/o/lib/libc/gen/vis.c#vis) 함수를 포함한다. 이 함수는 비주얼 포맷에서 출력할 수 없는 문자들을 표시하는데 사용된다.\[21\]

## 다른 언어들에서의 C 표준 라이브러리

몇몇 언어들은 자신의 라이브러리에 표준 C 라이브러리의 기능을 포함한다. 라이브러리는 그 언어의 구조에 어울리게 해서 채택되지만, 동작 의미는 비슷하게 된다. 예를 들면 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 언어는 이름공간 `std` (예를 들면 `std::printf`, `std::atoi`, `std::feof`)에서 C 표준 라이브러리의 기능을 포함하는데, 헤더 파일도 C의 것과 비슷하다(`cstdio`, `cmath`, `cstdlib`, 등). 다른 언어들은 [D와](../Page/D_\(프로그래밍_언어\).md "wikilink") 비슷한 접근법을 갖는데 [파이썬](../Page/파이썬.md "wikilink")의 경우 [C파이썬](https://ko.wikipedia.org/wiki/C파이썬 "wikilink")이 있다. 예를 들면 파이썬 2에서 빌트인 파일 객체들은 "C의 `stdio` 패키지를 사용해서 구현되었다"\[22\]고 정의되어서, 사용 가능한 연산들(open, read, write 등)은 상응하는 C 함수들과 같은 동작을 한다고 기대할 수 있다.

## 다른 언어들의 표준 라이브러리들과의 비교

C 표준 라이브러리는 다른 언어들의 표준 라이브러리들과 비교했을 때 작다고 할 수 있다. C 라이브러리는 수학, 문자열 조작, 형 변환 그리고 파일과 콘솔 기반 입출력 함수들의 기본 집합을 제공한다. 이것은 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") [표준 템플릿 라이브러리처럼](../Page/표준_템플릿_라이브러리.md "wikilink") 컨테이너 타입의 표준 집합을 포함하지 않는다. 이러한 작은 표준 라이브러리의 장점은 일할 ISO C 환경을 다른 언어들 보다 더 쉽게 제공한다는 것이며, 결과적으로 C를 새로운 플랫폼에 포팅하는 것이 상대적으로 쉽게 된다.

## 같이 보기

  - [C++ 표준 라이브러리](../Page/C++_표준_라이브러리.md "wikilink")

## 각주

## 더 읽어보기

  - Plauger, P. J. (1992). *The Standard C library*. Englewood Cliffs, N.J: Prentice Hall. [ISBN](../Page/국제_표준_도서_번호.md "wikilink") 0-13-131509-9.

## 외부 링크

  - [The C Library Reference Guide](https://web.archive.org/web/20150118141700/http://www.acm.uiuc.edu/webmonkeys/book/c_guide/index.html)
  - [Handy list of which headers are in which standard](http://www.schweikhardt.net/identifiers.html)
  - Microsoft [C Run-Time Libraries](http://msdn.microsoft.com/en-us/library/abx4dbyh.aspx) on MSDN
  - NetBSD [C libraries manual](http://netbsd.gw.com/cgi-bin/man-cgi?intro+3+NetBSD-current) and [full C library source](http://BXR.SU/NetBSD/lib/libc/)
  - [Manual pages for the original C standard libraries in Unix](http://man.cat-v.org/unix-1st/3/)

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [C_표준_라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.  International Organization for Standardization|International Electrotechnical Commission|IEC (1999). *[ISO/IEC 9899:1999(E): Programming Languages - C](../Page/C99.md "wikilink") §7.19.1 para 1*
2.
3.
4.
5.  [Other built-in functions provided by GCC](http://gcc.gnu.org/onlinedocs/gcc-4.1.1/gcc/Other-Builtins.html#Other-Builtins), GCC Manual
6.
7.  Morris worm that takes advantage of the well-known vulnerability in `gets()` have been created as early as in 1988.
8.  in C standard library, string length calculation and looking for a string's end have Linear time and are inefficient when used on the same or related strings repeatedly
9.
10.
11. [Do you use the TR 24731 'safe' functions in your C code?](http://stackoverflow.com/questions/372980/do-you-use-the-tr-24731-safe-functions-in-your-c-code) - Stack overflow
12.
13.
14.
15.
16.
17.
18.
19. Miller, Todd C. and Theo de Raadt. [strlcpy and strlcat - consistent, safe, string copy and concatenation](http://www.usenix.org/events/usenix99/millert.html). Proceedings of the 1999 USENIX Annual Technical Conference, June 6–11, 1999, pp. 175–178.
20.
21.
22.