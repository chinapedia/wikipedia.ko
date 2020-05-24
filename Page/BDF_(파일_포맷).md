> This article is converted from Wikipedia: [BDF \(파일 포맷\)](https://ko.wikipedia.org/wiki/BDF_\(파일_포맷\)).


Adobe 의 BDF(Glyph Bitmap Distribution Format)은 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink") [글꼴](../Page/글꼴.md "wikilink") 을 저장하기위한 [파일 형식이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink"). 내용은 컴퓨터 및 인간이 읽을 수있는 [텍스트 파일](../Page/텍스트_파일.md "wikilink") 형식을 취한다. BDF는 일반적으로 Unix 계열의 [X 윈도 시스템](../Page/X_윈도_시스템.md "wikilink") 환경에서 사용된다. 주로 보다 효율적이고 [오픈타입](../Page/오픈타입.md "wikilink")(OpenType) 및 [트루타입](../Page/트루타입.md "wikilink")(TrueType) 글꼴과 같은 확장 가능한 글꼴로 [PCF](https://ko.wikipedia.org/wiki/PCF_\(파일_포맷\) "wikilink") 글꼴 형식으로 대체되었다.

## 포맷구성

2013 년 현재 BDF의 현재 버전은 2.2이다. 향후 개정은 예상되지 않고있다. 이전 버전은 CBDF(Character Bitmap Distribution Format)라고 불렸었다.

1988년 **X 컨소시엄**은 BDF 2.1을 X 윈도우 화면 글꼴의 표준으로 채택했지만\[1\] , [X 윈도우는](https://ko.wikipedia.org/wiki/X_윈도우_시스템 "wikilink") [PCF](https://ko.wikipedia.org/wiki/PCF_\(파일_포맷\) "wikilink") , [오픈타입](../Page/오픈타입.md "wikilink") 및 [트루타입](../Page/트루타입.md "wikilink")과 같은 다른 글꼴 표준으로 크게 옮겨졌다.

버전 2.2에는 비 [서구권](https://ko.wikipedia.org/wiki/서구권 "wikilink")언어에대한 쓰기 지원이 추가되었다. 예를 들어, BDF 2.2 글꼴 정의의 글리프는 단순히 왼쪽에서 오른쪽 방향이 아닌 위에서 아래 방향으로 렌더링을 지정할 수도 있다.

BDF 글꼴 파일은 세 부분으로 구성됩니다.

1.  글꼴의 모든 글리프에 적용되는 전역(Global) 섹션
2.  각 글리프에 대해 별도의 항목이있는 섹션
3.  ENDFONT 문

## 예

이것은 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 대문자 'A'에 대해 하나의 [글리프가](../Page/자체.md "wikilink") 포함 된 예제 글꼴이다. 이 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink") 문자는 [GNU 유니폰트](../Page/GNU_유니폰트.md "wikilink")(GNU Unifont) 에서 가져온 것이다.

    <nowiki>
    STARTFONT 2.1
    FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
    SIZE 16 75 75
    FONTBOUNDINGBOX 16 16 0 -2
    STARTPROPERTIES 2
    FONT_ASCENT 14
    FONT_DESCENT 2
    ENDPROPERTIES
    CHARS 1
    STARTCHAR U+0041
    ENCODING 65
    SWIDTH 500 0
    DWIDTH 8 0
    BBX 8 16 0 -2
    BITMAP
    00
    00
    00
    00
    18
    24
    24
    42
    42
    7E
    42
    42
    42
    42
    00
    00
    ENDCHAR
    ENDFONT
    </nowiki>

## 같이 보기

  - [PCF](https://ko.wikipedia.org/wiki/PCF_\(파일_포맷\) "wikilink")
  - [파일 형식](https://ko.wikipedia.org/wiki/파일_형식 "wikilink")

## 각주

## 참고

  -
[분류:글꼴 포맷](https://ko.wikipedia.org/wiki/분류:글꼴_포맷 "wikilink") [분류:X 윈도 시스템](https://ko.wikipedia.org/wiki/분류:X_윈도_시스템 "wikilink")

1.