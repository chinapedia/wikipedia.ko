> This article is converted from Wikipedia: [PICA200](https://ko.wikipedia.org/wiki/PICA200).


**PICA200**은 일본의 GPU 설계 기업 [디지털 미디어 프로페셔널스](https://ko.wikipedia.org/wiki/디지털_미디어_프로페셔널스 "wikilink")(DMP)사가 설계한 임베디드 장치용 [그래픽 처리 장치](../Page/그래픽_처리_장치.md "wikilink")(GPU)이다. SIGGRAPH 2005에서 발표되었으며 [SIGGRAPH 2006](../Page/SIGGRAPH.md "wikilink") 콘퍼런스에서 시연되었다. PICA는 DMP의 그래픽 프로세서의 브랜드이며, 휴대기기에서부터 고성능 아케이드 시스템에 이르는 분야를 대상으로 한다. PICA200은 단순히 PICA 계열의 200 MHz 클럭의 GPU를 말한다.

PICA200은 특정 대상 시스템의 필요에 따라 구성을 변경하는 기능을 갖춘 IPC(instruction-programmable core)가 있으며, 3차원 그래픽스 엔진에 활용할 수 있다. PICA200은 2세대 DMP의 사유 마에스트로(MAESTRO) 그래픽스 기술("MAESTRO-2G")을 지원하며 여기에는 [OpenGL ES 1.1](../Page/OpenGL_ES.md "wikilink") API 지원, 선택적 OpenGL ES 1.1 확장팩, 일부 DMP 사유 확장(절차적 테스처링\[1\], BRDF<small>(bidirectional reflectance distribution function)</small>, Cook-Torrance specular highlights, 폴리곤 서브디비전<small>("Geo Shader", tessellation)</small>,\[2\], 부드러운 그림자 투사, 버텍스 당 서브서피스 스캐터링과 같은 사용자 지정 하드웨어 기반 셰이딩 알고리즘을 사용할 수 있음)을 포함한다.\[3\]

## 응용

DMP는 [닌텐도](../Page/닌텐도.md "wikilink")가 PICA200을 자신들의 [휴대용 게임기](../Page/휴대용_게임기.md "wikilink") [닌텐도 3DS용](../Page/닌텐도_3DS.md "wikilink") GPU로 채택했다고 발표하였다.\[4\]

## 사양

  - [65 nm](https://ko.wikipedia.org/wiki/65_nm "wikilink") 싱글 코어\[5\](최대 클럭 주파수 400 MHz)
      - 픽셀 성능: 800 Mpixel/s\[6\]
          - 400 Mpixel/s @100 MHz\[7\]
          - 1600 Mpixel/s @400 MHz
      - 버텍스 성능: 15.3 Mpolygon/s at 200 MHz\[8\]
          - 40Mtriangle/s @100 MHz\[9\]
          - 160Mtriangle/s @400 MHz
  - 소비 전력: 0.5-1.0 mW/MHz\[10\]
  - 프레임 버퍼 최대 4095×4095 픽셀
  - 지원 픽셀 포맷: RGBA 4-4-4-4, RGB 5-6-5, RGBA 5-5-5-1, RGBA 8-8-8-8
  - 버텍스 프로그램 *(ARB_vertex_program)*
  - [렌더 트 텍스처](https://ko.wikipedia.org/wiki/렌더_트_텍스처 "wikilink")
  - 하드웨어 T\&L(Hardware Transform and Lighting)
  - [밉맵](../Page/밉맵.md "wikilink")
  - [Bilinear texture filtering](https://ko.wikipedia.org/wiki/텍스처_필터링 "wikilink")
  - [알파 블렌딩](../Page/알파_채널.md "wikilink")
  - Full-scene anti-aliasing (2×2)
  - Phong Shading
  - Cel Shading
  - Perspective-Correct Texture Mapping
  - Dot3 Bump Mapping/Normal Mapping.
  - Shadow Mapping
  - Shadow Volumes
  - Self-Shadowing
  - Lightmapping
  - Environment Mapping/Reflection Mapping
  - Volumetric Fog\[11\]
  - Post-processing effects like motion, bloom, depth of field, HDR rendering, gamma correction
  - Polygon offset
  - Depth Test, Stencil Test, Alpha Test.
  - Clipping, Culling
  - 8-bit stencil buffer
  - 24-bit depth buffer
  - Single/Double/Triple buffer
  - 5-Stage TEV Pipeline
  - TEV Combiner Buffer(Only the first four TEV stages can write to the combiner buffer)
  - Color Combiners, Alpha Combiners, Texture Combiners.
  - PICA-FBM frame buffer management
  - ***DMP's MAESTRO-2G*** 기술:
      - per-pixel lighting
      - per-vertex sub-surface scattering
      - procedural texture
      - refraction mapping
      - subdivision primitive
      - shadow
      - gaseous object rendering
      - bidirectional reflectance distribution function
      - Cook-Torrance Model
      - polygon subdivision
      - soft shadowing

## 각주

## 외부 링크

  - [PICA200 3D Graphics IP](https://web.archive.org/web/20101130052019/http://www.dmprof.com/english/e_products/e_pica_200/)
  - [PICA200 block diagram](https://web.archive.org/web/20110721174021/http://journal.mycom.co.jp/photo/articles/2010/06/22/pica200/images/001l.jpg)

[분류:그래픽 하드웨어](https://ko.wikipedia.org/wiki/분류:그래픽_하드웨어 "wikilink") [분류:그래픽 처리 장치](https://ko.wikipedia.org/wiki/분류:그래픽_처리_장치 "wikilink")

1.
2.
3.
4.   [\[html\]](http://www.dmprof.com/release/20100621_3DS_EN.html)  [\[pdf\]](http://www.dmprof.com/release/20100621_3DS_EN.pdf)
5.
6.
7.
8.
9.
10.
11.