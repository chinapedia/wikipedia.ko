> This article is converted from Wikipedia: [AND ](https://ko.wikipedia.org/wiki/AND_).


|           |            |
| --------- | ---------- |
| **INPUT** | **OUTPUT** |
| A         | B          |
| 0         | 0          |
| 0         | 1          |
| 1         | 0          |
| 1         | 1          |

**AND 게이트**는 [논리곱](https://ko.wikipedia.org/wiki/논리곱 "wikilink")을 구현하는 기본 [디지털](https://ko.wikipedia.org/wiki/디지털 "wikilink") [논리 게이트이다](https://ko.wikipedia.org/wiki/논리_게이트 "wikilink").

## 기호

AND 게이트에는 세 가지 [기호](https://ko.wikipedia.org/wiki/기호 "wikilink")가 있다: [ANSI](https://ko.wikipedia.org/wiki/ANSI "wikilink")(미국식) 기호, [IEC](https://ko.wikipedia.org/wiki/국제_전기_표준_회의 "wikilink")(유럽식) 기호, 현재는 사용이 권장되지 않는 [DIN](https://ko.wikipedia.org/wiki/독일_공업_규격_위원회 "wikilink") 기호. 더 자세한 정보는 [논리 게이트](https://ko.wikipedia.org/wiki/논리_게이트 "wikilink") 문서를 참조.

|                                                                             |                                                                           |                                                                           |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [파일:AND ANSI.svg](https://ko.wikipedia.org/wiki/파일:AND_ANSI.svg "wikilink") | [파일:AND IEC.svg](https://ko.wikipedia.org/wiki/파일:AND_IEC.svg "wikilink") | [파일:AND DIN.svg](https://ko.wikipedia.org/wiki/파일:AND_DIN.svg "wikilink") |
| MIL/ANSI 기호                                                                 | IEC 기호                                                                    | DIN 기호                                                                    |

"A", "B" 입력과 "C" 출력이 있는 AND 게이트는 \(C = A \cdot B\)라는 논리식을 구현한다.

## 구현

|                                                                     |                                                                          |                                                                      |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------ | -------------------------------------------------------------------- |
| [섬네일](https://ko.wikipedia.org/wiki/파일:DiodeANDgate.png "wikilink") | [섬네일](https://ko.wikipedia.org/wiki/파일:TransistorANDgate.png "wikilink") | [섬네일](https://ko.wikipedia.org/wiki/파일:NMOS_AND_gate.png "wikilink") |

AND 게이트는 일반적으로 N채널(그림)이나 P채널 [MOSFET](https://ko.wikipedia.org/wiki/MOSFET "wikilink")을 사용하여 설계된다. 디지털 입력 "a"와 "b"는 출력 "F"가 AND와 동일한 결과를 갖도록 만든다.

### 대안

특정 AND 게이트를 사용할 수 없으면 [NAND나](https://ko.wikipedia.org/wiki/NAND_게이트 "wikilink") [NOR](https://ko.wikipedia.org/wiki/NOR_게이트 "wikilink") 게이트로부터 만들 수 있는데 NAND와 NOR 게이트가 "유니버설 게이트"(universal gate)로 간주되기 때문이며\[1\] 이들을 사용하여 다른 모든 것들을 만들 수 있다는 의미이다.

| 원하는 게이트                                                                                       | NAND 구성                                                                               | NOR 구성                                                                                |
| --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| [파일:AND ANSI Labelled.svg](https://ko.wikipedia.org/wiki/파일:AND_ANSI_Labelled.svg "wikilink") | [파일:AND from NAND.svg](https://ko.wikipedia.org/wiki/파일:AND_from_NAND.svg "wikilink") | [파일:AND using NOR.svg](https://ko.wikipedia.org/wiki/파일:AND_using_NOR.svg "wikilink") |
|                                                                                               |                                                                                       |                                                                                       |

## IC 패키지

AND 게이트는 IC 패키지에서 이용이 가능하다. 7408 IC는 저명한 QUAD 2-Input AND GATES이며 4개의 독립 게이트를 포함하고 있고 논리 AND를 수행한다. [섬네일](https://ko.wikipedia.org/wiki/파일:QUAD_2-Input_AND_GATE_IC.png "wikilink")

## 같이 보기

  - [OR 게이트](../Page/OR_게이트.md "wikilink")
  - [NOT 게이트](https://ko.wikipedia.org/wiki/NOT_게이트 "wikilink")
  - [NAND 게이트](https://ko.wikipedia.org/wiki/NAND_게이트 "wikilink")
  - [NOR 게이트](https://ko.wikipedia.org/wiki/NOR_게이트 "wikilink")
  - [XOR 게이트](https://ko.wikipedia.org/wiki/XOR_게이트 "wikilink")
  - [XNOR 게이트](https://ko.wikipedia.org/wiki/XNOR_게이트 "wikilink")
  - [IMPLY 게이트](https://ko.wikipedia.org/wiki/IMPLY_게이트 "wikilink")
  - [논리 게이트](https://ko.wikipedia.org/wiki/논리_게이트 "wikilink")

## 각주

[분류:논리 게이트](https://ko.wikipedia.org/wiki/분류:논리_게이트 "wikilink")

1.  Mano, M. Morris and Charles R. Kime. *Logic and Computer Design Fundamentals, Third Edition.* Prentice Hall, 2004. p. 73.