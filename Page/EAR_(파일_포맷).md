> This article is converted from Wikipedia: [EAR \( \)](https://ko.wikipedia.org/wiki/EAR_\(_\)).


**EAR**(Enterprise ARchive)은 하나 이상의 모듈들은 하나의 아카이브로 묶어서 여러 [모듈이](https://ko.wikipedia.org/wiki/자바_EE_애플리케이션 "wikilink") [애플리케이션 서버에](https://ko.wikipedia.org/wiki/애플리케이션_서버 "wikilink") 동시에 일관성 있게 배치될 수 있도록 하기 위한 [자바 EE에](https://ko.wikipedia.org/wiki/자바_EE "wikilink") 쓰이는 [파일 형식이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink").

[앤트](../Page/아파치_앤트.md "wikilink"), [메이븐](../Page/아파치_메이븐.md "wikilink"), [Gradle](../Page/Gradle.md "wikilink")이 EAR 파일을 빌드하는데 사용될 수 있다.

## 파일 구조

EAR 파일은 .ear 확장자를 가진 표준 [JAR 파일](../Page/JAR_\(파일_포맷\).md "wikilink")(ZIP 파일)이며, 애플리케이션 모듈을 대표하는 하나 이상의 엔트리 및 하나 이상의 배치 기술자를 포함하는 META-INF라는 이름의 메타데이터 디렉터리가 있다.

### 모듈

  - 웹 모듈은 [.war](../Page/WAR_\(파일_포맷\).md "wikilink") 확장자를 지닌다.
  - [POJO](https://ko.wikipedia.org/wiki/POJO "wikilink") 자바 클래스는 [.jar](https://ko.wikipedia.org/wiki/.jar "wikilink") 파일 안에 배치될 수 있다. 하나 이상의 웹 구성 요소, 다른 리소스, [웹 애플리케이션](../Page/웹_애플리케이션.md "wikilink") [배치 서술자로](https://ko.wikipedia.org/wiki/배치_서술자 "wikilink") 이루어진 배치 가능한 단위이다. 이 웹 모듈은 표준 웹 애플리케이션 포맷 내의 디렉터리, 파일 [계층](../Page/계층.md "wikilink") 안에 포함된다.
  - [엔터프라이즈 자바빈즈](../Page/엔터프라이즈_자바빈즈.md "wikilink") 모듈은 [.jar](https://ko.wikipedia.org/wiki/.jar "wikilink") 확장자를 지니며 영구적으로 배치된 클래스를 기술하는 자신만의 META-INF 디렉터리 서술자가 있다.
  - [리소스 어댑터](https://ko.wikipedia.org/wiki/JCA "wikilink") 모듈은 .rar 확장자를 지닌다.

### META-INF 디렉터리

META-INF 디렉터리에는 적어도 자바 EE 배치 서술자(Java EE Deployment Descriptor)로 알려져 있는 application.xml 배치 서술자가 포함된다. 여기에는 다음의 XML 엔티티가 포함된다:

  - `icon`: 애플리케이션을 대표하는 이미지를 위한 위치를 지정한다. 하부 구역은 `small-icon`, `large-icon`을 위해 생성된다.
  - `display-name`: 애플리케이션을 식별한다.
  - `description`
  - 각 아카이브 내의 `module` 요소
  - 0개 이상의 `security-role` 요소: 애플리케이션 내의 전역 보안 역할

## 같이 보기

  - [WAR (파일 포맷)](../Page/WAR_\(파일_포맷\).md "wikilink")
  - [JAR (파일 포맷)](../Page/JAR_\(파일_포맷\).md "wikilink")

## 외부 링크

  - <http://java.sun.com/j2ee/1.4/docs/glossary.html>
  - <http://java.sun.com/javaee/5/docs/tutorial/doc/bnaby.html#indexterm-47>

[분류:아카이브 포맷](https://ko.wikipedia.org/wiki/분류:아카이브_포맷 "wikilink") [분류:자바 플랫폼, 엔터프라이즈 에디션](https://ko.wikipedia.org/wiki/분류:자바_플랫폼,_엔터프라이즈_에디션 "wikilink")