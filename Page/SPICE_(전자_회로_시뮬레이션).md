> This article is converted from Wikipedia: [SPICE \(  \)](https://ko.wikipedia.org/wiki/SPICE_\(__\)).


**SPICE** (*Simulation Program with Integrated Circuit Emphasis*)\[1\]\[2\] 는 공용 [오픈소스](https://ko.wikipedia.org/wiki/오픈소스 "wikilink") [아날로그 회로](../Page/아날로그_회로.md "wikilink") [시뮬레이터이다](https://ko.wikipedia.org/wiki/전자_회로_시뮬레이션 "wikilink"). 이것은 [집적 회로와](https://ko.wikipedia.org/wiki/집적_회로 "wikilink") 보드 레벨 설계에 사용되며, 회로 설계의 무결성을 확인하고 그 [회로](https://ko.wikipedia.org/wiki/회로 "wikilink")의 동작을 예측한다.

## 소개

개별 부품으로 이루어진 보드 레벨 설계와는 달리, 집적 회로를 제조하기 전에 [브레드보드](../Page/브레드보드.md "wikilink")로 실험하는 것은 굉장히 어렵다. 또한, [포토마스크](https://ko.wikipedia.org/wiki/포토마스크 "wikilink")등의 제조를 위한 전제조건들은 설계단계에서의 완벽함을 필요로 하게 되었다. 이러한 배경으로 인해 SPICE를 사용하여 시뮬레이션하는 방법은 집적 회로를 제조하기 전에 미리 트랜지스터 레벨에서 회로작동을 시험하기 위해 업계표준으로 자리잡게 되었다.

보드 레벨 설계는 종종 브레드보드를 통해 테스트된다. 하지만 브레드보드를 활용해도 [기생 소자와](https://ko.wikipedia.org/wiki/기생_소자 "wikilink") 같은 몇몇 회로의 특성은 실제 제조후와 비교했을 때 정확하지 않을 수 있다. 이러한 기생소자들은 SPICE를 통해 더 정확하게 측정이 가능하다. 또한, 설계자들은 제조시의 오차 발생을 대비해 모형보다 더 정확한 정보를 갖기 원한다. 그러한 이유로 [몬테 카를로의](https://ko.wikipedia.org/wiki/몬테_카를로_방법 "wikilink") 시뮬레이션을 수행하는데에 SPICE를 사용하는 것은 흔한 일이다.

회로 시뮬레이션 프로그렘은 [트랜지스터](https://ko.wikipedia.org/wiki/트랜지스터 "wikilink"), [저항](https://ko.wikipedia.org/wiki/저항 "wikilink"), [축전기](../Page/축전기.md "wikilink") 등으로 이루어진 회로요소, 그리고 그들의 연결들을 모두 기록한 넷리스트를 받아서 그것을 풀기위한 방정식들로 변환\[3\]한다. 그 후, 이러한 [비선형](../Page/비선형.md "wikilink") [미분](https://ko.wikipedia.org/wiki/미분 "wikilink") [대수](https://ko.wikipedia.org/wiki/대수학 "wikilink")[방정식](https://ko.wikipedia.org/wiki/방정식 "wikilink")을 비선형 [적분](https://ko.wikipedia.org/wiki/적분 "wikilink") 방식, [뉴턴 방법](https://ko.wikipedia.org/wiki/뉴턴_방법 "wikilink"), [희소행렬](https://ko.wikipedia.org/wiki/희소행렬 "wikilink") 등의 방식으로 정리된 일반 방정식이 사용자에게 주어지게 된다.

## 기원

SPICE는 [캘리포니아 대학교 버클리의](https://ko.wikipedia.org/wiki/캘리포니아_대학교_버클리 "wikilink") 전자공학 연구실에서 도널드 페더슨 교수(Donald Pederson) 의 지도를 받는 로렌스 네이글(Laurence Nagel) 에 의해 만들어졌다. SPICE1은 본래 네이글이 로널드 로러(Ronald Rohrer) 교수 밑에서 작업한 CANCER 프로그램\[4\]의 파생으로 제작되었다. CANCER는 "Computer Analysis of Nonlinear Circuits, Excluding Radiation"의 약자로\[5\], 이 시기에는 [미국 국방부에서](https://ko.wikipedia.org/wiki/미국_국방부 "wikilink") 회로가 방사능에 얼마나 잘 버티는지에 대해 측정하기 위한 시뮬레이터가 개발되고 있었다. 네이글의 지도교수였던 로러가 떠나고 새 지도교수, 페더슨은 특허를 이미 받은 CANCER의 사용제약을 없애고, [퍼블릭 도메인으로](https://ko.wikipedia.org/wiki/퍼블릭_도메인 "wikilink") 사용되기에 충분한 프로그램이라고 생각하였다.\[6\]

SPICE1는 1973년에 처음 소개되었다.\[7\] 그 당시에는 [포트란](https://ko.wikipedia.org/wiki/포트란 "wikilink")으로 짜여졌고, [노달 회로분석를](../Page/노달_회로분석.md "wikilink") 사용해 회로의 방정식을 구했다. 하지만, 노달 회로분석은 인덕터, 부동 전압원, 종속원들을 표현하는 데에는 어려움이 많았다. SPICE1은 또한 비교적 소수의 회로만 사용이 가능하였고, 과도신호에 대한 고정된 시간동안의 분석만 가능하였다. 1975년, 현재의 명성을 가지게 해 준 SPICE2\[8\]가 포트란으로 개발되었다. SPICE2는 더 많은 소자와 \[\[노달변형_회로분석|노달변형 회로분석을 통한 더 폭넓은 과도신호 분석을 가능하게 하였다. 그리고 동료 대학원생인 엘리스 코헨(Ellis Cohen)에 의해 포트란에 기초한 메모리 할당 시스템이 적용되었다. 1983년에 마지막으로 포트란으로 짜여진 SPICE가 업데이트 되었고, 토마스 쿼리스(Thomas Quarles)는 리차드 뉴턴(A. Richard Newton)의 지도를 받으며 1989년, C로 짜여진 SPICE3\[9\]를 개발하였다. SPICE3는 [X 윈도우 시스템의](https://ko.wikipedia.org/wiki/X_윈도우_시스템 "wikilink") 방식을 주가하고, 같은 문법을 사용하도록 만들어졌다.

[소스코드](https://ko.wikipedia.org/wiki/소스코드 "wikilink")가 공개된 초기 [퍼블릭 도메인 소프트웨어](https://ko.wikipedia.org/wiki/퍼블릭_도메인_소프트웨어 "wikilink") 프로그램으로서\[10\], SPICE는 널리 배급되고 사용되었다. SPICE의 대중성은 곧 "회로를 SPICE 하다" 라는 표현을 "회로를 시뮬레이션하다"와 동의어로 만드는데 충분했다.\[11\] 과거에는 [캘리포니아 대학교 버클리에서](https://ko.wikipedia.org/wiki/캘리포니아_대학교_버클리 "wikilink") 자기 테이프의 가격을 충당하기 위해서 약간의 비용을 받고 제공되었으며, 현재는 [BSD 허가서에](https://ko.wikipedia.org/wiki/BSD_허가서 "wikilink") 따라 자유롭게 사용이 가능하다.

## 과도신호 분석

과도신호 분석은 시간에 대해 종속적이기 때문에, 기존과는 다른 방식의 분석 알고리즘을 사용한다. 하지만, 과도신호 분석은 DC 동작점 분석을 선행하므로, 대부분의 DC분석 알고리즘은 과도신호분석에 사용된다.

### 과도신호 분석을 위한 초기조건

발진기 또는 피드백 회로같은 몇몇 회로들은 안정된 동작점을 가지고 있지 않는다. 이러한 회로들은 초기 조건을 확인하기 위해서 피드백 루프를 개방하거나, 처음부터 초기조건을 지정해주어야만 한다. DC 동작점 분석은 UIC 매개변수가 있을경우 무시된다. 만약 UIC가 .TRAN 선언에 포함되어있다면, 과도신호 분석은 .IC 선언으로 분석된 노드의 전압을 이용해 동작한다. .IC 선언에서 5V로 지정되었을 경우, 초기시간에서의 전압이 5V가 되는것이다.

과도신호 분석중에 DC 동작점을 추정한 값을 저장하기 위해 .OP 선언을 사용할수도 있다.

<code>

`   .TRAN 1ns 100ns UIC`
`   .OP 20ns`

</code>

.TRAN 선언의 UIC 매개변수로 인해 초기 동작점 분석은 무시된다. .OP선언은 과도신호 동작점을 t=20일 때의 값으로 계산하게 된다.

비록 과도신호 분석이 수렴된 DC분석을 제공하지만, 과도신호 분석 스스로는 부족한 경우가 많다. 과도신호 분석에서 "internal timestep too small" 오류가 발생할 경우가 있는데, 이것이 바로 저런 이유로 생기는 에러이다. 수렴 실패는 실제 DC 동작점 값이 초기조건과 크게 다를 경우 발생하는 문제이다.

## 적용

SPICE는 학계에서도, 산업적으로도, 영리 제품으로서도 많은 회로 시뮬레이션 프로그램의 토대로 우뚝섰다. 첫번째 SPICE의 영리버젼은 ISPICE인데, [National CSS에서](https://ko.wikipedia.org/wiki/National_CSS "wikilink") 시분할 서비스의 상호작용 버전으로 제작하였다.\[12\] 가장 유명한 상업 제품으로는 현재 [카덴스 디자인 시스템에서](https://ko.wikipedia.org/wiki/케이던스_디자인_시스템 "wikilink") 소유중인 [PSPICE](https://ko.wikipedia.org/wiki/Orcad "wikilink") 와 [시놉시스에서](https://ko.wikipedia.org/wiki/시놉시스_\(회사\) "wikilink") 소유중인 HSPICE가 있다. 학계 부문에서는 [조지아 테크에서](https://ko.wikipedia.org/wiki/조지아_테크 "wikilink") 제작한 XSPICE와 CODECS에서 시작되어 캘리포니아 대학교 버클리와 오레곤 주 대학교에서 만든 Cider가 있다.  집적회로 산업은 SPICE를 빠르게 받아들이고 있으며, 지금도 개발되고 있다.\[13\]

오늘날에는 몇몇, 특히 거대한 회사를 위시한 IC 제조업체들은 계속해서 SPICE를 토대로 한 회로 시뮬레이션 프로그램을 개발하기 위한 팀을 꾸리고 있고, 이 결과로 [Analog Devices에서](../Page/아날로그_디바이스.md "wikilink") 만든 ADICE, [Linear Technology에서](https://ko.wikipedia.org/wiki/Linear_Technology "wikilink") 만든 LTspice 등이 있다.

SPICE의 탄생은 2011년 [IEEE Milestone에서](https://ko.wikipedia.org/wiki/전기_전자_기술자_협회 "wikilink") 언급되었는데, 이때의 언급은 "범세계적 표준 집적회로 시뮬레이터" 이다.\[14\]

## 프로그램 특징 및 구조

SPICE는 현재 집적회로 설계에 필요한 분석법과 소자들을 가지고 있고, 편리하게 쓰기에 충분히 강력하며 빠른 덕분에 유명해졌다.\[15\] 그 이전에 쓰인 프로그램들은 한정된 기능만 수행하였는데, BIAS\[16\]와 SLIC\[17\]이 그러하였다. SPICE는 이러한 기능들을 모두 포함해 많은 회로를 성공적으로 시뮬레이트 하게 되었다.

### 분석

SPICE2에는 다음과 같은 분석이 가능하다.

  - AC 분석 ([선형](https://ko.wikipedia.org/wiki/선형 "wikilink") [소신호](https://ko.wikipedia.org/wiki/소신호_분석 "wikilink") 주파수 도메인 분석)
  - DC 분석 (비선형 [정지점](https://ko.wikipedia.org/wiki/바이어스 "wikilink") 계산)
  - DC 전달 커브 분석 (입력신호가 변할 경우의 동작점 계산)
  - 잡음 분석 (특정 출력에서 관측되는 잡음 분석을 위한 소신호 분석)
  - [전달 함수](https://ko.wikipedia.org/wiki/전달_함수 "wikilink") 분석(소신호 획득 및 임피던스 계산)
  - 과도신호 분석(시간 도메인에서의 대신호 분석)

SPICE가 비선형 회로모델을 자주 사용하기 때문에, 소신호 분석에는 회로가 선형에 가깝게 되는 정지점 계산이 필수적이다. SPICE2는 다른 소신호 분석방식도 가지고있는데, [민감도 분석](https://ko.wikipedia.org/wiki/민감도_분석 "wikilink"), [극영점 분석](https://ko.wikipedia.org/wiki/극영점_분석 "wikilink"), 그리고 [소신호 왜곡 분석이](https://ko.wikipedia.org/wiki/소신호_왜곡_분석 "wikilink") 바로 그것이다. 극한 기후에서의 시뮬레이션을 가정하기 위해서 자동으로 갱신되는 반도체 모델 매개변수도 존재한다.

적절한 분석과 매개변수 선택은 매우 종요하다. 선형 분석과 비선형 분석은 필요한 경우가 다르며, 시뮬레이션이 적용하는 기본값만 사용할 경우 과도신호 분석에 제대로 된 값을 얻기 힘들다.\[18\]

### 장치 모델

SPICE2는 수많은 [트랜지스터 모델을](https://ko.wikipedia.org/wiki/트랜지스터_모델 "wikilink") 포함하고 있다. 그것 뿐만 아니라, [커플링을](../Page/유도계수.md "wikilink") 포함한 저항, 축전기, 인덕터 등도 가지고 있다. [전압원](https://ko.wikipedia.org/wiki/전압원 "wikilink"), [전류원](https://ko.wikipedia.org/wiki/전류원 "wikilink"), 이상적인 [전송선](https://ko.wikipedia.org/wiki/전송선 "wikilink"), 능동소자, 종속원들도 포함하고 있다.

### 입력과 출력:넷리스트, 도식화 및 기입

SPICE2는 텍스트로 된 [넷리스트](https://ko.wikipedia.org/wiki/넷리스트 "wikilink")를 받아 문장으로 출력한다. 이것은 1975년에 자주 쓰인 방식이다. 이러한 출력방식은 문장들의 모임으로 구성될수도 있고, [문자로 된 "그림"이](https://ko.wikipedia.org/wiki/아스키아트 "wikilink") 될 수도 있다. SPICE3는 이전의 방식도 그대로 가지고 있지만, [C 셸과](https://ko.wikipedia.org/wiki/C_셸 "wikilink") 비슷한 [명령 줄 인터페이스로도](../Page/명령_줄_인터페이스.md "wikilink") 제어할 수 있다. 또한 개발용 [워크 스테이션이](https://ko.wikipedia.org/wiki/워크스테이션 "wikilink") 더 흔해짐에 따라[X 윈도우 시스템](https://ko.wikipedia.org/wiki/X_윈도우_시스템 "wikilink") 방식도 추가되었다.

업체들과 다양한 자유 소프트웨어 프로젝트들은 [스키매틱 캡쳐](https://ko.wikipedia.org/wiki/스키매틱_캡쳐 "wikilink") 프론트엔드를 추가하였는데, 이 덕분에 회로의 [개략도](https://ko.wikipedia.org/wiki/개략도 "wikilink")를 직접 그리면 프로그램이 자동으로 넷리스트를 만드는 기능이 추가되었다. 또한, [그래픽 사용자 인터페이스가](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 추가되고, 전압과 전류의 출력값을 벡터로 조작할 수 있게 되었다. 게다가, 파형을 볼 수 있는 적절한 그래픽 도구들이 추가되었다.

## 각주

## 외부 링크

  - [Spice at UC Berkeley](https://embedded.eecs.berkeley.edu/pubs/downloads/spice/index.htm)

### 참조한 원본 문서

  - [The original SPICE1 paper](http://www.eecs.berkeley.edu/Pubs/TechRpts/1973/22871.html)
  - [L. W. Nagel's dissertation (SPICE2)](http://www.eecs.berkeley.edu/Pubs/TechRpts/1975/9602.html)
  - [Thomas Quarles' dissertation (SPICE3)](http://www.eecs.berkeley.edu/Pubs/TechRpts/1989/1216.html)
  - [A brief history of SPICE](http://www.ecircuitcenter.com/SpiceTopics/History.htm)
  - [SPICE2 and SPICE3 at UC Berkeley](http://embedded.eecs.berkeley.edu/pubs/downloads/spice/index.htm)
  - [Cider at UC Berkeley](http://embedded.eecs.berkeley.edu/pubs/downloads/cider/index.htm)

[분류:1973년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1973년_소프트웨어 "wikilink") [분류:EDA 소프트웨어](https://ko.wikipedia.org/wiki/분류:EDA_소프트웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:포트란으로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:포트란으로_작성된_자유_소프트웨어 "wikilink") [분류:회로 설계 시뮬레이션 프로그램](https://ko.wikipedia.org/wiki/분류:회로_설계_시뮬레이션_프로그램 "wikilink")

1.  Nagel, L. W, and Pederson, D. O., *SPICE (Simulation Program with Integrated Circuit Emphasis)*, Memorandum No. ERL-M382, University of California, Berkeley, Apr. 1973
2.  Nagel, Laurence W., *SPICE2: A Computer Program to Simulate Semiconductor Circuits*, Memorandum No. ERL-M520, University of California, Berkeley, May 1975
3.
4.
5.
6.
7.  2nd spice1 ref
8.  2nd spice2 ref
9.  Quarles, Thomas L., *Analysis of Performance and Convergence Issues for Circuit Simulation*, Memorandum No. UCB/ERL M89/42, University of California, Berkeley, Apr. 1989.
10. [history-of-spice](http://www.allaboutcircuits.com/textbook/reference/chpt-7/history-of-spice/) on allaboutcircuits.com *"The origin of SPICE traces back to another circuit simulation program called CANCER. Developed by professor Ronald Rohrer of U.C. Berkeley along with some of his students in the late 1960’s, CANCER continued to be improved through the early 1970’s. When Rohrer left Berkeley, CANCER was re-written and re-named to SPICE, released as version 1 to the public domain in May of 1972. Version 2 of SPICE was released in 1975 (version 2g6—the version used in this book—is a minor revision of this 1975 release). Instrumental in the decision to release SPICE as a public-domain computer program was professor Donald Pederson of Berkeley, who believed that all significant technical progress happens when information is freely shared. I for one thank him for his vision."*
11.
12. Vladimirescu, Andrei, *SPICE -- The Third Decade*, Proc. 1990 IEEE Bipolar Circuits and Technology Meeting, Minneapolis, Sept. 1990, pp. 96–101
13. K. S. Kundert, *The Designer’s Guide to SPICE and Spectre*, Kluwer. Academic Publishers, Boston , 1995
14.
15. Nagel, L., [Is it Time for SPICE4?](http://www.cs.sandia.gov/nacdm/talks/Nagal_Larry_NACDM2004.pdf) , 2004 Numerical Aspects of Device and Circuit Modeling Workshop, June 23–25, 2004, Santa Fe, New Mexico. Retrieved on 2007-11-10
16.
17.
18.