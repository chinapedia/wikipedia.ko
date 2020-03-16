> This article is converted from Wikipedia: [Yacc](https://ko.wikipedia.org/wiki/Yacc).


컴퓨터 소프트웨어인 **Yacc**는 [유닉스](../Page/유닉스.md "wikilink") 시스템의 표준 [파서 생성기이다](https://ko.wikipedia.org/wiki/파서_생성기 "wikilink"). 이름은 "또다른 컴파일러 컴파일러"란 재귀적인 뜻의 영어 Yet Another Compiler Compiler 의 약자에서 왔다. [파서](https://ko.wikipedia.org/wiki/파서 "wikilink")(parser)란 [컴파일러](../Page/컴파일러.md "wikilink")의 일부분으로 입력의 의미부를 구분해 주는 역할을 하며, Yacc는 [배커스-나우르 표기법](https://ko.wikipedia.org/wiki/배커스-나우르_표기법 "wikilink")(BNF)으로 표기된 [문법](../Page/문법.md "wikilink")을 주면 그것에 따르는 파서를 만들 수 있는 [C언어](../Page/C_\(프로그래밍_언어\).md "wikilink") 코드를 만들어 준다.

Yacc는 AT\&T의 스티븐 C. 존슨이 유닉스 운영체제 용으로 개발했다. 후에 버클리 Yacc, [GNU bison](../Page/GNU_bison.md "wikilink"), MKS yacc, Abraxas yacc 등의 호환 클론들이 만들어졌다. 이들은 성능이 향상되고, 부가 기능이 덧붙여 졌지만 기본적인 기능은 동일했다.

Yacc가 만들어내는 파서와 더불어 어휘 분석기(lexical analyzer)가 필요하기 때문에 [Lex](../Page/Lex.md "wikilink")나 [flex](https://ko.wikipedia.org/wiki/flex_\(어휘분석기\) "wikilink") 같은 어휘 분석기 생성기가 같이 쓰인다. [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") [POSIX](../Page/POSIX.md "wikilink") P1003.2 표준은 Lex와 Yacc의 기능과 요구사항을 정의하고 있다.

## 같이 보기

  - [GNU bison](../Page/GNU_bison.md "wikilink")
  - [Flex (어휘분석기)](../Page/Flex_\(어휘분석기\).md "wikilink")

## 외부 링크

  - [버클리 Yacc](http://dickey.his.com/byacc/byacc.html): 특정 C 컴파일러에의 종속성을 피하기 위해 만들어진 yacc
  - [Essence](https://web.archive.org/web/20050305150105/http://www.informatik.uni-freiburg.de/proglang/software/essence/), 스킴 프로그래밍 언어용 [LR(1)](https://ko.wikipedia.org/wiki/LR\(1\) "wikilink") 파서
  - [Parser-tools](https://web.archive.org/web/20050416083124/http://download.plt-scheme.org/scheme/plt/collects/parser-tools/) for DrScheme.
  - [ML-Yacc](http://www.smlnj.org/doc/ML-Yacc/index.html) 표준 ML 용 yacc

[분류:컴파일러](https://ko.wikipedia.org/wiki/분류:컴파일러 "wikilink") [분류:구문 분석기](https://ko.wikipedia.org/wiki/분류:구문_분석기 "wikilink")