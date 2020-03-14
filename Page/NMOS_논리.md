> This article is converted from Wikipedia: [NMOS ](https://ko.wikipedia.org/wiki/NMOS_).


**N형 금속산화물 반도체 논리**는 [논리 회로와](https://ko.wikipedia.org/wiki/논리_회로 "wikilink") 다른 디지털 회로를 실행하기 위해 n형 [MOSFET](https://ko.wikipedia.org/wiki/MOSFET "wikilink")을 이용한다. NMOS트랜지스터는 차단상태, 선형상태, 포화상태, 속도 포화 상태의 4가지 동작 상태가 있다. N형 [MOSFET](https://ko.wikipedia.org/wiki/MOSFET "wikilink")은 PDN이라고 불리는 배열로 배치되는데, PDN은 논리 게이트 출력과 음 전압원 사이에 N형 [MOSFET](https://ko.wikipedia.org/wiki/MOSFET "wikilink")이 놓이고, 논리게이트 출력과 양 전압원 사이에 저항이 놓이는 배열이다. 회로는 만약 출력값이 낮으면 PDN이 활성화되어 음 전압원과 출력사이에 전류가 흐르도록 하기 위해 설계되었다.

[right](https://ko.wikipedia.org/wiki/파일:NMOS_NOR_WITH_RESISTIVE_LOAD.PNG "wikilink")

예를 들어, NMOS 논리에 NOR게이트가 있다고 치자. 만약 입력A나 입력B가 높으면(논리1=참), 각각의 MOS트랜지스터는 출력과 음전압원 사이에서 매우 약한 저항으로 작용함으로써 출력갑을 낮게 한다(논리0=거짓). 만약 A와 B가 모두 높으면, 두 개의 트랜지스터는 도체가 되고, 훨씬 더 낮은 저항경로를 만든다. 출력값이 높게 나올 때는 두 개의 트랜지스터가 모두 OFF상태일 때뿐인데, 이때는 입력A와 입력B가 모두 낮아서 NOR게이트의 참값조건을 만족시킬 때이다.

| A | B | A NOR B |
| - | - | ------- |
| 0 | 0 | 1       |
| 0 | 1 | 0       |
| 1 | 0 | 0       |
| 1 | 1 | 0       |

[MOSFET](https://ko.wikipedia.org/wiki/MOSFET "wikilink")은 저항으로 작동할 수 있기 때문에, 전체 회로를 N형 [MOSFET](https://ko.wikipedia.org/wiki/MOSFET "wikilink")만으로 구성할 수 도 있다. 따라서 수년간, NMOS 회로는 훨씬 더 느린 P형 트랜지스터를 써야하는 PMOS나 [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink")회로보다 훨씬 더 빨랐다. 또한 CMOS는 P기판 위에 N-웰을 얹어 P형 트랜지스터를 작동시켜야하기 때문에, NMOS를 제조하기가 훨씬 더 쉬웠다. NMOS의 주요한 문제는 출력이 NMOS의 경우엔 낮음값인 정상상태에서도 직류전류가 흘러야한다는 점이었다. 이것은 정적 전력 소실을 의미하는 것으로, 즉 회로가 작동하고 있지 않을 때도, 전력이 손실된다. 이것은 상당한 정적 전류 손실이 일어난다는 점에서 현대의 고속력, 고밀도의 [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink")회로에서 일어나는 현상과 비슷하지만, [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink")회로에서 일어나는 것은 누설 때문으로, [바이어스](https://ko.wikipedia.org/wiki/바이어스 "wikilink") 때문은 아니다. 하지만, ASIC나 [SRAM](https://ko.wikipedia.org/wiki/SRAM "wikilink") 등에 사용되는, 오래되거나 속도가 느린 정적 [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink") 회로는 대부분 매우 낮은 정적 전력 소모를 가진다. 또한, NMOS회로는 낮음에서 높음값으로 전환되는 것이 느리다. 높음에서 낮음으로 전환할 때, 트랜지스터는 낮은 저항값을 가지고, 출력에 있는 용량성 전하는 빠르게 빠져나간다(축전기를 매우 낮은 저항값을 갖는 저항기로 방전시키는 것과 비슷한 원리이다). 하지만 출력과 양 전원 레일사이의 저항은 훨씬 더 크기 때문에 낮음에서 높음 값으로 전환하는 것은 시간이 더 오래 걸린다(높은 저항값을 갖는 저항기로 축전기를 충전하는 것과 비슷한 원리이다). 낮은 저항값을 갖는 저항을 사용하는 것은 과정을 더 빠르게 해주겠지만 정적 전력손실을 증가시킬 것이다. 하지만 게이트를 빠르게 만드는 가장 흔하면서 더 나은 방법은 로드로 증가형 트랜지스터 대신 공핍형 트랜지스터를 쓰는 것이다. 사실 DTL, TTL, ECL같은 비대칭 입력 논리 레벨은 NMOS 회로를 소음에 약간 민감하게 만든다. 이런 단점은 왜 마이크로프로세서 같은 대부분의 고속의 디지털회로에 [CMOS](https://ko.wikipedia.org/wiki/CMOS "wikilink")논리가 대신하게 되었는지 말해준다.

[분류:집적 회로](https://ko.wikipedia.org/wiki/분류:집적_회로 "wikilink")