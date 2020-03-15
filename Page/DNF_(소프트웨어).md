> This article is converted from Wikipedia: [DNF \(\)](https://ko.wikipedia.org/wiki/DNF_\(\)).


**DNF**(Dandified Yum)는 [RPM](https://ko.wikipedia.org/wiki/RPM_패키지_매니저 "wikilink") 기반 [리눅스 배포판을](https://ko.wikipedia.org/wiki/리눅스_배포판 "wikilink") 위한 [패키지 관리도구이다](https://ko.wikipedia.org/wiki/패키지_관리자 "wikilink").

[페도라](https://ko.wikipedia.org/wiki/페도라_\(운영_체제\) "wikilink") 18에 처음 도입되었고,\[1\] [페도라](https://ko.wikipedia.org/wiki/페도라_\(운영_체제\) "wikilink") 22와 [레드햇 엔터프라이즈 리눅스](https://ko.wikipedia.org/wiki/레드햇_엔터프라이즈_리눅스 "wikilink") 8부터 기존의 [Yum](https://ko.wikipedia.org/wiki/Yum "wikilink")을 대신하여 기본 패키지 관리도구로 채택되었다.\[2\]\[3\]

DNF는 [Yum](https://ko.wikipedia.org/wiki/Yum "wikilink")의 낮은 성능, 많은 메모리 사용량, 비효율적인 중복 의존성 해결 메커니즘 등의 문제를 해결하기 위해 개발되었고,\[4\] Yum과 달리, 외부 라이브러리인 libsolv를 통해 의존성 문제를 처리한다.\[5\]

DNF는 [RPM 패키지 매니저와](https://ko.wikipedia.org/wiki/RPM_패키지_매니저 "wikilink") 여러 지원 라이브러리를 이용하여 패키지 관리 작업을 수행한다.

처음에는 [Yum](https://ko.wikipedia.org/wiki/Yum "wikilink") 3.4를 기반으로 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")으로 개발되었지만, 지금은 대부분의 기능을 [C로](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") [포팅](https://ko.wikipedia.org/wiki/포팅 "wikilink")하여 libdnf 라이브러리로 옮기는 작업이 진행중이다.\[6\]

## 의존 라이브러리

### libdnf

  - DNF와 기반 라이브러리들의 고수준 [API](https://ko.wikipedia.org/wiki/API "wikilink")를 제공
  - [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [LGPLv2+](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서#GPLv2 "wikilink")

### libsolv

  - [충족 가능성](https://ko.wikipedia.org/wiki/충족_가능성_문제 "wikilink") [알고리즘](https://ko.wikipedia.org/wiki/알고리즘 "wikilink")을 이용하여 패키지 의존성 문제를 처리하는 라이브러리
  - 패키지를 관리하고 저장소를 이용할 때 사용
  - [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), [BSD 허가서](https://ko.wikipedia.org/wiki/BSD_허가서 "wikilink")

### librepo

  - 리눅스 저장소에서 메타 데이터와 패키지를 내려받을 때 사용하는 [API](https://ko.wikipedia.org/wiki/API "wikilink")를 제공 ([libcURL과](https://ko.wikipedia.org/wiki/cURL "wikilink") 유사한 C와 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")용 API)
  - [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), [LGPLv2+](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서#GPLv2 "wikilink")

### libcomps

  - 파이썬으로 작성된 yum.comps 라이브러리를 대체하기 위해 C로 작성된 라이브러리. [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")용 바인딩도 제공.
  - [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), GPLv2+

## 각주

## 외부 링크

  -
[분류:페도라 프로젝트](https://ko.wikipedia.org/wiki/분류:페도라_프로젝트 "wikilink") [분류:리눅스 패키지 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_패키지_관리_관련_소프트웨어 "wikilink") [분류:레드햇 소프트웨어](https://ko.wikipedia.org/wiki/분류:레드햇_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.