> This article is converted from Wikipedia: [ \(API\)](https://ko.wikipedia.org/wiki/_\(API\)).


**벌컨**(Vulkan)은 오버헤드가 적은 크로스 플랫폼 3D 그래픽스 및 컴퓨팅 API이다. 이는 GDC 2015에서 [크로노스 그룹에](https://ko.wikipedia.org/wiki/크로노스_그룹 "wikilink") 의해 처음으로 소개되었다.

초기의 Vulkan API는 [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink")의 차세대 버전으로 준비되었는데, 현재는 "OpenGL" 이라는 이름을 이어가지 않고 Vulkan 이라는 이름으로 결정되었다.

OpenGL처럼 Vulkan은 게임이나 상호작용성 미디어와 같은 고성능 실시간 3D 그래픽스 애플리케이션을 모든 플랫폼에서 고성능으로 CPU를 적게 사용하도록 개발하는 것을 목표로 만들어진 [API](https://ko.wikipedia.org/wiki/API "wikilink")이며 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")의 [Direct3D 12](https://ko.wikipedia.org/wiki/Direct3D_12 "wikilink"), [애플](https://ko.wikipedia.org/wiki/애플 "wikilink")의 [메탈](../Page/메탈_\(API\).md "wikilink"), [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")의 [맨틀과](https://ko.wikipedia.org/wiki/맨틀_\(API\) "wikilink") 같은 성격의 [API](https://ko.wikipedia.org/wiki/API "wikilink")이다. CPU 사용량에 대해서 더 이야기 하자면 Vulkan은 [멀티 코어](https://ko.wikipedia.org/wiki/멀티_코어 "wikilink") CPU의 여러 코어 사이에 로드를 더 잘 분배할 수 있다.

## 역사

크로노스 그룹은 2014년 7월 차세대 그래픽스 API를 만들기 위한 프로젝트를 시작하였으며, 이는 [밸브 코퍼레이션의](https://ko.wikipedia.org/wiki/밸브_코퍼레이션 "wikilink") 킥오프 미팅과 함께한다.\[1\] [SIGGRAPH](https://ko.wikipedia.org/wiki/SIGGRAPH "wikilink") 2014에서 이 프로젝트는 참여자들의 요청에 따라 공개 발표되었다.\[2\]

## 벌컨을 지원하는 소프트웨어

### 비디오 게임

  - [The Talos Principle](https://ko.wikipedia.org/wiki/The_Talos_Principle "wikilink") - 벌컨 렌더링을 지원하는 최초의 게임.\[3\]
  - [도타 2](../Page/도타_2.md "wikilink") - 2016년 5월 벌컨 지원을 공개.\[4\]
  - [둠](https://ko.wikipedia.org/wiki/둠_\(2016년_비디오_게임\) "wikilink") - 2016년 7월 벌컨 지원을 공개.\[5\]
  - vkQuake - 벌컨 [퀘이크](https://ko.wikipedia.org/wiki/퀘이크_\(비디오_게임\) "wikilink") [이식을](https://ko.wikipedia.org/wiki/이식_\(컴퓨팅\) "wikilink") 2016년 7월 공개.\[6\]\[7\]
  - [Roblox](https://ko.wikipedia.org/wiki/Roblox "wikilink") - 2017년 3월, Roblox를 위한 벌컨 지원이 추가됨.
  - [Star Citizen](https://ko.wikipedia.org/wiki/Star_Citizen "wikilink") - 2017년 3월, 클라우드 임페리엄 게임즈의 그래픽스 프로그래밍 감독 Alistair Brown은 공식 스타 시티즌 포럼에서 클라우드 임페리엄이 이제 스타 시티즌과 Squadron 42에 벌컨 구현을 집중할 것이라고 발표하였다. [DirectX](https://ko.wikipedia.org/wiki/DirectX "wikilink") 지원은 중단될 것인데, 이는 고객들이 윈도우 10을 사용하도록 강제하기 때문이다.\[8\]
  - [매드 맥스](https://ko.wikipedia.org/wiki/매드_맥스 "wikilink") - 2017년 3월, 개발자들은 리눅스 포팅으로 예외적으로 벌컨의 베타 지원을 추가하였다.\[9\]
  - [Ballistic Overkill](https://ko.wikipedia.org/wiki/Ballistic_Overkill "wikilink") - 2017년 5월 벌컨 지원을 공개.
  - Quake III Arena Kenny Edition - [퀘이크 3 엔진](https://ko.wikipedia.org/wiki/퀘이크_3_엔진 "wikilink") 모드(mod)가 2017년 5월 벌컨 지원을 추가.
  - [Ashes of the Singularity: Escalation](https://ko.wikipedia.org/wiki/Ashes_of_the_Singularity:_Escalation "wikilink") - 차기작에 벌컨 지원 추가 예정.
  - vkDoom3 - [Doom3 BFG의](https://ko.wikipedia.org/wiki/Doom_3:_BFG_Edition "wikilink") 벌컨 포팅 지원을 2017년 8월 공개.
  - [Wolfenstein II: The New Colossus](https://ko.wikipedia.org/wiki/Wolfenstein_II:_The_New_Colossus "wikilink") - 벌컨만 지원. 2017년 런칭.
  - [X4: Foundations](https://ko.wikipedia.org/wiki/X4:_Foundations "wikilink") - 벌컨 전용 그래픽스 엔진과 함께 2018년 런칭 예정
  - [X-Plane 11](https://ko.wikipedia.org/wiki/X-Plane "wikilink") - Laminar Research는 2017년 하반기에 OpenGL에서 벌컨으로 이동할 예정이며, 테스트는 2018년에 시작.

### 게임 콘솔 에뮬레이터

  - Beetle/Mednafen PSX,\[10\] [Mednafen PlayStation의](https://ko.wikipedia.org/wiki/Mednafen "wikilink") Libretro 포팅
  - [돌핀](https://ko.wikipedia.org/wiki/돌핀_\(에뮬레이터\) "wikilink")\[11\]
  - [Mupen64Plus Libretro 포팅](https://ko.wikipedia.org/wiki/Mupen64Plus "wikilink")의\[12\]
  - [RPCS3](https://ko.wikipedia.org/wiki/RPCS3 "wikilink")
  - [PPSSPP](https://ko.wikipedia.org/wiki/PPSSPP "wikilink")
  - [Xenia](http://xenia.jp/)

### 게임 엔진

  - [소스](https://ko.wikipedia.org/wiki/소스_\(게임_엔진\) "wikilink") - 2015년 3월, [밸브 코퍼레이션은](https://ko.wikipedia.org/wiki/밸브_코퍼레이션 "wikilink") 소스 2 엔진을 발표하였으며 이는 오리지널 [소스](https://ko.wikipedia.org/wiki/소스_\(게임_엔진\) "wikilink") 엔진의 뒤를 이으며 벌컨을 지원한다.\[13\]\[14\]
  - 시리어스 엔진 4 - 2016년 2월, [Croteam](https://ko.wikipedia.org/wiki/Croteam "wikilink")은 시리어스 엔진에 벌컨을 지원하고 있었다고 발표하였다.\[15\]
  - [언리얼 엔진](https://ko.wikipedia.org/wiki/언리얼_엔진 "wikilink") - 2016년 2월,[에픽게임즈](../Page/에픽게임즈.md "wikilink")는 언리얼 엔진 4가 [삼성그룹](https://ko.wikipedia.org/wiki/삼성그룹 "wikilink")의 [삼성 갤럭시 S7](../Page/삼성_갤럭시_S7.md "wikilink") 언팩 행사에서 벌컨을 지원할 것임을 발표하였다.\[16\]\[17\]
  - [토크](https://ko.wikipedia.org/wiki/토크_\(게임_엔진\) "wikilink") - 2016년 4월, 개발자 공동체는 벌컨 지원 포함을 발표하였다.\[18\]\[19\]
  - [퀘이크 엔진](https://ko.wikipedia.org/wiki/퀘이크_엔진 "wikilink") - 2016년 7월 벌컨 지원이 추가되었다.
  - [id Tech 3](https://ko.wikipedia.org/wiki/id_Tech_3 "wikilink") - 2017년 5월 벌컨 지원이 추가되었다.
  - [id Tech 4](https://ko.wikipedia.org/wiki/id_Tech_4 "wikilink") - 2017년 8월 벌컨 지원이 추가되었다.
  - [id Tech 6](https://ko.wikipedia.org/wiki/id_Tech_6 "wikilink") - 2016년 5월, [이드 소프트웨어는](https://ko.wikipedia.org/wiki/이드_소프트웨어 "wikilink") 테크 6 엔진을 구동하는 둠이 벌컨을 지원할 것이라 발표하였다.\[20\]
  - [Xenko](https://ko.wikipedia.org/wiki/Xenko "wikilink") - 2016년 7월 벌컨 지원이 추가되었다.\[21\]
  - [유니티](https://ko.wikipedia.org/wiki/유니티_\(게임_엔진\) "wikilink") - 이 엔진은 버전 5.6부터 벌컨 지원이 추가되었다.\[22\]
  - [크라이엔진](https://ko.wikipedia.org/wiki/크라이엔진 "wikilink") - 5.4 릴리스에 벌컨 지원이 추가되었다.\[23\]
  - Intrinsic - 벌컨을 지원하는 자유-오픈 소스 크로스 플랫폼 게임 엔진.\[24\]
  - [Unigine](https://ko.wikipedia.org/wiki/Unigine "wikilink") - 2017년 4월, [Unigine Corp는](https://ko.wikipedia.org/wiki/Unigine_Corp "wikilink") Unigine의 벌컨 지원이 2017년 로드맵에 있다고 발표하였다.\[25\]
  - Abyss Engine - 2017년 5월, 딥 실버 FISHLABS는 벌컨을 지원하는 안드로이드에 갤럭시 온 파이어 3를 출시하였다.\[26\]
  - Banshee 3D - 벌컨을 지원하는 자유-오픈 소스 크로스 플랫폼 게임 엔진.\[27\]
  - [Godot](https://ko.wikipedia.org/wiki/Godot "wikilink") - 2차원, 3차원 크로스 플랫폼 오픈 소스, 게임 엔진. 2018년 2월 말에 개발자들은 모든 플랫폼을 대상으로 OpenGL ES 3만을 사용하지 않고 OpenGL ES 2와 벌컨을 혼합하여 사용하겠다고 발표하였다\[28\].

### 렌더링 엔진

  - UX3D Engine - 2017년 9월 벌컨 지원이 추가되었다.

### 개발 도구

  - [GPU PerfStudio](https://ko.wikipedia.org/wiki/GPU_PerfStudio "wikilink") 3.6은 리눅스, 윈도우에서 벌컨을 지원한다.\[29\]
  - [GTK+ Scene Graph Kit은](https://ko.wikipedia.org/wiki/GTK+_Scene_Graph_Kit "wikilink") GTK+ 3.90의 일부로서 2017년 3월 출시되었으며 벌컨 렌더링 경로를 포함한다.\[30\]
  - [RenderDoc](https://ko.wikipedia.org/wiki/RenderDoc "wikilink")은 벌컨을 지원하며, 그 추가 시점은 2016년 2월 10일이다.\[31\]

### 운영 체제 구성 요소

벌컨 윈도우 시스템 통합(Vulkan Window System Integration, WSI)은 [EGL이](https://ko.wikipedia.org/wiki/EGL_\(API\) "wikilink") OpenGL ES를 위해 하는 것과 동일한 것을 벌컨을 위해 한다.\[32\] EGL은 네이티브 플랫폼 윈도잉 시스템과 통신할 목적으로 OpenGL ES 프로그램에 쓰인다. EGL은 컨텍스트 관리, 표면 바인딩, 렌더링 동기화를 관리한다.

## 호환성

| 기업                                                                         | 하드웨어                                                    | 소프트웨어 지원: Vulkan 1.0                                                                                                             |
| -------------------------------------------------------------------------- | ------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| 마이크로아키텍처                                                                   | 이용 가능 시점                                                | GPU ([칩](https://ko.wikipedia.org/wiki/다이_\(집적_회로\) "wikilink"))                                                                 |
| AMD                                                                        |                                                         |                                                                                                                                  |
| [GCN 5th](https://ko.wikipedia.org/wiki/그래픽스_코어_넥스트 "wikilink")            | 2017년 08월                                               | Vega 10                                                                                                                          |
| [GCN 4th](https://ko.wikipedia.org/wiki/그래픽스_코어_넥스트 "wikilink")            | 2016년 06월                                               | Polaris 10, Polaris 11, Polaris 12                                                                                               |
| [GCN 3rd](https://ko.wikipedia.org/wiki/그래픽스_코어_넥스트 "wikilink")            | 2014년 08월                                               | Tonga, Fiji, [Carrizo](https://ko.wikipedia.org/wiki/엑스카베이터_\(마이크로아키텍처\) "wikilink")                                             |
| [GCN 2nd](https://ko.wikipedia.org/wiki/그래픽스_코어_넥스트 "wikilink")            | 2013년 03월                                               | Bonaire, Hawaii, [Kaveri](https://ko.wikipedia.org/wiki/스팀롤러_\(마이크로아키텍처\) "wikilink"), Kabini, Temash, Mullins, Beema, Carrizo-L |
| [GCN 1st](https://ko.wikipedia.org/wiki/그래픽스_코어_넥스트 "wikilink")            | 2012년 01월                                               | Oland, Cape Verde, Pitcairn, Tahiti                                                                                              |
| [TeraScale 3](https://ko.wikipedia.org/wiki/테라스케일_\(마이크로아키텍처\) "wikilink") | 2010년 12월                                               | Cayman, Trinity/Richland                                                                                                         |
| [TeraScale 2](https://ko.wikipedia.org/wiki/테라스케일_\(마이크로아키텍처\) "wikilink") | 2009년 09월                                               | Cedar, Cypress, Juniper, Redwood, Palm, Sumo                                                                                     |
| [TeraScale 1](https://ko.wikipedia.org/wiki/테라스케일_\(마이크로아키텍처\) "wikilink") | 2007년 05월                                               | R600, RV630, RV610, RV790, RV770, …                                                                                              |
| Nvidia                                                                     |                                                         |                                                                                                                                  |
| [볼타](https://ko.wikipedia.org/wiki/볼타_\(마이크로아키텍처\) "wikilink")             | December 2017                                           | GV10x                                                                                                                            |
| [파스칼](https://ko.wikipedia.org/wiki/파스칼_\(마이크로아키텍처\) "wikilink")           | 2016년 05월                                               | GP10x                                                                                                                            |
| [맥스웰](https://ko.wikipedia.org/wiki/맥스웰_\(마이크로아키텍처\) "wikilink")           | 2014년 02월                                               | GM10x, GM20x                                                                                                                     |
| [케플러](https://ko.wikipedia.org/wiki/케플러_\(마이크로아키텍처\) "wikilink")           | 2012년 03월                                               | GK10x, GK110, GK208                                                                                                              |
| [페르미](https://ko.wikipedia.org/wiki/페르미_\(마이크로아키텍처\) "wikilink")           | 2010년 03월                                               | GF10x, GF11x                                                                                                                     |
| [테슬라](https://ko.wikipedia.org/wiki/테슬라_\(마이크로아키텍처\) "wikilink")           | 2006년 11월                                               | G8x, G9x, GT20x, GT21x                                                                                                           |
| Intel                                                                      | [커피레이크](https://ko.wikipedia.org/wiki/커피레이크 "wikilink") | 2017년 10월                                                                                                                        |
| [Kaby Lake](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")                       | 2016년 09월                                               |                                                                                                                                  |
| [Skylake](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")                         | 2015년 08월                                               |                                                                                                                                  |
| [Broadwell](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")                       | 2014년 09월                                               |                                                                                                                                  |
| [Haswell](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")                         | 2013년 06월                                               |                                                                                                                                  |
| [Ivy Bridge](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")                      | 2012년 04월                                               |                                                                                                                                  |
| [Sandy Bridge](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")                    | 2011년 01월                                               |                                                                                                                                  |
| [Westmere](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")                        | 2010년 01월                                               |                                                                                                                                  |
| Imagination Technologies                                                   |                                                         |                                                                                                                                  |
| [파워VR](https://ko.wikipedia.org/wiki/파워VR "wikilink") Series 8             | 2016년 02월                                               | GE8200, GE8300                                                                                                                   |
| PowerVR Series 7                                                           | 2014년 11월                                               | GE7400, GE7800, GT7200, GT7400, GT7600, GT7800, GT7900                                                                           |
| PowerVR Series 6                                                           | 2012년 01월                                               | G6100, G6200, G6230, G6400, G6430, G6630, RK3368, G6050, G6060, G6100 (XE), G6110, GX6240, GX6250, GX6450, GX6650                |
| PowerVR Series 5                                                           | 2009년 01월                                               | SGX543, SGX544, SGX554                                                                                                           |
| Qualcomm                                                                   |                                                         |                                                                                                                                  |
| [아드레노](https://ko.wikipedia.org/wiki/아드레노 "wikilink") 500 series           |                                                         | Adreno 510, Adreno 530, Adreno 540                                                                                               |
| Adreno 400 series                                                          |                                                         | Adreno 418,Adreno 420,Adreno 430                                                                                                 |
| Adreno 300 series                                                          |                                                         |                                                                                                                                  |
| ARM                                                                        |                                                         |                                                                                                                                  |
| [Bifrost](https://ko.wikipedia.org/wiki/말리_\(GPU\) "wikilink")\[33\]       | 2016년 06월                                               | Mali-G71, …                                                                                                                      |
| [Midgard](https://ko.wikipedia.org/wiki/말리_\(GPU\) "wikilink") 4th         | Q4 2015                                                 | Mali-T860, Mali-T830, Mali-T880                                                                                                  |
| Midgard 3rd                                                                | 2013년 10월                                               | Mali-T760, …                                                                                                                     |
| Midgard 2nd                                                                | 2012년 08월                                               | Mali-T600 series, T720                                                                                                           |

## 같이 보기

  - [Direct3D](https://ko.wikipedia.org/wiki/Direct3D "wikilink") - 벌컨의 주 경쟁 API
  - [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink") - 크로노스 그룹의 다른 그래픽스 API
  - [OpenCL](https://ko.wikipedia.org/wiki/OpenCL "wikilink") - 크로노스 그룹의 [이기종 컴퓨팅](https://ko.wikipedia.org/wiki/이기종_컴퓨팅 "wikilink") 프레임워크
  - [맨틀](https://ko.wikipedia.org/wiki/맨틀_\(API\) "wikilink") - 벌컨의 재단 AMD의 낮은 수준의 그래픽스 및 연산 API
  - [메탈](../Page/메탈_\(API\).md "wikilink") - iOS와 macOS용의 낮은 수준의 그래픽스 및 연산 API
  - [AMDGPU](https://ko.wikipedia.org/wiki/AMDGPU "wikilink") - AMD의 리눅스용의 완전한 오픈 소스 통합 그래픽스 드라이버

## 각주

  - 내용주

## 외부 링크

  - [Vulkan 1.0 specification](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html)

[분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:그래픽 표준](https://ko.wikipedia.org/wiki/분류:그래픽_표준 "wikilink") [분류:비디오 게임 개발](https://ko.wikipedia.org/wiki/분류:비디오_게임_개발 "wikilink") [분류:가상 현실](https://ko.wikipedia.org/wiki/분류:가상_현실 "wikilink") [분류:2015년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2015년_소프트웨어 "wikilink")

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
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.