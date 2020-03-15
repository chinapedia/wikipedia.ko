> This article is converted from Wikipedia: [RAID](https://ko.wikipedia.org/wiki/RAID).


**복수 배열 독립 디스크**(Redundant Array of Independent Disks 혹은 Redundant Array of Inexpensive Disks)는 여러 개의 [하드 디스크에](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink") 일부 중복된 [데이터](https://ko.wikipedia.org/wiki/데이터 "wikilink")를 나눠서 저장하는 기술이다. **디스크 어레이**(disk array)라고도 한다. 데이터를 나누는 다양한 방법이 존재하며, 이 방법들을 **레벨**이라 하는데, 레벨에 따라 저장장치의 신뢰성을 높이거나 전체적인 성능을 향상시키는 등의 다양한 목적을 만족시킬 수 있다.

최초에 제안되었을 때는 다섯가지의 레벨이 존재했는데, 이후에 중첩 레벨을 비롯한 여러 가지 다른 레벨들이 추가되었다.

RAID는 여러 개의 디스크를 하나로 묶어 하나의 논리적 디스크로 작동하게 하는데, 하드웨어적인 방법과 소프트웨어적인 방법이 있다. 하드웨어적인 방법은 [운영 체제에](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 이 디스크가 하나의 디스크처럼 보이게 한다. 소프트웨어적인 방법은 주로 운영체제 안에서 구현되며, 사용자에게 디스크를 하나의 디스크처럼 보이게 한다.

## 역사

RAID의 기반이 되는 개념은 [Geac 컴퓨터 코퍼레이션의](https://ko.wikipedia.org/wiki/Geac_컴퓨터_코퍼레이션 "wikilink") 공동 창업자 Gus German, Ted Grunau가 이에 대한 개념으로 MF-100을 가리키면서 처음 이야기되었다.\[1\]

RAID라는 용어는 1987년 [캘리포니아 대학교 버클리의](https://ko.wikipedia.org/wiki/캘리포니아_대학교_버클리 "wikilink") [데이비드 패터슨](https://ko.wikipedia.org/wiki/데이비드_패터슨 "wikilink"), [가스 깁슨](https://ko.wikipedia.org/wiki/가스_깁슨 "wikilink"), [랜디 카츠가](https://ko.wikipedia.org/wiki/랜디_카츠 "wikilink") 발명하였다.

## 표준 레이드 레벨

흔히 쓰이는 레이드 레벨을 간추리면 다음과 같다.

[섬네일](https://ko.wikipedia.org/wiki/파일:RAID_0.svg "wikilink")

  - [RAID 0](https://ko.wikipedia.org/wiki/RAID_0 "wikilink")
    [패리티](../Page/패리티_비트.md "wikilink")(오류 검출 기능)가 없는 [스트리핑된](https://ko.wikipedia.org/wiki/데이터_스트리핑 "wikilink") 세트 (적어도 2 개의 디스크). 개선된 성능에 추가적인 기억 장치를 제공하는 게 장점이지만 실패할 경우 자료의 안전을 보장할 수 없다. 디스크에서 실패가 일어나면 배열을 파괴하게 되는데, 이러한 파괴는 디스크를 많이 장착할수록 가능성이 더 크다. 하나의 단일 디스크 실패는 배열을 완전히 파괴한다. 왜냐하면 데이터가 레이드 0으로 쓰일 때, 데이터는 여러 조각으로 나뉘기 때문이다. 조각의 수는 드라이브 안의 디스크 수와 일치한다. 조각들은 각 디스크에 동시적으로 같은 섹터 위에 기록된다. 완전한 데이터 덩어리의 작은 토막들이 병렬로 드라이브를 읽어 낼 수 있게 해 주며, 이러한 종류의 배열은 넓은 대역너비를 제공한다. 그러나 디스크들의 한 섹터가 실패할 때는 모든 다른 디스크 위의 일치하는 섹터가 사용 불능으로 표시된다. 왜냐하면 데이터의 일부가 손상된 것이 아니기 때문이다. 레이드 0은 오류 검출 기능을 제공하지 않기 때문에 어떠한 오류도 복구하지 못한다. 배열에 디스크를 더 많이 넣으면 더 높은 대역을 사용할 수 있겠지만 데이터 손실의 큰 위험이 도사리게 된다.
  - [RAID 1](https://ko.wikipedia.org/wiki/RAID_1 "wikilink")
    [패리티](../Page/패리티_비트.md "wikilink")(오류 검출 기능)가 없는 [미러링된](../Page/디스크_미러링.md "wikilink") 세트 (적어도 2 개의 디스크). 디스크 오류와 단일 디스크 실패에 대비하여 실패 방지 기능이 있다. 분할 탐색을 지원하는 다중 스레드를 지원하는 운영 체제를 사용할 때 읽기 성능이 향상된다. 다만, 쓰기를 시도할 때에는 약간의 성능 저하가 뒤따른다. 배열은 적어도 하나의 드라이브가 기능하는 한 계속 동작한다.
  - [RAID 3](https://ko.wikipedia.org/wiki/RAID_3 "wikilink") 및 [RAID 4](https://ko.wikipedia.org/wiki/RAID_4 "wikilink")
    패리티가 단순 제공되는(dedicated) 스트리핑된 세트 (적어도 3 개의 디스크). (RAID 4는 2개의 디스크)
  - [RAID 5](https://ko.wikipedia.org/wiki/RAID_5 "wikilink")
    패리티가 배분되는(distributed) 스트리핑된 세트 (적어도 3 개의 디스크).
  - [RAID 6](https://ko.wikipedia.org/wiki/RAID_6 "wikilink")
    패리티가 배분되는(distributed) 스트리핑된 세트 (적어도 4 개의 디스크).
  - [RAID 0+1](https://ko.wikipedia.org/wiki/RAID_0+1 "wikilink")
    레이드 0+1은 먼저 디스크를 스트리핑(RAID 0)하고, 디스크를 미러링(RAID 1) 한다. (적어도 4개의 디스크)
    디스크가 6개일경우는 3개씩 스트리핑하고 미러링을 그다음에 수행한다.
  - [RAID 10](https://ko.wikipedia.org/wiki/RAID_10 "wikilink")([RAID 1+0](https://ko.wikipedia.org/wiki/RAID_1+0 "wikilink"))
    레이드 10은 먼저 디스크를 미러링(RAID 1)하고, 그 이후 스트리핑 한다. (적어도 4개의 디스크)
    디스크가 6개일 경우는 2개씩 미러링을 하고, 미러링된 3개를 스트리핑 한다.
  - [RAID 50](https://ko.wikipedia.org/wiki/RAID_50 "wikilink")([RAID 5+0](https://ko.wikipedia.org/wiki/RAID_5+0 "wikilink"))
    패리티가 배분되는(distributed) 스트리핑된 세트를 다시 스트리핑(RAID 0) 한다. (적어도 6개의 디스크)
  - [RAID 1E](https://ko.wikipedia.org/wiki/RAID_1E "wikilink")
    미러링과 데이터 스트라이핑의 결합이다.(적어도 3 개의 디스크).

## 비표준 레이드 레벨

  - [RAID 1.5](https://ko.wikipedia.org/wiki/RAID_1.5 "wikilink")

읽기 시에는 RAID 0 처럼 작동하여 성능상의 이점을 얻는다. 쓰기 시에는 RAID 5처럼 작동하여 안정성을 도모한다. RAID 1에 비해 읽기 성능에서 약간의 이점이 있을 뿐이라 널리 쓰이지는 않는다. HighPoint사의 컨트롤러에서만 지원하는 방식이다.

## 같이 보기

  - [디스크 어레이 컨트롤러](https://ko.wikipedia.org/wiki/디스크_어레이_컨트롤러 "wikilink")
  - [하드 디스크 드라이브](https://ko.wikipedia.org/wiki/하드_디스크_드라이브 "wikilink")
  - [S.M.A.R.T.](https://ko.wikipedia.org/wiki/S.M.A.R.T. "wikilink")

## 각주

## 외부 링크

  -
[분류:컴퓨터 저장 매체](https://ko.wikipedia.org/wiki/분류:컴퓨터_저장_매체 "wikilink")

1.  [Parents of Invention: The Development of Library Automation Systems in the Late 20th Century.](https://books.google.com/books?id=xUT_d4tN7AgC&lpg=PA103&dq=ted%20grunau&pg=PA103#v=onepage&q=ted%20grunau&f=false) By Christopher Syed <https://books.google.com/books?id=xUT_d4tN7AgC&lpg=PA103&dq=ted%20grunau&pg=PA103#v=onepage&q=ted%20grunau&f=false>