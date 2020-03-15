> This article is converted from Wikipedia: [MIL-STD-498](https://ko.wikipedia.org/wiki/MIL-STD-498).


**MIL-STD-498** (Military-Standard-498)은 미국의 군사 표준규격이었으며, "소프트웨어 개발과 문서화 요건을 수립"하기 위한 목적으로 만들어졌다. 이 표준 규격은 1994년 11월 8일 공표되었으며, 기존의 표준규격인 [DOD-STD-2167A](https://ko.wikipedia.org/wiki/DOD-STD-2167A "wikilink"), [DOD-STD-7935A](https://ko.wikipedia.org/wiki/DOD-STD-7935A "wikilink"), 그리고 [DOD-STD-1703](https://ko.wikipedia.org/wiki/DOD-STD-1703 "wikilink")을 대체하여 적용되었다. 그리고 상용 표준이 만들어지는 동안 2년 동안 잠정적인 표준으로 적용되었다.

이 표준규격은 1998년 5월 27일 [J-STD-016](https://ko.wikipedia.org/wiki/J-STD-016 "wikilink")과 [IEEE 12207로](https://ko.wikipedia.org/wiki/IEEE_12207 "wikilink") 대체되어 효력을 상실했다. [한국](https://ko.wikipedia.org/wiki/한국 "wikilink")을 포함하여 미국이 아닌 다른 나라에서는 여전히 이 표준 규격을 따르는 경우가 있는데, 그 이유는 새로운 표준규격에 비해 MIL-STD-498이 자유롭게 공개되어 있어, 더욱 익숙하고 이익을 가져다준다고 판단되었기 때문이다.

## 데이터 아이템 기술(Data Item Descriptions)

표준규격의 주요 구성요소는 22개의 데이터 아이템 기술(DIDs)이다. 각 DID는 요구되는 **데이터 아이템**의 내용을 기술한 것으로, 소프트웨어 또는 소프트웨어 생명주기의 특정 단계를 기술한 "문서"가 된다. 이 문서들은 소프트웨어 코드에서부터 다양한 전자 또는 종이 보고서 등 여러 형태가 될 수 있다. 그리고 계약 당사자들은 정의된 인정 범위 내에서 결과물의 형태를 지정해야 한다. 그리고 이들 데이터 아이템이 모여져서 계약에 의한 납품 목록을 구성하게 된다. 프로젝트의 성격에 따라, 일부 데이터 아이템만 요구되는 경우도 있을 수 있다.

정의되어 있는 DID 목록은 다음과 같다.

  - **소프트웨어 개발 계획서(Software Development Plan)** (SDP) - 소프트웨어 개발을 수행하기 위한 계획
  - **소프트웨어 테스트 계획서(Software Test Plan)** (STP) - 소프트웨어 테스트를 수행하기 위한 계획
  - **소프트웨어 설치 계획서(Software Installation Plan)** (SIP) - 실제 사용자의 소프트웨어 설치를 위한 계획
  - **소프트웨어 이전 계획서(Software Transition Plan)** (STrP) - 지원 조직으로의 소프트웨어 이전을 위한 계획
  - **운영 개념 기술서(Operational Concept Description)** (OCD) - 시스템 운영시의 개념을 기술
  - **시스템/서브시스템 명세서(System/Subsystem Specification)** (SSS) - 시스템이 만족해야할 요구사항을 정의
  - **소프트웨어 요구사항 명세서(Software Requirements Specification)** (SRS) - CSCI가 만족해야할 요구사항을 정의
  - **인터페이스 요구사항 명세서(Interface Requirements Specification)** (IRS) - 하나 또는 다수의 인터페이스에 대한 요구사항을 정의
  - **시스템/서브시스템 설계 기술서(System/Subsystem Design Description)** (SSDD) - 시스템 설계
  - **소프트웨어 설계 기술서(Software Design Description)** (SDD) - CSCI 설계
  - **인터페이스 설계 기술서(Interface Design Description)** (IDD) - 하나 또는 다수의 인터페이스 설계
  - **데이터베이스 설계 기술서(Database Design Description)** (DBDD) - 데이터베이스 설계
  - **소프트웨어 테스트 기술서(Software Test Description)** (STD) - 테스트를 위한 데스트 케이스 및 과정을 기술
  - **소프트웨어 테스트 보고서(Software Test Report)** (STR) - 테스트 결과 보고
  - **소프트웨어 제품 기술서(Software Product Specification)** (SPS) - 실행가능한 소프트웨어, 소스코드, 지원을 위한 정보
  - **소프트웨어 버전 기술서(Software Version Description)** (SVD) - 납품 파일 목록과 관련 정보
  - **소프트웨어 사용자 매뉴얼(Software User Manual)** (SUM) - 소프트웨어 사용자를 위한 매뉴얼
  - **소프트웨어 입출력 매뉴얼(Software Input/Output Manual)** (SIOM) - 컴퓨터 센터에 설치되는 배치/상호작용 소프트웨어의 사용자를 위한 매뉴얼
  - **소프트웨어 센터 운영자 매뉴얼(Software Center Operator Manual)** (SCOM) - 컴퓨터 센터에 설치되는 배치/상호작용 소프트웨어의 운영자를 위한 매뉴얼
  - **컴퓨터 운영 매뉴얼(Computer Operation Manual)** (COM) - 컴퓨터를 운영하기 위한 지침
  - **컴퓨터 프로그래밍 매뉴얼(Computer Programming Manual)** (CPM) - 컴퓨터를 프로그래밍 하기 위한 지침
  - **펌웨어 지원 매뉴얼(Firmware Support Manual)** (FSM) - 펌웨어 장치를 프로그래밍 하기 위한 지침

## 외부 링크

  - [MIL-STD-498 PDF 문서](http://www.abelia.com/498pdf/roadmap.pdf)
  - [The MIL-STD-498 표준규격 HTML](https://web.archive.org/web/20080703211729/http://www.pogner.demon.co.uk/mil_498/)
  - [MIL-STD-498 요약](https://web.archive.org/web/20100531034813/http://www.stsc.hill.af.mil/crosstalk/1995/02/MILSTD.asp)

[분류:미국 군사규격](https://ko.wikipedia.org/wiki/분류:미국_군사규격 "wikilink") [분류:소프트웨어 문서화](https://ko.wikipedia.org/wiki/분류:소프트웨어_문서화 "wikilink")