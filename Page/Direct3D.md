> This article is converted from Wikipedia: [Direct3D](https://ko.wikipedia.org/wiki/Direct3D).


**다이렉트3D**()는 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")의 [DirectX](https://ko.wikipedia.org/wiki/DirectX "wikilink") [API](https://ko.wikipedia.org/wiki/API "wikilink")에서 [3차원 그래픽스](https://ko.wikipedia.org/wiki/3차원_컴퓨터_그래픽스 "wikilink") 연산과 출력을 담당하는 부분이다. 마이크로소프트의 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 운영 체제([윈도 95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") 이상)에서만 작동하며, [엑스박스](https://ko.wikipedia.org/wiki/엑스박스 "wikilink")와 [엑스박스 360](https://ko.wikipedia.org/wiki/엑스박스_360 "wikilink") 게임 콘솔의 그래픽 API로 사용되고 있다. 다이렉트3D와 비슷한 역할을 하는 API로는 [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink")이 있으며 역할은 같지만 각자가 서로 다른 장단점을 가지고 있다.

## 역사

[1992년](https://ko.wikipedia.org/wiki/1992년 "wikilink") 렌더모픽스(RenderMorphics)라는 회사에서 리얼리티 랩(Reality Lab)이라는 3차원 그래픽스 [API](https://ko.wikipedia.org/wiki/API "wikilink")를 만들기 시작했다. [1995년](https://ko.wikipedia.org/wiki/1995년 "wikilink") 2월에 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")는 [윈도 95에](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") 쓰일 3차원 그래픽스 API를 위하여 렌더모픽스 사를 인수했고, DirectX의 2.0 버전에서 처음 다이렉트3D가 도입되었다.

당시의 Direct3D는 하드웨어 제조사들이 지원하기 쉽도록 "실행 버퍼" 모델을 사용하고 있었는데 이는 프로그래머들에게 많은 불편을 야기했다. 다이렉트3D 5.0 버전에서는 DirectPrimitive API를 도입하여 실행 버퍼 모델을 대체하였다.

Direct3D 6.0 버전에서는 당시 최신 하드웨어를 지원할 수 있도록 많은 기능이 추가되었다. x86, [SSE](https://ko.wikipedia.org/wiki/스트리밍_SIMD_확장 "wikilink"), [3DNow](https://ko.wikipedia.org/wiki/3DNow "wikilink")를 위해 지오메트리 파이프라인이 최적화되었고, 간단한 [텍스처](https://ko.wikipedia.org/wiki/텍스처 "wikilink") 관리 기능이 추가되었으며, [범프 매핑](https://ko.wikipedia.org/wiki/범프_매핑 "wikilink") 등과 같은 고급 그래픽 효과를 사용할 수 있게 되었다.

Direct3D 7.0에서는 .dds 텍스처 파일 포맷이 도입되었으며, 6.0 버전에 추가되었던 기능들이 CPU가 동작했던 것을 그래픽 하드웨어가 맡아주기 위한 하드웨어 [변환 및 조명](https://ko.wikipedia.org/wiki/변환_및_조명 "wikilink") 기능이 추가되었다.

Direct3D 8에서는 [다이렉트드로](https://ko.wikipedia.org/wiki/다이렉트드로 "wikilink")를 독립적인 API로 분리시켰다. [버텍스 셰이더와](https://ko.wikipedia.org/wiki/버텍스_셰이더 "wikilink") [픽셀 셰이더가](https://ko.wikipedia.org/wiki/픽셀_셰이더 "wikilink") 지원되기 시작하였으며, 셰이더를 프로그래머가 직접 프로그래밍할 수 있게 되었지만 정해진 가이드라인이 없어서 그래픽 하드웨어 제조사가 제공하는 셰이딩 어셈블리어를 통해 구현해야 하는 단점이 있다.

Direct3D 9에서는 C언어와 유사한 모습의 고수준 셰이더 언어(HLSL)를 통해 가이드라인을 지원하기 시작하였다. 이로 인해서 [HDR](https://ko.wikipedia.org/wiki/하이_다이내믹_레인지_렌더링 "wikilink"), 정점 버퍼 인덱싱과 같은 기능을 사용할 수 있게 되었다.

Direct3D 10은 구조를 대폭 정리하는 등의 큰 변화를 거쳤다. [윈도 비스타에](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") 기본적으로 포함되어 있지만 하위 버전과의 호환성은 없어서 WDDM 기반에 Direct3D 9 수준의 기능을 구현한 Direct3D 9Ex 라이브러리가 포함되었다.

Direct3D 11은 Direct3D 10에 채택되지 못 했던 테셀레이션과 멀티스레드 기능이 정식으로 추가되었다. 윈도 비스타 SP2에서 플랫폼 업데이트를 통해 사용이 가능하며, 윈도 7부터 기본적으로 포함되어 있다.

Direct3D 12는 오픈소스의 벌컨과 AMD의 맨틀의 성격이 같다. 윈도 10에서만 사용이 가능하다.

## 디스플레이 모드

다이렉트3D는 다음의 두 가지 화면 방식을 제공한다:

  - **전체화면 모드**: 다이렉트3D 응용 프로그램은 디스플레이 장치로 모든 그래픽 출력을 만들어 낸다. 이 모드에서 다이렉트3D는 자동으로 Alt-Tab을 잡아 내고 화면 해상도와 화소 포맷을 프로그래머가 관여하지 않아도 설정하고 복원한다. 또한 '예외 합동 방식'(Exclusive Cooperative Mode) 때문에 오류를 찾아내고 수정하는 데에 많은 애를 먹을 수 있다.
  - **창 모드**: 결과물은 창 영역 안 쪽에 보인다. 다이렉트3D는 [GDI와](https://ko.wikipedia.org/wiki/그래픽_장치_인터페이스 "wikilink") 데이터를 주고 받으며 디스플레이의 그래픽 출력을 만들어 낸다. 드라이버 지원에 따라 창 모드는 전체 화면과 동일하게 수행할 수 있다.

## 파이프라인

1.  **입력 어셈블러**
2.  **[버텍스 셰이더](https://ko.wikipedia.org/wiki/버텍스_셰이더 "wikilink")**
3.  **[지오메트리 셰이더](https://ko.wikipedia.org/wiki/지오메트리_셰이더 "wikilink")**
4.  **스트림 출력**
5.  **레스터라이저**
6.  **[픽셀 셰이더](https://ko.wikipedia.org/wiki/픽셀_셰이더 "wikilink")**
7.  **출력 병합**

## 예제

다이렉트3D로 삼각형 그리기:

``` cpp
 // A 3-vertex polygon definition
 D3DLVERTEX v[3];
 // Vertex established
 v[0]=D3DLVERTEX( D3DVECTOR(0.f, 5.f, 10.f), 0x00FF0000, 0, 0, 0 );
 // Vertex established
 v[1]=D3DLVERTEX( D3DVECTOR(0.f, 5.f, 10.f), 0x0000FF00, 0, 0, 0 );
 // Vertex established
 v[2]=D3DLVERTEX( D3DVECTOR(0.f, 5.f, 10.f), 0x000000FF, 0, 0, 0 );
 // Function call to draw the triangle
 pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX, v, 3, 0 );
```

다이렉트3D 9로 삼각형 그리기:

``` cpp
 struct Vertex { float x, y, z; D3DCOLOR color; };
 Vertex triangle[] = {
  { 0.f, 5.f, 10.f, 0x00FF0000 },
  { 0.f, 5.f, 10.f, 0x0000FF00 },
  { 0.f, 5.f, 10.f, 0x000000FF }
 };
 // set Flexible Vertex Format
 pDevice->SetFVF(D3DFVF_XYZ | D3DFVF_DIFFUSE);
 // Draw - UP stands for 'user pointer', that is data
 //is provided through a pointer and not through buffers
 pDevice->DrawPrimitiveUP(D3DPT_TRIANGLELIST, 1, triangle, sizeof(Vertex));
```

## 같이 보기

  - [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink")
  - [글라이드](https://ko.wikipedia.org/wiki/글라이드 "wikilink")

## 외부 링크

  - [DirectX 웹사이트](http://www.gamesforwindows.com/en-US/directx/)
  - [MSDN: DirectX Graphics and Gaming](http://msdn.microsoft.com/en-us/library/windows/desktop/ee663274)
  - [DirectX 10: The Future of PC Gaming](https://web.archive.org/web/20080706004419/http://www.bit-tech.net/hardware/2006/11/30/directx10_future_of_pc_gaming/1.html) Technical article discussing the new features of DirectX 10 and their impact on computer games

[3D](https://ko.wikipedia.org/wiki/분류:DirectX "wikilink") [분류:3차원 컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/분류:3차원_컴퓨터_그래픽스 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:1995년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1995년_소프트웨어 "wikilink")