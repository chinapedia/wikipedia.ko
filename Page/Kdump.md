> This article is converted from Wikipedia: [Kdump](https://ko.wikipedia.org/wiki/Kdump).


**kdump**는 [커널 패닉](../Page/커널_패닉.md "wikilink") 이벤트 시에 [충돌 덤프를](../Page/코어_덤프.md "wikilink") 생성하는 [리눅스 커널의](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 한 부분이다. Kdump가 발생하면 디버깅 목적으로 분석될 수 있고 충돌의 원인을 결정할 수 있는 메모리 이미지(또한 vmcore라고도 알려진)를 익스포트한다. [ELF](https://ko.wikipedia.org/wiki/ELF_파일_형식 "wikilink") 객체로서 익스포트된 메인 메모리의 덤프된 이미지는 커널 충돌을 다루는 동안에 직접적으로 /proc/vmcore를 통해서 접근될 수 있으며 로컬상으로 접근 가능한 [파일 시스템으로](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 또는 raw 디바이스 그리고 네트워크를 통해 접근 가능한 원격 시스템으로 자동으로 저장될 수 있다.\[1\]\[2\]

## 내부

[섬네일](https://ko.wikipedia.org/wiki/파일:Kdump.svg "wikilink")

커널 충돌이 일어나는 이벤트 발생 시에, kdump는 *dump-capture kernel*로 알려진 다른 리눅스 커널을 부팅함으로써 시스템의 일관성을 유지하며 이것을 메모리 덤프를 익스포트하고 저장하는데 사용한다. 결과적으로 시스템은 여러 문제들을 유발할 수 있는 이미 충돌된 커널 대신에 깨끗하고 신뢰성 있는 환경으로 부팅된다. 이 "듀얼 커널" 레이아웃을 구현하기 위해서 kdump는 [kexec](https://ko.wikipedia.org/wiki/kexec "wikilink")을 사용한다. kexec은 커널 충돌 이후에 즉시 덤프-캡처 커널로 부팅하며, kdump는 [부트로더](https://ko.wikipedia.org/wiki/부트로더 "wikilink")의 실행 없이 현재 실행 중인 커널로 부팅할 수 있는 kexec의 능력을 사용한다. 덤프-캡처 커널은 이 목적을 위한 독립적인 [리눅스 커널](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 이미지이거나 또는 재배치 가능한 커널을 지원하는 아키텍처에서 재사용 가능한 주요 커널 이미지일 수 있다.\[3\]\[4\]\[5\]\[6\]

부팅되고 덤프-캡처 커널을 실행하는 동안 미리 RAM의 작은 부분을 예약함으로써 메인 메모리(RAM)의 내용들은 보존된다. 또한 덤프-캡처 커널은 미리 로드되기 때문에 주요 커널에서 사용되는 RAM의 어떤 부분도 커널 충돌을 다루는 동안에 겹쳐써지지 않는다. 램의 이 보존된 부분은 덤프-캡처 커널에 의해서 사용되며 일반적인 시스템 동작에서는 사용되지 않는다. [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 같은 몇몇 아키텍처들은 어디에 로드되었는지와 상관 없이 커널을 부트하기 위해 RAM의 작은 고정된 위치 부분을 요구한다; 이 경우 kexec는 이 RAM의 부분의 복사본을 만들고 이것은 또한 덤프-캡처 커널에 의해 접근될 수 있다. RAM의 저장된 부분의 크기와 옵셔널 위치는 커널 부트 파라미터 crashkernel에 명시되며 kexec 명령줄 라인 유틸리티는 주요 커널이 덤프-캡처 커널을 미리 로드하고 initrd 이미지를 RAM의 보존된 부분에 관련시키기 위해 부팅된 이후에 사용된다.\[7\]\[8\]\[9\]

리눅스 커널의 한 부분인 기능 외에도 추가적인 사용자 공간 유틸리티들이 kdump 메카니즘을 지원하는데, 위에서 언급한 kexec 유틸리티가 그것이다.\[10\]\[11\] kexec의 패치로서 제공되는 공식 유틸리티들 외에도 몇몇 [리눅스 배포판은](https://ko.wikipedia.org/wiki/리눅스_배포판 "wikilink") kdump의 동작을 단순화하는 추가적인 유틸리티들을 제공하는데 메모리 덤프 파일의 자동화된 저장의 설치가 그것이다.\[12\]\[13\]\[14\] 생성된 덤프 파일들은 GDB를 사용하거나 [레드햇](https://ko.wikipedia.org/wiki/레드햇 "wikilink")의 충돌 전용 유틸리티를 사용해서 분석될 수 있다.\[15\]\[16\]

## 역사

kdump 기능은 kexec와 함께 리눅스 커널 버전 2.6.13에 추가되었다.\[17\]

## 같이 보기

  - [debugfs](https://ko.wikipedia.org/wiki/debugfs "wikilink") - 리눅스 커널의 RAM 기반 파일 시스템으로서 디버깅 목적으로 설계되었다.
  - [kdump (BSD)](https://ko.wikipedia.org/wiki/kdump_\(BSD\) "wikilink") - ktrace 유틸리티에 의해 생성된 트레이스 파일을 보는 용도의 BSD 유틸리티.
  - [리눅스 커널 웁스](../Page/리눅스_커널_웁스.md "wikilink") - 리눅스 커널의 잠재적으로 치명치 않은 비정상적 행동.

## 각주

## 외부 링크

  -
  - [Kdump, a Kexec-based Kernel Crash Dumping Mechanism](http://lse.sourceforge.net/kdump/documentation/ols2oo5-kdump-paper.pdf), IBM, 2005, by Vivek Goyal, Eric W. Biederman, and Hariprasad Nellitheertha

[분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")

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
11.
12.
13.
14.
15.
16.
17.