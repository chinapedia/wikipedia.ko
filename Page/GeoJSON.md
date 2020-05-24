> This article is converted from Wikipedia: [GeoJSON](https://ko.wikipedia.org/wiki/GeoJSON).


**GeoJSON**(지오제이슨)\[1\]은 위치정보를 갖는 점을 기반으로 체계적으로 지형을 표현하기 위해 설계된 개방형 공개 표준 형식이다. 이것은 [JSON](../Page/JSON.md "wikilink")인 [자바스그립트](https://ko.wikipedia.org/wiki/JavaScript "wikilink") 오브젝트 노테이션(Object Notation)을 사용하는 [파일 포맷이다](https://ko.wikipedia.org/wiki/파일_포맷 "wikilink").\[2\]\[3\]

[지리좌표계](https://ko.wikipedia.org/wiki/지리좌표계 "wikilink")의 점을 기반으로 [Geocoding](https://ko.wikipedia.org/wiki/Geocoding "wikilink")된 지형지물(주소 및 위치), 라인스트링(LineString - 거리, 고속도로 및 경계등 정보를 담고있는 문자열) 또는 [폴리라인](https://ko.wikipedia.org/wiki/선분 "wikilink"), 다각형 (국가,도시, 토지) 및 이러한 유형의 여러 부분으로 구성된 모음을 특징으로 한다.\[4\] GeoJSON 기능은 물리적 세계의 엔티티만을 나타낼 필요는 없다. 예를 들어, 모바일 라우팅 및 네비게이션 애플리케이션은 GeoJSON을 사용하여 서비스 범위를 확장 기술할 수 있다.\[5\] 또한 [GPX](../Page/GPX.md "wikilink")가 특정 목적을 위한 경로 정보 공유 도구로 활용되는것처럼 즉, 산악 등반이나 마운틴 바이크를 위한 루트 및 길안내 자료등으로 사용할수있다.

GeoJSON 형식은 공식 표준 조직이 아니라 [국제 인터넷 표준화 기구](https://ko.wikipedia.org/wiki/IETF "wikilink") 산하 워킹그룹에 의해 작성되고 유지된다는 점에서 다른 [GIS](https://ko.wikipedia.org/wiki/GIS "wikilink") 표준과 다르지만\[6\][XML](../Page/XML.md "wikilink")을 기반으로 한[GPX](../Page/GPX.md "wikilink")와 함께 사실상 표준처럼 사용된다. 특징으로는 일반적인 [구글맵](https://ko.wikipedia.org/wiki/구글맵 "wikilink")이나 [오픈스트리트맵](../Page/오픈스트리트맵.md "wikilink")서비스가 \[위도,경도\]의 표기법을 사용하나 GeoJSON은 [WGS 84가](https://ko.wikipedia.org/wiki/세계_지구_좌표_시스템 "wikilink") 권장하는 \[경도,위도\]의 표기법을 지원한다는 점이다.\[7\] GeoJSON은 지형 공간 토폴로지를 인코딩하며 일반적으로 파일 크기가 더 작다.

GeoJSON의 주목할만한 계열은 TopoJSON이다.

## 워킹그룹

GeoJSON 형식의 워킹그룹과 토론은 2007년 3월에 시작되었으며\[8\] 형식 지정은 2008년 6월에 마무리되었다.

2015년 4월 [IETF](https://ko.wikipedia.org/wiki/IETF "wikilink")(Internet Engineering Task Force)는 GeoJSON을 2016년 8월 RFC 7946으로 제안된 Geographic JSON 워킹그룹을 구성했다.\[9\]

## 예

다음은 [말레이시아](../Page/말레이시아.md "wikilink"),[싱가포르](../Page/싱가포르.md "wikilink")등이 위치해 있는 [자바 해의](https://ko.wikipedia.org/wiki/자바_해 "wikilink") [말레이 제도에서의](../Page/말레이_제도.md "wikilink") 가상의 GeoJson 표현이다.\[10\]

``` JavaScript
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [102.0, 0.5]
      },
      "properties": {
        "prop0": "value0"
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "LineString",
        "coordinates": [
          [102.0, 0.0], [103.0, 1.0], [104.0, 0.0], [105.0, 1.0]
        ]
      },
      "properties": {
        "prop0": "value0",
        "prop1": 0.0
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
            [100.0, 0.0], [101.0, 0.0], [101.0, 1.0],
            [100.0, 1.0], [100.0, 0.0]
          ]
        ]
      },
      "properties": {
        "prop0": "value0",
        "prop1": { "this": "that" }
      }
    }
  ]
}
```

### 주요 Geometries 형태

<table>
<caption>기본형태(Geometry primitives)</caption>
<thead>
<tr class="header">
<th><p>주요 형식(Type)</p></th>
<th><p>사용예(Examples)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/점_(기하학).md" title="wikilink">Point</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_Point.svg" title="wikilink">파일:SFA Point.svg</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/선분" title="wikilink">LineString</a>(polyline)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_LineString.svg" title="wikilink">파일:SFA LineString.svg</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Polygon" title="wikilink">Polygon</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_Polygon.svg" title="wikilink">파일:SFA Polygon.svg</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_Polygon_with_hole.svg" title="wikilink">파일:SFA Polygon with hole.svg</a></p></td>
<td><div class="sourceCode" id="cb1"><pre class="sourceCode JavaScript"><code class="sourceCode javascript"><span id="cb1-1"><a href="#cb1-1"></a><span class="op">{</span></span>
<span id="cb1-2"><a href="#cb1-2"></a>    <span class="st">&quot;type&quot;</span><span class="op">:</span> <span class="st">&quot;Polygon&quot;</span><span class="op">,</span></span>
<span id="cb1-3"><a href="#cb1-3"></a>    <span class="st">&quot;coordinates&quot;</span><span class="op">:</span> [</span>
<span id="cb1-4"><a href="#cb1-4"></a>        [[<span class="dv">35</span><span class="op">,</span>_10]<span class="op">,</span>_[<span class="dv">45</span><span class="op">,</span>_45]<span class="op">,</span>_[<span class="dv">15</span><span class="op">,</span>_40]<span class="op">,</span>_[<span class="dv">10</span><span class="op">,</span>_20]<span class="op">,</span>_[<span class="dv">35</span><span class="op">,</span>_10<span class="op">|</span><span class="dv">35</span><span class="op">,</span> <span class="dv">10</span>]<span class="op">,</span> [<span class="dv">45</span><span class="op">,</span> <span class="dv">45</span>]<span class="op">,</span> [<span class="dv">15</span><span class="op">,</span> <span class="dv">40</span>]<span class="op">,</span> [<span class="dv">10</span><span class="op">,</span> <span class="dv">20</span>]<span class="op">,</span> [<span class="dv">35</span><span class="op">,</span> <span class="dv">10</span>]]<span class="op">,</span></span>
<span id="cb1-5"><a href="#cb1-5"></a>        [[<span class="dv">20</span><span class="op">,</span>_30]<span class="op">,</span>_[<span class="dv">35</span><span class="op">,</span>_35]<span class="op">,</span>_[<span class="dv">30</span><span class="op">,</span>_20]<span class="op">,</span>_[<span class="dv">20</span><span class="op">,</span>_30<span class="op">|</span><span class="dv">20</span><span class="op">,</span> <span class="dv">30</span>]<span class="op">,</span> [<span class="dv">35</span><span class="op">,</span> <span class="dv">35</span>]<span class="op">,</span> [<span class="dv">30</span><span class="op">,</span> <span class="dv">20</span>]<span class="op">,</span> [<span class="dv">20</span><span class="op">,</span> <span class="dv">30</span>]]</span>
<span id="cb1-6"><a href="#cb1-6"></a>    ]</span>
<span id="cb1-7"><a href="#cb1-7"></a><span class="op">}</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

<table>
<caption>복잡한 형태(Multipart geometries)</caption>
<thead>
<tr class="header">
<th><p>형식(Type)</p></th>
<th><p>사용예(Examples)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/점_(기하학).md" title="wikilink">MultiPoint</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_MultiPoint.svg" title="wikilink">파일:SFA MultiPoint.svg</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/선분" title="wikilink">MultiLineString</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_MultiLineString.svg" title="wikilink">파일:SFA MultiLineString.svg</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Polygon" title="wikilink">MultiPolygon</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_MultiPolygon.svg" title="wikilink">파일:SFA MultiPolygon.svg</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/파일:SFA_MultiPolygon_with_hole.svg" title="wikilink">파일:SFA MultiPolygon with hole.svg</a></p></td>
<td><div class="sourceCode" id="cb1"><pre class="sourceCode JavaScript"><code class="sourceCode javascript"><span id="cb1-1"><a href="#cb1-1"></a><span class="op">{</span></span>
<span id="cb1-2"><a href="#cb1-2"></a>    <span class="st">&quot;type&quot;</span><span class="op">:</span> <span class="st">&quot;MultiPolygon&quot;</span><span class="op">,</span></span>
<span id="cb1-3"><a href="#cb1-3"></a>    <span class="st">&quot;coordinates&quot;</span><span class="op">:</span> [</span>
<span id="cb1-4"><a href="#cb1-4"></a>        [</span>
<span id="cb1-5"><a href="#cb1-5"></a>            [[<span class="dv">40</span><span class="op">,</span>_40]<span class="op">,</span>_[<span class="dv">20</span><span class="op">,</span>_45]<span class="op">,</span>_[<span class="dv">45</span><span class="op">,</span>_30]<span class="op">,</span>_[<span class="dv">40</span><span class="op">,</span>_40<span class="op">|</span><span class="dv">40</span><span class="op">,</span> <span class="dv">40</span>]<span class="op">,</span> [<span class="dv">20</span><span class="op">,</span> <span class="dv">45</span>]<span class="op">,</span> [<span class="dv">45</span><span class="op">,</span> <span class="dv">30</span>]<span class="op">,</span> [<span class="dv">40</span><span class="op">,</span> <span class="dv">40</span>]]</span>
<span id="cb1-6"><a href="#cb1-6"></a>        ]<span class="op">,</span></span>
<span id="cb1-7"><a href="#cb1-7"></a>        [</span>
<span id="cb1-8"><a href="#cb1-8"></a>            [[<span class="dv">20</span><span class="op">,</span>_35]<span class="op">,</span>_[<span class="dv">10</span><span class="op">,</span>_30]<span class="op">,</span>_[<span class="dv">10</span><span class="op">,</span>_10]<span class="op">,</span>_[<span class="dv">30</span><span class="op">,</span>_5]<span class="op">,</span>_[<span class="dv">45</span><span class="op">,</span>_20]<span class="op">,</span>_[<span class="dv">20</span><span class="op">,</span>_35<span class="op">|</span><span class="dv">20</span><span class="op">,</span> <span class="dv">35</span>]<span class="op">,</span> [<span class="dv">10</span><span class="op">,</span> <span class="dv">30</span>]<span class="op">,</span> [<span class="dv">10</span><span class="op">,</span> <span class="dv">10</span>]<span class="op">,</span> [<span class="dv">30</span><span class="op">,</span> <span class="dv">5</span>]<span class="op">,</span> [<span class="dv">45</span><span class="op">,</span> <span class="dv">20</span>]<span class="op">,</span> [<span class="dv">20</span><span class="op">,</span> <span class="dv">35</span>]]<span class="op">,</span></span>
<span id="cb1-9"><a href="#cb1-9"></a>            [[<span class="dv">30</span><span class="op">,</span>_20]<span class="op">,</span>_[<span class="dv">20</span><span class="op">,</span>_15]<span class="op">,</span>_[<span class="dv">20</span><span class="op">,</span>_25]<span class="op">,</span>_[<span class="dv">30</span><span class="op">,</span>_20<span class="op">|</span><span class="dv">30</span><span class="op">,</span> <span class="dv">20</span>]<span class="op">,</span> [<span class="dv">20</span><span class="op">,</span> <span class="dv">15</span>]<span class="op">,</span> [<span class="dv">20</span><span class="op">,</span> <span class="dv">25</span>]<span class="op">,</span> [<span class="dv">30</span><span class="op">,</span> <span class="dv">20</span>]]</span>
<span id="cb1-10"><a href="#cb1-10"></a>        ]</span>
<span id="cb1-11"><a href="#cb1-11"></a>    ]</span>
<span id="cb1-12"><a href="#cb1-12"></a><span class="op">}</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

## 지원 소프트웨어

GeoJSON은 [OpenLayers](https://ko.wikipedia.org/wiki/OpenLayers "wikilink")\[11\], [Leaflet](https://ko.wikipedia.org/wiki/Leaflet "wikilink"), [MapServer](https://ko.wikipedia.org/wiki/MapServer "wikilink")\[12\], [Geoforge](https://ko.wikipedia.org/wiki/Geoforge "wikilink") 소프트웨어\[13\] [GeoServer](../Page/GeoServer.md "wikilink")\[14\], [GeoDjango](../Page/장고_\(웹_프레임워크\).md "wikilink")\[15\], [GDAL](https://ko.wikipedia.org/wiki/GDAL "wikilink")\[16\], Safe Software FME 등 많은 매핑 및 [GIS](https://ko.wikipedia.org/wiki/GIS "wikilink") 소프트웨어 패키지에서 지원하고있다.\[17\] [CartoDB](https://ko.wikipedia.org/wiki/CartoDB "wikilink")\[18\]와 GDAL OGR 변환 라이브러리를 통해 형식을 처리하는 [PostGIS](https://ko.wikipedia.org/wiki/PostGIS "wikilink")\[19\]와 [Mapnik](https://ko.wikipedia.org/wiki/Mapnik "wikilink")\[20\]에서 GeoJSON을 사용할 수도 있다. [Bing Maps](https://ko.wikipedia.org/wiki/Bing_Maps "wikilink"), [야후\!](../Page/야후!.md "wikilink"), [HERE](https://ko.wikipedia.org/wiki/HERE "wikilink")\[21\] 및 [Google](https://ko.wikipedia.org/wiki/Google "wikilink")은 [API](../Page/API.md "wikilink") 서비스에서 GeoJSON을 지원한다.

[Google Maps](https://ko.wikipedia.org/wiki/Google_Maps "wikilink") JavaScript API v3은 2014년 3월 19일 기준으로 GeoJSON 데이터 레이어의 통합을 직접 지원한다.\[22\]\[23\] [Julia](../Page/줄리아_\(프로그래밍_언어\).md "wikilink") 언어의 경우 GeoJSON.jl 패키지를 사용할 수 있다.

[GitHub](https://ko.wikipedia.org/wiki/GitHub "wikilink")은 GeoJSON 렌더링\[24\]과 Potrace GeoJSON 내보내기도 지원한다.

Geojson.io는 웹 브라우저에서 GeoJSON 렌더링 및 편집을 지원합니다.

## TopoJSON 스키마

[위도](../Page/위도.md "wikilink")0 °와 [경도](https://ko.wikipedia.org/wiki/경도 "wikilink") 0 ° 근처에 [GIS](https://ko.wikipedia.org/wiki/GIS "wikilink") 정보가 주어지면 모든 메타 데이터를 포함하고있는 단순하지만 유효하고 완전한 topojson 파일의 'Polygon', ' LineString ', 'Point' ,'arc' 및 'properties'는 다음과 같이 정의할수있다. [섬네일](https://ko.wikipedia.org/wiki/파일:Topojson_shapes-en.svg "wikilink")

``` JavaScript
{
  "type":"Topology",
  "transform":{
    "scale": [1,1],
    "translate": [0,0]
  },
  "objects":{
    "two-squares":{
      "type": "GeometryCollection",
      "geometries":[
        {"type": "Polygon", "arcs":[[0,1|0,1]],"properties": {"name": "Left_Polygon" }},
        {"type": "Polygon", "arcs":[[2,-1|2,-1]],"properties": {"name": "Right_Polygon" }}
      ]
    },
    "one-line": {
      "type":"GeometryCollection",
      "geometries":[
        {"type": "LineString", "arcs": [3],"properties":{"name":"Under_LineString"}}
      ]
    },
    "two-places":{
      "type":"GeometryCollection",
      "geometries":[
        {"type":"Point","coordinates":[0,0],"properties":{"name":"Origine_Point"}},
        {"type":"Point","coordinates":[0,-1],"properties":{"name":"Under_Point"}}
      ]
    }
  },
  "arcs": [
    [[1,2],[0,-2|1,2],[0,-2]],
    [[1,0],[-1,0],[0,2],[1,0|1,0],[-1,0],[0,2],[1,0]],
    [[1,2],[1,0],[0,-2],[-1,0|1,2],[1,0],[0,-2],[-1,0]],
    [[0,-1],[2,0|0,-1],[2,0]]
  ]
}
```

## 확장성

GeoJSON은 [GPX](../Page/GPX.md "wikilink")와 호환되면서도, [XML](../Page/XML.md "wikilink")에 기반한 GPX와는 다르게 [스키마나](../Page/XML_스키마.md "wikilink") 태그의 [엘리먼트](../Page/HTML_요소.md "wikilink") 제약으로부터 훨씬 자유롭다. 따라서 [폴리라인](https://ko.wikipedia.org/wiki/폴리라인 "wikilink")(라인스트링)의 압축이 가능하고 적은 량(light-weight)의 데이타로 응용 프로그램의 적재에 용이할 수 있다.\[25\]\[26\]

## 같이 보기

  - [GeoServer](../Page/GeoServer.md "wikilink")
  - [GPX](../Page/GPX.md "wikilink")
  - [KML](https://ko.wikipedia.org/wiki/KML "wikilink")

## 참고

  - [오픈스트리트맵](https://wiki.openstreetmap.org/w/index.php?title=Polyline&redirect=no)
  - [구글맵](https://developers.google.com/maps/documentation/utilities/polylineutility)
  - [속성과 형상 데이터 표현이 가능한 GeoJSON - Taewook Kang](https://sites.google.com/site/bimprinciple/in-the-news/sogseong-gwahyeongsangdeiteopyohyeon-iganeunghangeojson)
  - [WHAT IS GPX?](http://www.topografix.com/gpx.asp)

[분류:지리 정보 시스템](https://ko.wikipedia.org/wiki/분류:지리_정보_시스템 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:JSON](https://ko.wikipedia.org/wiki/분류:JSON "wikilink")

1.  [The GeoJSON Format](https://tools.ietf.org/html/rfc7946)
2.  <http://geojson.org/>
3.  <https://tools.ietf.org/html/rfc7946>
4.  [OSM](https://wiki.openstreetmap.org/wiki/GeoJSON)
5.  [iOS Location and Maps Programming Guide](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/LocationAwarenessPG/ProvidingDirections/ProvidingDirections.html)
6.  [The GeoJSON Discussion List](http://lists.geojson.org/listinfo.cgi/geojson-geojson.org)
7.  [lon,lat-4. Coordinate Reference System](https://tools.ietf.org/html/rfc7946#section-1.3)
8.  [March 2007 Archives by thread](http://lists.geojson.org/pipermail/geojson-geojson.org/2007-March/thread.html)
9.  <https://datatracker.ietf.org/wg/geojson/history/>
10. [mapbox,OSRM](http://geojson.io/#map=5/3.755/99.580)
11.
12. <http://mapserver.org/output/template_output.html>
13. <http://leafletjs.com/reference.html#geojson>
14.
15.
16.
17.
18. <http://developers.cartodb.com/documentation/cartodb-js.html>
19.
20.
21.
22. <https://developers.google.com/maps/documentation/javascript/examples/layer-data-simple>
23. <http://googledevelopers.blogspot.com/2014/03/maps-made-easier-geojson-in-javascript.html>
24. <https://github.com/blog/1528-there-s-a-map-for-that>
25. [구글맵](https://developers.google.com/maps/documentation/utilities/polylinealgorithm)
26.