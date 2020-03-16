> This article is converted from Wikipedia: [MD5](https://ko.wikipedia.org/wiki/MD5).


**MD5**()는 128비트 [암호화 해시 함수이다](../Page/암호화_해시_함수.md "wikilink"). [RFC](../Page/RFC.md "wikilink") 1321로 지정되어 있으며, 주로 프로그램이나 파일이 원본 그대로인지를 확인하는 무결성 검사 등에 사용된다. [1991년](../Page/1991년.md "wikilink")에 [로널드 라이베스트가](../Page/로널드_라이베스트.md "wikilink") 예전에 쓰이던 [MD4](../Page/MD4.md "wikilink")를 대체하기 위해 고안했다.

[1996년](../Page/1996년.md "wikilink")에 MD5의 설계상 결함이 발견되었다. 이것은 매우 치명적인 결함은 아니었지만, 암호학자들은 해시 용도로 [SHA](../Page/SHA.md "wikilink")-1과 같이 다른 안전한 알고리즘을 사용할 것을 권장하기 시작했다. [2004년](../Page/2004년.md "wikilink")에는 더욱 심한 암호화 결함\[[http://eprint.iacr.org/2005/067\]이](http://eprint.iacr.org/2005/067%5D이) 발견되었고. [2006년](../Page/2006년.md "wikilink")에는 노트북 컴퓨터 한 대의 계산 능력으로 1분 내에 해시 충돌을 찾을 정도로 빠른 알고리즘이 발표\[[http://eprint.iacr.org/2006/105\]되기도](http://eprint.iacr.org/2006/105%5D되기도) 하였다. 현재는 MD5 알고리즘을 보안 관련 용도로 쓰는 것은 권장하지 않으며, 심각한 보안 문제를 야기할 수도 있다. 2008년 12월에는 MD5의 결함을 이용해 [SSL](https://ko.wikipedia.org/wiki/SSL "wikilink") 인증서를 변조하는 것이 가능하다는 것이 발표되었다\[1\].

## 알고리즘

\[\[파일:MD5 algorithm.svg|right|thumbnail|300px|단일 MD5 연산. MD5에서는 이 단일 연산을 64번 실행한다. 16개의 연산을 그룹화한 4 라운드로 묶인다. F는 각 라운드에서 사용하는 비선형 함수를 가리키며, 각 라운드에서는 각각 다른 함수를 사용한다. M<sub>i</sub>는 입력 메시지의 32-비트 블록을 의미한다.

[left shift](https://ko.wikipedia.org/wiki/파일:lll.png "wikilink")<sub>*s*</sub>는 s칸 만큼의 레프트 로테이션을 가리키며, s는 각 연산 후 값이 변한다. [Addition](https://ko.wikipedia.org/wiki/파일:Boxplus.png "wikilink") 은 모듈로 2<sup>32</sup> 덧셈을 말한다.

\]\]

MD5는 임의의 길이의 메시지(variable-length message)를 입력받아, 128비트짜리 고정 길이의 출력값을 낸다. 입력 메시지는 512 비트 블록들로 쪼개진다; 메시지를 우선 [패딩하여](https://ko.wikipedia.org/wiki/패딩_\(암호학\) "wikilink") 512로 나누어떨어질 수 있는 길이가 되게 한다. 패딩은 다음과 같이 한다: 우선 첫 단일 비트, 1을 메시지 끝부분에 추가한다. 512의 배수의 길이보다 64 비트가 적은 곳까지 0으로 채운다. 나머지 64 비트는 최초의(오리지널) 메시지의 길이를 나타내는 64 비트 정수(integer)값으로 채워진다.

메인 MD5 알고리즘은 A,B,C,D라고 이름이 붙은 32 비트 워드 네 개로 이루어진 하나의 128 비트 스테이트(state)에 대해 동작한다. A,B,C,D는 소정의 상수값으로 초기화된다. 메인 MD5 알고리즘은 각각의 512 비트짜리 입력 메시지 블록에 대해 차례로 동작한다. 각 512 비트 입력 메시지 블록을 처리하고 나면 128 비트 스테이트(state)의 값이 변하게 된다.

하나의 메시지 블록을 처리하는 것은 4 단계로 나뉜다. 한 단계를 "라운드"(round)라고 부른다; 각 라운드는 비선형 함수 F, [모듈라 덧셈](https://ko.wikipedia.org/wiki/모듈라_덧셈 "wikilink"), 레프트 로테이션(left rotation)에 기반한 16개의 동일 연산(similar operations)으로 이루어져 있다. 오른쪽 그림은 한 라운드에서 이루어지는 한 연산(operation)을 묘사하고 있다.

함수 F에는 4가지가 있다; 각 라운드마다 각각 다른 F가 쓰인다:

\[F(X,Y,Z) = (X\wedge{Y}) \vee (\neg{X} \wedge{Z})\]

\[G(X,Y,Z) = (X\wedge{Z}) \vee (Y \wedge \neg{Z})\]

\[H(X,Y,Z) = X \oplus Y \oplus Z\]

\[I(X,Y,Z) = Y \oplus (X \vee \neg{Z})\]

\(\oplus, \wedge, \vee, \neg\)는 각각 [XOR](https://ko.wikipedia.org/wiki/XOR "wikilink"), [논리곱](https://ko.wikipedia.org/wiki/논리곱 "wikilink"), [논리합](https://ko.wikipedia.org/wiki/논리합 "wikilink") 그리고 [NOT](https://ko.wikipedia.org/wiki/논리부정 "wikilink") 연산을 의미한다.

### 의사코드

MD5 알고리즘의 [의사코드](../Page/의사코드.md "wikilink")는 다음과 같다:

<span style="color:green;">`//`*`Note:``   ``All``   ``variables``   ``are``   ``unsigned``   ``32``   ``bits``   ``and``   ``wrap``   ``modulo``   ``2^32``   ``when``   ``calculating`*</span>
**`var`**` `*`int`*`[64] r, k`

<span style="color:green;">`//`*`r``   ``specifies``   ``the``   ``per-round``   ``shift``   ``amounts`*</span>
`r[ 0..15] := {7, 12, 17, 22,  7, 12, 17, 22,  7, 12, 17, 22,  7, 12, 17, 22}`
`r[16..31] := {5,  9, 14, 20,  5,  9, 14, 20,  5,  9, 14, 20,  5,  9, 14, 20}`
`r[32..47] := {4, 11, 16, 23,  4, 11, 16, 23,  4, 11, 16, 23,  4, 11, 16, 23}`
`r[48..63] := {6, 10, 15, 21,  6, 10, 15, 21,  6, 10, 15, 21,  6, 10, 15, 21}`

<span style="color:green;">`//`*`Use``   ``binary``   ``integer``   ``part``   ``of``   ``the``   ``sines``   ``of``   ``integers``   ``as``   ``constants:`*</span>
**`for`**` i `**`from`**` 0 `**`to`**` 63`
`    k[i] := floor(abs(sin(i + 1)) × (2 `**`pow`**` 32))`

<span style="color:green;">`//`*`Initialize``   ``variables:`*</span>
**`var`**` `*`int`*` h0 := 0x67452301`
**`var`**` `*`int`*` h1 := 0xEFCDAB89`
**`var`**` `*`int`*` h2 := 0x98BADCFE`
**`var`**` `*`int`*` h3 := 0x10325476`

<span style="color:green;">`//`*`Pre-processing:`*</span>
**`append`**` "1" bit `**`to`**` message`
**`append`**` "0" bits `**`until`**` message length in bits ≡ 448 (mod 512)`
**`append`**` bit (bit, not byte) length of unpadded message `**`as`**` `*`64-bit``   ``little-endian``   ``integer`*` `**`to`**` message`

<span style="color:green;">`//`*`Process``   ``the``   ``message``   ``in``   ``successive``   ``512-bit``   ``chunks:`*</span>
**`for``   ``each`**` `*`512-bit`*` chunk `**`of`**` message`
`    break chunk into sixteen 32-bit little-endian words w[i], 0 ≤ i ≤ 15`

`    `<span style="color:green;">`//`*`Initialize``   ``hash``   ``value``   ``for``   ``this``   ``chunk:`*</span>
`    `**`var`**` `*`int`*` a := h0`
`    `**`var`**` `*`int`*` b := h1`
`    `**`var`**` `*`int`*` c := h2`
`    `**`var`**` `*`int`*` d := h3`

`    `<span style="color:green;">`//`*`Main``   ``loop:`*</span>
`    `**`for`**` i `**`from`**` 0 `**`to`**` 63`
`        `**`if`**` 0 ≤ i ≤ 15 `**`then`**
`            f := (b `**`and`**` c) `**`or`**` ((`**`not`**` b) `**`and`**` d)`
`            g := i`
`        `**`else``   ``if`**` 16 ≤ i ≤ 31`
`            f := (d `**`and`**` b) `**`or`**` ((`**`not`**` d) `**`and`**` c)`
`            g := (5×i + 1) `**`mod`**` 16`
`        `**`else``   ``if`**` 32 ≤ i ≤ 47`
`            f := b `**`xor`**` c `**`xor`**` d`
`            g := (3×i + 5) `**`mod`**` 16`
`        `**`else``   ``if`**` 48 ≤ i ≤ 63`
`            f := c `**`xor`**` (b `**`or`**` (`**`not`**` d))`
`            g := (7×i) `**`mod`**` 16`

`        temp := d`
`        d := c`
`        c := b`
`        b := b + `**`leftrotate`**`((a + f + k[i] + w[g]) , r[i])`
`        a := temp`

`    `<span style="color:green;">`//`*`Add``   ``this``   ``chunk's``   ``hash``   ``to``   ``result``   ``so``   ``far:`*</span>
`    h0 := h0 + a`
`    h1 := h1 + b`
`    h2 := h2 + c`
`    h3 := h3 + d`

**`var`**` `*`int`*` digest := h0 `**`append`**` h1 `**`append`**` h2 `**`append`**` h3 `<span style="color:green;">`//`*`(expressed``   ``as``   ``little-endian)`*</span>

`  `<span style="color:green;">`//`*`leftrotate``   ``function``   ``definition`*</span>
`  `**`leftrotate`**` (x, c)`
`      return (x << c) `**`or`**` (x >> (32-c));`

  - 참고: RFC 1321에 나온 공식외에 다음과 같은 공식을 쓰면 퍼포먼스가 향상될 수 있다(어셈블리어가 사용될 때 유용하다 - 다른 언어가 쓰일 경우에는 대개 컴파일러가 위의 코드를 최적화 해준다.)

`(0  ≤ i ≤ 15): f := d `**`xor`**` (b `**`and`**` (c `**`xor`**` d))`
`(16 ≤ i ≤ 31): f := c `**`xor`**` (d `**`and`**` (b `**`xor`**` c))`

## 각주

<references/>

[분류:암호화 해시 함수](https://ko.wikipedia.org/wiki/분류:암호화_해시_함수 "wikilink") [분류:체크섬 알고리즘](https://ko.wikipedia.org/wiki/분류:체크섬_알고리즘 "wikilink")

1.