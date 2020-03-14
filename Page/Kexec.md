> This article is converted from Wikipedia: [Kexec](https://ko.wikipedia.org/wiki/Kexec).


**kexec**은 현재 돌아가는 커널에 새로운 커널을 부팅하게 하는 [리눅스 커널의](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 메커니즘이다. 근본적으로 kexec는 [부트로더](https://ko.wikipedia.org/wiki/부트로더 "wikilink") 단계와 하드웨어 초기화 단계를 건너뛰며 직접적으로 새로운 커널을 메인 메모리에 로드하고 즉시 실행한다. 이것은 전체 리부팅과 관련된 긴 시간을 피하고 [다운타임](https://ko.wikipedia.org/wiki/다운타임 "wikilink")을 최소화 시킴으로써 시스템이 높은 가용성을 충족하게 한다.\[1\]\[2\]

실현 가능케하기 위해 kexec는 다음의 두 가지 메커니즘을 구현해야 한다.

  - 현재 진행 중인 커널의 메모리는 돌아가는 도중에 새로운 커널에 의해 덮어써진다.
  - 새로운 커널은 일반적으로 모든 하드웨어 장치들이 잘 정의된 상태라고 가정한다. 실제 리부팅을 우회하는 것은 장치들을 알려지지 않은 상태로 남기며 새로운 커널은 이 상태에서 회복되어야 한다.

오직 사인된 커널만 kexec에 의해서 부트되게 지원하기 위해 리눅스 커널의 3.17부터 추가되었다.\[3\] 이것은 루트 사용자가 임의의 코드를 kexec를 통해 로드하고 실행하는 것을 불허하며 오직 사인된 리눅스 커널 모듈만 실행 중인 커널에 삽입될 수 있다.\[4\]\[5\]\[6\]

## 같이 보기

  - [kdump](https://ko.wikipedia.org/wiki/kdump "wikilink") - 내부적으로 kexec를 사용하는 리눅스 커널의 충돌 덤프 메커니즘
  - [kGraft](https://ko.wikipedia.org/wiki/kGraft "wikilink") - SUSE에 의해 개발된 리눅스 커널 라이브 패치 기법
  - [kpatch](https://ko.wikipedia.org/wiki/kpatch "wikilink") - 레드햇에 의해 개발된 리눅스 커널 라이브 패치 기법
  - [Ksplice](https://ko.wikipedia.org/wiki/Ksplice "wikilink") - Ksplice 사에 의해 개발된 리눅스 커널 라이브 패치 기법

## 각주

## 외부 링크

  - [Using kexec and kdump to get core files on Fedora and CentOS hosts](http://prefetch.net/blog/index.php/2009/07/06/using-kdump-to-get-core-files-on-fedora-and-centos-hosts/)

[분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink")

1.
2.
3.
4.
5.
6.