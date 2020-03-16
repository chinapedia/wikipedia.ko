> This article is converted from Wikipedia: [FLOW-MATIC](https://ko.wikipedia.org/wiki/FLOW-MATIC).


**FLOW-MATIC**(본래 이름: B-0 (Business Language version 0))은 영어와 비슷한 최초의 데이터 처리 언어이다. 1955년부터 1959년까지의 기간 동안 [그레이스 호퍼](../Page/그레이스_호퍼.md "wikilink") 하의 [레밍턴 랜드의](../Page/레밍턴_랜드.md "wikilink") [유니박 I용으로](../Page/유니박_I.md "wikilink") 개발되었다. [코볼](../Page/코볼.md "wikilink") 개발에 중대한 영향을 미쳤다.

## 개발

호퍼는 사무용 데이터 처리 고객들이 수학 기호에 불편해한다는 것을 발견하였다. 1953년 말 그녀는 데이터 처리 문제는 영어 키워드를 이용하여 표현되어야 한다고 주장하였으나 랜드 관리부는 이 아이디어가 실현 불가능하다고 생각하였다. 1955년 초, 그녀와 그녀의 팀은 이러한 프로그래밍 언어에 대한 사양을 작성하고 프로토타입을 구현하였다.\[1\] FLOW-MATIC 컴파일러는 1958년 초에 대중들의 이용이 가능하게 되었으며 실질적으로는 1959년에 완성되었다.\[2\]

## 샘플 프로그램

샘플 FLOW-MATIC 프로그램은 다음과 같다:\[3\]\[4\]

``` cobolfree
 (0)  INPUT INVENTORY FILE-A PRICE FILE-B ; OUTPUT PRICED-INV FILE-C UNPRICED-INV
     FILE-D ; HSP D .
 (1)  COMPARE PRODUCT-NO (A) WITH PRODUCT-NO (B) ; IF GREATER GO TO OPERATION 10 ;
     IF EQUAL GO TO OPERATION 5 ; OTHERWISE GO TO OPERATION 2 .
 (2)  TRANSFER A TO D .
 (3)  WRITE-ITEM D .
 (4)  JUMP TO OPERATION 8 .
 (5)  TRANSFER A TO C .
 (6)  MOVE UNIT-PRICE (B) TO UNIT-PRICE (C) .
 (7)  WRITE-ITEM C .
 (8)  READ-ITEM A ; IF END OF DATA GO TO OPERATION 14 .
 (9)  JUMP TO OPERATION 1 .
(10)  READ-ITEM B ; IF END OF DATA GO TO OPERATION 12 .
(11)  JUMP TO OPERATION 1 .
(12)  SET OPERATION 9 TO GO TO OPERATION 2 .
(13)  JUMP TO OPERATION 2 .
(14)  TEST PRODUCT-NO (B) AGAINST ZZZZZZZZZZZZ ; IF EQUAL GO TO OPERATION 16 ;
     OTHERWISE GO TO OPERATION 15 .
(15)  REWIND B .
(16)  CLOSE-OUT FILES C ; D .
(17)  STOP . (END)
```

이 샘플에는 오직 프로그램의 실행문들  섹션만 포함되어 있다. 레코드 필드 와 는  섹션에 정의되며, 여기에는 영어와 같은 문법을 이용하지는 않았다.\[5\]

## 참고문헌

  - Hopper, Grace (1978). Keynote Address, *[History of Programming Languages I](http://portal.acm.org/citation.cfm?id=800025)*. ACM. pp. 16–20.
  - Hopper, Grace (1959). “Automatic programming: Present status and future trends”, *Mechanisation of Thought Processes*, National Physical Laboratory Symposium 10. Her Majesty's Stationery Office. pp 155–200, cited in
  - Sammet, Jean (1969). *Programming Languages: History and Fundamentals*. Prentice-Hall. p. 316–324.
  - Sammet, Jean (1978). "The Early History of COBOL", *[History of Programming Languages I](http://portal.acm.org/citation.cfm?id=800025)*. ACM. pp. 199–243.
  - Sperry Rand Corporation (1957) *[Introducing a New Language for Automatic Programming: Univac Flow-Matic](https://web.archive.org/web/20130702225747/http://www.computerhistory.org/collections/accession/102646140)*

## 각주

<references />

[분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:코볼](https://ko.wikipedia.org/wiki/분류:코볼 "wikilink") [분류:1955년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1955년_개발된_프로그래밍_언어 "wikilink")

1.  Hopper (1978) p. 16.
2.  Sammet (1969) p. 316
3.  Sperry Rand (1957) p. 7.
4.  Sammet (1969) p. 323.
5.  Hopper (1978) p. 18.