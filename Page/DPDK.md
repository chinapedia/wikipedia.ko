> This article is converted from Wikipedia: [DPDK](https://ko.wikipedia.org/wiki/DPDK).


**DPDK**(Data Plane Development Kit)는 고속 [패킷 처리를](https://ko.wikipedia.org/wiki/패킷_처리 "wikilink") 위한 [데이터 플레인](https://ko.wikipedia.org/wiki/데이터_플레인 "wikilink")(data plane) 라이브러리와 [네트워크 인터페이스 컨트롤러](../Page/네트워크_인터페이스_컨트롤러.md "wikilink")(NIC) 드라이버의 집합이다. DPDK는 [인텔 x86](https://ko.wikipedia.org/wiki/인텔_x86 "wikilink") 프로세서를 위한 프로그래밍 프레임워크를 제공하며 빠른 속도의 데이터 패킷 네트워킹 응용 프로그램을 빠르게 개발할 수 있게 한다.\[1\]\[2\] 범위는 [인텔 아톰](../Page/인텔_아톰.md "wikilink") 프로세서에서 [인텔 제온](https://ko.wikipedia.org/wiki/인텔_제온 "wikilink") 프로세서에 이르며 [IBM 파워 8과](https://ko.wikipedia.org/wiki/IBM_파워_8 "wikilink") 같은 다른 프로세서 아키텍처의 지원도 진행 중이다.\[3\] 오픈 소스인 [BSD 라이선스](https://ko.wikipedia.org/wiki/BSD_라이선스 "wikilink") 하에 제공, 지원된다\[4\].

## 개요

DPDK 프레임워크는 환경 추상화 계층(EAL)을 만듦으로써 특정한 하드웨어/소프트웨어 환경을 위한 라이브러리 집합을 만든다.\[5\] EAL은 환경 특화 요소들을 숨기고, 사용 가능한 하드웨어 가속기와 다른 하드웨어와 운영 체제(리눅스, FreeBSD) 요소인 표준 프로그래밍 인터페이스를 라이브러리에 제공한다. 특정 환경을 위한 EAL이 만들어지면 개발자는 라이브러리에 링크하여 자신의 응용 프로그램을 만들 수 있다. 이를테면 EAL은 프레임워크를 제공하여 리눅스, FreeBSD, 인텔 IA 32/64비트, IBM 파워8을 지원할 수 있다.

또한 EAL은 시간 참조, 일반 버스 접근, 추적 및 디버그 기능 및 알람 작업을 포함한 추가 서비스를 제공한다.

DPDK는 빠른 데이터 플레인 성능을 위한 low overhead run-to-completion 모델을 구현했고, 폴링을 통해 장치에 접근하여 인터럽트 처리의 성능 오버 헤드를 제거하였다.

또한 DPDK에는 소프트웨어 아키텍처의 모범 사례를 강조하는 소프트웨어 예제, 데이터 구조 디자인 및 저장에 대한 팁, 응용 프로그램 프로파일링 및 성능 조정 유틸리티 및 일반적인 네트워크 성능 결함에 대한 팀이 포함되어 있다.

## 라이브러리

DPDK에는 다음을 위한 최적화된 NIC 드라이버와 데이터 플레인 라이브러리를 포함하고 있다:\[6\]

  - 큐 관리자는 락이 없는 큐(lockless queues)를 구현한다
  - 버퍼 관리자는 고정 크기의 버퍼를 미리 할당한다
  - 메모리 관리자는 메모리에 오브젝트의 풀을 할당하며 링을 사용하여 free object를 저장한다. 모든 DRAM 채널에서 객체가 균등하게 분산되도록 한다.
  - 폴 모드 드라이버(PMD)는 비동기 통보 없이 동작하도록 설계되었으며 부하를 감소시킨다.
  - 패킷 프레임워크는 패킷 처리 개발을 도와주는 라이브러리의 집합이다.

모든 라이브러리는 dpdk/lib/librte_\* 디렉터리에 저장된다.

### 플러그인

DPDK에는 다양한 하드웨어 유형의 드라이버가 포함되어 있다.\[7\] 과거에는 몇가지 추가적인 out-of-tree 플러그인이 있었지만, 이제는 사용되지 않는다.

  - [`librte_pmd_virtio.so`](http://dpdk.org/browse/virtio-net-pmd/refs/)
  - [`librte_pmd_vmxnet3.so`](http://www.dpdk.org/browse/vmxnet3-usermap/refs/)
  - [`librte_pmd_memnic_copy.so`](http://www.dpdk.org/browse/memnic/refs/)
  - `librte_pmd_mlx4.so`
  - `librte_crypto_nitrox.so`
  - `librte_crypto_quickassist.so`

## 환경

DPDK는 원래 지원되지 않는 베어 메탈 모드를 사용하여 실행되도록 설계되었다. 실제로 DPDK의 EAL은 Linux 또는 FreeBSD 사용자 영역 응용 프로그램을 지원한다.

EAL은 모든 프로세서를 지원하기 위해 확장될 수 있다.

## 각주

[분류:라우터](https://ko.wikipedia.org/wiki/분류:라우터 "wikilink") [분류:컴퓨터 네트워킹](https://ko.wikipedia.org/wiki/분류:컴퓨터_네트워킹 "wikilink") [분류:가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:가상화_소프트웨어 "wikilink") [분류:이더넷](https://ko.wikipedia.org/wiki/분류:이더넷 "wikilink") [분류:리눅스 재단 프로젝트](https://ko.wikipedia.org/wiki/분류:리눅스_재단_프로젝트 "wikilink")

1.  Simon Stanley,[All Change for Packet Processing](http://www.heavyreading.com/commchip/document.asp?doc_id=228565) , Heavy Reading, 2013
2.  Shamus McGillicudy, [Intel DPDK, switch and server ref designs push SDN ecosystem forward](http://searchsdn.techtarget.com/news/2240182264/Intel-DPDK-switch-and-server-ref-designs-push-SDN-ecosystem-forward), SearchSDN, April 2013
3.
4.  Simon Stanley,[DPDK Goes Open-Source](http://embedded.communities.intel.com/community/en/software/blog/2013/05/16/roving-reporter-dpdk-goes-open-source) , Intel Embedded Community, May 2013
5.  Intel Corporation, [Intel® Data Plane Development Kit: Programmers Guide](http://www.intel.com/content/www/us/en/intelligent-systems/intel-technology/intel-dpdk-programmers-guide.html), November 2012
6.
7.