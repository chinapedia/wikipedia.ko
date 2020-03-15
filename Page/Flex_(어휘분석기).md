> This article is converted from Wikipedia: [Flex \(\)](https://ko.wikipedia.org/wiki/Flex_\(\)).


**flex**는 《fast lexical analyzer generator》의 줄임말로 [lex](https://ko.wikipedia.org/wiki/lex "wikilink")의 기능을 개선한 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink"). 주로 [bison과](../Page/GNU_bison.md "wikilink") 쌍을 이루어 구문 분석기를 만드는 데 사용된다. flex를 이용하면 [C로](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 구문 문석 코드를 만들 수 있다. 한편 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 코드를 만들어 주는 비슷한 기능을 하는 프로그램으로 [flex++](https://ko.wikipedia.org/wiki/flex++ "wikilink")가 있으며 flex와 함께 배포된다. 작성자는 "Vern Paxson"씨로 1987년도에 처음 만들어졌다.

## 예제

아래는 [PL/0](https://ko.wikipedia.org/wiki/PL/0 "wikilink") 프로그래밍 언어를 위한 Flex 스캐너의 예이다.

인식되는 토큰은 다음과 같다: '`+`', '`-`', '`*`', '`/`', '`=`', '`(`', '`)`', '`,`', '`;`', '`.`', '`:=`', '`<`', '`<=`', '`<>`', '`>`', '`>=`'; 숫자: `0-9 {0-9}`; 식별자: `a-zA-Z {a-zA-Z0-9}` 및 키워드: `begin`, `call`, `const`, `do`, `end`, `if`, `odd`, `procedure`, `then`, `var`, `while`.

``` c
%{
#include "y.tab.h"
%}

digit [0-9]
letter [a-zA-Z]

%%
"+" { return PLUS; }
"-" { return MINUS; }
"*" { return TIMES; }
"/" { return SLASH; }
"(" { return LPAREN; }
")" { return RPAREN; }
";" { return SEMICOLON; }
"," { return COMMA; }
"." { return PERIOD; }
":=" { return BECOMES; }
"=" { return EQL; }
"<>" { return NEQ; }
"<" { return LSS; }
">" { return GTR; }
"<=" { return LEQ; }
">=" { return GEQ; }
"begin" { return BEGINSYM; }
"call" { return CALLSYM; }
"const" { return CONSTSYM; }
"do" { return DOSYM; }
"end" { return ENDSYM; }
"if" { return IFSYM; }
"odd" { return ODDSYM; }
"procedure" { return PROCSYM; }
"then" { return THENSYM; }
"var" { return VARSYM; }
"while" { return WHILESYM; }
{letter}({letter}|{digit})* {
                       yylval.id = strdup(yytext);
                       return IDENT;      }
{digit}+ { yylval.num = atoi(yytext);
                       return NUMBER;     }
[ \t\n\r] /* skip whitespace */
. { printf("Unknown character [%c]\n",yytext[0]);
                       return UNKNOWN;    }
%%

int yywrap(void){return 1;}
```

## 관련 항목

  - [lex](https://ko.wikipedia.org/wiki/lex "wikilink")
  - [bison](../Page/GNU_bison.md "wikilink")
  - [yacc](https://ko.wikipedia.org/wiki/yacc "wikilink")
  - [ragel](https://ko.wikipedia.org/wiki/ragel "wikilink")

## 외부 링크

  - [소스포지 웹사이트](http://flex.sourceforge.net/)

  - [ANSI C lex 정의](http://www.quut.com/c/ANSI-C-grammar-l-1998.html)

[분류:컴파일러](https://ko.wikipedia.org/wiki/분류:컴파일러 "wikilink") [분류:구문 분석기](https://ko.wikipedia.org/wiki/분류:구문_분석기 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")