> This article is converted from Wikipedia: [VR](https://ko.wikipedia.org/wiki/VR).


**파워VR**(PowerVR)은 [이매지네이션 테크놀로지의](https://ko.wikipedia.org/wiki/이매지네이션_테크놀로지 "wikilink") 그래픽 사업 부문으로, 2D/3D 가속, 비디오 인코딩/디코딩, 이미지 프로세싱, [DirectX](https://ko.wikipedia.org/wiki/DirectX "wikilink"), [OpenGL ES](../Page/OpenGL_ES.md "wikilink"), [OpenVG](https://ko.wikipedia.org/wiki/OpenVG "wikilink"), [OpenCL](https://ko.wikipedia.org/wiki/OpenCL "wikilink") 가속 등을 지원하는 임베디드 그래픽 하드웨어 및 소프트웨어를 개발하고 있다.

초기 PowerVR 제품군은 데스크톱 PC 시장에서 [3dfx](../Page/3dfx.md "wikilink")와 같은 기존 회사의 그래픽 카드보다 더 나은 가격대 성능비로 경쟁하는 제품이었다. PC 그래픽 카드 시장이 [OpenGL](../Page/OpenGL.md "wikilink")과 [Direct3D](../Page/Direct3D.md "wikilink") 등장 이후로 빠르게 변화하면서, PowerVR과 같은 소규모 업체는 시장에서 퇴출되었었다.

이후 PowerVR은 노트북 컴퓨터를 대상으로 한 저전력 그래픽 카드인 [GPU(그래픽 처리 장치)로](https://ko.wikipedia.org/wiki/그래픽_처리_장치 "wikilink") 방향을 전환하였다. 시간이 지나면서 임베디드 시스템, 핸드헬드 장치, 스마트폰의 급격한 시장확장으로 여기에 사용되는 SoC에 사용될 수 있도록 변화하였다. PowerVR 가속기는 PowerVR에서 직접 제조하지 않으며, 회로 설계 및 특허권은 TI, 인텔, NEC, 삼성, ST마이크로일렉트로닉스, 프리스케일, 애플, NXP 등 반도체 제조 회사에 라이선스된다.

## 기술

PowerVR 칩셋은 3D 처리에 타일 기반 지연된 렌더링(Tile-based deferred rendering, TBDR)을 사용한다. 폴리곤을 생성하는 프로그램이 드라이버에 삼각형 정보를 전달해 주면, 드라이버에서는 메모리에 연속된 삼각형이나 인덱스 형식으로 저장한다. 다른 아키텍처와는 다르게, 현재 비디오 프레임에 사용되는 모든 폴리곤 정보가 도착하기 전까지 렌더링이 실행되지 않는다. 또한, 가능한 경우 각각 픽셀에서 어떤 표면이 보이는지를 결정하기 전까지 텍스처와 셰이딩 작업이 지연된다. 지연된 렌더링은 이러한 아키텍처를 이야기한다.

렌더링 과정에서 전체 디스플레이는 작은 사각형 그리드로 나뉘며, 각각의 그리드는 타일로 취급된다. 각각 타일에는 그 타일 내에서 보이는 삼각형 정보가 연결되며, 타일별 렌더링된 이미지가 합쳐져서 전체 이미지가 나타난다. 타일 렌더링 과정은 레이캐스팅과 비슷하게 이루어진다. 각각 광선은 타일별 삼각형에 비쳐지며, 각각 픽셀은 카메라에서 가장 가까운 삼각형에 의해서 그려진다. PowerVR 하드웨어는 개별 타일 행과 연결된 다각형의 깊이 정보를 1 사이클에 계산한다.

이 방식은 안 보이는 폴리곤을 그리지 않아도 된다는 장점을 가지고 있다. 또한 폴리곤 처리 순서와는 관계 없이 반투명 폴리곤의 투명도를 올바르게 처리할 수 있다. (시리즈 2 및 MBX에만 구현되었다. API 지원 문제 및 비용 문제 때문에 일반적으로 포함되지 않는다.) 한 번에 렌더링이 한 타일만 이루어지기 때문에, 전체 타일을 더 빠른 칩 메모리에 저장해 두고 다음 타일을 처리하기 전에 비디오 메모리에 복사할 수 있다. 일반적인 경우 개별 타일은 프레임당 한 번만 처리된다.

현재 PowerVR은 그래픽 시장에서 유일한 TBDR 기반 카드이다. 마이크로소프트는 탤리스먼 프로젝트에서 타일 기반 렌더링을 연구했던 적이 있었다. 타일 기반 3D 그래픽 기술을 개발했던 기가픽셀 사는 3dfx에 인수되었고, 이후 엔비디아에 인수되지만 엔비디아에서는 타일 기반 렌더링을 도입할 계획이 없다. 인텔은 내장 그래픽에서 비슷한 개념인 존 렌더링을 사용하고 있으나, 숨은 공간 삭제(HSR) 및 지연된 텍스처 작업을 완벽하게 실행하지 않는다.

현재 PowerVR 소프트웨어 및 하드웨어는 동영상 인코딩/디코딩, 이미지 프로세싱, DirectX, OpenGL ES, OpenVG, OpenCL 가속 등을 지원한다.\[1\]

## PowerVR 칩셋

  - <sup>\[1\]</sup> 이매지네이션 테크놀로지 공식 데이터
  - <sup>\[2\]</sup> USSE (Universal Scalable Shader Engine) 파이프/텍스처 매핑 유닛(TMU)
  - <sup>\[3\]</sup> USSE2 (Universal Scalable Shader Engine 2) 파이프/텍스처 매핑 유닛(TMU)
  - 모든 모델은 타일 기반 지연된 렌더링(TBDR)을 지원한다.

### 시리즈 1 (NEC)

[섬네일](https://ko.wikipedia.org/wiki/파일:VideoLogic_Apocalypse_3Dx.jpg "wikilink") PCX1(μPD62010) 및 PCX2(μPD62011) 모델이 존재한다. PCX1 모델은 1996년 출시되었고, 초당 30만 폴리곤을 처리할 수 있다. PCX2 모델은 1997년 출시되었고, 초당 45만 폴리곤으로 성능이 향상되었다. PCI 버스 확장 카드는 4MB 전용 비디오 메모리를 탑재하였고, 3D 가속 전용으로 출시되었기 때문에 별도의 2D 카드가 필요하다. 비디오 오버레이 기능 및 그래픽 카드 메모리에 직접 접근하는 기능을 제공한다. Direct3D 및 전용 API인 SGL(Super Graphics Library)를 지원한다. 컴팩과 같은 컴퓨터 회사에 OEM으로 납품되기도 했고, 매트록스와 같은 회사에서 PCI 카드로도 출시되었다.

  - 모든 모델은 DirectX 3.0을 지원한다.

| 모델            | 출시        | 공정 ([nm](https://ko.wikipedia.org/wiki/나노미터 "wikilink")) | 메모리 (MiB)   | 코어 클럭 (MHz) | 메모리 클럭 (MHz) | 코어 구성<sup>1</sup> | 필레이트 | 메모리 |
| ------------- | --------- | -------------------------------------------------------- | ----------- | ----------- | ------------ | ----------------- | ---- | --- |
| MOperations/s | MPixels/s | MTextels/s                                               | MVertices/s | 대역폭 (GB/s)  | 버스 종류        | 버스 폭 (비트)         |      |     |
| PCX1          | 1996      | 500                                                      | 4           | 60          | 60           | 1:0:1:1           | 60   | 60  |
| PCX2          | 1997      | 350                                                      | 4           | 66          | 66           | 1:0:1:1           | 66   | 66  |
|               |           |                                                          |             |             |              |                   |      |     |

  - <sup>1</sup> 픽셀 셰이더:버텍스 셰이더:텍스처 매핑 유닛:렌더 출력 유닛

### 시리즈 2 (NEC)

2세대 PowerVR2(칩 코드명 CLX2)는 1998년 2월 23일 출시되었다. 2D 표시 기능이 추가되어서 PC 플랫폼에서 독립된 카드로 작동할 수 있다. [세가](https://ko.wikipedia.org/wiki/세가 "wikilink")에서는 [새턴의](https://ko.wikipedia.org/wiki/세가_새턴 "wikilink") 후속 기종 [드림캐스트를](https://ko.wikipedia.org/wiki/세가_드림캐스트 "wikilink") 설계하면서 내부 경쟁을 벌였다. 그 결과 [3dfx](../Page/3dfx.md "wikilink") 부두 2를 제치고 PowerVR2가 선정되었다. 그 결과 드림캐스트로 출시된 [퀘이크 III 아레나와](https://ko.wikipedia.org/wiki/퀘이크_III_아레나 "wikilink") 같은 게임은 PC 버전에 비해서 성능과 화질이 더 좋았다. PC용으로 출시된 Neon 250은 시장에 늦게 등장하였고, 출시 당시에는 중급형 그래픽 카드 시장에 머물러야 했다.

  - 모든 제품은 250 nm 공정으로 제조되었다.
  - 모든 제품은 DirectX 6.0을 지원하고, PMX1은 MiniGL을 지원하였다.

| 모델            | 출시        | 메모리 (MiB)  | 코어 클럭 (MHz) | 메모리 클럭 (MHz) | 코어 구성<sup>1</sup> | 필레이트      | 메모리 |
| ------------- | --------- | ---------- | ----------- | ------------ | ----------------- | --------- | --- |
| MOperations/s | MPixels/s | MTextels/s | MVertices/s | 대역폭 (GB/s)   | 버스 종류             | 버스 폭 (비트) |     |
| CLX2          | 1998      | 8          | 100         | 100          | 1:0:1:1           | 100       | 100 |
| PMX1          | 1999      | 32         | 125         | 125          | 1:0:1:1           | 125       | 125 |
|               |           |            |             |              |                   |           |     |

  - <sup>1</sup> 픽셀 셰이더:버텍스 셰이더:텍스처 매핑 유닛:렌더 출력 유닛

### 시리즈 3 (ST)

[right](https://ko.wikipedia.org/wiki/파일:STMicroelectronics_STG4500_\(PowerVR_Kyro_II\).png "wikilink") 2001년 [ST마이크로일렉트로닉스](../Page/ST마이크로일렉트로닉스.md "wikilink")에서는 PowerVR 3세대를 라이선스하여 STG4000 카이로 및 STG4500 카이로 II 칩에 사용하였다. 당시 경쟁 제품인 ATI [라데온](../Page/라데온.md "wikilink") DDR 및 엔비디아 [지포스 2](https://ko.wikipedia.org/wiki/지포스_2 "wikilink") GTS의 성능을 앞질렀으나, 하드웨어 T\&L 기능이 없었다. 많은 게임에서 하드웨어 T\&L 기능을 지원하면서 카이로 II의 성능상 이점이 퇴색되었다.

  - 모든 모델은 DirectX 6.0을 지원한다.

| 모델            | 출시        | 공정 (nm)    | 메모리 (MiB)   | 코어 클럭 (MHz) | 메모리 클럭 (MHz) | 코어 구성<sup>1</sup> | 필레이트 | 메모리  |
| ------------- | --------- | ---------- | ----------- | ----------- | ------------ | ----------------- | ---- | ---- |
| MOperations/s | MPixels/s | MTextels/s | MVertices/s | 대역폭 (GB/s)  | 버스 종류        | 버스 폭 (비트)         |      |      |
| STG4000       | 2000      | 250        | 32/64       | 115         | 115          | 2:0:2:2           | 230  | 230  |
| STG4500       | 2001      | 180        | 32/64       | 175         | 175          | 2:0:2:2           | 350  | 350  |
| STG4800       | 미출시       | 180        | 64          | 200         | 200          | 2:0:2:2           | 400  | 400  |
| STG5500       | 미출시       | 130        | 64          | 250         | 250          | 4:0:4:4           | 1000 | 1000 |
|               |           |            |             |             |              |                   |      |      |

  - <sup>1</sup> 픽셀 셰이더:버텍스 셰이더:텍스처 매핑 유닛:렌더 출력 유닛

### 시리즈 4 (ST)

PowerVR 4세대 기반인 STM의 STG5000 칩셋은 하드웨어 T\&L을 지원하였으나, 시장에 출시되지는 못하였다. STM에서 그래픽 칩셋 사업을 중단하면서 STG5000 및 카이로 3 칩셋의 출시가 취소되었다.

| 모델                           | 년도                       | 다이 크기 (mm<sup>2</sup>)<sup>\[1\]</sup>                      | 코어 구성                                  | 필레이트 (@ 200 MHz) | 버스 폭 (비트) | API (버전) |
| ---------------------------- | ------------------------ | ----------------------------------------------------------- | -------------------------------------- | ---------------- | --------- | -------- |
| MTriangles/s<sup>\[1\]</sup> | MPixel/s<sup>\[1\]</sup> | [DirectX](https://ko.wikipedia.org/wiki/DirectX "wikilink") | [OpenGL](../Page/OpenGL.md "wikilink") |                  |           |          |
| MBX Lite                     | 2001년 2월                 | 4@130 nm?                                                   | 0/1/1/1                                | 1.0              | 100       | 64       |
| MBX                          | 2001년 2월                 | 8@130 nm?                                                   | 0/1/1/1                                | 1.68             | 150       | 64       |

### MBX

PowerVR은 모바일 그래픽 시장에 저전력 PowerVR MBX를 출시하였다. MBX와 후속작 SGX는 [인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink"), [TI](https://ko.wikipedia.org/wiki/TI "wikilink"), [삼성](https://ko.wikipedia.org/wiki/삼성 "wikilink"), [NEC](https://ko.wikipedia.org/wiki/NEC "wikilink"), [NXP](https://ko.wikipedia.org/wiki/NXP "wikilink"), [프리스케일](https://ko.wikipedia.org/wiki/프리스케일 "wikilink"), [르네사스](https://ko.wikipedia.org/wiki/르네사스 "wikilink"), 선플러스에 라이선스되었다. [아이폰](../Page/아이폰.md "wikilink") 1세대, [노키아 N95](https://ko.wikipedia.org/wiki/노키아_N95 "wikilink"), [소니에릭슨 P1](https://ko.wikipedia.org/wiki/소니에릭슨_P1 "wikilink"), [모토로라 Z8](https://ko.wikipedia.org/wiki/모토로라_Z8 "wikilink"), [아이팟](https://ko.wikipedia.org/wiki/아이팟 "wikilink") 등 스마트폰 및 미디어 장치에 사용되었다.

MBX는 MBX 및 MBX Lite 두 종류로 출시되었다. 두 제품이 지원하는 기능은 같으나, MBX는 속도에 최적화되었고 MBX Lite는 저전력에 최적화되었다. MBX는 FPU, Lite FPU, VGP, VGP Lite와 함께 사용될 수 있다.

### 비디오 및 디스플레이 코어

PowerVR은 비디오 코어(MVED/VXD) 및 비디오/디스플레이 코어(PDP)를 지원하기 시작하였다. HD/SD 동영상 디코딩을 지원한다. PDP 시리즈는 소니 브라비아와 같은 HDTV에 사용되었다.

### 시리즈 5 (SGX)

PowerVR 시리즈 5 SGX는 픽셀 셰이더, 버텍스 셰이더, 지오메트리 셰이더를 하드웨어에서 지원하며, OpenGL ES 2.0 및 DirectX 10.1, 셰이더 모델 4.1을 지원한다.

SGX GPU 코어는 다양한 포터블 장치의 SoC에 사용되었다. PowerVR이 사용된 장치 SoC는 애플 A4, TI OMAP 3 및 4, 삼성 허밍버드 등이다. 인텔은 메드필드 플랫폼에서 SGX540을 사용하였다.\[2\]

| 모델                           | 년도                       | 다이 크기 (mm<sup>2</sup>)<sup>\[1\]</sup> | 코어 구성<sup>\[2\]</sup> | 필레이트 (@ 200 MHz) | 버스 폭 (비트) | API (버전) | GFLOPS(@ 200 MHz) |
| ---------------------------- | ------------------------ | -------------------------------------- | --------------------- | ---------------- | --------- | -------- | ----------------- |
| MTriangles/s<sup>\[1\]</sup> | MPixel/s<sup>\[1\]</sup> | DirectX                                | OpenGL                | OpenGL ES        |           |          |                   |
| SGX520                       | 2005년 7월                 | 2.6@65 nm                              | 1/1                   | 7                | 100       | 32-128   | 미지원               |
| SGX530                       | 2005년 7월                 | 7.2@65 nm                              | 2/1                   | 14               | 200       | 32-128   | 미지원               |
| SGX531                       | 2006년 10월                |                                        | 2/1                   | 14               | 200       | 32-128   | 미지원               |
| SGX535                       | 2007년 11월                |                                        | 2/2                   | 14               | 400       | 32-128   | 9.0c              |
| SGX540                       | 2007년 11월                |                                        | 4/2                   | 20               | 400       | 32-128   | 미지원               |
| SGX545                       | 2010년 1월                 | 12.5@65 nm                             | 4/2                   | 40               | 400       | 32-128   | 10.1              |

### 시리즈 5XT (SGXMP)

PowerVR 시리즈 5XT SGXMP 칩은 SGX 시리즈의 다중 코어 버전으로 추가 개선이 이루어졌다. [플레이스테이션 비타](https://ko.wikipedia.org/wiki/플레이스테이션_비타 "wikilink") 장치에는 PowerVR SGX543(MP4+) 모델이 채용되었다. 일반적인 MP4 모델과의 차이는 소니 제품을 위해 추가된 기능이 있다. MP4는 쿼드코어, MP8은 옥타코어 기반 칩이다. 애플 A5를 사용하는 아이패드 2세대 및 [아이폰 4S](../Page/아이폰_4S.md "wikilink") 칩에는 듀얼코어 SGX543MP2가 탑재되어 있다. 아이패드 3세대는 쿼드코어 MP4가 탑재되었다.\[3\]

| 모델                           | 출시                       | 코어                                                          | 다이 크기 (mm<sup>2</sup>)<sup>\[1\]</sup> | 코어 구성<sup>\[3\]</sup>                                     | 필레이트 (@ 200 MHz) | 버스 폭 (비트) | API (버전) | GFLOPS(@ 200 MHz, 코어당) |
| ---------------------------- | ------------------------ | ----------------------------------------------------------- | -------------------------------------- | --------------------------------------------------------- | ---------------- | --------- | -------- | ---------------------- |
| MTriangles/s<sup>\[1\]</sup> | GPixel/s<sup>\[1\]</sup> | [DirectX](https://ko.wikipedia.org/wiki/DirectX "wikilink") | [OpenGL](../Page/OpenGL.md "wikilink") | [OpenCL](https://ko.wikipedia.org/wiki/OpenCL "wikilink") |                  |           |          |                        |
| SGX543                       | 2009년 1월                 | 1-16                                                        | 5.4@32 nm                              | 4/2                                                       | 35               | 3.2       | 128-256  | 9.0 L3                 |
| SGX544                       | 2010년 6월                 | 1-16                                                        | 5.4@32 nm                              | 4/2                                                       | 35               | 3.2       | 128-256  | 9.0 L3                 |
| SGX554                       | 2010년 12월                | 1-16                                                        | 8.7@32 nm                              | 8/2                                                       | 35               | 3.2       | 128-256  | 9.0 L3                 |

SGXMP는 단일 및 다중 코어 구성으로 사용될 수 있다.\[4\]

### 시리즈 6 (Rogue)

PowerVR 시리즈 6은 코드명 'Rogue'인 새로운 아키텍처를 채용하였다. ST-에릭슨은 개발 중인 NovaThor 프로세서에 PowerVR 시리즈 6을 탑재할 예정이라고 밝혔다.\[5\] 미디어텍은 태블릿 대상 쿼드코어 MT8135(Cortex-A15 및 A7 각각 2개) 칩에 PowerVR 시리즈 6을 탑재할 것이라고 밝혔다.\[6\] 시리즈 6 코어를 여러 개 장착한 시리즈 6XT가 현재 개발 중이다.

클러스터당 2개의 TMU를 장착하였고 최대 GFLOPS는 FP32 값에만 해당된다.\[7\] G6x00 계열은 면적, G6x30 계열은 성능에 최적화되었다.

| 모델          | 출시        | 코어 수       | 다이 크기 (mm<sup>2</sup>)                                      | 코어 구성<sup>\[3\]</sup>                  | SIMD 레인                                      | 필레이트 (@650 MHz) | 버스 폭 (비트) | API (버전) | GFLOPS(@650 MHz, 코어당) |
| ----------- | --------- | ---------- | ----------------------------------------------------------- | -------------------------------------- | -------------------------------------------- | --------------- | --------- | -------- | --------------------- |
| MPolygons/s | 픽셀 (GP/s) | 텍스처 (GT/s) | [DirectX](https://ko.wikipedia.org/wiki/DirectX "wikilink") | [OpenGL](../Page/OpenGL.md "wikilink") | [OpenGL ES](../Page/OpenGL_ES.md "wikilink") |                 |           |          |                       |
| G6100       | 2013년 2월  | 1          |                                                             | 1/4                                    | 16                                           |                 | 20.8      | 2.6      | 128                   |
| G6200       | 2012년 1월  | 2          |                                                             | 2/2                                    | 32                                           | 163             | 20.8      | 2.6      |                       |
| G6230       | 2012년 6월  | 2          |                                                             | 2/2                                    | 32                                           | 163             | 20.8      | 2.6      |                       |
| G6400       | 2012년 1월  | 4          |                                                             | 4/2                                    | 64                                           | 163             | 20.8      | 5.2      |                       |
| G6430       | 2012년 6월  | 4          |                                                             | 4/2                                    | 64                                           | 163             | 20.8      | 5.2      |                       |
| G6630       | 2012년 11월 | 6          |                                                             | 6/2                                    | 96                                           | 163             | 20.8      | 7.8      |                       |
|             |           |            |                                                             |                                        |                                              |                 |           |          |                       |
|             |           |            |                                                             |                                        |                                              |                 |           |          |                       |

## 참조

[모바일 GPU 동향(ETRI-전자통신동향분석, 2013,한진호,변경진,엄낙웅)](https://web.archive.org/web/20161104020653/http://www.dbpia.co.kr/SKnowledge/ArticleDetail/NODE03608886)

## 외부 링크

  - [공식 사이트](http://www.imgtec.com/)

[분류:그래픽 처리 장치](https://ko.wikipedia.org/wiki/분류:그래픽_처리_장치 "wikilink")

1.  [Texas Instruments announces multi-core, 1.8GHz OMAP4470 ARM processor for Windows 8](http://www.engadget.com/2011/06/02/texas-instruments-announces-multi-core-1-8ghz-omap4470-arm-proc/), By Amar Toor, Jun 2nd 2011, Engadget
2.  [Intel's Medfield & Atom Z2460 Arrive for Smartphones: It's Finally Here](http://www.anandtech.com/show/5365/intels-medfield-atom-z2460-arrive-for-smartphones), by Anand Lal Shimpi, Jan 10 2012, anandtech
3.  [Apple iPad 2 GPU Performance Explored: PowerVR SGX543MP2 Benchmarked](http://www.anandtech.com/show/4216/apple-ipad-2-gpu-performance-explored-powervr-sgx543mp2-benchmarked), by Anand Lal Shimpi, 2011/03/12, Anandtech
4.  [TI Announces OMAP4470 and Specs: PowerVR SGX544, 1.8 GHz Dual Core Cortex-A9](http://www.anandtech.com/show/4413/ti-announces-omap-4470-and-specs-powervr-sgx544-18-ghz-dual-core-cortexa9), by Brian Klug, 6/2/2011, AnandTech, Inc.
5.  , Imagination Technologies Ltd.
6.  , MediaTek Inc.
7.  <http://www.anandtech.com/show/7335/the-iphone-5s-review/7>