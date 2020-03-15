> This article is converted from Wikipedia: [AUTOSAR](https://ko.wikipedia.org/wiki/AUTOSAR).


**AUTOSAR** (AUTomotive Open System ARchitecture)는 2003년에 만들어진 자동차관련 분야의 세계적인 개발 파트너쉽이다\[1\]. 자동차 ECU의 개방형 표준 소프트웨어 구조를 개발하고 설립하는데 목적을 두고있다. 구체적인 목표로는 다양한 차량 및 플랫폼 변형, 소프트웨어 이전 가능성, 가용성 및 안전 요구 사항 고려, 다양한 파트너 간의 협력, 천연 자원의 지속 가능한 활용 및 전체 "[제품 수명주기](https://ko.wikipedia.org/wiki/제품_수명_주기_관리 "wikilink")"에 걸친 유지 관리 가능성에 대한 확장 성이 포함된다.

## 역사

AUTOSAR 개발 파트너쉽은 2003년 7월에 열린 산업 표준 자동차 E/E architecture 구조를 만들고 발전시키기 위해 [BMW](../Page/BMW.md "wikilink"), [보쉬](../Page/로베르트_보쉬.md "wikilink"), [콘티넨탈](https://ko.wikipedia.org/wiki/콘티넨탈_AG "wikilink"), [다임러](https://ko.wikipedia.org/wiki/다임러_AG "wikilink"), 지멘스 VDO, 그리고 [폭스바겐](https://ko.wikipedia.org/wiki/폭스바겐 "wikilink")에 의해 설립되었다. [포드](https://ko.wikipedia.org/wiki/포드_모터_컴퍼니 "wikilink") 자동차가 2003년 11월에 핵심 파트너(Core Partner)로 가입했고, 그 해 12월에는 [푸조](../Page/푸조.md "wikilink")와 [토요타가](https://ko.wikipedia.org/wiki/토요타_자동차 "wikilink") 추가로 가입했다. 다음 해 11월에는 [GM이](https://ko.wikipedia.org/wiki/제너럴_모터스 "wikilink") 핵심 파트너에 합류했고, 2008년 2월 지멘스 VDO가 콘티넨탈에 인수된 후 이는 자체 핵심 파트너에서 제외되었다.

2003년부터 AUTOSAR는 클래식 플랫폼(Classic Platform)을 위한 표준 자동차 소프트웨어 구조로써 4개의 릴리즈(Release)를 제공해 왔으며, 1개의 승인 테스트 릴리즈(Acceptance Tests Release)를 공개했다.  AUTOSAR 클래식 플랫폼의 작업은 다음과 같이 세 단계로 나눌 수 있다.

  - Phase I (2004-2006): 표준을 위한 기본 개발 (Releases 1.0, 2.0 and 2.1)
  - Phase II (2007-2009): 구조와 방법론 측면에서의 표준 확장(Releases 3.0, 3.1 and 4.0)
  - Phase III (2010-2013): 유지 보수 및 개선(Releases 3.2, 4.1 and 4.2)

2013 년 AUTOSAR 컨소시엄은 클래식 플랫폼이 표준을 유지하고 선택된 개선 사항 (릴리스 R4.2 및 승인 테스트 릴리스 1.0 포함)을 제공하기 위해 지속적인 작업 모드를 시작했다.

2016년에는 어뎁티브 플랫폼(Adaptive Platform)을 개발하기 시작했다. 그의 첫 번째 릴리스는 2017년 초반에 발표되었고, 그 해 10월에 두번째 릴리즈인 17-10이, 그리고 2018년 3월에 18-03 릴리즈가 발표되었다. 최근의 목표는 2018 년 10 월AUTOSAR 클래식, 어뎁티브 및 기반(Foundation)표준을 어우르는 릴리즈의 출시를 위해 주요 개발 활동을 마무리하고 그것을  포함시키는 것이다.\[2\]

## 개념과 목표

AUTOSAR는 기본 소프트웨어 모듈을 설명하고 애플리케이션 인터페이스를 정의하며 표준화 된 교환 형식을 기반으로 일반적인 개발 방법론을 구축하는 일련의 사양서 (specifications)를 제공한다. AUTOSAR 계층화 된 소프트웨어 아키텍처가 제공하는 기본 소프트웨어 모듈은 각기 다른 제조업체(OEMs, Manufacturers)의 자동차 및 여러 공급업체(Suppliers, Tiers)의 전자 부품에 사용 될 수 있는데, 이를 통해 연구 개발 비용을 줄이고 점차 확대되고 있는 자동차 및 전자 소프트웨어 구조의 복잡성에 대비 하자는 것이다. AUTOSAR는 이러한 기본 지침에 바탕을 두고 성능, 안전성 및 환경 친화성을 개선하고 차량의 서비스 수명 동안 소프트웨어 및 하드웨어의 교환 및 업데이트를 용이하게하는 혁신적인 전자 시스템의 길을 열어 줄 수 있도록 고안되었다. 다가오는 기술에 대비하고 품질에 대한 타협없이 비용 효율성을 향상시키는 것을 목표로한다.

## 소프트웨어 구조

AUTOSAR는 3개의 계층의 구조를 사용한다.

  - 기본 소프트웨어: 상위 소프트웨어 계층의 기능적 부분을 실행하는 데 필요한 서비스를 제공하는 기능적 작업 자체가없는 표준화 된 소프트웨어 모듈
  - [런타임 환경](../Page/런타임.md "wikilink")(Runtime environment/RTE) : 응용 프로그램 소프트웨어 구성 요소 간 및 기본 소프트웨어와 응용 프로그램 간의 ECU 내부 및 내부 정보 교환을 위해 네트워크 토폴로지에서 추출한 미들웨어
  - 응용 프로그램 계층 : 런타임 환경과 상호 작용하는 응용 프로그램 소프트웨어 구성 요소

## AUTOSAR 방법론

  - 시스템 구성 설명에는 모든 시스템 정보와 서로 다른 ECU간에 합의 된 정보 (예 : 버스 신호bus signals 정의)가 포함된다.
  - [ECU](https://ko.wikipedia.org/wiki/ECU "wikilink") 추출 : 특정 ECU (예 : 특정 ECU가 액세스 할 수있는 신호)에 필요한 시스템 구성 설명의 정보를 포함한다.
  - ECU 구성 설명 (ECU Configuration Description) : 특정 ECU에 국한되는 모든 기본 소프트웨어 구성 정보를 포함한다. 이 정보를 사용하여 실행 가능한 소프트웨어, 기본 소프트웨어 모듈의 코드, 그리고 이를 통한 소프트웨어 구성 요소의 코드를 생성할 수 있다.

## 클래식 플랫폼 Classic Platform\[3\]

AUTOSAR 클래식 플랫폼은 [OSEK](https://ko.wikipedia.org/wiki/OSEK/VDX "wikilink") 기반의 임베디드 실시간  ECU 표준이다. 주요 결과물로는 사양서(Specifications)가 있다.

AUTOSAR 클래식 플랫폼의 구조는 응용 프로그램, 런타임 환경 (RTE) 및 기본 소프트웨어 (BSW)와 같이 마이크로 컨트롤러에서 실행되는 세 가지 소프트웨어 계층사이를 가장 높은 추상 수준으로 구별한다. 응용 소프트웨어 계층은 대부분 하드웨어로부터 독립적이다. 소프트웨어 구성 요소 간의 통신과 BSW에 대한 액세스는 응용 프로그램의 전체 인터페이스를 나타내는 RTE를 통해 발생한다.

BSW는 세 가지 주요 계층과 복잡한 드라이버로 나뉜다.

  - 서비스
  - ECU (Electronic Control Unit) 추상화
  - 마이크로 컨트롤러 추상화

서비스는 시스템, 메모리 및 통신 서비스를 위한 인프라를 대표하는 기능 그룹으로 더 나뉜다.

클래식 플랫폼의 꼭 필요한 개념중의 하나는 가상 기능 버스(virtual functional bus:VFB)이다. 이 가상 기능 버스(VFB)는 특정 ECU에 아직 배치되지 않은 인프라 스트럭처에서 어플리케이션을 분리하는 추상적인 RTE 의 한 세트이다. 이는 전용 포트를 통해 통신하므로 응용 프로그램 소프트웨어의 통신 인터페이스는 이러한 포트ports에 매핑되어야한다. VFB는 개별 ECU 내에서와 ECU들간의 통신을 처리한다. 응용 관점에서 하위 수준의 기술이나 종속성에 대한 자세한 지식을 필요로 하지 않는다. 이는 하드웨어 독립적 개발 및 응용 프로그램 소프트웨어 사용을 지원한다.

또한 클래식 플랫폼은 프랑카 [인터페이스 정의 언어](https://ko.wikipedia.org/wiki/인터페이스_정의_언어 "wikilink")(Franca interface description language:IDL)를 사용하여 GENIVI와 같은 비 AUTOSAR 시스템과도 결합할 수 있다.

## 어뎁티브 플랫폼 Adaptive Platform\[4\]

새로운 유스 케이스는 어뎁티브 플랫폼의 개발을 필요로 했다. 한 가지 중요한 예로는 운전자가 일시적으로 및 /또는 부분적으로 차량 주행에 대한 책임을 전하는 맥락에서의 고도로 자동화 된 운전이다. 이는 교통 표지나 신호등과 같은 교통 인프라스트럭쳐, 최신 교통 정보나 지도에 엑세스 하기 위한클라우드 서버, 또는 마이크로프로세서의 사용 및 병렬 처리를 위한 고성능 컴퓨터 하드웨어의 사용을 필요로 한다(예: GPUs).

또한 Car-2-X 애플리케이션은 차량 및 외부 시스템과의 상호 작용을 필요로한다. 이는 시스템이 안전한 온보드(on-board) 통신, 교차 영역 컴퓨팅 플랫폼 (cross-domain computing platform) 지원, 스마트 폰 통합, 비 AUTOSAR 시스템 통합 등을 제공해야 함을 의미한다. 더불어 클라우드 기반 서비스에는 보안 클라우드 상호 작용 및 비상 차량 선점과 같은 보안을위한 전용 수단이 필요하다. 이 서비스는  원격 진단, 무선 업데이트 (over the air: OTA), 수리 및 교환 처리와 같은 원격 및 분산 서비스를 가능하게한다.

다양한 고객 애플리케이션 전개를 지원하고 하이앤드(high-end) 컴퓨팅 파워를 필요로하는 애플리케이션을 위한 환경을 제공하기 위해서 AUTOSAR 는 근래에 어뎁티브 플랫폼(Adaptive Platform)을 표준화 시키고 있다. 그의 핵심은 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 표준에 기반한 운영 체제이다. IEEE1003.13 (namely PSE51)에 따르면 이 운영체제는 POSIX의 서브셋을 거쳐 어플리케이션을 통해 사용될 수 있다.  

어뎁티브 플랫폼은 서비스와 애플리케이션 프로그래밍 인터페이스 [application programming interfaces (APIs)와](../Page/API.md "wikilink") 같은 2가지 타입의 인터페이스가 가능하다. 이 플랫폼은 기능 클러스터를 포함하는데, 이는 서비스와 어뎁티브 플랫폼을 기반으로 그룹화된다.

기능 클러스터:

  - 어뎁디브 플랫폼의 어셈블리 기능들
  - 필요 사양서의 정의
  - 애플리케이션과 네트워크 관점으로 부터의 소트프웨어 플랫폼의 행동 묘사
  - 그러나 어뎁티브 플랫폼을 구현하는 아키텍처의 최종 SW 설계를 제한하지 않음

AUTOSAR 어뎁티브 플랫폼 기반의 기능 클러스터는 서비스가 차량내의 네트워크에 분산되는 동안 (가상)머신당 최소한 하나 이상의 인스턴스를 가져야한다.  

어뎁티브 플랫폼의 서비스는 다음을 포함한다:

  - 업데이트 및 구성 관리
  - 상태 관리
  - 네트워크 관리
  - 진단

AUTOSAR 어뎁티브 플랫폼에는 사양서와 코드가 모두 포함되어 있다. 클래식 플랫폼과 비교하여 AUTOSAR는 어뎁티브 플랫폼을 통해 유효성 검사주기를 단축하고 기본 개념을 설명하기위한 구현을 개발하고 있다. 이런 AUTOSAR의 기술 구현은 모든 파트너가 사용할 수 있다.

## 기반표준 Foundation\[5\]

기반을 만드는 표준 목적은 AUTOSAR 플랫폼 간의 상호 운용성을 강화하는 것이다. 이런 기반에는 공통 방법론과 함께AUTOSAR 플랫폼간에 공유되는 공통 요구 사항과 기술 사양서 (프로토콜의 예시)가 포함되어 있다.

## 승인 테스트 Acceptance Tests\[6\]

2014 년 AUTOSAR는 테스트에 드는 노력과 비용을 최소화하기 위해 승인 테스트(Acceptance Tests)를 도입했다. 이 승인 테스트의 사양(Specifications)은 각 플랫폼의 지정된 인터페이스를 사용하는 시스템 테스트 사양이다. 또한 이 테스트는 버스([Bus](../Page/버스_\(컴퓨팅\).md "wikilink"))의 특정 행동을 고려한다. 이것들은 특정 플랫폼 기능에 대한 블랙 박스 테스트 케이스로 볼 수 있다.  표준 승인 테스트의 사양서는 이러한 목표에 기여한다.

## 표준화된 응용 프로그램 인터페이스

제조업체(manufacturers)와 공급업체(suppliers) 사이의 기술 인터페이스의 표준화 및 다른 소프트웨어 계층(layers) 간의 인터페이스의 표준화는 AUTOSAR 기술 목표를 달성하는데  있어서 기초라고 볼 수 있다.

## 조직 과 멤버

AUTOSAR의 멤버십은 다섯가지로 분류된다. 파트너사들의 기여도는 이 멤버십의 유형에 따라 다르게 정의된다.

  - Core Partners 핵심 파트너
  - Premium Partners 프리미엄 파트너
  - Associate Partners 제휴 파트너
  - Development Partners 개발 파트너
  - Attendees 언텐디스:참석자

핵심 파트너는 설립 파트너인 BMW, Bosch, Continental, Daimler AG, Ford, General Motors, PSA Peugeot Citroën, Toyota ,Volkswagen을 포함한다. 이 회사들은 AUTOSAR 개발 파트너십의 조직, 관리 및 제어를 담당한다.  이 핵심 멤버들 사이에서, 이사회는 전반적인 전략과 로드맵을 정의한다. 운영위원회는 일상적으로 비 기술 운영과 파트너 가입, 홍보 및 계약 문제를 관리한다. 의장과 부의장은 9개월간의 임명기간동안 위와 같은 목표를 위해 운영위원회를 대표한다. 그리고 AUTOSAR의 공식 대변인은 외부와의 의사소통과 같은 대외적인 활동을 담당한당\[7\]

프리미엄 및 개발 파트너는 핵심 파트너가 수립 한 프로젝트 리더 팀이 조정하고 모니터링하는 업무 패키지에 기여한다\[8\]. 그리고 제휴 파트너는 AUTOSAR에서 이미 발표 한 표준 문서들을 사용한다\[9\]. 참석자(Attendees)는 현재 학술 협력 및 비상업적 프로젝트에 참여하고 있다\[10\].

2018년 2월 현재 200여개가 넘는 회사들이 AUTOSAR 개발 파트너쉽에 참여하고 있다.

## 사양서

  - AUTOSAR 4.0

<!-- end list -->

1.  메인
    1.  [AUTOSAR_TF_Glossary](https://web.archive.org/web/20120526103003/http://www.autosar.org/download/R4.0/AUTOSAR_TR_Glossary.pdf)
    2.  [AUTOSAR_RS_Main](https://web.archive.org/web/20120603154435/http://autosar.org/download/R4.0/AUTOSAR_RS_Main.pdf)
    3.  [AUTOSAR_RS_BSWAndRTEFeatures](https://web.archive.org/web/20120603154821/http://autosar.org/download/R4.0/AUTOSAR_RS_BSWAndRTEFeatures.pdf)
    4.  [AUTOSAR_EXP_VFB](https://web.archive.org/web/20120603155912/http://autosar.org/download/R4.0/AUTOSAR_EXP_VFB.pdf)
    5.  [ProjectObjectives](https://web.archive.org/web/20120603154545/http://autosar.org/download/R4.0/AUTOSAR_RS_ProjectObjectives.pdf)

## 각주

<references />

## 외부 링크

  - [AUTOSAR 공식 웹사이트](http://www.autosar.org)
  - [AUTOSAR 개발도구 공통기반](http://www.artop.org) [Artop](https://ko.wikipedia.org/wiki/Artop "wikilink")
  - [xing의 AUTOSAR 그룹](http://www.xing.com/net/autosar/) [xing](https://ko.wikipedia.org/wiki/xing "wikilink")
  - [일본 자동차 소프트웨어 공통기반 구조 ([JasPar](https://ko.wikipedia.org/wiki/JasPar "wikilink"))](https://web.archive.org/web/20130603020913/https://www.jaspar.jp/english/index_e.php) 공식 웹사이트
  - [AUTOSAR에 관하여](http://www.freescale.com/autosar) 프리스케일 반도체 AUTOSAR 홈페이지
  - [ETAS Gmbh 홈페이지](http://www.etas.com) AUTOSAR 개발 Tool 제공
  - [Elektrobit Automotive GmbH 홈페이지](http://www.elektrobit.com)
  - [한눈에 살펴보는 AUTOSAR](http://www.eb-tresos-blog.com/technologies/autosar/) EB사에서 제작한 비디오. AUTOSAR에 관한 간략한 소개
  - [AUTOSAR BSW Platform](http://www.comasso.org/) [COMASSO](https://ko.wikipedia.org/wiki/COMASSO "wikilink")
  - [AUTOSAR 프로젝트 파트너 Vector](https://kr.vector.com/vk_autosar_solutions_ko.html)

[분류:소프트웨어 구조](https://ko.wikipedia.org/wiki/분류:소프트웨어_구조 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.