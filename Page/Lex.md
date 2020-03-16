> This article is converted from Wikipedia: [Lex](https://ko.wikipedia.org/wiki/Lex).


**Lex**는 [컴퓨터 과학](../Page/컴퓨터_과학.md "wikilink") 분야에서 [구문 분석을](../Page/구문_분석.md "wikilink") 위한 대표적인 프로그램이다.\[1\] Lex는 일반적으로 [파서](https://ko.wikipedia.org/wiki/파서 "wikilink")(Parser) 제작을 담당하는 [Yacc](../Page/Yacc.md "wikilink")와 함께 사용된다. Lex는 [에릭 슈미트와](../Page/에릭_슈미트.md "wikilink") 마이크 레스크가 만든 것으로, 대부분의 [유닉스](../Page/유닉스_계열.md "wikilink") 시스템의 구문 분석 표준으로 사용되고 있고, 그 정의는 [POSIX](../Page/POSIX.md "wikilink") 표준에 명시되어 있다.

Lex는 구문 분석기를 읽어와서, Lexer를 만든 뒤 이를 C 언어로 만들어진 소스 코드의 형태로 출력한다.

Lex는 저작권이 있는 소프트웨어로 시작했지만, [AT\&T](../Page/AT&T.md "wikilink")의 소스 코드에 기반하는 버전은 [오픈 소스](../Page/오픈_소스.md "wikilink") 정책을 따라 [오픈 솔라리스](https://ko.wikipedia.org/wiki/오픈_솔라리스 "wikilink") 등에서 사용된다. 이외에도 유명한 [오픈 소스](../Page/오픈_소스.md "wikilink") 버전의 Lex로는 빠른 Lex(Fast Lex)라는 의미의 [flex가](https://ko.wikipedia.org/wiki/flex_\(어휘분석기\) "wikilink") 존재한다.

## Lex 파일의 예

``` c
/*** Definition section ***/

%{
/* C code to be copied verbatim */
#include <stdio.h>
%}

/* This tells flex to read only one input file */
%option noyywrap

%%
    /*** Rules section ***/

    /* [0-9]+ matches a string of one or more digits */
[0-9]+  {
            /* yytext is a string containing the matched text. */
            printf("Saw an integer: %s\n", yytext);
        }

.|\n    {   /* Ignore all other characters. */   }

%%
/*** C Code section ***/

int main(void)
{
    /* Call the lexer, then quit. */
    yylex();
    return 0;
}
```

입력이 `flex`에 제공되면 C 파일 로 변환된다. 정수의 문자열과 일치하여 출력하는 실행 파일로 컴파일된다. 이를테면 아래와 같이 입력하면:

`abc123z.!&*2gj6`

프로그램은 다음과 같이 출력한다:

`Saw an integer: 123`
`Saw an integer: 2`
`Saw an integer: 6`

## 각주

[분류:컴파일 도구](https://ko.wikipedia.org/wiki/분류:컴파일_도구 "wikilink") [분류:구문 분석기](https://ko.wikipedia.org/wiki/분류:구문_분석기 "wikilink")

1.  [1. Levine, John R; Mason, Tony; Brown, Doug (1992). LEX & YACC (2 ed.). O'Reilly. pp. 1-2. ISBN 1-56592-000-7.](http://books.google.co.in/books?id=YrzpxNYegEkC&printsec=frontcover#PPA1,M1)