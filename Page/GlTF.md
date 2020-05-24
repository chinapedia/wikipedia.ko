> This article is converted from Wikipedia: [GlTF](https://ko.wikipedia.org/wiki/GlTF).


**glTF**(GL Transmission Format의 줄임말)는 3차원 장면과 모델을 표현하는 파일 포맷으로 [JSON](../Page/JSON.md "wikilink") 표준에 기반하고 있다. [크로노스 그룹](../Page/크로노스_그룹.md "wikilink") (Khronos Group)의 3D Format 작업반에서 제정한 표준이며, HTML5DevConf 2016 행사에서 처음 발표되었다. 효율성과 상호 운용성을 강조한 파일 포맷으로서, 실행에 필요한 부하를 최소화 하도록 설계되었다.

## 역사

2012년 3월, [크로노스 그룹은](../Page/크로노스_그룹.md "wikilink") [COLLADA](../Page/COLLADA.md "wikilink")와 [WebGL](../Page/WebGL.md "wikilink")을 결합하는 작업을 시작하였다.\[1\]\[2\]\[3\] Fabrice Robinet JSON 포맷에 기반한 효율적인 이진 파일을 사용하는 방식을 제안하였고, 2012년 [SIGGRAPH](../Page/SIGGRAPH.md "wikilink") 에서 개최된 WebGL meetup 행사에서 Brandon Jones와 Fabrice Robinet 이 첫번째 glTF 관련 데모를 보여 주었다. 초기에는 WebGL Transmissions Format (WebGL TF)으로 불리었다.\[4\]

2013년 3월, Cesium glTF\[5\] 채택을 공식 발표하였고, 2017년 8월 10일 [3D Tiles](http://cesiumjs.org/2016/09/06/3D-Tiles-and-the-OGC/) 로 [OGC Community](https://ko.wikipedia.org/wiki/Open_Geospatial_Consortium "wikilink") 표준으로 채택되었다. 이 표준은 glTF 기반으로서 위치 데이터 정보, 메타데이터, 스타일 데이터를 대규모의 3차원 지형 데이터 세트로 저장하고 이를 스트리밍하는데 활용하였다.\[6\]\[7\]\[8\]

### glTF 1.0

2015년 10월 19일 glTF 1.0 표준이 공식 발표되었다.\[9\]

### glTF 2.0

2017년 3월 3일 [GDC WebGL/WebVR/glTF Meetup](https://www.facebook.com/daniel.tiger.37/videos/10206505664880625/?permPage=1) 행사에서 [마이크로소프트](../Page/마이크로소프트.md "wikilink")는 glTF 2.0을 3차원 자산 표현 포맷으로 자신의 제품군인 [Paint 3D](https://ko.wikipedia.org/wiki/Paint_3D "wikilink"), [3D Viewer](https://ko.wikipedia.org/wiki/Microsoft_3D_Viewer "wikilink"), [Remix 3D](https://ko.wikipedia.org/wiki/Remix_3D "wikilink"), [Babylon.js](https://ko.wikipedia.org/wiki/Babylon.js "wikilink"), and [Microsoft Office에](https://ko.wikipedia.org/wiki/Microsoft_Office "wikilink") 사용한다고 공식 발표하였다.\[10\]\[11\] 같은 행사에서 Microsoft, [Fraunhofer와](https://ko.wikipedia.org/wiki/Fraunhofer_Society "wikilink") University of Pennsylvania 학생들은 glTF 2.0 컨텐츠를 [WebGL](../Page/WebGL.md "wikilink"), [DirectX](../Page/DirectX.md "wikilink"), and [Vulkan을](https://ko.wikipedia.org/wiki/Vulkan_\(API\) "wikilink") 이용하여 렌더링하는 것을 시연하였다.\[12\]

2017년 3월, [구글](../Page/구글.md "wikilink")은 glTF 기능 확장판인 Draco를 발표하였다. 이를 통해 point cloud 데이터와 메쉬 데이터를 압축할 수 있다.\[13\]

glTF 2.0 표준은 2017년 6월 5일, Web3D 2017 Conference 행사에서 공식 발표되었다.\[14\]

### GLB

GLB 는 glTF에서 사용하는 이진 파일 포맷으로 외부 이미지를 참조하는 대신 직접 텍스처를 포함하는데 사용된다. glb 파일은 [Facebook 3D Posts에](https://ko.wikipedia.org/wiki/Facebook_3D_Posts "wikilink") 사용된다.



## 소프트웨어 생태계

glTF 로더는 오픈소스 프로젝트인 [WebGL engines](https://github.com/KhronosGroup/glTF#webgl-engines) 과 [Three.js](../Page/Three.js.md "wikilink"), [Babylon.js](https://ko.wikipedia.org/wiki/Babylon.js "wikilink"), [Cesium](http://cesiumjs.org), [PEX](https://github.com/pex-gl/pex), [xeogl](http://xeogl.org), 및 [A-Frame](https://aframe.io)을 통해 얻을 수 있다.

오픈소스 [glTF 변환 도구](https://github.com/KhronosGroup/glTF#converters)는 [COLLADA](../Page/COLLADA.md "wikilink"), [FBX](https://ko.wikipedia.org/wiki/FBX "wikilink") 및 [OBJ를](https://ko.wikipedia.org/wiki/Wavefront_.obj_file "wikilink") 지원하며. [Assimp는](https://ko.wikipedia.org/wiki/Open_Asset_Import_Library "wikilink") glTF 내보내기 기능을 제공한다..

glTF 파일은 다양한 3D 편집도구를 사용해 내보내기를 할 수 있다. 여기에는 [Blender](../Page/블렌더_\(소프트웨어\).md "wikilink"), [Vectary](https://ko.wikipedia.org/wiki/Vectary "wikilink"), [Autodesk 3ds Max](https://ko.wikipedia.org/wiki/Autodesk_3ds_Max "wikilink") (using [Verge3D](https://ko.wikipedia.org/wiki/Verge3D "wikilink") exporter\[15\]), [Autodesk Maya](https://ko.wikipedia.org/wiki/Autodesk_Maya "wikilink"), [Modo](https://ko.wikipedia.org/wiki/Modo "wikilink"), [Paint 3D](https://ko.wikipedia.org/wiki/Paint_3D "wikilink"), [Substance Painter](https://ko.wikipedia.org/wiki/Substance_Painter "wikilink")\[16\] 등이 포함된다.

오픈소스인 [glTF utility libraries](https://github.com/KhronosGroup/glTF#loaders-and-viewers)를 이용하면 [자바스크립트](../Page/자바스크립트.md "wikilink"), [Node.js](../Page/Node.js.md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [C\#](../Page/C_샤프.md "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [Go](../Page/Go_\(프로그래밍_언어\).md "wikilink"), [러스트](../Page/러스트_\(프로그래밍_언어\).md "wikilink"), [Haxe](../Page/Haxe.md "wikilink"), [Ada](../Page/에이다_\(프로그래밍_언어\).md "wikilink"), [TypeScript](https://ko.wikipedia.org/wiki/TypeScript "wikilink")와 같은 다양한 언어에서 glTF를 활용할 수 있다.

오픈소스로 제공되는 [glTF validator](https://github.com/KhronosGroup/glTF-Validator)를 사용하면 만들어진 파일이 glTF 표준에 적합한지를 테스틀 할 수 있다.\[17\]

관련된 소프트웨어 도구 정보는 [glTF GitHub repository](https://github.com/KhronosGroup/glTF#gltf-tools) 웹 페이지에서 얻을 수 있다.

## 각주

## 외부 링크

  - [glTF 공식 웹페이지](https://www.khronos.org/gltf/)
  - [glTF 2.0 표준](https://github.com/KhronosGroup/glTF/blob/master/specification/README.md)

[분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:그래픽 표준](https://ko.wikipedia.org/wiki/분류:그래픽_표준 "wikilink") [분류:웹 개발](https://ko.wikipedia.org/wiki/분류:웹_개발 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.