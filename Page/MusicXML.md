> This article is converted from Wikipedia: [MusicXML](https://ko.wikipedia.org/wiki/MusicXML).


**MusicXML**은 악보를 [XML](https://ko.wikipedia.org/wiki/XML "wikilink") 형식으로 표기하는 오픈 [포맷이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink"). Recordare 사에서 개발해 2004년 1월 버전 1.0이 발표된 후, 2005년 5월 버전 1.1이, 2007년 6월 버전 2.0이 발표되었다. [확장자는](../Page/파일_확장자.md "wikilink") `.xmz`이었으나 [W3C](https://ko.wikipedia.org/wiki/W3C "wikilink")개발로 .mxl (또는 .musicxml)로 바뀌었다.

많은 프로그램이 이 포맷을 지원하고 있고, 변환 플러그인이 다수 개발되었기 때문에 현재 존재하는 대부분의 음악 프로그램에서 입출력이 가능하다.

## 파일 포맷

일반적으로 .mxl 확장자 [파일 포맷은](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 압축된 MusicXML에 사용되고, .musicxml은 비압축파일 확장자로 사용하고 있다.

## W3C 개발

MusicXML 개발은 2011년 Recordare를 인수한 MakeMusic이 관리했다.\[1\]\[2\]이어서 MusicXML 개발은 2015년7월에 웹에서의 공개(오픈) 표준을 제정하는 [W3C](https://ko.wikipedia.org/wiki/W3C "wikilink") Music Notation 커뮤니티 그룹으로 이관되었다.\[3\]

버전 1.0은 2004년1월에 릴리스되었다. 버전 1.1은 2005년5월에 향상된 형식 지원을 통해 릴리스되었다. 버전 2.0은 2007 년 6 월에 발표되었으며 표준 압축 형식을 포함한다.\[4\] 이 모든 버전은 일련의 DTD ( Document Type Definition)로 정의되었다 . 버전 2.0의 XML 스키마 정의 (XSD) 구현은 2008 년 9 월에 릴리스되었다. 버전 3.0은 DTD 및 XSD 버전에서 향상된 가상 악기 지원을 사용하여 2011 년 8 월에 릴리스되었다.\[5\]\[6\] 버전 3.1은 표준 음악 글꼴 레이아웃 (SMuFL)에 대한 향상된 지원으로 2017 년 12 월에 발표되었다.\[7\] MusicXML DTD와 XSD는 W3C Community Final Specification Agreement에 따라 각각 자유롭게 재배포 가능하다.\[8\]

이로서 musicXML를 통해서 서로 다른 다양한 음악 프로그램간에 정보 교환 및 [파일](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink")(data) 호환이 가능하게 되었다. 또한 musicXML에 특화되어 제작된 전용 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink")파일은 [JQuery](https://ko.wikipedia.org/wiki/JQuery "wikilink")와 함께 스탠드얼론상태인 [PC환경에서도](https://ko.wikipedia.org/wiki/개인용_컴퓨터 "wikilink") [ABC표기법에](../Page/ABC_기보법.md "wikilink") 기반해서 웹 브라우저 상에서 편집과 재생이 가능토록해 주기도 한다.\[9\]\[10\]

MusicX라는 [음악](../Page/음악.md "wikilink") [프로그램과는](https://ko.wikipedia.org/wiki/TV_프로그램 "wikilink") 관련이 없다.

## 예시

다장조의 도 음을 표기한 경우는 아래와 같다. [섬네일](https://ko.wikipedia.org/wiki/파일:MusicXML_C_Whole_Note.svg "wikilink")

``` xml
  <?xml version="1.0" encoding="UTF-8" standalone="no"?>
  <!DOCTYPE score-partwise PUBLIC
      "-//Recordare//DTD MusicXML 2.0 Partwise//EN"
      "http://www.musicxml.org/dtds/partwise.dtd">
  <score-partwise version="2.0">
    <part-list>
      <score-part id="P1">
        <part-name>Music</part-name>
      </score-part>
    </part-list>
    <part id="P1">
      <measure number="1">
        <attributes>
          <divisions>1</divisions>
          <key>
            <fifths>0</fifths>
          </key>
          <time>
            <beats>4</beats>
            <beat-type>4</beat-type>
          </time>
          <clef>
            <sign>G</sign>
            <line>2</line>
          </clef>
        </attributes>
        <note>
          <pitch>
            <step>C</step>
            <octave>4</octave>
          </pitch>
          <duration>4</duration>
          <type>whole</type>
        </note>
      </measure>
    </part>
  </score-partwise>
```

위 표기는 이와 같은 악보를 나타낸다.

## 지원하는 프로그램

  - MakeMusic\!
  - [피날레](../Page/피날레_\(소프트웨어\).md "wikilink")(Finale 2008이후)
  - [시벨리우스](../Page/시벨리우스_\(소프트웨어\).md "wikilink")(Sibelius 4 이후)
  - Encore 5
  - capella Media Producer
  - NOTION
  - Harmony Assistant
  - Guitar Pro
  - [뮤즈스코어](https://ko.wikipedia.org/wiki/뮤즈스코어 "wikilink")(MuseScore)
  - Cubase

## 각주

## 외부 링크

  -
  - [MusicXML Definition](http://www.musicxml.com/UserManuals/MusicXML/MusicXML.htm) - 규격서

  - [W3C 공식웹사이트](https://www.w3.org/2017/12/musicxml31/)

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:음악 소프트웨어](https://ko.wikipedia.org/wiki/분류:음악_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  <https://wim.vree.org/js/xml2abc-js_index.html>
10. [W3C 공식웹사이트](https://www.w3.org/community/music-notation/)