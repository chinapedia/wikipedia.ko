> This article is converted from Wikipedia: [SCAD](https://ko.wikipedia.org/wiki/SCAD).


**오픈SCAD**(OpenSCAD)는 솔리드 3D CAD([컴퓨터 지원 설계](../Page/컴퓨터_지원_설계.md "wikilink")) 오브젝트를 만들기 위한 [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink") 애플리케이션이다. 자체 기술 언어를 사용하는 스크립트 기반 모델러이며, 부분적인 미리 보기를 지원하지만 3D 뷰에서 마우스를 사용하여 상호작용적으로 선택, 수정을 할 수는 없다. 오픈SCAD 스크립트는 지오메트릭 프리미티브(구체, 상자, 원기둥 등)를 규정하며 이것들이 어떻게 수정, 병합되어 [3차원 모델을](https://ko.wikipedia.org/wiki/3차원_모델링 "wikilink") 렌더링할지를 정의한다. 이와 같은 방식으로 이 프로그램은 [구조적 입체 기하학](https://ko.wikipedia.org/wiki/구조적_입체_기하학 "wikilink")(CSG)를 따른다. 오픈SCAD는 [윈도우](../Page/마이크로소프트_윈도우.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [OS X용으로](https://ko.wikipedia.org/wiki/OS_X "wikilink") 이용이 가능하다.

## 미리 보기

[Z 버퍼링을](../Page/Z_버퍼링.md "wikilink") 사용한 모델의 빠른 미리 보기를 위해 오픈SCAD는 [오픈CSG와](https://ko.wikipedia.org/wiki/구조적_입체_기하학 "wikilink") [오픈GL](https://ko.wikipedia.org/wiki/오픈GL "wikilink")을 이용한다.

3차원 모델 위치는 다른 3D 모델러와 비슷한 방식으로 마우스를 사용하여 뷰 안에서 상호작용적으로 조작이 가능하다. 또, 기본 카메라 위치를 스크립트에 정의할 수도 있다.

부분 색들은 3D 뷰에 정의할 수 있다. (투명도 포함)\[1\]

## 내보내기

  - 뷰를 png 포맷으로 내보낼 수 있다.
  - 2차원 모델을 [DXF](../Page/DXF.md "wikilink")로 내보낼 수 있다.
  - 3D 부분은 [AMF](https://ko.wikipedia.org/wiki/Additive_Manufacturing_File_Format "wikilink"), [OFF](https://ko.wikipedia.org/wiki/OFF "wikilink"), [STL로](../Page/STL_\(파일_포맷\).md "wikilink") 내보낼 수 있다. 색이나 물질 정의가 없다.

## 가져오기

  - DXF로 된 2차원 드로잉을 가져온 다음 모놀리딕 부분으로 extrude가 가능하다.
  - 3D 부분은 STL로 가져온 다음 스케일링이 가능하다.

## 애니메이션

[섬네일](https://ko.wikipedia.org/wiki/파일:Strandbeest_3d_-_crank_offset_corrected.gif "wikilink") 애니메이션은 단순한 모델을 위해 수초 당 여러 그림을 속도별로 움직이는 것이 가능하다. 애니메이션은 어떠한 변수에라도 영향을 줄 수 있는데, 카메라 위치라든지 파트별 차원, 위치, 모양, 존재를 예로 들 수 있다. 영화 제작에 유용한 그림 집합들로 녹화할 수 있다.

## 각주

## 외부 링크

  -
[분류:3차원 그래픽 소프트웨어](https://ko.wikipedia.org/wiki/분류:3차원_그래픽_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink")

1.  Transparency is evaluated in the construction order, so a part is only transparent for parts already built