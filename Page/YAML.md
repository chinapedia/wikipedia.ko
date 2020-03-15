> This article is converted from Wikipedia: [YAML](https://ko.wikipedia.org/wiki/YAML).


**YAML**은 [XML](../Page/XML.md "wikilink"), [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"), [펄](../Page/펄.md "wikilink"), [RFC2822](https://ko.wikipedia.org/wiki/RFC2822 "wikilink")에서 정의된 e-mail 양식에서 개념을 얻어 만들어진 '사람이 쉽게 읽을 수 있는' 데이터 직렬화 양식이다. 2001년에 [클라크 에반스가](https://ko.wikipedia.org/wiki/클라크_에반스 "wikilink") 고안했고, Ingy dot Net 및 Oren Ben-Kiki와 함께 디자인했다.

YAML이라는 이름은 "YAML은 마크업 언어가 아니다 (YAML Ain't Markup Language)” 라는 [재귀적인 이름에서](../Page/재귀_약자.md "wikilink") 유래되었다. 원래 YAML의 뜻은 “또 다른 마크업 언어 (Yet Another Markup Language)”였으나, YAML의 핵심은 문서 마크업이 아닌 데이터 중심에 있다는 것을 보여주기 위해 이름을 바꾸었다. 오늘날 XML과 [JSON](../Page/JSON.md "wikilink")이 데이터 직렬화에 주로 쓰이기 시작하면서, 많은 사람들이 YAML을 '가벼운 마크업 언어'로 사용하려 하고 있다.

## 요소

YAML은 모든 데이터를 리스트, 해쉬, 스칼라 데이터의 조합으로 적절히 표현할 수 있다는 믿음을 가지고 만들어졌다. 문법은 상대적으로 이해하기 쉽고, 가독성이 좋도록 디자인되었으며, 고급 컴퓨터 언어에 적합하다. 또한 들여쓰기 및 XML의 특수기호를 사용하기 때문에, XML과 거의 비슷하다.

  - YAML 문자열은 UTF-8 또는 UTF-16과 같이 출력 가능한 유니코드 문자집합을 이용한다.
  - 공백 문자를 이용한 들여쓰기로 구조체를 구분한다. 그러나 탭문자를 들여쓰기에 사용하지 않는다.
  - 리스트 요소는 여러 줄에 쓸 때에는 하이픈(**-**)으로 시작하는 한 줄에 하나의 요소를 표현하며, 한 줄에 모아 쓸 때에는 대괄호(**\[\]**)를 이용하며 쉼표로 각 요소를 구분한다.
  - 해쉬는 콜론 기호를 이용해서 **키:값**의 형태로 한 줄에 하나를 표현하거나, 한 줄에 모아 쓸 때에는 중괄호(**{}**)를 이용하며 쉼표로 각 요소를 구분한다.
  - 간단한 값(스칼라 값)은 보통 아무 표시를 하지 않으나 따옴표("")나 작은 따옴표('')를 이용해 둘러쌀 수 있다.
  - 따옴표 안에서 특수 문자는 C언어 스타일(역슬래쉬키와 함께쓰이는 제어문자 예. \\n)로 표시한다.
  - 블록 값은 보존(|) 또는 접기(\>)의 선택 지시자로 나눈다.
  - 하나의 스트림에 있는 여러 개의 문서는 하이픈 3개(---)로 나누며, 마침표 세개(...)로 스트림의 끝을 나타낸다.
  - 반복되는 노드는 기본적으로 &를 통해 나타내며, \* 문자 이후의 내용을 참조한다.
  - 주석은 \#으로 표시하며, 한 줄이 끝날 때까지 유효하다.
  - 노드들은 타입과 느낌표로 시작해 URI 주소를 지시하는 태그를 통해 라벨이 붙는다.
  - YAML 문서는 % 문자로 시작되는 몇 개의 지시자를 통해 특정 작업을 수행한다. YAML 1.1에서는 두 개의 지시자가 정의되어 있다.
      - %YAML 지시자는 주어진 문서의 YAML 버전을 나타내는 데 사용한다.
      - %TAG 지시자는 URI 주소를 나타내는 데 주로 사용하며, 이들 주소는 노드 타입 태그에 사용한다.

YAML은 공백과 스칼라 값을 가지고 있는 리스트 구분자를 위해 쉼표와 콜론이 필요하다. 미래의 표준화를 위해 YAML에서는 @, 엑센트 기호 ‘ 2개의 기호 문자를 예약해두고 있다.

## 예제

### 리스트

``` yaml
 --- # Favorite movies, block format
 - Casablanca
 - Spellbound
 - Notorious
 --- # Shopping list, inline format
 [Casablanca, Spellbound, Notorious]
```

### 해시

``` yaml
 --- # Block
 name: John Smith
 age: 33
 --- # Inline
 {name: John Smith, age: 33}
```

### Block Literals

#### Newlines preserved

``` yaml
 --- |
   There was a young fellow of Warwick
   Who had reason for feeling euphoric
       For he could, by election
       Have triune erection
   Ionic, Corinthian, and Doric 11
```

#### Newlines folded

``` yaml
 --- >
   Wrapped text
   will be folded
   into a single
   paragraph

   Blank lines denote
   paragraph breaks
```

### 해시의 리스트

``` yaml
 - {name: John Smith, age: 33}
 - name: Mary Smith
   age: 2
```

### 리스트의 해시

``` yaml
 men: [John Smith, Bill Jones]
 women:
   - Mary Smith
   - Susan Williams
```

## 구현

다음 언어에서 YAML을 이용할 수 있다:

  - [자바스크립트](../Page/자바스크립트.md "wikilink")
  - [오브젝티브-C](../Page/오브젝티브-C.md "wikilink")
  - [펄](../Page/펄.md "wikilink")
  - [PHP](../Page/PHP.md "wikilink")
  - [파이썬](../Page/파이썬.md "wikilink")
  - [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink") (YAML을 사실상의 직렬화 형식으로 이용한다. YAML은 버전 1.8 이후로부터 표준 라이브러리에 포함되었다.)
  - [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink")
  - [하스켈](../Page/하스켈.md "wikilink")
  - [XML](../Page/XML.md "wikilink")
  - [러스트](../Page/러스트_\(프로그래밍_언어\).md "wikilink")

## 따로 볼 것들

다른 단순화된 마크업 언어들이 있다:

  - [JSON](../Page/JSON.md "wikilink") : YAML과 같은 철학의 구현이며, 주석 스타일을 제외하고 매우 비슷하다.
  - [Simple Outline XML](https://ko.wikipedia.org/wiki/Simple_Outline_XML "wikilink")
  - [OGDL](https://ko.wikipedia.org/wiki/OGDL "wikilink")
  - [S-expression](https://ko.wikipedia.org/wiki/S-expression "wikilink")s
  - [plist](../Page/프로퍼티_리스트.md "wikilink"), [NEXTSTEP](https://ko.wikipedia.org/wiki/NEXTSTEP "wikilink")의 객체 직렬화 형식이다.

## 외부 링크

  - [YAML.org](http://www.yaml.org)
  - [YAML 명세서](http://www.yaml.org/spec/)
  - [YAML Cookbook](https://web.archive.org/web/20080509211926/http://yaml4r.sourceforge.net/cookbook/)
  - [YAML in Five Minutes](https://web.archive.org/web/20060618031422/http://yaml.kwiki.org/?YamlInFiveMinutes)
  - [YAML as a superset of JSON](https://web.archive.org/web/20080914015703/http://redhanded.hobix.com/inspect/yamlIsJson.html)

[분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink") [분류:데이터 직렬화 포맷](https://ko.wikipedia.org/wiki/분류:데이터_직렬화_포맷 "wikilink")