> This article is converted from Wikipedia: [OpenEHR](https://ko.wikipedia.org/wiki/OpenEHR).


**openEHR**은 [건강 정보학의](https://ko.wikipedia.org/wiki/건강_정보학 "wikilink") [개방 표준](https://ko.wikipedia.org/wiki/개방_표준 "wikilink") 명세서이며, [전자건강기록](https://ko.wikipedia.org/wiki/전자건강기록 "wikilink")(Electronic Health Records, EHRs) 내의 건강 데이터의 관리와 저장, 검색, 교환에 대해 기술하고 있다. openEHR에서 한 개인에 대한 모든 건강 데이터는 "하나의 인생(lifetime)"과 벤더 중립적, 개인 중심적 EHR에 저장된다. openEHR 명세서는 EHR Extract 명세서\[1\]를 포함하지만 [EN 13606과](https://ko.wikipedia.org/wiki/EN_13606 "wikilink") [HL7](https://ko.wikipedia.org/wiki/HL7 "wikilink")와 같은 다른 표준들이 EHR 시스템들 간의 데이터의 교환에 중점을 두는 것과는 달리 일차적인 관심사는 아니다.

openEHR 명세서는 openEHR EHR의 오픈 연구 및 개발, 구현를 지원하는 비영리 재단인, openEHR Foundation에서 관리한다. 명세서들은 15년간의 유럽과 호주의 EHR과 새로운 패더다임 연구와 개발 성과에 기반하고 있으며, 컨텐츠의 명세을 위한 아카타입 방법론\[2\]\[3\]으로 알려진 것을 포함하고 있다.

openEHR 명세서\[4\]는 EHR, 인적정보(demographic), 임상 워크플로우(clinical workflow), [아키타입을](https://ko.wikipedia.org/wiki/archetype_\(information_science\) "wikilink") 위한 정모 모델과 서비스 모델들을 포함한다. 이것들은 의료-법률적으로 완전하게 배포되고 버전관리된 EHR 인프라스트럭처의 기반이 되도록 설계되었다.

## 아키텍처

[섬네일](https://ko.wikipedia.org/wiki/파일:Openehr_block_diagram.png "wikilink") 전체 openEHR 명세서의 아키텍처는 다음의 핵심 성분으로 구성되어 있다.:

  - ('참조모델'로 알려진) 정보 모델들(information models);
  - 아키타입 형식(archetype formalism);
  - 이식가능한 아키타입 질의 언어(archetype query language);
  - 서비스 모델들 / APIs.

첫번째 두 개를 이용하여 '아키타입'과 '템플릿'의 개발을 하는데, 이것은 임상 및 그와 관련된 컨텐츠의 정규모델이며 기반이 되는 기본 명세서들보다 더 많이 그 자체로 실질적인 하나의 표준의 층을 구성한다. 질의언어는 질의가 물리적인 데이터베이스 스카마타보다는 아키타입 기반으로 만들어질 수 있도록 하여, 질의를 물리적 영구층의 상세내역과 분리한다. 서비스 모델은 EHR 서비스와 Demographics 서비스를 포함하는 핵심 백엔드 서비스에 대한 액세스를 정의하고, 아키타입 패스(archetype paths)에 기반을 둔 경량의 REST 기반의 API는 애플리케이션 액세스를 위해 사용된다.

openEHR 아키텍처 개요는 아키텍처와 상세한 명세에 대한 요약을 제공한다.\[5\]

## 참조모델

openEHR 명세서의 중심 부분은 '참조모델'\[6\]로 알려진 정보모델 세트이다. 이 모델들은 openEHR 시스템의 기본 정보모델을 구성하며 불변의 전자건강기록(EHR), EHR Extract, Demographics model의 의미론 뿐만 아니라 데이터 타입 및 데이터 스트럭처, 식별자, 유용한 디자인 패턴 등의 지원을 정의한다.

EHR component의 몇몇 핵심 클래스들는 OBSERVATION와 EVALUATION, INSTRUCTION, ACTION, ADMIN_ENTRY를 포함하는 ENTRY 클래스들 그리고 의약품 오더, 외과와 기타 치료를 포함하는 중재술의 생애주기에 대한 표준 모델을 정의하는 상태 기계인 Instruction State Machine이다.

## 아키타입과 멀티레벨 모델링

openEHR 프레임워크 내의 핵심적인 혁신은 ("참조모델"로 알려진) [information model에서](https://ko.wikipedia.org/wiki/information_model "wikilink") 모든 임상 정보의 명세를 배제하고, 대신에 참조모델을 따라 개발된 시스템에서 실행시 바로 소비될 수 있고 임상의와 환자가 기록할 필요가 있는 컨텐츠의 정의를 표현하는 강력한 수단을 제공하는 것이다. 이는 대규모로 성장하면서 지속적으로 변하는 건강 정보 타입들의 일반적인 문제를 규모있게 처리할 필요성이 있다는 것에 따라 정당화된다.\[7\]

임상 컨텐츠는 정보모델 밖에 존재하는 두 가지 타입의 산출물로 구체화된다. 첫번째는 "[archetypes](https://ko.wikipedia.org/wiki/Archetype_\(information_science\) "wikilink")(아키타입)이라는 것으로, 재사용가능한 데이터 포인트와 데이터 그룹 정의, 즉, 다양한 문맥에서 재사용될 수 있는 컨텐츠 아이템을 정규적으로 정의하는 공간을 제공하며, 전형적인 예는 "전신동맥혈압 측정(systemic arterial blood pressure measurement)"과 "혈청 나트륨(serum sodium)"이다. 이러한 많은 데이터 포인트는, 알레르기 반응을 기록하는 데이터 아이템 그룹 또는 간기능검사결과에서의 분석물(analyte)같은 논리적 그룹에서 발생한다. 몇몇 아키타입은 비록 일반적으로는 10-20개 이지만 50개 정도와 같은 다양한 데이터 포인트를 갖는다. 아키타입의 집합은, 컨텐츠가 공동으로 설계되고 검토되고 발표되는 "거버넌스 단위"로 기능하는 각각의 아키타입을 가지는 재사용가능한 도메인 컨텐츠 정의의 "라이브러리"로 이해될 수 있다.

두번째 종류의 산출물은 openEHR에서 "template(템플릿)"로 알려져있으며, 환자퇴원요약 또는 영상의학보고서를 구성하는 데이터 아이템같은 유즈 케이스에 특징적인 데이터 세트를 논리적으로 표현하는데 사용된다.\[8\] 템플릿은 수많은 아키타입들로부터 관련된 아이템을 참조하여 구성된다. 템플릿은 각 아키타입에서 단지 1-2개의 데이터 포인트 또는 그룹만을 필요로할 수 있다. 기술적인 표현 면에서 openEHR 템플릿은 아카티입으로부터 구성되기 때문에 아키타입의 의미론을 위반할 수 없다. 템플릿은 거의 항상 로컬에서 사용하기위해 소프트웨어 개발자와 임상 분석가에 의해 개발된다. 템플릿은 전형적으로 [GUI](https://ko.wikipedia.org/wiki/GUI "wikilink") 화면형식, 메시지 정의, 문서정의 용도로 정의되는데, 그자체로 "운영(operational)" 컨텐츠 정의와 일치한다.

정보모델에 대한 두 단계 모델의 정당성은 만약 데이터 세트 정의가 라이브러리의 기정의된 데이터 포인트로 구성되어 있다면, 모든 기록된 데이터는 (즉, 템플릿 인스턴스) 궁극적으로 표준 컨텐츠 정의의 인스턴스가 될 것이라는 것이다. 이것은 작업에 대한 표준화된 질의를 위한 기반을 제공한다. 아키타입 "라이브러리" 레벨이 없이는, 모든 데이터 세트가 (즉. 운영 컨텐츠 덩어리) 유일하게 정의되고 표준방식으로 질의하는 것은 어렵다.

따라서 openEHR은 AQL(Archetype Querying Language).\[9\]로 알려진 아키타입 기반의 질의방식을 정의하고 있다.

특히 openEHR은 공유치료계획(shared care plan)을 모델링하는데 사용되어왔으며, 아키타입은 공유치료계획의 개념을 수용하도록 설계되어왔다.\[10\]

개개인의 건강기록은 내용이 상당히 다를 수 있지만, openEHR 데이터 인스턴스 내의 핵심정보는 항상 아키타입으로 정리된다. 이것이 작동하는 방식은 고수준의 재사용할 수 있는, 심지어 어떤 경우에는 보편적인, 방법으로 임상정보를 표현하는 아키타입을 생성하는 것이다.\[11\]

### 아키타입 형식

openEHR 아키타입은 openEHR 공개 명세인 "Archetype Definition Language(ADL, 아키타입정의언어)"로 표현된다. 두 가지 버전이 사용가능한데, ADL 1.4,\[12\]와 ADL 2\[13\]로, 새로운 릴리즈가 개선된 부분 중에 specialisation(상세화) 그리고 redefinition(재정의), annotations(어노테이션)를 더 잘 지원한다.\[14\] ADL 1.4 릴리즈와 "객체모델"에 해당하는 Archetype Object Model (AOM, 아키타입객체모델)은 CEN과 ISO의 "Archetype Definition Language" 표준 ([ISO standard 13606-2](https://ko.wikipedia.org/wiki/ISO/TC_215 "wikilink"))의 근간이 된다.

템플릿은 파일 확장자인 ".oet"로 알려진, 역사적으로 단순하면서 실질적으로 산업계에서 개발한 XML 형식으로 개발되어왔다.\[15\] ADL 2는 ADL 언어의 확장을 사용하여 문제없이 아카타입과 함께 템플릿을 표현하는 방식을 정의한다.\[16\]

### 아키타입의 품질보증

아키타입을 개발하기위한 다양한 원칙들을 찾아내왔다.\[17\] 예를 들어, openEHR 아키타입의 어떤 세트들은 상호배타적과 같은 수많은 공리를 따르도록 품질관리될 필요가 있다. 아키타입은 소프트웨어 구현과 기반구조에 독립적으로, 임상의들이 해당 분야의 실제 요구사항을 만족시킨다는 것을 보장하기위해, 임상의 그룹 하에서 관리될 수 있다. 아키타입은 임상지식의 명세가 지속적으로 발전라고 개발될 수 있도록 설게된다. openEHR 내에서 표현되는 정보 디자인을 구현하는데 발생하는 문제는 실제 시스템 제한사항과 정보 디자인 간의 조율을 어느 정도로 하는가에 집중된다.

[Electronic health record](https://ko.wikipedia.org/wiki/Electronic_health_record "wikilink") 분야에는 [HL7](https://ko.wikipedia.org/wiki/HL7 "wikilink") \[\[HL7_V3\]와_\[\[SNMED_CT|HL7 V3\]와 [SNMED CT와](https://ko.wikipedia.org/wiki/SNMED_CT "wikilink") 같이 그들의 범위가 겹치서 관리가 어려운 많은 기존의 수많은 정보모델이 있다. openEHR 접근방식은 단독으로 사용되지 않는 한, 조율을 해야하는 문제에 직면하게된다.

## 국제 협력

openEHR 접근방식에 따라서, 공유되고 관리되는 아키타입의 사용은 기술과 기관 그리고 문화적 문맥에 관계없이 세계적으로 openEHR 건강데이터가 일관성을 가지고 작성되고 보여질 수 있다는 것을 보증할 것이다. 이러한 접근방식은 또한 새로운 아키타입이 임상기록유지하기 위한 미래의 필요성을 만족시키도록 정의될 수 있다면 어떠한 EHR에서 사용되는 실제 데이터 모델이라도 유연하게 적용될 수 있다는 것을 의미한다. 최근 호주에서의 작업은 어떻게 아키타입과 템플릿이 openEHR 건강기록시스템 내의 과거 건강기록과 메시지 데이터의 사용을 용이하게 하고 표준화된 메시지와 CDA 문서를 출력하는데 사용될 수 있는 보여준다.

국제수준에서 디자인과 거버넌스의 형식에 대한 합의를 이루기위한 전망은 다양한 의료-법률적 환경에서 문화적 차이 그리고 [reference clinical terminology](https://ko.wikipedia.org/wiki/SNOMED_CT "wikilink")(참조임상용어체계)가 어느정도까지 통합되어야 하는가와 같은 기술적인 차이까지 영향과 함께 이론적인 수준에 머물러 있다.

openEHR 프레임워크는 Electronic Health Record Communication Standard ([ISO 13606](https://ko.wikipedia.org/wiki/ISO_13606 "wikilink"))와 일치하며, Archetype Object Model 2 (AOM2)는 공식적으로 ISO TC 215에 의해 ISO 13606:2 2017년 개정판의 초기명세로 받아들여졌다.

## 전세계적 도입

openEHR 아키타입은 [National e-Health Transition Authority of Australia](http://www.nehta.gov.au/) 그리고 the UK NHS [Health and Social Care Information Centre (HSCIC)](http://www.hscic.gov.uk/home), the Norwegian [Nasjonal IKT organisation](https://web.archive.org/web/20160629135353/http://www.nasjonalikt.no/no/), Slovenian Ministry of Health에서 사용되고 있다.

openEHR은 브라질에서 표준화된 EHR를 기반으로 선택되었다[1](http://bvsms.saude.gov.br/bvs/saudelegis/gm/2011/prt2073_31_08_2011.html).

[openEHR Industry Partners](https://web.archive.org/web/20171203021532/http://www2.openehr.org/industry_partners/index)이 개발한 제품을 포함하여 전세계적으로 상업적인 솔루션으로 사용되기 시작되었다.

## Clinical Knowledge Manager (CKM)

openEHR 모델링 접근방식의 산출물 중에 하나는 건강데이터를 표현하는 아카타입, 템플릿, 용어체계 서브세트의 오픈 개발이다. openEHR의 개방성때문에, 이러한 구조체는 건강정보시스템에서 사용되거나 구현되는 것이 공개적으로 가능하다. 커뮤니티 사용자들은 Clinical Knowledge Manager (CKM)로 알려진 협업저장소 내의 이러한 구조체들을 공유, 토론, 승인할 수 있다. openEHR CKM을 사용하는 곳들 중 일부는 다음과 같다.

  - [openEHR Clinical Knowledge Manager](http://openehr.org/knowledge)
  - [NEHTA Clinical Knowledge Manager](https://web.archive.org/web/20180928234015/http://dcm.nehta.org.au/ckm/)
  - [UK Clinical Knowledge Manager](https://web.archive.org/web/20161217063848/http://www.clinicalmodels.org.uk/ckm/)
  - [Norwegian National ICT Clinical Knowledge Manager](http://arketyper.no/ckm/)
  - [Slovenian MoH Clinical Knowledge Manager](http://ukz.ezdrav.si/ckm/OKM_sl.html)

## 같이 볼 것

  - [Archetype (information science)](https://ko.wikipedia.org/wiki/Archetype_\(information_science\) "wikilink")
  - [European Institute for Health Records](https://ko.wikipedia.org/wiki/European_Institute_for_Health_Records "wikilink")
  - [Electronic Health Record Communication](https://ko.wikipedia.org/wiki/EN_13606 "wikilink") ([ISO](https://ko.wikipedia.org/wiki/International_Organization_for_Standardization "wikilink")/[CEN](https://ko.wikipedia.org/wiki/European_Committee_for_Standardization "wikilink") EN 13606 - EHRcom)
  - [Health Level 7](https://ko.wikipedia.org/wiki/Health_Level_7 "wikilink")
  - [Health Informatics Service Architecture](https://ko.wikipedia.org/wiki/Health_Informatics_Service_Architecture "wikilink") (HISA)
  - [HIPAA](https://ko.wikipedia.org/wiki/HIPAA "wikilink")
  - [ProRec](https://ko.wikipedia.org/wiki/ProRec "wikilink")
  - [SNOMED CT](https://ko.wikipedia.org/wiki/SNOMED_CT "wikilink")

## 참고문헌

## 외부 링크

  - [openEHR Korea 웹사이트](http://www.openEHR.kr)
  - [openEHR Foundation website](http://www.openEHR.org)
  - [openEHR specifications](http://www.openehr.org/programs/specification/workingbaseline)
  - [openEHR 2015 white paper](http://www.openehr.org/resources/white_paper_docs/openEHR_vendor_independent_platform.pdf)

[분류:1989년 설립](https://ko.wikipedia.org/wiki/분류:1989년_설립 "wikilink") [분류:재단법인](https://ko.wikipedia.org/wiki/분류:재단법인 "wikilink")

1.
2.   (PDF)
3.   (PDF)
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.  (PDF)