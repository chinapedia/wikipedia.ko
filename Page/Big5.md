> This article is converted from Wikipedia: [Big5](https://ko.wikipedia.org/wiki/Big5).


**Big-5** 또는 **Big5**는 [타이완](../Page/타이완.md "wikilink"), [홍콩](../Page/홍콩.md "wikilink"), [마카오](../Page/마카오.md "wikilink")에서 [정체자](https://ko.wikipedia.org/wiki/정체자 "wikilink")에 쓰이는 [중국어 문자 인코딩](https://ko.wikipedia.org/wiki/중국어_문자_인코딩 "wikilink") 방식이다.

[간체자](https://ko.wikipedia.org/wiki/간체자 "wikilink")를 사용하는 [중국 대륙은](https://ko.wikipedia.org/wiki/중국_대륙 "wikilink") [GB](https://ko.wikipedia.org/wiki/GBK "wikilink") 문자 집합을 대신 사용한다.

Big5는 이를 개발한 타이완 내 5개 기업의 컨소시엄에서 나온 이름이다.\[1\] 2016년 2월 기준 모든 웹 페이지 중 0.1%가 Big5를 사용한다.\[2\]\[3\]

## 구조

오리지널 Big5 문자 집합의 정렬 순서는 사용 주기, 획순, 그리고 강희자전 순이다.

오리지널 Big5 문자 집합은 흔히 사용되는 수많은 문자들이 빠져있었다. 이 문제를 해결하기 위해 각 벤더는 자체 확장을 개발하였다. ETen 확장은 대중화를 통해 현재의 Big5 표준의 일부로 되었다.

Big5의 구조는 [ISO 2022](https://ko.wikipedia.org/wiki/ISO_2022 "wikilink") 표준을 준수하지 않으며, [Shift JIS](../Page/Shift_JIS.md "wikilink") 인코딩과 어느 정도 유사하다. 다음 구조의 [더블 바이트 문자 집합](https://ko.wikipedia.org/wiki/더블_바이트_문자_집합 "wikilink")(DBCS)로 되어 있다.

|                  |                                                    |
| ---------------- | -------------------------------------------------- |
| 첫 바이트 ("리드 바이트") | 0x81 \~ 0xfe (사용자 정의에 속하지 않은 문자들의 경우 0xa1 \~ 0xf9) |
| 두 번째 바이트         | 0x40 \~ 0x7e, 0xa1 \~ 0xfe                         |

(앞의 0x는 16진수를 의미한다)

## 확장

### 벤더의 확장

  - [ETen](https://ko.wikipedia.org/wiki/ETen "wikilink")(倚天)
  - [코드 페이지 950](../Page/코드_페이지_950.md "wikilink")
  - ChinaSea(中國海字集)
  - 사쿠라 폰트
  - Unicode-at-on(Unicode補完計畫, 과거 이름: BIG5 확장)
  - OPG

### 공식 확장

  - Taiwan Ministry of Education font(臺灣教育部造字檔)
  - Taiwan Council of Agriculture font(臺灣農委會常用中文外字集)
  - Big5+
  - Big-5E
  - Big5-2003
  - CDP(Chinese Data Processing font, 漢字構形資料庫)
  - [HKSCS](https://ko.wikipedia.org/wiki/HKSCS "wikilink")(Hong Kong Supplementary Character Set)

## 같이 보기

  - [유니코드](../Page/유니코드.md "wikilink")

## 각주

## 외부 링크

  - [Mozilla and the Big5 Family of Encodings](http://moztw.org/docs/big5/): an overview of Big5 encodings with code charts for each extension and relevant Firefox bugs. <small>(Traditional Chinese)</small>
  - [Big5 character code table](http://ash.jp/code/cn/big5tbl.htm)

[분류:문자 집합](https://ko.wikipedia.org/wiki/분류:문자_집합 "wikilink")

1.  [chinese mac Character Sets](http://chinesemac.org/pages/character_sets.html)
2.  [Historical trends in the usage of character encodings, December 2016](http://w3techs.com/technologies/history_overview/character_encoding)
3.  [Frequenty Asked Questions](http://w3techs.com/faq)