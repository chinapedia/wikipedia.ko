> This article is converted from Wikipedia: [DNSSEC](https://ko.wikipedia.org/wiki/DNSSEC).


**DNSSEC**(Domain Name System Security Extensions)는 [인터넷 프로토콜](https://ko.wikipedia.org/wiki/인터넷_프로토콜 "wikilink")(IP) 네트워크에 사용되어 [도메인 네임 시스템](https://ko.wikipedia.org/wiki/도메인_네임_시스템 "wikilink")(DNS)이 제공하는 특정한 종류의 정보를 취득하기 위한 [국제 인터넷 표준화 기구](https://ko.wikipedia.org/wiki/국제_인터넷_표준화_기구 "wikilink")(IETF) 사양을 위한 스위트의 하나이다. DNS 클라이언트에게 DNS 데이터의 [메시지 인증](https://ko.wikipedia.org/wiki/메시지_인증 "wikilink"), 실체에 대한 인증 거부, 데이터 무결성을 제공하지만 가용성이나 비밀 보장을 제공하지는 않는 DNS에 대한 확장 집합이다.

## 조작

### 리소스 레코드

  - RRSIG (리소스 레코드 서명, resource record signature)
  - DNSKEY
  - DS (delegation signer)
  - NSEC (next secure record)
  - NSEC3 (next secure record version 3)
  - NSEC3PARAM (next secure record version 3 parameters)

#### 알고리즘

<table>
<thead>
<tr class="header">
<th><p>알고리즘 필드</p></th>
<th><p>알고리즘</p></th>
<th><p>출처</p></th>
<th><p>구현 상태<ref>{{웹 인용</p></th>
<th><p>url = <a href="http://tools.ietf.org/html/rfc6944">http://tools.ietf.org/html/rfc6944</a></p></th>
<th><p>title = RFC-6944</p></th>
<th><p>publisher = <a href="https://ko.wikipedia.org/wiki/국제_인터넷_표준화_기구" title="wikilink">IETF</a> }}</ref></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/RSA" title="wikilink">RSA</a>/<a href="https://ko.wikipedia.org/wiki/MD5" title="wikilink">MD5</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/디지털_서명_알고리즘" title="wikilink">DSA</a>/<a href="https://ko.wikipedia.org/wiki/SHA-1" title="wikilink">SHA-1</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>RSA/SHA-1</p></td>
<td><p>RFC 3110</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>RSASHA1-NSEC3-SHA1</p></td>
<td><p>RFC 5155</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td><p>RSA/<a href="https://ko.wikipedia.org/wiki/SHA-2" title="wikilink">SHA-2</a>56</p></td>
<td><p>RFC 5702</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>10</p></td>
<td><p>RSA/<a href="https://ko.wikipedia.org/wiki/SHA-2" title="wikilink">SHA-512</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>12</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/GOST" title="wikilink">GOST</a> <a href="https://ko.wikipedia.org/wiki/GOST" title="wikilink">R 34.10-2001</a></p></td>
<td><p>RFC 5933</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>13</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/ECDSA" title="wikilink">ECDSA</a>/<a href="https://ko.wikipedia.org/wiki/SHA-2" title="wikilink">SHA-2</a>56</p></td>
<td><p>RFC 6605</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p>ECDSA/<a href="https://ko.wikipedia.org/wiki/SHA-2" title="wikilink">SHA-384</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 역사

DNS가 중요한 인터넷 서비스의 하나이지만, 1990년에 [스티브 벨로빈은](https://ko.wikipedia.org/wiki/스티브_M._벨로빈 "wikilink") 그 안에서 심각한 보안 결함을 발견하였다. 이에 대한 연구가 시작되었고, 그의 논문이 1995년 공개되면서 점차 연구가 증진되기 시작했다.\[1\] 초기 RFC 2065가 1997년 IETF에 의해 출판되었고 이러한 사양을 구현하려는 초기 시도가 IETF RFC 2535로서 1999년의 개정판으로 이어졌다. RFC 2535에 기반한 DNSSEC를 배치할 계획이 세워졌다.

## IETF 표준

  - RFC 2535 Domain Name System Security Extensions
  - RFC 3833 A Threat Analysis of the Domain Name System
  - RFC 4033 DNS Security Introduction and Requirements (*DNSSEC-bis*)
  - RFC 4034 Resource Records for the DNS Security Extensions (*DNSSEC-bis*)
  - RFC 4035 Protocol Modifications for the DNS Security Extensions (*DNSSEC-bis*)
  - RFC 4398 Storing Certificates in the Domain Name System (DNS)
  - RFC 4470 Minimally Covering NSEC Records and DNSSEC On-line Signing
  - RFC 4509 Use of SHA-256 in DNSSEC Delegation Signer (DS) Resource Records (RRs)
  - RFC 5155 DNSSEC Hashed Authenticated Denial of Existence
  - RFC 6781 DNSSEC Operational Practices, Version 2

## 각주

## 외부 링크

  - [DNSSEC](http://www.dnssec.net/) - DNSSEC information site: DNSSEC.net

[DNSSEC](https://ko.wikipedia.org/wiki/분류:DNSSEC "wikilink") [분류:인터넷 표준](https://ko.wikipedia.org/wiki/분류:인터넷_표준 "wikilink") [분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:도메인 네임 시스템](https://ko.wikipedia.org/wiki/분류:도메인_네임_시스템 "wikilink") [분류:공개 키 암호](https://ko.wikipedia.org/wiki/분류:공개_키_암호 "wikilink")

1.  ["Using the Domain Name System for System Break-Ins"](http://citeseer.ist.psu.edu/bellovin95using.html) by Steve Bellovin, 1995