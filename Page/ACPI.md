> This article is converted from Wikipedia: [ACPI](https://ko.wikipedia.org/wiki/ACPI).


**고급 구성 및 전원 인터페이스**(Advanced Configuration and Power Interface, ACPI) 규격은 [HP](../Page/휴렛_팩커드.md "wikilink"), [인텔](../Page/인텔.md "wikilink"), [마이크로소프트](../Page/마이크로소프트.md "wikilink"), [피닉스](https://ko.wikipedia.org/wiki/피닉스_\(기업\) "wikilink"), 그리고 [도시바](../Page/도시바.md "wikilink")가 개발하고, 1996년 12월에 처음 공개된 최초의 [오픈 표준이다](https://ko.wikipedia.org/wiki/오픈_표준 "wikilink"). 하드웨어 감지, 메인보드 및 장치 구성, [전원 관리를](https://ko.wikipedia.org/wiki/전원_관리 "wikilink") 담당하는 일반적인 인터페이스를 정의한다. 이 규격\[[http://www.acpi.info/spec.htm\]에](http://www.acpi.info/spec.htm%5D에) 따르면, "ACPI는 OSPM 안의 주 구성 요소이다."

## 역사

ACPI 사양의 최초의 판은 1996년 12월 출간되었으며, 16 및 32비트 주소 공간을 지원한다. 2000년 8월 ACPI는 리비전 2.0에 이르러 64비트 주소 지원뿐 아니라, 멀티프로세서 워크스테이션과 서버를 지원하기에 이른다.

2004년 9월 리비전 3.0이 출시되었으며, ACPI 사양 지원이 [SATA](https://ko.wikipedia.org/wiki/SATA "wikilink") 컨트롤러, [PCI 익스프레스](../Page/PCI_익스프레스.md "wikilink") 버스, 256개 이상 프로세서의 [멀티프로세서](https://ko.wikipedia.org/wiki/멀티프로세서 "wikilink") 지원, [광센서](https://ko.wikipedia.org/wiki/광검출기 "wikilink") 및 사용자 감지 장치로까지 넓혀졌고 열 모델을 이전 프로세서 중심 지원 이상으로 확대하였다.

2009년 6월 출시된 ACPI 사양 리비전 4.0은 디자인에 다양한 새로운 기능들을 추가하였다. 특별한 점으로는 [USB 3.0](../Page/USB_3.0.md "wikilink") 지원, 논리 프로세서 유휴 지원, [x2APIC](https://ko.wikipedia.org/wiki/x2APIC "wikilink") 지원을 들 수 있다.

ACPI 사양 리비전 5.0은 2011년 12월에 출시되었으며\[1\], 그 뒤 리비전 5.1은 2014년 7월 출시되었다.\[2\]

최신 사양 판은 6.1로, 2016년 3월 출시되었다.\[3\]

## 상태

### 전역 상태

ACPI 규격은 ACPI 호환 컴퓨터 시스템에서 사용할 수 있는 다음의 몇 가지 (전역) 상태를 정의한다.

  - **G0 (S0)**: 작업 중(Working)이다.
  - **G1**: 대기 모드(Sleeping)이다.
      - **S0ix**: Modern Standby.
      - **S1**: 전력이 필요한 상태에 놓은 대기 모드이다.
      - **S2**: S1보다 더 전력을 아끼는 대기 모드이다. CPU의 전원을 차단하지만, 이 기능을 잘 쓰이지 않는다.
      - **S3**: 절전 모드, 절전. 메인 메모리는 꺼져 있지 않다.
      - **S4**: [최대 절전 모드](https://ko.wikipedia.org/wiki/최대_절전_모드 "wikilink")
  - **G2 (S5)**: 소프트 종료(Soft Off)
  - **G3**: 기계적 종료(Mechanical Off)

### 장치 상태

장치 상태 D0-D3는 장치에 따라 바뀐다:

  - D0: 완전히 켬, 동작 중
  - D1 및 D2: 중간 전력 상태 (기계에 따라 정의가 다름)
  - D3: 끔, 장치가 꺼져 있으며 컴퓨터 버스에 응답하지 않음

### 프로세서 상태

CPU 전력 상태 C0-C3는 다음과 같이 정의된다:

  - C0: 동작 중
  - C1: 중단, 프로세서는 아무런 명령어도 실행하지 않지만 즉시 실행 상태로 되돌아갈 수 있다. [펜티엄 4와](../Page/펜티엄_4.md "wikilink") 같은 일부 프로세서는 전력을 아끼기 위해 강화된 C1 상태(C1E)를 지원한다.
  - C1E: Enhanced Halt CPU 내부 클럭을 소프트웨어로 멈추고 CPU의 전압을 낮춤. 버스 인터페이스 유닛과 APIC는 최고 속도로 작동
  - C2: 클럭 중단, 원래 상태로 돌아가는 데 시간이 오래 걸린다.
  - C3: 프로세서가 [캐시](../Page/캐시.md "wikilink")를 유지하지 않지만, 다른 상태는 유지한다. C3를 지원하는 프로세서가 여럿 있지만, 이들 프로세서마다 정상 동작 상태로 되돌아가는 데에는 걸리는 시간이 다르다.
  - C4: Deeper Sleep CPU 전압을 낮춤
  - C4E/C5: Enhanced Deeper Sleep CPU의 전압을 낮추고 메모리 캐시를 끔
  - C6: Deep Power Down CPU 내부 클럭을 줄이고 CPU 전압을 낮춤

### 성능 상태

장치나 프로세서가 각각 D0, C0으로 동작할 때, 몇 가지 전력 성능 상태들 가운데 하나로 동작한다. 이러한 상태들은 추가된 기능에 따라 달라질 수 있지만 P0은 언제나 최고의 성능 상태이며, P1에서 P*n-1*은 차례로 낮은 성능의 상태를 가지며, 최대 *n*의 기능 수는 16으로 제한된다..

## ACPI 표

아래의 표들은 하드웨어 정보를 얻기 위해 운영 체제가 사용하는 것이다.

  - RSDP (루트 시스템 서술 포인터)
  - RSDT (루트 시스템 서술 테이블)
  - DSDT (차별화된 시스템 서술 테이블) : 기본 시스템에 대한 구성 정보를 제공한다.
  - XSDT (확장 시스템 서술 테이블)
  - FADT (고정 ACPI 서술 테이블)
  - FACS (펌웨어 ACPI 제어 구조)
  - SBST (스마트 배터리 테이블)
  - ECDT (임베디드 컨트롤러 시동 리소스 테이블)
  - MADT (다중 APIC 서술 테이블)
  - SRAT (시스템 리소스 어피니티 테이블)
  - SLIT (시스템 지역화 거리 정보 테이블)
  - SLIC (소프트웨어 허가 서술 테이블)
  - SSDT (두 번째 시스템 서술자 테이블)

## 함께 보기

  - [그린 컴퓨팅](../Page/그린_컴퓨팅.md "wikilink")
  - [전원 관리 키](https://ko.wikipedia.org/wiki/전원_관리_키 "wikilink")

## 각주

## 외부 링크

  - [ACPI 홈페이지](http://www.acpi.info/)

[분류:바이오스](https://ko.wikipedia.org/wiki/분류:바이오스 "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:컴퓨터 하드웨어 표준](https://ko.wikipedia.org/wiki/분류:컴퓨터_하드웨어_표준 "wikilink") [분류:시스템 관리](https://ko.wikipedia.org/wiki/분류:시스템_관리 "wikilink") [분류:개방형 표준](https://ko.wikipedia.org/wiki/분류:개방형_표준 "wikilink")

1.
2.
3.