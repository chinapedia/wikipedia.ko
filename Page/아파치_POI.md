> This article is converted from Wikipedia: [ POI](https://ko.wikipedia.org/wiki/_POI).


**아파치 POI**()는 [아파치 소프트웨어 재단에서](../Page/아파치_소프트웨어_재단.md "wikilink") 만든 라이브러리로서 [마이크로소프트 오피스](https://ko.wikipedia.org/wiki/마이크로소프트_오피스 "wikilink") [파일 포맷을](https://ko.wikipedia.org/wiki/파일_포맷 "wikilink") 순수 [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") 언어로서 읽고 쓰는 기능을 제공한다. 주로 [워드](https://ko.wikipedia.org/wiki/마이크로소프트_워드 "wikilink"), [엑셀](https://ko.wikipedia.org/wiki/엑셀 "wikilink"), [파워포인트](https://ko.wikipedia.org/wiki/파워포인트 "wikilink")와 파일을 지원하며 최근의 오피스 포맷인 Office Open XML File Formats \[1\] (OOXML, 즉 xml 기반의 \*.docx, \*.xlsx, \*.pptx 등) 이나 [아웃룩](https://ko.wikipedia.org/wiki/마이크로소프트_아웃룩 "wikilink"), [비지오](../Page/마이크로소프트_비지오.md "wikilink"), [퍼블리셔](https://ko.wikipedia.org/wiki/퍼블리셔 "wikilink") 등으로 지원 파일 포맷을 늘려가고 있다.

## 역사

**POI** 라는 이름은 "Poor Obfuscation Implementation"의 줄임말 \[2\] 로서 기존의 [마이크로소프트 오피스의](https://ko.wikipedia.org/wiki/마이크로소프트_오피스 "wikilink") 파일 포맷(OLE 2 Compund Document Format : OLE2)이 일부러 해독하기 힘들게 만들어 놓은것 같음에도 불구하고 실제로 [리버스 엔지니어링되어](../Page/리버스_엔지니어링.md "wikilink") 사용할 수 있게 되었음을 의미한다. POI 프로젝트 내부에서 사용하는 각 모듈의 이름들 또한 이와 비슷하게 유머섞인 이름들로 되어있다.

## Office Open XML 지원

POI 는 3.5 버전부터 ISO/IEC 29500:2008 [오피스 오픈 XML](../Page/오피스_오픈_XML.md "wikilink") 파일 포맷을 지원한다. [SourceSense](http://www.sourcesense.com/) 라는 [오픈소스](https://ko.wikipedia.org/wiki/오픈소스 "wikilink") 업체로부터 많은 지원을 받았는데 이 업체는 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")와 협력하여 개발을 한 것으로 알려져 있다. \[3\]

## 아키텍처

Apache POI는 다음과 같은 하위 [컴포넌트](https://ko.wikipedia.org/wiki/컴포넌트 "wikilink")로 구성되어 있다.

  - POIFS(Poor Obfuscation Implementation File System) : [마이크로소프트 오피스의](https://ko.wikipedia.org/wiki/마이크로소프트_오피스 "wikilink") OLE 2 Compound document 파일 포맷을 읽고 쓰는 컴포넌트. 모든 오피스 파일 포맷은 OLE2 방식이므로 하위 모든 컴포넌트의 기반이 된다.
  - HSSF(Horrible SpreadSheet Format) : [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink") [엑셀](https://ko.wikipedia.org/wiki/엑셀 "wikilink") 파일포맷을 읽고 쓰는 컴포넌트로서 엑셀 97버전부터 현재까지 지원한다.
  - XSSF(XML SpreadSheet Format) : [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink") [엑셀](https://ko.wikipedia.org/wiki/엑셀 "wikilink") 2007부터 지원하는 [오피스 오픈 XML](../Page/오피스_오픈_XML.md "wikilink") 파일 포맷인 \*.xlsx 파일을 읽고 쓰는 컴포넌트이다.
  - HPSF(Horrible Property Set Format) : 오피스 파일의 문서요약 정보를 읽는데 사용되는 컴포넌트이다.
  - HWPF(Horrible Word Processor Format) : [마이크로소프트 워드](https://ko.wikipedia.org/wiki/마이크로소프트_워드 "wikilink") 97(\*.doc) 파일을 읽고 쓰는데 사용되는 컴포넌트이다. 아직까지는 개발 초기단계이다.
  - HSLF(Horrible Slid Layout Format) : [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink") [파워포인트](https://ko.wikipedia.org/wiki/파워포인트 "wikilink") 파일을 읽고 쓰는데 사용되는 컴포넌트이다.
  - HDGF(Horrible DiaGram Format) : [마이크로소프트 비지오](../Page/마이크로소프트_비지오.md "wikilink") 파일을 읽는데 사용하는 컴포넌트이다.
  - HPBF(Horrible PuBlisher Format) : [마이크로소프트 퍼블리셔](../Page/마이크로소프트_퍼블리셔.md "wikilink") 파일을 다루는데 사용되는 컴포넌트이다.
  - HSMF(Horrible PuBlisher Format) : [마이크로소프트 아웃룩에서](https://ko.wikipedia.org/wiki/마이크로소프트_아웃룩 "wikilink") 사용되는 \*.msg 파일을 다루는데 사용되는 컴포넌트이다.
  - DDF(Dreadful Drawing Format) : [마이크로소프트 오피스에서](https://ko.wikipedia.org/wiki/마이크로소프트_오피스 "wikilink") 사용되는 이미지 파일을 읽어오는데 사용하는 컴포넌트이다.

HSSF 컴포넌트가 가장 안정적이고 많은 기능을 지원하며 다른 컴포넌트들은 사용은 가능하나 아직까지는 개발 단계이다.

## 같이 보기

  - [오피스 오픈 XML](../Page/오피스_오픈_XML.md "wikilink")

## 참고 문헌

[분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:아파치 소프트웨어 재단 프로젝트](https://ko.wikipedia.org/wiki/분류:아파치_소프트웨어_재단_프로젝트 "wikilink") [분류:자바 라이브러리](https://ko.wikipedia.org/wiki/분류:자바_라이브러리 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink")

1.  [Standard ECMA-376, Office Open XML File Formats](http://www.ecma-international.org/publications/standards/Ecma-376.htm)
2.
3.