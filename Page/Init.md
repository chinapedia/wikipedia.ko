> This article is converted from Wikipedia: [Init](https://ko.wikipedia.org/wiki/Init).


[thumb](https://ko.wikipedia.org/wiki/파일:Version_7_UNIX_SIMH_PDP11_Etc.png "wikilink"): `/etc`를 나열할 때 `init`와 `rc`가 보인다.\]\] [thumb](https://ko.wikipedia.org/wiki/파일:Version_7_UNIX_SIMH_PDP11_Etc_Rc.png "wikilink") 스크립트 `/etc/rc`의 내용.\]\] [유닉스](../Page/유닉스.md "wikilink") 기반 컴퓨터 [운영 체제에서](../Page/운영_체제.md "wikilink") **init**은 컴퓨터 시스템의 [부팅](../Page/부팅.md "wikilink") 과정 중 최초의 [프로세스](../Page/프로세스.md "wikilink")이다. Init은 시스템이 종료될 때까지 계속 실행하는 [데몬](../Page/데몬_\(컴퓨팅\).md "wikilink") 프로세스이다. 다른 모든 프로세스의 직간접 [부모 프로세스이며](https://ko.wikipedia.org/wiki/부모_프로세스 "wikilink") 자동으로 [고아 프로세스들을](https://ko.wikipedia.org/wiki/고아_프로세스 "wikilink") 입양한다. Init은 [하드 코딩된](https://ko.wikipedia.org/wiki/하드_코딩 "wikilink") [파일 이름을](../Page/파일_이름.md "wikilink") 이용하여 [커널에](../Page/커널_\(컴퓨팅\).md "wikilink") 의해 시작된다. 커널이 이를 시작할 수 없으면 [커널 패닉이](../Page/커널_패닉.md "wikilink") 발생한다. Init은 일반적으로 [프로세스 식별자](../Page/프로세스_식별자.md "wikilink") 1로 할당된다.

## 리서치 유닉스 스타일/BSD 스타일

[리서치 유닉스의](https://ko.wikipedia.org/wiki/리서치_유닉스 "wikilink") init은 /etc/rc에 위치한 셸 스크립트를 실행한 다음, /etc/ttys가 통제하는, 터미널의 [getty를](https://ko.wikipedia.org/wiki/getty_\(유닉스\) "wikilink") 실행하였다. 실행 수준은 존재하지 않는데, /etc/rc 파일이 init에 의한 프로그램의 실행을 정의한다. 이 시스템의 이점은 수동 편집이 단순하고 쉽다는 것이다. 그러나 시스템에 추가된 새로운 소프트웨어는 기존 파일에 대한 변경이 필요한데 시스템의 부팅을 불가능하게 만들 수 있다.

## SysV 스타일

이전과 비교할 때 AT\&T의 [유닉스 시스템 III은](https://ko.wikipedia.org/wiki/유닉스_시스템_III "wikilink") 새로운 스타일의 시스템 시작 구성을 도입하였으며,\[1\] 이러한 수정 사항들과 더불어 [유닉스 시스템 V로](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") 새로 태어났는데, 이를 "SysV 스타일 init"이라 부른다.

### 실행 수준

System V의 [실행 수준은](https://ko.wikipedia.org/wiki/실행_수준 "wikilink") 기기의 특정한 상태를 기술하며, 프로세스와 데몬에 의해 결정된다. 일반적으로 8개의 실행 수준이 있으며, 그 중 3개는 표준으로 간주되는 운영 체제의 필수 부분이다.:

  -
    0\. 중단(Halt)
    1\. [단일 사용자 모드](https://ko.wikipedia.org/wiki/단일_사용자_모드 "wikilink") (S 또는 s)
    6\. [재기동](https://ko.wikipedia.org/wiki/재기동 "wikilink")

이 표준들 외에 유닉스 및 유닉스 계열 운영 체제들은 실행 수준을 조금 다르게 처리한다. 공통 분모인 `/etc/inittab` 파일은 시스템에서의실행 수준의 설정을 정의한다.

### 기본 실행 수준

| 운영 체제                                                                        | 기본 실행 수준                    |
| ---------------------------------------------------------------------------- | --------------------------- |
| [AIX](https://ko.wikipedia.org/wiki/AIX "wikilink")                          | 2                           |
| [젠투 리눅스](../Page/젠투_리눅스.md "wikilink")                                       | 3\[2\]                      |
| [HP-UX](../Page/HP-UX.md "wikilink")                                         | 3 (콘솔/서버/다중 사용자) 또는 4 (그래픽) |
| [슬랙웨어 리눅스](https://ko.wikipedia.org/wiki/슬랙웨어_리눅스 "wikilink")                | 3                           |
| [솔라리스](../Page/솔라리스_\(운영_체제\).md "wikilink")                                 | 3\[3\]                      |
| [유닉스 시스템 V](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") 릴리스 3.x, 4.x | 2                           |
| [유닉스웨어](../Page/유닉스웨어.md "wikilink") 7.x                                     | 3                           |

오른쪽 표에서 실행 수준 5를 기본으로 하는 리눅스 배포판의 경우, 실행 수준 5는 [X 윈도 시스템을](../Page/X_윈도_시스템.md "wikilink") 실행 중인 다중 사용자 그래픽 환경을 호출하며, 일반적으로 [GDM이나](https://ko.wikipedia.org/wiki/그놈_디스플레이_매니저 "wikilink") [KDM과](https://ko.wikipedia.org/wiki/KDE_디스플레이_매니저 "wikilink") 같은 [디스플레이 매니저를](https://ko.wikipedia.org/wiki/X_디스플레이_매니저 "wikilink") 동반한다. 그러나 [솔라리스](../Page/솔라리스_\(운영_체제\).md "wikilink") 운영 체제는 일반적으로 실행 수준 5를 종료 및 기기의 전원 끄기를 수행한다.

## init의 대안

  - [BootScripts](https://ko.wikipedia.org/wiki/고보리눅스 "wikilink")
  - [busybox-init](../Page/비지박스.md "wikilink")
  - [DEMONS](https://ko.wikipedia.org/wiki/DEMONS "wikilink")
  - eINIT
  - [Epoch](https://ko.wikipedia.org/wiki/Epoch "wikilink")
  - [Initng](https://ko.wikipedia.org/wiki/Initng "wikilink")
  - [launchd](https://ko.wikipedia.org/wiki/launchd "wikilink")
  - Mudur
  - nosh
  - [OpenRC](https://ko.wikipedia.org/wiki/OpenRC "wikilink")
  - [runit](https://ko.wikipedia.org/wiki/runit "wikilink")
  - s6
  - [서비스 관리 기능](https://ko.wikipedia.org/wiki/서비스_관리_기능 "wikilink")
  - [셰퍼드](../Page/셰퍼드.md "wikilink")
  - [systemd](https://ko.wikipedia.org/wiki/systemd "wikilink")
  - [SystemStarter](https://ko.wikipedia.org/wiki/SystemStarter "wikilink")
  - [Upstart](https://ko.wikipedia.org/wiki/Upstart "wikilink")

## 각주

## 외부 링크

  - [FreeBSD init man page](http://www.freebsd.org/cgi/man.cgi?query=init&apropos=0&sektion=0&manpath=FreeBSD+6.2-stable&format=html)

  - [A paper summarizing Unix init schemes](http://arxiv.org/abs/0706.2748) (2007)

  -

  - [A history of modern init systems (1992–2015)](http://blog.darknedgy.net/technology/2015/09/05/0/)

[분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")

1.
2.
3.