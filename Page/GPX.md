> This article is converted from Wikipedia: [GPX](https://ko.wikipedia.org/wiki/GPX).


**GPX**(GPS Exchange Format)는 응용 소프트웨어의 공통 GPS 데이터 형식으로 설계된 XML 스키마이다. 구체적인 표현이나 개별적인 용도를 위해 웨이포인트(waypoint), 트랙(track) 및 루트(경로,route)를 기술하는 데 사용된다. 형식은 공개되어 있으며 라이센스 비용을 지불할 필요없이 사용할 수 있다. 위치 데이터 (및 선택적으로 고도, 시간 및 기타 정보)는 태그에 저장되며 [GPS](https://ko.wikipedia.org/wiki/GPS "wikilink") 장치와 소프트웨어간에 상호 교환될 수 있다. 데이터에 대한 일반적인 응용 소프트웨어에는 다양한 지도 소스에 투영된 트랙보기,지도 주석 달기, 현위치에서 찍은 시간을 기준으로 사진의 위치 정보 태그 지정등이 포함된다.

## 데이타 형식

[섬네일](https://ko.wikipedia.org/wiki/파일:Wayroutrackp.png "wikilink")

  - 트랙 : 비트맵 지도에 경로의 모든 절곡 부를 정확하게 그릴 수 있도록 충분한 수의 트랙 포인트가 트랙에 만들어진다. 이것은 예를 들어 여행 경로를 기록한 GPS의 데이타 출력 또는 과도하거나 충분하지 않은 포인트들을 제거 또는 생성하기 위해 그러한 점의 재정렬 또는 벡터 지도에서 추출한 것과 같은 모든 소스의 데이터

<!-- end list -->

  - 루트 : 프로그램이 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink")이나 [벡터](https://ko.wikipedia.org/wiki/벡터 "wikilink") 지도상에 해당 트랙을 가져온후 루트(경로)는 지나온 지점들이 누적되어감에따라 루트가 그려진다. 경로 지점은 횡단 또는 교차점이거나 여행 프로젝트를 진행하는 중간에 벗어난 지점과 같이 멀리 떨어져있을 수도 있다. 따라서 이러한 행적 경로는 GPX 파일에 저장하고 다시 로드할 수 있다.

<!-- end list -->

  - [웨이포인트](https://ko.wikipedia.org/wiki/웨이포인트 "wikilink") : 웨이 포인트는 관심 장소(POI,Point of interest)라고도 불린다. 그것들은 GPS 장치로 기록 할 수있는 단일 지점이다. 웨이 포인트는 일반적으로 다음과 같은 기차역,레스토랑,우편함,기타등등 흥미로운 객체의 지리적 위치를 표시한다.\[1\]

## 단위

[위도](https://ko.wikipedia.org/wiki/위도 "wikilink")와 [경도](https://ko.wikipedia.org/wiki/경도 "wikilink")는 모두 [WGS 84 데이터를](https://ko.wikipedia.org/wiki/세계_지구_좌표_시스템 "wikilink") 사용하여 [십진도](https://ko.wikipedia.org/wiki/십진도 "wikilink")(Decimal degrees,DD) 및 고도 (미터)로 표시된다. 날짜와 시간은 현지 시간이 아니며 대신 [ISO 8601](https://ko.wikipedia.org/wiki/ISO_8601 "wikilink") 형식을 사용하는 협정 세계시 ([UTC](https://ko.wikipedia.org/wiki/UTC "wikilink"))이다.\[2\]

## 사용 예

다음은 특정 [Garmin](https://ko.wikipedia.org/wiki/Garmin "wikilink") [Oregon 400t](https://ko.wikipedia.org/wiki/Oregon_400t "wikilink") 핸드 헬드 GPS 장치로 제작된 GPX 파일이다. 아래 문서는 GPX 형식으로 저장할 수있는 모든 기능을 보여주지는 않지만 예를 들어, 웨이 포인트나 확장 기능은 없는 경로이지만 특정 [XML 스키마가](../Page/XML_스키마.md "wikilink") 적용된 GPX 트랙의 사용을 보여주고있다.

``` xml
<?xml version="1.0" encoding="UTF-8" standalone="no" ?>

<gpx ns="http://www.topografix.com/GPX/1/1" xmlns:gpxx="http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx="http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator="Oregon 400t" version="1.1" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href="http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat="47.644548" lon="-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat="47.644548" lon="-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat="47.644548" lon="-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## 함께보기

  - [KML](https://ko.wikipedia.org/wiki/KML "wikilink")
  - [GeoJSON](../Page/GeoJSON.md "wikilink")

## 참고

[분류:지리정보시스템](https://ko.wikipedia.org/wiki/분류:지리정보시스템 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:GPS](https://ko.wikipedia.org/wiki/분류:GPS "wikilink") [분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink")

1.  [오픈스트리트맵](https://wiki.openstreetmap.org/wiki/Upload_Waypoints)
2.  [GPX: the GPS Exchange Format](http://www.topografix.com/gpx.asp)