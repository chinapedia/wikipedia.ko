> This article is converted from Wikipedia: [APNG](https://ko.wikipedia.org/wiki/APNG).


**APNG**()는 [PNG](../Page/PNG.md "wikilink")를 확장한 이미지 파일 포맷으로, Stuart Parmenter와 Vladimir Vukicevic가 제안했다. 이 포맷은 [GIF](../Page/GIF.md "wikilink")와 비슷한 방법으로 애니메이션을 구현하면서 기존 PNG 파일과의 하위 호환성을 유지했기 때문에 GIF보다 더 높은 품질을 보여 준다. PNG 기반의 애니메이션 파일 포맷으로 [MNG](https://ko.wikipedia.org/wiki/MNG "wikilink")도 있지만, APNG는 MNG보다 구현이 간단하고 호환성이 유지된다는 장점이 있다.

APNG 파일의 첫 프레임은 일반적인 PNG 스트림으로 저장되기 때문에, APNG를 해석할 수 없는 기존 PNG 디코더들도 APNG 파일의 첫 프레임을 보여 줄 수 있다. 나머지 프레임들과 애니메이션 정보들은 별도의 스트림으로 저장된다.

2013년 기준으로 [libpng](https://ko.wikipedia.org/wiki/libpng "wikilink")를 사용한 APNG 구현이 있지만, 대부분의 이미지 라이브러리, 뷰어, 편집기에서 APNG를 지원하지 않기 때문에 아직 대중적으로 사용되지는 않고 있다.

## 역사

APNG 사양은 [스로버](https://ko.wikipedia.org/wiki/스로버 "wikilink")(Throbber)와 같은 인터페이스에 필요한 애니메이션을 저장할 수 있게 하기 위해 2004년 [모질라 코퍼레이션의](../Page/모질라_코퍼레이션.md "wikilink") Stuart Parmenter와 Vladimir Vukićević가 만들었다. 2003년 5월, 모질라는 APNG 기능의 하부 집합을 제공하는 [MNG](https://ko.wikipedia.org/wiki/MNG "wikilink") 애니메이션 지원을 추가하였으며, MNG 디코더 라이브러리(300KB)에 필요한 큰 파일 크기에 대한 염려를 언급하였다.\[1\] PNG 디코더의 뒷쪽에 빌드된 APNG 디코더는 훨씬 더 작은 구성 요소였다.

## 기술적 상세 내용

PNG 파일은 [PNG 시그너처](http://www.w3.org/TR/PNG/#5PNG-file-signature)(8개의 특수 바이트)와 일련의 [청크들](http://www.w3.org/TR/PNG/#5Chunk-layout)로 이루어진다. 청크 하나는 4개의 부분으로 이루어진다: 길이 (4 바이트), 청크의 유형 (4바이트), 청크 데이터 (길이 바이트), CRC (4바이트).

<table>
<caption>하나의 PNG 청크 구조</caption>
<tbody>
<tr class="odd">
<td><p>길이<br />
(4 바이트)</p></td>
<td><p>청크 유형<br />
(4 바이트)</p></td>
<td><p>청크 데이터<br />
(길이 바이트)</p></td>
<td><p>CRC<br />
(4 바이트)</p></td>
</tr>
</tbody>
</table>

약 20개의 각기 다른 [청크 유형](http://www.w3.org/TR/PNG/#11Chunks)이 있지만 최소한의 PNG의 경우 3개만 필요하다: [IHDR](http://www.w3.org/TR/PNG/#11IHDR) (그림 헤더) 청크, 하나 이상의 [IDAT](http://www.w3.org/TR/PNG/#11IDAT) (그림 데이터) 청크, [IEND](http://www.w3.org/TR/PNG/#11IEND) (그림 끝부분) 청크.

<table>
<caption>매우 단순한 PNG 파일의 구조</caption>
<tbody>
<tr class="odd">
<td><p><code>89 50 4E 47 0D 0A 1A 0A</code><br />
PNG 시그너처</p></td>
<td><p><code>IHDR</code><br />
그림 헤더</p></td>
<td><p><code>IDAT</code><br />
그림 데이터</p></td>
<td><p><code>IEND</code><br />
그림 끝부분</p></td>
</tr>
</tbody>
</table>

다음의 그래픽은 최소한의 PNG 파일의 내용을 보여주며 하나의 빨간 화소만을 표현하고 있다. PNG 시그너처 바이트와 개개의 청크들은 아래와 같이 색으로 표시하였다. 왼쪽에서 바이트 값들은 [16진 형식으로](https://ko.wikipedia.org/wiki/16진수 "wikilink") 표시되어 있고, 오른쪽에는 [ISO-8859-1에](https://ko.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink") 일치하는 문자들을 나타내고 있다. (점의 경우 인식하지 못하는 문자 및 제어 문자를 의미) 듀얼 디스플레이는 [헥사 편집기에](https://ko.wikipedia.org/wiki/헥사_편집기 "wikilink") 일반화되어 있다. 청크들은 사람들이 읽을 수 있는 4바이트 유형 이름 때문에 식별이 쉽다. (아래의 예 IHDR, IDAT & IEND의 경우)

<table>
<thead>
<tr class="header">
<th><p>16진</p></th>
<th><p>문자</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span style="background:#fcc;">89 50 4E 47 0D 0A 1A 0A </span><span style="background:#cfc;">00 00 00 0D 49 48 44 52</span><br />
<span style="background:#cfc;">00 00 00 01 00 00 00 01 08 02 00 00 00 90 77 53</span><br />
<span style="background:#cfc;">DE </span><span style="background:#ccf;">00 00 00 0E 49 44 41 54 78 DA 62 F8 CF C0 00</span><br />
<span style="background:#ccf;">10 60 00 03 01 01 00 66 FD 9F 24 </span><span style="background:#fec;">00 00 00 00 49</span><br />
<span style="background:#fec;">45 4E 44 AE 42 60 82</span></p></td>
<td><p><span style="background:#fcc;">.PNG....</span><span style="background:#cfc;">....IHDR</span><br />
<span style="background:#cfc;">..............wS</span><br />
<span style="background:#cfc;">Þ</span><span style="background:#ccf;">....IDATxÚbøÏÀ.</span><br />
<span style="background:#ccf;">.`.....fý.$</span><span style="background:#fec;">....I</span><br />
<span style="background:#fec;">END®B`.</span></p></td>
</tr>
</tbody>
</table>

[프레임](https://ko.wikipedia.org/wiki/파일:Apng_assembling.svg "wikilink")

## 응용 프로그램 지원

  - 이미지 처리 프로그램

[어도비 포토샵에서는](../Page/어도비_포토샵.md "wikilink") 지원되지 않는다.

  - [김프](../Page/김프.md "wikilink") (APNG 플러그인 필요)
  - cphktool APNG Anime Maker
  - Gamani GIF Movie Gear
  - [ImageJ](https://ko.wikipedia.org/wiki/ImageJ "wikilink")
  - [Imagine](https://ko.wikipedia.org/wiki/Imagine "wikilink")
  - Konvertor
  - [KSquirrel](https://ko.wikipedia.org/wiki/KSquirrel "wikilink")
  - [페인트 닷 넷](https://ko.wikipedia.org/wiki/페인트_닷_넷 "wikilink")
  - [XnView](../Page/XnView.md "wikilink")

<!-- end list -->

  - 웹 브라우저

인터넷 익스플로러에서는 지원되지 않는다.

  - 게코 기반 웹 브라우저
      - 모질라 파이어폭스
      - 씨몽키
      - Iceweasel 등
  - [사파리](../Page/사파리_\(웹_브라우저\).md "wikilink")
  - 오페라(프레스토 렌더링 엔진 기반, 웹킷 엔진 기반은 APNG 추가 기능 필요)
  - [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink")/크로미엄 (APNG 추가 기능 필요, 버전 59부터 자체지원)

<!-- end list -->

  - 모바일

<!-- end list -->

  - [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink") (사파리8이상에서 지원)
  - 안드로이드 (안드로이드용 파이어폭스, 크롬 버전 59 이상으로 가능, 앱에서는 불가)
  - 오페라 모바일 / 윈도 모바일

## 각주

## 외부 링크

  - [APNG 사양](https://web.archive.org/web/20100705233055/https://wiki.mozilla.org/APNG_Specification)
  - [libpng를 사용한 구현](http://littlesvr.ca/apng/)
  - [Discussion about MNG vs. APNG](https://bugzilla.mozilla.org/show_bug.cgi?id=apng)
  - [Slightly friendlier discussion about MNG vs. APNG](https://bugzilla.mozilla.org/show_bug.cgi?id=apngspec)

[분류:그래픽 파일 포맷](https://ko.wikipedia.org/wiki/분류:그래픽_파일_포맷 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.