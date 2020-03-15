> This article is converted from Wikipedia: [CICS](https://ko.wikipedia.org/wiki/CICS).


**CICS**(Customer Information Control System, 고객 정보 제어 시스템)는 [z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink")와 [z/VSE](https://ko.wikipedia.org/wiki/z/VSE "wikilink") 운영 체제를 사용하는 [IBM 메인프레임](../Page/IBM_메인프레임.md "wikilink") 시스템에서 주로 구동되는 [트랜잭션 서버이다](https://ko.wikipedia.org/wiki/거래_처리_시스템 "wikilink").

CICS는 고속의 대용량 [온라인 트랜잭션 처리를](https://ko.wikipedia.org/wiki/온라인_트랜잭션_처리 "wikilink") 지원하도록 설계된 [미들웨어](https://ko.wikipedia.org/wiki/미들웨어 "wikilink")이다. CICS에서의 "트랜잭션"은 하나 이상의 오브젝트에 영향을 미칠 수 있는, 단일 요청이 발행한 처리 단위이다.\[1\] 이러한 처리는 보통 상호 작용적(화면 지향)이지만 백그라운드 트랜잭션이 가능하다.

CICS는 운영 체제의 기능을 확장하거나 대체하는 서비스들을 제공하며 운영 체제의 일반화된 서비스들보다 더 효율적이고 특히 다양한 터미널 서비스와 통신을 한다는 관점에서 프로그래머들이 사용하기 더 쉽다.

CICS용으로 개발된 응용 프로그램들은 다양한 [프로그래밍 언어로](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink") 작성할 수 있으며 CICS가 제공하는 언어 확장을 사용하여 파일, 데이터베이스 연결, 터미널과 같은 리소스와 상호 작용한다든지, 웹 서비스와 같은 기능을 호출할 수 있다.

CICS가 은행, 보험 기업들과 같은 금융 기업들 사이에 상당한 이목을 끌고 있으며, [포춘 500](https://ko.wikipedia.org/wiki/포춘_500 "wikilink") 기업들 가운데 90%가 여러 정부 기관들과 더불어 CICS를 구동하고 있는 것으로 보고되고 있다.\[2\] 또, CICS는 여러 소규모 단체에도 널리 쓰이고 있다.

최근의 CICS 트랜잭션 서버는 [웹 서비스](https://ko.wikipedia.org/wiki/웹_서비스 "wikilink"), [엔터프라이즈 자바 빈즈](https://ko.wikipedia.org/wiki/엔터프라이즈_자바_빈즈 "wikilink") (EJBs), [이벤트 처리](https://ko.wikipedia.org/wiki/이벤트_처리 "wikilink"), [Atom](https://ko.wikipedia.org/wiki/Atom "wikilink") 피드, [REST](https://ko.wikipedia.org/wiki/REST "wikilink")ful 인터페이스 지원 등이 강화되었다. CICS 트랜잭션 서버 버전 4.2는 2011년 6월 24일 상용화되었으며 시스템 이벤트, 64비트 자바, 트랜잭션 추적, [패스프레이즈](https://ko.wikipedia.org/wiki/패스프레이즈 "wikilink")에 대한 지원이 추가되었다.\[3\]

## 역사

CICS 이전에 단일 스레드 방식의 트랜잭션 처리 시스템인 [IBM MTCS가](https://ko.wikipedia.org/wiki/IBM_MTCS "wikilink") 있었다. 나중에 MTCS-CICS 브리지가 개발되어 본래의 응용 프로그램들을 변경하지 않고도 이러한 트랜잭션들을 CICS 하에서 실행할 수 있게 되었다.

CICS는 원래 미국 [일리노이주](https://ko.wikipedia.org/wiki/일리노이주 "wikilink") [데스 플레인즈의](https://ko.wikipedia.org/wiki/데스_플레인즈 "wikilink") IBM 개발 센터에서 개발되었는데, 그 기점은 공익 산업의 요구가 있던 1966년을 기점으로 한다. 최초의 CICS 제품은 1968년 PU-CICS(*Public Utility Customer Information Control System*)라는 이름으로 공개되었다. 곧바로 다른 많은 산업들로 응용화되면서, [IMS](../Page/IBM_정보_관리_시스템.md "wikilink") [데이터베이스 관리 시스템이](https://ko.wikipedia.org/wiki/데이터베이스_관리_시스템 "wikilink") 나온지 오래지 않아 앞글자인 Public Utility가 빠진 CICS 프로그램 제품이 1969년 7월 8일 첫 릴리즈로 선보이게 되었다.

1974년 CICS 개발은 오늘날에도 개발 업무를 계속하고 있는 영국의 IBM 허슬리(IBM Hursley) 지역이 맡게 되었다.

## 프로그래밍

### 프로그래밍 고려 사항

다중 사용자 상호 작용 트랜잭션 응용 프로그램들은 동시에 여러 [트랜잭션](https://ko.wikipedia.org/wiki/데이터베이스_트랜잭션 "wikilink") [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink")를 지원하기 위해 [quasi](https://ko.wikipedia.org/wiki/wikt:quasi- "wikilink")-[reentrant가](https://ko.wikipedia.org/wiki/재진입성 "wikilink") 요구되었다.\[4\] 한 응용 프로그램에서 소프트웨어 코드 오류가 하나 있으면 어떠한 사용자라도 시스템에 접근하지 못할 수 있었다. CICS 재진입/재이용가능한 제어 프로그램들의 모듈러 디자인을 통해 여러 응용 프로그램들에 속한 여러 사용자들이 32K의 값비싼 [마그네틱 코어](https://ko.wikipedia.org/wiki/자기_철심 "wikilink") [물리 메모리](https://ko.wikipedia.org/wiki/물리_메모리 "wikilink")([운영 체제](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 포함)를 장착한 컴퓨터에서 실행할 수 있었다.

CICS 응용 프로그램의 프로그래머들이 트랜잭션을 가능한 효율적으로 만들려면 상당한 노력이 필요했다. 흔히 썼던 기법으로 개개의 프로그램을 4,096 바이트 보다 적게 크기를 제한하는 것이었는데, 이로써 CICS는 다른 프로그램이나 다른 응용 프로그램의 기억 공간의 필요에 따라 사용 중이지 않는 특정 프로그램이 차지한 메모리를 쉽게 재이용할 수 있었다. [가상 메모리가](https://ko.wikipedia.org/wiki/가상_메모리 "wikilink") 1972년 OS/360 버전에 추가되었을 때 4K 전략은 [페이징](https://ko.wikipedia.org/wiki/페이징 "wikilink")과 [스래싱](https://ko.wikipedia.org/wiki/스래싱 "wikilink")으로 인한 비생산적인 리소스 경합 부하를 줄이기 위해 훨씬 더 중요해졌다.

컴파일된 고급 코볼 및 PL/I 언어 프로그램들의 효율성이 더욱 더 요구되었다. 수많은 CICS 응용 프로그램들은 꾸준히 어셈블리어로 작성되어나갔는데, 이는 코볼과 PL/I 지원이 가능해진 뒤에도 마찬가지였다.

[MVS](../Page/MVS.md "wikilink") 리전(region), 곧 전체 파티션은 CICS 커널 코드를 포함한 동일한 [메모리 보호](https://ko.wikipedia.org/wiki/메모리_보호 "wikilink") 키와 더불어 동작하였다. 프로그램 오류와 CICS 제어 블록 오류는 시스템 다운의 잦은 원인이기도 했다. 특정 응용 프로그램의 소프트웨어에 오류가 일어나면 하나 이상의 현재 실행 중인 응용 트랜재션의 메모리(코드나 데이터)를 덮어쓸 수 있다.

20년이 넘는 기간 동안 여러 CICS 새 릴리즈에서 이러한 심각한 단점들은 존속하였다. 공익회사나 대형 은행, 기타 수십억 달러의 금융 기업들에겐 CICS 응용 트랜잭션이 이따금 중요했다. 고급 CICS 기술자들의 수는 적고 수요는 많았다. 복잡한 학습 곡선은 얕고 길었다. 초보 개발자들은 기업 운영에 큰 부정적인 영향을 미치기도 했다.

마침내 테스트 및 디버그 기능을 제공하던 모니터링 프로그램 제어를 통해 모든 테스트를 수행함으로써 고급 응용 프로그램 보호 기준 제공이 가능하게 되었다. 이러한 소프트웨어 중 하나로 [OLIVER가](https://ko.wikipedia.org/wiki/IBM_OLIVER "wikilink") 있으며, [반가상화](https://ko.wikipedia.org/wiki/반가상화 "wikilink")를 제공하는 응용 프로그램 코드의 [명령 집합 시뮬레이터를](https://ko.wikipedia.org/wiki/명령_집합_시뮬레이터 "wikilink") 이용하여 응용 프로그램들이 메모리를 훼손하는 일을 막을 수 있었다.

### 매크로 수준 프로그래밍

CICS가 처음 출시되었을 때 [IBM 360 어셈블러로](https://ko.wikipedia.org/wiki/IBM_베이직_어셈블리어 "wikilink") 작성된 응용 트랜잭션 프로그램들만 지원했다. [코볼](https://ko.wikipedia.org/wiki/코볼 "wikilink")과 [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink")에 대한 지원은 수년 뒤 추가되었다. 초기의 어셈블러 지향으로 인해 CICS 서비스에 대한 요청은 어셈블러 매크로 명령을 이용하여 만들어졌다. 이를테면 파일로부터 레코드를 읽는 요청은 CICS의 파일 제어 프로그램에 대한 매크로 호출을 통해 다음과 비슷하게 만들어진다:

`DFHFC TYPE=READ,DATASET=myfile,TYPOPER=UPDATE,....etc.`

이로써 나중에 "매크로 수준의 CICS"라는 용어가 만들어졌다.

### 명령 수준 프로그래밍

1980년대 동안 허슬리 지역의 IBM은 "명령 수준 CICS"을 지원하는 CICS의 중간 버전을 만들어냈다. 이 릴리즈는 오래된 프로그램들을 지원하였을뿐 아니라 새로운 명령 수준의 응용 프로그램에 대한 새로운 실행 계층을 도입하였다.

일반적인 명령 수준 호출은 다음과 같다:

``` cobolfree
 EXEC CICS
     SEND MAPSET('LOSMATT') MAP('LOSATT')
 END-EXEC
```

### 실행 시간 변환

초기 1990년대에 도입된 명령 수준 전용 CICS는 초기 버전들의 CICS에 견주어 몇 가지 이점을 제공하였다. 그러나 IBM은 초기 버전용으로 작성된 매크로 수준의 응용 프로그램들에 대한 지원을 중단하였다. 다시 말해, 수많은 응용 프로그램들은 명령 수준 EXEC 명령만을 사용하도록 변환하거나, 완전히 다시 작성되어야 했다.

당시 다방면으로 수십년 동안 생산된 수백만의 프로그램들이 전 세계에 있었던 것으로 짐작된다. 이들을 다시 작성할 경우 필연적인 새로운 기능의 추가 없이 새로운 버그들만 발생시킬 수 밖에 없었다.

그러나 APT 인터내셔널의 Command CICS 따위의 변환 소프트웨어를 사용하여 매크로 수준의 프로그램들을 실행하는 것이 가능하긴 했다. 이로써 응용 프로그램들이 차기 버전의 CICS의 새로운 기능에 대한 이점을 취함과 동시에 원래의 변형되지 않은 코드 기반을 유지할 수 있게 되었다. 이와 동일한 기술을 사용하여 오늘날 실행 중인 프로그램들이 여전히 있는 것으로 간주된다.

### 새로운 프로그래밍 스타일

최근의 CICS 트랜잭션 서버는 현대의 수많은 프로그래밍 스타일에 대한 지원을 포함하고 있다.

CICS 트랜잭션 서버 버전 2.1에서 엔터프라이즈 자바 빈즈 (EJB)에 대한 지원을 도입하였다. CICS 트랜잭션 서버 버전 2.2에서는 소프트웨어 개발자 툴킷을 지원하였다. CICS는 IBM의 웹스피어 제품 계열과 동일한 런타임 컨테이너를 제공하므로 EJB 애플리케이션들은 CICS와 웹스피어 간에 이식이 가능하며 EJB 애플리케이션들의 개발 및 디플로이먼트(deployment)를 위한 통일된 도구 이용이 가능하다.

## 트랜잭션

하나의 CICS 트랜잭션은 함께 태스크를 수행하는 명령들의 모임이다.

각각의 CICS 프로그램은 트랜잭션 식별자를 이용하여 초기화된다. CICS 화면은 일반적으로 BMS 어셈블러 매크로나 타사 도구로 만들어진 모듈을 가리키는 맵이라는 구조체로 송신된다. CICS 화면들은 사용된 터미널의 종류에 따라 여러 색을 가졌거나 강조된, 아니면 깜박이는 글자를 포함할 수 있다. 아래의 예는 코볼을 통해 어떻게 맵을 송신할 수 있는지에 대한 것이다. 최종 사용자가 데이터를 입력하면 CICS로부터 맵을 가져옴으로써 프로그램에 접근할 수 있게 된다.

``` cobolfree
 EXEC CICS
     RECEIVE MAPSET('LOSMATT') MAP('LOSATT') INTO(OUR-MAP)
 END-EXEC.
```

### BMS 맵 코드의 예

BMS(Basic Mapping Support)는 다음과 같은 어셈블러 매크로들을 통해 화면 포맷을 정의한다. CICS 로드 라이브러리 내의 로드 모듈인 물리 맵 집합(physical map set)과, 소스 프로그램에 복사된 PL/I의 DSECT, 코볼, 어셈블러 등을 가리키는 심볼릭 맵 집합(symbolic map set)을 둘 다 생성한다.\[5\]

``` cobolfree
 LOSMATT DFHMSD TYPE=MAP,                                               X
                MODE=INOUT,                                             X
                TIOAPFX=YES,                                            X
                TERM=3270-2,                                            X
                LANG=COBOL,                                             X
                MAPATTS=(COLOR,HILIGHT),                                X
                DSATTS=(COLOR,HILIGHT),                                 X
                STORAGE=AUTO,                                           X
                CTRL=(FREEKB,FRSET)
 *
 LOSATT  DFHMDI SIZE=(24,80),                                           X
                LINE=1,                                                 X
                COLUMN=1
 *
 LSSTDII DFHMDF POS=(1,01),                                             X
                LENGTH=04,                                              X
                COLOR=BLUE,                                             X
                INITIAL='MQCM',                                         X
                ATTRB=PROT
 *
         DFHMDF POS=(24,01),                                            X
                LENGTH=79,                                              X
                COLOR=BLUE                                              X
                ATTRB=ASKIP,                                            X
                INITIAL='PF7-          8-           9-          10-     X
                    11-            12-CANCEL'
 *
           DFHMSD   TYPE=FINAL
           END
```

## 구조

[z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink") 환경에서 CICS 설치본은 하나 이상의 리전(region, 일반적으로 CICS region을 가리킴)\[6\]을 이루며, 하나 이상의 z/OS 시스템 이미지들을 가로지른다. 상호 작용적인 트랜잭션을 처리하지만 각각의 CICS 리전은 배치 처리 및 표준 JCL 문을 포함한 배치 주소 공간으로 시작할 수 있다. (무기한으로 실행하는 잡) 또, 각각의 CICS는 시작된 태스크로서 시작할 수 있다. 배치 잡이든, 시작된 태스크로든 어떠한 것이든 간에 CICS 리전은 유지 보수(MVS나 CICS)를 위해 종료하기 앞서 수일, 수주, 수개월에 걸쳐 동작할 수 있다.

설치본들은 다양한 리전을 위해 수많은 주소 공간으로 나뉘는데 이를테면 다음과 같다:

  - 응용 프로그램 구분,
  - 기능 구분,
  - 단일 리전이나 주소 공간의 부하 용량 제한 회피

일반적인 설치본은 수많은 구별된 응용 프로그램들을 이룬다. 각각의 응용 프로그램은 보통 자신만의 TOR(Terminal-Owning Region) 및 하나 이상의 AOR(Application-Owning Region)을 가지고 있으며, 다른 구성 방식 또한 가능하다. 이를테면 AOR은 파일 입출력을 수행하지 않지만, AOR 트랜잭션을 위해 파일 입출력을 수행하는 FOR(File-Owning region)이 있다.

## 구성 요소

CICS 시스템은 온라인 핵(nucleus), 배치 지원 프로그램, 응용 프로그램 서비스를 이룬다.\[7\]

### 핵

CICS 핵은 수많은 기능 모듈을 이룬다.

  - KCP (작업 제어 프로그램, Task Control Program).
  - SCP (기억 제어 프로그램, Storage Control Program).
  - PCP (프로그램 제어 프로그램, Program Control Program).
  - PIP (프로그램 인터럽트 제어 프로그램, Program Interrupt Control Program).
  - ICP(구간 제어 프로그램, Interval Control Program).
  - DCP(덤프 제어 프로그램, Dump Control Program).
  - TCP(터미널 제어 프로그램, Terminal Control Program).
  - FCP(파일 제어 프로그램, File Control Program).
  - TDP(임시 데이터 제어 프로그램, Transient Data Control Program).
  - TSP(임시 기억 제어 프로그램, Temporary Storage Control Program).

### 지원 프로그램

온라인 기능뿐 아니라 CICS는 배치 잡으로 실행할 수 있는 지원 프로그램들이 여럿 있다.\[8\]

  - 고급 언어 (매크로) 전처리기.
  - 명령어 변환기.
  - 덤프 유틸리티 – CICS 덤프 관리가 만들어낸, 서식 있는 덤프를 인쇄한다.
  - 트레이스 유틸리티 – CICS 트레이스 출력에 서식을 입히고 인쇄한다.
  - 저널 포맷팅 유틸리티 – 오류 발생 시 CICS 리전(region)의 서식화된 덤프를 인쇄한다.

### 응용 프로그램 서비스

다음의 CICS 구성 요소들은 응용 프로그램 개발을 지원한다.\[9\]

  - BMS(기본 매핑 지원, Basic Mapping Support)는 장치 독립적인 터미널 입출력을 제공한다.
  - DIP(데이터 교환 프로그램, Data Interchange Program)는 [IBM 3770](https://ko.wikipedia.org/wiki/IBM_2780/3780#2770.2C_3770 "wikilink") 및 [IBM 3790](https://ko.wikipedia.org/wiki/IBM_3790 "wikilink") 프로그래머블 장치에 대한 지원을 추가한다.
  - 2260 호환성은 [IBM 2260](https://ko.wikipedia.org/wiki/IBM_2260 "wikilink") 디스플레이 장치용으로 작성된 프로그램들을 3270 디스플레이에서 실행할 수 있게 한다.
  - EXEC 인터페이스 프로그램 – `EXEC CICS`를 통해 만든 호출들을 CICS 함수에 대한 호출로 변환하는 조그마한 프로그램.
  - 내장 함수 – 테이블 검색, 음성 변환, 필드 확인, 필드 편집, 비트 검사, 입력 서식 추가, 편중 검색(weighted retrieval)

## 참조

<references />

## 외부 링크

  -
[분류:트랜잭션 처리](https://ko.wikipedia.org/wiki/분류:트랜잭션_처리 "wikilink") [분류:IBM 소프트웨어](https://ko.wikipedia.org/wiki/분류:IBM_소프트웨어 "wikilink")

1.
2.  IBM, 2004. [CICS 35 year anniversary](http://www.ibm.com/software/htp/cics/35/cics_intro/)
3.  IBM, 2011. [CICS Transaction Server for z/OS V4.2](http://www.ibm.com/cics/tserver/v42/)
4.
5.
6.
7.
8.
9.