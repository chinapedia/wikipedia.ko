> This article is converted from Wikipedia: [GN \(빌드 시스템\)](https://ko.wikipedia.org/wiki/GN_\(빌드_시스템\)).


**GN**(Generates Ninja build files)은 [닌자](../Page/닌자_\(빌드_시스템\).md "wikilink")(Ninja)로 응용프로그램 프로젝트를 구축 할 수 있도록 Ninja 빌드 파일을 생성하는 메타 빌드 시스템이다.\[1\]

## GYP의 차세대 메타 빌드시스템

  - GN 파일은 [GYP](../Page/GYP_\(소프트웨어\).md "wikilink") 파일보다 읽기 쉽고 유지 관리가 쉽다.\[2\]
  - GN은 GYP보다 최대 약20 배 빠르다.
  - GN은 빌드의 일부로 Ninja가 필요에 따라 자동으로 다시 실행되도록 지원한다. 이렇게하면 빌드 파일을 변경할 때 GN을 다시 실행하는 것을 기억할 필요가 없다.
  - GN은 [의존성](https://ko.wikipedia.org/wiki/데이터_의존성 "wikilink") 적용을위한 더 나은 도구를 제공한다 (gn check 및 visibility, public_deps 및 data_deps 옵션 참조).
  - GN은 빌드 트리 그래프를 쿼리하기 위한 도구를 제공한다. 예를 들어 "X가 의존하는 것"과 "X에 의존하는 것"을 조회할 수 있다.

## 크로미움 프로젝트와의 관계

크로미움 프로젝트에의한 GN 프로젝트는 [닌자](../Page/닌자_\(빌드_시스템\).md "wikilink")(Ninja)로 [크로미움(Chromium)을](https://ko.wikipedia.org/wiki/크로미움_\(웹_브라우저\) "wikilink") 빌드 할 수 있도록 Ninja 빌드 파일을 생성하는 메타 빌드 시스템이다.

2016 년 10 월 기준으로 모든 Chromium 빌드가 GYP에서 GN으로 전환되었다. 거의 모든 GYP 파일이 크로미움 저장소(Chromium repos)에서 대체되었다. 결과적으로 더 이상 GYP로 빌드 할 수 없다.

변환할 필요가있는 "Closure Compilation"빌더를위한 GYP 파일이 여전히 남겨져있다. 일부 관련 프로젝트 (예 : [V8](https://ko.wikipedia.org/wiki/V8 "wikilink"), [Skia](https://ko.wikipedia.org/wiki/Skia "wikilink"))는 여전히 자체적인 이유로 GYP를 지원할 수 있다. 아직도 gclient가 GYP_DEFINES를 사용하는것과 같은 기능을 남겨놓고 있다.

## 함께보기

  - [닌자](../Page/닌자_\(빌드_시스템\).md "wikilink")(Ninja)

## 각주

[분류:컴퓨터 프로그래밍](https://ko.wikipedia.org/wiki/분류:컴퓨터_프로그래밍 "wikilink")

1.  [What is GN?](https://chromium.googlesource.com/chromium/src/+/master/tools/gn/README.md)
2.  [GN](https://chromium.googlesource.com/chromium/src/+/master/tools/gn/docs/standalone.md)