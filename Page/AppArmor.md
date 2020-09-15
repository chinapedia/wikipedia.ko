> This article is converted from Wikipedia: [AppArmor](https://ko.wikipedia.org/wiki/AppArmor).


**AppArmor** ("Application Armor")는 시스템 관리자가 프로그램 프로필 별로 프로그램의 역량을 제한할 수 있게 해주는 [리눅스 커널](../Page/리눅스_커널.md "wikilink") [보안 모듈이다](../Page/리눅스_보안_모듈.md "wikilink"). 프로필들은 네트워크 액세스, raw 소켓 액세스 그리고 파일의 읽기, 쓰기, 실행 같은 능력을 허용할 수 있다. AppArmor는 강제적 접근 통제(MAC)를 제공함으로써 전통적인 유닉스 임의적 접근 통제(DAC) 모델을 지원한다. 이것은 리눅스 버전 2.6.36부터 포함되었으며, 개발은 2009년부터 [캐노니컬](../Page/캐노니컬.md "wikilink") 사에 의해 지원된다.

## 상세

직접적으로 프로필을 작성하는 대신, AppArmor는 프로필 위반이 기록되지만 금지되지는 않는 학습 모드를 포함한다. 이 기록은 프로그램의 일반적인 행위에 기반한 Apparmor 프로필을 생성하는데 사용될 수 있다.

AppArmor는 [리눅스 보안 모듈](../Page/리눅스_보안_모듈.md "wikilink")(LSM) 커널 인터페이스를 사용해서 구현되었다.

AppArmor는 [SELinux를](../Page/보안_강화_리눅스.md "wikilink") 대체하는 한 부분으로서 제공되는데, 이것이 관리자들에게 설치하고 관리하기 어렵다는 비판이 있었기 때문이다.\[1\] 파일에 라벨을 적용하는 것에 기반하는 SELinux와는 달리, AppArmor는 파일 경로를 통해 작동한다. AppArmor의 지지자들은 평범한 사용자들에게는 SELinux를 배우는 것보다 훨씬 쉽다고 주장한다.\[2\] 그들은 또한 AppArmor이 현재 시스템과 동작하기 위해 더 적은 수정을 요구한다고 주장한다: 예를 들면 SELinux는 "security labels"를 지원하는 파일시스템을 요구해서 NFS를 통해 마운트된 파일들에 대한 접근 통제를 제공할 수 없다. AppArmor는 파일시스템에 상관이 없다.

## 다른 시스템들

AppArmor는 설치된 소프트웨어에서 발생할 수 있는 행위들을 제어하는 문제에 여러 가능한 접근법을 나타낸다.

[SELinux](../Page/보안_강화_리눅스.md "wikilink") 시스템은 일반적으로 AppArmor과 비슷한 접근법을 취한다. 한가지 중요한 차이점은 SELinux는 경로 대신 아이노드 번호로 파일 시스템 객체들을 구별한다. 예를 들면 이것은 하드 링크가 생성됐을 때 [아이노드](../Page/아이노드.md "wikilink")에 참조되는 데이터가 같을 것이기 때문에 SELinux가 계속 새로 생성된 하드 링크에 대한 접근을 거부하는 것과 달리 AppArmor에서는 접근 가능해 진다.

SELinux와 AppArmor는 또한 어떻게 관리되는지와 어떻게 시스템에 통합되는지에 대해서 큰 차이를 보인다.

프로세스의 고립은 또한 가상화 같은 메커니즘을 통해 성취될 수 있다; Vserver에서 [OLPC](../Page/OLPC.md "wikilink") 프로젝트는 개개의 애플리케이션들을 샌드박스한다.

2007년에 [Smack_(소프트웨어)](../Page/Smack_\(소프트웨어\).md "wikilink")이 도입되었다.

2009년에 Tomoyo로 불리는 새로운 솔루션이 리눅스 2.6.30에 포함되었다; appArmor처럼 이것도 경로 기반 접근 통제를 사용한다.

### 사용

AppArmor는 2007년 4월 우분투에서 처음으로 성공적으로 포트/패키지되었다. 우분투 7.10부터는 기본 패키지가 되었으며 8.04부터는 단지 디폴트로 CUPS를 보호하는 릴리즈의 한 부분이 되었다. 우분투 9.04를 시작으로 MySQL 같은 여러 요소들이 설치된 프로필들을 가지게 되었다. 우분투 9.10에서 AppArmor는 개선이 강화되었고 자신의 게스트 세션, libvirt 가상 머신 등과 함께 제공되었다.\[3\]

AppArmor는 2010년 10월 커널 릴리즈 2.6.36에 통합되었다.\[4\]\[5\]\[6\]\[7\]

AppArmor는 2014년 Synology의 DSM 5.1 베타에 통합되었다.\[8\]

## 같이 보기

  - [리눅스 침입 탐지 시스템](https://ko.wikipedia.org/wiki/리눅스_침입_탐지_시스템 "wikilink")
  - [Systrace](https://ko.wikipedia.org/wiki/Systrace "wikilink")

## 각주

## 외부 링크

  - [AppArmor Wiki](http://wiki.apparmor.net/index.php/Main_Page)
  - [AppArmor](https://web.archive.org/web/20150921153747/https://en.opensuse.org/SDB:AppArmor) description from openSUSE.org
  - [LKML thread](https://lkml.org/lkml/2006/4/19/199) containing comments and criticism of AppArmor
  - [Apparmor packages for Ubuntu](https://wiki.ubuntu.com/AppArmor)
  - [Counterpoint:](http://www.linux-magazine.com/issues/2006/69/counterpoint) Novell and Red Hat security experts face off on AppArmor and SELinux
  - <http://www.novell.com/linux/security/apparmor/>

[분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.