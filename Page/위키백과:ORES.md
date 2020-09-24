> This article is converted from Wikipedia: [위키백과:ORES](https://ko.wikipedia.org/wiki/위키백과:ORES).


[right](https://ko.wikipedia.org/wiki/파일:Objective_Revision_Evaluation_Service_logo.svg "wikilink")

**ORES**는 Objective Revision Evaluation Service 의 약자로써, 위키백과 위키에서 사용할 수 있는 웹 서비스와 API 서비스를 제공합니다. 이러한 도구를 통해 문서 훼손을 빠르게 발견하고 제거할 수 있도록 돕습니다. ORES는 2019년 4월 기준으로 "문서의 질"과 "편집의 질"을 측정합니다.

ORES는 [백엔드 소프트웨어이며](https://ko.wikipedia.org/wiki/빽단 "wikilink"), ORES 데이터를 위키백과에서 직접 사용하려면 별도의 확장기능을 설치해야 합니다.

다음 기능에서 ORES를 사용할 수 있습니다.

  - 자바스크립트 기반 새로운 최근 바뀜/주시문서 목록

## 편집의 질

[ORES_edit_quality_flow.svg](https://ko.wikipedia.org/wiki/File:ORES_edit_quality_flow.svg "fig:ORES_edit_quality_flow.svg")

위키백과의 "열린 백과사전"으로써의 가장 큰 난제는 문제가 될 수 있는 편집을 검토하는 것입니다. 선의의 사용자가 의도치 않게 위키백과에 해를 끼치는 경우를 감지해 도와줘야 할 수도 있습니다.

이러한 데이터는 최근 바뀜 데이터를 필터링함으로써 최근 바뀜을 검토하는 사용자의 작업을 편하게 하기 위해 사용됩니다. 문서 편집 품질은 기본 지원과 고급 기능 지원이 있습니다.

### 기본 지원

문제가 있는 편집은 [되돌려지고](../Page/도움말:되돌리기.md "wikilink"), 문제가 없는 편집은 되돌려지지 않으리라는 추측을 기반으로, 위키에서 되돌려진 편집을 가져와 분석할 수 있습니다. 이 방식은 쉽고 빠르게 처리할 수 있지만, 모든 문서의 되돌림이 문서 훼손 때문은 아니므로 이 기능으로 감지할 수 있는 문서 훼손에는 제한이 있습니다. 이러한 문제를 해결하기 위해, ORES는 되돌려진 판의 내용에서 "나쁜 말"을 찾습니다.

  - `reverted`: 문서가 결과적으로 추후에 되돌려질지 추측합니다

### 고급 기능 지원

기본 지원의 추측 없이, 위키백과 편집자가 이 편집이 문서 훼손이고, 이 편집은 선의의 기여라는 것을 직접 평가할 수 있습니다. 이러한 작업은 공동체가 시간을 투자해 분류를 해야 하지만, 단순한 추측보다 훨씬 정확하고 편집의 품질에 관한 예측을 좀 더 잘 해낼 수 있습니다. 대부분의 도구는 고급 기능이 지원되어야 동작합니다.

  - `damaging`: 편집이 유해한지 무해한지 추측합니다.
  - `goodfaith`: 편집이 선의로 이루어졌는지 추측합니다.

## 같이 보기

  - [위키백과:사랑방 (기술)/2017년 3월\#ORES 도입](https://ko.wikipedia.org/wiki/위키백과:사랑방_\(기술\)/2017년_3월#ORES_도입 "wikilink")
  - [위키백과:사랑방 (기술)/2017년 4월\#ORES 편집 품질 캠페인](https://ko.wikipedia.org/wiki/위키백과:사랑방_\(기술\)/2017년_4월#ORES_편집_품질_캠페인 "wikilink")
      - [업데이트 1](https://ko.wikipedia.org/wiki/위키백과:사랑방_\(기술\)/2017년_5월#ORES_업데이트_no.1 "wikilink")
      - [업데이트 2](https://ko.wikipedia.org/wiki/위키백과:사랑방_\(기술\)/2017년_10월#ORES_업데이트_no.2 "wikilink")
  - [편집 품질 측정하기](https://labels.wmflabs.org/ui/kowiki/)
      - [편집 품질 진행도](https://labels.wmflabs.org/stats/kowiki/)