> This article is converted from Wikipedia: [ISCSI](https://ko.wikipedia.org/wiki/ISCSI).


**iSCSI**(Internet Small Computer System Interface)는 컴퓨팅 환경에서 데이터 스토리지 시설을 이어주는 [IP](../Page/인터넷_프로토콜.md "wikilink") 기반의 스토리지 네트워킹 표준이다. iSCSI는 IP 망을 통해 [SCSI](../Page/SCSI.md "wikilink") 명령을 전달함으로써 인트라넷을 거쳐 데이터 전송을 쉽게 하고 먼 거리에 걸쳐 스토리지를 관리하는 데 쓰인다. iSCSI는 근거리 통신망과 원거리 통신망, 아니면 인터넷을 통해 데이터를 전송하는 데 쓰이며 위치에 영향을 받지 않는 데이터 보관과 복구를 사용할 수 있게 한다.

특수 목적의 케이블링을 요구하는 전통적인 [파이버 채널과](../Page/파이버_채널.md "wikilink") 달리 iSCSI는 기존의 네트워크 인프라를 사용하여 먼 거리에 걸쳐 운영할 수 있다.

## 운영 체제 지원

| 운영 체제                                                                | 첫 공개일     | 버전                                             | 기능                                                                                                       |
| -------------------------------------------------------------------- | --------- | ---------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| [i5/OS](https://ko.wikipedia.org/wiki/IBM_i5/OS "wikilink")          | 2006년 10월 | i5/OS V5R4M0                                   | Target, Multipath                                                                                        |
|                                                                      |           |                                                |                                                                                                          |
| [VMware ESX](https://ko.wikipedia.org/wiki/VMware_ESX_서버 "wikilink") | 2006년 06월 | ESX 3.5.0                                      | Initiator, Multipath                                                                                     |
|                                                                      |           |                                                |                                                                                                          |
| [AIX](https://ko.wikipedia.org/wiki/AIX_운영_체제 "wikilink")            | 2002년 10월 | AIX 5.3 TL10 , AIX 6.1 TL3                     | Target, Initiator                                                                                        |
| [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink")            | 2003년 6월  | 2000, XP 프로, 2003, 비스타, 2008, 2008 R2, 7,8,8.1 | Initiator, Target†, Multipath                                                                            |
| [넷웨어](https://ko.wikipedia.org/wiki/노벨_넷웨어 "wikilink")               | 2003년 8월  | NetWare 5.1, 6.5, & OES                        | Initiator, Target                                                                                        |
| [HP-UX](../Page/HP-UX.md "wikilink")                                 | 2003년 10월 | HP 11i v1, HP 11i v2, HP 11i v3                | Initiator                                                                                                |
| [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_운영_체제 "wikilink")          | 2005년 2월  | 솔라리스 10, 오픈솔라리스                                | Initiator, Target, Multipath, [iSER](https://ko.wikipedia.org/wiki/ISCSI_Extensions_for_RDMA "wikilink") |
| [리눅스](../Page/리눅스.md "wikilink")                                     | 2005년 6월  | 2.6.12                                         | Initiator, Target, Multipath, [iSER](https://ko.wikipedia.org/wiki/ISCSI_Extensions_for_RDMA "wikilink") |
| [NetBSD](../Page/NetBSD.md "wikilink")                               | 2006년 2월  | 4.0, 5.0                                       | Initiator (5.0), Target (4.0)                                                                            |
| [프리BSD](https://ko.wikipedia.org/wiki/프리BSD "wikilink")              | 2008년 2월  | 7.0                                            | Initiator, Target from NetBSD                                                                            |
| [오픈VMS](https://ko.wikipedia.org/wiki/오픈VMS "wikilink")              | 2008년 2월  | 8.3-1H1                                        | Initiator, Multipath                                                                                     |
|                                                                      |           |                                                |                                                                                                          |

†Target은 윈도 통합 데이터 스토리지 서버 (WUDSS)의 일부로만 사용할 수 있다.

## 같이 보기

  - [하이퍼SCSI](https://ko.wikipedia.org/wiki/하이퍼SCSI "wikilink")

## 외부 링크

  - [솔라리스 iSCSI 스택 살펴보기](http://prefetch.net/new/solarisiscsi.html)
  - [iSCSI 기술의 마이크로소프트 포털 사이트](http://www.microsoft.com/windowsserver2003/technologies/storage/iscsi/default.mspx)

### RFC

  - RFC 3720
  - RFC 3721
  - RFC 3722
  - RFC 3723
  - RFC 3347
  - RFC 3783
  - RFC 3980
  - RFC 4018
  - RFC 4173
  - RFC 4544
  - RFC 4850
  - RFC 4939
  - RFC 5048
  - RFC 5047
  - RFC 5046

[분류:이더넷](https://ko.wikipedia.org/wiki/분류:이더넷 "wikilink")