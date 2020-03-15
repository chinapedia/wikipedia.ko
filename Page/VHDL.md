> This article is converted from Wikipedia: [VHDL](https://ko.wikipedia.org/wiki/VHDL).


[섬네일를](https://ko.wikipedia.org/wiki/파일:Vhdl_signed_adder_source.svg "wikilink") 표현하는 VHDL 소스.\]\]

**VHDL**()은 [디지털 회로](../Page/디지털_회로.md "wikilink") 및 [혼합 신호](https://ko.wikipedia.org/wiki/혼합_신호 "wikilink")(mixed-signal, 아날로그 신호 포함)를 표현하는 [하드웨어 기술 언어이다](../Page/하드웨어_기술_언어.md "wikilink"). [FPGA](../Page/FPGA.md "wikilink")나 [집적회로](https://ko.wikipedia.org/wiki/집적회로 "wikilink") 등의 [전자공학](../Page/전자공학.md "wikilink") 회로를 처리하는 [설계 자동화에](../Page/컴퓨터_지원_설계.md "wikilink") 사용한다.

주로 디지털 회로 설계에 사용된다. 기존의 심볼에 의한 [회로도](../Page/회로도.md "wikilink") 작성 대신 언어적 형태로 전자회로의 기능을 표현한다. 아날로그 신호(mixed-signal)는 VHDL-AMS(VHDL Analog and Mixed-Signal Extensions)\[1\] 로 표현하나, 실제 활용면에서 디지털회로에 많이 적용되어 사용한다.

VHDL로 표현된 회로는, 실제 동작하는 기능적 소자로 변환하는 합성(synthesis) 과정을 거치면 동작할 수 있는 회로가 완성된다. 이때 FPGA나 ASIC 등을 위한 환경에 따라 합성된 실제회로의 소자가 달라지기 때문에 칩 설계 시 목적에 맞는 소자가 합성되도록 하는 개발도구가 존재한다. 예를 들어 FPGA를 판매하는 회사는 보통, 회로 입력(심볼 및 VHDL코드) 부터 시작해서 VHDL 코드의 합성, 모듈(소자)의 배치 등을 지원하는 도구를 지원한다.

## 역사

VHDL는 원래 [미국 국방부에서](../Page/미국_국방부.md "wikilink") [주문형 집적회로](https://ko.wikipedia.org/wiki/주문형_집적회로 "wikilink")(ASIC)의 문서화에 사용하기 위해 만든 언어였다. 즉, 복잡한 매뉴얼로 회로의 동작 내용을 설명하는 대신, 회로의 동작 내용을 문서화하여 설명하기 위해 개발했다. 그러나 이런 문서를 회로 디자인 과정에서 시뮬레이션에 사용하게 되었고, VHDL 파일을 읽어들여서 논리 합성을 한 다음 실제 회로 형태를 출력하는 기능을 덧붙이게 되었다. 오늘날에는 [디지털 회로의](../Page/디지털_회로.md "wikilink") 설계, 검증, 구현등의 모든 용도로 사용하고 있다.

VHDL은 [에이다](https://ko.wikipedia.org/wiki/에이다 "wikilink") 프로그래밍 언어의 부분집합에 디지털 회로에 필수적인 시간 개념을 추가하는 방식으로 만들어졌으나, [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") 표준화 작업을 거치면서 오늘날과 같은 형태와 문법을 가지게 되었다..

## 예제

VHDL을 이용한 간단한 [논리연산](https://ko.wikipedia.org/wiki/논리연산 "wikilink") 중 [AND](https://ko.wikipedia.org/wiki/AND "wikilink") 게이트는 다음과 같다.

``` VHDL
-- (this is a VHDL comment)

-- import std_logic from the IEEE library
library IEEE;
use IEEE.std_logic_1164.all;

-- this is the entity
entity ANDGATE is
  port (
    I1 : in std_logic;
    I2 : in std_logic;
    O  : out std_logic);
end entity ANDGATE;

-- this is the architecture
architecture RTL of ANDGATE is
begin
  O <= I1 and I2;
end architecture RTL;
```

### MUX 템플릿

[멀티플렉서](../Page/멀티플렉서.md "wikilink")(multiplexer, 또는 'MUX') 논리회로에서 다양하게 사용한다. 다음 MUX 예에서, 선택 입력 `S`에 의해 입력 `A`와 `B`를 선택적으로 출력 `X` 반영한다.

다음과 같이 MUX를 VHDL로 코딩할 수 있다:

``` VHDL
X <= A when S = '1' else B;
```

### 래치 템플릿

[트랜스페어런스 래치](https://ko.wikipedia.org/wiki/플립플럽#래치 "wikilink")(transparent latch) 메모리의 한 비트 정보를 저장 유지하는 회로로 게이트 신호에 *enable*에 의해 입력 D가 출력된다.

VHDL에서 D 래치는:

``` VHDL
-- latch template 1:
Q <= D when Enable = '1' else Q;

-- latch template 2:
process(D,Enable)
begin
  if Enable = '1' then
    Q <= D;
  end if;
end process;
```

### D 플립플럽

[D 플립플럽](https://ko.wikipedia.org/wiki/플립플럽#D_플립플럽 "wikilink") [클럭 신호](../Page/클럭_신호.md "wikilink") 상승 또는 하강 엣지에서 입력 D가 출력 Q에 반영된다.

다음 예는 비동기 RESET 신호와 함께 있는 플립플럽 예이다:

``` VHDL
DFF : process(RST, CLK)
begin
  if RST = '1' then
    Q <= '0';
  elsif rising_edge(CLK) then
    Q <= D;
  end if;
end process DFF;
```

VHDL의 다른 표현으로 엣지 트리거(edge-triggered)의 동작은 **event** 신호 특성으로 나타낼수 있다.

*event*을 사용한 엣지 표현 예:

``` VHDL
DFF : process(RST, CLK)
begin
  if RST = '1' then
    Q <= '0';
  elsif CLK'event and CLK = '1' then
    Q <= D;
  end if;
end process DFF;
```

### 카운터 예

비동기 *RESET*과 함께, 증감 카운터 예이다. 32비트 카운터로 'unsigned' 형이다. 이를 위해 'unsigned', 'std_logic_vector', VHDL *generics*을 사용하였다.

``` VHDL
library IEEE;
use IEEE.std_logic_1164.all;
use IEEE.numeric_std.all;    -- unsigned형를 위해

entity COUNTER is
  generic (
    WIDTH : in natural := 32);
  port (
    RST   : in std_logic;
    CLK   : in std_logic;
    LOAD  : in std_logic;
    Q     : out std_logic_vector(WIDTH-1 downto 0));
end entity COUNTER;

architecture RTL of COUNTER is
  signal CNT : unsigned(WIDTH-1 downto 0);
begin
  process(RST, CLK) is
  begin
    if RST = '1' then
      CNT <= (others => '0');
    elsif rising_edge(CLK) then
      if LOAD = '1' then
        CNT <= unsigned(DATA); -- unsigned형으로 변환
      else
        CNT <= CNT + 1;
      end if;
    end if;
  end process;

  Q <= std_logic_vector(CNT); -- type is converted back to std_logic_vector
end architecture RTL;
```

### 시뮬레이션을 위한 구조

VHDL 코드 중에 회로의 표현이 주이지만 다음의 경우는 하드웨어로 합성하지 않고 시뮬레이션을 위한 방법으로 사용한 예이다. 따라서 이 VHDL 코드는 하드웨어로 합성되지 않고(non-synthesizable) 다양한 용도로 사용할 수 있다.

예를 들어 다음 코드는 50 MHz [클럭 신호을](../Page/클럭_신호.md "wikilink") 표현하는 예이다. 이것은 실제 하드웨어 회로의 시뮬레이션 입력 신호로 사용하기 위해, 시뮬레이션에서만 클럭이 생성되는 코드이다. 실제로 클럭을 생성하지 않고 시뮬레이션 상에서만 신호가 생성되기 때문에 실제 하드웨어에서 동작하려면 클럭신호를 별도로 만들어 주어야 한다.

``` VHDL
process
begin
  CLK <= '1'; wait for 10 NS;
  CLK <= '0'; wait for 10 NS;
end process;
```

클럭 뿐만 아니라, 시뮬레이션을 위해 다음과 같은 여러가지 신호를 만들어 VHDL 코드 모듈에 입력으로 사용할 수 있다.

``` VHDL
process
begin
  wait until START = '1'; -- START=H가 될 때까지 기다린다.

  for i in 1 to 10 loop -- 몇 개의 클럭 주기동안 기다리고...
    wait until rising_edge(CLK);
  end loop;

  for i in 1 to 10 loop     -- 1부터 10까지 DATA에 넣기, 1 매 주기마다
    DATA <= to_unsigned(i, 8);
    wait until rising_edge(CLK);
  end loop;

  -- 출력이 변할 때 까지 기다림.
  wait on RESULT;

  -- 한 클럭 주기 동안 ACK 펄스를 만든다.
  ACK <= '1';
  wait until rising_edge(CLK);
  ACK <= '0';

  -- 계속...
end process;
```

## 각주

<references/>

## 같이 보기

  - [하드웨어 기술 언어](../Page/하드웨어_기술_언어.md "wikilink")
  - [ABEL](https://ko.wikipedia.org/wiki/아벨_프로그래밍_언어 "wikilink") ("Advanced Boolean Expression Language")
  - [AHDL](../Page/AHDL.md "wikilink") (알테라 HDL, [Altera가](../Page/알테라.md "wikilink") 만든 상용 언어)
  - [PALASM](https://ko.wikipedia.org/wiki/PALASM "wikilink")
  - [Verilog](https://ko.wikipedia.org/wiki/Verilog "wikilink") ([IEEE 1364](https://ko.wikipedia.org/wiki/IEEE_1364 "wikilink"))
  - [GHDL](https://ko.wikipedia.org/wiki/GHDL "wikilink") - VHDL [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink") 시뮬레이터

## 외부 링크

  - [VHDL 예제들](http://esd.cs.ucr.edu/labs/tutorial/)
  - [VHDL 강좌](http://www.asic-world.com/vhdl/tutorial.html)

[분류:하드웨어 기술 언어](https://ko.wikipedia.org/wiki/분류:하드웨어_기술_언어 "wikilink") [분류:디지털 전자공학](https://ko.wikipedia.org/wiki/분류:디지털_전자공학 "wikilink") [분류:전자공학](https://ko.wikipedia.org/wiki/분류:전자공학 "wikilink")

1.