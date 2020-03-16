> This article is converted from Wikipedia: [IDMS](https://ko.wikipedia.org/wiki/IDMS).


**IDMS**(Integrated Database Management System, 통합 데이터베이스 관리 시스템)는 [메인프레임](../Page/메인프레임.md "wikilink")을 위한 [네트워크](../Page/네트워크_모델.md "wikilink") ([CODASYL](../Page/CODASYL.md "wikilink")) [데이터베이스 관리 시스템이다](../Page/데이터베이스_관리_시스템.md "wikilink"). [B.F. 굿리치가](https://ko.wikipedia.org/wiki/굿리치 "wikilink") 처음 개발하였으며, 나중에 컬리난 데이터베이스 시스템스(Cullinane Database Systems, 1983년에는 [컬리넷](https://ko.wikipedia.org/wiki/컬리넷 "wikilink")으로 사명 변경)가 시장에 출시하였다. 1989년 이후로 이 제품은 [CA 테크놀로지스가](../Page/CA_테크놀로지스.md "wikilink") 소유하고 있으며, 어드밴티지 CA-IDMS로 제품명이 바뀌었다가, 나중에는 간단히 **CA IDMS**로 변경되었다.

## 역사

IDMS의 뿌리는 1964년 처음 출시된, [제너럴 일렉트릭의](../Page/제너럴_일렉트릭.md "wikilink") [찰스 바크만](../Page/찰스_바크만.md "wikilink") 주도 팀이 개발한 [통합 데이터 스토어](https://ko.wikipedia.org/wiki/통합_데이터_스토어 "wikilink")(IDS)라는 선구적인 [데이터베이스 관리 시스템으로](../Page/데이터베이스_관리_시스템.md "wikilink") 거슬러 올라간다.\[1\]

## 통합 데이터 사전

통합 [데이터 사전](https://ko.wikipedia.org/wiki/데이터_사전 "wikilink")(IDD, Integrated Data Dictionary)은 IDMS의 복잡한 기능들 가운데 하나이다. IDD는 주로 데이터베이스 정의들을 관리할 목적으로 개발되었다. IDD는 IDMS 데이터베이스 그 자체이다.

데이터베이스 관리자들과 그 밖의 사용자들은 DDDL(데이터 사전 정의 언어, Data Dictionary Definition Language)를 이용하여 IDD에 접속하였다.

또, IDD는 ADS/온라인, IDMS-DC와 같은 IDMS 계열의 다른 제품들에 정의와 코드를 저장하는 목적으로도 사용되었다.

IDD는 확장이 가능하므로 무엇이든 간에 이에 대한 정의들을 만드는 목적으로 사용될 수 있다는 강점이 있다. 일부 기업들은 이를 이용하여 사내 문서를 개발한다.

## 출시 역사 (CA)

| 출시 버전 | 출시일             | 주요 기능                                                                                                                                                                                                         |
| ----- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| R12   | 1992            | 24시간 처리, 논리·물리 분리, 카탈로그 관리, [교착 상태](../Page/교착_상태.md "wikilink") 관리, 중앙에서 관리되는 보안 기능, [SQL](../Page/SQL.md "wikilink")                                                                                        |
| R14   | 1999-01-09\[2\] | [병렬 시스플렉스](https://ko.wikipedia.org/wiki/IBM_병렬_시스플렉스 "wikilink") 활용, 멀티태스킹                                                                                                                                   |
| R15   | 2001-04-25\[3\] | 성능 개선, 데이터 공유                                                                                                                                                                                                 |
| R16   | 2004-04-13\[4\] | [2단계 커밋](../Page/2단계_커밋_프로토콜.md "wikilink"), [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink"), [병렬 접근 볼륨](https://ko.wikipedia.org/wiki/장치_제어_블록 "wikilink") 활용, [XML](../Page/XML.md "wikilink") 출판 |
| R17   | 2008-10-30\[5\] | 성능 개선, [zIIP](https://ko.wikipedia.org/wiki/zIIP "wikilink") 지원, 자동 복구 기능 개선\[6\]                                                                                                                             |
| R18   | 2011-06-02      | zIIP 지원 강화, 자동 시스템 튜닝, 성능 개선, 단순화된 설치 및 유지보수                                                                                                                                                                  |

## 같이 보기

  - CA [데이터콤/DB](https://ko.wikipedia.org/wiki/데이터콤/DB "wikilink")
  - IBM [정보 관리 시스템](https://ko.wikipedia.org/wiki/정보_관리_시스템 "wikilink")

## 각주

<references />

## 외부 링크

  - [CA IDMS](http://www.ca.com/us/products/detail/CA-IDMS.aspx)

  - [IDMS Public Discussion Forum](http://ibmmainframes.com/forum-15.html)

  - [CA-IDMS & ADS Application Developers & DBAs LinkedIn Group](http://www.linkedin.com/groups?mostPopular=&gid=682797)

[분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink")

1.
2.  [findarticles.com](http://findarticles.com/p/articles/mi_m0EIN/is_1997_Jan_9/ai_19008506/)
3.  [Computer Associates announces CA-IDMS release 15.0 for OS390 and zOS Advanced availability and scalability features support increased customer demands for eBusiness transactions...](http://www.highbeam.com/doc/1G1-73634540.html)
4.  [CAs Advantage CA-IDMS Database r16 for zOS Optimizes Performance Ease of Use and Flexibility BTs 1.7 Terabyte Customer Database Processes 10 Billion Transactions Annually With...](http://www.highbeam.com/doc/1G1-131523758.html)
5.  [CA IDMS r17 exploits zIIP engine to deliver greater capacity Latest database release highlights CAs leadership in utilization of IBM mainframe specialty processors Enhanced ar...](http://www.highbeam.com/doc/1G1-188076001.html)
6.  <http://www.ca.com/~/media/Files/productbriefs/idms_db_ps_190116.pdf>