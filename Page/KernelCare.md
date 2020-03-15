> This article is converted from Wikipedia: [KernelCare](https://ko.wikipedia.org/wiki/KernelCare).


**KernelCare**는 실시간 커널 패치 서비스로서 유명한 리눅스 커널들을 위한 보안 패치와 버그 수정을 제공하며\[1\] 이것은 시스템을 재부팅하지 않고서도 설치될 수 있다.\[2\]

KernelCare 소프트웨어는 [GPL2](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 하에서 배포된다. 첫 베타 버전은 2014년 3월에 공개되었으며 2014년 5월 상용으로 런치되었다. KernelCare는 [CentOS](https://ko.wikipedia.org/wiki/CentOS "wikilink")/[RHEL](https://ko.wikipedia.org/wiki/레드햇_엔터프라이즈_리눅스 "wikilink") 5.x, 6.x, 7.x; CloudLinux 5.x, 6.x and 7.x; 상응하는 클라우드 서버; Virtuozzo; [OpenVZ](https://ko.wikipedia.org/wiki/OpenVZ "wikilink"); [데비안](https://ko.wikipedia.org/wiki/데비안 "wikilink") 6.x, 7.x, 8.x; 그리고 [우분투](https://ko.wikipedia.org/wiki/우분투_\(운영_체제\) "wikilink") 14.04 LTS, 15.10을 지원한다.\[3\] \[4\]

## 개요

KernelCare 에이전트는 사용자의 서버에 상주한다. 이것은 주기적으로 KernelCare 배포 서버를 확인한다. 만약 현재 실행중인 커널을 위한 새로운 패치가 사용 가능하다면 KernelCare 에이전트는 다운로드하고 실행중인 커널에 패치를 적용한다.

KernelCare 패치는 커널에서 취약점이나 버그 코드를 대체하는데 사용되는 코드 조각들이다. 이것은 임의 코드 수정 또는 간과한 보안 검사, 함수들의 집합 또는 데이터 구조체의 수정이 될 수도 있다.\[5\] 이 패치는 보통 컴파일되지만 생성된 코드는 원본 소스 코드의 수정에 의해 야기되는 모든 수정된 코드 조각들과 이러한 코드 조각들을 어떻게 적용할지에 대한 추가적인 정보를 갖는다. 코드 수정의 결과물은 안전하게 실행 중인 커널에 적용된다.

특별한 KernelCare [커널 모듈은](../Page/적재_가능_커널_모듈.md "wikilink") 패치들을 적용시킨다. 이것은 패치들을 커널 주소 공간에 로드하고 재배치를 설정하며(즉 원본 커널 코드와 데이터에 대한 참조를 수정) 안전하게 실행 흐름을 원본 코드에서 업데이트된 코드 블록으로 전환시켜 준다. 이 코드는 패치가 안전하게 적용되었고 CPU는 새로운 버전으로 전환할 때 동시에 원본 코드 블록을 실행하지 않는다는 것을 보장한다.\[6\]\[7\]

## 같이 보기

  - [동적 소프트웨어 업데이트](https://ko.wikipedia.org/wiki/동적_소프트웨어_업데이트 "wikilink") - 프로그램이 실행 중일 때 업그레이드를 수행하는 것에 초점을 맞춘 연구 분야
  - [kexec](https://ko.wikipedia.org/wiki/kexec "wikilink") - 실행 중인 시스템에서 새로운 커널 전체를 로딩하는 기법
  - [kGraft](https://ko.wikipedia.org/wiki/kGraft "wikilink"), [kpatch](https://ko.wikipedia.org/wiki/kpatch "wikilink") 그리고 [Ksplice](https://ko.wikipedia.org/wiki/Ksplice "wikilink") - 다른 리눅스 커널 실시간 패칭 기술.

## 각주

## 외부 링크

  -
  - [Source code download](http://patches.kernelcare.com/downloads/opensource/)

[분류:C로 작성된 자유 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_보안_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.