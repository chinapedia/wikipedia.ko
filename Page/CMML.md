> This article is converted from Wikipedia: [CMML](https://ko.wikipedia.org/wiki/CMML).


**연속 미디어 마크업 언어**(, CMML)는 비디오와 오디오에 사용되는 [마크업 언어이다](../Page/마크업_언어.md "wikilink"). [HTML](../Page/HTML.md "wikilink")이 텍스트를 다룬다면, CMML은 비디오와 오디오 미디어를 다룬다. CMML은 본질적으로 시간이 지정된 텍스트 코덱이다. 이를 통해 '클립'이라고 불리는 일시적 부분으로 나누고 시간 연속적으로 샘플링된 데이터 파일을 구조화하는 것이 가능하다. 그리고 부가적인 정보를 클립과 함께 제공한다. 이 정보는 HTML과 비슷하며 본질적으로 오디오와 비디오 파일의 텍스트적 표현이다. CMML은 다른 바이너리 파일들에서 텍스트적 검색을 가능하게 한다.

CMML은, 자막 및 시간지정 메타미디어를 제공하기 위해서, 모든 [Ogg](../Page/Ogg.md "wikilink") 미디어 포맷과 사용하는 것이 가능하다.

## CMML 컨텐츠 예제

``` xml
<cmml>
  <stream timebase="0">
    <import src="galaxies.ogv" contenttype="video/ogg"/>
  </stream>
  <head>
    <title>Hidden Galaxies</title>
    <meta name="author" content="CSIRO"/>
  </head>
  <clip id="findingGalaxies" start="15">
    <a href="http://www.aao.gov.au/galaxies.anx#radio">
      Related video on detection of galaxies
    </a>
    <img src="galaxy.jpg"/>
    <desc>What's out there?</desc>
    <meta name="KEYWORDS" content="Radio Telescope"/>
  </clip>
</cmml>
```

## 외부 링크

  - [CMML 개요](https://web.archive.org/web/20130308071304/http://wiki.xiph.org/index.php/CMML)
  - CMML 문서 원본과 추가적인 표준, 기록 [Annodex CMML 표준 버전 2.1](https://web.archive.org/web/20130329181659/http://annodex.net/TR/draft-pfeiffer-cmml-03.html)

[분류:Xiph.Org 프로젝트](https://ko.wikipedia.org/wiki/분류:Xiph.Org_프로젝트 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")