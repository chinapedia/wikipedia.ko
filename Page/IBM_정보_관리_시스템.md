> This article is converted from Wikipedia: [IBM   ](https://ko.wikipedia.org/wiki/IBM___).


**IBM 정보 관리 시스템**(IBM Information Management System, IMS)은 방대한 [트랜잭션 처리](https://ko.wikipedia.org/wiki/트랜잭션_처리 "wikilink") 기능을 갖춘 결합형 [계층형 데이터베이스이자](https://ko.wikipedia.org/wiki/계층형_모델 "wikilink") [정보 관리](https://ko.wikipedia.org/wiki/정보_관리 "wikilink") 시스템이다.

## 역사

[IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")은 [아폴로 계획을](https://ko.wikipedia.org/wiki/아폴로_계획 "wikilink") 위해 1966년부터 [로크웰과](https://ko.wikipedia.org/wiki/로크웰_인터내셔널 "wikilink") [캐터필러](https://ko.wikipedia.org/wiki/캐터필러 "wikilink")와 함께 IMS를 설계하였으며, [새턴 V](https://ko.wikipedia.org/wiki/새턴_V "wikilink") 달 로켓과 아폴로 우주선의 매우 큰 [자재 명세서의](https://ko.wikipedia.org/wiki/자재_명세서 "wikilink") 목록을 만드는데 사용되었다.

최초의 "IMS READY" 메시지가 1968년 8월 14일 [캘리포니아주](https://ko.wikipedia.org/wiki/캘리포니아주 "wikilink") [다우니의](https://ko.wikipedia.org/wiki/다우니_\(캘리포니아주\) "wikilink") [IBM 2740](https://ko.wikipedia.org/wiki/IBM_2741 "wikilink") 터미널에 나타났다.\[1\] 그 와중에 IMS는 IBM [시스템/360](https://ko.wikipedia.org/wiki/시스템/360 "wikilink") 기술이 현재의 [z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink")와 [시스템 z9](https://ko.wikipedia.org/wiki/IBM_시스템_z9 "wikilink"), [z10](https://ko.wikipedia.org/wiki/IBM_시스템_z10 "wikilink") 기술로 진화하면서 수많은 발전을 겪었다. 이를테면 IMS는 현재 [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink"), [JDBC](https://ko.wikipedia.org/wiki/JDBC "wikilink"), [XML](https://ko.wikipedia.org/wiki/XML "wikilink")를, 그리고 2005년 말부터는 [웹 서비스를](https://ko.wikipedia.org/wiki/웹_서비스 "wikilink") 지원하고 있다.

번 와츠(Vern Watts)는 수년 동안 IMS의 수석 설계자였다. 와츠는 1956년 IBM에 입사하여 IBM의 실리콘 밸리 개발 연구소에서 그가 죽은 2009년 4월 4일까지 일하였다.\[2\] 그는 1960년대 이후로 IMS에 계속 일했었다.\[3\]

## 데이터베이스

IMS DB 구성 요소는 [계층형 모델을](https://ko.wikipedia.org/wiki/계층형_모델 "wikilink") 이용하여 데이터를 저장하며, 이는 그 뒤에 나온 IBM의 [관계형 데이터베이스](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink") [DB2와는](https://ko.wikipedia.org/wiki/IBM_DB2 "wikilink") 상당히 다르다. IMS에서 계층형 모델은 세그먼트라는 이름의 데이터 블록을 이용하여 구현된다. 각 세그먼트는 여러 조각의 데이터를 포함할 수 있는데, 이를 필드로 부른다. 이를테면 고객 데이터베이스는 전화번호, 이름, 나이와 같은 필드가 있는 루트 세그먼트(해당 계층의 최상위에 있는 세그먼트)를 가질 수 있다. 차일드 세그먼트를 다른 세그먼트 아래에 추가할 수도 있다. 다른 데이터베이스와는 달리 IMS에 세그먼트 내의 모든 데이터를 정의할 필요는 없다. 세그먼트는 40바이트의 크기로 정의할 수 있으나 하나의 필드에는 키 필드로서 6바이트만큼만 정의하며 이는 쿼리 수행 시 세그먼트를 찾기 위해서 존재한다. IMS는 프로그램에 의해 지시된대로 40바이트만큼을 검색하고 저장하지만 그 밖의 다른 바이트들이 무엇을 대표하는지에는 큰 관심을 두지 않는다. 실제로 세그먼트 내의 모든 데이터는 [코볼](https://ko.wikipedia.org/wiki/코볼 "wikilink") 카피북에 매핑할 수 있다. [DL/I](https://ko.wikipedia.org/wiki/DL/I "wikilink") 쿼리를 사용하는 일뿐 아니라, 필드를 IMS 안에 정의하여 데이터가 보안을 이유로 특정 응용 프로그램으로부터 보이지 않게 할 수 있다. IMS DB의 구성 요소는 트랜잭션 매니저 구성 요소 없이 별개로 구매가 가능하며 [CICS](../Page/CICS.md "wikilink")와 같은 시스템에 사용할 수 있다.

IMS 계층형 데이터베이스에는 다음의 3가지 기본 형태가 있다:

  - 풀 펑션(Full Function) 데이터베이스
  - 패스트 패스(Fast Path) 데이터베이스
  - HALDB(High Availability Large Databases)

## 트랜잭션 매니저

IMS는 IMS DC 또는 IMS TM라는 이름의 [트랜잭션 매니저이며](https://ko.wikipedia.org/wiki/트랜잭션_처리 "wikilink"), [CICS](../Page/CICS.md "wikilink"), [BEA 턱시도](https://ko.wikipedia.org/wiki/턱시도_\(소프트웨어\) "wikilink")(현재는 오라클 소유)와 함께 전통적인 3대 트랜잭션 매니저 가운데 하나이다. 트랜잭션 매니저는 최종 사용자나 다른 응용 프로그램과 상호 작용하고 비즈니스 명령을 처리하며 프로세스를 통한 상태를 관리하여 시스템이 비즈니스 명령을 올바르게 데이터 스토어에 기록할 수 있게 한다. 그러므로 IMS TM은 마치 [CGI](https://ko.wikipedia.org/wiki/공용_게이트웨이_인터페이스 "wikilink") 프로그램을 통해 동작하는 웹 애플리케이션과 매우 비슷하며, 데이터베이스를 조회하거나 업데이트하는 인터페이스를 제공한다.

## 응용 프로그램

IMS 이전에 기업체와 정부는 자신들만의 트랜잭션 처리 환경을 작성하여야 했다. IMS TM은 고성능의 트랜잭션 실행을 위해 직관적이고 사용하기 쉬우며 신뢰할만한 표준 환경을 제공한다.

오늘날 IMS는 1982년에 선보인 IBM의 [관계형 데이터베이스](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink") 시스템인 [DB2를](https://ko.wikipedia.org/wiki/IBM_DB2 "wikilink") 보완한다. 일반적으로 IMS는 공통 작업들에 대해서는 DB2 보다 더 빠르게 수행하지만 중요도가 없는 일에 대해 설계하고 유지 보수를 하는데 프로그래밍의 수고가 더 많이 들어간다.

## 같이 보기

  - [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink")
  - [IBM DB2](https://ko.wikipedia.org/wiki/IBM_DB2 "wikilink")

## 각주

<references />

## 외부 링크

  - [IMS Family - IBM Software](http://www-306.ibm.com/software/data/ims/index.html)

  - [Information Management Software for z/OS Solutions Information Center](https://web.archive.org/web/20140105210332/http://publib.boulder.ibm.com/infocenter/dzichelp/v2r2/index.jsp)

  - [IBM Redbook: IMS Primer](http://www.redbooks.ibm.com/redbooks/pdfs/sg245352.pdf)

  -

  - [IBM InfoSphere Guardium S-TAP for IMS on z/OS for detection of policy violations and compliance auditing](http://www-01.ibm.com/software/data/guardium/)

  - [An Introduction to IMS: Second Edition](http://www.ibmpressbooks.com/bookstore/product.asp?isbn=0132887010)

[분류:아폴로 계획](https://ko.wikipedia.org/wiki/분류:아폴로_계획 "wikilink") [분류:데이터베이스 엔진](https://ko.wikipedia.org/wiki/분류:데이터베이스_엔진 "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:IBM 메인프레임 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM_메인프레임_운영_체제 "wikilink") [분류:NoSQL](https://ko.wikipedia.org/wiki/분류:NoSQL "wikilink")

1.
2.  IBM IMS Newsletter *[Volume 902](http://publib.boulder.ibm.com/infocenter/dzichelp/v2r2/topic/com.ibm.imsnews2.doc/newsletters/v902/v902.htm)*
3.  Luongo, Chris et al. (October 2008). *[The Tale of Vern Watts](https://www.youtube.com/watch?v=x98hgieE08o)*. International Business Machines Corporation. Retrieved on April 7, 2009.