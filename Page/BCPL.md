> This article is converted from Wikipedia: [BCPL](https://ko.wikipedia.org/wiki/BCPL).


**BCPL**(Basic Combined Programming Language)은 1966년 [케임브리지 대학교에서](https://ko.wikipedia.org/wiki/케임브리지_대학교 "wikilink") [마틴 리처드가](https://ko.wikipedia.org/wiki/마틴_리처드 "wikilink") 설계한 [절차적](https://ko.wikipedia.org/wiki/절차적_프로그래밍 "wikilink") [명령형](https://ko.wikipedia.org/wiki/명령형_프로그래밍 "wikilink"), [구조적](https://ko.wikipedia.org/wiki/구조적_프로그래밍 "wikilink") [컴퓨터](https://ko.wikipedia.org/wiki/컴퓨터 "wikilink") [프로그래밍 언어이다](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink").

원래 다른 언어들을 위한 [컴파일러](https://ko.wikipedia.org/wiki/컴파일러 "wikilink")를 작성하기 위해 고안하였다가, BCPL은 더 이상 일반적으로 쓰이지 않게 되었다. 그러나 이 언어의 영향력은 여전한데 BCPL을 문법적으로 변경한 것이 이른바 [B이고](https://ko.wikipedia.org/wiki/B_\(프로그래밍_언어\) "wikilink"), [C 프로그래밍 언어가](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 이것 위에 기반을 두었기 때문이다. 이로 말미암아 수많은 C 프로그래머들에게 **Before C Programming Language**라는 유머러스한 [배크로님](https://ko.wikipedia.org/wiki/배크로님 "wikilink")을 선사해 주었다.\[1\]

BCPL은 활 괄호(`{ }`)를 사용한 최초의 프로그래밍 언어이다. 괄호는 거듭되는 문법의 변화를 생존시켰고, 프로그램 소스 코드의 문들을 표기하는 일반적인 수단이 되었다. 현실적으로 당시 키보드의 제한으로 소스 프로그램들은 종종 { } 기호 대신 $( 와 $) 기호를 종종 사용하였다. BCPL에서 쓰이는 '//'라는 한 줄 [주석은](../Page/주석_\(프로그래밍\).md "wikilink") [C에](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 도입되지 않았지만 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")과 나중에 [C99](https://ko.wikipedia.org/wiki/C99 "wikilink")에 다시 등장하였다.

## 예

아래의 완전하고 호환성 있는 예제는 마틴 리처드의 BCPL 배포판에서 가져온 것이다.

팩토리얼 인쇄:

    GET "LIBHDR"

    LET START() = VALOF $(
        FOR I = 1 TO 5 DO
            WRITEF("%N! = %I4*N", I, FACT(I))
        RESULTIS 0
    $)

    AND FACT(N) = N = 0 -> 1, N * FACT(N - 1)

[N퀸 문제의](https://ko.wikipedia.org/wiki/8퀸_문제 "wikilink") 카운트 해결책:

    GET "LIBHDR"

    GLOBAL $(
        COUNT: 200
        ALL: 201
    $)

    LET TRY(LD, ROW, RD) BE
        TEST ROW = ALL THEN
            COUNT := COUNT + 1
        ELSE $(
            LET POSS = ALL & ~(LD | ROW | RD)
            UNTIL POSS = 0 DO $(
                LET P = POSS & -POSS
                POSS := POSS - P
                TRY(LD + P << 1, ROW + P, RD + P >> 1)
            $)
        $)

    LET START() = VALOF $(
        ALL := 1
        FOR I = 1 TO 12 DO $(
            COUNT := 0
            TRY(0, 0, 0)
            WRITEF("%I2-QUEENS PROBLEM HAS %I5 SOLUTIONS*N", I, COUNT)
            ALL := 2 * ALL + 1
        $)
        RESULTIS 0
    $)

## 각주

[분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:구조적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:구조적_프로그래밍_언어 "wikilink") [분류:시스템 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:시스템_프로그래밍_언어 "wikilink")

1.  Expert C Programming: Deep C Secrets by Peter Van Der Linden (Prentice Hall, 1994)