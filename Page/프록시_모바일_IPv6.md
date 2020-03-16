> This article is converted from Wikipedia: [  IPv6](https://ko.wikipedia.org/wiki/__IPv6).


**Proxy Mobile IP**(**PMIP** 또는 **Proxy Mobile IPv6**)는 [IETF](https://ko.wikipedia.org/wiki/IETF "wikilink")에서 정의한 [네트워크](https://ko.wikipedia.org/wiki/네트워크 "wikilink") [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")이다. Proxy Mobile IP는 [Mobile IP와](https://ko.wikipedia.org/wiki/Mobile_IP "wikilink") 유사하게 동작하지만 [단말](https://ko.wikipedia.org/wiki/단말 "wikilink")에 이동성에 대한 어떠한 처리도 요구하지 않는다는 차이점이 있다. Proxy Mobile IP와 같이 단말의 이동과 관련하여 단말에게 어떠한 특별한 동작을 요구하지 않는 기법을 통칭하여 [망 기반 이동성 관리](https://ko.wikipedia.org/wiki/망_기반_이동성_관리 "wikilink")(network-based mobility management)라고 한다. Proxy Mobile IP를 사용할 경우, 단말의 [TCP/IP 프로토콜 스택에는](../Page/인터넷_프로토콜_스위트.md "wikilink") 어떠한 수정도 가해지지 않으며 단말은 자신의 [IP](../Page/인터넷_프로토콜.md "wikilink") 주소를 바꾸지 않고 접속 위치를 바꿀 수 있다.

## 동작 원리

Proxy Mobile IP는 두 네트워크 구성요소 - [LMA](https://ko.wikipedia.org/wiki/Local_Mobility_Anchor "wikilink")(Local Mobility Anchor), [MAG](https://ko.wikipedia.org/wiki/Mobile_Access_Gateway "wikilink")(Mobile Access Gateway) 사이에서 동작하는 프로토콜이다. MAG는 단말이 접속한 [링크](https://ko.wikipedia.org/wiki/링크 "wikilink")에 연결된 [라우터](../Page/라우터.md "wikilink")에서 동작하면서 단말의 이동과 관련한 처리를 담당한다. LMA는 Proxy Mobile IP [도메인](https://ko.wikipedia.org/wiki/도메인 "wikilink") 내에서 단말에 대한 [홈 에이전트](https://ko.wikipedia.org/wiki/홈_에이전트 "wikilink")(Home agent)로 동작한다.

Proxy Mobile IP는 다음과 같은 순서로 동작한다.

  - 단말이 Proxy Mobile IP 도메인으로 진입한다.
  - MAG는 단말에 대한 [권한부여](https://ko.wikipedia.org/wiki/권한부여 "wikilink")(authorization)을 수행한다.
  - 단말은 자신의 IP 주소를 획득한다.
  - MAG는 단말의 위치를 LMA에 알린다.
  - MAG와 LMA는 양방향 터널을 개설한다.

## 같이 보기

  - [Mobile IP](https://ko.wikipedia.org/wiki/Mobile_IP "wikilink")
  - [Mobile IPv6](https://ko.wikipedia.org/wiki/Mobile_IPv6 "wikilink")

## 외부 링크

  - [Proxy Mobile IPv6 IETF 드래프트](https://web.archive.org/web/20100205154204/http://ietfreport.isoc.org/all-ids/draft-ietf-netlmm-proxymip6-18.txt)
  - [Proxy Mobile IPv6 IETF RFC 표준(RFC5213)](http://tools.ietf.org/html/rfc5213)

[분류:컴퓨터 네트워킹](https://ko.wikipedia.org/wiki/분류:컴퓨터_네트워킹 "wikilink") [분류:컴퓨터 통신](https://ko.wikipedia.org/wiki/분류:컴퓨터_통신 "wikilink") [분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:통신공학](https://ko.wikipedia.org/wiki/분류:통신공학 "wikilink") [분류:통신](https://ko.wikipedia.org/wiki/분류:통신 "wikilink")