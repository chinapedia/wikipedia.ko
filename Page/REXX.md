> This article is converted from Wikipedia: [REXX](https://ko.wikipedia.org/wiki/REXX).


**REXX** (REstructured eXtended eXecutor)는 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")사가 개발한 [해석](https://ko.wikipedia.org/wiki/해석_언어 "wikilink") [프로그래밍 언어이다](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink"). 배우기 쉬울뿐 아니라 읽기도 쉬운, 구조화된 고급 프로그래밍 언어이다. REXX는 수많은 컴퓨터 운영 체제를 지원하며 컴파일러는 IBM 메인프레임으로 사용할 수 있다. REXX의 경우 상용 버전과 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") [인터프리터](https://ko.wikipedia.org/wiki/인터프리터 "wikilink")가 둘 다 존재한다.

REXX는 [스크립트](../Page/스크립트_언어.md "wikilink") 및 [매크로](https://ko.wikipedia.org/wiki/매크로_\(컴퓨터_과학\) "wikilink") 언어로 사용되며 데이터와 텍스트를 처리하고 보고서를 만드는 목적으로 종종 사용된다. [펄](https://ko.wikipedia.org/wiki/펄 "wikilink")과 유사성이 있는데, REXX는 [공통 게이트웨이 인터페이스](https://ko.wikipedia.org/wiki/공통_게이트웨이_인터페이스 "wikilink")(CGI) 프로그래밍과 잘 맞으며 실제로 이 목적을 위해 사용된다. REXX는 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [MVS](../Page/MVS.md "wikilink"), [VM](https://ko.wikipedia.org/wiki/VM_\(운영_체제\) "wikilink"), [아미가OS](https://ko.wikipedia.org/wiki/아미가OS "wikilink")와 같은 일부 운영 체제의 주된 스크립트 언어이며 [KEDIT](https://ko.wikipedia.org/wiki/XEDIT "wikilink"), [THE](https://ko.wikipedia.org/wiki/더_헤슬링_에디터 "wikilink"), [ZOC](https://ko.wikipedia.org/wiki/ZOC_\(소프트웨어\) "wikilink") 터미널 에뮬레이터와 같은 기타 일부 소프트웨어에서 내부 매크로 언어로도 사용된다. 또한, REXX 언어는 REXX 엔진이 설치된 경우 윈도우 스크립팅 호스트 ActiveX 스크립트 엔진 언어를 사용하는 프로그램(VBScript, JScript)의 스크립트 및 매크로에 사용할 수 있다.

REXX는 VM/SP 이상, TSO/E 버전 2 이상, OS/2 (1.3 이상, 공식적으로 Procedures Language/2), 아미가OS 버전 2 이상, PC DOS(7.0 또는 2000), 윈도우 NT 4.0 (리소스 킷: Regina)와 함께 제공된다. OS/2용 REXX 스크립트는 다른 스크립트 언어와 함께 .cmd라는 파일 확장자를 함께 쓰고 있으며 스크립트의 첫 줄은 사용할 인터프리터를 규정한다. REXX를 인지하는 애플리케이션들을 위한 REXX 매크로는 애플리케이션이 정의하는 확장 기능을 사용한다. 1980년대 말에 REXX는 [IBM 시스템 애플리케이션 아키텍처용](https://ko.wikipedia.org/wiki/IBM_시스템_애플리케이션_아키텍처 "wikilink") 공통 스크립트 언어가 되었으며, 여기에서 이름이 "SAA Procedure Language REXX"로 변경되었다.

REXX 스크립트나 명령은 [CP/CMS](https://ko.wikipedia.org/wiki/CP/CMS "wikilink")와 VM/307의 과거 [EXEC](https://ko.wikipedia.org/wiki/CMS_EXEC "wikilink") 명령 언어 및 VM/SP의 [EXEC 2](https://ko.wikipedia.org/wiki/EXEC_2 "wikilink") 명령 언어를 REXX이 대체한다는 의미로 종종 "EXEC"를 가리키기도 한다.

## 역사

Rexx는 1979년 3월 20일부터 1982년 중순까지 'own-time' 프로젝트로서, 또 원래는 [EXEC](https://ko.wikipedia.org/wiki/EXEC "wikilink")와 [EXEC 2](https://ko.wikipedia.org/wiki/EXEC_2 "wikilink") 언어를 대체할 [스크립트 프로그래밍 언어로서](https://ko.wikipedia.org/wiki/스크립트_프로그래밍_언어 "wikilink"), IBM의 [마이크 콜리셔에](https://ko.wikipedia.org/wiki/마이크_콜리셔 "wikilink") 의해 [어셈블리어](https://ko.wikipedia.org/wiki/어셈블리어 "wikilink")로 설계되어 처음 구현되었다.\[1\] 모든 시스템을 위한 [매크로나](https://ko.wikipedia.org/wiki/매크로_\(컴퓨터_과학\) "wikilink") 스크립트 언어가 되도록 설계되었다. 또, Rexx는 [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink") 프로그래밍 언어의 버전을 더 단순하고 더 쉽게 배울 수 있도록 고안되었다.

1981년 텍사스 주 휴스턴의 SHARE 56 콘퍼런스에서 대중에게 처음 설명되었다.\[2\]

## 기능

REXX는 다음의 기능을 제공한다:

  - [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink") 기반
  - [동적 자료형](https://ko.wikipedia.org/wiki/형_시스템 "wikilink") (선언이 없음)
  - [예약어](https://ko.wikipedia.org/wiki/예약어 "wikilink") 없음 (로컬 환경은 제외)
  - [다배장 정수](https://ko.wikipedia.org/wiki/다배장_정수 "wikilink")
  - [부동 소수점](https://ko.wikipedia.org/wiki/부동_소수점 "wikilink")
  - 자체 함수의 고급 선택
  - 기억 자료 자동 관리
  - 충돌 보호
  - [연상 배열](https://ko.wikipedia.org/wiki/연상_배열 "wikilink")
  - 시스템 명령과 기능에 직접 접근
  - 단순 오류 관리, 자체 추적 및 오류 정정
  - 인간의 제한이 거의 없음
  - 단순화된 입출력 기능

## 예제

다음은 간단한 계산기를 구현한 것이다.

``` rexx
 X = 'input BYE to quit'
 do until X = 'BYE' ; interpret 'say' X ; pull X ; end
```

## 각주

## 외부 링크

  - [REXX 언어 페이지](http://www.ibm.com/rexx/) (IBM)
  - [REXX 언어 협회](http://www.rexxla.org/)
  - [오픈 오브젝트 Rexx 웹사이트](http://www.oorexx.org/)

[분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:1979년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1979년_개발된_프로그래밍_언어 "wikilink") [분류:IBM 소프트웨어](https://ko.wikipedia.org/wiki/분류:IBM_소프트웨어 "wikilink") [분류:셸](https://ko.wikipedia.org/wiki/분류:셸 "wikilink")

1.
2.