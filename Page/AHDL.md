> This article is converted from Wikipedia: [AHDL](https://ko.wikipedia.org/wiki/AHDL).


**알테라 하드웨어 기술 언어** ()는 [복합 프로그래머블 논리 소자](../Page/복합_프로그래머블_논리_소자.md "wikilink")(CPLD)와 [현장 프로그래머블 게이트 어레이](https://ko.wikipedia.org/wiki/현장_프로그래머블_게이트_어레이 "wikilink")(FPGA)를 프로그램 하기 위한 [알테라](https://ko.wikipedia.org/wiki/알테라 "wikilink") 사\[1\]의 자산 [하드웨어 기술 언어](https://ko.wikipedia.org/wiki/하드웨어_기술_언어 "wikilink") (HDL)이다.

알테라의 쿼터스 ()와 맥스+ ()의 컴파일러로 컴파일하며, 이 언어는 [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 같은 문법을 가지고 [VHDL](https://ko.wikipedia.org/wiki/VHDL "wikilink")처럼 비슷하게 동작한다.

## 예제

간단한 예시로 아래의 코드 조각은 8비트 업카운터를 수행한다.

    % a simple AHDL up counter, released to public domain 11/13/2006 %
    % [block quotations achieved with percent sign] %
    % like c, ahdl functions must be prototyped %

    % PROTOTYPE:
     FUNCTION COUNTER (CLK)
        RETURNS (CNTOUT[7..0]); %

    % function declaration, where inputs, outputs, and
    bidirectional pins are declared %
    % also like c, square brakets indicate an array %

    SUBDESIGN COUNTER
    (
        CLK     :INPUT;
        CNTOUT[7..0]    :OUTPUT;
    )

    % variables can be anything from flip-flops (as in this case),
    tri-state buffers, state machines, to user defined functions %

    VARIABLE
        TIMER[7..0]: DFF;

    % as with all hardware description languages, think of this
     less as an algorithm and more as wiring nodes together %

    BEGIN
        DEFAULTS

            TIMER[].prn = VCC; %  this takes care of d-ff resets %
            TIMER[].clrn = VCC;
        END DEFAULTS;

        TIMER[].d = TIMER[].q + H"1";
    END;

## 같이 보기

  - [쿼터스 II](https://ko.wikipedia.org/wiki/쿼터스_II "wikilink")

## 각주

<references />

[분류:하드웨어 기술 언어](https://ko.wikipedia.org/wiki/분류:하드웨어_기술_언어 "wikilink")

1.  <http://www.altera.com>