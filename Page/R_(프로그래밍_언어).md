> This article is converted from Wikipedia: [R \(프로그래밍 언어\)](https://ko.wikipedia.org/wiki/R_\(프로그래밍_언어\)).


**R**는 통계 계산과 그래픽을 위한 [프로그래밍 언어이자](../Page/프로그래밍_언어.md "wikilink") 소프트웨어 환경이다. [뉴질랜드](../Page/뉴질랜드.md "wikilink") [오클랜드 대학의](../Page/오클랜드_대학교.md "wikilink") 로버트 젠틀맨(Robert Gentleman)과 로스 이하카(Ross Ihaka)에 의해 시작되어 현재는 R 코어 팀이 개발하고 있다. R는 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink") 하에 배포되는 [S 프로그래밍 언어의](https://ko.wikipedia.org/wiki/S_\(프로그래밍_언어\) "wikilink") 구현으로 [GNU](../Page/GNU.md "wikilink") [S라고도](https://ko.wikipedia.org/wiki/S_\(프로그래밍_언어\) "wikilink") 한다. R는 통계 소프트웨어 개발과 자료 분석에 널리 사용되고 있으며, 패키지 개발이 용이해 통계 소프트웨어 개발에 많이 쓰이고 있다.

## 소개

R의 문법과 통계처리 부분은 AT\&T 벨 연구소가 개발했던 [S를](https://ko.wikipedia.org/wiki/S_\(프로그래밍_언어\) "wikilink") 참고했고, 데이터 처리부분은 [스킴으로부터](../Page/스킴_\(프로그래밍_언어\).md "wikilink") 영향을 받았다.

R는 다양한 통계 기법과 수치 해석 기법을 지원한다. R는 사용자가 제작한 패키지를 추가하여 기능을 확장할 수 있다. 핵심적인 패키지는 R와 함께 설치되며, [CRAN(the Comprehensive R Archive Network)](http://cran.r-project.org/)을 통해 2020년 3월 기준 15,400개 이상의 패키지를 내려 받을 수 있다.

R의 또 다른 강점은 그래픽 기능으로 수학 기호를 포함할 수 있는 출판물 수준의 그래프를 제공하는 것이다.

R는 통계 계산과 소프트웨어 개발을 위한 환경이 필요한 통계학자와 연구자들 뿐만 아니라, [행렬](../Page/행렬.md "wikilink") 계산을 위한 도구로서도 사용될 수 있으며 이 부분에서 GNU Octave나 [MATLAB](../Page/MATLAB.md "wikilink")에 견줄 만한 결과를 보여준다.

R는 윈도, 맥 OS 및 리눅스를 포함한 UNIX 플랫폼에서 이용 가능하다.

### 처리속도

[인터프리터](../Page/인터프리터.md "wikilink") 언어라는 이유로 처리속도가 낮다는 평가를 받는 경우가 많다. 그러나 실제로는 [S의](https://ko.wikipedia.org/wiki/S_\(프로그래밍_언어\) "wikilink") 상용판인 S-PLUS보다 많은 경우 속도가 빠를 뿐만 아니라, 범용행렬계 언어의 표준과도 같은 [MATLAB](../Page/MATLAB.md "wikilink")과 그 파생어인 [GNU Octave](https://ko.wikipedia.org/wiki/GNU_Octave "wikilink"), [Scilab](https://ko.wikipedia.org/wiki/Scilab "wikilink")보다도 종합적으로 빠르다는 평가가 있다.

### RStudio

[RStudio](../Page/RStudio.md "wikilink")는 오픈 소스인 R를 좀 더 편하게 사용하기 위해 개발된 프로그램(IDE, 통합 개발 환경)이다.



## 통계적 특성

R 및 그 라이브러리는 [선형](../Page/선형_회귀.md "wikilink") 및 [비선형](https://ko.wikipedia.org/wiki/:en:Nonlinear_regression "wikilink") 모델링, 고전 통계 테스트, [시계열](../Page/시계열.md "wikilink") 분석, 분류, [클러스터링](../Page/데이터_클러스터.md "wikilink") 등 다양한 통계 및 그래픽 기술을 구현한다. R는 기능 및 확장을 통해 쉽게 확장 가능하며 R 커뮤니티는 패키지와 관련된 적극적인 기여로 유명하다. R의 표준 함수 중 많은 것은 R 자체로 작성되어 사용자가 쉽게 알고리즘을 사용할 수 있다. 계산 작업의 경우 C, C ++ 및 Fortran 코드를 런타임에 링크하고 호출할 수 있다. R 객체를 직접 C, C ++,\[1\] Java\[2\],NET\[3\]또는 Python 코드로 작성할 수 있다. R는 많은 사람들이 만든 패키지를 공유해 특정 기능이나 특정 분야의 연구 분야에서 매우 확장성이 뛰어나다. [S의](https://ko.wikipedia.org/wiki/S_\(프로그래밍_언어\) "wikilink") 전통으로 인해 R는 대부분의 통계 컴퓨팅 언어보다 강력한 객체 지향 프로그래밍 기능을 제공한다.

R의 또 다른 장점은 수학 그래픽을 포함해 고품질의 그래프를 만들 수 있는 정적 그래픽이다. 다이나믹하고 인터랙티브 한 그래픽도 추가 패키지를 통해 제공된다.\[4\]

R에는 [LaTeX](../Page/LaTeX.md "wikilink")와 유사한 자체 문서 형식인 [Rd](http://www.hep.by/gnu/r-patched/r-exts/R-exts_49.html)가 있으며, 이는 온라인과 하드카피에서 포괄적인 문서를 제공하는 데 사용된다.

## 각주

## 외부 링크

  -
  -
  - [R 프로젝트 홈페이지](http://www.r-project.org/)

  - [R Development Translation Team (Korean)](http://www.openstatistics.net//)

[분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink") [분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:1993년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1993년_개발된_프로그래밍_언어 "wikilink") [분류:과학 소프트웨어](https://ko.wikipedia.org/wiki/분류:과학_소프트웨어 "wikilink") [분류:문학적 프로그래밍](https://ko.wikipedia.org/wiki/분류:문학적_프로그래밍 "wikilink")

1.
2.
3.
4.