> This article is converted from Wikipedia: [POV-Ray](https://ko.wikipedia.org/wiki/POV-Ray).


**POV-Ray**는 다양한 컴퓨터 플랫폼에서 사용할 수 있는 [레이 트레이싱](https://ko.wikipedia.org/wiki/레이_트레이싱 "wikilink") 프로그램이다. 원래는 David Kirk Buck와 Aaron A. Collins가 작성한 [DKBTrace](https://ko.wikipedia.org/wiki/DKBTrace "wikilink") 기반이었다. 만든이 Alexander Enzmann가 공헌하였던 초기 Polyray 레이트레이서로부터의 영향도 있었다. POV-Ray는 소스 코드가 공개되어 있는 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink").

## 기능

[섬네일](https://ko.wikipedia.org/wiki/파일:Glasses_800_edit.png "wikilink") POV-Ray는 만들어진 이후로 지금에 이르러 완성도가 매우 높다. 최근에 나온 소프트웨어 버전은 다음의 기능을 포함하고 있다:

  - 매크로와 루프를 지원하는 [튜링 완전](https://ko.wikipedia.org/wiki/튜링_완전 "wikilink") 장면 서술 언어 (SDL)\[1\]
  - 미리 준비된 장면, 텍스처, 객체
  - 수많은 기하학 원시 데이터와 [CSG](https://ko.wikipedia.org/wiki/CSG "wikilink")(구조적 고체 기하학) 지원
  - 여러 종류의 [광원](https://ko.wikipedia.org/wiki/빛 "wikilink")
  - [안개](../Page/안개.md "wikilink"), 매체([연기](https://ko.wikipedia.org/wiki/연기_\(화학\) "wikilink"), [구름](https://ko.wikipedia.org/wiki/구름 "wikilink"))와 같은 대기 효과
  - [포톤 매핑을](https://ko.wikipedia.org/wiki/포톤_매핑 "wikilink") 사용한 [반사](https://ko.wikipedia.org/wiki/반사 "wikilink"), [굴절](../Page/굴절.md "wikilink"), [화선](../Page/화선.md "wikilink")
  - [라디오시티](https://ko.wikipedia.org/wiki/라디오시티 "wikilink") (radiosity)
  - [주름](https://ko.wikipedia.org/wiki/주름 "wikilink"), 울퉁불퉁한 모습, 물결과 같은 표면 패턴 ([절차적 텍스처와](https://ko.wikipedia.org/wiki/절차적_텍스처 "wikilink") [범프 매핑](https://ko.wikipedia.org/wiki/범프_매핑 "wikilink") 사용)
  - [TGA](https://ko.wikipedia.org/wiki/TGA "wikilink"), [PNG](https://ko.wikipedia.org/wiki/PNG "wikilink"), [JPEG](https://ko.wikipedia.org/wiki/JPEG "wikilink") (입력만)로 [텍스처](https://ko.wikipedia.org/wiki/텍스처 "wikilink"), 랜더 출력 지원
  - 확장된 사용자 문서

## SDL로 작성한 프로그래밍 예

아래의 예는 POV-Ray가 사용하는 SDL의 예제로 랜더링할 장면을 설명한다. 카메라, 광원, 단순한 상자 모양, 변형 효과, 회전 등의 사용을 증명하고 있다.

[섬네일](https://ko.wikipedia.org/wiki/파일:I_example_povray_scene_rendering.png "wikilink")

``` povray
 #version 3.6;
 #include "colors.inc"
 global_settings { assumed_gamma 1.0 }

 background   { color rgb <0.25, 0.25, 0.25> }

 camera       { location  <0.0, 0.5, -4.0>
                direction 1.5*z
                right     x*image_width/image_height
                look_at   <0.0, 0.0, 0.0> }

 light_source { <0, 0, 0>
                color rgb <1, 1, 1>
                translate <-5, 5, -5> }

 light_source { <0, 0, 0>
                color rgb <0.25, 0.25, 0.25>
                translate <6, -6, -6> }

 box          { <-0.5, -0.5, -0.5>
                <0.5, 0.5, 0.5>
                texture { pigment { color Red }
                          finish  { specular 0.6 }
                          normal  { agate 0.25 scale 1/2 } }
                rotate <45,46,47> }
```

아래의 예는 변수 선언, 할당, 비교, while 루프를 사용한 스크립트 부분이다.:

[섬네일](https://ko.wikipedia.org/wiki/파일:I_example_povray_scene_rendering2.png "wikilink")

``` povray
 #declare the_angle = 0;

 #while (the_angle <= 360)
    box {   <-0.5, -0.5, -0.5>
        <0.5, 0.5, 0.5>
                texture { pigment { color Red }
                          finish  { specular 0.6 }
                          normal  { agate 0.25 scale 1/2 } }
        rotate the_angle }
    #declare the_angle = the_angle + 45;
 #end
```

## 각주

## 외부 링크

  -
  -
[분류:3차원 그래픽 소프트웨어](https://ko.wikipedia.org/wiki/분류:3차원_그래픽_소프트웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:C++ 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:GNU AGPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_AGPL_라이선스_소프트웨어 "wikilink") [분류:자유 그래픽 스포트웨어](https://ko.wikipedia.org/wiki/분류:자유_그래픽_스포트웨어 "wikilink")

1.