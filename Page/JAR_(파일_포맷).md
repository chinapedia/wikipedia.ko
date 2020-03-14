> This article is converted from Wikipedia: [JAR \( \)](https://ko.wikipedia.org/wiki/JAR_\(_\)).


**JAR**(, 자바 아카이브)는 여러개의 [자바 클래스 파일과](https://ko.wikipedia.org/wiki/자바_클래스 "wikilink"), 클래스들이 이용하는 관련 리소스(텍스트, 그림 등) 및 [메타데이터](https://ko.wikipedia.org/wiki/메타데이터 "wikilink")를 하나의 파일로 모아서 [자바 플랫폼에](https://ko.wikipedia.org/wiki/자바_플랫폼 "wikilink") [응용 소프트웨어나](https://ko.wikipedia.org/wiki/응용_소프트웨어 "wikilink") [라이브러리를](https://ko.wikipedia.org/wiki/라이브러리_\(컴퓨팅\) "wikilink") 배포하기 위한 [소프트웨어](https://ko.wikipedia.org/wiki/소프트웨어 "wikilink") [패키지](https://ko.wikipedia.org/wiki/패키지 "wikilink") 파일 포맷이다.\[1\]

JAR 파일은 실제로 [ZIP 파일 포맷으로](https://ko.wikipedia.org/wiki/ZIP_\(파일_포맷\) "wikilink") 이루어진 [압축 파일로서](https://ko.wikipedia.org/wiki/압축_파일 "wikilink"), 파일 확장자는 `.jar`이다. 컴퓨터 사용자들은 [JDK에](https://ko.wikipedia.org/wiki/자바_개발_킷 "wikilink") 포함된 `jar` 명령어를 이용하여 JAR 파일을 만들거나 압축을 풀 수 있다. 또, `zip` 도구를 사용할 수도 있으나 압축 시에는 [매니페스트](https://ko.wikipedia.org/wiki/매니페스트 "wikilink") 파일이 처음이어야 하는 경우가 있어서 zip 파일 헤더의 엔트리 순서가 중요하다. JAR 안에서 파일 이름들은 유니코드 텍스트로 되어 있다.\[2\]

## 설계

JAR 파일은 [자바 런타임이](https://ko.wikipedia.org/wiki/자바_런타임 "wikilink") 효율적으로 애플리케이션을 [배치](https://ko.wikipedia.org/wiki/배치 "wikilink")(디플로이)할 수 있는 수단으로 설계되었다. 자바 애플리케이션을 구성하는 클래스와 관련 리소드들을 단일 파일로 묶어 압축된 형태인 JAR 파일은, 한 차례의 요청으로 애플리케이션 전체를 다운로드할 수 있게 해준다.

JAR 파일은 `META-INF/MANIFEST.MF`경로에 위치한 [매니페스트 파일을](https://ko.wikipedia.org/wiki/매니페스트_파일 "wikilink") 선택적으로 포함할 수 있다. 매니페스트 파일 안에는, 어떻게 JAR 파일을 이용할지를 기술한 엔트리 정보가 적혀있다. 이를테면 [클래스패스(자바)](https://ko.wikipedia.org/wiki/클래스패스\(자바\) "wikilink") 엔트리를 사용하면 해당 JAR 파일과 함께 로드할 다른 JAR 파일들을 지정할 수 있다. `java.util.zip` 패키지는 JAR 파일을 읽고 쓰는 클래스들을 포함하고 있다.

## 압축 해제

JAR 파일의 압축을 해제하는데는, ZIP 파일을 해제하는 표준 소프트웨어를 사용하거나 [자바 개발 키트에](../Page/자바_개발_키트.md "wikilink") 포함된 `jar` 명령을 이용할 수 있다.: `jar -xf foo.jar`

## 보안

개발자들은 JAR 파일들에 [디지털 서명을](https://ko.wikipedia.org/wiki/디지털_서명 "wikilink") 할 수 있다. 이 경우 서명 정보는 내재된 매니페스트 파일의 일부가 된다. JAR 그 자체에 서명되는 것은 아니라, 압축 파일 안의 모든 파일들이 체크섬으로 나열된다. 즉, 체크섬을 통해 서명이 된다는 것을 뜻한다. 여러 개의 엔트리들은 각기 서명함으로써 JAR 파일 자체를 변경하여 JAR 파일을 서명할 수 있지만 서명된 파일들은 그 자체로 유효한 상태로 남아있다. 서명된 JAR 파일들을 자바 런타임이 로드할 때 서명이 유효한지 확인하고 서명이 일치하지 않는 클래스들은 로드를 거부할 수 있다.

JAR 파일 안의 내용은, 경우에 따라 [리버스 엔지니어링을](https://ko.wikipedia.org/wiki/리버스_엔지니어링 "wikilink") 어렵게 하기 위해 [난독화](https://ko.wikipedia.org/wiki/난독화 "wikilink")되기도 한다.

## 실행 가능한 JAR 파일

실행 가능한 자바 프로그램은, 프로그램이 사용하는 다른 라이브러리와 함께 JAR파일로 압축될 수 있다. JAR파일이 실행 가능하려면, 파일 안에 포함된 메니페스트 파일에 [엔트리 포인트의](https://ko.wikipedia.org/wiki/엔트리_포인트 "wikilink") 클래스 이름이 `Main-Class: myPrograms.MyClass` 형식으로 기술되어야 하며, 명시적으로 클래스패스 정보가 기술되어 있어야 한다.(이때 -cp 인수는 무시된다) 운영체제에 따라서는 JAR 파일의 아이콘을 직접 클릭해서 실행가능하기도 하다. JAR 파일을 커맨드 라인에서 실행시키기 위해서는 `java -jar foo.jar`라고 입력한다.

## 메니페스트

JAR 파일 안에 포함되어 있는 매니페스트 파일은, 메타데이터 정보를 포함하고 있다.\[3\]\[4\] 이 메타데이터 정보에는 확장 정보 및 패키지 관련 데이터가 기술되어 있으며, 섹션 형식으로 구성된 키-값 쌍 형태의 문자열이다. JAR이 실행 가능하도록 하기 위해서는, 메니페스트 파일에, 애플리케이션의 메인 클래스의 이름이 기술되어 있어야 한다. 메니페스트 파일의 명칭은 `MANIFEST.MF`이며, 이 파일이 포함되어 있는 디렉토리는, 압축된 파일의 내용물 가운데 가장 첫번째 위치에 배치되어야 한다.

## 관련 포맷

JAR 포맷을 바탕으로 다음과 같은 파일 포맷들이 생겨났다.

  - [WAR (파일 포맷)](../Page/WAR_\(파일_포맷\).md "wikilink") : 웹 애플리케이션을 구성하는 자바 클래스와, [자바 서버 페이지](https://ko.wikipedia.org/wiki/자바_서버_페이지 "wikilink"), 관련 [XML](https://ko.wikipedia.org/wiki/XML "wikilink") 파일 등을 묶은 압축 파일 포맷
  - [RAR](https://ko.wikipedia.org/wiki/자바_EE_커넥터_아키텍처 "wikilink") (resource adapter archive) : J2EE 커넥터 아키텍처(JCA) 애플리케이션을 묶는데 사용되는 압축 포맷이다.
  - [EAR](https://ko.wikipedia.org/wiki/EAR_\(파일_포맷\) "wikilink") (enterprise archive) : 자바 엔터프라이스 애플리케이션에서 이용되는 압축 포맷으로, 애플리케이션 클래스 및 관련 JAR, WAR, RAR 압축 파일들을 묶는 용도로 사용된다.
  - [APK](../Page/안드로이드_응용_프로그램_패키지.md "wikilink") (Android Application Package) : [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink") 애플리케이션에서 사용되는 자바 압축 포맷의 일종이다.\[5\]

## 같이 보기

  - [Java Platform Module System](https://ko.wikipedia.org/wiki/Java_Platform_Module_System "wikilink")

## 각주

## 외부 링크

  - [JAR File Overview](http://download.oracle.com/javase/6/docs/technotes/guides/jar/jarGuide.html)

  - [JAR File Specification](http://download.oracle.com/javase/6/docs/technotes/guides/jar/jar.html)

  - [Original JAR File Specification](http://www.cse.yorku.ca/tech/other/jdk1.2.1/docs/guide/jar/manifest.html)

[분류:아카이브 포맷](https://ko.wikipedia.org/wiki/분류:아카이브_포맷 "wikilink") [분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink")

1.
2.
3.
4.
5.