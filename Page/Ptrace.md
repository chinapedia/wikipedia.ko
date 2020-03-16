> This article is converted from Wikipedia: [Ptrace](https://ko.wikipedia.org/wiki/Ptrace).


**ptrace**는 여러 [유닉스](../Page/유닉스.md "wikilink")와 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제에서 발견되는 [시스템 호출이다](../Page/시스템_호출.md "wikilink"). ptrace(이 이름은 "process trace"의 축약형이다)를 통해 컨트롤러가 대상의 내부 상태를 조사하고 조작하게 함으로써, 한 [프로세스](../Page/프로세스.md "wikilink")가 다른 프로세스를 제어할 수 있다. ptrace는 [디버거](../Page/디버거.md "wikilink")와 다른 코드 분석, 특히 소프트웨어 개발을 도와주는 도구들에서 사용된다.

## 사용

ptrace는 디버거([gdb](https://ko.wikipedia.org/wiki/gdb "wikilink") 같은), [strace](https://ko.wikipedia.org/wiki/strace "wikilink")와 [ltrace](https://ko.wikipedia.org/wiki/ltrace "wikilink") 같은 트레이싱 툴 그리고 [코드 커버리지](../Page/코드_커버리지.md "wikilink") 툴들에서 사용된다. ptrace는 또한 고쳐지지 않은 버그를 피하거나 보안 특성들을 극복하기 위한 특별한 프로그램들에 의해 실행 중인 프로그램들을 패치하는데 사용되기도 한다. 이것은 더 나아가 [샌드박스](https://ko.wikipedia.org/wiki/샌드박스_\(컴퓨터_보안\) "wikilink")\[1\]\[2\]로서 그리고 런타임 환경 시뮬레이터(비-루트 소프트웨어를 위한 루트 접근을 에뮬레이팅하는 것 같이\[3\]\[4\])로서 사용되기도 한다.

ptrace 호출을 사용해서 다른 프로세스를 어태치함으로써, 툴은 대상의 연산에 대한 광범위한 제어를 갖는다. 이것은 [파일 서술자](../Page/파일_서술자.md "wikilink"), 메모리 그리고 [레지스터에](../Page/프로세서_레지스터.md "wikilink") 대한 조작을 포함한다. 또한 대상의 코드를 싱글 스텝핑하고, 시스템 호출과 그 결과를 가로채며 대상의 [시그널](../Page/유닉스_신호.md "wikilink") 핸들러와 행동에 대한 주고 받는 시그널들을 조작할 수도 있다. 대상의 메모리에 쓸 수 있는 권한은 단지 대상의 데이터 저장소가 아니라 애플리케이션의 코드 세그먼트도 포함하며, 컨트롤러가 대상의 실행 중인 코드에 [브레이크포인트](../Page/브레이크포인트.md "wikilink")를 설치하고 패치할 수 있게 한다.\[5\]

다른 프로세스를 조사하고 바꾸는 능력이 매우 강력함에 따라, ptrace는 오직 소유자가 시그널을 보낼 수 있는 프로세스들만 어태치할 수 있다(일반적으로 자신의 프로세스들); [슈퍼 유저](https://ko.wikipedia.org/wiki/슈퍼_유저 "wikilink") 계정은 거의 대부분의 프로세스를 ptrace할 수 있다(커널 2.6.26 이전 버전에서 init을 제외하고). capabilities 기반 보안의 특징을 갖는 리눅스 시스템들에서 ptrace의 능력은 CAP_SYS_PTRACE capability\[6\] 또는 YAMA [리눅스 보안 모듈에](../Page/리눅스_보안_모듈.md "wikilink") 의해 제한된다.\[7\] [FreeBSD](../Page/FreeBSD.md "wikilink")에서는 FreeBSD jail과 강제적 접근 통제 정책들에 의해 제한된다.

## 제한

컨트롤러와 대상 사이의 통신들은, 고정된 작은 크기의 메모리 블록을 둘 사이에 전달하는 ptrace의 반복되는 호출들을 사용해서 이뤄진다(호출 마다 두 [문맥 교환을](https://ko.wikipedia.org/wiki/문맥_교환 "wikilink") 필요로하는); 이것은 오직 워드 크기의 블록들을 통해서 수행됨으로 인해 대상의 메모리의 큰 양에 접근할 때 상당한 비효율을 보인다(각 워드마다 ptrace 호출이 필요하다).\[8\] 이 이유로 유닉스의 8th 에디션은 procfs를 도입하였는데, 이것은 다른 프로세스의 메모리에 대한 직접적인 접근을 허용한다 - 디버거 지원을 위한 `/proc`의 사용은 솔라리스, BSD, AIX에서도 지원되며 리눅스도 이것과 거의 비슷하게 카피하였다.\[9\] 솔라리스 같은 몇몇은 시스템 호출로서의 ptrace를 완전히 제거하고, 이것의 호출을 플랫폼의 procfs로 변환하는 라이브러리 호출로 고정시켰다.\[10\] 이러한 시스템들은 제어받는 프로세스에 명령어를 보내기 위해 열린 /proc 파일의 파일 서술자에 [ioctls를](../Page/Ioctl.md "wikilink") 사용한다.\[11\]

ptrace는 디버거와 그것과 비슷한 툴들을 지원하는데 필요한 단지 가장 기본적인 인터페이스를 제공한다. 이것을 사용하는 프로그램은 반드시 스택 레이아웃, [응용 프로그램 이진 인터페이스](../Page/응용_프로그램_이진_인터페이스.md "wikilink"), [시스템 호출](../Page/시스템_호출.md "wikilink") 메커니즘, 네임 맹글링, 디버그 데이터의 포맷 그리고 [기계어](../Page/기계어.md "wikilink")의 디스어셈블링에 대한 이해 같은 운영체제와 아키텍처에 대한 구체적인 지식을 알아야 한다. 더 나아가 대상 프로세스에 실행 가능한 코드를 삽입하는(gdb 같이) 또는 사용자가 대상의 문맥에 명령어를 입력할 수 있게 하는 프로그램은 [프로그램 로더의](https://ko.wikipedia.org/wiki/로더_\(컴퓨팅\) "wikilink") 도움 없이 반드시 자신의 코드를 스스로 생성하고 로드해야 한다.

## 지원

ptrace는 리눅스를 포함한 여러 유닉스 계열들에서 지원된다.

리눅스는 또한 프로세스들에게 다른 프로세스들이 자신을 어태치하는 것을 막는 능력을 준다. 프로세스들은 `prctl` syscall을 호출할 수 있으며 자신의 `PR_SET_DUMPABLE` 플래그를 클리어할 수 있다; 최근 커널들에서 이것은 비-루트 프로세스들이 호출하는 프로세스를 ptrace하는 것을 막는다; [OpenSSH](../Page/오픈SSH.md "wikilink") 인증 에이전트는 이 메커니즘을 ptrace를 통한 ssh 세션 하이재킹을 막는데 사용한다.\[12\]\[13\]\[14\]

이 특징이 활성화된 시스템에서 "`gdb --attach`"와 "`strace -p`" 같은 명령어들은 통하지 않을 것이다. ptrace_scope 제한의 알려진 의도는 더 나은 보안이었지만, 이것이 단지 보안 연극(security theater)이라는 것은 쉽게 알아챌 수 있다; 사용자의 계정을 크랙한 공격자는 ptrace를 다른 의도로 사용함으로써 쉽게 의도를 달성할 수 있다.

잠긴 부트 로더를 가진 몇몇 안드로이드 폰들에서 ptrace는 '2nd 부트'를 활성화하고 시스템 파일들을 대체하기 위해 init 프로세스에 대한 통제를 얻는데 사용될 수 있다.

## 각주

## 외부 링크

  - [Article from Linux Gazette about ptrace](https://web.archive.org/web/20100330123847/http://tldp.org/LDP/LGNET/81/sandeep.html)
  - [Article about ptrace in linux journal](http://www.linuxjournal.com/article/6100)

[분류:디버깅](https://ko.wikipedia.org/wiki/분류:디버깅 "wikilink") [분류:유닉스](https://ko.wikipedia.org/wiki/분류:유닉스 "wikilink")

1.  [sydbox](http://freecode.com/projects/sydbox)
2.  [PRoot](http://proot.me)
3.
4.
5.
6.
7.  [Yama.txt in Linux Git](https://www.kernel.org/doc/Documentation/security/Yama.txt)
8.
9.
10.
11.
12.
13.
14.