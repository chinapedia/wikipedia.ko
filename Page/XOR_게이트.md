> This article is converted from Wikipedia: [XOR 게이트](https://ko.wikipedia.org/wiki/XOR_게이트).


|           |            |
| --------- | ---------- |
| **INPUT** | **OUTPUT** |
| A         | B          |
| 0         | 0          |
| 0         | 1          |
| 1         | 0          |
| 1         | 1          |

[thumb](https://ko.wikipedia.org/wiki/파일:CMOS_XOR_Gate.svg "wikilink") **XOR 게이트**, **EOR 게이트**, **EXOR 게이트**는 참 입력의 개수가 홀수일 때 참 (1/HIGH) 출력을 내보내는 디지털 [논리 게이트이다](https://ko.wikipedia.org/wiki/논리_게이트 "wikilink"). [배타적 논리합을](../Page/배타적_논리합.md "wikilink") 구현하며 게이트의 입력 중 하나만이 오직 참이라면 그 결과는 참이 된다.

XOR 게이트는 exclusive OR 게이트의 줄임말로 한국어로는 상호 배제적인 OR 게이트이다. 상호 배제적 OR 게이트란 이름의 의미는 OR 게이트와 동일하게 작동하지만 입력값이 동일한 경우에는 1을 출력하지 않는다는 의미이다. 입력값이 서로 다르면 1을 출력하고, 같으면 0을 출력한다.

## 기호

XOR 게이트의 기호는 두 가지가 있다. 전통적인 기호, [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") 기호. 더 자세한 정보는 [논리 게이트 기호를](https://ko.wikipedia.org/wiki/논리_게이트 "wikilink") 참조.

|                                                                             |  |                                                                           |
| --------------------------------------------------------------------------- |  | ------------------------------------------------------------------------- |
| [파일:XOR ANSI.svg](https://ko.wikipedia.org/wiki/파일:XOR_ANSI.svg "wikilink") |  | [파일:XOR IEC.svg](https://ko.wikipedia.org/wiki/파일:XOR_IEC.svg "wikilink") |
| 전통적인 XOR 기호                                                                 |  | IEEE XOR 기호                                                               |

{{-}}

[논리 기호](https://ko.wikipedia.org/wiki/논리_기호_목록 "wikilink") ⊕, [J*pq*](../Page/배타적_논리합.md "wikilink"), 그리고 ⊻는 대수식에서 XOR을 가리키는데 사용할 수 있다.

[C 계열 언어는](https://ko.wikipedia.org/wiki/C_프로그래밍_언어 "wikilink") [탈자 기호](https://ko.wikipedia.org/wiki/탈자_기호 "wikilink") **^**를 사용하여 비트의 배타논리합을 지시한다. (이 언어 계열에서 탈자 기호는 기호의 유사성에도 불구하고 [논리곱](https://ko.wikipedia.org/wiki/논리곱 "wikilink")(AND)을 의미하지 않는다.)

## 패스 게이트 로직 와이어링

XOR 게이트는 [MOSFET](../Page/MOSFET.md "wikilink")을 사용하여 구성할 수 있다. XOR 게이트의 [패스 트랜지스터 로직](https://ko.wikipedia.org/wiki/패스_트랜지스터_로직 "wikilink") 구현 도표는 아래와 같다.\[1\]\[2\]\[3\]\[4\]\[5\]\[6\]

[thumb](https://ko.wikipedia.org/wiki/파일:CmosXORGate.png "wikilink")

## 대안

특정한 종류의 게이트를 사용할 수 없으면 사용 가능한 다른 게이트로부터 동일한 기능을 구현하는 회로를 구성할 수 있다. XOR 함수를 구현하는 회로는 XNOR 게이트, 그리고 NOT 게이트를 통해 구성할 수 있다.

|                                                                        |                                                                       |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------- |
| [frame](https://ko.wikipedia.org/wiki/파일:XOR_from_NAND.svg "wikilink") | [frame](https://ko.wikipedia.org/wiki/파일:XOR_from_NOR.svg "wikilink") |

|                                                                          |
| ------------------------------------------------------------------------ |
| [frame](https://ko.wikipedia.org/wiki/파일:254px_3gate_XOR.jpg "wikilink") |

{{-}}

## 같이 보기

  - [AND 게이트](../Page/AND_게이트.md "wikilink")
  - [OR 게이트](../Page/OR_게이트.md "wikilink")
  - [NOT 게이트](https://ko.wikipedia.org/wiki/NOT_게이트 "wikilink")
  - [NAND 게이트](../Page/NAND_게이트.md "wikilink")
  - [NOR 게이트](../Page/NOR_게이트.md "wikilink")

## 각주

## 외부 링크

  - [Interactive XOR Gate](https://web.archive.org/web/20170717073123/http://teahlab.com/xor_gate/), Demonstrate the logic flow of the XOR Gate circuit created with Teahlab's simulator.

[분류:논리 게이트](https://ko.wikipedia.org/wiki/분류:논리_게이트 "wikilink")

1.  ["A comparative performance analysis of various CMOS design techniques for XOR and XNOR circuits: Fig. 7. High performance transmission gate XOR, XNOR circuits"](http://researchtrend.net/ijet/1_Shiv.pdf) .
2.  ["Designing combinational logic gates in CMOS"](http://bwrcs.eecs.berkeley.edu/Classes/ic541ca/ic541ca_f01/Notes/chapter6.pdf). p. 233
3.  ["Transmission Gate XOR"](http://gram.eng.uci.edu/~ece151/ece151/slides2/sld063.htm) .
4.  ["transmission-gate XOR (tiny XOR)"](https://tams-www.informatik.uni-hamburg.de/applets/hades/webdemos/05-switched/40-cmos/xor-tgate.gif)  (via [1](https://tams-www.informatik.uni-hamburg.de/applets/hades/webdemos/05-switched/40-cmos/xor-tgate.html) )
5.  ["Figure 3, Exclusive OR and XNOR gate"](https://wiki.analog.com/university/courses/electronics/electronics-lab-30).
6.  ["Pass-Transistor Logic: Transmission Gate XOR"](https://ece.uwaterloo.ca/~mhanis/ece637/lecture11.pdf) (p. 11)