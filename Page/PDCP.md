> This article is converted from Wikipedia: [PDCP](https://ko.wikipedia.org/wiki/PDCP).


**PDCP**(Packet Data Convergence Protocol)는 [UMTS](../Page/UMTS.md "wikilink")내 무선 트래픽 스택의 계층 중 하나이며, IP 헤더 압축 및 압축 해지, 사용자 데이터의 전송, Radio Bearer에 대한 시퀀스 번호 유지를 수행한다.

압축 기술은 RFC 2507 또는 RFC 3095에 기반한다. RFC 1144에서 기술되는 몇 가지 정보도 사용되지만 현대 [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink")에서는 사용되지 않는다.

만일, **PDCP**가 *압축 없음*으로 구성될 경우, **PDCP**는 압축없이 IP 패킷을 전송한다. **PDCP**는 Radio Link Control (RLC)이라 불리는 하위 계층에서 제공하는 서비스를 사용한다.

**PDCP** 헤더는 두 개의 필드로 구성된다: PID, PDU TYPE.

  - **[PDU Type](https://ko.wikipedia.org/wiki/Protocol_data_unit "wikilink")** 필드는 PDU가 데이터 PDU인지 Sequence Number PDU인지를 가리킨다.
  - **PID** 필드는 사용되는 헤더 압축 프로토콜 타입, 패킷 타입, CID를 가리킨다.

## 참고 문헌

  - ETSI TS 125 323 V5.0.0; Universal Mobile Telecommunications System (UMTS); Packet Data Convergence Protocol (PDCP) specification (3GPP TS 25.323 version 5.0.0 Release 5); Mar. 2002; pp. 1-21; XP-002259036.
  - Wu, Chih-Hsiang , *Method for determining triggering of a PDCP sequence number synchronization procedure*, September 2007, [US Patent 7266105](https://web.archive.org/web/20090822151114/http://www.patentstorm.us/patents/7266105/claims.html), Innovative Sonic Limited

[분류:이동 통신](https://ko.wikipedia.org/wiki/분류:이동_통신 "wikilink")