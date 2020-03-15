> This article is converted from Wikipedia: [V ](https://ko.wikipedia.org/wiki/V_).


[350px](https://ko.wikipedia.org/wiki/파일:V-model.JPG "wikilink")

**V 모델**(V-model)은 [소프트웨어 개발 프로세스로](https://ko.wikipedia.org/wiki/소프트웨어_개발_프로세스 "wikilink") [폭포수 모델의](../Page/폭포수_모델.md "wikilink") 확장된 형태 중 하나로 볼 수 있다. 아래 방향으로 선형적으로 내려가면서 진행되는 [폭포수 모델과](../Page/폭포수_모델.md "wikilink") 달리, 이 프로세스는 오른쪽 그림과 같이 코딩 단계에서 위쪽으로 꺾여서 알파벳 V자 모양으로 진행된다. V 모델은 개발 생명주기의 각 단계와 그에 상응하는 [소프트웨어 시험](https://ko.wikipedia.org/wiki/소프트웨어_시험 "wikilink") 각 단계의 관계를 보여준다.

V 모델은 소프트웨어 개발의 각 단계마다 상세한 문서화를 통해 작업을 진행하는 잘 짜인 방법을 사용한다. 또한 테스트 설계와 같은 테스트 활동을 코딩 이후가 아닌 프로젝트 시작 시에 함께 시작하여, 전체적으로 많은 양의 프로젝트 비용과 시간을 감소시킨다.

## 검증(Verification) 단계들

### 요구사항 분석

[요구사항 분석](https://ko.wikipedia.org/wiki/요구사항_분석 "wikilink") 단계에서, 개발될 시스템에 대한 [요구사항](../Page/요구사항.md "wikilink")은 시스템 사용자의 필요를 분석함으로써 얻을 수 있다. 이 단계는 목표로 하는 이상적인 시스템이 수행해야할 기능에 대해 고민하는 단계이다. 그러나 이 단계에서는 소프트웨어가 어떻게 설계되고 구현될 것인지에 대한 사항은 다루지 않는다. 통상적으로 이 단계에서는 사용자를 만나 기능에 대한 의견을 청취하고, 이를 사용자 요구사항 문서로 생성하게 된다.

사용자 요구사항 문서는 일반적으로 사용자가 기대하는 시스템의 기능적 요구사항, 물리적 요구사항, 인터페이스 요구사항, 성능 요구사항, 데이터 요구사항, 보안(security) 요구사항 등을 기록한다. 이 문서는 비지니스 분석가가 시스템에 대해 이해한 바를 사용자와 협의할때 이용되는 문서이기도 하다. 이 문서는 또한 시스템 설계 단계에서 설계자에 대한 지침으로 사용되기 때문에, 사용자는 주의깊이 이 문서를 검토하여야 한다. 통상적으로 사용자 수락시험에 대한 설계는 이 요구사항 분석 단계에서 이루어진다. 참고로 [기능적 요구사항과](https://ko.wikipedia.org/wiki/기능적_요구사항 "wikilink") [비기능적 요구사항](https://ko.wikipedia.org/wiki/비기능적_요구사항 "wikilink") 항목을 살펴보라.

### 시스템 설계

[시스템 설계](https://ko.wikipedia.org/wiki/시스템_설계 "wikilink") 단계에서 시스템 엔지니어는 사용자 요구사항 문서를 면밀히 검토하는 것을 통해 개발할 시스템에 대해 분석하고 이해한다. 또한 시스템 엔지니어는 사용자 요구사항을 구현 가능성과 필요한 기술들을 파악한다. 그리고 만약 요구사항 중 어느 한 가지라도 구현이 불가능할 경우, 이에 대해 사용자에게 알린다. 문제점이 발견되면 해결 가능할 경우, 변경 사항을 반영하여 요구사항 문서를 수정한다.

그러한 과정을 거쳐 개발 단계를 위한 청사진이 될 소프트웨어 기술서(software specification document)가 생성된다. 이 문서는 일반적인 시스템 구성과 메뉴 구조, [자료 구조](https://ko.wikipedia.org/wiki/자료_구조 "wikilink") 등을 기술한다. 또한 기술서는 비즈니스 시나리오에 대한 예나 샘플 윈도, 이해를 돕기 위한 보고서 등을 추가로 포함할 수 있다. 엔티티 다이어그램(entity diagrams)이나 데이터 목록(data dictionary)과 같은 기술자료 또한 설계 단계에서 산출된다. 그에 더하여 시스템 테스트를 위한 문서도 이 단계에서 준비된다.

### 아키텍처 설계

[컴퓨터 아키텍처](https://ko.wikipedia.org/wiki/컴퓨터_아키텍처 "wikilink") 및 [소프트웨어 아키텍처](https://ko.wikipedia.org/wiki/소프트웨어_아키텍처 "wikilink") 설계 단계를 합쳐서 고수준 설계라 부른다. 아키텍처를 선택함으로써 만들어지는 베이스라인은 일반적으로 모든 구현될 모듈 항목과 그 간략한 기능을 정의하고, 모듈 간의 인터페이스, 관계, 의존성을 기술하며, 필요한 데이터베이스 테이블, 아키텍처 다이어그램, 적용기술 내역을 기술한다. 또한 이 단계에서 통합 테스트에 대한 설계가 이루어진다.

### 모듈 설계

[모듈 설계](https://ko.wikipedia.org/wiki/모듈_설계 "wikilink") 단계를 다른 말로 저수준 설계라 부른다. 아키텍처 설계 단계에서 정의된 모듈 항목을 더 세분하여 각각의 모듈에 대한 기술을 작성하며, 이를 이용하여 프로그래머들이 코딩을 시작할 수 있도록 만들어 준다.

이 단계에서 작성될 저수준 설계 문서 또는 프로그램 명세서에서는 각 모듈의 상세한 기능 로직을 의사 코드 (pseudocode)를 이용하여 기술하고, API 명세를 통해 의존성 관련 이슈를 포함하여 각 모듈의 모든 인터페이스 상세 사항을 기술하며, 각 모듈의 에러 코드와 메시지를 기술하며, 각 모듈의 입력과 출력을 기술하며, 필요할 경우 모듈에서 사용하는 데이터 베이스 테이블의 구조와 요소별 타입과 크기또한 기술한다. 또한 이 단계에서는 단위 테스트를 위한 케이스와 절차가 설계된다.

## 유효화(Validation) 단계들

### 단위 테스트

V 모델 방식의 소프트웨어 개발에서 [단위 테스트는](https://ko.wikipedia.org/wiki/단위_테스트 "wikilink") 테스트 프로세스의 첫 단계이다. 소프트웨어 개발 전문가인 Barry Boehm에 따르면, 단위 시험 단계에서 오류를 수정할 경우, 고객에까지 오류가 전달되었을 때에 비해 수백 배의 수정 비용을 절감할 수 있다.

단위 테스트 시에는 에러를 줄이기 위한 의도로 작성된 코드에 대한 분석을 진행한다. 또한 코드가 효율적으로 작성되었는지, 프로젝트 내에 합의된 코딩 표준을 준수하고 있는지도 검증한다. 대개 이 단계에서의 테스트는 [화이트박스 테스트이다](https://ko.wikipedia.org/wiki/화이트박스_테스트 "wikilink"). 모듈 설계 단계에서 준비된 테스트 케이스를 이용하며, 코드를 개발한 개발자가 직접 수행한다.

### 통합 테스트

[통합 테스트](https://ko.wikipedia.org/wiki/통합_테스트 "wikilink") 단계에서는, 각각의 모듈들을 통합하여, 통합된 컴포넌트 간의 인터페이스와 상호작용 상의 오류를 발견하는 작업을 수행한다. 대개 이 단계에서는 테스트는 [블랙박스 테스트](https://ko.wikipedia.org/wiki/블랙박스_테스트 "wikilink")(Black box testing) 이며, 따라서 코드를 직접 확인하는 형태는 아니다. 아키텍처 설계 단계에서 준비된 테스트 케이스를 사용하여 테스트가 진행되며, 일반적으로 개발자가 진행한다.

### 시스템 테스트

[시스템 테스트는](https://ko.wikipedia.org/wiki/시스템_테스트 "wikilink") 실제 구현된 시스템과 계획된 사양(specifications)을 서로 비교하는 작업이다. 이 단계에서 시스템 테스트에 대한 설계가 시스템 설계 문서로부터 도출되어 사용된다. 때로 시스템 테스트는 자동화 도구를 이용하여 [자동화된다](https://ko.wikipedia.org/wiki/테스트_자동화 "wikilink"). 모든 모듈을 통합한 후에, 시스템 레벨의 에러들이 이 테스트 단계를 통해 발견될 수 있다. 개발자와 다른 별도의 테스트팀에 의해 수행된다.

### 인수 테스트

인수 테스트는 시스템이나 시스템의 일부 또는 특정한 비기능적인 특성에 대해 "확신(Confidence)"을 얻는 작업이다. 이 단계에서 결함을 찾는 것은 인수 테스팅의 주 목적이 아니다. 이 테스트는 시스템을 배포하거나 실제 사용할만한 준비가 되었는지에 대해 평가한다. 하지만 대규모의 통합 테스트를 시스템에 대한 인수 테스트 이후에 실행할 수 있기 때문에 인수 테스팅이 반드시 최종 단계 테스팅이라고는 할 수 없다. 인수 테스팅의 전형적인 형태는 사용자 인수 테스팅, 운영상의 인수 테스팅등이 있다.

## 같이 보기

  - [시스템 개발 생명주기](https://ko.wikipedia.org/wiki/시스템_개발_생명주기 "wikilink")
  - [제품 생명주기 관리](https://ko.wikipedia.org/wiki/제품_생명주기_관리 "wikilink")

## 더 읽을 거리

  - Roger S. Pressman:*Software Engineering: A Practitioner's Approach*, The McGraw-Hill Companies,
  - Mark Hoffman & Ted Beaumont: *Application Development: Managing the Project Life Cycle*, Mc Press, ISBN-10: 1883884454
  - Boris Beizer: *Software Testing Techniques.* Second Edition, International Thomson Computer Press, 1990,

## 외부 링크

  - [A paper by Christian Bucanac](http://www.bucanac.com/documents/The_V-Model.pdf)
  - [소프트웨어 생명주기와 식스시그마(The SDLC and SixSigma)](https://web.archive.org/web/20070929144804/http://www.iacis.org/iis/2004_iis/PDFfiles/Boggs.pdf)
  - [중소규모 DB 응용을 위한 소프트웨어 생명주기(SDLC for small and medium DB applications)](https://web.archive.org/web/20070423113916/http://www.elucidata.com/refs/sdlc.pdf)

[분류:소프트웨어 공학](https://ko.wikipedia.org/wiki/분류:소프트웨어_공학 "wikilink") [분류:소프트웨어 프로젝트 관리](https://ko.wikipedia.org/wiki/분류:소프트웨어_프로젝트_관리 "wikilink")