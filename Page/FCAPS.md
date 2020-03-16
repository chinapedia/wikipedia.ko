> This article is converted from Wikipedia: [FCAPS](https://ko.wikipedia.org/wiki/FCAPS).


**FCAPS**는 [네트워크 관리를](https://ko.wikipedia.org/wiki/네트워크_관리 "wikilink") 위한 [ISO](../Page/국제_표준화_기구.md "wikilink") [통신 관리망](https://ko.wikipedia.org/wiki/통신_관리망 "wikilink") 모델이자 프레임워크이다. FCAPS는 고장, 구성, 회계, 성능, 보안(fault, configuration, accounting, performance, security)의 준말이다. 청구를 하지 않는 조직에서 "회계"는 "관리"(adimistration)로 대체하기도 한다.

## 역사

1980년대 초, FCAPS라는 용어가 [개방형 시스템 간 상호 접속](../Page/개방형_시스템_간_상호_접속.md "wikilink") 시스템 관리 개요(OSI SMO) 표준인 ISO 10040의 최초 워킹 드래프트 (N1719)에 도입되었다. 당시 의도는 5개의 구별된 프로토콜 표준을 기능별로 정의하는 것이었다. 초기 경험에 따르면 이 프로토콜들은 매우 유사하기 때문에 이 프로토콜들의 개발을 책임지는 ISO 워킹 그룹(ISO/TC97/SC16/WG4, 나중에는 ISO-IEC/JTC1/SC21/WG4으로 이름이 변경됨)은 대신 5개의 전 분야에 대해 하나의 프로토콜을 만들기로 결정하였다. 이 프로토콜은 [CMIP](https://ko.wikipedia.org/wiki/CMIP "wikilink")(common management information protocol)로 불린다. 1990년대 [통신 관리망](https://ko.wikipedia.org/wiki/통신_관리망 "wikilink")(TMN)의 작업 중 일부로서 ITU-T는 더 나아가 FCAPS를 TMN 관리 기능 권고안(M.3400)의 일부로 다듬었다. FCAPS의 개념은 네트워크 관리 기능을 교육하는 데 유용한 것으로 밝혀졌다. 이로써 대부분의 교과서는 FCAPS를 설명하는 구문으로 시작하게 된다.

## 모델의 5가지 기능

OSI 네트워크 관리 모델은 5가지 기능을 분류하며 이를 FCAPS 모델로도 부른다.

**FCAPS 및 ISO (FAB) 모델**

| FCAPS         | FAB         |
| ------------- | ----------- |
| Fault         | Assurance   |
| Configuration | Fulfillment |
| Accounting    | Billing     |
| Performance   | Assurance   |
| Security      | Fulfillment |

## 네트워크 관리국

네트워크 관리 모델 용어로서 **네트워크 관리국**(, NMS)은 호스트, 게이트웨이, 터미널 서버 등의 [네트워크 요소](https://ko.wikipedia.org/wiki/네트워크_요소 "wikilink")(NE)들을 감시하고 통제하는 [네트워크 관리 애플리케이션](https://ko.wikipedia.org/wiki/네트워크_관리_애플리케이션 "wikilink")(NMA)를 실행하는 주체이다. 이 네트워크 요소들은 [관리 에이전트](https://ko.wikipedia.org/wiki/관리_에이전트 "wikilink")(management agent, MA)를 사용하여 네트워크 관리국이 요청한 네트워크 관리 기능들을 수행한다. [간이 망 관리 프로토콜](../Page/간이_망_관리_프로토콜.md "wikilink")(SNMP)을 사용하여 네트워크 관리국들과 네트워크 요소 안의 에이전트들 간의 관리 정보를 통신한다. NMS는 RFC 1157 "A Simple Network Management Protocol"에 기술되어 있다.

NMS는 모든 망에 FCAPS 기능을 제공한다. FCAPS: Fault, Configuration, Accounting, Performance, Security는 ISO 모델에 의해 정의되는 분류들이다.

## 내용주

  - [Cisco Internetworking Technology Handbook](http://docwiki.cisco.com/wiki/Internetworking_Technology_Handbook)
  - [ISO/IEC 7498-4: Information processing systems -- Open Systems Interconnection -- Basic Reference Model -- Part 4: Management framework](http://standards.iso.org/ittf/PubliclyAvailableStandards/s014258_ISO_IEC_7498-4_1989\(E\).zip)

## 같이 보기

  - [네트워크 관리 시스템](../Page/네트워크_관리_시스템.md "wikilink")

## 참고문헌

  - ISO/IEC 10040, 1998, "Information technology - Open Systems Interconnection - Systems management overview" (available as <http://www.itu.int/rec/T-REC-X.701-199708-I>)
  - ITU-T, 1996, "M.3010 Principles for a telecommunications management network"
  - ITU-T, 1997, "M.3400 TMN management functions"
  - ITU-T, "M.3050 Enhanced Telecom Operations Map (eTOM) – The business process framework"

## 외부 링크

  - [FCAP Basics](http://www.solarwinds.com/network-monitoring-design-philosophy.aspx#step_2)
  - [SNMP Center](https://web.archive.org/web/20151122005332/http://snmpcenter.com/category/nms/)
  - [SNMP OID List](https://opmantek.com/network-management-system-nmis-supported-vendors-snmp.html)
  - [ISO](http://www.iso.org/)

[분류:네트워크 관리](https://ko.wikipedia.org/wiki/분류:네트워크_관리 "wikilink")