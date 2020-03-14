> This article is converted from Wikipedia: [COCOMO](https://ko.wikipedia.org/wiki/COCOMO).


**COCOMO**(constructive cost model의 약자)는 소프트웨어 개발의 공정 개발 기간의 견적 방법 중 하나이며, 1981년에 [배리 W. 보임이](https://ko.wikipedia.org/wiki/배리_W._보임 "wikilink") 제창했다. 이 모델은 프로젝트에 영향을 줄 수있는 다양한 특성들 -예를들자면 개발기간, 투입공수 같은 변수-을 변수로 회귀공식을 만들어 소프트웨어 개발 비용을 산정한다.

모델의 복잡도에 따라 Basic COCOMO, Intermediate COCOMO, Detailed COCOMO으로 세분화 할 수 있다.

## Basic COCOMO

**Basic COCOMO**는 프로그램 크기를 예측하는 기능으로써 소프트웨어 개발에 대한 노력과 비용을 계산한다. 프로그램 크기는 수천 줄의 소스코드 예측 안에 표현된다.(SLOC, KLOC).

다음은 COCOMO에서 사용하는 소프트웨어 프로젝트 클래스 세 가지 :

  - Organic projects - 엄격하지 않은 요구사항에 대한 좋은 작업 경험을 가진 작은 팀
  - Semi-detached projects - 엄격하지 않은 요구사항과 다양한 요구사항에 대해 다양한 작업 경험을 가진 중간 팀
  - Embedded projects - 타이트한 제약조건 속에서 발전되어온 팀. organic 과 semi-detached 프로젝트가 결합됐다.(하드웨어, 소프트웨어, 조작상의, ...)

Basic COCOMO 식은 다음과 같은 형태를 취한다.

  -
    **Effort Applied (E)** = a<sub>b</sub>(KLOC)<sup>b<sub>b</sub></sup> **\[man-months\]**
    **Development Time (D)** = c<sub>b</sub>(Effort Applied)<sup>d<sub>b</sub></sup> **\[months\]**
    **People required (P)** = Effort Applied / Development Time **\[count\]**

여기서 **KLOC**는 프로젝트 소스 코드의 라인 수를 천 단위로 산정된다. *a<sub>b</sub>*, *b<sub>b</sub>*, *c<sub>b</sub>*, *d<sub>b</sub>* 사이의 관계는 다음 표를 따른다.

| Software project | *a*<sub>*b*</sub> | *b*<sub>*b*</sub> | *c*<sub>*b*</sub> | *d*<sub>*b*</sub> |
| ---------------- | ----------------- | ----------------- | ----------------- | ----------------- |
| Organic          | 2.4               | 1.05              | 2.5               | 0.38              |
| Semi-detached    | 3.0               | 1.12              | 2.5               | 0.35              |
| Embedded         | 3.6               | 1.20              | 2.5               | 0.32              |

Basic COCOMO는 빠른 코드 예측에 좋다. 하지만 하드웨어의 한계, 팀원들의 능력과 경험, 최신 개발툴과 기술의 사용 등의 변수를 계산하지 못 한다. [분류:소프트웨어 개발](https://ko.wikipedia.org/wiki/분류:소프트웨어_개발 "wikilink")