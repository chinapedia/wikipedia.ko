> This article is converted from Wikipedia: [Einstein@Home](https://ko.wikipedia.org/wiki/Einstein@Home).


**Einstein@Home**은 [미국](../Page/미국.md "wikilink")의 [위스콘신 대학교](../Page/위스콘신_대학교.md "wikilink") 밀워키 캠퍼스에서 주관하고 있는 [BOINC](../Page/BOINC.md "wikilink")(Berkeley Open Infrastructure Network Computing) 기반의 [분산 컴퓨팅](../Page/분산_컴퓨팅.md "wikilink") 프로젝트 중 하나이다. 이 프로젝트는 [아레시보 천문대로](../Page/아레시보_천문대.md "wikilink") 관측된 자료를 [LIGO](https://ko.wikipedia.org/wiki/LIGO "wikilink")(, 레이저 간섭 중력파 관측소)로부터 받아 [펄서](https://ko.wikipedia.org/wiki/펄서 "wikilink") 등으로부터 오는 [중력파](../Page/중력파.md "wikilink")를 감지하기 위한 프로젝트이다.

## 개요

Einstein@Home은 [2005년](../Page/2005년.md "wikilink") [2월 19일](../Page/2월_19일.md "wikilink") [2005년 세계 물리의 해를](https://ko.wikipedia.org/wiki/2005년_세계_물리의_해 "wikilink") 맞이하여 미국 물리학협회()로부터 지원을 받아 시작되었다. 이 프로젝트는 [BOINC](../Page/BOINC.md "wikilink")을 이용하는 다른 프로젝트들([SETI@home](../Page/SETI@home.md "wikilink")등)과 마찬가지로 일반 사용자들의 자발적인 참여로 이루어지며 [2010년](../Page/2010년.md "wikilink") 1월 기준으로 BOINC 내부 프로젝트 중 세 번째로 많은 사용자들이 참여하고 있는 프로젝트이다. \[1\]

## 목적

Einstein@Home의 목적은 전천(全天)을 대상으로 [중력파](../Page/중력파.md "wikilink")의 존재를 실증하는 것이다. [아인슈타인](https://ko.wikipedia.org/wiki/아인슈타인 "wikilink")의 [일반상대성이론](https://ko.wikipedia.org/wiki/일반상대성이론 "wikilink")에 따르면 모든 질량을 가진 물체는 중력파를 발생하게 되어있고 특히 [펄서](https://ko.wikipedia.org/wiki/펄서 "wikilink")나 [블랙홀](https://ko.wikipedia.org/wiki/블랙홀 "wikilink") 등과 같이 비정상적으로 큰 중력을 가진 물체들의 경우에는 더 큰 중력파를 발생하게 되어 있으나 아직까지 중력파가 존재한다는 명확한 증거는 찾지 못하였다.

그러나 지금까지 [태양](../Page/태양.md "wikilink")의 중력에 의한 별빛의 휨 현상, [수성의 근일점 이동](https://ko.wikipedia.org/wiki/수성의_근일점_이동 "wikilink"), [은하단](../Page/은하단.md "wikilink")의 중력에 의한 [중력 렌즈](https://ko.wikipedia.org/wiki/중력_렌즈 "wikilink") 현상 등 일반상대성 이론의 증거들이 계속 밝혀져 왔기 때문에 중력파 또한 발견될 것이라 생각하고 그 발견을 위해 노력하고 있다. 만일 중력파가 발견된다면 이론의 정확함이 또 한번 밝혀짐과 동시에 거의 모든 물체를 통과하는 성질에 의하여 지금까지 [암흑물질](../Page/암흑물질.md "wikilink")등에 의하여 관측이 불가능했던 [은하계](https://ko.wikipedia.org/wiki/은하계 "wikilink")의 중심부라든지 별의 내부 등을 관측할 수 있는 기회가 될 수 있다.

## 소프트웨어

Einstein@Home은 LIGO나 GEO로부터 넘겨받은 데이터를 [고속 푸리에 변환](../Page/고속_푸리에_변환.md "wikilink")(, FFT)를 이용하여 분석한다.

### CUDA

[2009년](../Page/2009년.md "wikilink") [11월 26일에는](../Page/11월_26일.md "wikilink") [CUDA](../Page/CUDA.md "wikilink")()를 이용하여 계산을 할 수 있는 프로그램이 홈페이지를 통하여 제공이 되었으며 이를 이용하면 계산을 훨씬 빠르게 수행할 수 있다.

### 최적화 프로그램

기본적으로 홈페이지에서 제공하는 프로그램은 비교적 예전 [CPU부터](../Page/중앙_처리_장치.md "wikilink") 최신의 CPU까지 모두 작동할 수 있도록 최신 CPU에서 제공하는 여러가지 최적화된 명령어([x86](https://ko.wikipedia.org/wiki/x86 "wikilink")계열 CPU의 경우에는 [MMX](../Page/MMX.md "wikilink")나 [SSE](https://ko.wikipedia.org/wiki/SSE "wikilink") 등)들을 사용하지 않는다. 그러나 해당 명령어들은 [부동소수점](../Page/부동소수점.md "wikilink")연산의 향상을 위하여 추가된 만큼 사용할 경우 속도의 향상이 있기 때문에 최신 CPU의 성능 향상을 위해 별도로 최적화된 프로그램을 일부 개발자들이 만들어서 배포하고 있다. 또한 계산의 알고리즘을 개선하여 정식 배포 프로그램까지 적용한 경우도 있다. \[2\]

## 참고 자료

<references />

## 같이 보기

  - [BOINC](../Page/BOINC.md "wikilink")
  - [SETI@home](../Page/SETI@home.md "wikilink")
  - [아인슈타인](https://ko.wikipedia.org/wiki/아인슈타인 "wikilink")
  - [중력파](../Page/중력파.md "wikilink")

## 외부 링크

  - [Einstein@Home 공식 홈페이지](http://einstein.phys.uwm.edu/)

  - [BOINC 공식 홈페이지](http://boinc.berkeley.edu)

  - [SETIKAH@KOREA 팀 홈페이지](http://cafe.naver.com/setikah)

[분류:BOINC](https://ko.wikipedia.org/wiki/분류:BOINC "wikilink") [분류:중력파 망원경](https://ko.wikipedia.org/wiki/분류:중력파_망원경 "wikilink") [분류:2005년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2005년_소프트웨어 "wikilink")

1.
2.