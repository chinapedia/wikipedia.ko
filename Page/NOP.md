> This article is converted from Wikipedia: [NOP](https://ko.wikipedia.org/wiki/NOP).


[컴퓨터 과학에서](../Page/컴퓨터_과학.md "wikilink") **NOP** 또는 **NOOP**(No Operation)은 [어셈블리어](../Page/어셈블리어.md "wikilink")의 명령, [프로그래밍 언어의](../Page/프로그래밍_언어.md "wikilink") 문, [컴퓨터 프로토콜](../Page/통신_프로토콜.md "wikilink") 명령의 하나로, 아무 일도 하지 않는다.

## 기계어

| CPU 아키텍처                                                                                                                                                                                                    | [Mnemonic](../Page/기억술.md "wikilink") | [바이트](../Page/바이트.md "wikilink")                 | [Opcode](https://ko.wikipedia.org/wiki/Opcode "wikilink")            |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | ------------------------------------------------ | -------------------------------------------------------------------- |
| [인텔](../Page/인텔.md "wikilink") [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") [CPU](../Page/중앙_처리_장치.md "wikilink") 계열                                                                                 | `NOP`                                 | 1; 1–9 (i686)                                    | [0x](https://ko.wikipedia.org/wiki/16진 "wikilink")90; 0x66 0x90\[1\] |
| [인텔](../Page/인텔.md "wikilink") [8051](https://ko.wikipedia.org/wiki/8051 "wikilink") / [MCS-51](https://ko.wikipedia.org/wiki/MCS-51 "wikilink") 계열                                                         | `NOP`                                 | 1                                                | 0x00                                                                 |
| [ARM A32](../Page/ARM_아키텍처.md "wikilink")                                                                                                                                                                   | `NOP`                                 | 4                                                | 0x00000000                                                           |
| [ARM T32](../Page/ARM_아키텍처.md "wikilink") (16비트)                                                                                                                                                            | `NOP`                                 | 2                                                | 0xb000                                                               |
| [ARM T32](../Page/ARM_아키텍처.md "wikilink") (32비트)                                                                                                                                                            | `NOP`                                 | 4                                                | 0xf3af 8000                                                          |
| [ARM A64](../Page/ARM_아키텍처.md "wikilink") (64비트)                                                                                                                                                            | `NOP`                                 | 4                                                | 0xd503201f                                                           |
| [IBM 시스템/360](https://ko.wikipedia.org/wiki/IBM_시스템/360 "wikilink"), [IBM 시스템/370](https://ko.wikipedia.org/wiki/IBM_시스템/370 "wikilink"), [유니박 시리즈 90](https://ko.wikipedia.org/wiki/유니박_시리즈_90 "wikilink") | `NOP`                                 | 4                                                | 0x47000000 또는 0x470nnnnn 또는 0x47n0nnnn (여기에서 "n"은 임의의 4비트 값)         |
| `NOPR`                                                                                                                                                                                                      | 2                                     | 0x0700 또는 0x070n 또는 0x07n0 (여기에서 "n"은 임의의 4비트 값) |                                                                      |
| [SuperH](https://ko.wikipedia.org/wiki/SuperH "wikilink")                                                                                                                                                   | `NOP`                                 | 2                                                | 0x0009                                                               |
| [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink")                                                                                                                                                  | `NOP`                                 | 4                                                | 0x00000000                                                           |
| [MIPS-X](../Page/MIPS-X.md "wikilink")                                                                                                                                                                      | `NOP`                                 | 4                                                | 0x60000019                                                           |
| [MMIX](../Page/MMIX.md "wikilink")                                                                                                                                                                          | `SWYM`                                | 4                                                | 0xfd\*\*\*\*\*\*                                                     |
| [모토로라 68000 패밀리](https://ko.wikipedia.org/wiki/모토로라_68000_패밀리 "wikilink")                                                                                                                                   | `NOP`                                 | 2                                                | 0x4e71                                                               |
| [모토로라 6809](https://ko.wikipedia.org/wiki/모토로라_6809 "wikilink")                                                                                                                                             | `NOP`                                 | 1                                                | 0x12                                                                 |
| [MOS 테크놀로지 65xx](https://ko.wikipedia.org/wiki/MOS_테크놀로지_65xx "wikilink") (예: [6502](https://ko.wikipedia.org/wiki/6502 "wikilink"))                                                                        | `NOP`                                 | 1                                                | 0xea                                                                 |
| [파워PC](../Page/파워PC.md "wikilink")                                                                                                                                                                          | `NOP`                                 | 4                                                | 0x60000000                                                           |
| [PIC 마이크로컨트롤러](https://ko.wikipedia.org/wiki/PIC_마이크로컨트롤러 "wikilink")                                                                                                                                       | `NOP`                                 | 12비트                                             | 0b000000000000                                                       |
| [SPARC](../Page/SPARC.md "wikilink")                                                                                                                                                                        | `NOP`                                 | 4                                                | 0x01000000                                                           |
| [Z80](https://ko.wikipedia.org/wiki/Z80 "wikilink")                                                                                                                                                         | `NOP`                                 | 1                                                | 0x00                                                                 |
| [PDP-11](../Page/PDP-11.md "wikilink")                                                                                                                                                                      | `NOP`                                 | 16비트                                             | 000240 (8진법)                                                         |
| [VAX](../Page/VAX.md "wikilink")                                                                                                                                                                            | `NOP`                                 | 1                                                | 0x01                                                                 |

## 코드

### 에이다

[에이다](https://ko.wikipedia.org/wiki/에이다 "wikilink")에서 `null` 문은 NOP 역할을 한다.\[2\]

### 제이쿼리

[제이쿼리](https://ko.wikipedia.org/wiki/제이쿼리 "wikilink") 라이브러리는 아무 것도 하지 않는 `jQuery.noop()` 함수를 제공한다.\[3\]

### 비주얼 베이직

[비주얼 베이직](../Page/비주얼_베이직.md "wikilink") 언어의 `;` 문은 아무 일도 하지 않는다.

## 같이 보기

  - [IEFBR14](../Page/IEFBR14.md "wikilink")

## 각주

[분류:기계어](https://ko.wikipedia.org/wiki/분류:기계어 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink") [분류:무 (철학)](https://ko.wikipedia.org/wiki/분류:무_\(철학\) "wikilink")

1.
2.  [Ada Reference Manual — null statements](http://www.adaic.org/resources/add_content/standards/05aarm/html/AA-5-1.html#S0134). "The execution of a null_statement has no effect."
3.  [jQuery.noop()](http://api.jquery.com/jquery.noop/) from jQuery API documentation