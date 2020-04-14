> This article is converted from Wikipedia: [WAR \(파일 포맷\)](https://ko.wikipedia.org/wiki/WAR_\(파일_포맷\)).


**WAR**(\[1\], 웹 애플리케이션 아카이브) 파일은 [소프트웨어 공학에서](../Page/소프트웨어_공학.md "wikilink") [자바서버 페이지](../Page/자바서버_페이지.md "wikilink"), [자바 서블릿](../Page/자바_서블릿.md "wikilink"), [자바 클래스](https://ko.wikipedia.org/wiki/자바_클래스_파일 "wikilink"), [XML](../Page/XML.md "wikilink"), 파일, 태그 라이브러리, 정적 웹 페이지 ([HTML](../Page/HTML.md "wikilink") 관련 파일) 및 [웹 애플리케이션을](../Page/웹_애플리케이션.md "wikilink") 함께 이루는 기타 자원을 한데 모아 배포하는데 사용되는 [JAR 파일이다](../Page/JAR_\(파일_포맷\).md "wikilink").

## 예

다음의 견본 *web.xml* 파일은 [서블릿의](../Page/자바_서블릿.md "wikilink") 선언 및 연결을 증명하고 있다:

``` xml
 <?xml version="1.0" encoding="UTF-8"?>
 <!DOCTYPE web-app
     PUBLIC "-//Sun Microsystems, Inc.//DTD Web Application 2.2//EN"
     "http://java.sun.com/j2ee/dtds/web-app_2_2.dtd">

 <web-app>
     <servlet>
         <servlet-name>HelloServlet</servlet-name>
         <servlet-class>mypackage.HelloServlet</servlet-class>
     </servlet>

     <servlet-mapping>
         <servlet-name>HelloServlet</servlet-name>
         <url-pattern>/HelloServlet</url-pattern>
     </servlet-mapping>

     <resource-ref>
         <description>
             Resource reference to a factory for javax.mail.Session
             instances that may be used for sending electronic mail messages,
             preconfigured to connect to the appropriate SMTP server.
         </description>
         <res-ref-name>mail/Session</res-ref-name>
         <res-type>javax.mail.Session</res-type>
         <res-auth>Container</res-auth>
     </resource-ref>
 </web-app>

```

/WEB-INF/classes 디렉터리는 [클래스로더의](../Page/자바_클래스로더.md "wikilink") [클래스패스](https://ko.wikipedia.org/wiki/클래스패스 "wikilink")(classpath) 위에 존재한다. 이 장소가 .class 파일들이 웹 애플리케이션 실행 시 호출되는 장소이다.

/WEB-INF/lib 디렉터리에 위치한 JAR 파일들은 클래스로더의 클래스패스에 존재할 수 있다.

## 같이 보기

  - [EAR](../Page/EAR_\(파일_포맷\).md "wikilink")
  - [JAR](../Page/JAR_\(파일_포맷\).md "wikilink")
  - [EXE](../Page/PE_포맷.md "wikilink")

## 각주

## 외부 링크

  - [Oracle Java EE 7 Tutorial: Packaging Web Archives](https://docs.oracle.com/javaee/7/tutorial/packaging003.htm)
  - [Oracle Java EE 6 Tutorial: Web Modules](http://docs.oracle.com/javaee/6/tutorial/doc/bnadx.html)
  - [Oracle Java EE 5 Tutorial: Web Modules](http://docs.oracle.com/javaee/5/tutorial/doc/bnadx.html)
  - [Sun Microsystems: XML Schema for the Servlet 2.5 Web ARchive (WAR) File](http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd)
  - [Sun Microsystems: XML Schema for the Servlet 2.4 Web ARchive (WAR) File](http://java.sun.com/xml/ns/j2ee/web-app_2_4.xsd)
  - [JSR 154: Java Servlet 2.4 Specification](http://jcp.org/en/jsr/detail?id=154)

[분류:아카이브 포맷](https://ko.wikipedia.org/wiki/분류:아카이브_포맷 "wikilink") [분류:자바 플랫폼, 엔터프라이즈 에디션](https://ko.wikipedia.org/wiki/분류:자바_플랫폼,_엔터프라이즈_에디션 "wikilink")

1.