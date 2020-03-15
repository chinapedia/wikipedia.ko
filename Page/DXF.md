> This article is converted from Wikipedia: [DXF](https://ko.wikipedia.org/wiki/DXF).


**DXF**는 미국 오토데스크 사의 오토캐드 와 다른 수많은 캐드 소프트웨어들 간의 파일 교환을 위한 포맷이며, 캐드 데이터 상호 운용성을 위한 사실상([de facto](https://ko.wikipedia.org/wiki/de_facto "wikilink")) 표준이 되었다.

대한민국의 캐디안소프트가 개발한 캐디안(CADian)를 비롯하여 오픈소스 캐드인 [큐캐드(Qcad)등](../Page/QCad.md "wikilink") 많은 캐드(CAD) 개발사들이 오토캐드(AutoCAD)와의 호환성을 유지하기 위하여 이 포맷을 지원하고 있다.

## 파일 구조\[1\]

  - **HEADER** 섹션

<!-- end list -->

  -
    도면에 대한 일반 정보를 포함한다. 이 섹션은 AutoCAD 데이터베이스의 버전 번호와 다양한 시스템 변수로 구성된다. 각 매개변수는 변수 이름과 연관된 값을 포함하고 있다.

<!-- end list -->

  - **CLASSES** 섹션

<!-- end list -->

  -
    데이터베이스의 BLOCKS, ENTITIES 및 OBJECTS 섹션에서 인스턴스가 사용되는 응용프로그램 정의 클래스에 대한 정보를 보유하고 있다. 클래스 정의는 클래스 계층에 고정된다.

<!-- end list -->

  - **TABLES** 섹션

<!-- end list -->

  -

      -
        다음의 기호 테이블에 대한 정의를 포함한다.
        APPID(응용프로그램 식별 테이블)
        BLOCK_RECORD(블록 참조 테이블)
        DIMSTYLE(치수 스타일 테이블)
        LAYER(도면층 테이블)
        LTYPE(선종류 테이블)
        STYLE(텍스트 스타일 테이블)
        UCS(사용자 좌표계 테이블)
        VIEW(View table,테이블 보기)
        VPORT(뷰포트 구성 테이블)

<!-- end list -->

  - **BLOCKS** 섹션

<!-- end list -->

  -
    도면의 각 블록 참조를 구성하는 블록 정의 및 도면요소(entity- 점, 선, 면, 원, 텍스트 등 도면을 형성하는 각 그림 요소를 의미한다)를 포함한다.

<!-- end list -->

  - **ENTITIES** 섹션

<!-- end list -->

  -
    블록 참조(삽입 도면요소)와 함께 도면의 그래픽 객체(도면요소)를 포함한다.

<!-- end list -->

  - **OBJECTS** 섹션

<!-- end list -->

  -
    도면의 비그래픽 객체를 포함한다. 도면요소 또는 기호 테이블 레코드 또는 기호 테이블이 아닌 객체는 모두 이 섹션에 저장된다. OBJECTS 섹션에 표시되는 항목의 예로는 다중선 스타일 및 그룹이 포함된 라이브러리를 들 수 있다.

<!-- end list -->

  - **THUMBNAILIMAGE** 섹션

<!-- end list -->

  -
    도면의 미리보기 이미지 데이터를 포함한다. 이 섹션은 선택 사항이다.

<!-- end list -->

  - **END OF FILE**

## 파일형식\[2\]

**DXF**는 오토데스크사의 오토캐드를 포함해서 [CAD](https://ko.wikipedia.org/wiki/CAD "wikilink") 프로그램들이 자사의 캐드파일을 가독성이 가능한 텍스트 파일([ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink"))로 변환하는 [파일 포맷이다](https://ko.wikipedia.org/wiki/파일_포맷 "wikilink").

소스가 공개된 캐드 형식(파일 포맷)으로 되어 있어서 사실상 산업표준으로 널리 유용하게 사용되고 있다.

<small>DXF 파일 형식

-----

  -
    0 **(헤더 섹션의 시작)**
    SECTION
    2
    HEADER
      -
        <헤더 변수 항목들 >
    0
    ENDSEC **(헤더 섹션의 끝)**

<!-- end list -->

  -
    0*' (테이블 섹션의 시작)*'
    SECTION
    2
    TABLES
    0
    TABLE
    2
    VPORT
    70
    (viewport테이블 최대항목수)
      -
        <viewport 테이블 변수 항목들>
    0
    ENDTAB
    0
    TABLE
    2
    APPID, DIMSTYLE, LTYPE, LAYER, STYLE, UCS, VIEW, VPORT
    70
    (테이블 최대 항목수)
      -
        <테이블 항목들 >
    0
    ENDTAB
    0
    ENDSEC **(테이블 섹션의 끝)**

<!-- end list -->

  -
    0 **(블럭섹션의 시작)**
    SECTION
    2
    BLOCKS
      -
        <정의 도면요소들 >
    0
    ENDSEC **(블럭섹션의 끝)**

<!-- end list -->

  -
    0 **(엔티티섹션의 시작)**
    SECTION
    2
    ENTITIES
      -
        <도면 요소들 >
    0
    ENDSEC **(엔티티섹션의 끝)**

<!-- end list -->

  -
    0
    EOF **(파일의 끝)**

-----

</small>

## 같이 보기

  - [오토데스크](https://ko.wikipedia.org/wiki/오토데스크 "wikilink")
  - [오토캐드](../Page/오토캐드.md "wikilink")
  - [큐캐드(Qcad)](../Page/QCad.md "wikilink")
  - [CAD](../Page/컴퓨터_지원_설계.md "wikilink")

## 참고

## 외부 링크

  - [DXF 규격](https://web.archive.org/web/20070905200720/http://usa.autodesk.com/adsk/servlet/item?siteID=123112&id=8446698)

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink")

1.  <http://docs.autodesk.com/ACD/2011/KOR/filesDXF/WS1a9193826455f5ff18cb41610ec0a2e719-796b.htm>
2.  <http://webcache.googleusercontent.com/search?q=cache:fEKnE4QT5OMJ:hmjkor.tistory.com/attachment/cfile27.uf%401708064E502C7767338D02.doc+&cd=2&hl=ko&ct=clnk&gl=kr&client=firefox-b>