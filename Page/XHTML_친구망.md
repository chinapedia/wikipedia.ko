> This article is converted from Wikipedia: [XHTML ](https://ko.wikipedia.org/wiki/XHTML_).


**XFN**(XHTML Friends Network; XHTML 친구망)은 하이퍼링크를 이용해 인간 관계를 표현하는 간단한 수단으로 [글로벌 멀티미디어 프로토콜 그룹](https://ko.wikipedia.org/wiki/글로벌_멀티미디어_프로토콜_그룹 "wikilink")(GMPG)이 개발하였다. 최근에 블로그가 웹 분야에서 빠른 성장을 보이고 있는데, XFN은 단순히 <a href> 태그에 'rel' 속성을 추가함으로써, 작성자가 다른 사람들과의 관계를 표현할 수 있는 방법을 제공한다. 다음이 한 예이다.

``` html5
<a href="http://jeff.example.org" rel="friend met">
```

## 소개

XFN은 링크에 인간적인 면을 담는다. 갈수록 많은 사람들이 다양한 노드(node) 사이의 관계를 보여주는 [테크노라티](https://ko.wikipedia.org/wiki/테크노라티 "wikilink")와 [피드스터](https://ko.wikipedia.org/wiki/피드스터 "wikilink") 같은 사회적 네트워크 서비스를 이용하기 시작하고 있다. 이 같은 서비스들은 노드 사이의 기계적인 관계를 밝히는 데는 유용하지만, 인간적 관계에 대해서는 그렇지 못하다.

XFN은 개인적 관계의 수준을 정의된 집합으로 나타내는 방법으로 개개의 관계를 대략적으로 보여준다. [HTML](../Page/HTML.md "wikilink")과 [XHTML](../Page/XHTML.md "wikilink") 문서에서는 이 같은 관계의 수준이 하이퍼링크의 rel 속성으로 나타난다. XFN을 통해 작성자는 자신이 읽은 웹로그중의 어떤 것들이 친구(물리적 만남이 있었거나, 혹은 다른 어떤 관계든지)에 속하는지를 표현할 수 있다. XFN 관계 형식은 순서에 상관이 없으며, 블로그 모임이나 링크 페이지에 인간적인 면을 덧붙이며, 웹로그의 일반적인 특징이 되어가고 있다.

현대적 기능을 갖춘 브라우저에서 XFN을 사용하는 작성자는 특정한 유형의 링크에 스타일을 쉽게 지정할 수 있다. 말하자면 friend(친구)에 대해서는 굵은 글씨를, co-worker(직장 동료)에 대해서는 기울임 글씨를 적용하는 식이다.

## XFN 1.1 프로파일

  - 교우 관계 (하나를 선택)
      - **contact** - 접촉할 수단을 아는 사람.
      - **acquaintance** - 서로 인사나 짧은 대화가 있어왔던 사람.
      - **friend** - 친구. 알고 있는 동료나 동향인.

<!-- end list -->

  - 물리적 관계
      - **met** - 실제로 만난 적이 있는 사람.

<!-- end list -->

  - 직업상 관계
      - **co-worker** - 동업자 혹은 직장 동료.
      - **colleague** - 같은 학문/활동 분야에 몸 닮고 있는 사람.

<!-- end list -->

  - 지리적 관계 (하나를 선택)
      - **co-resident** - 공통 거주자. 같은 (길)거리에 있는 사람.
      - **neighbor** - 근방에 사는 이웃.

<!-- end list -->

  - 가족 (하나를 선택)
      - **child** - 친자 혹은 양자, 또는 보호자 관계인 사람.
      - **parent** - child의 역관계. 부모.
      - **sibling** - 공통된 부모를 가진 사람. 형제, 자매, 남매.
      - **spouse** - 결혼한 사람. 배우자.
      - **kin** - 상대적으로 확장된 가족의 일원으로 간주되는 사람. 친척.

<!-- end list -->

  - 연애 관계
      - **muse** - 영감을 가져다주는 사람. 뮤즈.
      - **crush** - 자신이 완전히 빠져버린 사람.
      - **date** - 만나고 있는 사람.
      - **sweetheart** - 매우 친밀하며, 헌신적이고 단독적인 관계. 연인.

<!-- end list -->

  - 신원
      - **me** - 자신의 다른 URL에 대한 링크. 다른 관계와 같이 표시될 수 없다.

### 예

지미 웨일스(Jimmy Wales)가 만났던 한 친구의 사이트에 대한 링크는 다음과 같이 관계를 표현할 수 있다.

``` html5
<a href="http://www.jimmywales.com/" rel="friend met">지미 웨일스</a>
```

## 같이 보기

  - [FOAF](https://ko.wikipedia.org/wiki/FOAF "wikilink")
  - [DOAC](https://ko.wikipedia.org/wiki/DOAC "wikilink")
  - [마이크로포맷](../Page/마이크로포맷.md "wikilink")

## 외부 링크

  - [GMPG의 XFN 홈페이지](http://gmpg.org/xfn/)
  - [XFN 1.1 프로파일](http://gmpg.org/xfn/11)
  - [RubHub](http://rubhub.com/) - XFN 검색 엔진
  - [XHTML 프렌즈](http://xhtmlfriends.net/) - 사회적 네트워크 / 지리적인 시각화 서비스와 검색 엔진
  - [XFN 생성기](http://gmpg.org/xfn/creator) XFN 하이퍼링크 생성기
  - [마이크로포맷](http://microformats.org/)

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink")