> This article is converted from Wikipedia: [QSAM](https://ko.wikipedia.org/wiki/QSAM).


[IBM 메인프레임](../Page/IBM_메인프레임.md "wikilink") [운영 체제에서](../Page/운영_체제.md "wikilink") **QSAM**(Queued sequential access method, 대기 순차 접근 방법)\[1\]은 [데이터셋](https://ko.wikipedia.org/wiki/데이터셋 "wikilink")을 순차적으로 읽고 쓰는 접근 방식이다. QSAM은 [OS/360](https://ko.wikipedia.org/wiki/OS/360 "wikilink"), [OS/VS2](https://ko.wikipedia.org/wiki/OS/VS2 "wikilink"), [MVS](../Page/MVS.md "wikilink"), [z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink") 및 관련 운영 체제에서 이용할 수 있다.

QSAM은 [천공 카드](../Page/천공_카드.md "wikilink") 리더, 펀치, 라인 프린터와 같은 본래부터 순차적인 장치들과, 자기 디스크와 같이 직접 어드레싱할 수 있는 장치의 데이터에 사용된다. QSAM은 장치 독립성을 제공한다: 각기 다른 장치에 최대한 동일한 [API](../Page/API.md "wikilink") 호출이 사용된다.

QSAM의 queue는 대기 처리를 뜻하며 읽기의 차단을 막고 쓰기를 차단하는 완충 역할을 담당한다. 이를 통해 프로그램들이 물리 블록의 데이터 안에 위치한 논리 데이터를 읽고 쓸 수 있게 한다. 이는 프로그램들이 물리 블록의 데이터에 접근할 수 있지만 블록 안의 논리 데이터로의 접근을 지원하지 못하는, 덜 진보화된 [BSAM](https://ko.wikipedia.org/wiki/BSAM "wikilink")(기본 순차 입출력 방식)과는 반대된다.

실제로 QSAM은 truncate된 마지막 블록과 truncate된 임베디드 블록을 관리하며, 이들은 사용자에게 완전히 투명하게 나타난다.

QSAM의 API는 [유닉스](../Page/유닉스.md "wikilink")와 [윈도우와](../Page/마이크로소프트_윈도우.md "wikilink") 같은 다른 운영 체제의 *open*, *read*, *write*, *close* 호출에서 제공하는 인터페이스와 견줄 수 있다.

## 같이 보기

  - [순차 접근 메모리](https://ko.wikipedia.org/wiki/순차_접근_메모리 "wikilink")(SAM)
  - [HSAM](../Page/IBM_정보_관리_시스템.md "wikilink")
  - [ISAM](https://ko.wikipedia.org/wiki/색인_순차_접근_방식 "wikilink")(색인 순차 접근 방식)

## 각주

[분류:IBM 메인프레임 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM_메인프레임_운영_체제 "wikilink")

1.