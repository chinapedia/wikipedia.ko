> This article is converted from Wikipedia: [Waf](https://ko.wikipedia.org/wiki/Waf).


**와프**(Waf또는 WAF)는 컴퓨터 소프트웨어의 자동 컴파일 및 설치를 지원하도록 설계된 빌드 자동화 도구이다. 이것은 파이썬으로 작성되었으며 토마스 네기(Thomas Nagy)가 관리한다.

Waf의 소스 코드는 [New BSD License의](../Page/BSD_허가서.md "wikilink") 조건에 따라 배포되는 [오픈 소스 소프트웨어이다](../Page/오픈_소스_소프트웨어.md "wikilink"). 함께 제공되는 문서는 수정 및 상업적 재배포를 금지하는 CC-BY-NC-ND 라이센스하에 있다. 이러한 상태에서 [데비안](../Page/데비안.md "wikilink") 프로젝트는 그들의 배포판에 Waf 문서를 포함시키고있다.

## 히스토리

토마스 네기(Thomas Nagy)는 Autotools와같은 높은 수준의 기능을 제공하는 SCons 위에 기반하여 설계된 BKsys라는 빌드 자동화 도구를 만들었었다. 이는 KDE 4 개발주기의 초기 단계에서 KDE를 Autotools에서 최신 빌드 시스템으로 전환하려는 노력의 일환이었다. BKsys / SCons는 새로운 표준 빌드 시스템으로 KDE 커뮤니티에서 선택했다. 토마스 네기(Thomas Nagy)가 SCons의 근본적인 문제(특히 취약한 확장성)가 너무 복잡하고 수정하는데도 어려움이있다는 결정적인 이유로 그는 Waf라는 완전한 빌드시스템의 재작성을 시작했다. BKsys가 막 다른 골목으로 인식되면서 KDE는 대신 [CMake](../Page/CMake.md "wikilink")로 전환하기로 결정했으나 Waf는 계속해서 개별 프로젝트로 유지되어 왔으며 이후 다른 공동체에서 많은 추가 개발과 채택이 이루어졌다.\[1\]\[2\]

## CDT

서로 다른 기종의 [운영체제](https://ko.wikipedia.org/wiki/운영체제 "wikilink")에 대한 크로스 디벨롭먼트 툴(Cross Development Tools)로서 빌드 자동화 시스템에 강점을 가지고있다.\[3\]\[4\]

## 함께보기

  - [make](https://ko.wikipedia.org/wiki/make_\(소프트웨어\) "wikilink")
  - [ninja](../Page/닌자_\(빌드_시스템\).md "wikilink")

## 참고

## 외부 링크

  -
[분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink")

1.
2.
3.  Eclipse CDT for C/C++ , Cross GNU , Cross ARM GNU
4.  [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink") - [The GNU Embedded Toolchain for Arm](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads)