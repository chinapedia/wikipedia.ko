> This article is converted from Wikipedia: [Procfs](https://ko.wikipedia.org/wiki/Procfs).


**proc 파일시스템** (**procfs**)은 유닉스 계열 운영 체제에서 프로세스와 다른 시스템 정보를 계층적 파일 구조 같은 형식으로 보여주는 특별한 파일시스템으로서, 전통적인 트레이싱 방식이나 커널 메모리로의 간접적인 접근 보다는 더 편리하고 표준적인 방식인 동적으로 커널이 소유하는 프로세스 데이터에 접근하는 방식을 제공한다. 일반적으로 이것은 부트 타임에 */proc* 라는 이름의 마운트 포인트에 매핑된다. proc 파일 시스템은 커널에서 내부 데이터 구조체에 대한 인터페이스 처럼 행동하며 런타임(sysctl) 시에 특정한 커널 파라미터를 바꾸고 시스템에 대한 정보를 얻는데 사용될 수 있다.

[솔라리스](../Page/솔라리스_\(운영_체제\).md "wikilink"), [IRIX](../Page/IRIX.md "wikilink"), [BSD](../Page/BSD.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [AIX](../Page/IBM_AIX.md "wikilink") 등의 수많은 유닉스 계열 운영 체제들이 proc 파일시스템을 지원한다. 리눅스 커널은 이것을 프로세스와 관련 없는 데이터까지 확장하였다.

Proc 파일시스템은 커널 영역과 사용자 영역 사이의 통신에 대한 방식을 제공한다. 예를 들면 프로세스 리포팅 유틸리티 [ps의](../Page/Ps_\(유닉스\).md "wikilink") [GNU](../Page/GNU.md "wikilink") 버전은 proc 파일 시스템을 어떤 특별한 [시스템 호출의](../Page/시스템_호출.md "wikilink") 사용 없이 자신의 데이터를 얻는데 사용한다.

## 역사

### 리눅스

리눅스에서 /proc은 커널 프로세스를 포함하는 각 실행 중인 프로세스들을 위한 디렉토리를 포함하며 디렉토리는 /proc/PID라는 이름을 갖는다(PID는 프로세스 번호이다). 각 디렉토리는 한 프로세스에 관한 정보 뿐만 아니라 다음을 포함한다:

  - /proc/PID/cmdline, 프로세스를 시작한 명령어.
  - /proc/PID/cwd, 프로세스의 현재 [작업 디렉토리에](../Page/작업_디렉토리.md "wikilink") 대한 [심볼릭 링크](../Page/심볼릭_링크.md "wikilink").
  - /proc/PID/environ는 프로세스에 영향을 미치는 환경 변수들의 이름과 값들을 포함한다.
  - /proc/PID/exe, 존재하는 경우 원본 실행 파일에 대한 심볼릭 링크.
  - /proc/PID/fd, 각 열린 [파일 서술자에](../Page/파일_서술자.md "wikilink") 대한 심볼릭 링크를 포함하는 디렉토리.
  - /proc/PID/fdinfo, 각 열린 파일 서술자에 대한 위치와 플래그들을 서술하는 엔트리들을 포함하는 디렉토리.
  - /proc/PID/maps, 매핑된 파일들과 블록들(힙과 스택 같은)에 대한 정보를 포함하는 텍스트 파일.
  - /proc/PID/mem, 프로세스의 [가상 메모리를](../Page/가상_메모리.md "wikilink") 보여주는 바이너리 이미지로서 오직 [ptrace](https://ko.wikipedia.org/wiki/ptrace "wikilink") 하는 프로세스에 의해서만 접근될 수 있다.
  - /proc/PID/root, 프로세스에 의해 보여지는 루트 경로에 대한 심볼릭 링크. 프로세스가 chroot jail에서 실행중이지 않은 이상 대부분의 프로세스들에서 이것은 /에 링크된다.
  - /proc/PID/status는 실행 상태와 메모리 사용을 포함하는 프로세스에 대한 기본 정보들을 갖는다.
  - /proc/PID/task, 이 프로세스에 의해 시작된 작업들에 대한 하드 링크를 포함하는 디렉토리.

[PID는](../Page/프로세스_식별자.md "wikilink") [pgrep](https://ko.wikipedia.org/wiki/pgrep "wikilink"), [pidof](https://ko.wikipedia.org/wiki/pidof "wikilink") 또는 [ps](../Page/Ps_\(유닉스\).md "wikilink") 같은 유틸리티들에 의해서 얻을 수 있다:

``` console
$ ls -l /proc/$(pgrep -n python)/fd        # List all file descriptors of the most recently started `python' process
samtala 0
lrwx------ 1 baldur baldur 64 2011-03-18 12:31 0 -> /dev/pts/3
lrwx------ 1 baldur baldur 64 2011-03-18 12:31 1 -> /dev/pts/3
lrwx------ 1 baldur baldur 64 2011-03-18 12:31 2 -> /dev/pts/3
$ readlink /proc/$(pgrep -n python)/exe    # List executable used to launch the most recently started `python' process
/usr/bin/python3.1
```

2.6 커널에서 대부분의 정보가 /sys에 마운트된 독립된 슈도 파일 시스템인 sysfs로 옮겨졌지만, 이것은 또한 프로세스와 관련 없는 시스템 정보도 포함한다:

  - 전력 관리 모드에 따라 /proc/acpi 또는 /proc/apm, 이것은 sysfs 이전의 것이다.
  - /proc/buddyinfo, 메모리 단편화를 다루는 [버디 알고리즘에](https://ko.wikipedia.org/wiki/버디_알고리즘 "wikilink") 관한 정보.<ref>

</ref>

  - /proc/bus, 컴퓨터의 다양한 버스들을 보여주는 디렉토리들을 포함하며 예를 들면 input/[PCI](../Page/PCI_버스.md "wikilink")/[USB](../Page/USB.md "wikilink")가 있다. 이것의 대부분은 sysfs하에 더 많은 정보를 갖는 /sys/bus로 대체되었다.
  - /proc/fb, 사용 가능한 프레임버퍼들에 관한 목록.
  - /proc/cmdline, 커널에 넘겨지는 부트 옵션.
  - /proc/cpuinfo, 벤더와 스피드, 캐시 크기, sibling의 수, 코어 그리고 [CPU 플래그](../Page/CPUID.md "wikilink") 같은 CPU에 대한 정보를 포함한다.

멀티 코어 CPU에서, /proc/cpuinfo는 다음의 계산이 적용되는 두 필드 "siblings"와 "cpu cores"를 갖는다:\[1\]

`"siblings" = (HT per CPU package) * (# of cores per CPU package)`
`"cpu cores" = (# of cores per CPU package)`

CPU package는 물리적 CPU를 의미하며 여러 코어들을 가질 수 있다. 이것은 [하이퍼스레딩](../Page/하이퍼스레딩.md "wikilink")과 다중 코어 사이에서 구별할 수 있게 해주는데 CPU 패키지에 대한 하이퍼스레드들의 수는 *siblings / CPU cores*에 의해 계산될 수 있다. 만약 CPU 패키지 값들이 같다면, 하이퍼스레딩은 지원되지 않는다.\[2\]

  - /proc/crypto, 사용 가능한 암호화 모듈들에 대한 목록.
  - /proc/devices, 장치 ID에 의해 정렬된 캐릭터와 블록 장치들 뿐만 아니라 /dev 이름에 대한 목록.
  - /proc/diskstats, 논리 디스크 장치들 각각을 위한 몇몇 정보들을 보여준다.
  - /proc/filesystems, 리스팅 시의 커널에 의해 지원되는 파일 시스템들의 목록.
  - /proc/interrupts, /proc/iomem, /proc/ioports 그리고 /proc/irq, 다양한 시스템 자원들을 사용하는 장치들에 관한 자명한 세부 사항들.
  - /proc/meminfo, 커널이 어떻게 자신의 메모리를 관리하는지에 대한 요약을 포함한다.
  - /proc/modules, /proc에서 가장 중요한 파일들 중 하나로서 현재 로드된 커널 모듈들의 리스트를 포함한다. 이것은 의존성에 대한 표시를 준다.
  - /proc/mounts, self/mounts에 대한 심볼릭 링크로서 현재 마운트된 장치들과 그들의 마운트 포인트를 보여준다.
  - /proc/net, 네트워크 스택에 관한 실제로 유용한 정보를 포함하는 디렉토리로서, 특히 존재하는 네트워크 연결을 보여주는 nf_conntrack ([iptables](https://ko.wikipedia.org/wiki/iptables "wikilink") FORWARD가 네트워크 연결들을 리다이렉트할 때 라우팅을 트래킹하는 경우에 유용하다).
  - /proc/partitions, 장치 번호와 이것들의 사이즈 그리고 /dev 이름들에 대한 목록.
  - /proc/scsi, [SCSI](../Page/SCSI.md "wikilink") 또는 [RAID](../Page/RAID.md "wikilink") 컨트롤러를 통해 연결된 장치들에 대한 정보를 보여준다.
  - /proc/self 에서 현재 프로세스에 대한 심볼릭 링크를 보여준다 (즉, [PID](https://ko.wikipedia.org/wiki/PID "wikilink")가 현재 프로세의 것인 곳에서 /proc/PID/).
  - /proc/slabinfo, 리눅스 커널에서 자주 사용되는 객체들의 캐쉬들에 대한 통계를 보여준다.
  - /proc/swaps, 활성화된 스왑 파티션과 이것들의 다양한 크기와 속성들에 대한 목록.
  - /proc/sys 하에서 동적으로 설정 가능한 커널 옵션들에 대한 접근. /proc/sys 아래에는 읽고 쓰기 가능한 가상 파일들을 포함하는 커널의 영역을 표현하는 디렉토리들이 보인다. 예를 들면 주로 참조되는 가상 파일로 /proc/sys/net/ipv4/ip_forward가 있는데, 이것은 방화벽이나 터널들을 라우팅하는데 필요하다. 이 파일은 '1' 또는 '0'을 갖는다: 이것이 1이며, IPv4 스택은 패킷을 포워드하고, 0이면 하지 않는다.
  - /proc/sysvipc, 메모리 공유와 [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink") (IPC) 정보를 포함한다.
  - /proc/tty, 현재 터미널들에 대한 정보를 포함한다.
  - /proc/uptime, 부트 이후에 그리고 유휴 모드에서 보낸 시간.
  - /proc/version, 리눅스 커널 버전, 배포판 번호, [gcc](../Page/GNU_컴파일러_모음.md "wikilink") 버전 번호 그리고 다른 현재 실행중인 커널의 버전과 관련된 다른 정보들을 포함한다.
  - 다른 파일들은 다양한 하드웨어, 모듈 설정 그리고 커널에 대한 변화들에 의존한다.

## 각주

  - [Unix 8th Edition proc(2) manual page](http://man.cat-v.org/unix_8th/4/proc) - 원본 procfs에 대한 설명.
  - [Plan 9 procfs manual page](http://man.cat-v.org/plan_9/3/proc) - procfs 개념을 확장한 플랜 9, 프로세스 제어와 조작에 관한 많은 확장을 제공한다.
  - [Linux Manual Pages Proc(5)](https://web.archive.org/web/20160303182044/http://manpages.courier-mta.org/htmlman5/proc.5.html) procfs에 대한 리눅스 매뉴얼 문서.
  - [Documentation/filesystems/proc.txt](http://kernel.org/doc/Documentation/filesystems/proc.txt) procfs에 대한 리눅스 커널 문서.

## 외부 링크

  - [A brief history of /proc](https://blogs.oracle.com/eschrock/entry/the_power_of_proc) Eric Schrock's Weblog
  - [Access the Linux kernel using the Procfs](http://www.ibm.com/developerworks/library/l-proc.html) An IBM developerWorks article by M. Tim Jones
  - [Linux-Filesystem-Hierarchy](http://tldp.org/LDP/Linux-Filesystem-Hierarchy/html/proc.html) Linux Documentation Project
  - [Discover the possibilities of the /proc directory](https://web.archive.org/web/20130310084458/http://archive09.linux.com/feature/126718) by Federico Kereki

[분류:리눅스 커널의 인터페이스](https://ko.wikipedia.org/wiki/분류:리눅스_커널의_인터페이스 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink")

1.
2.