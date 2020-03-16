> This article is converted from Wikipedia: [JNDI](https://ko.wikipedia.org/wiki/JNDI).


**JNDI**(Java Naming and Directory Interface)는 [디렉터리 서비스에서](https://ko.wikipedia.org/wiki/디렉터리_서비스 "wikilink") 제공하는 데이터 및 객체를 발견(discover)하고 참고(lookup)하기 위한 [자바 API다](https://ko.wikipedia.org/wiki/자바_API "wikilink").

NDI는 일반적으로 다음의 용도로 쓰인다:

  - 자바 애플리케이션을 외부 디렉터리 서비스에 연결 (예: 주소 데이터베이스 또는 [LDAP](../Page/LDAP.md "wikilink") 서버)
  - [자바 애플릿이](../Page/자바_애플릿.md "wikilink") 호스팅 [웹 컨테이너가](../Page/웹_컨테이너.md "wikilink") 제공하는 구성 정보를 참고.<ref>

</ref>

## 배경

자바 [RMI와](../Page/자바_원격_함수_호출.md "wikilink") [자바 EE](https://ko.wikipedia.org/wiki/자바_EE "wikilink") API들은 JNDI API를 이용하여 네트워크 안의 오브젝트를 참고한다.

API는 다음을 제공한다.

  - 오브젝트를 이름에 바인드하기 위한 구조
  - 일반 쿼리를 허용하는 디렉터리 참조 인터페이스
  - 디렉터리 엔트리를 수정할 시기를 클라이언트가 결정할 수 있게 하는 이벤트 인터페이스
  - LDAP 서비스의 추가 기능을 지원하는 LDAP 확장

[SPI](https://ko.wikipedia.org/wiki/서비스_제공자_인터페이스 "wikilink") 부분은 다음을 포함하여 실질적으로 모든 종류의 네이밍 및 디렉터리 서비스를 지원한다:

  - [LDAP](../Page/LDAP.md "wikilink")
  - [DNS](../Page/도메인_네임_시스템.md "wikilink")
  - [NIS](../Page/네트워크_정보_서비스.md "wikilink")
  - [CORBA](https://ko.wikipedia.org/wiki/CORBA "wikilink") 이름 서비스
  - [파일 시스템](../Page/파일_시스템.md "wikilink")

[썬 마이크로시스템즈는](../Page/썬_마이크로시스템즈.md "wikilink") 1997년 3월 10일 JNDI 사양을 최초로 공개하였다.\[1\] 2006년 기준으로 JNDI의 버전은 1.2이다.

## 버전의 역사

| JNDI 버전  | 발표 | 자바 플랫폼                                                        | 중요한 변화 |
| -------- | -- | ------------------------------------------------------------- | ------ |
| JNDI 1.2 |    | [Java EE](https://ko.wikipedia.org/wiki/Java_EE "wikilink") 5 |        |
| JNDI 1.0 |    |                                                               |        |

JNDI 역사

## 각주

## 외부 링크

  - [자바 SE 7 JNDI 문서](http://docs.oracle.com/javase/7/docs/technotes/guides/jndi/index.html)
  - [자바 SE 8 JNDI 문서](http://docs.oracle.com/javase/8/docs/technotes/guides/jndi/index.html)
  - [JNDI 강좌](http://docs.oracle.com/javase/jndi/tutorial/)

[분류:자바 플랫폼, 엔터프라이즈 에디션](https://ko.wikipedia.org/wiki/분류:자바_플랫폼,_엔터프라이즈_에디션 "wikilink")

1.