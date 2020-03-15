> This article is converted from Wikipedia: [OSGi](https://ko.wikipedia.org/wiki/OSGi).


**OSGi**(Open Service Gateway initiative) Alliance는 [1999년](../Page/1999년.md "wikilink")에 [썬 마이크로시스템즈](../Page/썬_마이크로시스템즈.md "wikilink"), [IBM](../Page/IBM.md "wikilink"), [에릭손](../Page/에릭손.md "wikilink") 등이 구성한 개방형 표준 단체이다. (OSGi Alliance는 처음에 Connected Alliance라고 불렸음) 그 뒤 여러 해 동안 OSGi Alliance는 원격 관리 될 수 있는 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 기반의 서비스 플랫폼을 제정해왔다. 이 표준 사양의 핵심은 응용 프로그램의 생명주기(Life cycle) 모델과 서비스 레지스트리(Service Registry)를 정의하는 프레임워크(Framework)이다. OSGi 표준 사양에는 이 프레임워크에 기반하여 매우 다양한 OSGi 서비스가 정의되어 있다.

OSGi 프레임워크는 독립적인 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink")/[가상 머신](../Page/가상_머신.md "wikilink") 환경에서 제공하고 있지 않는 세련되고, 완전하며 동적인 SOA(Service Oriented Architecture) 기반의 [컴포넌트](https://ko.wikipedia.org/wiki/컴포넌트 "wikilink") 모델을 구현한다. 응용 프로그램 또는 구성 요소(번들, Bundle)는 재시동 과정 없이 원격지를 통해 설치(installed), 시작(started), 정지(stopped), 업데이트(updated) 그리고 제거(uninstalled)할 수 있다.

## OSGi 적용 분야

OSGi의 본래 적용 분야는 RG([Residential Gateway](https://ko.wikipedia.org/wiki/Residential_Gateway "wikilink")), 홈게이트웨이였으나 OSGi의 응용 가능성으로 인해 훨씬 폭넓고 다양한 분야에 적용 되고 있다. 현재 OSGi 표준 사양은 차세대 스마트폰 뿐만 아니라 [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink") IDE와 같은 데스크톱 응용 프로그램에까지도 적용되고 있다. OSGi 서비스 플랫폼은 홈게이트웨이, 텔레매틱스 단말(예:BMW, SimensVDO), 모바일 단말, 산업 자동화, 빌딩 자동화, [PDA](https://ko.wikipedia.org/wiki/PDA "wikilink") / [스마트폰](../Page/스마트폰.md "wikilink") / [태블릿](../Page/태블릿_컴퓨터.md "wikilink") 등의 모바일 단말, [그리드 컴퓨팅](https://ko.wikipedia.org/wiki/그리드_컴퓨팅 "wikilink"), 백색가전(예: BSH, 보쉬-지멘스 가전 합작회사의 Serve@Home, [Clare Controls](http://www.clarecontrols.com/), [Xanboo](https://web.archive.org/web/20000511141816/http://www.xanboo.com/), [AlertMe](https://web.archive.org/web/20130326154156/https://www.alertme.com/) 등), 엔터테인먼트 (예: 필립스의 iPronto), 기업 차량 관리(예: Acunia의 [Fleet Management Solution](https://web.archive.org/web/20060210023839/http://www.acunia.com/web/acuniatpl1.asp?customer=13&ut=L&hmain=1389&stype=X) 등), [로봇 미들웨어와](https://ko.wikipedia.org/wiki/로봇_미들웨어 "wikilink") 데스크톱, 엔터프라이즈 서버 등에 응용할 수 있다.

## Architecture

OSGi (개방형 서비스 게이트웨이 이니셔티브) 은 모듈형 소프트웨어 프로그램과 라이브러리를 개발 및 배포하기위한 자바 프레임 워크입니다. 각 번들은 강하게 결합하고, 동적으로 로딩이 가능한 class, jar 그리고 명시적으로  외부 종속성을 선언하는 환경설정파일의 모음입니다.

프레임 워크는 개념적으로 다음 부분으로 구성되어 있습니다.

### Bundles

Bundles은 추가적인 manifest 헤더를 가진 jar 로 구성된다.

### Services

Service층은  Plain Old Java Interfaces (POJI)  혹은  Plain Old Java Objects (POJO) 를 위한 publish-find-bind model 을 제공함으로써   bundle을 동적인 방식으로  연결한다.

### Services Registry

관리 서비스( 서비스등록, 서비스추적, 서비스참조) 를 위한  응용프로그램 인터페이스이다.

### Life-Cycle

생명주기 관리((install, start, stop, update, and uninstall)를 위한 응용프로그램 인터페이스이다.

### Modules

캡슐화를 정의하고 종속성을 선언하는 층이다. ( 어떻게 bundle이 코드를 불러오고 내보내는지)

### Security

번들로 하여금 미리 정의된 기능을 제한하는 보안측면을 다루는 층이다.

### Execution Environment

특정 플랫폼에서 어떤 method와 class가 가용한지 정의한다.   정해진 실행환경은 없다. 왜냐하면, 실행환경은  Java Community Process가 Java의  새로운 version과 에디션을 생성할 때마다 그 변경사항에 종속적이기 때문이다. 어째튼, 아래 목록이 현재 대부분의 OSGi 실현체에 의해 지원되는 실행환경이다.

  - CDC-1.0/Foundation-1.0

<!-- end list -->

  - CDC-1.1/Foundation-1.1

<!-- end list -->

  - OSGi/Minimum-1.0

<!-- end list -->

  - OSGi/Minimum-1.1

<!-- end list -->

  - JRE-1.1

<!-- end list -->

  - J2SE-1.2 부터 J2SE-1.6까지

## OSGi 표준 사양

  - OSGi Release 1 (R1): 2000년 5월
  - OSGi Release 2 (R2): 2001년 10월
  - OSGi Release 3 (R3): 2003년 3월
  - OSGi Release 4 (R4): 2005년 10월 / 2006년 9월
      - Core Specification (R4 Core): 2005년 10월
      - Mobile Specification (R4 Mobile / JSR-232): 2006년 9월
  - OSGi Release 4.1 (R4.1): 2007년 3월 (별칭: JSR-291)
  - OSGi Release 4.2 (R4.2): 2009년 9월
      - Core and Compendium Version 4.2: 2009년 9월
      - Enterprise Version 4.2: 2010년 3월
  - OSGi Release 4.3 (R4.3): 2011년 4월
      - Compendium Version 4.3 and Residential Version 4.3: 2012년 5월
  - OSGi Release 5 (R5): 2012년 6월
      - Core and Enterprise: 2012년 6월
  - OSGi Release 6 (R6): 2015년 6월
      - Core: 2015년 6월
  - OSGi Release 7 (R7): 2018년 4월
      - Core and Compendium: 2018년 4월

## OSGi 관련 표준

  - RFC-2608 ([Service Location Protocol](https://ko.wikipedia.org/wiki/Service_Location_Protocol "wikilink"))
  - Sun [Jini](../Page/Jini.md "wikilink")
  - Sun JCP [JSR-8](http://www.jcp.org/en/jsr/detail?id=8) (Open Services Gateway Specification)
  - Sun JCP [JSR-232](http://www.jcp.org/en/jsr/detail?id=232) (Mobile Operational Management)
  - Sun JCP [JSR-246](http://www.jcp.org/en/jsr/detail?id=246) (Device Management API)
  - Sun JCP [JSR-249](http://www.jcp.org/en/jsr/detail?id=249) (Mobile Service Architecture for CDC)
  - Sun JCP [JSR-277](http://www.jcp.org/en/jsr/detail?id=277) (Java Module System)
  - Sun JCP [JSR-291](http://www.jcp.org/en/jsr/detail?id=291) (Dynamic Component Support for Java SE - AKA OSGi 4.1)
  - Sun JCP [JSR-294](http://www.jcp.org/en/jsr/detail?id=294) (Improved Modularity Support in the Java Programming Language)
  - [HGi](http://www.homegatewayinitiative.org/) (Home Gateway initiative)

## 대한민국의 OSGi 커뮤니티

  - [OSGi User Forum Korea](http://korea.osgiusers.org/Main/HomePage)

## 주요 OSGi 적용 프로젝트

  - [Apache Aries](https://ko.wikipedia.org/wiki/Apache_Aries "wikilink")
  - [Apache Karaf](https://ko.wikipedia.org/wiki/Apache_Karaf "wikilink")
  - [Apache Felix](https://ko.wikipedia.org/wiki/Apache_Felix "wikilink")
  - [Apache Sling](https://ko.wikipedia.org/wiki/Apache_Sling "wikilink")
  - [Business Intelligence and Reporting Tools (BIRT) Project](https://ko.wikipedia.org/wiki/BIRT_Project "wikilink")
  - [Cytoscape](https://ko.wikipedia.org/wiki/Cytoscape "wikilink")
  - [DataNucleus](https://ko.wikipedia.org/wiki/DataNucleus "wikilink")
  - [EasyBeans](https://ko.wikipedia.org/wiki/EasyBeans "wikilink")
  - [Eclipse](https://ko.wikipedia.org/wiki/Eclipse_\(software\) "wikilink")
  - [Paremus Service Fabric](https://ko.wikipedia.org/wiki/Paremus_Service_Fabric "wikilink")
  - [Eclipse Virgo](https://ko.wikipedia.org/wiki/SpringSource_dm_Server "wikilink")
  - [Event Insight](https://ko.wikipedia.org/wiki/Event_Insight "wikilink")
  - [GlassFish](https://ko.wikipedia.org/wiki/GlassFish "wikilink")
  - [Fuse ESB](https://ko.wikipedia.org/wiki/Fuse_ESB "wikilink")
  - [GX WebManager Community Edition](https://ko.wikipedia.org/wiki/GX_WebManager_Community_Edition "wikilink")
  - [JBoss](https://ko.wikipedia.org/wiki/JBoss "wikilink")
  - [JOnAS](https://ko.wikipedia.org/wiki/JOnAS "wikilink") 5
  - [JOSSO](https://ko.wikipedia.org/wiki/JOSSO "wikilink") 2
  - [Netbeans](https://ko.wikipedia.org/wiki/Netbeans "wikilink")
  - [Nuxeo](https://ko.wikipedia.org/wiki/Nuxeo "wikilink")
  - [OpenEJB](https://ko.wikipedia.org/wiki/OpenEJB "wikilink")
  - [SpringSource dm Server](https://ko.wikipedia.org/wiki/SpringSource_dm_Server "wikilink")
  - [Weblogic](https://ko.wikipedia.org/wiki/Weblogic "wikilink")
  - [WebSphere](https://ko.wikipedia.org/wiki/WebSphere "wikilink")
  - [WSO2 Carbon](https://ko.wikipedia.org/wiki/WSO2_Carbon "wikilink")
  - [Atlassian](https://ko.wikipedia.org/wiki/Atlassian "wikilink") [Confluence](../Page/컨플루언스_\(소프트웨어\).md "wikilink") & [JIRA](https://ko.wikipedia.org/wiki/Atlassian_Jira "wikilink")
  - [IntelliJIDEA](https://ko.wikipedia.org/wiki/IntelliJIDEA "wikilink")

## 관련 서적

  - [OSGi 관련 서적 목록](http://www.osgi.org/Links/Books)
  - [Programming Open Service Gateways with Java Embedded Server(TM) Technology](http://books.google.co.kr/books?id=GZ5wb8HDEJ8C&printsec=frontcover&hl=ko#v=onepage&q&f=false),

## 같이 보기

  - [OSGi 사양 구현](https://en.wikipedia.org/wiki/OSGi_Specification_Implementations)
  - [OSGi 시장적용사례](https://web.archive.org/web/20130304222337/http://www.osgi.org/Markets/HomePage)
  - [OSGi 시장적용사례 - 엔터프라이즈](http://www.osgi.org/Markets/Enterprise)
  - [OSGi 시장적용사례 - 오픈소스](https://web.archive.org/web/20130303201636/http://www.osgi.org/Markets/OpenSource)
  - [OSGi 시장적용사례 - 모바일](http://www.osgi.org/Markets/Mobile)
  - [OSGi 시장적용사례 - 텔레매틱스](http://www.osgi.org/Markets/Telematics)
  - [OSGi 시장적용사례 - 스마트홈](http://www.osgi.org/Markets/SmartHome)
  - [OSGi 시장적용사례 - 헬스케어](http://www.osgi.org/Markets/EHealth)

[분류:1999년 설립](https://ko.wikipedia.org/wiki/분류:1999년_설립 "wikilink") [분류:표준화 기구](https://ko.wikipedia.org/wiki/분류:표준화_기구 "wikilink") [분류:자바로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바로_작성된_자유_소프트웨어 "wikilink")