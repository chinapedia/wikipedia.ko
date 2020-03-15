> This article is converted from Wikipedia: [ROHC](https://ko.wikipedia.org/wiki/ROHC).


**ROHC**()는 [IP](https://ko.wikipedia.org/wiki/인터넷_프로토콜 "wikilink"), [UDP](../Page/사용자_데이터그램_프로토콜.md "wikilink"), [RTP](https://ko.wikipedia.org/wiki/RTP "wikilink"), [TCP](https://ko.wikipedia.org/wiki/전송_제어_프로토콜 "wikilink") 헤더를 압축하는 표준화된 기법이다. 이 압축 기법은 IETF RFC 1144, RFC 2508에 기술된 기존의 압축 기법과 비교하여 패킷 유실이 많이 발생하는 무선 링크에서 높은 성능을 보여준다.

스트리밍 애플리케이션에서 IP, UDP, RTP 헤더의 오버헤드는 [IPv4](https://ko.wikipedia.org/wiki/IPv4 "wikilink")의 경우 40 바이트이며, [IPv6](https://ko.wikipedia.org/wiki/IPv6 "wikilink")의 경우 60 바이트이다. [VoIP](https://ko.wikipedia.org/wiki/VoIP "wikilink")의 경우 이 수치는 전체 전송되는 데이터의 60%에 해당되는 양이다. 이러한 엄청난 오버헤드는 대역폭이 한정된 무선 시스템에서는 심각한 문제를 야기할 수 있다.

ROHC를 통해 40 바이트 또는 60 바이트의 오버헤드는 1 또는 3 바이트로 압축되며 수신 측에 전달된 이후 압축이 해제된다.

RFC 3095에 따르면, ROHC는 세 종류의 동작 방식을 가진다: Unidiretional 모드, Bidirectional Optimistic 모드, Bidirectional Reliable 모드.

## Unidirectional Mode (U-Mode)

Unidirectional 모드에서 모든 패킷은 compressor에서 decompressor로의 한 방향으로만 전송된다. 따라서 이 모드는 decompressor에서 compressor로의 경로가 없거나 사용할 수 없는 경우 쓰인다.

## Bidirectional Optimistic Mode (O-Mode)

Bidirectional Optimistic 모드는 Unidirectional 모드와 유사하지만, 오류 복구 요청 메시지(error recovery request)와 중요 context 업데이트 메시지(significant context update)에 대한 확인 메시지가 decompressor에서 compressor로 전송된다는 차이점이 있다. O-mode는 압축 효율을 극대화시키면서 간헐적으로 피드백 채널을 사용하는 특징을 지닌다.

## Bidirectional Reliable Mode (R-Mode)

Bidirectional Reliable 모드는 많은 측면에서 위의 두 방식과 차이점을 보인다. 중요한 차이점으로는 보다 광범위한 피드백 채널의 사용과 보다 엄격한 로직의 적용을 들 수 있다. 이를 통해 compressor와 decompressor는 서로 간의 context synchronization을 유지할 수 있게 된다.

## IR(Initialization & Refresh) 상태, FO(First-Order) 상태, SO(Second-Order) 상태

ROHC 알고리즘은 비디오 압축 기법과 유사하다. 즉 베이스 프레임(base frame)이 있으면 그 이후로는 베이스 프레임과의 차이점을 표시한 프레임이 전송된다. 이렇게 하면 베이스 프레임이 손실되지 않는 한, 높은 패킷 유실율에서도 높은 압축율을 유지할 수 있게 된다.

ROHC compressor는 세 가지 상태 중 하나에 놓이게 된다. IR(Initialization & Refresh) 상태는 compressor가 방금 생성되거나 재설정된 상태로 이 상태에서는 전체 패킷 헤더가 전송된다. FO(First-Order) 상태에서는 compressor가 IP 주소, 포트 번호와 같은 정적인 필드를 인식하고 저장한다. 또한 이 상태에서 compressor는 동적인 패킷 필드 차이를 전송한다. 즉, FO 상태는 정적 필드를 압축하면서 부분적으로 동적 필드도 압축되는 상태이다. SO(Second-Order) 상태에서 compressor는 RTP 시퀀스 번호와 같은 모든 동적 필드를 압축하고 단지 논리적인 시퀀스 번호와 다음 패킷을 검증하기 위한 일부 체크섬(checksum)만을 전송한다. 일반적으로 FO 상태에서는 모든 정적 필드와 대부분의 동적 필드가 압축되고, SO 상태에서는 시퀀스 번호와 체크섬을 사용하여 주기적으로 모든 동적 필드를 압축한다.

시퀀스 번호 필드의 크기는 compressor가 재설정되기 전까지 ROHC가 유실할 수 있는 패킷의 개수에 좌우된다. ROHC 패킷의 크기가 1 바이트일 때는 시퀀스 번호 크기가 4 비트 (-1/+14 프레임 오프셋)이 되며, 2 바이트일 때는 6 비트(-1/+62 프레임 오프셋)가 된다. 따라서 ROHC는 1, 2 바이트 헤더를 통해 최대 62개의 유실 프레임을 허용할 수 있다.

## SO(Second-Order) ROHC 헤더 - 1 바이트 헤더

일반적인 ROHC 구현에서, SO 상태로 들어가면 40 바이트의 IP/UDP/RTP 헤더(VoIP의 경우)는 1 바이트 ROHC 헤더로 바뀐다. 이 상태에서 8 비트 ROHC 헤더는 세 개의 필드로 구성된다.

  - 1 비트 패킷 타입 플래그(packet-type flag): 보다 큰 ROHC 헤더인 경우 '1'로 설정
  - 4 비트 시퀀스 번호: 베이스 프레임에서 -1 \~ +14까지의 범위를 표현
  - 3 비트 CRC

## 새로운 ROHC RFC 문서들

현재, ROHC을 이해하고 구현하는 과정에서 발생하는 혼란을 줄이기 위한 두 개의 새로운 RFC 문서가 발행되어 있다(RFC 4995, RFC 5225). RFC 4995는 ROHC 구조(framework)에 정의하고 있는 반면, RFC 5225는 새로운 버전의 ROHC 프로파일에 대해 정의하고 있다.

## 외부 링크

  - [IETF의 ROHC 공식 working group](https://web.archive.org/web/20090604034444/http://www.ietf.org/html.charters/rohc-charter.html)
  - RFC 3095 - "ROHC Framework and four profiles: RTP, UDP, ESP, and uncompressed"
  - RFC 4815 - Corrections and Clarifications to RFC 3095
  - RFC 4995 - "The RObust Header Compression (ROHC) Framework"
  - RFC 4996 - "RObust Header Compression (ROHC): A Profile for TCP/IP (ROHC-TCP)"
  - RFC 5225 - "RObust Header Compression Version 2 (ROHCv2): Profiles for RTP, UDP, IP, ESP and UDP-Lite"
  - [A free implementation of ROHC on sourceforge.net](http://rohc.sourceforge.net/)
  - [A free and efficient library implementing the ROHC standard](http://launchpad.net/rohc/)

[알고리즘](https://ko.wikipedia.org/wiki/분류:데이터_압축 "wikilink")