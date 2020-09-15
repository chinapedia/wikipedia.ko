> This article is converted from Wikipedia: [XGrids](https://ko.wikipedia.org/wiki/XGrids).


***xGrids(영어 : Extensible Power Grid Management Platforms With Intelligence,*** 이하 통칭 xGrids) 또는 지능형전력망 플랫폼은 [SCADA](https://ko.wikipedia.org/wiki/SCADA "wikilink"), [ESS](https://ko.wikipedia.org/wiki/에너지_저장_시스템 "wikilink")(에너지 저장 시스템), DAS, [HVDC](../Page/초고압직류송전.md "wikilink"), WAMAC, 디지털 변전소, 신재생 에너지 등 다양한 전력시스템들을 연계하고, ICT 기반으로 정보를 수집, 전력망을 통합·운영하는 [한국전력공사](https://ko.wikipedia.org/wiki/한국전력공사 "wikilink")(영어:[KEPCO](https://ko.wikipedia.org/wiki/KEPCO "wikilink"))의 전력 플랫폼이다.\[1\]

## 개발배경

스마트그리드에 대한 전반적인 관심과 확대를 넓히려는 대한민국 정부의 관심과 노력의 흐름에 맞춰 2013년 한국전력공사도 슬로건을 "Clean & Efficient Smart Energy Creator"로 바꾸며 새로운 정부 정책산업과 글로벌 에너지 산업 흐름에 맞췄다. xGrids는 2011년 산업통산자원부(전력진흥과)에서 제정된 지능형전력망의 구축 및 이용촉진에 관한 법률(*약칭:지능형전력망법*)\[2\]에 법적근거를 두고 개발을 시작했다. 정부는 5년을 주기로 계획을 발표하며 현재 2차 계획까지 발표된 상태이다.

### \- 제 1차 지능형 전력망 기본계획\[2012년 7월\]

전력망 신뢰도 향상을 위하여 차세대 감시제어시스템, 스마트 배전망 등 구현 로드맵 설정.\[3\]

### \- 제 2차 지능형 전력망 기본계획\[2018년 7월\]

송전ㆍ배전망에 구축된 다양한 전력시스템들을 연계하고, ICT 기반으로 정보를 수집, 전력망을 통합ㆍ운영하는 플랫폼(<small>*스마트그리드 플랫폼 구축(xGrids)*</small>) 개발.\[4\]

## 개발과정

xGrids(지능형전력망 플랫폼)는 차세대 SCADA 시스템 프로젝트\[5\]를 기반으로 시작됐다.

### \- 차세대 SCADA시스템 프로젝트

2005년 전체 전력망 단위의 감시, 제어를 위한 국제 표준(IEC 61790)이 제정됐다. 대한민국 정부는 본격적으로 스마트그리드를 촉진하기 위한 법률를 2011년 제정하며 변화를 주문하였고, 같은 해 ICT와 전력 그리드를 융합하는 지능형 전력 그리드 관련 종합 계획을 마련했다. 정부의 계획에 맞추는 과정에서 많은 문제가 발생했고, 해결해야할 문제가 67가지(예를 들자면 서버)가 발생했다. 2011년 시범사업을 진행했지만 실패했고, 2013년 제로 베이스에서부터 시작해 2014년 7월 총 17개의 하위 프로젝트로 구성된 차세대 스카다 로드맵 구축하여 2019년 현재 한국전력공사의 SCADA 시스템을 완성했다.\[6\]

### \- 차세대 지능형 전력망(xGrids)

한국전력공사는 송변전 및 배전망은 하나로 동작하나, 추진요소는 개별 구축·운전되어 실시간 통합운영에 한계를 느꼈다. 차세대 SCADA시스템 프로젝트를 기반으로 다양한 전력시스템을 연계·해석하여 이전보다 전력망을 안정적이고 효율적으로 운영하기 위해 전력망 통합운영 플랫폼을 구축하고, 관련 앱(Application) S/W를 개발하기 위해 연계 사업을 진행 중이다.\[7\]

## 상표권

  - 상표명 : Intelligent Power Grid Platforms xGrids\[8\]

<!-- end list -->

  - 출원일자 : 2015년 12월 01일

<!-- end list -->

  - 공고일자 : 2016년 05월 09일\[9\]

## 플랫폼 종류

### \- xGrids SCADA(지능형스카다)

xGrids SCADA는 '차세대 SCADA 시스템 프로젝트'를 기반으로 2014년부터 시작하여 2019년에 프로젝트를 완성했다. 유연한(확장가능한) 지능형 SCADA시스템 구조를 개발했다. SCADA S/W는 Application 계층, Middle-Ware계층, SCADA Core계층으로 구분해 계층 간 독립성과 무결성을 확립하고, 모듈형 개발방식인 CDB를 채택했다. 기존 SCADA시스템 구조는 Process 와 업무(Application)이 상호 중첩된 구조로 새로운 업무의가 개발될 경우 Process의 변경 또는 영향이 발생하였다. 하지만 xGrids SCADA(지능형스카다)는 이를 개선하기 위하여 업무(Application)와 Process를 엄격히 구분하고 중간에 Middle ware 계층을 두었다. 그리고 이를 통해 지능형 Application의 개발하여, 현재 우리가 스마트폰에 다양한 App.을 설치해 사용하는 것처럼 SCADA 상에서 다양한 App.을 사용할수 있도록 구축할 예정이다.\[10\]

### \- xGrids Renewable(재생에너지 감시·제어시스템)

실시간 재생에너지 상태감시 및 출력 제어를 통해 전기 품질을 유지하고, 정전예방 등 안정적인 전력계통 운영기반 마련을 위해 2019년 5월 전남지역에 재생에너지 감시·제어시스템(xGrids Renewable)을 시범 구축했다. 송변전 계통운영시스템(지능형 SCADA)과 배전 지능화 시스템(DAS) 간 정보공유 연계를 통해 일반 배전선로(부하고객과 발전고객 혼재)에 접속돼 있는 소규모 재생에너지와 전용 배전선로에 접속돼 있는 중소규모 재생에너지의 감시 및 제어정보를 통합할 계획이다. 앞으로 이를 확대해 154kV 이상 재생에너지의 감시 및 제어를 담당하고 있는 전력거래소와 정보공유를 통해 ‘중앙관제센터-계통운영센터-급전분소(배전센터)’ 로 이어지는 현재 전력계통 운영체계를 기반으로 전국 재생에너지의 계층적 운영체계를 구현할 계획이다.\[11\]

***- 이외 플랫폼 추가 구축예정(디지털변전소 정보 전송장치 등)***\[12\]

## 수상경력

  - ***2016 CIO Award*** - 한국전력 수상 \[**차세대 SCADA시스템 프로젝트**\]\[13\]

→ **수상 배경**: 100만개의 전력설비가 생성하는 Big Data(국내 최대 금융시스템에서 실시간 처리하는 데이타량의 50배가 넘는 규모)를 세계 최초로 분석하여 전력설비 상태감시와 고장분석에 활용하는 지능형전력망을 구축하였고, 이로써 설비 투자비용을 5년간 597억원을 절감하여 세계 최고수준의 전력공급 신뢰도와 전기품질을 달성한 부분에 대해 인정받음.\[14\]

  -
## 각주

[분류:전력](https://ko.wikipedia.org/wiki/분류:전력 "wikilink")

1.  산업통상부자원부 \<[제2차 국가 지능형 전력망 기본계획](http://www.motie.go.kr/common/download.do?fid=bbs&bbs_cd_n=6&bbs_seq_n=64958&file_seq_n=1)\> 22p에서 확인. 2018년 8월 9일.
2.  \<[지능형전력망의 구축 및 이용촉진에 관한 법률 (약칭:지능형전력망법)](http://www.law.go.kr/lsInfoP.do?lsiSeq=113440&ancYd=20110524&ancNo=10714&efYd=20111125&nwJoYnInfo=N&efGubun=Y&chrClsCd=010202#0000)\> \[시행 2011년 11월 25일\] \[법률 제10714호, 2011년 5월 24일 제정\]
3.  \<[제1차 지능형전력망 기본계획 및 2012 시행계획](http://www.motie.go.kr/common/download.do?fid=bbs&bbs_cd_n=6&bbs_seq_n=60639&file_seq_n=1)\> 65p에서 확인. 2012년 7월 20일.
4.
5.  \<[인터뷰 | 국내 최초 CIO100 어워드 수상\! 한국전력 차세대 스카다 프로젝트](http://www.ciokorea.com/news/30470)\> 기사 전문에서 확인. 2016년 7월 3일.
6.  \<[인터뷰 | 국내 최초 CIO100 어워드 수상\! 한국전력 차세대 스카다 프로젝트](http://www.ciokorea.com/news/30470#csidx3b5bbbb1df461bf8ffb212eb65618d4)\> 기사 3문단 '차세대 스카다(SCADA) 시스템 프로젝트'에서 확인. 2016년 7월 13일.
7.  산업통상부자원부 \<[제2차 국가 지능형 전력망 기본계획](http://www.motie.go.kr/common/download.do?fid=bbs&bbs_cd_n=6&bbs_seq_n=64958&file_seq_n=1)\> 22p에서 확인. 2018년 8월 9일.
8.  \<[한전, 전력빅데이터 분석·지능형전력망 구현...‘2016 CIO 100 Awards’ 수상](http://asiaee.net/article.php?aid=925041979)\> 기사 4문단 '차세대 지능형전력망(xGrids)의 국내 특허출원을 완료'에서 확인. 2016년 8월 17일.
9.  \<[KIPRIS 특허정보 검색서비스](https://ko.wikipedia.org/wiki/doi:10.8080/4120150057719 "wikilink")\> 상세정보에서 확인. 2015년 12월 1일.
10. \<[전기저널 2015년 9월호 차세대 스카다(SCADA)시스템 Zero-base 혁신](http://www.elec.or.kr/elec_journal/2015_9/7.pdf)\> 전문에서 확인. 2015년 9월 18일.
11. \<[한전, 지역 재생에너지 제어 시스템 구축](http://electimes.com/article.php?aid=1560983861181086002)\> 기사 전문에서 확인. 2016년 6월 20일.
12. 산업통상부자원부 \<[제2차 국가 지능형 전력망 기본계획](http://www.motie.go.kr/common/download.do?fid=bbs&bbs_cd_n=6&bbs_seq_n=64958&file_seq_n=1)\> 38p에서 확인. 2018년 8월 9일.
13. \<[한전, 국내 최초 ‘CIO 100 Awards' 수상](http://www.pgnkorea.com/news/articleView.html?idxno=6019)\> 기사 3문단 \<‘차세대 SCADA시스템 프로젝트’로 수상\>에서 확인. 2016년 6월 4일.
14. \<[한전, '美 CIO 100 Awards' 국내 최초 수상](http://www.econovill.com/news/articleView.html?idxno=296358)\> 기사 본문에서 확인. 2016년 8월 17일.