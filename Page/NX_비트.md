> This article is converted from Wikipedia: [NX 비트](https://ko.wikipedia.org/wiki/NX_비트).


**NX 비트**(, 실행 방지 비트)는 프로세서 명령어나 코드 또는 데이터 저장을 위한 메모리 영역을 따로 분리하는 [CPU의](../Page/중앙_처리_장치.md "wikilink") 기술이다. 이 기능은 [하버드 아키텍처](../Page/하버드_아키텍처.md "wikilink") 프로세서에서 보통 쓰인다. 그러나 NX 비트는 기본적인 [폰 노이만 구조](../Page/폰_노이만_구조.md "wikilink") 프로세서에서 보안을 목적으로 많이 쓰인다.

NX 특성으로 지정된 모든 메모리 구역은 데이터 저장을 위해서만 사용되며, 프로세서 명령어가 그 곳에 상주하지 않음으로써 실행되지 않도록 만들어 준다. [실행 보호라는](https://ko.wikipedia.org/wiki/실행_보호 "wikilink") 일반 기술은 특정한 종류의 악성 소프트웨어를 컴퓨터에 들어오지 못하게 막는 데 사용된다. 악성 소프트웨어의 경우 자신의 코드를 다른 프로그램의 자료 기억 영역에 심어 놓은 다음 이 구역 안에서 자신의 코드를 실행하게 만들며, 이를 [버퍼 오버플로](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink") 공격이라고 한다.

인텔은 eXecute Disable의 약자인 **XD 비트**로 광고하기로 결정하였다. 그러나 인텔의 XD 비트와 AMD의 NX 비트는 같은 기능을 수행하며 이름만 다른 것이다.

## 하드웨어 배경

80286 이후의 x86 프로세서들은 [세그먼트](../Page/메모리_세그먼트.md "wikilink") 수준으로 추가된 비슷한 기능을 제공한다. 그러나 이러한 제어 구조는 너무 빈약하여 쓸모가 없다. 특히 [플랫 메모리 모델(Flat memory model)을](https://ko.wikipedia.org/wiki/:en:Flat_memory_model "wikilink") 사용하는 현대의 소프트웨어의 경우에는 그렇다. 완전한 세그먼트가 아닌, 각 페이지마다 실행을 제어할 수 있는 새로운 구조가 필요하게 되었다.

페이지 수준의 구조는 [썬의](../Page/썬_마이크로시스템즈.md "wikilink") [SPARC](../Page/SPARC.md "wikilink"), [알파](../Page/DEC_알파.md "wikilink"), [IBM](../Page/IBM.md "wikilink")의 [파워PC](../Page/파워PC.md "wikilink")와 같은 다른 다양한 프로세서 아키텍처에서 여러 해 동안 사용되었다. 2001년에 인텔은 [IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink") 아키텍처를 사용하는 자사의 [아이테니엄](../Page/아이테니엄.md "wikilink") (Merced) 프로세서에 비슷한 기능을 추가하였지만, 당시 사람들이 애용하던 x86 프로세서 계열(펜티엄, 셀러론, 제온 등)에는 도입하지 않았다. x86 아키텍처의 경우, [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")는 [애슬론 64와](../Page/애슬론_64.md "wikilink") [옵테론](../Page/옵테론.md "wikilink")과 같은 [AMD64](https://ko.wikipedia.org/wiki/AMD64 "wikilink") 계열 프로세서에 NX 비트를 도입하였다. NX 비트라는 용어는 다른 프로세서의 비슷한 기술을 서술할 때에도 흔히 쓰이게 되었다.

AMD가 이 기능을 AMD64 명령어 세트에 도입하기로 결정한 뒤, 인텔은 후반 프레스캇 코어의 x86 기반의 [펜티엄 4](../Page/펜티엄_4.md "wikilink") 프로세서부터 이와 비슷한 기능을 도입하였다.

구체적으로 말해, NX 비트는 [페이지 테이블](../Page/페이지_테이블.md "wikilink") 안에 있는 64비트 엔트리의 비트 숫자 63(최상위 비트)을 일컫는다. 이 비트가 0으로 설정된 경우, 코드는 그 페이지에서 실행될 수 있다. 1로 설정된 경우, 코드는 그 페이지에서 실행될 수 없으며 어떠한 것도 그 데이터에 상주할 수 없다. 또한 [물리 주소 확장](../Page/물리_주소_확장.md "wikilink") (PAE) 페이지 테이블 포맷으로만 사용될 수 있다는 것도 잊어서는 안 된다. 왜냐하면 x86의 원래 32비트 페이지 테이블 포맷은 분명히 비트 63이 존재하지 않기 때문이다.

## 소프트웨어 구현

하드웨어로 이 기능을 구현하기 앞서, 여러 운영 체제는 소프트웨어를 통해 이 기능을 가상으로 구현하였다. 이를테면 **[W^X](https://ko.wikipedia.org/wiki/W^X "wikilink")** 또는 **[Exec Shield](../Page/Exec_Shield.md "wikilink")**를 들 수 있다.

NX 비트의 이점을 이용하고 이를 가상으로 구현하는 기능을 포함하는 [운영 체제는](../Page/운영_체제.md "wikilink") [스택과](../Page/콜_스택.md "wikilink") [히프](../Page/동적_메모리_할당.md "wikilink") 메모리 영역이 실행되지 못하게 막으며, 실행 가능한 메모리를 기록하지 못하게 막는다. 특히 [새서 웜과](https://ko.wikipedia.org/wiki/새서_웜 "wikilink") [블래스터 웜과](https://ko.wikipedia.org/wiki/블래스터_웜 "wikilink") 같은 코드를 실행하고 거부하는 특정한 [버퍼 오버플로의](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink") 이용을 막는 데 도움을 준다. 이러한 공격은 쓰기 가능, 실행 가능이 되기 위한 메모리 일부 (보통 스택)에 따라 달라진다. 쓰기나 실행이 불가한 경우, 공격은 실패로 끝난다.

## 운영 체제로의 도입

수많은 운영 체제는 NX 정책을 포함하고 있으며, 그 운영 체제들 가운데 일부는 NX 에뮬레이션을 사용한다. 일부 기술의 경우, 각 기술이 지원하는 주된 기능을 다음과 같이 요약하고 있다.

  - 하드웨어 지원 프로세서: (CPU 아키텍처의 쉼표 구분 목록)
  - 에뮬레이션: (아니오) 또는 (아키텍처 독립) 또는 (CPU 아키텍처의 쉼표 구분 목록)
  - 기타 지원: (없음) 또는 (CPU 아키텍처의 쉼표 구분 목록)
  - 표준 분배: (아니오) 또는 (예) 또는 (이 기술을 지원하는 버전이나 배포의 쉼표 구분 목록)
  - 공개일: (처음 공개된 날)

아키텍처 독립 [에뮬레이션](https://ko.wikipedia.org/wiki/에뮬레이션 "wikilink")을 공급하는 기술은 하드웨어적으로 지원하지 않는 모든 프로세서에서 사용할 수 있다. "기타 지원"는 NX 비트가 분명히 존재하지 않는 프로세서를 위한 것이다.

### FreeBSD

[FreeBSD](../Page/FreeBSD.md "wikilink")는 2007년 4월 6일 이후로 NX를 지원하지 않는다.

### OS X

인텔 기반 [OS X은](https://ko.wikipedia.org/wiki/OS_X "wikilink") [애플](../Page/애플.md "wikilink")로부터 NX 비트를 지원한다. (처음 공개한 인텔 기반의 10.4.4 뒤로).

### 리눅스

[리눅스 커널은](../Page/리눅스_커널.md "wikilink") NX 비트를 지원하는 CPU(이를테면 현재 팔리는 64비트 AMD, 인텔, VIA, 트랜스메타 CPU)의 기본 하드웨어 NX를 지원하고 있다.

x86_64 CPU 위의 64비트 모드에서 이 기능에 대한 지원이 [2004년](../Page/2004년.md "wikilink")에 [앤디 클린에](https://ko.wikipedia.org/wiki/앤디_클린 "wikilink") 의해 추가되었고, 같은 해에 [인고 몰나는](https://ko.wikipedia.org/wiki/인고_몰나 "wikilink") 64비트 CPU 위의 32 비트 모드에서 NX 비트에 대한 지원을 추가하였다. 이러한 기능들은 안정화된 리눅스 커널(2004년 8월에 공개한 2.6.8 이후)에서 사용할 수 있다.

32비트 x86 CPU와 64비트 x86 호환 CPU에서 실행되는 32비트 x86 커널 위의 NX 비트의 이용은 매우 중요하다. 왜냐하면 32비트 x86 커널은 보통 [AMD64](https://ko.wikipedia.org/wiki/AMD64 "wikilink")나 [IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink")가 제공하는 NX 비트를 예측하지 못하기 때문이다. NX 사용 가능화 패치는 "NX 비트"를 사용할 수 있는 환경을 갖추었을 경우 이러한 커널이 NX 비트를 사용할 수 있게 도와 준다.

일부 데스크톱 [리눅스 배포판](../Page/리눅스_배포판.md "wikilink"), 이를테면 [페도라 코어 6](https://ko.wikipedia.org/wiki/페도라_코어 "wikilink"), [우분투 리눅스](https://ko.wikipedia.org/wiki/우분투_리눅스 "wikilink"), [오픈수세](../Page/오픈수세.md "wikilink")는 32 비트 모드에서 NX 비트 접근에 요구되는 HIGHMEM64 옵션을 기본 커널에서 켜 놓지 않는다. 그 까닭은 NX 비트 사용에 필요한 PAE 모드를 켜 놓고 (PAE를 지원하지 않는) [펜티엄 프로](../Page/펜티엄_프로.md "wikilink") 이전, [셀러론 M](https://ko.wikipedia.org/wiki/셀러론_M "wikilink"), [펜티엄 M](../Page/펜티엄_M.md "wikilink") 프로세서를 사용할 경우, 시동에 실패하기 때문이다. PAE를 지원하지 않는 다른 프로세서는 [AMD K6](../Page/AMD_K6.md "wikilink") 이전, [트랜스메타 크루소](https://ko.wikipedia.org/wiki/트랜스메타_크루소 "wikilink"), [VIA C3](https://ko.wikipedia.org/wiki/VIA_C3 "wikilink") 이전, 그리고 [Geode](https://ko.wikipedia.org/wiki/Geode "wikilink") GX/LX가 있다. [페도라 코어 6은](https://ko.wikipedia.org/wiki/페도라_코어 "wikilink") PAE, NX를 지원하는 커널 PAE 패키지를 제공하지 않는다.

실행 방지 기능은 다른 비 x86 프로세서에도 존재한다.

## 같이 보기

  - [데이터 실행 방지](../Page/데이터_실행_방지.md "wikilink")

## 외부 링크

  - [CPU 기반 보안: NX Bit](http://hardware.earthweb.com/chips/article.php/3358421)
  - [AMD, 인텔이 바이러스 방지 기술을 칩에 추가한다](http://zdnet.com/2100-1105_2-5137832.html?tag=nl)
  - [마이크로소프트 보안 개발자 센터: 윈도 XP SP 2: 실행 보호](http://msdn.microsoft.com/security/productinfo/XPSP2/memoryprotection/execprotection.aspx)

[분류:중앙 처리 장치](https://ko.wikipedia.org/wiki/분류:중앙_처리_장치 "wikilink") [분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink")