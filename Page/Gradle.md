> This article is converted from Wikipedia: [Gradle](https://ko.wikipedia.org/wiki/Gradle).


**Gradle**은 Groovy를 이용한 [빌드 자동화](https://ko.wikipedia.org/wiki/빌드_자동화 "wikilink") 시스템이다. Groovy와 유사한 도메인 언어를 채용하였으며, 현재 [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink") 앱을 만드는데 필요한 안드로이드 스튜디오의 공식 빌드 시스템이기도 하다. Java, [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink")/[C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 등과 같은 여러 가지 언어를 지원한다.

## 자바 프로젝트의 예

[메이븐](../Page/아파치_메이븐.md "wikilink") 디렉터리 구조가 자바 소스와 리소스에 사용된다고 가정하자. 이 디렉터리들은 **src/main/java**, **src/main/resources**, **src/test/java**, **src/test/resources**이다.

**build.gradle**

``` groovy
apply plugin: 'java'
```

**gradle build**을 실행하면 다음과 같이 출력된다:

``` console
> gradle build
:compileJava
:processResources
:classes
:jar
:assemble
:compileTestJava
:processTestResources
:testClasses
:test
:check
:build

BUILD SUCCESSFUL
```

## 각주

## 외부 링크

  -
[분류:컴파일 도구](https://ko.wikipedia.org/wiki/분류:컴파일_도구 "wikilink") [분류:자바 개발 도구](https://ko.wikipedia.org/wiki/분류:자바_개발_도구 "wikilink") [분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink")