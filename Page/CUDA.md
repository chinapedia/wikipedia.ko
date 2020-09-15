> This article is converted from Wikipedia: [CUDA](https://ko.wikipedia.org/wiki/CUDA).


[섬네일](https://ko.wikipedia.org/wiki/파일:CUDA_processing_flow_\(En\).PNG "wikilink") **CUDA** ("Compute Unified Device Architecture", 쿠다)는 [그래픽 처리 장치](../Page/그래픽_처리_장치.md "wikilink")(GPU)에서 수행하는 (병렬 처리) 알고리즘을 C 프로그래밍 언어를 비롯한 산업 표준 언어를 사용하여 작성할 수 있도록 하는 [GPGPU](https://ko.wikipedia.org/wiki/GPGPU "wikilink") 기술이다. CUDA는 [엔비디아](../Page/엔비디아.md "wikilink")가 개발해오고 있으며 이 아키텍처를 사용하려면 엔비디아 GPU와 특별한 스트림 처리 드라이버가 필요하다. CUDA는 G8X GPU로 구성된 지포스 8 시리즈급 이상에서 동작한다. CUDA 플랫폼은 [컴퓨터 커널의](https://ko.wikipedia.org/wiki/컴퓨터_커널 "wikilink") 실행을 위해 GPU의 가상 [명령 집합과](https://ko.wikipedia.org/wiki/명령_집합 "wikilink") 병렬 연산 요소들을 직접 접근할 수 있는 소프트웨어 계층이다.\[1\]

개발자는 패스스케일 오픈64 C 컴파일러로 컴파일 된 '쿠다를 위한 C' (C언어를 엔비디아가 확장한 것) 를 사용하여 GPU 상에서 실행시킬 알고리듬을 작성할 수 있다. 쿠다 구조는 일련의 계산 인터페이스를 지원하며 이에는 [OpenCL](../Page/OpenCL.md "wikilink"), DirectX Compute가 포함된다. C 언어가 아닌 다른 프로그래밍언어에서의 개발을 위한 래퍼(Wrapper)도 있는데, 현재 [파이썬](../Page/파이썬.md "wikilink"), [펄](../Page/펄.md "wikilink"), [포트란](../Page/포트란.md "wikilink"), [자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") [매트랩](https://ko.wikipedia.org/wiki/매트랩 "wikilink") 등을 위한 것들이 있다. 이러한 접근성은 병렬 프로그래밍 전문가들이 GPU 리소스를 쉽게 이용할 수 있게 해주며, 이는 그래픽스 프로그래밍의 고급 기술을 요구하였던 [Direct3D](../Page/Direct3D.md "wikilink")와 [OpenGL](../Page/OpenGL.md "wikilink")과 같은 이전 API 솔루션들과 대비된다. 또, CUDA는 [OpenACC](https://ko.wikipedia.org/wiki/OpenACC "wikilink")와 [OpenCL](../Page/OpenCL.md "wikilink")과 같은 프로그래밍 프레임워크를 지원한다.\[2\]

최신 드라이버는 모두 필요한 쿠다 콤포넌트를 담고 있다. 쿠다는 모든 엔비디아 GPU (G8X 시리즈 이후) 를 지원하며 이 대상에는 [지포스](../Page/지포스.md "wikilink"), [쿼드로](../Page/엔비디아_쿼드로.md "wikilink"), [테슬라](https://ko.wikipedia.org/wiki/테슬라 "wikilink") 제품군이 포함된다. 엔비디아는 지포스 8 시리즈를 위해 개발된 프로그램들이 수정 없이 모든 미래의 엔비디아 비디오 카드에서 실행될 것이라고 선언하였다.

쿠다를 통해 개발자들은 쿠다 GPU 안 병렬 계산 요소 고유의 명령어 집합과 메모리에 접근할 수 있다. 쿠다를 사용하여 최신 엔비디아 GPU를 효과적으로 개방적으로 사용할 수 있다. 그러나 CPU와는 달리 GPU는 병렬 다수 코어 구조를 가지고 있고, 각 코어는 수천 스레드를 동시에 실행시킬 수 있다. 응용 프로그램이 수행하는 작업(계산)이 이러한 병렬처리연산에 적합할 경우, GPU를 이용함으로써 커다란 성능 향상을 기대할 수 있다.

컴퓨터 게임 업계에서는 그래픽 랜더링에 덧붙여, 그래픽 카드의 게임 물리 계산 (파편, 연기, 불, 유체 등 물리 효과)에 사용되며, 예로는 [피직스](https://ko.wikipedia.org/wiki/피직스 "wikilink")와 [불렛](https://ko.wikipedia.org/wiki/불렛 "wikilink")이 있다. 쿠다는 그래픽이 아닌 응용 프로그램, 즉, 계산 생물학, 암호학, 그리고 다른 분야에서 10배 또는 그 이상의 속도 혜택을 가져왔다. 이 한 예는 [BOINC](../Page/BOINC.md "wikilink") 분산 계산 클라이언트이다.

쿠다는 저수준 API와 고수준 API 모두를 제공한다. 최초의 CUDA SDK는 2007년 2월 15일에 공개되었으며 [마이크로소프트 윈도와](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [리눅스](../Page/리눅스.md "wikilink")를 지원했다. [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") 지원은 2.0 버전에 추가되었다.

## 이점

쿠다가 그래픽 API를 사용하는 전통적인 범용 GPU에 비해 가지는 몇가지 장점은 다음과 같다.

  - 흩뿌린 읽기 - 코드가 메모리의 임의 위치에서 데이터를 읽을 수 있다.
  - [공유 메모리](../Page/공유_메모리.md "wikilink") - 쿠다는 고속 공유 메모리 지역 (16 또는 48KB 크기) 을 드러내어 스레드 간에 나눌 수 있게 해 준다. 이는 사용자 관리 캐시로 사용될 수 있는데, 텍스처 룩업을 이용하는 경우 보다 더 빠른 대역폭이 가능해진다.
  - 디바이스 상의 읽기, 쓰기가 호스트보다 더 빠르다.
  - 정수와 비트 단위 연산을 충분히 지원한다. 정수 텍스처 룩업이 포함된다.

## 제한

  - 재귀호출, [함수 포인터가](../Page/함수_포인터.md "wikilink") 없는 C 언어의 하부 집합을 확장하여 사용한다. 그러나 한개의 처리 장치가 여러개의 쪼개진 메모리 공간에 대하여 작업하여야 하는 점이 다른 C 언어 실행 환경과 다른 점이다.
  - 텍스처 랜더링은 지원 되지 않는다.
  - 배정도에 관해서는 IEEE 754 표준과 다르지 않다. 단정도에서는 [비정규 값과](../Page/비정규_값.md "wikilink") 신호 NaN이 지원되지 않고, IEEE [반올림](../Page/반올림.md "wikilink") 모드 가운데서는 두가지만 지원하며, 이도 명령어에 따라서 지원되는 것으로 제어 단어(Control word)에서 지원 되는 것은 아니다.(이것이 제한점인지는 논란의 대상이 될 수 있다) 그리고 나눗셈과 제곱근의 정밀도가 단정도에 비해 조금 낮다.
  - CPU와 GPU 사이의 버스 대역폭과 시간 지연에서 병목이 발생할 수 있다.
  - 스레드가 최소한 32개씩 모여서 실행되어야 최선의 성능 향상을 얻을 수 있으며, 스레드 수의 합이 수천개가 되어야 한다. 프로그램 코드에서의 분기는, 각각의 32 스레드가 같은 실행 경로를 따른다면, 성능에 큰 지장을 주지 않는다. [SIMD](../Page/SIMD.md "wikilink") 실행 모델은 어떠한 내재적으로 분기하는 임무에게는 심각한 제한이 된다. (예를 들어, 광선 추적 가속 자료 구조)
  - 쿠다 기반 GPU는 엔비디아에서만 나온다.

## 지원 GPU

CUDA 수준의 지원 GPU 및 카드이다. [엔비디아 웹사이트](http://developer.nvidia.com/cuda-gpus)도 참고할 것:

<table>
<thead>
<tr class="header">
<th><p>연산<br />
능력<br />
(버전)</p></th>
<th><p><a href="../Page/마이크로아키텍처.md" title="wikilink">마이크로-<br />
아키텍처</a></p></th>
<th><p>GPU</p></th>
<th><p>지포스</p></th>
<th><p>쿼드로</p></th>
<th><p>테슬라</p></th>
<th><p>기타</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/테슬라_(마이크로아키텍처)" title="wikilink">테슬라</a></p></td>
<td><p>G80</p></td>
<td><p>지포스 8800 울트라, 지포스 8800 GTX, 지포스 8800 GTS(G80)</p></td>
<td><p>쿼드로 FX 5600, 쿼드로 FX 4600, 쿼드로 Plex 2100 S4</p></td>
<td><p>테슬라 C870, 테슬라 D870, 테슬라 S870</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.1</p></td>
<td><p>G92, G94, G96, G98, G84, G86</p></td>
<td><p>지포스 GTS 250, 지포스 9800 GX2, 지포스 9800 GTX, 지포스 9800 GT, 지포스 8800 GTS(G92), 지포스 8800 GT, 지포스 9600 GT, 지포스 9500 GT, 지포스 9400 GT, 지포스 8600 GTS, 지포스 8600 GT, 지포스 8500 GT, 지포스 G110M, 지포스 9300M GS, 지포스 9200M GS, 지포스 9100M G, 지포스 8400M GT, 지포스 G105M</p></td>
<td><p>쿼드로 FX 4700 X2, 쿼드로 FX 3700, 쿼드로 FX 1800, 쿼드로 FX 1700, 쿼드로 FX 580, 쿼드로 FX 570, 쿼드로 FX 470, 쿼드로 FX 380, 쿼드로 FX 370, 쿼드로 FX 370 Low Profile, 쿼드로 NVS 450, 쿼드로 NVS 420, 쿼드로 NVS 290, 쿼드로 NVS 295, 쿼드로 Plex 2100 D4, 쿼드로 FX 3800M, 쿼드로 FX 3700M, 쿼드로 FX 3600M, 쿼드로 FX 2800M, 쿼드로 FX 2700M, 쿼드로 FX 1700M, 쿼드로 FX 1600M, 쿼드로 FX 770M, 쿼드로 FX 570M, 쿼드로 FX 370M, 쿼드로 FX 360M, 쿼드로 NVS 320M, 쿼드로 NVS 160M, 쿼드로 NVS 150M, 쿼드로 NVS 140M, 쿼드로 NVS 135M, 쿼드로 NVS 130M, 쿼드로 NVS 450, 쿼드로 NVS 420, 쿼드로 NVS 295</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.2</p></td>
<td><p>GT218, GT216, GT215</p></td>
<td><p>지포스 GT 340*, 지포스 GT 330*, 지포스 GT 320*, 지포스 315*, 지포스 310*, 지포스 GT 240, 지포스 GT 220, 지포스 210, 지포스 GTS 360M, 지포스 GTS 350M, 지포스 GT 335M, 지포스 GT 330M, 지포스 GT 325M, 지포스 GT 240M, 지포스 G210M, 지포스 310M, 지포스 305M</p></td>
<td><p>쿼드로 FX 380 Low Profile, 엔비디아 NVS 300, 쿼드로 FX 1800M, 쿼드로 FX 880M, 쿼드로 FX 380M, 엔비디아 NVS 300, NVS 5100M, NVS 3100M, NVS 2100M, ION</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.3</p></td>
<td><p>GT200, GT200b</p></td>
<td><p>지포스 GTX 295, GTX 285, GTX 280, 지포스 GTX 275, 지포스 GTX 260</p></td>
<td><p>쿼드로 FX 5800, 쿼드로 FX 4800, 쿼드로 FX 4800 for Mac, 쿼드로 FX 3800, 쿼드로 CX, 쿼드로 Plex 2200 D2</p></td>
<td><p>테슬라 C1060, 테슬라 S1070, 테슬라 M1060</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2.0</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페르미_(마이크로아키텍처)" title="wikilink">페르미</a></p></td>
<td><p>GF100, GF110</p></td>
<td><p>지포스 GTX 590, 지포스 GTX 580, 지포스 GTX 570, 지포스 GTX 480, 지포스 GTX 470, 지포스 GTX 465, 지포스 GTX 480M</p></td>
<td><p>쿼드로 6000, 쿼드로 5000, 쿼드로 4000, 쿼드로 4000 for Mac, 쿼드로 Plex 7000, 쿼드로 5010M, 쿼드로 5000M</p></td>
<td><p>테슬라 C2075, 테슬라 C2050/C2070, 테슬라 M2050/M2070/M2075/M2090</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2.1</p></td>
<td><p>GF104, GF106 GF108, GF114, GF116, GF117, GF119</p></td>
<td><p>지포스 GTX 560 Ti, 지포스 GTX 550 Ti, 지포스 GTX 460, 지포스 GTS 450, 지포스 GTS 450*, 지포스 GT 640 (GDDR3), 지포스 GT 630, 지포스 GT 620, 지포스 GT 610, 지포스 GT 520, 지포스 GT 440, 지포스 GT 440*, 지포스 GT 430, 지포스 GT 430*, 지포스 GT 420*, 지포스 GTX 675M, 지포스 GTX 670M, 지포스 GT 635M, 지포스 GT 630M, 지포스 GT 625M, 지포스 GT 720M, 지포스 GT 620M, 지포스 710M, 지포스 610M, 지포스 820M, 지포스 GTX 580M, 지포스 GTX 570M, 지포스 GTX 560M, 지포스 GT 555M, 지포스 GT 550M, 지포스 GT 540M, 지포스 GT 525M, 지포스 GT 520MX, 지포스 GT 520M, 지포스 GTX 485M, 지포스 GTX 470M, 지포스 GTX 460M, 지포스 GT 445M, 지포스 GT 435M, 지포스 GT 420M, 지포스 GT 415M, 지포스 710M, 지포스 410M</p></td>
<td><p>쿼드로 2000, 쿼드로 2000D, 쿼드로 600, 쿼드로 410, 쿼드로 4000M, 쿼드로 3000M, 쿼드로 2000M, 쿼드로 1000M, NVS 5400M, NVS 5200M, NVS 4200M, 엔비디아 NVS 315, 엔비디아 NVS 310</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/케플러_(마이크로아키텍처)" title="wikilink">케플러</a></p></td>
<td><p>GK104, GK106, GK107</p></td>
<td><p>지포스 GTX 770, 지포스 GTX 760, 지포스 GT 740, 지포스 GTX 690, 지포스 GTX 680, 지포스 GTX 670, 지포스 GTX 660 Ti, 지포스 GTX 660, 지포스 GTX 650 Ti BOOST, 지포스 GTX 650 Ti, 지포스 GTX 650, 지포스 GTX 880M, 지포스 GTX 780M, 지포스 GTX 770M, 지포스 GTX 765M, 지포스 GTX 760M, 지포스 GTX 680MX, 지포스 GTX 680M, 지포스 GTX 675MX, 지포스 GTX 670MX, 지포스 GTX 660M, 지포스 GT 750M, 지포스 GT 650M, 지포스 GT 745M, 지포스 GT 645M, 지포스 GT 740M, 지포스 GT 730M, 지포스 GT 640M, 지포스 GT 640M LE, 지포스 GT 735M, 지포스 GT 730M</p></td>
<td><p>쿼드로 K5000, 쿼드로 K4200, 쿼드로 K4000, 쿼드로 K2000, 쿼드로 K2000D, 쿼드로 K600, 쿼드로 K420, 쿼드로 K500M, 쿼드로 K510M, 쿼드로 K610M, 쿼드로 K1000M, 쿼드로 K2000M, 쿼드로 K1100M, 쿼드로 K2100M, 쿼드로 K3000M, 쿼드로 K3100M, 쿼드로 K4000M, 쿼드로 K5000M, 쿼드로 K4100M, 쿼드로 K5100M, 엔비디아 NVS 510</p></td>
<td><p>테슬라 K10, GRID K340, GRID K520</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.2</p></td>
<td><p>GK20A</p></td>
<td></td>
<td></td>
<td></td>
<td><p>Tegra K1, Jetson TK1</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.5</p></td>
<td><p>GK110, GK208</p></td>
<td><p>지포스 GTX 타이탄 Z, 지포스 GTX 타이탄 Black, 지포스 GTX 타이탄, 지포스 GTX 780 Ti, 지포스 GTX 780, 지포스 GT 640 (GDDR5), 지포스 GT 630 v2, 지포스 GT 730, 지포스 GT 720, 지포스 GT 710,지포스 GT 740M (64비트, DDR3)</p></td>
<td><p>쿼드로 K6000, 쿼드로 K5200</p></td>
<td><p>테슬라 K40, 테슬라 K20x, 테슬라 K20</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.7</p></td>
<td><p>GK210</p></td>
<td></td>
<td></td>
<td><p>테슬라 K80</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/맥스웰_(마이크로아키텍처)" title="wikilink">맥스웰</a></p></td>
<td><p>GM107, GM108</p></td>
<td><p>지포스 GTX 750 Ti, 지포스 GTX 750, 지포스 GTX 960M, 지포스 GTX 950M, 지포스 940M, 지포스 930M, 지포스 GTX 860M, 지포스 GTX 850M, 지포스 845M, 지포스 840M, 지포스 830M</p></td>
<td><p>쿼드로 K2200, 쿼드로 K1200, 쿼드로 K620, 쿼드로 M2000M, 쿼드로 M1000M, 쿼드로 M600M, 쿼드로 K620M, 엔비디아 NVS 810</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.2</p></td>
<td><p>GM200, GM204, GM206</p></td>
<td><p>지포스 GTX 타이탄 X, 지포스 GTX 980 Ti, 지포스 GTX 980, 지포스 GTX 970, 지포스 GTX 960, 지포스 GTX 950, 지포스 GTX 750 SE, 지포스 GTX 980M, 지포스 GTX 970M, 지포스 GTX 965M</p></td>
<td><p>쿼드로 M6000 24GB, 쿼드로 M6000, 쿼드로 M5000, 쿼드로 M4000, 쿼드로 M2000, 쿼드로 M5500, 쿼드로 M5000M, 쿼드로 M4000M, 쿼드로 M3000M</p></td>
<td><p>테슬라 M4, 테슬라 M40, 테슬라 M6, 테슬라 M60</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.3</p></td>
<td><p>GM20B</p></td>
<td></td>
<td></td>
<td></td>
<td><p>Tegra X1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.0</p></td>
<td><p><a href="../Page/파스칼_(마이크로아키텍처).md" title="wikilink">파스칼</a></p></td>
<td><p>GP100</p></td>
<td></td>
<td><p>쿼드로 GP100</p></td>
<td><p>테슬라 P100</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.1</p></td>
<td><p>GP102, GP104, GP106, GP107,</p>
<p>GP108</p></td>
<td><p>엔비디아 타이탄 X, 지포스 GTX 1080, GTX 1070, GTX 1070 Ti, GTX 1060, GTX 1050 Ti, GTX 1050</p></td>
<td><p>쿼드로 P6000, 쿼드로 P5000, 쿼드로 P4000, 쿼드로 P2200, 쿼드로 P2000, 쿼드로 1000, 쿼드로 P620, 쿼드로 P600, 쿼드로 P400</p></td>
<td><p>테슬라 P40, 테슬라 P4</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.0</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/볼타_(마이크로아키텍처)" title="wikilink">볼타</a></p></td>
<td><p>GV100</p></td>
<td><p>엔비디아 타이탄 V</p></td>
<td><p>쿼드로 GV100</p></td>
<td><p>테슬라 V100</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>Jetson AGX Xavier</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.5</p></td>
<td><p>튜링</p></td>
<td><p>TU102, TU104, TU106, TU116, TU117</p></td>
<td><p>엔베디아 타이탄 RTX, 지포스 RTX 2080Ti, RTX 2080, RTX 2070, RTX 2060, 지포스 GTX 1660 Ti, GTX 1660, GTX 1650</p></td>
<td><p>쿼드로 RTX 8000, 쿼드로 RTX 6000, 쿼드로 RTX 5000, 쿼드로 RTX 4000</p></td>
<td><p>테슬라 T4</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>9.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>9.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>9.2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>10.1</p></td>
<td><p>튜링</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>10.0</p></td>
<td><p>튜링</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

'\*' - [OEM](../Page/OEM.md "wikilink") 전용 제품

## 언어 결합

  - [커먼 리스프](../Page/커먼_리스프.md "wikilink") - [cl-cuda](https://github.com/takagi/cl-cuda)
  - [포트란](../Page/포트란.md "wikilink") - [FORTRAN CUDA](http://www.hoopoe-cloud.com/Solutions/Fortran/Default.aspx), [PGI CUDA Fortran Compiler](http://www.pgroup.com/resources/cudafortran.htm)
  - F\# - [Alea.CUDA](https://web.archive.org/web/20141010163529/https://www.quantalea.net/products/introduction/)
  - [하스켈](../Page/하스켈.md "wikilink") - [Data.Array.Accelerate](http://hackage.haskell.org/package/accelerate)
  - [IDL](https://ko.wikipedia.org/wiki/대화형_데이터_언어 "wikilink") - [GPULib](http://www.txcorp.com/products/GPULib/)
  - [Java](../Page/자바_\(프로그래밍_언어\).md "wikilink") - [jCUDA](http://www.cass-hpc.com/solutions/legacy/jcuda), [JCuda](http://www.jcuda.org/jcuda/JCuda.html), [JCublas](http://www.jcuda.org/jcuda/jcublas/JCublas.html), [JCufft](http://www.jcuda.org/jcuda/jcufft/JCufft.html), [CUDA4J](http://www.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.71.doc/user/gpu_developing_cuda4j.html)
  - [루아](../Page/루아_\(프로그래밍_언어\).md "wikilink") - [KappaCUDA](https://web.archive.org/web/20160815110157/https://psilambda.com/download/kappa-extras/)
  - [매스매티카](../Page/매스매티카.md "wikilink") - [CUDALink](http://reference.wolfram.com/mathematica/CUDALink/tutorial/Overview.html)
  - [MATLAB](../Page/MATLAB.md "wikilink") - 병렬 컴퓨팅 툴박스, MATLAB 분산 컴퓨팅 서버,\[3\] [재킷과](https://ko.wikipedia.org/wiki/재킷_\(소프트웨어\) "wikilink") 같은 타사 패키지.
  - [.NET](../Page/닷넷_프레임워크.md "wikilink") - [CUDA.NET](http://www.cass-hpc.com/solutions/libraries/cuda-net), [Managed CUDA](https://kunzmi.github.io/managedCuda/), [CUDAfy.NET](http://www.hybriddsp.com) .NET 커널 및 호스트 코드, CURAND, CUBLAS, CUFFT
  - [펄](../Page/펄.md "wikilink") - [KappaCUDA](https://web.archive.org/web/20100825231711/http://psilambda.com/download/kappa-for-perl/), [CUDA::Minimal](https://github.com/run4flat/perl-CUDA-Minimal)
  - [파이썬](../Page/파이썬.md "wikilink") - [Numba](http://numba.pydata.org/), NumbaPro, [PyCUDA](http://mathema.tician.de/software/pycuda), [KappaCUDA](https://web.archive.org/web/20160815113344/https://psilambda.com/download/kappa-for-python/), [Theano](http://deeplearning.net/software/theano/)
  - [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink") - [KappaCUDA](https://web.archive.org/web/20160815110157/https://psilambda.com/download/kappa-extras/)
  - [R](../Page/R_\(프로그래밍_언어\).md "wikilink") - [gputools](https://web.archive.org/web/20140210082556/http://brainarray.mbni.med.umich.edu/brainarray/rgpgpu/)

## 예제

### C++

이 예제는 텍스처 하나를 어떤 이미지로부터 GPU상의 행렬로 읽어들인다.

``` c
cudaArray* cu_array;
texture<float, 2> tex;

// 행렬 할당
cudaMallocArray(&cu_array, cudaCreateChannelDesc<float>(), width, height);

// 이미지 데이터를 행렬로 복사
cudaMemcpy(cu_array, image, width*height, cudaMemcpyHostToDevice);

// 행렬을 텍스처에 연결한다.
cudaBindTexture(tex, cu_array);

// 커널을 실행한다
dim3 blockDim(16, 16, 1);
dim3 gridDim(width / blockDim.x, height / blockDim.y, 1);
kernel<<< gridDim, blockDim, 0 >>>(d_odata, width, height);
cudaUnbindTexture(tex);

__global__ void kernel(float* odata, int height, int width)
{
   unsigned int x = blockIdx.x*blockDim.x + threadIdx.x;
   unsigned int y = blockIdx.y*blockDim.y + threadIdx.y;
   float c = texfetch(tex, x, y);
   odata[y*width+x] = c;
}
```

### 파이썬

파이선 언어의 바인딩은 [PyCUDA](http://mathema.tician.de/software/pycuda)에서 구할 수 있다.

아래 예제는 두 배열의 곱을 GPU 상에서 계산한다.

``` numpy
import pycuda.driver as drv
import numpy
import pycuda.autoinit

mod = drv.SourceModule("""
__global__ void multiply_them(float *dest, float *a, float *b)
{
  const int i = threadIdx.x;
  dest[i] = a[i] * b[i];
}
""")

multiply_them = mod.get_function("multiply_them")

a = numpy.random.randn(400).astype(numpy.float32)
b = numpy.random.randn(400).astype(numpy.float32)

dest = numpy.zeros_like(a)
multiply_them(
        drv.Out(dest), drv.In(a), drv.In(b),
        block=(400,1,1))

print dest-a*b
```

[행렬 곱셈을 단순화하는 추가 파이선 바인딩](https://web.archive.org/web/20090420124748/http://kered.org/blog/2009-04-13/easy-python-numpy-cuda-cublas/)을 사용한 예제이다.

``` numpy
import numpy
from pycublas import CUBLASMatrix
A = CUBLASMatrix( numpy.mat([[1,2,3],[4,5,6|1,2,3],[4,5,6]],numpy.float32) )
B = CUBLASMatrix( numpy.mat([[2,3],[4,5],[6,7|2,3],[4,5],[6,7]],numpy.float32) )
C = A*B
print C.np_mat()
```

## 같이 보기

  - [OpenCL](../Page/OpenCL.md "wikilink")
  - [범용 GPU](https://ko.wikipedia.org/wiki/GPGPU "wikilink")
  - [병렬 컴퓨팅](../Page/병렬_컴퓨팅.md "wikilink")
  - [스트림 프로세싱](https://ko.wikipedia.org/wiki/스트림_프로세싱 "wikilink")
  - [벌컨](../Page/벌컨_\(API\).md "wikilink")
  - [rCUDA](https://ko.wikipedia.org/wiki/rCUDA "wikilink")

## 각주 및 참고 문헌

1.  제이슨 샌더스, 에드워드 캔드롯 저, [박춘언](https://hermet.pe.kr/notice/29) 역, *예제로 배우는 CUDA 프로그래밍(입문자를 위한 GPGPU 프로그래밍의 기초)*, .
2.  Farber, Rob 저, *CUDA Application Design and Development*, .
3.  Hwu, Wen-Mei 저, *GPU Computing GEMs - Jade Edition*, .

## 외부 링크

  -

  - [CUDA 커뮤니티](https://plus.google.com/communities/114632076318201174454) - [구글+](../Page/구글+.md "wikilink")

  - [VRAM 크기 조절 도구](https://devtalk.nvidia.com/default/topic/726765/need-a-little-tool-to-adjust-the-vram-size/)

  - [CUDA GPUs](http://www.nvidia.com/object/cuda_learn_products.html) - 공식적으로 CUDA를 지원하는 장치 목록

[분류:컴퓨터 물리 엔진](https://ko.wikipedia.org/wiki/분류:컴퓨터_물리_엔진 "wikilink") [분류:GPGPU](https://ko.wikipedia.org/wiki/분류:GPGPU "wikilink") [분류:엔비디아 소프트웨어](https://ko.wikipedia.org/wiki/분류:엔비디아_소프트웨어 "wikilink") [분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink")

1.
2.
3.