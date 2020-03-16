> This article is converted from Wikipedia: [VAX](https://ko.wikipedia.org/wiki/VAX).


[섬네일](https://ko.wikipedia.org/wiki/파일:VAX_11-780_intero.jpg "wikilink") **VAX**는 [디지털 이큅먼트 코퍼레이션](../Page/디지털_이큅먼트_코퍼레이션.md "wikilink")(DEC)가 1970년대 중반에 개발한 [명령어 집합 아키텍처](../Page/명령어_집합.md "wikilink")(ISA)이다.

## 명칭

"VAX"는 가상 주소 확장(virtual address extension)의 준말인데, 그 이유는 VAX가 오래된 16비트 [PDP-11](../Page/PDP-11.md "wikilink")의 32비트 확장으로 간주되었고 ([프라임 컴퓨터](https://ko.wikipedia.org/wiki/프라임_컴퓨터 "wikilink") 이후) [가상 메모리를](../Page/가상_메모리.md "wikilink") 처음 채택하여 더 넓은 주소 공간을 관리하였기 때문이다. 초기 버전의 VAX 프로세서는 호환성 모드를 구현하여 PDP-11 명령의 다수를 에뮬레이트하였기에 실제로 이러한 호환성을 강조하여 VAX-11로 불렸다.

## 운영 체제

네이티브 VAX [운영 체제는](../Page/운영_체제.md "wikilink") 디지털의 VAX/VMS였다. (1991년\~1992년 초반에 [OpenVMS](../Page/OpenVMS.md "wikilink")로 이름이 바뀜. 당시 [알파에](../Page/DEC_알파.md "wikilink") 포팅되어 [POSIX](../Page/POSIX.md "wikilink") 표준에 맞게 수정되어 [X/Open](https://ko.wikipedia.org/wiki/X/Open "wikilink") 컨소시엄의 [XPG4](https://ko.wikipedia.org/wiki/XPG4 "wikilink")와 호환된다고 하여 그렇게 정해짐.)\[1\]

## 역사

1977년 10월 25일에 [디지털 이큅먼트 코퍼레이션](../Page/디지털_이큅먼트_코퍼레이션.md "wikilink")(DEC)가 선보인 [VAX-11](https://ko.wikipedia.org/wiki/VAX-11 "wikilink")/780이 이 아키텍처를 구현한 영향력 있는 [컴퓨터](../Page/컴퓨터.md "wikilink")들 가운데 최초의 것이다.\[2\] [케임브리지 멜론 대학교의](https://ko.wikipedia.org/wiki/케임브리지_멜론_대학교 "wikilink") [C. 고든 벨의](https://ko.wikipedia.org/wiki/고든_벨 "wikilink") 박사 과정의 학생인 빌 스트레커(Bill Strecker)가 이 아키텍처를 맡았다.\[3\] 가격, 성능 수준, 용량이 각기 다른 수많은 모델들이 차후에 만들어졌다. VAX [슈퍼미니컴퓨터](https://ko.wikipedia.org/wiki/슈퍼미니컴퓨터 "wikilink")는 1980년대 초에 매우 인기를 끌었다.

## 프로세서 구조

[섬네일](https://ko.wikipedia.org/wiki/파일:Microvax_3600_\(2\).jpg "wikilink")

### 가상 메모리 맵

<table>
<tbody>
<tr class="odd">
<td style="text-align: center;"><p>DEC VAX 레지스터</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><table>
<tbody>
<tr class="odd">
<td><p><sup>3</sup><sub>1</sub></p></td>
<td><p>. . .</p></td>
<td><p><sup>2</sup><sub>3</sub></p></td>
<td><p>. . .</p></td>
<td><p><sup>1</sup><sub>5</sub></p></td>
<td><p><sup>1</sup><sub>4</sub></p></td>
<td><p><sup>1</sup><sub>3</sub></p></td>
<td><p><sup>1</sup><sub>2</sub></p></td>
<td><p><sup>1</sup><sub>1</sub></p></td>
<td><p><sup>1</sup><sub>0</sub></p></td>
<td><p><sup>0</sup><sub>9</sub></p></td>
<td><p><sup>0</sup><sub>8</sub></p></td>
<td><p><sup>0</sup><sub>7</sub></p></td>
<td><p><sup>0</sup><sub>6</sub></p></td>
<td><p><sup>0</sup><sub>5</sub></p></td>
<td><p><sup>0</sup><sub>4</sub></p></td>
<td><p><sup>0</sup><sub>3</sub></p></td>
<td><p><sup>0</sup><sub>2</sub></p></td>
<td><p><sup>0</sup><sub>1</sub></p></td>
<td><p><sup>0</sup><sub>0</sub></p></td>
<td><p><em>(bit position)</em></p></td>
</tr>
<tr class="even">
<td><p>General registers</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R0</p></td>
<td><p>Register 0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R1</p></td>
<td><p>Register 1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R2</p></td>
<td><p>Register 2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R3</p></td>
<td><p>Register 3</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R4</p></td>
<td><p>Register 4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R5</p></td>
<td><p>Register 5</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R6</p></td>
<td><p>Register 6</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R7</p></td>
<td><p>Register 7</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R8</p></td>
<td><p>Register 8</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R9</p></td>
<td><p>Register 9</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R10</p></td>
<td><p>Register 10</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R11</p></td>
<td><p>Register 11</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R12 / AP</p></td>
<td><p>Register 12 / Argument Pointer</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R13 / FP</p></td>
<td><p>Register 13 / Frame Pointer</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R14 / SP</p></td>
<td><p>Register 14 / Stack Pointer</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>R15 / PC</p></td>
<td><p>Register 15 / Program Counter</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Status flags</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ko.wikipedia.org/wiki/사인_플래그" title="wikilink">N</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/제로_플래그" title="wikilink">Z</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/오버플로_플래그" title="wikilink">V</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/캐리_플래그" title="wikilink">C</a></p></td>
<td><p>Condition Code Register</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

VAX 가상 메모리는 4개의 부분으로 나뉘는데, 크기는 각각 1 기가바이트(어드레싱 문맥에 따라 2<sup>30</sup> 바이트)이다:

| 구분 | 주소 범위                       |
| -- | --------------------------- |
| P0 | `0x00000000` - `0x3fffffff` |
| P1 | `0x40000000` - `0x7fffffff` |
| S0 | `0x80000000` - `0xbfffffff` |
| S1 | `0xc0000000` - `0xffffffff` |

VMS의 경우, 사용자 프로세스 공간을 위해 P0을, 프로세스 스택을 위해 P1을, 운영 체제를 위해 S0을 사용하였으며 S1은 예비로 남겨두었다.

### 권한 모드

VAX는 4개의 하드웨어 구현 권한 모드가 있다.

| 번호 | 모드    | VMS 사용  | 참고           |
| -- | ----- | ------- | ------------ |
| 0  | 커널    | OS 커널   | 최고 수준의 권한 단계 |
| 1  | 실행    | 파일 시스템  |              |
| 2  | 수퍼바이저 | 셸 (DCL) |              |
| 3  | 사용자   | 일반 프로그램 | 최저 수준의 권한 단계 |
|    |       |         |              |

### 프로세서 상태 레지스터

| CM | TP | MBZ | FD | IS | cmod | pmod | MBZ | IPL | MBZ | DV | FU | IV | T | N | Z | V | C |
| -- | -- | --- | -- | -- | ---- | ---- | --- | --- | --- | -- | -- | -- | - | - | - | - | - |
| 31 | 30 | 29  | 27 | 26 | 25   | 23   | 21  | 20  | 15  | 7  | 6  | 5  | 4 | 3 | 2 | 1 | 0 |

| 비트    | 의미                  |
| ----- | ------------------- |
| 31    | PDP-11 호환 모드        |
| 30    | 트레이스 보류             |
| 29:28 | MBZ (0이어야 함)        |
| 27    | 첫 부분 완료 (인터럽트 명령)   |
| 26    | 인터럽트 스택             |
| 25:24 | 현재의 권한 모드           |
| 23:22 | 이전 권한 모드            |
| 21    | MBZ (0이어야 함)        |
| 20:16 | IPL (인터럽트 우선 순위 수준) |
| 15:8  | MBZ (0이어야 함)        |
| 7     | 10진 오버플로 트랩 활성화     |
| 6     | 부동소수점 언더플로 트랩 활성화   |
| 5     | 정수 오버플로 트랩 활성화      |
| 4     | 트레이스                |
| 3     | 부정                  |
| 2     | 영(0)                |
| 1     | 오버플로                |
| 0     | 캐리                  |

## 각주

## 외부 링크

  - [HP: VAX Systems](https://web.archive.org/web/20041207213429/http://h18002.www1.hp.com/alphaserver/vax/)

  - [DEC Microprocessors](http://simh.trailing-edge.com/dsarchive.html)

  - [SimH VAX](http://simh.trailing-edge.com/) Open source emulator that supports VAX architecture

[분류:1997년 출시](https://ko.wikipedia.org/wiki/분류:1997년_출시 "wikilink") [분류:미니컴퓨터](https://ko.wikipedia.org/wiki/분류:미니컴퓨터 "wikilink") [분류:32비트 컴퓨터](https://ko.wikipedia.org/wiki/분류:32비트_컴퓨터 "wikilink")

1.
2.
3.