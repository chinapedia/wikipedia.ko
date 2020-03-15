> This article is converted from Wikipedia: [SIMM](https://ko.wikipedia.org/wiki/SIMM).


[섬네일](https://ko.wikipedia.org/wiki/파일:Atari_STE_256kB_RAM_2.jpg "wikilink") **SIMM**(single in-line memory module, 싱글 인라인 메모리 모듈)은 [개인용 컴퓨터의](https://ko.wikipedia.org/wiki/개인용_컴퓨터 "wikilink") [램](https://ko.wikipedia.org/wiki/램 "wikilink") [메모리 모듈의](https://ko.wikipedia.org/wiki/메모리_모듈 "wikilink") 일종으로 현재 주류인 [DIMM](../Page/DIMM.md "wikilink")과는 다르다.

초기의 PC [메인보드](https://ko.wikipedia.org/wiki/메인보드 "wikilink")([XT와](https://ko.wikipedia.org/wiki/IBM_XT "wikilink") 같은 [8088](https://ko.wikipedia.org/wiki/8088 "wikilink") PC들)에서는 [DIP](https://ko.wikipedia.org/wiki/DIP "wikilink") 소켓에 칩을 끼워 사용하였다. [80286](https://ko.wikipedia.org/wiki/80286 "wikilink")의 PC/[AT에는](https://ko.wikipedia.org/wiki/IBM_AT "wikilink") 기억량이 대폭 늘어나고 메인보드의 공간을 절약하거나 간단히 메모리를 증설할 수 있도록 메모리 모듈이 쓰이게 되었다. 메모리를 늘리기 위해서 8-9개의 DRAM 칩을 끼우던 것이 메모리 모듈 1개를 추가하는 것으로 끝나게 되었다. 80286 컴퓨터에서는 비표준의 [SIPP](https://ko.wikipedia.org/wiki/SIPP "wikilink")(single in-line pin package)을 사용하는 것도 있었지만 장착할 때 핀이 꺾이거나 부러지는 일이 많았기 때문에 핀 대신 접점 방식을 이용하는 SIMM이 급속히 보급되었다.

SIMM은 1983년 WANG Laboratories의 연구원인 제임스 클레이튼이 고안했으며 1980년대 중반 [IBM PS/2에](https://ko.wikipedia.org/wiki/IBM_PS/2 "wikilink") 도입되어 메인보드의 소형화나 높은 용량의 메모리 장착, 여러 메모리 칩들과의 호환성 문제 등을 해결해 주었다. 초기의 SIMM은 30핀 8비트 데이터([패리티](https://ko.wikipedia.org/wiki/패리티 "wikilink")의 경우 9비트)로 286과 [386](https://ko.wikipedia.org/wiki/386 "wikilink"), [486](https://ko.wikipedia.org/wiki/486 "wikilink") 시스템에 사용되었으며 90년대 중반 이후 72핀 32비트 데이터(패리티의 경우 36비트)로 교체되어 486, [펜티엄](https://ko.wikipedia.org/wiki/펜티엄 "wikilink"), [펜티엄 프로와](https://ko.wikipedia.org/wiki/펜티엄_프로 "wikilink") 일부 [펜티엄 II](https://ko.wikipedia.org/wiki/펜티엄_II "wikilink") 시스템에도 사용되었다.

[매킨토시](https://ko.wikipedia.org/wiki/매킨토시 "wikilink") IIfx에서는 비표준의 64핀 SIMM이 사용되었다.

메모리 모듈과 프로세서에서 데이터 버스 폭이 다를 경우에는 2개이나 4개의 모듈로 [메모리 뱅크를](https://ko.wikipedia.org/wiki/메모리_뱅크 "wikilink") 채워야 한다. 이를테면, 데이터 버스가 16 비트인 286과 [386SX](https://ko.wikipedia.org/wiki/386SX "wikilink")의 경우 메모리 뱅크당 2개의 SIMM, 32 비트의 [386DX](https://ko.wikipedia.org/wiki/386DX "wikilink")과 486은 뱅크당 30핀 SIMM 4개나 72핀 SIMM 을 1개, 64 비트 펜티엄은 72핀 SIMM 2개가 필요하다.

초기의 SIMM 소켓은 기존의 푸쉬 타입의 소켓이었지만 곧 끼우고 회전시켜서 고정하는 [ZIF](https://ko.wikipedia.org/wiki/ZIF "wikilink")(Zero insertion force) 소켓이 사용되었다. 보통 SIMM을 달 경우 비스듬하게 소켓에 넣고, 일정 위치(보통 90도)까지 세워서 고정시킨다. 분리할 경우엔 양다리에 있는 금속이나 플라스틱 클립을 벌려서 잠금상태를 풀고 SIMM을 기울인 다음 뽑는다. 초기의 소켓에서는 플라스틱 클립이 사용되고 있었지만 부러지기 쉬웠기 때문에 금속제로 바뀌었다.

SIMM 에 장착된 [DRAM](https://ko.wikipedia.org/wiki/DRAM "wikilink")으로는 [EDO](https://ko.wikipedia.org/wiki/EDO "wikilink")(Extended Data Out)이나 [FPM](https://ko.wikipedia.org/wiki/FPM "wikilink")(Fast Page Mode)이 사용되고 있었으며 [JEDEC](https://ko.wikipedia.org/wiki/JEDEC "wikilink") JESD-21C로 표준화되어 있다.

## 일반적인 메모리 크기

  - 30핀 SIMM - 256KB, 1MB, 4MB, 16MB
  - 72핀 SIMM - 1MB, 2MB, 4MB, 8MB, 16MB, 32MB, 64MB, 128MB, 256MB

## 핀 배열

| Pin \# | 이름             | 신호 설명                  |
| ------ | -------------- | ---------------------- |
| 1      | V<sub>CC</sub> | \+5VDC                 |
| 2      | CAS            | Column Address Strobe  |
| 3      | DQ1            | Data 0                 |
| 4      | A0             | Address 0              |
| 5      | A1             | Address 1              |
| 6      | DQ2            | Data 1                 |
| 7      | A2             | Address 2              |
| 8      | A3             | Address 3              |
| 9      | V<sub>SS</sub> | Ground                 |
| 10     | DQ3            | Data 2                 |
| 11     | A4             | Address 4              |
| 12     | A5             | Address 5              |
| 13     | DQ4            | Data 3                 |
| 14     | A6             | Address 6              |
| 15     | A7             | Address 7              |
| 16     | DQ5            | Data 4                 |
| 17     | A8             | Address 8              |
| 18     | A9             | Address 9              |
| 19     | A10            | Address 10             |
| 20     | DQ6            | Data 5                 |
| 21     | W              | Write Enable           |
| 22     | V<sub>SS</sub> | Ground                 |
| 23     | DQ7            | Data 6                 |
| 24     | NC             | No Internal Connection |
| 25     | DQ8            | Data 7                 |
| 26     | NC             | No Internal Connection |
| 27     | RAS            | Row Address Strobe     |
| 28     | NC             | No Internal Connection |
| 29     | NC             | No Internal Connection |
| 30     | V<sub>CC</sub> | \+5VDC                 |

30-pin SIMM 메모리 모듈

| Pin \# | 패리티 없음         | 패리티            | 신호 설명                   |
| ------ | -------------- | -------------- | ----------------------- |
| 1      | V<sub>SS</sub> | V<sub>SS</sub> | Ground                  |
| 2      | DQ0            | DQ0            | Data 0                  |
| 3      | DQ1            | DQ1            | Data 1                  |
| 4      | DQ2            | DQ2            | Data 2                  |
| 5      | DQ3            | DQ3            | Data 3                  |
| 6      | DQ4            | DQ4            | Data 4                  |
| 7      | DQ5            | DQ5            | Data 5                  |
| 8      | DQ6            | DQ6            | Data 6                  |
| 9      | DQ7            | DQ7            | Data 7                  |
| 10     | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                 |
| 11     | PD1            | PD1            | Presence Detect 1       |
| 12     | A0             | A0             | Address 0               |
| 13     | A1             | A1             | Address 1               |
| 14     | A2             | A2             | Address 2               |
| 15     | A3             | A3             | Address 3               |
| 16     | A4             | A4             | Address 4               |
| 17     | A5             | A5             | Address 5               |
| 18     | A6             | A6             | Address 6               |
| 19     | A10            | A10            | Address 10              |
| 20     | n/c            | PQ8            | Data 8 (Parity 1)       |
| 21     | DQ9            | DQ9            | Data 9                  |
| 22     | DQ10           | DQ10           | Data 10                 |
| 23     | DQ11           | DQ11           | Data 11                 |
| 24     | DQ12           | DQ12           | Data 12                 |
| 25     | DQ13           | DQ13           | Data 13                 |
| 26     | DQ14           | DQ14           | Data 14                 |
| 27     | DQ15           | DQ15           | Data 15                 |
| 28     | A7             | A7             | Address 7               |
| 29     | A11            | A11            | Address 11              |
| 30     | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                 |
| 31     | A8             | A8             | Address 8               |
| 32     | A9             | A9             | Address 9               |
| 33     | /RAS3          | RAS3           | Row Address Strobe 3    |
| 34     | /RAS2          | RAS2           | Row Address Strobe 2    |
| 35     | DQ16           | DQ16           | Data 16                 |
| 36     | n/c            | PQ17           | Data 17 (Parity 2)      |
| 37     | DQ18           | DQ18           | Data 18                 |
| 38     | DQ19           | DQ19           | Data 19                 |
| 39     | V<sub>SS</sub> | V<sub>SS</sub> | Ground                  |
| 40     | /CAS0          | CAS0           | Column Address Strobe 0 |
| 41     | /CAS2          | CAS2           | Column Address Strobe 2 |
| 42     | /CAS3          | CAS3           | Column Address Strobe 3 |
| 43     | /CAS1          | CAS1           | Column Address Strobe 1 |
| 44     | /RAS0          | RAS0           | Row Address Strobe 0    |
| 45     | /RAS1          | RAS1           | Row Address Strobe 1    |
| 46     | A12            | A12            | Address 12              |
| 47     | /WE            | WE             | Read/Write              |
| 48     | A13            | A13            | Address 13              |
| 49     | DQ20           | DQ20           | Data 20                 |
| 50     | DQ21           | DQ21           | Data 21                 |
| 51     | DQ22           | DQ22           | Data 22                 |
| 52     | DQ23           | DQ23           | Data 23                 |
| 53     | DQ24           | DQ24           | Data 24                 |
| 54     | DQ25           | DQ25           | Data 25                 |
| 55     | n/c            | PQ26           | Data 26 (Parity 3)      |
| 56     | DQ27           | DQ27           | Data 27                 |
| 57     | DQ28           | DQ28           | Data 28                 |
| 58     | DQ29           | DQ29           | Data 29                 |
| 59     | DQ31           | DQ31           | Data 31                 |
| 60     | DQ30           | DQ30           | Data 30                 |
| 61     | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                 |
| 62     | DQ32           | DQ32           | Data 32                 |
| 63     | DQ33           | DQ33           | Data 33                 |
| 64     | DQ34           | DQ34           | Data 34                 |
| 65     | n/c            | PQ35           | Data 35 (Parity 4)      |
| 66     | PD2            | PD2            | Presence Detect 2       |
| 67     | PD3            | PD3            | Presence Detect 3       |
| 68     | PD4            | PD4            | Presence Detect 4       |
| 69     | PD5            | PD5            | Presence Detect 5       |
| 70     | PD6            | PD6            | Presence Detect 6       |
| 71     | PD7            | PD7            | Presence Detect 7       |
| 72     | V<sub>SS</sub> | V<sub>SS</sub> | Ground                  |

72 핀 ECC SIMM 메모리 모듈

## 관련 항목

  - [DIP](https://ko.wikipedia.org/wiki/DIP "wikilink")
  - [SIP](https://ko.wikipedia.org/wiki/SIP "wikilink")
  - [ZIP](https://ko.wikipedia.org/wiki/ZIP "wikilink")
  - [DIMM](../Page/DIMM.md "wikilink")

## 외부 링크

  - [SIMM 설치 가이드](https://web.archive.org/web/20120716225721/http://www.edgetechcorp.com/support/installation-manuals/1000%20General%20SIMM%20Ver2\(09-04\).pdf)

[분류:컴퓨터 메모리](https://ko.wikipedia.org/wiki/분류:컴퓨터_메모리 "wikilink")