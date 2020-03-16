> This article is converted from Wikipedia: [LWJGL](https://ko.wikipedia.org/wiki/LWJGL).


**LWJGL**(Light Weight Java Game Library)는 [자바를](../Page/자바_\(프로그래밍_언어\).md "wikilink") 위한 오픈 소스 게임 개발 라이브러리이다.

2014년 11월 13일, 기존의 LWJGL 버전을 완전히 다시 쓴 LWJGL 3 제작을 발표하였고 2015년 4월 17일 알파 버전을 공개하였다. 전 버전 보다 더 많은 라이브러리를 포함하고 있으며 오큘러스 리프트 소프트웨어 제작을 위한 라이브러리 또한 포함하고 있다.

## 바인딩

| 바인딩                                                                               | 설명                                                                          | 참고                                                |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------- |
| [EGL](../Page/EGL_\(API\).md "wikilink")                                          | 크로노스 렌더링 API와, 기반이 되는 네이티브 플랫폼 윈도 시스템 간의 인터페이스.                             |                                                   |
| [OpenCL](../Page/OpenCL.md "wikilink")                                            | 크로스 플랫폼 [병렬 컴퓨팅용](../Page/병렬_컴퓨팅.md "wikilink") API.                        |                                                   |
| [OpenGL](../Page/OpenGL.md "wikilink")                                            | 대부분의 [GPU](../Page/그래픽_처리_장치.md "wikilink") 벤더들이 구현한 3D 그래픽스 구현체.           | 대부분의 확장 기능들이 지원되지만 요청에 따라 덜 유명한 확장 기능들이 추가될 수 있다. |
| [OpenGL ES](../Page/OpenGL_ES.md "wikilink")                                      | 휴대 전화, 태블릿, 콘솔 등 [임베디드 시스템을](../Page/임베디드_시스템.md "wikilink") 위한 OpenGL.     |                                                   |
| [벌컨](../Page/벌컨_\(API\).md "wikilink")                                            | 차기 크로스 플랫폼 3D 그래픽스 API.                                                     |                                                   |
| [GLFW](https://ko.wikipedia.org/wiki/GLFW "wikilink")                             | OpenGL 및 벌컨 컨텍스트, 사용자 입력을 관리하는데 필요한 창 관리 라이브러리.                             |                                                   |
| [JAWT](https://ko.wikipedia.org/wiki/JAWT "wikilink")                             | [AWT](../Page/애브스트랙트_윈도_툴킷.md "wikilink") 네이티브 인터페이스.                       |                                                   |
| [nfd](https://ko.wikipedia.org/wiki/nfd "wikilink")                               | 크기가 작은 크로스 플랫폼 네이티브 파일 다이얼로그 라이브러리.                                         |                                                   |
| [tinyfd](https://ko.wikipedia.org/wiki/tinyfd "wikilink")                         | 크기가 작은 네이티브 다이얼로그 라이브러리.                                                    |                                                   |
| [OpenAL](../Page/OpenAL.md "wikilink")                                            | 3차원 오디오 API.                                                                | ALC 및 기타 확장 지원함.                                  |
| [OpenAL Soft](https://ko.wikipedia.org/wiki/OpenAL_Soft "wikilink")               | OpenAL의 자유 라이선스 소프트웨어 구현체.                                                  |                                                   |
| [bgfx](https://ko.wikipedia.org/wiki/bgfx "wikilink")                             | 다중 그래픽스 백엔드를 지원하는 크로스 플랫폼 렌더링 라이브러리.                                        |                                                   |
| [LibOVR](https://ko.wikipedia.org/wiki/LibOVR "wikilink")                         | [오큘러스 리프트](../Page/오큘러스_리프트.md "wikilink") SDK의 API.                        |                                                   |
| [NanoVG](https://ko.wikipedia.org/wiki/NanoVG "wikilink")                         | OpenGL을 사용한 2D 벡터 그래픽스 렌더링 라이브러리.                                           |                                                   |
| [Nuklear](https://ko.wikipedia.org/wiki/Nuklear "wikilink")                       | 단순 [GUI](../Page/그래픽_사용자_인터페이스.md "wikilink") 라이브러리.                        |                                                   |
| [par shapes](https://ko.wikipedia.org/wiki/par_shapes "wikilink")                 | [파라메트릭](https://ko.wikipedia.org/wiki/파라메트릭_서피스 "wikilink") 및 기타 단순 도형 생성기. |                                                   |
| [STB](https://ko.wikipedia.org/wiki/STB_\(라이브러리\) "wikilink")                     | 이미지, 사운드, 글꼴을 로드하기 위한 가벼운 싱글 파일 라이브러리.                                      |                                                   |
| [dyncall](https://ko.wikipedia.org/wiki/dyncall "wikilink")                       | 포터블한 방식으로 동적으로 C 함수를 호출하기 위한 라이브러리.                                         |                                                   |
| [C 동적 메모리 할당](../Page/C_동적_메모리_할당.md "wikilink")                                  | 저급(Low-level) 메모리 관리.                                                       |                                                   |
| [LMDB](https://ko.wikipedia.org/wiki/Lightning_Memory-Mapped_Database "wikilink") | [메모리 맵 파일을](../Page/메모리_맵_파일.md "wikilink") 이용한 고속 데이터베이스 라이브러리.            |                                                   |
| [xxHash](https://ko.wikipedia.org/wiki/xxHash "wikilink")                         | 고속 [해시 알고리즘](../Page/해시_함수.md "wikilink").                                  |                                                   |
| [VMA](https://ko.wikipedia.org/wiki/Vulkan_Memory_Allocator "wikilink")           | 벌컨 그래픽스 API용 메모리 할당자                                                        |                                                   |

제공되는 바인딩\[1\]\[2\]

## 저명한 사용

  - [마인크래프트](../Page/마인크래프트.md "wikilink")\[3\]

## 같이 보기

  - [JMonkeyEngine](https://ko.wikipedia.org/wiki/JMonkeyEngine "wikilink"), LWJGL 로 제작한 게임 엔진
  - [마인크래프트](../Page/마인크래프트.md "wikilink"), LWJGL 로 제작한 유명한 게임

## 각주

## 외부 링크

  - [공식 웹사이트](http://www.lwjgl.org/)
  - [GitHub](https://github.com/LWJGL)
  - [Stack Overflow](https://en.wikipedia.org/wiki/Stack_Overflow)

[분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자바로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바로_작성된_자유_소프트웨어 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:자바 API](https://ko.wikipedia.org/wiki/분류:자바_API "wikilink") [분류:자바 라이브러리](https://ko.wikipedia.org/wiki/분류:자바_라이브러리 "wikilink") [분류:비디오 게임 개발 소프트웨어](https://ko.wikipedia.org/wiki/분류:비디오_게임_개발_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.
2.
3.