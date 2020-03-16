> This article is converted from Wikipedia: [GeoServer](https://ko.wikipedia.org/wiki/GeoServer).


**GeoServer**(지오서버)는 지리공간 데이터를 공유하고 편집할 수 있는 [Java로](../Page/자바_\(프로그래밍_언어\).md "wikilink") 개발된 오픈 소스 [GIS](https://ko.wikipedia.org/wiki/지리정보시스템 "wikilink") 소프트웨어 서버이다. 상호운용성을 전제로 개발되었기 때문에, 개방형 표준을 사용하여 다양한 공간 데이터 소스를 서비스할 수 있게 한다.

GeoServer는 커뮤니티 기반 프로젝트이기 때문에, 전 세계의 개인과 기관의 다양한 그룹에 의해 개발, 테스트 및 지원된다.

GeoServer는 [웹 맵 서비스](https://ko.wikipedia.org/wiki/웹_맵_서비스 "wikilink")(WMS) 뿐만 아니라 [Open Geospatial Consortium](https://ko.wikipedia.org/wiki/Open_Geospatial_Consortium "wikilink")(OGC) [Web Feature Service](https://ko.wikipedia.org/wiki/Web_Feature_Service "wikilink")(WFS), [Web Coverage Service](https://ko.wikipedia.org/wiki/Web_Coverage_Service "wikilink")(WCS) 그리고 [Web Processing Service](https://ko.wikipedia.org/wiki/Web_Processing_Service "wikilink")(WPS) 표준에 대한 [참조 구현이기도](https://ko.wikipedia.org/wiki/참조_구현 "wikilink") 하다. GeoServer는 지리공간 웹(GeoSpatial Web)의 핵심 컴포넌트를 구성한다.

## 목표

GeoServer는 자유 및 개방형 [Spatial Data Infrastructure](https://ko.wikipedia.org/wiki/Spatial_Data_Infrastructure "wikilink") 내에서의 노드 역할을 목표로 한다. [Apache HTTP Server가](https://ko.wikipedia.org/wiki/Apache_HTTP_Server "wikilink") [HTML](../Page/HTML.md "wikilink") 게시를 위한 자유 및 개방형 웹 서버를 제공하는 것처럼, GeoSever는 지리공간 데이터에 대해 같은 역할을 수행하는 것이다.

## 포맷 지원

GeoServer는 다음을 포함하는 다양한 포맷을 지원한다:

  - [PostGIS](https://ko.wikipedia.org/wiki/PostGIS "wikilink")
  - [Oracle Spatial](https://ko.wikipedia.org/wiki/Oracle_Spatial "wikilink")
  - [ArcSDE](https://ko.wikipedia.org/wiki/ArcSDE "wikilink")
  - [DB2](../Page/IBM_DB2.md "wikilink")
  - [MySQL](../Page/MySQL.md "wikilink")
  - [Shapefile](https://ko.wikipedia.org/wiki/Shapefile "wikilink")s
  - [GeoTIFF](https://ko.wikipedia.org/wiki/GeoTIFF "wikilink")
  - [GTOPO30](https://ko.wikipedia.org/wiki/GTOPO30 "wikilink")
  - [ECW](https://ko.wikipedia.org/wiki/ECW_\(file_format\) "wikilink"), [MrSID](https://ko.wikipedia.org/wiki/MrSID "wikilink")
  - [JPEG2000](https://ko.wikipedia.org/wiki/JPEG2000 "wikilink")

GeoServer의 확장팩을 이용하면 [GDAL](https://ko.wikipedia.org/wiki/GDAL "wikilink") 라이브러리가 제공하는 더 많은 포맷을 사용할 수 있다.

## 주요 기능

  - [Web Map Service](https://ko.wikipedia.org/wiki/Web_Map_Service "wikilink")(WMS)
  - [Web Feature Service](https://ko.wikipedia.org/wiki/Web_Feature_Service "wikilink")(WFS)
  - [WFS transactional profile](https://ko.wikipedia.org/wiki/Web_Feature_Service#Transactions "wikilink") (WFS-T)
  - [Web Coverage Service](https://ko.wikipedia.org/wiki/Web_Coverage_Service "wikilink")(WCS)
  - [Web Processing Service](https://ko.wikipedia.org/wiki/Web_Processing_Service "wikilink")(WPS)
  - [Web Map Tile Service](https://ko.wikipedia.org/wiki/Web_Map_Tile_Service "wikilink")(WMTS)
  - [Tile Map Service](https://ko.wikipedia.org/wiki/Tile_Map_Service "wikilink")(TMS)

GeoServer는 표준 프로토콜을 이용하여 [KML](https://ko.wikipedia.org/wiki/Keyhole_Markup_Language "wikilink"), [GML](https://ko.wikipedia.org/wiki/Geography_Markup_Language "wikilink"), [Shapefile](https://ko.wikipedia.org/wiki/Shapefile "wikilink"), [GeoRSS](https://ko.wikipedia.org/wiki/GeoRSS "wikilink"), [PDF](https://ko.wikipedia.org/wiki/Portable_Document_Format "wikilink"), [GeoJSON](../Page/GeoJSON.md "wikilink"), [JPEG](../Page/JPEG.md "wikilink"), [GIF](../Page/GIF.md "wikilink"), [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink"), [PNG](https://ko.wikipedia.org/wiki/Portable_Network_Graphics "wikilink") 등의 포맷을 출력할 수 있다. 또한, [WFS transactional profile](https://ko.wikipedia.org/wiki/Web_Feature_Service#Transactions "wikilink") (WFS-T)를 통하여 데이터 편집이 가능하며, 데이터 미리보기를 위한 통합된 [OpenLayers](https://ko.wikipedia.org/wiki/OpenLayers "wikilink") 클라이언트를 포함한다.

GeoServer는 이 외에도 [KML을](https://ko.wikipedia.org/wiki/Keyhole_Markup_Language "wikilink") 이용한 [Google Earth의](https://ko.wikipedia.org/wiki/Google_Earth "wikilink") 네트워크 링크 기능을 통해 지리공간 데이터를 발행할 수 있다. 사용자 정의 팝업, 시간 및 고도 시각화, "super-overlays"를 포함한 [Google Earth의](https://ko.wikipedia.org/wiki/Google_Earth "wikilink") 고급 기능을 지원한다.

GeoServer는 [GIS](https://ko.wikipedia.org/wiki/지리정보시스템 "wikilink") 라이브러리인 [GeoTools](https://ko.wikipedia.org/wiki/GeoTools "wikilink")를 기본으로 사용한다.

## 활용

  - [MassGIS](https://ko.wikipedia.org/wiki/MassGIS "wikilink") (Massachusetts state GIS)
  - [TriMet](https://ko.wikipedia.org/wiki/TriMet "wikilink") (Transit agency for Portland, Oregon)
  - [Ordnance Survey](https://ko.wikipedia.org/wiki/Ordnance_Survey "wikilink") (National Mapping Agency of the UK)
  - [Institut Géographique National](https://ko.wikipedia.org/wiki/Institut_Géographique_National "wikilink") (National Mapping Agency of France)
  - [GBIF](https://ko.wikipedia.org/wiki/GBIF "wikilink") (Global Biodiversity Information Facility)
  - [세계은행](../Page/세계은행.md "wikilink")
  - [Global Earthquake Model](https://ko.wikipedia.org/wiki/Global_Earthquake_Model "wikilink")
  - [FAO](https://ko.wikipedia.org/wiki/FAO "wikilink") (Food and Agriculture Organization of the United Nations)
  - [New York City Department of Information Technology and Telecommunications](https://ko.wikipedia.org/wiki/New_York_City_Department_of_Information_Technology_and_Telecommunications "wikilink")
  - [TeamSurv](http://www.teamsurv.eu)

## 아키텍처

GeoServer는 [REST](../Page/REST.md "wikilink") 서비스의 프레임워크로 [Restlet](https://ko.wikipedia.org/wiki/Restlet "wikilink")을 사용한다. 내장된 [Jetty (web server)](https://ko.wikipedia.org/wiki/Jetty_\(web_server\) "wikilink") 내장 서버를 제공하지만, 일반 [servlet container도](https://ko.wikipedia.org/wiki/Java_Servlet#Servlet_containers "wikilink") 지원한다. [TileCache](https://ko.wikipedia.org/wiki/TileCache "wikilink")와 유사한 Java 기반 캐싱 컴포넌트인 [GeoWebCache](https://ko.wikipedia.org/wiki/GeoWebCache "wikilink")가 통합되어 있으나 독립적으로 활용이 가능하다.\[1\]

## 함께보기

  - [KML](https://ko.wikipedia.org/wiki/KML "wikilink")
  - [GeoJSON](../Page/GeoJSON.md "wikilink")
  - [GPX](../Page/GPX.md "wikilink")

## 참고

<references/>

## 외부 링크

  - [GeoServer 공식 웹사이트](http://geoserver.org/)
  - [GeoServer 블로그](http://blog.geoserver.org)
  - [OpenPlans](http://openplans.org/) (GeoServer 원 저작자)
  - [OpenGeo](https://web.archive.org/web/20110226000704/http://opengeo.org/) [Open Planning Project의](https://ko.wikipedia.org/wiki/OpenPlans "wikilink") 지리공간 컨설팅 부서

소스코드(GitHub): <https://github.com/geoserver>

[분류:지리정보시스템](https://ko.wikipedia.org/wiki/분류:지리정보시스템 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:자바로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바로_작성된_자유_소프트웨어 "wikilink")

1.