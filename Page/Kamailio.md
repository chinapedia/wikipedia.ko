> This article is converted from Wikipedia: [Kamailio](https://ko.wikipedia.org/wiki/Kamailio).


이전 **OpenSER** (그리고 **SIP Express Router (SER)**와 일부 공통 이력을 공유하는)인 **Kamailio**는 [GNU General Public License에](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 따라 라이센스가 부여 된 [SIP](../Page/세션_개시_프로토콜.md "wikilink") 서버이다. SIP 등록자, 프록시 또는 리디렉션 서버로 작동하도록 구성 할 수 있으며 현재 지원하는 기능은 [RADIUS](../Page/RADIUS.md "wikilink") / [syslog](https://ko.wikipedia.org/wiki/syslog "wikilink") 계정 및 권한 부여, [XML-RPC](../Page/XML-RPC.md "wikilink") 및 [JSON-RPC](../Page/JSON-RPC.md "wikilink") 기반 원격 제어, [SQL](../Page/SQL.md "wikilink") 및 [NoSQL](../Page/NoSQL.md "wikilink") 백엔드, [IMS](../Page/IP_멀티미디어_서브시스템.md "wikilink") / [VoLTE](https://ko.wikipedia.org/wiki/VoLTE "wikilink") 확장 등이 있다.

> Kamailio는 하 와이어로 대화를 의미한다. "특별한 맛으로 선택되었다."\[1\]

## 기능

Kamailio는 아키텍처 별 최적화를 통해 순수 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 로 작성되었다.\[2\] 소규모 사무실 사용, 엔터프라이즈 [PBX](../Page/기업용_전화_시스템.md "wikilink") 교체 및 이동 통신사 서비스 (SIP 시그널링 서버, [프록시)](../Page/세션_개시_프로토콜.md "wikilink") 등 많은 실시간 통신 서비스에 사용되는 것을 포함하여 많은 시나리오에 맞게 구성 할 수 있다. 특징은 다음과 같다.\[3\]

  - SIP 전화 시스템
  - SIP로드 밸런서
  - SIP 보안 방화벽
  - 최소 비용 라우팅 엔진
  - IMS / VoLTE 플랫폼
  - 인스턴트 메시징 및 프레즌스 서비스
  - SIP IPv4-IPv6 게이트웨이
  - MSRP 릴레이
  - SIP-WebRTC 게이트웨이

## 용법

Kamailio는 대규모 [인터넷 서비스 제공 업체](../Page/인터넷_서비스_제공자.md "wikilink") 에서 공중 전화 서비스를 제공하는 데 사용된다. 독일 ISP *1 & 1* 에서는 수백만 명의 사용자를 대상으로 한 가장 큰 공개 발표가 진행되고 있다.\[4\] 공급자 sipgate 에서 또 다른 대규모 배포가 작동 중이다.

## 포크

### OpenSIPS

SER 및 OpenSER\[5\] 코드베이스에서 "자신의 방식으로 전환"하기로 결정한 SER 포크인 OpenSIPS로 [음성](../Page/음성_인터넷_프로토콜.md "wikilink") 텍스트 및 비디오 커뮤니케이션을 처리하는데 사용할 수있는 VoIP (Voice [over IP)](../Page/음성_인터넷_프로토콜.md "wikilink") 용 [SIP](../Page/세션_개시_프로토콜.md "wikilink") 의 [무료 소프트웨어를](../Page/자유_소프트웨어.md "wikilink") 구현한다. OpenSIPS는 수천 건의 전화를 제공하는 설치를 위해 고안되었고 [IETF](../Page/국제_인터넷_표준화_기구.md "wikilink") RFC 3261과 호환된다.\[6\] 이 소프트웨어는 2017 년 Google에서 오픈 소스 피어 보너스 상을 수상했다.\[7\]

## 역사

Kamailio의 뿌리는 **SIP Express Router (SER)** 의 첫 번째 줄이 쓰여 졌던 2001 년으로 거슬러 올라간다. 당시 실무 그룹은 [iptel.org에](https://web.archive.org/web/20200510223631/https://iptel.org/) 결과를 [공개했다.](https://web.archive.org/web/20200510223631/https://iptel.org/) 2002년 9월에 코드 자체가 [GPL](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 에 따라 공개되었다.\[8\] **SER** 의 첫 번째 포크는 2005년에 시작되었다 — **OpenSER**\[9\] — 나중에 **Kamailio** 가 될 코드로 다시 병합된다.\[10\] **SER** 과 **OpenSER** 의 코드베이스 (이후 **Kamailio**로 알려짐)는 2012년 12월에 수렴되었으며, **Kamailio** 를 프로젝트의 주요 이름으로 계속 사용하기로 결정했으며 오픈 소스로 남아 있다.\[11\]

개발 첫 해 동안 웹 기반 사용자 프로비저닝 인 *serweb* 을 사용할 수있었다.

### 타임 라인

[SIP 라우터 가족 역사](https://ko.wikipedia.org/wiki/파일:SER_SIP_router_family_history.svg "wikilink")

  - 2001 년

:\* **SIP Express Router (SER)**는 Fraunhofer Institute for Open Communication Systems (FOKUS)에서 처음 개발했다.

  - 2002

:\* 제 3 자 기여 ( ENUM 모듈)\[12\]

:; 구월

::\* **코드는 [GPL이며](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 최초 공개**\[13\]

  - 2003 년

:\* 일반 공개 적용이 시작된다. 추가적인 무료 및 오픈 소스 코드는 독립적 인 제 3자가 제공한다.\[14\]

  - 2004 년

:\* FOKUS 팀의 일부는 SER 저작권과 함께 새로 만든 회사 iptel.org로 이전한다.

:\* SER 핵심 개발자 5명 중 2명과 주요 기여자 1 명이 OpenSER이라는 새로운 [무료](../Page/자유_소프트웨어.md "wikilink") [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") 소프트웨어 프로젝트를 시작한다.

  - 2005 년

:\* IPtel.org는 Tekelec에 인수되었고, Tekelec 세션 라우터와 CSCF을 책임졌다.\[15\]

  - 2007 년

:; 5월 12일

::\* SER 2.0 [RC](../Page/소프트웨어_배포_생명_주기.md "wikilink") -1 (Ottendorf) 사용 가능

  - 2008 년

:; 8월

::\* 유사한 상표와의 충돌을 피하기 위해 **OpenSER의** 이름을 **Kamailio** 로 바꿈\[16\]

:; 11월 4일

::\* Kamailio 개발자는 SER 개발자와 협력하여 미래의 sip-router 프로젝트를 만들 계획을 발표하고 발표한다\[17\]

  - 2013 년

:\* FOKUS와 Kamailio 커뮤니티는 독일 베를린에서 연례 'Kamailio World'컨퍼런스의 첫 번째 반복을 조직한다.\[18\]

## 참고 문헌

[분류:자유 서버 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_서버_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.