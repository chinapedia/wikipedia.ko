> This article is converted from Wikipedia: [FB-DIMM](https://ko.wikipedia.org/wiki/FB-DIMM).


[right](https://ko.wikipedia.org/wiki/파일:FB-DIMM.JPG "wikilink") **FB-DIMM**(Fully Buffered DIMM)은 메모리 시스템의 신뢰성과 밀집도를 개선하는데 사용될 수 있는 메모리 기술의 하나이다. 전통적으로 [메모리 컨트롤러가의](../Page/메모리_컨트롤러.md "wikilink") 데이터 라인들은 모든 [DRAM](https://ko.wikipedia.org/wiki/DRAM "wikilink") 모듈의 데이터 라인에 연결되어야 한다. (예: [멀티드롭 버스](https://ko.wikipedia.org/wiki/멀티드롭_버스 "wikilink")) 메모리 폭이 접근 속도와 더불어 늘어날수록 버스와 장치 간 인터페이스의 신호는 감소한다. 이 경우 속도와 메모리 밀집도를 제한하므로 FB-[DIMM](../Page/DIMM.md "wikilink")은 다른 접근을 취하여 이 문제를 해결한다.

240핀 DDR2 FB-DIMM은 전통적인 240핀 DDR2 DIMM과는 다르게 등급이 더 높다. 그 결과 이 두 개의 DIMM 타입은 기계적으로나 전기적으로 서로 호환성이 없다.

거의 모든 RAM 사양에서처럼 FB-DIMM 사양은 [JEDEC](https://ko.wikipedia.org/wiki/JEDEC "wikilink")에 의해 출판되었다.

## 기술

FB-DIMM 구조는 메모리 컨트롤러와 메모리 모듈 사이의 고급 메모리 버퍼(advanced memory buffer, AMB)를 도입하였다. 전통적인 DRAM의 [병렬](https://ko.wikipedia.org/wiki/병렬_통신 "wikilink") 버스 구조와 달리 FB-DIMM은 메모리 컨트롤러와 AMB 사이에 [직렬 인터페이스가](../Page/직렬_통신.md "wikilink") 있다. 이렇게 하면 실현가능한 수준 이상으로 메모리 컨트롤러의 핀 수를 늘리지 않더라도 메모리 대역을 증가시킬 수 있다. 이 구조를 통해 메모리 컨트롤러는 메모리 모듈에 직접 기록하지 않는다. 이 작업은 AMB에서 처리한다. 그러므로 AMB는 신호 버퍼링 및 재전송을 통해 신호 약화를 보완할 수 있게 된다.

## 프로토콜

JEDEC 표준 [JESD206](http://www.jedec.org/standards-documents/results/JESD206)은 이 프로토콜을 정의하며 JESD82-20은 DDR2 메모리에 대한 AMB 인터페이스를 정의한다. 이 프로토콜은 다른 수많은 영역에 일반적으로 기술되어 있다.\[1\]\[2\]\[3\]\[4\]\[5\]

## 각주

## 외부 링크

  - [How FB-DIMM Memories Work](https://web.archive.org/web/20060304232206/http://www.hardwaresecrets.com/article/266)

  - [디 인콰이어러](https://ko.wikipedia.org/wiki/디_인콰이어러 "wikilink") 시리즈: [Part 1](http://www.theinquirer.net/?article=15167) [Part 2](http://www.theinquirer.net/?article=15189) [Part 3](http://www.theinquirer.net/?article=15214)

[분류:컴퓨터 메모리](https://ko.wikipedia.org/wiki/분류:컴퓨터_메모리 "wikilink")

1.
2.
3.
4.
5.