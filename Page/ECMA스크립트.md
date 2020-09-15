> This article is converted from Wikipedia: [ECMA스크립트](https://ko.wikipedia.org/wiki/ECMA스크립트).


**ECMA스크립트**(ECMAScript, 또는 ES\[1\])란, [Ecma International이](../Page/Ecma_인터내셔널.md "wikilink") **ECMA-262** 기술 규격에 따라 정의하고 있는 표준화된 [스크립트 프로그래밍 언어를](https://ko.wikipedia.org/wiki/스크립트_프로그래밍_언어 "wikilink") 말한다. [자바스크립트](../Page/자바스크립트.md "wikilink")를 표준화하기 위해 만들어졌다. [액션스크립트](../Page/액션스크립트.md "wikilink")와 [J스크립트](../Page/J스크립트.md "wikilink") 등 다른 구현체도 포함하고 있다.\[2\] ECMA스크립트는 [웹의](../Page/월드_와이드_웹.md "wikilink") 클라이언트 사이드 스크립트로 많이 사용되며 [Node.js](../Page/Node.js.md "wikilink")를 사용한 서버 응용 프로그램 및 서비스에도 점차 많이 쓰이고 있다.

## 역사

1996년 3월, [넷스케이프](../Page/넷스케이프.md "wikilink")에서 [넷스케이프 네비게이터](https://ko.wikipedia.org/wiki/넷스케이프_네비게이터 "wikilink") 2.0을 출시하면서 자바스크립트를 지원하기 시작했다. 웹 페이지 동작을 향상시키는 언어로서 자바스크립트의 성공은, [마이크로소프트](../Page/마이크로소프트.md "wikilink")가 이와 "적당히" 호환되는 J스크립트를 개발하는 계기가 되었다. J스크립트는 1996년 8월, [인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") 3.0에 포함되어 출시되었다.

넷스케이프는 표준화를 위해 자바스크립트 기술 규격을 [Ecma 인터내셔널에](../Page/Ecma_인터내셔널.md "wikilink") 제출하였고, 이 규격에 대한 작업은 ECMA-262의 이름으로 1996년 11월부터 시작됐다. ECMA-262의 초판은 ECMA 일반 회의에서 1997년 6월 채택됐다.

ECMA스크립트는 ECMA-262에 의해 표준화된 언어의 이름이다. 자바스크립트와 J스크립트는 모두 ECMA스크립트와의 호환을 목표로 하면서, ECMA 규격에 포함되지 않는 확장 기능을 제공한다.

### 판본

ECMA-262는 10개의 판이 출판되었다. 10판 표준에 대한 작업은 2019년 6월에 마무리됐다.

| 판   | 출판일       | 이름                       | 이전 판과의 차이점                                                                                                                                                 |
| --- | --------- | ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | 1997년 6월  |                          | 초판                                                                                                                                                         |
| 2   | 1998년 6월  |                          | ISO/IEC 16262 국제 표준과 완전히 동일한 규격을 적용하기 위한 변경.                                                                                                               |
| 3   | 1999년 12월 |                          | 강력한 정규 표현식, 향상된 문자열 처리, 새로운 제어문 , try/catch 예외 처리, 엄격한 오류 정의, 수치형 출력의 포매팅 등.                                                                               |
| 4   | 버려짐       |                          | 4번째 판은 언어에 얽힌 정치적 차이로 인해 버려졌다. 이 판을 작업 가운데 일부는 5번째 판을 이루는 기본이 되고 다른 일부는 ECMA스크립트의 기본을 이루고 있다.                                                              |
| 5   | 2009년 12월 |                          | 더 철저한 오류 검사를 제공하고 오류 경향이 있는 구조를 피하는 하부집합인 "strict mode"를 추가한다. 3번째 판의 규격에 있던 수많은 애매한 부분을 명확히 한다.\[3\]                                                      |
| 5.1 | 2011년 6월  |                          | ECMA스크립트 표준의 제 5.1판은 ISO/IEC 16262:2011 국제 표준 제3판과 함께 한다.                                                                                                  |
| 6   | 2015년 6월  | ECMAScript 2015 (ES2015) | 6판에는 클래스와 모듈 같은 복잡한 응용 프로그램을 작성하기 위한 새로운 문법이 추가되었다. 하지만 이러한 문법의 의미는 5판의 strict mode와 같은 방법으로 정의된다. 이 판은 "ECMAScript Harmony" 혹은 "ES6 Harmony" 등으로 불리기도 한다. |
| 7   | 2016년 6월  | ECMAScript 2016 (ES2016) | 제곱연산자 추가, Array.prototype.includes                                                                                                                         |
| 8   | 2017년 6월  | ECMAScript 2017 (ES2017) | 함수 표현식의 인자에서 trailing commas 허용, Object values/entries 메소드, async/await 등.                                                                                 |
| 9   | 2018년 6월  | ECMAScript 2018 (ES2018) | Promise.finally, Async iteration, object rest/spread property 등.                                                                                           |
| 10  | 2019년 6월  | ECMAScript 2019 (ES2019) | Object.fromEntries, flat, flatMap, Symbol.description, optional catch 등.                                                                                   |

2004년 6월에 Ecma 인터내셔널은 [E4X](https://ko.wikipedia.org/wiki/E4X "wikilink")(XML을 위한 ECMA스크립트)로 알려진 ECMA스크립트의 확장을 정의하는 ECMA-357을 출판했으나 2015년에 표준에서 제외됐다.\[4\]\[5\]

## 같이 보기

  - [자바스크립트](../Page/자바스크립트.md "wikilink")
  - [J스크립트](../Page/J스크립트.md "wikilink")

## 각주

<references />

## 외부 링크

  -
<!-- end list -->

  - ISO 표준

<!-- end list -->

  - [ISO 16262](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=55755)

<!-- end list -->

  - ECMA 표준

<!-- end list -->

  - [표준 ECMA-262 ECMA스크립트 언어 규격](http://www.ecma-international.org/publications/standards/Ecma-262.htm)
      - [표준 ECMA-262 ECMA스크립트 언어 규격 3판 (1999년 12월)](http://www.ecma-international.org/publications/files/ECMA-ST-ARCH/ECMA-262,%203rd%20edition,%20December%201999.pdf)
      - [표준 ECMA-262 ECMA스크립트 언어 규격 3판 최종 (2000년 3월 24일)](http://wayback.archive.org/web/20100201000000*/http://www.mozilla.org/js/language/E262-3.pdf)
      - [표준 ECMA-262 ECMA스크립트 언어 규격 5판 (2009년 12월)](http://www.ecma-international.org/publications/files/ECMA-ST-ARCH/ECMA-262%205th%20edition%20December%202009.pdf)
      - [표준 ECMA-262 ECMA스크립트 언어 규격 5.1판 (2011년 6월)](https://web.archive.org/web/20111103184035/http://www.ecma-international.org/publications/files/ECMA-ST/ECMA-262%20edition%205.1,%20June%202011.pdf)
      - [표준 ECMA-262 ECMA스크립트 언어 규격 6판 (2015년 6월)](https://web.archive.org/web/20150412040502/http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-262.pdf)
      - [표준 ECMA-262 ECMA스크립트 언어 규격 9판 (2018년 6월)](http://ecma-international.org/ecma-262/9.0/index.html)
      - [표준 ECMA-262 ECMA스크립트 언어 규격 10판 (2019년 6월)](http://ecma-international.org/ecma-262/10.0/index.html)
  - [표준 ECMA-290 ECMA스크립트 컴포넌트 규격 (1999년 6월)](http://www.ecma-international.org/publications/standards/Ecma-290.htm)
  - [표준 ECMA-327 ECMA스크립트 3판 축약판 (2001년 6월)](http://www.ecma-international.org/publications/standards/Ecma-327.htm)
  - [표준 ECMA-357 XML을 위한 ECMA스크립트(E4X) 규격 (2004년 6월)](https://web.archive.org/web/20131104082608/http://www.ecma-international.org/publications/standards/Ecma-357.htm)

[분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:ISO 표준](https://ko.wikipedia.org/wiki/분류:ISO_표준 "wikilink") [분류:C 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어_계열 "wikilink") [분류:자바스크립트 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:자바스크립트_프로그래밍_언어_계열 "wikilink") [분류:컴퓨터 표준](https://ko.wikipedia.org/wiki/분류:컴퓨터_표준 "wikilink") [분류:Ecma 표준](https://ko.wikipedia.org/wiki/분류:Ecma_표준 "wikilink")

1.
2.
3.  [Changes to JavaScript, Part 1: EcmaScript 5](https://www.youtube.com/watch?v=Kq4FpMe6cRs)
4.
5.