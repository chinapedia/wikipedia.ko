> This article is converted from Wikipedia: [Nm \(유닉스\)](https://ko.wikipedia.org/wiki/Nm_\(유닉스\)).


**nm**은 다수의 최신 [유닉스](../Page/유닉스.md "wikilink")와 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제에](../Page/운영_체제.md "wikilink") 포함되어 있는 명령어이다. nm은 라이브러리, 컴파일된 오브젝트 모듈, 공유 오브젝트 파일, 독립 실행파일등의 바이너리 파일을 검사해서 그 파일 들에 저장된 내용 또는 메타 정보를 표시한다. nm은 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink") 과정에서 이름 겹침과 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 이름 맹글링 문제를 해결하거나 툴체인의 다른 부분을 확인하는 데 사용된다.

[GNU](../Page/GNU.md "wikilink") 프로젝트는 높은 기능을 갖춘 nm 프로그램을 [GNU Binutils](https://ko.wikipedia.org/wiki/GNU_Binutils "wikilink") 패키지에 포함시키고 있다. GNU 툴체인의 다른 부분과 함께 주어진 nm 바이너리는 특정 컴퓨터 아키텍처와 바이너리 포맷만을 위해 컴파일 된 것이므로 의심스런 바이너리를 검사하기 위해 nm을 사용하는 보안 전문가들은 보통 여러 타겟 용으로 만들어 놓은 nm 바이너리를 갖고 있다.

## nm 출력 예제

``` c
/*
 * File name: test.c
 * For C code compile with:
 * gcc -c test.c
 *
 * For C++ code compile with:
 * g++ -c test.cpp
 */

int global_var;
int global_var_init = 26;

static int static_var;
static int static_var_init = 25;

static int static_function()
{
    return 0;
}

int global_function(int p)
{
    static int local_static_var;
    static int local_static_var_init=5;

    local_static_var = p;

    return local_static_var_init + local_static_var;
}

int global_function2()
{
    int x;
    int y;
    return x+y;
}

#ifdef __cplusplus
extern "C"
#endif
void non_mangled_function()
{
    // I do nothing
}

int main(void)
{
    global_var = 1;
    static_var = 2;

    return 0;
}
```

이전 코드가 [gcc](https://ko.wikipedia.org/wiki/GNU_컴파일러_모드 "wikilink") C 컴파일러로 컴파일되면, `nm` 명령의 출력은 아래와 같다:

    # nm test.o
    0000000a T global_function
    00000025 T global_function2
    00000004 C global_var
    00000000 D global_var_init
    00000004 b local_static_var.1255
    00000008 d local_static_var_init.1256
    0000003b T main
    00000036 T non_mangled_function
    00000000 t static_function
    00000000 b static_var
    00000004 d static_var_init

C++ 컴파일러를 사용하면 출력은 아래와 같이 다르다:

    # nm test.o
    0000000a T _Z15global_functioni
    00000025 T _Z16global_function2v
    00000004 b _ZL10static_var
    00000000 t _ZL15static_functionv
    00000004 d _ZL15static_var_init
    00000008 b _ZZ15global_functioniE16local_static_var
    00000008 d _ZZ15global_functioniE21local_static_var_init
             U __gxx_personality_v0
    00000000 B global_var
    00000000 D global_var_init
    0000003b T main
    00000036 T non_mangled_function

## 같이 보기

  - [objdump](https://ko.wikipedia.org/wiki/objdump "wikilink")

## 외부 링크

  - [(영문) [맨페이지](https://ko.wikipedia.org/wiki/맨페이지 "wikilink")의 설명](http://www.linuxmanpages.com/man1/nm.1.php)
  - [nm 활용](https://web.archive.org/web/20070930015621/http://kldp.org/node/68410)

[분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")