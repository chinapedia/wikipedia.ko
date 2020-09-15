> This article is converted from Wikipedia: [국가서지LOD](https://ko.wikipedia.org/wiki/국가서지LOD).


**국가서지 LOD**는 [국립중앙도서관](../Page/국립중앙도서관.md "wikilink")에서 제공하는 [공공 데이터 개방](../Page/공공_데이터_개방.md "wikilink") 서비스이다.

[국립중앙도서관](../Page/국립중앙도서관.md "wikilink")은 국가대표도서관으로서 국가지식 정보자원을 망라적으로 수집하며, 이 자원에 대한 정보를 [국가서지](https://web.archive.org/web/20181204093802/http://www.nl.go.kr/nation/)로 체계화하고 있다.

이렇게 구축된 국가서지 데이터를 정보수요자가 필요에 따라 활용할 수 있도록 표준형식에 맞게 개방하여 데이터 중심의 의미적 연결성을 확보하고 다양한 웹 자원과 자유롭게 연계, 융합하여 도서관 및 웹 데이터를 더욱 풍부하게 만드는 기반을 조성하고자 개방형 연결 데이터(Linked Open Data)로 발행하여 제공하고 있다.

## 데이터 구성

국가서지 LOD에서 서비스 되는 데이터는 [국립중앙도서관](../Page/국립중앙도서관.md "wikilink")의 서지 및 주제명, 저자명과 전국의 도서관 정보를 기존의 (KOR)MARC 또는 DBMS에서 [RDF](../Page/자원_기술_프레임워크.md "wikilink") 형식으로 변환하여 웹상에 Linked Open Data 형식으로 발행된다. 각 데이터셋을 다운로드 할 수 있도록 트리플 단위로 제공할 뿐 아니라, 온라인 목록 형태로도 표출한다.

발행 데이터는 [JASON](../Page/JSON.md "wikilink"), RDF/XML, [Turtle](https://ko.wikipedia.org/wiki/Turtle "wikilink"), N3, nTriple과 같은 다양한 기계가독형 데이터 형식으로 제공한다.

### URI 체계

국가서지 LOD에서 식별을 위해 사용하는 [URI](../Page/통합_자원_식별자.md "wikilink") 체계는 다음과 같다.

  - [인스턴스](https://ko.wikipedia.org/wiki/인스턴스 "wikilink") 체계 : http://lod.nl.go./resource/<id>
  - Class & Property 체계 : http://lod.nl.go.kr/ontology/<name>
  - 가독성 URI 체계 (주제명) : http://lod.nl.go.kr/subject/<주제명>
  - 가독성 URI 체계 (저자명) : http://lod.nl.go.kr/author/<저자명>
  - 기타 : http://lod.nl.go.kr/<type> /<id or name>

### 온톨로지

[국립중앙도서관](../Page/국립중앙도서관.md "wikilink")의 데이터를 RDF로 표현하기 위한 [온톨로지](../Page/온톨로지.md "wikilink") 스키마로 BIBO, SKOS, FOAF를 활용하였다. 서지 데이터는 bibo:Document 클래스를 기반으로 각각의 분류에 맞게 생성하였으며, 주제명은 SKOS, 저자명은 FOAF를 기반으로 표현하였다.

### SPARQL Endpoint

국가서지 LOD 정보에 질의를 통해 접근 할 수 있도록 [SPARQL](../Page/SPARQL.md "wikilink") Endpoint 를 제공한다.

### 데이터셋(dataset)

국가서지 LOD는 다음과 같은 데이터셋으로 구성되어 있다.

  - 국립중앙도서관 LOD 서지(단행물, 연속간행물, 온라인자료, 학술기사)
  - 국립중앙도서관 LOD 저자명
  - 국립중앙도서관 LOD 주제명
  - 국립중앙도서관 LOD 도서관 정보
  - 국립중앙도서관 LOD 인터링킹 정보

## 응용 서비스

국가서지 LOD에서는 발행한 데이터의 활용 사례로 다양한 응용 서비스를 제공하고 있다.

### 데이터 컬렉션

데이터 컬렉션은 [국립중앙도서관](../Page/국립중앙도서관.md "wikilink")의 국가서지 LOD에 [SPARQL](../Page/SPARQL.md "wikilink") 질의를 적용하여 구성한 서비스이다. 특정 주제나 자료의 형태 등 사용자의 요구에 맞는 메타데이터를 추출하여 컬렉션 목록을 제공한다. 현재 ‘사진으로 보는 저자’, ‘어린이 문학상 컬렉션’, ‘전시도록 컬렉션’, ‘시청각자료 컬렉션’이 있다.

### 대한민국 도서관 지도

국가서지 LOD에서 제공하는 도서관 정보와 지도를 결합하여 제공하는 서비스이다. 책 제목이나 ISBN 검색을 통해 찾고자 하는 자료의 위치 정보를 알려준다. 각 도서관의 위치, 관종구분, 휴관일, 홈페이지 등의 정보도 확인할 수 있다.

### 고신문 디지털 컬렉션

고신문 디지털 컬렉션은 [국립중앙도서관](../Page/국립중앙도서관.md "wikilink")이 보유한 고신문을 LOD 기반의 기계 질의를 통해 기사 단위로 구축한 목록이다. 일제강점기, 군정기, 독립운동, 해방 등 시대별 및 주제별 탐색을 제공한다.

### KDC 주제별 탐색

[국립중앙도서관](../Page/국립중앙도서관.md "wikilink")의 단행본 메타데이터에 KDC([한국십진분류법](../Page/한국십진분류법.md "wikilink"))에 따라 체계적으로 접근할 수 있는 탐색 브라우저이다. KDC 4, 5, 6판의 트리를 제공하며, 각 판별 분류 트리를 통해 목(目)구분(1000구분)까지 탐색 할 수 있다.

## LODAC (Linked Open Data Annual Conference)

[국립중앙도서관](../Page/국립중앙도서관.md "wikilink")에서는 국가서지 LOD와 연계하여 매년 LODAC(Linked Open Data Annual Conference)를 개최한다. [공공 데이터](../Page/공공_데이터.md "wikilink"), [링크드 데이터와](https://ko.wikipedia.org/wiki/링크드데이터 "wikilink") 더불어 인공지능이나 loT 등 데이터 기반의 다양한 주제들에 대해서 논의하며, LOD 활용을 위한 워크숍도 열린다. 2018년에는 ‘오픈데이터, 디지털 트랜스포메이션을 말하다.’라는 주제로 진행되었다.

## 외부 링크

  - [국가서지 웹사이트](https://web.archive.org/web/20181204093802/http://www.nl.go.kr/nation/)
  - [LODAC 웹사이트](https://web.archive.org/web/20191229090002/http://www.lodac.kr/)

[분류:서지학](https://ko.wikipedia.org/wiki/분류:서지학 "wikilink")