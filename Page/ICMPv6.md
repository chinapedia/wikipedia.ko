> This article is converted from Wikipedia: [ICMPv6](https://ko.wikipedia.org/wiki/ICMPv6).


**ICMPv6**(Internet Control Message Protocol version 6)은 [IPv6](../Page/IPv6.md "wikilink")(인터넷 프로토콜 버전 6)용 [인터넷 제어 메시지 프로토콜](../Page/인터넷_제어_메시지_프로토콜.md "wikilink")(ICMP) 구현체이다. IPCMv6는 RFC 4443에 정의되어 있다.\[1\] ICMPv6는 IPv6의 중요한 부분이며 오류 보고와 진단 기능(예: [핑](../Page/핑.md "wikilink"))을 수행하고, 앞으로의 변경사항을 구현할 확장기능을 위한 프레임워크를 가지고 있다.

새로운 ICMPv6 메시지 타입을 정의하는 여러 확장기능들과 기존 ICMPv6 메시지 타입을 위한 새로운 옵션들이 게시되고 있다. [이웃 탐색 프로토콜](https://ko.wikipedia.org/wiki/이웃_탐색_프로토콜 "wikilink")(NDP)은 IPv6의 노드 탐색 프로토콜이며 [ARP의](../Page/주소_결정_프로토콜.md "wikilink") 기능을 대체하고 강화한다.\[2\] [안전 이웃 탐색](https://ko.wikipedia.org/wiki/안전_이웃_탐색 "wikilink")(Secure Neighbor Discovery, SEND)은 추가 보안을 제공하는 NDP의 확장이다. [멀티캐스트 리스너 디스커버리](https://ko.wikipedia.org/wiki/멀티캐스트_리스너_디스커버리 "wikilink")(MLD)는 직접 부착된 링크 위의 [멀티캐스트](../Page/멀티캐스트.md "wikilink") 리스너를 IPv6 라우터가 탐색하기 위해 사용되며 이는 마치 [IPv4](../Page/IPv4.md "wikilink")에서 [인터넷 그룹 관리 프로토콜](https://ko.wikipedia.org/wiki/인터넷_그룹_관리_프로토콜 "wikilink")(IGMP)을 사용하는 것과 같다. [멀티캐스트 라우터 디스커버리](https://ko.wikipedia.org/wiki/멀티캐스트_라우터_디스커버리 "wikilink")(MRD)는 멀티캐스트 라우터의 탐색을 허용한다.

## 메시지 타입과 포맷

ICMPv6 메시지들은 오류 메시지와 정보 메시지로 분류할 수 있다. ICMPv6 메시지들은 IPv6 패킷에 의해 전달되며 이 패킷 안의 ICMPv6의 [IPv6 넥스트 헤더](../Page/IPv6.md "wikilink") 값은 값 58로 설정된다.

ICMPv6 메시지는 헤더와 프로토콜 페이로드로 구성된다. 헤더에는 오직 3개의 필드만을 담고 있다: *type* (8비트), *code* (8비트), *checksum* (16비트). *type*은 메시지의 타입을 지정한다. 0\~127 사이(high-order 비트는 0)의 값은 오류 메시지를 나타내는 반면, 128\~255 사이의 값(high-order 비트는 1)은 정보 메시지를 의미한다. *code* 필드의 값은 메시지의 타입에 따라 달라지며 메시지의 세부 수준을 제공한다. *checksum* 필드는 ICMP 메시지의 최소한의 수준의 무결성 확인을 제공한다.

| 비트 오프셋 | 0–7    | 8–15 | 16–31    |
| ------ | ------ | ---- | -------- |
| **0**  | Type   | Code | Checksum |
| **32** | 메시지 본문 |      |          |
|        |        |      |          |

ICMPv6 패킷

### 타입

컨트롤 메시지는 *type* 필드의 값에 의해 식별된다. *code* 필드는 메시지의 추가 문맥 정보를 제공한다. 일부 메시지들은 ICMP 메시지 타입과 동등한 역할을 수행한다.

|      타입       |                                                                   코드                                                                    |
| :-----------: | :-------------------------------------------------------------------------------------------------------------------------------------: |
|       값       |                                                                   의미                                                                    |
| ICMPv6 오류 메시지 |                                                                                                                                         |
|       1       |                                           [목적지 도달 불가](../Page/인터넷_제어_메시지_프로토콜.md "wikilink")                                            |
|       1       |                                                         목적지와의 통신이 관리적인 측면에서 금지됨                                                         |
|       2       |                                                               원본 주소 범위 초과                                                               |
|       3       |                                                                주소 도달 불가                                                                 |
|       4       |                                                                포트 도달 불가                                                                 |
|       5       |                                                     원본 주소가 정책의 ingress/egress를 실패함                                                      |
|       6       |                                                               목적지로의 루트 거부                                                               |
|       7       |                                                              원본 라우팅 헤더의 오류                                                              |
|       2       |                                      [패킷이 너무 큼](https://ko.wikipedia.org/wiki/IPv6_패킷 "wikilink")                                       |
|       3       |                                             [시간 초과](../Page/인터넷_제어_메시지_프로토콜.md "wikilink")                                              |
|       1       |                                                    조각 재조합(fragment reassembly) 시간 초과                                                    |
|       4       |                                                                 파라미터 문제                                                                 |
|       1       |                                                          인식할 수 없는 넥스트 헤더 타입 확인                                                          |
|       2       |                                                           인식할 수 없는 IPv6 옵션 확인                                                           |
|      100      |                                                                 비공개 실험                                                                  |
|      101      |                                                                 비공개 실험                                                                  |
|      127      |                                                      ICMPv6 오류 메시지를 위한 확장을 위해 예약됨                                                       |
| ICMPv6 정보 메시지 |                                                                                                                                         |
|      128      |                                                      [핑](../Page/핑.md "wikilink")                                                       |
|      129      |                                                      [핑](../Page/핑.md "wikilink")                                                       |
|      130      | [멀티캐스트 리스너 쿼리](https://ko.wikipedia.org/wiki/멀티캐스트_리스너_쿼리 "wikilink") ([MLD](https://ko.wikipedia.org/wiki/멀티캐스트_리스너_디스커버리 "wikilink")) |
|      131      |                              [멀티캐스트 리스너 리포트](https://ko.wikipedia.org/wiki/멀티캐스트_리스너_리포트 "wikilink") (MLD)                              |
|      132      |                                [멀티캐스트 리스너 던](https://ko.wikipedia.org/wiki/멀티캐스트_리스너_던 "wikilink") (MLD)                                |
|      133      |                            Router Solicitation ([NDP](https://ko.wikipedia.org/wiki/이웃_탐색_프로토콜 "wikilink"))                             |
|      134      |                                                       Router Advertisement (NDP)                                                        |
|      135      |                                                       Neighbor Solicitation (NDP)                                                       |
|      136      |                                                      Neighbor Advertisement (NDP)                                                       |
|      137      |                                                             리다이렉트 메시지 (NDP)                                                             |
|      138      |                                                                라우터 리넘버링                                                                 |
|       1       |                                                               라우터 리넘버링 결과                                                               |
|      255      |                                                                시퀀스 번호 리셋                                                                |
|      139      |                                                              ICMP 노드 정보 쿼리                                                              |
|       1       |                                                데이터 필드는 이 쿼리의 주제인 이름을 포함하며 NOOP의 경우 비어있다.                                                |
|       2       |                                                    데이터 필드는 이 쿼리의 주제인 IPv4 주소를 포함한다.                                                     |
|      140      |                                                              ICMP 노드 정보 응답                                                              |
|       1       |                                                  응답자가 답변 제공을 거부한다. 응답 데이터 필드는 비어있게 된다.                                                  |
|       2       |                                             응답자에 대한 쿼리의 Qtype을 알 수 없다. 응답 데이터 필드는 비어있게 된다.                                              |
|      141      |                                             Inverse Neighbor Discovery Solicitation Message                                             |
|      142      |                                            Inverse Neighbor Discovery Advertisement Message                                             |
|      143      |             Multicast Listener Discovery ([MLDv2](https://ko.wikipedia.org/wiki/멀티캐스트_리스너_디스커버리 "wikilink")) 리포트 (RFC 3810)             |
|      144      |                                              Home Agent Address Discovery Request Message                                               |
|      145      |                                               Home Agent Address Discovery Reply Message                                                |
|      146      |                                                       Mobile Prefix Solicitation                                                        |
|      147      |                                                       Mobile Prefix Advertisement                                                       |
|      148      |                    Certification Path Solicitation ([SEND](https://ko.wikipedia.org/wiki/안전_이웃_탐색_프로토콜 "wikilink"))                     |
|      149      |                                                 Certification Path Advertisement (SEND)                                                 |
|      151      |                    Multicast Router Advertisement ([MRD](https://ko.wikipedia.org/wiki/멀티캐스트_라우터_디스커버리 "wikilink"))                     |
|      152      |                                                   Multicast Router Solicitation (MRD)                                                   |
|      153      |                                                   Multicast Router Termination (MRD)                                                    |
|      155      |                                                               RPL 컨트롤 메시지                                                               |
|      200      |                                                                 비공개 실험                                                                  |
|      201      |                                                                 비공개 실험                                                                  |
|      255      |                                                      ICMPv6 정보 메시지를 위한 확장을 위해 예약됨                                                       |

위의 표는 완전하지 않으며, 할당된 IPCMv6 타입의 완전한 목록은 이 링크에서 볼 수 있다: [IANA: ICMPv6 Parameters](http://www.iana.org/assignments/icmpv6-parameters).

### 체크섬

ICMPv6는 헤더에 16비트 [체크섬](../Page/체크섬.md "wikilink")을 포함시킴으로써 최소한의 수준의 메시지 무결성 확인을 제공한다. 체크섬은 IPv6 표준에 의거하여 IPv6 헤더의 [의사 헤더로](../Page/사용자_데이터그램_프로토콜.md "wikilink") 시작하여 계산되며\[3\] 원본과 도착 주소, 패킷 길이와 넥스트 헤더 필드로 구성되며 후자의 경우 58이라는 값으로 설정된다. 이 의사 헤더 뒤에 체크섬은 IPCMv6 메시지와 함께 계속해나간다. 체크섬 계산은 인터넷 프로토콜 표준에 따라 수행된다.\[4\] [ICMP의](../Page/인터넷_제어_메시지_프로토콜.md "wikilink") IPv4의 계산 방식과는 차이가 있으나 [TCP에서](../Page/전송_제어_프로토콜.md "wikilink") 수행되는 계산 방식과 비슷하다.

| 비트 오프셋 | 0 – 7     | 8–15   | 16–23 | 24–31 |
| ------ | --------- | ------ | ----- | ----- |
| 0      | 원본 주소     |        |       |       |
| 32     |           |        |       |       |
| 64     |           |        |       |       |
| 96     |           |        |       |       |
| 128    | 도착 주소     |        |       |       |
| 160    |           |        |       |       |
| 192    |           |        |       |       |
| 224    |           |        |       |       |
| 256    | ICMPv6 길이 |        |       |       |
| 288    | 제로(0)     | 넥스트 헤더 |       |       |
|        |           |        |       |       |

ICMPv6 의사 헤더

## 메시지 처리

IPCMv6 노드가 패킷을 수신하면 메시지의 타입에 의존하는 조치에 착수해야 한다. ICMPv6 프로토콜은 네트워크 부하를 피하기 위해 동일 도착지로 전송되는 오류 메시지의 수에 제한을 두어야 한다. 이를테면 노드가 오류가 있는 패킷의 포워드를 계속하는 경우 ICMP는 최초 패킷에 오류 신호를 보내고 주기적으로 이 작업을 수행하며, 여기에는 최소한의 고정 주기라든지 고정된 네트워크 최대 부하가 설정된다. ICMP 오류 메시지는 다른 ICMP 오류 메시지에 대한 응답에 대해 송신해서는 안 된다.

## 각주

## 외부 링크

  - [IANA: ICMPv6 Parameters](https://www.iana.org/assignments/icmpv6-parameters/icmpv6-parameters.xhtml)

  -
[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:인터넷 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_계층_프로토콜 "wikilink") [분류:네트워크 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_계층_프로토콜 "wikilink") [분류:IPv6](https://ko.wikipedia.org/wiki/분류:IPv6 "wikilink")

1.  RFC 4443, *Internet Control Message Protocol (ICMPv6) for the Internet Protocol Version 6 (IPv6) Specification*
2.  RFC 3315, § 3
3.  [RFC 2460, '' Internet Protocol, Version 6 (IPv6) Specification*, Section 8.1 (*Upper-Layer Checksum''), S. Deering, R. Hinden (December 1998)](http://tools.ietf.org/html/rfc2460#section-8.1)
4.  RFC 1071, *Computing the Internet Checksum*, R. Braden, D. Borman, C. Partridge (September 1988)