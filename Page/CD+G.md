> This article is converted from Wikipedia: [CD+G](https://ko.wikipedia.org/wiki/CD+G).


**CD+G**(**CD+Graphics**)는 오디오 CD에 그래픽 데이터를 추가한 것으로 오디오 데이터 기록 영역의 비어 있는 부분을 활용하여 노래 가사나 간단한 배경 화면 등을 기록한 것이다. 주로 가라오케 CD로 이용되었으며 음악은 일반 CD플레이어로도 재생된다.

## 세부 사항

오디오 CD는 플레이시 초당 75섹터를 읽어오는데 각 섹터는 2352 바이트(24 × 98) 크기로 오디오 데이터와 96 바이트의 서브채널 데이터로 구성되며 이 중에서 96바이트의 서브채널 데이터는 24바이트의 4패킷으로 구성된다.

한 패킷은

  - 1바이트 커맨드(command)
  - 1바이트 인스트럭션(instruction)
  - 2바이트 패리티Q(parityQ)
  - 16바이트 데이터(data)
  - 4바이트 패리티P(parityP)

로 나뉜다.

여기서 16바이트의 데이터는 각각 P, Q, R, S, T, U, V, W의 8비트로 구성되며 이 비트를 서브코드 채널이라고 한다.

|        |   |   |   |   |   |   |   |   |
| ------ | - | - | - | - | - | - | - | - |
| **채널** | P | Q | R | S | T | U | V | W |
| **비트** | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |

P채널은 트랙의 시작을 식별하는데 사용하며 Q채널은 사용자의 데이터 영역위치 정보, 매체의 카달로그 수, [국제 표준 녹음 코드](../Page/국제_표준_녹음_코드.md "wikilink")(ISRC)라는 3가지 형태의 서브코드 Q데이터가 들어있다. R\~W까지의 채널은 CD+G의 텍스트와 그래픽 저장용으로 사용되며 [CD-Text](https://ko.wikipedia.org/wiki/CD-Text "wikilink")도 같은 채널을 사용한다.

CD+G에 이용할 수 있는 용량은 바이트당 6비트 × 패킷당 16바이트 × 섹터당 4패킷 × 초당 75섹터 = 초당 28800비트이며 해상도 300 × 216이고 16컬러의 그림을 표시할 수 있다.

CD+G를 플레이 할 수 있는 대표적인 기기는 NEC [PC 엔진](https://ko.wikipedia.org/wiki/PC_엔진 "wikilink") CD, 필립스 [CD-i](../Page/CD-i.md "wikilink"), [세가 새턴과](../Page/세가_새턴.md "wikilink") [메가 CD](../Page/메가_CD.md "wikilink"), [3DO](https://ko.wikipedia.org/wiki/3DO_인터렉티브_멀티플레이어 "wikilink"), [아미가 CD32와](https://ko.wikipedia.org/wiki/아미가_CD32 "wikilink") CDTV, [아타리 재규어](../Page/아타리_재규어.md "wikilink") CD 등이 있다.

## 외부 링크

  - [The CD+G Museum](http://www.cdplusg.com/)
  - [CD+G revealed](http://www.jbum.com/cdg_revealed.html)
  - [CD+G faq](https://web.archive.org/web/20061105114510/http://www.ncf.carleton.ca/~aa571/cdgfaq.htm)
  - [CD+G 타이틀 리스트](http://www.tricerasoft.com/cdglist.html)

[G](https://ko.wikipedia.org/wiki/분류:CD "wikilink") [분류:소리 저장 매체](https://ko.wikipedia.org/wiki/분류:소리_저장_매체 "wikilink") [분류:영상 저장 매체](https://ko.wikipedia.org/wiki/분류:영상_저장_매체 "wikilink")