> This article is converted from Wikipedia: [ANTLR](https://ko.wikipedia.org/wiki/ANTLR).


컴퓨터 기반 언어 인식에서 **ANTLR**(앤틀러, Another Tool For Language Recognition)는 구문 분석을 위해 [LL(\*)을](https://ko.wikipedia.org/wiki/LL_파서 "wikilink") 사용하는 [파서 발생기이다](https://ko.wikipedia.org/wiki/컴파일러_컴파일러 "wikilink"). ANTLR은 1989년 처음 개발된 PCCTS(Purdue Compiler Construction Tool Set)의 뒤를 이으며 현재 개발이 진행 중이다. 유지보수는 [샌프란시스코 대학교의](https://ko.wikipedia.org/wiki/샌프란시스코_대학교 "wikilink") [Terence Parr](https://ko.wikipedia.org/wiki/Terence_Parr "wikilink") 교수가 맡고 있다.

## 예

다음의 예에서 ANTLR의 파서는 "1 + 2 + 3"의 식의 합의 형태로 표시할 수 있다:

``` antlr
 // Common options, for example, the target language
 options
 {
  language = "CSharp";
 }
 // Followed by the parser
 class SumParser extends Parser;
 options
 {
   k = 1; // Parser Lookahead: 1 Token
 }
 // Definition of an expression
 statement: INTEGER (PLUS^ INTEGER)*;
 // Here is the Lexer
 class SumLexer extends Lexer;
 options
 {
   k = 1; // Lexer Lookahead: 1 characters
 }
 PLUS: '+';
 DIGIT: ('0'..'9');
 INTEGER: (DIGIT)+;
```

다음의 나열은 프로그램 내 파서 호출을 증명한다:

``` java
 TextReader reader;
 // (...) Fill TextReader with character
 SumLexer lexer = new SumLexer(reader);
 SumParser parser = new SumParser(lexer);

 parser.expression();
```

## 같이 보기

  - [자바CC](../Page/자바CC.md "wikilink")

## 외부 링크

  -
  - [ANTLRWorks](http://tunnelvisionlabs.com/products/demo/antlrworks)

  - [ANTLR Studio](http://www.placidsystems.com/antlrstudio.aspx)

[분류:1992년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1992년_소프트웨어 "wikilink") [분류:퍼블릭 도메인 소프트웨어](https://ko.wikipedia.org/wiki/분류:퍼블릭_도메인_소프트웨어 "wikilink") [분류:구문 분석기](https://ko.wikipedia.org/wiki/분류:구문_분석기 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")