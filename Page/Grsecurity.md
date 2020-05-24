> This article is converted from Wikipedia: [Grsecurity](https://ko.wikipedia.org/wiki/Grsecurity).


**grsecurity**는 [보안](../Page/컴퓨터_보안.md "wikilink") 강화를 강조한 [리눅스 커널](../Page/리눅스_커널.md "wikilink") [패치들의](../Page/패치_\(컴퓨팅\).md "wikilink") 집합이다.\[1\] 이것은 일반적으로 [웹 서버나](../Page/웹_서버.md "wikilink") 사용자들에게 셸 접근을 제공하는 시스템 같이 신뢰되지 않은 위치에서 원격 접속을 받는 컴퓨터 시스템들에서 사용된다.

## PaX

grsecurity 번들 중에서 주요한 요소는 [PaX](https://ko.wikipedia.org/wiki/PaX "wikilink")이다. 무엇보다도 데이터 메모리, 스택을 실행 불가능하게 또는 쓰기 불가능하게 표시하는 패치를 한다. 목적은 [버퍼 오버플로](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink") 같은 많은 보안 취약점들을 예방하는데 도움을 주는, 메모리의 겹쳐쓰기 방지이다. PaX는 또한 쉽게 예측 가능한 메모리 주소에 의존한 공격들의 가능성을 감소시키기 위해 중요한 메모리 주소를 난수화하는 [주소 공간 배치 난수화](https://ko.wikipedia.org/wiki/주소_공간_배치_난수화 "wikilink") (ASLR)를 제공한다. PaX는 grsecurity 개발자들에 의해 개발되지 않았다. 이것은 젠투 리눅스 등의 리눅스 배포판들에서 사용 가능하다.\[2\]

## 역할 기반 접근 제어

grsecurity의 또 다른 주목할만한 요소로 [역할 기반 접근 제어](../Page/역할_기반_접근_제어.md "wikilink") (RBAC) 시스템의 완전한 제공이 있다. RBAC는 사용자들과 프로세스들이 정확히 동작하고 그 이상의 일을 하지 않게 하기 위한 절대 최소 권한을 갖는 완전한 최소 권한 시스템을 만들기 위한 목적을 위해, 일반적으로 [유닉스](../Page/유닉스.md "wikilink") [접근 제어 목록에](../Page/접근_제어_목록.md "wikilink") 의해 제공되는 것보다 낮은시스템에 대한 접근을 제한하기 위해 고안되었다. 만약 시스템이 감염되면 이 방식은 공격자의 시스템에 대한 정보 획득과 파괴에 대한 능력을 대폭 감소시킬 수 있다. 각 역할은 할 수 있는 것과 없는 것에 대한 각 제한들을 가지며 이러한 역할과 제한들은 필요한 경우 수정될 수 있는 [접근 정책을](https://ko.wikipedia.org/wiki/접근_정책 "wikilink") 형성한다.

RBAC 기능들 목록:

  - 사용자와 그룹을 위한 도메인 지원
  - 역할 변환 테이블
  - [IP](../Page/인터넷_프로토콜.md "wikilink")-기반 역할들
  - 특별한 규칙에 대한 비-[root](../Page/슈퍼유저.md "wikilink") 접근
  - 인증을 요구하지 않는 특별한 역할들
  - 중첩된 주체
  - 설정에서 [변수들에](https://ko.wikipedia.org/wiki/변수_\(컴퓨터_과학\) "wikilink") 대한 지원
  - 설정에서 변수들에 대한 And, or, 그리고 difference 집합 연산자들
  - [setuid](https://ko.wikipedia.org/wiki/setuid "wikilink") 그리고 [setgid](https://ko.wikipedia.org/wiki/setgid "wikilink") 파일들의 생성을 제어하는 객체 모드
  - 객체 모드들의 생성과 삭제
  - 상속된 것의 [커널](../Page/커널_\(컴퓨팅\).md "wikilink") 해석
  - 실시간 [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 해결
  - 특정한 프로세스들에 대한 [ptrace](https://ko.wikipedia.org/wiki/ptrace "wikilink") 거부 능력
  - 사용자와 그룹 변환 검사
  - 커널 인증과 로그 학습을 위한 /dev/grsec 엔트리
  - 설정 없이 전체 시스템을 위한 최소 권한 정책을 생성하는 코드
  - gradm에 대한 정책 통계
  - 상속 기반 학습
  - 관리자의 상속 기반 학습을 활성화시키는 설정 파일 학습
  - 부모 또는 문제가 되는 프로세스의 전체 경로 이름
  - gradm을 위한 RBAC 상태 함수
  - 주어진 프로세스를 시작한 개인의 원격 주소를 주는 /proc/<pid>/ipaddr
  - 안전한 정책 강화
  - read, write, append, execute, view, 그리고 read-only ptrace 객체 허용 지원
  - hide, protect, 그리고 subject flags 겹쳐쓰기 지원
  - PaX flags 지원
  - 공유 메모리 보호 기능
  - 모든 알림에 대응하는 통합된 로컬 공격 대응
  - 프로세스가 절대 트로이 코드를 실행할 수 없게 보장하는 Subject flag
  - 완전한 기능의 감사
  - Resource, socket, 그리고 capability 지원
  - 무차별 대입 공격 익스플로잇에 대한 보호
  - /proc/pid filedescriptor/memory 보호
  - 존재하지 않는 파일/프로세스들에 대한 규칙들
  - 주체와 객체들에 대한 정책 재생성
  - 설정 가능한 로그 제거
  - 설정 가능한 프로세스 설명
  - 사람이 읽을 수 있는 설정
  - 파일 시스템 또는 아키텍처에 의존하지 않는 특징
  - 넓은 범위: 메모리가 다룰 수 있는 만큼의 많은 정책들을 지원
  - 런타임 메모리 할당 거부
  - [SMP](https://ko.wikipedia.org/wiki/대칭형_다중_처리 "wikilink") 안전
  - 대부분의 연산들에 대한 O(1) 시간 효율성
  - 추가적인 정책들을 명시하는 지시자 포함
  - Enable, disable, reload 능력
  - 커널 프로세스를 숨기는 선택지

## Chroot 제한

grsecurity는 여러 취약점들과 [권한 확대](../Page/권한_확대.md "wikilink") 공격들을 예방하기 위해 다양한 방식으로 [chroot](https://ko.wikipedia.org/wiki/chroot "wikilink")를 제한한다. 다음은 추가적인 검사이다:

  - chroot 외부의 [공유 메모리에](../Page/공유_메모리.md "wikilink") 대한 어태치 금지
  - chroot 외부의 [`kill`](https://ko.wikipedia.org/wiki/kill "wikilink"), `ptrace` (architecture-independent), `capget`, `setpgid`, `getpgid` 그리고 `getsid` 금지
  - chroot 외부의 `fcntl`에 의한 시그널 보내기 금지
  - chroot 외부의 프로세스 보기 금지, 심지어 이 마운트되었더라도
  - [마운트](https://ko.wikipedia.org/wiki/마운트 "wikilink") 또는 재 마운트 금지
  - `pivot_root` 금지
  - 더블 chroot 금지
  - chroot 외부의 `fchdir` 금지
  - chroot에 대한 강제된 [`chdir`](https://ko.wikipedia.org/wiki/chdir "wikilink")`("/")`
  - `(f)`[`chmod`](https://ko.wikipedia.org/wiki/chmod "wikilink")`  +s ` 금지
  - [`mknod`](https://ko.wikipedia.org/wiki/mknod "wikilink") 금지
  - [`sysctl`](https://ko.wikipedia.org/wiki/sysctl "wikilink") 쓰기 금지
  - 스케줄 우선 순위에 대한 상승 금지
  - chroot 외부의 추상적인 유닉스 도메인 소켓 연결 금지
  - cap을 통한 위험한 권한 제거

## 기타 기능

grsecurity는 또한 리눅스 커널에 대한 강화된 [감사](../Page/감사.md "wikilink")를 제공한다. 무엇보다도 사용자, 장치들의 [마운팅](../Page/Mount_\(유닉스\).md "wikilink")/언마운팅, 시스템 시간과 데이터에 대한 변화, 그리고 [`chdir`](https://ko.wikipedia.org/wiki/작업_디렉터리 "wikilink") 로깅이라는 특정한 그룹을 감사하기 위한 방식으로 설정될 수 있다. 다른 감사 타입들 중 몇몇은  거부된 자원 시도, 실패한 [`fork`](../Page/포크_\(시스템_호출\).md "wikilink") 시도와 [IPC](../Page/프로세스_간_통신.md "wikilink") 생성, 삭제 그리고 `exec` 로깅을 관리자가 인자들과 함께 기록할 수 있게 한다.

신뢰된 경로 실행은 사용자가 [root](../Page/슈퍼유저.md "wikilink") 사용자에 의해 소유되지 않은 바이너리를 실행하는 것을 예방하는데 사용되는 선택적인 기능이다. 이것은 사용자들로부터 자신의 악의적인 바이너리를 실행하는 것으로부터 그리고 실수로 악의적인 사용자에 의해 수정된 시스템 바이너리를 실행하는 것으로부터 방어한다.

grsecurity는 또한 chroot "jails"의 작동을 강화한다. chroot jail은 특정한 프로세스를 시스템의 나머지로부터 고립시키는데 사용될 수 있어서 서비스가 감염되었을 때 피해를 최소화시킬 수 있다. grsecurity가 방어하려고 하는 chroot jail의 탈출에 관한 여러 방식들이 존재한다.

또한 보안을 강화시키고 root 사용자에 대한 [`dmesg`](https://ko.wikipedia.org/wiki/dmesg "wikilink") 와 [`netstat`](https://ko.wikipedia.org/wiki/netstat "wikilink") 명령어를 제한하는 것 같이 사용자가 시스템에 관한 불필요한 정보를 얻는 것을 막는 기능들도 존재한다.\[3\]

다음은 추가적인 기능들과 보안 개선 사항들이다:

  - 프로세스 소유자들에 대한 정보 누수를 막는 `/proc` 제한
  - [`/tmp` 레이스를](https://ko.wikipedia.org/wiki/심볼릭_레이스 "wikilink") 막는 심볼릭링크/하드링크 제한
  - [FIFO](../Page/선입_선출.md "wikilink") 제한
  - `dmesg` 제한
  - 신뢰하는 경로 실행의 구현 강화
  - [GID](https://ko.wikipedia.org/wiki/그룹_식별자_\(유닉스\) "wikilink")-기반 소켓 제한
  - 로킹 메커니즘과 함께 거의 모든 옵션들이 [`sysctl`](https://ko.wikipedia.org/wiki/sysctl "wikilink")-조정 가능하다.
  - 모든 알림과 감사가 공격자의 IP 주소를 기록하는 기능을 지원한다.
  - 로컬 연결들의 탐지: 공격자의 IP 주소를 다른 태스크로 복사한다.
  - [무차별 대입 공격](https://ko.wikipedia.org/wiki/무차별_대입_공격 "wikilink") 익스플로잇의 자동적인 저지
  - Low, medium, high, 그리고 custom 보안 수준
  - 조정 가능한 로깅

## 같이 보기

  - [Exec Shield](../Page/Exec_Shield.md "wikilink")
  - [리눅스 보안 모듈](../Page/리눅스_보안_모듈.md "wikilink")
  - [보안 강화 리눅스](../Page/보안_강화_리눅스.md "wikilink")

## 각주

## 외부 링크

  -
  - [Academic Research Publications Mentioning grsecurity/PaX](https://grsecurity.net/research.php)

  -
[분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink") [분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink")

1.
2.
3.