> This article is converted from Wikipedia: [Plain Old Java Object](https://ko.wikipedia.org/wiki/Plain_Old_Java_Object).


**Plain Old Java Object**, 간단히 **POJO**는 말 그대로 해석을 하면 오래된 방식의 간단한 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 오브젝트라는 말로서 [Java EE](https://ko.wikipedia.org/wiki/Java_EE "wikilink") 등의 중량 [프레임워크](https://ko.wikipedia.org/wiki/프레임워크 "wikilink")들을 사용하게 되면서 해당 프레임워크에 종속된 "무거운" 객체를 만들게 된 것에 반발해서 사용되게 된 용어이다. 2000년 9월에 [마틴 파울러](https://ko.wikipedia.org/wiki/마틴_파울러 "wikilink"), 레베카 파슨, 조쉬 맥킨지 등이 사용하기 시작한 용어로서 마틴 파울러는 다음과 같이 그 기원을 밝히고 있다. \[1\]

POJO라는 용어는 이후에 주로 특정 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 모델이나 기능, [프레임워크](https://ko.wikipedia.org/wiki/프레임워크 "wikilink") 등을 따르지 않은 자바 오브젝트를 지칭하는 말로 사용되었다. [스프링 프레임워크는](../Page/스프링_프레임워크.md "wikilink") POJO 방식의 프레임워크이다.

## POJO 현상

POJO라는 용어는 기존의 복잡한 [프레임워크](../Page/소프트웨어_프레임워크.md "wikilink") 대신 일반적이고 쉬운 용어가 필요한 다른 분야에도 널리 사용되기 시작했다.

  - POPO : Plain Old PHP Object의 약자로서, [PHP](../Page/PHP.md "wikilink") 언어에서 사용
  - POCO : Plain Old CLR Object의 약자로서, [닷넷 프레임워크에서](../Page/닷넷_프레임워크.md "wikilink") 사용
  - PODS : Plain Old Data Structures의 약자로서, [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 언어에서 오직 C 언어의 특징만 사용하는 경우
  - POD : Plain Old Documentation의 약자로서, [펄](../Page/펄.md "wikilink")(Perl) 언어에서 사용
  - POTS : Plain Old Telephone Service의 약자

## 정의

이상적으로, POJO는 자바 언어 사양 외에 어떠한 제한에도 묶이지 않은 자바 오브젝트라고 할 수 있다. 이를테면 POJO는 다음을 따라야 할 필요는 없다.

1.  미리 정의된 클래스의 확장. 예:
    ``` java
    public class Foo extends javax.servlet.http.HttpServlet { ...
    ```
2.  미리 정의된 인터페이스의 구현. 예:
    ``` java
    public class Bar implements javax.ejb.EntityBean { ...
    ```
3.  미리 정의된 [애너테이션을](../Page/자바_애너테이션.md "wikilink") 포함. 예:
    ``` java
    @javax.persistence.Entity public class Baz { ...
    ```

그러나 기술적 어려움이나 기타 이유로 인해 POJO 호환으로 기술하고 있는 수많은 소프트웨어 제품이나 프레임워크들은 실제로 정상 동작을 위해 퍼시스턴스(persistence)와 같은 기능을 위해 미리 정의된 애너테이션의 사용을 요구하고 있다.

## 각주

[분류:자바 (프로그래밍 언어)](https://ko.wikipedia.org/wiki/분류:자바_\(프로그래밍_언어\) "wikilink") [분류:브랜드 경영](https://ko.wikipedia.org/wiki/분류:브랜드_경영 "wikilink")

1.