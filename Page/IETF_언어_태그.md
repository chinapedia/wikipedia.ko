> This article is converted from Wikipedia: [IETF  ](https://ko.wikipedia.org/wiki/IETF__).


**IETF 언어 태그**()는 [BCP](https://ko.wikipedia.org/wiki/BCP "wikilink") 47(현재는 [RFC 5646](http://tools.ietf.org/html/rfc5646)과 [RFC 4647](http://tools.ietf.org/html/rfc4647))에 따라서 정의되는 기술 사양이다. 이것은 [HTTP](https://ko.wikipedia.org/wiki/Hypertext_Transfer_Protocol "wikilink")\[1\], [HTML](https://ko.wikipedia.org/wiki/HTML "wikilink")\[2\], [XML](https://ko.wikipedia.org/wiki/XML "wikilink")\[3\], [PNG](https://ko.wikipedia.org/wiki/PNG "wikilink")\[4\] 등과 같은 대부분의 기술 표준에서 사용된다.

## 서식

언어 태그는 하이픈에 따라서 나뉘는, 하나 이상의 ‘하위 태그’로부터 구성된다. 일반적으로는 다음의 순서로 쓰인다.

  - (언어)

  - (문자 체계)

  - (지역)

  - (변이형)

  - (확장)

  - (개인용)

따라서, 서식은 대체로 다음과 같이 표기된다.(이 중  태그만 필수이다)

각각의 하위 태그는 아래의 규격에서 파생되고 있다.

  - : [ISO 639-1](https://ko.wikipedia.org/wiki/ISO_639-1 "wikilink"), [ISO 639-2](https://ko.wikipedia.org/wiki/ISO_639-2 "wikilink"), [ISO 639-3](https://ko.wikipedia.org/wiki/ISO_639-3 "wikilink"), [ISO 639-5](https://ko.wikipedia.org/wiki/ISO_639-5 "wikilink")\[5\]

  - : [ISO 15924](https://ko.wikipedia.org/wiki/ISO_15924 "wikilink")

  - : [ISO 3166-1 alpha-2](https://ko.wikipedia.org/wiki/ISO_3166 "wikilink"), [UN M.49](https://ko.wikipedia.org/wiki/UN_M.49 "wikilink")

  - : (독자이므로 파생처의 규격 없음)

  - : (추후 확장을 위한 예약 영역이므로 파생처의 규격 없음)

  - : (개인적인 사용 부분이므로 파생처의 규격 없음)

IANA에 의해서 관리되고 있다. [Language Subtag Registry(언어 하위 태그 레지스트리)](http://www.iana.org/assignments/language-subtag-registry)에는 현재 공개되어 있는 유효한 하위 태그의 목록이 있다.

하위 태그에서는 알파벳의 대소문자를 구별하지 않지만, 사양에서는 언어 하위 태그 레지스티리와 같은 방법으로, 즉  하위 태그에 대해서는 모든 것이 대문자이며,  하위 태그에 대해서는 머릿글자만이 대문자이며, 그 외의 모든 하위 태그에 대항서는 소문자로 작성하는 것을 권장하고 있다.

언어 태그의 사용방법으로 자주 보이는 스타일은 그저  하위 태그만을 사용하지만,  하위 태그와  하위 태그를 사용하는 방법이다. 예를들면, `en`은 단일한  하위 태그(ISO 639-1에서)로 구성되며, [영어](https://ko.wikipedia.org/wiki/영어 "wikilink")를 나타낸다. 한편, `en-CA`는  하위 태그 후에  하위 태그 `CA`(ISO 3166-1에서)를 붙여서 구성하며, 캐나다 영어를 나타낸다.

## 역사

IETF 언어 태그는 [1995년](https://ko.wikipedia.org/wiki/1995년 "wikilink") 5월 발행한 [RFC 1766](http://tools.ietf.org/html/rfc1766)에서 처음으로 정의됐다. 이것은 [2001년](https://ko.wikipedia.org/wiki/2001년 "wikilink") 1월에 [RFC 3066](http://tools.ietf.org/html/rfc3066)으로 치환됐다. 이것은 [ISO 639-2](https://ko.wikipedia.org/wiki/ISO_639-2 "wikilink") 코드를 추가해서(이전에는 ISO 639-1 코드만이 허용되고 있었다), 처음으로 하위 태그에 숫자를 사용하는 것을 인정했다.

사양의 다음 판은 [2006년](https://ko.wikipedia.org/wiki/2006년 "wikilink") 9월 발행한 [RFC 4646](http://tools.ietf.org/html/rfc4646)(사양의 주요부분)과 [RFC 4647](http://tools.ietf.org/html/rfc4647)(매칭의 태도에 대해서)이였다. RFC 4646은 언어 태그에 따라서 구조화된 서식을 도입하고 이전부터 사용되고 있던 ISO 639(part 1과 2)와 ISO 3166에 더해서 [ISO 15924와](https://ko.wikipedia.org/wiki/ISO_15924 "wikilink") [UN M.49를](https://ko.wikipedia.org/wiki/UN_M.49 "wikilink") 이용하고 있으며, 하위 태그의 레지스트리를 오래된 것에서 새로운 것으로 바뀌어 있다. 또한 이 이전에 정의되어 있던 태그로 새로운 구조에 적합하지 않은 것에 대해서는 RFC 3066과의 호환성을 유지하기 위해서 계승되어 있다.

IETF 워킹 그룹은 사양의 다음 판을 준비하고 있는 바 있으며, 현재 승인 작업 중이다. 이 판의 주된 목적은 언어 하위 태그 레지스트에 [ISO 639-3를](https://ko.wikipedia.org/wiki/ISO_639-3 "wikilink") 취하는 것에 있다\[6\].

## 언어 태그의 예

아래는 BCP47로부터 발췌한 것이다\[7\].

  - 하위 태그만:

      - (독일어)
      - (일본어)
      - (grandfathered 태그의 예)

  - \-:

      - (중국어 (번체자))
      - (중국어 (간체자))
      - (세르비아어 (키릴 문자))
      - (세르비아어 (라틴 문자))

  - \--:

      - (중국 대륙에서 사용되는 중국어 (간체자))
      - (세르비아 몬테네그로에서 사용되는 세르비아어 (라틴 문자))

  - \-:

      - (슬로베니아어 Nadiza 방언)

  - \--:

      - (스위스에서 사용되는 독일어, 1901년 [맞춤법](https://ko.wikipedia.org/wiki/맞춤법 "wikilink")에 사용된 독일어)
      - (이탈리아에서 사용되는 슬로베니아 Nadiza 방언)

  - \---:

      - (이탈리아에서 사용되는 슬로베니아어 (라틴문자) Nadiza 방언. 주: `sl`은 암묵한 가운데 `Latn`를 포함하고 있지만 이 태그는 권종하지 않는다)

  - \-：

      - (영어 (미국))
      - (스페인어 (라틴 아메리카), UN 지역 코드 이용)

등.

## 각주

## 같이 보기

  - [IETF](https://ko.wikipedia.org/wiki/IETF "wikilink")

## 외부 링크

  - [BCP 47](http://tools.ietf.org/rfc/bcp/bcp47.txt) - 현재의 사양

  - [Language Subtag Registry (언어 하위 태그 레지스트리)](http://www.iana.org/assignments/language-subtag-registry) - IANA에 의해서 관리

  - [검색 툴](http://r12a.github.io/apps/subtags/)

  - [Language tags in HTML and XML](http://www.w3.org/International/articles/language-tags/Overview.en.php) - W3C에 의한 개요 설명

  - [Language Tags](http://www.langtag.net/) - 비공식 사이트, 여러 툴이 있다

  - [IANA Language Subtag Registry Search](http://rishida.net/utils/subtags/) - 비공식 사이트, 하위 태그를 검색할 수 있다.

[1766](https://ko.wikipedia.org/wiki/분류:RFC "wikilink") [분류:ISO 표준](https://ko.wikipedia.org/wiki/분류:ISO_표준 "wikilink")

1.  [RFC 2616: Hypertext Transfer Protocol -- HTTP/1.1, section 3.10](http://tools.ietf.org/html/rfc2616#section-3.10)
2.  [HTML 4.01 Specification, section 8.1](http://www.w3.org/TR/html401/struct/dirlang.html#h-8.1)
3.  [Extensible Markup Language (XML) 1.0 (Fourth Edition), section 2.12](http://www.w3.org/TR/REC-xml/#sec-lang-tag)
4.  [Portable Network Graphics (PNG) Specification (Second Edition), section 11.3.4.5](http://www.w3.org/TR/PNG/#11iTXt)
5.  [RFC 5646, section 2.2.1](http://tools.ietf.org/html/rfc5646#section-2.2.1)
6.
7.  Examples of Language Tags, *[Tags for Identifying Languages](http://tools.ietf.org/html/bcp47)*, 2006.