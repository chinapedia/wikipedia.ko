> This article is converted from Wikipedia: [OLE DB](https://ko.wikipedia.org/wiki/OLE_DB).


**OLE DB**(Object Linking and Embedding, Database) 또는 **객체 연결 삽입 데이터베이스**는 [마이크로소프트](../Page/마이크로소프트.md "wikilink")사가 개발한 [API](../Page/API.md "wikilink")로, 통일된 방식으로 저장된 여러 종류의 [데이터](https://ko.wikipedia.org/wiki/데이터 "wikilink")에 접근하기 위해 만들어졌다. [컴포넌트 오브젝트 모델](../Page/컴포넌트_오브젝트_모델.md "wikilink") (COM)을 사용하여 추가된 인터페이스 집합이며 [객체 연결 삽입과는](../Page/객체_연결_삽입.md "wikilink") 관련이 없다. [ODBC](../Page/ODBC.md "wikilink")를 높은 수준으로 대체하면서도 그 뒤를 잇도록 설계되었으며 [오브젝트 데이터베이스와](https://ko.wikipedia.org/wiki/오브젝트_데이터베이스 "wikilink") [SQL](../Page/SQL.md "wikilink") 추가가 필수적이지 않은 [스프레드시트](../Page/스프레드시트.md "wikilink") 같이 더 다양한 범위의 비[관계형 데이터베이스를](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink") 지원하기 위해 기능을 확장하였다.

OLE DB는 데이터 저장을 데이터소스, 세션, 명령어, 열 집합을 포함한 추상 집합을 통해 접근해야 하는 응용 프로그램과 따로 떼어놓는다. 그 까닭은 다른 응용 프로그램들이 여러 종류와 원천의 데이터에 접근해야 하며 기술적인 측면에서 어떻게 동작하는지를 알 필요는 없기 때문이다. OLE DB는 개념적으로 소비자(consumer)와 제공자(provider)로 구분되어 있다. 소비자는 데이터에 접근해야 하는 응용 프로그램이며 제공자는 인터페이스를 추가하는 소프트웨어 구성 요소이다. 이로써 데이터는 소비자에게 전달된다. **OLE DB는 [마이크로소프트 데이터 액세스 구성 요소](https://ko.wikipedia.org/wiki/마이크로소프트_데이터_액세스_구성_요소 "wikilink")(MDAC) 스택의 일부이다.** MDAC는 마이크로소프트 기술들을 한데 모아 놓은 것으로, 프로그래머가 거의 모든 데이터 저장소에 접근하는 통일되고 포괄적인 방법을 허용해 주는 프레임워크로서 함께 상호작용을 할 수 있게 도와 준다. 텍스트 파일과 스프레드시트로 [오라클](../Page/오라클_데이터베이스.md "wikilink") [SQL 서버](https://ko.wikipedia.org/wiki/SQL_서버 "wikilink"), [Sybase ASE와](https://ko.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink") 같은 복잡한 데이터베이스를 통하여 이러한 단순한 데이터 저장소를 접근할 수 있게 OLE DB 제공자를 만들 수 있다. 또, 전자 우편 시스템과 같은 계층 데이터저장소로의 접근을 제공할 수 있다.

그러나 서로 다른 저장 기술은 각기 다른 수행 기능을 보이므로 OLE DB 제공자는 OLE DB에 이용할 수 있는 가능한 모든 인터페이스를 추가하지 않을 수 있다. 사용할 수 있는 수행 기능은 COM 오브젝트를 사용함으로써 추가할 수 있다. OLE DB 제공자는 데이터 저장 기술 기능을 특정한 COM 인터페이스에 매핑할 것이다. 마이크로소프트는 제공자 정의(provider-specific)로 인터페이스를 사용할 수 있다고 설명한다. 이는 이에 수반되는 데이터베이스 기술에 의지하여 적용하지 못할 수도 있음을 말한다. 다만 제공자들이 데이터 저장 수행 기능을 늘릴 수 있으며 이러한 수행 기능들은 마이크로소프트 환경에서 서비스(services)로 알려져 있다.

## OLE DB 제공자

  - [마이크로소프트](http://msdn.microsoft.com/data/) - 몇 가지 OLE DB 제공자를 MDAC오 [JET](https://ko.wikipedia.org/wiki/제트_데이터베이스_엔진 "wikilink") 키트의 일부로 제공
  - [심바 테크놀로지스](https://ko.wikipedia.org/wiki/심바_테크놀로지스 "wikilink") - 다차원, 스타형 데이터베이스 연결을 위한 OLAP 제공자의 사용자 지정 OLE DB를 만드는 데 쓰이는 SDK인 심바프로바이더(SimbaProvider) 제공
  - [오픈링크 소프트웨어](https://web.archive.org/web/20090826194206/http://uda.openlinksw.com/oledb/) - [ODBC](../Page/ODBC.md "wikilink")와 [JDBC](../Page/JDBC.md "wikilink")에 대한 OLE DB 브리지뿐 아니라 수많은 [SQL](../Page/SQL.md "wikilink") DBM를 위한 OLE DB 제공자 제공
  - [SQLSummit.com: OLE DB 제공자의 카탈로그](http://www.sqlsummit.com/oledbVen.htm)
  - [인터베이스와 파이어보드요 OLE DB 제공자 (14개의 데이터베이스 형태 지원, 무료/프로 버전 모두 사용 가능)](http://www.ibprovider.com/)
  - [OLE DB Provider for PostgreSQL](http://www.zenkov.com/)

[분류:데이터베이스 API](https://ko.wikipedia.org/wiki/분류:데이터베이스_API "wikilink") [분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:SQL](https://ko.wikipedia.org/wiki/분류:SQL "wikilink")