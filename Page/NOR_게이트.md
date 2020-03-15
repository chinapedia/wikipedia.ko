> This article is converted from Wikipedia: [NOR ](https://ko.wikipedia.org/wiki/NOR_).


|           |            |
| --------- | ---------- |
| **INPUT** | **OUTPUT** |
| A         | B          |
| 0         | 0          |
| 0         | 1          |
| 1         | 0          |
| 1         | 1          |

**NOR 게이트**는 [부정논리합](https://ko.wikipedia.org/wiki/부정논리합 "wikilink")을 구현하는 디지털 [논리 회로이며](https://ko.wikipedia.org/wiki/논리_회로 "wikilink") 진리표에 따라 동작한다. 게이트에 대한 두 개의 입력이 LOW(0)이면 HIGH(1) 출력이 발생하며, 두 입력 중 하나가 HIGH(1)이면 LOW 출력(0)이 발생한다. NOR은 [OR](../Page/OR_게이트.md "wikilink") 연산자의 [부정](https://ko.wikipedia.org/wiki/부정 "wikilink")의 결과이다. AND 게이트에서 모든 입력이 반전된 것으로 간주할 수도 있다.

오리지널 [아폴로 가이던스 컴퓨터는](https://ko.wikipedia.org/wiki/아폴로_가이던스_컴퓨터 "wikilink") 4,100개의 IC를 사용하였으며 각각이 하나의 3개의 입력 NOR 게이트만을 포함하고 있었다.

## 기호

NOR 게이트에는 3개의 기호가 있다: ANSI(미국식) 기호, IEC(유럽식) 기호, 사용이 권장되지 않는 [DIN](https://ko.wikipedia.org/wiki/독일_공업_규격_위원회 "wikilink") 기호. 더 자세한 정보는 [논리 회로](https://ko.wikipedia.org/wiki/논리_회로 "wikilink") 문서 참조. NOR 게이트의 ANSI 기호는 도치 버블(inversion bubble)이 연결된 표준 OR 게이트이다.

|                                                                                               |                                                                           |                                                                           |
| --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [파일:NOR ANSI Labelled.svg](https://ko.wikipedia.org/wiki/파일:NOR_ANSI_Labelled.svg "wikilink") | [파일:NOR IEC.svg](https://ko.wikipedia.org/wiki/파일:NOR_IEC.svg "wikilink") | [파일:NOR DIN.svg](https://ko.wikipedia.org/wiki/파일:NOR_DIN.svg "wikilink") |
| MIL/ANSI 기호                                                                                   | IEC 기호                                                                    | DIN 기호                                                                    |

{{-}}

[섬네일](https://ko.wikipedia.org/wiki/파일:NorAdder.svg "wikilink").\]\]

## 하드웨어 기술 및 핀

NOR 게이트는 기본적인 논리 게이트이므로 이들은 [TTL과](https://ko.wikipedia.org/wiki/트랜지스터-트랜지스터_논리 "wikilink") [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink") [IC에서](https://ko.wikipedia.org/wiki/집적_회로 "wikilink") 인식된다. 표준 4000 시리즈인 CMOS IC는 4001이며 4개의 독립적인 2개의 입력, NOR 게이트를 포함한다. 핀 그림은 다음과 같다:

<table>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/파일:NOR_Pinout.jpg" title="wikilink">left</a>-포맷 IC의 핀 그림]]</p></td>
<td><p><code> 1  Input A1</code><br />
<code> 2  Input B1</code><br />
<code> 3  Output Q1</code><br />
<code> 4  Output Q2</code><br />
<code> 5  Input B2</code><br />
<code> 6  Input A2</code><br />
<code> 7  V</code><sub><code>ss</code></sub><br />
<code> 8  Input A3</code><br />
<code> 9  Input B3</code><br />
<code> 10 Output Q3</code><br />
<code> 11 Output Q4</code><br />
<code> 12 Input B4</code><br />
<code> 13 Input A4</code><br />
<code> 14 V</code><sub><code>dd</code></sub></p></td>
</tr>
</tbody>
</table>

### 이용

아래의 장치들은 [페어차일드 반도체](https://ko.wikipedia.org/wiki/페어차일드_반도체 "wikilink"), [필립스](https://ko.wikipedia.org/wiki/필립스 "wikilink"), [텍사스 인스트루먼트와](https://ko.wikipedia.org/wiki/텍사스_인스트루먼트 "wikilink") 같은 대부분의 반도체 제조업체들로부터 이용이 가능하다. 이들은 보통 스루홀 [DIP](https://ko.wikipedia.org/wiki/이중_직렬_패키지 "wikilink") 및 [SOIC](https://ko.wikipedia.org/wiki/SOIC "wikilink") 포맷으로 이용할 수 있다. 대부분의 [데이터시트 데이터베이스를](https://ko.wikipedia.org/wiki/데이터시트 "wikilink") 통해 데이터시트를 쉽게 이용할 수 있다.

유명한 CMOS 및 TTL 논리 계열에서 최대 8개의 입력을 갖춘 NOR 게이트를 사용할 수 있다:

  - [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink")
      - 4001: Quad 2-input NOR gate
      - 4025: Triple 3-input NOR gate
      - 4002: Dual 4-input NOR gate
      - 4078: Single 8-input NOR gate
  - [TTL](https://ko.wikipedia.org/wiki/트랜지스터-트랜지스터_논리 "wikilink")
      - 7402: Quad 2-input NOR gate
      - 7427: Triple 3-input NOR gate
      - 7425: Dual 4-input NOR gate (w/ strobe, 사용이 권장되지 않음)
      - 74260: Dual 5-Input NOR Gate
      - 744078: Single 8-input NOR Gate

오래된 [RTL](https://ko.wikipedia.org/wiki/저항-트랜지스터_논리 "wikilink") 및 [ECL](https://ko.wikipedia.org/wiki/ECL "wikilink") 계열에서 NOR 게이트는 효율적이었으며 매우 흔히 사용되었다.

## 구현

|                                                                   |                                                                            |                                                                               |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [frame](https://ko.wikipedia.org/wiki/파일:NMOS_NOR.png "wikilink") | [thumbnail](https://ko.wikipedia.org/wiki/파일:PMOS-NOR-gate.svg "wikilink") | [right](https://ko.wikipedia.org/wiki/파일:NOR_gate_layout.png "wikilink").\]\] |

위의 그림은 [NMOS 논리](../Page/NMOS_논리.md "wikilink") 회로를 사용하는 2-input NOR 게이트의 구성을 보여준다.

아래의 그림은 [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink") 기술을 사용하는 2-input NOR 게이트를 보여준다. [섬네일](https://ko.wikipedia.org/wiki/파일:Cmosunbuff.png "wikilink")

### 대안

특정 NOR 게이트를 사용할 수 없으면 [NAND](../Page/NAND_게이트.md "wikilink") 게이트로부터 만들 수 있는데, 그 이유는 NAND와 NOR 게이트는 유니버설 게이트(universal gate)로 간주되기 때문이다. 즉, 다른 모든 게이트를 만드는데 사용할 수 있다는 의미이다.\[1\]

| NAND 구성                                                                               |
| ------------------------------------------------------------------------------------- |
| [파일:NOR from NAND.svg](https://ko.wikipedia.org/wiki/파일:NOR_from_NAND.svg "wikilink") |

## 같이 보기

  - [AND 게이트](../Page/AND_게이트.md "wikilink")
  - [OR 게이트](../Page/OR_게이트.md "wikilink")
  - [NOT 게이트](https://ko.wikipedia.org/wiki/NOT_게이트 "wikilink")
  - [NAND 게이트](../Page/NAND_게이트.md "wikilink")
  - [XOR 게이트](../Page/XOR_게이트.md "wikilink")
  - [XNOR 게이트](https://ko.wikipedia.org/wiki/XNOR_게이트 "wikilink")
  - [불 논리](https://ko.wikipedia.org/wiki/불_논리 "wikilink")
  - [논리 회로](https://ko.wikipedia.org/wiki/논리_회로 "wikilink")
  - [NOR 로직](https://ko.wikipedia.org/wiki/NOR_로직 "wikilink")
  - [플래시 메모리](https://ko.wikipedia.org/wiki/플래시_메모리 "wikilink")

## 각주

## 외부 링크

  - [Interactive NOR gate](https://web.archive.org/web/20170729191249/http://teahlab.com/nor_gate/), Displays the logic simulation of the NOR Gate.

[분류:논리 게이트](https://ko.wikipedia.org/wiki/분류:논리_게이트 "wikilink")

1.  Mano, M. Morris and Charles R. Kime. *Logic and Computer Design Fundamentals, Third Edition.* Prentice Hall, 2004. p. 73.