> This article is converted from Wikipedia: [BOINC](https://ko.wikipedia.org/wiki/BOINC).


**네트워크 컴퓨팅을 위한 버클리 공개 인프라스트럭처**(Berkeley Open Infrastructure for Network Computing, **BOINC**)은 [캘리포니아 대학교 버클리에서](../Page/캘리포니아_대학교_버클리.md "wikilink") 개발한 대한민국의 [코리아앳홈](https://ko.wikipedia.org/wiki/코리아앳홈 "wikilink")과 같은 자원봉사자들을 대상으로 한 분산컴퓨팅을 이용해서 정보를 처리하는 [미들웨어](../Page/미들웨어.md "wikilink")이다. 이 프로그램은 같은 대학교의 프로젝트인 [SETI@home](../Page/SETI@home.md "wikilink")개발에서 나왔으나, [SETI@home](../Page/SETI@home.md "wikilink")을 비롯한 수학, 의학, 분자 생물학, 기후학, 천체물리학같은 주제들에 대해서도 사용할 수 있다. BOINC은 오픈소스 공개 프로그램이고, [GNU 약소 일반 공중 사용 허가서](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink")(, LGPL)를 채용하고 있다.

BOINC은 [SETI@home](../Page/SETI@home.md "wikilink") 프로젝트를 이끌어가는 버클리 대학교 우주과학 연구소의 데이비드 P. 안드레센이 주축인 팀에서 개발되었다. 유사 슈퍼컴퓨팅 플랫폼인 BOINC는 2008년 11월 23일 기준으로 전 세계적으로 500,000개 이상의 가동중인 컴퓨터(호스트)를 가지고 있으며, 평균 4.2 페타플롭스의 연산능력을 가지고 있다.\[1\] BOINC은 미국 국립과학재단의 SCI/0221529 상\[2\] 과 SCI/0438443\[3\], 그리고 SCI/0721124 상\[4\] 에 의해 투자받았다. BOINC 프로젝트는 [2010년 11월](../Page/2010년_11월.md "wikilink") 기준으로 누적 사용자 206만명, 누적 컴퓨터 581만 대가 넘으며, [2008년 1월](../Page/2008년_1월.md "wikilink") 기준으로 BOINC 프로젝트 중 하나인 SETI@Home은 340만 년의 컴퓨터 시간 동안 가동되었다.

## BOINC의 디자인&구조

BOINC은 누구든지 분산 컴퓨팅 프로젝트를 시작할 수 있게 하는 자유 구조로 설계되었다. 대부분의 BOINC 프로젝트들은 수익도 없고, 자원자가 없으면 프로젝트를 돌릴 힘도 없을 정도이다. 그러나, BOINC은 이익을 바라지 않고 이 프로젝트를 지원해준다. BOINC은 서버 시스템과 클라이언트 시스템으로 이루어져 있으며, 이 둘이 분산, 작업, 그리고 일한 유닛을 보내는 것등을 서로 상호 소통하는 구조로 디자인되었다.

## BOINC 플랫폼의 기원

BOINC은 처음 [SETI@home](../Page/SETI@home.md "wikilink") 프로젝트를 관리하기 위해 개발되었다.

원래 SETI 클라이언트는 BOINC 프로그램 아닌 오직 [SETI@home](../Page/SETI@home.md "wikilink")만 돌릴 수 있는 프로그램이었다. 최초의 자원봉사 분산컴퓨팅 프로젝트 중 하나인 [SETI@home](../Page/SETI@home.md "wikilink")은 높은 수준의 보안이 설계되지 않았다. 그래서 몇몇 참여자들은 프로젝트에서 부정한 방법으로 기여를 높이는 방법을 썼다. BOINC의 디자인 요소 중 부정한 사용자에 의한 공격을 차단하는 것이 중요한 부분 중 하나였다.\[5\]

BOINC 프로젝트는 2001년 1월에 시작되었으며, 동년 4월 10일날 처음 출시되었다. 최초의 BOINC 기반 프로젝트는 2004년 6월 9일에 시작된 [Predictor@home](https://ko.wikipedia.org/wiki/Predictor@home "wikilink")이다.

## BOINC 프로젝트

BOINC에는 여러가지 과학 프로젝트가 있으며, 그중 대중들에겐 [SETI@home](../Page/SETI@home.md "wikilink"), [월드 커뮤니티 그리드](../Page/월드_커뮤니티_그리드.md "wikilink") 등이 많이 알려져 있다.

위 사항들은 기본적인 내용으로 실제 구동하는 프로젝트를 기준으로 해당 프로젝트의 요구사항에 맞춰야 한다.(프로젝트별로 메모리 사용량과 디스크 사용량이 상이함)

## BOINC 관리자

BOINC은 크게 각각의 등록된 프로젝트를 실행하는 BOINC 본체 프로그램과 운영과 관련된 환경을 관리하는 관리자 프로그램(BOINC Manager)으로 구성되며 일반 사용자들이 보게 되는 화면은 관리자 화면이다. 사용자들은 관리자를 통하여 등록된 프로젝트의 진행현황 및 구동 여부를 통제하고 그 결과를 조회할 수 있다.

## 화면보호기

BOINC 화면보호기와 프로젝트 화면보호기로 나뉘며, 화면보호기 설정에서 상세 설정을 할 수 있다.

BOINC 화면보호기는 BOINC 매니저에서 제공하는 정보를 출력한다. 활성화된 작업 진행 상황과 참여 중인 프로젝트의 크레딧 정보 등을 보여준다.

프로젝트 화면보호기는 각 분석 작업 프로세스에서 제공하는 정보를 출력한다. ‘그래픽 보여주기’ 기능을 제공하는, 연산 중인 작업에 한하여 작동한다. SETI@Home이나 Einstein@Home 등 일부 프로젝트에서만 지원하며, 프로젝트 홈페이지에서 화면보호기의 디자인을 변경할 수 있다.

## GPU 사용

일부 프로젝트에서는 수학, 과학 및 공학분야의 복잡한 연산을 보다 빠르게 수행하기 위해 [CPU뿐만이](../Page/중앙_처리_장치.md "wikilink") 아닌 그래픽 카드의 [GPU를](../Page/그래픽_처리_장치.md "wikilink") 사용하는 기능이 있다. 해당 프로젝트에서 GPU용 프로그램을 지원해야 하며 GPU 기능을 지원하는 경우 CPU에 비해 훨씬 더 빠르게 계산을 수행할 수 있다. 단, 프로젝트마다 지원하는 GPU가 다르기 때문에 해당 프로젝트가 [엔비디아](../Page/엔비디아.md "wikilink")의 GPU를 지원하는지 [ATI](https://ko.wikipedia.org/wiki/ATI "wikilink")사의 GPU를 지원하는지 확인을 하고 사용해야 한다.

## 크레딧 시스템

BOINC의 각 프로젝트들은 연산을 수행한 내역에 대해 일정량의 크레딧을 제공하며 각각의 크레딧에 다른 사용자와 비교함으로써 서로 경쟁을 할 수 있는 시스템을 제공하고 있다. BOINC 공식 사이트 외에 각 사용자별 크레딧 현황을 프로젝트별 및 통합으로 제공해 주는 사이트들이 여럿 존재한다.\[6\] \[7\]

## 각주

## 외부 링크

  - [버클리 네트워크 컴퓨팅을 위한 공개 기반 (BOINC)](http://boinc.berkeley.edu/)
  - [데이비드 안데르센 인터뷰](https://web.archive.org/web/20061025082041/http://acmqueue.com/modules.php?name=Content&pa=printer_friendly&pid=313&page=1)
  - [BOINC 프로젝트별 처리량 통계 집계 사이트(Boincstats.com)](http://boincstats.com)
  - [SETIKAH@KOREA (대한민국 1위팀)](http://cafe.naver.com/setikah)

[BOINC](https://ko.wikipedia.org/wiki/분류:BOINC "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 과학 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_과학_소프트웨어 "wikilink")

1.
2.  [Research and Infrastructure Development for Public-Resource Scientific Computing](http://www.nsf.gov/awardsearch/showAward.do?AwardNumber=0221529), The National Science Foundation
3.  [SCI: NMI Development for Public-Resource Computing and Storage](http://www.nsf.gov/awardsearch/showAward.do?AwardNumber=0438443), The National Science Foundation
4.  [SDCI NMI Improvement: Middleware for Volunteer Computing](http://www.nsf.gov/awardsearch/showAward.do?AwardNumber=0721124), The National Science Foundation
5.
6.
7.