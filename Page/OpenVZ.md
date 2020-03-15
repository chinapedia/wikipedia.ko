> This article is converted from Wikipedia: [OpenVZ](https://ko.wikipedia.org/wiki/OpenVZ).


**OpenVZ**은 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 기반에서 운영 체제 수준에서의 가상화를 지원하는 솔루션이다. OpenVZ은 1개의 물리적 서버에 여러 개의 독립된 VPS(가상 독립 서버,Virtual Private Servers) 또는 VE(가상환경,Virtual Environments)와 같은 운영 체제 인스턴스를 실행할 수 있다.

이 가상 머신은 보통 [VMWare](https://ko.wikipedia.org/wiki/VMWare "wikilink")나 [반가상화](https://ko.wikipedia.org/wiki/반가상화 "wikilink")(paravirtualization)을 지원하는 [Xen](https://ko.wikipedia.org/wiki/Xen "wikilink")과 비교되곤 하는데, OpenVZ은 호스트와 게스트 시스템 모두 동일한 리눅스 운영체계로 실행되어야 한다.(단, VE 사이에서 리눅스 배포판이 서로 다를 수는 있다.) 하지만, OpenVZ는 이런 단점에도 불구하고 높은 성능에 대한 장점을 가지고 있는데, 공식 웹 사이트에 따르면 OpenVZ의 경우 단독 서버에 비해 겨우 1\~3% 정도의 성능 저하만 존재한다고 한다.\[1\] OpenVZ는 수정된 [리눅스 커널과](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 사용자 수준의 관리 도구로 이루어져 있다.

OpenVZ는 [페러럴즈](https://ko.wikipedia.org/wiki/페러럴즈 "wikilink")에서 상용으로 제공 중인 [Virtuozzo](https://ko.wikipedia.org/wiki/Virtuozzo "wikilink")의 기반 시스템이며, GPL 라이선스 2에 의해서 배포된다.

## 커널

OpenVZ는 가상환경(Virtual Envroments, VE)를 지원하기 위해서 수정된 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 커널을 사용한다. 이 커널은 가상화, 격리, 자원 관리, 체크포인트 등을 지원한다.

### 가상화와 격리

각각의 VE는 각 가상화 단위로 분리되며, 각각의 물리적 하드웨어를 가진 서버와 같이 작동한다.

  - 파일
    각각 분리된 시스템 라이브러리, 응용 소프트웨어, 그리고 **가상화된** `/proc`와 `/sys`, 가상화된 락(locks)을 제공한다.

<!-- end list -->

  - 사용자 및 그룹
    VE마다 별도의 root 사용자를 가지고, 사용자와 그룹을 자유롭게 할당할 수 있다. 생성된 root와 사용자 계정 등은 호스트 시스템에 영향을 미치지 않는다.

<!-- end list -->

  - 프로세스
    VE는 자신만의 프로세스가 할당되며, PID 역시 가상화된다. VE 내의 *init*의 PID는 1이다.

<!-- end list -->

  - 네트워크
    VE의 가상 네트워크 장비는 별도의 IP 주소를 할당 받을 수 있으며, iptables 및 라우팅 규칙을 설정할 수 있다.

<!-- end list -->

  - 장치
    필요하다면 VE는 실제 물리적 네트워크 장치 및 직렬 포트, 디스크 파티션을 읽을 수 있도록 허가 받을 수 있다.

<!-- end list -->

  - IPC 객체
    [공유 메모리](https://ko.wikipedia.org/wiki/공유_메모리 "wikilink"), [세마포어](https://ko.wikipedia.org/wiki/세마포어 "wikilink"), 메시지 시스템 등을 제공한다.

### 자원 관리

OpenVZ은 2단계 디스크 할당 제한(Disk quota), 공평한 CPU 스케줄러, 사용자별 통계 등의 3가지 리소스 관리 방법을 제공한다. 할당된 리소스는 VE가 실행되는 동안 변경될 수 있으며, 다시 시작하면 소멸된다.

  - 2단계 디스크 할당 제한

각각의 VE는 자신의 디스크 할당 양을 가지고 있으며, 보통 디스크 블록의 크기나 [inode](https://ko.wikipedia.org/wiki/inode "wikilink")(통상적으로 파일의 숫자)로 나타낼 수 있다. 이와 별도로 VE 내부에서는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink")에서 제공하는 사용자별 또는 그룹별 디스크 할당 제한을 별도로 설정할 수 있다.

  - CPU 스케줄러

OpenVZ는 2단계의 공평한 CPU 스케줄러를 제공한다. 첫 번째 단계어서 각 VE는 VE별로 할당된 CPU 할당 제한 값에 기반하여 CPU 시간을 제공받을 수 있는지 결정한다. 두 번째 단계에서 표준 리눅스 스케줄러는 VE에 실제 프로세스 스케줄을 할당한다. 각각의 VE별로 별도로 CPU 할당 값을 설정할 수 있으며, 실제 CPU에서는 이 값을 비율로 계산하여 할당한다.

  - 입출력 스케줄러

<!-- end list -->

  - 사용자 통계

## 참조

<references />

## 외부 링크

  -
  - [OpenVZ 위키](https://web.archive.org/web/20080820003919/http://wiki.openvz.org/)

  - [다른 가상화 기술과의 비교](http://wiki.openvz.org/Introduction_to_virtualization)

  - [OpenVZ 커널 해커 인터뷰](https://archive.is/20121220232413/kerneltrap.org/node/6492)

  - [EasyVZ: OpenVZ 관리 GUI](http://binarykarma.com/)

[분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:시스템_소프트웨어 "wikilink") [분류:자유 가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_가상화_소프트웨어 "wikilink")

1.  Official OpenVZ web site, <http://openvz.org/>