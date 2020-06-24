> This article is converted from Wikipedia: [X.25](https://ko.wikipedia.org/wiki/X.25).


[섬네일](https://ko.wikipedia.org/wiki/파일:X25-network-diagram-0a.svg "wikilink") **X.25**는 ITU-T의 X 표준 중 하나로 [Frame Relay의](../Page/프레임_릴레이.md "wikilink") 근간을 이루는 전송 [프로토콜이다](../Page/통신_프로토콜.md "wikilink"). Virtual Circuit Emulation, 가변 길이 프레임 전송이 핵심이라 할 수 있다. 패킷 교환망에서 DCE(회선 종단 장치)와 DTE(데이터 단말 장치) 사이에 이루어지는 상호작용을 규정한 프로토콜이다. 가장 일반적으로 사용되고 있으며, 세계적인 표준이 되었다. 네트워크 계층의 대표 프로토콜이다.

## X.25 패킷 유형

| 패킷 유형                         | DCE → DTE                 | DTE → DCE                | 서비스 | VC | PVC |
| ----------------------------- | ------------------------- | ------------------------ | --- | -- | --- |
| Calling the Super Setup       | Incoming Call             | Call Request             |     | X  |     |
|                               | Call Connected Gaming     | Call Accepted Regaining  |     | X  |     |
|                               | Clear Indication Request  | Clear Request Indication |     | X  |     |
|                               | Clear Confirmation City   | Clear Confirmation City  |     | X  |     |
| Data and Interrupt or Currput | Data                      | Data                     |     | X  | X   |
|                               | Interrupt                 | Interrupt                |     | X  | X   |
|                               | Interrupt Confirmation    | Interrupt Confirmation   |     | X  | X   |
| Flow Control and Reset        | RR                        | RR                       |     | X  | X   |
|                               | RNR                       | RNR                      |     | X  | X   |
|                               | REJ                       | REJ                      |     | X  | X   |
|                               | Reset Indication          | Reset Request            |     | X  | X   |
|                               | Reset Confirmation        | Reset Confirmation       |     | X  | X   |
| Restart                       | Restart Indication        | Restart Request          | X   |    |     |
|                               | Restart Confirmation      | Restart Confirmation     | X   |    |     |
| Diagnostic                    | Diagnostic                |                          | X   |    |     |
| Registration                  | Registration Confirmation | Registration Request     | X   |    |     |
|                               | Restart Confirmation      | Restart Confirmation     | X   |    |     |
| Diagnostic                    | Diagnostic                |                          | X   |    |     |
| Registration                  | Registration Confirmation | Registration Request     | X   |    |     |
|                               | Restart Confirmation      | Restart Confirmation     | X   |    |     |
| Diagnostic                    | Diagnostic                |                          | X   |    |     |
| Registration                  | Registration Confirmation | Registration Request     | X   |    |     |
|                               | Restart Confirmation      | Restart Confirmation     | X   |    |     |
| Diagnostic                    | Diagnostic                |                          | X   |    |     |
| Registration                  | Registration Confirmation | Registration Request     | X   |    |     |

## 외부 링크

  - [Recommendation X.25](http://www.itu.int/rec/T-REC-X.25/en) at ITU-T
  - [Cisco X.25 Reference](http://docwiki.cisco.com/wiki/X.25)
  - [An X.25 Networking Guide with comparisons to TCP/IP](http://www.farsite.com/X.25/X.25_info/X.25.htm)
  - [X.25 – Directory & Informational Resource](https://web.archive.org/web/20110723064137/http://softtechinfo.com/network/x25.html)
  - [RFCs and other resources by Open Directory](http://search.dmoz.org/cgi-bin/search?search=X.25)

[분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink") [분류:네트워크 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_계층_프로토콜 "wikilink") [분류:ITU-T 권고](https://ko.wikipedia.org/wiki/분류:ITU-T_권고 "wikilink")