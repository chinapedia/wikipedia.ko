> This article is converted from Wikipedia: [LXC](https://ko.wikipedia.org/wiki/LXC).


**LXC** (LinuX Containers)는 단일 컨트롤 호스트 상에서 여러 개의 고립된 리눅스 시스템 (컨테이너)들을 실행하기 위한 운영 시스템 레벨 가상화 방법이다. 리눅스 커널은 cgroups를 절충하여 가상화 머신을 시작할 필요 없이 자원 할당 (CPU, 메모리, 블록 I/O, 네트워크 등)을 한다. Cgroups는 또한 애플리케이션 입장에서 프로세스 트리, 네트워크, 사용자 ID, 마운트된 파일 시스템 등의 운영 환경을 완전히 고립시키기 위해 namespace isolation을 제공한다. LXC는 cgroups와 namespace를 결합하여 애플리케이션을 위한 고립된 환경을 제공한다. [도커](https://ko.wikipedia.org/wiki/도커_\(소프트웨어\) "wikilink")(Docker) 또한 실행 드라이버의 하나로 LXC를 사용할 수 있으며 이를 통해 이미지 관리와 개발 서비스를 제공한다.

## 개요

LXC는 완전한 가상머신을 작성하는 대신 자신의 고유한 프로세스와 네트워크 스페이스를 가지는 가상 환경을 통해 운영 시스템 레벨의 가상화를 제공한다. LXC는 리눅스 버전 2.6.24에서 릴리즈된 리눅스 커널 cgroups 기능에 의존한다. 이는 또한 메인라인 리눅스 커널에 통합되어 있는 namespace-고립 기능에도 의존한다.

## 보안

원래 LXC 컨테이너는 OpenVZ와 같은 다른 OS-레벨 가상화 방법에 비해 보안수준이 안전하지 않았다: 3.8 이전의 리눅스 커널에서는 게스트 시스템의 root 사용자가 root 권한으로 호스트 시스템 상에서 임의의 코드를 실행할 수 있었다.  1.0 릴리즈부터 컨테이너는 “unprivileged containers”를 사용하여 호스트 상의 일반 사용자로 실행된다. Unprivileged containers는 직접 하드웨어에 접근할 수 없도록 제한된다. 그럼에도 불구하고 제대로 구성된다면 1.0 보안 모델에서도 privileged containers는 적절한 고립을 제공할 수 있다.

## 대안

LXC는 OpenVZ나 Linux-VServer와 같은 다른 리눅스 OS-레벨 가상화 테크놀로지와 유사하며 다른 OS에서는 FreeBSD jails, AIX Workload Partitions, Solaris Containers와 같은 OS-레벨 가상화 테크놀로지가 있다. OpenVZ와 달리, LXC는 vanilla Linux kernel에서 커널 소스에 추가적인 패치를 적용할 필요 없이 동작한다. LXC 버전 1은 2014년 2월 20일 릴리즈되었으며 향후 5년간 지원될 예정이다.

## 각주

## 외부 링크

  -
  - [IBM developerworks article about LXC](http://www.ibm.com/developerworks/linux/library/l-lxc-containers/)

  - ["Evading from Linux Containers" by Marco D'Itri](http://blog.bofh.it/debian/id_413)

  - [Presentation about cgroups and namespaces, the underlying technology of Linux containers, by Rami Rosen](http://www.haifux.org/lectures/299/netLec7.pdf)

  - [Presentation about Linux Containers and the future cloud, by Rami Rosen](http://haifux.org/lectures/320/netLec8_final.pdf)

  - [LXC : Install and configure the Linux Containers](https://wiki.deimos.fr/LXC_:_Install_and_configure_the_Linux_Containers)

  - [LSS: Secure Linux containers](https://lwn.net/Articles/515034/) (LWN.net)

  - [Introduction to Linux Containers](http://z900collector.wordpress.com/linux/containers/)

[분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink") [분류:자유 가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_가상화_소프트웨어 "wikilink")