> This article is converted from Wikipedia: [Errno.h](https://ko.wikipedia.org/wiki/Errno.h).


**errno.h**는 [C의](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") [표준 라이브러리](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") 내의 [헤더 파일이다](https://ko.wikipedia.org/wiki/헤더_파일 "wikilink"). `errno` (오류 번호 ("error number")의 줄임말) 라는 정적 메모리 위치에 저장된 오류 코드를 통해 오류 상태를 보고 및 검색하기 위한 매크로를 정의한다.\[1\]

한 값 (오류 번호)은 에러를 감지 했을 때 특정 [라이브러리 함수에](https://ko.wikipedia.org/wiki/라이브러리_함수 "wikilink") 의해 `errno`에 저장된다. 프로그램 시작시, 이 값에는 0이 저장된다. 라이브러리 함수들은 오직 0보다 큰 값을 저장한다. 모든 라이브러리 함수는 오류를 감지하는 지 여부와 상관없이 반환 전에 저장된 값을 대체할 수 있다. 대부분 함수들은 특별한 값, 보통 [포인터](https://ko.wikipedia.org/wiki/포인터 "wikilink")를 반환하는 함수의 경우 [NULL](../Page/널_포인터.md "wikilink") 및 함수의 경우 -1을 반환하여 오류를 감지했음을 나타낸다. 몇 가지 함수는 호출자가 사전에 `errno`으로 설정하고 이후에 오류를 감지했는지 그 다음 오류를 감지했는지 확인하기 위해 테스트를 해야 한다.

대부분의 함수는 특별한 값, 보통 포인터를 반환하는 함수의 경우 NULL 및 정수를 반환하는 함수의 경우 -1을 반환하여 오류를 감지했음을 나타냅니다.

`errno` 매크로는 유형이 `int`인 [lvalue으로](https://ko.wikipedia.org/wiki/값_\(컴퓨터_과학\) "wikilink") 확장되며, 플랫폼에 따라 `extern` 및/혹은 `volatile` 유형 지정자와 함께\[2\] errno 기능을 사용하는 함수에서 마지막으로 생성 된 오류 코드가 포함된다.\[3\] 본래 이는 정적 메모리 위치이지만 오늘날 매크로는 멀티 스레딩을 허용하기 위해 거의 항상 매크로가 사용되어 각 스레드에 자체 오류 번호를 볼 수 있도록 되어 있다.

이 헤더 파일은 에러 코드를 나타내기 위한 정수형 상수를 나타내는 매크로도 정의한다. 이 [C 표준 라이브러리는](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") 아래 3개의 매크로로 정의되는 데 필요하다.\[4\]

**EDOM**

  -
    함수 도메인의 바깥의 파라미터의 결과. 예 - `sqrt(-1)`

**ERANGE**

  -
    함수의 범위 바깥 결과로 부터 나온 결과. 예 - 32비트 길이의 시스템에서 `strtol("0xfffffffff",NULL,0)`

**EILSEQ** <small>(1에서 C89으로 1994년 개정된 표준을 필요로 함)</small>\[5\]

  -
    잘못된 바이트 시퀀스의 결과. 예 - [UTF-8](https://ko.wikipedia.org/wiki/UTF-8 "wikilink")를 쓰는 시스템 상의 `mbstowcs(buf,"\xff", 1)`.

[AIX](https://ko.wikipedia.org/wiki/AIX "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 혹은 [솔라리스](https://ko.wikipedia.org/wiki/솔라리스 "wikilink")와 같은 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 호환 운영 체제에는 파일을 열 수 없는 경우를 위한 **EACCES**와 같은 것 외에 위의 것 보다 훨씬 더 많은 오류 값을 포함된다. [C++11](https://ko.wikipedia.org/wiki/C++11 "wikilink") 추가적으로 POSIX 사양에서 발견되는 많은 동일한 값을 정의한다.\[6\]\[7\]

전통적으로, intro(2)라는 이름으로 지어진 [유닉스 시스템 메뉴얼의](https://ko.wikipedia.org/wiki/메뉴얼_페이지 "wikilink") 첫번째 페이지에 모든 errno.h 매크로가 게시되어 있으나 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")는 errno(3)에 매크로들이 게시되어 있다.

## 각주

<references/>

[분류:C 표준 라이브러리 헤더](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리_헤더 "wikilink")

1.  International Standard for Programming Language C (C99), ISO/IEC 9899:1999, p. 186
2.
3.
4.
5.
6.
7.