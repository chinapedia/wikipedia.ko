> This article is converted from Wikipedia: [블루드래곤 \(CFML\)](https://ko.wikipedia.org/wiki/블루드래곤_\(CFML\)).


**블루드래곤(BlueDragon)**은 어도비 콜드퓨전과 비슷한 CFML 엔진이다. 뉴 아틀란타(New Atlanta)사의 제품으로 개발/배포되고 있다.

블루드래곤 애플리케이션은 마이크로소프트 윈도, 리눅스, 맥 OS X 등 다양한 플랫폼상에서 동작하게 된다. 그리고 콜드퓨전 MX 7과 대부분 호환된다.

2008년 3월 뉴 아틀란타는 블루드래곤의 Java EE 에디션을 오픈 소스로 발표했다.

## 제품군

블루드래곤은 6가지 제품군으로 구분된다.

  - BlueDragon Server
  - BlueDragon Server JX (콜드퓨전 단독 실행 버전과 유사)
  - BlueDragon for J2EE Application Servers (BD J2EE)
  - BlueDragon for the Microsoft .NET Framework (BD .NET)
  - BlueDragon, BEA WebLogic Edition (BEA시절 제품으로 판매했었음)
  - Open BlueDragon, BlueDragon for J2EE의 오픈소스 버전.

BlueDragon Server와 BlueDragon Server JX는 윈도, 리눅스, OS X위에서 독립적으로 돌아가는 서버를 포함하고 있다. BD J2EE는 어떤 J2EE 서버든지 설치해서 CFML 애플리케이션을 사용할 수 있으며 콜드퓨전 MX처럼 CFML과 J2EE의 통합 기능을 활용할 수 있다. BEA WebLogic Edition은 BD J2EE버전을 BEA의 웹로직 서버에 특화되어 사용할 수 있도록 제공하고 있다. BD.NET은 마이크로소프트 닷넷 프레임워크과 IIS위에서 CFML 애플리케이션을 닷넷 웹 애플리케이션처럼 개발할 수 있도록 확장해주어 CFML과 ASP.NET과 통합된 기능을 제공한다. 콜드퓨전에서는 제공되지 않는 기능이다.

블루드래곤의 Server JX와 J2EE, 닷넷, 웹로직 에디션은 상업적 제품이며 30일간 시험판 버전을 다운로드 할 수 있고 한 개의 개발자 IP만을 지원하는 개발자 버전은 제한 없이 사용할 수 있다.

Server 에디션은 이와 다르게 개발단계에서는 무료로 사용할 수 있고 호스팅이나 재판매, 상업적 사용은 제한된다. 무료 서버 에디션에서 지원하는 CFML 태그는 다른 제품과 동일하지만 MS 윈도에서 ODBC 드라이버만 지원한다(리눅스와 맥 OS X에서는 MySQL이나 PostgreSQL만 지원한다). 그리고 MS 윈도에서는 IIS만 지원하고 리눅스나 맥 OS X에서는 아파치만 지원하며 SSL 연결은 지원되지 않는다.

Server JX, J2EE, .NET 지원 제품과 같은 상업용 에디션은 이런 제한 없이 사용할 수 있다.

마이크로소프트 닷넷 플랫폼에서 동작하는 닷넷 에디션 블루드래곤은 닷넷 플랫폼의 기능을 활용해 CFML 애플리케이션을 만들 수 있다. 닷넷 객체를 사용하듯이 CFML과 ASP.NET 사이에 통합된 기능을 활용할 수 있다.

오픈 블루드래곤은 GPLv3기반 블루드래곤의 오픈소스 버전이다. 오픈소스버전과 J2EE버전의 차이점은 상업적인 라이브러리(PDF 생성지원과 같은)를 제외하고 마이크로소프트 SQL 서버를 위한 JTurbo JDBC 드라이버와 블루드래곤 운영자 애플리케이션이 제외되었다. 톰캣이나 JBoss, Jetty와 같은 J2EE 애플리케이션 서버 위에서 동작하게 된다.

블루드래곤은 2002년 처음 공개되었다.

## 적용 사례

글로벌 커뮤니티인 마이스페이스에서 2005년 닷넷 버전 블루드래곤을 온라인 애플리케이션에 적용했다.

## 호환성

블루드래곤 7.0은 어도비 콜드퓨전 MX 7.0.2와 호환되도록 설계되었지만 약간의 CFML 구현상 차이가 있다. 블루드래곤은 콜드퓨전에 없는 추가된 태그와 함수, 기능을 제공한다. 마찬가지로 콜드퓨전에서 제공하는 것 중 일부는 블루드래곤에서 지원되지 않는다. 뉴 아틀란타는 문서를 통해 어도비 콜드퓨전 MX와 호환성 관련 목록을 제공하고 있다.

## 외부 링크

  - [블루드래곤 제품 웹사이트](http://www.newatlanta.com/bluedragon)
  - [OPENBD 웹사이트](http://www.openbluedragon.org/)

## 커뮤니티

  - [OPEN COLDFUSION](https://web.archive.org/web/20100418105630/http://cafe.naver.com/opencfml)

[분류:CFML 컴파일러](https://ko.wikipedia.org/wiki/분류:CFML_컴파일러 "wikilink")