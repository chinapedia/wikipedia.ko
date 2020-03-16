> This article is converted from Wikipedia: [6LoWPAN](https://ko.wikipedia.org/wiki/6LoWPAN).


**6LoWPAN**\[1\]은 [IETF](https://ko.wikipedia.org/wiki/IETF "wikilink")의 워킹 그룹 중 하나이며, [IEEE 802.15.4로](../Page/IEEE_802.15.4.md "wikilink") 대표되는 저전력 무선 사설 네트워크(Low-power Wireless Personal Area Network), [센서 네트워크](https://ko.wikipedia.org/wiki/센서_네트워크 "wikilink") 위에서 [인터넷](../Page/인터넷.md "wikilink") [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")을 사용하기 위한 아키텍처 등을 표준화하고 있는 단체이다.

## 표준 문서

  - RFC 4919\[2\]
  - RFC 4944\[3\]: 제목은 'Transmission of IPv6 Packet over [IEEE 802.15.4](../Page/IEEE_802.15.4.md "wikilink") Networks'이며, 최소 MTU가 1280 옥텟인 IPv6 패킷을 페이로드에 최대 127 옥텟을 담을 수 있는 [IEEE 802.15.4](../Page/IEEE_802.15.4.md "wikilink") 프레임에 전송하기 위한 헤더 압축, 링크 단계 단편화/재조립 메커니즘 등을 수행하는 6LoWPAN 애플리케이션 계층을 정의하고 있다.
  - draft-ietf-6lowpan-nd\[4\]: 일반적인 신뢰성 있는 링크(가령, [이더넷](../Page/이더넷.md "wikilink") 등)를 가정하고 동작하는 [IPv6](../Page/IPv6.md "wikilink") Neighbor Discovery [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")은 [멀티캐스트](../Page/멀티캐스트.md "wikilink")를 기반으로 하고 있기 때문에 LoWPAN에는 잘 맞지 않다. 이 드래프트는 '6LoWPAN Neighbor Discovery'에 관한 것으로 멀티캐스트의 사용을 지양하고, LoWPAN 영역에 대해서는 그 경계에 있는 경계 라우터 (Edge Router)에 Neighbor Discovery에 관한 기능을 집중시켰다.
  - draft-ietf-6lowpan-hc\[5\]: RFC4944에서 정의한 헤더 압축에 대해서 보완할 사항에 대해 정의한 드래프트이다. 표준이 완료되면 RFC4944를 갱신하게 된다.

## 각주

[분류:IPv6](https://ko.wikipedia.org/wiki/분류:IPv6 "wikilink") [무선 네트워크](https://ko.wikipedia.org/wiki/분류:무선_네트워크 "wikilink")

1.  IETF 6LoWPAN Working Group <http://tools.ietf.org/wg/6lowpan>
2.  RFC 4919
3.  RFC 4944
4.  draft-ietf-6lowpan-nd <http://tools.ietf.org/html/draft-ietf-6lowpan-nd>
5.  draft-ietf-6lowpan-hc <http://tools.ietf.org/html/draft-ietf-6lowpan-hc>