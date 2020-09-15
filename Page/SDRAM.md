> This article is converted from Wikipedia: [SDRAM](https://ko.wikipedia.org/wiki/SDRAM).


**SDRAM**(**S**ynchronous **D**ynamic **R**andom **A**ccess **M**emory, 에스디 램)은 [DRAM](https://ko.wikipedia.org/wiki/DRAM "wikilink")의 발전된 형태이다. 보통 DRAM 과는 달리 제어 장치 입력을 클록펄스(Clock Pulse)와 동시에 일어나도록 하는 **동기식 DRAM**이다.

[DDR SDRAM의](../Page/DDR_SDRAM.md "wikilink") 보급으로 SDR SDRAM이라는 관례적인 명칭이 주어졌다. SDR은 **S**ingle **D**ata **R**ate 의 약자이다. 이 의미는 기존의 SDRAM 이 각 클록펄스가 상승 또는 하강하는 시점에서 한번만 정보를 전송하는 것에서 나온 명칭이다.

## SDR SDRAM

### SDRAM 제어 신호

  - CKE(Clock Enable). Low 신호가 들어오면, 칩은 클럭이 멈춘 것처럼 동작한다.
  - /CS(Chip Select). High 신호가 들어오면, 칩은 다른 모든 입력(CKE 제외)을 무시하며 NOP 명령을 수신한 것처럼 동작한다.
  - DQM(Data Mask). High 신호가 들어오면, 이러한 신호들은 데이터 입출력을 억제한다.

### 명령 신호

  - /RAS (Row Address Strobe): 이름과 달리 실제로는 스트로브(strobe)가 아닌 단순한 명령 비트이다. /CAS, /WE와 더불어 8개 명령 중 하나를 선택한다.
  - /CAS (Column Address Strobe): 이름과 달리 실제로는 스트로브가 아닌 단순한 명령 비트이다. /RAS, /WE와 더불어 8개 명령 중 하나를 선택한다.
  - /WE (Write enable): /RAS, /CAS와 더불어 8개 명령 중 하나를 선택한다.

### 뱅크 셀렉션 (BAn)

SDRAM 장치는 내부적으로 2개나 4개 또는 8개의 독립된 내부 데이터 뱅크로 나뉜다.

### 어드레싱 (A10/An)

수많은 명령들은 주소 입력 핀에 존재하는 주소를 사용한다. 주소를 사용하지 않거나 컬럼 주소가 존재하는 일부 명령들도 A10을 사용하여 종류를 선택한다.

### 명령

| /CS | /RAS | /CAS | /WE | BA*n* | A10  | A*n*   |
| --- | ---- | ---- | --- | ----- | ---- | ------ |
| H   | x    | x    | x   | x     | x    | x      |
| L   | H    | H    | H   | x     | x    | x      |
| L   | H    | H    | L   | x     | x    | x      |
| L   | H    | L    | H   | bank  | L    | column |
| L   | H    | L    | H   | bank  | H    | column |
| L   | H    | L    | L   | bank  | L    | column |
| L   | H    | L    | L   | bank  | H    | column |
| L   | L    | H    | H   | bank  | row  |        |
| L   | L    | H    | L   | bank  | L    | x      |
| L   | L    | H    | L   | x     | H    | x      |
| L   | L    | L    | H   | x     | x    | x      |
| L   | L    | L    | L   | 0 0   | mode |        |

## SDRAM의 세대

### SDR SDRAM

[섬네일의](https://ko.wikipedia.org/wiki/파일:Micron_48LC32M8A2-AB.jpg "wikilink") 64 메가바이트 사운드 메모리는 [마이크론](../Page/마이크론_테크놀로지.md "wikilink") 48LC32M8A2-75 C SDRAM 칩을 사용하며 133MHz/7.5 나노초 8 비트의 너비로 동작한다 \[1\]\]\] **싱글 데이터 레이트 SDRAM**(**SDR SDRAM**, **S**ingle **D**ata **R**ate **SDRAM**)은 클럭 사이클 한 개 당 한 개의 커맨드(command)를 받거나 한 워드(word) 만큼의 데이터(data)를 주고받을 수 있는 SDRAM을 말한다. 전형적인 클럭 주파수는 100 및 133 MHz였다. 데이터 버스 사이즈는 4 비트, 8 비트, 16 비트 등으로 다양하였는데, 단 일반적으로 SDR SDRAM 칩들은 64 (non-ECC) 혹은 72 ([ECC](https://ko.wikipedia.org/wiki/오류_정정_부호 "wikilink")) 비트를 한 번에 읽을 수 있는 168 핀 [DIMM](../Page/DIMM.md "wikilink") 형태로 조립되었다.

### DDR SDRAM

### DDR2 SDRAM

### DDR3 SDRAM

### DDR4 SDRAM

## 각주

[SDRAM](https://ko.wikipedia.org/wiki/분류:SDRAM "wikilink") [분류:대한민국의 발명품](https://ko.wikipedia.org/wiki/분류:대한민국의_발명품 "wikilink")

1.